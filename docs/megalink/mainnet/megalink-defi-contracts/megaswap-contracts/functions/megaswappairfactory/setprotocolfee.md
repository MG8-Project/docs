---
description: 'Updated : 2024.07.08'
---

# setProtocolFee

```solidity
function setProtocolFee(
    address _tokenA, 
    address _tokenB, 
    uint8 _newFee 
) external onlyFeeAdmin
```



유동성풀(**L**iquidity **P**ool) 해제 시 프로토콜 Fee 발생\
Protocol Fee 에 대한 설정(1만 자리, 소수점 2자리까지, 일반적으로 0.05%)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>설정할 페어 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>설정할 페어 토큰B 주소</td></tr><tr><td>uint8</td><td>_newFee</td><td>Fee 금액(30 = 0.3%, 최대 1%)</td></tr></tbody></table>



**Example**

```javascript
// Protocol Fee 설정
await MantiswapFactoryContract.setProtocolFee(
    mockToken0Contract.address, 
    mockToken1Contract.address, 
    5
);

// 0.05% 의 수수료
```



