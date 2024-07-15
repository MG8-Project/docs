---
description: 'Updated : 2024.07.08'
---

# doOffGameNFT

```solidity
function doOffGameNFT(
    OffGameNftRequest[] memory _request,
) external onlyRelayAdmin
```



NFT Off mode



**Parameters**

```solidity
struct OffGameNFTRequest{
    address nftContract;
    string messageId;
    uint256 tokenId;
    address owner;
    string ownerUid;
    uint256 txFee;
}
```

<table><thead><tr><th width="279.4">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>OffGameNftRequest</td><td>_request</td><td>request 배열</td></tr><tr><td>OffGameNftRequest.address</td><td>nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>OffGameNftRequest.string</td><td>messageId</td><td>메시지 고유 ID</td></tr><tr><td>OffGameNftRequest.uint256</td><td>tokenId</td><td>token id</td></tr><tr><td>OffGameNftRequest.address</td><td>owner</td><td>사용자 eoa</td></tr><tr><td>OffGameNftRequest.string</td><td>ownerUid</td><td>사용자 uid</td></tr><tr><td>OffGameNftRequest.uint256</td><td>txFee</td><td>tx 수수료</td></tr></tbody></table>



**Example**

```javascript
await manageNftRouterContract.doOffGameNFT(
            [{nftContract:fairyNftContract.address,
            messageId:"1234", 
            tokenId:3, 
            owner:accounts[0].address, 
            ownerUid:uid1, 
            txFee:ethers.utils.parseEther("100")}]
)
```



