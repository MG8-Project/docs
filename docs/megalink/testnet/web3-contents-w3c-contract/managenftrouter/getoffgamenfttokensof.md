---
description: 'Updated : 2024.07.08'
---

# getOffGameNFTTokensOf

```solidity
function getOffGameNFTTokensOf(
   address _nftContract, 
   address _owner
) external view returns(uint256[] memory tokens)
```



NFT 소유 정보(off mode)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>address</td><td>_owner</td><td>사용자 eoa</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint256[]</td><td>tokens</td><td>소유중인  nft 정보(on mode)</td></tr></tbody></table>



**Example**

```javascript
data = await manageNftRouterContract.getOffGameNFTTokensOf(fairyNftContract.address, accounts[0].address)

// result
[
  BigNumber { value: "1" },
  BigNumber { value: "2" },
  BigNumber { value: "3" }
]
```



