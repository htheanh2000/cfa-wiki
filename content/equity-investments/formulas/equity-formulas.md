---
title: Equity Investments — Formula Sheet
type: formula
subject: equity-investments
module: M01-M08
los: ["1.a-1.l", "2.a-2.k", "3.a-3.g", "4.a-4.h", "5.a-5.e", "6.a-6.e", "7.a-7.c", "8.a-8.e"]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, formulas, DDM, gordon-growth, leverage, margin, valuation, multiples]
---

# Equity Investments — Formula Sheet

---

## M01: Market Organization and Structure

### Leverage Ratio

$$\text{Leverage Ratio} = \frac{\text{Asset Value}}{\text{Equity Value}} = \frac{1}{\text{Margin Percentage}}$$

where Margin Percentage = Initial Margin / Asset Value.

### Margin Return (Return on Leveraged Position)

**Long position**:

$$r_{\text{margin}} = \frac{P_1 - P_0 + D - \text{Interest on Borrowed Funds}}{P_0 \times \text{Initial Margin \%}}$$

where:
- $P_0$ = purchase price
- $P_1$ = selling price
- $D$ = dividends received
- Initial Margin % = equity as fraction of total position

**Short position**:

$$r_{\text{short}} = \frac{P_0 - P_1 - D - \text{Interest on Borrowed Shares}}{P_0 \times \text{Initial Margin \%}}$$

### Margin Call Price

**Long position** — margin call triggered when equity falls to maintenance margin:

$$P_{\text{margin call}} = P_0 \times \frac{1 - \text{Initial Margin \%}}{1 - \text{Maintenance Margin \%}}$$

where:
- $P_0$ = original purchase price
- Initial Margin % = fraction of equity deposited initially
- Maintenance Margin % = minimum equity fraction before margin call

**Short position**:

$$P_{\text{margin call}} = P_0 \times \frac{1 + \text{Initial Margin \%}}{1 + \text{Maintenance Margin \%}}$$

---

## M02: Security Market Indexes

### Price Return Index

$$\text{Price Return} = \frac{V_1 - V_0}{V_0}$$

$$\text{Price Return Index}_t = \text{Index}_{t-1} \times (1 + \text{PR}_t)$$

where $V$ = index value, $\text{PR}$ = price return for the period.

### Total Return Index

$$\text{Total Return Index}_t = \text{Total Return Index}_{t-1} \times (1 + \text{TR}_t)$$

where:

$$\text{TR}_t = \frac{V_1 - V_0 + \text{Income}_t}{V_0}$$

$\text{Income}_t$ includes dividends, interest, and other distributions.

### Price-Weighted Index Return

$$R = \frac{\sum_{i=1}^{N} P_{i,1} - \sum_{i=1}^{N} P_{i,0}}{\sum_{i=1}^{N} P_{i,0}}$$

where $P_{i,t}$ = price of stock $i$ at time $t$, $N$ = number of stocks.

### Market-Cap-Weighted Index Return

$$R = \frac{\sum_{i=1}^{N} w_i \times R_i}{\sum_{i=1}^{N} w_i}$$

where $w_i = P_i \times Q_i$ (market cap weight).

---

## M04: Overview of Equity Securities

### Book Value per Share

$$\text{BVPS} = \frac{\text{Total Shareholders' Equity} - \text{Preferred Equity}}{\text{Common Shares Outstanding}}$$

### Return on Equity (ROE)

$$\text{ROE} = \frac{\text{Net Income}}{\text{Average Total Equity}}$$

### DuPont Decomposition (3-factor)

$$\text{ROE} = \underbrace{\frac{\text{Net Income}}{\text{Revenue}}}_{\text{Profit Margin}} \times \underbrace{\frac{\text{Revenue}}{\text{Total Assets}}}_{\text{Asset Turnover}} \times \underbrace{\frac{\text{Total Assets}}{\text{Equity}}}_{\text{Financial Leverage}}$$

---

## M05: Company Analysis — Past and Present

### Gross Margin

$$\text{Gross Margin} = \frac{\text{Revenue} - \text{COGS}}{\text{Revenue}}$$

### Operating Margin

$$\text{Operating Margin} = \frac{\text{Operating Income}}{\text{Revenue}}$$

### EBITDA Margin

$$\text{EBITDA Margin} = \frac{\text{EBITDA}}{\text{Revenue}}$$

### Cash Conversion Cycle

$$\text{CCC} = \text{DSO} + \text{DIO} - \text{DPO}$$

where:
- $\text{DSO} = \frac{\text{Accounts Receivable}}{\text{Revenue}} \times 365$
- $\text{DIO} = \frac{\text{Inventory}}{\text{COGS}} \times 365$
- $\text{DPO} = \frac{\text{Accounts Payable}}{\text{COGS}} \times 365$

### Return on Invested Capital (ROIC)

$$\text{ROIC} = \frac{\text{NOPAT}}{\text{Invested Capital}}$$

where $\text{NOPAT} = \text{EBIT} \times (1 - \text{Tax Rate})$ and $\text{Invested Capital} = \text{Debt} + \text{Equity} - \text{Cash}$.

---

## M07: Company Analysis — Forecasting

### Degree of Operating Leverage (DOL)

$$\text{DOL} = \frac{\%\Delta \text{Operating Income}}{\%\Delta \text{Revenue}}$$

### Sustainable Growth Rate

$$g = \text{ROE} \times b$$

where $b$ = retention ratio = $1 - \text{Payout Ratio}$.

---

## M08: Equity Valuation — Concepts and Basic Tools

### Gordon Growth Model (GGM)

$$\boxed{V_0 = \frac{D_1}{r - g}}$$

where:
- $D_1 = D_0 \times (1 + g)$ = expected next dividend
- $r$ = required rate of return (must be $> g$)
- $g$ = constant dividend growth rate

### Implied Required Return (from GGM)

$$r = \frac{D_1}{P_0} + g = \text{Dividend Yield} + \text{Capital Gains Yield}$$

### One-Period DDM

$$V_0 = \frac{D_1 + P_1}{1 + r}$$

### Multi-Period DDM

$$V_0 = \sum_{t=1}^{n} \frac{D_t}{(1+r)^t} + \frac{P_n}{(1+r)^n}$$

### Price-to-Earnings (P/E)

**Trailing P/E**:

$$\text{Trailing P/E} = \frac{P_0}{E_0}$$

**Leading (Forward) P/E**:

$$\text{Leading P/E} = \frac{P_0}{E_1}$$

**Justified Leading P/E (from GGM)**:

$$\frac{P_0}{E_1} = \frac{1 - b}{r - g}$$

where $(1 - b)$ = dividend payout ratio.

### Price-to-Book (P/B)

$$\text{P/B} = \frac{P_0}{\text{BVPS}}$$

**Justified P/B**:

$$\frac{P_0}{B_0} = \frac{\text{ROE} - g}{r - g}$$

### Price-to-Sales (P/S)

$$\text{P/S} = \frac{P_0}{\text{Sales per Share}}$$

### Price-to-Cash Flow (P/CF)

$$\text{P/CF} = \frac{P_0}{\text{Cash Flow per Share}}$$

### Enterprise Value (EV)

$$\text{EV} = \text{Market Cap} + \text{Total Debt} - \text{Cash \& Equivalents}$$

### EV/EBITDA

$$\text{EV/EBITDA} = \frac{\text{Enterprise Value}}{\text{EBITDA}}$$

### Net Asset Value (NAV)

$$\text{NAV per Share} = \frac{\text{Market Value of Assets} - \text{Market Value of Liabilities}}{\text{Shares Outstanding}}$$

---

## Quick Reference Table

| Formula | Module | Key Variables |
|---------|--------|---------------|
| Leverage Ratio = $1 / \text{Margin \%}$ | M01 | Margin percentage |
| Margin Call (Long) = $P_0 \times \frac{1 - IM}{1 - MM}$ | M01 | Initial/maintenance margin |
| Total Return = $\frac{V_1 - V_0 + \text{Inc}}{V_0}$ | M02 | Price change + income |
| ROE = Net Income / Equity | M04 | Profitability |
| BVPS = (Equity - Pref) / Shares | M04 | Book value |
| CCC = DSO + DIO - DPO | M05 | Working capital efficiency |
| GGM: $V_0 = D_1/(r-g)$ | M08 | Dividend, return, growth |
| Justified P/E = $(1-b)/(r-g)$ | M08 | Payout, return, growth |
| EV = MCap + Debt - Cash | M08 | Enterprise value |

---

## Related Pages

- [[equity-investments/modules/m01-market-organization/index|M01: Market Organization and Structure]]
- [[equity-investments/modules/m02-security-market-indexes/index|M02: Security Market Indexes]]
- [[equity-investments/modules/m04-equity-securities-overview/index|M04: Overview of Equity Securities]]
- [[equity-investments/modules/m05-company-analysis-past/index|M05: Company Analysis — Past and Present]]
- [[equity-investments/modules/m08-equity-valuation/index|M08: Equity Valuation]]
