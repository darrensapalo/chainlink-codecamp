# Chainlink codecamp

The following are some useful information to support the chainlink codecamp.

## Terminologies

### Basic

**1. What is Metamask?**

MetaMask is a software cryptocurrency wallet used to interact with the Ethereum blockchain. It allows users to access their Ethereum wallet through a browser extension or mobile app, which can then interact with decentralized applications on the web.

**2. What is a wallet address?**

A wallet address is like an account number for a bank account. It is a unique string of characters that represents the destination for a cryptocurrency transaction. For example, if you're sending or receiving Bitcoin, Ether, or any other type of cryptocurrency, you'll need to send it to a specific wallet address.

**3. What is Chainlink?**

Chainlink is a decentralized oracle network that enables smart contracts on Ethereum to securely connect to external data sources, APIs, and payment systems.

**4. What is an oracle network?**

In the context of web3 and blockchain technology, an oracle network is a system that provides smart contracts with data from the real world. Smart contracts on blockchains like Ethereum are autonomous and deterministic, meaning they can only handle data that exists within the blockchain. However, for many applications, it's necessary to use data from the outside world, such as price information, weather data, or the result of a sports game. This is where oracles come in.

An oracle is a service that sends real-world data to the blockchain so that smart contracts can use this data in their computations. However, relying on a single oracle could introduce a point of failure or potential manipulation. To mitigate this risk, an oracle network is used.

An oracle network is a group of multiple oracles that work together to deliver reliable and trustworthy data to the blockchain. The data provided by each oracle in the network is aggregated and processed to produce a result that is resistant to manipulation and is more reliable than data from a single source.

Chainlink is a notable example of an oracle network. It's a decentralized network that allows smart contracts on Ethereum to securely connect to various external data sources, APIs, and payment systems.

**5. What is a Testnet?**

A testnet is an alternative blockchain used by developers for testing. It operates just like the main blockchain (also known as mainnet) but its currency has no value, allowing developers to experiment without worrying about breaking the mainchain or losing money.

**6. What is the MATIC token?**

MATIC is the native utility token of the Polygon network, a platform for Ethereum scaling and infrastructure development. It is used for a variety of purposes including payment for transaction fees and participation in the proof-of-stake consensus.

**7. In the context of web3 and wallet addresses, what is a private key?**

A private key in the context of web3 and wallet addresses is a secret number that allows cryptocurrency to be spent. Every crypto wallet address is associated with a private key, and whoever knows this key has control over the associated funds. It's critically important to keep this key secret.

**8. In the context of web3, what is a faucet?**

A faucet in the context of web3 is a service that provides free tokens for testnet testing. Developers can request tokens from these faucets to use in their projects while they're in the testing phase.

**9. In metamask, what's the difference between an Asset (fungible tokens) and NFTs (non-fungible tokens)?**

In MetaMask, an asset or fungible token represents a type of cryptocurrency that can be divided and each individual unit is equivalent to every other unit. Ether and many other tokens fall into this category. Non-fungible tokens (NFTs), on the other hand, are unique and cannot be replaced with something else. NFTs are used to create verifiable digital scarcity, as well as digital ownership, and the possibility of asset interoperability across multiple platforms.

### Intermediate

**10. What is Solidity?**

Solidity is an object-oriented programming language for writing smart contracts. It is used for implementing smart contracts on various blockchain platforms, most notably, Ethereum.

**11. What is Alchemy?**

Alchemy is a blockchain development platform that provides tools and infrastructure services for developers building on Ethereum. It provides reliable APIs and other services to help developers create and operate decentralized applications more efficiently.

**12. What is Polygon?**

Polygon (previously Matic Network) is a layer 2 scaling solution for Ethereum that aims to provide faster and cheaper transactions on Ethereum using Layer 2 sidechains, which are blockchains that run alongside the Ethereum main chain. Users can deposit Ethereum tokens to a Polygon bridge contract, interact with them within Polygon, and then later withdraw them back to the Ethereum main chain if necessary.

**13. What is Chainlink Functions? What is it for?**

Chainlink Functions provides smart contracts with access to a trust-minimized compute infrastructure. This means that a smart contract sends code to a Decentralized Oracle Network (DON), and each oracle within the DON runs the code in a serverless environment, aggregating all the independent runs and returning the final result to the smart contract. The code can range from simple computation to fetching data from API providers. Chainlink Functions can be used to connect to any public data, transform it before consumption, connect to password-protected data sources, external decentralized databases, or even to Web2 applications, among other possibilities.

[Source](https://docs.chain.link/chainlink-functions)

**14. What is a Zeppelin Contract Wizard?**

The Zeppelin Contract Wizard is an interactive tool developed by OpenZeppelin for building a contract using components from OpenZeppelin Contracts. It allows you to select the type of contract you want (with current support for ERC20 and ERC721), set parameters and desired features such as token name, symbol, premint amount, access control, etc., and the Contract Wizard will generate the necessary code. The generated code can then be compiled and deployed, or used as a starting point and customized with application-specific logic. Once the code is complete, there are several options for how to proceed with it, such as copying to clipboard, downloading it, or opening it in Remix IDE. The tool can pull OpenZeppelin Contracts from an npm dependency, but it also provides an option to work without npm, generating a ZIP file containing the generated code and all the necessary files from OpenZeppelin Contracts

[Source](http://blog.openzeppelin.com/wizard)

**15. What does VRF mean?**

VRF stands for Verifiable Random Function. In the context of blockchains and smart contracts, a VRF is a function that generates a random number that is verifiable on-chain. This is important for certain applications like gaming, lottery, and other use cases where a random outcome needs to be proven to be fair and unbiased. One well-known implementation of VRF is provided by Chainlink, which provides a provably-fair and verifiable source of randomness for smart contracts on Ethereum and other blockchains.

**16. What is the Request and Receive cycle?**

Random values cannot be reference data found on the blockchain. If the result of randomness is stored on-chain, any actor could retrieve the value and predict the outcome. Instead, randomness must be requested from an oracle, which generates a number and a cryptographic proof. Then, the oracle returns that result to the contract that requested it. 

In Chainlink, this sequence is known as the Request and Receive cycle.

**17. How are VRFs funded on Chainlink?**

VRF requests receive funding from subscription accounts. The Subscription Manager lets you create an account and pre-pay for VRF requests, so that funding of all your application requests are managed in a single location. To learn more about VRF requests funding, see Subscriptions limits.

[Source](https://docs.chain.link/getting-started/intermediates-tutorial/)