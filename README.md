# solidity
## HelloWorld Smart Contract

### Introduction

This is a tutorial on how to create a HelloWorld smart contract using Solidity. 

### Prerequisites

- Node.js installed on your computer
- Truffle framework installed

### Step 1: Create a new Truffle project

```
truffle init
```

### Step 2: Create a new smart contract

Create a new file in the contracts directory called `HelloWorld.sol`. 

### Step 3: Write the smart contract code

```
// SPDX-License-Identifier: MIT
pragma solidity >=0.4.21 <0.8.22;

contract HelloWorld {
    string public message;

    constructor() {
        message = "Hello, World!";
    }

    function getMessage() public view returns(string memory){
      return (message);
    }
}
```

### Step 4: Compile the smart contract

```
truffle compile
```

### Step 5: Deploy the smart contract

```
truffle migrate
```

### Step 6: Interact with the smart contract

```
const HelloWorld = artifacts.require("HelloWorld");

const contract = await HelloWorld.deployed();

const message = await contract.getMessage();

console.log(message); // "Hello, World!"
```

### Conclusion

You have now successfully created, compiled, deployed, and interacted with a HelloWorld smart contract. 

### Additional Resources

- [Truffle documentation](https://truffleframework.com/docs/)
- [Solidity documentation](https://docs.soliditylang.org/en/v0.8.22/)
