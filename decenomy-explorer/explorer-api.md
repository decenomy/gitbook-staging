---
description: >-
  This documentation is intended to provide information on the available methods
  to extract data from DECENOMY Explorer using its API.
---

# Explorer API

Being a public API, there is no need to use any kind of authentication.

\
[API v1](explorer-api.md#api-v1-endpoint-url) reports plain text\
\
[API v2](explorer-api.md#api-v2-endpoint-url) reports more info in detail



## API v1 Endpoint URL

<mark style="color:blue;">https://explorer.decenomy.net/api/v1/coins/</mark><mark style="color:yellow;">coin</mark><mark style="color:blue;">/</mark>

### Path parameters v1

<table><thead><tr><th width="196">Name</th><th width="131" align="center">Type</th><th width="316">Description</th><th>Info</th></tr></thead><tbody><tr><td>coin</td><td align="center">string</td><td>should be replaced by the coin ticker, always in caps</td><td>Required</td></tr></tbody></table>

### Query parameters v1

<table><thead><tr><th width="179">Name</th><th width="154" align="center">Type</th><th width="313">Description</th><th>Info</th></tr></thead><tbody><tr><td>getblockcount</td><td align="center">string</td><td>Plain block count, just the block number value</td><td>Optional</td></tr><tr><td>getmoneysupply</td><td align="center">string</td><td>Supply - circulating supply, just the supply number value</td><td>Optional</td></tr></tbody></table>

### Example query v1

```
https://explorer.decenomy.net/api/v1/coins/SAPP/getblockcount
```

### Example response v1

```
1987842
```



## API v2 Endpoint URL

<mark style="color:blue;">https://explorer.decenomy.net/api/v2/</mark><mark style="color:yellow;">coin</mark><mark style="color:blue;">/</mark>

### Path parameters v2

<table><thead><tr><th width="198">Name</th><th width="134" align="center">Type</th><th width="314">Description</th><th align="center">Info</th></tr></thead><tbody><tr><td>coin</td><td align="center">string</td><td>should be replaced by the coin ticker, always in caps</td><td align="center">Required</td></tr></tbody></table>

### Query parameters v2

<table><thead><tr><th width="196">Name</th><th width="137" align="center">Type</th><th width="313">Description</th><th>Info</th></tr></thead><tbody><tr><td>blocks</td><td align="center">string</td><td>Last 30 blocks - blockhash tx / <br>/ blocktime / height / confirmations</td><td>Optional</td></tr><tr><td>transactions</td><td align="center">string</td><td>Last 30 blocks - blockhash / blocktime / height / tx / <br>confirmations / recipients / amount</td><td>Optional</td></tr><tr><td>peers</td><td align="center">string</td><td>Full information of peers available</td><td>Optional</td></tr><tr><td>masternodes</td><td align="center">string</td><td>Full information of each masternode in the network</td><td>Optional</td></tr><tr><td>info</td><td align="center">string</td><td>Wallet and blockchain information</td><td>Optional</td></tr><tr><td>masternode/count</td><td align="center">string</td><td>Total number of masternodes connected in the network</td><td>Optional</td></tr><tr><td>status</td><td align="center">string</td><td>The status of blockchain based on the last block received</td><td>Optional</td></tr></tbody></table>

### Example query v2

```
https://explorer.decenomy.net/api/v2/SAPP/info
```

### Example response v2

```
{
  "response": {
    "connections": 171,
    "errors": "",
    "blocks": 1987846,
    "paytxfee": 0,
    "moneysupply": 1224915018.8013475,
    "difficulty": 527924.3523641471,
    "keypoolsize": 100,
    "keypoololdest": 1627317470,
    "walletversion": 169900,
    "timeoffset": 0,
    "testnet": false,
    "version": 1050100,
    "staking status": "Staking Inactive",
    "protocolversion": 70931,
    "services": "NETWORK/BLOOM/",
    "balance": 0,
    "relayfee": 0.0001,
    "proxy": ""
  },
  "success": true
}
```

