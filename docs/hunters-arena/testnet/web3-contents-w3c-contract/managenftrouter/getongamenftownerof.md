---
description: 'Updated : 2024.07.08'
---

# getOnGameNFTOwnerOf

```solidity
function getOnGameNFTOwnerOf(
   address _nftContract, 
   uint256 _tokenId
) external view returns(string uid)
```



NFT 소유자 uid (on mode)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>uint256</td><td>_tokenId</td><td>token id</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>string</td><td>uid</td><td>소유주 uid</td></tr></tbody></table>



**Example**

```javascript
data = await manageNftRouterContract.getOnGameNFTOwnerOf(fairyNftContract.address, 1)

// result
uid
```



