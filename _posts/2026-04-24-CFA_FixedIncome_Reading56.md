---
title: "CFA Fixed Income Reading 56 - Interest Rate Risk and Return"
date: 2026-04-24
categories: cfa
tags: [Fixed Income, CFA Level I, Interest Rate Risk, Holding Period Return, Macaulay Duration]
---

## 1. Sources of Bond Return

A bond investor's return comes from three sources:

1. Coupon and principal payments
2. Interest earned by reinvesting coupon payments
3. Capital gain or loss if the bond is sold before maturity

The importance of each source depends on the investor's holding period.

---

## 2. Holding Period Return

**Holding period return (HPR)** measures the return over the investor's actual investment horizon.

$$HPR = \left(\frac{\text{Ending Value} + \text{Coupon Income}}{\text{Beginning Price}}\right)^{1/n} - 1$$

Where $$n$$ is the number of years in the holding period.

---

## 3. Carrying Value

**Carrying value** = bond price along its constant-yield price trajectory.

Capital gain or loss is measured relative to carrying value, not simply relative to purchase price.

$$\text{Capital Gain/Loss} = \text{Sale Price} - \text{Carrying Value}$$

If the bond is sold at the same YTM as its purchase YTM, there is no capital gain or loss relative to the carrying value.

---

## 4. Price Risk and Reinvestment Risk

| Investment horizon | Main risk |
|------|------|
| Short horizon | Price risk dominates |
| Long horizon | Reinvestment risk dominates |
| Horizon near Macaulay duration | Price and reinvestment effects offset more closely |

For an investor holding to maturity, price fluctuations before maturity are less important, but reinvestment risk remains.

---

## 5. Change in YTM

When yields rise:

- bond price falls
- reinvestment income rises

When yields fall:

- bond price rises
- reinvestment income falls

This is the core tradeoff between price risk and reinvestment risk.

---

## 6. Macaulay Duration

**Macaulay duration** = weighted average time to receive the bond's promised cash flows.

Weights are based on each cash flow's present value as a proportion of the bond's full price.

$$MacDur = \sum_{t=1}^{N} t \times w_t$$

Where:

$$w_t = \frac{PV(CF_t)}{\text{Full Price}}$$

### Duration Gap

$$\text{Duration Gap} = \text{Macaulay Duration} - \text{Investment Horizon}$$

| Gap | Main exposure |
|------|------|
| Positive duration gap | Price risk dominates |
| Negative duration gap | Reinvestment risk dominates |

### Exam Points

- HPR can differ from YTM when the bond is sold before maturity or coupons are reinvested at different rates.
- Carrying value is the correct benchmark for measuring capital gain/loss.
- Macaulay duration helps identify the horizon where price risk and reinvestment risk offset.

