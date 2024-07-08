---
description: 'Updated : 2024.07.08'
---

# getShareOfPool



```solidity
function getShareOfPool( 
   address _tokenA, 
   address _tokenB, 
   uint _amountADesired, 
   uint _amountBDesired, 
   bool _owned
)external view returns (uint poolRatio)
```



유동성 풀의 지분율 구할 때 사용



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_tokenA</td><td>LP 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>LP 토큰B 주소</td></tr><tr><td>uint</td><td>_amountADesired</td><td>LP 토큰A 개수</td></tr><tr><td>uint</td><td>_admoutBDesired</td><td>LP 토큰B 개수 </td></tr><tr><td>bool</td><td>_owned</td><td>소유중인 유동성 풀 지분율 확인 여부<br>true : 소유중인 유동성 풀 지분율<br>false : 값에 의한 유동성 풀 지분</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>uint</td><td>poolRatio</td><td>지분 %<br>1만자리(백분율, 소수점2까지 표현)</td></tr></tbody></table>



**※ Reserves를 통한 연산 방법**

```solidity
// totalLiquidity의 경우 pairContract totalSupply()를 통해 획득

liquidity = Math.min((amount0*totalLiquidity) / _reserve0, (amount1*totalLiquidity) / _reserve1);
totalLiquidity = totalLiquidity+liquidity;

// 1만자리 연산을 위해..
uint _numerator  = liquidity * (10 ** 5);
uint _quotient =  ((_numerator / (totalLiquidity)) + 5) / 10;

if( liquidity > 0 )
    return _quotient >= 10000 ? 10000 : _quotient;
else
    return 0;
```



**Example**

```javascript
// 지분율 얻기(값에 의한)
await routerContract.getShareOfPool(
    mockToken0Contract.address, 
    mockToken1Contract.address, 
    ethers.utils.parseEther("10.0"), 
    ethers.utils.parseEther("5.0"),
    false
)

// 결과 (9.09%의 영향도)
BigNumber { value: "909" }

    
// 지분율 얻기(소유중인)
await routerContract..getShareOfPool(
    mockToken0Contract.address,
    mockToken1Contract.address,
    0,
    0,
    true
)
    
// 결과 (100%의 영향도)
BigNumber { value: "10000" }
```



