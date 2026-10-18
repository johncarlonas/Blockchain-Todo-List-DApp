
<div align="center">

<h1>Blockchain Todo List DApp</h1>

<p>
  A decentralized to-do list application built with Ethereum smart contracts, allowing users to manage tasks through a blockchain-connected web interface.
</p>

<p>
  My first decentralized application, developed while exploring blockchain technology, Solidity, and Web3 development.
</p>

<p>
  <img src="https://img.shields.io/badge/SOLIDITY-363636?style=for-the-badge&logo=solidity&logoColor=white" alt="Solidity" />
  <img src="https://img.shields.io/badge/ETHEREUM-3C3C3D?style=for-the-badge&logo=ethereum&logoColor=white" alt="Ethereum" />
  <img src="https://img.shields.io/badge/BOOTSTRAP-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap" />
  <img src="https://img.shields.io/badge/TRUFFLE-5E464D?style=for-the-badge&logo=truffle&logoColor=white" alt="Truffle" />
  <img src="https://img.shields.io/badge/WEB3.JS-F16822?style=for-the-badge&logo=web3dotjs&logoColor=white" alt="Web3.js" />
  <img src="https://img.shields.io/badge/METAMASK-F6851B?style=for-the-badge&logo=metamask&logoColor=white" alt="MetaMask" />
</p>

</div>

---

## Overview

**Blockchain Todo List DApp** is my first decentralized application, created as a personal project while learning the fundamentals of blockchain technology and Ethereum-based application development.

I built this project to understand how traditional web development concepts can be combined with smart contracts to create applications that interact with a blockchain.

Unlike a conventional to-do list that stores tasks in a centralized database, this project explores storing and retrieving task information through an Ethereum smart contract.

The application combines a browser-based interface, wallet connectivity, and Solidity smart contracts running on a local Ethereum development network.

Through this project, I explored smart contract development, blockchain transactions, wallet integration, and communication between a JavaScript frontend and the Ethereum network.

## Features

| Feature | Description |
| --- | --- |
| Blockchain Task Storage | Stores task records using an Ethereum smart contract. |
| Task Creation | Allows users to submit new tasks through the application interface. |
| Task Retrieval | Reads stored task information from the blockchain. |
| Task Organization | Presents active and completed task sections based on task status. |
| Wallet Integration | Connects the application to an Ethereum-compatible browser wallet. |
| Smart Contract Interaction | Uses Web3.js and Truffle Contract to communicate with deployed contracts. |
| Local Blockchain Development | Supports contract deployment and testing using a local Ethereum development network. |

## How It Works

The application uses an Ethereum smart contract to manage task data.

The frontend communicates with the deployed contract through a Web3 provider supplied by an Ethereum-compatible browser wallet.

The general process involves:

1. Connecting the browser to an Ethereum-compatible wallet.
2. Accessing the smart contract deployed on the local blockchain.
3. Reading stored task records through contract functions.
4. Submitting new tasks through blockchain transactions.
5. Displaying task information in the web interface.

Task records are stored within the smart contract's state rather than a traditional application database.

Creating a task involves a blockchain transaction, while retrieving task data uses the contract's public read functions.

## Smart Contract

The main smart contract is located at:

`contracts/TodoList.sol`

It defines the structure and storage of tasks on the Ethereum blockchain.

### Task Structure

Each task contains three fields:

| Field | Type | Description |
| --- | --- | --- |
| `id` | `uint` | Unique task identifier. |
| `content` | `string` | Task description. |
| `completed` | `bool` | Indicates whether the task is completed. |

The contract uses a mapping to associate task identifiers with their corresponding records.

### Contract Functions

**`createTask(string memory _content)`**

Creates a new task record and stores it in the smart contract.

Each new task receives an incremented identifier and an initial completion status of `false`.

**`taskCount()`**

Returns the total number of tasks created in the contract.

**`tasks(uint)`**

Provides access to a task record using its identifier through Solidity's public mapping getter.

### Initial Task

The contract constructor creates an initial task upon deployment:

```text id="5mekd2"
Create My First Task
```

This provides a starting record for demonstrating smart contract data retrieval.

### Contract Deployment

The project uses Truffle migrations to deploy its contracts.

| File | Purpose |
| --- | --- |
| `contracts/TodoList.sol` | Main task storage contract. |
| `contracts/Migrations.sol` | Tracks Truffle migration progress. |
| `migrations/1_initial_migration.js` | Deploys the Migrations contract. |
| `migrations/2_deploy_contracts.js` | Deploys the TodoList contract. |
| `truffle-config.js` | Configures the development network and compiler settings. |

## Tech Stack

| Technology | Purpose |
| --- | --- |
| Solidity | Smart contract development. |
| Ethereum | Blockchain platform for contract execution. |
| Truffle | Smart contract compilation and deployment. |
| Web3.js | JavaScript interaction with the Ethereum blockchain. |
| Truffle Contract | JavaScript abstraction for deployed contracts. |
| MetaMask | Browser wallet and Ethereum provider integration. |
| Ganache | Local Ethereum blockchain development environment. |
| JavaScript | Application logic and blockchain interactions. |
| HTML5 | User interface structure. |
| CSS3 | Application styling. |
| Bootstrap 4 | Responsive layout and interface components. |
| jQuery | DOM manipulation and interface updates. |
| Node.js and npm | Dependency and development tooling. |

## Project Structure

```text id="eswff2"
Blockchain-Todo-List-DApp/
├── build/
│   └── contracts/
│       ├── Migrations.json
│       └── TodoList.json
├── contracts/
│   ├── Migrations.sol
│   └── TodoList.sol
├── migrations/
│   ├── 1_initial_migration.js
│   └── 2_deploy_contracts.js
├── src/
│   ├── app.js
│   └── index.html
├── .gitignore
├── bs-config.json
├── package-lock.json
├── package.json
└── truffle-config.js
```

### Directory Descriptions

- **`contracts/`** contains the Solidity smart contracts defining the application's blockchain logic.
- **`migrations/`** contains JavaScript deployment scripts used by Truffle.
- **`build/contracts/`** stores compiled contract artifacts, including contract ABIs and deployment metadata.
- **`src/`** contains the frontend HTML and JavaScript files.
- **`truffle-config.js`** defines the Ethereum development network configuration.
- **`bs-config.json`** configures the local development web server.

## Getting Started

Follow these steps to run the application locally.

### Prerequisites

Install the following tools:

- [Node.js and npm](https://nodejs.org/)
- [Git](https://git-scm.com/)
- [Ganache](https://archive.trufflesuite.com/ganache/)
- [MetaMask](https://metamask.io/)

The repository uses the Truffle development toolchain and Solidity `0.5.0`.

Because the project uses an older Ethereum development stack, a compatible Node.js environment may be necessary.

### 1. Clone the Repository

Clone the project from GitHub:

```bash id="5vkyca"
git clone https://github.com/johncarlonas/Blockchain-Todo-List-DApp.git
```

Navigate into the project directory:

```bash id="n0x0w7"
cd Blockchain-Todo-List-DApp
```

### 2. Install Dependencies

Install the project's dependencies:

```bash id="dce32x"
npm install
```

The repository includes a `package-lock.json` file for dependency resolution.

Truffle and the other development tools are declared in the project's package configuration.

### 3. Configure Ganache

Launch Ganache and create or open a local Ethereum development workspace.

Configure the local blockchain connection to match `truffle-config.js`:

| Setting | Value |
| --- | --- |
| Host | `127.0.0.1` |
| Port | `7545` |
| Network | Local Ethereum development network |

The corresponding Truffle configuration is:

```javascript id="d69ca7"
development: {
  host: "127.0.0.1",
  port: 7545,
  network_id: "*"
}
```

Keep Ganache running while compiling and deploying the contracts.

### 4. Compile Smart Contracts

Compile the Solidity contracts:

```bash id="krnrge"
npx truffle compile
```

This generates or updates the compiled contract artifacts inside `build/contracts/`.

The generated artifacts contain information needed for frontend interactions with deployed contracts.

### 5. Deploy Smart Contracts

Run the Truffle migrations:

```bash id="4c142x"
npx truffle migrate --network development
```

To redeploy the contracts from the beginning, run:

```bash id="mufhw6"
npx truffle migrate --network development --reset
```

Truffle deploys the contracts to the configured local Ethereum network.

### 6. Configure MetaMask

Open MetaMask in your browser.

1. Add a custom network using the RPC URL `http://127.0.0.1:7545`.
2. Use the network's chain ID shown by Ganache.
3. Select the local network in MetaMask.
4. Import a Ganache test account if needed.
5. Connect the wallet to the local application.

Only use test accounts and credentials from your local Ganache workspace.

Never import a wallet containing real assets into an experimental development environment.

### 7. Start the Application

Run the local development server:

```bash id="d4rnjr"
npm run dev
```

The project uses `lite-server` to serve the frontend and compiled contract artifacts.

Open the local server address displayed in your terminal, typically:

```text id="tmem3e"
http://localhost:3000
```

Keep Ganache, the development server, and your Ethereum wallet available while interacting with the application.

## Available Commands

| Command | Description |
| --- | --- |
| `npm install` | Installs project dependencies. |
| `npm run dev` | Starts the local development server. |
| `npx truffle compile` | Compiles Solidity smart contracts. |
| `npx truffle migrate --network development` | Deploys contracts to the local blockchain. |
| `npx truffle migrate --network development --reset` | Reruns contract migrations. |
| `npx truffle console --network development` | Opens an interactive Truffle console. |
| `npm test` | Invokes the configured Mocha test command. |

## Interacting with the Smart Contract

The Truffle console can be used to inspect deployed contracts and interact with their public functions.

Start the console:

```bash id="sj6ldn"
npx truffle console --network development
```

### Retrieve the Deployed Contract

```javascript id="um0zgi"
const todoList = await TodoList.deployed();
```

### Read the Task Count

```javascript id="y5md6p"
const count = await todoList.taskCount();
console.log(count.toString());
```

### Retrieve a Task

```javascript id="0kbnsf"
const task = await todoList.tasks(1);
console.log(task);
```

### Create a New Task

```javascript id="g8e9cw"
await todoList.createTask("Learn Solidity");
```

### Verify the Updated Task Count

```javascript id="56w7by"
const updatedCount = await todoList.taskCount();
console.log(updatedCount.toString());
```

These commands demonstrate direct interaction with the smart contract through the local Ethereum network.

## Development Concepts Explored

This project introduced me to several important concepts in blockchain development.

### Smart Contracts

I learned how Solidity can be used to define structured data and functions that execute on a blockchain.

### Blockchain State

I explored how smart contracts maintain task information through state variables, structures, and mappings.

### Blockchain Transactions

I learned the difference between reading blockchain state and submitting transactions that modify it.

### Wallet Integration

I experimented with connecting a browser-based application to an Ethereum wallet and accessing blockchain functionality through a Web3 provider.

### Contract Deployment

I used Truffle migrations to compile and deploy contracts to a local Ethereum development environment.

### Decentralized Application Development

I explored how a traditional HTML, CSS, and JavaScript frontend can communicate with smart contracts instead of relying entirely on a conventional backend and database.

## Project Background

Blockchain Todo List DApp was my first project while exploring blockchain and decentralized application development.

I wanted to understand how blockchain applications work beyond cryptocurrency transactions, particularly how smart contracts can be used to manage application data.

A to-do list provided a simple starting point for learning Solidity, Ethereum contract deployment, Web3 integration, and browser-based wallet connectivity.

This project served as an introduction to the development workflow behind decentralized applications and helped me build a foundation for exploring more advanced blockchain concepts.

---

<div align="center">

**Blockchain Todo List DApp**

My first step into blockchain and Web3 development.

Developed by [John Carlo E. Nas](https://github.com/johncarlonas)

</div>
