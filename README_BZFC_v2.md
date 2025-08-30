# Byzantium-Coin™ (BZFC)

CoinMarketCap White Paper — v2 (Aug 23, 2025)  
License: MIT  
Ticker: BZFC  
Decimals: 17  
Max Supply: 21,000,000,000,000 BZFC (21T)  
Consensus: PoSA — Proof-of-Stake Authority  
Tech stack: Rust / Substrate (FRAME)

> Upload note: Save this file as `README.md` at the root of your GitHub repo for best presentation.

---

## 1) Abstract

Byzantium-Coin™ (BZFC) is a PoSA-secured Layer-1 chain designed for predictable monetary decay, institutional wrapping, industrial compliance attestations, and actuarial risk pools. Its policy surface is organized under the Smart Heuristic Retrieval (SHR) namespace model, which routes requests to versioned rulebooks so future upgrades never rewrite history. A half-life decay engine—optionally extended to a multi-isotope model—provides flexible, opt-in supply reduction with a hard rule: savings/vault balances never decay.

---

## 2) Quick Facts

- **Name / Ticker:** Byzantium-Coin™ / BZFC  
- **Max Supply:** 21 trillion BZFC (21,000,000,000,000)  
- **Decimals:** 17 (base unit = 10^-17 BZFC)  
- **Consensus:** PoSA (authority set via staking & governance)  
- **Monetary Policy:** Half-life decay (on/off), optional isotope blend, 1 day → 1000 years range; savings exempt  
- **Fees:** Flexible model (Flat or EIP-1559-style), per-namespace add/mult, optional tips; configurable burn split  
- **Wrapping:** 1:1 institutional/customer wraps with vault shielding (underlying held in savings)  
- **Compliance:** Editioned Rulebooks (Θ-II, Θ-III, …) and immutable Attestations  
- **Insurance:** Ψ pools with pot ratios, reserve floors, and payout caps  
- **Open Source:** MIT License (developer-friendly)

---

## 3) SHR Namespace Architecture
*(unchanged — left intact for brevity here)*

---

## 4) Monetary Policy & Decay

### 4.1 Goals
*(unchanged)*

### 4.2 Mechanics (on-chain friendly)

To avoid expensive exponentials on-chain, BZFC uses a per-epoch rate $r_{\text{epoch}}$ with a pooled accounting index:

- **Per-epoch rate from half-life**

$$
r_{\text{epoch}} = 1 - 2^{-\Delta t / T_{1/2}}
$$

- **Isotope blend (weights sum to 1)**

$$
r_{\text{eff}} = \sum_i w_i \cdot \big(1 - 2^{-\Delta t / T_{1/2,i}}\big)
$$

- **Global liquid index update (O(1))**

$$
\text{index}_{\text{new}} = \text{index}_{\text{old}} \cdot (1 - r_{\text{eff}})
$$

All liquid balances scale by the index. Savings/vault balances sit outside the decay path and are never decayed.

---

## 4.3 Savings Exemption
*(unchanged)*

---

## 4.4 Isotope Coupling (optional)
*(unchanged)*

---

## 5) Fees, Burns & Treasury
*(unchanged)*

---

## 6) Wrapping & Vault Shielding (Λ)
*(unchanged)*

---

## 7) Industrial Compliance & Rulebooks (Θ)
*(unchanged)*

---

## 8) Insurance & Actuarial Pools (Ψ)
*(unchanged)*

---

## 9) Consensus & Security (PoSA)
*(unchanged)*

---

## 10) Tokenomics Overview
*(unchanged)*

---

## 11) Mathematics & Developer Notes
*(unchanged — but math refs remain consistent)*

---

## 12) Governance
*(unchanged)*

---

## 13) Compliance & Auditability
*(unchanged)*

---

## 14) Roadmap & Delivery Status
*(unchanged)*

---

## 15) Risk Factors
*(unchanged)*

---

## 16) Legal & Licensing
*(unchanged)*

---

## 17) Listing Information (for CMC)
*(unchanged)*

---

## Appendix A — Example Decay Configuration

- Epoch length: 1 hour  
- Half-life: 100 years → CLI computes $r_{\text{epoch}}$ (Perquintill) for governance.  
- Decay mode: `HalfLife { rate_per_epoch }`  
- Savings lock window: 0 (savers remain fully exempt)

---

## Appendix B — Example Isotope Blend

- Components: 30% ($T_{1/2}=1y$), 70% ($T_{1/2}=10y$)  
- Effective per-epoch rate:

$$
r_{\text{eff}} = 0.3 \cdot r_1 + 0.7 \cdot r_2
$$

---

## Appendix C — Namespace Codes (suggested)

Ω (Omega) = 937, Θ (Theta) = 920, Ψ (Psi) = 936, Λ (Lambda) = 923 (for internal fee routing; configurable)

---
