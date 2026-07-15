# Aave Mechanism Analysis


# 1. Problem


Crypto lacks native credit system.

Traditional lending depends on:

- identity
- credit score
- intermediaries


Aave replaces credit evaluation with:

- collateral
- smart contracts
- liquidation


---

# 2. Liquidity Pool


Aave does not match individual lenders and borrowers.

Instead:

Supplier

↓

Liquidity Pool

↓

Borrower


---

# 3. Over Collateralized Lending


Borrowers must provide collateral higher than borrowed assets.


Example:


ETH collateral

↓

Borrow USDC



---

# 4. Interest Rate Model


Aave adjusts borrowing rates based on utilization rate.


Higher utilization:

↓

higher borrowing rate


Lower utilization:

↓

lower borrowing rate


---

# 5. Liquidation


When collateral value decreases:

Health factor decreases

↓

Liquidation triggered

↓

Liquidator repays debt

↓

Receives collateral reward


