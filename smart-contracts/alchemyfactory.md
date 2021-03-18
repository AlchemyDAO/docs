# AlchemyFactory

This contract creates new Alchemy Contracts which wrap NFT tokens into ERC20 tokens in order to create a DAO around them.



### `init`

```text
function init(address governorFactory, uint votinginit, address timelockFactory, uint256 timelockinit) external
```





### `_burn`

```text
function _burn(uint256 amount) internal
```





### `burnForETH`

```text
function burnForETH() external
```





### `Buyshares`

```text
function Buyshares(uint256 amount) external 
```





### `buyout`

```text
function buyout() external
```





### `burnSharesForSale`

```text
function burnSharesForSale(uint256 amount) onlyTimeLock external 
```





### `mintSharesForSale`

```text
function mintSharesForSale(uint256 amount) onlyTimeLock external
```





### `changeBuyoutPrice`

```text
function changeBuyoutPrice(uint256 amount) onlyTimeLock external
```





### `setNftSale`

```text
function setNftSale(uint256 nftarrayid, uint256 price, bool sale) onlyTimeLock external 
```





### `buySingleNft`

```text
function buySingleNft(uint256 nftarrayid) external
```





### `addNft`

```text
function addNft(address new_nft, uint256 tokenid) onlyTimeLock external
```





### `returnNft`

```text
function returnNft() onlyTimeLock external 
```





### `executeTransaction`

```text
function executeTransaction(address target, uint256 value, string memory signature, bytes memory data) onlyTimeLock external
```





### `getCurrentVotes`

```text
function getCurrentVotes(address account) external
```





### `delegate`

```text
function delegate(address delegatee) public
```





### `getPriorVotes`

```text
function getPriorVotes(address account, uint blockNumber) public 
```





### `_delegate`

```text
function _delegate(address delegator, address delegatee) internal
```





### `_moveDelegates`

```text
function _moveDelegates(address srcRep, address dstRep, uint256 amount) internal
```





### `_writeCheckpoint`

```text
function _writeCheckpoint(address delegatee, uint32 nCheckpoints, uint256 oldVotes, uint256 newVotes) internal 
```





### `distributeAlc`

```text
function distributeAlc(uint amount) internal
```





### `NFTDAOMint`

```text
function NFTDAOMint(
    IERC721 nftAddress_,
    address owner_,
    uint256 tokenId_,
    uint256 totalSupply_,
    string memory name_,
    string memory symbol_,
    uint256 buyoutPrice_
) public
```





### `newFactoryOwner`

```text
function newFactoryOwner(address payable newOwner) external
```





### `getFactoryOwner`

```text
function getFactoryOwner() public 
```

