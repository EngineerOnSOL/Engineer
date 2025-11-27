<div align="center">
  <img src="https://i.imgur.com/yaK8qjS.png" alt="The Engineer Protocol Banner" width="100%">
  
  # The Engineer Protocol
  
  ### Reputation-Based Staking on Solana
  
  [![Solana](https://img.shields.io/badge/Solana-14F195?style=for-the-badge&logo=solana&logoColor=white)](https://solana.com)
  [![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/engineer_on_sol)
  
  **Build your engineering rank through time commitment, not capital alone.**
  
</div>

---

## Overview

The Engineer is a **reputation-based staking protocol** deployed on Solana that rewards consistent commitment through dynamic reward scaling, progressive rank multipliers, and NFT-enhanced benefits. Unlike traditional staking protocols that favor capital concentration, The Engineer emphasizes **time commitment** and **consistent participation**.

### Key Features

- **Time-Based Reputation System** - Earn reputation through stake duration, not amount
- **Progressive Rank System** - 5 engineering ranks from Apprentice to Chief Engineer
- **NFT License Gates** - Unlock enhanced multipliers (1.5x - 3.0x) with NFT credentials
- **Dynamic Pool Scaling** - Reward rates adjust based on pool availability
- **Vault Rotation** - 10 independent vaults prevent single-point depletion
- **Hourly Distributions** - Real-time reward accrual and claiming

---

## How It Works

### Stake Tokens
Stake $ENGINEER tokens for a minimum of 1 hour, maximum of 24 hours.

### Earn Reputation
- **Base Rate:** +1 reputation per full hour staked
- **6-Hour Bonus:** +2 additional reputation (total +8 for 6 hours)
- Reputation accumulates across all staking sessions

### Climb Ranks
| Rank | Reputation Required | Base Multiplier | NFT Required |
|------|---------------------|-----------------|--------------|
|  Apprentice Engineer | 0 - 49 | 1.0x | No |
|  Junior Engineer | 50 - 149 | 1.2x | No |
|  Senior Engineer | 150 - 399 | 1.5x | **Yes** |
|  Principal Engineer | 400 - 799 | 2.0x | **Yes** |
|  Chief Engineer | 800+ | 3.0x | **Yes** |

###  Unlock Multipliers
- **Without NFT:** Capped at 1.2x multiplier (Junior Engineer)
- **With NFT:** Full multiplier access based on reputation tier
- **NFT Mint Requirements:** 150+ reputation + 0.15 SOL

---

## Reward Calculation

The protocol uses a multi-factor reward calculation:
```
Base Reward = Staked Amount × 1% per hour
Pool-Scaled Reward = Base Reward × (Pool Percentage / 100)
Final Reward = Pool-Scaled Reward × Rank Multiplier
```

### Example Scenarios

**Scenario A: High Reputation, No NFT**
- Stake: 1,000 ENGINEER for 1 hour
- Reputation: 500 (Principal Engineer tier)
- Pool Status: 80% remaining
- NFT: No
```
Base: 1,000 × 1% = 10 tokens
Pool-Scaled: 10 × 0.80 = 8 tokens
Multiplier: 8 × 1.2 = 9.6 tokens (capped at Junior)
```

**Scenario B: High Reputation + NFT**
- Stake: 1,000 ENGINEER for 1 hour
- Reputation: 500 (Principal Engineer tier)
- Pool Status: 80% remaining
- NFT: Yes
```
Base: 1,000 × 1% = 10 tokens
Pool-Scaled: 10 × 0.80 = 8 tokens
Multiplier: 8 × 2.0 = 16 tokens (full Principal multiplier)
```

---

## Tokenomics

### Total Supply
- **1,000,000,000 ENGINEER** tokens

### Reward Distribution
- **Total Rewards:** 200,000,000 tokens (20% of supply)
- **Vault Structure:** 10 independent vaults
- **Per Vault:** 20,000,000 tokens (2% of supply)
- **Distribution:** Sequential vault rotation

### Dynamic Reward Scaling

The protocol implements automatic reward rate adjustment based on pool depletion:

| Pool Status | Hourly Rate |
|-------------|-------------|
| 100% Full | 1.00% |
| 75% Full | 0.75% |
| 50% Full | 0.50% |
| 25% Full | 0.25% |

This mechanism ensures **multi-month sustainability** and prevents rapid pool exhaustion.

---

## NFT License System

### Engineer License NFT
The Engineer License NFT functions as a **"Senior Engineer License"** that unlocks enhanced multiplier tiers.

**Specifications:**
- Collection Size: 100 NFTs
- Mint Cost: 0.15 SOL
- Mint Requirement: Minimum 150 reputation
- Limit: One per wallet address
- Transferable: Yes (benefits tied to holder's reputation)

**Functionality:**
```solidity
if (user.hasNFT && user.reputation >= 150) {
    applyFullRankMultiplier();
} else {
    capAtJuniorMultiplier(1.2x);
}
```

---

### Staking Steps

1. **Connect Wallet**
```
   Visit: https://www.the-engineer.fun/
   Connect your Phantom wallet
```

2. **Stake Tokens**
```
   Minimum: 1 hour
   Maximum: 24 hours
   Recommended: 6 hours (for reputation bonus)
```

3. **Earn & Claim**
```
   Reputation accrues automatically
   Rewards can be claimed hourly
```

4. **Mint NFT** (Optional)
```
   Requires: 150+ reputation
   Cost: 0.15 SOL
   Unlocks: Full multiplier access
```

---

## Reputation Examples

| Stake Duration | Reputation Earned | Notes |
|----------------|-------------------|-------|
| 30 minutes | 0 | Below minimum |
| 1 hour | +1 | Base rate |
| 2 hours | +2 | Base rate |
| 5 hours | +5 | Base rate |
| **6 hours** | **+8** | **+6 base + 2 bonus** |
| 12 hours | +14 | +12 base + 2 bonus |
| 24 hours | +26 | +24 base + 2 bonus |

> **Pro Tip:** Stake in 6-hour increments to maximize reputation efficiency with the cycle bonus.

---

## 🛠️ Technical Stack

- **Blockchain:** Solana
- **Smart Contracts:** Rust (Anchor Framework)
- **Frontend:** React.js / Next.js
- **Wallet Integration:** Wallet Adapter
- **NFT Standard:** Metaplex
- **Data Storage:** IPFS (NFT metadata)

---

## 🔗 Links

- **Website:** [the-engineer.tech](https://www.the-engineer.tech/)
- **Twitter:** [@Engineer_on_sol](https://x.com/Engineer_on_sol)

---

## Disclaimer

This protocol involves financial risk. Staking rewards are not guaranteed and depend on pool availability, market conditions, and protocol parameters. Always DYOR (Do Your Own Research) before participating in any DeFi protocol.

---

<div align="center">
  
  ### Built with by The Engineer Team
  
  **Rewarding commitment, not just capital.**
  
</div>
