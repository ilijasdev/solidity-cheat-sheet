# solidity-cheat-sheet
Solidity learning materials

## Contracts
Solidity's code is encapsulated in **contracts**.
**contract** is fundamental building block of application that run on EVM.

**pragma** define which Solidity complier code should use. First line in `ObservingPool` contract in this repo.

***Heads up*** - `ObservingPool` contract is just working template, if you want to use it, use it on your own risk. Variables and functions are only for presentation and explanations purpose.

## Variables and Data Types
Solidity support two variable state - **memory** and **storage**. 
State variables are permanently stored in contract storage. 

**uint** data type is an unsigned integer (its value must be non-negative).
**int** data type for signed integers.

> Note: In Solidity, uint is actually an alias for uint256, a 256-bit unsigned integer. You can declare uints with less bits — uint8, uint16, uint32, etc.. But in general you want to simply use uint except in specific cases, which we'll talk about in later lessons.

For more complex data use **structs**. Line 4 in `ObservingPool` contract in this repo.
For data collections use **array** (_fixed_ or _dynamic_ use depends on needs).
> Note: You can declare an array as public, and Solidity will automatically create a getter method for it. The syntax looks like: `Pools[] public pool;` Other contracts would then be able to read from, but not write to, this array. So this is a useful pattern for storing public data in your contract.
