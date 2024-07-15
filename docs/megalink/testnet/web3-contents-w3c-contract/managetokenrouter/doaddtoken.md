---
description: 'Updated : 2024.07.08'
---

# doAddToken

### **Celeb (DB) -> pFandom (Contract) 으로 변경하는 역할** \[Only Relay Admin]

```solidity
function doAddToken(
    AddAndRemoveTokenRequest[] memory _request,
) external onlyRelayAdmin
```

**Parameters**

```solidity
struct AddAndRemoveTokenRequest{
    address tokenContract;
    string messageId;
    uint256 amount;
    string ownerUid;
    uint256 txFee;
}
```

<table><thead><tr><th width="343.4">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>AddAndRemoveTokenRequest</td><td>_request</td><td>request 배열</td></tr><tr><td>AddAndRemoveTokenRequest.address</td><td>tokenContract</td><td>토큰 컨트랙트 주소</td></tr><tr><td>AddAndRemoveTokenRequest.string</td><td>messageId</td><td>메시지 고유 ID</td></tr><tr><td>AddAndRemoveTokenRequest.uint256</td><td>amount</td><td>토큰 수량</td></tr><tr><td>AddAndRemoveTokenRequest.string</td><td>ownerUid</td><td>사용자 uid</td></tr><tr><td>AddAndRemoveTokenRequest.uint256</td><td>txFee</td><td>tx 수수료</td></tr></tbody></table>



**Example**

```javascript
await manageTokenRouterContract.doAddToken(
        [{tokenContract:tokenContract.address,
        messageId:"1234", 
        ownerUid:uid1, 
        amount:ethers.utils.parseEther("100"),
        txFee:ethers.utils.parseEther("100")}]
);
```



