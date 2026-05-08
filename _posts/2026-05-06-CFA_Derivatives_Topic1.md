---
title: "CFA Derivatives Topic 1 - Derivative Instruments and Market Features"
date: 2026-05-06
categories: cfa
tags: [Derivatives, CFA Level I, Forward Commitment, Contingent Claims, CDS]
---

이 글은 Derivatives PDF의 Topic 1 필기를 축약하지 않고, 페이지 순서와 원래 필기 흐름을 유지해서 블로그 형식으로 옮긴 버전이다.

## Page 1. Reading 66. Derivative Instrument and Derivative Market features

1. 증권
- 증권 security : 권리와 의무를 증명하는 문서(증서) 형태로 존재하는 금융상품
- 주식, 채권 -&gt; 전통적인 금융상품
2. 계약(contracts)
- 계약서의 형태로 존재하는 금융상품
- 파생상품(derivatives)
*정의 : 전통적인 금융상품(주식 및 채권)의 가격 움직임에 의해 그 가치가 결정되는 금융상품
- 선도계약, 선물계약, 스왑계약, 옵션계약
- 기초자산(underlying asset) : 파생상품의 가치를 결정하는 금융상품
: stock, bond, index, FX(외환), interest rate, commodities, credit 등
3. 파생상품 종류
- 선도계약(forward contract) : 미래의 특정시점에 기초자산을 미리 정한 가격으로 매매하기로
약정하는 계약
- 선물계약(futures contract) : 미래의 특정시점에 기초자산을 미리 정한 가격으로 매매하기로 약
정하는 계약. 다만, 계약조건이 '표준화'되어, 거래소에서 거래되는 형태
- 스왑계약(swap contract) : 거래당사자 간에 미래의 일정기간 동안 서로 다른 현금흐름을 교환
하기로 약정하는 계약. 선도 계약을 시리즈(series)로 계약하는 형태
-&gt; 위 의 3가지 파생상품의 경우 계약의 양 당사자는 반드시 계약을 이행해야할 의무(obligation)를
가짐
-&gt; 쌍방의무(bilateral obligation or forward commitment)
-&gt; 사기로 한 사람은 반드시 미리 약정한 가격으로 사야하고, 팔기로 한 사람은 반드시 미리 약정한
가격으로 팔아야만 함
〈파생상품의 구조&gt;
{=0
t=t*
t=T
좌생계약의 체결
매매가격의 결정 V.
만이전 파생상품의 가치
매매가 이루어지는
사정. 4f

---

## Page 2. 4. 옵션계약

- 콜옵션(Call option) : 미래 특정 시점에 기초자산을 미리 정한 가격을 살 수 있는 권리
- 풋옵션(put option) : 미래 특정 시점에 기초자산을 미리 정한 가격을 팔 수 있는 권리
-&gt; 옵션을 매수한 사람은 권리(right)를 가지고 있고, 옵션을 매도한 사람은 의무(obligation)만 가지고
있음
-&gt; 일방의무(Unilateral obligation or contingent claims)
- 옵션 매수자(옵션 롱포지션) : 옵션의 행사 여부를 선택할 수 있는 권리만 가지고 있음
- 옵션 매수자에게 유리한 경우 -&gt; 옵션을 행사하고, 옵션 매도자는 반드시 거래에 응해야 함
- 옵션 매수자에게 불리한 경우 -&gt; 옵션을 행사하지 않을 수 있음
- 옵션 매도자 : 옵션행사에 응해야할 의무만 가지고 있음
&lt;파생상품의 구조&gt;- 옵션 계약
t=0
t=T
-
파생계약의 체결
매매가 이루어지는 시점.
매매가격의 결정
옵션 행사 아 미행사.
5. 신용파생상품(credit derivatives)
- 신용파생상품 : 파생상품의 기초자산이 채권 등에 내재된 신용위험(credit risk)
- 신용위험 : 채권의 등급하향, 스프레드의 확대, 또는 채무불이행 등으로 손실이 발생할 위험
CDS(credit default swap)
- 채권의 채무불이행 등의 신용위험에 대해 일정한 수수료를 지급하는 대가로, 신용사건(부도) 발생
시 원금을 보장받는 파생상품
CoS premium
추자
채현 투자자
채런 발행자
보장매수자
CPotealion Bygon)
protection
보장매도자
Cprorecion seller )
이자 + 원금 .
-&gt; 채전투자자 : "아 애도 못갚을거 같은데?
채린
- IB에게 가서 CDS 체결하자"
( reterence entity)
CDS는 swap 계약이지만, contingent claim 일방의무의 성격을 가지고 있다
- 신용사건이 발생하지 않는 경우 : 매년 보험료만 지불하고, 수령하는 금액이 없음
-&gt; 보장 매도자는 아무런 의무가 없음
- 신용사건이 발생한 경우 : 부도채권에 대한 원금을 보장받을 수 있음

![Map of derivative contract types: forward commitments and contingent claims](/images/cfa/derivatives-topic1-contract-map.svg)

*Forward commitment과 contingent claim을 한 번에 구분하기 위한 보조 그림.*

---

## Page 3. 6. 파생상품이 거래되는 시장(market)에 따른 구분

장내파생상품(exchanged-traded derivatives) : 거래소에서 거래되는 파생상품
- 거래소(exchange) : 기초자산의 종류, 계약단위 만기, 결제 방식, 거래 시간 등 거래방법이 표준화
되고, 규격화된 시장
-&gt; 유동성(liquidity)와 투명성(transparency)가 높음
- 거래소는 청산소(central clearing house)라는 기관을 두고, 모든 계약의 거래 상대방이 되게 하고
계약의 이행을 보증하게 함
- 선물 계약, 옵션 계약이 주로 거래소에서 거래됨
장외파생상품(Over the counter derivatives) : 거래소 외의 장소에서 거래되는 파생상품을 총칭
- 계약 당사자 간 사적 계약에 의해 거래가 이루어짐
-&gt; 거래 당사자 간에 계약조건을 Customizing 할 수 있음
-&gt; 거래상대방이 계약을 이행하지 않을 위험이 있음 -&gt; 거래상대방 위험(counterparty risk)
- CCP(central counterparty) : OTC 거래에서 거래소 또는 청산소의 역할을 수행하는 기관
- 선도 계약, 스왑 계약, 일부 옵션이 OTC에서 거래됨
A
계약
계약.
{
Geong nouse.
B
C
계약.
7. 파생상품의 장점

### 1) 위험관리 및 배분(ability to change risk allocation, transfer risk, and manage risk)

- 위험(risk) : 기대치에서 벗어나는 것= 변동성
- 보유하고 있는 금융자산의 가치가 하락하는 것 뿐만 아니라, 상승하는 것 또한 위험이 될 수 있음
- 파생상품을 이용할 경우, 전통적인 금융자산이 가지고 있는 위험을 제거할 수 있음(변동성 하락)
- Heage 가능
- 변동성 자체를 VisK로 볼 순 없다. 변동성이 없으면 수익도 없는 것이므로.

---

## Page 4. 2) 가격 및 변동성에 대한 정보 제공(information discovery)

- 파생상품은 미래시점에 대한 균형가격 정보, 시장에 내재되어 있는 변동성 등에 대한 정보를 제공
- 선물(futures) : 미래 균형가격에 대한 정보 제공 -&gt; expected future spot price
-&gt; 현물 원유 가격이 $70인데 선물 가격이 $76이라면 미래에 원유 가격이 현재보다 비싸질 것이라고
예측할 수 있다
- 옵션(option) : 변동성에 대한 정보 제공 -&gt; implied volatility 내재된 변동성을 볼 수 있음
-&gt; 어떤 주식에 대한 옵션(행사가격이 아니라 옵션 프리미엄) 매우 비싸다면, 이 주식은 미래에 많은 변
동성을 가질 것으로 예측할 수 있음. 그래서 이 변동성을 헷지하기 위한 권리가 매우 비싼 것
음선의 가격 모델. 후 (8, 7, 7, 6, 위)
변동성에 대한 정보 .

### 3) operation advantages

- ease of short sales: 파생상품을 활용하는 경우, 매도 포지션(short position)을 쉽게 구축할 수 있음
-&gt; 현물을 공매도 하기는 어렵지만, 파생상품은 비교적 용이함
- lower transaction cost : 거래 비용 절감
-&gt; 실제로 현물을 옮길 필요 없이 그냥 계약상으로 존재하고 중간에 포지션 마감을 할 수 있음
- greater leverage : 레버리지(leverage) 포지션 구축이 가능함
-&gt; 매우 적은 돈(initial margin)으로 큰 포지션 구축이 가능함
- greater liquidity : 거래소 상품의 경우 유동성이 매우 높음

### 4) Improved Market efticiency

- 파생상품을 이용한 차익거래(arbitrage) 수행으로 시장효율성(market efficiency) 제고 가능

---

## Page 5. 8. 파생상품의 위험(risks)


### 1) Implicit leverage : 파생상품은 레버리지 효과가 있는 경우 존재함

-&gt; 예상치 못한 높은 리스크를 실현할 수 있음

### 2) Basis risk

- Basis : 현, 선물 가격 차이
- hedge와 basis risk
-&gt; short hedge position : Long spot + Short futures -&gt;S - F
-&gt; perfect hedge : 기초자산의 가격변동과 선물가격의 변동금액이 정확하게 일치하는 경우
-&gt; basis risk : 헷지 대상(assets being hedged)과 헷지 수단(derivatives) 의 가격변동이 일치하
지 않을 위험. 일반적으로 현물가격의 변동금액과 선물가격의 변동금액이 일치하지 않으며, 이를
basis risk 라고 한다.
-&gt; 파생상품을 이용한 hedge는 가격 리스크(price risk)를 베이시스(basis risk)로 전환하는 것

### 3) liquidity risk 유동성 위험

- 유동성 위험 : 일시적인 자금부족으로 정해진 결제 시점에 결제 의무를 이행하지 못할 위험
-&gt; 파생상품은 헷지거래 과정에서도 유동성 위험에 노출될 수 있음
-&gt; margin call이 왔음에도 추가 증거금을 납부하지 못한 경우

### 4) counterparty risk 거래상대방 위험

- 파생상품 거래의 상대방이 선도계약에 대한 의무를 이행하지 않을 위험
- 장외파생상품이 가지고 있는 위험
-&gt; 선물(futures)과 같은 장내 파생상품은 margin제도 운영 및 거래소 이행보증으로 거래상대방
위험에 노출되지 않음

### 5) System risk

- 파생상품은 거래 규모가 크고, 다양한 파생상품 거래가 서로 간에 복잡하게 얽혀있음
- 특정 counterparty risk가 발생할 경우, 거래상대방 위험이 확대 및 전염될 우려가 있음

---

## Page 6. 9. 파생상품 투자 기관


### 1) 일반 기업 : 금융기관이 아닌 일반 기업도 파생상품을 거래하는 경우가 있음, 이는 대부분 헷지를 목적으

로 하는 경우가 많음
- 기업의 환리스크 헷지 목적 -&gt; FX forward
- 자금 조달 과정에서의 금리 위험 헷지 목적 -&gt; IRS 등
- 원자재 구매 과정에서 원자재 가격 위험 헷지 목적 -&gt; Commodity Futures 등
헷지 회계(hedge accounting)
- 헷지 목적으로 체결한 파생상품의 손익을 당기순이익에 반영하는 경우, 기업의 손익 변동성을 오히려
확대시킬 수 있음
- 일반 기업이 파생상품을 현물 자산의. 가격 위험 헷지 목적으로 활용하는 경우, 당기 손익에 미치는 영
향을 축소시키기 위해서 일정한 요건이 갖추어지는 경우 헷지 회계를 반영할 수 있도록 함
-&gt; 쉽게 말해 헤지 대상과 헤지 수단의 손익을 회계상 같은 시점에 반영하게 해주는 특별 회계 처리
-&gt; 경제적으로 헷지를 통해 리스크를 줄였지만, 회계상의 이익만 출렁이게 하는 것을 방지
ex)
Fair value hedge : 기업이 가지고 있는 자산, 부채의 공정가치 변동위험을 헷지하기 위해 파생상품을 이
용하는 것
-&gt; 정유회사가 보유하고 있는 원유가격 하락을 헷지하기 위해 short hedge를 하는 경우
-&gt; 현물과 선물의 가격변동을 상계처리하여, 당기순이익에 반영하지 않을 수 있음
Cash flow hedge : 기업이 가지고 있는 자산, 부채, 예상거래의 미래 현금흐름 변동 위험을 헷지하기 위해
파생상품을 이용하는 것
-&gt; 정유회사가 미래에 매수해야하는 원유 가격 상승위험을 헷지하기 위해서 long hedge를 하는 경우
-&gt; 실제 원유 현물을 매수할 때까지의 원유 선물의 손익은 당기순이익에 반영하지 않을 수 있음
Net investment hedge : 해외 사업장의 순자산에 대하여 위험을 회피하고자 파생상품을 이용하는 것

### 2) 금융기관 : 일반적으로 change risk allocation, transfer risk, and manage risk 목적으로 활용

---

## Page 7. 10. 차익거래(arbitrage)

- 정의 : 추가적인 비용이나 위험부담 없이, 이익을 얻고자 하는 거래
- 대표적인 유형 : 동일한 상품이나 서로 다른 두 개의 시장에서 거래되는 가격이 다를 경우
-&gt; 일물일가의 법칙 위반
-&gt; 가격이 저렴한 시장에서 그 상품을 매입하고, 동시에 가격이 비싼 시장에서 매도하면 추가적인 위
험부담 없이 이익을 얻을 수 있음(buy low and sell high)
- 시장 사이에 발생한 일시적인 가격 불균형은 차익거래에 의하여 균형상태로 회귀함(효율적)
-&gt; 가격이 저렴한 시장 -&gt; 상품 매입 -&gt; 가격 상승
-&gt; 가격이 비싼 시장 -&gt; 상품 매도 -&gt; 가격 하락
-&gt; 균형가격으로 수렴
No arbitrage forward(futures price)
- 선도, 선물 계약에서 미래에 매매하기로 약정하는 가격을 정할 때, 차익거래 개념이 사용됨
- 미래에 선도가격(forward contract price)은 차익거래가 발생하지 않을 가격으로 결정
-&gt; no arbitrage forward price
일물일가의 법칙(the law of one price)
- 두 개의 자산이 동일한 위험과 동일한 현금흐름을 가지고 있다면 가격이 동일해야 함
- 일일가의 법칙이 성립하지 않는 상황에서는, 이론적으로는 차익거래가 가능
무위험 결합포트폴리오
- 두 개의 위험자산을 결합하여 무위험 포트폴리오 구성 가능(주식 - 선도계약, 채권 -CDS 등)
-&gt; 삼성전자 주식 매수 -&gt; 주가 하락 시 손실 발생
-&gt; 선도계약 매도(기초자산 삼성 전자 주식) : 미래에 특정 시점에 삼성전자를 얼마에 팔겠다.
-&gt; 주가 하락 시 이익 발생
- 기초자산 매입 + 선도계약 매도 -&gt; 선도계약 만료일까지 기초가격의 변동에 영향을 받지 않는 무위험
결합포트폴리오 구성 가능
- 무위험 포트폴리오에 기대하는 수익률은 무위험 수익률
-&gt; 무위험 수익률과 다를 경우 차익거래 가능
-&gt; 왜 수익 0 이 아니라 무위험 수익이냐?
-&gt; 선도 계약의 가격은 무위험 수익률을 얻는 다는 가정하에 결정되기 때문
-&gt; 주식 현물 5000원 매수, 같은 주식을 기초자산으로 하는 선도계약 매도
-&gt; 주식이 2000원이 되었다면 현물에서는 3000원 손해지만 선도계약에서 이익이 발생하는 데, 이
때 선도계약의 매도 가격이 기존 5000원이 아니라 무위험수익률이 반영된(5000)*(1+r) 임
-&gt; 그래서 무위험 수익률을 얻는 것임
차익거래의 기능 : 가격의 불균형이 해소되어, 시장의 효율성이 향상됨

---
