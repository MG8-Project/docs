---
description: 'Updated  : 2024.07.08'
---

# setSwapFee

```solidity
function setSwapFee(
    address _tokenA, 
    address _tokenB, 
    uint8 _newFee 
) external onlyFeeAdmin
```



Swap 시 SwapFee 발생\
SwapFee 에 대한 설정(1만 자리, 소수점 2자리까지, 일반적으로 0.3%)

**※Swap Fee 의 경우 LP 등록한 사람에게 수수료로 보상(지분율에 따라 차등)**



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>설정할 페어 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>설정할 페어 토큰B 주소</td></tr><tr><td>uint8</td><td>_newFee</td><td>SwapFee 금액(30 = 0.3%, 최대 1%)</td></tr></tbody></table>



**Example**

```javascript
// Swap Fee 설정
await MantiswapFactoryContract.setSwapFee(
    mockToken0Contract.address,
    mockToken1Contract.address,
    25,
) 

// 0.25% 의 수수료
```



