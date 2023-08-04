---
description: Learn ARV and PRV compounding works
---

# Compounding Rewards

The compounding process involves making use of your WETH rewards to acquire more ARV or PRV tokens, which leads to an increase in potential rewards. This strategy allows for the exponential growth of your investment in ARV or PRV.

Users can decide to compound the rewards they have received during the previous epoch (this limitation may change in the future). By compounding users should expect the following:

* **Compounding ARV rewards** will increase the user's ARV staked balance without impacting the lock length.
* **Compounding PRV rewards** will increase the user's staked PRV staked balance.

On Auxo’s [rewards page](https://auxo.fi/rewards) you will find two Autocompound buttons: one for your ARV rewards and one for your PRV rewards.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

They allow you to:

* Delegate the Ops Multisig to claim rewards
* Swap them for AUXO
* Convert them to ARV or PRV
* Stake the ARV or PRV on your behalf

{% hint style="info" %}
Be mindful that

* The compounding option will be shown as long as you have an ARV or PRV lock.
* The delegation mechanism works like an ON/OFF switch, once set to ON, it will automatically compound rewards until the delegation is revoked.
* Additionally, the holder's preference won't change regardless of the lock's status (expired/unlocked/redeemed).
{% endhint %}

## Compounding schedule

The delegated rewards will be staked on your behalf on the 25th of the month, ready for the next epoch distribution.

{% hint style="danger" %}
Rewards need to be delegated by the 24th of each month at midnight UTC. Rewards delegated after that will be compounded in the next month.
{% endhint %}
