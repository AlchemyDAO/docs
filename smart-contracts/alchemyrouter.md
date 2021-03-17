# AlchemyRouter

The Alchemy Router has the task to split the incoming rewards.

The rewards will go 50% to the treasury and 50% to the StakingRewards contract.

### `distribute`

```text
function distribute() internal
```



### `deposit`



```text
function deposit() external payable
```



### `fallback`

```text
fallback() external payable
```



### `receive`

```text
receive() external payable
```



### `newStakingrewards`

```text
function newStakingrewards(IStakingRewards newRewards) public 
```





### `newTreasury`

```text
function newTreasury(address payable newTrewasury) public 
```





### `newAlchemyFactory`

```text
function newAlchemyFactory(address newAlchemyAddress) public
```



### `newAlchemyFactoryOwner`

```text
function newAlchemyFactoryOwner(address payable newFactoryOwner) public
```



### `newOwner`

```text
function newOwner(address newOwner) public
```









