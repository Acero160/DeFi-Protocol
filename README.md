# 🔒 DeFi Protocol

A fully decentralized, over-collateralized **Stablecoin System** built on Ethereum.  
This project includes the smart contracts to deploy a decentralized stablecoin (DSC) backed by crypto assets such as WETH and WBTC, along with a secure engine for minting, burning, collateral management, and liquidation.

---

## ⚙️ Key Features

- **Decentralized Stablecoin (DSC)**:
  - Pegged to USD.
  - ERC20 compliant.
  - Minted and burned only by DSCEngine to maintain stability.

- **DSCEngine**:
  - Over-collateralization enforced (minimum health factor > 1).
  - Supports multiple collateral assets (e.g., WETH, WBTC).
  - Automated liquidation process with bonus incentives.
  - Secure price feed integration using Chainlink Oracles.

- **Helper Configuration**:
  - Automatic setup for local (Anvil) or Sepolia testnet environments.
  - Mock deployments for price feeds and tokens during local testing.

---

## 🏗️ How It Works

1. **Collateral Deposit**  
   Users deposit accepted collateral (e.g., WETH, WBTC) into the DSCEngine.

2. **Mint Stablecoins**  
   Based on the value of the deposited collateral, users can mint a proportionate amount of DSC tokens.

3. **Health Factor Maintenance**  
   The system enforces over-collateralization through a health factor mechanism to prevent undercollateralization.

4. **Liquidations**  
   Accounts with a health factor below 1 can be liquidated to secure the protocol’s solvency, rewarding liquidators with a bonus.

5. **Redemption**  
   Users can burn DSC to redeem their original collateral.

---

## 📜 Contracts Overview

| Contract | Description |
|:--------:|:------------|
| **DecentralizedStableCoin** | ERC20 token with mint and burn functionalities restricted to DSCEngine. |
| **DSCEngine** | Core engine that handles collateral management, minting, health factor checks, and liquidations. |
| **DeployDSC** | Deployment script to deploy both DSC and DSCEngine contracts. |
| **HelperConfig** | Helper script to configure price feeds and mock contracts based on the network. |

---

## ✨ Future Improvements

- Add more collateral types (e.g., stablecoins, other bluechip assets).
- Implement governance system for updating parameters like liquidation threshold and bonus.
- Expand to Layer 2 solutions for lower gas fees.

---

## 📬 Contact

If you have any questions or want to collaborate, feel free to reach out via GitHub or open an issue!



