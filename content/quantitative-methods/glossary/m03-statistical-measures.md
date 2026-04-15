---
title: "Glossary: M03 — Statistical Measures of Asset Returns"
type: glossary
subject: quantitative-methods
module: M03
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, statistics, mean, variance, skewness, kurtosis, correlation]
---

# Glossary: M03 — Statistical Measures of Asset Returns

**Module**: [[quantitative-methods/modules/m03-statistical-measures/index|M03]]
**Formulas**: [[quantitative-methods/formulas/statistical-measures|Formula Sheet]]

---

## Arithmetic Mean

The sum of all observed values divided by the number of observations. The most common measure of central tendency and an unbiased estimator of the population mean.

$$\bar{X} = \frac{\sum_{i=1}^{n} X_i}{n}$$

**LOS**: 3.a | **Key**: Sensitive to outliers; always greater than or equal to the [[#Geometric Mean Return|geometric mean]]. | **See also**: [[quantitative-methods/glossary/m01-rates-and-returns#Arithmetic Mean Return|Arithmetic Mean Return]]

---

## Weighted Mean

A mean that assigns different weights to each observation, reflecting its relative importance. Used in portfolio return calculations.

$$\bar{X}_w = \sum_{i=1}^{n} w_i X_i \qquad \text{where } \sum w_i = 1$$

**LOS**: 3.a | **Application**: Portfolio expected return where $w_i$ = portfolio weight of asset $i$.

---

## Trimmed Mean

The arithmetic mean calculated after removing a stated percentage of the most extreme observations from both tails of the distribution. Reduces the influence of outliers.

**LOS**: 3.a | **Example**: A 5% trimmed mean removes the bottom 5% and top 5% of observations before computing the mean.

---

## Winsorized Mean

A mean calculated by replacing extreme values at both tails with the value at a specified percentile, rather than removing them. Less distorted by outliers than the arithmetic mean.

**LOS**: 3.a | **Contrast**: [[#Trimmed Mean]] removes extremes; Winsorized mean replaces them with the boundary value.

---

## Median

The midpoint of a sorted data set — 50% of observations lie above and 50% lie below. For an even number of observations, it is the average of the two middle values.

**LOS**: 3.a | **Key**: Not affected by extreme outliers. Preferred over mean when distribution is skewed. | **Related**: [[#Positive Skew]], [[#Negative Skew]]

---

## Mode

The value that appears most frequently in a data set. A distribution may be unimodal, bimodal, or multimodal. The mode is the only measure of central tendency applicable to nominal (categorical) data.

**LOS**: 3.a | **Note**: In a symmetrical, unimodal distribution: mean = median = mode.

---

## Quantile

A value below which a specified proportion of the observations fall. Quantiles divide a distribution into equal parts. Includes [[#Quartile]], [[#Quintile]], [[#Decile]], and [[#Percentile]].

**LOS**: 3.b | **See**: [[#Percentile]], [[#Quartile]], [[#Quintile]], [[#Decile]]

---

## Percentile

A quantile that divides a distribution into 100 equal parts. The $p$-th percentile is the value below which $p\%$ of observations fall.

$$L_y = \frac{(n+1) \times y}{100}$$

where $L_y$ = location of the $y$-th percentile and $n$ = number of observations.

**LOS**: 3.b | **Example**: The 90th percentile is the value at or below which 90% of data falls.

---

## Quartile

A quantile that divides a distribution into four equal parts. Q1 = 25th percentile, Q2 = 50th percentile (median), Q3 = 75th percentile.

**LOS**: 3.b | **Related**: [[#Interquartile Range (IQR)]]

---

## Quintile

A quantile that divides a distribution into five equal parts. Each quintile contains 20% of observations.

**LOS**: 3.b

---

## Decile

A quantile that divides a distribution into ten equal parts. Each decile contains 10% of observations.

**LOS**: 3.b

---

## Interquartile Range (IQR)

The difference between the third and first quartiles (Q3 − Q1). Measures the spread of the middle 50% of the data, making it robust to outliers.

$$IQR = Q3 - Q1$$

**LOS**: 3.c | **Use**: More robust measure of dispersion than [[#Range]] when outliers are present.

---

## Range

The simplest measure of dispersion — the difference between the maximum and minimum values in a data set.

$$\text{Range} = X_{\max} - X_{\min}$$

**LOS**: 3.c | **Limitation**: Highly sensitive to outliers; uses only two data points.

---

## Mean Absolute Deviation (MAD)

The average of the absolute deviations of observations from their arithmetic mean. A measure of dispersion that treats all deviations equally.

$$MAD = \frac{\sum_{i=1}^{n} |X_i - \bar{X}|}{n}$$

**LOS**: 3.c | **Note**: Less mathematically tractable than variance but easier to interpret intuitively.

---

## Variance (Population)

The average of squared deviations from the population mean. Measures the dispersion of the entire population.

$$\sigma^2 = \frac{\sum_{i=1}^{N} (X_i - \mu)^2}{N}$$

**LOS**: 3.c | **Related**: [[#Variance (Sample)]], [[#Standard Deviation]]

---

## Variance (Sample)

An estimate of population variance calculated from a sample. Uses $n-1$ in the denominator to correct for bias (Bessel's correction).

$$s^2 = \frac{\sum_{i=1}^{n} (X_i - \bar{X})^2}{n-1}$$

**LOS**: 3.c | **Key**: Dividing by $n-1$ makes $s^2$ an unbiased estimator of $\sigma^2$.

---

## Standard Deviation

The positive square root of variance. Expressed in the same units as the original data, making it more interpretable than variance.

$$\sigma = \sqrt{\sigma^2} \qquad s = \sqrt{s^2}$$

**LOS**: 3.c | **Related**: [[#Coefficient of Variation (CV)]], [[quantitative-methods/glossary/m04-probability#Standard Deviation of Random Variable|Standard Deviation of Random Variable]]

---

## Coefficient of Variation (CV)

The ratio of standard deviation to the mean. A dimensionless measure of relative dispersion that allows comparison of variability across data sets with different units or means.

$$CV = \frac{s}{\bar{X}}$$

**LOS**: 3.c | **Key**: Higher CV → greater relative risk per unit of expected return. | **Application**: Comparing risk of investments with different expected returns.

---

## Target Downside Deviation

A measure of downside risk calculated as the standard deviation of returns below a specified target return $B$. Also called target semideviation.

$$s_{\text{target}} = \sqrt{\frac{\sum_{\text{all } R_t < B} (R_t - B)^2}{n-1}}$$

**LOS**: 3.c | **Key**: Only penalizes returns below the target; ignores returns above the target. More relevant to risk-averse investors.

---

## Skewness

A measure of the asymmetry of a distribution around its mean. A symmetrical distribution has skewness of zero.

$$\text{Skewness} = \frac{1}{n} \cdot \frac{\sum_{i=1}^{n}(X_i - \bar{X})^3}{s^3}$$

**LOS**: 3.d | **See**: [[#Positive Skew]], [[#Negative Skew]]

---

## Positive Skew

A distribution where the right tail is longer than the left tail. The mean is greater than the median, which is greater than the mode (mean > median > mode).

**LOS**: 3.d | **Implication for investors**: A few large positive returns pull the mean upward; the typical (median) outcome is lower than the mean.

---

## Negative Skew

A distribution where the left tail is longer than the right tail. The mean is less than the median, which is less than the mode (mean < median < mode).

**LOS**: 3.d | **Implication for investors**: A few large negative returns pull the mean down; more common in portfolios using options strategies. | **Related**: [[#Kurtosis]]

---

## Kurtosis

A measure of the "peakedness" and tail heaviness of a distribution relative to the normal distribution. The normal distribution has kurtosis of 3 (excess kurtosis = 0).

$$\text{Kurtosis} = \frac{1}{n} \cdot \frac{\sum_{i=1}^{n}(X_i - \bar{X})^4}{s^4}$$

**LOS**: 3.d | **See**: [[#Leptokurtic]], [[#Mesokurtic]], [[#Platykurtic]], [[#Excess Kurtosis]]

---

## Leptokurtic

A distribution with kurtosis greater than 3 (excess kurtosis > 0). Has fatter tails and a higher peak than the normal distribution. More extreme outcomes (outliers) are more likely.

**LOS**: 3.d | **Risk implication**: Fat tails mean greater probability of extreme losses or gains than a normal distribution predicts.

---

## Mesokurtic

A distribution with kurtosis equal to 3 (excess kurtosis = 0). The [[quantitative-methods/glossary/m05-portfolio-math#Normal Distribution|normal distribution]] is mesokurtic.

**LOS**: 3.d

---

## Platykurtic

A distribution with kurtosis less than 3 (excess kurtosis < 0). Has thinner tails and a flatter peak than the normal distribution. Extreme outcomes are less likely than a normal distribution predicts.

**LOS**: 3.d

---

## Excess Kurtosis

Kurtosis minus 3. Measures kurtosis relative to the normal distribution. Leptokurtic distributions have positive excess kurtosis; platykurtic have negative excess kurtosis.

$$\text{Excess Kurtosis} = \text{Kurtosis} - 3$$

**LOS**: 3.d | **Related**: [[#Leptokurtic]], [[#Platykurtic]], [[#Mesokurtic]]

---

## Covariance

A measure of how two variables move together. Positive covariance means they tend to move in the same direction; negative covariance means they tend to move in opposite directions.

$$\text{Cov}(X,Y) = \frac{\sum_{i=1}^{n}(X_i - \bar{X})(Y_i - \bar{Y})}{n-1}$$

**LOS**: 3.e | **Limitation**: Magnitude depends on the scale of variables, making comparison difficult. | **Related**: [[#Correlation]], [[quantitative-methods/glossary/m05-portfolio-math#Covariance (Portfolio)|Portfolio Covariance]]

---

## Correlation

A standardized measure of the linear relationship between two variables, ranging from −1 to +1. Dimensionless and scale-independent.

$$\rho_{XY} = \frac{\text{Cov}(X,Y)}{s_X \cdot s_Y}$$

**LOS**: 3.e | **Interpretation**: +1 = perfect positive linear relationship; 0 = no linear relationship; −1 = perfect negative linear relationship. | **Related**: [[quantitative-methods/glossary/m05-portfolio-math#Correlation (Portfolio)|Portfolio Correlation]]

---

## Frequency Distribution

A tabular presentation of data showing the number of observations (frequency) falling within each class interval. Enables analysis of the shape of a distribution.

**LOS**: 3.f | **Related**: [[#Relative Frequency]], [[#Cumulative Frequency]]

---

## Relative Frequency

The frequency of a class interval expressed as a fraction or percentage of the total number of observations.

$$\text{Relative Frequency} = \frac{\text{Class Frequency}}{\text{Total Observations}}$$

**LOS**: 3.f

---

## Cumulative Frequency

The sum of the frequencies of all class intervals up to and including a given class. Shows how many observations fall at or below a certain value.

**LOS**: 3.f | **Related**: [[quantitative-methods/glossary/m05-portfolio-math#Cumulative Distribution Function (CDF)|CDF]]

---

## Contingency Table

A table that displays the frequency distribution of two or more categorical variables simultaneously. Used to examine the relationship between variables and assess statistical independence.

**LOS**: 3.g | **Application**: Basis for the [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|chi-square test of independence]].

---

## Structured Data

Data that is organized in a defined, searchable format — typically rows and columns in a database or spreadsheet. Easily processable by traditional analytical tools.

**LOS**: 3.h | **Examples**: Stock prices, financial statement data, economic indicators. | **Contrast**: [[#Unstructured Data]]

---

## Unstructured Data

Data that does not follow a predefined format or organization. Requires specialized processing techniques such as [[quantitative-methods/glossary/m11-big-data-techniques#Natural Language Processing (NLP)|NLP]] before it can be analyzed.

**LOS**: 3.h | **Examples**: Social media posts, news articles, satellite images, audio recordings. | **Related**: [[quantitative-methods/glossary/m11-big-data-techniques#Text Analytics|Text Analytics]]

---

## Time Series Data

A sequence of observations of a variable collected at equally spaced intervals over time. Used to identify trends, cycles, and seasonality.

**LOS**: 3.h | **Examples**: Daily stock prices, monthly GDP, quarterly earnings. | **Related**: [[#Cross-Sectional Data]], [[#Panel Data]]

---

## Cross-Sectional Data

Observations of multiple subjects (firms, countries, individuals) collected at a single point in time. Used to compare across entities.

**LOS**: 3.h | **Examples**: P/E ratios of S&P 500 companies at year-end; GDP of 50 countries in 2023.

---

## Panel Data

A data set that contains both time series and cross-sectional dimensions — multiple entities observed over multiple time periods. Also called longitudinal data.

**LOS**: 3.h | **Advantage**: Allows control for both cross-sectional and time-series variation. | **Related**: [[#Time Series Data]], [[#Cross-Sectional Data]]
