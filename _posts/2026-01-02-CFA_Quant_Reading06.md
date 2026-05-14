---
title: "Simulation Methods (Reading 6)"
date: 2026-01-02
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 6, Quant]
excerpt: "Sihyun CFA Notes - Simulation Methods (Reading 6)"
---

## Quick Take

- 중심 주제: **Simulation Methods**
- 먼저 잡을 축: lognormal distribution, log return, multiperiod compounding, Monte Carlo simulation
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Lognormal distribution
2. Log return과 compounding
3. Monte Carlo simulation

## Main Notes

## 1. Simulation Method

Simulation은 특정 distribution을 가정하고 여러 번의 random path를 만들어 결과 범위를 보는 방법이다.

## 2. Lognormal Distribution

어떤 변수 `X`가 lognormal distribution을 따른다는 말은:

```text
ln(X) ~ Normal distribution
```

Asset price나 gross return은 음수가 될 수 없기 때문에 lognormal distribution으로 다루기 좋다.

## 3. Gross Return and Log Return

| Return | 표기 |
|--------|------|
| Holding period return | `R` |
| Gross return | `1 + R` |
| Log return | `r = ln(1 + R)` |

필기 예시:

```text
R = 10%
gross return = 1.1
log return = ln(1.1) = 0.0953 = 9.53%
```

```text
R = 20%
gross return = 1.2
log return = ln(1.2) = 18.23%
```

## 4. Multiperiod Compounding

가격은 각 기간의 gross return을 곱해서 계산한다.

```text
Pt = P0(1 + R1)(1 + R2)(1 + R3)...(1 + Rn)
```

log를 취하면 곱이 합으로 바뀐다.

```text
ln(Pt) = ln(P0) + ln(1 + R1) + ln(1 + R2) + ... + ln(1 + Rn)
```

즉 log return은 여러 기간을 더하기 쉽다.

## 5. Exponential Compounding

```text
Pt = P0 * e^r
r = ln(1 + R)
```

## 6. Monte Carlo Simulation

Monte Carlo simulation은 return, price, VaR 같은 값을 확률분포 기반으로 반복 생성해서 가능한 결과 범위를 보는 방법이다.

- random value를 반복적으로 생성한다.
- 여러 scenario의 terminal value를 만든다.
- portfolio risk 또는 VaR 같은 값을 추정하는 데 사용한다.
