---
title: "CFA FSA Reading 33 — Analysis of Long-Term Assets"
date: 2026-04-06
categories: cfa
tags: [FSA, CFA Level I, Long-Term Assets]
---

## 1. Intangible Assets (무형자산)

물리적 실체가 없는 장기자산 (특허, 브랜드, 저작권 등)

- **유한한 수명** → 상각(Amortization) 적용
- **무한한 수명** → 상각 없음, 매년 손상검사(Impairment Test)

---

## 2. Identifiable vs Unidentifiable IA

### Identifiable IA 인식 요건
1. 분리 가능하거나 계약·법적 권리에서 발생
2. 기업이 통제 가능
3. 미래 경제적 효익이 기대됨

추가 요건:
- 원가를 신뢰성 있게 측정 가능
- 미래 경제적 효익의 유입이 개연성 있음

### Unidentifiable IA
- 별도로 구매 불가, 무한한 수명 가능
- 대표적 예시: **Goodwill**

$$\text{Goodwill} = \text{매수가격} - \text{순자산 공정가치(식별 가능 자산 − 부채)}$$

---

## 3. 내부 창출 무형자산 (Internally Created IA)

원칙적으로 **발생 시 비용처리(Expensed as Incurred)**

### IFRS
- **Research Cost**: 즉시 비용처리
- **Development Cost**: 요건 충족 시 **자본화 가능**

### US GAAP
- Research + Development 모두 원칙적으로 **즉시 비용처리**
- 예외: 자체 사용 또는 판매 목적 **소프트웨어 개발비** → 기술적 실현가능성(Technological Feasibility) 이후 자본화 가능

---

## 4. 외부 구매 무형자산 (Purchased IA)

- 유형자산과 동일하게 취득원가(공정가치)로 BS에 초기 인식
- **자본화 효과**:
  - 첫 해: NI 높음 (즉시 비용처리 대비)
  - 이후: NI 낮음 (상각비 발생)
  - CFO 감소, CFI 증가

---

## 5. 사업결합으로 취득한 IA (Business Combination)

| 항목 | 금액 |
|------|------|
| 매수가격 | 2,000 |
| 순자산 공정가치 (A−L) | (1,500) |
| 기존 미인식 식별 가능 무형자산 공정가치 | (200) |
| **Goodwill** | **300** |

---

## 6. Impairment (손상)

자산의 가치가 장부가 이하로 하락하는 것

### IFRS
- 매년 손상 징후 검토
- **손상 조건**: 장부가 > **회수가능액** (= Max(순공정가치, 사용가치))
- 손상차손 = 장부가 − 회수가능액 → IS 인식
- **손상차손 환입 가능** (단, 원래 손상차손 한도 내)

### US GAAP
**2단계 검사:**
1. **Recoverability Test**: 장부가 > 미래 미할인 CF → 손상
2. **Loss Measurement**: 손상차손 = 장부가 − 공정가치(또는 할인 CF)
- **손상차손 환입 불가**

---

## 7. Impairment의 재무제표 영향

| 항목 | 손상 당기 | 이후 기간 |
|------|-----------|-----------|
| Asset | ↓ | — |
| NI | ↓ | ↑ (D&A 감소) |
| ROA / ROE | ↓ | ↑ |
| Cash Flow | **영향 없음** | — |

> 손상은 과세소득을 줄이지 않으므로 CF에 영향 없음
> 손상 결정은 경영진의 주관적 판단이 개입 → **이익 조작 가능성** 존재

---

## 8. 무한수명 IA의 손상검사

- 상각 없이 **최소 연 1회** 손상검사
- 장부가 vs 공정가치 비교

---

## 9. Derecognition (제거)

장기자산을 BS에서 제거하는 경우: 매각, 교환, 폐기

$$\text{처분손익} = \text{매각대금} - \text{장부가(순장부가)}$$

IS의 기타손익(Other Gains and Losses)으로 보고

---

## 10. Spin-off

| 구분 | 내용 |
|------|------|
| **Spin-off** | 자산(사업부·자회사)을 새로운 법인으로 이전 후 주주에게 주식 배분 |
| 모회사 입장 | 해당 자산을 Held for Sale로 분류 후 제거 |
| 자회사 주식 | 모회사 APIC(자본잉여금)에서 차감 |

---

## 11. Long-Lived Asset 분석 지표

$$\text{Fixed Asset Turnover} = \frac{\text{Revenue}}{\text{Average Net Fixed Assets}}$$

$$\text{Average Age} = \frac{\text{Accumulated Depreciation}}{\text{Annual Depreciation Expense}}$$

$$\text{Total Useful Life} = \frac{\text{Historical Cost (Gross)}}{\text{Annual Depreciation Expense}}$$

$$\text{Remaining Useful Life} = \frac{\text{Ending Net PP\&E}}{\text{Annual Depreciation Expense}}$$

- Average Age가 높을수록 자산이 노후화 → 경쟁력 저하 가능성
- 향후 대규모 CAPEX 시점 및 자금 조달 필요성 추정에 활용
