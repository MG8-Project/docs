---
description: 'Updated : 2024.07.08'
---

# withdrawPair

```solidity
function withdrawPair( 
    address _tokenA,
    address _tokenB,
    uint256 _liquidity, 
    uint256 _amountAMin, 
    uint256 _amountBMin,
    uint _deadline
) external ensure(_deadline) returns (uint amountA, uint amountB)
```



토큰+토큰 언스테이킹 할 때 사용 (리워드 자동 획득)

**※ 리턴 사용 안함**



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>스테이킹 된 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>스테이킹 된 토큰B 주소</td></tr><tr><td>uint256</td><td>_liquidity</td><td>언스테이킹 할 토큰 개수<br>(유동성 토큰)</td></tr><tr><td>uint256</td><td>_amountMinA</td><td>스테이킹 할 토큰A 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint256</td><td>_amountMinB</td><td>스테이킹  할 토큰B 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint256 </td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Example**

```javascript
// 토큰+토큰 출금
await routerContract.withdraw(
    mockToken0Contract.address,
    mockToken1Contract.address,
    100000,
    0,
    0,
    MaxUint256
) 
```



