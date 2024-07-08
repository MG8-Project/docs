---
description: 'Updated : 2024.07.08'
---

# doOffGameToken

### Celeb -> pFandom 으로 변경하는 역할을 함 \[Only Relay Admin]



```solidity
function doOffGameToken(
    OffGameTokenRequest[] memory _request,
) external onlyRelayAdmin
```



Token Off mode



**Parameters**

```solidity
struct OffGameTokenRequest{
    address tokenContract;
    string messageId;
    uint256 amount;
    address owner;
    string ownerUid;
    uint256 txFee;
}
```

<table><thead><tr><th width="293.4">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>OffGameTokenRequest</td><td>_request</td><td>request 배열</td></tr><tr><td>OffGameTokenRequest.address</td><td>tokenContract</td><td>토큰 컨트랙트 주소</td></tr><tr><td>OffGameTokenRequest.string</td><td>messageId</td><td>메시지 고유 ID</td></tr><tr><td>OffGameTokenRequest.uint256</td><td>amount</td><td>토큰 수량</td></tr><tr><td>OffGameTokenRequest.address</td><td>owner</td><td>사용자 eoa</td></tr><tr><td>OffGameTokenRequest.string</td><td>ownerUid</td><td>사용자 uid</td></tr><tr><td>OffGameTokenRequest.uint256</td><td>txFee</td><td>tx 수수료</td></tr></tbody></table>



**Example**

```javascript
await manageTokenRouterContract.doOffGameToken(
            [{tokenContract:tokenContract.address,
            messageId:"1234", 
            amount:ethers.utils.parseEther("100"), 
            owner:accounts[0].address, 
            ownerUid:uid1, 
            txFee:ethers.utils.parseEther("10")}]
)
```



