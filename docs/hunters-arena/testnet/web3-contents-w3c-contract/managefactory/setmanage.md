---
description: 'Updated : 2024.07.08'
---

# setManage



```solidity
function setManage(
    address _pointContract, 
    address _manageContract
) external onlyAdmin
```



Router에서 사용하기 위해서, ERC721, ERC20 토큰과 Manage 토큰을 매핑해주는 함수



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_pointContract</td><td>ERC721, ERC20 컨트랙트 주소</td></tr><tr><td>address</td><td>_manageContract</td><td>pointContract에 맞는 manageContract 주소</td></tr></tbody></table>



**Example**

```javascript
await ManageFactoryContract.setManage(
    fairyNftContract.address, 
    manageFairyNftContract.address
);
```



