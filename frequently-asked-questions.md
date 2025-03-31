# Frequently Asked Questions

1. **What is Hedgehog and what does it do?**\
   Hedgehog is an on-chain lending protocol on the Hedera network. It transforms real-world shares into fungible tokens, which users can deposit as collateral to borrow KES. The system bridges traditional finance with blockchain by integrating tokenization, a real-time price oracle, and dynamic liquidity management.
2. **How does Hedgehog use tokenized real-world shares as collateral?**\
   Hedgehog converts physical shares into digital tokens with a one-to-one backing. Hedgehog LTD acquires the shares, tokenizes them via smart contracts (through the Issuer), and these tokens then serve as collateral for borrowing operations on-chain.
3. **What blockchain network powers Hedgehog?**\
   Hedgehog is built on the Hedera network, leveraging its speed, security, and scalability for secure and efficient on-chain lending.
4. **How does asset tokenization work in the system?**\
   Hedgehog LTD buys real-world shares and uses smart contracts to mint tokens representing those shares. When a user redeems tokens for KES, the corresponding tokens are burned, ensuring that every token always has a real-world asset backing.
5. **What role does the PriceOracle play in Hedgehog?**\
   The PriceOracle continuously updates token valuations by converting real-world share prices into USDC values. This real-time data drives accurate minting/burning, risk management, and dynamic liquidity adjustments, ensuring that all on-chain transactions reflect current market conditions.
6. **How is liquidity managed on the platform?**\
   Liquidity management is handled through a dual system:
   * **Off-Chain:** Hedgehog LTD monitors share prices and maintains an on-chain KES reserve, automatically replenishing it if needed.
   * **On-Chain:** The Lender contract organizes liquidity pools, mints LP tokens for KES deposits, and ensures that loans are over-collateralized.
7. **How do the off-chain and on-chain components interact?**\
   The off-chain component (managed by Hedgehog LTD) handles share acquisition, tokenization, and reserve management. Meanwhile, the on-chain smart contracts (PriceOracle, Issuer, and Lender) manage token valuation, minting/burning, and lending operations. Together, they create a seamless bridge between traditional financial assets and blockchain-based lending.
8. **What are the key functions of the Issuer contract?**\
   The Issuer is responsible for creating and managing the tokenized assets. It mints tokens when shares are acquired and burns them upon redemption, maintaining a strict one-to-one asset backing. It also enables token transactions in KES and incorporates KYC processes to ensure regulatory compliance.
9. **How does the Lender contract facilitate borrowing and ensure over-collateralization?**\
   The Lender contract sets up dedicated lending pools for each tokenized asset. Users borrow USDC by providing tokenized shares as collateral. The system requires borrowers to over-collateralize (125% of the loan value) and mandates a 110% repayment, with an automatic liquidation trigger if collateral values drop to 90% of the initial value.
10. **What risk control mechanisms are integrated into Hedgehog?**\
    Hedgehog employs several safeguards:
    * **Dynamic Liquidity Management:** Ensures sufficient KES reserves.
    * **Real-Time Price Updates:** Keeps token valuations current via the PriceOracle.
    * **Over-Collateralization:** Borrowers must maintain collateral above the loan amount.
    * **Automated Liquidation:** Triggers if collateral value falls too low.
    * **Circuit Breaks and Unsolvability Conditions:** Prevent systemic failures during market stress.
11. **How are KYC and regulatory compliance handled?**\
    The Issuer contract integrates KYC procedures, ensuring that only verified users can trade tokenized assets. This compliance measure enhances trust and aligns with regulatory standards.
12. **What happens if the value of the collateral falls below the required threshold?**\
    If the collateral's value drops to 90% of its initial level, the Lender contract automatically triggers a liquidation process. This mechanism is designed to protect the system by maintaining the necessary over-collateralization and minimizing risk.
13. **How are LP tokens used in the lending pools?**\
    When users deposit USDC into a lending pool, they receive LP tokens representing their share of that pool. These tokens allow users to claim a proportional return on lending activities and facilitate smooth withdrawals from the pool.
14. **How does borrowing work**

    Users borrow KES from the Lending contract by providing their tokenised shares as collateral at 125% collateral.&#x20;
15. **How does lending work**

    Users can provide liquidity into lending pools for specific assets and get back liquidity pool tokens that represent their share of the pool.
16. **How does purchasing tokens work**

    To purchase a token for a specific asset, you pay KES to the Issuer smart contract and it will deposit the equivalent amount of the token in your wallet.
17. How does selling work.

    To sell a token you send the token you want sold to the Issuer and it will deposit the current valuation based on the latest updated price from the oracle to your account.
