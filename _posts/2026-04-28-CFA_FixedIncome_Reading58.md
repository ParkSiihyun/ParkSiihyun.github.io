---
title: "CFA Fixed Income Reading 58 - Yield-Based Bond Convexity and Portfolio Properties"
date: 2026-04-28
categories: cfa
tags: [Fixed Income, CFA Level I, Convexity, Portfolio Duration, Barbell]
---

## 1. Why Convexity Matters

Modified duration is a linear approximation, but the true bond price-yield relationship is curved.

Convexity improves the estimate of price change when yield changes are larger.

$$\%\Delta P \approx -ModDur(\Delta Y) + \frac{1}{2}Convexity(\Delta Y)^2$$

The convexity adjustment is usually positive for option-free bonds.

---

## 2. Approximate Convexity

Approximate convexity uses bond prices when yields move up and down.

$$ApproxConvexity = \frac{V_- + V_+ - 2V_0}{(\Delta Y)^2 V_0}$$

Where:

| Term | Meaning |
|------|------|
| $$V_-$$ | Value when yield decreases |
| $$V_+$$ | Value when yield increases |
| $$V_0$$ | Initial value |

---

## 3. Convexity Properties

Convexity is affected by many of the same features that affect duration.

| Feature | Effect on convexity |
|------|------|
| Longer maturity | Higher convexity |
| Lower coupon | Higher convexity |
| Lower YTM | Higher convexity |
| More dispersed cash flows | Higher convexity |

For two bonds with the same duration, the bond with more dispersed cash flows usually has higher convexity.

---

## 4. Bullet vs Barbell

| Portfolio type | Structure | Convexity |
|------|------|------|
| **Bullet** | Cash flows concentrated around one maturity | Lower |
| **Barbell** | Cash flows concentrated at short and long maturities | Higher |

A barbell portfolio can have the same duration as a bullet portfolio but higher convexity.

---

## 5. Portfolio Duration and Convexity

Portfolio duration can be calculated as the market-value weighted average of individual bond durations.

$$D_P = w_1D_1 + w_2D_2 + \cdots + w_nD_n$$

Where:

$$w_i = \frac{\text{Full Price of Bond } i}{\text{Total Portfolio Value}}$$

The same weighted-average logic can be applied to convexity.

### Limitation

This approach assumes that every bond's yield changes by the same amount, meaning a parallel shift in the yield curve.

### Exam Points

- Convexity improves duration-based price estimates.
- Positive convexity benefits investors for large rate moves.
- Barbell portfolios generally have more convexity than comparable bullet portfolios.
- Weighted-average duration assumes parallel yield curve shifts.

