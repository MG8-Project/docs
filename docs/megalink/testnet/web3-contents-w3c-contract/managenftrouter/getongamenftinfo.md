---
description: 'Updated :  2024.07.08'
---

# getOnGameNFTInfo

```solidity
function getOnGameNFTInfo(
   address _nftContract, 
   uint256 _tokenId
) external view returns(IManageNFT.NFTData memory info)
```



NFT 정보(on mode)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>NFT 컨트랙트 주소</td></tr><tr><td>uint256</td><td>_tokenId</td><td>token id</td></tr></tbody></table>



**Return Values**

```solidity
struct NFTData{
  uint256 onGameTime;
  string url;
} 
```

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>NFTData</td><td>info</td><td>nft data 정보</td></tr><tr><td>NFTData.uint256</td><td>onGameTime</td><td>on mode 시작 시간</td></tr><tr><td>NFTData.string</td><td>url</td><td>nft url 정보</td></tr></tbody></table>



**Example**

```javascript
data = await manageNftRouterContract.getOnGameNFTInfo(fairyNftContract.address, 1)

// result
[
  BigNumber { value: "1675650182" },
  'http://test.com/fairy/1',
  onGameTime: BigNumber { value: "1675650182" },
  url: 'http://test.com/fairy/1'
]
```



