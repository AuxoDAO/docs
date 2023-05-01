# On chain voting

On-chain governance is based on the [Open Zeppelin Governor](https://docs.openzeppelin.com/contracts/4.x/api/governance) contract, which allows for on-chain voting similar to Compound’s Governor Alpha & Bravo.

The voting power of each account in the Auxo governance setup is determined by the balance of the Active Rewards Vault (ARV). ARV is a non-transferable token which implements `ERC20Votes` extension and keeps track of historical balances.

The Auxo Governor implements the following parameters:

**Voting Delay:** 13140 blocks (\~= 44 hours)\
_The delay between a proposal being created and it being able to be voted on, in blocks_

**Voting Period:** 50000 blocks (\~= 7days)\
_The duration of a vote in blocks_

**Proposal Threshold:** 10000 ARV\
_Minimum amount of ARV that must be delegated to a wallet before it can create a new proposal. Users can either self delegate or pool voting power by delegating to a representative._

**Quorum:** 5%\
_Minimum percentage of total ARV tokens that must participate in a vote for it to be considered valid._

### Timelock <a href="#timelock" id="timelock"></a>

The governance setup implements `GovernorTimelockControl` that binds the execution process to an instance of TimelockController. Practically speaking, this adds a delay to all successful proposals in addition to the voting duration.

The Timelock implements the following parameters:

**Timelock Delay:** 1 days\
_Delay between vote passing and ability to execute through timelock controller._

**Timelock Admin:** 0x6458A23B020f489651f2777Bd849ddEd34DfCcd2\
_Admin can circumvent gov delays on the timelock, useful in post-deploy operations._

**Timelock Executor:** `0x0000000000000000000000000000000000000000 (Anyone)`\
_Who can call `execute()` on the timelock controller_
