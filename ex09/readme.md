# Blockchain

## Objectives
* Initialize Blockchain
* Create Keys
* Configure Node
* Declare Persistent Data
* Create Schema
* Define Transactions
* Implement API
* Define and then Run Service
## TO DO
Add necessary dependencies to your Cargo.toml:
```
[package]
name = "cryptocurrency"
version = "0.1.0"
authors = ["Your Name <your@email.com>"]

[dependencies]
iron = "0.5.1"
bodyparser = "0.7.0"
router = "0.5.1"
serde = "1.0"
serde_json = "1.0"
serde_derive = "1.0"
exonum = "0.1.0"
```
We need to import crates with necessary types. Edit your src/main.rs:
```
extern crate serde;
extern crate serde_json;
#[macro_use] extern crate serde_derive;
#[macro_use] extern crate exonum;
extern crate router;
extern crate bodyparser;
extern crate iron;

use exonum::blockchain::{self, Blockchain, Service, GenesisConfig,
                         ValidatorKeys, Transaction, ApiContext};
use exonum::node::{Node, NodeConfig, NodeApiConfig, TransactionSend,
                   ApiSender, NodeChannel};
use exonum::messages::{RawTransaction, FromRaw, Message};
use exonum::storage::{Fork, MemoryDB, MapIndex};
use exonum::crypto::{PublicKey, Hash};
use exonum::encoding;
use exonum::api::{Api, ApiError};
use iron::prelude::*;
use iron::Handler;
use router::Router;
```

Then you should work with other objectives

In the end you should have fully functional Exonum blockchain with two wallets and be able to transfer some money between them
