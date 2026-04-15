---
title: Portfolio Management — Master Formula Sheet
type: formula
subject: portfolio-management
created: 2026-04-12
updated: 2026-04-12
tags: [formulas, CAPM, Sharpe, Treynor, Jensen, CML, CAL, portfolio-variance]
---

# Portfolio Management — Master Formula Sheet

## 1. Expected Return (Building Blocks)

$$1 + E(R) = (1 + r_{rf})(1 + E(\pi))(1 + E(RP))$$

where:
- $r_{rf}$ = real risk-free rate
- $E(\pi)$ = expected inflation premium
- $E(RP)$ = expected risk premium

## 2. Real Return

$$R_{\text{real}} = \frac{1 + R_{\text{nominal}}}{1 + \pi} - 1$$

## 3. Utility Function

$$U = E(R) - \frac{1}{2} A \sigma^2$$

where $A$ = risk aversion coefficient ($A > 0$ for risk-averse investors).

## 4. Capital Allocation Line (CAL)

$$E(R_p) = R_f + \left[\frac{E(R_i) - R_f}{\sigma_i}\right] \sigma_p$$

where the slope $\frac{E(R_i) - R_f}{\sigma_i}$ is the Sharpe ratio of the risky portfolio.

## 5. Capital Market Line (CML)

$$E(R_p) = R_f + \left[\frac{E(R_m) - R_f}{\sigma_m}\right] \sigma_p$$

Applies only to **efficient portfolios** (combinations of the risk-free asset and the market portfolio).

## 6. Portfolio Variance (Two Assets)

$$\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2 w_1 w_2 \rho_{12} \sigma_1 \sigma_2$$

Equivalently: $\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2 w_1 w_2 \text{Cov}_{12}$

## 7. Covariance

$$\text{Cov}_{12} = \frac{\sum_{t=1}^{n}(R_{1t} - \bar{R}_1)(R_{2t} - \bar{R}_2)}{n - 1}$$

## 8. Correlation

$$\rho_{12} = \frac{\text{Cov}_{12}}{\sigma_1 \sigma_2}$$

where $-1 \le \rho_{12} \le +1$.

## 9. Beta

$$\beta_i = \frac{\text{Cov}(R_i, R_m)}{\sigma_m^2} = \rho_{im} \times \frac{\sigma_i}{\sigma_m}$$

## 10. CAPM

$$E(R_i) = R_f + \beta_i [E(R_m) - R_f]$$

where $E(R_m) - R_f$ = market risk premium.

## 11. Market Model

$$R_i = \alpha_i + \beta_i R_m + e_i$$

where:
- $\alpha_i$ = abnormal return (intercept)
- $e_i$ = firm-specific error term

## 12. Portfolio Beta

$$\beta_p = \sum_{i=1}^{n} w_i \times \beta_i$$

## 13. Sharpe Ratio

$$\text{Sharpe} = \frac{R_p - R_f}{\sigma_p}$$

Uses **total risk**. Appropriate for evaluating the investor's **entire** portfolio.

## 14. Treynor Ratio

$$\text{Treynor} = \frac{R_p - R_f}{\beta_p}$$

Uses **systematic risk**. Appropriate for evaluating a **sub-portfolio**.

## 15. M-Squared ($M^2$)

$$M^2 = (R_p - R_f) \frac{\sigma_m}{\sigma_p} - (R_m - R_f)$$

Equivalently:

$$M^2 = (\text{Sharpe}_p - \text{Sharpe}_m) \times \sigma_m$$

Returns a **percentage** — the excess return of a leveraged/de-leveraged portfolio matched to market risk.

## 16. Jensen's Alpha

$$\alpha_p = R_p - [R_f + \beta_p (R_m - R_f)]$$

Positive $\alpha$ indicates the manager outperformed the CAPM prediction.

## 17. Diversification Ratio

$$\text{Diversification ratio} = \frac{\sigma(\text{equally-weighted portfolio})}{\sigma(\text{randomly selected security})}$$

A ratio closer to zero indicates greater diversification benefit.

## See Also

- [[portfolio-management/concepts/portfolio-risk-return|Portfolio Risk and Return]]
- [[portfolio-management/concepts/capm-and-sml|CAPM and SML]]
- [[portfolio-management/concepts/performance-measurement|Performance Measurement]]
