# Reading 32 — Analysis of Inventories

---

## 1. Inventory 회계 방법

| 방법 | COGS | Inventory (BS) | Net Income |
|------|------|----------------|------------|
| **FIFO** (First In, First Out) | 낮음 | 높음 | 높음 |
| **LIFO** (Last In, Last Out) | 높음 | 낮음 | 낮음 |

> - FIFO: IFRS + US GAAP 모두 허용
> - LIFO: **US GAAP만 허용** (IFRS 불허)

---

## 2. Inventory Measurement (재고자산 측정)

### FIFO (IFRS & US GAAP 공통)

BS에 **Lower of Cost or NRV(Net Realizable Value)**로 보고

$$\text{NRV} = \text{예상 판매가} - \text{예상 판매비용} - \text{완성원가}$$

- NRV < 장부가 → **재고자산 Write-down** (손실을 COGS에 가산)
- 이후 가치 회복 시 **Write-up 가능** → **IFRS만 허용**, US GAAP 불허

### LIFO (US GAAP만 허용)

BS에 **Lower of Cost or Market**으로 보고

| 조건 | Market 기준 |
|------|-------------|
| NRV − 정상이익 < Replacement Cost < NRV | Replacement Cost |
| Replacement Cost > NRV | NRV |
| Replacement Cost < NRV − 정상이익 | NRV − 정상이익 |

> LIFO는 재고 장부가가 낮기 때문에 Write-down 발생 가능성이 낮음

---

## 3. Inflation 환경에서 FIFO vs LIFO 비교

| 항목 | FIFO | LIFO |
|------|------|------|
| COGS | 낮음 | 높음 |
| Net Income | 높음 | 낮음 |
| Tax | 높음 | 낮음 |
| Cash Flow | 낮음 | **높음** |
| Inventory (BS) | 높음 | 낮음 |
| Current Ratio | 높음 | 낮음 |
| Working Capital | 높음 | 낮음 |

> 물가 하락 시 효과 반전

---

## 4. Inventory Write-down의 재무제표 영향

| 항목 | 영향 |
|------|------|
| Inventory (CA) | ↓ |
| Current Ratio (CA/CL) | ↓ |
| Quick Ratio | **변화 없음** (Inv 제외) |
| Inventory Turnover (COGS/Avg Inv) | ↑ (COGS↑, Inv↓) |
| Total Asset Turnover (Rev/TA) | ↑ |
| Debt-to-Asset Ratio | ↑ |
| Debt-to-Equity Ratio | ↑ (NI↓ → Equity↓) |
| Gross/Operating/Net Margin | ↓ |
| ROA / ROE | 당기 ↓, **이후 기간 ↑** (D&A 감소 효과) |
| Cash Flow | **영향 없음** (세금 감소 효과 없음) |

---

## 5. LIFO Liquidation

LIFO 기업의 **재고 수량이 감소**할 때 발생:

- 오래된 저원가 재고가 COGS로 인식됨 → COGS 급감
- → Profit Margin 및 세금 일시적 증가
- **Non-recurring, 지속 불가능한 이익** → Analyst 주의 필요

---

## 6. LIFO Reserve

$$\text{LIFO Reserve} = \text{Inventory (FIFO)} - \text{Inventory (LIFO)}$$

- LIFO 기업을 FIFO 기준으로 비교 분석할 때 사용
- IFRS는 LIFO 불허이므로 LIFO Reserve 개념 없음

---

## 7. Inventory 구성 분석

| 항목 | 시사점 |
|------|--------|
| Raw Materials 증가 | 수요 증가 예상 |
| Finished Goods 증가 | 수요 감소 / 판매 부진 가능성 → Write-down 위험 |
| 과도한 재고 보유 | 보관비용·보험료·재고세 발생, 현금 비효율 |

---

## 8. 주요 재고 관련 지표

$$\text{Inventory Turnover} = \frac{\text{COGS}}{\text{Average Inventory}}$$

$$\text{Days of Inventory on Hand (DOH)} = \frac{365}{\text{Inventory Turnover}}$$

- DOH가 높을수록 재고가 오래 쌓여 있다는 의미
- 업종 평균과 비교하여 재고 관리 효율성 판단
