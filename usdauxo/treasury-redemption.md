# Treasury redemption

**On Sep 6, 2023 the DAO has voted to dissolve and enable redemption of treasury assets. The DAO is no longer operating.**

The AuxoDAO members have [voted](https://snapshot.org/#/auxo.eth/proposal/0xd0fc1ecadf23dbaa5fb1e925c5406ce112280cb7f560773cb58a38661ca861e0) to dissolve the DAO, the DAO treasury is returned to its holders in order to allow them to claim back their ETH.&#x20;

Considering the fact that the DAO Treasury was affected by the [alETH pool exploit](https://discord.com/channels/1095291124245086278/1095322014669086804/1135263776556470453) there’ll be 2 distribution events, the first one scoping the Treasury’s balance before redistribution of stolen funds, and the final one scoping to distribute the funds returned from the exploit (if any).

Each distribution will be done snapshot-based, and the claiming of the WETH will be possible through the website’s UI. Each distribution will have a merkle tree issued, and it will be based on the DAO notarizes value of prorata of cumulative holdings.

### Holder types and Actions

| Type                      | Action                                                                                                                                                                                                           |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Auxo holders              | Just go and claim.                                                                                                                                                                                               |
| ARV holders               | Just go and claim. All ARV is eligible, regardless its level and lock time. To know how much Auxo you’ll be entitled to, go to [https://auxo.fi/ARV](https://auxo.fi/ARV) and check the Your AUXO staked amount. |
| PRV stakers & PRV holders | Just go and claim. All PRV is eligible, regardless if staked or not. To know how much Auxo you’ll be entitled to, go to [https://auxo.fi/PRV](https://auxo.fi/PRV) and check the **Your AUXO staked** amount.    |
| ARV/PRV compounders       | You must cancel the compounding delegation before claiming. Go to [https://auxo.fi/rewards](https://auxo.fi/rewards) and revoke the delegation. Once done, see ARV and PRV points                                |

### How to redeem?

The page [https://auxo.fi/treasury-redemption](https://auxo.fi/treasury-redemption) allows all Auxo, PRV, ARV holders to redeem and claim ETH pro-rata from their holdings. AUXO won’t be burned, meaning that this process requires no need to exit your position in any way, so you can choose to perform this action as long as the website is up and running, or do it manually via smartcontracts using the merkle-tree in the notarization vote.

The process will be split in two phases, issuing a distribution process for each with their own merkle trees.

* Phase 1: First Claim action. Claim all your pro-rata share of treasury funds which exist in October 2023.
* Phase 2: Final Claim action. Claim the pro-rata of the resulting balance returned from the Alchemix exploit. Remember this can be 0 or higher.

The redemption amount will consider the addresses’ pro-rata balances of `YOUR_AUXO_IN_ARV + YOUR_AUXO_PRV + YOUR_AUXO_IN_PRV_STAKED + YOUR_AUXO` for that specific distribution. This means that you’ll need to claim phase 1 and then phase 2 separately.&#x20;

### Next Steps

The DAO core team will repeat the distribution process when and if the alETH pool funds are returned, if ever. The team has agreed to monitor and regroup twice between the next 12 moths, or once the situation is resolved. In the mean time no further actions should be expected by the DAO members.
