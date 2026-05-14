---
title: "Exchange Rate Calculations (Reading 19)"
date: 2026-01-05
categories: cfa
tags: [Economics, CFA Level I, Reading 19, Economics]
excerpt: "Sihyun CFA Notes - Exchange Rate Calculations (Reading 19)"
---

## Quick Take

- 중심 주제: **Exchange Rate Calculations**
- 먼저 잡을 축: Cross rate : the exchange btw two currencies implied by their exchange rates with a common, third currency
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Cross rate
2. Spot/forward no-arbitrage
3. Forward quote in points
4. Forward premium / discount

## Main Notes

## 1. Cross Rate

**Cross rate**: common third currency를 통해 implied되는 두 통화 간 exchange rate.

- KRW / 아르헨티나 통화처럼 active FX market이 없는 currency pair에서는 cross rate가 필요하다.

필기 예시:

```text
MXN / USD = 10.70
USD / AUD = 0.60

MXN / AUD = (MXN / USD) * (USD / AUD)
          = 10.70 * 0.60
          = 6.42
```

## 2. Arbitrage Condition: Spot and Forward

Spot exchange rate와 forward exchange rate는 interest rate parity(IRP)로 연결된다.

```text
F(x/y) = S(x/y) * [(1 + r_x) / (1 + r_y)]
```

필기 예시:

```text
S(ABE/DUB) = 4.5671
90-day rate of ABE = 5%
90-day rate of DUB = 3%

F(ABE/DUB) = 4.5898
```

## 3. No-Arbitrage Forward Rate

필기 예시에서는 no-arbitrage forward rate가 `4.5898 ABE/DUB`인데, 시장 forward rate가 `4.6000 ABE/DUB`인 경우를 비교한다.

핵심 구조:

1. DUB를 빌린다.
2. spot market에서 ABE로 바꾼다.
3. ABE를 투자한다.
4. forward contract로 ABE를 DUB로 바꾼다.
5. DUB 차입금을 갚고 남는 금액이 arbitrage profit이다.

예시 숫자 흐름:

```text
borrow 1000 DUB
spot: 1000 DUB * 4.5671 = 4567.1 ABE
invest ABE at 5%: 4567.1 * 1.05 = 4795.45 ABE
forward at 4.6000 ABE/DUB: 4795.45 / 4.6000 = 1042.49 DUB
repay DUB at 3%: 1000 * 1.03 = 1030 DUB
profit = 1042.49 - 1030 = 12.49 DUB
```

## 4. Forward Quote in Points or Percentage Terms

Forward exchange rate는 points 또는 percentage terms로 표시할 수 있다.

```text
1 point = 0.0001
18.3 points = 0.00183
```

- forward points가 positive면 spot에 더한다.
- forward points가 negative면 spot에서 뺀다.

## 5. Forward Premium / Forward Discount

Forward rate가 spot보다 높으면 forward premium, 낮으면 forward discount.

필기 예시:

```text
USD/EUR spot = 1.312
USD/EUR forward = 1.320
```

```text
forward premium = (forward - spot) / spot
```

90-day forward premium을 annualize할 때는 4를 곱한다.
