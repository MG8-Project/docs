---
description: 'Updated : 2024.07.08'
---

# investPairETH

```solidity
function investPairETH(
    address _token,
    uint _amountTokenDesired,
    uint _amountTokenMin,
    uint _amountETHMin,
    uint _deadline
)external payable ensure(_deadline)
```



토큰+코인 Staking 할 때 사용(LP+Staking)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_token</td><td>스테이킹 할 토큰 주소</td></tr><tr><td>uint256</td><td>_amountDesired</td><td>스테이킹 할 토큰 개수</td></tr><tr><td>uint256</td><td>_amountMin</td><td>스테이킹 할 토큰 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint256</td><td>_amountETHMin</td><td>스테이킹 할 Coin 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint </td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Example**

```javascript
const overrides = {
  gasLimit: 9999999,
  value : ethers.utils.parseEther("50.0")
}

// 토큰 거래에 대한 허용
await mockToken0Contract.approve(routerContract.address, MaxUint256)

// Staking(LP+Staking)
await routerContract.investPairETH(
    mockToken0Contract.address,
    ethers.utils.parseEther("20.0"),
    0,
    0,
    MaxUint256,
    overrides
)
```



