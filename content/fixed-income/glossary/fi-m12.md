---
title: "Glossary: FI Module 12 — Convexity and Portfolio Duration"
type: glossary
subject: fixed-income
module: M12
created: 2026-04-12
updated: 2026-04-12
tags: [glossary, convexity, money-convexity, effective-convexity, portfolio-duration]
---

# Glossary: FI Module 12 — Convexity and Portfolio Duration

| Term | Definition |
|------|-----------|
| **Convexity** | A measure of the curvature of the price-yield relationship; second-order sensitivity to yield changes |
| **Approximate convexity** | Numerical estimate: $(PV_{-} + PV_{+} - 2 \times PV_0) / (\Delta y^2 \times PV_0)$ |
| **Money convexity** | Convexity × full price; used for dollar-based convexity adjustments |
| **Effective convexity** | Convexity measure using benchmark curve shifts; appropriate for bonds with embedded options |
| **Positive convexity** | The property of option-free bonds where price gains from yield decreases exceed losses from yield increases |
| **Negative convexity** | A region where the price-yield curve is concave; callable bonds exhibit this when yields are low |
| **Convexity adjustment** | The second-order correction to the duration estimate: $\frac{1}{2} \times \text{Con} \times \Delta y^2$ |
| **Portfolio duration** | The weighted average of individual bond durations: $D_p = \sum w_i D_i$ |
| **Portfolio convexity** | The weighted average of individual bond convexities: $C_p = \sum w_i C_i$ |
| **Parallel shift** | A uniform change in yields across all maturities; the assumption underlying portfolio duration |
| **Cash flow yield** | The IRR of a bond portfolio's aggregate cash flows |
| **Dispersion** | The variance of cash flow timing around the Macaulay duration; related to convexity |

See also: [[fixed-income/concepts/convexity|Convexity]], [[fixed-income/concepts/duration|Duration]]
