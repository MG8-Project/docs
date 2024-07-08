---
description: 'Updated : 2024.07.08'
---

# setFeeTo

```solidity
function setFeeTo(
    address _tokenA,
    address _tokenB, 
    address _newFeeTo
) external onlyFeeAdmin
```



Protocol Fee 발생 시 Fee를 받을 대상&#x20;

**※ 설정 없을 시 동작 안함(Protocol fee)**



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>설정할 페어 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>설정할 페어 토큰B 주소</td></tr><tr><td>address</td><td>_newFeeTo</td><td>프로토콜 Fee 받을 대상 주소</td></tr></tbody></table>



**Example**

```javascript
// Protocol Fee 받을 대상 설정
await MantiswapFactoryContract.setFeeTo(
    mockToken0Contract.address,
    mockToken1Contract.address,
    accounts[0].address
)    
```



