---
description: Earn rewards without governance obligations
---

# PRV (Passive Rewards Vault)

The Passive Rewards Vault (PRV) offers the possibility to participate in the Auxo ecosystem outside of governance related matters. PRV is created by depositing AUXO into the vault at a 1:1 ratio and the vault token can be staked to earn rewards.

PRV implements a `delayed withdrawal mechanism` to AUXO, PRV holders can burn their token to get AUXO back — subject to the availability in the vault.

## Who is PRV for?

* DAO members with no interest in direct governance seeking a passive approach.
* Participants who want the optionality of being able to exit their position at any time.
* Users who are concerned about minimising both the gas expenditures and effort required to maintain a fully maximised rewards position.

## Rewards in PRV Comment <a href="#rewards-in-prv" id="rewards-in-prv"></a>

PRV receives 30% of the total monthy distribution of WETH rewards which are distributed via the PRV Staking Contract.

**PRV Stakers are not required to vote to get rewards and are not subject to lock.**

* Staking PRV is epoch based.
* Staked PRV tokens are never locked but need to be staked for the entire epoch in order to receive rewards
* PRV unstaked in the middle of an epoch give up their rewards.
* Staked PRV continue to earn rewards in perpetuity until unstaked.

Staked PRV can be withdrawn at any time and transferred, but once withdrawn, the user would have to re-deposit and wait for a full epoch to finish before being eligible for rewards.

Rewards for PRV non-qualifying will be redirected to operations.

## How staking works in PRV

As PRV can be freely converted from Auxo or from ARV at any time, there is a small staking requirement before PRV rewards are earned. This requirement prevents the purchase of large quantities of PRV immediately prior to distribution, then liquidate the token right after collecting rewards. Staking in PRV comes without lockup, tokens can exit the staking contract at anytime.

PRV must be staked in the PRV Locker for a full staking epoch before rewards can be claimed. However, users need only do this once: staked tokens continue to earn rewards in perpetuity until the PRV is unstaked.

A staking epoch lasts for a full calendar month and begins on at the start of said month, as an example:

* Assume we have an epoch `March epoch` which lasts from block X (00:00 March 1st) → block Y (23:59 March 31st)
* Rewards for the `March Epoch` will be distributed _after the epoch is over_ (at the start of _April)_

<figure><img src="../../.gitbook/assets/rewards prv.png" alt=""><figcaption></figcaption></figure>

* Alice stakes 100 PRV on the 20th Februrary. This is before the `March Epoch` begins and so Alice will be eligible for the rewards distribution _at the_ _end of the epoch._
* Bob stakes 100 PRV on the 2nd March, Bob will **not** be eligible for rewards, until the end of the next epoch (at the end of April/start of May)
* If Alice staked 50 PRV more _before_ `March Epoch` begins, then her 150 PRV would be eligible for rewards at the start of April.
* If Alice staked 50 PRV more **after** `March Epoch` begins, she will earn rewards on 100 PRV at the end of `March Epoch` then will earn rewards on the full 150 PRV at the end of the April Epoch.
* Therefore, a user will typically wait 4 - 8 weeks before their first rewards are eligible

> [⚠️ Staked PRV can be withdrawn at any time and transferred, but once withdrawn, the user would have to re-deposit and wait for a full epoch to finish before being eligible for rewards](#user-content-fn-1)[^1]



## Withdrawal mechanics

The amount of PRV that can be redeemed for AUXO each epoch _(redemption availability)_ will vary based on how the price of AUXO trades compared to the treasury net asset value (NAV). As NAV is considered to be the fair market value for AUXO, the redemption mechanism was designed to help the price stabilise around the NAV _(denominated in ETH)_.

$$
FairValue = NAV = \frac{Treasury Assets}{TotalAuxoSupply}
$$

The system will work as follows:

At the beginning of each epoch, the price of AUXO will be assessed based on how it is trading relative to the NAV.

1. Shall the price of AUXO _(denominated in ETH)_ trade at a discount, no AUXO will be redeemable through PRV in the given epoch.
2. Shall the price of AUXO _(denominated in ETH)_ trade at a premium, PRV will be redeemable for AUXO proportionally to the magnitude of the premium per se. Simply put, the larger the premium, the more AUXO can be redeemed through PRV.

In code terms, withdrawals only active in a given epoch `if(AUXOETH > NAV_eth*(1 + B%))`

where:

* AUXOETH, is the price of AUXO denominated in ETH
* NAV\_eth, is the net asset value of AUXO denominated in ETH

The `B factor` is a parameter ranging between 5% and 50% that will act as a ‘buffer’ (hence the B) and will be selected by the treasury committee each epoch. The `B factor` exists to mitigate additional selling pressure that could suppress the price of AUXO into further discount.

For instance, if at the beginning of an epoch AUXO will be trading at a 50% premium with respect to its NAV, then the B factor may be chosen to be somewhere between 5% and 15%. In other words, the magnitude of the redemption of that epoch will be as big as to allow enough selling pressure to bring down the price to 5% or 15% above NAV. Practically speaking, if the entire redemption availability gets filled and organic selling pressure adds on top of if, the price may very well trade within the buffer (below NAV\*(1 + B%)).

On the other hand, if at the beginning of the epoch the price of AUXO finds itself trading below a 5% premium to NAV, then no redemptions would be put in place for the current epoch. This because, shall redemptions be activated as to bring the price down to NAV, additional organic selling pressure may add up and suppress the price further in undervalued territory.

In sum, the buffer will act as an additional price stability mechanism where the higher the premium vs NAV at epoch start, the more room there will be for PRV redemptions into AUXO.

The system described above implies that shall there be little demand for AUXO (aka, AUXO trading at or below NAV) no redemptions would be available for PRV holders until the price starts trading at a healthy premium. On the other hand however, in periods of high demand and higher price appreciation, redemption rates can turn to be quite high thus allowing PRV holders to own more liquid holdings while at the same time ensuring the price of AUXO not to trade at many multiples above its fair market value.

PRV is a fully backed future claim on AUXO which earns rewards. PRV holders bet that AUXO price will be trading at healthy levels and get rewarded for stabilizing the market when it is trading at discount to NAV by keeping AUXO away from circulation.

[^1]: 
