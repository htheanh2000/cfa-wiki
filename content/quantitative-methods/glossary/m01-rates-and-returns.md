---
title: "Glossary: M01 — Rates and Returns"
type: glossary
subject: quantitative-methods
module: M01
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, rates, returns]
---

# Glossary: M01 — Rates and Returns

**Module**: [[quantitative-methods/modules/m01-rates-and-returns/index|M01]]
**Formulas**: [[quantitative-methods/formulas/rates-and-returns|Formula Sheet]]

---

## Interest Rate

The amount a lender charges for the use of assets, expressed as a percentage of the principal. Can be interpreted as a [[#Discount Rate]], [[#Opportunity Cost]], or [[#Required Rate of Return]].

**LOS**: 1.a | **See**: [[quantitative-methods/modules/m01-rates-and-returns/index#LOS 1.a — Interest Rates|M01 — LOS 1.a]]

---

## Discount Rate

The rate at which investors discount future cash flows to arrive at their present value. A higher discount rate implies a lower present value.

**LOS**: 1.a | **Related**: [[quantitative-methods/glossary/m02-time-value-of-money#Present Value|Present Value]]

---

## Opportunity Cost

The value that investors forgo by choosing a particular course of action. If an investor can earn 8% on bonds, the opportunity cost of investing in stocks instead is 8%.

**LOS**: 1.a

---

## Required Rate of Return

The minimum rate of return an investor must receive to accept an investment. Composed of:

$$r = r_f + \text{Default RP} + \text{Liquidity RP} + \text{Maturity RP}$$

**LOS**: 1.a | **See**: [[#Nominal Risk-Free Rate]], [[#Default Risk Premium]], [[#Liquidity Risk Premium]], [[#Maturity Risk Premium]]

---

## Nominal Risk-Free Rate

The rate of return on a risk-free asset (e.g., US Treasury bill). Composed of two components:

$$r_f = \text{Real risk-free rate} + \text{Inflation premium}$$

**LOS**: 1.a | **Related**: [[#Real Risk-Free Rate]], [[#Inflation Premium]]

---

## Real Risk-Free Rate

The theoretical rate of return on an investment with zero risk and zero inflation. Reflects only the time preference for consumption — the compensation for deferring consumption.

**LOS**: 1.a | **Note**: Mainly theoretical; not directly observable in markets.

---

## Inflation Premium

The compensation investors require for the expected loss of purchasing power due to inflation over the investment horizon.

$$\text{Nominal risk-free rate} = \text{Real risk-free rate} + \text{Inflation premium}$$

**LOS**: 1.a | **Example**: If real rate = 2% and expected inflation = 3%, then nominal risk-free rate ≈ 5%.

---

## Default Risk Premium

The excess return that compensates investors for the risk that a borrower will not make promised payments in a timely manner.

**LOS**: 1.a | **Example**: Difference between corporate bond yield and Treasury yield of same maturity (the "credit spread").

---

## Liquidity Risk Premium

The excess return that compensates investors for the risk of receiving less than fair value when an investment must be sold quickly.

**LOS**: 1.a | **Example**: Small corporate bonds trade infrequently → higher liquidity premium than US Treasuries.

---

## Maturity Risk Premium

The excess return that compensates investors for the increased sensitivity of the market value of debt to changes in interest rates as maturity is extended.

**LOS**: 1.a | **Note**: Longer maturity → greater interest rate risk → higher maturity premium.

---

## Holding Period Return (HPR)

The return earned from holding an asset for a single specified period (1 day, 1 week, 1 year, etc.).

$$HPR = \frac{P_1 - P_0 + I_1}{P_0} = \frac{\text{Ending value}}{\text{Beginning value}} - 1$$

**LOS**: 1.b | **See**: [[quantitative-methods/formulas/rates-and-returns#Holding Period Return (HPR)|Formula]]

---

## Arithmetic Mean Return

The simple average of a series of periodic returns. An unbiased estimator of the true mean return.

$$\bar{R} = \frac{R_1 + R_2 + \cdots + R_n}{n}$$

**LOS**: 1.b | **Key**: Always ≥ geometric mean (equality only when all returns are identical).

---

## Geometric Mean Return

The compound periodic rate of growth. Accounts for the compounding effect of returns over multiple periods.

$$\bar{R}_G = \sqrt[n]{(1+R_1)(1+R_2)\cdots(1+R_n)} - 1$$

**LOS**: 1.b | **Key**: Better measure of actual investment performance than arithmetic mean. Always ≤ arithmetic mean.

---

## Harmonic Mean

A measure of central tendency calculated as the reciprocal of the arithmetic mean of reciprocals. Best used when data consists of rates and ratios.

$$\bar{X}_H = \frac{n}{\sum_{i=1}^{n} \frac{1}{X_i}}$$

**LOS**: 1.b | **Key application**: Dollar cost averaging, averaging P/E ratios. Always ≤ geometric mean.

---

## Money-Weighted Return (MWR)

The internal rate of return (IRR) of all cash flows in and out of a portfolio. Affected by the timing and size of cash flows.

**LOS**: 1.c | **Use**: Measures the investor's actual experience. | **See**: [[#Time-Weighted Return (TWR)]]

---

## Time-Weighted Return (TWR)

The compound rate of growth of $1 initially invested. Not affected by external cash flows.

$$TWR = (1+HPR_1)(1+HPR_2)\cdots(1+HPR_n) - 1$$

**LOS**: 1.c | **Use**: Measures the portfolio manager's skill (independent of client cash flow timing).

---

## Gross Return

The return earned by the investment manager before deduction of management and administrative fees. Trading expenses ARE included (deducted) in gross return.

**LOS**: 1.e | **Key**: Often used to evaluate manager skill because it excludes fees the manager doesn't control.

---

## Net Return

The return after deducting management and administrative fees from the gross return.

$$R_{\text{net}} = R_{\text{gross}} - \text{Management fees}$$

**LOS**: 1.e

---

## Real Return

The return adjusted for inflation. Measures the increase in purchasing power.

$$R_{\text{real}} = \frac{1 + R_{\text{nominal}}}{1 + \text{Inflation}} - 1$$

**LOS**: 1.e | **Approximation**: $R_{\text{real}} \approx R_{\text{nominal}} - \text{Inflation}$

---

## After-Tax Return

The return after accounting for taxes on investment income and gains.

$$R_{\text{after-tax}} = R_{\text{pretax}} \times (1 - \text{tax rate})$$

**LOS**: 1.e

---

## Leveraged Return

The return on an investment that is partially financed with borrowed capital. Amplifies both gains and losses.

$$R_L = R_p + \frac{V_B}{V_E}(R_p - r_D)$$

where $V_B$ = borrowed capital, $V_E$ = equity capital, $r_D$ = borrowing cost

**LOS**: 1.e | **Key**: Leverage increases return only when $R_p > r_D$. It amplifies BOTH gains and losses.

---

## Continuously Compounded Return

The natural logarithm of the gross return. Used in lognormal asset pricing models.

$$r_{cc} = \ln(1 + HPR) = \ln\left(\frac{S_1}{S_0}\right)$$

**LOS**: 1.d | **Key**: Always less than HPR for positive returns. Additive over time: $r_{0,T} = r_{0,1} + r_{1,2} + \cdots + r_{T-1,T}$

**Related**: [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|Lognormal Distribution]]
