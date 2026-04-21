---
title: "CFA Equity Reading 40 — Security Market Index"
date: 2026-04-20
categories: cfa
tags: [Equity, CFA Level I, Index]
---

## 1. Security Market Index

자산군, 증권시장, 특정 섹터 등의 실적을 보여주는 것

**예시**: 한국종합주가지수(KOSPI), KOSPI200, S&P500, DJIA 등

---

## 2. Price Index vs Return Index

기준년도의 지수를 **100**으로 잡고 복리수익률로 현재의 지수를 계산

| 지수 유형 | 계산 방식 |
|-----------|-----------|
| **Price index** | $\text{Price Return} = \dfrac{V_1 - V_0}{V_0}$ |
| **Return index** | $\text{Total Return} = \dfrac{V_1 - V_0 + \text{Income}}{V_0}$ |

---

## 3. Choices in Index Construction and Management

| 결정 사항 | 예시 |
|-----------|------|
| Which target market? | 미국 + 주식 |
| Which securities? | 시가총액 상위 500개 |
| How much weight? | 시가총액 가중치 / 가격 가중치 |
| When rebalanced? | 가중치 변경은 얼마나 자주? |
| When re-examined? | 종목 교체는 어떻게? |

---

## 4. Weighting Methods

### Price-Weighted Index

: 인덱스에 포함된 증권의 **가격의 산술평균**

- 고가 주식이 인덱스에 더 큰 영향을 줌
- 초기에는 각 종목의 가격의 산술평균 그 자체를 인덱스 100으로 설정
- **주식 분할** 같은 이벤트가 있으면 분모도 같이 조정해줘야 함 → 가격만 반토막 나면 인덱스 급락

**예시**: Dow Jones Industrial Average (DJIA)

---

### Equal-Weighted Index

: 각 종목에 **동일한 금액**을 투자한 포트폴리오의 수익률 = 각 종목 수익률의 **산술평균**

- 각 종목의 가중치를 같게 한다는 점에서 시가총액 가중치 인덱스와 차이
- 직관: 모든 종목에 동일하게 투자한 포트폴리오
- 시작 100, 각 종목의 수익률의 산술평균이 6.7%면 → **106.7**

---

### Market Capitalization-Weighted Index (Value-Weighted Index)

: 각 종목의 시가총액 비중으로 가중치를 부여

- 가중치 = 각 종목의 시가총액 / 전체 시가총액
- 인덱스 수익률 = 가중치 × 각 종목의 수익률

---

### Weighting Methods 예제

| 종목 | 가격 | 주식 수 | 시가총액 |
|------|------|---------|---------|
| A주 | $100 → $110 | 10 | 1,000 → 1,100 |
| B주 | $50 | 30 | 1,500 |
| Total | $150 → $160 | - | 2,500 → 2,600 |

**1. Price Weighted**
- 초기 평균: (100 + 50) / 2 = **$75**
- 이후 평균: (110 + 50) / 2 = **$80**
- 수익률: (80 - 75) / 75 = **6.7%** → Index: 100 → 106.7

**2. Equal Weighted**
- $100씩 A에 1주, $100씩 B에 2주 투자
- A: $100 → $110 (10% 수익), B: $100 → $100 (0% 수익)
- 수익률: (10% × 1/2) + (0% × 1/2) = **5%** → Index: 100 → 105

**3. Market Capitalization Weighted**
- A 가중치: 1,000 / 2,500 = **40%**
- B 가중치: 1,500 / 2,500 = **60%**
- 수익률: (10% × 40%) + (0% × 60%) = **4%** → Index: 100 → 104

---

### Weighting Methods 특징 비교

| 방법 | 특징 |
|------|------|
| **Price weighted** | 고가 주식이 더 큰 영향 / 계산 단순 / 주식 분할 시 임의적 변동 발생 |
| **Equal weighted** | 자주 리밸런싱 필요 / Under/Over representation 자주 발생 / 계산 단순 |
| **Market cap weighted** | 시가총액 큰 주식이 더 큰 영향 / 회사의 가치와 가중치가 연관 / Momentum 전략과 유사 |

---

## 5. Rebalancing & Reconstitution

### Rebalancing (가중치 재조정)

: 가격 변화로 흐트러진 포트폴리오 내 증권의 가중치를 재조정

- Price weighted / Market cap weighted는 가격 변화로 자동 조정
- **Equal weighted는 리밸런싱이 가장 중요한 이슈** (가격 조금만 변해도 비중이 깨짐)

### Reconstitution (종목구성 변경)

: 주기적으로 인덱스 기준을 충족하지 못하는 종목을 삭제하고 새 종목으로 교체

---

## 6. Uses of Market Indexes

- **Reflection of market sentiment** : 시장 분위기 파악
- **Benchmark of manager performance** : 펀드매니저의 최소 기준 (시장 수익률은 이겨야 하지 않겠나? → 알파 찾기)
- **Measure of market return and risk**
- **Measure of beta and risk adjusted return**
  - CAPM: 주식의 수익률 = 무위험 수익률 + 베타 × (시장 수익률 - 무위험 수익률)
- **Model portfolios** for index funds and ETFs

---

## 7. Type of Equity Indexes

| 유형 | 설명 |
|------|------|
| **Broad Market index** | 전체 시장 성과, 시장 총가치의 90% 이상 포함 (Ex. Wilshire 5000) |
| **Multi market index** | 여러 나라 시장 인덱스 (Ex. MSCI Emerging Markets) |
| **Sector index** | 특정 산업 섹터 수익률 (헬스케어, 금융 등) |
| **Style index** | 시가총액 및 가치/성장 전략 수익률 (Ex. Dow Jones US Small Cap Value) |

### 대표 지수 비교

| 지수 | 특징 |
|------|------|
| **DJIA** | 미국 대형주 30개 / Price weighted / WSJ 편집자가 종목 선정 |
| **Nikkei Stock Average** | 일본 대형주 225개 / Modified Price weighted |

---

## 8. Types of Fixed Income Indexes

- **Large universe of securities**: 채권은 기업뿐만 아니라 정부, 정부기관도 발행
- **Dealer market and infrequent trading**: 채권은 비유동적, 최근 거래가 없어 가격 추정 필요
- **Illiquidity, transaction costs, high turnover**: 채권 인덱스를 복제하는 것이 어렵고 비용이 많이 듦

---

## 9. Indexes for Alternative Investments

### Commodity Indexes

: Represent futures contracts on commodities

- 운용사마다 다양한 가중치 방식 사용 → 같은 상품이라도 인덱스마다 수익/리스크 특성이 크게 다를 수 있음
- **Future vs Actual**: 상품 인덱스는 현물 가격이 아닌 **선물 가격** 기반
- Commodity index return = 무위험 이자율 + 선물 가격 변화 + roll yield

### Real Estate Indexes

- Based on appraisals(평가), repeat property sales, or REIT performance
- 실물 부동산은 비유동적이나 REIT 주식은 유동적

### Hedge Fund Indexes

- 헤지펀드는 규제 미적용 → 인덱스 제공자에게 성과 보고 의무 없음
- 성과가 나쁜 펀드가 보고를 중단할 수 있어 **Survivorship Bias** 발생
- 같은 스타일이라도 인덱스마다 성과 차이가 클 수 있음
