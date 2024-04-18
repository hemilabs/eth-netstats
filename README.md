# Ethereum Network Stats with POA and POW support

This is a visual interface for tracking proof-of-work ("mainnet") and proof-of-authority ("testnet") network status. It uses WebSockets to receive stats from running nodes and output them through an angular interface. It is the front-end implementation for [ethstats-client](https://github.com/goerli/ethstats-client).

## Proof-of-Authority

![Screenshot](src/images/screenshot-poa.png "Screenshot POA")

## Installation

Make sure you have node.js and npm installed.

Clone the repository and install the dependencies:

```bash
git clone https://github.com/goerli/ethstats-server
cd ethstats-server
npm install
```

## Build

In order to build the static files you have to run grunt tasks which will generate dist directories containing the js and css files, fonts and images.

```bash
grunt poa
```

## Configuration

Set the following environment variables:

* `WS_SECRET`: Server secret.

## Run

```bash
docker run --env-file .env --interactive --publish 3000:3000 --rm --tty hemilabs/ethstats-server:master
```
