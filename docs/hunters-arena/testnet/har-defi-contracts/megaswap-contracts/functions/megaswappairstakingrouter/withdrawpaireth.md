---
description: 'Updated : 2024.07.08'
---

# withdrawPairETH

```solidity
function withdrawPairETH( 
    address _token,
    uint _liquidity,
    uint _amountTokenMin,
    uint _amountETHMin,
    uint _deadline
) external ensure(_deadline)
```



토큰+코인 언스테이킹 할 때 사용 (리워드 자동 획득)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_token</td><td>스테이킹 된 토큰 주소</td></tr><tr><td>uint256</td><td>_liquidity</td><td>언스테이킹 할 토큰 개수</td></tr><tr><td>uint256</td><td>_amountMin</td><td>스테이킹 할 토큰 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint256</td><td>_amountETHMin</td><td>스테이킹  할 코인 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint256 </td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Example**

```javascript
// 토큰+코인 출금
await routerContract.withdrawPairETH(
    mockToken0Contract.address,
    100000,
    0,
    0,
    MaxUint256
) 
```



