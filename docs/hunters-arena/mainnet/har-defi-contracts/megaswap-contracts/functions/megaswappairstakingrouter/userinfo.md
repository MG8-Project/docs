---
description: 'Updated : 2024.07.08'
---

# userInfo

```solidity
function userInfo( 
    address _tokenA, 
    address _tokenB,
    address _to
) external view returns(
    uint256 liquidity, 
    uint256 reward, 
    uint256 cumulativeReward, 
    uint256 feeCollect0,
    uint256 feeCollect1
)
```



페어 스테이킹 금액 및 수령 받을 수 있는 리워드 얻을 때 사용



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>스테이킹 된 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>스테이킹 된 토큰B 주소<br>(코인의 경우 WETH주소)</td></tr><tr><td>address</td><td>_to</td><td>확인 할 사용자 주소</td></tr></tbody></table>



**Return Values**

| Type    | Value            | Description  |
| ------- | ---------------- | ------------ |
| uint256 | liquidity        | 예치 된 LP 값    |
| uint256 | reward           | 리워드 수령 가능 개수 |
| uint256 | cumulativeReward | 누적 리워드 보상    |
| uint256 | feeCollect0      | swap 수수료     |
| uint256 | feeCollect1      | swap 수수료     |



**Example**

```javascript
// 유저정보 (예치금+리워드 수령액)
await routerContract.userInfo(
    mockToken0Contract.address,
    mockToken1Contract.address,
    accounts[1].address
) 
    
// 결과
[ BigNumber { value: "3535" }, BigNumber { value: "9999" }, BigNumber { value: "0" },
BigNumber { value: "0" }, BigNumber { value: "2999999999999999" } ]

// 유저정보 (예치금+리워드 수령액)
await routerContract.connect(accounts[1]).userInfo(
    mockToken0Contract.address,
    WMATICContract.address,
    accounts[1].address
) 
    
// 결과
[ BigNumber { value: "7071" }, BigNumber { value: "9999" }, BigNumber { value: "0" },
BigNumber { value: "0" }, BigNumber { value: "2999999999999999" } ]
```



