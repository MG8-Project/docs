---
description: 'Updated : 2024.07.08'
---

# setTokenContract



```solidity
function setTokenContract(
    address _tokenContract,
) external onlyRelayAdmin
```



NFT 라우터 함수 중 Fee 및  ERC20 재화소모 시 사용 될 ERC20 주소 설정



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenContract</td><td>ERC20 컨트랙트 주소</td></tr></tbody></table>



**Example**

```javascript
await ManageNftRouterContract.setTokenContract(
    tokenContract.address,
);
```



\=
