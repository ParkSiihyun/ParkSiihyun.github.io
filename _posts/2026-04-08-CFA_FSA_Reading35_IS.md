# Reading 35 — Analyzing Income Statements

---

## 1. Revenue Recognition 기본 개념

### AR (Accounts Receivable)
- 현금 판매: 즉시 수익 인식
- 신용 판매: 판매 시점에 수익 인식 + BS에 AR 생성
- IS에는 반품·할인 차감 후 **순매출(Net Revenue)**으로 보고
  - 예) 예상 품질보증비, 고객 할인

### Unearned Revenue (선수수익)
- 재화·용역 이전 전에 현금 수령 시 → **부채(Unearned Revenue)** 인식
- 재화·용역 이전 시 → 수익 인식

---

## 2. Revenue Recognition 5단계 (IFRS & US GAAP 통합 기준)

| 단계 | 내용 |
|------|------|
| **1단계** | 고객과의 계약 식별 (수금 가능성: IFRS 50%↑, US GAAP 80%↑) |
| **2단계** | 계약 내 수행의무(Performance Obligation) 식별 |
| **3단계** | 거래가격 결정 (고정 or 변동) |
| **4단계** | 거래가격을 수행의무에 배분 |
| **5단계** | 수행의무 이행 시 수익 인식 |

> 수익은 **환입 가능성이 매우 낮을 때만** 인식

---

## 3. 수익 인식 시점: Over Time vs At a Point in Time

### Over Time 인식 조건 (아래 중 하나 해당 시)
- 고객이 이행 과정에서 동시에 효익을 수취
  - 예) 서비스·유지보수 계약, 청소 용역
- 공급자가 고객이 통제하는 자산을 창출·강화
- 자산이 공급자에게 대체적 용도가 없고, 이행 완료분에 대한 지급 청구권 보유
  - 예) 고객 맞춤형 설비 제작, 건설 계약

### At a Point in Time
- 위 조건 미충족 시

---

## 4. Revenue Recognition 예시

### 건설 계약 (Over Time — Input Method)

> 계약금액 $10M, 총 예상원가 $8M

| 연도 | 투입원가 | 진행률 | 인식 수익 | 인식 이익 |
|------|---------|-------|---------|---------|
| Y1 | $4M | 50% | $5M | $1M |
| Y2 | $2M | 75% | $2.5M | $0.5M |
| Y3 | $2M | 100% | $2.5M | $0.5M |

### Principal vs Agent

| 구분 | 수익 인식 | Gross Margin |
|------|---------|--------------|
| **Principal** | 총 판매금액 (Gross) | 낮음 (10%) |
| **Agent** | 수수료만 (Net) | 높음 (100%) |

> Agent는 재화를 직접 제공하지 않고, 재고 리스크·신용 리스크를 부담하지 않음

---

## 5. 특수 수익 인식 케이스

### Franchising & Licensing (예: McDonald's)
| 수익 유형 | 인식 방법 |
|---------|---------|
| 초기 가맹비 | Over Time |
| 로열티 | Over Time |
| 가맹점 공급 물품 (설비·식재료) | At a Point in Time |

### Software License
- 설치 후 업데이트·개선이 계약에 포함 → **Over Time**
- 업데이트 없이 단순 라이선스만 → **At a Point in Time**

### Bill and Hold
- 구매자 요청으로 판매자가 물건을 보관하는 경우
- 통제권 이전 요건 충족 시 수익 인식 가능

---

## 6. Expense Recognition

### Matching Principle (대응 원칙)
수익 창출에 기여한 비용은 해당 수익과 **같은 기간**에 인식

### Capitalized Interest (자본화 이자)
- 자산 건설 기간 중 발생한 이자 → 자산 원가에 포함(자본화)
- 자산 완공 후 감가상각을 통해 비용화 → Matching Principle 충족

**CF 처리 시 조정:**

| 항목 | 조정 전 | 조정 후 |
|------|---------|---------|
| CFO | 과대 | 감소 (자본화 이자만큼 차감) |
| CFI | 과소 | 증가 (자본화 이자만큼 가산) |

---

## 7. Nonrecurring Items

비반복적 항목 — 영업이익(EBIT) 위에 포함, **세전(Pre-tax)** 보고

예) 자산 처분 손익, 손상차손, Write-off

```
Revenue
- Operating Expenses
= EBIT
± Non-operating Items
= Pre-tax Income
- Income Tax
= Net Income
```

---

## 8. Discontinued Operations (중단영업)

경영진이 처분을 결정했거나 당기 중 처분한 사업 부문

- **세후(After-tax)** 기준으로 IS 하단에 별도 표시
- Phaseout Period(측정일 ~ 실제 처분일) 동안의 손익 포함

---

## 9. Changes in Accounting Policies & Estimates

| 변경 유형 | 적용 방법 | 과거 재무제표 수정 |
|---------|---------|----------------|
| **회계정책 변경** (기준서 변경) | 소급 적용 (Retrospective) | O |
| **회계추정 변경** (경영진 결정, 예: 내용연수) | 전진 적용 (Prospective) | X |
| **오류 수정** | 소급 적용 | O |
| **수정 소급 적용** | 기초잔액 조정 | X (과거 재무제표 수정 없음) |

> 회계정책·오류 수정은 비교가능성 향상을 위해 소급 적용  
> CF에는 일반적으로 영향 없음

---

## 10. EPS (Earnings Per Share)

### Basic EPS

$$\text{Basic EPS} = \frac{\text{NI} - \text{Preferred Dividends}}{\text{Weighted Average Common Shares Outstanding}}$$

### Weighted Average Shares 계산 주의사항
- 주식 수는 **보유 기간 비율**로 가중
- **자사주(Treasury Stock)**: 발행주식에서 차감
- **주식배당·주식분할**: **연초 소급 적용** (연중 발생해도)

### Diluted EPS (DEPS)

희석 증권 (Convertible Bond, Convertible Preferred Stock, Stock Option, Warrant) 존재 시

**Method 1 — If-Converted Method** (CB, 전환우선주)

$$\text{DEPS} = \frac{\text{NI} + \text{이자비용} \times (1-t)}{\text{기본 주식수} + \text{전환 시 발행 주식수}}$$

> 전환우선주: 분자에서 우선배당 제거, 분모에 전환 주식수 추가  
> DEPS > BEPS이면 **Anti-dilutive** → DEPS = BEPS로 보고

**Method 2 — Treasury Stock Method** (Stock Option, Warrant)

$$\text{순증가 주식수} = \text{행사 주식수} - \frac{\text{행사가} \times \text{행사 주식수}}{\text{시장가}}$$

> 행사로 들어온 현금으로 시장가에 자사주 매입한다고 가정  
> NI 변동 없음 (현금 유입이 IS에 영향 없으므로)

### Common-Size I/S
각 항목을 **Revenue 대비 비율(%)**로 표시
