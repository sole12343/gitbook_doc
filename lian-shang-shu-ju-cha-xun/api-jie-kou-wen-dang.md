---
description: 由于不同的api接口所消耗的资源不同，所以此处先介绍api不同接口的对应的点数价格，之后介绍接口的使用说明。
---

# Api接口文档

### 获取Api key

您可以通过注册帐户并在帐户设置中生成 API 密钥来获取 API 密钥。将此 API 密钥包含在 API 请求的标头中以进行身份​​验证。

以下是有关如何获取 API 密钥的分步指南：

[www.multichaindatabase.com/docs/get-apikey](https://www.google.com)



### 对应Api消耗点数价格

<table><thead><tr><th width="316">Api名字</th><th width="311">url</th><th>Cost(CUs)</th></tr></thead><tbody><tr><td>查询区块详情 block-fills</td><td>/api/v1/explorer/block/block-fills</td><td>10</td></tr><tr><td>查询区块列表 block-list</td><td>/api/v1/explorer/block/block-list</td><td>50</td></tr><tr><td>查询区块的交易列表transaction-list</td><td>/api/v1/explorer/transaction/transaction-list</td><td>50</td></tr><tr><td><p>查询交易哈希的交易详情</p><p>transaction-detail</p></td><td>/api/v1/explorer/transaction/transaction-detail</td><td>10</td></tr><tr><td><p>查询交易哈希的内部交易</p><p>internal-transaction-list</p></td><td>/api/v1/explorer/transaction/internal-transaction-list</td><td>30</td></tr><tr><td><p>查询交易哈希的代币交易</p><p>token-transaction-list</p></td><td>/api/v1/explorer/transaction/token-transaction-list</td><td>10</td></tr><tr><td><p>查询地址原生代币的最新余额</p><p>coin-balance</p></td><td>/api/v1/explorer/address/coin-balance</td><td>10</td></tr><tr><td><p>查询地址原生代币的历史余额</p><p>history-coin-balance</p></td><td>/api/v1/explorer/address/history-coin-balance</td><td>50</td></tr><tr><td><p>查询地址普通交易列表</p><p>transaction-list</p></td><td>/api/v1/explorer/address/transaction-list</td><td>50</td></tr></tbody></table>



### api接口使用说明

1.根据区块号查询区块详情

**/api/v1/explorer/block/block-fills**

&#x20;heards:

```
apikey:xxxxxxxxx
```

params:

```
chain:(必填，eth/btc/tron...)
block_number:(非必填，默认返回最新区块的信息，)
```

response:

```json
{
  "data": {
    "totalDifficulty": 270863178297429100,
    "baseFeePerGas": null,
    "blockReward": 0,
    "miner-label": [],
    "miner": "0x790b8a3ce86e707ed0ed32bf89b3269692a23cc1",
    "excessBlobGas": null,
    "number": 123333,
    "gasLimit": 3141592,
    "gasUsed": 0,
    "size": 541,
    "parentHash": "0xe521f41e8e33ad7f49183a354c29f405dc9c554c766c738f86dabc0a9d186e0f",
    "txNumber": 0,
    "blobGasUsed": null,
    "hash": "0xf32cf8c8e4e22a2d480fb27588482f391b5bcb6ba93f1898546fafcd5b7fb6dd",
    "timestamp": "2015-08-22 10:18:44"
  },
  "status": "success"
}
```



2.根据区块号查询区块列表

**/api/v1/explorer/block/block-list**

&#x20;heards:

```
apikey:xxxxxxxxx
```

params:

```
chain:(必填，eth/btc/tron...)
start_block_number:开始区块号
end_block_number:结束区块号(非必填，默认返回最新100个区块的基本信息)
```

response:

```json
{
  "block_list": [
    {
      "timestamp": "2015-07-31 17:24:21",
      "number": 10002,
      "hash": "0xd2be089e42481ec27e8d12a9e67a33eb964242b8990c036062f184f026099930",
      "parentHash": "0x7e86236e83a62e7b04d09561e9e98822f353333f16ba57497ab61d8f7f9f93ab",
      "nonce": "0x776619bcba79177e",
      "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
      "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
      "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "stateRoot": "0xa390e56d2c55172a79716602650107e2c7e99f67485e7450d1a34612e01b59a1",
      "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "miner": "0xcf9d0f720cba659bad47d38f3c8a6f40ba7a8fe5",
      "difficulty": 598426678236,
      "totalDifficulty": 2304959541059713,
      "size": 539,
      "extraData": "0x476574682f76312e302e302f6c696e75782f676f312e342e32",
      "gasLimit": 5000,
      "gasUsed": 0,
      "transactionCount": 0,
      "baseFeePerGas": null,
      "withdrawalsRoot": null,
      "withdrawals": "[]",
      "blobGasUsed": null,
      "excessBlobGas": null
    },
    {
      "timestamp": "2015-07-31 17:23:47",
      "number": 10000,
      "hash": "0xdc2d938e4cd0a149681e9e04352953ef5ab399d59bcd5b0357f6c0797470a524",
      "parentHash": "0xb9ecd2df84ee2687efc0886f5177f6674bad9aeb73de9323e254e15c5a34fc93",
      "nonce": "0xb75e5f372524d34c",
      "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
      "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
      "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "stateRoot": "0x4de830f589266773eae1a1caa88d75def3f3a321fbd9aeb89570a57c6e7f3dbb",
      "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "miner": "0xbf71642d7cbae8faf1cfdc6c1c48fcb45b15ed22",
      "difficulty": 598426820912,
      "totalDifficulty": 2303762395359969,
      "size": 541,
      "extraData": "0x476574682f76312e302e302f77696e646f77732f676f312e342e32",
      "gasLimit": 5000,
      "gasUsed": 0,
      "transactionCount": 0,
      "baseFeePerGas": null,
      "withdrawalsRoot": null,
      "withdrawals": "[]",
      "blobGasUsed": null,
      "excessBlobGas": null
    },
    {
      "timestamp": "2015-07-31 17:24:31",
      "number": 10003,
      "hash": "0x666b0b3b9e80806a86146c7807c53932777ecba3ad2415767ab831f97c2a7ade",
      "parentHash": "0xd2be089e42481ec27e8d12a9e67a33eb964242b8990c036062f184f026099930",
      "nonce": "0x21bc229d66ed720b",
      "sha3Uncles": "0x97c192eb4cc89402c9b7eb4dab2314c8ac091d388f34f795095b10e347fa03f5",
      "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
      "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "stateRoot": "0x6c610a0c5b616e9f3ca6051a8f805819ffe15821e9e89c68e734e210e9c62b49",
      "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "miner": "0x33bc13fdf135073277971b4d9f4f72082e907996",
      "difficulty": 598718878762,
      "totalDifficulty": 2305558259938475,
      "size": 1082,
      "extraData": "0x476574682f76312e302e302d30636463373634372f6c696e75782f676f312e34",
      "gasLimit": 5000,
      "gasUsed": 0,
      "transactionCount": 0,
      "baseFeePerGas": null,
      "withdrawalsRoot": null,
      "withdrawals": "[]",
      "blobGasUsed": null,
      "excessBlobGas": null
    },
    {
      "timestamp": "2015-07-31 17:23:59",
      "number": 10001,
      "hash": "0x7e86236e83a62e7b04d09561e9e98822f353333f16ba57497ab61d8f7f9f93ab",
      "parentHash": "0xdc2d938e4cd0a149681e9e04352953ef5ab399d59bcd5b0357f6c0797470a524",
      "nonce": "0xb0964e5ea365b716",
      "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
      "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
      "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "stateRoot": "0xd0707c514fe349605ce4061d8039edfb95d564dea245088e1e28deaee1ca66f3",
      "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "miner": "0x4e5c9fd685dcc9abede1cbde4959039388bf7c5a",
      "difficulty": 598719021508,
      "totalDifficulty": 2304361114381477,
      "size": 539,
      "extraData": "0x476574682f76312e302e302f6c696e75782f676f312e342e32",
      "gasLimit": 5000,
      "gasUsed": 0,
      "transactionCount": 0,
      "baseFeePerGas": null,
      "withdrawalsRoot": null,
      "withdrawals": "[]",
      "blobGasUsed": null,
      "excessBlobGas": null
    }
  ],
  "status": "success"
}

```







