---
description: 'Updated : 2024.07.08'
---

# ⭐ doOnGameToken

### **Fandom -> pFandom (Token On mode) 기능을 수행.**

:warning:ADMIN UID에 항시 토큰 잔량이 필요하므로 위 함수를 통해 잔량 보충을 진행할 것. (ADMIN UID = "adminUid")

```solidity
function doOnGameToken(
    address _tokenContract,
    uint256 _amount,
    string memory _ownerUid
) external
```



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_nftContract</td><td>토큰컨트랙트 주소</td></tr><tr><td>uint256</td><td>_amount</td><td>token 수량</td></tr><tr><td>string</td><td>_ownerUid</td><td>사용자 uid</td></tr></tbody></table>



**Example**

```javascript
await ManageTokenRouterContract.doOnGameToken(
    tokenContract.address,
    ethers.utils.parseEther("100"),
    uid,
);
```



