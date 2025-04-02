# GreenStake Architecture

## Overview
GreenStake is a decentralized platform designed to facilitate donations and investments in renewable energy projects using blockchain technology. The platform ensures transparency, security, and efficiency in fund allocation, allowing users to support green initiatives while earning rewards.

## Architectural Components

### 1. **Frontend**
- **Framework:** Next.js (TypeScript)
- **Styling:** Tailwind CSS
- **Web3 Integration:** `wagmi` for Ethereum interaction
- **Wallet Support:** MetaMask, WalletConnect
- **UI Components:** React-based UI with interactive dashboards

### 2. **Backend & Smart Contracts**
- **Blockchain:** Arbitrum Sepolia (Layer 2 Ethereum)
- **Development Environment:** Hardhat with TypeScript
- **Smart Contracts:**
  - `ProjectListing.sol`: Handles project registration and management
  - `Donate.sol`: Manages donations, fund distribution, and donor tracking
  - `DAO.sol`: Governs community decision-making and fund allocation
  - `ReentrancyGuard.sol`: Security contract preventing reentrancy attacks

### 3. **Smart Contract Architecture**
- **Project Registration:** Owners register renewable energy projects on the blockchain.
- **Donation Handling:** Users send crypto donations, which are securely distributed.
- **Fund Distribution:**
  - **80%** to Project Owner
  - **15%** to DAO members
  - **5%** to the GreenStake platform for maintenance
- **DAO Governance:** DAO members vote on project approvals and funding allocation.
- **Reward Mechanism:** Users receive staking rewards or governance tokens for contributing.

### 4. **Storage & Data Handling**
- **On-Chain Data:** Project metadata, fund transactions, and governance records stored in smart contracts.
- **Off-Chain Data:** User profiles and additional project details managed via decentralized storage (IPFS or Arweave).

### 5. **Security Measures**
- **Reentrancy Protection:** `ReentrancyGuard.sol` ensures secure fund transactions.
- **Access Control:** Only authorized users can modify project details.
- **Transparent Transactions:** All donations and fund movements are publicly verifiable on Arbitrum Sepolia.

### 6. **Deployment Strategy**
- **Smart Contracts:** Deployed using Hardhat scripts to Arbitrum Sepolia.
- **Frontend Hosting:** Hosted on decentralized storage or cloud platforms.
- **Continuous Integration (CI/CD):** Automated testing and deployment using GitHub Actions.

### 7. **User Roles**
- **Donors:** Users who contribute funds to renewable energy projects.
- **Project Owners:** Entities submitting and managing renewable projects.
- **DAO Members:** Community participants responsible for decision-making.
- **Platform Admins:** Handle maintenance and governance of the platform.

## Conclusion
GreenStake's architecture ensures a secure, transparent, and efficient method for funding renewable energy initiatives. By leveraging blockchain, DAOs, and decentralized storage, the platform democratizes access to green investments and fosters sustainable development.

