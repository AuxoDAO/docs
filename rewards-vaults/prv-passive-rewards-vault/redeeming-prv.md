# Redeeming PRV

{% hint style="success" %}
Mechanics are explained in [#redemption-mechanics](./#redemption-mechanics "mention")
{% endhint %}

PRV is redeemable for Auxo, subject to a fixed monthly budget. This budget is calculated based on the price of Auxo compared to its fair market value.

As a PRV holder, I can convert my PRV to Auxo when withdrawals are enabled. The amount I can redeem will be based on:

1. The amount of unstaked PRV in my wallet
2. The remaining budget allocated for redemptions

### PRV in my wallet

The maximum amount of PRV I can redeem will depend on the amount of unstaked PRV in my wallet (staked PRV is not included) at a specific block snapshot. The block snapshot is typically taken at midnight UTC on the same day withdrawals are enabled.

### Total Budget

The total amount of redeemable PRV for all users is determined by the budget allocated for each epoch. This budget operates on a first-come, first-served basis. Once the budget is exhausted, redemptions will no longer be active until the next epoch, even if users hold PRV in their wallets.

{% embed url="https://www.loom.com/share/a2b0ca9bd2284ebe9d22a63da9fa2902?sid=36704f5e-1890-4a62-b622-985164ec89a7" %}
