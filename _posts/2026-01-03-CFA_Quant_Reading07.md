---
title: "Estimation and Inference (Reading 7)"
date: 2026-01-03
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 7, Quant]
excerpt: "Sihyun CFA Notes - Estimation and Inference (Reading 7)"
---

## Quick Take

- 중심 주제: **Estimation and Inference**
- 먼저 잡을 축: Probability sampling : 모집단의 개체들이 뽑힐 확률을 아는 표본추출, Random sampling
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Probability sampling
2. Nonprobability sampling
3. Central limit theorem

## Main Notes

## 1. Probability Sampling

**Probability sampling**: 모집단의 개체들이 뽑힐 확률을 아는 표본추출.

### Random Sampling

| 방법 | 필기 정리 |
|------|-----------|
| Simple random sampling | 모집단의 모든 개체가 동일한 확률로 선택되는 표본추출 |
| Stratified random sampling | 모집단을 다양한 특징 기준으로 작은 그룹(strata)으로 나누고 각 그룹 내에서 무작위 추출 |
| Systematic sampling | population에서 every nth member를 선택. 예: 1번, 11번, 21번, 31번 |
| Cluster sampling | 모집단을 여러 cluster로 나눈 뒤 일부 cluster만 뽑아서 조사 |

Cluster sampling의 포인트:

- stratified와 다르게 각각의 cluster가 모집단의 성격을 전반적으로 반영해야 한다.
- 각 cluster끼리는 전반적으로 비슷해야 한다.
- 모집단을 전수조사할 수 없으니 몇 개의 cluster만 뽑아서 조사한다.

## 2. Nonprobability Sampling

**Nonprobability sampling**: 모집단의 개체가 뽑힐 확률을 모르는 표본추출.

| 방법 | 필기 정리 |
|------|-----------|
| Convenience sampling | 구하기 쉬운 data만 사용 |
| Judgmental sampling | 연구자가 경험과 판단에 따라 선택한 data만 사용 |

## 3. Central Limit Theorem

**Central limit theorem(중심극한정리)**:

- 표본의 관측치 `n`이 충분히 크면, 모집단의 분포가 어떻든 표본평균의 분포는 정규분포를 따른다.

$$
\begin{aligned}
E(\bar{X})&=\mu\\
\operatorname{Var}(\bar{X})&=\frac{\sigma^2}{n}\\
SE(\bar{X})&=\frac{\sigma}{\sqrt{n}}
\end{aligned}
$$

모집단 표준편차 `sigma`를 모르면 sample standard deviation `s`를 사용한다.

$$SE(\bar{X})=\frac{s}{\sqrt{n}}$$
