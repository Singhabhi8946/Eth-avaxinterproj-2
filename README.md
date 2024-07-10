# Eth-avaxinterproj-2
This project demonstrates a basic use case of Hardhat for developing smart contracts, and React for building a simple frontend.



## Prerequisites
Before you begin, ensure you have met the following requirements:

- Node.js and npm installed
- Hardhat installed globally
- A code editor like VSCode
- Project Setup
- Clone the repository:
- Install the dependencies:
```
npm install
```
## Execution


- Create a new Hardhat project:
```
npx hardhat
```
- Add the sample contract Greeter.sol in the contracts folder: Our smart contracts : Greeter.sol

- Write a test for the contract in the test folder: npx hardhat test :- To test the hardhat project

- Deploy the contract using a script in the scripts folder:

-  We require the Hardhat Runtime Environment explicitly here. This is optional but useful for running the script in a standalone fashion through `node <script>`.
- When running the script with `npx hardhat run <script>` you'll find the Hardhat
- Runtime Environment's members available in the global scope.
```
const hre = require("hardhat");

async function main() {
  
  const Greeter = await hre.ethers.getContractFactory("Greeter");
  const greeter = await Greeter.deploy("Hello, Hardhat!");

  await greeter.deployed();

  console.log("Greeter deployed to:", greeter.address);
}


main()
  .then(() => process.exit(0))
  .catch((error) => {
    console.error(error);
    process.exit(1);
  });
```
## Frontend Setup
Using React App

Create a new React app:
```
npx create-react-app mydapp
cd mydapp
```
Install web3 dependencies:
```
npm install ethers
```

## Deploy Project
- Start the Hardhat local network:
```
npx hardhat node
```
- Deploy the smart contract to the local network:
```
npx hardhat run scripts/deploy.js --network localhost
```
- Start the React development server:
```
npm run start
```
- Open your browser and go to http://localhost:3000 to interact with the frontend.

## Author
Abhinav Singh
## License
This project is licensed under the MIT License. See the LICENSE file for details.




