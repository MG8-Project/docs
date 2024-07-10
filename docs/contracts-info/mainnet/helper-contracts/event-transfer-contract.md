---
description: 'Updated : 2024.07.10'
---

# Event Transfer Contract



## 📌  Contract Information <a href="#stg-contract-information" id="stg-contract-information"></a>

*   [Contract](https://bscscan.com/address/0xD6a1D71965aa0090F603E44630e6eA8475817f64) : <mark style="color:red;">0xD6a1D71965aa0090F603E44630e6eA8475817f64</mark>

    * Deployer : 0xC3932FFD8D85697f4c18Cce2Fb4Dc93b81a9aE49 (Dev Team AC-1)
    * Network : BSC Mainnet
    * Solidity Compiler Version : v0.8.19
    * Verified : false

    ```
    [ { "anonymous": false, "inputs": [ { "indexed": false, "internalType": "address", "name": "from", "type": "address" }, { "indexed": false, "internalType": "address", "name": "listed", "type": "address" }, { "indexed": false, "internalType": "bool", "name": "state", "type": "bool" } ], "name": "Authorized", "type": "event" }, { "anonymous": false, "inputs": [ { "indexed": false, "internalType": "address", "name": "from", "type": "address" }, { "indexed": false, "internalType": "address", "name": "to", "type": "address" }, { "indexed": false, "internalType": "uint256", "name": "amount", "type": "uint256" }, { "indexed": false, "internalType": "address", "name": "token", "type": "address" } ], "name": "BatchTransfer", "type": "event" }, { "inputs": [ { "components": [ { "internalType": "address", "name": "token", "type": "address" }, { "internalType": "address", "name": "to", "type": "address" }, { "internalType": "uint256", "name": "amount", "type": "uint256" } ], "internalType": "struct TokenTransmitter.TransferRequest[]", "name": "transferInfo", "type": "tuple[]" } ], "name": "doBatchTransfer", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "anonymous": false, "inputs": [ { "indexed": true, "internalType": "address", "name": "previousOwner", "type": "address" }, { "indexed": true, "internalType": "address", "name": "newOwner", "type": "address" } ], "name": "OwnershipTransferred", "type": "event" }, { "inputs": [], "name": "renounceOwnership", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "address", "name": "account", "type": "address" }, { "internalType": "bool", "name": "state", "type": "bool" } ], "name": "setAllowList", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "uint256", "name": "amount", "type": "uint256" } ], "name": "setBatchTransferLimit", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "address", "name": "newOwner", "type": "address" } ], "name": "transferOwnership", "outputs": [], "stateMutability": "nonpayable", "type": "function" }, { "inputs": [ { "internalType": "address", "name": "user", "type": "address" } ], "name": "allowList", "outputs": [ { "internalType": "bool", "name": "authorized", "type": "bool" } ], "stateMutability": "view", "type": "function" }, { "inputs": [], "name": "batchTransferLimit", "outputs": [ { "internalType": "uint256", "name": "", "type": "uint256" } ], "stateMutability": "view", "type": "function" }, { "inputs": [], "name": "owner", "outputs": [ { "internalType": "address", "name": "", "type": "address" } ], "stateMutability": "view", "type": "function" } ]
    ```



> More Details
>
> * Contract Owner : 0xC3932FFD8D85697f4c18Cce2Fb4Dc93b81a9aE49
> * TransferAdmin :
>   * 0x768871c2F009E8C24c7779F6075Faef45e83ceB6
>   * 0xa44ED2FB17239bBd77E0975F03B4D16acCe05D94
> * MG8 ( CA - 0xdC0D0Eb492e4902C5991C5cB2038fB06409e7F99 )
