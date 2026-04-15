---
title: "Glossary — Derivatives M08: Pricing and Valuation of Options"
type: glossary
subject: derivatives
module: "M08"
created: 2026-04-12
updated: 2026-04-12
tags: [glossary, derivatives, options, moneyness, bounds]
---

# Glossary — M08: Pricing and Valuation of Options

| Term | Definition |
|---|---|
| **Exercise (intrinsic) value** | The payoff if the option were exercised immediately: $\max(0, S - X)$ for calls, $\max(0, X - S)$ for puts |
| **Time value** | The portion of the option premium that exceeds the exercise value; reflects the probability of favorable price movement before expiration |
| **Moneyness** | The relationship between the underlying price and the strike price, determining whether exercise would be profitable |
| **In-the-money (ITM)** | An option with positive exercise value: $S > X$ for calls, $S < X$ for puts |
| **At-the-money (ATM)** | An option where the underlying price approximately equals the strike price ($S \approx X$) |
| **Out-of-the-money (OTM)** | An option with zero exercise value that would not be exercised: $S < X$ for calls, $S > X$ for puts |
| **Deep in-the-money** | An option that is significantly ITM; behaves increasingly like the underlying (call) or a short position (put) |
| **Deep out-of-the-money** | An option that is significantly OTM; has very low probability of being exercised and minimal time value |
| **Lower bound (call)** | The minimum value of a European call: $c_0 \geq \max(0,\; S_0 - X/(1+r)^T)$ |
| **Lower bound (put)** | The minimum value of a European put: $p_0 \geq \max(0,\; X/(1+r)^T - S_0)$ |
| **Upper bound (call)** | The maximum value of a call: $c_0 \leq S_0$ (can never exceed the underlying price) |
| **Upper bound (put)** | The maximum value of a European put: $p_0 \leq X/(1+r)^T$; American put: $P_0 \leq X$ |
| **Option premium** | The market price of an option = exercise value + time value |
| **Time decay (theta)** | The erosion of an option's time value as expiration approaches; all else equal, options lose value over time |
| **Volatility effect** | Higher volatility increases the value of both calls and puts because it raises the probability of large favorable payoffs while the downside is limited to the premium |

## See Also

- [[derivatives/concepts/option-valuation|Option Valuation]]
- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/glossary/der-m07|Glossary — M07]]
- [[derivatives/glossary/der-m09|Glossary — M09]]
