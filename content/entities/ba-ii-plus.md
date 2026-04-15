---
title: BA II Plus Calculator
type: entity
category: instrument
created: 2026-04-09
updated: 2026-04-09
tags: [calculator, financial-calculator, texas-instruments]
---

# BA II Plus Calculator

**Type**: Financial calculator
**Manufacturer**: Texas Instruments
**Role**: Primary computation tool for CFA exam candidates

## Key Functions

| Key | Function |
|-----|----------|
| **N** | Number of periods |
| **I/Y** | Interest rate per period (%) |
| **PV** | Present value (cash flow at $t=0$) |
| **PMT** | Payment per period |
| **FV** | Future value |
| **CPT** | Compute unknown variable |
| **CF** | Cash flow worksheet (for IRR, NPV) |
| **IRR** | Internal rate of return |
| **2ND** | Access secondary functions |

## Sign Convention

- **Cash outflows** → negative (money you pay)
- **Cash inflows** → positive (money you receive)

## Common Operations

### TVM (Lump Sum, Annuity)

1. Clear: `2ND` → `CLR TVM`
2. Enter known variables (N, I/Y, PV, PMT, FV)
3. Press `CPT` then the unknown variable

### IRR / MWR (Cash Flow Method)

1. `CF` → enter cash flows ($CF_0$, $CF_1$, ...) with frequencies ($F_{01}$, ...)
2. Use `+/-` for negative cash flows
3. Press `IRR` → `CPT`

## Referenced In

- [[modules/quantitative-methods/m01-rates-and-returns/index|M01]] — MWR calculation
- [[modules/quantitative-methods/m02-time-value-of-money/index|M02]] — FV, PV, Annuity, Perpetuity
