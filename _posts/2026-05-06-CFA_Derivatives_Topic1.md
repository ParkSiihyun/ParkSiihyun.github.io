---
title: "CFA Derivatives Topic 1 - Derivative Instruments and Market Features"
date: 2026-05-06
categories: cfa
tags: [Derivatives, CFA Level I, Forward Commitments, Options, CDS]
---

## 1. What Is a Derivative?

**Derivative** = a financial contract whose value depends on the value of an underlying asset, rate, index, or event.

Common underlying exposures:

| Underlying | Examples |
|------|------|
| Equity | individual stock, equity index |
| Fixed income | bond, interest rate |
| Currency | FX rate |
| Commodity | oil, gold, agricultural products |
| Credit | credit event, default risk |

---

## 2. Contract Types

Derivatives can be grouped by payoff structure.

| Type | Core idea | Examples |
|------|------|------|
| **Forward commitment** | Both parties are obligated to transact in the future | Forward, futures, swap |
| **Contingent claim** | Payoff depends on an event or exercise decision | Option, credit derivative |

<figure class="sh-diagram">
  <img src="/images/cfa/derivatives-topic1-contract-map.svg" alt="Map of derivative contract types: forward commitments and contingent claims">
  <figcaption>Forward commitment는 양쪽 모두 미래 거래 의무가 있고, contingent claim은 특정 조건이나 선택권에 따라 payoff가 달라진다.</figcaption>
</figure>

---

## 3. Forwards, Futures, Options, Swaps

| Instrument | Description |
|------|------|
| **Forward** | Private OTC contract to buy or sell an asset later at a price set today |
| **Futures** | Standardized exchange-traded forward-style contract with daily settlement |
| **Option** | Right, but not obligation, to buy or sell an asset |
| **Swap** | Agreement to exchange cash flows over time |
| **Credit Default Swap (CDS)** | Contract that transfers credit risk of a reference entity |

---

## 4. CDS Structure

**Credit default swap (CDS)** transfers credit risk from one party to another.

| Party | Position |
|------|------|
| **Protection buyer** | Pays CDS premium; receives payment if credit event occurs |
| **Protection seller** | Receives premium; pays if credit event occurs |
| **Reference entity** | Borrower or issuer whose credit risk is referenced |

The CDS buyer is economically buying insurance against default.

---

## 5. Exchange vs OTC Market

| Feature | Exchange-traded | OTC |
|------|------|------|
| Contract terms | Standardized | Customized |
| Counterparty risk | Reduced by clearinghouse | Bilateral counterparty exposure |
| Liquidity | Often higher | Depends on contract |
| Flexibility | Lower | Higher |

Clearinghouses reduce counterparty risk through margin, daily settlement, and netting.

---

## 6. Benefits of Derivatives

Derivatives can improve market function when used properly.

| Benefit | Meaning |
|------|------|
| Risk transfer | Shift risk to the party willing to hold it |
| Risk management | Hedge unwanted exposures |
| Information discovery | Prices can reveal expected future spot prices |
| Operational efficiency | Lower transaction cost than trading underlying assets directly |
| Market efficiency | Arbitrage helps align prices |

---

## 7. Risks of Derivatives

| Risk | Description |
|------|------|
| Counterparty risk | Other party may fail to perform |
| Basis risk | Hedge instrument does not perfectly track exposure |
| Liquidity risk | Position may be hard to exit |
| Operational risk | Valuation, documentation, or collateral process can fail |
| Systemic risk | Network of exposures can amplify stress |

### Basis Risk Example

Short hedge:

$$\text{Position} = \text{Long Spot} + \text{Short Futures}$$

The hedge is imperfect when spot price and futures price do not move together.

---

## 8. Arbitrage and Law of One Price

**Arbitrage** = earning riskless profit by buying low and selling high.

The **law of one price** says identical payoffs should have the same price.

No-arbitrage logic is the foundation for forward, futures, swap, and option pricing.

### Exam Points

- Forwards, futures, and swaps are forward commitments.
- Options and credit derivatives are contingent claims.
- Exchange trading reduces counterparty risk through standardization and clearing.
- Derivatives help transfer risk but introduce counterparty, basis, liquidity, and systemic risk.
- No-arbitrage pricing relies on equivalent payoffs having equivalent prices.

