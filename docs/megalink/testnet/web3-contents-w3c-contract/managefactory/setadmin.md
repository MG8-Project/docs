---
description: 'Updated : 2024.07.08'
---

# setAdmin

```solidity
function setManage(
    address _admin
) external onlyAdmin
```



admin 주소변경



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_admin</td><td>변경 될 admin 주소</td></tr></tbody></table>



**Example**

```javascript
await ManageFactoryContract.setAdmin(
    accounts[1].address
);
```



