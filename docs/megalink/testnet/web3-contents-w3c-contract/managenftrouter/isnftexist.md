---
description: 'Updated : 2024.07.08'
---

# isNFTExist

```solidity
function isNFTExist(
   address _nftContract, 
   uint256 _tokenId
) external view returns(bool exist)
```



NFT 존재  여부



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>uint256</td><td>_tokenId</td><td>token id</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>bool</td><td>exist</td><td>존재여부</td></tr></tbody></table>



**Example**

```javascript
data = await manageNftRouterContract.isNFTExist(fairyNftContract.address, 1)

// result
true
```



