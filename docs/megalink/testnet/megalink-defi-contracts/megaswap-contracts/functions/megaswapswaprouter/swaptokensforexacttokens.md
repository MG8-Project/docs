---
description: 'Updated : 2024.07.08'
---

# swapTokensForExactTokens

```solidity
function swapTokensForExactTokens(
    uint _amountOut,
    uint _amountInMax,
    address[] calldata _path,
    address _to,
    uint _deadline
) external virtual ensure(_deadline) returns (uint[] memory amounts)
```



토큰->토큰으로 swap (TO->FROM)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint</td><td>_amountIn</td><td>swap을 통해 획득 할 토큰 개수</td></tr><tr><td>uint</td><td>_amountOutMin</td><td>swap에 사용 할 최대 토큰 개수<br>(Slippage 값 이용)</td></tr><tr><td>address[]</td><td>_path</td><td>swap에 사용 될 토큰 쌍 주소</td></tr><tr><td>address</td><td>_to</td><td>swap 할 계정 주소</td></tr><tr><td>uint</td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint[]</td><td>amounts</td><td>swap 된 토큰 개수</td></tr></tbody></table>



**Example**

```javascript
// 토큰 거래에 대한 허용
await mockToken0Contract.approve(routerContract.address, MaxUint256)
await mockToken1Contract.approve(routerContract.address, MaxUint256)

// swap
await swapRouterContract.swapTokensForExactTokens(
    5000,
    MaxUint256,
    [mockToken0Contract.address, mockToken1Contract.address],
    accounts[0].address,
    MaxUint256,
    overrides
)
```



