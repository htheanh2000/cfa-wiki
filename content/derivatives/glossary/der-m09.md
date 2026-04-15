---
title: "Glossary — Derivatives M09: Option Replication Using Put-Call Parity"
type: glossary
subject: derivatives
module: "M09"
created: 2026-04-12
updated: 2026-04-12
tags: [glossary, derivatives, put-call-parity, synthetic, protective-put, fiduciary-call]
---

# Glossary — M09: Option Replication Using Put-Call Parity

| Term | Definition |
|---|---|
| **Protective put** | A portfolio of long stock + long put; provides downside protection while maintaining upside participation. Payoff: $\max(S_T, X)$ |
| **Fiduciary call** | A portfolio of long call + risk-free bond (face value $X$); produces the same payoff as a protective put: $\max(S_T, X)$ |
| **Put-call parity** | The no-arbitrage relationship linking European call and put prices: $S_0 + p_0 = c_0 + X/(1+r)^T$ |
| **Synthetic call** | A position replicating a call option: long stock + long put + borrow PV of strike |
| **Synthetic put** | A position replicating a put option: long call + short stock + lend PV of strike |
| **Synthetic stock** | A position replicating long stock: long call + short put + lend PV of strike |
| **Synthetic bond** | A position replicating a risk-free bond: long stock + long put + short call (covered call + protective put) |
| **Put-call forward parity** | Put-call parity using the forward price: $F_0(T)/(1+r)^T + p_0 = c_0 + X/(1+r)^T$ |
| **Covered call** | A portfolio of long stock + short call; generates premium income but caps upside at the strike price |
| **Conversion** | An arbitrage strategy exploiting put-call parity violations: long stock + long put + short call = synthetic bond; compare yield to actual risk-free rate |

## See Also

- [[derivatives/concepts/put-call-parity|Put-Call Parity]]
- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/glossary/der-m08|Glossary — M08]]
- [[derivatives/glossary/der-m10|Glossary — M10]]
