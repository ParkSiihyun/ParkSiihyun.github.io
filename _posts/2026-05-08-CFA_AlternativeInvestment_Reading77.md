---
title: "Alternative Investment Performance and Returns (Reading 77)"
date: 2026-05-08
categories: cfa
tags: [Alternative Investments, CFA Level I, Performance, XIRR, Hedge Fund Fees, Reading 77]
excerpt: "Sihyun CFA Notes - Alternative Investment Performance and Returns (Reading 77)"
---

## Quick Take

- 중심 주제: **Alternative Investment Performance and Returns**
- 먼저 잡을 축: 현금흐름 타이밍, J-curve, valuation hierarchy, redemption terms, return biases
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Timing of cash flows
2. XIRR, J-curve, MOIC
3. Valuation of investments
4. Redemption terms
5. Side letters and fee terms
6. Biases in AI returns
7. Hedge fund fee calculation

## Main Notes

## 1. Timing of cash flows

Alternative investment의 현금흐름은 phase별로 나누어 볼 수 있다.

| Phase | 내용 |
|---|---|
| Capital commitment phase | Investments를 identify하고 partners에게 capital calls를 하는 단계 |
| Capital deployment phase | Manager가 fund를 운용하고, 투자 대상 firms or projects에 직접 관여하는 단계 |
| Capital distribution phase | Returns가 positive로 전환되고 accelerate되는 단계 |

## 2. XIRR, J-curve, MOIC

### J-curve effect

Alternative investment는 초반 commitment/deployment phase에서 수익률이 낮거나 negative가 될 수 있고, 이후 capital distribution phase에서 returns가 크게 발생한다.

- Maximum returns는 capital distribution phase에서 발생한다.
- Commitment phase에서는 negative return이 나타날 수 있다.

### IRR and XIRR

IRR은 cash flow timing에 민감하다. AI에서는 capital calls와 distributions의 timing이 불규칙하기 때문에 XIRR을 사용해 성과를 보는 흐름이 중요하다.

### MOIC

MOIC는 Multiple of Invested Capital이다.

투자한 자본 대비 얼마를 회수했는지를 보는 성과지표이다.

## 3. Valuation of Investments

Alternative investment는 valuation이 어렵다.

### Fair value hierarchy

| Level | 내용 | 예시 |
|---|---|---|
| Level 1 | Exchange-traded securities처럼 관찰 가능한 시장가격이 있는 경우 | 상장증권 |
| Level 2 | 직접 가격은 없지만 관찰 가능한 inputs가 있는 경우 | 유사자산 가격 등 |
| Level 3 | 관찰 가능한 시장가격이 부족하고 valuation이 추정에 의존하는 경우 | PE, VC |

Level 3 자산은 fair value가 자주 변하지 않는 것처럼 보일 수 있다.

그 결과 AI의 reported returns는 실제보다 다음처럼 보일 수 있다.

- Higher
- Less risky
- Less correlated with traditional investments

## 4. Redemption

Redemption은 환매이다.

AI는 J-curve 특성상 초반 수익률이 낮을 수 있기 때문에, 수익률이 낮으면 투자자들이 환매를 원할 수 있다. 하지만 AI는 비유동적이므로 초반 환매를 금지하거나 환매수수료를 높게 책정하는 경우가 많다.

### Lockup period

Lockup period는 initial investment 이후 LP가 redemption을 요청할 수 없거나, redemption을 요청하면 significant fees를 부담해야 하는 기간이다.

### Notice period

Notice period는 fund가 redemption request를 fulfill하기 위해 필요한 시간이다.

- 환매를 위한 사전 통보 기간

### Redemption fees

Fund manager는 share redemption 과정에서 significant transaction costs를 부담할 수 있다.

- Redemption fees는 이 비용을 offset할 수 있다.

### Gate

Gate는 manager가 temporary period 동안 redemptions를 제한하는 재량이다.

예시:

- 이번 달에는 전체 자금의 10%까지만 환매 가능
- Partial redemption

## 5. Side letters and fee terms

### Side letters

Side letters에는 customized fee structures가 들어간다.

- Investors는 다른 투자자들이 partnership agreement와 다른 terms를 받을 수 있음을 알아야 한다.
- 특정 LP와 맺는 비밀 계약의 성격이 있다.

### Founders class shares

Founders class shares는 early investors가 relatively better terms를 받는 investment interests이다.

- 초기투자자 우대 지분

### Either-or fees

Either-or fees는 management fee와 performance fee 중 하나만 적용하는 구조이다.

예시:

- 1% management fee
- 30% performance fee
- 둘 중 큰 것 하나만 선택

## 6. Biases in AI returns

AI는 각각의 펀드 성격이 너무 달라 수익률과 지수 분석이 어렵다.

| Bias | 내용 |
|---|---|
| Vintage year issue | 펀드가 시작된 연도를 함께 봐야 한다. PE/VC는 시장 상황에 따라 성과가 매우 다르기 때문에 같은 시기에 시작한 펀드끼리 비교해야 공정하다. |
| Survivorship bias | 망한 펀드의 데이터가 사라지는 현상. 망한 70개 펀드의 성과는 사라지고 살아남은 30개 펀드의 성과만 보일 수 있다. |
| Backfill bias | 좋은 성과만 뒤늦게 데이터베이스에 넣는 것. 헤지펀드 매니저가 성과가 좋은 펀드만 성과지표에 포함시키는 경우가 있다. |

### Return calculation of AI

$$r=\frac{V_1-V_0-Total\ fees}{V_0}$$

## 7. Hedge fund fees example

가정:

- Beginning value = $110M
- Management fee = 2%, beginning AUM 기준
- Performance fee = 20%
- High watermark 적용
- Soft hurdle rate = 5%
- Performance fees는 management fee 차감 후 gains 기준

### Year 1

가정:

- Year-end before fees = $100M
- Beginning value = $110M

Management fee:

$$110M \times 2\% = 2.2M$$

After management fee:

$$100M - 2.2M = 97.8M$$

High watermark 110M보다 낮으므로 performance fee는 없다.

### Year 2

가정:

- Beginning value = $98M
- Year-end before fees = $119M

Management fee:

$$98M \times 2\%=1.96M$$

After management fee:

$$119M-1.96M=117.04M$$

High watermark는 $110M이다.

Performance fee:

$$117.04M-110M=7.04M$$

$$7.04M\times20\%=1.41M$$

Total fee:

$$1.96M+1.41M=3.37M$$

Net return:

$$\frac{119M-3.37M-98M}{98M}=18\%$$
