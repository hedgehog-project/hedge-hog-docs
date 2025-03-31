# Issuer

The Issuer is the engine behind the creation and management of tokenized assets within the Hedgehog Lending Protocol. Its responsibilities extend across asset tokenization, liquidity management, and regulatory compliance. Here’s an in-depth look at its functions:

* **Token Creation and Management:**\
  The Issuer is responsible for creating the fungible asset that represents tokenized shares. This process guarantees that every token is backed 1:1 with real-world shares held by Hedgehog LTD.
* **Minting and Burning Mechanisms:**\
  When Hedgehog LTD acquires shares, the Issuer mints new tokens that are issued to users in exchange for USDC. Conversely, when users sell tokens back for USDC, the corresponding tokens are burned. This dynamic minting and burning process preserves the one-to-one backing of assets and maintains balance within the system.
* **Token Transactions in USDC:**\
  The Issuer enables a smooth marketplace where users can purchase tokenized assets with USDC and redeem tokens for USDC. The integration with the PriceOracle ensures that these transactions reflect up-to-date market values, fostering a fair and transparent trading environment.
* **KYC and Regulatory Compliance:**\
  To adhere to legal and regulatory standards, the Issuer incorporates Know Your Customer (KYC) procedures. This ensures that only verified user accounts can trade specific tokenized assets, adding an extra layer of trust and compliance to the platform.
* **Reserve Management:**\
  To safeguard liquidity and ensure that users can reliably redeem their tokens, the Issuer maintains at least 90% of USDC reserves for each token. This reserve mechanism is crucial, especially when share prices rise, as it guarantees that there is enough USDC on-chain to support all user claims and token redemptions.

In summary, the Issuer is central to the protocol’s operation, seamlessly integrating asset tokenization with robust liquidity and compliance measures to ensure that all token transactions are secure, transparent, and reflective of real-world market conditions.
