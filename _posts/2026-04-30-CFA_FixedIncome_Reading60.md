---
title: "Credit Risk (Reading 60)"
date: 2026-04-30
categories: cfa
tags: [Fixed Income, CFA Level I, Credit Risk, Expected Loss, Credit Spread, Reading 60]
excerpt: "Sihyun CFA Notes - Credit Risk (Reading 60)"
---

## Quick Take

- 중심 주제: **Credit Risk**
- 먼저 잡을 축: Credit Risk, Illiquidity vs Insolvency, Expected Loss
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Credit Risk
2. Illiquidity vs Insolvency
3. Expected Loss
4. Expected Loss and Credit Spread
5. Credit Ratings
6. Credit Spread Risk
7. Yield Spread Components

## Main Notes

## 1. Credit Risk

**Credit risk** = risk that a borrower fails to make promised interest or principal payments.

Credit risk arises when the borrower's repayment sources are not sufficient to service debt.

| Issuer type | Repayment source |
|------|------|
| Secured corporate debt | Operating cash flow plus collateral value |
| Unsecured corporate debt | Mainly operating cash flow |
| Sovereign debt | Tax revenue, tariffs, and fiscal capacity |

---

## 2. Illiquidity vs Insolvency

| Condition | Meaning |
|------|------|
| **Illiquid** | Borrower may have assets but lacks cash at the needed time |
| **Insolvent** | Borrower's assets and cash flows are insufficient to meet obligations |

Illiquidity can sometimes be temporary; insolvency is a deeper credit problem.

---

## 3. Expected Loss

Credit risk is often measured through expected loss.

$$\text{Expected Loss} = PD \times LGD$$

Where:

| Term | Meaning |
|------|------|
| **PD** | Probability of default |
| **LGD** | Loss given default |
| **Recovery Rate** | Portion recovered if default occurs |
| **EAD** | Exposure at default |

$$LGD(\%) = 1 - \text{Recovery Rate}$$

$$LGD(\$) = EAD \times (1 - \text{Recovery Rate})$$

---

## 4. Expected Loss and Credit Spread

Annualized expected loss can be used as a rough estimate of the required annual credit spread over a risk-free benchmark.

$$\text{Expected Loss}(\%) = PD \times LGD(\%)$$

Example:

| Input | Value |
|------|------|
| Probability of default | 3% |
| Recovery rate | 75% |
| LGD | 25% |

$$\text{Expected Loss} = 3\% \times 25\% = 0.75\%$$

If the bond's actual credit spread is greater than 0.75%, investors may be more than compensated for estimated credit loss. If the spread is lower, compensation may be inadequate.

---

## 5. Credit Ratings

Credit ratings help investors compare credit risk across issuers, sectors, and instruments.

| Rating category | Meaning |
|------|------|
| **Investment grade** | Baa3 / BBB- or higher |
| **High yield** | Ba1 / BB+ or lower |

### Limitations

- Ratings can lag market prices.
- Some risks are difficult to assess.
- Rating agencies are not perfect.
- Market spreads often react faster than ratings.

---

## 6. Credit Spread Risk

**Credit spread risk** = risk that credit spreads widen, causing risky bond prices to fall.

This is especially important for investment grade bond investors because default probability may be low but spread movements can still affect price materially.

| Factor | Spread impact |
|------|------|
| Strong economic growth | Spreads tend to contract |
| Recession or crisis | Spreads tend to widen |
| Issuer financial deterioration | Spreads widen |
| Lower liquidity | Bid-offer spread widens |

High yield spreads are usually more volatile than investment grade spreads.

---

## 7. Yield Spread Components

Yield spread can include:

- credit spread
- liquidity spread
- term premium
- optionality premium

Bid-offer spread is a common proxy for liquidity risk.

### Exam Points

- Expected loss combines probability and severity.
- Recovery rate reduces LGD.
- Ratings are useful but lag market information.
- Credit spreads widen in weaker economic conditions and when liquidity deteriorates.
