---
title: Fixed Income — Master Formula Sheet
type: formula
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [bond-pricing, duration, convexity, yield, credit, spreads, forward-rates]
---

# Fixed Income — Master Formula Sheet

---

## 1. Bond Pricing

**Present Value of a Bond:**

$$PV = \sum_{t=1}^{n} \frac{PMT}{(1+r)^t} + \frac{FV}{(1+r)^n}$$

where $PMT$ = coupon payment, $FV$ = face value, $r$ = market discount rate per period, $n$ = number of periods.

---

## 2. Current Yield

$$\text{Current Yield} = \frac{\text{Annual Coupon}}{\text{Bond Price}}$$

---

## 3. Accrued Interest

$$AI = PMT \times \frac{t}{T}$$

where $t$ = days since last coupon, $T$ = days in coupon period.

---

## 4. Full Price and Flat Price

$$\text{Full Price} = \text{Flat Price} + AI$$

**Full price between coupon dates:**

$$PV^{\text{Full}} = PV \times (1 + r)^{t/T}$$

where $PV$ = value at last coupon date, $t/T$ = fraction of period elapsed.

---

## 5. Effective Annual Rate (EAR)

$$EAR = \left(1 + \frac{APR}{n}\right)^n - 1$$

where $n$ = compounding periods per year.

---

## 6. APR Conversion Between Periodicities

$$\left(1 + \frac{APR_m}{m}\right)^m = \left(1 + \frac{APR_n}{n}\right)^n$$

---

## 7. Yield Spreads

**G-Spread:**

$$G\text{-spread} = YTM_{\text{bond}} - YTM_{\text{govt}}$$

**Z-Spread (zero-volatility spread):**

$$PV = \sum_{t=1}^{n} \frac{CF_t}{(1 + S_t + Z)^t}$$

where $S_t$ = spot rate for period $t$, $Z$ = Z-spread (solve for $Z$).

**OAS (Option-Adjusted Spread):**

$$OAS = Z\text{-spread} - \text{Option Value (in spread terms)}$$

---

## 8. Forward Rates

**Forward rate from spot rates:**

$$(1 + S_n)^n = (1 + S_1)(1 + f_{1,1})(1 + f_{2,1}) \cdots (1 + f_{n-1,1})$$

**General relationship:**

$$(1 + S_{A+B})^{A+B} = (1 + S_A)^A \times (1 + f_{A,B})^B$$

**Solving for a forward rate:**

$$f_{A,B} = \left[\frac{(1 + S_{A+B})^{A+B}}{(1 + S_A)^A}\right]^{1/B} - 1$$

---

## 9. Macaulay Duration

$$\text{MacDur} = \frac{\sum_{t=1}^{n} t \times PV(CF_t)}{PV}$$

---

## 10. Modified Duration

$$\text{ModDur} = \frac{\text{MacDur}}{1 + r}$$

**Price change approximation:**

$$\%\Delta PV \approx -\text{ModDur} \times \Delta \text{Yield}$$

---

## 11. Approximate Modified Duration

$$\text{ApproxModDur} = \frac{PV_{-} - PV_{+}}{2 \times PV_0 \times \Delta \text{Yield}}$$

---

## 12. Money Duration (Dollar Duration)

$$\text{MoneyDur} = \text{ModDur} \times PV^{\text{Full}}$$

$$\Delta PV \approx -\text{MoneyDur} \times \Delta \text{Yield}$$

---

## 13. PVBP (Price Value of a Basis Point)

$$PVBP = \frac{PV_{-} - PV_{+}}{2}$$

where $PV_{\pm}$ = prices after ±1 bp yield change.

---

## 14. Approximate Convexity

$$\text{ApproxCon} = \frac{PV_{-} + PV_{+} - 2 \times PV_0}{\Delta \text{Yield}^2 \times PV_0}$$

---

## 15. Price Change with Duration and Convexity

$$\%\Delta PV \approx (-\text{ModDur} \times \Delta \text{Yield}) + \left(\frac{1}{2} \times \text{Convexity} \times \Delta \text{Yield}^2\right)$$

---

## 16. Effective Duration

$$\text{EffDur} = \frac{PV_{-} - PV_{+}}{2 \times PV_0 \times \Delta \text{Curve}}$$

For bonds with embedded options; uses benchmark curve shift.

---

## 17. Effective Convexity

$$\text{EffCon} = \frac{PV_{-} + PV_{+} - 2 \times PV_0}{\Delta \text{Curve}^2 \times PV_0}$$

---

## 18. Key Rate Duration

$$\text{KeyRateDur}_k = \frac{-1}{PV} \times \frac{\Delta PV}{\Delta r_k}$$

where $\Delta r_k$ = change in the spot rate at maturity $k$ only.

---

## 19. Credit Risk

**Expected Loss:**

$$\text{Expected Loss} = POD \times LGD \times \text{Exposure}$$

**Loss Given Default:**

$$LGD = 1 - \text{Recovery Rate}$$

---

## 20. FRN Discount Margin

The discount margin (DM) is the spread over the reference rate such that the FRN's price equals its market value:

$$PV = \frac{(QM + R) \times FV/m}{(1 + \frac{R + DM}{m})^1} + \frac{(QM + R) \times FV/m}{(1 + \frac{R + DM}{m})^2} + \cdots + \frac{(QM + R) \times FV/m + FV}{(1 + \frac{R + DM}{m})^N}$$

where $QM$ = quoted margin, $R$ = reference rate, $DM$ = discount margin, $m$ = periods per year.

- If $DM > QM$: FRN trades at a **discount**
- If $DM < QM$: FRN trades at a **premium**
- If $DM = QM$: FRN trades at **par**

---

## 21. Money Market Yields

**Bank Discount Yield:**

$$r_{BD} = \frac{D}{FV} \times \frac{360}{\text{Days}}$$

**Money Market Yield:**

$$r_{MM} = \frac{D}{PV} \times \frac{360}{\text{Days}}$$

**Bond Equivalent Yield:**

$$r_{BEY} = \frac{D}{PV} \times \frac{365}{\text{Days}}$$

where $D = FV - PV$.

**Conversion:**

$$r_{MM} = r_{BD} \times \frac{FV}{PV} = \frac{r_{BD}}{1 - r_{BD} \times \frac{\text{Days}}{360}}$$

---

## 22. Portfolio Duration

$$D_{\text{portfolio}} = \sum_{i=1}^{n} w_i \times D_i$$

where $w_i$ = market value weight of bond $i$.

---

## Related Pages

- [[fixed-income/concepts/bond-valuation|Bond Valuation]]
- [[fixed-income/concepts/duration|Duration]]
- [[fixed-income/concepts/convexity|Convexity]]
- [[fixed-income/concepts/yield-measures|Yield Measures]]
- [[fixed-income/concepts/yield-spreads|Yield Spreads]]
- [[fixed-income/concepts/term-structure|Term Structure]]
- [[fixed-income/concepts/credit-risk|Credit Risk]]
