---
title: "CFA Derivatives Topic 2 - Pricing and Valuation of Forward Contracts"
date: 2026-05-06
categories: cfa
tags: [Derivatives, CFA Level I, Forwards, Cost of Carry, FX Forward]
---

## 1. Forward Contract Basics

**Forward contract** = private agreement to buy or sell an underlying asset at a future date for a price agreed today.

| Term | Meaning |
|------|------|
| **Contract date** | Date the forward is initiated |
| **Expiration date** | Date the transaction occurs |
| **Forward price** | Price agreed today for future delivery |
| **Underlying asset** | Asset, currency, or rate referenced by the contract |

At initiation, a standard forward usually has:

$$V_0(T) = 0$$

The forward price is set so neither side has value at contract initiation.

---

## 2. Long and Short Forward Payoff

At expiration:

$$\text{Long Forward Payoff} = S_T - F_{0,T}$$

$$\text{Short Forward Payoff} = F_{0,T} - S_T$$

| Position | Benefits when |
|------|------|
| Long forward | Spot price rises above forward price |
| Short forward | Spot price falls below forward price |

<figure class="sh-diagram">
  <img src="/images/cfa/derivatives-topic2-forward-payoff.svg" alt="Forward contract payoff diagram for long and short positions">
  <figcaption>Forward payoff는 만기 spot price와 계약 시 정한 forward price의 차이로 결정된다.</figcaption>
</figure>

---

## 3. Pricing vs Valuation

| Concept | Meaning |
|------|------|
| **Pricing** | Determining the no-arbitrage forward price at contract initiation |
| **Valuation** | Determining the value of an existing forward contract after initiation |

At initiation, the contract value is zero. After initiation, value can become positive or negative as spot price, interest rates, or carry benefits change.

---

## 4. Cost of Carry Model

Forward pricing uses the cost of carrying the underlying asset until expiration.

Basic no-income case:

$$F_{0,T} = S_0(1 + r)^T$$

Continuous compounding version:

$$F_{0,T} = S_0e^{rT}$$

With costs and benefits:

$$F_{0,T} = [S_0 + PV(\text{Costs}) - PV(\text{Benefits})](1 + r)^T$$

Continuous version:

$$F_{0,T} = S_0e^{(r + c - b)T}$$

Where:

| Term | Meaning |
|------|------|
| $$r$$ | risk-free rate |
| $$c$$ | cost of carry, such as storage |
| $$b$$ | benefit, such as dividend, interest, or convenience yield |

---

## 5. Forward Value After Initiation

For a long forward with original forward price $$F_{0,T}$$:

$$V_t(T) = S_t - \frac{F_{0,T}}{(1+r)^{T-t}}$$

More generally, with carry costs and benefits:

$$V_t(T) = S_t + PV_t(\text{Costs}) - PV_t(\text{Benefits}) - PV_t(F_{0,T})$$

The short forward has the opposite value.

---

## 6. Currency Forwards

For FX forwards, the cost of carry is based on interest rate parity.

If the quote is price currency per one unit of base currency:

$$F_{p/b} = S_{p/b}\frac{(1+r_p)^T}{(1+r_b)^T}$$

Where:

| Term | Meaning |
|------|------|
| $$p$$ | price currency |
| $$b$$ | base currency |
| $$r_p$$ | interest rate of price currency |
| $$r_b$$ | interest rate of base currency |

If the base currency interest rate is higher, the forward price in price-currency terms tends to be lower, all else equal.

---

## 7. Interest Rate Forwards and FRAs

**Forward Rate Agreement (FRA)** = contract on a future borrowing or lending rate.

The forward rate is implied by spot rates:

$$ (1 + S_2)^2 = (1 + S_1)(1 + f_{1,1}) $$

FRA payoff:

$$\text{FRA Payoff} = \text{Notional} \times (S - F) \times \frac{\text{Days}}{360}$$

Settlement is discounted because payment is usually made at the beginning of the loan period.

### Exam Points

- Forward contract value is usually zero at initiation.
- Long forward payoff is $$S_T - F_{0,T}$$.
- Forward price is a no-arbitrage price; forward value changes after initiation.
- Carry costs increase forward price; benefits decrease forward price.
- FX forwards follow interest rate parity.
- FRAs hedge future borrowing or lending rate risk.

