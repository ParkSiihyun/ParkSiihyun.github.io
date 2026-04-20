# Reading 35 — Analysis of Income Taxes

---

## 1. 핵심 용어 정리

| 용어 | 정의 |
|------|------|
| **Taxable Income** | 세법상 과세소득 |
| **Taxes Payable** | 과세소득 × 현행 세율 = Current Tax Expense |
| **Income Tax Expense** | Current Tax Expense + Deferred Tax Expense |
| **Tax Loss Carryforward** | 현재·과거 손실을 미래 과세소득에서 차감 가능 → DTA 인식 |

---

## 2. 회계이익 vs 과세소득의 차이

```
IS (회계)                     세무
Revenue     → Taxable Amount
(Expense)   → Deductible Amount
─────────────────────────────
Pretax Income   →   Taxable Income
× 회계 세율       × 법정 세율(Statutory Rate)
= Tax Expense    = Current Tax Expense (Taxes Payable)
```

> 회계이익과 과세소득의 차이 → **Reconciliation** 필요

---

## 3. Temporary vs Permanent Difference

### Temporary Difference (일시적 차이)
- F/S와 세무상 처리 시점 차이 → **미래에 반전(Reverse)**됨
- → **DTL 또는 DTA** 발생

예시:
- 감가상각: 회계는 정액법, 세무는 가속상각 → 초기 DTL
- Unearned Revenue: 세무상 먼저 과세 → DTA
- Warranty: 세무상 실제 지출 시 비용 인정 → DTA
- Bad Debt: 세무상 실제 대손 시 공제 → DTA

### Permanent Difference (영구적 차이)
- 반전되지 않음 → **DTL/DTA 발생 없음**
- Effective Tax Rate ≠ Statutory Tax Rate의 원인

---

## 4. DTL vs DTA

| 구분 | 발생 원인 | 의미 |
|------|---------|------|
| **DTL** (Deferred Tax Liability) | 회계이익 > 과세소득 (세금 나중에 납부) | 미래에 세금 더 낼 것 |
| **DTA** (Deferred Tax Asset) | 회계이익 < 과세소득 (세금 미리 납부) | 미래에 세금 덜 낼 것 |

$$\text{Income Tax Expense} = \text{Current Tax Expense} + \Delta\text{DTL} - \Delta\text{DTA}$$

---

## 5. 세율 적용 원칙

| 항목 | 적용 세율 |
|------|---------|
| Current Tax Expense | **현행 법정 세율 (Current Statutory Rate)** |
| Deferred Tax Expense | **미래 예상 세율 (Future Tax Rate)** |

> Deferred Tax는 **누적된 Temporary Difference** 전체에 미래 세율을 적용하여 계산

**미래 세율 변화의 영향:**
- 세율 ↑ → DTL 부담 증가, DTA 가치 증가
- 세율 ↓ → DTL 부담 감소, DTA 가치 감소

---

## 6. Tax Loss Carryforward와 DTA

- 당기 순영업손실(NOL)을 미래 과세소득에서 차감 가능 → **DTA 인식**
- 적자가 누적된 기업일수록 DTA가 많이 쌓임 → 미래 절세 효과 큼

---

## 7. Realizability of DTA (DTA 실현가능성)

DTA는 "미래에 세금을 덜 낼 것"이라는 의미이지, 납세 능력을 보장하지 않음

- DTA 실현가능성이 낮다고 판단될 경우 → **Valuation Allowance** 설정
- Valuation Allowance 만큼 R/E(이익잉여금) 감소

```
DTA              1,000
Valuation Allowance  (500)   ← 실현 불확실 부분
Net DTA            500
```

---

## 8. Reverse 가능성이 낮은 DTL

예) 지분법 회계: 자회사 이익 발생 시 모회사가 지분법이익 인식 → DTL 발생  
→ 자회사가 배당 계획이 없고 CAPEX에만 집중한다면 DTL이 반전될 가능성 낮음  
→ 이런 DTL은 실질적으로 부채가 아닌 Equity로 볼 수 있음

---

## 9. 계산 예시

### Example 1 — 기본 구조

> Y1, Y2 모두 세전이익 $10,000 / 세율 20% / Y1에 일시적 차이 +$2,000 발생

**Y1:**
- CTE = (10,000 + 2,000) × 20% = **$2,400**
- DTE = −(2,000 × 20%) = **−$400** (DTL 증가)
- Tax Expense = $2,000

**Y2:**
- CTE = (10,000 − 2,000) × 20% = **$1,600**
- DTE = +(2,000 × 20%) = **+$400** (DTL 감소)
- Tax Expense = $2,000

---

### Example 2 — Permanent + Temporary Difference 혼재

> Pretax Income $1,000 / Temporary Difference $200 / Permanent Difference $100(−)  
> Y1 세율 40%, Y2 세율 30%

**Case 1 — Permanent Difference만 있는 경우:**
- CTE = (1,000 + 200 − 100) × 40% = $440
- DTE = −(200 × 40%) = −$80
- **Tax Expense = $360**, Effective Tax Rate = 36%

**Case 2 — Temporary $200, 세율 Y1→Y2 변경:**
- CTE = (1,000 − 200) × 40% = $320
- DTE = 200 × **30%** (미래 세율 적용) = $60
- **Tax Expense = $380**, Effective Tax Rate = 38%
