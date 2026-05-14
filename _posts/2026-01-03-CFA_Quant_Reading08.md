---
title: "Hypothesis Testing (Reading 8)"
date: 2026-01-03
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 8, Quant]
excerpt: "Sihyun CFA Notes - Hypothesis Testing (Reading 8)"
---

## Quick Take

- 중심 주제: **Hypothesis Testing**
- 먼저 잡을 축: Hypothesis testing : 가설 검정, Nul hypothesis H0 : hypothesis that the researcher wants to reject
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Null/alternative hypothesis와 rejection rule
2. Type I/II error와 p-value
3. Mean, variance, paired comparison, F-test

## Main Notes

## 1. Hypothesis Testing

**Hypothesis testing**: 가설 검정.

| Hypothesis | 의미 |
|------------|------|
| Null hypothesis `H0` | researcher가 reject하고 싶어하는 가설 |
| Alternative hypothesis `Ha` | `H0`를 기각할 충분한 근거가 있을 때 받아들이는 대립가설 |

### Two-Tail Test

예시: 유의수준 `alpha = 5%`.

```text
critical values = -1.96, +1.96
decision rule: test statistic < -1.96 또는 > +1.96이면 reject H0
```

| Test | alpha | Critical value |
|------|-------|----------------|
| two-tail | 10% | ±1.65 |
| two-tail | 5% | ±1.96 |
| two-tail | 1% | ±2.58 |
| one-tail | 5% | 1.65 |
| one-tail | 1% | 2.33 |

## 2. Type of Error

| Error | 의미 |
|-------|------|
| Type I error | `H0`가 실제로 true인데 reject하는 것 |
| Type II error | `H0`가 실제로 false인데 fail to reject하는 것 |

## 3. P-Value

**P-value**: 귀무가설을 기각하기 위해 필요한 최소한의 유의수준.

- p-value보다 유의수준이 커야 귀무가설을 기각할 수 있다.
- 유의수준이 5%인데 p-value가 5%보다 작으면 귀무가설을 기각한다.
- 유의수준이 5%인데 p-value가 10%면 귀무가설을 기각하지 못한다.

## 4. Types of Hypothesis Tests

필기 포인트:

- 언제 어떤 분포를 쓰는지 구분한다.
- 각 분포가 어떻게 생겼는지 판단한다.
- 양측검정인지 단측검정인지 구분한다.
- 각각의 통계량과 임계값을 어떻게 구하는지 알아야 한다.

## 5. Value of Population Mean

모집단의 표준편차를 아는지 모르는지가 핵심이다.

| 상황 | 사용 통계량 |
|------|-------------|
| 모집단의 분산/표준편차를 안다 | z-statistic |
| 모집단의 분산/표준편차를 모른다 | t-statistic |

- `n`의 크기가 충분히 크면 t distribution은 z distribution과 매우 유사하다.
- 그래서 큰 표본에서는 z critical value를 사용해도 무방한 경우가 있다.

예시:

```text
sample mean = 0.1%
s = 0.25%
n = 250
H0: mu = 0
Ha: mu != 0

t statistic = (0.001 - 0) / (0.0025 / sqrt(250)) = 6.33
critical value = ±1.96
```

`6.33 > 1.96`이므로 `H0`를 reject.

## 6. Difference Between Means: Independent Samples

두 모집단 간의 평균 차이가 있는지 검정한다.

예시:

- 주식 평균 수익률 vs 채권 평균 수익률.

가설 형태:

```text
H0: mu1 = mu2
Ha: mu1 != mu2
```

또는 단측검정:

```text
H0: mu1 <= mu2
Ha: mu1 > mu2
```

핵심은 두 sample이 independent인지 확인하고, variance 가정에 따라 pooled variance 또는 별도 variance를 사용한다.

## 7. Paired Comparisons: Dependent Samples

앞의 두 테스트가 independent samples였다면, paired comparison은 서로 연결된 표본이다.

예시:

- 같은 사람의 운동 전/후 몸무게.
- 다이어트 프로그램 전/후 체중.

각 pair의 차이를 새로운 변수 `d`로 만든다.

```text
d = X_after - X_before
t = (dbar - mu_d) / (s_d / sqrt(n))
```

## 8. Value of Population Variance

Population variance 검정은 chi-square statistic을 사용한다.

```text
H0: sigma^2 = sigma0^2
Ha: sigma^2 != sigma0^2

chi-square statistic = (n - 1)s^2 / sigma0^2
```

필기 예시:

```text
sigma0^2 = 0.04
n = 24
s^2 = 0.038
alpha = 5%

chi-square statistic = (24 - 1)(0.038) / 0.04 = 20.76
```

## 9. Comparing Two Population Variances: F-Test

두 population variance를 비교할 때 F-test를 사용한다.

```text
H0: sigma1^2 = sigma2^2
Ha: sigma1^2 != sigma2^2

F statistic = s1^2 / s2^2
```

필기 예시:

```text
s1 = 4.3
s2 = 3.8
F = (4.3^2) / (3.8^2) = 1.28
critical value = 1.94
```

`1.28 < 1.94`이면 `H0`를 reject하지 못한다.
