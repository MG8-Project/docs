---
description: 'Updated : 2024.07.08'
---

# doBreedNFT

```solidity
function doBreedNFT(
    BreedNFTRequest[] memory _request,
) external onlyRelayAdmin
```



NFT Breed



**Parameters**

```solidity
struct BreedNFTRequest{
    address nftContract;
    string messageId;
    string ownerUid;
    uint256 matronId;
    uint256 sireId;
    uint256 breedFee;
    uint256 tokenId;
    string url;
    uint256 txFee;
}
```

<table><thead><tr><th width="279.4">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>BreedNFTRequest</td><td>_request</td><td>request 배열</td></tr><tr><td>BreedNFTRequest.address</td><td>nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>BreedNFTRequest.string</td><td>messageId</td><td>메시지 고유 ID</td></tr><tr><td>BreedNFTRequest.string</td><td>ownerUid</td><td>사용자 uid</td></tr><tr><td>BreedNFTRequest.uint256</td><td>matornId</td><td>부모 token id</td></tr><tr><td>BreedNFTRequest.uint256</td><td>sireId</td><td>부모 token id</td></tr><tr><td>BreedNFTRequest.uint256</td><td>breedFee</td><td>브리딩 수수료</td></tr><tr><td>BreedNFTRequest.uint256</td><td>tokenId</td><td>브리딩 결과 토큰 id</td></tr><tr><td>BreedNFTRequest.string</td><td>url</td><td>브리딩 결과 url</td></tr><tr><td>BreedNFTRequest.uint256</td><td>txFee</td><td>tx 수수료</td></tr></tbody></table>



**Example**

```javascript
await manageNftRouterContract.doBreedNFT(
        [{nftContract:fairyNftContract.address
        messageId:"1234", 
        ownerUid:uid1, 
        matronId:1, 
        sireId:2, 
        breedFee:ethers.utils.parseEther("200"), 
        tokenId:1001, 
        url:"http://test.com/fairy/", 
        txFee:ethers.utils.parseEther("100")}]
);
```



