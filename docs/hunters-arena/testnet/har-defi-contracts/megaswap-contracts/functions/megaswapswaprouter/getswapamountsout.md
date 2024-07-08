---
description: 'Updated : 2024.07.08'
---

# getSwapAmountsOut

```solidity
function getSwapAmountsOut(
    uint _amountIn, 
    address[] memory _path
) public view virtual returns (uint[] memory amounts)
```



Swap 시 받을 수 있는 개수를 얻을 때 사용\
(FROM->TO)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint</td><td>_amountIn</td><td>swap 시 바꿀 토큰 개수</td></tr><tr><td>address[]</td><td>_path</td><td>토큰 개수를 확인 할 토큰 쌍 주소</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint[]</td><td>amounts</td><td>swap 시 In/Out 토큰 개수</td></tr></tbody></table>



**※Reserves를 통한 연산 방법**

```solidity
//수수료 사용 유무에 따라 swapFee 지정(30 = 0.03%)
uint amountInWithFee = amountIn*(10000-swapFee)
uint numerator = amountInWithFee*(reserveOut);
uint denominator = (reserveIn*10000)+amountInWithFee;        
amountOut = numerator / denominator;
```



**Example**

```javascript
// swap 토큰 개수 얻기
await routerContract.getSwapAmountsOut(
    10000
    [mockToken0Contract.address, mockToken1Contract.address]
)

// 결과
[ BigNumber { value: "10000" }, BigNumber { value: "4984" } ]
```



