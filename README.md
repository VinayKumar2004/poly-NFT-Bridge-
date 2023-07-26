# poly-NFT-Bridge-
in this project, an NFT collection is to be deployed on the goerli network, Map the collection to Polygon, and Transfer assets to mumbai network using Polygon Bridge.

## Table of Contents
### Project Overview
- Prerequisites
- Installation
- Usage
- Deployment
- Testing
- License
  
### Prerequisites

Node.js (>=12.x)
npm (>=6.x)
Hardhat (>=2.x)
Polygon (Mumbai Testnet) Account and MATIC Tokens for gas fees

IPFS account and API key for storing images

Installation

Clone the repository:
```git clone https://github.com/VinayKumar2004/poly-NFT-Bridge-```
cd your-nft-project
Install the dependencies:
npm install
Set up environment variables:

### makefile
# Create a .env file and add the following variables:
PRIVATE_KEY=your-private-key-for-wallet
RPC_URL=your-rpc-url-for-Goerli
PINATA_API_KEY=your-pinata-api-key
PINATA_SECRET_API_KEY=your-pinata-secret-api-key
Usage

### Generate NFT Images:

Use DALLE 2 or Midjourney to create five unique images and store them on IPFS using the Pinata service.
Deploy the ERC721 Contract:

### Deploy the ERC721 contract on the Goerli Ethereum Testnet using Hardhat.
Map the deployed contract to the Polygon network using the Polygon token mapper.
Mint NFTs:

Use the Hardhat script to batch mint all NFTs based on the generated images and metadata stored on IPFS.
Transfer NFTs to Polygon:

Use the Hardhat script to approve and transfer the NFTs to the Polygon Mumbai Testnet via the FxPortal Bridge.
Deploying to Goerli Ethereum Testnet:

npx hardhat run scripts/deploy.js --network goerli

npx hardhat run scripts/batchMint.js --network goerli

npx hardhat run scripts/approvedDeposit.js --network goerli

### Mapping the contract to Polygon Network:
Get Polygon (Matic) Wallet:

To interact with the Polygon token mapper, you need a Polygon wallet that holds MATIC tokens to cover the gas fees for the mapping process. If you don't have one already, create a wallet on the Polygon Mumbai Testnet. You can get testnet MATIC tokens from the Polygon Faucet.
Deploy Your ERC721 Contract to Goerli Ethereum Testnet:

Before mapping, you need to deploy your ERC721 contract to the Goerli Ethereum Testnet. Make sure your contract is correctly deployed and functional on the testnet.
Obtain Contract Address on Goerli Testnet:

Get the address of your deployed ERC721 contract on the Goerli Ethereum Testnet. This is the contract that you want to map to the Polygon network.
Go to the Polygon Token Mapper Website:

Access the Polygon token mapper website: https://mapper.matic.today/
Connect Your Polygon (Matic) Wallet:

Connect your Polygon wallet to the Polygon token mapper website by clicking on "Connect Wallet" and selecting your wallet provider.
Initiate the Mapping:

Click on the "Map Your Token" button on the Polygon token mapper website.
Enter Contract Details:

Fill in the required details on the mapping page:
Source Network: Select "Ethereum Goerli Testnet" as the source network.
Target Network: Select "Matic Mumbai Testnet" as the target network.
Token Name: Enter the name of your ERC721 token.
Token Symbol: Enter the symbol for your ERC721 token (e.g., NFT).
Token Address: Paste the address of your deployed ERC721 contract on the Goerli Testnet.
Initiate Mapping Transaction:

After entering the contract details, click on "Map Token" to initiate the mapping transaction.
Confirm the Transaction:

Your wallet will prompt you to confirm the mapping transaction. Confirm the transaction and wait for it to be mined.
Mapping Confirmation:

Once the transaction is confirmed, you will receive a confirmation message on the Polygon token mapper website indicating that the mapping is successful.
Verify the Mapped Contract:

You can verify the mapped contract by clicking on "View on Explorer" on the Polygon token mapper website. This will take you to the Polygon explorer, where you can see your ERC721 contract on the Polygon Mumbai Testnet.
# Authors
Vinay Kumar (https://github.com/VinayKumar2004)

# License
This project is licensed under the MIT License - see the LICENSE.md file for details
