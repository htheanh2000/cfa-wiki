---
title: "Glossary: M08 — Hypothesis Testing"
type: glossary
subject: quantitative-methods
module: M08
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, hypothesis-testing, type-i-error, type-ii-error, p-value]
---

# Glossary: M08 — Hypothesis Testing

**Module**: [[quantitative-methods/modules/m08-hypothesis-testing/index|M08]]
**Formulas**: [[quantitative-methods/formulas/hypothesis-testing|Formula Sheet]]
**Concept page**: [[quantitative-methods/concepts/hypothesis-testing|Hypothesis Testing Concept]]

---

## Hypothesis Testing

A formal statistical procedure for evaluating a claim (hypothesis) about a population parameter using sample data. Involves specifying null and alternative hypotheses, computing a test statistic, and making a decision.

**LOS**: 8.a | **See**: [[quantitative-methods/concepts/hypothesis-testing|6-Step Process]] | **Related**: [[quantitative-methods/glossary/m07-estimation-and-inference#Confidence Interval|Confidence Interval]]

---

## Null Hypothesis

The hypothesis to be tested. Denoted $H_0$. Typically states that a parameter equals a specific value, or that there is no effect. The null hypothesis is assumed true unless evidence strongly contradicts it.

**LOS**: 8.a | **Key**: We never "prove" the null; we either reject it or fail to reject it.

---

## Alternative Hypothesis

The hypothesis that is accepted if the null hypothesis is rejected. Denoted $H_a$ or $H_1$. Represents what the analyst is trying to find evidence for.

**LOS**: 8.a | **Related**: [[#Two-Tailed Test]], [[#One-Tailed Test]]

---

## Two-Tailed Test

A test where the alternative hypothesis specifies that the parameter is different from (≠) the null value, in either direction. The rejection region is split between both tails.

$$H_0: \mu = \mu_0 \qquad H_a: \mu \neq \mu_0$$

**LOS**: 8.b | **Use**: When the analyst has no prior directional belief.

---

## One-Tailed Test

A test where the alternative hypothesis specifies a direction — either greater than or less than the null value. The rejection region is entirely in one tail.

**LOS**: 8.b | **See**: [[#Right-Tail Test]], [[#Left-Tail Test]]

---

## Right-Tail Test

A one-tailed test where the alternative hypothesis specifies that the parameter is greater than the null value.

$$H_0: \mu \leq \mu_0 \qquad H_a: \mu > \mu_0$$

**LOS**: 8.b | **Rejection**: Reject $H_0$ when test statistic exceeds the upper critical value.

---

## Left-Tail Test

A one-tailed test where the alternative hypothesis specifies that the parameter is less than the null value.

$$H_0: \mu \geq \mu_0 \qquad H_a: \mu < \mu_0$$

**LOS**: 8.b | **Rejection**: Reject $H_0$ when test statistic is less than the lower critical value.

---

## Test Statistic

A standardized value computed from sample data used to evaluate the null hypothesis. Measures how far the sample estimate is from the hypothesized value in standard error units.

$$\text{Test statistic} = \frac{\text{Sample statistic} - \text{Hypothesized value}}{\text{Standard error of statistic}}$$

**LOS**: 8.c | **Examples**: [[#z-Test]], [[#t-Test]], [[#Chi-Square Test]], [[#F-Test]]

---

## Critical Value

The boundary value of the test statistic that separates the rejection region from the non-rejection region. Determined by the chosen [[#Level of Significance]] and the distribution of the test statistic.

**LOS**: 8.c | **Related**: [[#Rejection Region]], [[quantitative-methods/glossary/m07-estimation-and-inference#Reliability Factor|Reliability Factor]]

---

## Rejection Region

The set of test statistic values for which the null hypothesis is rejected. Also called the critical region.

**LOS**: 8.c | **Rule**: Reject $H_0$ if the test statistic falls in the rejection region (i.e., $|t| > t_{\text{critical}}$ for a two-tailed test).

---

## Level of Significance

The probability of rejecting a true null hypothesis ([[#Type I Error]]). Denoted $\alpha$. Chosen before conducting the test.

**LOS**: 8.d | **Common levels**: 1%, 5%, 10%. | **Related**: [[#Power of a Test]], [[quantitative-methods/glossary/m07-estimation-and-inference#Level of Significance|Estimation context]]

---

## Type I Error

Rejecting a true null hypothesis. The probability of a Type I error equals $\alpha$, the level of significance. Also called a "false positive."

$$P(\text{Type I Error}) = \alpha$$

**LOS**: 8.d | **Trade-off**: Reducing $\alpha$ reduces Type I errors but increases [[#Type II Error]] probability.

---

## Type II Error

Failing to reject a false null hypothesis. Also called a "false negative." The probability of a Type II error is denoted $\beta$.

$$P(\text{Type II Error}) = \beta$$

**LOS**: 8.d | **Related**: [[#Power of a Test]] = $1 - \beta$

---

## Power of a Test

The probability of correctly rejecting a false null hypothesis.

$$\text{Power} = 1 - \beta = 1 - P(\text{Type II Error})$$

**LOS**: 8.d | **Key**: Higher power is better. Power increases with sample size, larger effect size, and higher $\alpha$.

---

## p-Value

The smallest level of significance at which the null hypothesis can be rejected, given the observed test statistic. Equivalently, the probability of obtaining a test statistic at least as extreme as the observed value, assuming $H_0$ is true.

**LOS**: 8.e | **Decision rule**: Reject $H_0$ if $p$-value $< \alpha$. | **Key**: A smaller $p$-value provides stronger evidence against $H_0$.

---

## Statistical Significance

A result is statistically significant if the probability of observing it by chance (when $H_0$ is true) is less than $\alpha$. Formally: the null hypothesis is rejected.

**LOS**: 8.f | **Key warning**: Statistical significance does not imply [[#Economically Significant|economic significance]].

---

## Economically Significant

A result is economically significant if the magnitude of the effect is large enough to be practically meaningful in a financial context — particularly after accounting for transaction costs and risk.

**LOS**: 8.f | **Key**: A statistically significant result (e.g., 0.01% excess return) may be economically trivial.

---

## z-Test

A hypothesis test using the standard normal distribution. Used when the population variance is known, or when the sample size is large (typically $n \geq 30$) so the CLT applies.

$$z = \frac{\bar{X} - \mu_0}{\sigma / \sqrt{n}}$$

**LOS**: 8.g | **Related**: [[quantitative-methods/glossary/m05-portfolio-math#Standard Normal Distribution|Standard Normal Distribution]]

---

## t-Test

A hypothesis test using the t-distribution. Used when the population variance is unknown and the sample size is small. Applied to tests of means, regression coefficients, and correlations.

$$t = \frac{\bar{X} - \mu_0}{s / \sqrt{n}} \qquad df = n - 1$$

**LOS**: 8.g | **Related**: [[quantitative-methods/glossary/m06-simulation-methods#Student's t-Distribution|Student's t-Distribution]], [[quantitative-methods/glossary/m10-simple-linear-regression#t-Test for Slope|Regression t-Test]]

---

## Chi-Square Test

A hypothesis test using the chi-square distribution. Used to test hypotheses about a population variance or to test independence of categorical variables.

For variance: $\chi^2 = \frac{(n-1)s^2}{\sigma_0^2} \qquad df = n-1$

**LOS**: 8.h | **Related**: [[quantitative-methods/glossary/m06-simulation-methods#Chi-Square Distribution|Chi-Square Distribution]], [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|Chi-Square Test of Independence]]

---

## F-Test

A hypothesis test using the F-distribution. Used to test equality of two population variances, or the overall significance of a regression model.

$$F = \frac{s_1^2}{s_2^2} \qquad df_1 = n_1 - 1, \quad df_2 = n_2 - 1$$

**LOS**: 8.h | **Related**: [[quantitative-methods/glossary/m06-simulation-methods#F-Distribution|F-Distribution]], [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|Regression F-Statistic]]

---

## Pooled Estimator

A combined estimate of a parameter (typically variance) from two or more samples, used when the parameter is assumed equal across groups. Applied in the pooled two-sample t-test.

$$s_p^2 = \frac{(n_1-1)s_1^2 + (n_2-1)s_2^2}{n_1 + n_2 - 2}$$

**LOS**: 8.g | **Condition**: Use only when population variances are assumed equal.

---

## Paired Comparison Test

A t-test applied to the differences between paired observations. Used when two sets of observations are related (e.g., before/after measurements for the same subjects).

$$t = \frac{\bar{d} - \mu_{d_0}}{s_d / \sqrt{n}} \qquad df = n - 1$$

where $\bar{d}$ = mean of paired differences.

**LOS**: 8.g | **Advantage**: Controls for individual differences, increasing statistical power.

---

## Parametric Test

A statistical test that makes assumptions about the distribution of the population (typically normality) and tests hypotheses about population parameters.

**LOS**: 8.i | **Examples**: [[#z-Test]], [[#t-Test]], [[#F-Test]], [[#Chi-Square Test]]. | **Contrast**: [[#Nonparametric Test]]

---

## Nonparametric Test

A statistical test that does not rely on assumptions about the population distribution or that tests hypotheses not about population parameters. Used when data are ranked, not normally distributed, or sample sizes are very small.

**LOS**: 8.i | **Examples**: Spearman rank correlation, sign test, Wilcoxon signed-rank test. | **See**: [[quantitative-methods/glossary/m09-parametric-tests#Spearman Rank Correlation|Spearman Rank Correlation]]
