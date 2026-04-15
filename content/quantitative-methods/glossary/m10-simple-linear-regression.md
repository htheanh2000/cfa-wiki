---
title: "Glossary: M10 — Simple Linear Regression"
type: glossary
subject: quantitative-methods
module: M10
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, regression, OLS, R-squared, ANOVA, heteroskedasticity]
---

# Glossary: M10 — Simple Linear Regression

**Module**: [[quantitative-methods/modules/m10-simple-linear-regression/index|M10]]
**Formulas**: [[quantitative-methods/formulas/regression|Formula Sheet]]
**Concept page**: [[quantitative-methods/concepts/regression|Regression Concept]]

---

## Simple Linear Regression

A statistical model that estimates the linear relationship between one [[#Dependent Variable]] and one [[#Independent Variable]]. The estimated model form is:

$$\hat{Y}_i = \hat{b}_0 + \hat{b}_1 X_i$$

**LOS**: 10.a | **Purpose**: Explain variation in $Y$, test whether $X$ helps explain $Y$, and make predictions. | **Related**: [[quantitative-methods/concepts/regression|Regression Concept]]

---

## Dependent Variable

The variable whose variation is being explained or predicted in a regression model. Placed on the left-hand side of the regression equation. Also called the response variable or regressand.

**LOS**: 10.a | **Notation**: $Y$ | **Contrast**: [[#Independent Variable]]

---

## Independent Variable

The variable used to explain or predict the dependent variable. Placed on the right-hand side of the regression equation. Also called the explanatory variable, predictor, or regressor.

**LOS**: 10.a | **Notation**: $X$ | **Contrast**: [[#Dependent Variable]]

---

## Intercept

The estimated value of the dependent variable when the independent variable equals zero. The regression line's crossing point on the $Y$-axis.

**LOS**: 10.a | **Notation**: $\hat{b}_0$ | **Caution**: The intercept may not have a meaningful economic interpretation if $X = 0$ is outside the data range.

---

## Slope Coefficient

The estimated change in the dependent variable associated with a one-unit increase in the independent variable.

$$\hat{b}_1 = \frac{\text{Cov}(X,Y)}{s_X^2}$$

**LOS**: 10.a | **Interpretation**: If $\hat{b}_1 = 2.5$, a one-unit increase in $X$ is associated with a 2.5-unit increase in $Y$, on average.

---

## Ordinary Least Squares (OLS)

The most common method for estimating regression coefficients. Minimizes the sum of squared residuals (vertical distances between observed and fitted values).

$$\min_{\hat{b}_0, \hat{b}_1} \sum_{i=1}^{n} \hat{\varepsilon}_i^2 = \min \sum_{i=1}^{n} (Y_i - \hat{b}_0 - \hat{b}_1 X_i)^2$$

**LOS**: 10.b | **Property**: Produces the Best Linear Unbiased Estimator (BLUE) when classical assumptions hold.

---

## Residual

The difference between the actual value $Y_i$ and the fitted value $\hat{Y}_i$ for observation $i$. Also called the estimated error.

$$\hat{\varepsilon}_i = Y_i - \hat{Y}_i = Y_i - \hat{b}_0 - \hat{b}_1 X_i$$

**LOS**: 10.b | **Key**: OLS minimizes $\sum \hat{\varepsilon}_i^2$. Residuals sum to zero: $\sum \hat{\varepsilon}_i = 0$.

---

## Regression Line

The estimated line $\hat{Y} = \hat{b}_0 + \hat{b}_1 X$ that minimizes the sum of squared residuals. Passes through the point $(\bar{X}, \bar{Y})$.

**LOS**: 10.b | **Related**: [[#Ordinary Least Squares (OLS)]]

---

## Sum of Squares Total (SST)

The total variation in the dependent variable around its mean. Decomposed into explained and unexplained variation.

$$SST = \sum_{i=1}^{n} (Y_i - \bar{Y})^2 = SSR + SSE$$

**LOS**: 10.c | **Related**: [[#Sum of Squares Regression (SSR)]], [[#Sum of Squares Error (SSE)]]

---

## Sum of Squares Regression (SSR)

The variation in $Y$ explained by the regression model — the portion attributable to the independent variable.

$$SSR = \sum_{i=1}^{n} (\hat{Y}_i - \bar{Y})^2$$

**LOS**: 10.c | **Also called**: Explained sum of squares (ESS).

---

## Sum of Squares Error (SSE)

The unexplained variation in $Y$ — the portion not captured by the regression model.

$$SSE = \sum_{i=1}^{n} (Y_i - \hat{Y}_i)^2 = \sum_{i=1}^{n} \hat{\varepsilon}_i^2$$

**LOS**: 10.c | **Also called**: Residual sum of squares (RSS).

---

## Coefficient of Determination (R²)

The proportion of the total variation in the dependent variable explained by the independent variable. Ranges from 0 to 1.

$$R^2 = \frac{SSR}{SST} = 1 - \frac{SSE}{SST}$$

**LOS**: 10.d | **Interpretation**: $R^2 = 0.72$ means 72% of the variation in $Y$ is explained by $X$. | **Note**: In simple linear regression, $R^2 = r_{XY}^2$ (squared Pearson correlation).

---

## Standard Error of Estimate (SEE)

A measure of the average magnitude of the regression residuals. Indicates how closely the regression line fits the data.

$$SEE = \sqrt{\frac{SSE}{n-2}} = \sqrt{MSE}$$

**LOS**: 10.d | **Key**: Lower SEE → better fit. Used to construct [[#Prediction Interval|prediction intervals]]. | **Related**: [[#Mean Square Error (MSE)]]

---

## Mean Square Regression (MSR)

The average explained variation per degree of freedom used by the regression model.

$$MSR = \frac{SSR}{k}$$

where $k$ = number of independent variables (= 1 for simple linear regression).

**LOS**: 10.e | **Related**: [[#F-Statistic]]

---

## Mean Square Error (MSE)

The average unexplained variation per degree of freedom — an estimate of the error variance.

$$MSE = \frac{SSE}{n-k-1} = \frac{SSE}{n-2} \quad \text{(simple regression)}$$

**LOS**: 10.e | **Related**: [[#Standard Error of Estimate (SEE)]]

---

## ANOVA (Analysis of Variance)

A table that partitions the total variation in $Y$ into explained (regression) and unexplained (error) components. Used to test the overall significance of the regression model.

| Source | SS | df | MS | F |
|--------|----|----|----|----|
| Regression | SSR | $k$ | MSR | MSR/MSE |
| Error | SSE | $n-k-1$ | MSE | |
| Total | SST | $n-1$ | | |

**LOS**: 10.e | **Related**: [[#F-Statistic]], [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-Test]]

---

## F-Statistic

The ratio of mean square regression to mean square error. Tests the null hypothesis that all regression slope coefficients are zero (model has no explanatory power).

$$F = \frac{MSR}{MSE} = \frac{SSR/k}{SSE/(n-k-1)}$$

**LOS**: 10.e | **Decision**: Reject $H_0$ if $F > F_{\text{critical}}$ (upper-tailed test). | **In simple regression**: $F = t_{\hat{b}_1}^2$.

---

## t-Test for Slope

Test of whether the slope coefficient is statistically significantly different from zero (or another hypothesized value).

$$t = \frac{\hat{b}_1 - b_{1,0}}{s_{\hat{b}_1}} \qquad df = n - 2$$

**LOS**: 10.f | **$H_0$**: $b_1 = 0$ (no linear relationship between $X$ and $Y$).

---

## t-Test for Correlation

Test of whether the population correlation coefficient is statistically significantly different from zero.

$$t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}} \qquad df = n - 2$$

**LOS**: 10.f | **Note**: In simple linear regression, this test is equivalent to the [[#t-Test for Slope]].

---

## t-Test for Intercept

Test of whether the intercept is statistically significantly different from zero.

$$t = \frac{\hat{b}_0 - b_{0,0}}{s_{\hat{b}_0}} \qquad df = n - 2$$

**LOS**: 10.f | **Note**: Often less economically meaningful than the slope test.

---

## Prediction Interval

An interval estimate for an individual value of $Y$ given a specific value of $X$. Wider than a confidence interval because it must account for both model uncertainty and individual error.

$$\hat{Y} \pm t_{\alpha/2, n-2} \times s_f$$

**LOS**: 10.g | **Related**: [[#Standard Error of Forecast]]

---

## Standard Error of Forecast

The standard deviation of the forecast error for a predicted value of $Y$ at a given $X = X_0$. Larger when $X_0$ is far from $\bar{X}$ or sample size is small.

$$s_f = SEE \sqrt{1 + \frac{1}{n} + \frac{(X_0 - \bar{X})^2}{\sum(X_i - \bar{X})^2}}$$

**LOS**: 10.g | **Related**: [[#Standard Error of Estimate (SEE)]], [[#Prediction Interval]]

---

## Homoskedasticity

The assumption that the variance of regression errors is constant across all values of the independent variable. A required classical regression assumption.

$$\text{Var}(\varepsilon_i) = \sigma^2 \quad \text{for all } i$$

**LOS**: 10.h | **Contrast**: [[#Heteroskedasticity]]

---

## Heteroskedasticity

Violation of the [[#Homoskedasticity]] assumption — the variance of the regression errors is not constant across all observations. Common in financial data.

**LOS**: 10.h | **Consequence**: OLS standard errors are biased → unreliable $t$- and $F$-statistics. | **Detection**: Breusch-Pagan test; visual inspection of residual plot.

---

## Linearity Assumption

The assumption that the relationship between the dependent and independent variables is linear. Required for OLS estimates to be unbiased.

**LOS**: 10.h | **Violation remedy**: Transform variables using [[#Log-Lin Model]], [[#Lin-Log Model]], or [[#Log-Log Model]].

---

## Independence Assumption

The assumption that the regression errors are uncorrelated with each other and with the independent variable. Violation (serial correlation) is common in time-series data.

**LOS**: 10.h | **Detection**: Durbin-Watson test for serial correlation.

---

## Normality Assumption

The assumption that the regression errors are normally distributed. Required for valid inference in small samples (t- and F-tests).

**LOS**: 10.h | **Note**: By the [[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem (CLT)|CLT]], this assumption is less critical in large samples.

---

## Cross-Sectional Regression

A regression using data from multiple subjects (firms, individuals, countries) observed at a single point in time.

**LOS**: 10.i | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Cross-Sectional Data|Cross-Sectional Data]]

---

## Time-Series Regression

A regression using data from a single subject observed at multiple points in time.

**LOS**: 10.i | **Concern**: Potential serial correlation in errors. | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Time Series Data|Time Series Data]]

---

## Indicator Variable

A binary variable that takes the value 1 if a condition is met and 0 otherwise. Used to represent categorical variables in regression. Also called a dummy variable.

$$D_i = \begin{cases} 1 & \text{if condition is true} \\ 0 & \text{otherwise} \end{cases}$$

**LOS**: 10.j | **Application**: Capturing structural differences between groups (e.g., recession vs. non-recession periods).

---

## Log-Lin Model

A regression model where the dependent variable is in log form and the independent variable is in level form.

$$\ln(Y_i) = b_0 + b_1 X_i + \varepsilon_i$$

**LOS**: 10.k | **Interpretation**: A one-unit increase in $X$ is associated with a $b_1 \times 100\%$ change in $Y$.

---

## Lin-Log Model

A regression model where the dependent variable is in level form and the independent variable is in log form.

$$Y_i = b_0 + b_1 \ln(X_i) + \varepsilon_i$$

**LOS**: 10.k | **Interpretation**: A 1% increase in $X$ is associated with a $b_1/100$ unit change in $Y$.

---

## Log-Log Model

A regression model where both the dependent and independent variables are in log form.

$$\ln(Y_i) = b_0 + b_1 \ln(X_i) + \varepsilon_i$$

**LOS**: 10.k | **Interpretation**: A 1% increase in $X$ is associated with a $b_1\%$ change in $Y$. The slope $b_1$ is the elasticity of $Y$ with respect to $X$.
