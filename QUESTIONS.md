# Overview of work

1. Reviewed, updated, and completed the whole setup instructions.
2. Performed tutorials 1-3 (deploy a smart contract on Remix IDE, data feeds tutorial, VRF game of thrones tutorial)


# Broad Questions

## 1. What is the expected completed work from the attendees?

🤔 Which parts are required and which parts are optional?

- (Required?) Running the Javascript that performs APY calculation
- (Optional?) Customizing their own smart contract via Open Zeppelin
- etc.

# Morning

The following are what we expect to accomplish on the AM session (9:30-11:00 AM). 

[Source](https://github.com/QingyangKong/Chainlink-bootcamp-day1)

- Learn to use Remix IDE
- Use OpenZepellin to define your own smart contract (opened on Remix IDE)
- Save the workshop attendee's progress on the Remix IDE

# Afternoon 

The following are what we expect to accomplish on the PM session (1:00-4:00 PM).

[Source](https://github.com/QingyangKong/Chainlink-bootcamp-day2)

- Load existing progress from Remix IDE to local machine VS Code
- Build a dynamic NFT that has its metadata updated from real world data off the blockchain (e.g. AccuWeather)
- This dynamic NFT is updated by triggering the functions-request hardhat CLI command.

## Back up

In case the attendees are unable to follow, we'll direct them to use the [starter repository](https://github.com/smartcontractkit/functions-hardhat-starter-kit).


## 2. Any specific concerns you want to discuss when it comes to workshop day?

- Plan B on network failures on your end
- etc.

# Specific Questions

## 1. What value do we specify on [steps 7-9](https://github.com/smartcontractkit/functions-hardhat-starter-kit) for the `--network` parameter? 

Use `polygonMumbai`.

```bash
npx hardhat functions-deploy-client --network polygonMumbai --verify true
```

```bash
npx hardhat functions-sub-create --network polygonMumbai --amount LINK_funding_amount_here --contract 0xDeployed_client_contract_address_here
```

```bash
npx hardhat functions-request --network polygonMumbai --contract 0xDeployed_client_contract_address_here --subid subscription_id_number_here
```

## 2. On which IDE to use

We should clone the starter kit project repository locally if and only if the attenee is struggling to catch up with the program.

We'll use the Remix IDE for introduction purposes during the morning session.

## 3. On interacting with the smart contract

When developing using the Chainlink Functions Starter Kit Repository, you technically only need to modify your request parametersin `Functions-request-config.js`. This is where you can specify which Javascript file to run and what parameters to use. Then, you use the `npx hardhat` CLI commands.

For live (e.g. testnet) or production use-cases, you would interact with the smart contract using Remix IDE, or the Polygon explorer and specify your parameters there.

### 3.a How do we access the smart contract from Remix IDE?

For the following smart contract: `0x18111cf4770CA5CFB02e9Be12620D14C08B0fbf0`

Visit: https://mumbai.polygonscan.com/address/0x18111cf4770CA5CFB02e9Be12620D14C08B0fbf0

1. On the bottom panel, go to Contract. It should have a green check mark saying that is validated.
2. Then, you can inspect the code or click "Read Contract" or "Write Contract".



## 6. When does the "Open zeppelin contract wizard" get used?

This will be used as the primary code path for the attendees, when building their own smart contracts.

## 7. When does the newly created AccuWeather app get used?

This will be used on the local machines, when accessing the APIs via encrypted environment variables.

## 8. When do the IPFS Metadata get used?

This gets used for the dynamic NFTs, which change depending on real-world state (e.g. temperature, etc).

## What does the error below mean?

Error:

```bash
darren@DESKTOP-SVK799G ~/g/g/d/functions-hardhat-starter-kit (main)> npx hardhat functions-sub-create --network polygonMumbai --amount 15 --contract 0x18111cf4770CA5CFB02e9Be12620D14C08B0fbf0
secp256k1 unavailable, reverting to browser version
Error HH101: Hardhat was set to use chain id 80001, but connected to a chain with id 137.

For more info go to https://hardhat.org/HH101 or run Hardhat with --show-stack-traces
darren@DESKTOP-SVK799G ~/g/g/d/functions-hardhat-starter-kit (main) [1]> 
```

Explanation:

You were connected to an incorrect chain, because you used the invalid POLYGON MUMBAI RPC URL, which should have been provided on the Alchemy dashboard > Apps.

# Action items

1. Request for the three values that Frank mentioned: (a) VRF Consumer base key, (b)key hash, (c) the callback gas limit.

2. expected secret key value: `POLYGON_API_KEY`, to be added via `env-enc`.

> Deploy and verify the client contract to an actual blockchain network by running:
> 
> `npx hardhat functions-deploy-client --network network_name_here --verify true`
> 
> Note: Make sure <explorer>_API_KEY is set if using `--verify true`, depending on which network is used.


3. Request clear (a) required steps and (b) optional steps (or back up steps) for AM and PM session.

4. On Saturday, a link will be provided (notepad) - Frank will write on the notepad for the attendees (link to repo, link to metadata IPFS)