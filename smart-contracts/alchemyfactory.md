# AlchemyFactory

This contract creates new Alchemy Contracts which wrap NFT tokens into ERC20 tokens in order to create a DAO around them.





```text
function init(address governorFactory, uint votinginit, address timelockFactory, uint256 timelockinit) external
```







```text
function _burn(uint256 amount) internal
```





```text
function burnForETH() external
```







```text
function Buyshares(uint256 amount) external 
```







```text
function buyout() external
```







```text
function burnSharesForSale(uint256 amount) onlyTimeLock external 
```







```text
function mintSharesForSale(uint256 amount) onlyTimeLock external
```







```text
function changeBuyoutPrice(uint256 amount) onlyTimeLock external
```







```text
function setNftSale(uint256 nftarrayid, uint256 price, bool sale) onlyTimeLock external 
```







```text
function buySingleNft(uint256 nftarrayid) external
```







```text
function addNft(address new_nft, uint256 tokenid) onlyTimeLock external
```







```text
function returnNft() onlyTimeLock external 
```







```text
function executeTransaction(address target, uint256 value, string memory signature, bytes memory data) onlyTimeLock external
```







```text
function getCurrentVotes(address account) external
```





```text
function delegate(address delegatee) public
```





```text
function getPriorVotes(address account, uint blockNumber) public 
```





```text
function _delegate(address delegator, address delegatee) internal
```





```text
function _moveDelegates(address srcRep, address dstRep, uint256 amount) internal
```





```text
function _writeCheckpoint(address delegatee, uint32 nCheckpoints, uint256 oldVotes, uint256 newVotes) internal 
```





```text
function distributeAlc(uint amount) internal
```







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





```text
function newFactoryOwner(address payable newOwner) external
```







```text
function getFactoryOwner() public 
```

