---
title: "Asset-Backed Security Instrument and Market Features (Reading 64)"
date: 2026-05-04
categories: cfa
tags: [Fixed Income, CFA Level I, ABS, Covered Bonds, CDO, CLO, Reading 64]
excerpt: "Sihyun CFA Notes - Asset-Backed Security Instrument and Market Features (Reading 64)"
---

## Quick Take

- 중심 주제: **Asset-Backed Security Instrument and Market Features**
- 먼저 잡을 축: Covered Bonds, Credit Enhancement in Covered Bonds, Hard Bullet vs Soft Bullet Covered Bonds
- 본문은 원본 필기 흐름을 유지하면서 정의, 비교, 공식, 예제를 읽기 좋게 정리한다.

## Reading Map

1. Covered Bonds
2. Credit Enhancement in Covered Bonds
3. Hard Bullet vs Soft Bullet Covered Bonds
4. ABS Credit Enhancement
5. Tranching and Waterfall
6. Credit Card ABS
7. CDO, CBO, and CLO

## Main Notes

## 1. Covered Bonds

Covered bonds are debt obligations backed by a cover pool, often mortgage loans.

Unlike typical ABS, the underlying assets usually remain on the issuer's balance sheet, and no SPE is created.

| Feature | Covered bond |
|------|------|
| Collateral | Cover pool, usually high-quality loans |
| Balance sheet | Assets remain with issuer |
| Credit tranching | Usually not used |
| Investor recourse | Dual recourse to cover pool and issuer |

---

## 2. Credit Enhancement in Covered Bonds

Covered bond investors have **dual recourse**:

1. claim on the cover pool
2. claim on other assets of the issuer

The value of the cover pool is usually greater than the face value of covered bonds issued.

This overcollateralization helps reduce credit risk.

---

## 3. Hard Bullet vs Soft Bullet Covered Bonds

| Type | Description |
|------|------|
| **Hard bullet** | Default may be triggered if scheduled payment is missed |
| **Soft bullet** | Maturity can be extended, often up to one year |

Soft bullet structures can reduce refinancing pressure at maturity.

---

## 4. ABS Credit Enhancement

Common credit enhancement structures:

| Enhancement | Description |
|------|------|
| **Overcollateralization** | Collateral value exceeds ABS face value |
| **Excess spread** | Collateral income exceeds payments owed to ABS investors |
| **Credit tranching** | Multiple tranches absorb losses in priority order |

---

## 5. Tranching and Waterfall

ABS cash flows and losses are allocated through a priority structure.

| Tranche | Position |
|------|------|
| Senior tranche | Paid first, absorbs losses last |
| Mezzanine tranche | Middle priority |
| Equity tranche | Paid last, absorbs losses first |

The junior or equity tranche protects senior tranches by absorbing initial credit losses.

<figure class="sh-diagram">
  <img src="/images/cfa/reading64-waterfall-tranching.svg" alt="ABS waterfall showing cash priority and loss absorption across senior mezzanine and equity tranches">
  <figcaption>Waterfall 구조에서는 cash는 senior부터 내려가고, 손실은 equity부터 올라가며 senior tranche를 보호한다.</figcaption>
</figure>

---

## 6. Credit Card ABS

Credit card receivable-backed securities are backed by pools of credit card debt owed to banks.

These structures often include a lockout or revolving period to keep the collateral pool relatively stable before principal repayment begins.

---

## 7. CDO, CBO, and CLO

| Instrument | Collateral |
|------|------|
| **CDO** | Pool of debt obligations |
| **CBO** | Corporate and emerging market bonds |
| **CLO** | Leveraged bank loans |

### CLO Types

| Type | Cash flow source |
|------|------|
| **Cash flow CLO** | Cash flows from underlying loans |
| **Market value CLO** | Trading value of collateral |
| **Synthetic CLO** | Credit derivative exposure rather than direct ownership |

### Exam Points

- Covered bonds remain on the issuer's balance sheet and provide dual recourse.
- ABS tranching creates different risk levels from the same collateral pool.
- Junior tranches absorb losses before senior tranches.
- CLO collateral is usually leveraged bank loans.
