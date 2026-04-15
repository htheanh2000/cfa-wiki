---
title: "Glossary: M05 — Portfolio Mathematics and Probability Distributions"
type: glossary
subject: quantitative-methods
module: M05
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, portfolio, distributions, normal, binomial, safety-first]
---

# Glossary: M05 — Portfolio Mathematics and Probability Distributions

**Module**: [[quantitative-methods/modules/m05-portfolio-math/index|M05]]
**Formulas**: [[quantitative-methods/formulas/portfolio-math|Formula Sheet]]
**Concept pages**: [[quantitative-methods/concepts/portfolio-risk|Portfolio Risk]], [[quantitative-methods/concepts/normal-distribution|Normal Distribution]]

---

## Portfolio Expected Return

The weighted average of expected returns of the assets in the portfolio, where weights are portfolio allocation proportions.

$$E(R_p) = \sum_{i=1}^{n} w_i E(R_i)$$

**LOS**: 5.a | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Weighted Mean|Weighted Mean]]

---

## Covariance (Portfolio)

The expected value of the product of deviations of two asset returns from their respective expected values. Measures how two asset returns move together.

$$\text{Cov}(R_i, R_j) = E\left[(R_i - E(R_i))(R_j - E(R_j))\right]$$

**LOS**: 5.a | **Key**: Negative covariance provides diversification benefits. | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Covariance|Covariance]]

---

## Covariance Matrix

A square matrix displaying the covariances between all pairs of assets in a portfolio. Diagonal elements are variances; off-diagonal elements are covariances.

$$\Sigma = \begin{pmatrix} \sigma_1^2 & \text{Cov}_{12} & \cdots \\ \text{Cov}_{21} & \sigma_2^2 & \cdots \\ \vdots & \vdots & \ddots \end{pmatrix}$$

**LOS**: 5.a | **Note**: A portfolio of $n$ assets has $n$ variances and $\frac{n(n-1)}{2}$ unique covariances.

---

## Correlation (Portfolio)

The standardized covariance between two asset returns, ranging from −1 to +1.

$$\rho_{ij} = \frac{\text{Cov}(R_i, R_j)}{\sigma_i \sigma_j}$$

**LOS**: 5.a | **Key**: Diversification reduces risk most when correlation is low (ideally negative). | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Correlation|Correlation]]

---

## Correlation Matrix

A square matrix displaying correlations between all pairs of assets. Diagonal elements equal 1; off-diagonal elements are correlations $\rho_{ij}$.

**LOS**: 5.a | **Related**: [[#Covariance Matrix]]

---

## Portfolio Variance

The weighted sum of covariances among all pairs of assets in the portfolio. For a two-asset portfolio:

$$\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2 w_1 w_2 \text{Cov}(R_1, R_2)$$

General: $\sigma_p^2 = \sum_i \sum_j w_i w_j \text{Cov}(R_i, R_j)$

**LOS**: 5.a | **Key**: Portfolio variance depends on ALL pairwise covariances, not just individual asset variances.

---

## Portfolio Standard Deviation

The positive square root of [[#Portfolio Variance]]. Represents the total risk of the portfolio.

$$\sigma_p = \sqrt{\sigma_p^2}$$

**LOS**: 5.a | **Related**: [[quantitative-methods/concepts/portfolio-risk|Portfolio Risk Concept]]

---

## Diversification Benefit

The reduction in portfolio risk (variance/standard deviation) achieved by combining assets whose returns are not perfectly positively correlated. Diversification eliminates unsystematic (firm-specific) risk.

**LOS**: 5.a | **Key**: Maximum diversification benefit when $\rho = -1$. No benefit when $\rho = +1$. | **Related**: [[quantitative-methods/concepts/portfolio-risk|Portfolio Risk]]

---

## Probability Distribution

A function that assigns probabilities to all possible values of a random variable. Must satisfy: $P(X = x) \geq 0$ for all $x$ and the sum (or integral) of all probabilities equals 1.

**LOS**: 5.b | **Types**: [[#Discrete Random Variable|Discrete]] distributions, [[#Continuous Random Variable|Continuous]] distributions.

---

## Probability Function

For a discrete random variable, the function $p(x) = P(X = x)$ that gives the probability of each specific value. Also called the probability mass function (PMF).

**LOS**: 5.b | **Contrast**: For continuous random variables, a probability density function (PDF) is used.

---

## Cumulative Distribution Function (CDF)

The function $F(x) = P(X \leq x)$ giving the probability that a random variable takes a value less than or equal to $x$. Ranges from 0 to 1 and is non-decreasing.

**LOS**: 5.b | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Cumulative Frequency|Cumulative Frequency]]

---

## Discrete Random Variable

A random variable that can take on only a countable number of distinct values (e.g., integers). Described by a probability mass function.

**LOS**: 5.b | **Examples**: Number of defaults in a portfolio; outcome of rolling a die. | **Related**: [[#Binomial Distribution]], [[#Discrete Uniform Distribution]]

---

## Continuous Random Variable

A random variable that can take on any value in an interval. Described by a probability density function. The probability of any single point equals zero.

**LOS**: 5.b | **Examples**: Stock returns, interest rates. | **Related**: [[#Normal Distribution]], [[#Continuous Uniform Distribution]]

---

## Discrete Uniform Distribution

A distribution where each of $n$ possible outcomes is equally likely. The simplest discrete distribution.

$$P(X = x_i) = \frac{1}{n} \quad \text{for each } i = 1, 2, \ldots, n$$

**LOS**: 5.c | **Example**: Rolling a fair die — each face has probability 1/6.

---

## Continuous Uniform Distribution

A distribution where the random variable is equally likely to take any value between a lower bound $a$ and upper bound $b$.

$$f(x) = \frac{1}{b-a} \quad \text{for } a \leq x \leq b$$

$$P(x_1 \leq X \leq x_2) = \frac{x_2 - x_1}{b - a}$$

**LOS**: 5.c

---

## Bernoulli Distribution

A distribution for a single trial with two possible outcomes: success (probability $p$) or failure (probability $1-p$).

$$E(X) = p \qquad \text{Var}(X) = p(1-p)$$

**LOS**: 5.d | **Related**: [[#Binomial Distribution]] (sum of independent Bernoulli trials)

---

## Binomial Distribution

The probability distribution of the number of successes in $n$ independent Bernoulli trials, each with probability of success $p$.

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$

$$E(X) = np \qquad \text{Var}(X) = np(1-p)$$

**LOS**: 5.d | **Application**: Probability of $k$ stocks rising out of $n$ stocks in a portfolio. | **Related**: [[quantitative-methods/glossary/m04-probability#Combination|Combination]]

---

## Normal Distribution

A symmetric, bell-shaped continuous probability distribution completely described by its mean $\mu$ and variance $\sigma^2$. The most important distribution in statistics.

$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$$

**LOS**: 5.e | **Key properties**: Symmetric; mean = median = mode; 68%/95%/99% rule. | **See**: [[quantitative-methods/concepts/normal-distribution|Normal Distribution Concept]]

---

## Standard Normal Distribution

A normal distribution with mean $\mu = 0$ and variance $\sigma^2 = 1$. Used with $z$-tables to compute probabilities for any normal distribution.

$$Z \sim N(0,1)$$

**LOS**: 5.e | **Related**: [[#Z-Score]], [[quantitative-methods/concepts/normal-distribution|Normal Distribution]]

---

## Z-Score

The number of standard deviations by which an observation differs from the mean. Standardizes a normal random variable to the standard normal.

$$Z = \frac{X - \mu}{\sigma}$$

**LOS**: 5.e | **Use**: Look up $P(Z \leq z)$ in standard normal table. | **Related**: [[#Standard Normal Distribution]]

---

## Shortfall Risk

The probability that a portfolio's return falls below a specified minimum acceptable return (threshold level or target). A downside risk measure.

**LOS**: 5.f | **Related**: [[#Safety-First Ratio]], [[#Roy's Safety-First Criterion]]

---

## Safety-First Ratio

A measure for comparing portfolios on the basis of downside risk. Higher is better.

$$\text{SF Ratio} = \frac{E(R_p) - R_L}{\sigma_p}$$

where $R_L$ = minimum acceptable (threshold) return.

**LOS**: 5.f | **Note**: Structurally similar to the Sharpe ratio, but uses $R_L$ instead of $R_f$. | **Related**: [[#Roy's Safety-First Criterion]]

---

## Roy's Safety-First Criterion

An approach to portfolio selection that chooses the portfolio with the highest safety-first ratio — i.e., the portfolio that minimizes the probability of portfolio return falling below the threshold return $R_L$.

$$\text{Optimal portfolio}: \max\left[\frac{E(R_p) - R_L}{\sigma_p}\right]$$

**LOS**: 5.f | **Related**: [[#Safety-First Ratio]], [[#Shortfall Risk]]
