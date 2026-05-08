---
title: "Pricing and Valuation of Options (Reading 70)"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Options, Put Call Parity, Binomial Model, Reading 70]
excerpt: "Sihyun CFA Notes - Pricing and Valuation of Options (Reading 70)"
---

## Quick Take

- 중심 주제: **Pricing and Valuation of Options**
- 먼저 잡을 축: Options vs forwards, 옵션계약 options, 행사방법에 따른 분류
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Options vs forwards
2. 옵션계약 options
3. 행사방법에 따른 분류
4. Option payoff
5. Option P/L과 break-even point
6. Moneyness
7. 옵션의 현재 시점 가치
8. 옵션가격과 변수의 관계
9. 옵션가치와 잔존만기
10. Put-call parity
11. Synthetic position
12. Put-call forward parity

## Main Notes

## 1. Options vs forwards

| 구분 | Options contract | Forwards contract |
|---|---|---|
| 계약의 성격 | Long position은 권리, short position은 의무 | Long position과 short position 모두 이행의무 |
| 초기비용 | 초기비용 initial cost > 0, option premium 존재 | 초기비용 = 0 |

## 2. 옵션계약 options

옵션계약은 특정자산을 특정 미래 시점 또는 그 이전에 약정된 가격으로 살 수 있거나 팔 수 있는 권리이다.

### 옵션계약의 구성항목

| 구성항목 | 내용 |
|---|---|
| 기초자산 S | 권리 행사 시 매수 또는 매도의 대상이 되는 특정자산 |
| 만기 expiration date, T | 권리를 행사할 수 있는 특정 시점 또는 일정 기간의 마지막 날 |
| 행사가격 exercise price, K | 권리를 행사할 때 적용되는 가격 |
| 옵션 프리미엄 option premium | 옵션을 매입할 때 지불하는 비용 |
| 포지션 position | 투자자의 현재 상태 |

옵션은 권리이기 때문에 옵션을 매입할 때 비용이 발생한다.

| 포지션 | 내용 |
|---|---|
| Long | 프리미엄을 지불하고 옵션을 매입한 사람 |
| Short | 프리미엄을 받고 옵션을 매도한 사람 |

### Call option

콜옵션은 살 수 있는 권리이다.

| 포지션 | 내용 |
|---|---|
| Call option long position | 옵션프리미엄을 지불하고 기초자산을 살 수 있는 권리 보유 |
| Call option short position | 옵션프리미엄을 받고 기초자산을 팔아야 할 의무 부담 |

### Put option

풋옵션은 팔 수 있는 권리이다.

| 포지션 | 내용 |
|---|---|
| Put option long position | 옵션프리미엄을 지불하고 기초자산을 팔 수 있는 권리 보유 |
| Put option short position | 옵션프리미엄을 받고 기초자산을 사야 하는 의무 부담 |

## 3. 행사방법에 따른 분류

| 옵션 | 행사 가능 시점 |
|---|---|
| European option | 옵션의 만기에 한 번만 행사가능, at expiration date |
| American option | 옵션의 만기일을 포함하여 언제든지 행사가능, at any time |

American option 보유자는 두 가지 선택권을 가진다.

- European option: 만기에 옵션 행사
- Early exercise option: 만기 이전에도 옵션 행사

American option 보유자는 두 옵션을 모두 보유하므로 두 옵션 중 큰 값이 American option의 가치이다.

$$American\ option\ value=MAX(European,\ early\ exercise)$$

$$American\ option\ value \ge European\ option\ value$$

## 4. Option payoff

Payoff는 만기시점 옵션의 가치이다. Premium은 sunk cost이므로 옵션 행사 여부에 영향을 주지 않는다.

| 포지션 | 행사 조건 | Payoff | Max profit | Max loss |
|---|---|---|---|---|
| Call option long | ST > K일 때 행사 | Max(0, ST - K) | Unlimited | -Premium |
| Call option short | ST > K일 때 행사당함 | -Max(0, ST - K) | Premium | Unlimited loss |
| Put option long | ST < K일 때 행사 | Max(0, K - ST) | K - Premium | -Premium |
| Put option short | ST < K일 때 행사당함 | -Max(0, K - ST) | Premium | -K + Premium |

## 5. Option P/L과 break-even point

| 포지션 | Break-even point |
|---|---|
| Call long | K + Premium |
| Call short | K + Premium |
| Put long | K - Premium |
| Put short | K - Premium |

## 6. Moneyness

Moneyness는 payoff 기준이다.

| 구분 | 의미 |
|---|---|
| In the money, ITM | 옵션 행사 시 이득인 상태 |
| At the money, ATM | 손해도 이득도 아님 |
| Out of the money, OTM | 지금 행사하면 손해 |
| Deep ITM | 개이득 |
| Deep OTM | 개손해 |

## 7. 옵션의 현재 시점 가치

옵션의 가치는 내재가치 intrinsic value와 시간가치 time value of money로 나뉜다.

$$Option\ value=Intrinsic\ value+Time\ value$$

### 내재가치

내재가치는 현재시점에서 옵션이 행사된다고 가정했을 때 얻게 되는 가치이다.

| 옵션 | 내재가치 |
|---|---|
| Call option | Max(St - K, 0) |
| Put option | Max(K - St, 0) |

예시:

- St = 55
- K = 50

| 옵션 | Intrinsic value |
|---|---|
| Call option | Max(5, 0) = 5 |
| Put option | Max(-5, 0) = 0 |

### 시간가치

시간가치는 옵션의 만기까지 기초자산 가격변화에 따라 이익을 얻을 수 있는 가능성에 대한 가치이다.

Deep out of the money인 상황이어도 남은 기간 동안 기초자산 가격이 오르거나 내릴 가능성이 있다. 이것이 time value이다.

## 8. 옵션가격과 변수의 관계

옵션가격은 다음 변수들의 함수이다.

$$C_t=f(S,K,r,T,\sigma)$$

만기시점에는 time value가 0이다. 더 이상 가능성이 없기 때문이다.

### 변수와 옵션가치의 상관관계

| 변수 증가 | European call | American call | European put | American put |
|---|---|---|---|---|
| 기초자산 St | 증가 | 증가 | 감소 | 감소 |
| 행사가격 K | 감소 | 감소 | 증가 | 증가 |
| 무위험수익률 r | 증가 | 증가 | 감소 | 감소 |
| 변동성 | 증가 | 증가 | 증가 | 증가 |
| 잔존만기 T - t | 일반적으로 증가 | 증가 | 일반적으로 증가 | 증가 |
| 보유편익: dividend, coupon | 감소 | 감소 | 증가 | 증가 |
| 보유비용 | 증가 | 증가 | 감소 | 감소 |

옵션은 주가가 하락하면 행사하지 않으면 그만이므로 변동성이 커질수록 가치가 커진다.

배당이 있는 주식의 경우 배당락이 발생할 수 있다. 유러피언 옵션은 배당락 전에 조기행사가 불가능하다.

## 9. 옵션가치와 잔존만기

잔존만기가 길어지면 일반적으로 옵션의 가치는 커진다. Time value가 증가하기 때문이다.

예외:

- 배당주식에 대한 European call option
- Deep ITM European put option

### 콜옵션

일반적으로 잔존만기가 길수록 콜옵션의 가치가 커진다.

- Call option의 upside potential은 unlimited
- 배당이 지급되는 주식이 기초자산인 European call option은 예외일 수 있음
- 기초자산에서 배당금이 지급되는 경우, 잔존만기 증가에 따른 옵션 가치 하락폭 배당락이 시간가치 상승폭보다 클 수 있음
- American option은 이 상황이 예상되면 조기행사하면 됨

### 풋옵션

일반적으로 잔존만기가 길수록 풋옵션의 가치가 커진다.

예외는 deep ITM European put option이다.

- Deep ITM인 경우 put option의 upside가 극히 제한적
- 하방은 뚫려 있음
- 이 경우 만기가 짧은 것이 유리할 수도 있음
- 만기가 길면 주가가 다시 상승할 위험이 있음
- American put option은 deep ITM이면 조기행사하면 되므로 만기가 길수록 가치가 커짐

## 10. Put-call parity

Put-call parity는 기초주식 S, 만기 T, 행사가격 K가 동일한 European call option과 put option 가격 사이에 성립하는 관계식이다.

$$Protective\ Put=Fiduciary\ Call$$

European call option과 put option의 경우에만 성립하며 American option에는 성립하지 않는다.

### Protective put

기초자산을 매입하고 put option을 매수하는 포지션이다.

- 기초자산 가격 하락 위험을 hedge하기 위해 put option 매수
- Long S + Long P

### Fiduciary call

Call option을 매수하고 call option 행사에 필요한 금액, 즉 행사가격을 무위험채권으로 보유하는 포지션이다.

- 행사시점에 행사가격 K를 받을 수 있는 zero coupon bond를 매수하는 것
- Long C + Long K / (1 + r)^T
- Fiduciary call은 naked call과 반대말

### 만기 payoff 비교

| 만기 주가 | Protective put | Fiduciary call |
|---|---|---|
| ST ≥ K | Long S = ST, long P = 0 → payoff = ST | Long C = ST - K, bond = K → payoff = ST |
| ST < K | Long S = ST, long P = K - ST → payoff = K | Long C = 0, bond = K → payoff = K |

Protective put과 fiduciary call의 payoff는 만기 주가 수준과 상관없이 항상 동일하다.

동일한 payoff를 갖는 두 자산은 동일한 가격이어야 한다.

$$S_0+p_0=c_0+\frac{K}{(1+r_f)^T}$$

정리:

$$p_0=c_0-S_0+\frac{K}{(1+r_f)^T}$$

$$c_0=S_0+p_0-\frac{K}{(1+r_f)^T}$$

### 예시

- S = $52
- rf = 5%
- 3 month
- K = 50
- Put = $1.50

3개월 50 call value:

$$c=S+p-\frac{K}{(1+r_f)^T}$$

$$c=52+1.50-\frac{50}{1.05^{1/4}}=4.11$$

## 11. Synthetic position

합성포지션은 서로 다른 금융상품을 결합하여 새로운 형태의 금융상품 포지션으로 합성하는 것이다.

| 합성포지션 | 식 |
|---|---|
| Synthetic stock | S = C - P + K / (1 + r)^T |
| Synthetic put | P = C - S + K / (1 + r)^T |
| Synthetic call | C = S + P - K / (1 + r)^T |
| Synthetic bond | K / (1 + r)^T = S + P - C |

## 12. Put-call forward parity

Put-call parity:

$$P_0+S_0=C_0+\frac{K}{(1+r_f)^T}$$

Forward price:

$$F_0(T)=S_0(1+r_f)^T$$

따라서:

$$S_0=\frac{F_0(T)}{(1+r_f)^T}$$

Put-call forward parity:

$$P_0+\frac{F_0(T)}{(1+r_f)^T}=C_0+\frac{K}{(1+r_f)^T}$$

## 13. 옵션평가 모형을 활용한 기업가치 측정

| 항목 | 의미 |
|---|---|
| V | 기업가치 |
| D | 채권자가치 |
| E | 주주가치 |

주주가치:

| 상황 | E |
|---|---|
| V > D | V - D |
| V < D | 0 |

$$E=Max(0,V-D)$$

이는 long call payoff와 유사하다.

채권자 가치는 만기에 D를 주는 zero coupon bond와 short put option의 조합으로 볼 수 있다.

$$Debt\ value=D-Max(D-V,0)$$

## 14. Boundary condition

### European option

만기 시점:

$$C_T=Max(0,S_T-K)$$

$$P_T=Max(0,K-S_T)$$

옵션의 가치는 내재가치보다 크거나 같아야 한다. 시간가치가 0 이상이기 때문이다.

European call lower bound:

$$C_0^E \ge Max\left(0,S_0-\frac{K}{(1+r_f)^T}\right)$$

European put lower bound:

$$P_0^E \ge Max\left(0,\frac{K}{(1+r_f)^T}-S_0\right)$$

### American option

American option은 European option과 early exercise option 중 큰 값이다.

$$American\ option=Max(European\ option,\ Early\ exercise\ option)$$

American call:

$$C_0^A \ge Max\left(S_0-\frac{K}{(1+r_f)^T},0\right)$$

American put:

$$P_0^A \ge Max(K-S_0,0)$$

Maximum value는 각 minimum value에서 음수 항목을 모두 0으로 취급한다.

### 예시: put option minimum value

- 4m American, European put
- K = 65
- S = 63
- rf = 5%

European put:

$$P^E=Max\left(\frac{K}{(1+r_f)^T}-S_0,0\right)=0.95$$

American put:

$$P^A=Max(K-S_0,0)=2$$

### 예시: call option minimum value

- 3m American, European call
- K = 65
- S = 68
- rf = 5%

$$C^E=Max\left(S_0-\frac{K}{(1+r_f)^T},0\right)=3.79$$

$$C^A=3.79$$

## 15. Option valuation: binomial tree model

Option valuation은 t = t' 시점에 옵션의 현재가치를 평가하는 것이다.

만기 call payoff:

$$C_T=Max(S_T-X,0)$$

t = 0에서는 ST를 알 수 없으므로 확률분포를 활용한다.

Option valuation model 또는 option pricing model:

- Black-Scholes formula
- Binomial tree model
- Monte Carlo simulation

## 16. Binomial tree model: hedged portfolio method

기초자산 수익률이 이항분포를 따른다고 가정한다. 만기의 주가는 일정한 비율로 up 또는 down한다.

$$S_u=S_0(1+u)$$

$$S_d=S_0(1+d)$$

예시:

- S0 = $50
- Su = $60
- Sd = $42
- u = 1.2
- d = 0.84

$$S_u=50(1.2)=60$$

$$S_d=50(0.84)=42$$

### Call option에 대한 hedged portfolio 구축

- Call option 행사가격 K = 55
- Hedged PF = short call + h × long stock
- 주가가 움직여도 hedged PF의 가치는 변하지 않는다.
- h는 hedge ratio, 즉 option delta

Call option은 기초자산인 주가가 움직일 때 delta만큼 가격이 변동하는 민감도를 가진다. 따라서 주식을 h개만큼 보유하면 short call의 손익과 주식 손익이 상쇄되어 hedged PF 구축이 가능하다.

### 계산

Hedged PF의 현재가치:

$$V_0=-C_0+hS_0$$

Up state:

$$V_u=-C_u+hS_u=-Max(0,S_u-K)+hS_u$$

Down state:

$$V_d=-C_d+hS_d=-Max(0,S_d-K)+hS_d$$

숫자로:

$$-5+60h=42h$$

$$18h=5$$

$$h=0.278$$

따라서 Vu = Vd = $11.68.

무위험수익률 rf = 3%라면:

$$V_0=\frac{11.68}{1.03}=11.34$$

그리고:

$$-C_0+0.278\times50=11.34$$

$$C_0=2.56$$

## 17. Binomial model with risk-neutral valuation

Risk-neutral probability를 사용한다.

| 기호 | 의미 |
|---|---|
| U | 1 + u |
| D | 1 + d |
| πu | 오를 확률 |
| πd | 내릴 확률 |

기대값:

$$E(S)=S_0U\pi_u+S_0D\pi_d$$

Risk-neutral 조건:

$$1+r_f=U\pi_u+D\pi_d$$

$$\pi_u=\frac{1+r_f-D}{U-D}$$

$$\pi_d=1-\pi_u$$

V와 D, rf를 주면 πu와 πd를 구해서 binomial tree model을 사용한다.

### 예시

- S0 = $30
- K = $30
- rf = 7%
- U = 1.15
- D = 0.87

Up state:

$$S_u=S_0(1+u)=30(1.15)=34.5$$

$$C_u=Max(S_u-K,0)=Max(34.5-30,0)=4.5$$

Down state:

$$S_d=S_0(1+d)=30(0.87)=26.1$$

$$C_d=Max(S_d-K,0)=0$$

Risk-neutral probability:

$$\pi_u=\frac{1.07-0.87}{1.15-0.87}=71.5\%$$

$$\pi_d=28.5\%$$

Risk-neutral expected stock value:

$$E(S_T)=34.5\times71.5\%+26.1\times28.5\%=32.1=30\times1.07$$

Call option value:

$$C_0=\frac{4.5\times71.5\%+0\times28.5\%}{1.07}=3.01$$
