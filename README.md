# bloxbergNonAuthorityNodeSetup-nethermind

[Nethermind](https://github.com/NethermindEth/nethermind) client setup for a bloxberg non-Authority / monitoring node.

This node configuration does not validate / seal blocks, it is best suited for independent users who are not part of the bloxberg consortium but want to utilize their own node.

Network and client settings are already adjusted to run in the bloxberg network. [config.json](./nethermind/config.json) corresponds to a .toml configuration of the parity client. [bloxberg.json](./nethermind/bloxberg.json) is the same as the parity Validator node's [bloxberg.json](https://github.com/bloxberg-org/bloxbergValidatorSetup/blob/master/validator/bloxberg.json). [static-nodes.json](./nethermind/static-nodes.json) is the Nethermind version of the Validator node's [bootnodes.txt](https://github.com/bloxberg-org/bloxbergValidatorSetup/blob/master/validator/bootnodes.txt).

## Requirements

* A Linux Server, preferably (Tested on Ubtuntu 20.04 LTS)
* Minimum 2 Cores CPU
* Minimum 4 GB RAM
* 100 GB of SSD storage

## Setup

- Install [docker](https://docs.docker.com/engine/install/ubuntu/) with [docker-compose-plugin](https://docs.docker.com/compose/install/)
- Clone this repository
- mkdir -p ./nethermind/db/bloxberg
- mkdir ./nethermind/keystore
- mkdir ./nethermind/logs

## Run

Run the client by `docker compose -p nethermind -f nethermind.yml up`

Ensure it is syncing and then you can close it with Ctrl+C.

To run in the background `docker compose -p nethermind -f nethermind.yml up -d`

