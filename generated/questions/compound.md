## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Compound
 
 
---

##### What are the differences between Compound V2 and Compound III (V3)?  

- [ ]  Collateral assets no longer earn interest
- [ ]  Only one token, called base token can earn interest and cannot be used as collateral
- [ ]  cTokens are no longer in use
- [x]  All of the above
  
Hint: NoHint
         
Explanation: In the new version of the protocol, there is a separate market for each token. That token acts as the "base token" in that market, only one base token can be set. A supplier can lend the base token in the market and can earn interest. No interest will be accrued by assets that are supplied as collateral and cTokens are no longer used.

Sub Topics: No Sub-Topics
 

---

##### Interest rates for supply and borrow are dependant on?  

- [ ]  A linear function
- [ ]  Governance
- [ ]  Compound DAO
- [x]  Utilization rates
  
Hint: NoHint
         
Explanation: The interest rates for supply and borrowing are based on the utilization rate of the base asset. Given by, `totalborrows / totalsupply` of given asset.

Sub Topics: No Sub-Topics
 

---

##### The supply function is used to perform which of the following actions?  

- [x]  Add collateral
- [x]  Supply base asset
- [x]  Repay borrow
- [ ]  Withdraw more borrowed asset
  
Hint: NoHint
         
Explanation: Supply function can be used to add collateral, supply the base asset, or repay an open borrow of the base asset.

Sub Topics: No Sub-Topics
 

---

##### Any amount of a collateral asset can be supplied to the protocol, there are no supply caps imposed on supplying collateral.  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: Collateral can only be added if the market is below its supplyCap.

Sub Topics: No Sub-Topics
 

---

##### When is an account liquidated?  

- [x]  When the account's borrow balance exceeds the liquidation collateral limit
- [ ]  When the tokens held in the market go above a certain limit
- [ ]  Both A and B are true and both imply the same phenomenon
- [ ]  Both A and B are false
  
Hint: NoHint
         
Explanation: When an account’s borrow balance exceeds the set liquidation collateral limit (which is separate and higher than borrow collateral factor), the account is then eligible for liquidation. Meaning, when the account balance for the account is negative. If a borrower accrues too much interest on their borrow, or the USD value of their collateral reduces, or the USD value of their borrow increases, the account becomes liquidatable.

Sub Topics: No Sub-Topics
 

---

##### What is the governance token of Compound? How can it be earned?  

- [ ]  USDC is the governance token of Compound
- [x]  COMP is the governance token of Compound
- [ ]  The governance token can only be bought from DEXs and not earned from the Compound protocol
- [x]  The governance token can be earned by interacting with the protocol (Lending, borrowing, etc) and can also be bought on DEXs
  
Hint: NoHint
         
Explanation: COMP is the governance token of Compound. It is earned by borrowers and lenders, that is, by interacting with the protocol COMP automatically accrues to the account.

Sub Topics: No Sub-Topics
 

---

##### Which of these is true about COMP distrubution?  

- [x]  COMP is distrubuted in equal amounts to lenders and borrowers
- [ ]  COMP is distrubuted more to borrowers
- [ ]  COMP is sometimes not distrubuted to lenders
- [ ]  COMP distrubution does not follow any pattern
  
Hint: NoHint
         
Explanation: Equal amount of COMP is distrubuted to lenders and borrowers.

Sub Topics: No Sub-Topics
 

---

##### The percentage of the collateral value that can be borrowed is represented by the liquidation collateral factor  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: The percentage of the collateral value that can be borrowed is represented by the borrowing collateral factor

Sub Topics: No Sub-Topics
 

---

##### Which of the following about supply and borrow rate model is true?  

- [ ]  Supply and borrow rate models are one and the same
- [x]  Supply and borrow rate models are two separate models
- [x]  Interest accrues every second in Compound III
- [ ]  Interest accrued is accounted for using cTokens
  
Hint: NoHint
         
Explanation: Supply and borrow rate models are not the same, they are two different models. Interest accrues every second on both borrows and supplies.

Sub Topics: No Sub-Topics
 

---

##### What is the liquidator required to do in a liquidation event? How are they incentivized?  

- [ ]  The protocol does not liquidate bad loans, it instead takes the collateral and starts earning interest on it
- [ ]  The protocol requires the liquidator to seize collateral and repay the loan like it was their own loan, the collateral can be bought at a discounted price by the liquidator using their base token, which can be sold at a higher price for a profit
- [x]  The protocol just requires the liquidator to call the liquidate function, for this, the liquidator is rewarded in base tokens
- [ ]  The protocol liquidates bad loans on its own, there is no need for liquidators
  
Hint: NoHint
         
Explanation: The protocol price feed allows a liquidator to determine the discounted price of seized collateral and sell it publicly. Any account (or liquidator) can buy the discounted collateral using the base asset, and the liquidator can then buy it back at a higher price on a DEX and pocket the difference.

Sub Topics: No Sub-Topics
 
