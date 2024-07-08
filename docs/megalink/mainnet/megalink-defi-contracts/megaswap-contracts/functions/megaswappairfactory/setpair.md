---
description: 'Updated : 2024.07.08'
---

# setPair

```solidity
function setPair(
    address _pairContract,
    address _tokenA,
    address _tokenB
) external onlyAdmin
```



Pair Contract 등록&#x20;

**※  중복 페어 토큰 컨트랙트 시 덮어씀**



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_pariContract</td><td>페어 컨트랙트 주소</td></tr><tr><td>address</td><td>_tokenA</td><td>설정할 페어 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>설정할 페어 토큰B 주소</td></tr></tbody></table>



**Example**

```javascript
// 페어 컨트랙트 등록
await MantiswapFactoryContract.setPair(
    pairContract.address,
    mockToken0Contract.address, 
    mockToken1Contract.address
)   
```



