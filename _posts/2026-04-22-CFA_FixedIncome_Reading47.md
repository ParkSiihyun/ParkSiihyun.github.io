---
title: "CFA Fixed Income Reading 47 — Fixed Income Instrument Features"
date: 2026-04-22
categories: cfa
tags: [Fixed Income, CFA Level I, Bonds, Coupon, Yield]
---

## 1. Fixed Income Instruments 기본 개념

| 구분 | 설명 |
|------|------|
| **Loans** | Private, nontradable agreements between borrower and lender |
| **Bonds (Fixed Income Securities)** | Standardized, tradable securities representing a debt investment |

- **Investors** in bonds are lending capital (= **principal / par / face value**) to the issuer
- **Issuer** promises to repay principal + interest (coupon), stated as a percentage of par
- 조달된 자본은 주로 **long-term investment** 자금으로 활용

---

## 2. Key Features of Bonds

### Issuer 발행자
- Sovereign national governments
- Corporations
- Local governments

### Maturity 만기
- **Tenor**: 잔여만기
- ≤ 1 year → **Money market securities**
- \> 1 year → **Capital market securities**
- 만기 없음 → **Perpetual bonds**

### Principal (Par / Face Value) 액면가
- 만기 시 상환하는 금액
- 일부 채권은 만기 이전에 분할 상환 (e.g., mortgage loan)

---

## 3. Coupon Rate and Frequency

쿠폰율 = 채권 액면가에 대한 연간 이자 지급 비율

| 지급 주기 | 예시 (Par $1,000, 4% annual) |
|-----------|-------------------------------|
| Annual | $40 × 1 |
| Semi-annual | $20 × 2 |
| Quarterly | $10 × 4 |

### Floating Rate Notes (FRN)
- 쿠폰이 변동 시장금리에 연동
- **FRN coupon = MRR (Market Reference Rate) + fixed margin (credit spread)**
- margin은 **basis points** (0.01%) 단위로 표현

> ex) FRN, quarterly: annualized MRR 2.3% + 75bp  
> → Quarterly rate = (2.3% + 0.75%) / 4 = **0.7625%**

---

## 4. Zero Coupon Bonds (Pure Discount Bonds)

- 만기 이전에 이자 지급 없음
- 액면가 **할인 발행** → 만기 시 par value 수령
- **Pure discount**: 모든 이자가 만기에 집중됨

---

## 5. Other Coupon Structures

### Step-up Coupon Bonds
- 쿠폰율이 **사전에 정해진 일정에 따라 상승**
- 금리 상승 시 투자자 보호 → 채권 가격 하락 방어

### Credit-Linked / Leveraged Loan
- 발행자의 신용등급이 낮아지면 쿠폰율 상승
- ex) **Leveraged loan**: 신용등급 낮은 차입자에게 제공되는 대출

### Payment-in-Kind (PIK) Bond
- 쿠폰을 현금 대신 **추가 채권 발행**으로 지급
- 신용등급이 매우 낮고, 유동성이 매우 불안정한 발행자

---

## 6. Principal Repayment Structures

### Bullet Structure
- 만기에 원금을 **일시 상환** (가장 일반적인 구조)

| Year | 1 | 2 | 3 | 4 | 5 |
|------|---|---|---|---|---|
| PMT | $50 | $50 | $50 | $50 | $1,050 |
| Principal Remaining | $1,000 | $1,000 | $1,000 | $1,000 | 0 |

### Amortizing Loan
- 각 기간 지급액에 **이자 + 원금 상환** 모두 포함

#### Fully Amortizing
- 마지막 지급으로 원금 **완전 상환**

| Year | 1 | 2 | 3 | 4 | 5 |
|------|---|---|---|---|---|
| PMT | 230.97 | 230.97 | 230.97 | 230.97 | 230.98 |
| Principal Remaining | 819.0 | 629.01 | 429.49 | 219.99 | 0 |

> N=5, I/Y=YTM 5%, PV=1000, FV=0 → PMT=?

#### Partially Amortizing
- 만기에 **balloon payment** (잔여 원금) 존재

> N=5, I/Y=5%, PV=1000, FV=-200 → PMT=-194.78

### Sinking Fund Provisions
- 원금을 **시리즈의 지급으로 상환**하는 조항

> ex) 20년 만기, 원금 $300M → 6년 후부터 매년 $20M씩 15년간 갚아나감

| 구분 | 내용 |
|------|------|
| **Advantage** | 원금을 계속 갚기 때문에 신용리스크 감소 |
| **Disadvantage** | 금리 하락 시 reinvestment risk 발생 → 설립된 채권수익률 강요 |

---

## 7. Waterfall Structures

- ABS(Asset-Backed Securities) & MBS(Mortgage-Backed Securities)의 원금 상환 순서 결정
- **Tranches**: 선순위(senior) → 후순위(junior) 순으로 원금 수령
- Senior tranche가 완전히 상환될 때까지 Junior tranche는 원금 미수령

---

## 8. Seniority (선순위)

- 파산/청산 시 채권 투자자의 청구권은 **주식 투자자보다 우선**
- **Senior debt > Junior (Subordinated) debt**
- 선순위일수록 credit risk 낮음

---

## 9. Yield Measures

$$P_0 = \sum_{t=1}^{N} \frac{CF_t}{(1+y)^t}$$

- **Prices and yields are inversely related**: $P \downarrow \Rightarrow y \uparrow$
- 여기서 yield = **YTM (Yield to Maturity)**

### Yield Curve

만기가 다른 채권은 서로 다른 yield를 가짐

| 형태 | 설명 |
|------|------|
| **Upward sloping (Normal)** | 장기일수록 uncertainty↑ → yield↑ |
| **Inverted** | 금융위기 때 자주 나타남 |

- Government bonds: 가장 낮은 credit risk → **yield curve의 benchmark**

---

## 10. Bond Indenture (채권 계약서)

- 채권 발행자와 투자자 간의 **법적 계약**
- 차입자의 의무와 제한 사항 명시
- 미래 발행자-투자자 간 모든 상호작용의 기반

### Source of Repayment (상환 재원)

| 발행자 유형 | 상환 재원 |
|------------|-----------|
| Sovereign | 세금 + 화폐 발행 능력 (인플레이션 가능) |
| Local government | 지방세, 인프라 운영 수익 (toll road 등) |
| Corporate (Secured) | 영업 CF + 담보 자산 (collateral) |
| Corporate (Unsecured) | 영업 CF only |
| ABS | SPE가 보유한 금융자산의 CF |

---

## 11. Bond Covenants (채권 내 의무 조항)

### Affirmative Covenants (긍정적 조항)
- 투자자의 권리를 강화하는 **이행 의무**

| 예시 | 내용 |
|------|------|
| **Cross default** | 발행자가 다른 채권에 디폴트 시, 이 채권도 디폴트로 간주 → 즉시 상환 요구 가능 |
| **Pari passu** | 동일 순위 채권자는 청산 시 동등한 지위 → 특정 채권을 subordinate 불가 |

### Negative Covenants (부정적 조항)
- 발행자에게 **~하지 말라**는 제한

- Entering into asset sales and leaseback agreements
- Pledges of collateral (이중담보 제공 금지)
- Issuance of debt ranking more senior (negative pledge clause)
- Additional borrowings, share repurchases, dividend payments — incurrence test 통과 시에만 허용
