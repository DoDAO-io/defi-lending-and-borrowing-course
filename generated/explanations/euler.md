## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Euler
 
 **About Euler**        

### What is Euler 
Euler is a non-custodial DeFi protocol that allows users to lend and borrow and the main factor that differentiates Euler form other trusted protocols like Aave and Compound is that,  in Euler any asset that has a WETH pair on Uniswap v3 can be added as a lending market on Euler by anyone straight away. There is a  significant unmet demand for lending and borrowing  the long tail of crypto assets which are not listed on Aave or Compound. Euler is managed by holders of a protocol native governance token called Euler Governance Token (EUL). 

### Asset Tiers
Listing multiple assets which are not necessarily mainstream comes with risk as their price can fluctuate a lot. Euler mitigates this risk by using different types of  pools which can/cannot be isolated from other assets.  This limits the exposure in case there are any bad debts. Another concept adopted by Euler is that they consider the risk factor of both the collateral and the borrowed asset to come up with the maximum amount that can be borrowed for the said collateral-liability asset pair called **risk-adjusted collateral**.   For example, in borrowing XYZ with a collateral factor of 0.5, say you are using $1000 USDC with a collateral factor of 0.9, the maximum amount borrowable would come out ot be 1000*0.5*0.9 = $450 worth of XYZ as opposed to the usual 1000*0.9 that we are used to. 
* Isolation-tier -** ** assets are available for ordinary lending and borrowing, but they cannot be used as collateral to borrow other assets, and they can only be borrowed in isolation. What this means is that they cannot be borrowed alongside other assets using the same pool of collateral.  * Cross-tier -** ** assets are available for ordinary lending and borrowing, and cannot be used as collateral to borrow other assets, but they can be borrowed alongside other assets. For example, if a user has USDC and DAI as collateral, and they want to borrow cross-tier assets ABC and XYZ, then they can do so from a single account on Euler. * Collateral-tier - assets are available for ordinary lending and borrowing, cross-borrowing, and they can be used as collateral. For example, a user can deposit collateral assets DAI and USDC, and use them to borrow collateral assets UNI and LINK, all from a single account.

### Liquidations
A borrower is considered to be in violation of Euler when the value of their risk-adjusted liabilities exceeds the value of their risk-adjusted collateral. A borrower who has just become in violation still has enough collateral to repay their loan, but is at risk of defaulting on their loan. As a result,  they may be liquidated to limit the potential for them to default. One of the issues with a fixed discount percentage for the liquidators on the collateral of the loan they repaid is that potential liquidators often have to engage in priority gas auctions (PGA) in order to find profitable liquidations, which exposes  the liquidation bonus as MEV (miner extractable value). In Euler they allow the discount to increase depending on how far under water a position is. Now, liquidators are forced to engage into a type of Dutch auction. As the discount gradually goes up, each liquidator must decide if they want to bid for a liquidation at the current discount being offered. Liquidator A might  be able to profit at 4%, but liquidator B might be so at 3.5% because they have a more efficient operation. This process is made more efficient by the TWAP oracles used on the Euler network which allow for a more smooth price movement over time which facilitates the dutch auction, preventing all liquidators from jumping in at once.

### Internal Working
Lenders who deposit into a liquidity pool on Euler, receive interest-bearing ERC20 eTokens in return, which can be redeemed for their share of the underlying assets in the pool at any time, provided there are unborrowed tokens in the pool.  Euler tokenises debts on the protocol with ERC20-compliant interfaces known as dTokens. The dToken interface allows the construction of positions without needing to interact with underlying assets, and can be used to create derivative products that include debt obligations. Euler uses a reversed version of the regular ERC20 transfer/approved methods for dTokens. This means that rather than being able to send tokens to anyone but requiring approval to take them, dTokens can be taken by anyone but require approval to accept them. This also prevents users from "burning" their dTokens.

### Other Important Features
Euler has a lot of innovative features and models that are built on top of the base lending and borrowing layer. These are

#### Minting & Burning and Leverage:
Minting is the recursive supplying and borrowing of the same asset as the collateral in order to achieve a leveraged position. Eg: Say you have 1000 USDC and you can make a borrow of upto 90% of USDC value, you take a loan of 900 USDC. Now you take the 900 USDC and supply it as collateral. Now with the increased borrowing  capacity, you take a loan of 810 USDC and supply it as collateral again. Now in the Euler protocol, you are earning interest on 1710 USDC while you only had 1000 USDC to begin with, thus increasing your yield. This concept of recursive borrowing and supplying is “Mint” and what it helps the user achieve is called leverage.
Burning is to delete one set of “borrow” and “deposit”, that is to repay one borrow position and withdraw the respective collateral i.e deleting one set of deposit and borrow the multiple sets of deposits and borrows made. 

#### Sub Accounts
Euler also has a very protocol specific feature called sub-accounts. Once an account is borrowed in an isolated tier, it would be locked from borrowing other assets. In order to not limit the user, Euler enables every Ethereum account to create up-to 256 sub-accounts, allowing the user to segregate their liabilities according to their needs.

#### Transaction Builder
Euler allows users to bundle a bunch of actions that would otherwise be separate transactions on their own into one by using the transaction builder. This feature ties in with the defer liquidity feature where the liquidity check on the user is done after a bundle of transactions considered as one, whereas usually, a liquidation  check is performed after every action that requires user liquidity (Borrow, withdraw etc). 

#### Feeless Flash Loans
Euler lacks a native concept of flash loans. But by making use of the defer liquidity feature, users can make an uncollateralized borrow, perform whatever operation they like, and then repay the borrow - all without being charged extra fees. This can be used to rebalance positions, build-up leveraged positions, take advantage of external arbitrage opportunities, and more. Because Euler only charges fees according to the time value of money, and from the blockchain's perspective flash loans are held for a duration of 0 seconds, they are entirely free on Euler (ignoring gas costs).

#### Interest Rates
To improve capital efficiency and do away with errors in determining parameters for the interest rates of every lending market, Euler uses reactive interest rates. By using a PID controller, Euler amplifies or dampens the rate of change in interest rates when utilization is above or below the target level of utilization respectively. As a result, reactive interest rates  that adapt to market conditions for the underlying asset in real-time are created, without the need for ongoing governance intervention. Interest is accrued every second on Euler.

 
 **EUL token**        

## EUL
The total supply of EUL is 27,182,818 (in homage to Euler’s number,[ e](https://en.wikipedia.org/wiki/E_(mathematical_constant))). The total supply of EUL is fixed for the first 4 years, after which EUL token holders may enact a governance proposal to inflate the supply by a maximum 2.718% per year. In that scenario, newly minted EUL will enter circulation via the Treasury.
The Euler protocol will be managed by holders of the Euler Governance Token (EUL), a native governance token for the protocol. EUL tokens will represent the voting power of the protocol software. Holders with enough EUL tokens will be able to make a formal proposal for change on the protocol. Token holders will then be able to vote on the proposal themselves or delegate their vote shares to a third party. 
Decisions token holders might vote on include proposals to alter:
* The tier of an asset * Collateral and borrow factors * Price oracle parameters * Reactive interest rate model parameters * Reserve factors
**How can you earn EUL?** The Euler token (EUL) is distributed to borrowers on select markets on the platform. Note that EUL is only earned by borrowing and cannot be earned by simply lending to the protocol.

   
  
 **References**        
Here are some important links to learn more about Compound III (V3)

https://docs.euler.finance/getting-started/white-paper

https://app.euler.finance/

https://goerli.euler.finance/ 
 
