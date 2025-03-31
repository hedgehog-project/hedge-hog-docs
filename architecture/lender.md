# Lender

The Lender is the backbone of the lending operations in the Hedgehog Lending Protocol. It is responsible for creating and managing lending pools, facilitating liquidity provision and withdrawals, and overseeing the entire loan lifecycle. Below are the key functionalities of the Lender:

* **Lending Pool Creation:**\
  The Lender creates dedicated lending pools for each tokenized asset issued by the Issuer. These pools aggregate liquidity and allow users to contribute USDC, creating a diversified pool for borrowing and lending activities.
* **Reserve Formation for Collateralized Assets:**\
  For every asset within a lending pool, the Lender establishes reserves to secure collateralized positions. These reserves are critical for maintaining the stability and liquidity of the lending process, ensuring that there is sufficient backing for all collateralized assets.
* **Liquidity Provision and LP Token Minting:**\
  Users can deposit USDC into a specific asset lending pool, which in turn mints liquidity provider (LP) tokens. These LP tokens represent the user’s share in the pool and entitle them to a proportional return on the lending activities conducted within the pool.
* **Liquidity Withdrawal Mechanism:**\
  The Lender facilitates the smooth withdrawal of liquidity from asset lending pools. This allows users to redeem their LP tokens for the underlying USDC, ensuring that liquidity is accessible when needed.
* **Loan Origination at 125% Collateral:**\
  The Lender enables users to take out loans using their tokenized assets as collateral. Loans are structured such that the borrower must provide collateral valued at 125% of the loan amount based on the current USDC price valuation, ensuring a healthy over-collateralization buffer.
* **Loan Repayment at 110% of the Loan Value:**\
  Borrowers are required to repay 110% of the loan amount, reflecting an interest margin and adding an extra layer of security to the lending protocol. This repayment model ensures that the protocol can cover potential losses and maintain liquidity.
* **Liquidation Process:**\
  If the value of the collateral falls to 90% of its initial value, the Lender automatically triggers the liquidation process. This mechanism is designed to protect both the lender and the system by minimizing the risk of under-collateralization, thereby preserving the overall stability of the protocol.

In summary, the Lender component integrates a comprehensive suite of functions that manage liquidity pools, collateralization, loan issuance, and risk mitigation. By enforcing strict collateral and repayment requirements, and incorporating automatic liquidation protocols, the Lender ensures that the Hedgehog Lending Protocol operates in a secure, efficient, and transparent manner.
