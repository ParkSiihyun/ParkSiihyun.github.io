---
title: "CFA Fixed Income Reading 55 - Term Structure of Interest Rates: Spot, Par, and Forward Curves"
date: 2026-05-04
categories: cfa
tags: [Fixed Income, CFA Level I, Term Structure, Spot Rates, Forward Rates]
---

## 1. Spot Rates

**Spot rate** = discount rate for a single payment to be received at a specific future date.

Spot rates are also called:

- zero-coupon rates
- zero rates

For a zero-coupon bond:

$$P_0 = \frac{FV}{(1 + S_N)^N}$$

Where $$S_N$$ is the N-period spot rate.

---

## 2. No-Arbitrage Valuation

A coupon bond can be valued by discounting each cash flow at the spot rate for that cash flow's maturity.

$$P_0 = \frac{C}{1 + S_1} + \frac{C}{(1 + S_2)^2} + \cdots + \frac{C + FV}{(1 + S_N)^N}$$

This is a no-arbitrage price because each cash flow is treated like a separate zero-coupon bond.

---

## 3. Par Yield

**Par yield** = coupon rate that makes a bond's price equal to par.

For a par bond:

$$P_0 = 100$$

The par curve is built from coupon rates that price bonds at par for each maturity.

| Curve | Based on |
|------|------|
| **Spot curve** | Zero-coupon rates |
| **Par curve** | Coupon rates for par bonds |
| **Yield curve** | YTMs of coupon bonds |

---

## 4. Forward Rates

**Forward rate** = borrowing or lending rate for a future period implied by current spot rates.

For annual rates:

$$ (1 + S_2)^2 = (1 + S_1)(1 + f_{1,1}) $$

More generally:

$$ (1 + S_N)^N = (1 + S_1)(1 + f_{1,1})(1 + f_{2,1})\cdots(1 + f_{N-1,1}) $$

Forward rates are implied rates, not guaranteed future spot rates.

---

## 5. Spot, Par, and Forward Curves

| Curve | Interpretation |
|------|------|
| **Spot curve** | Discount rates for zero-coupon cash flows |
| **Par curve** | Coupon rates that make bonds trade at par |
| **Forward curve** | Future short rates implied by current spot rates |

If the spot curve is upward sloping, longer-maturity spot rates are higher than shorter-maturity spot rates.

### Exam Points

- Use spot rates to value individual bond cash flows.
- Par yields are coupon rates, not discount rates for every cash flow.
- Forward rates are derived from spot rates through no-arbitrage logic.
- Spot curves are usually the cleanest curve for valuation.
