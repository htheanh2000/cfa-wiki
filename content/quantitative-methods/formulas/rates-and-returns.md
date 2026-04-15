---
title: "Formulas: Rates and Returns"
type: formula
subject: quantitative-methods
module: M01
created: 2026-04-09
updated: 2026-04-09
tags: [formulas, rates, returns, hpr, mwr, twr]
---

# Formulas: Rates and Returns

**Module**: [[quantitative-methods/modules/m01-rates-and-returns/index|M01]]

## Required Rate of Return

$$
r = r_f + \text{Default RP} + \text{Liquidity RP} + \text{Maturity RP}
$$

$$
r_f = \text{Real risk-free rate} + \text{Inflation premium}
$$

## Holding Period Return (HPR)

$$
HPR = \frac{P_1 - P_0 + I_1}{P_0}
$$

## Multi-Period HPR

$$
HPR = (1+R_1)(1+R_2)\cdots(1+R_n) - 1
$$

## Arithmetic Mean Return

$$
\bar{R} = \frac{R_1 + R_2 + \cdots + R_n}{n}
$$

## Geometric Mean Return

$$
\bar{R}_G = \sqrt[n]{(1+R_1)(1+R_2)\cdots(1+R_n)} - 1
$$

Also: $\bar{R}_G = \sqrt[n]{1 + HPR} - 1$

## Harmonic Mean

$$
\bar{X}_H = \frac{n}{\sum_{i=1}^{n} \frac{1}{X_i}}
$$

## Harmonic Mean Return

$$
\bar{X}_H = \frac{n}{\sum_{i=1}^{n} \frac{1}{1+R_i}} - 1
$$

## Key Inequality

$$
\bar{R}_H \leq \bar{R}_G \leq \bar{R}
$$

Equality holds only when all $R_i$ are identical.

## Money-Weighted Return (MWR)

Solve for $IRR$ in:

$$
\sum_{t=0}^{n} \frac{CF_t}{(1+IRR)^t} = 0
$$

## Time-Weighted Return (TWR)

$$
TWR = (1+HPR_1)(1+HPR_2)\cdots(1+HPR_n) - 1
$$

For periods > 1 year, annualize using geometric mean.

## Net Return

$$
R_{\text{net}} = R_{\text{gross}} - \text{Fees}
$$

## After-Tax Return

$$
R_{\text{after-tax}} = R_{\text{pretax}} \times (1 - \text{tax rate})
$$

## Real Return

$$
R_{\text{real}} = \frac{1 + R_{\text{nominal}}}{1 + \text{Inflation}} - 1
$$

## Leveraged Return

$$
R_L = R_p + \frac{V_B}{V_E}(R_p - r_D)
$$

where $V_B$ = borrowed capital, $V_E$ = equity capital, $r_D$ = borrowing cost
