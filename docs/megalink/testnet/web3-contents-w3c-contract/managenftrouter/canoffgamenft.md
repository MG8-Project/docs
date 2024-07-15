---
description: 'Updated : 2024.07.08'
---

# canOffGameNFT



```solidity
function canOffGameNFT(
    address _nftContract, 
    address _owner, 
    string memory _ownerUid, 
    uint256 _tokenId, 
    uint256 _txFee
) external view returns(bool)
```



NFT Off mode 사용 가능 여부



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>address</td><td>_owner</td><td>사용자 eoa</td></tr><tr><td>string</td><td>_ownerUid</td><td>사용자 uid</td></tr><tr><td>uint256</td><td>_tokenId</td><td>token id</td></tr><tr><td>uint256</td><td>_txFee</td><td>tx 수수료</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>bool</td><td></td><td>가능 True<br>불가능 False</td></tr></tbody></table>



**Example**

```javascript
await ManageNftRouterContract.canOffGameNFT(
    fairyNftContract.address,
    accounts[0].address,
    uid,
    1,
    ethers.utils.parseEther("1"),
);
```



