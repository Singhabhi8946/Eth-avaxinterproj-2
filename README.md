# Eth-avaxinterproj-2

This project demonstrates a basic use case of Hardhat for developing smart contracts, and React for building a simple frontend.

## Prerequsities

Before you begin, ensure you have met the following requirements:

- Node.js and npm installed
- Hardhat installed globally
- A code editor like VSCode


## Project setup

- Clone the repository:

- Install the dependencies:

```
npm install
```

## Execution 

Create a new Hardhat project:

- installing hardat
 ```
npm install hardat
```
- executing hardat
```
npx hardhat
```
Add the sample contract ```Greeter.sol``` in the contracts folder: 
- Our smart contracts : Greeter.sol

Write a test for the contract in the test folder: npx hardhat test :- To test the hardhat project

Deploy the contract using a script in the scripts folder:


- We require the Hardhat Runtime Environment explicitly here. This is optional
- but useful for running the script in a standalone fashion through `node <script>`.
- When running the script with `npx hardhat run <script>` you'll find the Hardhat
- Runtime Environment's members available in the global scope.
- Hardhat always runs the compile task when running scripts with its command line interface.
- If this script is run directly using `node` you may want to call compile manually to make sure everything is compiled await hre.run('compile');
- We get the contract to deploy
  ```
const hre = require("hardhat");

async function main() {
  const Greeter = await hre.ethers.getContractFactory("Greeter");
  const greeter = await Greeter.deploy("Hello, Hardhat!");

  await greeter.deployed();

  console.log("Greeter deployed to:", greeter.address);
}
```
