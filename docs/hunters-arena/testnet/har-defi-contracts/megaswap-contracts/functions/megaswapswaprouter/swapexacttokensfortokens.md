---
description: 'Udpated : 2024.07.08'
---

# swapExactTokensForTokens



```solidity
function swapExactTokensForTokens(
    uint _amountIn,
    uint _amountOutMin,
    address[] calldata _path,
    address _to,
    uint _deadline
) external virtual ensure(deadline) returns (uint[] memory amounts)
```



토큰->토큰으로 swap (FROM->TO)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint</td><td>_amountIn</td><td>swap에 사용 할 토큰 개수</td></tr><tr><td>uint</td><td>_amountOutMin</td><td>swap에서 획득 할 최소 토큰 개수<br>(Slippage 값 이용)</td></tr><tr><td>address[]</td><td>_path</td><td>swap에 사용 될 토큰 쌍 주소</td></tr><tr><td>address</td><td>_to</td><td>swap 할 계정 주소</td></tr><tr><td>uint</td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint[]</td><td>amounts</td><td>swap 된 토큰 개수</td></tr></tbody></table>



**Example**

```javascript
const overrides = {
    gasLimit: 9999999
}

// 토큰 거래에 대한 허용
await mockToken0Contract.approve(routerContract.address, MaxUint256)
await mockToken1Contract.approve(routerContract.address, MaxUint256)

// swap
await swapRouterContract.swapExactTokensForTokens(
    1000,
    0,
    [mockToken0Contract.address, mockToken1Contract.address],
    accounts[0].address,
    MaxUint256,
    overrides
)
```



