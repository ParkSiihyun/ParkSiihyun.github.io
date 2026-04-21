---
title: "CFA Equity Reading 41 — Market Efficiency"
date: 2026-04-20
categories: cfa
tags: [Equity, CFA Level I, EMH, Market Efficiency]
---

## 1. Informationally Efficient Capital Market

> The current price of a security **fully, quickly and rationally** reflects all available information about that security.

→ 모든 정보는 이미 가격에 반영되어 있기 때문에 모든 주식의 기대수익률은 **시장 위험에 대한 보상**일 뿐이다.

**"You can't beat the market"** → 시장 수익률을 이기기는 어렵다.

- Perfectly efficient market → 투자자는 **passive investment strategy** 사용해야 함
- Active investment strategy는 거래비용 및 운용 수수료로 인해 underperform
- **Only new information should move prices**

---

## 2. Market Value vs Intrinsic Value

| 개념 | 설명 |
|------|------|
| **Market value** | Asset's current price (현재 시장가격) |
| **Intrinsic value** (Real / Fundamental value) | 모든 정보를 가진 합리적 투자자가 기꺼이 지불하려는 가치 |

- **Efficient market**: MV = IV → 오직 새로운 정보만이 IV를 변화시킴
- **Inefficient market**: MV ≠ IV → Active investment의 수익률이 더 높을 수 있음

---

## 3. Factors Affecting Market Efficiency

| 요인 | 방향 |
|------|------|
| **Number of market participants** | 많을수록 시장 효율성 ↑ |
| **Availability of information** | 많을수록 효율성 ↑ (SEC: 애널리스트와 공개에 동일한 정보 제공 요구) |
| **Impediments to trading (장애물)** | 적을수록 효율성 ↑ (차익거래, 공매도가 활발해야 MV를 IV에 맞춤) |
| **Transaction and information costs** | 적을수록 효율성 ↑ |

---

## 4. Efficient Market Hypothesis (EMH)

### Weak Form Market Efficiency

: Current security prices fully reflect all **past security market data** (가격, 거래량 등)

- 과거 가격·거래량 데이터는 미래 가격 예측에 쓸모 없음
- → **Technical analysis**로는 평균적으로 양(+)의 위험조정수익률을 달성할 수 없음

### Semi-Strong Form Market Efficiency

: Security prices rapidly adjust to all **new publicly available information**

- 공개 재무제표, 뉴스, 공시 등이 이미 가격에 반영되어 있음
- → **Fundamental analysis**로는 평균적으로 양(+)의 위험조정수익률을 달성할 수 없음

### Strong Form Market Efficiency

: Security prices fully reflect **all information (public and private)**

- 내부정보(insider information)까지도 가격에 반영되어 있음
- None should be able to consistently achieve positive abnormal returns

---

## 5. Implications of EMH

### Risk Adjusted Returns

- 기대수익률은 CAPM 또는 multifactor model로 계산
- CAPM: **risk taking에 대한 보상** → risk adjusted return
- Real return - CAPM return = **alpha = abnormal return**

> CAPM 수익률이 시장수익률보다 높다고 해서 beat the market 한 것이 아님 → 단지 risk taking에 대한 보상일 뿐  
> **Beat the market은 알파(α)로 측정**

### Technical vs Fundamental Analysis

| 분석 방법 | 설명 |
|-----------|------|
| **Technical analysis** | 기술적 분석: 과거 차트/데이터를 분석 (Weak form에서 무의미) |
| **Fundamental analysis** | 기본적 분석: 재무제표 같은 기업 공시 데이터를 분석 (Semi-strong form에서 무의미) |

> Semi-strong form 효율적 시장이라면 technical & fundamental analysis 모두 무의미  
> **펀드매니저는 왜 존재하는가?** → Portfolio objectives 관리, **Asset allocation** 측면에서 도움이 됨

---

## 6. Market Anomalies

: Something that leads us to reject the hypothesis of market efficiency → **효율적 시장에서 벗어나는 이례현상**

### Time Series Anomalies

**Calendar Anomalies**

- **January effect**: 매년 1월 초 5거래일 동안 주가 수익률(특히 소형주)이 연중 다른 시기보다 현저히 높음
  - *Tax loss selling*: 투자자들이 12월에 손실 종목을 팔아 세금 처리 후 1월에 다시 매수
  - *Window dressing*: 포트폴리오 매니저들이 12월에 위험 종목을 팔고 1월에 다시 매수

- **Weekend / Holiday effects**: 금요일 양(+) 수익률 이후 월요일 음(-) 수익률, 휴일 전 수익률이 높음

- **Overreaction effect**: 과거 3~5년간 주가 수익률이 나빴던 기업이 이후 더 높은 수익률을 보임
  - 늘 잘하는 아이보다 가끔 잘하는 아이의 좋은 소식에 더 크게 반응하는 심리

- **Momentum effect**: 단기적으로 높은 수익률이 이후에도 계속 높은 수익률로 이어짐

> 위 모두 **과거 데이터로 초과수익률**을 낼 수 있기 때문에 **약형 효율적 시장 가설(Weak form EMH)을 반박**하는 증거

### Cross Sectional Anomalies

| 이상현상 | 설명 |
|----------|------|
| **Size effect** | Small cap이 Large cap을 outperform |
| **Value effect** | Value stocks가 Growth stocks를 outperform |

- *Value stocks*: 낮은 PER, 낮은 PBR, 높은 배당수익률 특징
- 모두 현재 재무제표를 보고 초과수익률을 낼 수 있기 때문에 **중강형 효율적 시장(Semi-strong form EMH)을 반박**하는 증거

### Other Anomalies

| 이상현상 | 설명 |
|----------|------|
| **Closed end investment funds** | 펀드 주식이 NAV보다 큰 할인율로 거래되는 현상 (운용수수료, 세금, 규제가 원인) |
| **Earnings surprise** | 예상치 못한 실적이 발표된 날 완전히 반영되지 않고 이후에도 가격 조정 지속 (어닝 서프라이즈 이후 투자하면 초과수익 가능) |
| **IPO** | IPO는 대체로 underpriced → 상장 첫날 주가가 공모가보다 올라가는 경우가 많음. 하지만 장기적으로는 평균 이하 성과 |

### Implications for Investors

- 이러한 이상현상에도 불구하고 **Consistent abnormal return을 얻을 수 없다면**, 시장은 여전히 효율적이다
- 위의 이상현상은 일시적인 현상에 불과할 수 있음

---

## 7. Behavioral Finance

: 투자자들의 실제 의사결정 프로세스를 연구 → 투자자는 완전한 정보를 가진 합리적 효용 극대화자가 아님

| 편향 | 설명 |
|------|------|
| **Loss aversion** | 손실을 동일한 크기의 이익보다 더 싫어함 |
| **Investor overconfidence** | 정보 분석 능력과 MV/IV 차이 식별 능력을 과대평가 |
| **Herding** | 다른 투자자들의 행동을 모방, 자신의 분석이 아닌 군중을 따름 |
| **Information cascade** | 정보가 적은 트레이더가 정보가 많은 트레이더의 행동을 보고 따라함 |

### CFA의 EMH에 대한 견해

> If investor rationality is viewed as a prerequisite for market efficiency → **markets are not efficient**  
> If market efficiency only requires that investors cannot **consistently earn abnormal risk adjusted returns** → **research supports that markets are efficient**
