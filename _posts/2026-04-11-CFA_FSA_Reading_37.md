---
title: "CFA FSA Reading 37 — Financial Analysis Techniques"
date: 2026-04-11
categories: cfa
tags: [FSA, CFA Level I, Ratios, Analysis]
---

## 1. Activity Ratios (활동성 지표)

### Receivables Turnover & DSO

$$\text{Receivables Turnover} = \frac{\text{Annual Sales}}{\text{Average Receivables}}$$

$$\text{DSO (Days Sales Outstanding)} = \frac{365}{\text{Receivables Turnover}}$$

- Turnover 높음 → 신용 관리 우수 **or** 신용 조건이 지나치게 엄격해 매출 손실 가능

### Inventory Turnover & DOH

$$\text{Inventory Turnover} = \frac{\text{COGS}}{\text{Average Inventory}}$$

$$\text{DOH (Days of Inventory on Hand)} = \frac{365}{\text{Inventory Turnover}}$$

- Turnover 높음 → 재고 관리 효율적 **or** 재고 부족으로 판매 기회 손실 가능

### Payables Turnover & DPO

$$\text{Payables Turnover} = \frac{\text{Purchases}}{\text{Average Payables}}$$

$$\text{Purchases} = \text{Ending Inventory} - \text{Beginning Inventory} + \text{COGS}$$

$$\text{DPO (Days Payable Outstanding)} = \frac{365}{\text{Payables Turnover}}$$

### Asset Turnover

$$\text{Total Asset Turnover} = \frac{\text{Revenue}}{\text{Average Total Assets}}$$

$$\text{Fixed Asset Turnover} = \frac{\text{Revenue}}{\text{Average Net Fixed Assets}}$$

- Turnover 높을수록 자산을 효율적으로 활용
- 단, 노후 자산으로 인해 Turnover가 높을 수도 있으므로 맥락 파악 필요

---

## 2. Liquidity Ratios (유동성 지표)

$$\text{Current Ratio} = \frac{CA}{CL}$$

$$\text{Quick Ratio} = \frac{CA - Inventory}{CL}$$

$$\text{Cash Ratio} = \frac{\text{Cash} + \text{Marketable Securities}}{CL}$$

- Current Ratio < 1 → 음(−)의 Working Capital → 유동성 위기 가능
- Current Ratio가 높을수록 단기 채무 상환 능력 우수

### Cash Conversion Cycle (CCC)

$$\text{CCC} = \text{DOH} + \text{DSO} - \text{DPO}$$

- CCC가 낮을수록 현금 회수 속도 빠름 → 양호
- CCC가 너무 높으면 유동성 지속적 악화 가능

---

## 3. Solvency Ratios (안정성 지표)

> **Total Debt** = 이자부담 부채(Interest-bearing debt)

$$\text{Debt-to-Equity} = \frac{\text{Total Debt}}{\text{Total Shareholders' Equity}}$$

$$\text{Debt-to-Capital} = \frac{\text{Total Debt}}{\text{Total Debt} + \text{Total SH's Equity}}$$

$$\text{Debt-to-Asset} = \frac{\text{Total Debt}}{\text{Total Assets}}$$

$$\text{Financial Leverage} = \frac{\text{Average Total Assets}}{\text{Average Total Equity}}$$

$$\text{Interest Coverage} = \frac{\text{EBIT}}{\text{Interest Payments}}$$

$$\text{Debt-to-EBITDA} = \frac{\text{Total Debt}}{\text{EBITDA}}$$

- Interest Coverage 낮을수록 채무 상환 어려움
- Debt-to-EBITDA: 현재 총부채를 CFO 근사치로 상환하는 데 걸리는 기간

### Financial Leverage 효과
부채를 사용할수록 EBIT 변동이 NI에 더 크게 반영됨

> 예) EBIT $100, 이자 $80 → NI $20  
> EBIT가 $120이 되면 NI는 $40으로 **100% 증가** (EBIT 증가율 20% 대비)  
> → 부채 없는 경우: NI $100 → $120으로 **20% 증가**에 그침

---

## 4. Profitability Ratios (수익성 지표)

$$\text{Gross Profit Margin} = \frac{\text{Gross Profit}}{\text{Revenue}}$$

$$\text{Operating Profit Margin} = \frac{\text{EBIT}}{\text{Revenue}}$$

$$\text{Pretax Margin} = \frac{\text{Pretax Income}}{\text{Revenue}}$$

$$\text{Net Profit Margin} = \frac{\text{NI}}{\text{Revenue}}$$

$$\text{ROA} = \frac{\text{NI}}{\text{Average Total Assets}}$$

$$\text{ROIC} = \frac{\text{NOPAT}}{\text{Average Long-term Capital}}$$

> **NOPAT** = EBIT × (1 − Tax Rate)  
> **Long-term Capital (Invested Capital)** = Total Assets − Operating Liabilities  
> ROIC는 채권자+주주의 자본(분모)에 채권자+주주의 이익(분자)을 대응 → ROA보다 정확한 수익성 지표

---

## 5. ROE — DuPont Analysis

### 3-Factor DuPont

$$\text{ROE} = \text{Net Profit Margin} \times \text{Total Asset Turnover} \times \text{Financial Leverage}$$

$$= \frac{\text{NI}}{\text{Revenue}} \times \frac{\text{Revenue}}{\text{Avg. Total Assets}} \times \frac{\text{Avg. Total Assets}}{\text{Avg. SH's Equity}}$$

### 5-Factor DuPont

$$\text{ROE} = \text{Tax Burden} \times \text{Interest Burden} \times \text{EBIT Margin} \times \text{Asset Turnover} \times \text{Financial Leverage}$$

| Factor | 계산식 |
|--------|--------|
| Tax Burden | NI / EBT (= 1 − 실효세율) |
| Interest Burden | EBT / EBIT |
| EBIT Margin | EBIT / Revenue |
| Asset Turnover | Revenue / Avg. Total Assets |
| Financial Leverage | Avg. Total Assets / Avg. SH's Equity |

### DuPont 분석의 유용성

ROE가 일정하게 유지되더라도 내부 구성 요소가 변하고 있을 수 있음

예) Net Profit Margin은 계속 하락하는데 Financial Leverage가 증가하면서 ROE를 유지하는 경우:
- 기업 리스크 증가 → COE(주주요구수익률) 상승 → **주가 하락**
- 주식 가치 = 미래 수익 / COE or WACC → Cost of Capital 증가는 주가에 부정적
