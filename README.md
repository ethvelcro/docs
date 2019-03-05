# [DEPRECATED]

This repo was created for the ETHDenver 2019 Hackathon.  We're keeping this available for historical purposes.

The project has been rebranded as Notus.  You can refer to the new Notus node [Github project](https://github.com/NotifyUs/notus-docs).

# Velcro Platform

Velcro allows you to listen to the Ethereum blockchain with webhooks.

# User Flow

1. A user uses the Dapp to define a query and bind it to a URL.  The data is stored in IPFS and the hook is registered in a smart contract.
2. A Velcro node polls the smart contract, and runs the queries.  If data is present, the URL for the query is called.
3. The URL endpoint could trigger SMS, trigger a Slack notification, serve as an Oracle, or anything you can dream of.

# Components

The system consists of a dapp, a smart contract, a Velcro Node, IPFS, and the Graph Protocol.

## Dapp

Allows users to interact with the Velcro smart contract and offers a human friendly interface to setup queries.

## Smart Contract

The Velcro smart contract is where users registers their queries and the URL endpoints they communicate with.  The query definition is stored in IPFS and the hash is recorded in the contract.

## IPFS

Used to store the query definitions.

## Velcro Node

The Velcro node reads the query definitions from the smart contracts and triggers the URLs.

# docs
Documentation and repos for Velcro, the coolest way to attach query webhooks to the Ethereum blockchain

## components

### dApp

[velcro-dapp](https://github.com/ethvelcro/velcro-dapp)

Public: https://velcro.netlify.com/

### contracts

[velcro-contracts](https://github.com/ethvelcro/velcro-contracts)

Main Contract Address: `0xeb458b030d6be178e301910f7077955574bb7be4`

### hook processor

[velcro-node](https://github.com/ethvelcro/velcro-node)

Docker Image: https://hub.docker.com/r/ethvelcro/velcro-node

Public: https://api.ethvelcro.network and `wss://api.ethvelcro.network`

## modes
The Velcro stack can run in one of two modes:
 - Using the public dApp with the hosted stack (easy!)
 - Deploying your own copy of the dApp, contract, and processor using instructions in those repos (harder, more control)
