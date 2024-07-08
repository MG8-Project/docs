---
description: 'Updated : 2024.07.08'
---

# swapExactETHForTokens



```solidity

function swapExactETHForTokens(    uint _amountOutMin,     address[] calldata _path,    address _to,     uint _deadline) external virtual payable ensure(_deadline) returns (uint[] memory amounts)

코인->토큰으로 swap (FROM->TO)
※ 코인은 msg.value 형태로 추가 

Parameters
```

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint</td><td>_amountOutMin</td><td>swap에서 획득 할 최소 토큰 개수<br>(Slippage 값 이용)</td></tr><tr><td>address[]</td><td>_path</td><td>swap에 사용 될 토큰 쌍 주소</td></tr><tr><td>address</td><td>_to</td><td>swap 할 계정 주소</td></tr><tr><td>uint</td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>

```solidity

Return Values
```

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint[]</td><td>amounts</td><td>swap 된 토큰 개수</td></tr></tbody></table>

```solidity

Example
// 5000 ETH swapconst overrides = {    gasLimit: 9999999,    value : 5000}// 토큰 거래에 대한 허용await mockToken0Contract.approve(routerContract.address, MaxUint256)// swapawait swapRouterContract.swapExactETHForTokens(    0,    [WMATICContract.address, mockToken0Contract.address],    accounts[0].address,    MaxUint256,    overrides)

2022.12.22
```
