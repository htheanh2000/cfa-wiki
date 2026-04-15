---
title: "Glossary — PM M02: Portfolio Risk and Return (Part 2)"
type: glossary
subject: portfolio-management
module: "M02"
created: 2026-04-12
updated: 2026-04-12
tags: [glossary, CAPM, SML, CML, beta, Sharpe, Treynor, Jensen]
---

# Glossary — PM M02: Portfolio Risk and Return (Part 2)

| Term | Definition |
|---|---|
| **Capital Market Line (CML)** | The CAL formed using the market portfolio as the risky asset: $E(R_p) = R_f + \frac{E(R_m)-R_f}{\sigma_m}\sigma_p$. Only efficient portfolios lie on the CML. |
| **Market portfolio** | The theoretical portfolio containing all risky assets weighted by their market capitalizations. Lies at the tangency of the CML and the efficient frontier. |
| **Systematic risk** | Risk due to economy-wide factors that cannot be diversified away. Measured by beta ($\beta$). Also called market risk or non-diversifiable risk. |
| **Nonsystematic risk** | Firm-specific risk that can be eliminated through diversification. Also called idiosyncratic, unique, or diversifiable risk. |
| **Beta ($\beta$)** | A measure of an asset's systematic risk: $\beta_i = \text{Cov}(R_i,R_m)/\sigma_m^2$. A beta of 1 implies the same systematic risk as the market. |
| **Capital Asset Pricing Model (CAPM)** | An equilibrium model: $E(R_i) = R_f + \beta_i[E(R_m)-R_f]$. Only systematic risk is rewarded; unsystematic risk earns no premium. |
| **Security Market Line (SML)** | The graphical depiction of the CAPM, plotting $E(R)$ against $\beta$. All correctly priced assets and portfolios lie on the SML. |
| **Market model** | A regression model: $R_i = \alpha_i + \beta_i R_m + e_i$. An empirical (not equilibrium) tool to estimate beta and alpha. |
| **Market risk premium** | The expected excess return of the market over the risk-free rate: $E(R_m) - R_f$. The slope of the SML. |
| **Security characteristic line** | The regression line of an asset's excess returns against the market's excess returns. Its slope is beta; its intercept is alpha. |
| **Sharpe ratio** | Risk-adjusted return using total risk: $(R_p - R_f)/\sigma_p$. Higher values indicate better risk-adjusted performance. |
| **Treynor ratio** | Risk-adjusted return using systematic risk: $(R_p - R_f)/\beta_p$. Appropriate when the portfolio is part of a larger diversified holding. |
| **$M^2$ (M-squared)** | Performance measure that leverages/de-leverages a portfolio to match market risk, then compares returns: $M^2 = (R_p-R_f)(\sigma_m/\sigma_p) - (R_m-R_f)$. Expressed in percentage units. |
| **Jensen's alpha** | The portion of return not explained by CAPM: $\alpha_p = R_p - [R_f + \beta_p(R_m - R_f)]$. Positive alpha indicates outperformance. |
| **Homogeneity of expectations** | CAPM assumption that all investors agree on expected returns, variances, and covariances for all assets. |
| **Lending portfolio** | A portfolio on the CML between $R_f$ and the market portfolio; investor lends at the risk-free rate (allocates some wealth to the risk-free asset). |
| **Borrowing portfolio** | A portfolio on the CML beyond the market portfolio; investor borrows at the risk-free rate to invest more than 100% in the market portfolio. |
| **Fama-French three-factor model** | Multi-factor model adding size (SMB) and value (HML) factors to the market factor: $E(R_i)-R_f = \beta_{\text{mkt}}(R_m-R_f) + \beta_{\text{SMB}}\cdot\text{SMB} + \beta_{\text{HML}}\cdot\text{HML}$. |

## See Also

- [[portfolio-management/concepts/capm-and-sml|CAPM and SML]]
- [[portfolio-management/concepts/performance-measurement|Performance Measurement]]
