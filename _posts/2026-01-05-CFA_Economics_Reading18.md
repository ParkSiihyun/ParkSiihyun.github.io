---
title: "Capital Flows and the FX Market (Reading 18)"
date: 2026-01-05 12:00:00 -0800
categories: cfa
tags: [Economics, CFA Level I, Reading 18, Economics]
excerpt: "Sihyun CFA Notes - Capital Flows and the FX Market (Reading 18)"
---

## Quick Take

- 중심 주제: **Capital Flows and the FX Market**
- 먼저 잡을 축: FX market participants, quote conventions, exchange rate regimes, balance of payments
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. FX market participants와 exchange rate quote
2. Exchange rate regimes
3. Changes in exchange rates
4. Balance of payments와 open economy identity
5. Capital restrictions

## Main Notes

## 1. The Foreign Exchange Market

Many companies have foreign exchange risk from cross-border transactions. 이 risk를 관리하기 위해 **forward currency contract**를 사용할 수 있다.

| Side | Participants |
|------|--------------|
| Sell side | primary dealers, large multinational banks |
| Buy side | corporations, investment accounts, governments and government entities, retail FX market |

Retail FX market에는 tourism, cross-border investment, speculative trading이 포함된다.

## 2. Types of Exchange Rates

| Term | 필기 정리 |
|------|-----------|
| Base currency | 기준이 되는 통화 |
| Price currency | 가격으로 표시되는 통화 |
| Direct quote | 외국 통화 한 단위당 자국 통화 몇 단위. 한국 기준 1달러당 1500원 |
| Indirect quote | 자국 통화 한 단위당 외국 통화 몇 단위. 예: 1원당 몇 달러 |
| Nominal exchange rate | exchange rate at a point in time |
| Real exchange rate | the purchasing power of one currency |
| Spot exchange rate | immediate delivery를 위한 exchange rate. 보통 trade 후 two business days |
| Forward exchange rate | 미래 exchange를 위한 exchange rate. 보통 단기라 30/360 방법 사용 |

$$\text{Real Exchange Rate}=\text{Nominal Exchange Rate}\times\frac{P_{foreign}}{P_{domestic}}$$

## 3. Calculating Percentage Change in FX Value

예시:

$$USD/EUR: 1.42 \to 1.39$$

이 quote에서 **base currency는 EUR**다.

$$\frac{1.39}{1.42}-1=-2.11\%$$

- 유로 가치가 달러 대비 **2.11% 평가절하(depreciated)** 되었다고 표현한다.
- 달러 가치가 유로 대비 2.11% 평가절상되었다고 바로 말하면 안 된다. base currency가 유로이기 때문이다.

달러가 유로 대비 얼마나 절상되었는지 보려면 USD를 base currency로 바꾼다.

$$EUR/USD:\frac{1}{1.42}\to\frac{1}{1.39}$$

$$\frac{(1/1.39)}{(1/1.42)}-1=2.16\%$$

달러 가치는 유로 대비 **2.16% 평가절상(appreciated)** 되었다고 표현한다.

## 4. Exchange Rate Regimes

### Countries Without Their Own Currency

| Regime | 필기 정리 |
|--------|-----------|
| Formal dollarization | 통화가 없는 국가가 dollar를 공식 통화로 사용 |
| Monetary union | 여러 국가가 common currency를 사용. 예: EU |

통화가 없는 국가는 독자적 통화정책을 가질 수 없고, 새로운 통화를 발행할 수도 없다.

### Countries With Their Own Currency

| Regime | 필기 정리 |
|--------|-----------|
| Currency board arrangement | 자국 통화를 특정 외국 통화에 고정하고 100% 외환보유액으로 뒷받침 |
| Conventional fixed peg | 자국 통화를 특정 통화에 일정 환율로 고정, 보통 +/- 1% 범위 |
| Target zone | 특정 permitted fluctuation 범위 안에서 움직이도록 허용 |
| Crawling peg | fixed peg를 유지하되 고정환율 자체를 점진적으로 조정 |
| Crawling bands | crawling peg + target zone, permissible band를 점진적으로 조정 |
| Managed floating | 평소에는 수요/공급에 따라 움직이나 필요하면 정부 개입 |
| Independently floating | 변동환율제도 |

### Currency Board Arrangement

- 강한 fixed exchange rate 제도다.
- Hong Kong처럼 currency가 equivalent amount of US dollars로 fully backed될 때만 발행되는 구조.
- “우리 돈은 언제든지 정해진 환율로 달러와 바꿔주겠다”는 약속에 가깝다.
- 자국 통화를 발행할 때 그만큼의 달러 외환보유액을 보유해야 한다.
- 통화남발이 어려워 인플레이션 억제에 도움이 된다.
- 고정환율제도이므로 환율 안정으로 무역과 투자 안정성이 증가한다.
- 독자적 통화정책은 거의 불가능하다.

### Conventional Fixed Peg

- currency board보다 약한 제도다.
- 예를 들어 한국이 1달러를 1300원에 고정하는 식이다.
- 중앙은행은 환율이 오르면 외환시장에 개입해 목표범위 내에 두려고 한다.
- currency board와 달리 어느 정도 통화정책이 가능하다.
- 외환보유액 100%가 필요하지 않다.

### Crawling Peg

- 인플레이션이 높은 국가에서 고정환율제도를 쓰면 자국 상품의 외화 표시가격이 매우 높아질 수 있다.
- 그래서 인플레이션에 맞춰 환율도 조금씩 평가절하시켜주는 것이 맞다.

## 5. Changes in Exchange Rates

환율 변동은 수입과 수출에 영향을 미친다.

- `USD/EUR` 환율이 상승하면 dollar value가 상승한다.
- 외화표시가격, 즉 달러의 유로표시가격이 상승하기 때문에 미국 수출이 줄어든다.
- 반대로 미국 내 유럽상품의 달러표시가격은 하락하므로 수입이 증가한다.

## 6. Balance of Payments

핵심 관계:

$$\text{Current Account}+\text{Capital Account}=0$$

다시 말해:

$$\text{경상수지}+\text{자본수지}=0$$

| Account | 의미 |
|---------|------|
| Current account | 나라의 실물 거래 흐름. 무역수지가 포함됨 |
| Trade balance | 수출 - 수입 |
| Capital account | 돈이 어떻게 들어오고 나가는지. 외국인 주식투자, 채권투자, 부동산 투자, 해외 대출 등 |

### Current Account and Capital Account

- 수출을 많이 해서 경상수지 흑자가 나면 외화를 많이 벌어들인다.
- 그러면 그 돈이 해외자산 투자 등으로 다시 나가야 하므로 자본수지는 적자가 된다.
- 수입을 많이 해서 외화가 부족하면 경상수지는 적자다.
- 그 부족한 돈을 해외 자본 유입으로 메워야 하므로 자본수지는 흑자다.
- 즉 미국이 중국과의 무역에서 자본수지 흑자를 봤다는 것은 중국인의 해외 자산이 증가했다는 것과 연결된다.

## 7. Open Economy Identity

$$X-M=(S-I)+(T-G)$$

순수출은 민간저축과 정부저축으로 볼 수 있다.

도출:

$$Y=C+I+G+(X-M)$$

$$I+X-M=Y-C-G$$

$$S=Y-C-G$$

따라서:

$$S=I+X-M$$

$$S-I=X-M$$

### NX가 양수인 경우

- 국내 저축이 국내 투자보다 많다.
- 남은 저축은 해외투자(net capital outflow)로 나간다.
- 해외 투자하려면 원화를 공급하고 달러로 바꿔야 한다.
- 원화가치가 절하된다.

### NX가 음수인 경우

- 국내 저축이 국내 투자보다 적다.
- 해외에서 자본을 가져와야 한다(net capital inflow).
- 해외 자본이 들어와 원화로 바뀐다.
- 원화 수요가 증가하고 원화가치가 절상된다.

## 8. Capital Restrictions

자본시장을 얼마나 개방할 것인가? 왜 자본시장을 규제하나?

| 이유 | 필기 정리 |
|------|-----------|
| Reduce volatility of domestic asset prices | 해외자본 유입은 국내 자산가격 변동성을 키울 수 있음 |
| Maintain fixed exchange rates | 고정환율 유지 |
| Keep domestic interest rates low | 자본이 해외로 빠져나가지 않고 국내에서 돌아야 낮은 이자율 유지 가능 |
| Protect strategic industries | 전략 산업 보호 |
