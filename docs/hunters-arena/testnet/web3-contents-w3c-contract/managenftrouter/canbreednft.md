---
description: 'Updated :  2024.07.08'
---

# canBreedNFT

```solidity
function canBreedNFT(
    address _nftContract,
    string memory _ownerUid, 
    uint256 _matronId, 
    uint256 _sireId, 
    uint256 _breedFee, 
    string memory _url, 
    uint256 _txFee
) external view returns(bool)
```



NFT Breed 사용 가능 여부



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>string</td><td>_ownerUid</td><td>사용자 uid</td></tr><tr><td>uint256</td><td>_matornId</td><td>부모 token id</td></tr><tr><td>uint256</td><td>_sireId</td><td>부모 token id</td></tr><tr><td>uint256</td><td>_breedFee</td><td>브리딩  수수료</td></tr><tr><td>string</td><td>_url</td><td>nft url</td></tr><tr><td>uint256</td><td>_txFee</td><td>tx 수수료</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>bool</td><td></td><td>가능 True<br>불가능 False</td></tr></tbody></table>



**Example**

```javascript
await ManageNftRouterContract.canBreedNFT(
    fairyNftContract.address,
    uid,
    1,
    2,
    ethers.utils.parseEther("10"),
    "http://test.com/fairy/",
    ethers.utils.parseEther("10"),
);
```



