# hw_blockchain
Homework #18: Proof of Authority Development Chain

The **Proof of Authority (PoA)** algorithm is typically used for private blockchain networks as it requires pre-approval of, or voting in of, the account addresses that can approve transactions (seal blocks).

**What is Proof of Authority:** 
- Allows only specific addresses to mine/produce blocks in the network. 
- A centralized but cheap algorithm mainly used to power test networks. 
- Never used in production of mainnet blockchains, only for development and testing in testnet blockchains.

## Install MyCrypto Desktop App 

MyCrypto is a free, open-source, client-side interface that allows you to interact directly with the blockchain. For example it allows you to manage ethereum wallets and make transactions in the blockchain.

https://www.mycrypto.com

## Install Go Ethereum

Go Ethereum is one of the three original implementations of the Ethereum protocol. It is written in Go, fully open-source and licensed under the GNU LGPL v3. For example it allows us to create our very own blockchain, from the genesis block to mining tokens and making transactions.

https://geth.ethereum.org/downloads/

## Network Configuration

**What is a node?:** A participant in the network that maintains a full copy of the blockchain. 

**Chain ID:** 555

**Blocktime:** 15 (default) 

**Network Name:** homeworknet 

#### Node 1: 
node1 will be a full node that is also mining

**Public Address of the Key:** 
0x48562B2cD2ACE40Cf8488D1468327e8d060c01EB

**Path of the Secret Key File:** 
node1/keystore/UTC--2021-02-08T22-04-45.647146000Z--48562b2cd2ace40cf8488d1468327e8d060c01eb

**Password:** 
val********


#### Node 2: 
node2 will be a full node that exposes an RPC port, allowing you to talk to it with other apps like MyCrypto

**Public Address of the Key:** 
0xdc95e5FDfC03597F8B84c2ade5B5E67e612f68D5

**Path of the Secret Key File:** 
node2/keystore/UTC--2021-02-08T22-07-12.515546000Z--dc95e5fdfc03597f8b84c2ade5b5e67e612f68d5

**Password:** 
val********


#### Enode from Node 1: 
enode://86ce5caa1bf8a326aa438b029011a16383e140abdc30ce2666eabe6a0e04546070ff9dde9d83793cb061b6ff819eec2658533217c8bdd056bb59417b8dd84cd0@127.0.0.1:30303

### Connecting to MyCyrpto 
Refer to Connecting_to_MyCyrpto.mov and to Sending_Transactions.mov to learn how to connect your 

### geth Flags
- The **--mine** flag tells the node to mine new blocks.
- The **--minerthreads** flag tells geth how many CPU threads, or "workers" to use during mining. Since our difficulty is low, we can set it to 1.
- The **--bootnodes** flag allows you to pass the network info needed to find other nodes in the blockchain. This will allow us to connect both of our nodes.
- The **--rpc** flag enables us to talk to our second node, which will allow us to use MyCrypto or Metamask to transact on our chain.
