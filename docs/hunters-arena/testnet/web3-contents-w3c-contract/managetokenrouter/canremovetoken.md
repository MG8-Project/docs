---
description: 'Updated : 2024.07.08'
---

# canRemoveToken

### Celeb -> pFandom 가능여부 확인 기능

```solidity
function canRemoveToken(
    address _tokenContract, 
    string memory _ownerUid, 
    uint256 _amount, 
) external view returns(bool)
```



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenContract</td><td>토큰 컨트랙트 주소</td></tr><tr><td>string</td><td>_ownerUid</td><td>사용자 uid</td></tr><tr><td>uint256</td><td>_amount</td><td>토큰 수량(+txFee)</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>bool</td><td></td><td>가능 True<br>불가능 False</td></tr></tbody></table>



**Example**

```javascript
await ManageTokenRouterContract.canRemoveToken(
    tokenContract.address,
    uid,
    ethers.utils.parseEther("1"),
);
```



