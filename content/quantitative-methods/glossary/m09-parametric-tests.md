---
title: "Glossary: M09 — Parametric and Nonparametric Tests"
type: glossary
subject: quantitative-methods
module: M09
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, nonparametric, spearman, chi-square, independence]
---

# Glossary: M09 — Parametric and Nonparametric Tests

**Module**: [[quantitative-methods/modules/m09-parametric-tests/index|M09]]
**Formulas**: [[quantitative-methods/formulas/parametric-tests|Formula Sheet]]

---

## Parametric Test (detailed)

A hypothesis test that relies on assumptions about the probability distribution of the population (typically that the data are normally distributed) and tests hypotheses about specific parameters such as the mean or variance. Requires data measured on at least an interval scale.

**LOS**: 9.a | **When to use**: When underlying distribution assumptions are met and data are interval or ratio scale. | **Examples**: [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-Test]], [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-Test]], [[quantitative-methods/glossary/m08-hypothesis-testing#z-Test|z-Test]]. | **Contrast**: [[#Nonparametric Test (detailed)]]

---

## Nonparametric Test (detailed)

A hypothesis test that does not rely on assumptions about the probability distribution of the population, or that tests hypotheses that are not about specific parameters. Used when data violate normality assumptions, are measured on an ordinal scale, or when sample sizes are very small.

**LOS**: 9.a | **When to use**: (1) Data are ranked (ordinal); (2) population is non-normal and sample is small; (3) hypothesis is not about a parameter (e.g., independence); (4) data contain outliers. | **Advantage**: Distribution-free. | **Disadvantage**: Less powerful than parametric tests when parametric assumptions hold.

---

## Spearman Rank Correlation

A nonparametric measure of the monotonic relationship between two variables, based on the ranks of the observations rather than their actual values. Ranges from −1 to +1.

$$r_s = 1 - \frac{6 \sum d_i^2}{n(n^2 - 1)}$$

where $d_i$ = difference between the ranks of the $i$-th pair of observations and $n$ = number of pairs.

**LOS**: 9.b | **Test statistic** (to test $H_0$: $\rho_s = 0$):
$$t = \frac{r_s \sqrt{n-2}}{\sqrt{1 - r_s^2}} \qquad df = n - 2$$

**Key**: More robust than Pearson correlation when data have outliers or are not normally distributed. | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Correlation|Pearson Correlation]]

---

## Chi-Square Test of Independence

A nonparametric test that determines whether two categorical variables are statistically independent. Uses a [[#Contingency Table (test context)]] to compare observed and expected frequencies.

$$\chi^2 = \sum_{\text{all cells}} \frac{(O_{ij} - E_{ij})^2}{E_{ij}}$$

$$df = (r-1)(c-1)$$

where $r$ = number of rows and $c$ = number of columns in the contingency table.

**LOS**: 9.c | **Decision**: Reject $H_0$ (independence) if $\chi^2 > \chi^2_{\alpha, df}$. | **Related**: [[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|Chi-Square Test]], [[quantitative-methods/glossary/m03-statistical-measures#Contingency Table|Contingency Table]]

---

## Contingency Table (test context)

A cross-tabulation matrix that displays the frequency distribution of two categorical variables simultaneously. Used as the input for the [[#Chi-Square Test of Independence]].

$$\begin{array}{c|cc|c}
 & B_1 & B_2 & \text{Total} \\
\hline
A_1 & O_{11} & O_{12} & R_1 \\
A_2 & O_{21} & O_{22} & R_2 \\
\hline
\text{Total} & C_1 & C_2 & n
\end{array}$$

**LOS**: 9.c | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Contingency Table|Contingency Table (descriptive)]]

---

## Expected Frequency

The frequency that would be expected in each cell of a contingency table if the two variables were perfectly independent. Used in the chi-square test.

$$E_{ij} = \frac{R_i \times C_j}{n}$$

where $R_i$ = row $i$ total, $C_j$ = column $j$ total, $n$ = overall sample size.

**LOS**: 9.c | **Rule of thumb**: All expected frequencies should be at least 5 for the chi-square approximation to be valid.

---

## Observed Frequency

The actual count of observations falling in each cell of a [[#Contingency Table (test context)]]. Compared to [[#Expected Frequency]] in the chi-square test statistic.

**LOS**: 9.c | **Notation**: $O_{ij}$ = observed frequency in row $i$, column $j$.
