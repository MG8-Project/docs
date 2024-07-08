---
description: 'Updated : 2024.07.08'
---

# collect



```solidity
function collect(
    address _tokenA,
    address _tokenB,
    uint _deadline
) public ensure(_deadline) returns(uint256 collect0, uint256 collect1)
```



스테이킹 이후 LP Swap 수수료만 받을 때 사용



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>스테이킹 된 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>스테이킹 된 토큰B 주소<br>(코인의 경우 WETH주소)</td></tr><tr><td>uint </td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Return Values**

| Type    | Value    | Description         |
| ------- | -------- | ------------------- |
| uint256 | collect0 | 수령한 tokenA swap 수수료 |
| uint256 | collect1 | 수령한 tokenB swap 수수료 |



**Example**

```javascript
await routerContract.collect(
    mockToken0Contract.address,
    mockToken1Contract.address,
    MaxUint256
) 

// 결과
[ BigNumber { value: "2999999999999999" }, BigNumber { value: "0" } ]
```



