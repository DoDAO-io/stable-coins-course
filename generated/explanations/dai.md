## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## DAI
 
 **DAI coin**        
### About


DAI is a decentralized stablecoin designed to maintain a value of one US dollar. It was created by the MakerDAO project, which was launched in 2017 by Rune Christensen, the CEO of MakerDAO. MakerDAO is an open-source project that is maintained by a team of developers and a community of volunteers.


DAI is unique in that it is a decentralized stablecoin, which means that it is not issued or controlled by any central authority. Instead, it is generated and managed by a network of smart contracts on the Ethereum blockchain. This decentralized nature of DAI allows it to be free from the influence of governments or financial institutions and makes it more resistant to censorship or interference.


DAI is used in various ways, including as a medium of exchange, a store of value, and a collateral asset. It has gained widespread adoption in the cryptocurrency community and has been used in a number of decentralized finance (DeFi) applications.


### Minting and Burning DAI


Dai is generated when users deposit collateral assets into [Maker Vaults](https://makerdao.com/en/whitepaper/#maker-vaults) (Maker Vaults facilitate the generation of Dai against locked-up collateral. Users open Vaults via the Oasis Borrow dashboard or one of many other user interfaces that allow the management of Vault operations ) within the Maker Protocol. This process allows users to access liquidity and enters Dai into circulation. Others can obtain Dai by purchasing it from brokers or exchanges, or by receiving it as payment.


Once generated, purchased, or received, Dai can be used in the same way as other cryptocurrencies. It can be sent to others, used as payment for goods and services, and even saved through a feature of the Maker Protocol called the [Dai Savings Rate (DSR)](https://ethereumprice.org/guides/article/dai-savings-rate-explained/).


If a user who has borrowed DAI against collateral decides to pay back the loan, the DAI coins are "burned" and the collateral deposit in the account is available for withdrawal. The process of minting and burning DAI helps to maintain its value at or near one US dollar.


The [MCD_DAI_JOIN](https://github.com/makerdao/developerguides/blob/master/dai/dai-token/dai-token.md#mint-and-burn) adapter contract in the Maker Protocol is authorized to call the mint and burn functions of the DAI token in order to increase or decrease the total supply of DAI. These functions are also used when users deposit or withdraw DAI from the Dai Savings Rate contract.


### Transparency and Audits


MakerDAO and the DAI stablecoin are designed to be transparent and auditable. The smart contracts that govern the Collateralized Debt Positions (CDPs) and the minting and burning of DAI are open-source, which allows anyone to review the code and understand how the system works.


In addition, MakerDAO has undergone several independent audits by reputable firms, which have found that the system is secure and functioning as intended. In 2019, Callisto Network Security conducted a security audit of the Dai Token (DAI) smart contract which identified four issues, including three of low severity and one of owner privileges (which could potentially be risky for investors). No critical security issues were discovered. The audit specifically identified known vulnerabilities of ERC-20 tokens, the ability for the contract owner to block transferring, a missing event in ERC20 compliance, and the need to check input addresses for empty values. Overall, the audited smart contract was determined to be safe to deploy, with only low severity issues found during the audit. [Here](https://callisto.network/dai-token-dai-security-audit/) is the complete report.


### Backing of DAI


All DAI is backed by surplus collateral that has been escrowed in audited and publicly viewable Ethereum smart contracts. This means that anyone with an internet connection can monitor the health of the system at any time by visiting [daistats.com](https://daistats.com/). Since, data related to DAI backing is available onchain, it can be queried by anyone. Also there are a number of graphing application that show the runtime information of the system.


The value of the collateral used to mint DAI must always exceed the value of the DAI itself, a process known as overcollaterization. This is to ensure that the collateral can cover the value of the DAI in the event that the market value of the collateral falls. If the value of the collateral falls below the value of the DAI, the vault account may be liquidated, with a ratio of 1.5 collateral to 1 DAI.


To ensure that undercollateralized accounts have sufficient funds to be liquidated, the MakerDAO system offers "keeper" accounts. Keepers are special user accounts that stake their cryptocurrency holdings to provide liquidity to pay off the collateral of vault accounts that lose value over time. This helps to maintain a steady supply of DAI in circulation to match the value of one US dollar.


### Maintaining Peg and Liquidation


Maintaining the peg of Dai is crucial to ensuring its stability and value as a stablecoin. One important aspect of this is the Liquidations system within the Maker Protocol. This system ensures that there is always enough collateral backing the Dai generated in Maker Vaults, and that collateral is auctioned off in a timely and efficient manner if it falls below its designated Liquidation Ratio (LR).


[Keepers](https://blog.makerdao.com/introduction-to-auctions-and-keepers-in-mcd/), who are independent actors typically automated bots, participate in these collateral auctions by bidding. The winning bidder receives the collateral, while a 13% liquidation penalty is added to the debt and levied on Vault owners. Any funds remaining are returned to the Vault owner.


Efficient and effective liquidation mechanisms are vital to maintain Dai stability and confidence in the currency. Collateral auctions must be carried out in a timely manner and in a liquid market environment. The Maker Protocol Liquidations System and Oasis.app provide users with vital information for all collateral assets available in the Maker Protocol.


Recently, Liquidations 1.2 was introduced to address the problem of extreme price volatility and a limited number of Keepers. This solution limits the number of auctions that can occur simultaneously and the total value of collateral being auctioned at any one time. This allows Keepers to recycle capital through exchanges and bid on multiple auctions, providing some protection for Vault owners in the event of a flash crash.


Efforts are also underway to finalize Liquidations 2.0, which aims to further improve the liquidation ecosystem by increasing the number of Keepers, providing a more efficient liquidation process, and improving the overall quality of the Keeper software. These efforts will help ensure that Dai remains stable and maintain confidence in the currency for both Vault owners and users.


### Issues and Hacks


Like any complex system, MakerDAO and DAI have experienced some issues and challenges. 


[On March 12th and 13th, 2020](https://medium.com/@whiterabbit_hq/black-thursday-for-makerdao-8-32-million-was-liquidated-for-0-dai-36b83cac56b6), the MakerDAO Protocol experienced a significant loss of 5.67 million DAI due to liquidations on the platform. This event, known as Black Thursday, was caused by a combination of factors including the drop in Ether price, blockchain congestion, and manipulation by liquidators.


The high gas prices associated with the congestion on the blockchain caused a delay in the update of the MakerDAO oracles, which provide the market price of Ether. This created an opportunity for liquidators to exploit the situation by bidding low amounts of DAI in liquidation auctions, as there were no other competitors at the time. This tactic led to massive profits for a small group of liquidators, but resulted in significant losses for Vault owners and the MakerDAO system as a whole.


In response to the crisis, the MakerDAO community came together to discuss and implement solutions. Instead of shutting down the system, the decision was made to launch a Debt Auction, where users can buy freshly minted MKRs (the governance token of MakerDAO) for DAI. The goal is to dilute the token share of current MKR holders and help eliminate the system debt. Additionally, new system parameters were selected to make it more difficult for fraudulent manipulations in the future. These include increasing the maximum lot size from 50 to 500 ETH and extending the duration of auction rounds.


The Black Thursday event exposed vulnerabilities in the MakerDAO Protocol and highlighted the need for continued monitoring and improvements to the system. The community is actively working to address these issues and prevent similar situations from occurring in the future. However, it's worth mentioning that security is always a trade-off and a zero-risk system is not possible.


### Good and Bad News


DAI has generally been well-received and has gained widespread adoption as a stablecoin. It has been used in various applications, including as a medium of exchange, a store of value, and a collateral asset.


However, there are also some concerns about the backing of DAI and the potential for market manipulation. Some critics have argued that the reliance on Ethereum as collateral makes DAI vulnerable to fluctuations in the value of Ethereum.


[Recently](https://cointelegraph.com/news/makerdao-should-seriously-consider-depegging-dai-from-usd-founder), MakerDAO founder Rune Christensen has suggested that the organization should "seriously consider" depegging its stablecoin, DAI, from the US dollar following recent sanctions on cryptocurrency mixer Tornado Cash and the freezing of USDC addresses by Circle. Christensen raised concerns over DAI's heavy reliance on a centralized asset, USDC, which represents over 50% of MakerDAO's DAI collateralization, according to Dai Stats. The stablecoin is currently the fourth largest USD-pegged stablecoin in the cryptocurrency market, with a market cap of $7 billion. The idea of converting all USDC from MakerDAO's peg stability module into ether was met with criticism, with Ethereum co-founder Vitalik Buterin calling it a "risky and terrible idea."


Despite these concerns, DAI has proven to be a reliable and stable stablecoin, and its use is likely to continue to grow in the future.


### References


  - `https://originstamp.com/blog/what-is-dai-coin-and-why-is-it-special/`
  - `https://makerdao.com/en/whitepaper/`
  - `https://blog.makerdao.com/the-maker-protocols-liquidations-system-upgrade-1-2-is-live/`
  - `https://blog.makerdao.com/the-market-collapse-of-march-12-2020-how-it-impacted-makerdao/`
 
 
