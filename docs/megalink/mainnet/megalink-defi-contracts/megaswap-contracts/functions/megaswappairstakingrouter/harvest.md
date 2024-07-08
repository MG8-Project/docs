---
description: 'Updated : 2024.07.08'
---

# harvest

```solidity
function harvest( 
    address _tokenA,
    address _tokenB,
    uint _deadline
) external ensure(_deadline)
```



페어 스테이킹 리워드 수령 할 때 사용



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>스테이킹 된 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>스테이킹 된 토큰B 주소<br>(코인의 경우 WETH주소)</td></tr><tr><td>uint </td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Example**

```javascript
// 리워드 수령
await routerContract.harvest(
    mockToken0Contract.address,
    mockToken1Contract.address,
    MaxUint256
) 
```



