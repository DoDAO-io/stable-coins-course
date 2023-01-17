## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Frax
 
 **FRAX coin**        
### Introduction

The [Frax protocol](https://frax.finance/) is a decentralized stablecoin that utilizes a novel mechanism to maintain price stability. It is open-source and permissionless and is currently implemented on Ethereum and 12 other chains. Frax was founded by Sam Hamidi-Kazemian, Travis Moore, and Jason Huan. It was announced in May 2019 as a Decentral bank and was launched on the Ethereum Mainnet in December 2020. The goal of the Frax protocol is to provide a highly scalable and decentralized form of algorithmic money, as an alternative to fixed-supply digital assets like Bitcoin.


The Frax ecosystem includes two stablecoins, FRAX and FPI, which are pegged to the US dollar and the US Consumer Price Index respectively. It also includes Fraxswap, a native automated market maker, and Fraxlend, a permissionless lending facility.


Frax is unique in that it is a fractional stablecoin, meaning that parts of its supply are backed by collateral and parts are algorithmically stabilized. Fraxswap is the first AMM to use time-weighted average market maker orders, which the Frax protocol uses for rebalancing collateral, minting and redeeming tokens, expanding and contracting FRAX supply, and deploying protocol-owned liquidity on-chain. Fraxlend allows for debt origination, customized non-custodial loans, and onboarding of collateral assets to the Frax Finance economy.


Frax's end goal is to build important decentralized stablecoins in the world, such as the Frax Price Index (FPI) stablecoin, which is pegged to a basket of consumer goods, creating its own unit of account separate from any nation-state denominated money. The Frax ecosystem includes four tokens: FRAX, the stablecoin targeting a tight band around $1/coin; Frax Share (FXS), the governance token of the entire Frax ecosystem which accrues fees, seigniorage revenue, and excess collateral value; FPI, the inflation-resistant, CPI-pegged stablecoin; and FPIS, the governance token of the Frax Price Index.


The Frax ecosystem also includes a Gauge Rewards System, where the community can propose new gauge rewards for strategies that integrate FRAX stablecoins. FXS emissions are fixed, halve each year, and entirely flow to different gauges based on the votes of FXS stakers.


### Price Stability


FRAX utilizes a technique called "arbitrage" to maintain price stability. Arbitrage is the practice of buying and selling assets in different markets to take advantage of price discrepancies. In the case of FRAX, when the price of FRAX rises above its target price, the algorithm will automatically sell FRAX in exchange for another cryptocurrency, such as Ethereum, to bring the price back down. When the price of FRAX falls below its target price, the algorithm will buy FRAX using the cryptocurrency it previously sold, bringing the price back up. Additionally, FRAX has a "mint and burn" mechanism, where when the price of FRAX is above its target price, users can "mint" new FRAX by providing collateral in the form of other cryptocurrencies, and when the price of FRAX is below its target price, users can "burn" FRAX by removing it from circulation. This mechanism helps to ensure that the supply of FRAX remains in line with demand, which helps to keep the price stable.


### Mint and Redeem

![Mint and Redeem](https://github.com/DoDAO-io/stable-coins-course/blob/959308058d7b56bc3dab215b5d03d945572e1dc7/images/mint_redeem.png?raw=true)
`Refernce: https://docs.frax.finance/`

The Frax Protocol's minting and redeeming system plays a crucial role in maintaining the stability of FRAX tokens. Users can mint FRAX by providing both collateral tokens (such as USDC) and governance tokens (FXS). The proportion of each token required is determined by the Frax [collateral ratio](https://docs.frax.finance/price-stability#collateral-ratio) (CR). For example, if the CR is 50%, a user can mint one dollar worth of FRAX by providing $0.50 worth of USDC and $0.50 worth of FXS. The same process reverses when a user chooses to redeem their FRAX for USDC and FXS.


When new FRAX tokens are minted, FXS is burned in proportion to the uncollateralized amount. With a collateralization ratio of 50%, for every FRAX token minted, $0.50 worth of FXS is burned. This decreases the circulating supply of FXS and creates buy pressure for the token. Conversely, when the protocol increases the collateralization ratio, more FXS is minted and distributed, increasing the supply and exerting downward pressure on the price. As usage and adoption of FRAX increases, more FRAX tokens are minted than redeemed, resulting in a large amount of FXS being burned and removed from circulation. This creates a resilient tokenomic model for FXS that helps ensure price stability for FRAX.


All FRAX tokens are fungible with one another and entitled to the same proportion of collateral no matter what collateral ratio they were minted at. This system of equations describes the minting function of the Frax Protocol:

![Mint](https://github.com/DoDAO-io/stable-coins-course/blob/959308058d7b56bc3dab215b5d03d945572e1dc7/images/mint.png?raw=true)
`Refernce: https://docs.frax.finance/`


Redeeming FRAX is done by rearranging the previous system of equations for simplicity, and solving for the units of collateral, Y, and the units of FXS, Z.

![Redeem](https://github.com/DoDAO-io/stable-coins-course/blob/959308058d7b56bc3dab215b5d03d945572e1dc7/images/redeem.png?raw=true)
`Refernce: https://docs.frax.finance/`


### Recollateralization and Buybacks


The Frax Protocol has built-in mechanisms, known as recollateralization and buybacks, to handle situations where additional collateral is needed or excess collateral is present. When the total collateral value in USD falls below the desired collateral ratio, recollateralization allows users to add collateral in exchange for newly minted FXS tokens at a bonus rate of 0.20%. This incentivizes arbitragers to close the gap and restore the collateral ratio for FRAX. On the other hand, buybacks occur when there is more collateral than needed to maintain the collateral ratio. In this case, FXS holders can use FXS tokens to "buy back" the excess collateral, which is then burned by the platform. This converts the excess value into FXS tokens, maintaining the target collateral ratio. However, it's important to note that there is no bonus rate for the buyback function.


### Transparency and Audits


FRAX is committed to transparency and has undergone several independent audits to ensure the security and stability of its platform. The team regularly publishes audit reports and technical details about the platform's underlying smart contracts on its GitHub page, allowing users and researchers to review and verify the platform's code. [Here](https://docs.frax.finance/other/audits) is the complete list of audits.


### Performance Upgrades: veFXS and FRAX v2 AMOs


The Frax protocol has introduced several performance upgrades to its system, including the veFXS and Frax v2 AMOs. The veFXS feature allows FXS holders to lock up their tokens for a certain period of time in order to generate voting escrow FXS and earn bonuses, governance rights, and AMO (Algorithmic Market Operations Controller) profits. The longer the FXS tokens are locked, the more bonuses awarded to the veFXS holders. Additionally, veFXS holders are able to participate in Frax gauges and influence or direct FXS to different FRAX gauges, a similar mechanism established by the Curve protocol and its gauge system.


Recently, [Convex has partnered with the Frax protocol](https://convexfinance.medium.com/december-update-protocol-expansion-cvx-eth-incentive-migration-2c9327b48259#0a3b) to further align the two protocols' incentive programs, specifically around locking veFXS into the CVX protocol. Convex was launched in [May 2021](https://convexfinance.medium.com/convex-finance-pre-launch-announcement-3630b2a428d0) as a platform intended to boost CRV rewards and simplify staking CRV for liquidity providers and stakers by creating an access point to CRV benefits through its native CVX token. As a result, Convex began actively collecting CRV and veCRV tokens as soon as it was introduced. By early summer 2021, it had become the largest holder of veCRV tokens in the [Curve Wars](https://medium.com/bityard/the-curve-wars-explained-2c4e9594617). Curve Finance compensates liquidity providers with CRV tokens, granting governance rights over which protocols' pools are supported through CRV awards and fee sharing.Thus, Frax holds [≈21%](https://daocvx.com/) of CVX giving them substantial governance power in the Convex protocol, which can be thought of as a proxy for veCRV governance power and directing future CRV rewards.


Furthermore, Frax has launched the algorithmic market operations modules, or AMOs, which creates smoother operations for Frax by automating the movement of FRAX and its collateral across the DeFi ecosystem. The Frax AMOs further enable FRAX growth by leveraging Frax’s assets in a capital efficient way.


### Growth and Adoption


One piece of good news for FRAX is the platform's growing user base and trading volume, which have steadily increased since its launch. The market cap reached $130M within a month of launch, and later on reached its peak at $2.9B. As of 14th Jan, 2023 the market cap is at $1.02B. FRAX has also received positive attention from the DeFi community and has partnered with several well-known projects in the space, including Chainlink and Compound.


The Frax protocol offers a new and improved solution for stablecoins by utilizing Automated Market Maker (AMM) technology. By combining the use of FRAX stablecoins and FXS governance tokens, the protocol ensures trustless stability, decentralization and scalability in the face of market instability. Unlike other stablecoins such as Tether or DAI, FRAX eliminates the risk of over-collateralization and sudden market fluctuations.


As the market adapts to the growing demands and challenges, the adoption of crypto and stablecoins continues to rise. Among the latest innovations in the crypto space, FRAX is leading the way with its unique fractional-algorithmic approach to stability. To learn more about FRAX and its approach, visit their [website](https://frax.finance/) as well as [github](https://github.com/FraxFinance) and read their [documentation](https://docs.frax.finance/v/en/), also you can follow them on [Twitter](https://twitter.com/fraxfinance) and join their community on [Telegram](https://t.me/fraxfinance).


### References:


-  https://frax.finance/
-  https://docs.frax.finance/
-  https://messari.io/report/frax-a-fractional-algorithmic-stablecoin
-  https://cryptobriefing.com/defi-project-spotlight-frax-finance-a-sweet-spot-for-stablecoins/
 
 
