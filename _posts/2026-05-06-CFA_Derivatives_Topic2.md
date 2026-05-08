---
title: "CFA Derivatives Topic 2 - Pricing and Valuation of Forward Contracts"
date: 2026-05-06
categories: cfa
tags: [Derivatives, CFA Level I, Forwards, Cost of Carry, FRA, FX Forward]
---

이 글은 Derivatives PDF의 Topic 2 필기를 축약하지 않고, 선도가격, valuation, FX forward, FRA 계산 흐름을 원래 페이지 순서대로 옮긴 버전이다.

## Page 8. Topic 2 : Pricing and Valuation of Forward Contracts

![Original Derivatives PDF page 8](/images/cfa/derivatives-pages/derivatives-page-08.jpg)

*원본 PDF p.8*

**OCR transcription**

1. 금융상품이 거래되는 시장(Market)
현물시장(Spot Market) : 거래가 성립되는 시점과 결제가 동일한 시점에 이루어지는 시장
-&gt; 거래시점 = 정산시점
- 현물거래(spot trade) : 현물시장에서 이루어지는 거래
- 현물가격(spot price) : 현물시장에서 매매하는 가격 -&gt; 현재 가격
- 현물이자율 or 현물환율(spot rate ; S) : 현물시장에서 매매하는 이자율 or 환율 -&gt; 현재 금리 or 환율
선도시장(forward market) : 미래시점에 기초자산을 매매하기로 약정하는 시장
-&gt; 거래가 성립되는 시점 =/ 정산시점
- 선도거래(forward trade) : 선도시장에서 이루어지는 거래
: 선도가격(orard price) : 미래의 시장에서 매매하기로 약정한 가격 1 6o(T)- SoCIt)T
- 선동이자율 or 선도환율(forward rate) : 미래시장에서 매매하기로 약정한 이자율 or 환율
[=0
t=+'
So : 기초자산의 계약당시 가격
Bt : 기초자산의 1시점 가격.
ST : 기초자산의 만기시점 가격.
(T) : 미계에 매매하기를 약전한 가격, 한육, 이자유
[=0 시점에 teT에 거래학 선도가격
t=T

---

## Page 9. 2. 선도계약(forward contracts)

![Original Derivatives PDF page 9](/images/cfa/derivatives-pages/derivatives-page-09.jpg)

*원본 PDF p.9*

**OCR transcription**

: 미래의 특정시점에 / 특정 기초자산을 / 미리 정한 가격으로 / 매매하기로 약정하는 계약
선도계약의 구성항목

### 1) 만료일(expiration date ; T) : 기초자산을 매매하기로 약정한 미래의 특정 시점


### 2) 기초자산(Underlying asset ; S) : 매매하기로 약정한 자산


### 3) 선도가격(Forward Price ; F(T)) : 기초자산을 매매하기로 약정한 가격


### 4) 포지션(position) : 투자자의 상태

-&gt; 매입포지션(long forward position) : 기초자산을 사기로 약정한 사람
-&gt; 매도포지션(Short forward position) : 기초자산을 팔기로 약정한 사람
선도계약의 특성

### 1) 기초자산(underlying asset)

- 금융자산(financial asset) : 주식, 채권, 통화, 금리
- 실물자산(physical asset or commodity) : 농산물, 광물 -&gt; Alternative investment

### 2) 계약당사자 간의 사적 계약(private contracts)

- Counterparty risk or default risk 존재
-&gt; 거래의 상대방이 선도계약에 대한 의무를 이행하지 않을 위험
- 반면, 사적계약이기 때문에 선도계약의 내용에 대해 Customizing 할 수 있다는 장점이 있음
선도계약의 체결일(Contract Date ; t=0)
- 선도계약 체결일 : 미래에 매매하기로 약정하기로 계약서를 체결하는 날
-&gt; 선도계약 체결을 위한 별도의 비용은 발생하지 않음
-&gt; 거래에 대한 정산을 만기시점에 하기 때문에 initial cost = 0
- 선도계약 체결일의 선도계약의 가치 = 0
-&gt; 선도가격은 cost of carry model을 기초로 결정된 균형가격이므로, 계약체결일의 선도계약은 어
떤 가치도 없는 균형상태임
-&gt; 아직 현물가격(S)가 변동하지 않았기 때문
-&gt; 왜냐하면 계약 당시에는 S의 변화가 없다고 가정하기 때문
Vo(T)= 0
t=0 시점에 안기가 T인 선도계약의 가치 = 0

---

## Page 10. 3. 선도계약의 Payoff and Settlement

![Original Derivatives PDF page 10](/images/cfa/derivatives-pages/derivatives-page-10.jpg)

*원본 PDF p.10*

**OCR transcription**


### 1) payor : 파생상품 만기시점의 가치(value at expiration) Ut,F

- 1ong porton reyot: dT- 1aCT) 3 센도약 당사자 간의 Zoosumn gone
-Shor postion Papot: Fa-$
!
}
ST
m!
[=0
VO=O
tt
-
=|
"우-ET)

### 2) Settlement(정산) : 파생상품 만기시점의 결제방식

- 실물인수도(physical delivery) : 선도계약 만기일에 약정한 선도가격을 지불하고, 현물자산 실물을
인수받고 정산하는 방법
- 현물정산(Cash settlement or Non Deliverable Forwards ; NDF) : 선도만기일의 현물가격과 선
도가격의 차액을 현금정산
주식의 가격이 몰라서
forward long Poation e Peyota ST -Fo(T) 라면 그만큼 현금을 받게 되고,
forard chor poition 사람은 FOCT)-S 만큼 현금을 지불해야 한다.

![Forward contract payoff diagram for long and short positions](/images/cfa/derivatives-topic2-forward-payoff.svg)

*Long forward와 short forward의 payoff 방향을 확인하기 위한 보조 그림.*

---

## Page 11. 4. 선도계약의 Valuation

![Original Derivatives PDF page 11](/images/cfa/derivatives-pages/derivatives-page-11.jpg)

*원본 PDF p.11*

**OCR transcription**


### 1) 금융상품의 가치

- 미래에 발생하는 모든 현금흐름의 현재가치의 합
- 선도계약의 현금흐름은
PayOR (ng postion)=ST-FoT)을 현자화하면 신도약의 가치(alic)가 됨,
Vo =
5-FO(T S.- 5O(T
(ltr)T
(lr,t : 0
( Fot)= So(Itr) 이므로) 선조가격이 이전에는 다음다.
왜 이렇게 되냐 ST를 우리는 모증하지만 ST의 현재가치는 그냥 S.잉.
미래에 Sp를 얻기 위해서는 그냥 현재 SO를 구매하면 되기 때문.
Vt=
S - FoCT)
Ctrit=f-
Fo(T)
(14거자

### 2) risk averse investors vs risk neutral investors

- risk averse investors : 위험회피적 투자자 -&gt; 위험에 대한 보상을 요구
-&gt; 현대 재무이론 : 위험회피적 투자자를 기본 가정으로 함
-&gt; 미래 현금흐름을 현가화 할 때, 위험을 반영한 할인율을 활용하여 현재가치 계산
-&gt; 할인율 「= risk free rate + spread
- risk neutral investors : 위험중립적 투자자 -&gt; 위험에 대한 보상을 요구하지 않는 투자자

### 3) replication and arbitrage

- 기초자산 매입 + 선도계약 매도 -&gt; 선도계약 만료일까지 기초자산의 가격 변동에 영향을 받지 않는 무
위험 포트폴리오 구성 가능
-&gt; risky asset + hedged derivative = risk free asset
-&gt; 현물자산과 파생상품을 활용하여 무위험자산을 복제(replication) 가능
-&gt; 무위험자산이 되지 않는다면, 차익거래(arbitrage) 가능

---

## Page 12. 5. 선도가격의 결정 : t= 0 시점에서 선도가격은 어떻게 결정하나?

![Original Derivatives PDF page 12](/images/cfa/derivatives-pages/derivatives-page-12.jpg)

*원본 PDF p.12*

**OCR transcription**

Cost of carry model
- 선도가격을 현물가격과 / 현물을 만기까지 보유하는 데 필요한 비용을 합한 금액으로 결정
- t=T 시점에 현물자산을 보유하는 방법
-&gt; t= 0 시점에 현물자산을 매입하여 t= T 시점까지 보유하는 방법
-&gt; t= 0 시점에 만기가 T시점인 선도계약을 매수하는 방법
-&gt; 두 방법의 경제적 실질이 같기 때문에 두 방법은 같은 가격이어야 한다.
선도가격 TO(T)= 현물가격 So + 보유비용 Cost of Couny
7 No arbitrage forvard price.

### 1) Cost of carry model의 가정

- 무위험이자율(risk free rate)로 차입이나 대출이 가능
-&gt; 위험에 대하여 보상을 요구하지 않는 risk neutral 가정
- 공매(shortselling)에 대한 제한이 없음
- 세금과 거래비용이 없음(no tax, no transaction Cost)

### 2) 현물 가격 : S0


### 3) 보유 비용(Cost of Carry)

- 차입하여 매입하는 경우 : 대출에 따른 이자비용 발생(rf)
- 자기자본으로 매입하는 경우 : 기초자산 매입에 따른 기회비용 발생(rf)
-&gt; 이 돈을 은행에 예금했더라면 얻을 수 있었던 이득

### 4) 선도가격

1 현물가격
507a So x (ltr)
보유비용.
- S x erT
보유비용은 S0 가격의 현물을 위의 두 방법 중 어떤 방법으로든 사서 만기까지 보유하는 데 드는 비용
SO 만큼 은행에 넣었더라면 SO*(1+r)^T 만큼 돈을 벌었을 것이고(기회비용)
SO 만큼 대출해서 들고 있었다면 SO*(1+r) T만큼 비용이 들었을 것이다(실제비용)

---

## Page 13. Cost of Carry Model의 확장 1-&gt; 기초자산이 금융자산인 경우 -&gt; 추가적인 보유 편익 발생

![Original Derivatives PDF page 13](/images/cfa/derivatives-pages/derivatives-page-13.jpg)

*원본 PDF p.13*

**OCR transcription**


### 1) 기초자산에서 발생하는 현금흐름 : 배당 dividends, 이자 interests

- 선물계약 만기 이전에 현물자산에서 배당/이자와 같은 현금흐름이 발생할 수 있음
- 보유기간동안 편익이 발생 -&gt; 보유비용을 감소시키는 효과
-&gt; 기초자산의 보정 : 선도계약 만기에 매수하는 기초자산은 중간에 발생한 현금흐름이 차감됨
£=0
Dvl
-
선도가의 = [So- PV of Benett x (1tr)
T
(r-b)-T
=
배영하, 이자소득등.
배당축, 쿠폰이자율 등.
-&gt; Dividend는 선도계약 long position이 아니라 주식보유자에게 귀속되기 때문에 기초자산 보유
비용에서 빼줘야 한다.
Cost of Carry Model 확장 2-&gt; 기초자산이 원자재인 경우 -&gt; 추가적인 비용과 편익이 발생

### 1) 추가적인 보유비용 : 보관비용(storage costs)

- 보유비용 : 원자재(commodity)의 보유 및 보관에 따른 창고임대료, 손상 가능성, 보험료 등
-&gt; 보유 비용을 늘리는 방향(선도가격을 늘리는 방향)으로 작용

### 2) 보유편익 : 현물 보유자에게 주어지는 비금전적인 혜택(convenience yield)

- Convenience yield : 원재자 부재 시 발생하는 불편과 비능률을 제거하는 이익
-&gt; 현물자산을 보유하고 있으면, 갑작스러운 공급 충격에 대응할 수 있음
-&gt; 보유 비용을 감소시키는 효과(선도가격을 줄이는 효과)

### 3) 선도가격

FolT= [So+PV of Cost - PV or Bonett ] x (1t))
= S: e(rtc-6): T

---

## Page 14. 6. Currency Forwards = FX forward

![Original Derivatives PDF page 14](/images/cfa/derivatives-pages/derivatives-page-14.jpg)

*원본 PDF p.14*

**OCR transcription**


### 1) 기초자산(underlying asset) : 외국통화(foreign currency)


### 2) 환율 표시방법

- 직접표시법 : 외국통화 한 단위의 가치를 자국 통화로 표시 -&gt; $1 = 1,200원
- 간접표시법 : 자국통화 한 단위의 가치를 외국통화로 표시 -&gt; 1원 =$1/1200

### 3) Spot trade(현물거래) vs forward trade(선도환거래)

- spot trade : 외환의 즉각적 인도를 조건으로 하는 거래(일반적으로 D+2 결제까지 현물로 인정)
-&gt; spot trade 에 적용되는 환율 : spot rate
- forward trade : 현물환거래(D+2) 이후를 결제일로 하는 외환거래
-&gt; forward trade에 적용되는 환율 : forward rate

### 4) 선도환율 forward rate은 어떻게 결정하는가? -&gt; interest rate parity(IRP)

- 모든 나라의 실질금리는 동일 -&gt; 각 국의 금리차는 환율에 의해 조정도기 때문이다
-&gt; 모든 나라의 실질금리가 동일하지 않으면 차익거래가 발생
- IRP : 국가 간 명목금리 차이가 존재하지만, 환율효과까지 반영하면 실질금리는 동일함
Cf) parity : 둘의 가치가 같아야 함을 의미
- Calculation
얘는 EUD 한 단위에 대한 USD의 단위
현문환율 5 , 선도환율 F
자주금리 (USD, Price Curenoy)= rp, 외국리 (EUR,Base aumency)= r6
자국통화 1단위 자국금리에 투자
tT
1x (It5]
이론상 두개의 가치가 같아야 항 -&gt;
자국통화 1단의를 EUR로 한전후 외국금리로 투자
후 T 시점에 재구통화로 파시 환전하기 위해 이 X (Itr6). F
선도한율로 1도

---

## Page 15. IxCIt@ S(Ita).F

![Original Derivatives PDF page 15](/images/cfa/derivatives-pages/derivatives-page-15.jpg)

*원본 PDF p.15*

**OCR transcription**

(I+t)

### 2) 경리면

Clthb)
#
F와 S가 직접표시법든 (F% 5) 간정표시법이든(Ty Sk)
- 아래에 있는 것을 BaeCineg로, 남로 두고 계산하면공, 등이며 Eu Gase!
(|+rg)
로 외우면 편함.!
(1tr)
Citg)-등 (ta)
(ltra)= Sns (ltrg)
Frry
eX) EVK (Bace Cumenay)해 3%, USD CPrice Cumenay) 금리 2%
(ltry) =3% (ltrx)= 2% Sx= 1:1
( (tVy)
Fry: Syy
(103)
= $ 10893
Cltra)
(1.02)

---

## Page 16. 7. 이산복리 연속복리

![Original Derivatives PDF page 16](/images/cfa/derivatives-pages/derivatives-page-16.jpg)

*원본 PDF p.16*

**OCR transcription**

원금 1원, 이자율 2% , 만기 t= T
Arnual
1 x Clt2%)
Semi annual
1 x Cl+¾½)F2
Quarter
1X(1+2¼) 54
N
1× C1+¼)
Continuaus
1 x eT
학인율
1x (1+28) 7
1x (1+2x4) 27
1× (1+¼¼) 47
1x (1+25)-7
Ix etT
이산복지와 같은 수익률 (등가성을 갖는)을 갖는 연속복리 봐 (T= 일때)
(1.02) : erl
in (1+0.02)=r
r= in 1.02 = 0.0198 = 1.98%

---

## Page 17. 8. Valnation : 다양한 시점에서 선도계약의 가치

![Original Derivatives PDF page 17](/images/cfa/derivatives-pages/derivatives-page-17.jpg)

*원본 PDF p.17*

**OCR transcription**

Priang-성도가격의 결정. 6(T) S tot of Cony
Vo(T)=O 계약의 가치 0|IRP
IRP
TO(T)# O 선도가격은 D 아님.
tct'
-+
V: (T) - Valuation
현재시점의 선도계약의 가치
7 9y의 현다.
VCT)
Valuation
£=t
T-t
/t
만기시점 Vf(T) Payot : ST- Fo(T)
FoCT)=S.(tFf)"
3 Cost of Carry.
ST- Fo(T)
Fo(T)
tat'시정 Ve(T)= 2149JTit= S- cinfit
ta 시점 Vo(C) =
CIfrf)"
(Ir4)T
Fo(T) &gt; VoCT) =0

---

## Page 18. 기초자산에서 추가적인 Cost Beneft이 발생하는 경우

![Original Derivatives PDF page 18](/images/cfa/derivatives-pages/derivatives-page-18.jpg)

*원본 PDF p.18*

**OCR transcription**

- 선도가격이 달라짐.

### 7) 6atof Cong: 청주시자, 보이 피하고 보관편의 배고

만기시점 VICT) : Si-FotT) ,
FoCT= [So +PvCast - Pv Beneft] Cl+rg)
tat'
Ut (T) :
ST -Fo(T)
FoC)
( 1+rg)tt
= S 1PY Cast- PV Benett- Cinfiet
ST-Fo(T)
아까
- 에서
( Itt)T
3.- 50(
ChA 가 되는 논리는 만기시점의 SP를
어떻게 현재로 가져을 것이냐, 만기의 Sp라는 현금흐름을 어떻게 복제해야 했을 때
So를 사는 것 밖에 없다. 라는 논리가 있었음.
같은 논리로
VE(T) :
ST-HOCT)
CIttpIC 에서 이번에는 의를 복제하는
과정에서 보관비와 편익이 발생하니 St+ PY (ast -PV Benettr이
되는 것이다.
V.(T)=0

---

## Page 19. 9. Forward Rate Agreement(선도금리계약) -&gt; interest Rate Forward

![Original Derivatives PDF page 19](/images/cfa/derivatives-pages/derivatives-page-19.jpg)

*원본 PDF p.19*

**OCR transcription**

- FRA : 미래의 일정 구간 동안 적용할 금리를 미리 약정하는 계약
-&gt; 미래의 금리를 사고 팔기로 약정하는 계약
-&gt; 지금 현재시점에서 미래의 forward rate을 거래하는 것
- underlying asset : 미래의 일정 구간동안 적용할 금리 -&gt; 선도금리
- FRA 기초자산으로 가장 많이 활용되는 금리: SOFR, MRR, Eurodollar deposit 거래에 적용되는 금리
-&gt; Eurodollar deposit : 미국이 아닌 다른 지역의 은행에서 달러를 기초로 거래되는 예금
S2
t=0
t=T
기초자산
기초자산의 만기시점
3 T= 0 시점에 1남 거래하는 것.
(1+Sa)+= (1+S)(1+1816)
50(7) = (1+1818)
(1fS2)}
( I+S,)
FRA position
- FRA long position : 선도금리를 미리 사는 계약 -&gt; 금리 상승위험이 있는 사람이 매입
-&gt; 금리 상승위험을 회피하기 위함
-&gt; 현물포지션 : 돈을 빌리려고 하는 사람
ex) fixed bond long, FRN issue한 사람, 미래 시점에 대규모 차입을 해야하는 사람
- FRA short position : 선도금리를 미리 파는 계약 -&gt; 금리 하락위험이 있는 사람이 매입
-&gt; 금리 하락위험을 회피하기 위함
-&gt; 현물포지션 : 돈을 빌려주려고 하는 사람
ex) fixed bond short 친 사람, FRN Iong한 사람, 미래에 대규모 자금이 들어오는 사람
Fixed bond short : 채권을 빌려서 팔아서 더 싼값에 매입해야 이득
금리가 상승해서 채권의 가격이 떨어지는 것을 노려야함
금리가 하락한다면 채권의 가격이 상승해서 채권 숏 포지션에서 손해를 본다 -&gt; FRA short으로 헷지

---

## Page 20. FRA - 금리 위험의 Hedge

![Original Derivatives PDF page 20](/images/cfa/derivatives-pages/derivatives-page-20.jpg)

*원본 PDF p.20*

**OCR transcription**

- FRA long position 예시
Company A : 30일 후에 90일간 자금을 차입할 예정 -&gt; 차입금리 : 90-day SOFR
{
Borrow qo days
t=h0
t=120
Company A가 직면한 위험 : 30일 후에 금리가 상승할 위험
-&gt; 금리를 미리 사는 계약을 체결해야함 -&gt; forward long position
-&gt; 30일 후에, 90-day SOFR가 상승한 경우 Forward 계약에서 이익 발생 -&gt; 금리 상승위험 헷지
- FRA short position 예시
Company B : 30일 후에 90일간 자금을 대출해줄 예정 -&gt; 대출금리 90-day SOFR
Lend tor go darys
t=0
t=30
to 2odays
Company B가 직면한 위험 : 30일 후에 금리가 하락할 위험
-&gt; 금리를 미리 파는 계약을 체결해야함 -&gt; forward short position
-&gt; 30일 후에, 90-day SOFT가 하락한 경우 Forward 계약에서 이익 발생 -&gt; 금리 하락위험 헷지

---

## Page 21. FRA Pricing

![Original Derivatives PDF page 21](/images/cfa/derivatives-pages/derivatives-page-21.jpg)

*원본 PDF p.21*

**OCR transcription**

- 기초자산(underlying asset) : 미래의 일정 구간동안 적용할 금리 -&gt; 선도금리
- FRA pricing : 미래 구간의 금리를 Forward rate으로 거나 팔자고 약정하면 no arbitrage
-&gt; Underlying asset이 SOFR과 같은 단기금리인 경우, 금리에 대한 Market convention은 "단리"
예시: 3mbm Nith notonal princral 41000 Rraing
31월 후 6개월짜리 금리가 기초자산
6M
[=0
t=3M
t=9M
3M MKR =1% , 9M MRR= 1.2% - HAR은 Cmva, 기준
(1+ 1.2%x음)= (I+AX)(I+ 3m6mx 음) "단리계산"
3mbm= 1.3% - 얘도 annual
복리 (l+ San )
A% (1+Sm)"PCi+ 3mon) Aa
t=3m 시점에서 Sem = 2%라면? FRA long paition 이라면 0.7% 이틀
5=3m 시점에서 Som = 1X 라면? FRA long pasifion 이라면 0. 3% 이득.
- 금리가 기초자산인 상품, 특징- 용어
Notional Frinciple : 계약서 상의 원금
Amuatized rafe: MRK, Fornard rate 등은 모두 영환산 공리.
Arear 위
Day comt adjustent

---

## Page 22. FRA Payott and Settement

![Original Derivatives PDF page 22](/images/cfa/derivatives-pages/derivatives-page-22.jpg)

*원본 PDF p.22*

**OCR transcription**

PAYA: 파생상품 계약 만기시점의 기치
FRA POSOP = Notional Princpal x (5-F) X D360
-
-
T53m
Som은 이 시점에서 확정
- 근데 그 금리가 적용되는 대상은 그 이후 6개월.
3 그래서 PO4O는 9m 시점의 이자차이
- 하지만 실제 FRA는 그럴 3m 시점에 확인해서 바크 정산.
ex) Poyotig: (1.57-1.32) X 8IM X 6R = 91000.
^
NP
이라는 POR는 9n에서 발생.
이를 3m으로 현기한해서 3m(만기시점)에 바로 정산.
81000
Setienent=-
-=$992.56
(1+ 15%×62)
t2 qm
{
P맹OP 학정

---
