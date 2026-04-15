---
title: "Glossary — Derivatives M10: Valuing a Derivative Using a One-Period Binomial Model"
type: glossary
subject: derivatives
module: "M10"
created: 2026-04-12
updated: 2026-04-12
tags: [glossary, derivatives, binomial, risk-neutral, hedge-ratio]
---

# Glossary — M10: Valuing a Derivative Using a One-Period Binomial Model

| Term | Definition |
|---|---|
| **Binomial model** | A discrete-time option pricing framework where the underlying can move to one of exactly two possible values (up or down) in each period |
| **Up factor ($u$)** | The multiplicative factor by which the stock price increases in the up state: $S^+ = S_0 \times u$ where $u > 1$ |
| **Down factor ($d$)** | The multiplicative factor by which the stock price decreases in the down state: $S^- = S_0 \times d$ where $d < 1$ |
| **Hedge ratio ($h$)** | The number of shares of the underlying needed to replicate one option: $h = (c^+ - c^-)/(S^+ - S^-)$; also called delta |
| **Risk-neutral probability ($\pi$)** | The probability of an up move in the risk-neutral framework: $\pi = (1 + r - d)/(u - d)$; not the actual probability of an up move |
| **Risk-neutral pricing** | A valuation method that discounts expected payoffs (computed using risk-neutral probabilities) at the risk-free rate: $c_0 = [\pi c^+ + (1-\pi)c^-]/(1+r)$ |
| **One-period binomial model** | The simplest binomial framework with a single time step from today to expiration; the foundation for multi-period models |
| **Replicating portfolio (binomial)** | A portfolio of $h$ shares of stock plus borrowing/lending at the risk-free rate that exactly replicates the option payoff in both up and down states |
| **No-arbitrage condition (binomial)** | The requirement that $d < (1 + r) < u$ — the risk-free return must lie between the down and up returns to prevent arbitrage |
| **Risk-neutral world** | A theoretical construct where all assets earn the risk-free rate; option prices derived in this world are valid in the real world because of no-arbitrage |

## See Also

- [[derivatives/concepts/option-valuation|Option Valuation]]
- [[derivatives/concepts/arbitrage-and-replication|Arbitrage and Replication]]
- [[derivatives/formulas/der-formulas|Derivatives Formula Sheet]]
- [[derivatives/glossary/der-m09|Glossary — M09]]
