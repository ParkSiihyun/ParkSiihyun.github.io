---
title: "Simple Linear Regression (Reading 10)"
date: 2026-01-04
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 10, Quant]
excerpt: "Sihyun CFA Notes - Simple Linear Regression (Reading 10)"
---

## Quick Take

- 중심 주제: **Simple Linear Regression**
- 먼저 잡을 축: dependent/independent variable, OLS, regression assumptions, R-squared, coefficient tests
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Simple linear regression model
2. OLS와 계수 추정
3. Regression assumptions
4. Model fit과 hypothesis test
5. Non-linear relationship models

## Main Notes

## 1. Regression Setup

| 용어 | 의미 |
|------|------|
| Dependent variable | 종속변수 `Y` |
| Independent variable | 설명변수 `X` |

회귀분석은 설명변수 `X`와 종속변수 `Y` 사이의 관계를 파악하는 것이다.

핵심 질문:

> X가 Y를 얼마나 잘 설명하나?

Simple linear regression model:

$$Y_i=b_0+b_1X_i+e_i$$

| 구성 | 의미 |
|------|------|
| `b0` | intercept |
| `b1` | slope coefficient |
| `ei` | error term |

오차항은 `X`가 `Y`를 설명하지 못한 부분이다.

## 2. Ordinary Least Squares

**OLS(Ordinary Least Squares)**는 residual의 제곱합을 최소화하는 regression line을 찾는다.

$$
\begin{aligned}
\hat{Y}_i&=b_0+b_1X_i\\
e_i&=Y_i-\hat{Y}_i\\
SSE&=\sum e_i^2
\end{aligned}
$$

회귀분석의 목적:

- 실제 데이터가 있고 이를 설명하고 싶다.
- `X`가 있고 `Y`가 여러 개 있을 때, 그 `X`에 대한 평균적인 `Y`값을 추정한다.
- 각각의 `X`에 대한 `Y`값들의 평균적인 추세가 어떻게 변하냐를 보는 것이다.

## 3. Regression Coefficients

Slope coefficient:

$$b_1=\frac{\operatorname{Cov}(X,Y)}{\operatorname{Var}(X)}$$

Intercept:

$$b_0=\bar{Y}-b_1\bar{X}$$

필기 예시:

| 항목 | 값 |
|------|----|
| Cov(S&P 500, ABC) | 0.000336 |
| Var(S&P 500) | 0.000522 |
| Mean return, S&P 500 | -2.7% |
| Mean return, ABC | -4.05% |

$$
\begin{aligned}
b_1&=\frac{0.000336}{0.000522}=0.64\\
b_0&=-4.05\%-0.64(-2.7\%)=-2.3\%
\end{aligned}
$$

해석:

- S&P 500 수익률이 1% 증가하면 ABC 주식의 수익률은 0.64% 상승한다.
- S&P 500 수익률이 0이면 ABC 주식의 수익률은 -2.3%이다.

## 4. Assumptions of Linear Regression

1. **A linear regression exists between dependent and independent variables**
   - `X`와 `Y` 사이에는 선형관계가 있다.
   - 엄밀히 말하면 `X`와 `Y`가 선형함수라는 뜻이 아니라, 계수가 선형이라는 뜻.

2. **Homoskedasticity**
   - 오차항의 분산이 모든 관측치 `X`에 대해 동일하다.
   - 회귀선 주변 데이터들이 퍼져있는 정도가 비슷해야 한다.

$$\operatorname{Var}(e_i)=\sigma^2$$

3. **Error terms are independent**
   - 한 관측치의 오차가 다른 관측치의 오차와 상관관계가 없다.
   - 오차에 상관관계가 생기면 설명변수가 누락되었을 수도 있다는 뜻.

$$\operatorname{Corr}(e_i,e_j)=0$$

4. **Error terms are normally distributed**

$$
\begin{aligned}
e_i&\sim N(0,\sigma^2)\\
E(e_i)&=0
\end{aligned}
$$

## 5. 왜 오차항의 분산이 존재하나?

이전의 생각:

- `X`라는 관측치가 1개이고 `Y`라는 관측치가 1개이면 오차항은 그냥 한 개로 정의되는 것 아닌가?

예시:

- `X`: 학습시간
- `Y`: 시험 성적

공부를 5시간 한 학생들 중에서도 성적이 60점인 학생, 70점인 학생, 80점인 학생이 있을 수 있다.

- 그러면 각각에서 오차항이 생긴다.
- 학습시간이라는 설명변수가 설명하지 못한 부분이 오차항이다.
- IQ, 가정환경 등이 다른 설명변수가 될 수 있다.
- 각 학습시간별로 오차항들이 있고, 이 오차항들의 분산이 모두 같다는 것이 등분산성이다.
- 그리고 그 오차항들은 bell-shaped normal distribution을 따른다고 가정한다.

결국 회귀선을 추정하는 것은 여러 `Y`값들의 평균적인 추세를 구하는 것이다. 그 추세를 `X`가 얼마나 잘 설명하는지가 regression fit 평가의 목적이다.

## 6. Goodness of Fit

$$
\begin{aligned}
SST&=\sum(Y_i-\bar{Y})^2\\
SSR&=\sum(\hat{Y}_i-\bar{Y})^2\\
SSE&=\sum(Y_i-\hat{Y}_i)^2\\
SST&=SSR+SSE
\end{aligned}
$$

| Measure | 의미 |
|---------|------|
| SST | total variation |
| SSR | regression이 설명한 variation |
| SSE | regression이 설명하지 못한 error variation |

왜 `Ybar`가 나오나?

- 회귀분석 전에는 표본평균 `Ybar`만으로 `Y` 데이터가 얼마나 퍼져있는지 분산을 추정했다.
- 회귀분석을 통해 `X`라는 설명변수로 `Y`의 평균적인 추세를 파악할 수 있다.
- 그래서 `X`라는 설명변수가 설명한 분산이 얼마나 되는지 묻는 것이다.
- 예를 들어 수익률을 설명하고 싶은데 어떤 변수가 수익률에 영향을 미치는지 모를 수 있다.
- 그런데 P/E ratio가 수익률을 매우 잘 설명한다면, P/E ratio가 `Y`에 영향을 미친다는 뜻이다.

## 7. Model Fit Measures

$$
\begin{aligned}
MSR&=\frac{SSR}{k}\\
MSE&=\frac{SSE}{n-k-1}
\end{aligned}
$$

- MSR이 높을수록 좋은 회귀 모델.
- MSE가 낮을수록 좋은 회귀 모델.

R-squared:

$$R^2=\frac{SSR}{SST}$$

## 8. Hypothesis Test of Regression Coefficient

$$
\begin{aligned}
H_0&:b_1=0\\
H_a&:b_1\ne0\\
t&=\frac{b_1-0}{SE(b_1)}\\
df&=n-2
\end{aligned}
$$

필기 예시:

$$
\begin{aligned}
b_1&=0.64\\
SE(b_1)&=0.26\\
t&=\frac{0.64}{0.26}=2.46
\end{aligned}
$$

## 9. Non-Linear Relationship

### Log-Lin Model

$$\ln(Y_i)=b_0+b_1X_i+e_i$$

`X`가 1단위 증가할 때 `Y`의 percentage change를 해석한다.

### Lin-Log Model

$$Y_i=b_0+b_1\ln(X_i)+e_i$$

`X`가 1% 증가할 때 `Y`가 얼마나 변하는지 해석한다.

### Log-Log Model

$$\ln(Y_i)=b_0+b_1\ln(X_i)+e_i$$

`X`가 1% 증가할 때 `Y`가 몇 % 변하는지 해석한다.
