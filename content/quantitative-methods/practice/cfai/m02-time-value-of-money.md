---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - time-value-of-money
source: "CFAI CFA1 Quant Practice 2026, pp.81-86"
module: "[[m02-time-value-of-money]]"
---

# M02 – Time Value of Money: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.81–86
**Back to module:** [[m02-time-value-of-money]]
**Glossary**: [[quantitative-methods/glossary/m02-time-value-of-money|M02 Terms]]

---

## Question 1

Grupo Ignacia issued 10-year corporate bonds 2 years ago with a coupon rate of 10.7% paid semiannually. Current [[quantitative-methods/glossary/m02-time-value-of-money#Yield to Maturity (YTM)|yield-to-maturity]] is 11.6%. The current price per MXN 100 par value is **closest to**:

- A. MXN 95.47
- B. MXN 97.18
- C. MXN 95.39

> [!answer]- Answer
> **C. MXN 95.39**
>
> The bond was issued 10 years ago but is now 2 years old, so it has **8 years remaining** (16 semiannual periods).
>
> Calculator inputs:
> - $N = 16$ (periods)
> - $I/Y = 5.8\%$ (= 11.6% / 2)
> - $PMT = 5.35$ (= 10.7 / 2)
> - $FV = 100$
>
> $$PV = \frac{5.35}{\left(1.058\right)^1} + \frac{5.35}{\left(1.058\right)^2} + \cdots + \frac{105.35}{\left(1.058\right)^{16}} = \text{MXN } 95.39$$
>
> The bond trades at a **discount** because the coupon rate (10.7%) is below the current YTM (11.6%).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Giá trái phiếu = PV của tất cả coupon payments + PV của face value, chiết khấu theo [[quantitative-methods/glossary/m02-time-value-of-money#Yield to Maturity (YTM)|YTM]]. Khi YTM > coupon rate → bond discount (giá < par). Khi YTM < coupon rate → bond premium (giá > par).
>
> **Tại sao C đúng:** Trái phiếu phát hành 10 năm, nay 2 tuổi → còn 8 năm = 16 kỳ semiannual. PMT = 10.7/2 = 5.35; I/Y = 11.6/2 = 5.8%; FV = 100. Giá ≈ 95.39 < 100 (discount) vì YTM 11.6% > coupon 10.7% — thị trường đang yêu cầu lợi suất cao hơn mức coupon trả.
>
> **Tại sao A sai (95.47):** Có thể do dùng sai số kỳ — ví dụ tính 10 năm thay vì 8 năm còn lại.
> **Tại sao B sai (97.18):** Có thể do dùng YTM hàng năm thay vì chia đôi cho semiannual, hoặc số kỳ sai.

---

## Question 2

Grey Pebble Real Estate takes a 5-year mortgage on 75% of a NZD 5,000,000 property at an annual interest rate of 4.8%, with monthly payments.

The monthly payment is **closest to**:

- A. NZD 70,424
- B. NZD 93,899
- C. NZD 71,781

> [!answer]- Answer
> **A. NZD 70,424**
>
> - Loan amount: $PV = 0.75 \times 5{,}000{,}000 = \text{NZD } 3{,}750{,}000$
> - Monthly rate: $r = 4.8\% / 12 = 0.4\%$
> - Number of periods: $n = 5 \times 12 = 60$
>
> $$PMT = \frac{PV \cdot r}{1 - (1+r)^{-n}} = \frac{3{,}750{,}000 \times 0.004}{1 - (1.004)^{-60}}$$
>
> $$PMT = \frac{15{,}000}{1 - 0.78715} = \frac{15{,}000}{0.21285} \approx \text{NZD } 70{,}424$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Công thức mortgage payment: $PMT = \frac{PV \cdot r}{1-(1+r)^{-n}}$. Đây là annuity payment — mỗi kỳ trả một khoản cố định bao gồm cả gốc lẫn lãi. Lưu ý phải convert lãi suất năm sang lãi suất tháng và số năm sang số tháng.
>
> **Tại sao A đúng:** Khoản vay = 75% × 5,000,000 = NZD 3,750,000. Lãi tháng = 4.8%/12 = 0.4%. Số kỳ = 60. Tử số = 3,750,000 × 0.004 = 15,000. Mẫu số = 1 − (1.004)⁻⁶⁰ ≈ 0.2128. PMT ≈ 70,424.
>
> **Tại sao B sai (93,899):** Có thể do dùng lãi suất năm 4.8% thay vì tháng 0.4%, hoặc n = 5 thay vì 60.
> **Tại sao C sai (71,781):** Gần đúng nhưng có thể phát sinh từ sai số làm tròn hoặc dùng lãi suất tháng sai (ví dụ 4.8%/12 tính không chính xác).

---

## Question 3

Mylandia Corp just paid a dividend of CAD 2.40. Dividends are expected to grow at a constant 3% per year. The required rate of return is 8%.

The current share price is **closest to**:

- A. CAD 48.00
- B. CAD 49.44
- C. CAD 51.84

> [!answer]- Answer
> **B. CAD 49.44**
>
> Using the Gordon Growth Model (constant dividend discount model):
> $$P_0 = \frac{D_1}{r - g} = \frac{D_0 \times (1+g)}{r - g}$$
>
> $$P_0 = \frac{2.40 \times 1.03}{0.08 - 0.03} = \frac{2.472}{0.05} = \text{CAD } 49.44$$
>
> Note: $D_0 = \text{CAD } 2.40$ is the **just-paid** dividend, so the next dividend $D_1 = 2.40 \times 1.03 = 2.472$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Gordon Growth Model (GGM): $P_0 = \frac{D_1}{r-g}$, trong đó $D_1$ là dividend **kỳ tới** (chưa trả). Bẫy phổ biến: dùng $D_0$ (vừa trả) thay vì $D_1$ → understate giá trị. Mô hình này là [[quantitative-methods/glossary/m02-time-value-of-money#Growing Perpetuity|growing perpetuity]] — chuỗi dòng tiền tăng trưởng mãi mãi.
>
> **Tại sao B đúng:** $D_0 = 2.40$ đã được trả. $D_1 = 2.40 \times 1.03 = 2.472$. $P_0 = 2.472 / (0.08 - 0.03) = 2.472 / 0.05 = 49.44$.
>
> **Tại sao A sai (48.00):** Dùng $D_0$ thay vì $D_1$: $2.40 / 0.05 = 48.00$ — bẫy cổ điển của GGM. Nhà đầu tư mua hôm nay sẽ nhận $D_1$, không phải $D_0$ đã trả rồi.
> **Tại sao C sai (51.84):** Có thể nhầm tăng trưởng 2 kỳ: $2.40 \times 1.03^2 / 0.05 = 51.84$ — áp dụng growth factor hai lần.

---

## Question 4

Mylandia Corp revises its dividend forecast: dividends will grow at 10% for 3 years, then revert to a [[quantitative-methods/glossary/m02-time-value-of-money#Growing Perpetuity|perpetual growth rate]] of 3%. The required return remains 8%.

The current share price is **closest to**:

- A. CAD 49.98
- B. CAD 55.84
- C. CAD 59.71

> [!answer]- Answer
> **C. CAD 59.71**
>
> **Stage 1 – Dividends during high-growth period** (using $D_0 = \text{CAD } 2.40$):
>
> | Year | Dividend |
> |------|----------|
> | $D_1$ | $2.40 \times 1.10 = 2.6400$ |
> | $D_2$ | $2.64 \times 1.10 = 2.9040$ |
> | $D_3$ | $2.904 \times 1.10 = 3.1944$ |
>
> **Stage 2 – Terminal value at end of Year 3:**
> $$D_4 = 3.1944 \times 1.03 = 3.2902$$
> $$P_3 = \frac{D_4}{r - g} = \frac{3.2902}{0.08 - 0.03} = \frac{3.2902}{0.05} = 65.804$$
>
> **Present value of all cash flows:**
> $$P_0 = \frac{2.64}{1.08} + \frac{2.904}{1.08^2} + \frac{3.1944 + 65.804}{1.08^3}$$
>
> $$P_0 = 2.444 + 2.490 + \frac{68.998}{1.2597} = 2.444 + 2.490 + 54.773 \approx \text{CAD } 59.71$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Multi-stage dividend discount model: chia làm 2 giai đoạn — high growth rồi stable growth. Terminal value tại cuối giai đoạn 1 = $P_3 = D_4/(r-g_{stable})$. Sau đó discount tất cả cash flows về hiện tại.
>
> **Tại sao C đúng:** Logic gồm 3 phần: (1) PV của $D_1, D_2, D_3$ trong giai đoạn tăng trưởng cao 10%; (2) Terminal value $P_3 = D_4/(r-g) = 3.2902/0.05 = 65.80$ tại năm 3; (3) PV tổng = 2.44 + 2.49 + (3.19 + 65.80)/1.08³ ≈ 59.71. Phần lớn giá trị (54.77/59.71 = 92%) đến từ terminal value — điển hình cho growth stocks.
>
> **Tại sao A sai (49.98):** Gần với giá tính theo constant growth (câu 3 = 49.44) — có thể không áp dụng high-growth phase hoặc dùng sai $g$.
> **Tại sao B sai (55.84):** Có thể sai ở bước tính $D_4$ hoặc discount sai số kỳ cho terminal value.

---

## Question 5

A Swiss zero-coupon bond has a face value of CHF 100, matures in 12 years, and currently trades at CHF 89. In 3 years, the same bond is expected to trade at CHF 95.25.

The **annualized return** over the 3-year holding period is **closest to**:

- A. 0.58%
- B. 1.64%
- C. 2.29%

> [!answer]- Answer
> **C. 2.29%**
>
> The annualized holding-period return over 3 years:
>
> $$r = \left(\frac{P_3}{P_0}\right)^{1/3} - 1 = \left(\frac{95.25}{89}\right)^{1/3} - 1$$
>
> $$r = (1.07022)^{0.3333} - 1 = 1.02292 - 1 \approx 2.29\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Annualized return từ holding period bất kỳ: $r = (P_t/P_0)^{1/t} - 1$, trong đó $t$ là số năm. Đây là bài tính return của zero-coupon bond — không có coupon nên toàn bộ return đến từ price appreciation.
>
> **Tại sao C đúng:** Mua tại 89, kỳ vọng bán tại 95.25 sau 3 năm. $r = (95.25/89)^{1/3} - 1 = 1.0702^{0.333} - 1 ≈ 2.29\%$ mỗi năm. Đây là annualized HPR trong 3 năm, không phải YTM đến maturity.
>
> **Tại sao A sai (0.58%):** Có thể là simple return chia đều: $(95.25-89)/89/3 ≈ 2.34\%$ không phải 0.58%, hoặc phát sinh từ lỗi tính toán khác.
> **Tại sao B sai (1.64%):** Có thể do nhầm holding period (ví dụ dùng 4 năm thay vì 3 năm) hoặc tính $r = (P_t/P_0)^{1/t}$ sai exponent.

---

## Question 6

The Grupo Ignacia bonds from Q1 are now 4 years old (6 years remaining). The current market price is MXN 97.50 per MXN 100 par. The coupon remains 10.7% paid semiannually.

The [[quantitative-methods/glossary/m02-time-value-of-money#Yield to Maturity (YTM)|yield-to-maturity]] is **closest to**:

- A. 11.28%
- B. 11.50%
- C. 11.71%

> [!answer]- Answer
> **A. 11.28%**
>
> Calculator inputs (solving for $I/Y$):
> - $N = 12$ (6 years × 2)
> - $PV = -97.50$
> - $PMT = 5.35$ (= 10.7 / 2)
> - $FV = 100$
>
> Solving: Semiannual rate $\approx 5.64\%$
>
> Annual YTM $= 5.64\% \times 2 = \mathbf{11.28\%}$
>
> The bond trades at a slight discount (97.50 < 100), so the YTM must be marginally above the coupon rate of 10.7%, confirming ~11.28%.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Yield to Maturity (YTM)|YTM]] là lãi suất chiết khấu làm cho PV của tất cả cash flows bằng giá thị trường. Khi giải YTM, cần input: N (kỳ số), PV (giá âm), PMT (coupon), FV (mệnh giá) → tìm I/Y. Với semiannual bond, YTM = 2 × semiannual rate.
>
> **Tại sao A đúng:** N = 12 (6 năm × 2), PV = −97.50, PMT = 5.35, FV = 100. Giải ra semiannual rate ≈ 5.64% → YTM = 11.28%. Kiểm tra logic: giá 97.50 < 100 (discount) nên YTM > coupon rate 10.7% ✓.
>
> **Tại sao B sai (11.50%):** YTM này tương ứng với giá thấp hơn 97.50 — nếu YTM cao hơn thì giá phải thấp hơn, không phải 97.50.
> **Tại sao C sai (11.71%):** Tương tự B — YTM càng cao thì giá càng thấp; 11.71% sẽ cho giá dưới 97.50.

---

## Question 7

Mylandia stock currently trades at CAD 60.00. The company just paid a dividend of CAD 2.40, and dividends are expected to grow [[quantitative-methods/glossary/m02-time-value-of-money#Perpetuity|perpetually]] at 3%.

The required rate of return is **closest to**:

- A. 8.00%
- B. 7.00%
- C. 7.12%

> [!answer]- Answer
> **C. 7.12%**
>
> Rearranging the Gordon Growth Model to solve for $r$:
>
> $$P_0 = \frac{D_1}{r - g} \implies r = \frac{D_1}{P_0} + g$$
>
> $$D_1 = D_0 \times (1 + g) = 2.40 \times 1.03 = 2.472$$
>
> $$r = \frac{2.472}{60.00} + 0.03 = 0.0412 + 0.03 = 0.0712 = 7.12\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> GGM giải ngược để tìm implied required return: $r = D_1/P_0 + g$. Thành phần $D_1/P_0$ là dividend yield kỳ vọng, cộng với $g$ (tốc độ tăng trưởng kỳ vọng) = total return. Đây là cách thị trường "định giá" required return qua mức giá hiện tại.
>
> **Tại sao C đúng:** $D_1 = 2.40 \times 1.03 = 2.472$. Dividend yield = 2.472/60 = 4.12%. Required return = 4.12% + 3% = 7.12%. Lưu ý: dùng $D_1$ không phải $D_0$ — nhà đầu tư mua hôm nay nhận dividend kỳ sau.
>
> **Tại sao A sai (8.00%):** 8% là required return từ câu 3 — nhưng bây giờ giá cổ phiếu đã tăng từ 49.44 lên 60.00, nên required return implied thấp xuống còn 7.12%.
> **Tại sao B sai (7.00%):** Gần đúng nhưng có thể do dùng $D_0$ thay vì $D_1$: $2.40/60 + 3\% = 7.00\%$ — bẫy cổ điển tương tự câu 3.

---

## Question 8

The NIFTY 50 index has a forward price-to-earnings (P/E) ratio of 15. Expected payout ratio is 50%, required return is 7.5%, and expected dividend growth is 4.5%.

An analyst should view the NIFTY 50 as:

- A. Overpriced
- B. Underpriced
- C. Fairly priced

> [!answer]- Answer
> **B. Underpriced**
>
> The fair (justified) forward P/E based on fundamentals:
>
> $$\text{Justified P/E} = \frac{\text{Payout ratio}}{r - g} = \frac{0.50}{0.075 - 0.045} = \frac{0.50}{0.03} = 16.67$$
>
> The current forward P/E of **15 < 16.67** (fair value), meaning the market is pricing the index below its intrinsic value. Therefore, the NIFTY 50 is **underpriced**.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Justified (fair value) forward P/E = Payout ratio / (r − g). Đây là ứng dụng trực tiếp của GGM: $P_0/E_1 = (D_1/E_1)/(r-g)$ = payout ratio / (r − g). So sánh P/E thị trường với P/E justified để xác định over/underpriced.
>
> **Tại sao B đúng:** Justified P/E = 0.50 / (0.075 − 0.045) = 0.50 / 0.03 = 16.67. Thị trường đang trade tại P/E = 15 < 16.67 → thị trường rẻ hơn giá trị nội tại → underpriced. Nếu mua ở P/E 15 khi fair value là 16.67, kỳ vọng capital gain khi thị trường về fair value.
>
> **Tại sao A sai:** Overpriced nghĩa là P/E thị trường > justified P/E. Ngược lại với tình huống này.
> **Tại sao C sai:** Fairly priced nghĩa là P/E thị trường = justified P/E = 16.67. Nhưng 15 ≠ 16.67.

---

## Question 9

An investor requires an 8% return and has USD 500,000 to invest. Two opportunities are available:

| Period | Opportunity 1 Cash Flows | Opportunity 2 Cash Flows |
|--------|--------------------------|--------------------------|
| 0 | −500,000 | −500,000 |
| 1 | 195,000 | 225,000 |
| 2 | 195,000 | 195,000 |
| 3 | 195,000 | 160,008 |

The investor should:

- A. Prefer Opportunity 1
- B. Prefer Opportunity 2
- C. Be indifferent between the two

> [!answer]- Answer
> **C. Be indifferent between the two**
>
> Using the **[[quantitative-methods/glossary/m02-time-value-of-money#Cash Flow Additivity|cash flow additivity]] principle**, consider the difference between Opportunity 2 and Opportunity 1:
>
> | Period | Difference (Opp 2 − Opp 1) |
> |--------|---------------------------|
> | 0 | 0 |
> | 1 | +30,000 |
> | 2 | 0 |
> | 3 | −34,992 |
>
> PV of difference at 8%:
> $$\frac{30{,}000}{1.08} + 0 + \frac{-34{,}992}{1.08^3} = 27{,}778 - 27{,}778 = 0$$
>
> The PV of the difference stream is exactly zero at 8%, confirming both opportunities are **economically identical** — the investor is indifferent.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Cash Flow Additivity|Cash flow additivity principle]]: nếu PV(A) = PV(B) tại cùng discount rate, thì A và B có giá trị kinh tế như nhau. Có thể kiểm tra bằng cách tính PV của difference stream (A − B).
>
> **Tại sao C đúng:** Opportunity 2 trả thêm $30,000 ở năm 1 nhưng trả ít hơn $34,992 ở năm 3. PV của +$30,000 năm 1 = 30,000/1.08 = 27,778. PV của −$34,992 năm 3 = −34,992/1.08³ = −27,778. Tổng PV difference = 0 → hai cơ hội **đồng giá trị** tại discount rate 8%. Nhà đầu tư hoàn toàn indifferent.
>
> **Tại sao A sai:** Nếu chỉ nhìn tổng cash flow: Opp 1 = $585,000 vs Opp 2 = $580,008 → Opp 1 nhiều hơn về nominal. Nhưng timing khác nhau và khi discount về PV thì bằng nhau — đây chính là ý nghĩa của time value of money.
> **Tại sao B sai:** Opp 2 nhận nhiều tiền hơn sớm (năm 1) nhưng ít hơn ở năm 3 — sau khi tính time value thì cân bằng hoàn toàn.

---

## Question 10

Italian government spot rates: 1-year = 0.73%, 2-year = 1.29%. The breakeven 1-year [[quantitative-methods/glossary/m02-time-value-of-money#Implied Forward Rate|forward rate]] one year from now is **closest to**:

- A. 1.01%
- B. 1.11%
- C. 1.85%

> [!answer]- Answer
> **C. 1.85%**
>
> Using the [[quantitative-methods/glossary/m02-time-value-of-money#No-Arbitrage Condition|no-arbitrage]] forward rate relationship:
> $$(1 + r_2)^2 = (1 + r_1)(1 + f_{1,1})$$
>
> $$f_{1,1} = \frac{(1.0129)^2}{(1.0073)} - 1 = \frac{1.02593}{1.0073} - 1 = 1.01850 - 1 \approx 1.85\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Implied Forward Rate|Implied forward rate]] $f_{1,1}$ là lãi suất kỳ vọng cho năm thứ 2, suy ra từ no-arbitrage: đầu tư 2 năm trực tiếp phải bằng đầu tư 1 năm rồi tái đầu tư năm tiếp theo. Công thức: $(1+r_2)^2 = (1+r_1)(1+f_{1,1})$.
>
> **Tại sao C đúng:** $(1.0129)^2 = 1.02593$ và $(1.0073)$ → $f_{1,1} = 1.02593/1.0073 - 1 = 1.85\%$. Logic: 2-year spot = 1.29% > 1-year spot = 0.73%, vì vậy năm thứ 2 phải có lãi suất cao hơn để bù đắp — kết quả 1.85% hợp lý (cao hơn cả hai spot rates).
>
> **Tại sao A sai (1.01%):** Gần với trung bình cộng $(0.73\% + 1.29\%)/2 = 1.01\%$ — cách tính sai, không dùng no-arbitrage.
> **Tại sao B sai (1.11%):** Có thể từ cách tính đơn giản hóa sai: $(1.29\% \times 2) - 0.73\% = 1.85\%$ là đúng; 1.11% phát sinh từ sai sót khác.

---

## Question 11

The current USD/EUR spot exchange rate is 1.025. The EUR risk-free rate is 0.75% and the USD risk-free rate is 3.25%. The 1-year forward USD/EUR exchange rate is **closest to**:

- A. USD/EUR 1.051
- B. USD/EUR 1.025
- C. USD/EUR 0.975

> [!answer]- Answer
> **A. USD/EUR 1.051**
>
> Using **covered interest rate parity**:
>
> $$F = S_0 \times \frac{1 + r_{USD}}{1 + r_{EUR}} = 1.025 \times \frac{1.0325}{1.0075}$$
>
> $$F = 1.025 \times 1.02481 = 1.0254 \times 1.02481 \approx 1.051$$
>
> The USD has a higher interest rate, so USD is at a **forward premium** relative to EUR, and the forward price of EUR in USD terms is higher than spot.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Covered interest rate parity: $F = S_0 \times \frac{1+r_{price currency}}{1+r_{base currency}}$. Trong đó USD/EUR nghĩa là "bao nhiêu USD để mua 1 EUR" (USD là price currency, EUR là base). Đồng nào lãi suất cao hơn sẽ có forward discount (mất giá về phía trước).
>
> **Tại sao A đúng:** $F = 1.025 \times (1.0325/1.0075) = 1.025 \times 1.02481 ≈ 1.051$. USD có lãi suất cao hơn (3.25% > 0.75%), nên 1 EUR mua được nhiều USD hơn trong tương lai → EUR forward premium. Điều này ngăn arbitrage: lợi thế lãi suất USD bị triệt tiêu bởi USD depreciation so với EUR.
>
> **Tại sao B sai (1.025):** Forward = spot chỉ khi hai lãi suất bằng nhau. Ở đây có chênh lệch lớn (2.5%), nên forward phải khác spot.
> **Tại sao C sai (0.975):** F < S nghĩa là EUR mất giá trong tương lai — điều này xảy ra khi lãi suất EUR > lãi suất USD. Nhưng thực tế ngược lại (EUR 0.75% < USD 3.25%).

---

## Question 12

A stock currently trades at USD 25. In one year, the price will either rise to USD 35 or fall to USD 15. An investor constructs a portfolio by **selling one call option** at a strike of USD 25 and **buying 0.5 shares** of stock.

The portfolio value at year-end is:

- A. USD 7.50 in both up and down scenarios
- B. USD 25 in both scenarios
- C. USD 17.50 if the stock goes up, USD 7.50 if the stock goes down

> [!answer]- Answer
> **A. USD 7.50 in both scenarios**
>
> This is the **replicating (hedge) portfolio** used in binomial option pricing.
>
> **If stock rises to USD 35:**
> - Value of 0.5 shares: $0.5 \times 35 = 17.50$
> - Call option expires in the money; payoff to short call: $-(35 - 25) = -10.00$
> - Portfolio value: $17.50 - 10.00 = \mathbf{7.50}$
>
> **If stock falls to USD 15:**
> - Value of 0.5 shares: $0.5 \times 15 = 7.50$
> - Call option expires worthless; payoff to short call: $0$
> - Portfolio value: $7.50 - 0 = \mathbf{7.50}$
>
> The portfolio is **risk-free** (perfectly hedged), delivering USD 7.50 in both states. This delta-hedged position is the foundation of [[quantitative-methods/glossary/m02-time-value-of-money#No-Arbitrage Condition|no-arbitrage]] option pricing.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Replicating portfolio trong binomial option pricing: tìm số cổ phiếu (delta, $\Delta$) để portfolio "short call + long $\Delta$ shares" có cùng giá trị ở cả up và down state. Delta = (C_up − C_down)/(S_up − S_down) = (10 − 0)/(35 − 15) = 0.5. Khi portfolio rủi ro bằng 0, nó phải kiếm risk-free rate.
>
> **Tại sao A đúng:** Up state: 0.5 × 35 − 10 = 7.50. Down state: 0.5 × 15 − 0 = 7.50. Portfolio hoàn toàn hedged — bất kể cổ phiếu tăng hay giảm, giá trị cuối đều là $7.50. Đây chính là no-arbitrage: nếu portfolio rủi ro bằng 0, phải có giá trị xác định ngay hôm nay = $7.50 / (1 + r_f).
>
> **Tại sao B sai (25 cả hai):** $25 là giá cổ phiếu hiện tại, không phải giá trị portfolio sau 1 năm.
> **Tại sao C sai (17.50 up, 7.50 down):** 17.50 là giá trị 0.5 cổ phiếu trong up state **trước khi trừ** nghĩa vụ short call (−10). Cần tính net portfolio value bao gồm cả vị thế call.


