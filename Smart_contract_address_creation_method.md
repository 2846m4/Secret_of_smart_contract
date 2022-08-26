Smart contract address creation method & difference between smart contract address and wallet address (EOA).

In this article, I will cover 3 essential questions, as a smart contract developers, we need to know how things work.

How many types of addresses does Ethereum have?
2. How was the smart contract address created?

3. Difference between smart contract address and EOA address?

Let’s start with a question.

1. How many types of address does Ethereum has?

Ethereum has two types of address,

Smart contract address
Wallet address or EOA.
Metamask account address is called wallet address or EOA for understanding.

2. How smart contract address created?

There is two method to create a smart contract address in Ethereum.

Each smart contract identifies in the blockchain by its address. This address is a long series of numbers and characters. It starts with 0xba… But the question is how this 0xba is computed.

Smart contract code deployed on the blockchain it is part of the transaction. When we deploy a smart contract on the blockchain, we need a wallet address so that the flow will be

Methode 1 . Wallet address => Transaction => Smart contract.

When we execute any transaction in the Ethereum network, it will increment a number called the Nonce. So smart contract address determine by its wallet address and Nonce.


So the conclusion is Nonce and sender address are put in the array and then using rlp. Encode () mechanism, after rlp.encode () operation result, hash it with sha3 () function and it will give 32 Bytes of data. the smart-contract address uses the last 20 Bytes of data of hashing.


Methode 2. Another way to create a smart contract address is using an opcode called CREATE2.

This CREATE2 depends on the sender address and code of contracts to create a smart contract address. It this not so papular to create a smart contract address.

3. Difference between smart contract address and EOA address?

Smart contract address: Smart contract address uniquely identify smart contract on the blockchain. Each smart contract address is associated with four different fields.

Nonce: Nonce is an integer that is incremented every time the address sends any transaction. So after the smart contract deploys that time Nonce = 0, then after the smart contract sends the first transaction nonce will increment to 1, and then so on.
Balance: if we send ether balance to smart contract its ether balance increase, and if a smart contract is sent to another address its ether balance decrease.
Code: when we program a smart contract in solidity this code goes to the store code field on the blockchain.
Data: where all the storage variables of the smart contract go to store. It’s very important that the memory variables can’t store in the blockchain.
Externally Owned Address (EOA): When we are creating an account in metamask or other Ethereum wallet it’s called EOA address. The big difference between EOA and smart contract address is EOA address has an associated private key to sign the transaction. So in smart contract address does not have any private key. Smart contract address only can do is react to incoming transactions that execute some of the smart contract functions.

EOA address also has 4 fields.

Nonce: Nonce is an integer that is incremented every time the address send any transaction
Balance: balance will increase/depress demand on send and receive.
Code : empty
Data: empty
Reference: 1. https://blog.smartdec.net/how-to-define-smart-contract-address-before-the-deploy-create2-use-case-for-decentralized-exchange-52b7daa7873b

2. https://www.zastrin.com/courses/ethereum-primer/lessons/2-4

3. https://eth.wiki/en/fundamentals/rlp

Join Coinmonks Telegram Channel and Youtube Channel learn about crypto trading and investing

Also, Read
Binance vs FTX | Best (SOL) Solana Wallets
How to Swap Crypto on Uniswap? | A-Ads Review
Cryptocurrency Savings Accounts | YoBit Review
Botsfolio vs Napbots vs Mudrex | Gate.io Exchange Review
CoinFLEX Review | AEX Exchange Review | UPbit Review
AscendEx Margin Trading | Bitfinex Staking | bitFlyer Review
Bitget Review | Gemini vs BlockFi cmd| OKEx Futures Trading
AscendEx Staking | Bot Ocean Review | Best Bitcoin Wallets
