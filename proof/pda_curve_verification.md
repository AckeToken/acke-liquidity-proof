# PDA Ownership Verification (No Private Key)

This verifies that the owner of the Raydium CLMM liquidity position is a **Program-Derived Address (PDA)**, meaning **no private key exists** and the liquidity **cannot be withdrawn**.

---

## Position Owner Address
GJyxRzHHRS7aGZP8kz8PZMDCHVn7CyDrEVfHRZDt5t5J

## Curve Check (ed25519)
ed25519_is_on_curve("GJyxRzHHRS7aGZP8kz8PZMDCHVn7CyDrEVfHRZDt5t5J") == FALSE

### Meaning:
- If an address is **on-curve**, it corresponds to a valid private key → a human or multisig could sign.
- If an address is **off-curve**, it is a **PDA** → **no private key exists**.

This value is **off-curve**, which means:

| Property | Result |
|---------|--------|
| Can anyone sign for this address? | **No** |
| Can the CLMM position be transferred or withdrawn? | **No** |
| Can a multisig take control? | **No** |
| Can the original deployer regain access? | **No** |

---

### Conclusion
The liquidity is **mathematically non-recoverable** and therefore **permanently locked**.
