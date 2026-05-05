---
title: "CFA Fixed Income Reading 53 - Yield and Yield Spread Measures for Fixed-Rate Bonds"
date: 2026-05-04
categories: cfa
tags: [Fixed Income, CFA Level I, Yield Measures, Yield Spreads, OAS]
---

## 1. Periodicity and Effective Annual Yield

**Periodicity** = number of coupon payments per year.

The greater the periodicity, the more compounding periods, and the greater the effective annual yield for the same stated annual yield.

$$EAY = \left(1 + \frac{\text{Stated Annual Yield}}{m}\right)^m - 1$$

| Term | Meaning |
|------|------|
| $$m$$ | Periodicity |
| EAY | Effective annual yield |

Example: stated annual YTM of 10%.

| Periodicity | EAY |
|------|------|
| Semiannual | $$(1.05)^2 - 1 = 10.25\%$$ |
| Quarterly | $$(1.025)^4 - 1 = 10.38\%$$ |

---

## 2. Yield Basis Conversion

Yields must be converted to the same periodicity before comparison.

Example: A bond quoted at 4% on a semiannual bond basis.

$$EAY = (1 + 0.04 / 2)^2 - 1 = 4.04\%$$

The equivalent quarterly bond basis yield solves:

$$\left(1 + \frac{YTM_q}{4}\right)^4 = 1.0404$$

Quarterly bond basis YTM is approximately 3.98%.

---

## 3. Street Convention and True Yield

| Yield measure | Description |
|------|------|
| **Street convention yield** | Assumes standard coupon dates and standard settlement conventions |
| **True yield** | Uses actual coupon payment dates |

True yield can differ slightly from street convention yield when actual coupon dates are irregular.

---

## 4. Current Yield and Simple Yield

$$\text{Current Yield} = \frac{\text{Annual Cash Coupon}}{\text{Bond Price}}$$

Current yield ignores capital gains/losses and reinvestment income.

**Simple yield** adjusts current yield by amortizing a premium or discount evenly over the remaining life of the bond.

---

## 5. Callable Bonds

For callable bonds, the investor's realized yield depends on whether and when the issuer calls the bond.

| Measure | Meaning |
|------|------|
| **Yield to Call** | Yield assuming the bond is called on a specific call date |
| **Yield to Maturity** | Yield assuming no call and repayment at maturity |
| **Yield to Worst** | Lowest yield among all call dates and maturity |

Investors focus on yield to worst because it represents the least favorable outcome among allowed redemption dates.

---

## 6. Option-Adjusted Yield

A callable bond can be viewed as:

$$\text{Callable Bond Value} = \text{Straight Bond Value} - \text{Call Option Value}$$

The **option-adjusted yield** is the yield of an equivalent option-free bond after accounting for the embedded call option.

---

## 7. Yield Spreads

Yield spreads help separate changes in interest rates from issuer-specific or bond-specific risk.

| Spread | Description |
|------|------|
| **G-spread** | Spread over a government bond yield |
| **I-spread** | Spread over an interbank market reference rate |
| **Z-spread** | Constant spread added to each spot rate that prices the bond |
| **OAS** | Z-spread after removing the value of embedded options |

For callable bonds:

$$OAS = Z\text{-spread} - \text{Option Yield Component}$$

### Exam Points

- Compare yields only after putting them on the same compounding basis.
- Yield to worst matters for callable bonds.
- Z-spread uses the full spot curve; YTM is a single weighted-average yield.
- OAS is cleaner for bonds with embedded options.

