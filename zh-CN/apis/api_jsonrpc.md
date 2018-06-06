# JSON-RPC API

[TOC]

## Getting Started

[JSON](http://json.org/)是一种轻量级的数据交换格式。它可以表示数字，字符串，有序的值序列以及名称/值对的集合。

[JSON-RPC](http://www.jsonrpc.org/specification)是一种无状态，轻量级的远程过程调用（RPC）协议。这个规范主要定义了几个数据结构和围绕它们处理的规则。它是传输不可知的，因为这些概念可以在同一个进程中，在套接字上，在HTTP上，或在许多不同的消息传递环境中使用。它使用JSON（[RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)）作为数据格式。

## JSON-RPC Support

JSON-RPC 2.0、HTTP、IPC

## 默认的块参数
以下方法具有额外的默认块参数：

eth_getBalance
eth_getCode
eth_getTransactionCount
eth_getStorageAt
eth_call
当请求作用于以太坊的状态时，最后的默认块参数决定块的高度。以下选项可用于defaultBlock参数：

HEX String - 一个整数块号码
String "earliest" 为最早/起源块
String "latest" - 为最新的开采块
String "pending" - 待处理状态/交易

## JSON-RPC API Reference

### 账本状态

gasPrice、协议版本、块高

eth_protocolVersion
eth_syncing
eth_mining
eth_hashrate
eth_gasPrice
eth_blockNumber

### 治理

协议升级提案、协议升级投票

共识治理：代表申请、委托、退出申请、得票数、获取代表信息、议员列表

### Accounts

创建账户、获取账户列表、修改交易秘钥、余额、签名

eth_coinbase
eth_accounts
eth_getBalance
eth_sign

### Block

获取块、获取叔块、同步状态
eth_getStorageAt
eth_getTransactionCount
eth_getBlockTransactionCountByHash
eth_getBlockTransactionCountByNumber
eth_getUncleCountByBlockHash
eth_getUncleCountByBlockNumber
eth_getCode

eth_getBlockByHash
eth_getBlockByNumber
eth_getUncleByBlockHashAndIndex
eth_getUncleByBlockNumberAndIndex

### Transations

发起交易、获取交易、获取交易收据、预估gas、预执行

eth_getTransactionCount
eth_sendTransaction
eth_sendRawTransaction
eth_call
eth_estimateGas
eth_getTransactionByHash
eth_getTransactionByBlockHashAndIndex
eth_getTransactionByBlockNumberAndIndex
eth_getTransactionReceipt

### DApp

获取编译器列表、编译、发布智能合约、修改智能合约信息

eth_getCompilers
eth_compileLLL
eth_compileSolidity
eth_compileSerpent

### Filter

eth_newFilter
eth_newBlockFilter
eth_newPendingTransactionFilter
eth_uninstallFilter
eth_getFilterChanges
eth_getFilterLogs
eth_getLogs

### Mining

挖矿获取任务、提交任务

eth_getWork
eth_submitWork
eth_submitHashrate

### Net

版本、连接数、网络监听状态

net_version
net_peerCount
net_listening

### Database

#### db_putString

* Parameters

* Returns

* Example

#### db_getString

- Parameters
- Returns
- Example

#### db_putHex

- Parameters
- Returns
- Example

#### db_getHex

- Parameters
- Returns
- Example

### Others

#### sha3

#### clientVersion