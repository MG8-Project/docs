---
description: 'Updated : 2024.07.08'
---

# getSwapAmountsIn



```solidity

function getSwapAmountsIn(    uint _amountOut,     address[] memory _path) public view virtual returns (uint[] memory amounts)

Swap 시 받을 수 있는 토큰 개수를 넣을 시 변경되어야 할 토큰 개수를 얻을 때 사용 
(TO->FROM)

Parameters
```

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint</td><td>_amountOut</td><td>swap 시 얻을 토큰 개수</td></tr><tr><td>address[]</td><td>_path</td><td>토큰 개수를 확인 할 토큰 쌍 주소</td></tr></tbody></table>

```solidity

Return Values
```

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint[]</td><td>amounts</td><td>swap 시 In/Out 토큰 개수</td></tr></tbody></table>

```solidity

※Reserves를 통한 연산 방법
//수수료 사용 유무에 따라 swapFee 지정(30 = 0.03%)uint numerator = (reserveIn*amountOut)*10000;uint denominator = (reserveOut-amountOut)*(10000-swapFee);amountIn = (numerator / denominator)+1;

Example
// swap 토큰 개수 얻기await routerContract.getSwapAmountsIn(    5000    [mockToken0Contract.address, mockToken1Contract.address])// 결과[ BigNumber { value: "10031" }, BigNumber { value: "5000" } ]

2023.01.02
```
