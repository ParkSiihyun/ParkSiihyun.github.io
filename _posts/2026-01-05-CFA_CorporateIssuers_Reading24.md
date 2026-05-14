---
title: "Capital Investment and Capital Allocation (Reading 24)"
date: 2026-01-05 18:00:00 -0800
categories: cfa
tags: [Corporate Issuers, CFA Level I, Reading 24, Corporate Issuers]
excerpt: "Sihyun CFA Notes - Capital Investment and Capital Allocation (Reading 24)"
---

## Quick Take

- 중심 주제: **Capital Investment and Capital Allocation**
- 먼저 잡을 축: capital investment types, NPV/IRR, ROIC vs WACC, capital allocation biases, real options
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Capital investment types
2. Capital allocation process
3. NPV, IRR, ROIC
4. Principles, errors, biases
5. Real options

## Main Notes

## 1. The Four Types of Capital Investment

| Type | 필기 정리 |
|------|-----------|
| Going concern projects | May be needed to maintain the business or reduce costs |
| Regulatory / compliance projects | May be required by a government agency or insurance company and often involve safety-related or environmental concerns |
| Expansion projects | Grow the business, entering new markets, introducing new products |
| Other projects | 그 외 capital investment |

Going concern projects는 기업이 계속해서 운영된다는 가정하에 진행되는 프로젝트다. 추가적인 수익보다 비용절감이 중요하다.

To reduce financing risk, companies use **match funding**.

**Match funding**: financing the projects with capital sources that are consistent with the project life.

예시:

- 20년짜리 사업
- 20년짜리 만기 부채

## 2. Capital Allocation Process

**Capital allocation process**: identifying and evaluating capital projects, usually longer than a year.

- Financial manager가 갖는 가장 중요한 책임
- Costly long-term assets의 구매는 회사의 future success를 결정함

Capital allocation process:

| Step | 내용 |
|------|------|
| Step 1 | Idea generation |
| Step 2 | Analyzing project proposals |
| Step 3 | Create the firm-wide capital budget |
| Step 4 | Monitoring decisions and conducting a post audit |

Step 2에서 capital project를 accept할지 reject할지는 expected future cash flow에 기반한다.

Step 3에서는 profitable projects를 prioritize한다.

## 3. NPV

**NPV(Net Present Value)**: the sum of the present values of all the expected incremental cash flows if a project is undertaken.

$$NPV=PV(\text{Operating Cash Flows})-\text{Investment Capital}$$

Discount rate는 cost of capital을 사용한다.

| NPV 결과 | 의미 |
|----------|------|
| Positive NPV | Expected to increase shareholder wealth |
| Negative NPV | Expected to decrease shareholder wealth |

**K = cost of capital = 기회비용**

- 다른 곳에 투자했다면 벌 수 있었던 수익
- 여기에 투자함으로써 포기해야 했던 수익

## 4. IRR

IRR은 outflow의 현재가치와 inflow의 현재가치를 같게 만들어주는 할인율이다. 즉, NPV를 0으로 만드는 할인율이다.

$$NPV=0$$

IRR이 cost of capital, 즉 다른 곳에 투자했더라면 벌 수 있었던 수익보다 크다면 좋은 투자다.

IRR은 conventional cash flow에서만 유효하다.

| Cash flow type | 의미 |
|----------------|------|
| Conventional CF | Project 기간 동안 cash flow의 부호가 한 번만 바뀌는 현금흐름 |
| Unconventional CF | Project 기간 동안 cash flow의 부호가 여러 번 바뀌는 현금흐름 |

## 5. NPV vs IRR

| Method | Advantage | Disadvantage |
|--------|-----------|--------------|
| NPV | Direct measure of the expected increase in the value of the firm | Cost of capital을 사용해야 함 |
| IRR | Measures profitability as a percentage, showing the return on each dollar invested | Cash flow가 IRR로 재투자된다고 가정함 |

NPV는 cash flow가 cost of capital로 재투자되는 것을 가정하지만, IRR은 cash flow가 IRR로 재투자되는 것을 가정한다. 이 IRR 재투자 가정은 사실상 불가능할 수 있다.

필기 예시:

| 시점 | Cash Flow |
|------|----------:|
| 0 | -100 |
| 1 | 80 |
| 2 | 80 |

이 투자의 IRR은 36%이다. 1년 뒤에 받은 80달러를 36%에 투자할 투자처를 또 찾는 것은 매우 어렵다.

Cost of capital은 다른 곳에 투자했더라면 얻을 수 있었던 수익이기 때문에 차라리 현실적이다.

## 6. ROIC

**ROIC(Return on Invested Capital)**:

$$ROIC=\frac{NOPAT}{\text{Average Book Value of Invested Capital}}$$

**NOPAT(Net Operating Profit After Tax)**:

$$NOPAT=NI+\text{After-tax Interest Expense}$$

NOPAT은 주주와 채권자 모두에게 돌아가는 이익이라고 생각하면 된다.

Invested capital은 debt + equity다. ROIC는 채권자와 주주의 돈을 받아서 얼마만큼의 이익을 냈는지 보는 지표다.

## 7. ROIC vs Required Rate of Return

주주와 채권자 모두의 요구수익률을 계산하기 위해서는 WACC를 사용한다.

**WACC**: Weighted Average Cost of Capital.

| 비교 | 해석 |
|------|------|
| ROIC > WACC | 이 회사의 수익성이 좋음 |

NPV와 IRR은 project-specific한 수익성 지표이지만, ROIC는 기업 전반에 대한 수익성 지표다.

## 8. Principles of Capital Allocation

| Principle | 필기 정리 |
|-----------|-----------|
| Based on after-tax cash flows, not accounting income | 회계상의 이익은 발생주의이기 때문에 현금흐름의 타이밍을 고려하지 않음 |
| Incremental cash flow only | 새로운 투자로 발생하는 현금흐름의 증가분만 고려 |
| Timing of cash flow is important | Earlier cash flows are worth more than later cash flows |

Sunk costs는 이미 발생한 매몰비용이므로 판단에 개입되어서는 안 된다.

## 9. Cognitive Errors of Capital Allocation

| Error | 필기 정리 |
|-------|-----------|
| Poor forecasting | 예측 오류 |
| Not considering the cost of internal funds | 내부유보금이라도 프로젝트에 쓰지 않았다면 배당으로 쓸 수 있었기 때문에 cost of equity와 동일한 관점에서 생각해야 함 |
| Incorrectly accounting for inflation | Real cash flow를 사용하면 real discount rate를 사용해야 함 |

## 10. Behavioral Biases of Capital Allocation

| Bias | 필기 정리 |
|------|-----------|
| Pet projects of senior management | 수익성이 아니라 단순히 좋아하는 사업이라서 하는 것 |
| Inertia in setting the entire capital budget | 매년 존재하는 opportunities를 고려하지 않고 prior year capital budget에 anchoring |
| Basing investment decisions on EPS, ROE | 지금 당장의 주가, EPS, ROE에 집착하다가 너무 근시안적인 투자를 할 우려 |

과거의 수치에 너무 매몰되는 anchoring을 조심해야 한다.

## 11. Real Options

**Real options**: 현실 프로젝트에 붙어있는 선택권, 즉 무언가를 선택할 수 있는 상황의 가치.

| Real option | 필기 정리 |
|-------------|-----------|
| Timing options | 더 많은 정보와 더 나은 판단을 위해 투자를 유보할 선택권 |
| Abandonment options | 이미 시작한 사업의 전망이 좋지 않을 경우 사업을 접고 자산을 처분할 권리 |
| Expansion / growth options | 프로젝트가 잘되면 나중에 더 크게 확장할 수 있는 옵션 |
| Flexibility options | 상황 변화에 따라 운영방식을 바꿀 수 있는 유연성 |
| Fundamental options | 천연자원 개발 프로젝트의 real options |

Abandonment option은 더 많은 손실을 입기 전에 사업을 접을 수 있다는 것 자체가 가치 있다.

Expansion option은 처음 투자를 작게 시작해도 이 사업이 엄청 커질 경우 확장할 수 있는 가치다.

Flexibility option의 예시:

- Price setting options: allow the company to change the price of a product. 상황에 따라 가격을 바꿀 수 있는 옵션
- Production flexibility options: 무엇을 얼마나 생산할지 조절할 수 있는 옵션

Fundamental option은 석유시추, 광산개발, 벌목 등의 자원 개발 프로젝트를 해당 commodity 가격이 높을 때에 맞춰서 개발하는 옵션이다. Timing option과 유사하다.
