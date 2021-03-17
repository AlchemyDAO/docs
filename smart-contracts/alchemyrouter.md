# AlchemyRouter

The Alchemy Router has the task to split the incoming rewards.

The rewards will go 50% to the treasury and 50% to the StakingRewards contract.

### `distribute`

```text
function distribute() internal
```

This function distributes the contract balance between the StakingRewards contract and the treasury. The split is done 50%:50%. This function also calls the notifyRewardAmount on the staking contract.

### `deposit`

```text
function deposit() external payable
```

This function is called after a buyout or sale of an NFT happens. The function only calls distribute\(\) if the contract balancer is greater than 0.1ETH.

### `fallback`

```text
fallback() external payable
```

Basic fallback function. The function only calls distribute\(\) if the contract balancer is greater than 0.1ETH.

### `receive`

```text
receive() external payable
```

Basic receive function. The function only calls distribute\(\) if the contract balancer is greater than 0.1ETH.

### `newStakingrewards`

```text
function newStakingrewards(IStakingRewards newRewards) public 
```

This function sets a new StakingRewards address. Only the owner can call this.

### `newTreasury`

```text
function newTreasury(address payable newTrewasury) public 
```

This function sets a new Treasury address. Only the owner can call this.

### `newAlchemyFactory`

```text
function newAlchemyFactory(address newAlchemyAddress) public
```

This function sets a new AlchemyDAOFactory address. Only the owner can call this.

### `newAlchemyFactoryOwner`

```text
function newAlchemyFactoryOwner(address payable newFactoryOwner) public
```

This function sets a new AlchemyDAOFactory owner address. Only the owner can call this.

### `newOwner`

```text
function newOwner(address newOwner) public
```

This function sets a new owner address of the contract. Only the owner can call this.







