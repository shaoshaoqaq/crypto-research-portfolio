# Uniswap V3 Mechanism Analysis


# 1. Background Problem


Before Uniswap:

Most exchanges used order-book models.


Order books require:

- buyers and sellers
- market makers
- high transaction efficiency


However, blockchain environments have:

- slower settlement
- fragmented liquidity
- permission requirements


AMM solves this by allowing users to trade against liquidity pools.



---

# 2. AMM Model


Uniswap V2 uses constant product AMM:


x * y = k


The pool automatically determines prices according to token reserves.



Advantages:


- No order matching
- Permissionless trading
- Anyone can provide liquidity



Problem:


Liquidity is distributed across the entire price range:

0 → infinity


Most liquidity is rarely used.



---

# 3. Concentrated Liquidity


Uniswap V3 changes the liquidity model.


Instead of providing liquidity across all prices:


V2:

