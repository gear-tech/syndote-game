<p align="center">
  <a href="https://gear-tech.io">
    <img src="https://github.com/gear-tech/gear/blob/master/images/logo-grey.png" width="400" alt="GEAR">
  </a>
</p>
<p align=center>
    <a href="https://github.com/gear-tech/gear-js/blob/master/LICENSE"><img src="https://img.shields.io/badge/License-GPL%203.0-success"></a>
</p>
<hr>

## Description

React application of [Syndote](#) based on [Rust smart-contract](#).

## Getting started

### Install packages:

```sh
yarn install
```

### Declare environment variables:

Create `.env` file, `.env.example` will let you know what variables are expected.

In case of issues with the application, try to switch to another network or run your own local node and specify its address in the `.env` file. When applicable, make sure the smart contract(s) wasm files are uploaded and running in this network accordingly.

In REACT_APP_SYNDOTE_NODE_ADDRESS var put 
```
wss://node-workshop.gear.rs
```
or if you launch local node
```
ws://localhost:9944
```

In REACT_APP_CONTRACT_ADDRESS var put Syncdote programm address which was deployed.

In order for all features to work as expected, the node and it's runtime version should be chosen based on the current `@gear-js/api` version.

### Set up file with metadata

Copy syndote.meta.wasm file from built program to `frontend/src/assets/wasm`

### Run the app:

```sh
yarn start
```

### Docker 

build

    docker build --rm --no-cache -t syndote:latest .

run

    docker run --rm  -p 8080:80  --name syndote syndote:latest


