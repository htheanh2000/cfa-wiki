---
title: "Formulas: Portfolio Mathematics"
type: formula
subject: quantitative-methods
module: M05
created: 2026-04-09
updated: 2026-04-09
tags: [formulas, portfolio, variance, covariance, correlation, normal-distribution, z-score]
---

# Formulas: Portfolio Mathematics

**Module**: [[quantitative-methods/modules/m05-portfolio-mathematics/index|M05]]

## Portfolio Expected Return

$$E(R_p) = \sum_{i=1}^{n} w_i \cdot E(R_i)$$

## Covariance

$$Cov(R_i, R_j) = E\left[(R_i - ER_i)(R_j - ER_j)\right]$$

From joint probability model:
$$Cov(R_A, R_B) = \sum_i \sum_j P(R_{A,i}, R_{B,j})(R_{A,i} - ER_A)(R_{B,j} - ER_B)$$

## Correlation

$$\rho(R_i, R_j) = \frac{Cov(R_i, R_j)}{\sigma_i \cdot \sigma_j}$$

Also: $Cov(R_i, R_j) = \rho_{ij} \cdot \sigma_i \cdot \sigma_j$

## Portfolio Variance (2-asset)

$$\sigma_p^2 = w_A^2\sigma_A^2 + w_B^2\sigma_B^2 + 2w_Aw_B \cdot Cov(R_A, R_B)$$

$$= w_A^2\sigma_A^2 + w_B^2\sigma_B^2 + 2w_Aw_B \cdot \rho_{AB} \cdot \sigma_A \cdot \sigma_B$$

## Portfolio Variance (N-asset)

$$\sigma_p^2 = \sum_{i=1}^{N}\sum_{j=1}^{N} w_i w_j \cdot Cov(R_i, R_j)$$

## Normal Distribution — Confidence Intervals

| Interval | Probability |
|----------|-------------|
| $\mu \pm 1\sigma$ | 68.27% |
| $\mu \pm 1.65\sigma$ | 90% |
| $\mu \pm 1.96\sigma$ | 95% |
| $\mu \pm 2.58\sigma$ | 99% |

## Z-Score (Standardization)

$$Z = \frac{X - \mu}{\sigma}$$

## Roy's Safety-First Ratio

$$SFRatio = \frac{E(R_p) - R_L}{\sigma_p}$$

where $R_L$ = minimum acceptable return (threshold)

**Choose portfolio with highest SFRatio.**

## Shortfall Probability

$$P(R_p < R_L) = N(-SFRatio)$$

where $N(\cdot)$ is the standard normal CDF
