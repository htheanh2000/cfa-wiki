---
title: "Glossary: FI Module 11 — Duration Measures"
type: glossary
subject: fixed-income
module: M11
created: 2026-04-12
updated: 2026-04-12
tags: [glossary, modified-duration, money-duration, PVBP, approximate-duration]
---

# Glossary: FI Module 11 — Duration Measures

| Term | Definition |
|------|-----------|
| **Modified duration** | Macaulay duration divided by $(1 + r)$; measures % price change per unit yield change |
| **Approximate modified duration** | Numerical estimate: $(PV_{-} - PV_{+}) / (2 \times PV_0 \times \Delta y)$ |
| **Annual modified duration** | Modified duration expressed on an annual basis (periodic ModDur / periods per year already embedded) |
| **Money duration (dollar duration)** | Modified duration × full price; gives the absolute dollar price change for a yield change |
| **PVBP (price value of a basis point)** | The dollar change in bond price for a 1 bp change in yield: $(PV_{-} - PV_{+}) / 2$ |
| **DV01 (dollar value of 01)** | Synonymous with PVBP; the dollar price change for a 1 basis point yield change |
| **Perpetuity duration** | Duration of a perpetuity: $\text{MacDur} = (1 + r) / r$; $\text{ModDur} = 1/r$ |
| **Duration of a zero-coupon bond** | Macaulay duration = maturity; modified duration = maturity / $(1 + r)$ |
| **Percentage price change** | $\%\Delta PV \approx -\text{ModDur} \times \Delta y$ (first-order approximation) |
| **Basis point (bp)** | One hundredth of a percentage point: 1 bp = 0.01% = 0.0001 |
| **Yield beta** | The sensitivity of a bond's yield to a change in the benchmark yield |
| **Duration contribution** | The weighted duration that each bond contributes to the portfolio: $w_i \times D_i$ |

See also: [[fixed-income/concepts/duration|Duration]]
