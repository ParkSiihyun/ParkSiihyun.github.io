---
title: "CFA Derivatives Topic 5 - Pricing and Valuation of Options"
date: 2026-05-07
categories: cfa
tags: [Derivatives, CFA Level I, Options, Put Call Parity, Binomial Model]
---

## 1. Options vs Forwards

**Option** = right, but not obligation, to buy or sell an underlying asset.

| Contract | Long position |
|------|------|
| Forward | Obligation to transact |
| Option | Right to exercise |

Options require an upfront premium because the long side receives a valuable right.

---

## 2. Call and Put Options

| Option | Right |
|------|------|
| **Call option** | Right to buy the underlying |
| **Put option** | Right to sell the underlying |

| Exercise style | Meaning |
|------|------|
| **European option** | Can be exercised only at expiration |
| **American option** | Can be exercised any time before or at expiration |

American option value is at least as high as European option value with the same terms.

---

## 3. Option Payoff at Expiration

| Position | Payoff |
|------|------|
| Long call | $$\max(S_T - K, 0)$$ |
| Short call | $$-\max(S_T - K, 0)$$ |
| Long put | $$\max(K - S_T, 0)$$ |
| Short put | $$-\max(K - S_T, 0)$$ |

<figure class="sh-diagram">
  <img src="/images/cfa/derivatives-topic5-option-payoffs.svg" alt="Payoff profiles for long call short call long put and short put options">
  <figcaption>Call은 upside exposure, put은 downside protection 또는 downside exposure를 만든다.</figcaption>
</figure>

---

## 4. Moneyness

| Moneyness | Call option | Put option |
|------|------|------|
| **In the money** | $$S > K$$ | $$S < K$$ |
| **At the money** | $$S \approx K$$ | $$S \approx K$$ |
| **Out of the money** | $$S < K$$ | $$S > K$$ |

Intrinsic value:

$$\text{Call Intrinsic Value} = \max(S - K, 0)$$

$$\text{Put Intrinsic Value} = \max(K - S, 0)$$

Option value:

$$\text{Option Value} = \text{Intrinsic Value} + \text{Time Value}$$

---

## 5. Factors Affecting Option Value

| Factor increases | Call value | Put value |
|------|------|------|
| Underlying price | Higher | Lower |
| Strike price | Lower | Higher |
| Risk-free rate | Higher | Lower |
| Time to expiration | Usually higher | Usually higher |
| Volatility | Higher | Higher |
| Dividends / benefits | Lower | Higher |

Volatility increases both call and put values because it increases upside potential for the option holder while downside is limited to the premium.

---

## 6. Put-Call Parity

For European options on a non-dividend-paying asset:

$$S_0 + p_0 = c_0 + \frac{K}{(1+r)^T}$$

This can be read as:

| Portfolio | Components |
|------|------|
| **Protective put** | Long stock + long put |
| **Fiduciary call** | Long call + present value of strike |

These portfolios have the same payoff at expiration, so they must have the same value today.

### Synthetic Positions

$$S_0 = c_0 - p_0 + \frac{K}{(1+r)^T}$$

$$p_0 = c_0 - S_0 + \frac{K}{(1+r)^T}$$

$$c_0 = S_0 + p_0 - \frac{K}{(1+r)^T}$$

---

## 7. Put-Call Forward Parity

If forward price is used:

$$F_{0,T} = S_0(1+r)^T$$

Then:

$$p_0 + \frac{F_{0,T}}{(1+r)^T} = c_0 + \frac{K}{(1+r)^T}$$

Forward parity is especially useful when the underlying forward price is easier to observe than the spot-and-carry package.

---

## 8. Option Bounds

European call lower bound:

$$c_0 \geq \max\left(0, S_0 - \frac{K}{(1+r)^T}\right)$$

European put lower bound:

$$p_0 \geq \max\left(0, \frac{K}{(1+r)^T} - S_0\right)$$

American put lower bound:

$$P_0 \geq \max(0, K - S_0)$$

---

## 9. Binomial Model

The binomial model values options by:

1. modeling up and down moves in the underlying
2. calculating option payoffs at expiration
3. discounting expected payoff under risk-neutral probabilities

Risk-neutral probability:

$$\pi_u = \frac{(1+r) - d}{u - d}$$

Option value:

$$V_0 = \frac{\pi_u V_u + (1-\pi_u)V_d}{1+r}$$

### Exam Points

- Long options have rights; short options have obligations.
- Long call payoff is $$\max(S_T-K,0)$$; long put payoff is $$\max(K-S_T,0)$$.
- Option value equals intrinsic value plus time value.
- Put-call parity links stock, call, put, and risk-free bond.
- Volatility increases both call and put values.
- Binomial valuation uses risk-neutral probabilities and discounted expected payoff.

