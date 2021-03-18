# GovernorAlphaFactory

This contract lets the Alchemy Contract set up its own GovernorAlpha instance to manage proposals.

There is a fixed amount needed to propose which is set at 1% of the total supply of the generated Alchemy ERC20 token and a quorum for votes set to 4% of the total supply.

### `init`

```text
function init(address timelock_) external
```

This function is called to set up the Governor contract with the matching timelock contract.



### `propose`

```text
function propose(address[] memory targets, uint[] memory values, string[] memory signatures, bytes[] memory calldatas, string memory description) public
```

Function that lets users create a proposal.

Takes the targets, values, function signatures, and the calldatas for the contract calls as well as a description.



### `queue`

```text
function queue(uint proposalId) public
```

This function is used to queue a proposal after it was successful.



### `_queueOrRevert`

```text
function _queueOrRevert(address target, uint value, string memory signature, bytes memory data, uint eta)
```

Internal function that either queues a proposal or cancels it.



### `execute`

```text
function execute(uint proposalId) public payable
```

The actual execute function for a proposal. This then calls the execue function on the timelock contract.

### `cancel`

```text
function cancel(uint proposalId) public
```

Cancels a defeated proposal.



### `getActions`

```text
function getActions(uint proposalId) public view returns (address[] memory targets, uint[] memory values, string[] memory signatures, bytes[] memory calldatas)
```

Returns the targets, signatures, values, and call data from a specific proposal.



### `getReceipt`

```text
function getReceipt(uint proposalId, address voter) public view returns (Receipt memory)
```

Gets a receipt for voting on a proposal.



### `state`

```text
function state(uint proposalId) public
```

Returns the current state of a proposal.



### `castVote`

```text
function castVote(uint proposalId, bool support)
```

Lets a user vote on a proposal.



### `castVoteBySig`

```text
function castVoteBySig(uint proposalId, bool support, uint8 v, bytes32 r, bytes32 s) public
```

Lets a user vote on a proposal by signature.



### `_castVote`

```text
function _castVote(address voter, uint proposalId, bool support) internal
```

Internal function to cast a vote.



### `GovernorMint`

```text
function GovernorMint(
    address nft_,
    uint supply_,
    uint votingtime_
) public
```

Factory function to mint a new governor alpha contract instance.



