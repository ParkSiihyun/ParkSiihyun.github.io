---
title: "Portfolio Mathematics (Reading 5)"
date: 2026-01-02
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 5, Quant]
excerpt: "Sihyun CFA Notes - Portfolio Mathematics (Reading 5)"
---

## Quick Take

- 중심 주제: **Portfolio Mathematics**
- 먼저 잡을 축: portfolio expected return, covariance matrix, portfolio variance, shortfall risk
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Portfolio expected return
2. Covariance, correlation, covariance matrix
3. Portfolio variance
4. Shortfall risk와 Roy's safety-first criterion

## Main Notes

## 1. Portfolio Expected Return

Portfolio expected return은 각 asset expected return의 weighted average다.

```text
E(Rp) = w1E(R1) + w2E(R2) + ... + wnE(Rn)
```

## 2. Covariance and Correlation

### Covariance

```text
Cov(Ri, Rj) = E[(Ri - E(Ri))(Rj - E(Rj))]
sample Cov(Ri, Rj) = sum[(Ri - Ribar)(Rj - Rjbar)] / (n - 1)
```

### Correlation

```text
Corr(Ri, Rj) = Cov(Ri, Rj) / (sigma_i sigma_j)
```

## 3. Covariance Matrix

Covariance matrix는 asset return 간의 variance/covariance를 한 번에 정리한 표다.

|  | Asset A | Asset B | Asset C |
|---|---:|---:|---:|
| **Asset A** | Var(A) | Cov(A,B) | Cov(A,C) |
| **Asset B** | Cov(B,A) | Var(B) | Cov(B,C) |
| **Asset C** | Cov(C,A) | Cov(C,B) | Var(C) |

- 대각선에는 각 asset의 variance가 들어간다.
- 대각선 밖에는 asset 간 covariance가 들어간다.

## 4. Portfolio Variance

일반식:

```text
Var(Rp) = sum_i sum_j wi wj Cov(Ri, Rj)
```

### Two Risky Assets

```text
Var(Rp)
= w1^2 sigma1^2
+ w2^2 sigma2^2
+ 2w1w2 sigma1 sigma2 rho12
```

### Three Assets

```text
Var(Rp)
= w1^2 sigma1^2 + w2^2 sigma2^2 + w3^2 sigma3^2
+ 2w1w2 Cov(1,2)
+ 2w1w3 Cov(1,3)
+ 2w2w3 Cov(2,3)
```

## 5. Shortfall Risk

**Shortfall risk**: portfolio value 또는 return이 특정 target value/return 아래로 떨어질 확률.

| 개념 | 의미 |
|------|------|
| Threshold level | 목표 return 또는 최소 허용 return |
| Shortfall risk | `P(Rp < threshold)` |
| Roy's safety-first criterion | shortfall risk를 최소화하는 portfolio 선택 |

Roy's safety-first ratio:

```text
SFRatio = [E(Rp) - RL] / sigma_p
```

- `RL`: threshold return.
- ratio가 클수록 threshold 아래로 떨어질 위험이 낮다.

필기 예시:

```text
Rp ~ Normal(mean = 10%, standard deviation = 5%)
target return = 2%

Z = (2% - 10%) / 5% = -1.6
P(Z < -1.6) = 0.0548 = 5.48%
```

따라서 이 portfolio의 shortfall risk는 **5.48%**.
