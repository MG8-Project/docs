---
description: 'Updated : 2024.07.08'
---

# MegaSwapSwapRouter

## Contract info

**Contract name**: MegaSwapPairSwapRouter

View the **MegaSwapSwapRouter** contract on:



**Source**\
[https://github.com/imantisco/cling-swap-sc-v2/blob/main/contracts/ClingswapPairSwapRouter.sol](https://github.com/imantisco/cling-swap-sc-v2/blob/main/contracts/ClingswapPairSwapRouter.sol)



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

<table><thead><tr><th width="401.2064807837227">Error String</th><th width="242.33333333333331">Description</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>MantiswapSwapRouter: E01</td><td>트랜잭션 시간 초과</td><td></td><td></td></tr><tr><td>MantiswapSwapRouter: E02</td><td>가격 영향도 초과</td><td></td><td></td></tr><tr><td>MantiswapSwapRouter: E03</td><td>불충분한 교환 될 토큰 개수</td><td></td><td></td></tr><tr><td>MantiswapSwapRouter: E04</td><td>초과된 교환 토큰 개수</td><td></td><td></td></tr><tr><td>MantiswapSwapRouter: E05</td><td>유효하지 않은 주소(WETH)</td><td></td><td></td></tr></tbody></table>



