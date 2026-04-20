---
title: "CFA FSA Reading 34 — Topics in Long-Term Liabilities and Equity"
date: 2026-04-07
categories: cfa
tags: [FSA, CFA Level I, Liabilities, Leases]
---

## 1. Leases 개요

**Lessee**: 자산 사용권을 임차하는 자  
**Lessor**: 자산을 임대하는 자

리스는 자산 구매의 대안적 자금조달 방법

### 리스의 장점
1. 초기 현금 지출 최소화
2. 상대적으로 저렴한 조달 비용
3. 기술 진부화 리스크 감소

---

## 2. Operating Lease vs Finance Lease

### Finance Lease 판단 기준 (아래 중 하나 해당 시)
1. 리스 종료 시 자산 소유권이 Lessee에게 이전
2. Lessee가 염가매수선택권을 보유하고 행사 예상
3. 리스 기간이 자산 내용연수의 대부분 (75% 이상)
4. 리스료의 현재가치 ≥ 자산 공정가치
5. Lessor가 해당 자산을 다른 용도로 사용 불가

> 위 조건 미해당 시 → **Operating Lease**

---

## 3. Lessee 회계처리

### Operating Lease (IFRS: 소액·단기 제외, US GAAP: 12개월 이하 또는 $5,000 이하 제외)

| 시점 | 회계처리 | CF 분류 |
|------|----------|---------|
| 리스료 지급 | Rent Expense | CFO |

### Finance Lease (IFRS) / Finance & Operating Lease (US GAAP)

**개시 시점**: ROU Asset↑, Lease Liability↑ (= PV of lease payments)

| 항목 | Finance Lease | Operating Lease (US GAAP) |
|------|--------------|--------------------------|
| CFO | 낮음 (이자만) | 높음 (전액) |
| CFF | 낮음 (원금만) | 높음 |
| 감가상각 | ROU 직선상각 | ROU = L/O 잔액과 일치하도록 조정 |

> IFRS: 이자비용 → CFO 또는 CFF 선택 가능

---

## 4. Finance Lease 상각 스케줄 예시

> PV = $35,460 / 연 리스료 = $10,000 / 이자율 5% / 4년

| 연도 | 기초 L/O | 이자비용(5%) | 리스료 | 원금상환 | 기말 L/O | ROU BV |
|------|---------|------------|-------|---------|---------|--------|
| 1 | 35,460 | 1,773 | 10,000 | 8,227 | 27,233 | 26,595 |
| 2 | 27,233 | 1,362 | 10,000 | 8,638 | 18,595 | 17,730 |
| 3 | 18,595 | 930 | 10,000 | 9,070 | 9,525 | 8,865 |
| 4 | 9,525 | 475 | 10,000 | 9,525 | 0 | 0 |

---

## 5. Lessor 회계처리

### Operating Lease (Lessor)

| 시점 | 회계처리 | CF 분류 |
|------|----------|---------|
| 리스료 수취 | Rent Revenue | CFO |
| 감가상각 | Depreciation Expense | — |

### Finance Lease (Lessor)

- **개시 시점**: Lease Receivable↑ (= PV of lease payments + PV of 잔존가치), PPE 제거 → CFI
- **이자수익**: CFO (IFRS는 CFI 선택 가능)
- 감가상각 없음 (자산 제거했으므로)

---

## 6. Pension Plans (연금)

### DC (Defined Contribution Plan)
- 기업이 **확정된 기여금**만 납입
- 미래 급여액은 운용 성과에 따라 결정
- **투자 리스크 → 직원 부담**
- 기업의 연금 비용 = 당기 기여금

### DB (Defined Benefit Plan)
- 직원의 **미래 급여액이 확정**
- **투자 리스크 → 기업 부담**

$$\text{Net Pension (Funded Status)} = \text{Plan Asset} - \text{PBO}$$

| 상태 | 의미 |
|------|------|
| (+) Overfunded | Plan Asset > PBO |
| (−) Underfunded | Plan Asset < PBO |

> **PBO (Projected Benefit Obligation)**: 현재까지 발생한 미래 급여 지급 의무의 현재가치 (급여인상률 반영)

---

## 7. Share-Based Compensation (주식기준보상)

### 핵심 개념
- **Grant Date**: 부여일 — IFRS·US GAAP 모두 공정가치로 측정
- **Vesting Period**: 가득기간 동안 보상비용을 균등 배분

예) SBC $1M, 4년 가득 → 매년 $250,000 비용 인식

### 유형별 정리

| 유형 | 설명 |
|------|------|
| **Stock Grant (RSU)** | 제한 조건부 주식 지급, FV = 부여일 주가 |
| **Performance Shares** | 성과 목표 달성 시 지급 |
| **Stock Option** | 행사가격으로 주식 매입 권리, Black-Scholes 등으로 평가 |
| **SARs** | 주가 상승분을 현금으로 지급 → 신주 발행 없어 희석 없음, 단 현금 유출 발생 |

### 회계처리 흐름

```
Vesting Period 동안:
  Dr. Compensation Expense
  Cr. APIC (for share-based compensation reserve)   ← Equity 증가

Vesting 후 Stock Grant 실행:
  Dr. APIC (reserve)
  Cr. Common Stock + APIC

Stock Option 행사 시:
  Dr. Cash (행사가 × 주식수)
  Dr. APIC (reserve)
  Cr. Common Stock + APIC
```

> Stock Option 행사로 인한 현금 유입은 IS에 영향 없음 → NI 변동 없음  
> 신주 발행으로 주식수 증가 → **Dilution 효과**
