---
title: "CFA Fixed Income Reading 52 - Fixed Income Bond Valuation: Prices and Yields"
date: 2026-05-04
categories: cfa
tags: [Fixed Income, CFA Level I, Bond Valuation, YTM, Accrued Interest]
---

## 1. Bond Value

The value of a bond is the present value of all promised cash flows.

$$V_0 = \sum_{t=1}^{N} \frac{CF_t}{(1 + y)^t}$$

Where:

| Term | Meaning |
|------|------|
| $$CF_t$$ | Coupon or principal cash flow at time $$t$$ |
| $$y$$ | Required yield per period |
| $$N$$ | Number of remaining periods |

The required yield can be viewed as a risk-free rate plus a risk premium.

---

## 2. Price, Coupon, and Yield

| Relationship | Bond trades at |
|------|------|
| Coupon rate = YTM | Par |
| Coupon rate > YTM | Premium |
| Coupon rate < YTM | Discount |

Example: A 5-year, 10% annual coupon bond with par value of $100.

| YTM | Price |
|------|------|
| 10% | $100.00 |
| 12% | $92.79 |
| 8% | $107.99 |

---

## 3. Semiannual Coupon Bonds

For semiannual coupon bonds:

- Divide annual coupon by 2.
- Divide annual YTM by 2.
- Multiply years to maturity by 2.

Example: 10% coupon, semiannual pay, par $100, annual YTM 8%, 5 years to maturity.

| Input | Value |
|------|------|
| N | 10 |
| PMT | 5 |
| FV | 100 |
| I/Y | 4 |

The price is approximately $108.11.

---

## 4. Yield to Maturity

**Yield to maturity (YTM)** = the single discount rate that equates the present value of a bond's promised cash flows to its market price.

To actually earn the YTM:

1. The investor must hold the bond to maturity.
2. The issuer must make all promised payments.
3. Coupon payments must be reinvested at the YTM.

---

## 5. Accrued Interest

When a bond trades between coupon dates, the buyer compensates the seller for the coupon interest earned since the last coupon date.

$$\text{Accrued Interest} = \text{Coupon Payment} \times \frac{\text{Days Since Last Coupon}}{\text{Days in Coupon Period}}$$

| Day-count method | Description |
|------|------|
| **Actual / Actual** | Uses actual days elapsed and actual days in coupon period |
| **30 / 360** | Assumes 30-day months and 360-day years |

---

## 6. Clean and Dirty Price

| Price | Meaning |
|------|------|
| **Flat / Clean Price** | Quoted price excluding accrued interest |
| **Full / Dirty Price** | Clean price plus accrued interest |

$$\text{Full Price} = \text{Flat Price} + \text{Accrued Interest}$$

Bond markets quote clean prices to avoid mechanical price jumps from accrued interest.

---

## 7. Price Convergence

As maturity approaches, a bond's price converges toward par value if the issuer does not default.

| Bond type | Price path |
|------|------|
| Premium bond | Falls toward par |
| Discount bond | Rises toward par |
| Par bond | Remains near par |

This is called the **constant-yield price trajectory**.

---

## 8. Matrix Pricing

**Matrix pricing** estimates the required yield or price for bonds that are not actively traded.

Common approach:

1. Find comparable bonds with similar credit quality.
2. Interpolate yields by maturity.
3. Add an appropriate credit spread if necessary.
4. Discount the target bond's cash flows using the estimated yield.

### Exam Points

- Bond price and yield move in opposite directions.
- Premium bonds have coupon rates above YTM.
- Dirty price includes accrued interest; clean price does not.
- Matrix pricing is useful when the bond itself is illiquid or not recently traded.

