## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Venus
 
 **About Venus**        

### What is Venus?
Venus is an algorithm based money market system on the BNB blockchain. It is a fork of Compound and MakerDAO.
### Why do we need Venus?
Venus is a powerful lending and borrowing, and stablecoin minting protocol that combines the features of Compound and MakerDAO, allowing users to utilize one collateral for both functionalities.  Built on the binance blockchain, Venus has inherent advantages like quick transaction times and low transaction costs. It provides flexiblity to the user, combining the features of lending and borrowing with minting stablecoins.  In the next section, we will discuss its features in more detail.
### Lending and borrowing
**vTokens** <br>
Each asset supported by the Venus Protocol is integrated through a vToken contract, an EIP-20 compliant representation of balances supplied to the protocol. 
Every time a user interacts with the Venus protocol, they do so through the vTokens smart contract. By supplying assets to the protocol, users earn an equivalent amount  of vTokens of the underlying asset according to the current exchange rate. The exchange rate depends on the supply rate value of the market entered. This means that the number of  vTokens you hold remains the same while the amount of underlying asset you can redeem using it will keep increasing, hence accumulating interest. Interest is accumulated every block in Venus, similar to Compound.
By minting vTokens, users  * Earn interest through the vToken's exchange rate, which increases in value relative to the underlying asset. * Gain the ability to use vTokens as collateral.
Let us now look at the functions offered within the lending and borrowing spectrum in Venus.
* **Mint/Supply -** The mint function allows a user to transfer an asset into the protocol in order to begin accumulating interest based on the current supply rate. The user then receives a quantity of vTokens, which is equal to the number of underlying tokens supplied divided by the current exchange rate.
* **Borrow -** The borrow function allows users to take out a loan from the protocol, which starts accruing interest based on the asset's borrowing rate. The amount borrowed can't be more than the user's account liquidity or the market's available liquidity. We'll discuss account liquidity more later.              
* **Redeem -** The redeem function allows users to convert a specified amount of vTokens into the underlying asset. The amount of underlying tokens received is equal to the number of vTokens redeemed, multiplied by the current exchange rate. To redeem vTokens, the user must have enough liquidity in their account and there must be enough liquidity available in the market. 
* **Repay borrow -** The repay function transfers an asset into the protocol, reducing the user's borrow balance. You can also repay a borrow on behalf of another address using the `repay borrow behalf` function.
### VAI
Like DAI, Venus has its own stablecoin, VAI. VAI is pegged to the USD. VAI is minted by borrowing it at 50% LTV. That is, $100 worth of assets can be used as collateral to mint a maximum of 50 VAI. Borrowing VAI works exactly similar to normal borrowing we have discussed above in the Venus protocol. This is where Venus derives its functionality from MakerDAO.
### Markets
Each token listed on Venus has its own market where it can be supplied and borrowed. Each market in Venus has its own distrubution rate for XVS, and supply and borrow rates for the given asset.  It is not mandatory that all markets provide a supply and borrow rate. For example, currently the XVS market in Venus does not provide any rewards for supplying or borrowing. Enter and Exit markets are commonly used terms when it comes to a market.

**Enter Market -** In order to supply collateral or borrow in a market, it must be entered first. 

**Exit Market -** Exited markets will not count towards account liquidity calculations. To exit would mean that the user has no more open borrows/ debt in the market and the user is not supplying to the market.

### Liquidation                                                                   
**Account liquidity** <br> Account Liquidity represents the USD value of assets borrowable by a user, before it reaches liquidation. Users with a shortfall (negative liquidity) are subject to liquidation, and can’t withdraw or borrow assets until Account Liquidity is positive again. <br><br> **How is it calculated?** <br> For each market the user has entered into, their supplied balance is multiplied by the market’s collateral factor, and summed. Borrow balances (Total amount borrower owes, including interest) are then subtracted, to equal Account Liquidity. Borrowing an asset reduces Account Liquidity for each USD borrowed. Withdrawing an asset reduces Account Liquidity  by the asset’s collateral factor times each USD withdrawn. <br><br> **Liquidation event** <br> A user with negative account liquidity who doesn't have enough collateral to cover their outstanding borrows may be subject to liquidation by other users of the protocol. When a liquidation occurs, a liquidator may repay some or all of an outstanding borrow on behalf of a borrower and in return receive a discounted amount of collateral held by the borrower.  The liquidation incentive is the discount that the liquidator receives. The liquidator first has to seize an asset as collateral as if they are repaying their own borrow, on repaying they receive vTokens with said incentive.


 
 **Rewards and tokens**        


### Tokens and Vaults    
### XVS                                                                                              
**XVS and its distribution**   
XVS is the native token of Venus, used in governance. XVS is earned by interacting with the protocol (by borrowing, lending and staking), for each block that the user is actively supplying to, borrowing from, or staking in the protocol, the user accumulates XVS.                                                                                      How much XVS is distributed to suppliers and borrowers in each market is determined by “venus speed”. This number is updated regularly to ensure that XVS is being distributed proportionally to the amount of utility each market provides.  The venus speed is updated automatically each time a user interacts with the protocol.
**Venus rate**
It is an integer that indicates the rate at which the protocol distributes XVS to markets’ suppliers or borrowers, every BSC block. The value is the amount of XVS (in wei), per block, per given market.

Venus speed is determined by,

` utility = vTokenTotalBorrows * assetPrice `

` utilityFraction = utility / sumOfAllVenusedMarketUtilities `

` marketVenusSpeed = venusRate * utilityFraction `


<br><br> **Claiming XVS**
  <br>
Venus users automatically earn XVS coins for each block they contribute to or borrow from the protocol. The protocol will automatically transfer the accrued XVS to a user's address when the total amount of XVS earned by that address (in a market)  reaches a certain threshold. If the address executes any of the mint, borrow, transfer, liquidateBorrow, repayBorrow, or redeem functions on that market, the user can claim their Venus tokens. Alternatively, users can call the claimVenus method on any  vToken contract at any time for more granular control over which markets to claim from.
<br><br>
### VRT   
Apart from XVS, there is VRT (Venus Reward Token) which was created in order to distribute the liquidity mining distribution among borrowers. VRT can be deposited in the VRT vault to earn rewards. In addition to that there is also provision for the user to exchange between  VRT and XVS at the rate of 12000 VRT = 1 XVS. Currently, VRT can be earned as interest in vaults. Only use case for VRT in the Venus protocol currently is to redeem it for XVS at the rate mentioned above. VRT can also be deposited in the VRT vault to obtain rewards. These two  functions will be available for a period of 12 months, after which VRT will no longer play a role in the Venus ecosystem.
<br><br>
### Venus Vaults
Venus Vault is a mechanism that locks XVS to improve the system’s anti-risk ability and distributes staking rewards. Apart from lending and borrowing to earn XVS, XVS can be staked/ held in Venus vaults to earn it as interest, the rewards are part of  the daily XVS output. It is important to note that XVS is the governance token of the Venus protocol and only staked XVS is eligible to be used as vote in the governance of Venus. Holding XVS in the vault gives you voting power, which you can delegate if  you choose to. Will enable you to obtain income distribution from the Venus protocol. The XVS deposited in the vault will have a 7 day period which you have to wait out till you can redeem your XVS, the XVS deposited in vaults cannot be used as collateral for borrowing.                                                            The Vault has multiple functions such as risk guarantee, voting governance, income distribution and rewards distribution, ensuring that the XVS holders’ benefits and responsibilities are equal.     <br> Venus offers vaults that support VRT, VAI and XVS. By holding VAI and XVS in vaults, the user gets incentivized by XVS. In the VRT vault however, the user get incentivized with VRT itself whose only usecase in the Venus protocol is to use it to redeem XVS.  So it is safe to say that all the vaults supported by Venus incentivize the user ultimately in XVS.

**Vaults in case of risk events**  <br>   After a risk event occurs in Venus and only if the Venus risk fund account is not sufficient to cover the shortfall, the XVS depositor in the vault will pay a maximum of 10% of the total deposit amount to compensate for the loss.

   
  
 **References**        
Here are some important links to learn more about Venus

https://docs.venus.io/docs/

https://blog.venus.io/venus-tokenomics-proposal-final-version-cc9afb51bdb7

https://venus.io/

https://testnet.venus.io/ 
 
