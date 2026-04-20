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
    The valuation, modeling, and finance formulas I reach for most — organized
    the way my brain organizes them. Written as a practitioner's reference, not
    a textbook appendix. Equations are on the left; the note under each one is
    where it actually lives.
  </p>
</div>

## Valuation

<div class="sh-formula">
  <h3 class="sh-formula__name">Enterprise Value (EV)</h3>
  <code class="sh-formula__eq">EV = Market Cap + Total Debt + Preferred Equity + Minority Interest − Cash &amp; Equivalents</code>
  <p class="sh-formula__note">Total value to <em>all</em> capital providers. Use EV multiples whenever capital structures differ. Mental check: if you bought every share and took over every dollar of debt, this is the enterprise-level price tag.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Equity Value (bridge from EV)</h3>
  <code class="sh-formula__eq">Equity Value = EV − Debt − Preferred − Minority Interest + Cash</code>
  <p class="sh-formula__note">The "equity bridge" — the single most common source of errors in valuation. Always use the <em>net</em> of debt and cash; always subtract preferred and minority at the EV → equity step, never at the EBITDA step.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Unlevered Free Cash Flow (FCFF)</h3>
  <code class="sh-formula__eq">FCFF = EBIT × (1 − T) + D&amp;A − CapEx − Δ NWC</code>
  <p class="sh-formula__note">Cash available to <em>all</em> investors before any financing effects. The numerator in an unlevered DCF. Discount at WACC to get EV.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Levered Free Cash Flow (FCFE)</h3>
  <code class="sh-formula__eq">FCFE = Net Income + D&amp;A − CapEx − Δ NWC + Net Borrowing</code>
  <p class="sh-formula__note">Cash available to <em>equity holders only</em>. Discount at cost of equity to get equity value directly. Used heavily in bank / FIG valuation.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Terminal Value — Gordon Growth</h3>
  <code class="sh-formula__eq">TV = FCF<sub>n+1</sub> / (WACC − g)</code>
  <p class="sh-formula__note">Perpetual-growth method. Keep <em>g</em> at or below long-run GDP (~2–3% US). An implied growth > nominal GDP means the company eventually becomes the entire economy — wrong by construction.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Terminal Value — Exit Multiple</h3>
  <code class="sh-formula__eq">TV = EBITDA<sub>n</sub> × Exit Multiple</code>
  <p class="sh-formula__note">Terminal-year EBITDA × a peer-derived multiple. Always cross-check by backing out the <em>implied</em> perpetual growth rate — if it's 6%, your multiple is too high.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Discounting Terminal Value</h3>
  <code class="sh-formula__eq">PV(TV) = TV / (1 + WACC)<sup>n</sup></code>
  <p class="sh-formula__note">Always discount TV back to today using the same WACC and the same period count as your final forecast cash flow. A classic error is double-discounting or off-by-one on <em>n</em>.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Adjusted Present Value (APV)</h3>
  <code class="sh-formula__eq">APV = EV<sub>unlevered</sub> + PV(Tax Shield) − PV(Financial Distress Costs)</code>
  <p class="sh-formula__note">Value as if all-equity, then layer in the financing side effects. Preferred when capital structure changes dramatically over the forecast (LBOs, project finance).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Dividend Discount Model (Gordon)</h3>
  <code class="sh-formula__eq">P<sub>0</sub> = D<sub>1</sub> / (R<sub>e</sub> − g)</code>
  <p class="sh-formula__note">Equity value of a stable, dividend-paying stock. Breaks down when g ≥ Re or when payout ratio is lumpy. Most useful for utilities, banks, and mature staples.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Residual Income Model</h3>
  <code class="sh-formula__eq">V<sub>0</sub> = B<sub>0</sub> + Σ [(ROE − R<sub>e</sub>) × B<sub>t-1</sub>] / (1 + R<sub>e</sub>)<sup>t</sup></code>
  <p class="sh-formula__note">Starts from book value, adds the PV of "economic profit" (returns above cost of equity). Strong for firms with reliable accounting and low/irregular dividends.</p>
</div>

## Cost of Capital

<div class="sh-formula">
  <h3 class="sh-formula__name">WACC</h3>
  <code class="sh-formula__eq">WACC = (E/V) × R<sub>e</sub> + (D/V) × R<sub>d</sub> × (1 − T)</code>
  <p class="sh-formula__note">Blended after-tax cost of capital. Weights are <em>market</em> values, not book. The (1 − T) only applies to debt because interest is tax-deductible; equity gets no such shield.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Cost of Equity — CAPM</h3>
  <code class="sh-formula__eq">R<sub>e</sub> = R<sub>f</sub> + β × (R<sub>m</sub> − R<sub>f</sub>)</code>
  <p class="sh-formula__note">R<sub>f</sub> = 10Y UST; β = systematic risk; (R<sub>m</sub> − R<sub>f</sub>) = equity risk premium (historically ~5–6%). The workhorse formula despite its flaws.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Cost of Equity — Build-Up Method</h3>
  <code class="sh-formula__eq">R<sub>e</sub> = R<sub>f</sub> + ERP + Size Premium + Specific-Company Premium</code>
  <p class="sh-formula__note">The valuation-for-private-company alternative to CAPM when no reliable beta exists. Size and specific-company premiums are judgment calls — document your reasoning.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Unlever / Re-lever Beta (Hamada)</h3>
  <code class="sh-formula__eq">β<sub>U</sub> = β<sub>L</sub> / [1 + (1 − T) × D/E]
β<sub>L</sub> = β<sub>U</sub> × [1 + (1 − T) × D/E]</code>
  <p class="sh-formula__note">Strip peer leverage to isolate business risk, then re-lever to your target's capital structure. Use median peer β<sub>U</sub> to reduce noise.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Cost of Debt (after-tax)</h3>
  <code class="sh-formula__eq">R<sub>d, after-tax</sub> = YTM × (1 − T)</code>
  <p class="sh-formula__note">Use <em>yield to maturity</em> on the firm's outstanding debt, not the coupon. For private companies, use a synthetic rating (interest coverage → implied credit spread).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Country Risk Premium (Damodaran approach)</h3>
  <code class="sh-formula__eq">CRP = Country Default Spread × (σ<sub>Equity</sub> / σ<sub>Bond</sub>)</code>
  <p class="sh-formula__note">Layer on top of the mature-market ERP when valuing emerging-market assets. Quick proxy: just use the sovereign credit spread.</p>
</div>

## Multiples

<div class="sh-formula">
  <h3 class="sh-formula__name">EV / EBITDA</h3>
  <code class="sh-formula__eq">EV / EBITDA</code>
  <p class="sh-formula__note">The most universal enterprise-level multiple. Capital-structure neutral and mostly D&amp;A-neutral. Industry benchmarks: 8–12x mature industrials, 15–25x software, 6–8x distressed cyclicals.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">EV / EBIT</h3>
  <code class="sh-formula__eq">EV / EBIT</code>
  <p class="sh-formula__note">Penalizes capital-intensive businesses (high D&amp;A) more than EV/EBITDA. More honest for comparing asset-heavy firms like airlines, telecom, semis.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">EV / (EBITDA − CapEx)</h3>
  <code class="sh-formula__eq">EV / (EBITDA − CapEx)</code>
  <p class="sh-formula__note">Buffett's preferred variant. Treats maintenance CapEx as a real cost. Useful when comparing firms with wildly different reinvestment needs.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">EV / Sales</h3>
  <code class="sh-formula__eq">EV / Revenue</code>
  <p class="sh-formula__note">The last-resort multiple for pre-profitability companies (early-stage SaaS, biotech). Meaningless across industries with different margin profiles.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">P / E</h3>
  <code class="sh-formula__eq">Share Price / EPS  =  Equity Value / Net Income</code>
  <p class="sh-formula__note">The most-quoted but most-abused multiple. Affected by leverage, tax rate, non-operating items. Only compare within similar capital structures.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">PEG Ratio</h3>
  <code class="sh-formula__eq">PEG = P/E  /  Earnings Growth Rate (%)</code>
  <p class="sh-formula__note">Peter Lynch's shortcut. < 1 is cheap, > 2 is expensive — roughly. Breaks down for low-growth or negative-growth firms.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">P / B</h3>
  <code class="sh-formula__eq">Share Price / Book Value per Share</code>
  <p class="sh-formula__note">The go-to for banks and asset-heavy financials. A P/B &lt; 1 often signals either distressed or cheap — check ROE vs. cost of equity to distinguish.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Justified P/B</h3>
  <code class="sh-formula__eq">P/B  =  (ROE − g) / (R<sub>e</sub> − g)</code>
  <p class="sh-formula__note">What a firm's P/B <em>should</em> be given its returns and cost of equity. If ROE = R<sub>e</sub>, P/B should equal 1. Powerful sanity check for bank valuation.</p>
</div>

## M&amp;A

<div class="sh-formula">
  <h3 class="sh-formula__name">Accretion / Dilution — Cash Deal</h3>
  <code class="sh-formula__eq">Accretive if:  Target NI Yield  &gt;  After-tax Cost of Cash
Target NI Yield = Target Net Income / Purchase Price
After-tax Cost of Cash = Cash Interest Rate × (1 − T)</code>
  <p class="sh-formula__note">The 30-second test every MD runs in their head before taking a pitch seriously. Below the hurdle, the deal dilutes Year-1 EPS.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Accretion / Dilution — Stock Deal</h3>
  <code class="sh-formula__eq">Accretive if:  Acquirer P/E  &gt;  Target effective P/E
Target effective P/E = (Purchase Price + Target Debt − Target Cash) / Target NI</code>
  <p class="sh-formula__note">A high-multiple acquirer can buy a lower-multiple target with stock and instantly print EPS — the "multiple arbitrage" that drove 2000s roll-ups.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Exchange Ratio</h3>
  <code class="sh-formula__eq">Exchange Ratio = Offer Price per Target Share / Acquirer Share Price</code>
  <p class="sh-formula__note">Number of acquirer shares issued per target share. Fixed ratio → acquirer bears the price risk; fixed value → target bears it. Collars split the difference.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Breakeven Synergies</h3>
  <code class="sh-formula__eq">Breakeven Pre-tax Synergies = Control Premium × Target Equity Value × (1 / (1 − T))</code>
  <p class="sh-formula__note">The level of synergies required to justify the premium. If the number looks impossible to hit, the deal is probably value-destructive.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Synergy Value</h3>
  <code class="sh-formula__eq">Synergy Value = Σ PV(after-tax synergies) − PV(integration costs)</code>
  <p class="sh-formula__note">Revenue synergies deserve heavy skepticism (historically ~30% realized); cost synergies are more credible (~60–70%). Always haircut management's number.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Contribution Analysis</h3>
  <code class="sh-formula__eq">Contribution % = Acquirer Metric / (Acquirer + Target Metric)</code>
  <p class="sh-formula__note">In a stock-for-stock merger-of-equals, compare each party's contribution to revenue, EBITDA, EPS, and cash flow vs. their pro-forma ownership split. Fairness opinion staple.</p>
</div>

## LBO Mechanics

<div class="sh-formula">
  <h3 class="sh-formula__name">Sources &amp; Uses</h3>
  <code class="sh-formula__eq">Sources: Debt + Sponsor Equity + Rollover Equity + Excess Cash
Uses:    Purchase Equity + Refinance Debt + Transaction &amp; Financing Fees

Sources = Uses</code>
  <p class="sh-formula__note">Every LBO model starts here. If Sources ≠ Uses, nothing downstream is right. Purchase Equity = Offer per Share × Diluted Shares.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Purchase Price (Enterprise Basis)</h3>
  <code class="sh-formula__eq">Purchase EV = Purchase Equity + Assumed Debt − Acquired Cash</code>
  <p class="sh-formula__note">LBO candidates usually have their debt refinanced, so assumed debt hits Uses as a refi payoff. "Cash-free, debt-free" deal structure is the standard.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Money-on-Money / MoIC</h3>
  <code class="sh-formula__eq">MoIC = Exit Equity Proceeds / Initial Sponsor Equity</code>
  <p class="sh-formula__note">The return the LP cares about after IRR. Target for a 5-year LBO: 2.0x–3.0x MoIC. Below 2.0x and the deal "worked but didn't print."</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">IRR (Quick Estimate from MoIC)</h3>
  <code class="sh-formula__eq">IRR ≈ MoIC<sup>(1/n)</sup> − 1</code>
  <p class="sh-formula__note">Rough check: 2.0x over 5 years ≈ 15% IRR; 2.5x over 5 years ≈ 20%; 3.0x over 5 years ≈ 25%. The "rule of 72" cousin for PE.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Debt Paydown (Cash Sweep)</h3>
  <code class="sh-formula__eq">Mandatory Repayment + 75–100% × Excess FCF → Revolver / Term Loan</code>
  <p class="sh-formula__note">LBO value creation lever #1. Every dollar of debt paid down is a dollar of equity value created, all else equal.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">LBO Value Creation Bridge</h3>
  <code class="sh-formula__eq">Δ Equity Value = EBITDA Growth + Multiple Expansion + Debt Paydown − Fees</code>
  <p class="sh-formula__note">The attribution everyone runs at exit. Best deals earn on all three; levered beta plays earn only on multiple expansion and are the risky kind.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Sponsor Promote / Carry Waterfall</h3>
  <code class="sh-formula__eq">1. Return of capital to LPs
2. Preferred return (8% hurdle) to LPs
3. GP catch-up
4. 80/20 split thereafter (LP/GP)</code>
  <p class="sh-formula__note">Standard PE waterfall. 20% carry above an 8% hurdle is market; mega-funds sometimes negotiate lower hurdles or tiered splits.</p>
</div>

## Bond Math

<div class="sh-formula">
  <h3 class="sh-formula__name">Current Yield</h3>
  <code class="sh-formula__eq">Current Yield = Annual Coupon / Current Market Price</code>
  <p class="sh-formula__note">Ignores price movement to maturity — useful only for a quick income read.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Yield to Maturity (approximation)</h3>
  <code class="sh-formula__eq">YTM ≈ [C + (F − P) / n]  /  [(F + P) / 2]</code>
  <p class="sh-formula__note">C = annual coupon, F = face, P = price, n = years. Good enough for back-of-envelope. Use a solver for accuracy.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Macaulay Duration</h3>
  <code class="sh-formula__eq">D<sub>Mac</sub> = Σ [t × CF<sub>t</sub> / (1+y)<sup>t</sup>]  /  Price</code>
  <p class="sh-formula__note">Weighted-average time to receive cash flows. Units are years. Equals maturity for a zero-coupon bond.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Modified Duration</h3>
  <code class="sh-formula__eq">D<sub>Mod</sub> = D<sub>Mac</sub> / (1 + y)</code>
  <p class="sh-formula__note">% price change for a 1-percentage-point yield move: ΔP/P ≈ −D<sub>Mod</sub> × Δy. A 7-year duration bond drops ~7% for a 100 bps yield rise.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">DV01 (Dollar Value of 01)</h3>
  <code class="sh-formula__eq">DV01 = D<sub>Mod</sub> × Price × 0.0001</code>
  <p class="sh-formula__note">Dollar change in price for a 1 bp yield move. Rates desk staple. Trading books run daily DV01 limits.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Convexity Adjustment</h3>
  <code class="sh-formula__eq">ΔP/P ≈ −D<sub>Mod</sub> × Δy + ½ × Convexity × (Δy)<sup>2</sup></code>
  <p class="sh-formula__note">Duration alone understates price gains and overstates losses for large yield moves. The convexity term corrects this; positive convexity is a feature of vanilla bonds.</p>
</div>

## Time Value of Money

<div class="sh-formula">
  <h3 class="sh-formula__name">Present Value / Future Value</h3>
  <code class="sh-formula__eq">PV = FV / (1 + r)<sup>n</sup>
FV = PV × (1 + r)<sup>n</sup></code>
  <p class="sh-formula__note">The single most important relationship in finance. If you can't do this in your head for small numbers, stop and drill until you can.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">PV of Ordinary Annuity</h3>
  <code class="sh-formula__eq">PV = C × [1 − (1 + r)<sup>−n</sup>] / r</code>
  <p class="sh-formula__note">Equal cash flow C at the end of each period for n periods. Bond coupon streams, mortgage payments, fixed pensions.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">PV of Perpetuity</h3>
  <code class="sh-formula__eq">PV = C / r</code>
  <p class="sh-formula__note">Flat cash flow C forever. The mental anchor for all terminal-value math.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">PV of Growing Perpetuity</h3>
  <code class="sh-formula__eq">PV = C<sub>1</sub> / (r − g)</code>
  <p class="sh-formula__note">Same as Gordon Growth. Requires r &gt; g; otherwise the result is negative or undefined.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Continuous Compounding</h3>
  <code class="sh-formula__eq">FV = PV × e<sup>r × n</sup></code>
  <p class="sh-formula__note">The limit as compounding frequency → ∞. Ubiquitous in derivatives pricing (Black-Scholes assumes it).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Effective Annual Rate (EAR)</h3>
  <code class="sh-formula__eq">EAR = (1 + APR/m)<sup>m</sup> − 1</code>
  <p class="sh-formula__note">Converts a stated APR with <em>m</em> compounding periods into the true annualized rate. A 12% APR compounded monthly = 12.68% EAR.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Net Present Value (NPV Rule)</h3>
  <code class="sh-formula__eq">NPV = Σ CF<sub>t</sub> / (1 + r)<sup>t</sup>  −  Initial Investment
Accept if NPV &gt; 0</code>
  <p class="sh-formula__note">The theoretical gold standard for investment decisions. Beats IRR when cash flows are non-conventional or projects are mutually exclusive.</p>
</div>

## DCF Mechanics

<div class="sh-formula">
  <h3 class="sh-formula__name">Mid-Year Convention</h3>
  <code class="sh-formula__eq">Discount Factor<sub>t</sub> = 1 / (1 + WACC)<sup>(t − 0.5)</sup></code>
  <p class="sh-formula__note">Assumes cash flows arrive mid-year rather than year-end. Increases PV by ~(WACC/2). Standard in bank-side DCFs.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Stub Period</h3>
  <code class="sh-formula__eq">Discount Factor<sub>stub</sub> = 1 / (1 + WACC)<sup>(days / 365)</sup></code>
  <p class="sh-formula__note">For the partial first year between the valuation date and fiscal year-end. Don't forget to pro-rate the forecast cash flow to match.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Implied Terminal Growth (from Exit Multiple)</h3>
  <code class="sh-formula__eq">g = WACC − (FCF<sub>n+1</sub> / TV)</code>
  <p class="sh-formula__note">The sanity check I run on every exit-multiple TV. If implied g &gt; GDP growth, you're inflating the outcome.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Enterprise to Equity Value (DCF Output)</h3>
  <code class="sh-formula__eq">Equity Value = EV − Debt − Preferred − Minority Interest + Cash − Other Non-Op Liabilities + Other Non-Op Assets</code>
  <p class="sh-formula__note">The full bridge in practice. Don't forget unfunded pension, operating lease liabilities (if you added back rent), and investments in unconsolidated affiliates.</p>
</div>

## Financial Ratios

<div class="sh-formula">
  <h3 class="sh-formula__name">Current / Quick / Cash Ratio</h3>
  <code class="sh-formula__eq">Current = Current Assets / Current Liabilities
Quick   = (Cash + ST Inv. + AR) / Current Liabilities
Cash    = (Cash + ST Inv.) / Current Liabilities</code>
  <p class="sh-formula__note">Tightening definitions of short-term liquidity. Quick excludes inventory (can't always sell it fast); Cash excludes AR (customers may not pay).</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Interest Coverage</h3>
  <code class="sh-formula__eq">EBIT / Interest Expense</code>
  <p class="sh-formula__note">How many times operating earnings cover interest. &lt; 2–3x is a red flag; rating-agency grid usually wants &gt; 4x for investment grade.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Net Debt / EBITDA</h3>
  <code class="sh-formula__eq">(Total Debt − Cash) / EBITDA</code>
  <p class="sh-formula__note">The leverage ratio IB/LBO speak: "4.5x levered." High-yield covenants often cap this. LBO sponsors target 5–7x at close, delever to 2–3x at exit.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Debt / Capital</h3>
  <code class="sh-formula__eq">Total Debt / (Total Debt + Book Equity)</code>
  <p class="sh-formula__note">Used in credit analysis and WACC weighting (market-value version). 30–40% is typical investment-grade; 60%+ is high yield territory.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Asset Turnover</h3>
  <code class="sh-formula__eq">Revenue / Avg Total Assets</code>
  <p class="sh-formula__note">How much revenue each dollar of assets produces. Retail &gt; 2x; capital-intensive industries often &lt; 1x. A component of DuPont ROE.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Inventory Turnover &amp; Days</h3>
  <code class="sh-formula__eq">Inv Turnover = COGS / Avg Inventory
Days Inventory = 365 / Inv Turnover</code>
  <p class="sh-formula__note">High turnover = efficient operations or thin margins; low turnover = slow-moving or over-ordered. Compare within industry only.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Cash Conversion Cycle</h3>
  <code class="sh-formula__eq">CCC = DSO + DIO − DPO</code>
  <p class="sh-formula__note">Days from spending cash on inventory to collecting from customers. Amazon famously runs negative CCC — suppliers finance their inventory.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">DuPont — 3-Step</h3>
  <code class="sh-formula__eq">ROE = (NI / Sales) × (Sales / Assets) × (Assets / Equity)
    = Net Margin × Asset Turnover × Equity Multiplier</code>
  <p class="sh-formula__note">Decomposes ROE into profitability, efficiency, and leverage. If ROE rose only because of leverage, that's a red flag.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">DuPont — 5-Step</h3>
  <code class="sh-formula__eq">ROE = (NI/EBT) × (EBT/EBIT) × (EBIT/Sales) × (Sales/Assets) × (Assets/Equity)
    = Tax Burden × Interest Burden × Operating Margin × Asset Turnover × Leverage</code>
  <p class="sh-formula__note">The CFA-favored version. Splits out tax and interest effects so you can isolate pure operating performance.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Return on Invested Capital (ROIC)</h3>
  <code class="sh-formula__eq">ROIC = NOPAT / Invested Capital
NOPAT = EBIT × (1 − T)
Invested Capital = Debt + Equity − Cash  (or Net PP&amp;E + NWC)</code>
  <p class="sh-formula__note">The truest profitability metric — ignores capital structure. If ROIC &gt; WACC, the firm creates value. If ROIC &lt; WACC, growth destroys value.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Economic Value Added (EVA)</h3>
  <code class="sh-formula__eq">EVA = (ROIC − WACC) × Invested Capital</code>
  <p class="sh-formula__note">Dollar value of economic profit created in a year. Captures the spread that multiples and earnings miss. Stern Stewart's contribution to the world.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Altman Z-Score (Public Manufacturers)</h3>
  <code class="sh-formula__eq">Z = 1.2 × (NWC/Assets) + 1.4 × (Retained Earnings/Assets)
   + 3.3 × (EBIT/Assets) + 0.6 × (Market Equity/Total Liab) + 1.0 × (Sales/Assets)</code>
  <p class="sh-formula__note">Z &gt; 2.99 = safe zone; 1.81–2.99 = grey; &lt; 1.81 = distress. Developed by Edward Altman in 1968 and still remarkably predictive.</p>
</div>

## Options &amp; Hedging (Quick Reference)

<div class="sh-formula">
  <h3 class="sh-formula__name">Put-Call Parity</h3>
  <code class="sh-formula__eq">C − P = S − K × e<sup>−rT</sup></code>
  <p class="sh-formula__note">The no-arbitrage relationship between a European call and put on the same underlying, strike, and expiry. Violations are pure arbitrage.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Treasury Stock Method (TSM)</h3>
  <code class="sh-formula__eq">Net New Shares = Options Outstanding − (Options × Strike) / Current Share Price</code>
  <p class="sh-formula__note">Converts in-the-money options into the net share count for diluted EPS and diluted equity value. Only in-the-money options count.</p>
</div>

<div class="sh-formula">
  <h3 class="sh-formula__name">Convertible Conversion Value</h3>
  <code class="sh-formula__eq">Conversion Value = Conversion Ratio × Current Share Price
Conversion Ratio = Face Value / Conversion Price</code>
  <p class="sh-formula__note">What the bond would be worth if converted today. A convert trades at max(conversion value, straight bond value).</p>
</div>

---

*Something missing or wrong? I add to this page as I study — send me a note at [sihyup2@uci.edu](mailto:sihyup2@uci.edu).*
