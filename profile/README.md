# Navigation

- [Projects](https://github.com/Super-Sonic-Validator#porjects)

- [Examples of work](https://github.com/Super-Sonic-Validator#examples-of-work)

- [Contacts](https://github.com/Super-Sonic-Validator#contacts)

# About Super Sonic team

As the blockchain landscape continues to evolve, so too will the challenges and opportunities it presents. At Super Sonic, we are committed to staying at the forefront of industry developments, continually enhancing our services and adopting the latest technologies. Our vision is to be a trusted partner for blockchain projects around the world, contributing to a secure, transparent, and decentralized digital future.

![image](https://github.com/Super-Sonic-Validator/.github/assets/175025803/fea5105a-209c-4d58-ba11-0aaac416398f)

# Porjects

We have been involved in projects such as 

- SGE
- Kujira
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

## Dill Node
```
#Update your server
sudo apt update && sudo apt upgrade -y

#Install Dependencies
sudo apt install build-essential git curl jq docker.io -y

#Install Go
wget https://golang.org/dl/go1.20.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.20.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
go version

#Install Docker Compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

#Clone the Dill Repository
git clone https://github.com/DillProject/dill-node.git
cd dill-node

#git clone https://github.com/DillProject/dill-node.git
cd dill-node

#Build the Dill Node
make build
./dilld version

#Initialize the Validator
./dilld init Supersonic --chain-id=dill-mainnet

#Configure Node Settings
#Edit the configuration files located in $HOME/.dilld/config/. Update the config.toml and app.toml for optimal performance. Here are some recommendations:
#Increase max_num_inbound_peers and max_num_outbound_peers.
#Configure your external IP under the p2p section.

#Download Genesis File
curl -s https://raw.githubusercontent.com/DillProject/mainnet/master/genesis.json > $HOME/.dilld/config/genesis.json

#Start the Dill Node
./dilld start

#Create and Fund Your Validator
./dilld keys add SupersonicWallet

#Create the Validator
./dilld tx staking create-validator \
  --amount=1000000udill \
  --from=SupersonicWallet \
  --commission-rate="0.10" \
  --commission-max-rate="0.20" \
  --commission-max-change-rate="0.01" \
  --min-self-delegation="1" \
  --pubkey=$(./dilld tendermint show-validator) \
  --moniker="Supersonic" \
  --chain-id=dill-mainnet

#Confirm Validator Status
./dilld query staking validator $(./dilld tendermint show-validator)

#Maintain Your Validator
journalctl -u dilld -f

```
More can be viewed in our [gitbook](https://super-sonic.gitbook.io/supersonic/aleo-deploy-dapp)

# Contacts

[Twitter](https://twitter.com/supsonic_team) | [GitBook](https://super-sonic.gitbook.io/supersonic) | [KeyBase](https://keybase.io/supsonic)

Mail | rachelaszdertg@gmail.com

Discord | super.sonic.
