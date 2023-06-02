# Checking your Eligibility

### ⛓️ On-Chain Votes Validation

1. Go to the [Snapshot GraphQL Editor](https://api.thegraph.com/subgraphs/name/jordaniza/auxo-gov-mainnet-1/graphql?query=++++query+OnChainVotes+%7B%0A++++++++voteCasts%28%0A++++++++++++where%3A+%7B+%0A++++++++++++++++timestamp\_gt%3A+0%2C%0A++++++++++++++++timestamp\_lte%3A+1685548065%2C%0A++++++++++++++++governor%3A+%220xB320Fc09B272D1658E99488ADc614E4645B1d83c%22%2C%0A++++++++++++++%09voter\_%3A+%7Bid%3A+%220x0fa36923d4dD8139673905DCddbC747Ad95EF353%22%7D%0A++++++++++++%7D%0A++++++++%29+%7B%0A++++++++++++id%0A++++++++++++receipt+%7B%0A++++++++++++++++reason%0A++++++++++++%7D%0A++++++++++++support+%7B%0A++++++++++++++++support%0A++++++++++++%7D%0A++++++++++++proposal+%7B%0A++++++++++++++++description%0A++++++++++++++++canceled%0A++++++++++++++++executed%0A++++++++++++++++id%0A++++++++++++++++endBlock%0A++++++++++++++++startBlock%0A++++++++++++++++proposer+%7B%0A++++++++++++++++++++id%0A++++++++++++++++%7D%0A++++++++++++++++proposalCreated+%7B%0A++++++++++++++++++++timestamp%0A++++++++++++++++%7D%0A++++++++++++%7D%0A++++++++++++governor+%7B%0A++++++++++++++++id%0A++++++++++++%7D%0A++++++++++++voter+%7B%0A++++++++++++++++id%0A++++++++++++%7D%0A++++++++++++timestamp%0A++++++++%7D+++++%0A++++%7D%0A+)
2. Find and replace `voter_` with your voting address.
3. Change `timestamp_gt` timestamp.
4. Change `timestamp_lte` timestamp.
5. Click the play ▶️ button on the top left.
6. If the query returns zero results, like shown below, you did not vote.

### ⚡Off-Chain Votes Validation

1. Go to the [Snapshot GraphQL Editor](https://hub.snapshot.org/graphql?query=%7B%20%0A%20%20votes\(first%3A%20100%2C%20where%3A%20%7B%0A%20%20%20%20%20%20%20%20voter%3A%20%22YOUR\_ADDRESS\_HERE%22%2C%0A%20%20%20%20space%3A%20%22auxo.eth%22%2C%0A%20%20%20%20created\_gt%3A%201638316800%2C%20created\_lt%3A%201640995200%0A%20%20%7D\)%20%0A%20%20%20%7B%0A%20%20%20%20voter%0A%20%20%20%20proposal%20%7B%0A%20%20%20%20%20%20id%2C%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D)
2. Find and replace `YOUR_ADDRESS_HERE` with your voting address.
3. Change `created_gt` timestamp.
4. Change `created_lt` timestamp.
5. Click the play ▶️ button on the top left.
6. If the query returns zero results, like shown below, you did not vote.

{% hint style="info" %}
Snapshot allows users to change votes until the vote is closed. Each time a user votes, the timestamp of the vote gets updated to the latest recording with only 1 timestamp. That last timestamp will determine if you voted within a certain epoch.
{% endhint %}

### 🦊 Check your address eligibility

1. Click on the Merkle Tree link in the Notarization Vote
2. Use the search option of your browser to search for your address
3. Once you have the result:
   1. Vote **VALID** if your address is there and the amount is correct
   2. Vote **INVALID** if your address is not or the amount is not correct
