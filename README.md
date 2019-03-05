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
