---
description: 'Updated : 2024.07.08'
---

# getLiquidityPair

```solidity
function getLiquidityPair(
    address _tokenA,
    address _tokenB,
    uint256 _amountIn
) external view returns (
    uint256 amountA,
    uint256 amountB
)
```



페어  토큰을 통해 각 토큰의 비율을 얻을 때 사용(페어스테이킹)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>LP 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>LP 토큰B 주소</td></tr><tr><td>uint256</td><td>_amountIn</td><td>얻으려는 수량</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="223">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint256</td><td>amountA</td><td>tokenA의 개수</td></tr><tr><td>uint256</td><td>amountB</td><td>tokenB의 개수</td></tr></tbody></table>



**※Reserves를 통한 연산 방법**

```solidity
uint amountB = (amountA*reserveB) / reserveA;
```



**Example**

```javascript
// 유동성풀을 통한 토큰 개수 얻기
await ComputeContract.connect(accounts[0]).getLiquidityPair(
    mockToken0Contract.address,
    mockToken1Contract.address,
    1000000
)

// 결과 (토큰A, 토큰B 개수)
[ BigNumber { value: "1000000" }, BigNumber { value: "500000" } ]
```



2023.01.11
