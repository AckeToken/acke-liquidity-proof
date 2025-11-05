# Vault Authority Chain (Program-Owned, Not Wallet-Owned)

These are the CLMM vault accounts that hold the actual assets. They are **program-owned** and bound to the CLMM state, not to any user wallet. Funds move only via swaps; no signer can withdraw them.

---

## Vault Accounts
ACKE vault: rySKvP1HEdwatCRdchAwGYwAoR9mRt3LhPbFAiorsap
WSOL vault: 7eLA8C4LFHNGD8Rh9awGuSbGBu3zuhWeZtrQwviicujN

## Position Owner (PDA)
GJyxRzHHRS7aGZP8kz8PZMDCHVn7CyDrEVfHRZDt5t5J

## PDA Source Program
RoCKeTyq1Wf8Co6e2x1RQCC6uxRkZrQ3mDJUEoQryhh

---

## Why this means “Locked”
- Vault owners trace to the CLMM program/PDA chain (not a wallet or multisig).
- PDA is **off-curve** (no private key, no signer).
- The controlling program exposes **no withdraw/reclaim instruction**.
- Therefore, **no entity can drain or redirect the vaults**.

---

### Summary
**Program-owned vaults + off-curve PDA + no withdraw path = liquidity permanently locked by architecture.**

