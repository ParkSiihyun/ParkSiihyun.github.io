---
title: "CFA FSA Reading 29 — Analyzing Balance Sheets"
date: 2026-04-03
categories: cfa
tags: [FSA, CFA Level I]
---

## 1. Balance Sheet 개요

Balance Sheet(BS)는 **특정 시점**의 자산, 부채, 자본을 보여주는 재무제표.

- **Cash**: 유동성이 가장 높은 자산
- **AR (Accounts Receivable)**: 아직 현금으로 회수되지 않은 매출채권
- **Inventory**: 재고자산 — 신용 조건(Credit Terms)에 따라 규모가 달라짐
- **CAPEX(자본지출)** 및 이자 지급은 Cash에 직접 영향

> BS는 과거 거래의 누적 결과를 보여주므로, IS(손익계산서)와 함께 분석해야 전체 그림이 보임

---

## 2. Common-Size Balance Sheet

각 항목을 **총자산(Total Assets) 대비 비율(%)**로 표시:

- 기업 간 규모 차이를 제거하여 **비교 분석**에 유용
- 연도별 자산 구성 변화 추이 파악 가능

---

## 3. Accounting of Financial Instruments

금융자산(Financial Assets)의 분류 및 측정 방법:

### HTM (Held-to-Maturity)

- **만기 보유 목적**의 채무증권
- **Amortized Cost(상각후원가)**로 측정

$$\text{Amortized Cost} = \text{발행가} - \text{원금 상환액} + \text{할인액 상각} - \text{할증액 상각} - \text{손상차손}$$

- 시장금리 변동에 따른 공정가치 변동을 BS에 반영하지 않음

---

### HFT (Held for Trading Securities)

- **단기 매매 목적**의 증권 (채권, 주식, 파생상품 등)
- BS에 **공정가치(Fair Value)**로 보고
- **미실현손익(Unrealized G/L)** → **IS에 반영** (당기손익)

---

### AFS (Available for Sale Securities)

- 만기 보유도 단기 매매도 아닌 증권
- BS에 **공정가치**로 보고 (HFT와 동일)
- **미실현손익** → **IS가 아닌 OCI(기타포괄손익)에 반영**

> US GAAP과 IFRS 간 세부 처리 방식에 차이 있음 (→ Level 2에서 심화)

---

### 분류 요약

| 구분 | 측정 방법 | 미실현손익 반영 위치 |
|------|-----------|----------------------|
| HTM | Amortized Cost | 반영 안 함 |
| HFT | Fair Value | IS (당기손익) |
| AFS | Fair Value | OCI (기타포괄손익) |
