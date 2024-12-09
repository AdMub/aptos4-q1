#### NFT Marketplace Backend on Aptos Blockchain
### Introduction
Welcome to the NFT Marketplace Backend project! This initiative is designed to guide developers in building a decentralized NFT marketplace backend using the Aptos blockchain and the Move programming language. Through this project, you will gain practical experience in implementing essential NFT marketplace functionalities such as minting, listing, purchasing, and transferring NFTs while ensuring secure, efficient, and transparent transactions.


### Learning Outcomes
By completing this project, you will:

Define and set up a Move module for managing an NFT marketplace on the Aptos blockchain.

Create and manage NFT structures, including attributes like rarity, ownership, and metadata.


Implement core marketplace functionalities:
      Minting NFTs.
      Listing NFTs for sale.
      Purchasing and transferring NFTs.
      Managing marketplace fees and secure ownership transfers.


Retrieve and filter NFTs based on attributes like rarity and sale status.


### Prerequisites
Before starting, ensure you have:

Basic knowledge of blockchain technology, the Aptos ecosystem, and Move programming.
Familiarity with tools like GitHub, VSCode, and terminal commands.
A working Linux or macOS environment, or access to GitHub Codespaces for Windows users.



### Project Setup

## Step 1: Setting Up Petra Wallet


Install the Petra Wallet browser extension.

Set up your wallet and securely save the seed phrase.

Switch to the Aptos Devnet under Settings > Network > Devnet.

Use the Faucet to get free test APT tokens.

Note: If Petra Wallet faces issues, consider alternatives like Pontem Wallet or Nightly Wallet.

## Step 2: Developer Environment Setup

Cloud Environment (GitHub Codespaces)
Fork the repository and open it in GitHub Codespaces:

# Install Aptos CLI:

curl -fsSL "https://aptos.dev/scripts/install_cli.py" | python3
aptos info  # Verify installation

# Local Environment (Linux/macOS)

# Clone the repository:

git clone https://github.com/your_username/aptos4-q1
cd aptos4-q1

## Install the Aptos CLI using the command above.


### Step 3: Configuring the Project

Open Move.toml and set your marketplace address:

[addresses]
NFTMarketplace = "your-marketplace-address-here"

# Replace "your-marketplace-address-here" with your Petra Wallet address.

# Add the following dependencies to Move.toml:

[dependencies]
AptosFramework = { git = "https://github.com/aptos-labs/aptos-core.git", subdir = "aptos-move/framework/aptos-framework", rev = "main" }
AptosStdlib = { git = "https://github.com/aptos-labs/aptos-core.git", subdir = "aptos-move/framework/aptos-stdlib", rev = "main" }
MoveStdlib = { git = "https://github.com/aptos-labs/aptos-core.git", subdir = "aptos-move/framework/move-stdlib", rev = "main" }


### Core Functionalities


## NFT Structures

# Key structures:

NFT: Attributes include ID, owner, name, description, URI, price, for-sale status, and rarity.

Marketplace: A collection of all NFTs managed as a vector.

ListedNFT: Simplified structure for sale listings.

# Marketplace Functions

Initialize the marketplace.

Mint new NFTs with unique attributes.

List NFTs for sale and set prices.

Purchase NFTs with secure ownership transfer and marketplace fee deductions.

Update prices and retrieve NFT details.

## Compiling and Publishing


# Step 6: Publishing the Contract

Initialize the Aptos project:

aptos init

Publish the Move module:

aptos move publish --package-dir . --named-addresses NFTMarketplace=<your-marketplace-address>

## Verify the deployment on Aptos Explorer.


## Step 7: Initializing the Marketplace

Use the Aptos Explorer to connect your wallet and initialize the marketplace.

Approve the transaction in your wallet.

Minting the First NFT


## Step 8: Minting and Verification

Use the mint_nft function in the Run tab of the NFTMarketplace module on Aptos Explorer.

Verify the minted NFT by retrieving its details in the View tab using get_all_nfts_for_owner.

# Key Features

Dynamic NFT Attributes: Supports rarity and metadata for enhanced engagement.

Marketplace Fee Management: Applies a transaction fee automatically.

Secure Ownership Transfers: Ensures secure and authorized transactions.


## Additional Resources

Aptos Dev Docs

Move Language Guide


## Conclusion

For technical assistance, join the StackUp Discord and ask your questions in the #aptos-helpdesk channel.

@ Stackup "https://earn.stackup.dev/campaigns/move-on-aptos-iv/quests/quest-1-building-an-nft-marketplace-dapp-backend-5510"

