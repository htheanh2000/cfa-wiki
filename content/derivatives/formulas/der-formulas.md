---
title: Derivatives — Master Formula Sheet
type: formula
subject: derivatives
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, formulas, forwards, futures, swaps, options, binomial, put-call-parity]
---

# Derivatives — Master Formula Sheet

---

## 1. Forward Payoff

**Long forward payoff**:

$$\text{Payoff}_{\text{long}} = S_T - F_0(T)$$

**Short forward payoff**:

$$\text{Payoff}_{\text{short}} = F_0(T) - S_T$$

where $S_T$ = spot price at expiration, $F_0(T)$ = forward price agreed at inception.

---

## 2. Option Payoff

**Long call**:

$$c_T = \max(0,\; S_T - X)$$

**Long put**:

$$p_T = \max(0,\; X - S_T)$$

**Short call**:

$$-c_T = -\max(0,\; S_T - X)$$

**Short put**:

$$-p_T = -\max(0,\; X - S_T)$$

where $X$ = strike (exercise) price.

---

## 3. Option Profit

$$\text{Profit}_{\text{long call}} = \max(0,\; S_T - X) - c_0$$

$$\text{Profit}_{\text{long put}} = \max(0,\; X - S_T) - p_0$$

$$\text{Profit}_{\text{short call}} = c_0 - \max(0,\; S_T - X)$$

$$\text{Profit}_{\text{short put}} = p_0 - \max(0,\; X - S_T)$$

where $c_0$, $p_0$ = option premium paid/received at inception.

---

## 4. Forward Pricing

**No-arbitrage forward price** (no income, no costs):

$$F_0(T) = S_0 \times (1 + r)^T$$

**With carry costs and income**:

$$F_0(T) = \bigl[S_0 - PV_0(I) + PV_0(C)\bigr] \times (1 + r)^T$$

where:
- $S_0$ = current spot price
- $r$ = risk-free rate per period
- $PV_0(I)$ = present value of income/benefits (dividends, coupons, convenience yield)
- $PV_0(C)$ = present value of carrying costs (storage, insurance)

---

## 5. Forward Valuation

**At inception** ($t = 0$):

$$V_0 = 0$$

**During life** ($0 < t < T$):

$$V_t(\text{long}) = S_t - \frac{F_0(T)}{(1 + r)^{T-t}}$$

**At expiration** ($t = T$):

$$V_T = S_T - F_0(T)$$

---

## 6. FRA Cash Settlement

**Forward Rate Agreement** — settlement at expiration of the FRA:

$$\text{Settlement (to long)} = \frac{(\text{MRR} - \text{IFR}) \times \text{Notional} \times \text{Period}}{1 + \text{MRR} \times \text{Period}}$$

where:
- $\text{MRR}$ = market reference rate at settlement (e.g., SOFR)
- $\text{IFR}$ = implied forward rate (agreed FRA rate)
- $\text{Period}$ = fraction of year (e.g., $\frac{90}{360}$)
- Denominator discounts to the settlement date

---

## 7. Futures

**Interest rate futures price**:

$$f = 100 - \text{yield}$$

**Basis Point Value (BPV)**:

$$\text{BPV} = \text{Notional} \times 0.01\% \times \text{Period}$$

$$= \text{Notional} \times 0.0001 \times \frac{\text{Days}}{360}$$

**Daily MTM gain/loss**:

$$\text{Daily P\&L} = (\text{Settlement Price}_t - \text{Settlement Price}_{t-1}) \times \text{Multiplier} \times \text{Contracts}$$

---

## 8. Interest Rate Swap

**Net settlement per period** (from fixed-rate payer's perspective):

$$\text{Settlement}_n = (\text{MRR}_n - F) \times \text{Notional} \times \text{Period}$$

where:
- $\text{MRR}_n$ = floating rate set at the *beginning* of period $n$
- $F$ = fixed swap rate (par swap rate)

**Par swap rate** (from spot rates):

$$F = \frac{1 - \frac{1}{(1 + z_N)^N}}{\sum_{i=1}^{N} \frac{\text{Period}}{(1 + z_i)^i}}$$

where $z_i$ = spot (zero) rate for period $i$.

---

## 9. Option Bounds

### Lower Bounds (European, no dividends)

**Call**:

$$c_0 \geq \max\!\left(0,\; S_0 - \frac{X}{(1+r)^T}\right)$$

**Put**:

$$p_0 \geq \max\!\left(0,\; \frac{X}{(1+r)^T} - S_0\right)$$

### Upper Bounds

| | European | American |
|---|---|---|
| **Call** | $c_0 \leq S_0$ | $C_0 \leq S_0$ |
| **Put** | $p_0 \leq \frac{X}{(1+r)^T}$ | $P_0 \leq X$ |

---

## 10. Put-Call Parity

**Standard (spot underlying)**:

$$\boxed{S_0 + p_0 = c_0 + \frac{X}{(1+r)^T}}$$

**Put-call forward parity**:

$$\boxed{\frac{F_0(T)}{(1+r)^T} + p_0 = c_0 + \frac{X}{(1+r)^T}}$$

Rearranged:

$$p_0 - c_0 = \frac{X - F_0(T)}{(1+r)^T}$$

### Synthetic Positions

| Synthetic | Composition |
|---|---|
| Call | $c_0 = S_0 + p_0 - \frac{X}{(1+r)^T}$ |
| Put | $p_0 = c_0 - S_0 + \frac{X}{(1+r)^T}$ |
| Stock | $S_0 = c_0 - p_0 + \frac{X}{(1+r)^T}$ |
| Bond | $\frac{X}{(1+r)^T} = S_0 + p_0 - c_0$ |

---

## 11. Binomial Option Pricing (One-Period)

**Up and down prices**:

$$S^+ = S_0 \times u, \quad S^- = S_0 \times d$$

**Option payoffs**:

$$c^+ = \max(0,\; S^+ - X), \quad c^- = \max(0,\; S^- - X)$$

**Hedge ratio (delta)**:

$$h = \frac{c^+ - c^-}{S^+ - S^-}$$

**Risk-neutral probability**:

$$\pi = \frac{(1 + r) - d}{u - d}$$

**Option price (risk-neutral pricing)**:

$$\boxed{c_0 = \frac{\pi \cdot c^+ + (1 - \pi) \cdot c^-}{1 + r}}$$

For puts, replace $c^+, c^-$ with $p^+ = \max(0, X - S^+)$ and $p^- = \max(0, X - S^-)$.

---

## See Also

- [[derivatives/concepts/forward-commitments|Forward Commitments]]
- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/concepts/arbitrage-and-replication|Arbitrage and Replication]]
- [[derivatives/concepts/option-valuation|Option Valuation]]
- [[derivatives/concepts/put-call-parity|Put-Call Parity]]
