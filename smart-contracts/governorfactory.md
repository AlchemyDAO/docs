# GovernorAlphaFactory

This contract lets the Alchemy Contract set up its own GovernorAlpha instance to manage proposals.

There is a fixed amount needed to propose which is set at 1% of the total supply of the generated Alchemy ERC20 token and a quorum for votes set to 4% of the total supply.

### `init`

```text
function init(address timelock_) external
```



### `propose`

```text
function propose(address[] memory targets, uint[] memory values, string[] memory signatures, bytes[] memory calldatas, string memory description) public
```



### `queue`

```text
function queue(uint proposalId) public
```



### `_queueOrRevert`

```text
function _queueOrRevert(address target, uint value, string memory signature, bytes memory data, uint eta)
```



### `execute`

```text
function execute(uint proposalId) public payable
```





### `cancel`

```text
function cancel(uint proposalId) public
```





### `getActions`

```text
function getActions(uint proposalId) public view returns (address[] memory targets, uint[] memory values, string[] memory signatures, bytes[] memory calldatas)
```



### `getReceipt`

```text
function getReceipt(uint proposalId, address voter) public view returns (Receipt memory)
```



### `state`

```text
function state(uint proposalId) public
```



### `castVote`

```text
function castVote(uint proposalId, bool support)
```



### `castVoteBySig`

```text
function castVoteBySig(uint proposalId, bool support, uint8 v, bytes32 r, bytes32 s) public
```



### `_castVote`

```text
function _castVote(address voter, uint proposalId, bool support) internal
```



### `GovernorMint`

```text
function GovernorMint(
    address nft_,
    uint supply_,
    uint votingtime_
) public
```

