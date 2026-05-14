---
title: "Rates and Returns (Reading 1)"
date: 2026-01-01 08:00:00 -0800
categories: cfa
tags: [Quantitative Methods, CFA Level I, Reading 1, Quant]
excerpt: "Sihyun CFA Notes - Rates and Returns (Reading 1)"
---

## Quick Take

- 중심 주제: **Rates and Returns**
- 먼저 잡을 축: 요구수익률, 보유기간수익률, 평균수익률, money-weighted/time-weighted return
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Required rate of return과 금리의 구성
2. HPR과 평균수익률
3. Money-weighted return vs Time-weighted return
4. Annualized, real/nominal, leveraged return

## Main Notes

## 1. Rates and Returns

| 용어 | 필기 정리 |
|------|-----------|
| Required rate of return | 요구수익률 |
| Discount rate | 할인율 |
| Interest rate | 금리, required rate of return과 같은 맥락 |

- 금리는 **opportunity cost**로 볼 수 있다.
- 다른 곳에 투자하지 않고 은행에 넣었더라면 얻었을 수익이 금리의 의미가 된다.

### Risk-Free Rate

- **Real risk-free rate**
  - no expectation of inflation
  - zero probability of default
- **Nominal risk-free rate**
  - `nominal risk-free rate = real risk-free rate + expected inflation rate`

### Time Preference

- 미래보다 현재의 돈의 가치가 더 높다.
- 그래서 미래 현금흐름은 현재가치로 할인한다.

### Risk of Securities

| Risk premium | 의미 |
|--------------|------|
| Default risk | 신용도가 낮을수록 부도 가능성이 높다. |
| Liquidity risk | 국채보다 회사채가 유동성 리스크가 더 크다. |
| Maturity risk | 만기가 긴 상품일수록 리스크가 더 크다. |

$$
\begin{aligned}
\text{nominal rate of interest}
&= \text{real risk-free rate}\\
&+ \text{inflation premium}\\
&+ \text{default risk premium}\\
&+ \text{liquidity premium}\\
&+ \text{maturity premium}
\end{aligned}
$$

## 2. Holding Period Return

**Holding Period Return(HPR)**: 보유기간 동안 발생한 수익률.

$$HPR=\frac{\text{Ending Value}-\text{Beginning Value}+\text{Income}}{\text{Beginning Value}}$$

여러 기간의 HPR은 단순합이 아니라 곱으로 연결한다.

$$\text{Multi-period HPR}=(1+HPR_1)(1+HPR_2)\cdots(1+HPR_n)-1$$

## 3. Average Return

### Arithmetic Mean Return

$$\text{Arithmetic Mean}=\frac{R_1+R_2+\cdots+R_n}{n}$$

### Geometric Mean Return

$$\text{Geometric Mean}=\left[(1+R_1)(1+R_2)\cdots(1+R_n)\right]^{1/n}-1$$

필기 예시:

| 기간 | 수익률 |
|------|--------|
| 6M | 2% |
| 1Y | 0.5% |
| 1.5Y | -1% |
| 2Y | 1.5% |

- 전체 기간 수익률은 각 기간의 gross return을 곱해서 계산한다.
- annual return은 전체 기간 수익률을 연율화한다.

### Harmonic Mean

**Harmonic mean**은 시간에 걸쳐 주식을 매수할 때 평균 매입단가를 계산하는 데 사용한다.

예시: mutual fund를 $1,000씩 세 번 매수.

| 매수가 | 매수 주식 수 |
|--------|--------------|
| $8 | 125.00 |
| $9 | 111.11 |
| $10 | 100.00 |

$$
\begin{aligned}
\text{Total Shares} &=125.00+111.11+100.00=336.11\\
\text{Average Cost} &=\frac{\$3{,}000}{336.11}=\$8.926\ \text{per share}
\end{aligned}
$$

평균의 관계:

$$\text{Harmonic Mean}\le \text{Geometric Mean}\le \text{Arithmetic Mean}$$

### Trimmed / Winsorized Mean

- outlier의 영향을 줄이는 방법.
- trimmed mean은 극단값을 제거한다.
- winsorized mean은 극단값을 제거하지 않고 가까운 값으로 대체한다.

## 4. Money-Weighted Return

**Money-weighted return**은 cash flow 관점의 수익률이다.

- IRR(internal rate of return)을 사용한다.
- 현금 유입의 현재가치와 현금 유출의 현재가치를 같게 만드는 할인율이다.

$$
\begin{aligned}
PV(\text{cash inflows})-PV(\text{cash outflows})&=0\\
NPV=0 &\Rightarrow r=IRR
\end{aligned}
$$

필기 예시:

| 시점 | 현금흐름 |
|------|----------|
| t=0 | -100 |
| t=1 | -118 |
| t=2 | +264 |

- stock price가 `P0 = $100`, `P1 = $120`, `P2 = $130`으로 움직이는 예시.
- 계산기 cash flow 기능으로 IRR을 계산하면 약 **13.86%**.

## 5. Time-Weighted Return

**Time-weighted return**은 기간별 성과를 compounding해서 계산한다.

필기 예시:

| 기간 | HPR |
|------|-----|
| 1기 | 22% |
| 2기 | 10% |

$$\text{Time-weighted Return}=\left[(1.22)(1.10)\right]^{1/2}-1=15.84\%$$

## 6. Common Measures of Return

### Annualized Return

$$\text{Annualized Return}=(1+HPR)^{365/\text{days}}-1$$

예시:

$$
\begin{aligned}
\text{90-day HPR}&=\frac{100.75-100}{100}=0.75\%\\
\text{Annualized Return}&=(1+0.0075)^{365/90}-1=3.08\%
\end{aligned}
$$

### Present Value

$$PV=\frac{FV}{\left(1+\frac{I/Y}{m}\right)^{mN}}$$

| 기호 | 의미 |
|------|------|
| `I/Y` | quoted annual interest rate |
| `N` | number of years |
| `m` | periodicity, compounding periods per year |

### Continuous Compounding

$$
\begin{aligned}
1+HPR&=e^r\\
r&=\ln(1+HPR)
\end{aligned}
$$

예시:

$$
\begin{aligned}
HPR&=20\%\\
r&=\ln(1.20)=18.232\%
\end{aligned}
$$

## 7. Return Conventions

| 구분 | 의미 |
|------|------|
| Gross return | management/admin fee 차감 전 |
| Net return | fee 차감 후 |
| Pretax / After-tax return | 세전 / 세후 수익률 |
| Real / Nominal return | 실질 / 명목 수익률 |

Real / nominal 관계:

$$
\begin{aligned}
1+r_{\text{nominal}}&=(1+r_{\text{real}})(1+\pi)\\
r_{\text{nominal}}&\approx r_{\text{real}}+\pi
\end{aligned}
$$

## 8. Leveraged Return

| 기호 | 의미 |
|------|------|
| `V0` | equity |
| `VB` | borrow amount |
| `i` | borrowing interest rate |
| `r` | earned by investment |

$$\text{Leveraged Return}=\frac{(V_0+V_B)r-iV_B}{V_0}$$

예시:

$$
\begin{aligned}
V_0&=100,\quad V_B=100,\quad r=20\%,\quad i=10\%\\
\text{Leveraged Return}
&=\frac{(200)(20\%)-(100)(10\%)}{100}=30\%
\end{aligned}
$$
