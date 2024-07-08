---
description: 'Updated : 2024.07.08'
---

# getPriceImpact

```solidity
function getPriceImpact(
    uint256 _tokenAmount,
    address[] memory _path
) public view returns (uint256 priceImpact)
```



유동성풀의 영향도를 구할 때 사용

(Swap 시 기본 5%로 설정)



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Explain</th></tr></thead><tbody><tr><td>uint256</td><td>_tokenAmount</td><td>교환 할 토큰 개수</td></tr><tr><td>address[]</td><td>_path</td><td>영향도를 확인 할 토큰 쌍 주소</td></tr></tbody></table>



**Return Values**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Explain</th></tr></thead><tbody><tr><td>uint256</td><td>priceImpact</td><td>영향도 %<br>1만자리(백분율, 소수점2까지 표현)</td></tr></tbody></table>



**※ Reserves를 통한 연산 방법**

```solidity
//수수료 사용 유무에 따라 swapFee 지정(30 = 0.03%)
uint amountInWithFee = amountIn*(10000-swapFee)
uint numerator = amountInWithFee*(reserveOut);
uint denominator = (reserveIn*10000)+amountInWithFee;
destAmount = numerator / denominator;


amountA = (amountIn*(10000-swapFee))/(10000)      
amountInFee = (amountA*reserveB) / reserveA
if (amountInFee <= destAmount) {
    priceImpact = 0;
} else {
    priceImpact = (((amountInFee - destAmount) * 10000) / amountInFee);
}
```



**Example**

```javascript
// 영향도 얻기
await routerContract.getPriceImpact(
    10000,
    [mockToken0Contract.address, mockToken1Contract.address]
)

// 결과 (0.02%의 영향도)
BigNumber { value: "2" }    
```



