## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Euler
 
 
---

##### What feature differentiates Euler from other DeFi protocols?  

- [ ]  Lending and borrowing
- [ ]  Governance
- [ ]  Debt tokenization
- [x]  Permissionless listing
  
Hint: none
         
Explanation: The main factor that differentiates Euler form other trusted protocols like Aave and Compound is permissionless listing of assets.

Sub Topics: No Sub-Topics
 

---

##### What is the necessary condition to permissionlessly list assets on Euler?  

- [ ]  The asset must go through governance scrutiny
- [ ]  The asset must be worth atleast 1 USD
- [x]  The asset must have a WBTC pair on Uniswap v3
- [ ]  The asset must have a WETH pair on Uniswap V3
  
Hint: none
         
Explanation: The asset must have a WETH pair on Uniswap v3, then it can be added as a lending market on Euler by anyone straight away.

Sub Topics: No Sub-Topics
 

---

##### What are the mechanisms adopted by Euler to minimize risk that comes with listing multiple assets?  

- [x]  Asset tiers
- [x]  Risk-adjusted collateral factor
- [ ]  Strict KYC and AML procedure
- [ ]  None of these
  
Hint: NoHint
         
Explanation: Euler mitigates risk by using different types of pools which can/cannot be isolated from other assets, they have an asset tier list to employ this feature. They also use risk-adjusted collateral factor. This limits the exposure in case there are any bad debts.

Sub Topics: No Sub-Topics
 

---

##### When a user borrows isolation tier asset from an account, that account is locked from further borrowing of any other asset  

- [x]  True
- [ ]  False
  
Hint: NoHint
         
Explanation: Isolation tier assets can only be borrowed in isolation. What this means is that they cannot be borrowed alongside other assets using the same pool of collateral.

Sub Topics: No Sub-Topics
 

---

##### When is an account at the risk of liquidation?  

- [ ]  When the user attempts to borrow two isolated tier assets from the same account
- [ ]  When the user borrows an asset from isolated tier
- [x]  When value of risk adjusted liabilities exceeds value of risk adjusted collateral
- [ ]  Both A and B are false
  
Hint: none
         
Explanation: A borrower is considered to be in violation of Euler when the value of their risk-adjusted liabilities exceeds the value of their risk-adjusted collateral.

Sub Topics: No Sub-Topics
 

---

##### How does Euler handle liquidation incentives differently?  

- [ ]  The percentage discount on seized collateral is fixed
- [x]  The percentage discount on the seized collateral increases as the loan becomes worse (more underwater)
- [ ]  The percentage discount on seized collateral decreases as the loan becomes worse (more underwater)
- [ ]  The liquidation incentive becomes a kind of English auction
  
Hint: NoHint
         
Explanation: In Euler instead of a fixed discount percentage on seized collateral, they allow the discount to increase depending on how far under water a position is.

Sub Topics: No Sub-Topics
 

---

##### Why do we need sub accounts? what is the concept of defer liquidity?  

- [x]  Sub accounts are accounts in Euler that the user can create with the same Ethereum account in order to segregate their liabilites and borrow multiple isolation tier assets from the same Ethereum account
- [x]  Defer liquidity is a concept that allows user to bundle a bunch of transactions and perfom a liquidity check on the user only at the end of the bundle instead of checking after every transaction
- [x]  Defer liqudity is what is done in transaction builder
- [ ]  sub accounts are other Ethereum accounts of the same user
  
Hint: NoHint
         
Explanation: Once a user borrows an isolation tier asset, that account is locked from borrowing further. It would be cumbersome to create multiple ethereum accounts for each borrow from isolation tier, hence sub accounts were introduced where users can create upto 256 subaccounts per ethereum account and manage liabilities in an efficient manner. Defer liquidity  is a function where the user can postpone (defer) liquidity checks on the account so that it is checked once after multiple transactions instead of once every transaction.

Sub Topics: No Sub-Topics
 

---

##### Euler lacks a native concept of flash loans  

- [x]  True
- [ ]  False
  
Hint: NoHint
         
Explanation: Euler lacks a native concept of flash loans. But by making use of the defer liquidity feature, users can make an uncollateralized borrow, perform whatever operation they like, and then repay the borrow - all without being charged extra fees.

Sub Topics: No Sub-Topics
 

---

##### Which of the following is true about dTokens and eTokens  

- [ ]  eTokens keep track of debt
- [x]  dTokens are ERC20-compliant interfaces,dTokens accrue the debt to be paid by users who have borrowed. They can be transferred to other accounts, but instead of transaction approval from the sender, it needs to be approved by the receiver
- [x]  eTokens are ERC20-compliant interfaces that the users receive on supplying collateral to the protocol. They accrue interest and overtime can be redeemed for a larger amount of underlying tokens. They can be redeemed given the redemption will not make open borrows unsustainable.
- [x]  Burning dTokens would mean that the loan is being repaid
  
Hint: NoHint
         
Explanation: Euler tokenises debts on the protocol with ERC20-compliant interfaces known as dTokens. Rather than being able to send tokens to anyone but requiring approval to take them, dTokens can be taken by anyone but require approval to accept them. This also prevents users from "burning" their dTokens. Lenders who deposit into a liquidity pool on Euler, receive interest-bearing ERC20 eTokens in return, which can be redeemed for their share of the underlying assets in the pool at any time, provided there are unborrowed tokens in the pool.

Sub Topics: No Sub-Topics
 

---

##### What is minting and burning in Euler?  

- [x]  Minting is the recursive supplying and borrowing of the same asset as the collateral in order to achieve a leveraged position.
- [ ]  Minting is borrowing EUL by overcollateralization
- [x]  Burning is withdrawing one supply and repaying its respective borrow from the multiple sets of borrows and supplies made in minting
- [ ]  Burning is repaying the borrow position of EUL
  
Hint: NoHint
         
Explanation: Minting is the recursive supplying and borrowing of the same asset as the collateral in order to achieve a leveraged position. Burning is deleting one set of deposit and borrow the multiple sets of deposits and borrows made in minting. Say you have 1000 USDC and you can make a borrow of upto 90% of USDC value, you take a loan of 900 USDC. Now you take the 900 USDC and supply it as collateral. Now with the increased borrowing capacity, you take a loan of 810 USDC and supply it as collateral again. Now in the Euler protocol, you are earning interest on 1710 USDC while you only had 1000 USDC to begin with.

Sub Topics: No Sub-Topics
 
