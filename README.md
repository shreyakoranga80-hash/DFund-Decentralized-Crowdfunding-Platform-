# DFund - Decentralized Crowdfunding Platform

DFund is a decentralized crowdfunding platform (dApp) built to enable transparent, secure, and intermediary-free fundraising. By leveraging Ethereum smart contracts, DFund ensures that campaign creation, backer contributions, and fund tracking are handled entirely on-chain with absolute transparency.

## 🚀 Features

- **Immutable Campaigns:** Create and launch crowdfunding campaigns directly on the blockchain.
- **Secure Crowdfunding:** Contributions are held safely within smart contracts, removing the need for a traditional third-party coordinator.
- **Real-Time Blockchain Statistics:** Dynamically tracks and displays total campaigns, total backers, and total raised Ethereum directly on the interface.
- **Web3 Wallet Integration:** Seamless connection with MetaMask for signing and executing transactions securely.
- **Modern UI/UX:** A sleek, fully responsive user dashboard designed with React and Tailwind CSS.

---

## 🛠️ Tech Stack

- **Frontend:** React.js, Tailwind CSS
- **Blockchain/Backend:** Solidity, Hardhat, Ethers.js

---

## 📦 Project Structure

```text
├── src/                  # Main React frontend components and state
├── public/               # Static assets and entry HTML
├── scripts/              # Hardhat deployment scripts for smart contracts
├── hardhat.config.js     # Ethereum development environment configurations
├── tailwind.config.js    # Styling configurations
└── package.json          # Project dependencies and operational scripts

### Prerequisites
Ensure you have the following tools installed:
- [Node.js](https://nodejs.org/) (v16+ recommended)
- [MetaMask Extension](https://metamask.io/) added to your web browser

### Step 1: Clone & Install Dependencies
```bash
# Clone your repository
git clone [https://github.com/shreyakoranga80-hash/DFund-Decentralized-Crowdfunding-Platform-.git](https://github.com/shreyakoranga80-hash/DFund-Decentralized-Crowdfunding-Platform-.git)
cd DFund-Decentralized-Crowdfunding-Platform-

# Install the project packages
npm install

### Step 2: Fire Up the Local Blockchain (Hardhat Node)
Before deploying the contract, you must run a simulated Ethereum network locally. Open a **separate, dedicated terminal window** inside your project root folder and run:
```bash
npx hardhat node

### Step 3: Deploy the Smart Contracts Locally
Go back to your **original terminal window** (keep the node terminal running in the background) and run the deployment script:
```bash
npx hardhat run scripts/deploy.js --network localhost

### Step 4: Configure MetaMask for Localhost
To interact with your deployed contract, your browser wallet needs to point to your local chain and utilize test funds:
1. Open your **MetaMask Extension** and click the network selector in the top-left corner.
2. Click **Add Network** -> **Add a network manually** at the bottom.
3. Fill in the following exact network values:
   - **Network Name:** Hardhat Localhost
   - **RPC URL:** `http://127.0.0.1:8545`
   - **Chain ID:** `31337`
   - **Currency Symbol:** `ETH`
4. Save and switch to this network.
5. In MetaMask, click **Add Account** -> **Import Account**.
6. Copy one of the long **Private Key** strings printed inside your running Hardhat Node terminal (Step 2) and paste it here. Your account will instantly show `10,000 ETH` in play money.

### Step 5: Launch the Frontend Web Application

Now that the local blockchain backend is live and your wallet is configured, start the React development server:

```bash
npm start

