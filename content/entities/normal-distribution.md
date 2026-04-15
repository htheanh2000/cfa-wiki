---
title: Normal Distribution
type: entity
category: distribution
created: 2026-04-09
updated: 2026-04-09
tags: [distribution, statistics, bell-curve, z-score]
---

# Normal Distribution

**Type**: Continuous probability distribution
**Also called**: Gaussian distribution, bell curve
**Notation**: $X \sim N(\mu, \sigma^2)$

## Key Properties

- Symmetric around mean $\mu$
- Fully described by two parameters: $\mu$ (mean) and $\sigma^2$ (variance)
- Tails extend to $\pm \infty$ but never touch zero
- Mean = Median = Mode

## Confidence Intervals

| Interval | Coverage |
|----------|----------|
| $\mu \pm 1\sigma$ | 68.27% |
| $\mu \pm 1.65\sigma$ | 90% |
| $\mu \pm 1.96\sigma$ | 95% |
| $\mu \pm 2.58\sigma$ | 99% |

## Standard Normal ($Z$)

$$Z = \frac{X - \mu}{\sigma} \sim N(0, 1)$$

## Related Distributions

| Distribution | Relationship |
|---|---|
| **Lognormal** | If $X \sim N$, then $e^X$ is lognormal |
| **t-distribution** | Approaches normal as $df \to \infty$ |
| **Chi-square** | Sum of squared standard normals |
| **F-distribution** | Ratio of two chi-square/df |

## Role in CFA Quant

The normal distribution is the foundation of:
- [[modules/quantitative-methods/m05-portfolio-mathematics/index|M05]] — Portfolio return modeling, Safety-First ratio
- [[modules/quantitative-methods/m06-simulation-methods/index|M06]] — Lognormal asset pricing, Monte Carlo
- [[modules/quantitative-methods/m07-estimation-and-inference/index|M07]] — CLT, confidence intervals
- [[modules/quantitative-methods/m08-hypothesis-testing/index|M08]] — z-test, t-test
- [[modules/quantitative-methods/m10-simple-linear-regression/index|M10]] — Normality assumption of residuals

## Limitation for Finance

- Real asset returns exhibit **fat tails** (leptokurtosis) and **skewness**
- Normal distribution underestimates probability of extreme events
- This is why [[modules/quantitative-methods/m03-statistical-measures/index|M03]] teaches skewness and kurtosis
