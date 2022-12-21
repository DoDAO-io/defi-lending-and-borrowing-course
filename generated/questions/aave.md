## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Aave
 
 
---

##### How do aTokens accrue interest for the supplier / lender?  

- [x]  The number of aTokens in the user's possession keeps increasing while the rate of exchange between atokens and the underlying tokens remains the same
- [ ]  The number of aTokens in the user's possession keeps remains the same while the rate of exchange between atokens and the underlying tokens keeps increasing
- [ ]  The number of aTokens in the user's possession keeps increasing while the rate of exchange between atokens and the underlying tokens also increases
- [ ]  aTokens are not used as of Aave V3
  
Hint: NoHint
         
Explanation: The value of an aToken is pegged to the value of the corresponding asset at a 1:1 ratio, and the user accumulates aTokens in their wallet according to the interest rate offered.

Sub Topics: No Sub-Topics
 

---

##### What logic does Aave follow to keep count of user's debt?  

- [x]  Debt tokenization
- [ ]  Calculation and accounting of debt in smart contracts
- [ ]  Appointing individuals to keep track of debt
- [ ]  Both A and C
  
Hint: NoHint
         
Explanation: Aave uses debt tokenization to keep count of user's debt called Debt tokens. Debt tokens are interest-accruing tokens that are minted and burned on borrow and repay, representing the debt owed by the token holder and are non-transferrable.

Sub Topics: No Sub-Topics
 

---

##### What are the types of debt tokens in Aave?  

- [ ]  EMI debt tokens
- [ ]  Transferrable debt tokens
- [x]  Variable debt tokens
- [x]  Stable debt tokens
  
Hint: NoHint
         
Explanation: Stable and variable debt tokens are the two type of debt tokens in Aave.

Sub Topics: No Sub-Topics
 

---

##### Which of these functionalities in Aave is built upon flash loans?  

- [ ]  Interest on supplied asset
- [x]  Collateral trading and repaying with collateral
- [ ]  Debt tokenization
- [ ]  Credit delegation
  
Hint: NoHint
         
Explanation: Collateral swapping / trading and Repay with collateral are built by using Flash Loans V2.

Sub Topics: No Sub-Topics
 

---

##### Which of the following are use cases of aTokens  

- [ ]  Repay loans
- [ ]  Accrue interest on supplied collateral
- [ ]  Debt tokenization
- [x]  Both A and B
  
Hint: NoHint
         
Explanation: aTokens are used to accrue interest, and they can also be used to directly repay loans without redeeming them for their underlying tokens.

Sub Topics: No Sub-Topics
 

---

##### Which of the following is a use case for E-Mode  

- [ ]  Minimize capital efficiency
- [x]  Maximize capital efficiency
- [ ]  To borrow newly listed assets
- [ ]  To improve the security of the protocol
  
Hint: NoHint
         
Explanation: E-Mode allows the borrower to maximize capital efficiency by increasing the LTV and lowering the liquidation threshold on assets borrowed in E-Mode.

Sub Topics: No Sub-Topics
 

---

##### Which of the following modes in Aave allows the user to list new assets with a designated debt ceiling?  

- [x]  Isolation mode
- [ ]  E-Mode
- [ ]  Siloed borrowing mode
- [ ]  New listing mode
  
Hint: NoHint
         
Explanation: Isolation mode on Aave lets you list new assets as Isolated with a designated debt ceiling.

Sub Topics: No Sub-Topics
 

---

##### In what denomination are the rewards users get for staking Aave in the Safety Module?  

- [ ]  In stkAAVE
- [ ]  In underlying tokens
- [ ]  Only in aTokens
- [x]  Both A and B
  
Hint: NoHint
         
Explanation: The Aave Protocol V3 now supports multiple rewards per token, which means that it's possible for an asset listing to enable additional incentive rewards denominated in underlying tokens.

Sub Topics: No Sub-Topics
 

---

##### Debt tokens are transferrable.  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: False, debt tokens are not transferrable.

Sub Topics: No Sub-Topics
 

---

##### How does locking your AAVE in the Safety Module help in a shortfall event?  

- [ ]  Part of the AAVE locked in the Safety Module will be given to the lenders in the market where there is a shortfall
- [x]  Part of the AAVE locked in the Safety Module will be auctioned off to help raise funds to cover the deficit
- [ ]  The AAVE locked in the Safety Module will be unlocked and given back to those who staked it
- [ ]  The Safety Module does not help in the event of a shortfall
  
Hint: NoHint
         
Explanation: If a Shortfall Event occurs, part of the locked AAVE is auctioned on the market to help raise funds to cover the deficit.

Sub Topics: No Sub-Topics
 

---

##### What are the ways of participating in liquidating a bad loan?  

- [x]  By calling liquidationCall directly in the pool contract and by creating bots or automated systed to liquidate bad loans
- [ ]  By buying the collateral from the address with bad debt by an off-chain settlement
- [ ]  Only by calling liquidationCall directly in the pool
- [ ]  Only by creating your own automated system to liquidate loans
  
Hint: NoHint
         
Explanation: A user with negative account liquidity who doesn't have enough collateral to cover their outstanding borrows may be subject to liquidation by other users of the protocol. When a liquidation occurs, a liquidator may repay some or all of an outstanding borrow on behalf of a borrower and in return receive a discounted amount of collateral held by the borrower.

Sub Topics: No Sub-Topics
 

---

##### Users can only receive awards on their behalf for staking AAVE.  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: False, Aave V3 allows users to claim rewards to another account, as well as themselves, and to claim multiple types of rewards per asset in a single transaction.

Sub Topics: No Sub-Topics
 
