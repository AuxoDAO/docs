---
description: This page compares the ARV and PRV Vaults for the AUXO protocol
---

# ARV vs PRV

## Rundown

### **ARV Target Profile**

* Users interested in active participation within DAO governance.
* Participants with longer time preferences - users looking for shorter horizons should consider Auxo Passive Rewards Vault (PRV).
* Stakers looking to absolutely maximise rewards.

### PRV **Target Profile**

* DAO members with no interest in direct governance seeking a passive approach.
* Participants who are happy with either exiting via secondary markets or via the  [#redemption-mechanics](../../rewards-vaults/prv-passive-rewards-vault/#redemption-mechanics "mention") described below.
* Users who are concerned about minimizing both the gas expenditures and effort required to maintain a fully maximized rewards position.

## Table of comparison

<table><thead><tr><th width="166">-</th><th width="294.3333333333333">ARV</th><th>PRV</th></tr></thead><tbody><tr><td>Rewards</td><td>70% Total</td><td>30% Total</td></tr><tr><td>Boosting</td><td>Required to maintain max rewards</td><td>Not required</td></tr><tr><td>Governance</td><td>Mandatory Participation</td><td>Cannot Vote</td></tr><tr><td>Transfer</td><td>Non transferable</td><td>Transferable</td></tr><tr><td>Lock</td><td>6 - 36 months</td><td>Based on NAV/Withdrawal Queue</td></tr><tr><td>Redemption</td><td>Right to burn at lock expiry and redeem from the redemption pool.</td><td>Based on NAV/Withdrawal Queue</td></tr><tr><td>Withdrawal Fee</td><td>NO</td><td>1%</td></tr><tr><td>Exit</td><td>Wait for unlock or migrate to PRV with a 20% penalty</td><td>Redeem for Auxo when available or sell in secondary markets</td></tr></tbody></table>

{% hint style="warning" %}
Note that, in addition to the time required to participate in ARV, there will be additional gas fees required to maintain a stake and vote. Users concerned about gas fees should consider PRV instead.
{% endhint %}

## The Difference in Rewards

Every month the DAO Treasury will distribute rewards to ARV and PRV stakers that come from the Treasury Farming operations.

* 70% of farmed rewards will accrue to ARV
* 30% of farmed rewards will accrue to PRV

On the surface then - ARV would appear to yield substantially higher than PRV.

**But this may not always be the case.**

As a staker, you should be aware of some of the different reward scenarios, and contrast them with your own investment horizons and risk profile. Below are some examples to help illustrate different scenarios and reward payouts per token.

{% hint style="info" %}
**Boring Disclaimer:** the examples here are illustrative, to give you a feel of the underlying concepts that drive reward differences. Don’t read these as advice of what to stake in, you need to make that call for yourself.
{% endhint %}

### Case 1 - More ARV than PRV

_In this example, we have more ARV holders than PRV._

Let's say 1000 WETH is distributed to stakers:

* There are 1000 ARV tokens and 200 PRV tokens across all stakers.
* All holders are eligible for max rewards:
  * All ARV holders are maximally boosted and have voted
  * All PRV users are staked for the full epoch

#### **Rewards Breakdown**

<table><thead><tr><th width="134">Token</th><th width="155">Total Rewards</th><th width="112">Supply</th><th>Payout/token</th></tr></thead><tbody><tr><td>ARV</td><td>700</td><td>1000</td><td>700 / 1000 = 0.7</td></tr><tr><td>PRV</td><td>300</td><td>200</td><td>300 / 200 = 1.5</td></tr></tbody></table>

In this case it may be better to stake into PRV until such time as positions favor ARV. Existing ARV stakers may wish to take advantage of the “Early Termination” mechanic from ARV → PRV.

#### **How to check**

ARV and PRV are ERC20 contracts. The “Total Supply” of each are available on block explorers or via the smart contracts.

### Case 2 Inactive ARV Stakers

_In this example, we can see a high number of ARV holders are inactive, meaning rewards are allocated between less stakers._

Same setup as case 1: 1000 WETH, 1000 ARV, 200 PRV

* In this case however, let’s say 60% of ARV tokens are held by stakers who habitually do not vote - either they forget, lose access to their wallet or have decided not to.
* Rewards that would otherwise accrue to these stakers are redistributed to existing ARV stakers.\*

#### **Rewards Breakdown**

<table><thead><tr><th width="111">Token</th><th width="148">Total Rewards</th><th width="102">Supply</th><th width="149">Active Supply</th><th>Payout/token</th></tr></thead><tbody><tr><td>ARV</td><td>700</td><td>1000</td><td>400</td><td>700 / 400 = 1.75</td></tr><tr><td>PRV</td><td>300</td><td>200</td><td>200</td><td>300 / 200 = 1.5</td></tr></tbody></table>

In this case, ARV for active stakers will be yielding more rewards per token. If as a user you are committed to voting and a long-term commitment, your rewards would likely be maximized by staking in ARV.

#### **How to check**

Votes will be conducted in public - you can check Tally and Snapshot for on-chain and offchain vote participation, relative to the total supply of ARV.

* _This is not the same for PRV: rewards for inactive PRV stakers will not necessarily be redistributed._

### Case 3 - Non-Boosted ARV

_In this example, we can see the average boost for ARV stakers is low, meaning extra rewards will accrue to fully boosted stakers._

Same setup as case 1: 1000 WETH, 1000 ARV, 200 PRV

* In this case however, let’s say the average boost level is 21 across all ARV stakers. This means most stakers receive just under 50% of the rewards for a fully boosted staker.
* Rewards that would otherwise accrue to these stakers are redistributed to higher boosted stakers, proportional to their boosted balance.

A user who is committed to voting and boosting, therefore, will receive additional rewards each epoch, redistributed from ARV stakers who are sitting at lower levels.\*

#### **How to check**

While it’s a bit difficult to check the average boost level for a non-technical user if there is demand - the DAO may consider surfacing this in a user interface.

* _This is not the same for PRV: rewards for inactive PRV stakers will not necessarily be redistributed._
