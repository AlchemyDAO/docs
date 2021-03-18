# TimelockFactory

This contract lets the Alchemy Contract set up its own Time Lock instance to execute proposals proposed through the GovernorAlpha contract instance.



### `setDelay`

```text
function setDelay(uint delay_) public
```

This function is used to set a new delay when executing the contract calls.



### `acceptAdmin`

```text
function acceptAdmin() public
```

A function used to accept a new admin for the timelock.



### `setPendingAdmin`

```text
function setPendingAdmin(address pendingAdmin_) public
```

A function to set a new pending admin for the timelock contract.



### `queueTransaction`

```text
function queueTransaction(address target, uint value, string memory signature, bytes memory data, uint eta) public
```

This function is used to queue a new transaction from the governor contract.



### `cancelTranaction`

```text
function cancelTransaction(address target, uint value, string memory signature, bytes memory data, uint eta)
```

This function is used to cancel a transaction.



### `executeTransaction`

```text
function executeTransaction(address target, uint value, string memory signature, bytes memory data, uint eta) public
```

This function is used to execute a transaction.



### `getBlockTimestamp`

```text
function getBlockTimestamp() internal
```

A function used to get the current Block Timestamp.



### `TimelockMint`

```text
function TimelockMint(
    address admin_,
    uint delay_
) external
```

The minting which mints a new Timelock contract instance.

