---
title: "Pricing and Valuation of Interest Rate Swaps (Reading 69)"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Swaps, Interest Rate Swap, FRA, Reading 69]
excerpt: "Sihyun CFA Notes - Pricing and Valuation of Interest Rate Swaps (Reading 69)"
---

## Quick Take

- 중심 주제: **Pricing and Valuation of Interest Rate Swaps**
- 먼저 잡을 축: 스왑계약 swap contracts, 스왑계약의 구성요소, 스왑계약과 선도계약의 비교
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. 스왑계약 swap contracts
2. 스왑계약의 구성요소
3. 스왑계약과 선도계약의 비교
4. 스왑계약의 종류
5. IRS의 유형
6. 스왑거래 사용목적
7. Interest rate swap, IRS
8. 금리스왑 예시
9. 선도계약으로 스왑계약 복제
10. Swap contracts pricing
11. Swap contract value at t = 0
12. Swap contract의 가치변동

## Main Notes

## 1. 스왑계약 swap contracts

스왑계약은 미래의 일정기간 동안 서로 다른 현금흐름을 주기적으로 교환하기로 약정하는 계약이다.

예시 구조:

- Receive floating rate
- Pay fixed rate
- Tenor마다 settlement

## 2. 스왑계약의 구성요소

| 구성요소 | 내용 |
|---|---|
| Termination date | 스왑계약의 만기일 |
| Tenor | 주기적인 정산이 이루어지는 구간 |
| Underlying asset | 정산시점마다 주기적으로 교환하는 특정자산 또는 특정자산의 현금흐름 |
| Settlement | 일정기간 동안 주기적으로 정산, periodic settlement |
| Counterparty | 계약당사자 |

### Payer와 receiver

| 구분 | 내용 |
|---|---|
| Payer | 지급하는 사람. fixed payer, equity payer |
| Receiver | 수취하는 사람. floating receiver |

### Position

| 포지션 | 내용 | 사용 상황 |
|---|---|---|
| Long swap | Receive floating, pay fixed | 고정금리 채권을 샀는데 변동금리로 바꾸고 싶을 때 |
| Short swap | Receive fixed, pay floating | 변동금리 채권을 샀는데 고정금리로 바꾸고 싶을 때 |

## 3. 스왑계약과 선도계약의 비교

### 공통점

| 항목 | 내용 |
|---|---|
| 거래비용 | 일반적으로 초기에 비용이 발생하지 않음 |
| 거래조건 | 거래방법, 만기 등에 제한이 없음 |
| 거래시장 | 당사자 간 직접 거래, OTC market |
| 신용위험 | 거래상대방 위험 존재. 만기가 길어 신용위험이 중요 |
| 거래주체 | 기관 institutions |

### 차이점

| 선도계약 | 스왑계약 |
|---|---|
| 만기에 한 번 정산 | 주기적으로 정산 |
| 단일 forward contract | series of forward contracts |

## 4. 스왑계약의 종류

| 유형 | 내용 |
|---|---|
| Interest rate swap, IRS | 동일한 통화에 대해 서로 다른 금리를 교환 |
| Currency swap, CRS | 서로 다른 통화에 대한 원금과 이자의 교환 |
| Equity swap | 주식, 포트폴리오, 인덱스 수익과 고정금리의 교환 |

CFA Level 1에서는 IRS를 보면 된다.

## 5. IRS의 유형

### Pay fixed receive floating

- Plain vanilla IRS
- 가장 기본이 되고 표준적인 IRS 계약
- 기초자산이 금리이기 때문에 명목원금 notional principal 개념이 필요
- 동일한 통화에 대해 고정금리와 변동금리 교환
- Netting 가능
- 금리상승 위험 hedge 가능

### Pay floating receive fixed

- Plain vanilla IRS
- 동일한 통화에 대해 고정금리와 변동금리 교환
- Netting 가능
- 금리하락 위험 hedge 가능

### Pay floating receive floating

- Basis swap
- 기준금리가 서로 다른 변동금리 교환
- 예: 1개월 SOFR와 6개월 SOFR 교환

## 6. 스왑거래 사용목적

IRS를 활용하면 기존의 부채 및 자산 금리구조를 전환할 수 있다.

### 부채의 금리구조 전환

Company X가 변동금리채권을 발행했을 때 swap dealer와 거래하여 다음 구조를 만들 수 있다.

- Company X는 swap dealer에게 fixed를 지급
- Company X는 swap dealer로부터 floating을 수취
- 결과적으로 변동금리 부채를 고정금리 부채처럼 전환

### 자산의 금리구조 전환

Investor A가 FRN에 투자하면 floating을 수취한다. Swap dealer와 거래하면 fixed를 수취하는 구조로 전환할 수 있다.

## 7. Interest rate swap, IRS

IRS는 일정기간 동안 서로 다른 금리의 이자를 교환하기로 약정하는 계약이다.

### Terminology

| 용어 | 내용 |
|---|---|
| Notional principal | 명목원금. 교환할 이자를 계산할 때 사용하는 원금 |
| Settlement date | 정산시점 |
| Termination date | 만기 |
| Fixed rate | 고정금리 |
| Floating rate | 변동금리 |

### Plain vanilla IRS

가장 일반적인 금리스왑은 고정금리를 지급하고 변동금리를 수취하기로 약정하는 계약이다.

- Pay fixed, receive floating
- 금리스왑에 일반적으로 이용되는 변동금리는 SOFR
- SOFR = Secured Overnight Financing Rate
- 서로 다른 금리에 대한 이자의 교환이므로 원금 자체가 실제로 교환될 필요는 없음
- 매 시점마다 net interest, 즉 고정금리와 변동금리 차액만 정산

### Net interest

Net interest는 고정금리와 변동금리의 차이에 명목원금을 곱한 금액이다.

$$Net\ interest=(Receive\ rate-Pay\ rate)\times\frac{Days}{360}\times Notional\ principal$$

예:

$$ (Swap\ fixed\ rate-SOFR_{t-1})\times NP\times\frac{Days}{360} $$

SOFR t-1Q는 t = 0에 결정된 3개월짜리 SOFR을 말한다. 2Q에서는 1Q에 결정된 3개월짜리 SOFR을 사용한다.

FRA는 t = 0에서 PV로 당겨 payoff를 정산했다는 점을 기억한다.

## 8. 금리스왑 예시

예시:

- 1Y quarterly paying IRS
- Plain vanilla
- Position: pay fixed 2%, receive floating 90-day SOFR
- Notional amount: $10M

### 1Q

- Pay fixed: 2%
- Receive SOFR0: 1.4%
- t = 0에 known amount

$$ (1.4\%-2\%)\times\$10M\times\frac{90}{360}=-\$15,000 $$

### 2Q

- Pay fixed: 2%
- Receive SOFR1: 1.6%
- t = 0에서는 unknown
- 1Q에서는 known

$$ (1.6\%-2\%)\times\$10M\times\frac{90}{360}=-\$10,000 $$

## 9. 선도계약으로 스왑계약 복제

- Swap contracts = a series of forward contracts
- IRS = a series of FRA

예시:

- 1Y quarterly-paying IRS
- Pay fixed, receive floating
- 만기와 기초자산이 다른 FRA로 복제 가능

| Swap tenor | Pay | Receive | FRA expiration | Underlying asset | F0(T) |
|---|---|---|---|---|---|
| 1Q | fixed rate | MRR t=0 | T = 1Q | MRR t=0 | fixed rate |
| 2Q | fixed rate | MRR t=1Q | T = 2Q | MRR 1Q | fixed rate |
| 3Q | fixed rate | MRR t=2Q | T = 3Q | MRR 2Q | fixed rate |
| 4Q | fixed rate | MRR t=3Q | T = 4Q | MRR 3Q | fixed rate |

Swap에서는 고정금리가 모두 같지만, swap을 FRA로 복제할 경우 각각의 spot fixed rate이 모두 다르다.

그래서 각각의 FRA는 off-market FRA가 된다. 즉 각각의 FRA 가치는 0이 아닐 수 있다. 하지만 swap 계약은 공정가격 swap fixed rate을 설정할 경우 계약 당시 swap의 가치는 0이 된다. 따라서 off-market FRA들의 가치 합도 0이라고 가정한다.

## 10. Swap contracts pricing

Forward contracts pricing은 선도가격을 결정하는 프로세스이다.

- 계약시점에서 선도계약 가치가 0이 되도록 설정
- No arbitrage pricing

Swap contracts pricing은 스왑계약의 고정금리 swap fixed rate을 결정하는 프로세스이다.

- 계약시점에서 스왑계약 가치가 0이 되도록 설정
- No arbitrage
- 변동금리의 현재가치와 고정금리의 현재가치가 동일하도록 설정
- Par fixed rate

Spot 금리를 알면 MRR 값을 현재 t = 0 시점에서 모두 알 수 있다.

공정 swap fixed rate은 지급하는 fixed leg의 현재가치와 수취하는 floating leg의 현재가치가 같도록 계산한다.

## 11. Swap contract value at t = 0

Pay fixed receive floating swap 기준:

| Tenor | Pay | Receive |
|---|---|---|
| 1Q | fixed rate | MRR t=0 |
| 2Q | fixed rate | MRR t=1Q |
| 3Q | fixed rate | MRR t=2Q |
| 4Q | fixed rate | MRR t=3Q |

계약시점에는 다음이 성립한다.

$$PV(pay\ amount,\ fixed)=PV(receive\ amount,\ floating)$$

FRA replication 관점에서 보면 각각의 FRA는 off-market forward이다. 각각의 FRA는 F0(T)가 공정가격이 아닌 FRA일 수 있다. 하지만 전체 swap value는 계약시점에 0이다.

## 12. Swap contract의 가치변동

### Pay fixed, receive floating

계약시점 t = 0에는 수령하는 변동금리와 지급하는 고정금리의 현재가치가 동일하도록 스왑계약을 체결한다.

t = t' 현재시점:

| 시장금리 변화 | 가치 변화 |
|---|---|
| SOFR 상승 | 수령하는 변동금리 금액이 상승하므로 가치 상승 |
| SOFR 하락 | 수령하는 변동금리 금액이 하락하므로 가치 하락 |

### Pay floating, receive fixed

계약시점 t = 0에는 수령하는 고정금리와 지급하는 변동금리의 현재가치가 동일하도록 스왑계약을 체결한다.

t = t' 현재시점:

| 시장금리 변화 | 가치 변화 |
|---|---|
| SOFR 상승 | 지급하는 변동금리 금액이 상승하므로 가치 하락 |
| SOFR 하락 | 지급하는 변동금리 금액이 하락하므로 가치 상승 |
