# $AUXO

$AUXO is an ERC-20 Token deployed on the Ethereum Network that represents share of the Auxo DAO treasury.

The AUXO token has a strictly controlled policy of expansion, it is designed to be non-dilutive versus the net asset value (NAV) of the treasury and **there is no mechanism of inflation.**

The AUXO token is fully distributed to it’s token holders apart for 20% held by the DAO at exclusive use of protocol-owned-liquidity and market making.\


### Net Asset Value

The Net Asset Value for AUXO is calculated as total assets held by the protocol divided by the total AUXO supply, in math terms:

> NAV = Assets / Total\_Auxo\_Supply

Assets comprehend:

* Liquid assets held in the treasury
* Illiquid assets held in the treasury
* ETH side of AUXO-ETH pairs where the treasury is providing liquidity

The valuation of the assets will follow a 7 day [TWAP](https://en.wikipedia.org/wiki/Time-weighted\_average\_price). The price of liquid assets will be recorded for TWAP computation every day at market open.

> 📝 The price of illiquid assets will vary based on the nature of the liquid asset itself. In case of escrowed tokens such as esGMX (which the treasury currently holds), their price will be assumed to be the same as liquid GMX.

It is only possible to mint new tokens, pending governance approval, with the inflow of new capital in the treasury at NAV value through a mechanism known as bonding. This feature ensures that previous holders are not diluted from newcomers joining the DAO.

