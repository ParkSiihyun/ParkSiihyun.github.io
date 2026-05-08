---
title: "Mortgage-Backed Security Instrument and Market Features (Reading 65)"
date: 2026-05-05
categories: cfa
tags: [Fixed Income, CFA Level I, MBS, RMBS, CMBS, Prepayment Risk, Reading 65]
excerpt: "Sihyun CFA Notes - Mortgage-Backed Security Instrument and Market Features (Reading 65)"
---

## Quick Take

- 중심 주제: **Mortgage-Backed Security Instrument and Market Features**
- 먼저 잡을 축: Mortgage-Backed Securities, Prepayment Risk, Mortgage Loan Features
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Mortgage-Backed Securities
2. Prepayment Risk
3. Mortgage Loan Features
4. LTV and DTI
5. Agency and Non-Agency RMBS
6. Mortgage Pass-Through Securities
7. Collateralized Mortgage Obligations
8. CMBS
9. PAC and Support Tranches

## Main Notes

## 1. Mortgage-Backed Securities

Mortgage-backed securities are backed by pools of mortgage loans.

The key difference from many corporate bonds is that mortgage borrowers can often repay principal earlier than scheduled.

This creates prepayment risk.

---

## 2. Prepayment Risk

**Prepayments** = principal repayments in excess of scheduled amortization.

| Risk | Meaning |
|------|------|
| **Contraction risk** | Cash flows arrive sooner than expected |
| **Extension risk** | Cash flows arrive later than expected |

Interest rates are a major driver of prepayment speed.

| Rate environment | Typical MBS effect |
|------|------|
| Rates fall | More refinancing, higher contraction risk |
| Rates rise | Less refinancing, higher extension risk |

<figure class="sh-diagram">
  <img src="/images/cfa/reading65-prepayment-risk-map.svg" alt="Mortgage-backed security prepayment risk map for falling and rising interest rates">
  <figcaption>MBS는 금리가 떨어지면 조기상환이 늘어 cash flow가 짧아지고, 금리가 오르면 조기상환이 줄어 cash flow가 길어진다.</figcaption>
</figure>

---

## 3. Mortgage Loan Features

| Feature | Meaning |
|------|------|
| Prepayment penalty | Fee charged when borrower prepays |
| Recourse loan | Lender can claim other borrower assets |
| Nonrecourse loan | Lender's claim is limited mainly to the property |
| Underwater mortgage | Property value is below loan balance |

---

## 4. LTV and DTI

**Loan-to-value (LTV)**:

$$LTV = \frac{\text{Loan Amount}}{\text{Property Value}}$$

**Debt-to-income (DTI)**:

$$DTI = \frac{\text{Monthly Debt Payments}}{\text{Monthly Pretax Income}}$$

| Loan type | Typical profile |
|------|------|
| Prime loan | Lower LTV and lower DTI |
| Subprime loan | Higher LTV and higher DTI |

---

## 5. Agency and Non-Agency RMBS

| Type | Description |
|------|------|
| **Agency RMBS** | Guaranteed by government or government-sponsored enterprise |
| **Non-agency RMBS** | Issued by private entities such as banks |

Agency RMBS collateral must meet underwriting standards.

Non-agency RMBS typically uses credit enhancement such as insurance, overcollateralization, or tranching.

---

## 6. Mortgage Pass-Through Securities

In a pass-through MBS, principal and interest payments from the mortgage pool are passed through to investors after servicing and administrative fees.

Important pool measures:

| Measure | Meaning |
|------|------|
| **WAM** | Weighted average maturity of the mortgage pool |
| **WAC** | Weighted average coupon rate of the mortgage pool |

---

## 7. Collateralized Mortgage Obligations

**CMO** = security backed by mortgage pass-through securities or pools of mortgages.

CMOs divide cash flows into multiple tranches with different exposure to prepayment risk.

| Tranche type | Feature |
|------|------|
| Sequential-pay tranche | Principal paid to tranches in order |
| Z-tranche / accrual tranche | Accrues interest until earlier tranches are paid |
| Principal-only security | Receives principal cash flows |
| Interest-only security | Receives interest cash flows |

Prepayment affects principal-only and interest-only securities differently.

---

## 8. CMBS

Commercial mortgage-backed securities are backed by commercial property loans.

Key CMBS features:

| Feature | Meaning |
|------|------|
| Call protection | Limits early repayment |
| Defeasance | Borrower substitutes acceptable collateral |
| Balloon payment | Large principal payment at maturity |

Compared with RMBS, CMBS loans are usually repaid from commercial property cash flows, such as tenant rent and business income.

---

## 9. PAC and Support Tranches

**Planned amortization class (PAC)** tranches are structured to provide more predictable principal payments as long as prepayments stay within a specified range.

Support tranches absorb more prepayment variability to protect PAC investors.

### Exam Points

- Falling rates create contraction risk; rising rates create extension risk.
- Agency RMBS has government or GSE support; non-agency RMBS relies more on credit enhancement.
- CMOs redistribute prepayment risk across tranches.
- CMBS credit depends heavily on commercial property cash flows and call protection.
