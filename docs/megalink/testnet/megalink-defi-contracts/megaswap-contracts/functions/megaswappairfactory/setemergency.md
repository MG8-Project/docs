---
description: 'Updated : 2024.07.08'
---

# setEmergency

```solidity
function setEmergency(
    address _tokenA, 
    address _tokenB, 
    bool _emergency
) external onlyFeeAdmin
```



Swap기능에 대한 Emergency Flag 장치



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>설정할 페어 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>설정할 페어 토큰B 주소</td></tr><tr><td>bool</td><td>_emergency</td><td>true : swap 중지, <br>false: swap 사용(기본)</td></tr></tbody></table>



**Example**

```javascript
// Emergency Flag 설정
await MantiswapFactoryContract.setEmergency(
    mockToken0Contract.address, 
    mockToken1Contract.address, 
    true
);


```



