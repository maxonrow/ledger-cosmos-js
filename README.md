# ledger-mxw-js a fork from @zondax/ledger-cosmos-js

This package provides a basic client library to communicate with a Mxw App running in a Ledger Nano S/S+/X devices

We recommend using the npmjs package in order to receive updates/fixes.

# Available commands

| Operation            | Response                    | Command                     |
| -------------------- | --------------------------- | --------------------------- |
| getVersion           | app version                 | ---------------             |
| publicKey            | pubkey                      | path (legacy command)       |
| getAddressAndPubKey  | pubkey + address            | path + ( showInDevice )     |
| showAddressAndPubKey | signed message              | path                        |
| appInfo              | name, version, flags, etc   | ---------------             |
| deviceInfo           | fw and mcu version, id, etc | Only available in dashboard |
| sign                 | signed message              | path + message + (HRP)      |

getAddress command requires that you set the derivation path (account, change, index) and has an option parameter to display the address on the device. By default, it will retrieve the information without user confirmation.

# Testing with real devices

It is possible to test this package with a real Ledger Nano device. To accomplish that, you will need to follow these steps:

- Install the application in the Ledger device
- Install the dependencies from this project
- Run tests

```shell script
yarn install
yarn test:integration
```
