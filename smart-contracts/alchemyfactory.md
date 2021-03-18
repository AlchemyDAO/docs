# AlchemyFactory

This contract creates new Alchemy Contracts which wrap NFT tokens into ERC20 tokens in order to create a DAO around them.



### `init`

```text
function init(address governorFactory, uint votinginit, address timelockFactory, uint256 timelockinit) external
```

This function initializes a new DAO for an NFT. It takes the address of the GovernorAlphaFactory and the TimelockFactory and the times for the voting period and also the timelock period.

After the function is run, a new DAO is fully functional and ready to use.



### `_burn`

```text
function _burn(uint256 amount) internal
```

Internal function to burn amount x from the total supply.



### `burnForETH`

```text
function burnForETH() external
```

This function can be called from each holder of the DAO token. If the Alchemy contract has an ETH balance the burner will get an adequate amount of ETH from the balancer and burns their DAO tokens for this event.



### `Buyshares`

```text
function Buyshares(uint256 amount) external 
```

This function allows anyone to buy shares from the DAO contract. These shares have to be issued from the DAO before.



### `buyout`

```text
function buyout() external payable
```

This function can be called by anyone by sending the buyout price in terms of ETH to the contract function. This will trigger the buyout process and burn the shares of the buyer if he has some.

The buyout price will also decrease if the buyer is a shareholder of the DAO, and so he will get a discount.

Finally, all the NFTs in the DAO will be transferred to the buyer.

Also, a 0.5% fee from the buyout price is then sent from the Alchemy Contract to the Alchemy Router and split amongst the treasury and the Staking Pool.



### `burnSharesForSale`

```text
function burnSharesForSale(uint256 amount) onlyTimeLock external 
```

This function will decrease the number of shares for sale in the DAO. Can only be called by the Timelock.



### `mintSharesForSale`

```text
function mintSharesForSale(uint256 amount) onlyTimeLock external
```

This function will increase the number of shares for sale in the DAO. Can only be called by the Timelock.



### `changeBuyoutPrice`

```text
function changeBuyoutPrice(uint256 amount) onlyTimeLock external
```

This function will change the buyout price for the DAO. Can only be called by the Timelock.



### `setNftSale`

```text
function setNftSale(uint256 nftarrayid, uint256 price, bool sale) onlyTimeLock external 
```

This function will set a specific NFT in the DAO on sale, so it can be bought separately. Can only be called by the Timelock.



### `buySingleNft`

```text
function buySingleNft(uint256 nftarrayid) external
```

This function is used to buy a single NFT from the DAO. The NFT must have been set on sale before. 

After the sale, the NFT is then transferred from the contract to the buyer and a 0.5% fee of the price is sent to the Alchemy Router.



### `addNft`

```text
function addNft(address new_nft, uint256 tokenid) onlyTimeLock external
```

This function adds a specific NFT to the DAOs NFT treasury array. Can only be called by the Timelock.



### `returnNft`

```text
function returnNft() onlyTimeLock external 
```

This function returns the original NFT to the owner. Can only be called by the Timelock.



### `executeTransaction`

```text
function executeTransaction(address target, uint256 value, string memory signature, bytes memory data) onlyTimeLock external
```

This function can execute any contract call. Can only be called by the Timelock.



### `getCurrentVotes`

```text
function getCurrentVotes(address account) external
```

This function is used to get the current votes of an address based on the timestamp.



### `delegate`

```text
function delegate(address delegatee) public
```

This function is used to delegate votingpower to an address.



### `getPriorVotes`

```text
function getPriorVotes(address account, uint blockNumber) public 
```

This function is used to determine the prior votes of an address.



### `_delegate`

```text
function _delegate(address delegator, address delegatee) internal
```

Internal function to set the delegatee.



### `_moveDelegates`

```text
function _moveDelegates(address srcRep, address dstRep, uint256 amount) internal
```

Internal function to move delegate votes to another address.



### `_writeCheckpoint`

```text
function _writeCheckpoint(address delegatee, uint32 nCheckpoints, uint256 oldVotes, uint256 newVotes) internal 
```

Internal function to write a snapshot of current votes for later processing.



### `distributeAlc`

```text
function distributeAlc(uint amount) internal
```

A function used to distribute the ALCH token amongst the community → people who mint an Alchemy contract.



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

Minting function for a new Alchemy contract.



### `newFactoryOwner`

```text
function newFactoryOwner(address payable newOwner) external
```

A function used to change the factory owner of the AlchemyFactory.



### `getFactoryOwner`

```text
function getFactoryOwner() public 
```

View function to get the current owner of the AlchemyFactory.

