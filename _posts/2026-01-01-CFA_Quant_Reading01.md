---
title: "Rates and Returns (Reading 1)"
date: 2026-01-01
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

```text
nominal rate of interest
= real risk-free rate
+ inflation premium
+ default risk premium
+ liquidity premium
+ maturity premium
```

## 2. Holding Period Return

**Holding Period Return(HPR)**: 보유기간 동안 발생한 수익률.

```text
HPR = (ending value - beginning value + income) / beginning value
```

여러 기간의 HPR은 단순합이 아니라 곱으로 연결한다.

```text
multi-period HPR = (1 + HPR1)(1 + HPR2)...(1 + HPRn) - 1
```

## 3. Average Return

### Arithmetic Mean Return

```text
arithmetic mean = (R1 + R2 + ... + Rn) / n
```

### Geometric Mean Return

```text
geometric mean = [(1 + R1)(1 + R2)...(1 + Rn)]^(1/n) - 1
```

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

```text
total shares = 125.00 + 111.11 + 100.00 = 336.11
average cost = $3,000 / 336.11 = $8.926 per share
```

평균의 관계:

```text
harmonic mean <= geometric mean <= arithmetic mean
```

### Trimmed / Winsorized Mean

- outlier의 영향을 줄이는 방법.
- trimmed mean은 극단값을 제거한다.
- winsorized mean은 극단값을 제거하지 않고 가까운 값으로 대체한다.

## 4. Money-Weighted Return

**Money-weighted return**은 cash flow 관점의 수익률이다.

- IRR(internal rate of return)을 사용한다.
- 현금 유입의 현재가치와 현금 유출의 현재가치를 같게 만드는 할인율이다.

```text
PV of cash inflows - PV of cash outflows = 0
NPV = 0이면 r = IRR
```

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

```text
time-weighted return = [(1.22)(1.10)]^(1/2) - 1 = 15.84%
```

## 6. Common Measures of Return

### Annualized Return

```text
annualized return = (1 + HPR)^(365 / days) - 1
```

예시:

```text
90-day HPR = (100.75 - 100) / 100 = 0.75%
annualized return = (1 + 0.0075)^(365/90) - 1 = 3.08%
```

### Present Value

```text
PV = FV / (1 + I/Y / m)^(mN)
```

| 기호 | 의미 |
|------|------|
| `I/Y` | quoted annual interest rate |
| `N` | number of years |
| `m` | periodicity, compounding periods per year |

### Continuous Compounding

```text
1 + HPR = e^r
r = ln(1 + HPR)
```

예시:

```text
HPR = 20%
r = ln(1.20) = 18.232%
```

## 7. Return Conventions

| 구분 | 의미 |
|------|------|
| Gross return | management/admin fee 차감 전 |
| Net return | fee 차감 후 |
| Pretax / After-tax return | 세전 / 세후 수익률 |
| Real / Nominal return | 실질 / 명목 수익률 |

Real / nominal 관계:

```text
1 + nominal = (1 + real)(1 + inflation)
nominal rate ≈ real rate + inflation rate
```

## 8. Leveraged Return

| 기호 | 의미 |
|------|------|
| `V0` | equity |
| `VB` | borrow amount |
| `i` | borrowing interest rate |
| `r` | earned by investment |

```text
leveraged return = [(V0 + VB)r - iVB] / V0
```

예시:

```text
V0 = 100
VB = 100
r = 20%
i = 10%

leveraged return = [(200)(20%) - (100)(10%)] / 100 = 30%
```
