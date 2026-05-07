---
title: "CFA Derivatives Topic 3 - Pricing and Valuation of Futures Contracts"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Futures, Margin, Marking to Market]
---

## 1. Futures Contract Basics

**Futures contract** = standardized exchange-traded contract to buy or sell an underlying asset at a future date.

Futures and forwards share the same economic idea, but futures are more standardized and are settled daily.

| Feature | Forward | Futures |
|------|------|------|
| Market | OTC | Exchange |
| Terms | Customized | Standardized |
| Counterparty risk | Higher | Lower due to clearinghouse |
| Settlement | Usually at expiration | Daily mark to market |
| Margin | Usually not standardized | Required |

---

## 2. Clearinghouse and Novation

The clearinghouse becomes the counterparty to both sides of the trade.

This process is called **novation**.

| Participant | Economic exposure |
|------|------|
| Long futures | Gains when futures price increases |
| Short futures | Gains when futures price decreases |
| Clearinghouse | Guarantees performance through margin and daily settlement |

---

## 3. Daily Settlement and Margin

Futures are marked to market daily.

| Term | Meaning |
|------|------|
| **Initial margin** | Deposit required to open a futures position |
| **Maintenance margin** | Minimum required margin account balance |
| **Variation margin** | Additional funds required when balance falls below maintenance margin |
| **Settlement price** | Price used for daily gain/loss calculation |

Daily gain/loss for one contract:

$$\text{Daily Settlement} = \text{Contract Size} \times \Delta \text{Futures Price}$$

<figure class="sh-diagram">
  <img src="/images/cfa/derivatives-topic3-futures-margin.svg" alt="Futures daily settlement and margin account mechanics">
  <figcaption>Futures는 매일 mark to market되므로 손익이 margin account에 바로 반영되고, 잔고가 maintenance margin 아래로 내려가면 variation margin이 필요하다.</figcaption>
</figure>

---

## 4. Futures Payoff

At expiration:

$$\text{Long Futures Payoff} = S_T - FP$$

$$\text{Short Futures Payoff} = FP - S_T$$

Where $$FP$$ is the futures price.

---

## 5. Interest Rate Futures

Interest rate futures are commonly quoted using:

$$\text{Futures Price} = 100 - \text{Annualized MRR in percent}$$

If the implied market reference rate increases, the futures price decreases.

### Basis Point Value

$$BPV = \text{Notional Principal} \times 0.01\% \times \frac{\text{Days}}{360}$$

BPV estimates the dollar value of a one basis point move in the referenced rate.

---

## 6. Futures vs Forwards

Futures and forwards can have different prices because of daily settlement.

| Relationship | Intuition |
|------|------|
| Positive correlation between rates and futures price | Futures price may exceed forward price |
| Negative correlation between rates and futures price | Futures price may be below forward price |

The difference comes from reinvestment effects created by daily settlement.

### Exam Points

- Futures contracts are standardized and exchange traded.
- Marking to market resets gains/losses every day.
- Clearinghouses reduce counterparty risk.
- Interest rate futures price moves inversely with the implied rate.
- Futures and forwards can differ because futures cash flows occur daily.

