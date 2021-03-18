# TimelockFactory

This contract lets the Alchemy Contract set up its own Time Lock instance to execute proposals proposed through the GovernorAlpha contract instance.



### `setDelay`

```text
function setDelay(uint delay_) public
```





### `acceptAdmin`

```text
function acceptAdmin() public
```





### `setPendingAdmin`

```text
function setPendingAdmin(address pendingAdmin_) public
```





### `queueTransaction`

```text
function queueTransaction(address target, uint value, string memory signature, bytes memory data, uint eta) public
```





### `cancelTranaction`

```text
function cancelTransaction(address target, uint value, string memory signature, bytes memory data, uint eta)
```





### `executeTransaction`

```text
function executeTransaction(address target, uint value, string memory signature, bytes memory data, uint eta) public
```





### `getBlockTimestamp`

```text
function getBlockTimestamp() internal
```





### `TimelockMint`

```text
function TimelockMint(
    address admin_,
    uint delay_
) external
```



