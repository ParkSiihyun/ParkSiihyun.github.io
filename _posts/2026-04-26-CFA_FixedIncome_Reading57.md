---
title: "Yield-Based Bond Duration Measures and Properties (Reading 57)"
date: 2026-04-26
categories: cfa
tags: [Fixed Income, CFA Level I, Duration, Modified Duration, PVBP, Reading 57]
excerpt: "Sihyun CFA Notes - Yield-Based Bond Duration Measures and Properties (Reading 57)"
---

## Quick Take

- 중심 주제: **Yield-Based Bond Duration Measures and Properties**
- 먼저 잡을 축: Modified Duration, Approximate Modified Duration, Money Duration and Dollar Duration
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Modified Duration
2. Approximate Modified Duration
3. Money Duration and Dollar Duration
4. Price Value of a Basis Point
5. Duration Properties

## Main Notes

## 1. Modified Duration

**Modified duration** estimates the percentage price change for a 1% change in yield.

$$ModDur = \frac{MacDur}{1 + y}$$

For semiannual coupon bonds, use the periodic yield and then adjust duration to an annual basis.

Approximation:

$$\%\Delta P \approx -ModDur \times \Delta YTM$$

Example: If modified duration is 3.5 and YTM rises by 0.50%:

$$\%\Delta P \approx -3.5 \times 0.005 = -1.75\%$$

---

## 2. Approximate Modified Duration

Approximate modified duration uses bond prices after small yield changes.

$$ApproxModDur = \frac{V_- - V_+}{2V_0 \Delta YTM}$$

Where:

| Term | Meaning |
|------|------|
| $$V_-$$ | Bond value when yield decreases |
| $$V_+$$ | Bond value when yield increases |
| $$V_0$$ | Initial bond value |

---

## 3. Money Duration and Dollar Duration

**Money duration** converts percentage price sensitivity into currency sensitivity.

$$\text{Money Duration} = ModDur \times \text{Full Price}$$

For a position:

$$\text{Dollar Duration} = ModDur \times \text{Market Value}$$

This tells us the approximate dollar change in value for a 1% yield change.

---

## 4. Price Value of a Basis Point

**PVBP** = price change for a 1 basis point change in yield.

$$PVBP = \frac{V_- - V_+}{2}$$

Where $$V_-$$ and $$V_+$$ are calculated using yields 1 bp lower and 1 bp higher.

PVBP is usually expressed per $100 of par value or for the full position.

---

## 5. Duration Properties

| Bond feature | Effect on duration |
|------|------|
| Longer maturity | Higher duration |
| Lower coupon | Higher duration |
| Lower YTM | Higher duration |
| More dispersed cash flows | Higher duration |

Zero-coupon bonds have duration equal to maturity because all cash flow is received at maturity.

### Exam Points

- Duration is a linear approximation.
- Modified duration estimates percentage price change.
- PVBP estimates price change for a 1 bp yield move.
- Lower-coupon and longer-maturity bonds usually carry more interest rate risk.
