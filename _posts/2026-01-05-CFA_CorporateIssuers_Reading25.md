---
title: "Capital Structure (Reading 25)"
date: 2026-01-05
categories: cfa
tags: [Corporate Issuers, CFA Level I, Reading 25, Corporate Issuers]
excerpt: "Sihyun CFA Notes - Capital Structure (Reading 25)"
---

## Quick Take

- 중심 주제: **Capital Structure**
- 먼저 잡을 축: WACC, debt capacity, MM propositions, tax shield, financial distress, pecking order
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. WACC and target capital structure
2. Debt capacity across life cycle
3. MM propositions
4. Taxes, financial distress, static tradeoff theory
5. Pecking order theory

## Main Notes

## 1. WACC

**WACC(weighted average cost of capital)**:

```text
WACC
= (weight of debt * pretax cost of debt * (1 - tax rate))
+ (weight of equity * cost of equity)
```

필기 예시:

| 항목 | 값 |
|------|----|
| Weight of debt | 50% |
| Weight of equity | 50% |
| Cost of debt | 8% |
| Cost of equity | 11% |
| Tax rate | 30% |

```text
WACC = (0.5 * 0.08 * 0.7) + (0.5 * 0.11)
     = 0.083
     = 8.3%
```

기업은 WACC를 최소화하는 capital structure를 target으로 한다.

## 2. Debt Capacity

회사의 자본구조에서 debt 비율에 영향을 주는 characteristics:

- company's capacity to service debt.
- stability of revenue.
- growth and predictability of cash flow.
- amount and liquidity of company assets.
- cost and availability of debt financing.
- amount of business risk.

일반적으로 기업이 안정적이고, 예측가능하고, 반복적인 현금흐름을 만들어낼수록 capital structure에서 debt 비율을 더 높일 수 있다.

Debt를 더 감당하기 좋은 회사:

- companies in non-cyclical industries.
- companies with low fixed operating costs.
- companies with subscription-based revenue.

영업레버리지가 높으면 sales가 조금만 움직여도 operating profit이 크게 흔들린다. 그래서 고정비 비율이 낮고 영업레버리지가 낮은 회사가 debt financing에 더 유리하다.

## 3. Debt-to-Equity Across Life Cycle

| Stage | 특징 |
|-------|------|
| Start-up stage | high business risk, high required interest rate, debt financing이 너무 비싸서 주로 equity financing, convertible debt 가능 |
| Growth stage | business risk somewhat reduced, debt financing cost somewhat reduced, investors may be willing to lend |
| Mature stage | cash flow가 significant and relatively stable, unsecured debt 포함 debt financing을 낮은 cost로 사용할 수 있음 |

## 4. Modigliani and Miller

**Modigliani and Merton Miller theory**:

- capital structure theory.
- the value of a firm is unaffected by its capital structure.

### MM Proposition 1: No Taxes

- operating income is independent of how the firm is financed.
- operating earnings are unaffected by financing decisions.
- debt와 equity 비율이 어떻게 달라져도 total value of debt and equity는 변하지 않는다.

### MM Proposition 2: Cost of Equity and Leverage

- debt financing은 원금과 이자를 법적으로 보장하기 때문에 cost of equity보다 cost of debt가 싸다.
- 그래서 기업은 비용이 더 싼 debt financing을 늘리려는 선택을 할 수 있다.
- 하지만 debt 비율이 증가하면 equity holders에게 돌아가는 cash flow의 risk가 증가한다.
- 주주들은 더 높은 required return을 요구하고 cost of equity가 상승한다.
- debt를 늘려 얻는 financing cost 감소분은 cost of equity 증가로 정확히 상쇄된다.
- 결과적으로 firm's WACC는 변하지 않는다.

MM Proposition 2의 구조:

```text
re = r0 + (D/E)(r0 - rd)
```

| 기호 | 의미 |
|------|------|
| `re` | levered firm cost of equity |
| `r0` | unlevered firm cost of equity |
| `rd` | cost of debt |
| `D/E` | debt-to-equity ratio |

## 5. MM with Taxes

Taxes가 있으면 debt는 tax shield를 제공한다.

- firms use debt financing because debt provides tax shield.
- tax shield는 tax rate와 debt amount에 의해 결정된다.
- 부채를 사용하는 기업이 tax shield 때문에 더 많은 수익을 남긴다.

```text
Value of levered firm = Value of unlevered firm + Value of tax shield
```

이 관점에서는 debt 100%를 사용하는 것이 WACC를 최소화하고 firm value를 극대화하는 길이다.

## 6. Costs of Financial Distress

Financial distress cost는 debt financing level이 높아질수록 증가한다.

1. **Costs of financial distress and bankruptcy**
   - direct costs: cash expenses associated with bankruptcy.
   - indirect costs: customers, creditors, suppliers, employees의 trust를 잃는 비용.

2. **Probability of financial distress**
   - financial leverage가 높아질수록 financial distress probability가 증가한다.

## 7. Static Tradeoff Theory

**Static tradeoff theory**:

- debt 사용으로 얻는 tax shield benefit과 financial distress cost를 balance한다.
- 파산비용과 세금 방어막이 정확히 상쇄되는 지점이 optimal capital structure.

```text
Value of levered firm
= Value of unlevered firm
+ PV(tax shield)
- PV(costs of financial distress)
```

흐름:

- debt가 늘면 처음에는 tax shield 때문에 firm value가 증가하고 WACC가 감소한다.
- 어느 지점 이후에는 expected financial distress cost가 tax benefit을 압도한다.
- 그때부터 firm value는 감소하고 WACC는 증가한다.

## 8. MM 정리

| 이론 | 결론 |
|------|------|
| MM with no taxes and no costs of financial distress | capital structure is irrelevant, WACC와 firm value는 변하지 않음 |
| MM with taxes but no costs of financial distress | WACC is minimized and firm value is maximized with 100% debt |
| Static tradeoff theory | tax shield benefit과 financial distress cost가 balance되는 지점이 optimal capital structure |

## 9. Analyst가 Target Capital Structure를 추정하는 법

- current capital structure를 보고 유추한다.
- 이때 book value가 유용한 경우도 있다.
- 같은 업계 기업들의 average capital structure를 보고 유추한다.

## 10. Pecking Order Theory

**Pecking order theory**:

- asymmetric information에 기반한다.
- management가 financing choice를 통해 investors에게 signal을 보낸다는 생각과 관련된다.
- 가장 부정적인 신호를 주는 자금조달 방법을 가장 마지막에 사용한다.

Financing preference:

1. internally generated capital is most preferred.
2. debt is the next best choice.
3. external equity is the least preferred financing option.

이 이론은 기업이 optimal D/E를 찾는 것이 아니라, 자금조달 선호 순서를 따른다고 본다.
