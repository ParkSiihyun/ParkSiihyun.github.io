---
title: "Parametric and Non-parametric Tests of Independence (Reading 9)"
date: 2026-01-03
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 9, Quant]
excerpt: "Sihyun CFA Notes - Parametric and Non-parametric Tests of Independence (Reading 9)"
---

## Quick Take

- 중심 주제: **Parametric and Non-parametric Tests of Independence**
- 먼저 잡을 축: Test for independence 독립성 검정, 두 변수간의 상관계수가 0인가?
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Pearson correlation coefficient test
2. Spearman rank correlation test
3. Chi-square test of independence

## Main Notes

## 1. Test for Independence

**독립성 검정**은 두 변수 사이에 관계가 있는지 보는 테스트다.

핵심 질문:

```text
두 변수 간의 correlation coefficient가 0인가?
```

## 2. Parametric Test: Pearson Correlation Coefficient

```text
H0: rho = 0
Ha: rho != 0
```

| 기호 | 의미 |
|------|------|
| `r` | sample correlation |
| `n` | sample size |

검정통계량:

```text
t = r * sqrt(n - 2) / sqrt(1 - r^2)
df = n - 2
```

## 3. Non-Parametric Test: Spearman Rank Correlation

Spearman rank correlation test는 두 rank set이 correlated되어 있는지 검정한다.

```text
rs = 1 - [6 * sum(di^2)] / [n(n^2 - 1)]
```

| 기호 | 의미 |
|------|------|
| `di` | 두 ranking 간 차이 |
| `n` | observation 수 |

필기 예시 구조:

| 항목 | Rank A | Rank B | d |
|------|--------|--------|---|
| A | 1 | 2 | -1 |
| B | 2 | 1 | 1 |
| C | 3 | 4 | -1 |
| D | 4 | 2 | 2 |

## 4. Chi-Square Test of Independence

카테고리형 변수 간 독립성을 검정한다.

예시: 두 변수 모두 `L / M / H` category를 가진 경우.

Observed frequency:

|  | L | M | H | Total |
|---|---:|---:|---:|---:|
| L | 28 | 53 | 42 | 123 |
| M | 42 | 32 | 39 | 113 |
| H | 49 | 25 | 14 | 88 |
| **Total** | 119 | 110 | 95 | 324 |

Expected frequency:

```text
Eij = (row total_i * column total_j) / grand total
```

Degrees of freedom:

```text
df = (number of rows - 1)(number of columns - 1)
df = (3 - 1)(3 - 1) = 4
```

Test statistic:

```text
chi-square = sum [(Oij - Eij)^2 / Eij]
```

필기 예시의 한 cell:

```text
O22 = 32
E22 = (113 * 110) / 324
cell contribution = (O22 - E22)^2 / E22 = 1.0667
```
