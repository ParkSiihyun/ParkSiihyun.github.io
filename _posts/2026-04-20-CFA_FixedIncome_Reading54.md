---
title: "Yield and Yield Spread Measures for Floating-Rate Instruments (Reading 54)"
date: 2026-04-20
categories: cfa
tags: [Fixed Income, CFA Level I, Floating Rate Notes, Money Markets, Discount Yield, Reading 54]
excerpt: "Sihyun CFA Notes - Yield and Yield Spread Measures for Floating-Rate Instruments (Reading 54)"
---

## Quick Take

- 중심 주제: **Yield and Yield Spread Measures for Floating-Rate Instruments**
- 먼저 잡을 축: Floating-Rate Notes, FRN Price and Margin, FRN Valuation Example
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Floating-Rate Notes
2. FRN Price and Margin
3. FRN Valuation Example
4. Money Market Yield Measures
5. Bond Equivalent Yield

## Main Notes

## 1. Floating-Rate Notes

**Floating-rate note (FRN)** = bond whose coupon rate resets periodically based on a market reference rate.

$$\text{Coupon Rate} = \text{MRR} + \text{Quoted Margin}$$

| Term | Meaning |
|------|------|
| **MRR** | Market reference rate, such as SOFR |
| **Quoted Margin (QM)** | Fixed spread actually paid in the coupon |
| **Required Margin / Discount Margin (DM)** | Spread required by investors to price the FRN at par |

FRN values tend to be more stable than fixed-rate bond values because coupons reset as market rates change.

---

## 2. FRN Price and Margin

| Relationship | FRN price |
|------|------|
| DM = QM | Par |
| DM > QM | Discount |
| DM < QM | Premium |

If investors require more spread than the bond pays, the price must fall below par.

---

## 3. FRN Valuation Example

Assume:

| Input | Value |
|------|------|
| Face value | $100,000 |
| Coupon reset | Semiannual |
| MRR | 3.0% |
| Quoted margin | 1.2% |
| Discount margin | 1.5% |

Annualized coupon rate:

$$3.0\% + 1.2\% = 4.2\%$$

Semiannual coupon:

$$4.2\% / 2 = 2.1\%$$

Required semiannual rate:

$$\frac{3.0\% + 1.5\%}{2} = 2.25\%$$

Because DM is greater than QM, the FRN trades below par.

---

## 4. Money Market Yield Measures

Money market instruments are quoted using different conventions, so conversion is essential.

### Add-On Yield

$$HPY = \text{Add-on Yield} \times \frac{\text{Days to Maturity}}{365}$$

Bank CDs, repos, and many market reference rates are commonly quoted as add-on yields.

### Discount Yield

$$\text{Discount Yield} = \frac{\text{Discount}}{\text{Face Value}} \times \frac{360}{\text{Days to Maturity}}$$

Treasury bills and commercial paper are often quoted on a discount yield basis.

---

## 5. Bond Equivalent Yield

**Bond equivalent yield (BEY)** converts a money market quote into an add-on yield using a 365-day year.

This makes the instrument more comparable with bond yields.

| Measure | Uses |
|------|------|
| HPY | Actual holding-period return |
| Discount yield | Discount from face value, 360-day convention |
| Add-on yield | Interest over beginning price |
| BEY | Add-on-style annualized yield, 365-day basis |
| EAY | Fully compounded annual yield |

### Exam Points

- FRNs trade near par when the quoted margin equals the required margin.
- Discount yield uses face value in the denominator.
- Add-on yield uses beginning price or investment amount.
- EAY is the cleanest annual comparison when compounding matters.
