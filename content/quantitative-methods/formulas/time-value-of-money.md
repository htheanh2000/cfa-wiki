---
title: "Formulas: Time Value of Money"
type: formula
subject: quantitative-methods
module: M02
created: 2026-04-09
updated: 2026-04-09
tags: [formulas, tvm, pv, fv, annuity, perpetuity]
---

# Formulas: Time Value of Money

**Module**: [[quantitative-methods/modules/m02-time-value-of-money/index|M02]]

## Future Value — Lump Sum

**Annual compounding:**
$$FV = PV \times (1 + r)^N$$

**Periodic compounding** ($m$ times/year):
$$FV = PV \times \left(1 + \frac{r}{m}\right)^{N \times m}$$

**Continuous compounding:**
$$FV = PV \times e^{r \times N}$$

## Present Value — Lump Sum

**Annual:**
$$PV = \frac{FV}{(1 + r)^N}$$

**Periodic:**
$$PV = \frac{FV}{\left(1 + \frac{r}{m}\right)^{N \times m}}$$

**Continuous:**
$$PV = \frac{FV}{e^{r \times N}}$$

## Ordinary Annuity

**Future Value:**
$$FV = PMT \times \frac{(1+r)^N - 1}{r}$$

**Present Value:**
$$PV = PMT \times \frac{1 - (1+r)^{-N}}{r}$$

## Annuity Due

$$FV_{\text{due}} = FV_{\text{ordinary}} \times (1+r)$$

$$PV_{\text{due}} = PV_{\text{ordinary}} \times (1+r)$$

## Perpetuity

**Standard** (first payment at $t=1$):
$$PV_0 = \frac{PMT_1}{r}$$

**Deferred** (first payment at year $n$):
$$PV_0 = \frac{PMT}{r} \times \frac{1}{(1+r)^{n-1}}$$

## Growing Perpetuity

$$PV_0 = \frac{PMT_1}{r - g}$$

where $g$ = constant growth rate, requires $r > g$

## Effective Annual Rate (EAR)

**From periodic rate:**
$$EAR = \left(1 + \frac{r}{m}\right)^m - 1$$

**From continuous rate:**
$$EAR = e^r - 1$$

## Continuously Compounded Return

$$r_{cc} = \ln(1 + HPR) = \ln\left(\frac{P_1}{P_0}\right)$$
