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
0 ---------------- infinity

Liquidity distributed everywhere



V3:


2500 --------3500

Liquidity concentrated near active price



LPs can select:

- lower price tick
- upper price tick


to create a liquidity position.


This improves capital efficiency.

:contentReference[oaicite:1]{index=1}


---

# 4. Tick System


Uniswap V3 divides price space into discrete ticks.


Each tick represents a small price interval.


LP positions are defined by:


lower tick

+

upper tick


When price crosses ticks:

- liquidity enters
- liquidity leaves


The pool updates active liquidity.


:contentReference[oaicite:2]{index=2}



---

# 5. Trade-off


Concentrated liquidity creates higher efficiency.

However:


Before V3:

LP:

Deposit assets

↓

Earn fees automatically



After V3:


LP:

Predict price range

↓

Manage position

↓

Adjust liquidity



Therefore:

V3 transforms LP from passive liquidity provider into active market maker.


---

# 6. User Flow


Trader:


Token A

↓

Uniswap Pool

↓

Token B



LP:


Token Deposit

↓

Choose Price Range

↓

Provide Liquidity

↓

Earn Trading Fees
