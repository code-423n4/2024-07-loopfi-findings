# QA Report

## Low Risk 
| Id | Title |
|:--:|:-------|
| [L-01] | The liquidationPenalty should be the penalty percentage, instead of the non-penalty percentage. |
| [L-02] | The preview functions of PoolV3 does not take pause and lock status into account. |
| [L-03] | The PoolV3 maxWithdraw/maxRedeem functions does not take lock status into account. |
| [L-04] | supplyRate() of PoolV3 should take quotaRevenue into account. |
| [L-05] | No method to remove a credit manager in PoolV3 |
| [L-06] | In StakingLPEth, the cooldown time always updates to the last cooldown action |
| [L-07] | VaultRegistry.sol may run out of gas when trying to remove a vault. |
| [L-08] | BalancerOracle and PendleOracle can only be upgraded if the current oracle is down. |
| [L-09] | PendleOracle still uses answeredInRound, but it is deprecated for Chainlink Aggregator. |
| [L-10] | PoolAction and SwapAction contraints the Pendle LP token seller to be the same as token recipient. |
| [L-11] | Code comment is incorrect for `PositionAction4626._onIncreaseLever` |
| [L-12] | ChefIncentivesController.claim() does not update price before checking eligibility |
| [L-13] | ChefIncentivesController `_updateEmissions()` function should be made public and called periodically |
| [L-14] | EligibilityDataProvider#lastEligibleTime() should multiply `priceToleranceRatio` when calculating eligiblity. |
| [L-15] | `EligibilityDataProvider#_lockedUsdValue()` does not check for validity nor staleness |
| [L-16] | `isRewardToken[rdntToken]` is not set to True for MultiFeeDistribution. |
| [L-17] | `mintersAreSet` is not checked when calling `setMinters`, and minters can be added multiple times. |
| [L-18] | No method to remove a minter |
| [L-19] | MultiFeeDistribution `_notifyUnseenReward()` function should be made public and called periodically |
| [L-20] | lastClaimTime is not updated during `MultiFeeDistribution#_getReward` |
| [L-21] | `MultiFeeDistribution#_getReward` does not have to call `setEligibilityExempt()` |
| [L-22] | PositionAction20/PositionAction4626/PositionActionPendle onWithdraw don't use correct token scale |

## [L-01] The liquidationPenalty should be the penalty percentage, instead of the non-penalty percentage.

### Bug Description

The liquidationPenalty should be the penalty percentage, instead of the non-penalty percentage. It should be `uint256 penalty = wmul(repayAmount, liqConfig_.liquidationPenalty);`.

```solidity
>       uint256 deltaDebt = wmul(repayAmount, liqConfig_.liquidationPenalty);
>       uint256 penalty = wmul(repayAmount, WAD - liqConfig_.liquidationPenalty);
        if (takeCollateral > position.collateral) revert CDPVault__tooHighRepayAmount();
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L530C1-L532C89

## [L-02] The preview functions of PoolV3 does not take pause and lock status into account.

### Bug Description

When the contract is paused, previewDeposit/previewMint/previewWithdraw/previewRedeem should all be zero.

When the contract is locked, users can't call withdraw/redeem (except for whitelisted users), but they can call deposit/mint. The preview functions should also update accordingly.

```solidity
    /// @notice Number of pool shares that would be minted on depositing `assets`
    function previewDeposit(uint256 assets) public view override(ERC4626, IERC4626) returns (uint256 shares) {
        shares = _convertToShares(_amountMinusFee(assets)); // U:[LP-10]
    }

    /// @notice Amount of underlying that would be spent to mint `shares`
    function previewMint(uint256 shares) public view override(ERC4626, IERC4626) returns (uint256) {
        return _amountWithFee(_convertToAssets(shares)); // U:[LP-10]
    }

    /// @notice Number of pool shares that would be burned on withdrawing `assets`
    function previewWithdraw(uint256 assets) public view override(ERC4626, IERC4626) returns (uint256) {
        return _convertToShares(_amountWithWithdrawalFee(_amountWithFee(assets))); // U:[LP-10]
    }

    /// @notice Amount of underlying that would be received after redeeming `shares`
    function previewRedeem(uint256 shares) public view override(ERC4626, IERC4626) returns (uint256) {
        return _amountMinusFee(_amountMinusWithdrawalFee(_convertToAssets(shares))); // U:[LP-10]
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L335-L353


## [L-03] The PoolV3 maxWithdraw/maxRedeem functions does not take lock status into account.

### Bug Description

When the contract is locked, users can't call withdraw/redeem (except for whitelisted users). The maxWithdraw/maxRedeem functions should also update accordingly.

```solidity
    modifier whenNotLocked() {
        if (_allowed[msg.sender]) {
            _;
        } else {
            _revertIfLocked();
            _;
        }
    }

    function withdraw(
        uint256 assets,
        address receiver,
        address owner
    )
        public
        override(ERC4626, IERC4626)
        whenNotPaused // U:[LP-2A]
>       whenNotLocked
        nonReentrant // U:[LP-2B]
        nonZeroAddress(receiver) // U:[LP-5]
        returns (uint256 shares)
    {
        uint256 assetsToUser = _amountWithFee(assets);
        uint256 assetsSent = _amountWithWithdrawalFee(assetsToUser); // U:[LP-8]
        shares = _convertToShares(assetsSent); // U:[LP-8]
        _withdraw(receiver, owner, assetsSent, assets, assetsToUser, shares); // U:[LP-8]
    }

    function redeem(
        uint256 shares,
        address receiver,
        address owner
    )
        public
        override(ERC4626, IERC4626)
        whenNotPaused // U:[LP-2A]
>       whenNotLocked
        nonReentrant // U:[LP-2B]
        nonZeroAddress(receiver) // U:[LP-5]
        returns (uint256 assets)
    {
        uint256 assetsSent = _convertToAssets(shares); // U:[LP-9]
        uint256 assetsToUser = _amountMinusWithdrawalFee(assetsSent);
        assets = _amountMinusFee(assetsToUser); // U:[LP-9]
        _withdraw(receiver, owner, assetsSent, assets, assetsToUser, shares); // U:[LP-9]
    }

    function maxWithdraw(address owner) public view override(ERC4626, IERC4626) returns (uint256) {
        return
            paused()
                ? 0
                : _amountMinusFee(
                    _amountMinusWithdrawalFee(Math.min(availableLiquidity(), _convertToAssets(balanceOf(owner))))
                ); // U:[LP-11]
    }

    /// @notice Maximum number of shares that can be redeemed for underlying by `owner`, 0 if pool is on pause
    function maxRedeem(address owner) public view override(ERC4626, IERC4626) returns (uint256) {
        return paused() ? 0 : Math.min(balanceOf(owner), _convertToShares(availableLiquidity())); // U:[LP-11]
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L366-L378

## [L-04] supplyRate() of PoolV3 should take quotaRevenue into account.

### Bug Description

When calculating supplyRate, it uses the annual interest to divide the total amount of lpETH. However, it only calculates base interest, and does not calculate quota interest. quotaRevenue should be added as well.

```solidity
    function supplyRate() external view override returns (uint256) {
        uint256 assets = expectedLiquidity();
        uint256 baseInterestRate_ = baseInterestRate();
        if (assets == 0) return baseInterestRate_;
        return
            ((baseInterestRate_ * _totalDebt.borrowed) * (PERCENTAGE_FACTOR - withdrawFee)) /
            PERCENTAGE_FACTOR /
            assets; // U:[LP-15]
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L603C1-L611C6

## [L-05] No method to remove a credit manager in PoolV3

### Bug Description

In PoolV3, admins can add a new credit manager, but they can't remove an existing credit manager.

```solidity
    function setCreditManagerDebtLimit(
        address creditManager,
        uint256 newLimit
    )
        external
        override
        controllerOnly // U:[LP-2C]
        nonZeroAddress(creditManager) // U:[LP-25A]
    {
        if (!_creditManagerSet.contains(creditManager)) {
            if (address(this) != ICreditManagerV3(creditManager).pool()) {
                revert IncompatibleCreditManagerException(); // U:[LP-25C]
            }
            _creditManagerSet.add(creditManager); // U:[LP-25D]
            emit AddCreditManager(creditManager); // U:[LP-25D]
        }
        _creditManagerDebt[creditManager].limit = _convertToU128(newLimit); // U:[LP-25D]
        emit SetCreditManagerDebtLimit(creditManager, newLimit); // U:[LP-25D]
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L797C1-L815C6

## [L-06] In StakingLPEth, the cooldown time always updates to the last cooldown action

### Bug Description

Say there are two calls to `cooldownAssets()`, one at T0, and second at T1. If T0+cooldownDuration > T1, then users can only unstake the assets in the first call at T1+cooldownDuration. This means users would need to wait another T1-T0.

```solidity
    function cooldownAssets(uint256 assets) external ensureCooldownOn returns (uint256 shares) {
        if (assets > maxWithdraw(msg.sender)) revert ExcessiveWithdrawAmount();

        shares = previewWithdraw(assets);

>       cooldowns[msg.sender].cooldownEnd = uint104(block.timestamp) + cooldownDuration;
        cooldowns[msg.sender].underlyingAmount += uint152(assets);

        _withdraw(msg.sender, address(silo), msg.sender, assets, shares);
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L797C1-L815C6

## [L-07] VaultRegistry.sol may run out of gas when trying to remove a vault.

### Bug Description

The removal of a vault is an O(n) implementation, while it could be an O(1) if it use the EnumerableSet.AddressSet.

```solidity
    function _removeVaultFromList(ICDPVault vault) private {
        uint256 vaultLen = vaultList.length;
        for (uint256 i = 0; i < vaultLen; ) {
            if (vaultList[i] == vault) {
                vaultList[i] = vaultList[vaultLen - 1];
                vaultList.pop();
                break;
            }

            unchecked {
                ++i;
            }
        }
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/VaultRegistry.sol#L80C1-L93C6

## [L-08] BalancerOracle and PendleOracle can only be upgraded if the current oracle is down.

### Bug Description

If oracles can only upgraded if they are down, this means there must be a time period that the oracle is down. This is unexpected, and it is best to upgrade before the downtime happens.

Oracles should be able to be upgraded even if they are up, not only to fix live issues, but to prevent future issues.

```solidity
    function _authorizeUpgrade(address /*implementation*/) internal override virtual onlyRole(MANAGER_ROLE){
>       if(_getStatus()) revert PendleLPOracle__authorizeUpgrade_validStatus();
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/oracle/PendleLPOracle.sol#L84-L86
- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/oracle/BalancerOracle.sol#L110-L112

## [L-09] PendleOracle still uses answeredInRound, but it is deprecated for Chainlink Aggregator.

### Bug Description

According to https://docs.chain.link/data-feeds/api-reference, answeredInRound is already deprecated, and can be removed.

```solidity
    function _fetchAndValidate() internal view returns (bool isValid, uint256 price) {
        try AggregatorV3Interface(aggregator).latestRoundData() returns (
            uint80 roundId, int256 answer, uint256 /*startedAt*/, uint256 updatedAt, uint80 answeredInRound
        ) {
>           isValid = (answer > 0 && answeredInRound >= roundId && block.timestamp - updatedAt <= stalePeriod);
            return (isValid, wdiv(uint256(answer), aggregatorScale));
        } catch {
            // return the default values (false, 0) on failure
        }
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/oracle/PendleLPOracle.sol#L116C1-L125C6


## [L-10] PoolAction and SwapAction contraints the Pendle LP token seller to be the same as token recipient.

### Bug Description

When exiting the Pendle LP Token, both PoolAction and SwapAction forces the seller to be the same as the outToken recipient. However, this may not be the case, and limits the use case of the protocol.

PoolAction.sol
```solidity
    function _pendleExit(PoolActionParams memory poolActionParams) internal returns (uint256 retAmount){
        ...
        if(poolActionParams.recipient != address(this)){
>           IPMarket(market).transferFrom(poolActionParams.recipient, market, netLpIn);
        } else {
            IPMarket(market).transfer(market, netLpIn);
        }
    }
```

```solidity
    function pendleExit(address recipient, uint256 minOut, bytes memory data) internal returns (uint256 retAmount){
        ...
        if(recipient != address(this)){
>           IPMarket(market).transferFrom(recipient, market, netLpIn);
        } else {
            IPMarket(market).transfer(market, netLpIn);
        }
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/SwapAction.sol#L358
- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PoolAction.sol#L286


## [L-11] Code comment is incorrect for `PositionAction4626._onIncreaseLever`

### Bug Description

This has nothing to do with the Yearn vault. It should be the CDPVault instead.

```solidity
>   /// @notice Hook to decrease lever by depositing collateral into the Yearn Vault and the Yearn Vault
    /// @param leverParams LeverParams struct
    /// @param upFrontToken the token passed up front
    /// @param upFrontAmount the amount of tokens passed up front [IYVault.decimals()]
    /// @param swapAmountOut the amount of tokens received from the stablecoin flash loan swap [IYVault.decimals()]
    /// @return Amount of collateral added to CDPVault position [wad]
    function _onIncreaseLever(
        LeverParams memory leverParams,
        address upFrontToken,
        uint256 upFrontAmount,
        uint256 swapAmountOut
    ) internal override returns (uint256)
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction4626.sol#L73


## [L-12] ChefIncentivesController.claim() does not update price before checking eligibility

### Bug Description

The eligibility of claiming LOOP rewards is related to the oracle price of the borrowed debt and lpETH-LOOP LP. `eligibleDataProvider.updatePrice();` should be called before claiming to make sure the price is up to date, since `eligibleDataProvider.isEligibleForRewards()` does not update the price.

```solidity
    function claim(address _user, address[] memory _tokens) public whenNotPaused {
        ...
        if (eligibilityMode != EligibilityModes.DISABLED) {
            if (!eligibleDataProvider.isEligibleForRewards(_user)) revert EligibleRequired();
            checkAndProcessEligibility(_user, true, true);
        }
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/ChefIncentivesController.sol#L518-L522



## [L-13] ChefIncentivesController `_updateEmissions()` function should be made public and called periodically

### Bug Description

`_updateEmissions()` function is to update the reward emission rate according to the latest schedule. It is currently called inside the `claim` function. But it should be public and callable by anyone. Admins should call it periodically to make sure the emission rate is always up-to-date, even if no one is calling the `claim` function.

```solidity
    function _updateEmissions() internal {
        if (block.timestamp > endRewardTime()) {
            _massUpdatePools();
            lastRPS = rewardsPerSecond;
            rewardsPerSecond = 0;
            return;
        }
        setScheduledRewardsPerSecond();
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/ChefIncentivesController.sol#L439




## [L-14] EligibilityDataProvider#lastEligibleTime() should multiply `priceToleranceRatio` when calculating eligiblity.

### Bug Description

The `priceToleranceRatio` is used to add a price tolerance. It is used when calculating `isEligibleForRewards()` in the system. But for the function `lastEligibleTime()`, it is not used.

This is a low severity issue because `lastEligibleTime()` is a view function that is not used anywhere.

```solidity
    function lastEligibleTime(address user) public view returns (uint256 lastEligibleTimestamp) {
        if (!isEligibleForRewards(user)) {
            return 0;
        }

>       uint256 requiredValue = requiredUsdValue(user);

        LockedBalance[] memory lpLockData = IMultiFeeDistribution(multiFeeDistribution).lockInfo(user);

        uint256 lockedLP;
        for (uint256 i = lpLockData.length; i > 0; ) {
            LockedBalance memory currentLockData = lpLockData[i - 1];
            lockedLP += currentLockData.amount;

            if (_lockedUsdValue(lockedLP) >= requiredValue) {
                return currentLockData.unlockTime;
            }
            unchecked {
                i--;
            }
        }
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/EligibilityDataProvider.sol#L225




## [L-15] `EligibilityDataProvider#_lockedUsdValue()` does not check for validity nor staleness

### Bug Description

With no information of how `priceProvider.getLpTokenPriceUsd()` is implemented, the oracle result should be checked with staleness and validity (e.g. it should be larger than 0).

```solidity
    function _lockedUsdValue(uint256 lockedLP) internal view returns (uint256) {
>       uint256 lpPrice = priceProvider.getLpTokenPriceUsd();
        return (lockedLP * lpPrice) / 10 ** 18;
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/EligibilityDataProvider.sol#L274C1-L277C6




## [L-16] `isRewardToken[rdntToken]` is not set to True for MultiFeeDistribution.

### Bug Description

In the initialize function of `MultiFeeDistribution`, rdntToken is set as reward token. However, `isRewardToken[rdntToken]` is not set to True.

```solidity
    function initialize(
        ...
    ) public initializer {
        ...

        rdntToken = IMintableToken(rdntToken_);
        _lockZap = lockZap_;
        daoTreasury = dao_;
        _priceProvider = priceProvider_;
        rewardTokens.push(rdntToken_);
        rewardData[rdntToken_].lastUpdateTime = block.timestamp;

        rewardsDuration = rewardsDuration_;
        rewardsLookback = rewardsLookback_;
        defaultLockDuration = lockDuration_;
        burn = burnRatio_;
        vestDuration = vestDuration_;
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/MultiFeeDistribution.sol#L250-L251





## [L-17] `mintersAreSet` is not checked when calling `setMinters`, and minters can be added multiple times.

### Bug Description

`mintersAreSet` is not checked when calling `setMinters`. This means minters can be added multiple times.

```solidity
    /// @notice Flag to prevent more minter addings
    bool public mintersAreSet;

    /**
     * @notice Set minters
     * @param minters_ array of address
     */
    function setMinters(address[] calldata minters_) external onlyOwner {
        uint256 length = minters_.length;
        for (uint256 i; i < length; ) {
            if (minters_[i] == address(0)) revert AddressZero();
            minters[minters_[i]] = true;
            unchecked {
                i++;
            }
        }
        mintersAreSet = true;
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/MultiFeeDistribution.sol#L266-L276





## [L-18] No method to remove a minter

### Bug Description

Admin can use `setMinters()` to add minters, but there is no method to remove minters.

```solidity
    function setMinters(address[] calldata minters_) external onlyOwner {
        uint256 length = minters_.length;
        for (uint256 i; i < length; ) {
            if (minters_[i] == address(0)) revert AddressZero();
            minters[minters_[i]] = true;
            unchecked {
                i++;
            }
        }
        mintersAreSet = true;
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/MultiFeeDistribution.sol#L266-L276



## [L-19] MultiFeeDistribution `_notifyUnseenReward()` function should be made public and called periodically

### Bug Description

`_notifyUnseenReward()` function is to update the latest rewards. It is currently called inside the `_getReward` function. But it should be public and callable by anyone. Admins should call it periodically to make sure the rewards are always distributed up-to-date, even no one is claiming the reawrds.

```solidity
    function _notifyUnseenReward(address token) internal {
        if (token == address(0)) revert AddressZero();
        if (token == address(rdntToken)) {
            return;
        }
        Reward storage r = rewardData[token];
        uint256 periodFinish = r.periodFinish;
        if (periodFinish == 0) revert InvalidPeriod();
        if (periodFinish < block.timestamp + rewardsDuration - rewardsLookback) {
            uint256 unseen = IERC20(token).balanceOf(address(this)) - r.balance;
            if (unseen > 0) {
                _notifyReward(token, unseen);
            }
        }
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/MultiFeeDistribution.sol#L1223





## [L-20] lastClaimTime is not updated during `MultiFeeDistribution#_getReward`

### Bug Description

When users call `getReward()` to get rewards, the lastClaimTime[] for user is not updated. It should be updated in the `_getReward` function.

```solidity
    /// @notice Last claim time of the user
    mapping(address => uint256) public lastClaimTime;

    function getReward(address[] memory rewardTokens_) public {
        _updateReward(msg.sender);
        _getReward(msg.sender, rewardTokens_);
        IPriceProvider(_priceProvider).update();
    }

    function _getReward(address user, address[] memory rewardTokens_) internal whenNotPaused {
        uint256 length = rewardTokens_.length;
        IChefIncentivesController chefIncentivesController = incentivesController;
        chefIncentivesController.setEligibilityExempt(user, true);
        for (uint256 i; i < length; ) {
            address token = rewardTokens_[i];
            _notifyUnseenReward(token);
            uint256 reward = rewards[user][token] / 1e12;
            if (reward > 0) {
                rewards[user][token] = 0;
                rewardData[token].balance = rewardData[token].balance - reward;

                IERC20(token).safeTransfer(user, reward);
                emit RewardPaid(user, token, reward);
            }
            unchecked {
                i++;
            }
        }
        chefIncentivesController.setEligibilityExempt(user, false);
        chefIncentivesController.afterLockUpdate(user);
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/MultiFeeDistribution.sol#L1244

## [L-21] `MultiFeeDistribution#_getReward` does not have to call `setEligibilityExempt()`

### Bug Description

Eligibility would not be changed by user claiming rewards, so it is useless to call `chefIncentivesController.setEligibilityExempt()`.

```solidity
    function _getReward(address user, address[] memory rewardTokens_) internal whenNotPaused {
        uint256 length = rewardTokens_.length;
        IChefIncentivesController chefIncentivesController = incentivesController;
>       chefIncentivesController.setEligibilityExempt(user, true);
        for (uint256 i; i < length; ) {
            address token = rewardTokens_[i];
            _notifyUnseenReward(token);
            uint256 reward = rewards[user][token] / 1e12;
            if (reward > 0) {
                rewards[user][token] = 0;
                rewardData[token].balance = rewardData[token].balance - reward;

                IERC20(token).safeTransfer(user, reward);
                emit RewardPaid(user, token, reward);
            }
            unchecked {
                i++;
            }
        }
>       chefIncentivesController.setEligibilityExempt(user, false);
        chefIncentivesController.afterLockUpdate(user);
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/MultiFeeDistribution.sol#L1244




## [L-22] PositionAction20/PositionAction4626/PositionActionPendle onWithdraw don't use correct token scale

### Bug Description

The token scale is incorrect for all `onWithdraw()` functions. The scale used for `CDPVault.withdraw(position, amount)` should be tokenScale, and the return value is WAD.

However, all use cases got them reversed, and they assume `CDPVault.withdraw(position, amount)` should be WAD, and the return value is tokenScale.

This would be an issue if tokenScale != 1e18.

PositionAction20.sol
```solidity
    /// @param amount Amount of collateral to withdraw [wad]
    /// @return Amount of collateral withdrawn [CDPVault.tokenScale()]
    function _onWithdraw(address vault, address position, address /*dst*/, uint256 amount) internal override returns (uint256) {
        return ICDPVault(vault).withdraw(position, amount);
    }
```

PositionAction4626.sol
```solidity
    /// @param amount Amount of collateral to withdraw [wad]
    /// @return Amount of collateral withdrawn [CDPVault.tokenScale()]
    function _onWithdraw(address vault, address /*position*/, address dst, uint256 amount) internal override returns (uint256) {
        uint256 collateralWithdrawn = ICDPVault(vault).withdraw(address(this), amount);

        // if collateral is not the dst token, we need to withdraw the underlying from the ERC4626 vault
        address collateral = address(ICDPVault(vault).token());
        if (dst != collateral) {
            collateralWithdrawn = IERC4626(collateral).redeem(collateralWithdrawn, address(this), address(this));
        }

        return collateralWithdrawn;
    }
```

```solidity
    /// @param amount Amount of collateral to withdraw [wad]
    /// @return Amount of collateral withdrawn [CDPVault.tokenScale()]
    function _onWithdraw(address vault, address position, address /*dst*/, uint256 amount) internal override returns (uint256) {
        return ICDPVault(vault).withdraw(address(position), amount);
    }
```

### Code Snippet

- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionActionPendle.sol#L45
- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction4626.sol#L61
- https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction20.sol#L50



