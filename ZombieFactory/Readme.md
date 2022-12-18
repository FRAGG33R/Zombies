# What is contract ?

<aside>
🔥 A contract is a program that runs on the Ethereum Virtual Machine (EVM). It is written in the Solidity programming language and is used to define a set of rules for a specific purpose, such as a crowdfunding campaign or a voting system. When a contract is deployed to the Ethereum blockchain, it becomes a self-contained, autonomous entity that can execute the code in its contract and interact with other contracts on the blockchain.

</aside>

<aside>



🔥 Contracts are typically used to encode business logic and automate processes, allowing them to be executed in a trustless, decentralized manner. They can be used to create tokens, manage decentralized applications (DApps), and facilitate various types of transactions and interactions on the blockchain

</aside>

---

The ZombieFactory contract is a Solidity contract that allows users to create and manage virtual "zombies" on the Ethereum blockchain.

## **Contract Structure**

The contract is written in Solidity and specifies a minimum compiler version of 0.5.0 and a maximum of 0.6.0 using the **`pragma solidity >=0.5.0 <0.6.0;`** directive.

The contract has a single event called **`NewZombie`**, which is triggered whenever a new zombie is created. The event has three parameters:

- **`zombieId`**: the unique ID of the new zombie
- **`name`**: the name of the new zombie
- **`dna`**: the DNA of the new zombie

The contract also has a single struct called **`Zombie`**, which represents a zombie and has two fields:

- **`name`**: the name of the zombie
- **`dna`**: the DNA of the zombie

The contract has an array called **`zombies`** that is used to store all of the zombies that have been created. This array is marked as **`public`**, which means that it can be accessed by any external contract or user.

## **Contract Functions**

The contract has several functions that allow users to interact with it:

- **`_createZombie(string memory _name, uint _dna)`**: this function is used to create a new zombie and add it to the **`zombies`** array. It takes two arguments: the name of the zombie and the zombie's DNA. This function is marked as **`private`**, which means that it can only be called from within the contract itself and not from external contracts or users.
- **`_generateRandomDna(string memory _str)`**: this function generates a random DNA value for a zombie based on the provided string. It is marked as **`private`** and **`view`**, which means that it can only be called from within the contract and does not modify the contract's state. It returns a **`uint`** value representing the generated DNA.
- **`createRandomZombie(string memory _name)`**: this function creates a new zombie with a randomly generated DNA value based on the provided name. It calls the **`_createZombie`** and **`_generateRandomDna`** functions to create and add the new zombie to the **`zombies`** array. This function is marked as **`public`**, which means that it can be called by any external contract or user.

## **Using the ZombieFactory Contract**

To use the ZombieFactory contract, you will need to have an Ethereum wallet and some Ether (the currency of the Ethereum blockchain). You can then deploy the contract to the Ethereum blockchain using a tool like Remix or Truffle, and call its functions to create and manage zombies.
