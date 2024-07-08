---
description: 'Updated : 2024.07.08'
---

# getLiquidityValue

```solidity
function getLiquidityValue(
    address _tokenA,
    address _tokenB,
    uint256 _liquidityAmount
) external view returns (
    uint256 tokenAAmount,
    uint256 tokenBAmount
)
```



유동성 풀 Token을 통해 각 토큰의 개수를 얻을 때 사용



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>LP 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>LP 토큰B 주소</td></tr><tr><td>uint256</td><td>_liquidityAmount</td><td>LP 토큰 개수</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="223">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint256</td><td>tokenAAmount</td><td>tokenA의 개수</td></tr><tr><td>uint256</td><td>tokenBAmount</td><td>tokenB의 개수</td></tr></tbody></table>



**Example**

```javascript
// 유동성풀을 통한 토큰 개수 얻기
await ComputeContract.connect(accounts[0]).getLiquidityValue(
    mockToken0Contract.address,
    mockToken1Contract.address,
    1000000
)

// 결과 (토큰A, 토큰B 개수)
[ BigNumber { value: "1414213" }, BigNumber { value: "707106" } ]
```



