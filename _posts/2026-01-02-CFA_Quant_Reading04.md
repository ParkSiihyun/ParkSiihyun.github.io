---
title: "Probability Trees and Conditional Expectations (Reading 4)"
date: 2026-01-02
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 4, Quant]
excerpt: "Sihyun CFA Notes - Probability Trees and Conditional Expectations (Reading 4)"
---

## Quick Take

- 중심 주제: **Probability Trees and Conditional Expectations**
- 먼저 잡을 축: expected value, variance, conditional probability, Bayes' formula
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Expected value와 variance
2. Conditional probability
3. Bayes' formula와 probability tree

## Main Notes

## 1. Expected Value

Expected value는 가능한 결과에 probability를 곱해서 더한 값이다.

```text
E(X) = P(x1)x1 + P(x2)x2 + ... + P(xn)xn
```

## 2. Variance

```text
Var(X) = E[(X - E(X))^2]
       = sum [(xi - mu)^2 * P(xi)]
```

## 3. Conditional Probability

```text
P(A | B) = P(A and B) / P(B)
```

독립이면:

```text
P(A | B) = P(A)
P(A and B) = P(A)P(B)
```

## 4. Bayes' Formula

```text
P(A | B) = [P(B | A)P(A)] / P(B)
```

Probability tree에서는 각 branch의 확률을 곱해 joint probability를 만들고, 필요한 조건부확률은 해당 branch들을 합산해서 계산한다.

## 5. 필기 예시 흐름

### Economy와 Outperformance

- economy 상태별로 outperform / underperform 확률을 나누는 probability tree.
- outperform이 관측되었을 때 economy 상태가 무엇이었는지 역으로 계산하는 형태.
- 즉 `P(economy state | outperform)`을 Bayes' formula로 계산한다.

### EPS Probability Tree

필기 구조:

| Scenario | Branch probability | EPS condition |
|----------|--------------------|---------------|
| High | 30% | EPS가 특정 기준 초과/미만 |
| Middle | 40% | EPS가 특정 기준 초과/미만 |
| Low | 30% | EPS가 특정 기준 초과/미만 |

예시 계산의 핵심:

```text
P(EPS condition) = sum of joint probabilities from all matching branches
P(scenario | EPS condition) = joint probability / P(EPS condition)
```
