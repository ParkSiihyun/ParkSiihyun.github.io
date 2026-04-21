---
title: "CFA Equity Reading 39 — Market Organization and Structure"
date: 2026-04-20
categories: cfa
tags: [Equity, CFA Level I, Market Structure]
---

## 1. Financial System

The financial system allows entities to **save, borrow, issue equity capital, manage risks, exchange assets, and to utilize information.**

→ 돈, 자산, 리스크, 정보 등을 거래할 수 있게 한다.

### Functions of the Financial System

| 기능 | 설명 |
|------|------|
| **Return Determination** | 차입(borrowing)과 저축(lending/saving)의 균형을 맞추는 수익률 결정 |
| **Allocation of Capital** | 제한된 자본을 가장 효율적인 용도로 배분 |

- Low rates of return → increase borrowing, reduce saving
- High rates of return → increase saving, reduce borrowing
- → **Equilibrium interest rate** 형성

---

## 2. Classification of Assets and Markets

### Asset 분류

| 구분 | 내용 |
|------|------|
| **Financial assets** | Securities (stocks/bonds), derivative contracts, currencies |
| **Real assets** | Real estate, equipment, commodities, physical assets |

### Financial Assets 세부 분류

| 종류 | 설명 |
|------|------|
| **Debt securities** | Promises to repay borrowed funds |
| **Equity securities** | Represent ownership positions |
| **Public securities** | 거래소에서 거래, 규제 대상 |
| **Private securities** | 공개 시장에서 거래 안 됨, 규제 없음 |
| **Derivative contracts** | 가치가 다른 자산(기초자산)에 의해 결정됨 |
| **Financial derivatives** | Equities, equity indexes, debt, debt indexes 기반 |
| **Physical derivatives** | Gold, oil, wheat 등 실물자산 기반 |

### Market 분류

| 구분 | 설명 |
|------|------|
| **Spot markets** | Markets for immediate delivery |
| **Forwards / Futures / Options** | Contracts for future delivery |
| **Primary market** | 신규 발행 증권 시장 |
| **Secondary market** | 기발행 증권의 유통 시장 |
| **Money market** | 만기 1년 이하 단기 채무 증권 |
| **Capital market** | 장기 채무 증권 및 주식 |
| **Traditional investment markets** | Debt and equity |
| **Alternative markets** | Hedge funds, commodities, real estate, collectibles |

---

## 3. Type of Assets

### Securities

**Equity securities**
- **Common stock** : residual claim of assets (보통주, 잔여청구권)
- **Preferred stock** : equity security with scheduled dividends (우선주)
- **Warrants** : the right to buy a firm's equity shares (신주인수권)

**Pooled investment vehicles (집합투자기구)**
- **Mutual funds** : open-end(펀드에서 직접 매수) / closed-end(2차 시장에서 거래)
- **ETF / ETN** : ETF는 실제 자산을 담음 / ETN은 운용사가 지정 인덱스 수익률을 보전해주겠다는 채권형 증권. 거래소에서 주식처럼 거래
  - *인덱스 펀드 vs ETF 차이*: 인덱스 펀드는 하루 한 번 가격 결정 / ETF는 주식처럼 실시간 거래
- **Asset backed securities** : 모기지, 자동차 대출 등 금융자산 풀에 대한 청구권
- **Hedge funds** : LP/GP 구조, 고액자산가 대상, 다양한 전략 활용

**Fixed income securities**
- **Bonds** : long term
- **Notes** : intermediate term
- **CP (Commercial Paper)** : short term debt issued by firm

**Contracts**
- Forward / Futures / Swap / Option / Insurance / Credit default swaps (CDS)

**Real Assets** : real estate, equipment, machinery

---

## 4. Financial Intermediaries

| 중개기관 | 역할 |
|----------|------|
| **Broker** | 매수/매도자를 매칭시켜 거래 체결 (장외에서) |
| **Block Broker** | 대량 주문 체결 지원 |
| **Dealer** | 자신의 재고로 직접 매수/매도하며 시장 조성 (Market Maker) |
| **Exchange 거래소** | 거래 플랫폼 제공 |
| **Securitizers** | 대량의 증권을 묶어 투자자에게 판매 |
| **Depository institution** | 예금금융기관 |
| **Arbitrageur 차익거래자** | 가격 차이를 이용한 무위험 수익 추구 |
| **Clearing house 청산소** | 결제 이행 보장 |
| **Custodians** | 예탁결제원 → 주식 보관 및 명의 이전 |
| **Investment banks** | 기업이 주식·채권을 발행해 투자자에게 매도하도록 지원 |

**Dealer 수익의 원천**: Bid price와 Ask price의 차이인 **Spread**

---

## 5. Position

| 포지션 | 설명 |
|--------|------|
| **Long position** | 현물 매수, 선물/옵션 매수 → 자산 가격 상승 시 이익 |
| **Short position** | Shortsale, 선물/옵션 매도 → 자산 가격 하락 시 이익 |

### Short Sale (공매도)

- 주식을 브로커를 통해 빌려서 매도
- 가격이 떨어지면 더 낮은 가격에서 사서 갚는 방식으로 수익 실현
- 빌린 기간 동안 발생한 Dividends/Interest는 주식 lender에게 귀속
- 주식을 빌리기 위해서는 **collateral** 예치 필요

### Margin Transaction (신용거래)

- **돈을 빌려서 주식을 사는 것** → 가격 오르면 더 비싼 가격에 팔아 갚음
- **Initial margin (개시증거금)**: 마진거래 개시 시점의 필요 자본 비율
- **Maintenance margin (유지증거금)**: 거래 중 유지해야 할 자본 비율, 미달 시 margin call 발생

#### Margin Transaction Example

| 항목 | 내용 |
|------|------|
| Shares purchased | 1,000주 |
| Purchase price | $100/주 → 총 $100,000 |
| Initial margin | 40% → 내 자본(E) $40,000, 빌린 돈(D) $60,000 |
| Annual dividend | $2/주 |
| Call money rate | 4% |
| Commission | $0.05/주 |
| Stock price after 1 year | $110 |

$$\text{Leverage Ratio} = \frac{\$100{,}000}{\$40{,}000} = 2.5$$

$$\text{투자자 수익률} = \frac{\$110{,}000 + \$2{,}000 - \$2{,}400 - \$60{,}000}{\$40{,}000 + \$50} \approx 23.7\%$$

#### Margin Call Price Example

> $40에 1주 매수, initial margin 50%, maintenance margin 25%일 때 margin call 가격은?

- 초기 내 자본 $20 (50%)
- 현재 주가 x로 가정 → Equity = x - 20, Maintenance margin = x × 25%
- 방정식: x - 20 = 0.25x → 0.75x = 20 → **x = $26.67**

---

## 6. Execution / Validity / Clearing

### Order 유형 (Execution)

| 주문 유형 | 설명 |
|-----------|------|
| **Market order (시장가 주문)** | 즉시 체결, 최우선 가격 적용, 원하지 않는 가격에 체결될 우려 |
| **Limit order (지정가 주문)** | 지정 가격 이하(매수) / 이상(매도)에만 체결, 미체결 가능성 있음 |
| **Hidden order** | 다른 시장 참여자에게 수량이 보이지 않는 주문 |
| **Ice berg order** | 일부 수량만 공개되는 주문 (대량 주문 시 시장 영향 최소화) |

### Validity (언제 주문이 이루어지나)

| 유형 | 설명 |
|------|------|
| **Day order** | 하루 지나면 무효 |
| **GTC (Good till cancelled)** | 취소 전까지 유효 |
| **IOC (Immediate or cancel)** | 즉시 체결 안 되면 취소 |
| **Good on close** | 종가 주문 |
| **Market on close** | 종가를 시장가로 주문 |
| **Stop orders** | 공매도 시 Stop-buy (가격 상승 손실 방지) / 롱포지션에서 Stop-sell (가격 하락 손실 방지) |

### Clearing (언제 정산되나)

- Retail trades are typically cleared and settled by the broker

---

## 7. Primary vs Secondary Capital Market

| 구분 | 설명 |
|------|------|
| **Primary capital market** | 신규 발행 증권 매각 (IPO, seasoned offerings) |
| **Secondary financial market** | 이미 발행된 증권의 거래 |

### Public Offerings (IPO)

- **Underwritten offering**: 투자은행이 전체 발행을 매입 보장 → 미매각분은 IB가 인수
- **Best efforts**: 미매각분에 대해 IB 인수 의무 없음

### Private placements

: 투자자에게 직접 증권 매도, 보통 IB 주선

---

## 8. Market Structures

| 구조 | 설명 |
|------|------|
| **Call market** | 특정 시간에만 거래 체결 (종가조작 방지 목적) |
| **Continuous market** | 시장 개장 중 언제든지 거래 (장중거래) |
| **Quote Driven Market** | 딜러(Market Maker)들끼리 Bid/Ask를 제시하며 거래 (OTC, Dealer Market) |
| **Order Driven Market** | 거래소 기반, 주문 매칭 규칙 적용 (Highest bid & Lowest ask 우선) |
| **Brokered Market** | 자산이 매우 비유동적이거나 특이해 브로커가 상대방을 찾아야 하는 거래 |

---

## 9. Characteristics of Well-Functioning Financial System

| 효율성 종류 | 설명 |
|-------------|------|
| **Operational efficiency** | Low trading cost (낮은 거래비용) |
| **Informational efficiency** | 정보가 Price에 모두 반영되어 있는가 |
| **Allocational efficiency** | 투자자 효용이 극대화되도록 자원이 배분되었는가 |
