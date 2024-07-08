---
description: 'Updated : 2024.07.08'
---

# ⭐ getOnGameBalanceToken

### OnMode된 Balance 토큰 체크



```solidity
function getOnGameBalanceToken(
   address _tokenContract, 
   string memory _ownerUid
) external view returns(uint256 amount)
```



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenContract</td><td>토큰 컨트랙트 주소</td></tr><tr><td>string</td><td>_ownerUid</td><td>사용자 uid</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint256</td><td>amount</td><td>보유 토큰 수량</td></tr></tbody></table>



**Example**

```javascript
data = await manageTokenRouterContract.getOnGameBalanceToken(tokenContract.address, uid)

// result
BigNumber { value: "1000000000000000000000" }
```



