---
title: "CFA Equity Reading 46 — Equity Valuation: Concepts and Basic Tools"
date: 2026-04-20
categories: cfa
tags: [Equity, CFA Level I, Valuation, DDM, DCF]
---

## 1. DDM — Dividend Discount Model

배당금을 현재가치로 할인하여 주식의 내재가치를 산출하는 모델

**V₀ = Σ [ Dₜ / (1 + Kₑ)ᵗ ]** (t = 1 → ∞)

> ※ **V ≠ P** : Intrinsic value ≠ Market price

| 변수 | 의미 |
|------|------|
| **V₀** | Current stock value (현재 주식 내재가치) |
| **Dₜ** | Dividend at time t (t 시점의 배당금) |
| **Kₑ** | Required rate of return on common equity |

---

### One-Year Holding Period DDM

**Value = P₁ / (1 + Kₑ) + D₁ / (1 + Kₑ)**

---

### Multiple-Year Holding Period DDM

**Value = D₁ / (1 + Kₑ) + D₂ / (1 + Kₑ)² + Pₙ / (1 + Kₑ)ⁿ**

---

### DDM Example

> A stock recently paid a dividend of $1.50, expected to grow at 8% per year. Required rate of return = 12%.  
> **3년 뒤 주식의 가격 = $51.00**

- D₀ = $1.5
- D₁ = 1.5 × (1.08)
- D₂ = 1.5 × (1.08)²
- D₃ = 1.5 × (1.08)³, P₃ = $51

---

## 2. Free Cash Flow to Equity (FCFE)

FCFE = 보통주 주주에게 지급 가능한 현금흐름

- FCFE reflects the firm's **capacity to pay dividends**

### FCFE 계산식

```
FCFE = NI + Depreciation/Amortization - Net Working Capital - CAPEX + Net Borrowing
     = CFO - CAPEX + Net Borrowing (borrowed - repaid)
```

**V₀ = Σ [ FCFEₜ / (1 + Kₑ)ᵗ ]** (t = 1 → ∞)

---

## 3. Estimating the Required Return for Equity

요구수익률(Kₑ)의 추정 → **수익률의 변동성** 기반

### CAPM (Capital Asset Pricing Model)

**Kᵢ = Rꜰ + βᵢ × [E(Rₘ) - Rꜰ]**

- 구성의 핵심: 위험 프리미엄을 얼마나 조정할지 결정

---

## 4. Preferred Stock Valuation

우선주는 **고정 배당금** 지급 + **만기 없음 (indefinite maturity)**

**Preferred Stock Value = Dₚ / Kₚ**

(무한등비급수의 합으로 도출)

### Example

> $100 par preferred stock, $5.00 annual dividend, required return = 8%

**Value = $5 / 0.08 = $62.5**

→ 액면 $100인 주식이 요구수익률 8%이면, $5를 8%로 사면 $62.5에 매수

---

## 5. Gordon Growth Model (Constant Growth Model)

배당이 **일정한 성장률(Gc)**로 영구히 성장한다고 가정

**V₀ = D₀(1+Gc)/(1+Ke) + D₀(1+Gc)²/(1+Ke)² + ... + D₀(1+Gc)^∞/(1+Ke)^∞**

- 첫째항: D₁ / (1 + Ke)
- 공비: (1 + Gc) / (1 + Ke)

> **수렴 조건: Ke > Gc 일 때만 성립** (Ke < Gc면 발산, 사용 불가)

### 등비급수 공식 적용

무한등비급수: S = a / (1 - 공비)

→ D₁/(1+Ke) ÷ [1 - (1+Gc)/(1+Ke)] = D₁/(1+Ke) ÷ [(Ke-Gc)/(1+Ke)]

**V₀ = D₁ / (Ke - Gc)**

### Gordon Growth Model Example

> D₀ = $1.5, growth rate = 8%, Ke = 12%

**V₀ = (1.5 × 1.08) / (0.12 - 0.08) = 1.62 / 0.04 = $40.50**

---

## 6. Key Insight: Ke vs Gc 관계

The stock's value is determined by the relationship between **Ke** and **Gc**

| 상황 | 주가 영향 |
|------|-----------|
| Ke와 Gc의 차이 확대 | 주식 가치 하락 |
| Ke와 Gc의 차이 축소 | 주식 가치 상승 |
| Ke와 Gc의 작은 변화 | 주식 가치에 **큰 변화** 발생 가능 |

- **Ke가 크다는 것**: 주식이 시장위험 대비 변동성이 크다(위험하다)는 뜻 → 위험한 주식의 가치는 안정적인 주식보다 낮음
- **Gc가 클수록**: 배당성장률이 큰 기업의 가치가 더 큼
- 즉, Ke는 작을수록, Gc는 클수록 좋음. **그 격차가 줄어들면 주식 가치 상승**

---

## 7. Estimating Growth Rate in Dividends

### 3가지 방법

1. **Use the historical growth in dividends for the firm** (과거 배당 성장률 사용)
2. **Use the median industry dividend growth rate** (산업 중간값 사용)
3. **Estimate sustainable growth rate** (지속가능 성장률 추정)

### Sustainable Growth Rate

: The rate at which equity, earnings, and dividends can continue to grow **indefinitely** assuming:
- ROE is constant
- Dividend payout ratio is constant
- No new equity is sold

**Sustainable Growth = (1 - Dividend Payout Ratio) × ROE = Retention Rate × ROE**

### Example (EPS 기반 D₁ 계산)

- D₁ = E₀ (earnings) × payout ratio × (1 + Gc)
- Gc = Retention rate × ROE
- D₁ = E₁ × payout ratio

> NI = 100, Payout = 30 (payout ratio 0.3), Retention = 70 (retention rate 0.7), ROE = 10%
>
> - Gc = 10% × 0.7 = **7%**
> - D₁ = E₀ × 0.3 × (1 + 0.07) = 30 × 1.07 = **32.1**

---

## 8. A Firm with No Current Dividend

현재 배당이 없는 기업의 경우, 미래에 배당이 시작될 시점을 예측하여 역산

### Example

> D₄ = E₄ × 0.5 = $0.82 (D₄를 알면 D₃를 알 수 있다)
>
> V₃ = D₄ / (Ke - Gc) = 0.82 / (0.1 - 0.05) = **$16.4**
>
> V₀ = 16.4 / (1.1)³ = **$12.32**

---

## 9. Multi-Stage Dividend Growth Model

성장률이 단계별로 다른 기업에 적용

**Vₙ = D(n+1) / (Ke - Gc)**

### Example

> D₀ = $1, 처음 2년: 15% 성장, 이후: 5% 성장, Ke = 11%

- D₁ = $1.15
- D₂ = $1.32
- D₃ = $1.386

> V₂ = D₃ / (Ke - Gc) = 1.386 / (0.11 - 0.05) = **$23.1**
>
> (2년 시점에서 바라본 3년 이후 시점의 배당들의 현가)

**V₀ = 1.15 / (1.11) + (1.32 + 23.1) / (1.11)²**

> Vₙ은 미래에 지급될 배당들의 현재가치인 거임. n 시점에서 바라본 것.  
> 그래서 n=2 시점의 배당은 따로 더해줘서 할인해야 함.

---

## 10. Appropriate Models 정리

| 상황 | 적합한 모델 |
|------|-------------|
| 안정적, 성숙한, 비경기민감, 배당 지급 기업 | **Gordon Growth Model** (constant growth) |
| 배당이 급격히 성장하거나, 느리게 또는 불규칙하게 성장하는 기업 | **Multistage Growth Model** |
| 초기 고성장 → 전환기 저성장 → 장기 안정 성장 (젊은 기업) | **3 Stage Model** |

---

## 11. Relative Valuation Measures (상대가치평가)

### Price Multiples

**Value = EPS × Multiples (Peer의 PER)**  
또는 BPS × PBR, Sales per share × P/S, CF per share × P/CF

- EPS × P/E > Price → **저평가!**

---

### Justified P/E (적정 P/E)

Gordon Growth Model에서:

- P₀ = D₁ / (K - g)
- 양변을 E₁으로 나누면:
- P₀/E₁ = (D₁/E₁) / (K - g) = **Payout ratio / (K - g)**

**∴ Justified P/E = Payout ratio / (K - g)**

: A benchmark for the price at which the stock should trade

---

### Multiples Based on Comparables

: Common benchmarks include the stock's **historical average** (time series) or **similar stocks/industry averages** (cross sectional)

- 법칙: **Law of one price** (동일 자산은 동일 가격)

**단점:**
1. Stock may appear overvalued by comparable method but undervalued by fundamental method
2. Different accounting methods → NI끼리 비교 불가
3. Cyclical 기업의 price multiple은 경기 상황에 따라 크게 영향 받음 (EPS가 너무 불안정하면 Sales나 CF를 사용하는 것도 방법)

**정리:**
- Price multiple = **펀더멘털** 방법 vs **비교** 방법 두 가지
  - 펀더멘털: Justified P/E를 구해서 비교
  - 비교: 자신의 과거와 비교 / 같은 산업 내 기업들과 비교

---

## 12. Enterprise Value (EV) Multiples

**Enterprise Value = Market Value of Equity (CS + PS) + Market Value of Debt - Cash and Investments**

= Take-over value (인수 시 지불해야 하는 전체 가치)

> 인수자는 D + E를 모두 사지만, Cash + Short term investments로 회수 가능

### EV/EBITDA 사용 이유

| 이유 | 설명 |
|------|------|
| EBITDA는 대부분 양수 | Earnings이 음수여도 EBITDA는 보통 양수 |
| 자본구조 영향 적음 | 기업 간 자본구조가 다르면 NI 비교가 어렵지만, EV/EBITDA는 자본구조에 덜 민감 |
| 분자가 전체 기업가치 | Operating income도 사용 가능 (채권자+주주 모두의 이익과 비교해야 하므로) |

### EV 활용 방법 (흐름 정리)

1. **EV / EBITDA**: 회사가 채권자와 주주의 돈으로 벌어들이는 돈에 비해 몇 배의 가치로 인정받고 있어?
2. 그러면 우리 회사는 이만큼 버니깐 → 우리 회사 가치(EV target)는 이정도 되겠네
3. **EV_target = EBITDA_target × (EV/EBITDA)_peer**
4. **Equity Value = EV_target + Cash - Debt - PS**
5. 우리 회사의 시가총액과 비교 → **고평가 / 저평가 판단**

---

## 13. Asset-Based Valuation

**Value = Market Value of Assets - Market Value of Liabilities**

**적합한 상황:**
- 주로 유형자산을 보유한 기업
- 시장가치가 있는 자산 보유 (금융, 천연자원 기업)
- 청산 중인 기업

**잠재적 문제:**
- 시장가치 결정의 어려움
- Book value와 MV의 큰 차이
- 무형자산 처리
- 인플레이션 환경에서의 왜곡

---

## 14. 각 Valuation Model 장단점 비교

### Present Value Models (DDM, FCFE)

| 구분 | 내용 |
|------|------|
| **장점** | 이론적으로 우수 |
| **단점** | Input(k, g)이 모두 추정치 → 불확실성 높음, 가치평가 시 input에 매우 민감 |

### Multiplier Models (P/E, P/B, EV/EBITDA 등)

| 구분 | 내용 |
|------|------|
| **장점** | 계산 쉽고 분석이 직관적으로 이해 가능 |
| **단점** | Fundamental vs Comparable 방식 간 결론 차이 가능 / 회계방법 다르면 비교 어려움 / 경기민감 기업의 multiple은 경제 상황에 크게 영향 / Industry/Size/Growth 다른 기업 간 비교 어려움 / 분모가 음의 값이면 사용 불가 |
