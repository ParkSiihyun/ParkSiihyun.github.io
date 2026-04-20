---
title: "CFA FSA Reading 36 — Financial Reporting Quality"
date: 2026-04-10
categories: cfa
tags: [FSA, CFA Level I, Reporting Quality]
---

## 1. Quality of Earnings

수익의 질은 **지속가능성(Sustainability)**과 **수준(Level)**으로 판단

- **지속 불가능한 이익**: 환율 변동, 자산 매각 등에서 발생
- **지속 가능한 이익**: 효율성 향상, 시장점유율 확대 등에서 발생

> US GAAP을 준수한 재무제표라도 수익의 질이 높다는 보장은 없음

---

## 2. Conservative vs Aggressive Accounting

| 구분 | 경향 | NI·RE | 배당 | 미래 수익 |
|------|------|-------|------|---------|
| **Conservative** | 비용 조기 인식 | 감소 | 감소 | 증가 |
| **Aggressive** | 수익 조기 인식 | 증가 | 증가 | 감소 |

> 채권자 입장에서는 Conservative가 선호됨  
> 기업들은 주가 안정을 위해 두 방법을 혼용 → **Earnings Smoothing**

### Cookie Jar
보수적 회계로 이익을 미리 숨겨두었다가 나중에 꺼내 쓰는 전략

---

## 3. Aggressive Accounting 기법

| 기법 | 내용 |
|------|------|
| Capitalizing current period costs | 즉시 비용처리 대신 자본화 → 감가상각으로 분산 |
| Longer asset useful life | 내용연수 길게 추정 → 연간 감가상각비 감소 |
| Higher salvage value | 잔존가치 높게 추정 → 감가상각 기준액 감소 |
| Straight-line depreciation | 초기 비용 최소화 (가속상각 대비) |
| Delayed impairment recognition | 손상차손 인식 지연 |
| Less bad debt accrual | 대손충당금 적게 설정 |
| Smaller valuation allowance on DTA | 평가충당금 적게 잡아 비용 감소 |

---

## 4. Conservative Accounting 기법

| 기법 | 내용 |
|------|------|
| Expensing current period costs | 즉시 비용처리 |
| Shorter asset useful life | 내용연수 짧게 추정 → 감가상각비 증가 |
| Lower salvage value | 잔존가치 낮게 추정 |
| Accelerated depreciation | 초기 비용 증가 |
| Early impairment recognition | 손상차손 조기 인식 |
| More bad debt accrual | 대손충당금 많이 설정 |
| Larger valuation allowance on DTA | 평가충당금 크게 잡아 비용 증가 |

> US GAAP의 보수적 기준 예시:
> - 연구비는 원칙적으로 발생 시 즉시 비용처리
> - 법적 손실 충당금은 지급 가능성이 높아질 때 인식
> - 재고 Write-down 의무화

---

## 5. Fraud Triangle

회계 부정이 발생하는 3가지 조건:

```
        Motivation (동기)
           /      \
Opportunity  —  Rationalization
  (기회)          (합리화)
```

### Motivation (동기)
- 경영진이 제시한 이익 가이던스 달성 압박
- 애널리스트 컨센서스 맞추기
- 전년 동기 실적 유지

### Opportunity (기회)
- 내부통제 취약
- 이사회의 감독 부실
- 허용 범위가 넓은 회계기준
- 위반 시 처벌 미약

### Rationalization (합리화)
- 규칙을 어기는 것이 정당하다는 자기합리화

---

## 6. 부정 방지 메커니즘

- **SEC** (미국), **FCA** (영국), **IOSCO** (국제) 등 규제기관
- 재무제표와 함께 **내부통제(Internal Controls)**도 감사 대상

---

## 7. 조작 가능한 주요 회계 항목

### Revenue Recognition
- Over Time vs At a Point in Time 선택
- FOB Shipping Point vs FOB Destination (인도 기준 차이)
- **Channel Stuffing**: 판매되지 않은 재고를 유통업자에게 밀어넣어 매출 인식
- **Bill-and-Hold**: 고객에게 구매를 유도하고 물건을 판매자가 보관하면서 수익 인식

### Estimates of Credit Losses (대손충당금)
- 수익 좋을 때 → 충당금 많이 잡아 이익 축소 (Cookie Jar)
- 수익 나쁠 때 → 충당금 줄여 이익 증가
- Warranty Reserve도 같은 메커니즘

### Valuation Allowance on DTA
- 적게 잡으면 비용 감소 → 이익 증가
- 많이 잡으면 비용 증가 → 이익 감소

### Depreciation Methods & Estimates
- 가속상각: 초기 비용 ↑, NI ↓, 이후 반전
- 정액법: 초기 비용 최소화
- 내용연수·잔존가치 조정으로 NI와 자산 장부가 조작 가능

### Inventory Method
- 인플레이션 환경: FIFO > 가중평균 순으로 Gross Profit 높음
- 인플레이션·디플레이션 모두에서 FIFO Inventory가 현재 가치를 더 잘 반영
- Weighted Average COGS가 현재 원가를 더 잘 반영 → Gross Profit의 Reporting Quality 더 높음

### Related Party Transactions (특수관계자 거래)
- 납품 단가 조작으로 이익 조작 가능

### Other CF Effects — Stretching Payables
- AR은 줄이고 AP를 늘려 CFO를 단기적으로 인위적 개선
- 예) 티몬·위메프 사태: 판매 대금을 AP로 보류하고 투자에 운용했으나 손실 후 지급 불능
