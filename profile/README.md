# Navigation

- [Projects](https://github.com/Super-Sonic-Validator#porjects)

- [Examples of work](https://github.com/Super-Sonic-Validator#examples-of-work)

- [Contacts](https://github.com/Super-Sonic-Validator#contacts)

# About Super Sonic team

As the blockchain landscape continues to evolve, so too will the challenges and opportunities it presents. At Super Sonic, we are committed to staying at the forefront of industry developments, continually enhancing our services and adopting the latest technologies. Our vision is to be a trusted partner for blockchain projects around the world, contributing to a secure, transparent, and decentralized digital future.

![image](https://github.com/Super-Sonic-Validator/.github/assets/175025803/fea5105a-209c-4d58-ba11-0aaac416398f)

# Porjects

We have been involved in projects such as 

- 0G
- Babylon
- Aleo
- Omni Network
- ZetaChain

and many others

# Examples of work

## 0G Node Setup and Management

Our team, Super Sonic, has extensive experience in setting up and managing nodes for various blockchain projects. One of our notable projects is our work with the 0G blockchain. Here are some highlights of our contributions, along with code examples:

**1. Initial Node Setup:** 

We successfully set up a full node for the 0G blockchain, ensuring that all configurations adhered to the best practices and security standards. Here is an example of our node configuration script:

```
#!/bin/bash
# Script to install and configure 0G node

# Update and install dependencies
sudo apt-get update
sudo apt-get install -y build-essential git wget

# Clone the 0G repository
git clone https://github.com/0GNetwork/0G.git
cd 0G

# Build the node software
make install

# Initialize the node
ogd init "Super Sonic Node"

# Download the genesis file
wget -O $HOME/.ogd/config/genesis.json "https://raw.githubusercontent.com/0GNetwork/0G/main/genesis.json"

# Configure the node (example of configuring the persistent peers)
PEERS="node1@10.0.0.1:26656,node2@10.0.0.2:26656"
sed -i.bak -e "s/^persistent_peers *=.*/persistent_peers = \"$PEERS\"/" $HOME/.ogd/config/config.toml

# Start the node
ogd start

```
More can be viewed in our [gitbook](https://super-sonic.gitbook.io/supersonic/0g-node-setup-and-management)

## Aleo Deploy dApp

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

apt install cargo

git clone https://github.com/AleoHQ/leo

cd leo

cargo install --path .

leo account import SUPERSONIC_PRIVATE_KEY

leo example

leo example lottery

cd lottery

leo run play

git init -b main

git add .

git config --local user.email "rachelaszdertg@gmail.com"

git commit -m "any message"

git branch -m main
git remote add origin YOUR_REPOSITORY_URL
git remote -v
git push -u origin main

branch 'main' set up to track 'origin/main'

```
More can be viewed in our [gitbook](https://super-sonic.gitbook.io/supersonic/aleo-deploy-dapp)

# Contacts

[Twitter](https://twitter.com/supsonic_team) | [GitBook](https://super-sonic.gitbook.io/supersonic) | [KeyBase](https://keybase.io/supsonic)

Mail | rachelaszdertg@gmail.com

Discord | super.sonic.
