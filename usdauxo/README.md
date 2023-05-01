# $AUXO

$AUXO is an ERC-20 Token deployed on the Ethereum Network that represents shares of the Auxo DAO treasury.

The AUXO token has a strictly controlled policy of expansion, it is designed to be non-dilutive versus the net asset value (NAV) of the treasury and **there is no mechanism of inflation.**

The AUXO token is fully distributed to it’s token holders, aside from 20% of supplu held by the DAO as protocol-owned-liquidity used in market making.

### Net Asset Value

The Net Asset Value for AUXO is calculated as total assets held by the protocol divided by the total AUXO supply, in math terms:

> NAV = Assets / Total\_Auxo\_Supply

Assets are comprised of:

* Liquid assets held in the treasury
* Illiquid assets held in the treasury
* ETH side of AUXO-ETH pairs where the treasury is providing liquidity

The valuation of the assets will follow a 7 day [TWAP](https://en.wikipedia.org/wiki/Time-weighted\_average\_price). The price of liquid assets will be recorded for TWAP computation every day at market open.

> 📝 The price of illiquid assets will vary based on the nature of the liquid asset itself. In case of escrowed tokens such as _esGMX_, their price will be assumed to be the same as their liquid equivalents (i.e. _GMX_).

It is only possible to mint new tokens with governance approval, specifically via an inflow of new capital into the treasury at NAV value through a mechanism known as _bonding_. This feature ensures that previous holders are not diluted from newcomers joining the DAO.

