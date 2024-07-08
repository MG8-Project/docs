# investPair

```solidity
function investPair(
    address _tokenA,
    address _tokenB,
    uint256 _amountADesired,
    uint256 _amountBDesired, 
    uint256 _amountAMin, 
    uint256 _amountBMin,
    uint _deadline
)external ensure(_deadline)
```



토큰+토큰 Staking 할 때 사용(LP+Staking)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>스테이킹 할 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>스테이킹 할 토큰B 주소<br>(코인의 경우 WETH주소)</td></tr><tr><td>uint256</td><td>_amountADesired</td><td>스테이킹 할 토큰A 개수</td></tr><tr><td>uint256</td><td>_amountBDesired</td><td>스테이킹 할 토큰B 개수 </td></tr><tr><td>uint256</td><td>_amountAMin</td><td>스테이킹 할 토큰A 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint256</td><td>_amountBMin</td><td>스테이킹 할 토큰B 최소 개수<br>(Slippage 값 이용)</td></tr><tr><td>uint </td><td>_deadline</td><td>트랜잭션 최대 시간<br>(현재시간+종료시간, sec단)</td></tr></tbody></table>



**Example**

```javascript
// 토큰 거래에 대한 허용
await mockToken0Contract.approve(routerContract.address, MaxUint256)
await mockToken1Contract.approve(routerContract.address, MaxUint256)

// Staking(LP+Staking)
await routerContract.investPair(
    mockToken0Contract.address,
    mockToken1Contract.address,
    10000,
    5000,
    0,
    0,
    MaxUint256
)
```



