---
title: "CFA Derivatives Topic 3 - Pricing and Valuation of Futures Contracts"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Futures, Margin, Marking to Market, Interest Rate Futures]
---

## 1. 선물계약 futures contracts

선물계약은 미래의 특정 시점에 특정 기초자산을 미리 정한 가격으로 매매하기로 약정하는 계약이다.

정의는 선도계약과 동일하다. 다만 거래조건, 즉 기초자산과 만기일 등을 규격화한 후 거래소에 상장시켜 거래한다.

## 2. 선물계약과 선도계약 비교

### 공통점

- Settlement는 physical delivery 또는 cash settlement 가능
- 계약시점의 파생상품 가치 = 0

### 차이점

| 구분 | 선물계약 |
|---|---|
| 거래방법, 거래단위, 만기일 | 표준화 |
| 거래장소 | 규정된 거래소 |
| 이행보증 | 청산소 clearing house |
| 증거금 | 존재 |
| 정산 | 일일정산 |
| 거래상대방 위험 | No counterparty risk |

선도거래는 일반적으로 선도계약 종료일에 정산한다.

## 3. 선물계약의 주요 특성

### 1) 거래소 exchange

선물거래가 이루어지는 정형화되고 조직화되고 규격화된 시장이다.

- 거래 시간
- 기초자산
- 거래방법
- 일정한 자격을 갖춘 회원
- 일정한 규칙 아래 매매

### 2) 청산소 clearing house

청산소는 모든 선물거래의 상대방이 됨으로써 선물거래의 이행을 보증하고, 선물거래의 손익을 정산해주는 기관이다.

- 거래소와 별도 기관으로 설치될 수 있음
- 거래소 기구의 일부로 설치될 수 있음
- 선물거래는 청산소의 이행보증으로 인해 no counterparty risk

### 3) Novation

Novation은 사적 계약을 거래소와의 계약으로 갱신하는 것이다.

Bilateral OTC market에서 거래상대방 간 계약을 거래소 또는 CCP와의 계약으로 바꾸어 netting과 clearing을 가능하게 한다.

### 4) 정산가격 settlement price

정산가격은 선물계약 만기일에 선물계약을 정산할 때 사용하는 현물가격이다.

| 포지션 | Payoff |
|---|---|
| Long position | ST - futures price |
| Short position | futures price - ST |

ST는 선물계약 만기일의 현물자산 종가, 즉 settlement price이다.

만기일 정산 시 단순히 종가를 사용하면 종가 조작 우려가 있다. 그래서 만기일 이전 일정 기간의 평균 또는 거래량 가중평균 가격을 사용하기도 한다.

### 5) Offsetting or reverse trade

- 선도계약은 만기까지 가는 것이 일반적
- 선물계약은 만기에 정산하지 않고 offsetting trade로 거래를 청산할 수 있음
- Offsetting trade는 만기 이전에 처음 선물거래 포지션과 반대 포지션의 거래를 통해 최초 선물거래를 청산하는 것

### 6) 선물시장 참여자

| 참여자 | 내용 |
|---|---|
| Hedgers | 현물가격의 가격 변동위험을 관리하기 위해 선물시장에 참여 |
| Speculators | 현물을 보유하지 않은 상태에서 선물시장에만 참여. 선물가격의 방향성에 betting |

### 7) Daily settlement, marking to market

Daily settlement는 선물가격 변화에 의한 손익을 매일매일 정산하여 증거금계좌에 반영하는 것이다.

- 증거금 계좌 = margin account
- Daily settlement와 marking to market을 같은 용어로 혼용하기도 한다.

### 8) Margin account 증거금 제도

증거금은 선물계약 당사자가 계약을 이행하지 않을 위험에 대비하기 위해 거래소가 징수하는 계약이행 보증금이다.

| 용어 | 내용 |
|---|---|
| Initial margin | 선물거래를 시작하기 위해 납부해야 하는 증거금. 비용이 아니라 판돈 |
| Maintenance margin | 거래를 지속하기 위해 반드시 유지해야 하는 증거금 |
| Variation margin | 증거금이 maintenance margin 이하로 감소했을 때 initial margin 수준으로 올리도록 요구되는 추가 증거금 |
| Margin call | Variation margin 납부 요구 |

### 9) Price limits

거래소에서 부과하는 선물계약의 일일 가격 변동 한도이다.

| 용어 | 내용 |
|---|---|
| Limit up | 일일 변동할 수 있는 상한 가격 |
| Limit down | 일일 변동할 수 있는 하한 가격 |
| Limit move | 상한 가격과 하한 가격 사이의 제한된 움직임 |

### 10) CCP central counterparty

CCP는 forwards, swaps와 같은 OTC 거래에서 거래상대방 간 정산업무를 수행하도록 지정한 기관이다.

- OTC 거래에서 거래소 또는 청산소와 유사한 역할 수행
- 2008 금융위기 이후 OTC 거래에서 counterparty risk를 통제하기 위해 증거금을 쓰는 경우가 많아짐
- CCP가 이 증거금을 관리하는 것이 일반적
- CCP는 청산소의 특별한 한 종류
- 거래상대방 사이에 끼어들어 거래가 원활하게 진행되도록 관리
- 과거 OTC에는 CCP가 없었지만 현대 OTC에는 CCP가 존재하는 경우가 많음

## 4. Margin 예시

5월물 금 선물 1계약을 매수한다.

| 항목 | 값 |
|---|---|
| 선물 1계약 | 100 ounce |
| Futures contract price | $1,950 / ounce |
| Initial margin | $5,000 |
| Maintenance margin | $4,700 |

### Day 0

Initial margin $5,000을 납입해야 선물거래를 시작할 수 있다.

### Day 1

Gold settlement가 $2.5 / ounce 하락한다.

$$Daily\ Settlement=100\ ounce\times(-2.5)=-\$250$$

Ending margin account = $5,000 - $250 = $4,750.

Maintenance margin보다 높다.

### Day 2

Gold settlement가 다시 $2.5 / ounce 하락한다.

$$Daily\ Settlement=100\ ounce\times(-2.5)=-\$250$$

Ending margin balance = $4,750 - $250 = $4,500.

Maintenance margin보다 낮다.

Margin call이 발생한다.

$$Variation\ Margin=\$5,000-\$4,500=\$500$$

Variation margin은 initial margin까지 다시 채우는 금액이다.

## 5. Margin에 대해서

Repo나 주식 대차거래에서의 margin과는 다르다.

예시에서 금 선물 1계약은 100 ounce이고, 선물가격은 ounce당 $1,950이다.

실제로 선물계약을 통해 얻는 손익은 $1,950에서 변하는 가격 변동량 × 100 ounce이다.

하루에 ounce당 $2가 오르면 이익은 $200이다.

| 시점 | 내용 |
|---|---|
| Day 0 | Gold futures long, 1950 진입, 계약 크기 100 oz |
| Day 1 | 종가 1952 |
| 상승폭 | 1952 - 1950 = 2 |
| 계약당 손익 | 2 × 100 = +200 |

Margin account에 +200이 들어온다.

핵심은 경제적으로 포지션 기준가격이 1952로 reset된 것과 거의 같다는 점이다.

- 1950에서 1952 상승분은 이미 현금으로 받았기 때문
- 다음날 가격 변동폭에 의해 또 일일정산
- 포지션 기준가격이 변동되는 것처럼 보임
- 계약상 변동되는 것은 아니지만 전날 종가에서의 변동분만큼 일일정산되므로 그렇게 보임
- 선물계약 자체의 가치는 거의 매일 0으로 수렴
- 매일매일 일일정산되기 때문
- 선도계약은 일일정산이 아니기 때문에 시간이 흐를수록 선도계약의 가치가 계속 증가

## 6. 금리선물 interest rate futures

금리선물은 기초자산을 금리 또는 채권으로 하는 선물계약이다.

- MRR 또는 T-bonds
- 선물은 계약 형태가 표준화되어 거래소에 상장되어 거래됨
- 금리선물의 표준화된 거래형태를 반드시 알아야 함
- 결제방식은 현금정산 cash settlement

### 가격 공시

금리선물 가격은 다음처럼 공시한다.

$$Futures\ Price=100-annualized\ MRR\ in\ percent$$

예를 들어 6개월 후 6개월짜리 금리를 기초자산으로 하는 futures price가 97이라면 forward MRR은 3%이다.

### Basis point value

BPV는 시장금리 MRR이 1bp 움직였을 때 금리선물계약의 가치 변동이다.

예시:

- 기초자산: 6m MRR
- Notional principal: $1M

$$BPV=\$1M\times0.01\%\times\frac{6}{12}=\$50$$

1bp당 계약 가치는 $50만큼 바뀐다.

실제 트레이더들은 100에서 빼지 않고 그냥 MRR × 100으로 3, 4 이런 식으로 bid/offer한다.

## 7. 선물 및 선도계약 비교

기초자산, 만기 등 계약 조건이 동일하다면 이론적으로 선도가격과 선물가격은 동일하다.

$$Forward\ Price=F_0=S_0(1+r_f)^T$$

$$Futures\ Price=FP_0=S_0(1+r_f)^T$$

다만 선도계약과 선물계약의 정산방법에 따라 차이가 발생한다.

- 선물계약은 일일정산 후 선물가격이 종가로 변경
- Initial margin과 일일정산 금액은 재투자 가능
- 금리가 중요

### 선물가격과 금리의 관계

| 관계 | 결과 |
|---|---|
| 선물가격과 금리의 상관관계가 negative이고 long position | 선물가격 상승 시 낮은 금리로 재투자 → futures 불리, forwards 유리 |
| 선물가격과 금리의 상관관계가 negative이고 long position | 선물가격 하락 시 낮은 금리로 자금 조달 가능 → futures 유리, forwards 불리 |
| 선물가격과 금리의 상관관계가 positive | 선물가격 상승 시 높은 금리로 재투자 가능 → futures 유리, forwards 불리 |
| 선물가격과 금리의 상관관계가 positive | 선물가격 하락 시 높은 금리로 자금 조달 → forwards 유리, futures 불리 |
