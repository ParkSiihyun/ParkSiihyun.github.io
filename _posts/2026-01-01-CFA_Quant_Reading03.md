---
title: "Statistical Measures of Asset Returns (Reading 3)"
date: 2026-01-01
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 3, Quant]
excerpt: "Sihyun CFA Notes - Statistical Measures of Asset Returns (Reading 3)"
---

## Quick Take

- 중심 주제: **Statistical Measures of Asset Returns**
- 먼저 잡을 축: mean/median/mode, outlier 처리, dispersion, skewness/kurtosis, covariance/correlation
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Center와 location
2. Dispersion과 downside risk
3. Shape: skewness와 kurtosis
4. Covariance와 correlation

## Main Notes

## 1. Measures of Center

| Measure | 필기 포인트 |
|---------|-------------|
| Mean | 평균 |
| Median | outlier의 영향을 mean보다 덜 받음 |
| Mode | 최빈값 |

- **Unimodal**: mode가 하나.
- **Bimodal**: mode가 두 개.

## 2. Methods for Dealing with Outliers

| 방법 | 의미 |
|------|------|
| Trimmed mean | 극단값을 제거해서 outlier의 영향을 줄임 |
| Winsorized mean | 극단값을 제거하지 않고 가까운 값으로 대체 |

필기 예시:

| Series | Values |
|--------|--------|
| Original | 11, 12, 13, 17, 20, 30, 200 |
| Winsorized | 11, 12, 13, 17, 20, 30, 30 |

## 3. Measures of Location

| Location measure | 의미 |
|------------------|------|
| Quantile | 분포를 일정 구간으로 나눈 위치 |
| Quartile | distribution divided into quarters |
| Quintile | 5개 구간 |
| Decile | 10개 구간 |
| Percentile | 100개 구간 |

Box and whisker plot:

$$
\text{min}\;-\;Q_1\;-\;\text{median}\;-\;Q_3\;-\;\text{max}
$$

$$IQR=Q_3-Q_1$$

## 4. Measures of Dispersion

### Mean Absolute Deviation

$$MAD=\frac{\sum_{i=1}^{n}|X_i-\bar{X}|}{n}$$

### Variance and Standard Deviation

$$
\begin{aligned}
s^2&=\frac{\sum_{i=1}^{n}(X_i-\bar{X})^2}{n-1}\\
\sigma^2&=\frac{\sum_{i=1}^{N}(X_i-\mu)^2}{N}\\
s&=\sqrt{s^2}
\end{aligned}
$$

### Coefficient of Variation

**Coefficient of Variation(CV)**은 relative dispersion이다.

$$CV=\frac{\text{Standard Deviation}}{\text{Mean Return}}$$

필기 예시:

| Asset | Mean return | Standard deviation | CV |
|-------|-------------|-------------------|----|
| T-bill | 0.25% | 0.76% | 0.76 / 0.25 |
| S&P 500 | 1.09% | 7.30% | 7.30 / 1.09 |

- CV는 수익 1단위당 감수하는 변동성을 비교하는 느낌.
- S&P 500은 T-bill보다 return dispersion이 더 크다.

### Downside Risk

Target downside deviation은 target보다 낮은 return만 downside risk로 본다.

$$\text{Target Downside Deviation}=\sqrt{\frac{\sum_{i=1}^{n}\min(0,R_i-R_{target})^2}{n}}$$

## 5. Skewness

**Skewness**는 distribution의 asymmetry를 측정한다.

| Shape | Tail | 관계 |
|-------|------|------|
| Positive skew | right tail이 김 | mean > median > mode |
| Negative skew | left tail이 김 | mean < median < mode |
| Symmetric | skewness = 0 | mean = median = mode |

## 6. Kurtosis

Kurtosis는 tail의 두꺼움과 peak를 보는 지표.

- Normal distribution의 kurtosis는 `3`.
- Excess kurtosis는 `kurtosis - 3`으로 본다.

## 7. Covariance and Correlation

### Covariance

$$
\begin{aligned}
\operatorname{Cov}(X,Y)&=E[(X-\mu_X)(Y-\mu_Y)]\\
s_{XY}&=\frac{\sum_{i=1}^{n}(X_i-\bar{X})(Y_i-\bar{Y})}{n-1}
\end{aligned}
$$

### Correlation

$$\rho_{XY}=\frac{\operatorname{Cov}(X,Y)}{\sigma_X\sigma_Y}$$

- correlation은 covariance를 표준화한 값이다.
- spurious correlation에 주의한다.
