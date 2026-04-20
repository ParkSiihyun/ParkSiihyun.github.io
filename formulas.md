---
layout: single
title: ""
permalink: /formulas/
author_profile: false
toc: true
toc_sticky: true
toc_label: "Sections"
---

<div class="sh-page-hero">
  <div class="sh-page-hero__eyebrow">Cheatsheet</div>
  <h1 class="sh-page-hero__title">Formula Cheatsheet</h1>
  <p class="sh-page-hero__lede">
    The core valuation and modeling formulas I reach for most — kept in one
    place for quick review before case studies and exams.
  </p>
</div>

## Valuation

<div class="sh-formula">
  <h3 class="sh-formula__name">Enterprise Value (EV)</h3>
  <code class="sh-formula__eq">EV = Market Cap + Debt + Preferred + Minority Interest − Cash</code>
  <p class="sh-formula__note">Total value to all capital providers. Use EV multiples when comparing companies with different capital structures.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Unlevered Free Cash Flow (FCFF)</h3>
  <code class="sh-formula__eq">FCFF = EBIT × (1 − T) + D&amp;A − CapEx − Δ Working Capital</code>
  <p class="sh-formula__note">The cash flow available to <em>all</em> investors before any financing effects. The numerator in an unlevered DCF.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Terminal Value — Gordon Growth</h3>
  <code class="sh-formula__eq">TV = FCF<sub>n+1</sub> / (WACC − g)</code>
  <p class="sh-formula__note">Assumes perpetual growth <em>g</em> beyond the forecast period. Keep <em>g</em> at or below long-run GDP growth (~2–3%).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Terminal Value — Exit Multiple</h3>
  <code class="sh-formula__eq">TV = EBITDA<sub>n</sub> × Exit Multiple</code>
  <p class="sh-formula__note">Uses the terminal-year EBITDA and a peer-derived multiple. Cross-check against Gordon growth for sanity.</p>
</div>

## Cost of Capital

<div class="sh-formula">
  <h3 class="sh-formula__name">WACC</h3>
  <code class="sh-formula__eq">WACC = (E/V) × R<sub>e</sub> + (D/V) × R<sub>d</sub> × (1 − T)</code>
  <p class="sh-formula__note">Blended after-tax cost of capital. Weights use <em>market</em> values, not book.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Cost of Equity — CAPM</h3>
  <code class="sh-formula__eq">R<sub>e</sub> = R<sub>f</sub> + β × (R<sub>m</sub> − R<sub>f</sub>)</code>
  <p class="sh-formula__note">Rf = risk-free rate (10Y UST); β = systematic risk; (Rm − Rf) = equity risk premium (~5–6%).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Unlevered / Re-levered Beta</h3>
  <code class="sh-formula__eq">β<sub>U</sub> = β<sub>L</sub> / (1 + (1 − T) × D/E)</code>
  <p class="sh-formula__note">Strip out peer leverage to get a pure-play business beta, then re-lever to your target's capital structure.</p>
</div>

## Multiples

<div class="sh-formula">
  <h3 class="sh-formula__name">EV / EBITDA</h3>
  <code class="sh-formula__eq">EV / EBITDA</code>
  <p class="sh-formula__note">The most common enterprise-level multiple. Capital-structure neutral and mostly D&amp;A-neutral.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">P / E</h3>
  <code class="sh-formula__eq">Share Price / EPS  =  Equity Value / Net Income</code>
  <p class="sh-formula__note">Equity multiple. Affected by capital structure — only compare within similar leverage profiles.</p>
</div>

## M&amp;A

<div class="sh-formula">
  <h3 class="sh-formula__name">Accretion / Dilution Quick Test (cash deal)</h3>
  <code class="sh-formula__eq">Accretive if:  Target Net Income Yield  &gt;  After-tax Cost of Cash</code>
  <p class="sh-formula__note">Target NI yield = Target NI / Purchase Price. After-tax cost of cash = cash interest rate × (1 − T).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Accretion / Dilution Quick Test (stock deal)</h3>
  <code class="sh-formula__eq">Accretive if:  Acquirer P/E  &gt;  Target effective P/E</code>
  <p class="sh-formula__note">Effective target P/E = (Purchase Price + Target Debt − Target Cash) / Target Net Income.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Synergy Value</h3>
  <code class="sh-formula__eq">Synergy Value = Σ PV(after-tax synergies) − PV(integration costs)</code>
  <p class="sh-formula__note">Revenue synergies deserve heavy skepticism; cost synergies are usually more credible.</p>
</div>

## Financial Ratios

<div class="sh-formula">
  <h3 class="sh-formula__name">Current Ratio / Quick Ratio</h3>
  <code class="sh-formula__eq">Current = Current Assets / Current Liabilities
Quick   = (Cash + ST Inv. + AR) / Current Liabilities</code>
  <p class="sh-formula__note">Short-term liquidity. Quick excludes inventory (harder to convert to cash quickly).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Interest Coverage</h3>
  <code class="sh-formula__eq">EBIT / Interest Expense</code>
  <p class="sh-formula__note">How many times operating earnings cover interest. Below 2–3x is a red flag.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Net Debt / EBITDA</h3>
  <code class="sh-formula__eq">(Total Debt − Cash) / EBITDA</code>
  <p class="sh-formula__note">A leverage ratio. IB / LBO speak: "4.5x levered". High-yield covenants often cap this.</p>
</div>

---

*Something missing? I add to this page as I study — send me a note at [sihyup2@uci.edu](mailto:sihyup2@uci.edu).*
