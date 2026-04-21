---
title: "CFA Equity Reading 45 — Company Analysis: Forecasting"
date: 2026-04-20
categories: cfa
tags: [Equity, CFA Level I, Company Analysis, Forecasting, Financial Modeling]
---

## 1. Forecast Approaches (예측 방법론)

### 네 가지 접근법

| 접근법 | 설명 |
|--------|------|
| **Historical results** | 과거 실적 기반 예측. 과거 트렌드를 미래에 그대로 적용 |
| **Historical base rate convergence** | 산업·경제 전체 평균으로 회귀하는 경향 반영. 예: 고마진 기업은 시간이 지나면서 평균 마진으로 수렴 |
| **Management guidance** | 경영진 제시 가이던스 참고. 단, 경영진 편향(낙관적 경향) 주의 |
| **Analyst discretionary forecast** | 애널리스트 자체 판단에 의한 예측. 독자적 분석 반영 |

### Forecast Horizon (예측 기간)

- 일반적으로 **보유 기간(holding period) 4~5년** 기준
- 산업 **경기순환(cyclicality)** 고려 → 전체 사이클 포함
- **기업 특수 이벤트** 반영 (신제품 출시, M&A, 구조조정 등)

---

## 2. Revenue Forecasting (매출 예측)

### Top-Down Approach

**거시경제 → 산업 → 기업** 순서로 추정

1. **GDP 성장률** 전망
2. **산업 성장률** 추정 (GDP 대비 배수 적용)
3. **기업의 시장점유율(Market Share)** 적용

$$\text{Revenue} = \text{Market Size} \times \text{Market Share}$$

### Bottom-Up Approach

**기업 자체 데이터**에서 출발하여 매출 구축

| 방법 | 설명 |
|------|------|
| **P × Q** | 가격 × 물량으로 분리 분석 |
| **제품 라인별(Product line)** | 제품군/지역별 매출 분해 |
| **Capacity-based** | 생산 가능 용량 × 가동률로 추정 |
| **Yield-based** | 특정 자산·고객으로부터의 수익률 기반 |
| **Hybrid** | 위 방법들의 혼합 적용 |

### Recurring vs Non-recurring Items

- **Recurring items**: 지속적으로 발생하는 항목 (영업 기반 예측)
- **Non-recurring items**: 일회성 항목 → 예측에서 **제외** 또는 별도 처리

---

## 3. COGS & SG&A Forecasting (비용 예측)

### COGS (매출원가) 예측

$$\text{Forecast COGS} = \frac{\text{Historical COGS}}{\text{Revenue}} \times \text{Estimated Future Revenue}$$

- 과거 **COGS/Revenue 비율**을 기반으로 미래 매출에 적용
- 원가 구조 변화(원자재 가격, 규모의 경제 등) 반영 필요

### SG&A (판매비·관리비) 예측

- 매출 변동에 **덜 민감** (고정비적 성격이 강함)
- 단기적으로는 안정적, 장기적으로는 매출 성장에 따라 완만히 증가
- **역사적 SG&A/Revenue 비율** + 기업 전략 변화 고려

---

## 4. Working Capital Forecasting (운전자본 예측)

### 핵심 공식

| 항목 | 예측 공식 | 비고 |
|------|-----------|------|
| **AR (매출채권)** | `DSO × (Sales / 365)` | DSO: Days Sales Outstanding |
| **Inventory (재고)** | `DOH × (COGS / 365)` | DOH: Days of Inventory on Hand |
| **AP (매입채무)** | `DPO × (Purchases / 365)` | DPO: Days Payable Outstanding |

### Cash Conversion Cycle (CCC)

**CCC = DSO + DOH - DPO**

- CCC가 **낮을수록** 운전자본 효율적 → 현금흐름 창출 능력 우수
- 소매업 등은 AP > AR → CCC 음수 가능 (현금을 먼저 받고 나중에 지급)

> **NWC와 현금흐름**: NWC 증가 → 현금 유출 / NWC 감소 → 현금 유입

---

## 5. CAPEX Forecasting (자본적 지출 예측)

**CAPEX = Maintenance CAPEX + Growth CAPEX**

| 구분 | 설명 | 예측 방법 |
|------|------|-----------|
| **Maintenance CAPEX** | 기존 자산 유지·교체 | 역사적 감가상각비 수준 참고 |
| **Growth CAPEX** | 사업 확장, 신규 설비 투자 | 매출 성장률·투자 계획 기반 |

- **자본집약 산업** (제조, 에너지, 통신): CAPEX 높음 → FCF 제약
- **소프트웨어/플랫폼**: CAPEX 낮음 → FCF 창출 능력 우수

---

## 6. Capital Structure Forecasting (자본구조 예측)

- **레버리지 비율** (부채비율, Net Debt/EBITDA 등) 목표 수준 설정
- 기업의 **신용등급**, 이자보상비율(Interest Coverage Ratio) 유지 수준 반영
- **배당 정책** 및 자사주 매입 계획 고려
- 부채 만기 구조와 차환(refinancing) 계획 반영

---

## 7. Scenario Analysis (시나리오 분석)

: 여러 가정을 **동시에** 변경하여 결과 비교 → 불확실성 범위 파악

| 시나리오 | 주요 가정 |
|----------|-----------|
| **Bull case (낙관)** | 높은 매출 성장률, 마진 개선, 낮은 금리, 유리한 경쟁 환경 |
| **Base case (기본)** | 컨센서스 기준, 중간 성장률·마진 |
| **Bear case (비관)** | 경쟁 심화, 마진 압박, 높은 금리, 수요 둔화 |

> **Sensitivity Analysis와의 차이**: Sensitivity는 변수를 **하나씩** 변화, Scenario는 **여러 변수를 동시에** 변화

---

## 8. Behavioral Biases in Analyst Forecasts (애널리스트 예측의 편향)

| 편향 | 설명 |
|------|------|
| **Overconfidence bias** | 자신의 예측 능력을 과신 → 신뢰구간 너무 좁게 설정 |
| **Anchoring bias** (Conservatism) | 초기 정보에 과도하게 집착, 새 정보 반영 부족 |
| **Representativeness bias** | 일부 특성으로 전체를 판단 → Base rate 무시 |
| **Confirmation bias** | 기존 견해를 확인하는 정보만 수집·해석 |
| **Illusion of control** | 통제 불가능한 요인을 통제 가능하다고 과신 |

> **예시 (Representativeness)**: "이 스타트업이 테슬라와 비슷하니 테슬라처럼 성공할 것"  
> → 대부분 스타트업은 실패한다는 Base Rate를 무시하는 오류
