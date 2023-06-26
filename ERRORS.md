# Errors

## Source file requires different compiler version

Sometimes you might encounter this error while compiling your solidity code.

`ParserError: Source file requires different compiler version (current compiler is 0.8.7+commit.e28d00a7.Emscripten.clang)`

Fix:

> An easy solution is to change your code to require v0.6 as well and compile with this version.
> 
> pragma solidity ^0.6.0;
> 
> [Source](https://stackoverflow.com/questions/70905645/parsererror-source-file-requires-different-compiler-version-current-compiler-i)

## Invalid RPC URL error 1 (rate limiting issue)

How do we handle timeout or rate limiting issues onsite? What can the attendees do/focus on while waiting for these kinds of issues to get resolved?

Command: 

```bash
npx hardhat functions-sub-create --network polygonMumbai --amount 8 --contract 0x18111cf4770CA5CFB02e9Be12620D14C08B0fbf0
```

CLI error response:

```bash
secp256k1 unavailable, reverting to browser version
Creating Functions billing subscription
An unexpected error occurred:

ProviderError: Too Many Requests error received from polygon-mumbai.g.alchemy.com
    at HttpProvider._fetchJsonRpcResponse (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/http.ts:212:15)
    at processTicksAndRejections (node:internal/process/task_queues:95:5)
    at HttpProvider.request (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/http.ts:85:29)
    at AutomaticGasPriceProvider._getGasPrice (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/gas-providers.ts:217:23)
    at AutomaticGasPriceProvider.request (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/gas-providers.ts:181:41)
    at EthersProviderWrapper.send (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@nomiclabs/hardhat-ethers/src/internal/ethers-provider-wrapper.ts:13:20)
```

Relevant docs:

- https://docs.alchemy.com/reference/error-reference
- https://docs.alchemy.com/reference/throughput
- https://ethereum.stackexchange.com/questions/139524/forking-mainnet-with-hardhat-alchemy-fails-with-too-many-requests

## Invalid RPC URL error 2 (rate limiting issue)

```bash
darren@DESKTOP-SVK799G ~/g/g/d/functions-hardhat-starter-kit (main) [1]> 
npx hardhat functions-sub-create --network polygonMumbai --amount 15 --contract 0x18111cf4770CA5CFB02e9Be12620D14C08B0fbf0
secp256k1 unavailable, reverting to browser version
An unexpected error occurred:

Error: missing revert data in call exception; Transaction reverted without a reason string [ See: https://links.ethers.org/v5-errors-CALL_EXCEPTION ] (data="0x", transaction={"from":"0xb1Be0a830Fc6120bc47b5ffC0d9FEc3304Cfa8B9","to":"0xeA6721aC65BCeD841B8ec3fc5fEdeA6141a0aDE4","data":"0xfa00763a000000000000000000000000b1be0a830fc6120bc47b5ffc0d9fec3304cfa8b9","accessList":null}, error={"name":"ProviderError","_stack":"ProviderError: Too Many Requests error received from polygon-mumbai.g.alchemy.com\n    at HttpProvider._fetchJsonRpcResponse (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/http.ts:212:15)\n    at processTicksAndRejections (node:internal/process/task_queues:95:5)\n    at HttpProvider.request (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/http.ts:85:29)\n    at EthersProviderWrapper.send (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@nomiclabs/hardhat-ethers/src/internal/ethers-provider-wrapper.ts:13:20)","code":-32005,"_isProviderError":true}, code=CALL_EXCEPTION, version=providers/5.7.2)
    at Logger.makeError (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@ethersproject/logger/src.ts/index.ts:269:28)
    at Logger.throwError (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@ethersproject/logger/src.ts/index.ts:281:20)
    at checkError (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@ethersproject/providers/src.ts/json-rpc-provider.ts:66:16)
    at EthersProviderWrapper.<anonymous> (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@ethersproject/providers/src.ts/json-rpc-provider.ts:642:20)
    at step (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@ethersproject/providers/lib/json-rpc-provider.js:48:23)
    at Object.throw (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@ethersproject/providers/lib/json-rpc-provider.js:29:53)
    at rejected (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@ethersproject/providers/lib/json-rpc-provider.js:21:65)
    at processTicksAndRejections (node:internal/process/task_queues:95:5) {
  reason: 'missing revert data in call exception; Transaction reverted without a reason string',
  code: 'CALL_EXCEPTION',
  data: '0x',
  transaction: {
    from: '0xb1Be0a830Fc6120bc47b5ffC0d9FEc3304Cfa8B9',
    to: '0xeA6721aC65BCeD841B8ec3fc5fEdeA6141a0aDE4',
    data: '0xfa00763a000000000000000000000000b1be0a830fc6120bc47b5ffc0d9fec3304cfa8b9',
    accessList: null
  },
  error: ProviderError: Too Many Requests error received from polygon-mumbai.g.alchemy.com
      at HttpProvider._fetchJsonRpcResponse (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/http.ts:212:15)
      at processTicksAndRejections (node:internal/process/task_queues:95:5)
      at HttpProvider.request (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/hardhat/src/internal/core/providers/http.ts:85:29)
      at EthersProviderWrapper.send (/home/darren/git/github.com/darrensapalo/functions-hardhat-starter-kit/node_modules/@nomiclabs/hardhat-ethers/src/internal/ethers-provider-wrapper.ts:13:20)
}
```