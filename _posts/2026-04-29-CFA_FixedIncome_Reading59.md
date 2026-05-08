---
title: "Curve-Based and Empirical Fixed Income Risk Measures (Reading 59)"
date: 2026-04-29
categories: cfa
tags: [Fixed Income, CFA Level I, Effective Duration, Key Rate Duration, Embedded Options, Reading 59]
excerpt: "Sihyun CFA Notes - Curve-Based and Empirical Fixed Income Risk Measures (Reading 59)"
---

## Quick Take

- 중심 주제: **Curve-Based and Empirical Fixed Income Risk Measures**
- 먼저 잡을 축: Why Yield-Based Measures Are Limited, Effective Duration, Effective Convexity
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Why Yield-Based Measures Are Limited
2. Effective Duration
3. Effective Convexity
4. Callable and Putable Bonds
5. Key Rate Duration
6. Empirical Duration

## Main Notes

## 1. Why Yield-Based Measures Are Limited

Yield-based duration works best for option-free bonds with predictable cash flows.

Bonds with embedded options are different because future cash flows and redemption dates can change as rates change.

Examples:

- callable bonds
- putable bonds
- mortgage-backed securities

For these bonds, a single YTM is not always the cleanest measure of interest rate risk.

---

## 2. Effective Duration

**Effective duration** measures sensitivity to changes in the benchmark yield curve.

$$EffDur = \frac{V_- - V_+}{2V_0 \Delta Curve}$$

Where:

| Term | Meaning |
|------|------|
| $$V_-$$ | Value if benchmark curve decreases |
| $$V_+$$ | Value if benchmark curve increases |
| $$V_0$$ | Initial value |
| $$\Delta Curve$$ | Change in benchmark curve |

Effective duration reflects the effect of changing rates on both discount rates and expected cash flows.

---

## 3. Effective Convexity

$$EffConvexity = \frac{V_- + V_+ - 2V_0}{(\Delta Curve)^2 V_0}$$

Effective convexity is especially important for callable bonds and mortgage-backed securities, where cash flows change as rates change.

---

## 4. Callable and Putable Bonds

Callable bond:

$$\text{Callable Bond Value} = \text{Straight Bond Value} - \text{Call Option Value}$$

Putable bond:

$$\text{Putable Bond Value} = \text{Straight Bond Value} + \text{Put Option Value}$$

| Bond type | Investor position |
|------|------|
| Callable bond | Short call option |
| Putable bond | Long put option |

Callable bonds can exhibit negative convexity when rates fall because the call option becomes more valuable to the issuer.

---

## 5. Key Rate Duration

**Key rate duration** measures price sensitivity to a change in one maturity point on the yield curve while other maturities are held constant.

This is useful for nonparallel yield curve shifts.

| Measure | Captures |
|------|------|
| Effective duration | Parallel shift in benchmark curve |
| Key rate duration | Specific maturity point movement |

Portfolio managers use key rate duration to understand exposure to steepening, flattening, and curvature changes.

---

## 6. Empirical Duration

**Empirical duration** estimates sensitivity from observed market price changes rather than a valuation model.

It can be useful when:

- model assumptions are unreliable
- cash flows are uncertain
- market behavior differs from theoretical pricing

### Exam Points

- Use effective duration for bonds with embedded options.
- Callable bonds may have negative convexity at low yields.
- Key rate duration is designed for nonparallel curve shifts.
- Yield-based duration assumes a single yield change; curve-based measures are more flexible.
