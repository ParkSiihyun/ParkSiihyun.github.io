# How I Use Bloomberg Terminal to Analyze an M&A Deal

Bloomberg Terminal is not a shortcut around thinking.

It is a research cockpit. The value is not that it gives me a perfect answer.
The value is that it lets me move faster from question to evidence: company
financials, market reaction, analyst estimates, relative valuation, sector
context, news, and deal data.

For this blog, the goal is simple:

> Use Bloomberg to research like a serious student, then publish original
> analysis using my own interpretation and public sources wherever possible.

One important rule: I should not copy proprietary Bloomberg tables, screenshots,
or data dumps into public posts. I can use the Terminal to guide research, check
facts, and shape my analysis, but the blog should rely on my own writing, my own
tables, and public source documents such as press releases, SEC filings, merger
agreements, proxy statements, investor presentations, and earnings transcripts.

## The basic workflow

For every M&A deal, I want Bloomberg to help answer seven questions.

| Step | Question | Bloomberg use | Blog output |
| --- | --- | --- | --- |
| 1 | What happened? | Deal search, news, company overview | Transaction snapshot |
| 2 | Who are the companies? | Company description, financials, segments | Buyer and target profiles |
| 3 | Why this deal? | News, industry research, peers | Strategic rationale |
| 4 | What price was paid? | Market data, multiples, estimates | Valuation bridge |
| 5 | Was the price reasonable? | Peer comparison, historical trading, estimates | My view on valuation |
| 6 | What could go wrong? | News, sector context, regulation, financing | Risk analysis |
| 7 | What did the market think? | Price chart, event window, analyst commentary | Market reaction |

The Terminal helps me gather evidence. The blog post is where I turn that
evidence into judgment.

## Step 1: Build the transaction snapshot

First, I need the clean facts:

- Acquirer
- Target
- Announcement date
- Deal value
- Consideration: cash, stock, or mixed
- Premium
- Status: pending, completed, terminated
- Required approvals
- Expected closing date

Bloomberg functions to explore:

```text
MA <GO>
N <GO>
CN <GO>
DES <GO>
```

`MA <GO>` is useful for finding and screening M&A transactions. `N <GO>` and
`CN <GO>` help with market news and company-specific news. `DES <GO>` gives a
starting overview for the company or security.

The blog version should not be a data dump. It should be a concise table that
explains the transaction.

## Step 2: Understand the buyer and target

Before analyzing the deal, I need to understand the companies as standalone
businesses.

Questions:

- What does each company do?
- How does each company make money?
- What are the main segments?
- Is revenue growing?
- Are margins improving or declining?
- How much debt does the buyer have?
- Is the target profitable?

Bloomberg functions to explore:

```text
DES <GO>
FA <GO>
GP <GO>
HP <GO>
EE <GO>
```

`FA <GO>` is useful for financial analysis. `GP <GO>` and `HP <GO>` help with
price history. `EE <GO>` is useful for analyst estimates, especially when the
deal depends on future growth or margin assumptions.

Blog output:

- One paragraph on the buyer
- One paragraph on the target
- A simple financial snapshot table
- A note on what each company needed from the other

## Step 3: Find the strategic rationale

Strategic rationale is the heart of the case study.

I want to know whether the buyer is trying to:

- Enter a new market
- Defend its existing market
- Acquire technology
- Acquire customers
- Add distribution
- Improve margins
- Accelerate growth
- Replace slowing organic growth
- Consolidate an industry

Bloomberg functions to explore:

```text
N <GO>
CN <GO>
BI <GO>
BICS <GO>
RV <GO>
```

`BI <GO>` can help with industry context. `BICS <GO>` is useful for understanding
industry classification and peer sets. `RV <GO>` helps me compare a company
against peers, which is important when asking whether the buyer paid a strategic
premium.

Blog output:

> My one-sentence thesis: [Buyer] acquired [Target] because [strategic reason],
> and paid [valuation view] to gain [specific asset or capability].

If I cannot write that sentence clearly, I probably do not understand the deal
yet.

## Step 4: Build the valuation bridge

The valuation section should explain the difference between market value and deal
value.

I want to check:

- Unaffected share price
- Offer price
- Premium to unaffected price
- Enterprise value
- Revenue and EBITDA multiples
- Forward estimates
- Peer multiples
- Precedent transaction context, if available

Bloomberg functions to explore:

```text
FA <GO>
RV <GO>
EE <GO>
GP <GO>
HP <GO>
```

The most important question is not simply "what multiple did the buyer pay?"

The better question is:

> What did the buyer need to believe for this price to make sense?

That belief might be higher growth, cost synergies, revenue synergies, margin
expansion, lower risk, strategic scarcity, or defensive value.

## Step 5: Check market context

A deal that looks expensive in one market environment might look normal in
another.

I want to understand:

- Where interest rates were
- Whether equity markets were strong or weak
- Whether the sector was trading at high or low multiples
- Whether M&A financing was attractive
- Whether competitors were consolidating
- Whether regulators were becoming more aggressive

Bloomberg functions to explore:

```text
BTMM <GO>
YC <GO>
ECO <GO>
BI <GO>
RV <GO>
```

This is where Bloomberg can help me write better than a normal student summary.
A deal is not just two companies. It is also a market environment.

## Step 6: Read the actual deal documents

Bloomberg helps me find the story, but public documents help me verify it.

For public-company deals, I should look for:

- Press release
- Investor presentation
- Merger agreement
- Proxy statement
- Tender offer documents
- 8-K
- 10-K and 10-Q filings
- Earnings call transcript

The Terminal can help locate filings and news quickly, but the blog should cite
publicly accessible source documents whenever possible.

This is the discipline:

> Use Bloomberg to discover. Use public documents to verify. Use my own analysis
> to publish.

## Step 7: Analyze market reaction

The market reaction is not always correct, but it is important evidence.

I want to check:

- Buyer stock reaction on announcement day
- Target stock reaction versus offer price
- Whether the spread implies deal risk
- Analyst commentary
- Credit rating or leverage concerns

Bloomberg functions to explore:

```text
GP <GO>
HP <GO>
CN <GO>
N <GO>
```

If the buyer stock falls, I should ask whether investors disliked the price,
strategic logic, financing, or integration risk. If the buyer stock rises, I
should ask what the market believes the buyer is gaining.

## My Bloomberg-to-blog system

Here is the process I want to use each time:

1. Pick one deal.
2. Spend 20 minutes in Bloomberg building the transaction snapshot.
3. Spend 30 minutes on buyer and target fundamentals.
4. Spend 30 minutes on valuation and peers.
5. Spend 20 minutes on market context.
6. Pull public documents and verify the key facts.
7. Write the one-sentence thesis.
8. Draft the case study using my M&A framework.
9. Build my own simple tables.
10. End with a clear view: good deal, fair deal, or bad deal.

The Terminal gives me speed. The blog should show judgment.

## Content this can create

Bloomberg can support several recurring series:

| Series | Format | Example |
| --- | --- | --- |
| Deal Teardown | Full case study | Why Microsoft bought LinkedIn |
| Function Diary | Short research note | What `RV <GO>` teaches about peer valuation |
| Market Context | Research log | What rates looked like before a major acquisition |
| Valuation Watch | Weekly table and commentary | SaaS multiples this week |
| Filing vs Terminal | Verification post | What Bloomberg summarized vs what the proxy actually said |
| Interview Prep | Concept applied to real company | EV vs equity value using a live company |

This is the edge: most students can summarize a deal. Fewer can connect the deal
to live market data, peer valuation, financing conditions, and public filings.

## First Bloomberg-backed posts to write

1. `How I Use Bloomberg Terminal to Analyze an M&A Deal`
2. `What RV <GO> Taught Me About Relative Valuation`
3. `How to Read an M&A Press Release Like a Banker`
4. `Microsoft-LinkedIn Revisited: Strategic Premium or Overpayment?`
5. `Deal Spread 101: What the Target Stock Price Says After Announcement`

The goal is not to become a Bloomberg power user overnight.

The goal is to make every research note a little more evidence-based than the
last one.
