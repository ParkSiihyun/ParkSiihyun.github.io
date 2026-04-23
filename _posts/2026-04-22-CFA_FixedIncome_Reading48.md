---
title: "CFA Fixed Income Reading 48 — Fixed Income Contingency Provisions"
date: 2026-04-22
categories: cfa
tags: [Fixed Income, CFA Level I, Callable Bond, Putable Bond, Convertible Bond]
---

## 1. Contingency Provisions 개요

- **Provisions > Covenants**: 조항 전반 > 채권 내 의무 조항
- Contingency Provisions = 특정 사건 발생 시 취할 수 있는 조치
- Bond indenture 내 contingency provisions = **Embedded options**

---

## 2. Callable Bonds

**Issuer에게 call option 부여** → 만기 이전에 정해진 가격(call price)으로 채권을 매입 상환할 권리

> ex) 6%, 20-year bond, issued at par on June 1, 2022
> - June 1, 2027 이후: 102% of par로 상환 가능
> - June 1, 2030 이후: 101% of par
> - June 1, 2031 이후: 100% of par (= **Call Schedule**)

- **Call protection**: 발행일로부터 최초 콜 가능일까지의 기간 (위 예시: 5년)

### Call Option의 가치

- 시장금리 하락 → 채권 가격 상승 → 발행자가 더 싼 가격에 재발행 가능 → **발행자에게 유리**
- 시장금리 상승 → 발행자는 콜 행사 안 함

### Call Risk (투자자 입장)

| 위험 | 내용 |
|------|------|
| Uncertain redemption date | 만기가 불확실해짐 |
| Call price = upper limit | 시장에서 채권 가격이 102 이상 오를 수 없음 (102에 콜할 것이므로) |

> 금리 하락 시 채권 가격이 상승하지만, 발행자는 그냥 들고 있을 필요가 없다. 콜 하고 재발행하면 된다. 이와 동시에 재권 시장에서는 금리가 하락하면 채권의 가격이 상승하는데, 어처피 102에 발행자가 콜 할 것이라 예상이 되면, 채권의 가격은 그 이상 오를 리가 없다.

### 가격 공식

$$P^{SB} = \sum_{t=1}^{N} \frac{CF_t}{(1+y_{SB})^t} > P^{CB} = \sum_{t=1}^{N} \frac{CF_t}{(1+y_{CB})^t}$$

- Call risk 때문에 투자자는 더 높은 yield 요구 → $y_{SB} < y_{CB}$
- $P^{SB} - P^{CB}$ = **Call option의 가치**

---

## 3. Putable Bonds

**Bondholder에게 put option 부여** → 정해진 가격(보통 par)에 발행자에게 채권을 되팔 권리

- 행사 시점: 금리 상승 또는 발행자 신용 악화로 채권 가격이 put price 아래로 하락했을 때
- 선택권이 **투자자**에게 있음 → putable bond는 더 높은 가격에 거래

$$P^{Putable} - P^{Straight} = \text{Put option의 가치}$$

---

## 4. Warrants 신주인수권

- 채권 보유자에게 발행 기업의 **보통주를 정해진 가격에 매수할 권리** 부여
- 일정 기간 동안 행사 가능

---

## 5. Convertible Bonds (CB)

채권을 발행 기업의 **보통주 일정 수량으로 교환할 권리** 부여

- Conversion option → 투자자에게 유리 → CB는 더 높은 가격(낮은 yield)으로 발행 가능

### 핵심 용어

| 용어 | 정의 |
|------|------|
| **Conversion Price** (전환가격) | 채권을 보통주로 전환할 때 적용되는 주당 금액 |
| **Conversion Ratio** (전환비율) | Par value / Conversion price = 전환 시 받는 주식 수 |
| **Conversion Value** | 전환 시 받는 주식들의 시장가치 |

> **예시:**
> - Par = $1,000, Conversion price = $40
> - Conversion ratio = 1,000 / 40 = **25 shares per bond**
> - 현재 주가 $50 → Conversion value = 25 × $50 = **$1,250**

---

## 6. Contingent Convertible Bonds (CoCo)

- **조건 발생 시 자동으로 주식으로 전환**되는 채권
- 주로 **은행**이 발행 — 은행은 특정 수준의 자기자본비율 유지 의무
- 은행의 equity가 required level 아래로 하락 → CoCo가 자동으로 보통주로 전환

---

## 7. Legal, Regulatory, and Tax Considerations

### 채권의 지역별 분류

| 구분 | 설명 |
|------|------|
| **Domestic bonds** | 발행자, 통화, 투자자 시장 모두 같은 국가 |
| **Foreign bonds** | 외국 발행자가 특정국의 통화로 그 나라 시장에서 거래 (ex. 한국 회사 → 달러 → 미국 시장) |
| **Eurobonds** | 특정 통화로 표시되지만 그 통화의 **국가 밖에서** 발행 (ex. 미국 달러 but 미국 밖에서 거래 → Eurodollar bond) |
| **Global bonds** | 여러 국가에서 동시에 발행 |

> - Eurobonds: 과거에는 **bearer bond** (무기명 채권) 형태로 발행
> - 현재는 **registered bonds** (소유자 기록 있음) 형태

- **Sukuk bonds**: 이슬람 율법을 준수하는 특수 조건의 채권

---

## 8. Taxation of Bond Income

채권 수익의 두 가지 원천과 세금 처리:

| 수익 유형 | 세금 처리 |
|-----------|-----------|
| **자본이득 (Capital gain)** | 일반 소득보다 낮은 세율 |
| **이자수익 (Interest income)** | 임금/급여처럼 과세 |

- 미국 **지방정부** 발행 채권의 이자수익: 면세
- **OID (Original Issue Discount) bonds** (ex. zero coupon bonds):
  - 할인된 금액(OID)을 이자수익으로 인식 → **실제로 받지 않아도 매년 과세**
