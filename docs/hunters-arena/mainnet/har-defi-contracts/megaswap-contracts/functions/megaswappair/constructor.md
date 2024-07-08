---
description: 'Updated : 2024.07.08'
---

# constructor

```solidity
constructor(
    address _factory,
    address _router,
    address _tokenA, 
    address _tokenB, 
    uint8 _swapFee, 
    uint8 _protocolFee,
    address _rewardToken,
    uint256 _rewardPerSecond,
    uint256 _startTimestamp,
    uint256 _bonusEndTimestamp
)
```



유동성풀(**L**iquidity **P**ool)  Pair Contract Contructor



**Parameters**

<table><thead><tr><th width="150">Type</th><th width="150">Value</th><th>Description</th></tr></thead><tbody><tr><td>address</td><td>_factory</td><td>pairFactory Contract 주소</td></tr><tr><td>address</td><td>_router</td><td>pairRouter Contract 주소</td></tr><tr><td>address</td><td>_tokenA</td><td>생성 할 페어 토큰A 주소</td></tr><tr><td>address</td><td>_tokenB</td><td>생성 할 페어 토큰B 주소</td></tr><tr><td>uint8</td><td>_swapFee</td><td>초기 swapFee 비율<br>(30 = 0.3%, 최대 1%)</td></tr><tr><td>uint8</td><td>_protocolFee</td><td>초기 protocolFee 비율<br>(5 = 0.05%, 최대 1%)</td></tr><tr><td>address</td><td>_rewardToken</td><td>스테이킹 시 보상 줄 토큰 주소</td></tr><tr><td>uint256</td><td>_rewardPerSecond</td><td>초당 보상토큰 금액</td></tr><tr><td>uint256</td><td>_startTimestamp</td><td>유동성 풀 생성 날짜</td></tr><tr><td>uint256</td><td>_bonusEndTimestamp</td><td>보상 완료 날짜(최대로 잡기)</td></tr></tbody></table>



**Example**

```javascript
const swapFee = 25;
const protocolFee = 5;
const rewardPerSecond = ethers.utils.parseEther("0.01");
const startTimestamp = parseInt(new Date().getTime() / 1000)
const bonusEndTimestamp = startTimestamp + 86400*30;

pairContract = await (await ethers.getContractFactory("MantiswapPair")).deploy(
    MantiswapFactoryContract.address,
    routerContract.address,
    mockToken0Contract.address, 
    mockToken1Contract.address, 
    swapFee, 
    protocolFee,
    mockRewardTokenContract.address,
    rewardPerSecond,
    startTimestamp,
    bonusEndTimestamp
);

parseInt(new Date().getTime() / 1000)+ 86400*30 = 30일
```



