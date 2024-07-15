---
description: 'Updated : 2024.07.08'
---

# doOnGameNFT

```solidity
function doOnGameNFT(
    address _nftContract,
    uint256 _tokenId,
    string memory _ownerUid
) external
```



NFT On mode



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>uint256</td><td>_tokenId</td><td>token id</td></tr><tr><td>string</td><td>_ownerUid</td><td>사용자 uid</td></tr></tbody></table>



**Example**

```javascript
await ManageNftRouterContract.doOnGameNFT(
    fairyNftContract.address,
    1,
    uid,
);
```



