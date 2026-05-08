---
title: "CFA Derivatives Topic 3 - Pricing and Valuation of Futures Contracts"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Futures, Margin, Marking to Market, Interest Rate Futures]
---

이 글은 Derivatives PDF의 Topic 3 필기를 축약하지 않고, 선물계약의 표준화, 청산소, 마진, 일일정산, 금리선물까지 원래 흐름대로 옮긴 버전이다.

## Page 23. Toric 3. Prang and Valuation of Futures Conrost.

1. 선물계약(Futures Contracts)
- 미래의 특정시점에 특정 기초자산을 미리 정한 가격으로 매매하기로 약정하는 계약
-&gt; 선도계약의 정의와 동일함
- 거래조건(기초자산, 만기일 등)을 규격화한 후, 거래소에 상장시켜 거래하는 형태
2. 선물계약과 선도계약의 비교
공통점
- Settlement : physical delivery or Cash settlement
- 계약시점의 파생상품 가치 = 0
차이점
- 거래방법, 거래단위, 만기일의 표준화
- 규정된 거래소에서 거래가 이루어짐
- 청산소 clearing house에서 이행 보증
- 증거금 제도가 존재
- 일일정산(선도거래는 일반적으로 선도계약 종료일에 정산)
- No counterparty risk
3. 선물계약의 주요 특성

### 1) 거래소 exchange

- 선물거래가 이루어지는 정형화되고, 조직화되고, 규격화 된 시장
- 거래 시간, 기초자산, 거래방법 등을 미리 정해놓고, 일정한 자격을 갖춘 회원들이 일정한 규칙 아래
매매를 하는 시장

### 2) 청산소 clearing house

- 모든 선물거래의 상대방이 됨으로써 선물거래의 이행을 보증하고, 선물거래의 손익을 정산해주는
기관
- 청산소는 거래소와 별도의 기관으로 설치될 수도 있고, 거래소 기구의 일부분으로 설치될 수도 있음
- 선물거래는 청산소의 이행보증으로 인해 -&gt; No counterparty risk

### 3) Novation : 사적 계약을 거래소와의 계약으로 갱신하는 것

Bilateral OTC mkt
Navailon to Exchange
2)
_CCP
555
B
(
B
75
c
Exchange Kefirg
A
1 25
5)
CCP
B
C

---

## Page 24. 4) 정산가격(Settlement price)

- 정산가격 : 선물계약의 만기일에 선물계약을 정산할 때 사용하는 현물가격 ~ ST
5MLong Position
Poy a ST - Faure Priee (FR)
- ST : 선물계약 만기일의 현물자산의 종가- Settenent Price
- 선물계약 정산시 단순히 증가인 사용한 경우 종가 조작우려가 있음.
3 만기일 이전 일정기간의 평천, 또는 거래량 가중평균 주가를 사용하기도 함.
Short rostion : 기초자산을 판기로 약정한 사람. PayoN: FP- ST

### 5) Offsetting or Reverse Trade

- 선도계약은 만기까지 가는 게 일반적
- 선물계약은 만기에 정산하지 않고, Offsetting trade를 통하여 거래를 청산할 수 있음
- Offsetting trade : 만기 이전에 처음 선물거래 포지션과 반대 포지션의 거래를 통하여
최초 선물 거래를 청산하는 것

### 6) 선물시장 참여자

- Hedgers : 현물가격의 가격 변동위험을 관리하기 위해 선물시장에 참여하는 사람
- Speculators : 현물을 보유하지 않은 상태에서 선물시장에만 참여하는 사람
-&gt; 선물가격의 방향성에 Betting 하는 사람

### 7) Daily settlement, Marking to Market(MTM)

- Daily settlement : 선물가격 변화에 의한 손익을 매일매일 정산하여 증거금계좌에 반영
- 증거금 계좌 : margin account
- Daily settlement 와 Marking to Market을 동일한 용어로 혼용하여 사용하기도 함

### 8) Margin account 증거금 제도

- 선물계약 당사자가 계약을 이행하지 않을 수 있는 위험을 대비하기 위해 거래소가 징수하는 계약이행
보증금 -&gt; performance guarantee
- 개시증거금(initial margin) : 선물거래를 시작하기 위해 납부 해야하는 증거금 -&gt; 비용이 아니라 판돈
- 유지증거금(maintenance margin) : 거래를 지속하기 위해서 반드시 유지해야하는 증거금
- 추가(변동)증거금(Variation margin) : 거래자의 증거금이 maintenace margin이하로 감소하였을 경우
증거금을 initial margin 수준으로 올리도록 추가적인 증거금 적립을 요구(margin call)가 들어옴

---

## Page 25. 9) Price limits(1일 가격 변동한도)

- 거래소에서 부과하는 선물계약의 일일 변동의 폭
- limit up : 일일 변동할 수 있는 상한 가격
- limit down : 일일 변동할 수 있는 하한 가격
- limit move : 상한 가격과 하한 가격 사이의 제한됨 움직임

### 10) CCP(Central Counterparty)

- Forwards, Swaps과 같은 OTC거래에서 거래상대방 간 정산업무를 수행할 수 있도록 지정한 기관
- OTC 거래에서의 거래소 또는 청산소와 유사한 역할을 수행
-&gt; 2008 금융위기 이후 OTC 거래에서의 Counterparty risk를 통제하기 위해, OTC 거래에서도 증거
금을 쓰는 경가 많아 졌고 CCP가 이 증거금을 관리하는 것이 일반적
-&gt; CCP는 그냥 청산소의 특별한 한 종류인데 거래상대방 사이에 끼어들어서 거래가 원활하게 진행되도
록 관리하는 기관임
-&gt; 과거 OTC에는 CCP가 없었지만 현대의 OTC에는 CCP가 존재하는 경우가 많다

### 11) Margin 관련 예시

만기에 후 100 OUnCe를 온스당 $ 1950에 사겠다는 것.
- 5월물 금 선물 1계약을 매수(선물 1계약 = 100ounce), Future Contract price =$1950 / ounce
- Each contract requires an initial margin deposit of $5000 and maintenance margin $4700
Day O : initial margin $5000을 납입해야 선물거래를 시작할 수 있음
Day 1 : Gold Settlement $2.5/ounce 하락
-&gt; daily settlement = 100 ounce* (-2.5)=-$250
&gt; ending margin account=$5000-$250=$4750 -&gt; maintenance margin 보다 높음
Day 2 : Gold Settlement $2.5/ounce 하락
-&gt; daily settlement = 100 ounce *-2.5 =- 250
-&gt; ending margin balance=$4750- 250=$4500 -&gt; maintenance margin보다 낮음
-&gt; Margin Call 발생!!!!!
-&gt; Variation margin =$5000-$4500=$500
Intal margim 까지

---

## Page 26. Margin에 대해서

- Repo나, 주식 대차거래에서의 마진과는 다르다.
- 앞의 예시에 금 선물 1계약(=100온스), 옵션 가격 온스당 $1950일 때
- 실제로 이 선물 계약을 통해서 얻는 손익은 $1950에서 변하는 가격 변동량 * 100온스이다.
예를 들어 하루에 온스당 $2불이 올랐다고 생각하면 얻는 이익은 $200불인 것이다.
Day 0
네가 gold futures long:
1950 진입
계약 크기 = 100 oz
Day 1 종가
선물가격:
1952
상승폭:
1952-1950=2
계약당 손익:
2* 100=+200
-&gt; 네 margin account에 +200 들어옴.
그리고 여기 핵심:
이제 경제적으로는:
네 포지션 기준가격이 1952로 reset된 것과 거의 같음.
왜냐면:
1950-*1952 상승분은 이미 현금으로 받았기 때문.
그리고 그 다음날 가격 변동폭에의해서 또 일일정산되고 내 포지션 기준 가격이 변동되는 것처럼 보임
계약상에서 변동되는 것은 아니지만. 전날 종가에서의 변동분만큼의 일일정산되기 때문에 그렇게 보이는
것이다.
-&gt; 선물 계약 자체의 가치는 따라서 거의 매일 0으로 수렴. 매일매일 일일정산되기 때문
-&gt; 선도 계약은 일일정산이 아니기 때문에 시간이 흐를 수록 선도계약의 가치가 계속 증가

![Futures daily settlement and margin account mechanics](/images/cfa/derivatives-topic3-futures-margin.svg)

*일일정산과 margin account reset 느낌을 잡기 위한 보조 그림.*

---

## Page 27. 4. 금리선물(Interest rate futures)

- 기초자산을 금리(이자율) 또는 채권으로 하는 선물 계약 -&gt; MRR or T bonds
- 선물은 계약의 형태가 표준화되어, 거래소에 상장되어 거래됨
금리선물의 표준화된 거래형태를 반드시 알아야함
- 결제방식 : 현금정산(Cash settlement)
- 가격공시
금리함..
Futures Price= 100-[100X
= 100- anpualzed MER in pereent
Ex) 6개월 후 6개월 지리 금리를 기초자산으로 하는 Fureprice &gt; Fonism 3%에 거래.
Basis point Value (BPV)
: 시장금리(1RR)가 1 op 응결였을 때, 하자계약 계약의 가치 번동.
C) 기초자산 Fenba, Notronal prinaple $IM 7정
BPV= SIM X 0.01%xOh = 450
1 bp당 내 계약의 가치는 50만을 바뀌는 구나.
bu 실제 트레이더들은 100 안하고 2냥 HKR X100해서 3,4, 이름에 bid oftar함.

---

## Page 28. 5. 선물 및 선도계약의 비교

- 기초자산, 만기 등 계약의 조건이 동일하다면, 이론적으로 선도가격과 선물가격은 동일
Torward Proe: ToCo- SCI+r4)T
Futures Price : FPo= So (ltr4)T
Got of Cony Modl
다만, 선도계약과 선물계약의 정산방법에 따라 차이가 발생
- 선물계약은 일일정산 후 선물가격이 종가로 변경
- mitial mang™ 3파은 인증 우 재투하가능
금리가 중요한 이유.
- 선물가격과 금리와의 관계: CorrC Futune Price, Interest rode)&lt;Long Pastion 청&gt;
Negative Cor.
- 선물가격 상승 시, 낮은 금리로 재투자
- Furures 불리
Forwards 유리
Posilfve Corr.
- 선물가격 하락 서, 낮은 궁리로 지금 조달 가능
- Futures 유리 Forwarc 불리
^
Positive Corr.
- 선물가격 상승 시 높은 금리로 재투자 가능
- Futures 유리 Forward 불리
Negotive Conr
- 선물가격 하락 시, 높은 금리로 자금 조달
V Toreard 유이 Tutuies. 부어.
〉

---
