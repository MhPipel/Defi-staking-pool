
# DeFi ERC20 Staking Pool

A secure and production-style ERC20 staking smart contract designed for decentralized finance (DeFi) applications.  
This project demonstrates best practices in Solidity development, smart contract security, and on-chain reward distribution.

---

##  Overview

This staking pool allows users to stake ERC20 tokens and earn rewards over time.  
Rewards are distributed proportionally based on the user's stake and staking duration.

The contract is built using OpenZeppelin libraries and follows modern Solidity security patterns.

---

##  Features

- ERC20 token staking
- Time-based reward distribution
- Secure reward calculation
- Reentrancy protection
- Owner-controlled reward rate
- Compatible with Remix IDE

---

## Architecture

- **StakingPool.sol**
  - Core staking logic
  - Reward calculation per token
  - Secure stake, withdraw, and claim functions

- **MockERC20.sol**
  - Test ERC20 token for local testing and demos

---

##  Security Considerations

- Uses OpenZeppelin `ReentrancyGuard` to prevent reentrancy attacks
- Uses OpenZeppelin `Ownable` for access control
- Prevents zero-amount staking and withdrawals
- Immutable token addresses for safety

---

##  Deployment (Remix IDE)

1. Open Remix IDE
2. Create a new workspace
3. Add both contracts to the `contracts` folder
4. Compile using Solidity version `0.8.20`
5. Deploy `MockERC20`
6. Deploy `StakingPool` using the MockERC20 address
7. Approve tokens before staking
8. Stake tokens and claim rewards

---

##  Example Workflow

```text
approve(stakingPoolAddress, amount)
stake(amount)
claimReward()
