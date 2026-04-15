---
title: Alternative Investments — Master Formula Sheet
type: formula
subject: alternative-investments
created: 2026-04-12
updated: 2026-04-12
tags: [formulas, MOIC, IRR, fees, cap-rate, commodity-futures, performance]
---

# Alternative Investments — Master Formula Sheet

## 1. Multiple on Invested Capital (MOIC)

$$\text{MOIC} = \frac{\text{Realized Value} + \text{Unrealized Value}}{\text{Total Amount Invested}}$$

where:
- **Realized value** = cash distributions received from exited investments
- **Unrealized value** = estimated fair value of remaining portfolio
- **Total amount invested** = total capital deployed (not committed)

> MOIC does not account for the time value of money.

## 2. Internal Rate of Return (IRR)

$$\sum_{t=0}^{T} \frac{CF_t}{(1 + IRR)^t} = 0$$

where:
- $CF_t$ = cash flow at time $t$ (negative for capital calls, positive for distributions)
- $T$ = total number of periods
- $IRR$ = the rate that makes NPV of all cash flows equal to zero

> IRR accounts for both the magnitude and timing of cash flows.

## 3. Management Fee

$$\text{Management Fee} = \text{Fee Rate} \times \text{AUM (or Committed Capital)}$$

where:
- **Fee rate** = annual percentage, typically 1.5%--2.0%
- **AUM** = assets under management (or committed capital during investment period)

**During investment period**: Fee base is often **committed capital**
**After investment period**: Fee base is often **invested capital** or **NAV**

## 4. Performance Fee — Hard Hurdle

$$\text{Performance Fee} = \text{Fee Rate} \times (\text{Return} - \text{Hurdle Rate}) \times \text{Capital}$$

where:
- **Fee rate** = performance fee percentage (typically 20%)
- **Return** = actual fund return
- **Hurdle rate** = minimum return threshold (typically 6%--8%)
- Only applied when $\text{Return} > \text{Hurdle Rate}$
- GP earns fee only on the **excess** return above the hurdle

## 5. Performance Fee — Soft Hurdle

$$\text{Performance Fee} = \text{Fee Rate} \times \text{Total Return} \times \text{Capital}$$

where:
- **Fee rate** = performance fee percentage (typically 20%)
- **Total return** = full return of the fund
- Only applied when $\text{Return} > \text{Hurdle Rate}$
- If hurdle is met, GP earns fee on the **entire** return (not just excess)

## 6. Net Return

$$\text{Net Return} = \text{Gross Return} - \text{Management Fee} - \text{Performance Fee}$$

where:
- **Gross return** = total return on investments before fees
- **Net return** = return actually received by LPs

## 7. Commodity Futures Pricing

$$F_0 \approx S_0 \times (1 + r)^T + \text{Storage Costs} - \text{Convenience Yield}$$

where:
- $F_0$ = futures price at time 0
- $S_0$ = spot price at time 0
- $r$ = risk-free rate
- $T$ = time to expiration (in years)
- **Storage costs** = cost of physically storing the commodity
- **Convenience yield** = benefit from holding the physical commodity (e.g., avoiding supply disruptions)

## 8. Contango and Backwardation

| Condition | Relationship | Implication |
|---|---|---|
| **Contango** | $F_0 > S_0$ | Storage costs exceed convenience yield; negative roll yield |
| **Backwardation** | $F_0 < S_0$ | Convenience yield exceeds storage costs; positive roll yield |

- **Roll yield** in contango: **negative** (selling low, buying high when rolling contracts)
- **Roll yield** in backwardation: **positive** (selling high, buying low when rolling contracts)

## 9. Capitalization Rate (Real Estate)

$$\text{Cap Rate} = \frac{\text{NOI}}{\text{Property Value}}$$

where:
- **NOI** = Net Operating Income = Rental income $-$ Operating expenses (excluding financing costs and depreciation)
- **Property value** = current market value or purchase price

Rearranged to find value:

$$\text{Property Value} = \frac{\text{NOI}}{\text{Cap Rate}}$$

> A lower cap rate implies higher property value (and vice versa). Cap rate is analogous to an earnings yield for real estate.

## Related Pages

- [[alternative-investments/concepts/ai-performance-measurement|Performance Measurement]]
- [[alternative-investments/concepts/real-assets|Real Assets]]
- [[alternative-investments/concepts/private-capital|Private Capital]]
- [[alternative-investments/concepts/alternative-investment-overview|Alternative Investment Overview]]
