# Overview

## Architecture

Hedgehog’s architecture is divided into two main components: the Off-Chain and On-Chain systems. Together, these components form a robust infrastructure that seamlessly bridges traditional financial markets with blockchain technology, ensuring accurate asset representation, dynamic liquidity management, and secure lending operations.

### Off-Chain Component

**Hedgehog LTD (The Company)** is responsible for the traditional finance operations that underpin the system. The key off-chain processes include:

* **Share Acquisition & Tokenization:**\
  Hedgehog LTD purchases shares from various institutions on the stock exchange. These real-world shares are then tokenized using smart contracts on the Hedera Blockchain, ensuring that every token represents a one-to-one claim on the underlying asset.
* **USDC Reserve Management:**\
  To maintain liquidity, the protocol ensures that there is always a sufficient amount of on-chain USDC in reserve. Hedgehog LTD constantly monitors the price fluctuations of the underlying shares. If a stock’s price falls, triggering a potential reserve shortfall, the system automatically restocks the on-chain USDC, ensuring that token holders can reliably exchange their tokens for USDC.

### On-Chain Component

On the blockchain side, Hedgehog leverages smart contracts to manage the lifecycle of tokenized assets and facilitate lending operations. The on-chain architecture is structured around three core smart contracts:

* **PriceOracle:**\
  The PriceOracle is the backbone of the pricing mechanism. It is continuously updated with the latest valuations of the underlying stocks, converting their prices into USDC values. This real-time pricing is essential for accurate token valuation and risk management.
* **Issuer:**\
  The Issuer contract is responsible for the minting and burning of tokenized assets. When Hedgehog LTD purchases shares, the Issuer mints corresponding tokens. Conversely, when tokens are redeemed for USDC, they are burned to maintain the one-to-one backing of assets.
* **Lender:**\
  The Lender contract orchestrates the lending operations. It manages liquidity provision to specific asset pools, issues loans, and handles liquidity withdrawals. This contract ensures that loans are over-collateralized and that asset pools remain adequately funded with USDC.

### Integration & System Flow

1. **Asset Tokenization:**\
   Hedgehog LTD acquires shares and tokenizes them via the Issuer contract, ensuring each token is backed by a real-world asset.
2. **Dynamic Liquidity Management:**\
   The off-chain component monitors market prices and triggers USDC reserve restocking when necessary, ensuring that the on-chain liquidity (managed by the Lender contract) is always sufficient.
3. **Real-Time Price Updates:**\
   The PriceOracle continuously updates asset valuations, which influences both the minting/burning processes and the risk assessment for lending operations.
4. **Lending Operations:**\
   Users can borrow USDC by providing their tokenized shares as collateral. The Lender contract manages the process, ensuring that the loans remain over-collateralized and that any liquidity changes are dynamically managed.

This hybrid architecture leverages the strengths of both traditional finance and blockchain, providing a secure, transparent, and responsive lending platform that is well-equipped to handle market volatility and liquidity challenges.

