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

$$E(R_p)=w_1E(R_1)+w_2E(R_2)+\cdots+w_nE(R_n)$$

## 2. Covariance and Correlation

### Covariance

$$
\begin{aligned}
\operatorname{Cov}(R_i,R_j)&=E[(R_i-E(R_i))(R_j-E(R_j))]\\
s_{ij}&=\frac{\sum_{t=1}^{n}(R_{i,t}-\bar{R}_i)(R_{j,t}-\bar{R}_j)}{n-1}
\end{aligned}
$$

### Correlation

$$\rho_{ij}=\frac{\operatorname{Cov}(R_i,R_j)}{\sigma_i\sigma_j}$$

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

$$\operatorname{Var}(R_p)=\sum_i\sum_j w_iw_j\operatorname{Cov}(R_i,R_j)$$

### Two Risky Assets

$$
\operatorname{Var}(R_p)=w_1^2\sigma_1^2+w_2^2\sigma_2^2+2w_1w_2\sigma_1\sigma_2\rho_{12}
$$

### Three Assets

$$
\begin{aligned}
\operatorname{Var}(R_p)
&=w_1^2\sigma_1^2+w_2^2\sigma_2^2+w_3^2\sigma_3^2\\
&+2w_1w_2\operatorname{Cov}(1,2)\\
&+2w_1w_3\operatorname{Cov}(1,3)\\
&+2w_2w_3\operatorname{Cov}(2,3)
\end{aligned}
$$

## 5. Shortfall Risk

**Shortfall risk**: portfolio value 또는 return이 특정 target value/return 아래로 떨어질 확률.

| 개념 | 의미 |
|------|------|
| Threshold level | 목표 return 또는 최소 허용 return |
| Shortfall risk | `P(Rp < threshold)` |
| Roy's safety-first criterion | shortfall risk를 최소화하는 portfolio 선택 |

Roy's safety-first ratio:

$$SF\ Ratio=\frac{E(R_p)-R_L}{\sigma_p}$$

- `RL`: threshold return.
- ratio가 클수록 threshold 아래로 떨어질 위험이 낮다.

필기 예시:

$$
\begin{aligned}
R_p&\sim N(\mu=10\%,\sigma=5\%)\\
R_L&=2\%\\
Z&=\frac{2\%-10\%}{5\%}=-1.6\\
P(Z<-1.6)&=0.0548=5.48\%
\end{aligned}
$$

따라서 이 portfolio의 shortfall risk는 **5.48%**.
