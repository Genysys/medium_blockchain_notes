# Test ERC20
It is simple example of the usage of token-test-suite library for ERC20 token full test coverage.<br>
You can find more in the [appropriate article on Medium](https://medium.com/better-programming/lets-talk-about-smart-contract-unit-testing-1317a2d2365a).

## Prerequisites

For development purposes, you will need `Node.js` and a package manager – `npm`. For the development, the following versions were used:
- `Node.js` – v12.18.3
- `npm` – 6.14.6

## 1. Installation

Run the command `$ npm install` to install all the dependencies specified in `package.json`.

## 2. Configuration
#### `.env`

For the deployment process to be successfully performed, **manually created** `.env` file with filled-in parameters should be present at the root of the project. You need the following to be filled:

**Dev settings**
- `DEV_MNEMONIC` Private key for the deployment.
- `INFURA_ID`. Infura API key.
- `GAS_PRICE`. Set the gas price for the deployment transaction.

**Contract settings**
- `UNIQUE_TOKEN_HOLDER` Address that will receive the total supply of Unique token
- `UNIQUE_TOKEN_SUPPLY` Total supply of Unique token

## 3. Running scripts

### Compilation
Use `$ npm run build` to compile the smart-contracts.

### *Dev tools*

`$ npm run dev:lint` to run Solidity and JavaScript linters and check the code for stylistic bugs.

`$ npm run dev:coverage` to run the unit-tests coverage utility.

`$ npm run dev:contract-size` to run the compiled contracts size check.

`$ npm run ganache` to start a local Ganache node.

### Testing

Run `$ npm run dev:ganache` to start the Ganache development network. Perform tests with `$ npm run test` to run all tests from the `test/` directory.

### Deployment
Before proceeding with the deployment process, make sure you have set up the `.env` file.

Run `$ npm run deploy --network <network_name>` with `<network_name>` replaced with testnet/mainnet name to deploy the smart-contracts.
