---
description: 'Updated : 2024.07.08'
---

# MegaSwapPairStakingRouter

## Contract info

**Contract name**: MegaSwapPairStakingRouter

View the **MegaSwapPairStakingRouter** contract on:



**Source**\
[https://github.com/imantisco/cling-swap-sc-v2/blob/main/contracts/ClingswapPairStakingRouter.sol](https://github.com/imantisco/cling-swap-sc-v2/blob/main/contracts/ClingswapPairStakingRouter.sol)



\
**How to Slippage**\
\
Max Slippage:

```javascript
let slippagePercentage = 0.5;
const slippageMax = 1 + slippagePercentage / 100;

let max = amountsIn[0]*slippageMax;
```

Min Slippage:

```javascript
let slippagePercentage = 0.5;
const slippageMin = 1 - slippagePercentage / 100;

let min = amountsOuts[1]*slippageMin;
```



**Error Values**

<table><thead><tr><th width="401.2064807837227">Error String</th><th width="242.33333333333331">Description</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>MantiswapPairRouter: E01</td><td>트랜잭션 시간 초과</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E02</td><td>토큰 주소가 0인 경우</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E03</td><td>불충분한 토큰A</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E04</td><td>불충분한 토큰B</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E05</td><td>토큰 개수 0</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E06</td><td>요청된 토큰 개수가 유동성 초과</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E07</td><td>유동성 0</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E08</td><td>리워드 토큰 개수 0</td><td></td><td></td></tr><tr><td>MantiswapPairRouter: E09</td><td>전체 유동성 0</td><td></td><td></td></tr></tbody></table>



