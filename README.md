# NFT Marketplace 
This is a decentralized NFT marketplace built using Solidity, Hardhat, Next.js, and Graph for listening to API calls.

[img](https://i.ibb.co/yq5ZZXC/marketplace.png)

## Live Link


## Overview
The NFT marketplace allows users to buy and sell non-fungible tokens (NFTs) using Ethereum. Users can connect their Ethereum wallet to the marketplace, view a list of available NFTs, and purchase them using ETH.

The marketplace also allows users to create their own NFTs by uploading images and descriptions, setting a price, and listing the NFT for sale.

##Technologies Used
1.Solidity: The programming language used for writing smart contracts on Ethereum.
2.Hardhat: An Ethereum development environment that helps developers write, test, and deploy smart contracts.
3.Next.js: A React framework for building server-side rendered web applications.
4.Graph: A platform for building and querying decentralized APIs.

## To Run First Deploy The Contract

*I have Used Sepolia network You can use your own network and can change in `Contracts - Hardhat/helper-hardhat`.*

## 1. Git clone the repo

In it's own terminal / command line, run: 

```
git clone https://github.com/Vswaroop04/SoliGraph-NFT-Marketplace/
cd SoliGraph-NFT-Marketplace
yarn
cd Contracts - Hardhat
yarn
cd Thegraphbackend
yarn
```

## 2. Deploy to sepolia 

After installing dependencies, deploy your contracts to sepolia:

```
cd Contracts - Hardhat
yarn hardhat deploy --network sepolia
```

## 3. Deploy your Own subgraph or Use My graph

## For Creating Your Own Subgraph
You can go to [Subgraph](https://thegraph.com/studio/) and can create a new subgraph and give the link of it in .env of root before that 

```
cd ..
cd Thegraphbackend
graph init --studio <Subgraphname>
graph auth --studio 
graph codegen && graph build
graph deploy --studio <Subgraphname>
```

Then, make a `.env` file and place your temporary query URL into it as `NEXT_PUBLIC_SUBGRAPH_URL`.


## 4. Start your UI

Make sure that:
- In your `networkMapping.json` you have an entry for `NftMarketplace` on the sepolia network. 
- You have a `NEXT_PUBLIC_SUBGRAPH_URL` in your `.env` file. 

```
yarn dev
```
<p align="center">
  Made with ❤ by Vishnu
</p>
