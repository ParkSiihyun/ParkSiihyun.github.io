---
title: "CFA Derivatives Topic 4 - Pricing and Valuation of Interest Rate Swaps"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Swaps, Interest Rate Swap, FRA]
---

이 글은 Derivatives PDF의 Topic 4 필기를 축약하지 않고, 스왑계약 구조, IRS, FRA 복제, swap fixed rate, 가치변동까지 원래 페이지 순서대로 옮긴 버전이다.

## Page 29. Topic 4. Pricing and Valuation of Interest rates and other swaps

1. 스왑계약(Swap contracts)
- 미래의 일정기간 동안 / 서로 다른 현금흐름을 / 주기적으로 교환하기로 약정하는 계약
Receiving flacting nate
Tenor
tenor
_tenor
-}
pay fired rate.
Seflement l.
Settement i.
setlene).
✓
Salener?.
2. 스왑계약의 구성요소

### 1) Termination Date(만기) : 스왑계약의 만기일

-&gt; tenor(정산구간) : 주기적인 정산이 이루어지는 구간

### 2) 기초자산(underlying asset) : 정산시점마다 주기적으로 교환하는 특정자산 or 특정자산의 현금흐름


### 3) 정산(settlement) : 일정기간 동안 주기적으로 정산(periodic settlement)


### 4) 계약당사자(counterparty)

- Payer : 지급하는 사람 -&gt; 고정금리를 지급(fixed payer), 주식의 수익을 지급(equity payer)
- Receiver : 수취하는 사람 -&gt; 변동금리를 수취(floating receiver)

### 5) position

- long swap : Receive floating pay fixed
-&gt; 고정금리 채권을 샀는데 변동금리로 바꾸고 싶을 때
- short swap : Receive fixed pay floating
-&gt; 변동금리 채권을 샀는데 고정금리로 바꾸고 싶을 때

---

## Page 30. 3. 스왑계약과 선도계약의 비교

공통점
- 거래비용 : 일반적으로 초기에 비용에 발생하지 않음
- 거래조건 : 거래방법, 만기 등에 제한이 없음
- 거래시 : 당사자 간에 직접 거래(OTC Market)
- 신용위험 : 거래상대방 위험 존재(Counterparty Risk)-&gt; 만기가 길어, 신용위험이 중요
- 거래주체 : 기관(institutions)
차이점
- 선도계약은 만기에 한 번에 정산
- 주기적으로 정산(series of forward contracts)
4. 스왑계약의 종류
- 이자율 스왑(Interest Rate Swap; IRS) : 동일한 통화(currency)에 대하여 서로 다른 금리를 교환
-&gt; Level 1 topic
- 통화스왑(currency swaps; CRS) : 서로 다른 통화(Currency)에 대한 원금과 이자의 교환
- 주식스왑(Equity Swaps) : 주식, 포트폴리오, 인덱스 수익(return)과 고정금리와의 교환
-&gt; CFA IV 1수준에서는 IRS 만 보면 됨
5. 스왑계약의 유형(IRS의 유형)

### 1) Pay fixed receive floating

- plain vanilla IRS : 가장 기본이 되고, 표준적인 형태의 IRS 계약이라는 의미
- 기초자산이 금리이기 때문에 명목원금(notional principal)의 개념의 필요
- 동일한 통화에 대하여 고정금리와 변동금르이 교환 -&gt; netting 가능
- pay fixed, receive floating -&gt; 금리상승 위험의 헤지 가능

### 2) pay floating receive fixed

- plain vanilla IRS
- 동일한 통화에 대하여 고정금리와 변동금리의 교환 -&gt; netting 가능
- pay floating, receive fixed -&gt; 금리하락 위험의 헤지 가능

### 3) pay floating receive floating

- basis swap -&gt; 기준금리가 서로 다른 변동금리를 교환
ex) 1개월 SOFR, 6개월 SOFR 교환

---

## Page 31. 6. 스왑거래 사용목적


### 1) 부채 및 자산의 금리 구조 전환 : IRS를 활용하는 경우, 기존의 금리구조의 전환 가능

고정금리 지금
Combany X
변동금리 채천 발행
floating 4취
Sinap Deaer
(snap bank, EB, 시중은행 )
floartng
2전투자자
investor A
invest FRN
floarting
FRN 1ssuer
Hloating
fxed
&gt; Sap Deater.

---

## Page 32. 7. Interest rate swap; IRS

- 일정기간 동안 서로 다른 금리의 이자를 교환하기로 약정하는 계약
- 명목원금(notional principal) : 교환할 이자를 계산할 때 사용하는 원금

### 1) IRS Terminology

- Notional Principal : 명목원금
- Settlement Date : 정산시점
- Termination Date : 만기
- Fixed rate : 고정금리
- Floating rate : 변동금리

### 2) Plain vanilla IRS : 가장 일반적인 금리스왑

- 고정금리를 지급하고, 변동금리를 수취하기로 약정하는 계약(pay fixed receive floating
..
금리스왑에 일반적으로 이용되는 변동금리 : SOFR(Secured Overnight Financing Rate)
- 금리스왑은 서로 다른 금리에 대한 이자의 교환으로, 원금자체가 실제적으로 교환될 필요가 없음
- 매 시점마다 Net interest(고정금리와 변동금리 차액)만 정산하면 됨
- Netting interest : 고정금리와 변동금리의 차이에 명목원금을 곱한 금액
-&gt; 정산시점마다 차액만 지급
Net nterest rote: (Recave r- Podr) X 360 X Notional pinaipal
ex)(Swo tned raie-SoFRtn) XNPx P360
1Q
20
3Q
4Q
SOFRt- 1Q에서 t=0에 결정된 3개월 짜리 SOFR을 말하는 것.
20 에서 =교에 결정된 3개월짜리 SOFR을 말하는 것.
아까 FRA는 그냥 t=0에서 PV 땡겨서 Payo서를 정산한 것 기억하기.

![Plain vanilla interest rate swap showing fixed and floating cash flows](/images/cfa/derivatives-topic4-swap-flow.svg)

*Pay fixed receive floating 구조를 빠르게 확인하기 위한 보조 그림.*

---

## Page 33. 8. 금리스왑 예시

- 예시 : TY Quarterly Paying IRS, plain vanilla
- position : pay fixed 2%, receive floating 90 day SOFR, Notional amount $10M
0
J0
-
40
++
1Q : Pou 2%
Receive SOFR. 1.4%
(1.4%-2%) X SIOMX
9%60= -45000
3 1=0에 Knocan cmount
20: P04 27
Recelve SOFR. 1.6%
(1622)* 610M x 99660=- 810000+ 5i 에서 402500m
@1 에서 Known.

---

## Page 34. 9. 선도계약으로 스왑계약 부제

- Suep Contracts : A Seres of Fornard ContacT
•IRS : A Seies of FRA
ex IS Quarterly- Paying IRs, roy fined.recele floating
- 만기와 기초자상이 다른 FRA로 복제 가능
Sunap
FRA
Tenor
Poy
receive
Epiration
Undongng Aset
IQ
fred rate
MRRt:0
T=IQ
MRRt=0
20
11
MCRte
T=2Q
3②
MRKt=2
T=3Q
4②
11
MARt=3
T=4Q
FOCT)
fived rate
MRRIQ
MPR 2Q
MRK3Q
1
S어운 Hked에 사는 것
- Pay Hued reve floaing
FRAI
FRA2
V2
FRA31
V3
FRA4
- qff market Jorward : 선도가격이 공정가격이 아닌 선도계약이라서
각각의 FRA의 Valme는 이 아니지만 그 VA는 0이다.
Swap은 기간 내 고정금리가 모두 같지만 Swap을 FRA로 복제할 경우 각각의 spot fixed rate이
모두 다르게 된다. 그래서 각각의 FRA들은 off market FRA가 된다. 즉 각각의 FRA들의 가치는
아니게 된다. 하지만 Swap계약은 공정가격 Swap fixed rate을 설정할 경우 계약 당시 Swap의
가치는 0이된다. 따라서 off market FRA들의 가치의 합도 그냥 0이라고 가정하는 것이다

---

## Page 35. 10. Swap contracts pricing

- forward contracts pricing : 선도가격을 결정하는 프로세스
-&gt; 계약시점에서 선도계약의 가치가 0이되도록 설정 -&gt; no arbitrage pricing
- Swap contracts pricing : 스왑계약의 고정금리(swap fixed rate)을 결정하는 프로세스
-&gt; 계약시점에서 스왑계약의 가치가 0이되도록 설정 -&gt; no abritrage
= 변동금리의 현재가치와 고정금리의 현재가치가 동일하도록 설정. = Par fred rate.
MAR3 = 2y15
MRR = 51
MRz=81남
MRl4 =3817
S1
1y⅓
냉상
VF
VF
/~F
CF
Calon ate par fred rate.
Sp0 금리를 알면 MAR의 값을 현재(t=0) 시점에서 모두 알 수 있다
MRR]
MRRL
+
+
(I+ Sr)
(IS)"
MRR3
( 1tSa
MRR4
( 1+S4)#
=
F
+ .
( tS)}
CI+Sa)

---

## Page 36. 11. Swap Contacls Value at t=0 (Pog fired receive floating)

Tenor
IQ
20
3②
4Q
Suap
Pay
fxed rate
1r
receive
MRRteo
MBRte
MRRt=2
MARt=3
I PV Pay qmount (fixed)
= PY receive amount (loating)
&lt; FRA repliartion&gt;
FRA
Epination
Ladogmg rset
T=Q
MRRt=0
T-2Q
T=3Q
FOCT)
twed rae
T=4Q
NRRIQ
/
MR 20
"
MRR3Q
: Spote fixed에 사는 것.
a Pay fxes receve fracting.
I V.CTl = o
자만 각각의 FRA는
0pf market forward.
= TOCT)가 공정가격이 아닌 FRA.

---

## Page 37. 12. Swap contracts 의 가치변동


### 1) Pay fixed Receive Floating

- Swap value at t= 0
-&gt; 계약시점에서 수령하는 변동금리과 지급하는 고정금리의 현재가치가 동일하도록 스왑계약 체결
- t=t' 현재시점
-&gt; 시장금리(SOFR)이 상승하는 경우 : 수령하는 변동금리의 금액이 상승하기 때문에 가치 상승
-&gt; 시장금리(SOFR)이 하락하는 경우 : 수령하는 변동금리의 금액이 하락하기 때문에 가치 하락

### 2) pay floating receive fixed

- Swap value at t= 0
-&gt; 계약시점에서 수령하는 고정금리와 지급하는 변동금리의 현재가치가 동일하도록 스왑계약 체결
- t=t' 현재시점
-&gt; 시장금리(SOFR)이 상승하는 경우 : 지급하는 변동금리의 금액이 상승하기 때문에 가치 하락
-&gt; 시장금리(SOFR)이 하락하는 경우 : 지급하는 변동금리의 금액이 하락하기 때문에 가치 상승

---
