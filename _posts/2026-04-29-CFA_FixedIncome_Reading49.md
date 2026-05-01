---
title: "CFA Fixed Income Reading 49 — Fixed Income Issuance and Trading"
date: 2026-04-29
categories: cfa
tags: [Fixed Income, CFA Level I, Bond Market, Primary Market, Secondary Market]
---

## 1. Bond Market Overview

채권시장은 발행자, 신용등급, 만기, 담보 여부 등에 따라 분류된다.

| 분류 기준 | 내용 |
|------|------|
| **Type of issuer** | Government, Corporate, SPE 등 |
| **Credit quality** | Investment grade vs High yield |
| **Original maturity** | Money market / Intermediate-term / Long-term |
| **Security** | Secured vs Unsecured |

---

## 2. Credit Quality

채권 신용등급은 발행자의 원리금 상환 능력을 평가한다. 대표적인 신용평가사로는 **S&P**와 **Moody's**가 있다.

| 구분 | S&P 기준 | Moody's 기준 | 의미 |
|------|------|------|------|
| **Investment Grade** | BBB- 이상 | Baa3 이상 | 상대적으로 낮은 신용위험 |
| **High Yield** | BB+ 이하 | Ba1 이하 | 높은 신용위험, 높은 요구수익률 |

- Investment grade bond = 신용위험이 낮은 채권
- High yield bond = speculative grade / junk bond
- **Fallen angel**: 원래 investment grade였으나 신용등급 하락으로 high yield가 된 발행자

---

## 3. Original Maturity

| 구분 | 만기 |
|------|------|
| **Money Market Securities** | 1년 이하 |
| **Intermediate-term Securities** | 1년 초과 ~ 10년 |
| **Long-term Securities** | 10년 초과 |

- 1년 초과 채권은 일반적으로 **Capital Market Securities**로 분류된다.

---

## 4. Credit / Maturity Spectrum

신용위험과 만기에 따라 채권상품은 스펙트럼상에 위치한다.

| 상대적 위치 | 예시 |
|------|------|
| Short-term / Low risk | Treasury bills, Repo |
| Short-term corporate funding | Commercial Paper, CDs, ABCP |
| Medium to long-term government | Treasury notes, Treasury bonds |
| Securitized products | ABS, MBS |
| Investment grade corporate | Unsecured investment grade corporate bonds |
| High risk corporate | High yield corporate bonds, Leveraged loans |

<figure class="sh-diagram">
  <img src="/images/cfa/reading49-credit-maturity-spectrum.svg" alt="Credit and maturity spectrum for fixed income instruments">
  <figcaption>Credit risk generally rises as issuers become weaker, while maturity risk rises as the time to principal repayment extends.</figcaption>
</figure>

### Key Points

- 영업현금흐름이 불안정한 회사는 debt 발행 시 투자자에게 **담보(security)**를 제공해야 할 가능성이 높다.
- 신용등급이 낮아질수록 투자자는 더 높은 yield를 요구한다.
- 담보가 있으면 투자자는 default 발생 시 회수 가능성이 높아진다.

---

## 5. Investor Positioning

투자자별로 선호하는 credit / maturity exposure가 다르다.

| 투자자 | 선호 자산 / 이유 |
|------|------|
| **Pension funds / Insurance companies** | 장기 부채와 매칭하기 위해 장기 investment grade securities에 투자 |
| **Corporations** | 초과 유동성 운용을 위해 CP, repo, ABCP 등에 투자 |
| **Central banks** | 통화정책 수행을 위해 Treasury notes 등 중기 국채 활용 |
| **Hedge funds / Distressed debt funds** | High yield, distressed debt 등 고위험 자산에 투자 |

<figure class="sh-diagram">
  <img src="/images/cfa/reading49-investor-positioning.svg" alt="Investor positioning by maturity and credit risk">
  <figcaption>Investor positioning is driven by liability matching, liquidity needs, policy goals, and risk appetite.</figcaption>
</figure>

### Central Bank Open Market Operations

- 중앙은행은 국채 매입/매도를 통해 commercial banks의 reserves를 조절한다.
- 국채 매입 → 은행 reserves 증가 → 유동성 증가
- 국채 매도 → 은행 reserves 감소 → 유동성 감소

---

## 6. Fixed Income Indexes

Fixed income index는 equity index보다 구성 종목 수가 많고 turnover가 높다.

### 왜 채권지수는 더 복잡한가?

1. Corporate bond issuers는 여러 종류의 채권을 동시에 발행할 수 있다.
   - 주식은 보통 한 회사당 common equity 한 종목이지만, 채권은 만기/쿠폰/선순위/담보 여부가 다른 여러 종목이 존재한다.

2. 채권은 만기가 있고 계속 새로 발행된다.
   - 만기 도래, 상환, 신규 발행 때문에 index constituents의 removal / replacement가 자주 발생한다.
   - 이를 **turnover**라고 한다.

3. 정부는 대규모 채권 발행자이다.
   - Broad bond index는 sovereign debt 비중이 클 수 있다.
   - Debt issuance trend의 변화는 maturity, credit quality, sector weight에 영향을 준다.

### Aggregate Index

**Aggregate index** = 다양한 sector와 maturity의 채권을 폭넓게 포함한 지수

- 예시: Bloomberg Barclays Aggregate Index
- Broad bond index는 government, corporate, securitized bonds 등 여러 sector를 포함할 수 있다.

### Benchmark 선택 기준

Bond fund의 benchmark는 fund의 실제 exposure와 맞아야 한다.

| 기준 | 설명 |
|------|------|
| **Sector focus** | Government, corporate, securitized 등 |
| **Credit quality** | Investment grade / high yield |
| **Maturity** | Short / intermediate / long-term |
| **Currency exposure** | 투자 통화와 benchmark 통화의 일치 여부 |

---

## 7. Primary Market

**Primary market** = issuer가 새로 발행한 채권을 투자자에게 판매하고 자본을 조달하는 시장

| 방식 | 내용 |
|------|------|
| **Public Offering** | 증권 규제기관에 등록 후 일반 투자자에게 판매 |
| **Private Placement** | 선택된 투자자에게만 판매 |
| **Debut Issuer** | 최초로 채권을 발행하는 issuer |

대부분의 primary market transaction은 investment bank 등 금융중개기관을 통해 이루어진다.

<figure class="sh-diagram">
  <img src="/images/cfa/reading49-primary-secondary-markets.svg" alt="Primary market and secondary market bond trading flow">
  <figcaption>Primary market transactions raise new capital for issuers; secondary market transactions transfer existing bonds through dealers and investors.</figcaption>
</figure>

### Underwritten vs Best Efforts Offering

| 구분 | 설명 |
|------|------|
| **Underwritten Offering** | 금융중개기관이 bond issue price를 보장 |
| **Best Efforts Offering** | 금융중개기관이 판매를 위해 노력하지만 issue price를 보장하지 않음 |

### Shelf Registration

**Shelf registration** = 채권 발행자가 일정 aggregate value의 채권 발행을 미리 등록하고, 필요할 때마다 순차적으로 발행하는 방식

- Master prospectus로 등록
- issuer가 자금이 필요할 때 발행 가능
- 반복 발행이 많은 회사에 유용

### Public Auction

- 일부 채권, 특히 government bonds는 public auction 방식으로 판매된다.

---

## 8. Secondary Market

**Secondary market** = 이미 발행된 채권이 투자자들 사이에서 거래되는 시장

- 채권 거래의 대부분은 **dealer / OTC market**에서 이루어진다.
- Dealer는 bid price와 ask price를 제시한다.

| 가격 | 의미 |
|------|------|
| **Bid price** | Dealer가 채권을 매수하려는 가격 |
| **Ask / Offer price** | Dealer가 채권을 매도하려는 가격 |
| **Bid-ask spread** | Dealer의 거래 수익 또는 liquidity cost |

### Spread와 Liquidity

Bid-ask spread는 채권의 유동성에 따라 달라진다.

| 채권 유형 | Spread |
|------|------|
| 최근 발행된 developed market sovereign bonds | 매우 좁음 |
| High credit quality corporate frequent issuers | 좁음 |
| Seasoned / off-the-run bonds | 더 넓음 |
| Low liquidity / lower credit quality bonds | 넓음 |

> 유동성이 좋을수록 거래 비용이 낮고, 유동성이 낮을수록 dealer가 더 넓은 spread를 요구한다.
