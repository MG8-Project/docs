---
description: 'Updated : 2024.07.10'
---

# Event Transfer Contract



## 📌 \[STG] Contract Information <a href="#stg-and-dev-contract-information" id="stg-and-dev-contract-information"></a>

* [Contract](https://testnet.bscscan.com/address/0x29C8E054c39Ae65e53f439448d5f99b5a161e398) : <mark style="color:red;">0x29C8E054c39Ae65e53f439448d5f99b5a161e398</mark>
* Deployer : 0xC3932FFD8D85697f4c18Cce2Fb4Dc93b81a9aE49 (Dev Team AC-1)
* Network : BSC Testnet
* Solidity Compiler Version : v0.8.19
* Verified : [True](https://testnet.bscscan.com/address/0x17b37e08802a5bC982246EA4a4806fc65CC73bb5#code)

```
[ { "anonymous": false, "inputs": [ { "indexed": false, "internalType": "address", "name": "from", "type": "address" }, { "indexed": false, "internalType": "address", "name": "listed", "type": "address" }, { "indexed": false, "internalType": "bool", "name": "state", "type": "bool" } ], "name": "Authorized", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": false, "internalType": "address", "name": "from", "type": "address" }, { "indexed": false, "internalType": "address", "name": "to", "type": "address" }, { "indexed": false, "internalType": "uint256", "name": "amount", "type": "uint256" }, { "indexed": false, "internalType": "address", "name": "token", "type": "address" } ], "name": "BatchTransfer", "type": "event" }, { "inputs": [ { "components": [ { "internalType": "address", "name": "token", "type": "address" }, { "internalType": "address", "name": "to", "type": "address" }, { "internalType": "uint256", "name": "amount", "type": "uint256" } ], "internalType": "struct TokenTransmitter.TransferRequest[]", "name": "transferInfo", "type": "tuple[]" } ], "name": "doBatchTransfer", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "anonymous": false, "inputs": [ { "indexed": true, "internalType": "address", "name": "previousOwner", "type": "address" }, { "indexed": true, "internalType": "address", "name": "newOwner", "type": "address" } ], "name": "OwnershipTransferred", "type": "event" }, { "inputs": [], "name": "renounceOwnership", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "address", "name": "account", "type": "address" }, { "internalType": "bool", "name": "state", "type": "bool" } ], "name": "setAllowList", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "uint256", "name": "amount", "type": "uint256" } ], "name": "setBatchTransferLimit", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "address", "name": "newOwner", "type": "address" } ], "name": "transferOwnership", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "address", "name": "user", "type": "address" } ], "name": "allowList", "outputs": [ { "internalType": "bool", "name": "authorized", "type": "bool" } ], "stateMutability": "view", "type": "function" }, { "inputs": [], "name": "batchTransferLimit", "outputs": [ { "internalType": "uint256", "name": "", "type": "uint256" } ], "stateMutability": "view", "type": "function" }, { "inputs": [], "name": "owner", "outputs": [ { "internalType": "address", "name": "", "type": "address" } ], "stateMutability": "view", "type": "function" } ]
```

> More Details
>
> * Contract Owner : 0xC3932FFD8D85697f4c18Cce2Fb4Dc93b81a9aE49
> * TransferAdmin :
>   * 0xC3932FFD8D85697f4c18Cce2Fb4Dc93b81a9aE49
>   * 0xa44ED2FB17239bBd77E0975F03B4D16acCe05D94
>   * 0x7C0e2Ee7B148dD0fE1894670FDa7d474AFFEC697
> * MG8 ( CA - 0x17b37e08802a5bC982246EA4a4806fc65CC73bb5 )

