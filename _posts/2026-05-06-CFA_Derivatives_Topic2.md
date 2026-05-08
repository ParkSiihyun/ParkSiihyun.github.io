---
title: "Pricing and Valuation of Forward Contracts (Reading 67)"
date: 2026-05-06
categories: cfa
tags: [Derivatives, CFA Level I, Forwards, Cost of Carry, FRA, FX Forward, Reading 67]
excerpt: "Sihyun CFA Notes - Pricing and Valuation of Forward Contracts (Reading 67)"
---

## Quick Take

- 중심 주제: **Pricing and Valuation of Forward Contracts**
- 먼저 잡을 축: 금융상품이 거래되는 시장, 선도계약 forward contracts, 선도계약의 payoff and settlement
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. 금융상품이 거래되는 시장
2. 선도계약 forward contracts
3. 선도계약의 payoff and settlement
4. 선도계약의 valuation
5. 선도가격의 결정: cost of carry model
6. Cost of carry model의 확장
7. Currency forwards = FX forward
8. 이산복리와 연속복리
9. 다양한 시점에서 선도계약의 가치
10. Forward Rate Agreement
11. FRA로 금리 위험 hedge
12. FRA pricing

## Main Notes

## 1. 금융상품이 거래되는 시장

### 현물시장 spot market

현물시장은 거래가 성립되는 시점과 결제가 동일한 시점에 이루어지는 시장이다.

- 거래시점 = 정산시점
- 현물거래 spot trade는 현물시장에서 이루어지는 거래
- 현물가격 spot price는 현물시장에서 매매하는 가격, 즉 현재 가격
- 현물이자율 또는 현물환율 spot rate은 현물시장에서 매매하는 이자율 또는 환율

### 선도시장 forward market

선도시장은 미래시점에 기초자산을 매매하기로 약정하는 시장이다.

- 거래가 성립되는 시점 ≠ 정산시점
- 선도거래 forward trade는 선도시장에서 이루어지는 거래
- 선도가격 forward price은 미래의 시장에서 매매하기로 약정한 가격
- 선도이자율 또는 선도환율 forward rate은 미래시장에서 매매하기로 약정한 이자율 또는 환율

| 기호 | 의미 |
|---|---|
| S0 | 기초자산의 계약 당시 가격 |
| St | 기초자산의 t시점 가격 |
| ST | 기초자산의 만기시점 가격 |
| F0(T) | t = 0 시점에 t = T에 거래하기로 약정한 선도가격 |

## 2. 선도계약 forward contracts

선도계약은 미래의 특정 시점에, 특정 기초자산을, 미리 정한 가격으로, 매매하기로 약정하는 계약이다.

### 선도계약의 구성항목

| 구성항목 | 내용 |
|---|---|
| 만료일 expiration date, T | 기초자산을 매매하기로 약정한 미래의 특정 시점 |
| 기초자산 underlying asset, S | 매매하기로 약정한 자산 |
| 선도가격 forward price, F(T) | 기초자산을 매매하기로 약정한 가격 |
| 포지션 position | 투자자의 상태 |

| 포지션 | 내용 |
|---|---|
| Long forward position | 기초자산을 사기로 약정한 사람 |
| Short forward position | 기초자산을 팔기로 약정한 사람 |

### 선도계약의 특성

| 특성 | 내용 |
|---|---|
| 기초자산 | 금융자산 또는 실물자산 |
| 금융자산 financial asset | 주식, 채권, 통화, 금리 |
| 실물자산 physical asset or commodity | 농산물, 광물. Alternative investment |
| 사적 계약 private contracts | 계약당사자 간의 사적 계약 |

사적 계약이므로 counterparty risk 또는 default risk가 존재한다. 거래 상대방이 선도계약 의무를 이행하지 않을 위험이다.

반면 사적 계약이기 때문에 선도계약 내용을 customizing할 수 있다는 장점이 있다.

### 선도계약의 체결일 contract date, t = 0

- 미래에 매매하기로 약정하는 계약서를 체결하는 날
- 선도계약 체결을 위한 별도 비용은 발생하지 않음
- 거래 정산을 만기시점에 하기 때문에 initial cost = 0
- 선도계약 체결일의 선도계약 가치 = 0

선도가격은 cost of carry model을 기초로 결정된 균형가격이므로, 계약체결일의 선도계약은 어떤 가치도 없는 균형상태이다. 아직 현물가격 S가 변동하지 않았기 때문이다.

$$V_0(T)=0$$

## 3. 선도계약의 payoff and settlement

### Payoff

Payoff는 파생상품 만기시점의 가치 value at expiration이다.

| 포지션 | Payoff |
|---|---|
| Long forward position | ST - F0(T) |
| Short forward position | F0(T) - ST |

선도계약 당사자 간 payoff는 zero-sum game이다.

### Settlement

Settlement는 파생상품 만기시점의 결제방식이다.

| 방식 | 내용 |
|---|---|
| Physical delivery | 선도계약 만기일에 약정한 선도가격을 지불하고 현물자산 실물을 인수받고 정산 |
| Cash settlement, NDF | 선도만기일의 현물가격과 선도가격의 차액을 현금정산 |

Forward long position의 payoff가 ST - F0(T)라면 그만큼 현금을 받게 되고, forward short position은 F0(T) - ST만큼 현금을 지불해야 한다.

## 4. 선도계약의 valuation

금융상품의 가치는 미래에 발생하는 모든 현금흐름의 현재가치의 합이다.

선도계약의 현금흐름은 long position 기준으로 ST - F0(T)이고, 이를 현가화하면 선도계약의 가치 value가 된다.

$$V_0 = \frac{S_T - F_0(T)}{(1+r)^T}$$

F0(T) = S0(1 + r)^T 이므로 계약체결시점의 선도계약 가치는 0이다.

ST를 모르지만 ST의 현재가치는 S0이다. 미래에 ST를 얻기 위해서는 현재 S0를 구매하면 되기 때문이다.

시점 t에서 만기 T인 선도계약 가치는 다음 흐름으로 본다.

$$V_t(T)=S_t-\frac{F_0(T)}{(1+r)^{T-t}}$$

### Risk averse investors vs risk neutral investors

| 투자자 | 내용 |
|---|---|
| Risk averse investors | 위험회피적 투자자. 위험에 대한 보상을 요구 |
| Risk neutral investors | 위험중립적 투자자. 위험에 대한 보상을 요구하지 않음 |

현대 재무이론은 위험회피적 투자자를 기본 가정으로 한다. 미래 현금흐름을 현가화할 때 위험을 반영한 할인율을 활용하여 현재가치를 계산한다.

$$r = risk\ free\ rate + spread$$

### Replication and arbitrage

기초자산 매입 + 선도계약 매도는 선도계약 만료일까지 기초자산의 가격 변동에 영향을 받지 않는 무위험 포트폴리오를 구성한다.

$$risky\ asset + hedged\ derivative = risk\ free\ asset$$

현물자산과 파생상품을 활용하여 무위험자산을 복제 replication할 수 있다. 무위험자산이 되지 않는다면 arbitrage가 가능하다.

## 5. 선도가격의 결정: cost of carry model

선도가격은 t = 0 시점에서 어떻게 결정되는가?

Cost of carry model은 선도가격을 현물가격과 현물을 만기까지 보유하는 데 필요한 비용을 합한 금액으로 결정한다.

t = T 시점에 현물자산을 보유하는 방법은 두 가지이다.

1. t = 0 시점에 현물자산을 매입하여 t = T 시점까지 보유
2. t = 0 시점에 만기가 T인 선도계약을 매수

두 방법의 경제적 실질이 같기 때문에 두 방법은 같은 가격이어야 한다.

$$Forward\ Price = Spot\ Price + Cost\ of\ Carry$$

### Cost of carry model의 가정

- 무위험이자율 risk-free rate로 차입이나 대출 가능
- 위험에 대해 보상을 요구하지 않는 risk neutral 가정
- 공매 short selling 제한 없음
- 세금과 거래비용 없음 no tax, no transaction cost

### 보유비용 cost of carry

| 상황 | 비용 |
|---|---|
| 차입하여 매입 | 대출에 따른 이자비용 발생 |
| 자기자본으로 매입 | 기초자산 매입에 따른 기회비용 발생 |

S0만큼 은행에 넣었더라면 S0 × (1 + r)^T만큼 돈을 벌었을 것이고, S0만큼 대출해서 보유했다면 S0 × (1 + r)^T만큼 비용이 들었을 것이다.

$$F_0(T)=S_0(1+r)^T$$

연속복리로는 다음과 같이 표현한다.

$$F_0(T)=S_0e^{rT}$$

## 6. Cost of carry model의 확장

### 기초자산이 금융자산인 경우

기초자산에서 배당 dividends 또는 이자 interests 같은 현금흐름이 발생할 수 있다.

- 선물계약 만기 이전에 현물자산에서 배당 또는 이자 현금흐름 발생
- 보유기간 동안 편익 발생
- 보유비용을 감소시키는 효과
- 선도계약 만기에 매수하는 기초자산은 중간에 발생한 현금흐름이 차감됨

Dividend는 선도계약 long position이 아니라 주식보유자에게 귀속되기 때문에 기초자산 보유비용에서 빼줘야 한다.

$$F_0(T)=[S_0-PV(Benefit)](1+r)^T$$

### 기초자산이 원자재인 경우

원자재는 추가적인 비용과 편익이 발생한다.

| 항목 | 내용 | 선도가격 효과 |
|---|---|---|
| Storage costs | 창고임대료, 손상 가능성, 보험료 등 | 선도가격 증가 |
| Convenience yield | 원자재 부재 시 발생하는 불편과 비능률을 제거하는 이익 | 선도가격 감소 |

현물자산을 보유하고 있으면 갑작스러운 공급 충격에 대응할 수 있다. Convenience yield는 보유비용을 감소시키는 효과가 있다.

$$F_0(T)=[S_0+PV(Cost)-PV(Benefit)](1+r)^T$$

연속복리 표현은 다음과 같다.

$$F_0(T)=S_0e^{(r+c-b)T}$$

## 7. Currency forwards = FX forward

### 기초자산

외국통화 foreign currency.

### 환율 표시방법

| 방식 | 내용 | 예시 |
|---|---|---|
| 직접표시법 | 외국통화 한 단위의 가치를 자국 통화로 표시 | $1 = 1,200원 |
| 간접표시법 | 자국통화 한 단위의 가치를 외국통화로 표시 | 1원 = $1 / 1,200 |

### Spot trade vs forward trade

| 거래 | 내용 | 적용 환율 |
|---|---|---|
| Spot trade | 외환의 즉각적 인도를 조건으로 하는 거래. 일반적으로 D+2 결제까지 현물로 인정 | spot rate |
| Forward trade | 현물환거래 D+2 이후를 결제일로 하는 외환거래 | forward rate |

### Interest rate parity

선도환율 forward rate은 interest rate parity, 즉 IRP로 결정된다.

- 모든 나라의 실질금리는 동일하다.
- 각국의 금리차는 환율에 의해 조정된다.
- 모든 나라의 실질금리가 동일하지 않으면 차익거래가 발생한다.
- IRP는 국가 간 명목금리 차이가 존재하더라도 환율효과까지 반영하면 실질금리가 동일하다는 의미이다.
- Parity는 둘의 가치가 같아야 함을 의미한다.

자국통화 1단위를 자국금리에 투자하는 것과, 자국통화 1단위를 외국통화로 환전 후 외국금리로 투자하고 T시점에 선도환율로 다시 자국통화로 환전하는 것은 이론상 같은 가치여야 한다.

FX forward에서 아래에 있는 것을 base currency로 두고 계산하면 편하다.

$$F_{f/p}=S_{f/p}\frac{(1+r_f)}{(1+r_p)}$$

예시:

- EUR이 base currency, 금리 3%
- USD가 price currency, 금리 2%
- S = 1.1

$$F = 1.1 \times \frac{1.03}{1.02}=1.1088$$

## 8. 이산복리와 연속복리

원금 1원, 이자율 2%, 만기 T라고 할 때:

| 방식 | 미래가치 | 할인율 |
|---|---|---|
| Annual | 1 × (1 + 2%)^T | 1 × (1 + 2%)^-T |
| Semiannual | 1 × (1 + 2% / 2)^(2T) | 1 × (1 + 2% / 2)^(-2T) |
| Quarter | 1 × (1 + 2% / 4)^(4T) | 1 × (1 + 2% / 4)^(-4T) |
| N | 1 × (1 + 2% / N)^(NT) | 1 × (1 + 2% / N)^(-NT) |
| Continuous | 1 × e^(rT) | 1 × e^(-rT) |

이산복리와 같은 수익률, 즉 등가성을 갖는 연속복리 r은 T = 1일 때 다음과 같이 계산한다.

$$1.02=e^r$$

$$r=\ln(1.02)=0.0198=1.98\%$$

## 9. 다양한 시점에서 선도계약의 가치

Pricing은 선도가격을 결정하는 것이다.

$$F_0(T)=S_0 + Cost\ of\ Carry$$

계약의 가치:

$$V_0(T)=0$$

IRP에서도 F0(T)는 0이 아니라 선도가격이고, 계약의 가치가 0이다.

Valuation은 현재시점의 선도계약 가치를 평가하는 것이다.

만기시점의 payoff:

$$V_T(T)=S_T-F_0(T)$$

t = t' 시점의 가치:

$$V_t(T)=S_t-\frac{F_0(T)}{(1+r_f)^{T-t}}$$

기초자산에서 추가적인 cost와 benefit이 발생하면 선도가격이 달라진다.

$$F_0(T)=[S_0+PV(Cost)-PV(Benefit)](1+r_f)^T$$

t = t' 시점의 valuation:

$$V_t(T)=S_t+PV(Cost)-PV(Benefit)-\frac{F_0(T)}{(1+r_f)^{T-t}}$$

만기 ST의 현재가치를 복제하려면 S0를 사는 논리가 있었고, 같은 논리로 이번에는 ST를 복제하는 과정에서 보관비와 편익이 발생하므로 St + PV(Cost) - PV(Benefit)이 된다.

## 10. Forward Rate Agreement

FRA는 선도금리계약이며 interest rate forward이다.

- 미래의 일정 구간 동안 적용할 금리를 미리 약정하는 계약
- 미래의 금리를 사고팔기로 약정하는 계약
- 현재시점에서 미래의 forward rate을 거래하는 것
- Underlying asset은 미래의 일정 구간 동안 적용할 금리, 즉 선도금리
- FRA 기초자산으로 가장 많이 활용되는 금리: SOFR, MRR, Eurodollar deposit 금리

Eurodollar deposit은 미국이 아닌 다른 지역의 은행에서 달러를 기초로 거래되는 예금이다.

### FRA position

| 포지션 | 내용 | 목적 | 현물포지션 예시 |
|---|---|---|---|
| FRA long position | 선도금리를 미리 사는 계약 | 금리 상승위험 회피 | 돈을 빌리려는 사람, fixed bond long, FRN issue, 미래 대규모 차입 |
| FRA short position | 선도금리를 미리 파는 계약 | 금리 하락위험 회피 | 돈을 빌려주려는 사람, fixed bond short, FRN long, 미래 대규모 자금 유입 |

Fixed bond short은 채권을 빌려서 팔고 더 싼 값에 매입해야 이득이다. 금리가 상승해서 채권 가격이 떨어지는 것을 노려야 한다. 금리가 하락하면 채권 가격이 상승하여 채권 short position에서 손해를 보므로 FRA short으로 hedge한다.

## 11. FRA로 금리 위험 hedge

### FRA long position 예시

Company A는 30일 후에 90일간 자금을 차입할 예정이다. 차입금리는 90-day SOFR이다.

| 시점 | 내용 |
|---|---|
| t = 0 | 현재 |
| t = 30 | 차입 시작 |
| t = 120 | 90일 차입 종료 |

Company A가 직면한 위험은 30일 후 금리가 상승할 위험이다.

- 금리를 미리 사는 계약을 체결해야 한다.
- Forward long position이 필요하다.
- 30일 후 90-day SOFR가 상승하면 forward 계약에서 이익이 발생한다.
- 금리 상승위험을 hedge한다.

### FRA short position 예시

Company B는 30일 후에 90일간 자금을 대출해줄 예정이다. 대출금리는 90-day SOFR이다.

Company B가 직면한 위험은 30일 후 금리가 하락할 위험이다.

- 금리를 미리 파는 계약을 체결해야 한다.
- Forward short position이 필요하다.
- 30일 후 90-day SOFR가 하락하면 forward 계약에서 이익이 발생한다.
- 금리 하락위험을 hedge한다.

## 12. FRA pricing

FRA의 기초자산은 미래의 일정 구간 동안 적용할 금리, 즉 선도금리이다.

FRA pricing은 미래 구간의 금리를 forward rate으로 사거나 팔자고 약정할 때 no arbitrage가 되도록 하는 것이다.

Underlying asset이 SOFR과 같은 단기금리인 경우 금리에 대한 market convention은 단리이다.

### 예시: 3m6m with notional principal $1,000

3개월 후 6개월짜리 금리가 기초자산이다.

| 금리 | 값 |
|---|---|
| 3M MRR | 1% |
| 9M MRR | 1.2% |

MRR은 annual 기준이다.

단리 계산:

$$(1+1.2\%\times\frac{9}{12})=(1+1\%\times\frac{3}{12})(1+3m6m\times\frac{6}{12})$$

결과적으로 3m6m forward rate은 약 1.3%이다.

만약 t = 3m 시점에서 S6m = 2%라면 FRA long position은 0.7% 이득이다.

만약 t = 3m 시점에서 S6m = 1%라면 FRA long position은 0.3% 손실이다.

### 금리가 기초자산인 상품의 용어

| 용어 | 내용 |
|---|---|
| Notional principal | 계약서상의 원금 |
| Annualized rate | MRR, forward rate 등은 모두 연환산 금리 |
| Arrear | 후취 |
| Day count adjustment | 일수 조정 |

## 13. FRA payoff and settlement

FRA payoff는 파생상품 계약 만기시점의 가치이다.

$$FRA\ Payoff=Notional\ Principal\times(S-F)\times\frac{D}{360}$$

S는 해당 시점에서 확정되지만, 그 금리가 적용되는 대상은 그 이후 기간이다. 따라서 payoff는 금리가 적용되는 기간의 이자차이이다. 하지만 실제 FRA는 만기시점에 확인해서 바로 정산한다.

예시:

$$Payoff=(1.5\%-1.3\%)\times\$1M\times\frac{6}{12}=\$1,000$$

이 payoff는 9개월 시점에서 발생한다. 이를 3개월 시점으로 현가화하여 만기시점에 바로 정산한다.

$$Settlement=\frac{\$1,000}{1+1.5\%\times\frac{6}{12}}=\$992.56$$
