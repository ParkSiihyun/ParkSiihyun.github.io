---
title: "CFA FSA Reading 30 — Analyzing Statements of Cash Flow"
date: 2026-04-04
categories: cfa
tags: [FSA, CFA Level I, Cash Flow]
---

## 1. Cash Flow Statement 개요

| 구분 | 기반 |
|------|------|
| IS (Income Statement) | Accrual-based (발생주의) |
| Cash Flow Statement | Cash-based (현금주의) |

- **CFO** (Cash Flow from Operations): 주로 유동자산·유동부채와 연관
- **CFI** (Cash Flow from Investing): 주로 비유동자산과 연관
- **CFF** (Cash Flow from Financing): 주로 비유동부채·자본과 연관

---

## 2. US GAAP vs IFRS — CF 분류 차이

| 항목 | US GAAP | IFRS |
|------|---------|------|
| 이자 지급 (발행자) | CFO | CFO or CFF |
| 이자 수취 (투자자) | CFO | CFO or CFI |
| 배당 수취 (투자자) | CFO | CFO or CFI |
| 배당 지급 (발행자) | **CFF** | CFF or CFO |

> 💡 배당 지급이 CFF인 이유: 배당은 IS를 거치지 않고 RE에서 직접 빠져나가기 때문에 영업활동이 아닌 재무활동으로 분류됨

---

## 3. Direct Method vs Indirect Method

- **Direct Method**: 현금 수입·지출 항목을 직접 표시 (CFO를 직접 계산)
- **Indirect Method**: NI에서 시작하여 비현금 항목과 운전자본 변동을 가감

> CFI, CFF는 두 방법 모두 Direct로 표시

---

## 4. CFO — Direct Method 계산

$$\text{Cash from Sales} = \text{Sales} - \Delta AR$$

$$\text{Cash for COGS} = -\text{COGS} - \Delta Inv + \Delta AP$$

$$\text{Cash for Wages} = -\text{Wage Expense} + \Delta W/P$$

$$\text{Cash for Interest} = -\text{Interest Expense} + \Delta I/P$$

$$\text{Cash for Tax} = -\text{Tax Expense} + \Delta T/P + \Delta DTL - \Delta DTA$$

---

## 5. CFO — Indirect Method 계산

```
Net Income
+ Depreciation & Amortization     (비현금 비용 가산)
- Gains / + Losses                 (CFI 항목 제거)
- ΔAR                              (매출채권 증가 → 현금 미수취)
- ΔInventory                       (재고 증가 → 현금 지출)
+ ΔAP                              (매입채무 증가 → 현금 미지급)
+ ΔW/P, ΔI/P, ΔT/P
+ ΔDTL - ΔDTA
= CFO
```

> 💡 재고 증감을 가감하는 이유: COGS는 비용처리 됐지만, 재고 매입에 지출한 현금(Inventory 증가분)은 NI에 반영되지 않으므로 별도로 차감해야 함

---

## 6. CFI 계산 (Direct)

- **PPE 취득**: Cash outflow (CAPEX)
- **PPE 처분**: Cash inflow = 처분 장부가 + 처분손익
- 감가상각누계액(Accumulated Depreciation) 감소 → 자산 처분 신호

---

## 7. CFF 계산 (Direct)

- **Bond 신규 발행**: CFF inflow
- **Capital Stock 감소** (유상감자·자사주 소각): CFF outflow
- **Dividend 지급**: `Dividend Declared - ΔDividend Payable` = Cash outflow

---

## 8. EBITDA와 CFO의 관계

$$\text{EBITDA} \approx \text{EBIT} + D\&A$$

- AR, AP, Inv가 서로 상쇄되거나 안정적인 경우 EBITDA ≈ CFO
- 단, **운전자본 변동이 큰 기업**은 EBITDA를 CFO 대용으로 사용하기 부적절

---

## 9. Working Capital 분석

- **운전자본 감소로 인한 CFO 증가** → ⚠️ Warning Sign
  - AR·Inv 감소 + AP 증가로 단기적으로 CFO를 높인 것
  - 영업으로 창출한 현금이 아니므로 **지속 불가능**

---

## 10. 기업 생애주기별 CF 패턴

| 단계 | CFO | CFI | CFF |
|------|-----|-----|-----|
| Early Stage | (−) | (−) | (+) |
| Growth | (+) | (−) | (+/−) |
| Mature | (+) | (−) | (−) |

- 초기 기업은 음(-)의 CFO를 외부 자금(채권·주식 발행)으로 충당
- 장기적으로 CFO > CAPEX를 달성해야 지속 가능

---

## 11. CFO vs EBIT

- **정상**: EBIT < CFO
- **주의**: EBIT > CFO → 이익은 났지만 현금이 들어오지 않은 상황
  - 수익 조기 인식 또는 비용 인식 지연 등 공격적 회계처리 가능성

---

## 12. Free Cash Flow

### FCFF (Free Cash Flow to the Firm)
채권자 + 주주 모두에게 귀속되는 현금

$$\text{FCFF} = \text{NI} + \text{NCC} - \Delta\text{Working Capital} + \text{Interest} \times (1 - t) - \text{CAPEX}$$

$$= \text{CFO} + \text{Interest} \times (1 - t) - \text{CAPEX}$$

### FCFE (Free Cash Flow to Equity)
주주에게 귀속되는 현금 (레버리지가 큰 기업에 주로 사용)

$$\text{FCFE} = \text{CFO} + \text{Net Borrowing} - \text{CAPEX}$$

> - **FCFF**: WACC(채권자 + 주주 가중평균수익률)로 할인
> - **FCFE**: COE(주주요구수익률)로 할인
