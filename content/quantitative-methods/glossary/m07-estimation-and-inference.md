---
title: "Glossary: M07 — Estimation and Inference"
type: glossary
subject: quantitative-methods
module: M07
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, sampling, estimation, CLT, confidence-interval, bias]
---

# Glossary: M07 — Estimation and Inference

**Module**: [[quantitative-methods/modules/m07-estimation-and-inference/index|M07]]
**Formulas**: [[quantitative-methods/formulas/estimation-inference|Formula Sheet]]
**Concept page**: [[quantitative-methods/concepts/sampling-and-estimation|Sampling and Estimation]]

---

## Population

The complete set of all items of interest to an analyst. Characterized by parameters such as the population mean $\mu$ and variance $\sigma^2$.

**LOS**: 7.a | **Contrast**: [[#Sample]]

---

## Sample

A subset of the population selected for analysis. Used to estimate population parameters when examining the entire population is impractical or impossible.

**LOS**: 7.a | **Related**: [[#Sampling Error]], [[#Sampling Distribution]]

---

## Parameter

A descriptive measure of an entire population (e.g., $\mu$, $\sigma^2$). Parameters are typically unknown and must be estimated from sample data.

**LOS**: 7.a | **Contrast**: [[#Statistic]]

---

## Statistic

A descriptive measure computed from a sample (e.g., sample mean $\bar{X}$, sample variance $s^2$). Used as an estimate of the corresponding population [[#Parameter]].

**LOS**: 7.a | **Related**: [[#Point Estimate]], [[#Unbiased Estimator]]

---

## Sampling Error

The difference between the value of a statistic computed from a sample and the true value of the population parameter.

$$\text{Sampling error} = \bar{X} - \mu$$

**LOS**: 7.b | **Note**: Sampling error does not imply a mistake; it is the natural variation due to working with a subset of the population.

---

## Simple Random Sampling

A sampling method in which every member of the population has an equal probability of being selected, and each sample of size $n$ is equally likely to be chosen.

**LOS**: 7.c | **Related**: [[#Probability Sampling]]

---

## Systematic Sampling

A sampling method in which every $k$-th member of the population is selected after a random starting point. Efficient for large populations with a natural ordering.

**LOS**: 7.c | **Risk**: Can introduce bias if the population has a periodic pattern matching the sampling interval.

---

## Stratified Random Sampling

A sampling method in which the population is divided into subgroups (strata) based on a characteristic, and random samples are drawn from each stratum in proportion to its size.

**LOS**: 7.c | **Advantage**: Ensures representation of all subgroups; reduces variance. | **Application**: Index construction, where bond/stock subgroups must be represented.

---

## Cluster Sampling

A sampling method in which the population is divided into clusters, a random selection of clusters is chosen, and all members of selected clusters are included.

**LOS**: 7.c | **Contrast**: [[#Stratified Random Sampling]] samples from each stratum; cluster sampling selects entire clusters.

---

## Convenience Sampling

A non-probability sampling method in which the sample consists of members of the population that are easy to obtain. Subject to selection bias.

**LOS**: 7.c | **Risk**: May not be representative of the population. | **Related**: [[#Non-Probability Sampling]]

---

## Judgmental Sampling

A non-probability sampling method in which the analyst uses personal judgment to select which population members to include in the sample.

**LOS**: 7.c | **Limitation**: Highly subjective and potentially biased. | **Related**: [[#Non-Probability Sampling]]

---

## Probability Sampling

Any sampling method in which each member of the population has a known, non-zero probability of being selected. Includes [[#Simple Random Sampling]], [[#Systematic Sampling]], [[#Stratified Random Sampling]], and [[#Cluster Sampling]].

**LOS**: 7.c | **Contrast**: [[#Non-Probability Sampling]]

---

## Non-Probability Sampling

Sampling methods where some members of the population have no chance of being selected, or the probability of selection is unknown. Includes [[#Convenience Sampling]] and [[#Judgmental Sampling]].

**LOS**: 7.c | **Risk**: Results may not be generalizable to the population.

---

## Sampling Distribution

The probability distribution of a statistic (e.g., sample mean $\bar{X}$) computed from all possible samples of a given size $n$ drawn from a population.

**LOS**: 7.d | **Key concept**: The [[#Central Limit Theorem (CLT)]] describes the sampling distribution of the mean.

---

## Central Limit Theorem (CLT)

States that for a population with mean $\mu$ and variance $\sigma^2$, the sampling distribution of the sample mean $\bar{X}$ approaches a normal distribution as $n$ increases, regardless of the population's distribution.

$$\bar{X} \sim N\left(\mu, \frac{\sigma^2}{n}\right) \quad \text{approximately, for large } n \text{ (typically } n \geq 30\text{)}$$

**LOS**: 7.d | **Importance**: Justifies the use of normal-based inference even when the population is non-normal. | **Related**: [[#Standard Error]], [[#Confidence Interval]]

---

## Standard Error

The standard deviation of the sampling distribution of a statistic. For the sample mean:

$$\sigma_{\bar{X}} = \frac{\sigma}{\sqrt{n}} \qquad s_{\bar{X}} = \frac{s}{\sqrt{n}} \text{ (when } \sigma \text{ unknown)}$$

**LOS**: 7.d | **Key**: Standard error decreases as sample size $n$ increases — larger samples produce more precise estimates.

---

## Point Estimate

A single value used to estimate an unknown population parameter. For example, $\bar{X}$ as an estimate of $\mu$.

**LOS**: 7.e | **Limitation**: Does not communicate the uncertainty of the estimate. | **Contrast**: [[#Confidence Interval]]

---

## Confidence Interval

A range of values constructed such that the probability is $(1 - \alpha)$ that the interval contains the true population parameter. Formula for the population mean:

$$\bar{X} \pm z_{\alpha/2} \frac{\sigma}{\sqrt{n}} \quad \text{(when } \sigma \text{ known)}$$

$$\bar{X} \pm t_{\alpha/2, n-1} \frac{s}{\sqrt{n}} \quad \text{(when } \sigma \text{ unknown)}$$

**LOS**: 7.e | **Key**: A 95% CI does NOT mean there is a 95% probability the true mean falls in THIS interval; rather, 95% of such intervals constructed over many samples will contain the true mean.

---

## Level of Significance

Denoted $\alpha$. The probability of making a [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]] — rejecting a true null hypothesis. The complement of the degree of confidence.

$$\alpha = 1 - \text{Degree of Confidence}$$

**LOS**: 7.e | **Common values**: $\alpha = 0.10$, $0.05$, $0.01$. | **Related**: [[quantitative-methods/glossary/m08-hypothesis-testing#Level of Significance|Hypothesis Testing]]

---

## Degree of Confidence

The probability $(1-\alpha)$ that the confidence interval contains the true parameter value. Also called the confidence level.

**LOS**: 7.e | **Common values**: 90%, 95%, 99%.

---

## Reliability Factor

The critical value ($z^*$ or $t^*$) used to construct a confidence interval. Determines the interval's width.

**LOS**: 7.e | **Common reliability factors**: $z_{0.025} = 1.96$ for 95% CI; $z_{0.005} = 2.576$ for 99% CI.

---

## Unbiased Estimator

An estimator whose expected value equals the population parameter it estimates. No systematic over- or under-estimation.

$$E(\hat{\theta}) = \theta$$

**LOS**: 7.f | **Example**: Sample mean $\bar{X}$ is unbiased for $\mu$; sample variance $s^2$ (with $n-1$ denominator) is unbiased for $\sigma^2$.

---

## Efficient Estimator

Among unbiased estimators, the one with the smallest variance. The most precise unbiased estimator.

**LOS**: 7.f | **Related**: [[#Unbiased Estimator]], [[#Consistent Estimator]]

---

## Consistent Estimator

An estimator that converges to the true population parameter as sample size increases — i.e., becomes more accurate with larger samples.

**LOS**: 7.f | **Key**: A consistent estimator may be biased in small samples but converges to the true value as $n \to \infty$.

---

## Data Snooping Bias

Bias that arises from repeatedly testing the same data set until a pattern or significant result is found. The discovered pattern may be spurious and not generalize to new data.

**LOS**: 7.g | **In practice**: Mining historical data to find investment strategies may identify patterns that worked in the past purely by chance.

---

## Sample Selection Bias

Bias that arises when some members of the population are systematically excluded from the sample, making the sample unrepresentative.

**LOS**: 7.g | **Related**: [[#Survivorship Bias]]

---

## Survivorship Bias

A form of [[#Sample Selection Bias]] in which only surviving (successful) entities are included in a sample — failed funds or firms that no longer exist are excluded.

**LOS**: 7.g | **Effect**: Overstates historical performance; understates risk. | **Example**: Mutual fund databases that exclude defunct funds show artificially high average returns.

---

## Look-Ahead Bias

Bias introduced when a study uses information that was not available at the time the investment decision would have been made. Overstates historical performance.

**LOS**: 7.g | **Example**: Using full-year earnings (reported in February) to make investment decisions retroactively dated to January of that year.

---

## Time Period Bias

Bias arising from selecting a sample period that is too short, too long, or not representative of all market conditions. Results may not generalize to other periods.

**LOS**: 7.g | **Example**: A strategy back-tested only during a bull market may appear superior but perform poorly in bear markets.

---

## Backfill Bias

Bias that arises when a database is filled with the historical returns of funds only after those funds are added to the database. Funds with poor early histories are less likely to be added — inflating reported performance.

**LOS**: 7.g | **Also called**: Instant history bias. | **Related**: [[#Survivorship Bias]], [[#Sample Selection Bias]]
