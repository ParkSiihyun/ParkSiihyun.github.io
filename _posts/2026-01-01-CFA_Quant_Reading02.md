---
title: "Time Value of Money in Finance (Reading 2)"
date: 2026-01-01
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 2, Quant]
excerpt: "Sihyun CFA Notes - Time Value of Money in Finance (Reading 2)"
---

## Quick Take

- 중심 주제: **Time Value of Money in Finance**
- 먼저 잡을 축: DCF, fixed income/equity valuation, forward rates, no-arbitrage
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Time Value of Money와 DCF
2. Fixed income / equity securities valuation
3. Cash flow additivity와 forward rates
4. Option pricing model의 출발점

## Main Notes

## 1. Time Value of Money

### Discounted Cash Flow Valuation

```text
FV = PV(1 + r)^N
FV = PV * e^(rT)   // continuous compounding
```

## 2. Fixed Income Securities

| Security | 필기 포인트 |
|----------|-------------|
| Zero-coupon bond | coupon 없이 만기 현금흐름을 할인 |
| Fixed-coupon bond | coupon과 principal을 각각 할인 |
| Perpetual bond / perpetuity | 영구 현금흐름 |
| Loan payments | loan amortization 계산 |

Perpetuity:

```text
PV of perpetuity = A / r
```

Loan payment 예시:

- loan amount: `$2,000`
- interest rate: `6%`
- amortizing loan 형태로 payment를 계산한다.

## 3. Equity Securities

### Preferred Stock

Preferred stock은 일정한 dividend를 perpetuity처럼 할인한다.

```text
preferred stock value = dividend / required rate of return
```

예시:

```text
par value = $100
annual dividend = $5
required rate of return = 8%

V = 5 / 0.08 = $62.50
```

### Common Stock

Common stock valuation은 DDM(Dividend Discount Model)을 사용한다.

#### Constant Growth DDM / Gordon Growth Model

```text
V0 = D1 / (r - g)
```

#### Multistage DDM

필기 예시:

| 가정 | 값 |
|------|----|
| `D0` | $1 |
| `ke` | 11% |
| 초기 성장률 | 15% |
| 안정 성장률 | 5% |

```text
D1 = 1.00(1.15) = 1.15
D2 = 1.15(1.15) = 1.3225
D3 = 1.3225(1.05) = 1.386

terminal value at t=2 = D3 / (0.11 - 0.05) = $23.10
V0 = D1/1.11 + (D2 + terminal value)/1.11^2
```

## 4. Cash Flow Additivity Principle

```text
V(CF1 + CF2) = V(CF1) + V(CF2)
```

- 4-year coupon bond는 여러 개의 zero-coupon bond로 분해해서 볼 수 있다.
- 이 원리가 no-arbitrage principle과 연결된다.

## 5. Forward Interest Rate

Spot rate와 forward rate의 no-arbitrage 관계:

```text
(1 + S2)^2 = (1 + S1)(1 + 1y1y)
```

- 장기 spot return은 짧은 spot rate와 forward rate를 이어 붙인 return과 같아야 한다.

## 6. Forward Currency Exchange Rate

```text
F(x/y) = S(x/y) * [(1 + r_x) / (1 + r_y)]
```

필기 예시:

| 항목 | 값 |
|------|----|
| Spot ABE/DUB | 4.5671 |
| ABE rate | 5% |
| DUB rate | 3% |

- 금리 차이를 반영해서 forward exchange rate를 계산한다.

## 7. Option Pricing Model

Binomial model의 접근:

1. hedged portfolio
2. risk-neutral pricing
