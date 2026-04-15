---
title: "Glossary: M06 — Simulation Methods"
type: glossary
subject: quantitative-methods
module: M06
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, simulation, monte-carlo, lognormal, distributions, bootstrap]
---

# Glossary: M06 — Simulation Methods

**Module**: [[quantitative-methods/modules/m06-simulation-methods/index|M06]]
**Formulas**: [[quantitative-methods/formulas/simulation-methods|Formula Sheet]]
**Concept page**: [[quantitative-methods/concepts/simulation-methods|Simulation Methods Concept]]

---

## Lognormal Distribution

A distribution of a variable whose natural logarithm is normally distributed. Used to model asset prices because it is bounded below by zero (prices cannot be negative).

$$\text{If } \ln(X) \sim N(\mu, \sigma^2), \text{ then } X \text{ is lognormally distributed.}$$

$$E(X) = e^{\mu + \sigma^2/2} \qquad \text{Var}(X) = e^{2\mu + \sigma^2}(e^{\sigma^2} - 1)$$

**LOS**: 6.a | **Key**: Lognormal distributions are right-skewed and bounded below at zero — consistent with stock prices. | **Related**: [[#Continuously Compounded Return]]

---

## Continuously Compounded Return

The natural log of the ratio of ending price to beginning price. If asset prices are lognormally distributed, continuously compounded returns are normally distributed.

$$r_{cc} = \ln\left(\frac{S_1}{S_0}\right) = \ln(1 + HPR)$$

**LOS**: 6.a | **Key**: Continuously compounded returns are additive over time; holding period returns are multiplicative. | **Related**: [[quantitative-methods/glossary/m01-rates-and-returns#Continuously Compounded Return|M01 — Continuously Compounded Return]], [[#Lognormal Distribution]]

---

## Student's t-Distribution

A symmetric, bell-shaped distribution with heavier tails than the normal distribution. Used when the population variance is unknown and the sample size is small.

**LOS**: 6.b | **Key properties**: Defined by [[#Degrees of Freedom]]; as degrees of freedom increase, the t-distribution approaches the standard normal. Heavier tails → more probability in extremes.

---

## Degrees of Freedom

The number of independent observations in a sample used to estimate a parameter. For a sample of $n$ observations, df = $n - 1$ when estimating the mean.

**LOS**: 6.b | **Role**: Determines the shape of the [[#Student's t-Distribution]], [[#Chi-Square Distribution]], and [[#F-Distribution]]. More df → closer to normal.

---

## Chi-Square Distribution

A distribution formed by the sum of the squares of $k$ independent standard normal variables. Used for testing [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|independence]] and variance.

$$\chi^2 = \sum_{i=1}^{k} Z_i^2 \quad \text{where } Z_i \sim N(0,1)$$

**LOS**: 6.b | **Properties**: Right-skewed; always non-negative; defined by [[#Degrees of Freedom]] $k$. | **Related**: [[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|Chi-Square Test]]

---

## F-Distribution

The ratio of two independent chi-square distributed variables, each divided by its degrees of freedom. Used to compare variances and in [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|regression ANOVA]].

$$F = \frac{\chi^2_{df_1}/df_1}{\chi^2_{df_2}/df_2}$$

**LOS**: 6.b | **Properties**: Non-negative; right-skewed; defined by two degrees of freedom parameters ($df_1$, $df_2$). | **Related**: [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-Test]]

---

## Monte Carlo Simulation

A method that uses repeated random sampling from specified probability distributions to generate a large number of scenarios and estimate the probability distribution of an outcome variable.

**LOS**: 6.c | **Steps**: (1) Specify distributions for input variables; (2) draw random values; (3) compute outcome; (4) repeat many times; (5) analyze the resulting distribution. | **Application**: Estimating [[#Value at Risk (VaR)]], option pricing, pension fund risk modeling.

---

## Value at Risk (VaR)

The minimum loss expected to be exceeded with probability $\alpha$ over a specified time horizon, at a given confidence level.

$$P(\text{Loss} > VaR) = \alpha$$

**LOS**: 6.c | **Example**: A daily VaR of \$1M at 5% means there is a 5% chance of losing more than \$1M in a day. | **Key limitation**: Does not describe the magnitude of losses exceeding VaR.

---

## Resampling

A class of statistical methods that repeatedly draw samples from observed data to make inferences about a population. Includes [[#Bootstrap]] and [[#Jackknife]].

**LOS**: 6.d | **Advantage**: Makes no assumptions about the underlying population distribution. | **Related**: [[quantitative-methods/concepts/simulation-methods|Simulation Methods Concept]]

---

## Bootstrap

A resampling method in which samples are drawn **with replacement** from the original observed data set. Used to estimate the sampling distribution of a statistic.

**LOS**: 6.d | **Process**: (1) Draw $B$ bootstrap samples of size $n$ (with replacement); (2) calculate the statistic for each; (3) use the empirical distribution of the $B$ statistics for inference. | **Contrast**: [[#Jackknife]]

---

## Jackknife

A resampling method in which each observation is systematically removed one at a time, and the statistic is recomputed on the remaining $n-1$ observations. Used to estimate bias and variance of estimators.

**LOS**: 6.d | **Key**: More structured than [[#Bootstrap]] (deterministic, not random). Less computationally flexible but useful for bias estimation.
