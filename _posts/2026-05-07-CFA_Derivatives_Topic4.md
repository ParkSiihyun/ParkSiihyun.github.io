---
title: "CFA Derivatives Topic 4 - Pricing and Valuation of Interest Rate Swaps"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Swaps, Interest Rate Swaps, FRA]
---

## 1. Swap Contract Basics

**Swap** = contract in which two parties exchange cash flows over time.

The most important Level I example is the plain vanilla interest rate swap.

| Swap position | Meaning |
|------|------|
| **Long swap** | Receive floating, pay fixed |
| **Short swap** | Receive fixed, pay floating |

Swaps usually trade OTC, so counterparty risk matters more than in exchange-traded futures.

---

## 2. Plain Vanilla Interest Rate Swap

In a plain vanilla interest rate swap:

- one party pays a fixed rate
- the other party pays a floating rate
- payments are based on notional principal
- only net interest is exchanged

<figure class="sh-diagram">
  <img src="/images/cfa/derivatives-topic4-swap-flow.svg" alt="Plain vanilla interest rate swap showing fixed and floating cash flows">
  <figcaption>Plain vanilla IRS는 fixed leg와 floating leg의 이자 차이만 net settlement하는 구조다.</figcaption>
</figure>

---

## 3. Swap Terminology

| Term | Meaning |
|------|------|
| **Notional principal** | Reference amount used to calculate payments |
| **Tenor** | Life of the swap |
| **Settlement dates** | Dates on which net payments occur |
| **Fixed rate** | Rate paid by fixed-rate payer |
| **Floating rate** | Market reference rate such as SOFR |

Net payment for pay fixed / receive floating:

$$\text{Net Payment} = (\text{Floating Rate} - \text{Fixed Rate}) \times \text{Notional} \times \frac{\text{Days}}{360}$$

---

## 4. Swap as a Series of FRAs

An interest rate swap can be viewed as a series of forward rate agreements.

| Period | Forward-style interpretation |
|------|------|
| First settlement | Known or near-known floating rate |
| Later settlements | Implied future floating rates |
| Full swap | Portfolio of FRAs |

This is why swap pricing relies on no-arbitrage forward rates.

---

## 5. Swap Pricing

At initiation, a fair swap has value close to zero.

The fixed rate is set so:

$$PV(\text{Fixed Payments}) = PV(\text{Floating Payments})$$

The fixed rate that makes the swap value zero is the **par swap rate**.

---

## 6. Swap Valuation After Initiation

After initiation, rates change and the swap can have positive or negative value.

For pay fixed / receive floating:

| Rate move | Effect |
|------|------|
| Floating rates rise relative to fixed rate | Swap value increases |
| Floating rates fall relative to fixed rate | Swap value decreases |

For receive fixed / pay floating, the signs are reversed.

### Exam Points

- A swap is economically a series of forward contracts.
- Long swap = receive floating, pay fixed.
- Net settlement uses rate difference times notional times day-count fraction.
- Fair swap fixed rate is the rate that makes initial value zero.
- Swap value changes after initiation as forward rates and discount rates change.

