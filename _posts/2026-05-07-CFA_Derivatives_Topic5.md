---
title: "CFA Derivatives Topic 5 - Pricing and Valuation of Options"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Options, Put Call Parity, Binomial Model]
---

이 글은 Derivatives PDF의 Topic 5 필기를 축약하지 않고, 옵션 payoff, moneyness, put-call parity, boundary condition, binomial model까지 원래 흐름대로 옮긴 버전이다.

## Page 38. TopiC 5 : Pricing and Valuation of Options

![Original Derivatives PDF page 38](/images/cfa/derivatives-pages/derivatives-page-38.jpg)

*원본 PDF p.38*

**OCR transcription**

Options vs Forwards
구분
계약의 성격
초기비용
pitions contract
Ang postions 권리안
Short postions 의무안
- 초기비용(inita ast) f0
option premium
Forwards Cortract
rong positions : 이행의우
Short postions : 이행의무
- 초기비용 = 0
1. 옵션계약(options)
- 특정자산을 / 특정 미래 시점 또는 그 이전에 / 약정된 가격으로 / 살 수 있는 / 팔 수 있는 권리
2. 옵션계약의 구성항목
- 기초자산 S : 권리 행사 시 매수 도는 매도의 대상이 되는 특정자산
- 만기(expiration date T) : 권리를 행사할 수 있는 특정 시점 또는 일정 기간의 마지막 날
- 행사가격(Exercise price K) : 권리를 행사할 때 적용되는 가격
- 옵션 프리미엄(option premium) : 옵션을 매입할 때 지불하는 비용
-&gt; 권리이기 때문에 옵션을 매입할 때에는 비용이 발생
- 포지션: 투자자의 현재상태
-&gt; long : 프리미엄을 지불하고, 옵션을 매입한 사람
-&gt; short : 프리미엄을 받고, 옵션을 매도한 사람
- 콜옵션(call option) : 살 수 있는 권리
-&gt; call option long position : 옵션프리미엄을 지불하고 기초자산을 살 수 있는 권리를 보유
-&gt; call option short position : 옵션프리미엄을 받고 기초자산을 팔아야 할 의무를 짐
- 풋옵션(put option) : 팔 수 있는 권리
-&gt; put option long position : 옵션프리미엄을 지불하고 기초자산을 팔 수 있는 권리를 보유
-&gt; put option short position : 옵션프리미엄을 받고 기초자산을 사야하는 의무를 짐

---

## Page 39. 3. 행사방법에 따른 분류

![Original Derivatives PDF page 39](/images/cfa/derivatives-pages/derivatives-page-39.jpg)

*원본 PDF p.39*

**OCR transcription**


### 1) European options : 옵션의 만기에 한 번만 행사가능 -&gt; at expiration date


### 2) American options : 옵션의 만기일을 포함하여, 언제든지 행사가능 -&gt; at any time

•아메리칸 옵션 보유자의 2가지 선택권
-&gt; European option : 만기에 옵션행사
-&gt; Early exercise option : 만기 이전에도 옵션행사
-&gt; american option 보유자는 2가지 옵션을 모두 보유하고 있으므로,
2개의 옵션 중 큰 값이 아메리칸 옵션의 가치
-&gt; american option value = MAX(European, early exercise)
- American option value &gt;= European option value
4. Option payoff : 만기시점 옵션의 가치
Poyot
K
BFP
A Payott
K
*
Max prott : 60
Call option long pastion
Max Loss:-Premium
주가 ST가 행사가격 K보다 클경우 행사
Payoff : Max (o,St-K)
Call option short postion
Max Troht: Prenium
주가 ST가 행사가격보다 클 때 행사당함.
Max IoSS : - 8
Poy 9P:-Max(o,k-Sr)
Per option Short postion
주가 ST가 K보파 작을 때 행사당함
Payoff:-Max(o.st-k)
Max prohit : Pr
MOX loss : - Mtpr
BED
Pagot : 연프리미일 고려 X
ASunken cost로 옵션행사 여부에
영향을 주지 않는다.
Pat ortion long Poston
주가 ST가 청사가격 K보다 작을 때 행사
Payoff Max Co. K-ST)
Max proft: k-ir
Max loss: -Pr

---

## Page 40. 옵션의 Poyott:/P/L

![Original Derivatives PDF page 40](/images/cfa/derivatives-pages/derivatives-page-40.jpg)

*원본 PDF p.40*

**OCR transcription**

Coll-long
Cal Short
/PAL
Pat long
BED: K-Pr
KPr
B?:
K-Rr
PL
5. Moneyness (Payott) 기준)
In the Money (ITM) : 옵연 행사 시 이득인 상태
At the Money (AIM) : 손해도 이들도 아님.
Dut of the Morg(0) : 지금행사하면 손해
Dee ITM : 개이득, Deo OTM : 개손해
K
BEP: kt pr

![Payoff profiles for long call short call long put and short put options](/images/cfa/derivatives-topic5-option-payoffs.svg)

*네 가지 기본 옵션 포지션의 payoff 방향을 확인하기 위한 보조 그림.*

---

## Page 41. 6. 옵션의 현재 시점에서의 가치

![Original Derivatives PDF page 41](/images/cfa/derivatives-pages/derivatives-page-41.jpg)

*원본 PDF p.41*

**OCR transcription**

옵션의 가치 = 내재가치(Trtrinsic value)+ 시간가치(Tine Vane of maney)
Vt
Time value
④
intrinsic Valve
St
Deep Ourt o the money
X
인 상황이지만 여전히
T-t 기간동안 SK가 이게 바로 Time Value : 남은 시간동안 기초자전의 가격이 올/내릴 가능성.
상승할 가능성은 있다.

### 1) 내재가치 : 현재시점에서 옵션이 행사된다고 가정했을 때 얻게 되는 가치

- 기초자산의 현재가격과 행사가격의 차이
- 콜옵션의 내재가치 = Max (St -k, 0)
- 풋옵션의 내재가치 = Max CK-St, o)
St=55 K=50 라면
Call option Intinsic value Max (5:0) =5
PuT ostion
"
MaX (-500)=0

### 2) 시간가치 : 옵션의 만기까지 기초자산 가격변화에 따라 이익을 얻을 수 있는 가능성에 대한 가치

---

## Page 42. 옵션가격과 변수와의 관계

![Original Derivatives PDF page 42](/images/cfa/derivatives-pages/derivatives-page-42.jpg)

*원본 PDF p.42*

**OCR transcription**

Gt:fCSR,r, T, 8) 각변수가 Optim의 가치에 어떤 영향을 주나?
무위험이자율
〈call option 〉
t=t'
-
discount
^
C 2 Max (Si-ontift, 0)
&lt;Put option)
t=t'
G= Max (ST-K,O)
이때 time Value는 O.
만기시점에는 더 이상 가능성 x
discount
R2 Max (cnTi -St,0)
&lt; 변수와 옵션가치의 상관관계&gt;
Call
Eurepean
④
t=T
-Pf=Max(K-S, 0)
Put
American
기초자산 St
행사가격 K
무위험수익률 다
변동성 I
잔존만기(T-t)
2유편의 : Div, Couron
보유비용
옵션은 주가가 하락하면
행사하지 않으면 그만이라
변동성이 커서 더 많이
상승하여 행사하는게 서음
배당이 있는 주식의 경우
? (+)
만기 전 배당락이 있을 수
있는데 유러피언은 이때
조기 행사 불가.
+

### 2) SE를 어디에 위치시키나?

①
Q
④
European
Q
얘도 같은논리.
안하면 그만.
미꺼 상황인에 Rit-Iong
? (+) 포지션은 먹물게 많이 없다 어차피
④ 배당락, Loupon 지급
- St 하락 초래
American
①
①
+

---

## Page 43. 8. 옵션가치와 잔존민기

![Original Derivatives PDF page 43](/images/cfa/derivatives-pages/derivatives-page-43.jpg)

*원본 PDF p.43*

**OCR transcription**

- 잔존만기가 길어지면, 일반적으로 옵션의 가치는 커짐 -&gt; time value 증가
- 예외 -&gt; 배당주식에 대한 유러피언 콜옵션, Deep ITM 유러피언 콜옵션

### 1) 콜옵션

- 일반적으로는 잔존만기가 길수록 콜옵션의 가치가 커짐
-&gt; call option's upside potential -&gt; unlimited
- 배당이 지급되는 주식이 기초자산인 유러피언 콜옵션의 경우 예외일 수 있음
-&gt; 기초자산으로부터 배당금이 지급되는 경우
-&gt; 잔존만기 증가에 따른 옵션의 가치의 하락폭(배당락)이 시간가치의 상승폭보다 더 클 수 있다
-&gt; 아메리칸 옵션의 경우 위의 상황이 예상된다면 조기행사하면 됨

### 2) 풋옵션

- 일반적으로는 잔존만기가 길수록 풋옵셥의 가치가 커짐
- 예외 -&gt; Deep ITM 유러피언 콜옵션의 경우에는 예외일 수 있음
-&gt; Deep ITM인 경우, 풋옵션의 upside가 극히 제한적, 하방은 뚫려있음
-&gt; 이 경우, 만기가 짧은 것이 유리할 수도 있음
-&gt; 만기가 길 경우, 주가가 다시 상승할 위험이 있음
- 아메리칸 풋옵션은 만기가 길수록 풋옵션의 가치가 커짐
-&gt; Deep ITM의 경우, 풋옵션을 조기행사하면 됨
9. 풋콜 패러티(put - call parity)
- 기초주식(S), 만기(T), 행사가격(K)가 동일한 유러피언 콜옵션과 풋옵션의 가격 사이에 성립하는
일정한 관계식
- Protective Put = Fiduciary Call
- 유러피온 콜옵션과 풋옵션의 경우에만 성립(아메리칸 옵션에는 성립하지 않음)

### 1) Protective put

- 기초자산을 매입하고, 풋옵션을 매수하는 포지션
- 기초자산 가격의 하락 위험을 헷지하기 위해서 풋옵션을 매수하는 포지션
- Long S + Long P

### 2) Fiduciary Call

- 콜옵션을 매수하고, 콜옵션 행사에 필요한 금액(=행사가격)을 무위험채권으로 보유하고 있는 포
지션 -&gt; 행사시점에 행사가격 K를 받을 수 있는 zero coupon bond를 매수하는 것
- Long C + Long K(1+R)^T
- Fiduciary Call은 Naked Call과 반대말

---

## Page 44. I) Protective put

![Original Derivatives PDF page 44](/images/cfa/derivatives-pages/derivatives-page-44.jpg)

*원본 PDF p.44*

**OCR transcription**


### 2) Fiduciary Call

만기시절
만기시점
S2K
Long S sT
SAK
누
Max (KS,0)
=kST
SK
LOgC Malito) Max Srykio)
=ST-K
NHT
Foyot StO=2 2+K-S-K Pagotf
k
3 Potecte poto FAuciarg Cl의 Py에#가 만기의 주가 수준에 상관없이 항상 동일
- 동일한 Pay에를 갖는 두 자산-&gt; 등일한 가격.
C+P= C+ K/cititT
P= C- S t
NcitAT
[- st P-MettyT
Promple Cal opion volation wing pt calipity
5- 852, F=52 3month 50 pats = $150
Eslinate 3m 50 Colls.
Gtp=Ct KtE
C= ato -k/CtrAyT
•#52+815-50610514 - 54.11

---

## Page 45. 3) 합성포지션 (Synthetic postion)

![Original Derivatives PDF page 45](/images/cfa/derivatives-pages/derivatives-page-45.jpg)

*원본 PDF p.45*

**OCR transcription**

- 서로 다른 금융상품을 결합하여 새로운 형폐의 궁융상품 포지션으로 합성하는 것.
- Sarthetic stocks: S= Cp+K/CH)T
Synthe Put : P=C-S+K/CItHA)T
synthetic Cal:C= Stp-k/(ltr4)T
oynthett bond: Klittyi= 8tp-C

### 4) Put call Foruard Parity

Pot call parity : Pot So= CotK/ CIttP)T
Put call Foruard Parity
Fo(T)= So(Itrf)T a S= CmsT
Do+Fo(r)/CHr)T= Co +K/city)

### 5) 옵션평가 3형을 활용한 기업가치 측정

기업가치 V, 채권자가치 D, 주주가치 트
E= V- D
TA VOD
= O
TA VAD Cho resTdual )
Caloption Pg과 유사
주주가치 E = Max (0, V-D) = long Coll
U = D
if V&gt;D
= V
FVCD
채전자 가치= 만기에 D를 구는 4ZC3 + @art pat option.
•D - Max(D-V,O) ig V2D HD, VD-V

---

## Page 46. 10. Boundary Condition

![Original Derivatives PDF page 46](/images/cfa/derivatives-pages/derivatives-page-46.jpg)

*원본 PDF p.46*

**OCR transcription**


### 1) European Option

5=0
discount.
t=T
Cf= Max (O,St-k) 내재가치
FT= Max Co, K-ST) 내재가치
CoF 2 Max (0, 5.- 5ltrp)F )
옵션의 가치는 내재가치보다는
PoE 2 NX(O,K/CHrA)-5) 크거나 같아야 함 (시간가치20)

### 2) American Option

Americon option- Max (European option, Fary Everise option)
〈coll option〉
O Earpean call otion lauer boad Max Co, 50-K/CHA)T)
@ Eary exerse opition louerband- Max Co, So TK) 지금 행사한다고 가정.
S.-k/CIt) 2So-K a CoA2 Max(So-krHip7,0)
&lt; put option〉
O Earopean put option louer pound = Max Co, KIcitef)-50)
a Torly exercise ostion louer bound= Max (O, k-So)
KCItHAT-So&lt;K-So = FA 2 Max(k-50.0)
Maximun value는 각 Minimumn value 에서 (-) 항목들 모두 0으로 취급.

---

## Page 47. ex) Min Value of Americah, Europech put options.

![Original Derivatives PDF page 47](/images/cfa/derivatives-pages/derivatives-page-47.jpg)

*원본 PDF p.47*

**OCR transcription**

An/ANE 65m15/5-63/7.52
PE= Max (K/(tr4) 50, 0) = 0.95
PA= Max (K-50,0) 32
Min Valve of American W European Coll optrons.
3m/ AXE 65c/ St=68 119=57
GE= Mox (So- NeCH4)7,0) =3.79
Ca=Ma (So-fCttf)5, 0)= 379.
II option vanation : 이항모형 (Binomial tree model)
option Valnation : tat'시점에 옵션의 현재가치를 평가
aiscount
(= Max (S:-×,0)
ST에 대한 정보가 필요
- t= 시점에서 알수없으 학급분포를 학용
Orion Valuation model or option Pricing model
- Black Sholes Tormula
- Binomial tree model AWl.
- Monte Caro simulation.

---

## Page 48. 1) Binomial tree model Cheaged PF Method)

![Original Derivatives PDF page 48](/images/cfa/derivatives-pages/derivatives-page-48.jpg)

*원본 PDF p.48*

**OCR transcription**

- 기초자산의 수익률이 이항분포를 따른다고 기정 : 내기의 주가는 일정한 비율로 1P doum.
MSu= Sox (Itu)
Spoun = Sox Cltd)
Stu)
J,(td)
ex) S=$50 Su= $60 Sd= $42 V= 1.2, D=0.84.
54=$50xC1.2) = 460
So
Sd=550× (0.84)= $42
Call option 에 대한 Hedged Pf 구축
Cal option 행사가의 후 55 K 주가와 합연의 인장도
Heaged PF= Shorticall+ hx long stocks
주가가 움직여도 Hedged PF의 가치는 변하지 않은다.답
h: hedg Rato : Ce ortion datom)
Call option은 기초자산인 주가가 움직일 때, Delta 만큼 가격이 변동하는 민감도를 가지고 있다
-&gt; 따라서 주식을 h개 만큼 보유하고 있으면, short call의 손익과 주식의 손익이 상쇄되어
hedged PF의 구축이 가능하다

---

## Page 49. 60

![Original Derivatives PDF page 49](/images/cfa/derivatives-pages/derivatives-page-49.jpg)

*원본 PDF p.49*

**OCR transcription**

55
Hedged PF의 Vo=-C. th So
Vu=-Cu thSu= -Max (OrSu-k) thSu =-555:60
Va a-Cd thSd = -Max Co,Sa-k) thSd = 0+6:42
"^
42 55
주식이 모르는 내리든 Hedged PF 의 가지는 같아야 한다.
5+ 60h = 427
18h=5 h⅝= 0.28
-. Vu= Vo- $11.68
~ PV of Vu=Vd a Vu/(ltrf) = Vo
VF 7-3% 2
V Vo=-Coth So = 1.66/.03 = 11.34
~ -Co+ 0.278250 =11.34
~ Co= $256

---

## Page 50. 2냥외우자.

![Original Derivatives PDF page 50](/images/cfa/derivatives-pages/derivatives-page-50.jpg)

*원본 PDF p.50*

**OCR transcription**


### 2) Binomial mode with rist neutral Valvation

7S.U
오를 확률 T어
So
S.- D
내직 학률 지
E(So)= SoC ltu)- mu t SoCltd)Td
S.=
=
Tu=
C ltrf)
So . U. Tu t So. D.Ta
(I++4)
14441
V-)
U=|+4
D=ltd
riskmental
Td~|- Tu
V와 D, 5를 주면 Tu, TI를 구해서 Bmomial tree madel 사용.
So=$30 I=$30, 4=7K , V=1.15
D
다
S0 -$30
Co=
$4:5
'.07
7:56~&gt; 54= SoC(tu) =$30(1.15) =$34:5
Cu= Max (Su-K,o)- Max ($34:5-930.0)
2857)
- 9 45
Sd-So(l+d)=$30(0.87)=826.1
Cd= Max (Sa -510)= 0
× 715% 4
30X285= 43.0

---
