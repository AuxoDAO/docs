---
description: Who we manage liquidity
---

# Protocol Owned Liquidity

Auxo aims to own within the DAO the vast majority of its liquidity, a process often referred as protocol owned liquidity (POL).

As Auxo generates value for its stakers directly from the yield it generates through treasury farming operations, it is reasonable to assume that a fair valuation for the AUXO token must fall somewhere near its Net Asset Value (NAV).&#x20;

To favor capital efficiency, the AUXOETH liquidity is hosted on a series of Uniswap V3 ranges. Pool parameters and market making operations are conducted as described below.

In an ideal scenario, the price of Auxo will trade at a slight premium with respect to its NAV. The goal of protocol conducted market making operations is to facilitate the price to gravitate around this ideal premium.

To start, the protocol will deploy a base layer of liquidity on the following range:

* `Upper bound = NAV * ub_factor`
* `Lower bound = NAV * lb_factor`

Where `ub_factor` and `lb_factor` are selected by treasury operators and define the distance of the upper and lower bound respectively from the NAV. The figure below provides a visual representation of how liquidity is intended to be deployed.

![](https://i.imgur.com/bIthtJF.png)

Additionally, the Treasury will deploy additional liquidity in a number of sub-ranges that are intended to work as support and resistance to the price in order to support convergence towards healthy price action.
