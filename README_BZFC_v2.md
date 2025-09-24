Byzantium-Coin (BZFC) White Paper — v3 (Sept 2025)
License: MIT
Ticker: BZFC
Decimals: 17
Max Supply: 21,000,000,000 BZFC (21B)
Consensus: PoSA — Proof-of-Stake Authority
Tech stack: Rust / Substrate (FRAME)
Official Website: https://byzantinefuturecapital.com
1) Abstract
Byzantium-Coin (BZFC) is a PoSA-secured Layer-1 blockchain designed for predictable supply reduction through traditional burn mechanisms, as well as advanced Monetary Half-Life and Part-Life decay models, alongside institutional wrapping, industrial compliance attestations, and actuarial risk pools.

Its modular policy surface is organized under the Smart Heuristic Retrieval (SHR) Namespace Architecture, which ensures all actions are routed to versioned rulebooks so upgrades never rewrite history.

BZFC integrates ISO-compliant mechanisms for financial messaging (ISO 20022), industrial attestations (ISO 9000), and security frameworks (ISO 27000). A pre-market burn-in phase reduced genesis supply from 1 trillion coins to 21 billion coins (final Max Supply). Thereafter, supply policy continues under configurable traditional burns, Monetary Half-Life, Part-Life, or Isotope models, while vault savings remain permanently exempt from decay.
2) Quick Facts
Name / Ticker: Byzantium-Coin / BZFC
Max Supply: 21,000,000,000 (21B, post-burn)
Decimals: 17 (base unit = 10⁻¹⁷ BZFC)
Consensus: PoSA (authority set via staking & governance)
Monetary Policy:
 - Pre-market burn (1T → 21B, ~60 days or flexible TBA)
 - Long-term Monetary Half-Life (1 day → 1000 years, savings exempt)
 - Part-Life fractional models (e.g., 3/16, 13/16)
 - Isotope blends (multi-component decay)
Fees: Flexible (Flat, EIP-1559-style, namespace-aware, configurable burn split)
Wrapping: 1:1 vault-shielded wraps for institutions & derivatives
Compliance: Editioned Rulebooks (Θ), immutable Attestations (ISO 9000 aligned)
Insurance: Ψ pools with pot ratios, reserve floors, payout caps
Open Source: MIT License (developer-friendly)
3) Pre-Market Burn Phase
Before mainnet listing, BZFC executed a pre-market burn-in run to compress supply to its final sustainable level:

- Genesis Supply: 1,000,000,000,000 BZFC (1T)
- Target Supply: 21,000,000,000 BZFC (21B)
- Duration: Governance-configurable — a short-term aggressive Monetary Half-Life may achieve full compression in ~60 days or timeframe TBA
- Mechanism: Accelerated Monetary Half-Life decay, optionally coupled with Part-Life tuning
- Final Max Supply: 21B BZFC (fixed for listings, exchanges, and explorers)

This burn phase is presented transparently as a pre-market supply adjustment, ensuring that CoinMarketCap, CoinGecko, and exchanges recognize the final Max Supply of 21B as the listing figure.
4) SHR Namespace Architecture
BZFC organizes policy into Greek-letter namespaces with immutable Roman-numeral editions:

- Ω (Omega): Monetary policy, decay, fees, vaults, savings, payments
- Θ (Theta): Industrial compliance attestations & certifications (ISO 9000 aligned)
- Ψ (Psi): Insurance pools, pot ratios, actuarial models
- Λ (Lambda): Wrapping, derivatives, cross-chain vault certificates

The SHR Router ensures all transactions are routed to the rulebook edition active at the time of action. Later rulebooks never rewrite history.
5) Monetary Policy & Decay
- Traditional Burns: One-time supply reductions via governance or protocol events
- Monetary Half-Life: Governance-controlled half-life, tunable from 1 day → 1000 years
- Part-Life: Fractional decay mechanisms (e.g., 3/16, 13/16 reductions)
- Isotope Models: Multi-component decay curves blending multiple half-lives
- Index Accounting: Efficient pooled decay index (O(1) per epoch)
- Savings Exemption: Vault balances are decay-free
- Governance Flexibility: On-chain referenda for all parameters, with event logging
6) ISO Compliance Mechanisms
ISO 20022 (Financial Messaging)
- BZFC transactions, fees, and vault wraps can be exported in ISO 20022-style message schemas
- Enables interoperability with banks, payment rails, and custodians

ISO 9000 (Industrial Compliance)
- Θ namespace rulebooks allow audits, material certification, and attestations
- Example: refinery steel batch audit recorded on-chain, ISO 9001 references locked in edition Θ-II

ISO 27000 (Security)
- PoSA validators operate under ISO 27001-aligned controls: key management, redundancy, monitoring
- Governance changes are logged immutably for audit reproducibility
7) Fees, Burns & Treasury
- Modes: Off, Flat, or EIP-1559
- Namespace-aware knobs (Ω/Θ/Ψ/Λ)
- Tips: optional
- Burn Split: Governance defines burn vs treasury
- Events: FeeCharged{total,burned,treasury} for transparency
8) Wrapping & Vault Shielding (Λ)
- 1:1 wrapping for institutional tokens or derivatives
- Underlying BZFC moved from Liquid → Savings vault (decay-exempt)
- Lifecycle: wrap_mint(policy, amount) / wrap_burn(policy, amount)
- Metadata: hash references (IPFS CIDs) for compliance and shielding rules
9) Industrial Compliance & Rulebooks (Θ)
- Register / lock rulebook editions
- Attestations bind subject hashes + payload evidence
- Annotations (Info, Supersede, Revoke) are append-only
- Aligns with ISO 9000 / 17025 audit principles
10) Insurance Pools (Ψ)
- Governance-defined pools: pot ratios, reserve floors, claim caps
- Premiums: Liquid → Savings vault (decay-exempt)
- Claims: Savings vault → claimant Liquid
- Actuarial counters for analytics
11) Consensus & Security (PoSA)
- PoSA with authority rotation & staking
- Bootstraps with curated set; decentralization roadmap
- Substrate Session/Aura integration
12) Governance
- Controls decay parameters, isotope blends, fees, Ψ pool configs, and rulebook lifecycle
- Parameter changes emit auditable events
- Transition path: Root/Sudo → councils → collectives
13) Compliance & Auditability
- Event-rich logs (DecayApplied, WrapMinted, Attested, PremiumPaid)
- CLI + browser tools export records in JSONL → CSV → ISO 20022 XML
- SHR ensures rulebook edition reproducibility
14) Tokenomics (Post-Burn)
- Max Supply: 21B (fixed, post-burn)
- Circulating Supply: To be set at mainnet genesis (transparent chainspec)
- Savings Vaults: Principal protected from decay
- Wrapping: Neutral to total supply; represents vault-shielded coins
- Emissions/Reductions: Driven by traditional burns, Monetary Half-Life, Part-Life, Isotope models, and fee burns
15) Roadmap & Delivery Status
Delivered:
- Ω pallet (decay engine, savings, fees)
- SHR Router + governance stubs
- PoSA authority scaffolds
- Half-Life CLI tool
- Λ wraps MVP + vault shielding
- Θ rulebooks & attestations
- Ψ pools MVP

Next:
- Security audits, formal verification of decay math
- Expanded explorer integration
- ISO 20022 schema exports
- Industrial pilot integrations (Θ-III/IV)
16) Risk Factors
- Governance misconfigurations (decay, fees, burn splits)
- PoSA centralization risk at early phases
- Smart contract / pallet bugs
- Regulatory risks remain jurisdiction-dependent
17) Listing Information (for CMC)
Project Name: Byzantium-Coin
Ticker: BZFC
Type: Layer-1 (Substrate FRAME, custom pallets)
Max Supply: 21,000,000,000 BZFC
Decimals: 17
Consensus: PoSA (Aura/Session)
Official Website: https://byzantinefuturecapital.com
Docs: This White Paper v3 + repo docs
Email: info@byzantinefuturecapital.com
Circulating Supply: To be disclosed at mainnet genesis
Appendices
A — Pre-Market Burn Parameters
- Genesis Supply: 1T
- Target Supply: 21B
- Duration: ~60 days or governance-defined (TBA)
- Half-life: ~10.8 days

B — Isotope Decay Models
- Example Blend: 30% T½ = 1 year, 70% T½ = 10 years
- Effective per-epoch decay:
  r_eff = 0.3 * r1 + 0.7 * r2

C — Namespace Codes
- Ω = 937 (Monetary Policy, Decay, Savings)
- Θ = 920 (Compliance Rulebooks)
- Ψ = 936 (Insurance Pools)
- Λ = 923 (Wrapping & Vault Shielding)
