## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Venus
 
 
---

##### Which of these features are available in Venus?  

- [ ]  Lending and borrowing
- [ ]  Stablecoin minting feature
- [ ]  Permissionless listing
- [x]  Both A and B
  
Hint: NoHint
         
Explanation: Venus has the features of a money market protocol and stablecoin minting protocol together.

Sub Topics: No Sub-Topics
 

---

##### What are the usecases of vTokens?  

- [ ]  To accrue interest only assets supplied
- [ ]  To accrue debt and be used as collateral
- [ ]  To accrue debt only
- [x]  To accrue debt and interest for borrowed and supplied assets respectively and be used as collateral
  
Hint: NoHint
         
Explanation: vToken contract is used for interacting with all the currency supported by Venus. They can be used as collateral to borrow.

Sub Topics: No Sub-Topics
 

---

##### The Mint (supply) function in Venus is used to?  

- [ ]  To mint their stable coin, VAI
- [ ]  To recursively supply and borrow the same asset to achieve a leveraged position
- [x]  To supply assets and mint vTokens
- [ ]  None of these
  
Hint: NoHint
         
Explanation: The mint function in venus is used to supply assets to the protocol and mint an equivalent amount of vTokens for the underlying asset.

Sub Topics: No Sub-Topics
 

---

##### What asset is VAI pegged to? At what LTV is it borrowed at?  

- [ ]  VAI is pegged to the EUR, it has LTV of 60%
- [ ]  VAI is pegged to the ETH, it has LTV of 70%
- [ ]  VAI is pegged to the gold, it has LTV of 20%
- [x]  VAI is pegged to the USD, it has LTV of 50%
  
Hint: NoHint
         
Explanation: VAI is pegged to the USD and it is borrowed at 50% LTV.

Sub Topics: No Sub-Topics
 

---

##### What is account liquidity? How is it calculated?  

- [x]  Account liquidity represents USD value of assets borrowable by user before it reaches liquidation
- [ ]  Account liquidity represents total collateral supplied to the protocol by the user
- [ ]  The total collateral supplied by user to each market is multipled with the respective collateral factor and then summed, to give account liquidity
- [x]  Supplied balance is multiplied by the market’s collateral factor, and summed. Borrow balances (Total amount borrower owes, including interest) are then subtracted, to equal Account Liquidity
  
Hint: NoHint
         
Explanation: Account Liquidity represents the USD value of assets borrowable by a user, before it reaches liquidation. For each market the user has entered into, their supplied balance is multiplied by the market’s collateral factor, and summed. Borrow balances (Total amount borrower owes, including interest) are then subtracted, to equal Account Liquidity.

Sub Topics: No Sub-Topics
 

---

##### What is the governance token of Venus?  

- [ ]  VEN is the governance token of Venus
- [x]  XVS is the governance token of Venus
- [ ]  VAI is the governance token of Venus
- [ ]  VNS is the governance token of Venus
  
Hint: NoHint
         
Explanation: XVS is the goveranance token of Venus

Sub Topics: No Sub-Topics
 

---

##### How is the amount of XVS distrubuted decided?  

- [x]  Decided by a value called "venus speed"
- [ ]  Decided by a value called "XVS distrubution rate"
- [ ]  Decided by VenusDAO
- [ ]  Decided by price oracles
  
Hint: NoHint
         
Explanation: How much XVS is distributed to suppliers and borrowers in each market is determined by “venus speed”. This number is updated regularly to ensure that XVS is being distributed proportionally to the amount of utility each market provides.

Sub Topics: No Sub-Topics
 

---

##### What is VRT? What is its use case?  

- [x]  VRT is Venus Reward Token, used to redeem XVS at a fixed rate
- [ ]  VRT is Venus Repeat Token, used to borrow XVS at a fixed rate
- [ ]  VRT is Venus Reward Token, used to gain interest at a fixed rate
- [ ]  VRT is Venus Return Token, used to redeem XVS at a fixed rate
  
Hint: NoHint
         
Explanation: VRT is Venus Reward Token, it can be redeemed for XVS at a fixed rate.

Sub Topics: No Sub-Topics
 

---

##### A user gains voting power by accumulating XVS in their account from interacting with the protocol  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: False, a user cannot gain voting power just by XVS accumulating XVS by interacting with the protocol. XVS has to be staked to get voting power.

Sub Topics: No Sub-Topics
 

---

##### How do vaults help Venus in the case of a shortfall (negative account liquidity) event?  

- [ ]  There are no vaults in Venus
- [x]  In case Venus risk funds are not sufficient to cover the shortfall, the XVS vault will be liquidated to to a maximum of 10% per user's deposited XVS to cover the loss
- [ ]  Immediately, the XVS vault will be liquidated to to a maximum of 10% per user's deposited XVS to cover the loss
- [ ]  XVS vaults are not used in times of risk events
  
Hint: NoHint
         
Explanation: After a risk event occurs in Venus and only if the Venus risk fund account is not sufficient to cover the shortfall, the XVS depositor in the vault will pay a maximum of 10% of the total deposit amount to compensate for the loss.

Sub Topics: No Sub-Topics
 

---

##### What happens when a user has negative account liquidity?  

- [x]  The user will be liquidated, their collateral will be sold for a discounted price and their loan will be repaid in parts or whole by a liquidator
- [ ]  The user will be liquidated, their collateral will be held by the protocol and their loan will be repaid in parts or whole by a liquidator
- [ ]  The user will be warned by the Venus DAO
- [ ]  The user will be allowed to stay with negative liquidity without facing any consequences
  
Hint: NoHint
         
Explanation: A user with negative account liquidity who doesn't have enough collateral to cover their outstanding borrows may be subject to liquidation by other users of the protocol. When a liquidation occurs, a liquidator may repay some or all of an outstanding borrow on behalf of a borrower and in return receive a discounted amount of collateral held by the borrower.

Sub Topics: No Sub-Topics
 
