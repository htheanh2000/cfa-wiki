---
title: "Glossary — Derivatives M05: Pricing and Valuation of Forward Contracts"
type: glossary
subject: derivatives
module: "M05"
created: 2026-04-12
updated: 2026-04-12
tags: [glossary, derivatives, forwards, FRA, pricing, valuation]
---

# Glossary — M05: Pricing and Valuation of Forward Contracts

| Term | Definition |
|---|---|
| **Forward price** | The price ($F_0(T)$) agreed at inception for future delivery, determined by no-arbitrage: $F_0(T) = S_0 \times (1+r)^T$ |
| **Forward value** | The current worth of an existing forward contract to a party; zero at inception, fluctuates during the contract's life: $V_t = S_t - F_0(T)/(1+r)^{T-t}$ |
| **Forward rate agreement (FRA)** | A forward contract on an interest rate; the buyer (long) profits if the market reference rate exceeds the agreed forward rate at settlement |
| **Implied forward rate (IFR)** | The future interest rate implied by current spot rates for adjacent periods; the rate that makes the FRA have zero value at inception |
| **No-arbitrage forward price** | The forward price derived from the cost of carry model that eliminates arbitrage opportunities |
| **Cost of carry (in forward pricing)** | The net cost of holding the underlying: $F_0(T) = [S_0 - PV(I) + PV(C)] \times (1+r)^T$, where $I$ = income, $C$ = costs |
| **Carry benefits** | Income received from holding the underlying (dividends, coupons, convenience yield) that reduces the forward price |
| **Carry costs** | Costs incurred from holding the underlying (storage, insurance, financing) that increases the forward price |
| **Physical settlement** | Forward settlement by delivering the actual underlying asset in exchange for the forward price |
| **Cash settlement** | Forward settlement by paying the cash difference between the spot price at expiration and the forward price |
| **Off-market forward** | A forward contract with a non-zero value at inception because the forward price is set away from the no-arbitrage level; requires a cash payment to compensate |
| **Settlement amount (FRA)** | $= \frac{(\text{MRR} - \text{IFR}) \times \text{Notional} \times \text{Period}}{1 + \text{MRR} \times \text{Period}}$ — the PV of the rate difference paid at settlement |

## See Also

- [[derivatives/concepts/forward-commitments|Forward Commitments]]
- [[derivatives/concepts/arbitrage-and-replication|Arbitrage and Replication]]
- [[derivatives/glossary/der-m04|Glossary — M04]]
- [[derivatives/glossary/der-m06|Glossary — M06]]
