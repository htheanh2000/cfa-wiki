---
title: "Glossary: M02 — Time Value of Money"
type: glossary
subject: quantitative-methods
module: M02
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, tvm, pv, fv, annuity]
---

# Glossary: M02 — Time Value of Money

**Module**: [[quantitative-methods/modules/m02-time-value-of-money/index|M02]]
**Formulas**: [[quantitative-methods/formulas/time-value-of-money|Formula Sheet]]

---

## Future Value (FV)

The amount to which a current deposit will grow over time when placed in an account paying compound interest.

$$FV = PV \times (1+r)^N$$

**LOS**: Pre.i | **Related**: [[#Present Value (PV)]]

---

## Present Value (PV)

Today's value of a cash flow that is to be received at some point in the future, discounted at the appropriate rate.

$$PV = \frac{FV}{(1+r)^N}$$

**LOS**: Pre.i | **Key**: The higher the discount rate, the lower the present value.

---

## Compounding

The process by which interest earned on an investment is reinvested, so that in subsequent periods, interest is earned on both the original principal and the accumulated interest.

**Types**: Annual, Semiannual, Quarterly, Monthly, Daily, [[#Continuous Compounding]]

**LOS**: Pre.i | **Key**: More frequent compounding → higher effective return.

---

## Simple Interest

Interest calculated only on the original principal amount, without reinvestment.

$$FV = PV \times (1 + r \times N)$$

**LOS**: Pre.i | **Contrast**: [[#Compounding]] includes reinvestment of interest.

---

## Continuous Compounding

Compounding that occurs an infinite number of times per year. The limiting case of periodic compounding.

$$FV = PV \times e^{r \times N}$$

**LOS**: Pre.i | **Related**: [[quantitative-methods/glossary/m01-rates-and-returns#Continuously Compounded Return|Continuously Compounded Return]]

---

## Effective Annual Rate (EAR)

The annualized rate of return that accounts for the effect of compounding within the year. Allows comparison of investments with different compounding frequencies.

$$EAR = \left(1 + \frac{r}{m}\right)^m - 1$$

**LOS**: Pre.i | **Key**: EAR > stated rate when compounding is more frequent than annual.

---

## Ordinary Annuity

A finite set of equal cash flows occurring at the **end** of each period.

$$PV = PMT \times \frac{1-(1+r)^{-N}}{r} \qquad FV = PMT \times \frac{(1+r)^N - 1}{r}$$

**LOS**: Pre.i | **Contrast**: [[#Annuity Due]]

---

## Annuity Due

A finite set of equal cash flows occurring at the **beginning** of each period.

$$FV_{\text{due}} = FV_{\text{ordinary}} \times (1+r) \qquad PV_{\text{due}} = PV_{\text{ordinary}} \times (1+r)$$

**LOS**: Pre.i | **Key**: Cash flows are one period earlier than ordinary annuity → multiply by $(1+r)$.

---

## Perpetuity

A never-ending series of equal cash flows, with the first payment occurring one period from now.

$$PV_0 = \frac{PMT_1}{r}$$

**LOS**: Pre.i | **Example**: Preferred stock with fixed dividend forever.

---

## Growing Perpetuity

A perpetuity where cash flows grow at a constant rate $g$ indefinitely.

$$PV_0 = \frac{D_1}{r - g}$$

**LOS**: 2.b | **Requirement**: $r > g$ | **Use**: Gordon Growth Model for stock valuation.

---

## Yield to Maturity (YTM)

The discount rate that makes the present value of a bond's cash flows equal to its market price. The bond's internal rate of return.

**LOS**: 2.a | **Key**: If price < par → YTM > coupon rate (discount bond). If price > par → YTM < coupon rate (premium bond).

---

## Cash Flow Additivity

The principle that the present value of any set of cash flows equals the sum of the present values of each individual cash flow. Ensures no arbitrage in financial markets.

**LOS**: 2.c | **Applications**: Implied forward rates, forward exchange rates, option pricing.

---

## Implied Forward Rate

The future interest rate that can be locked in today, derived from the relationship between spot rates of different maturities using [[#Cash Flow Additivity]].

$$F_{1,1} = \frac{(1+r_2)^2}{(1+r_1)} - 1$$

**LOS**: 2.c | **Use**: Breakeven reinvestment rate between short-term and long-term bonds.

---

## No-Arbitrage Condition

The principle that identical cash flows must have identical prices. If violated, risk-free profits are possible, and market forces will quickly eliminate the opportunity.

**LOS**: 2.c | **Applications**: Forward exchange rates, option pricing (put-call parity).
