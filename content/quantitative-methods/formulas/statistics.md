---
title: "Formulas: Statistical Measures"
type: formula
subject: quantitative-methods
module: M03
created: 2026-04-09
updated: 2026-04-09
tags: [formulas, statistics, mean, variance, skewness, kurtosis]
---

# Formulas: Statistical Measures

**Module**: [[quantitative-methods/modules/m03-statistical-measures/index|M03]]

## Arithmetic Mean

$$\bar{X} = \frac{\sum_{i=1}^{n} X_i}{n}$$

## Weighted Mean

$$\bar{X}_w = \sum_{i=1}^{n} w_i X_i$$

## Geometric Mean

$$\bar{X}_G = \sqrt[n]{X_1 \cdot X_2 \cdots X_n}$$

## Harmonic Mean

$$\bar{X}_H = \frac{n}{\sum_{i=1}^{n} \frac{1}{X_i}}$$

## Range

$$\text{Range} = X_{\max} - X_{\min}$$

## Mean Absolute Deviation (MAD)

$$MAD = \frac{\sum_{i=1}^{n} |X_i - \bar{X}|}{n}$$

## Population Variance

$$\sigma^2 = \frac{\sum_{i=1}^{N} (X_i - \mu)^2}{N}$$

## Sample Variance

$$s^2 = \frac{\sum_{i=1}^{n} (X_i - \bar{X})^2}{n - 1}$$

## Standard Deviation

$$\sigma = \sqrt{\sigma^2} \qquad s = \sqrt{s^2}$$

## Coefficient of Variation

$$CV = \frac{s}{\bar{X}}$$

## Target Downside Deviation

$$s_{\text{target}} = \sqrt{\frac{\sum_{\text{for all } X_i < B} (X_i - B)^2}{n - 1}}$$

where $B$ = target return (benchmark)

## Skewness (Sample)

$$S_k = \frac{n}{(n-1)(n-2)} \sum \left(\frac{X_i - \bar{X}}{s}\right)^3$$

## Excess Kurtosis (Sample)

$$K_E = \frac{n(n+1)}{(n-1)(n-2)(n-3)} \sum \left(\frac{X_i - \bar{X}}{s}\right)^4 - \frac{3(n-1)^2}{(n-2)(n-3)}$$

## Covariance (Sample)

$$Cov(X,Y) = \frac{\sum_{i=1}^{n}(X_i - \bar{X})(Y_i - \bar{Y})}{n-1}$$

## Correlation

$$\rho(X,Y) = \frac{Cov(X,Y)}{\sigma_X \cdot \sigma_Y}$$
