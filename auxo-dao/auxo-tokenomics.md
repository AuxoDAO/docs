# Distribution

Prior to a distribution, the DAO will gather staking and voting data for ARV, and staking data for PRV from relevant sources, and construct a view of the proposed rewards distribution. This will be shared to DAO members, who will be asked to vote on the validity of the proposed distribution.

{% hint style="info" %}
A cutoff block each month will be selected, votes cast after that block will be considered part of the following month.
{% endhint %}

* If the distribution is **notarized** (voted as valid), the DAO will distribute rewards via a distributor contract.
* If not, the DAO will resolve any issues and resubmit a new proposal for distribution.

Rewards will be distributed in WETH and will be claimable via a rewards contract. Rewards from multiple epochs can be claimed at once, there is no need for stakers to claim every month.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/07b1cada-bc84-4875-b652-37bbff39e56f/Untitled.png)
