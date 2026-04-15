---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - rates-and-returns
source: "CFAI CFA1 Quant Practice 2026, pp.38-44"
module: "[[m01-rates-and-returns]]"
---

# M01 – Rates and Returns: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.38–44
**Back to module:** [[m01-rates-and-returns]]
**Glossary**: [[quantitative-methods/glossary/m01-rates-and-returns|M01 Terms]]

---

## Question 1

The [[quantitative-methods/glossary/m01-rates-and-returns#Nominal Risk-Free Rate|nominal risk-free rate]] equals the [[quantitative-methods/glossary/m01-rates-and-returns#Real Risk-Free Rate|real risk-free rate]] plus a premium for:

- A. Maturity
- B. Liquidity
- C. Expected inflation

> [!answer]- Answer
> **C. Expected inflation**
>
> The Fisher equation states:
> $$r_{\text{nominal}} = r_{\text{real}} + \pi^e$$
> where $\pi^e$ is the expected inflation premium. Maturity and liquidity premiums are additional components that explain differences between various debt instruments, not the difference between the nominal and real risk-free rate.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Nominal Risk-Free Rate|Nominal risk-free rate]] = [[quantitative-methods/glossary/m01-rates-and-returns#Real Risk-Free Rate|real risk-free rate]] + [[quantitative-methods/glossary/m01-rates-and-returns#Inflation Premium|inflation premium]]. Đây là phương trình Fisher — lãi suất danh nghĩa phải bù đắp cho lạm phát kỳ vọng để nhà đầu tư không bị mất sức mua thực.
>
> **Tại sao C đúng:** Sự khác biệt giữa nominal và real risk-free rate chỉ là inflation premium — cả hai đều là "risk-free" nên không có maturity hay liquidity risk.
>
> **Tại sao A sai:** Maturity premium giải thích chênh lệch giữa các trái phiếu có kỳ hạn khác nhau, không phải giữa nominal và real rate.
> **Tại sao B sai:** Liquidity premium giải thích chênh lệch giữa tài sản thanh khoản cao và thấp, cũng không liên quan đến mối quan hệ nominal vs. real.

---

## Question 2

The risk premium that best explains the difference in yield between a 30-year US Treasury bond and a 30-year bond issued by a small private corporation is:

- A. [[quantitative-methods/glossary/m01-rates-and-returns#Inflation Premium|Inflation premium]]
- B. [[quantitative-methods/glossary/m01-rates-and-returns#Maturity Risk Premium|Maturity premium]]
- C. [[quantitative-methods/glossary/m01-rates-and-returns#Liquidity Risk Premium|Liquidity premium]]

> [!answer]- Answer
> **C. Liquidity premium**
>
> Both bonds share the same maturity (30 years), so the maturity premium does not explain the yield difference. Both are nominal instruments, so the inflation premium is also equal. The key difference is that US Treasuries trade in highly liquid markets with narrow bid-ask spreads, while bonds from a small private corporation trade infrequently and command a **liquidity premium** to compensate investors for this illiquidity.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Liquidity Risk Premium|Liquidity premium]] bù đắp cho nhà đầu tư khi nắm giữ tài sản khó bán (bid-ask spread rộng, ít giao dịch). [[quantitative-methods/glossary/m01-rates-and-returns#Maturity Risk Premium|Maturity premium]] bù đắp rủi ro lãi suất theo thời gian.
>
> **Tại sao C đúng:** Hai trái phiếu có cùng kỳ hạn 30 năm (loại maturity premium) và đều là nominal instrument (loại inflation premium). Điểm khác biệt duy nhất là thanh khoản: US Treasury giao dịch hàng nghìn tỷ mỗi ngày trong khi trái phiếu công ty tư nhân nhỏ hầu như không có thị trường thứ cấp.
>
> **Tại sao A sai:** Inflation premium như nhau vì cả hai trái phiếu đều bằng USD — cùng đồng tiền, cùng lạm phát kỳ vọng.
> **Tại sao B sai:** Maturity premium đã được "kiểm soát" — cả hai cùng 30 năm, nên phần premium này giống nhau.

---

## Question 3

Fund Y reported the following annual returns over five years:

| Year | Return |
|------|--------|
| 1 | 19.5% |
| 2 | −1.9% |
| 3 | 19.7% |
| 4 | 35.0% |
| 5 | 5.7% |

The [[quantitative-methods/glossary/m01-rates-and-returns#Geometric Mean Return|geometric mean annual return]] is **closest to**:

- A. 14.9%
- B. 15.6%
- C. 19.5%

> [!answer]- Answer
> **A. 14.9%**
>
> The geometric mean is calculated as:
> $$R_G = \left[\prod_{t=1}^{T}(1+R_t)\right]^{1/T} - 1$$
>
> $$R_G = \left[(1.195)(0.981)(1.197)(1.350)(1.057)\right]^{1/5} - 1$$
>
> Computing the product:
> - $1.195 \times 0.981 = 1.17225$
> - $1.17225 \times 1.197 = 1.40318$
> - $1.40318 \times 1.350 = 1.89429$
> - $1.89429 \times 1.057 = 2.00227$
>
> $$R_G = (2.00227)^{0.2} - 1 = 1.14893 - 1 \approx 14.9\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Geometric Mean Return|Geometric mean return]] đo tốc độ tăng trưởng kép thực tế của $1 đầu tư. Công thức: nhân tất cả (1 + R), rồi lấy căn bậc T. Đây là thước đo chính xác nhất cho hiệu suất đa kỳ.
>
> **Tại sao A đúng:** Tích của 5 hệ số tăng trưởng ≈ 2.002, tức $1 trở thành $2.002 sau 5 năm. Tốc độ kép hàng năm = $2.002^{0.2} - 1 ≈ 14.9\%$. Lưu ý: năm 2 có return âm (−1.9%) kéo geometric mean xuống thấp hơn arithmetic mean.
>
> **Tại sao B sai:** 15.6% là gần với arithmetic mean (trung bình cộng đơn giản) = $(19.5 - 1.9 + 19.7 + 35.0 + 5.7)/5 = 15.6\%$. Arithmetic mean luôn ≥ geometric mean khi có variance.
> **Tại sao C sai:** 19.5% là return của năm 1, không phải trung bình.

---

## Question 4

A portfolio manager invests EUR 5,000 annually in a stock at the following prices over four periods: EUR 62, EUR 76, EUR 84, EUR 90.

The average price paid per share is **best represented** as:

- A. [[quantitative-methods/glossary/m01-rates-and-returns#Harmonic Mean|Harmonic mean]] = EUR 76.48
- B. [[quantitative-methods/glossary/m01-rates-and-returns#Geometric Mean Return|Geometric mean]] = EUR 77.26
- C. [[quantitative-methods/glossary/m01-rates-and-returns#Arithmetic Mean Return|Arithmetic average]] = EUR 78.00

> [!answer]- Answer
> **A. Harmonic mean = EUR 76.48**
>
> When investing a **fixed dollar amount** periodically (dollar-cost averaging), the average cost per share is best measured by the **harmonic mean**:
>
> $$\bar{X}_H = \frac{n}{\sum_{i=1}^{n}\frac{1}{X_i}} = \frac{4}{\frac{1}{62}+\frac{1}{76}+\frac{1}{84}+\frac{1}{90}}$$
>
> Computing:
> - $1/62 = 0.016129$
> - $1/76 = 0.013158$
> - $1/84 = 0.011905$
> - $1/90 = 0.011111$
> - Sum $= 0.052303$
>
> $$\bar{X}_H = \frac{4}{0.052303} = \text{EUR } 76.48$$
>
> The harmonic mean is appropriate because more shares are purchased when prices are low, and fewer when prices are high — the harmonic mean properly weights this effect.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Harmonic Mean|Harmonic mean]] = $n / \sum(1/X_i)$. Dùng khi đầu tư số tiền cố định định kỳ (dollar-cost averaging). Khi giá thấp, mua được nhiều cổ phiếu hơn → những mức giá thấp được "weighted" nhiều hơn → harmonic mean thấp hơn arithmetic mean.
>
> **Tại sao A đúng:** Mỗi kỳ đầu tư EUR 5,000 cố định, nên số cổ phiếu mua = 5,000/giá. Harmonic mean tự động phản ánh đúng giá bình quân thực tế trả per share = EUR 76.48.
>
> **Tại sao B sai:** Geometric mean (EUR 77.26) dùng cho tính toán tốc độ tăng trưởng kép của return, không phải giá bình quân khi dollar-cost averaging.
> **Tại sao C sai:** Arithmetic mean (EUR 78.00) giả định mua số cổ phiếu bằng nhau ở mỗi mức giá — không phản ánh thực tế đầu tư số tiền cố định.

---

## Question 5

Regarding [[quantitative-methods/glossary/m01-rates-and-returns#Arithmetic Mean Return|arithmetic]] and [[quantitative-methods/glossary/m01-rates-and-returns#Geometric Mean Return|geometric means]] of investment returns, which statement is **most accurate**?

- A. The geometric mean is greater than the arithmetic mean for returns with non-zero variance
- B. The geometric mean measures the compound rate of growth of an investment
- C. The arithmetic mean measures the terminal value of an investment

> [!answer]- Answer
> **B. The geometric mean measures the compound rate of growth of an investment**
>
> - **A is incorrect**: For non-zero variance, the geometric mean is **less than** (not greater than) the arithmetic mean. The relationship is approximately $R_G \approx R_A - \frac{\sigma^2}{2}$.
> - **B is correct**: The geometric mean correctly measures the **compounded (time-weighted) rate of return**, giving the actual growth rate of a single dollar invested over the period.
> - **C is incorrect**: The arithmetic mean overstates the terminal value for multi-period returns with variance; it is useful as an estimate for a **single future period**, not for measuring terminal value.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Quan hệ giữa [[quantitative-methods/glossary/m01-rates-and-returns#Arithmetic Mean Return|arithmetic mean]] và [[quantitative-methods/glossary/m01-rates-and-returns#Geometric Mean Return|geometric mean]]: $R_G \approx R_A - \sigma^2/2$. Geometric mean luôn nhỏ hơn hoặc bằng arithmetic mean (bằng chỉ khi variance = 0, tức mọi kỳ có cùng return).
>
> **Tại sao B đúng:** Geometric mean = tốc độ tăng trưởng kép (CAGR). Nếu đầu tư $100 và geometric mean = 10%/năm, sau 5 năm sẽ có đúng $100 × 1.10⁵. Đây là thước đo "wealth growth" thực sự.
>
> **Tại sao A sai:** Ngược lại hoàn toàn — geometric mean **nhỏ hơn** arithmetic mean khi variance > 0. Ví dụ: +50% rồi −50% → arithmetic mean = 0% nhưng geometric mean = $\sqrt{1.5 \times 0.5} - 1 = -13.4\%$.
> **Tại sao C sai:** Arithmetic mean không đo terminal value — thực ra nó **phóng đại** terminal value. Arithmetic mean hữu ích để ước tính return kỳ vọng cho **một kỳ tương lai đơn lẻ**.

---

## Question 6

A fund receives investments and generates the following returns:

| Year | Investment at Start of Year | Annual Return |
|------|----------------------------|---------------|
| 1 | USD 1,000 | 15% |
| 2 | USD 4,000 | 14% |
| 3 | USD 45,000 | −4% |

Which return measure is **most likely negative**?

- A. Geometric mean return
- B. [[quantitative-methods/glossary/m01-rates-and-returns#Time-Weighted Return (TWR)|Time-weighted return (TWR)]]
- C. [[quantitative-methods/glossary/m01-rates-and-returns#Money-Weighted Return (MWR)|Money-weighted return (MWR)]]

> [!answer]- Answer
> **C. Money-weighted return (MWR)**
>
> The MWR is the IRR of all cash flows. Because the vast majority of capital (USD 45,000) was invested in Year 3 when the return was −4%, the MWR is heavily biased toward that poor year.
>
> **MWR (IRR) ≈ −2.22%** (negative)
>
> **TWR** strips out the timing of cash flows and equally weights each sub-period:
> $$R_{TWR} = [(1.15)(1.14)(0.96)]^{1/3} - 1 \approx 7.97\%$$
>
> The TWR is positive because it treats each period equally regardless of asset size. The MWR is negative because the large investment was made just before the loss year.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Money-Weighted Return (MWR)|MWR]] = IRR của tất cả cash flows, bị ảnh hưởng bởi timing và size của dòng tiền. [[quantitative-methods/glossary/m01-rates-and-returns#Time-Weighted Return (TWR)|TWR]] = geometric mean của các sub-period returns, loại bỏ hoàn toàn ảnh hưởng của cash flow timing — đây là thước đo chuẩn để đánh giá portfolio manager.
>
> **Tại sao C đúng:** $45,000 (chiếm ~91% tổng vốn) được đầu tư ngay trước năm lỗ −4%. MWR bị "kéo" mạnh về phía năm lỗ → âm ≈ −2.22%. Đây là hệ quả tất yếu: nhà đầu tư bơm tiền đúng lúc tệ nhất.
>
> **Tại sao A sai:** Geometric mean return = TWR ≈ 7.97% (dương), vì nó weight đều 3 kỳ bất kể số tiền.
> **Tại sao B sai:** TWR ≈ 7.97% (dương) — TWR không bị ảnh hưởng bởi việc $45,000 vào năm 3; nó chỉ nhân $(1.15)(1.14)(0.96)$ rồi lấy căn bậc 3.

---

## Question 7

A fund begins Year 1 with USD 10 million and earns 14%. At the start of Year 2, it attracts an additional USD 100 million and earns 8% in Year 2.

The [[quantitative-methods/glossary/m01-rates-and-returns#Money-Weighted Return (MWR)|money-weighted return (MWR)]] is **most likely**:

- A. Less than the [[quantitative-methods/glossary/m01-rates-and-returns#Time-Weighted Return (TWR)|time-weighted return (TWR)]]
- B. The same as the TWR
- C. Greater than the TWR

> [!answer]- Answer
> **A. Less than the TWR**
>
> Most of the capital (USD 100 million) was invested at the start of Year 2, when the return was the lower rate of 8%. The MWR is therefore biased toward the 8% return.
>
> **TWR** equally weights each year:
> $$R_{TWR} = \sqrt{(1.14)(1.08)} - 1 \approx 10.96\%$$
>
> **MWR** is closer to 8% because of the large capital inflow before the lower-return year.
>
> MWR < TWR when large cash inflows precede periods of below-average returns.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Quy tắc vàng về MWR vs. TWR: khi dòng tiền lớn vào **trước** kỳ có return thấp → MWR < TWR. Khi dòng tiền lớn vào **trước** kỳ có return cao → MWR > TWR. TWR luôn trung lập với timing.
>
> **Tại sao A đúng:** $100M vào đầu năm 2 (kỳ return thấp hơn: 8%). MWR bị kéo gần 8% vì phần lớn vốn hoạt động ở năm return thấp. TWR = $\sqrt{1.14 \times 1.08} - 1 ≈ 10.96\%$, cao hơn MWR vì weight đều cả hai năm.
>
> **Tại sao B sai:** MWR = TWR chỉ khi không có cash flow trung gian, hoặc return mọi kỳ bằng nhau.
> **Tại sao C sai:** MWR > TWR xảy ra khi tiền lớn vào trước kỳ **tốt** — trường hợp này ngược lại: tiền lớn vào trước kỳ return thấp hơn.

---

## Question 8

An investor compares three ETFs with the following [[quantitative-methods/glossary/m01-rates-and-returns#Holding Period Return (HPR)|holding-period returns]]:

| ETF | Holding Period | Return |
|-----|---------------|--------|
| ETF 1 | 125 days | 4.25% |
| ETF 2 | 8 weeks | 1.95% |
| ETF 3 | 16 months | 17.18% |

The ETF with the **highest annualized return** is:

- A. ETF 1
- B. ETF 2
- C. ETF 3

> [!answer]- Answer
> **B. ETF 2**
>
> Annualizing each return:
>
> **ETF 1** (125 days, assume 365-day year):
> $$r_1 = (1.0425)^{365/125} - 1 = (1.0425)^{2.92} - 1 \approx 12.92\%$$
>
> **ETF 2** (8 weeks = 8/52 year):
> $$r_2 = (1.0195)^{52/8} - 1 = (1.0195)^{6.5} - 1 \approx 13.37\%$$
>
> **ETF 3** (16 months = 16/12 year):
> $$r_3 = (1.1718)^{12/16} - 1 = (1.1718)^{0.75} - 1 \approx 12.63\%$$
>
> ETF 2 has the highest annualized return at **13.37%**.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Holding Period Return (HPR)|Annualized return]] = $(1 + R_{HPR})^{1/t} - 1$, trong đó $t$ là holding period tính theo năm. Phép tính này cho phép so sánh "táo với táo" giữa các khoản đầu tư có thời hạn khác nhau.
>
> **Tại sao B đúng:** ETF 2 có holding period ngắn nhất (8 tuần = 0.154 năm) nhưng return 1.95% trong thời gian đó — khi annualize bằng lũy thừa $^{52/8}$, nó đạt 13.37%, cao nhất trong 3 ETF. Đây là bài học quan trọng: return ngắn hạn cao khi annualize thường trội hơn return dài hạn tương đương.
>
> **Tại sao A sai:** ETF 1 (125 ngày) annualized ≈ 12.92% — thấp hơn ETF 2 dù holding period dài hơn.
> **Tại sao C sai:** ETF 3 (16 tháng) annualized ≈ 12.63% — thấp nhất vì 17.18% trong 16 tháng tương đương tốc độ tăng trưởng hàng năm thấp hơn.

---

## Question 9

A stock is priced at USD 208.25 at $t = 0$ and USD 186.75 at $t = 1$.

The **[[quantitative-methods/glossary/m01-rates-and-returns#Continuously Compounded Return|continuously compounded return]]** is closest to:

- A. −10.90%
- B. −10.32%
- C. 11.51%

> [!answer]- Answer
> **A. −10.90%**
>
> The continuously compounded (log) return is:
> $$r_{cc} = \ln\!\left(\frac{P_1}{P_0}\right) = \ln\!\left(\frac{186.75}{208.25}\right) = \ln(0.8968) \approx -0.1090 = -10.90\%$$
>
> Note: The simple holding-period return is $(186.75/208.25) - 1 = -10.32\%$ (answer B). The continuously compounded return is slightly more negative than the simple return, consistent with the relationship $r_{cc} = \ln(1 + r_{HPR})$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Continuously Compounded Return|Continuously compounded return]] = $\ln(P_1/P_0)$. Luôn nhỏ hơn simple HPR vì $\ln(1+r) < r$ với $r \neq 0$. Ưu điểm: có thể cộng trực tiếp qua thời gian (time-additive), dễ tính toán trong mô hình tài chính.
>
> **Tại sao A đúng:** $\ln(186.75/208.25) = \ln(0.8968) = -0.1090 = -10.90\%$. Đây là continuously compounded return — "tốc độ tăng trưởng tức thời liên tục."
>
> **Tại sao B sai:** −10.32% là simple HPR = $(186.75 - 208.25)/208.25$. Simple return luôn ít âm hơn (hoặc ít dương hơn) so với continuously compounded return.
> **Tại sao C sai:** +11.51% = $\ln(208.25/186.75)$ — nhầm chiều tính, đây là return nếu giá tăng từ 186.75 lên 208.25.

---

## Question 10

An equity portfolio has a market value of USD 25 million. It is 20% debt-financed (i.e., USD 5 million borrowed) at a cost of 6%. The portfolio return is 10%.

The [[quantitative-methods/glossary/m01-rates-and-returns#Leveraged Return|leveraged return]] is closest to:

- A. 11.0%
- B. 11.2%
- C. 13.2%

> [!answer]- Answer
> **A. 11.0%**
>
> The leveraged portfolio return formula is:
> $$R_L = R_P + \frac{V_B}{V_E}(R_P - r_B)$$
>
> where $V_B$ = borrowed capital, $V_E$ = equity capital, $r_B$ = borrowing rate.
>
> - Equity $V_E$ = USD 20 million (USD 25M total − USD 5M debt)
> - $V_B / V_E = 5/20 = 0.25$
>
> $$R_L = 10\% + 0.25 \times (10\% - 6\%) = 10\% + 0.25 \times 4\% = 10\% + 1\% = 11.0\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Leveraged Return|Leveraged return]] = $R_P + \frac{V_B}{V_E}(R_P - r_B)$. Phần $(R_P - r_B)$ là "spread" giữa portfolio return và borrowing cost — đây là lợi ích (hoặc tổn thất) từ đòn bẩy. Tỷ lệ $V_B/V_E$ khuếch đại spread đó.
>
> **Tại sao A đúng:** Equity = $25M - $5M = $20M. Leverage ratio $V_B/V_E = 5/20 = 0.25$. Spread = 10% − 6% = 4%. Leveraged return = 10% + 0.25 × 4% = 11%. Logic: đi vay $5M với lãi 6%, đầu tư tạo ra 10% → lãi ròng 4% trên khoản vay, và 0.25 × 4% = 1% bonus return cho equity holders.
>
> **Tại sao B sai:** 11.2% có thể phát sinh từ việc tính sai equity capital (dùng $25M thay vì $20M).
> **Tại sao C sai:** 13.2% sẽ đúng nếu leverage ratio = 0.8 ($5M/$6.25M) — tính sai phân bổ vốn.

---

## Question 11

An investment manager's [[quantitative-methods/glossary/m01-rates-and-returns#Gross Return|gross return]] is **best described** as:

- A. An after-tax nominal, risk-adjusted return
- B. The return prior to deduction of trading expenses
- C. Often used as a measure of the manager's investment skill because it excludes management and administrative expenses

> [!answer]- Answer
> **C. Often used as a measure of the manager's investment skill because it excludes management and administrative expenses**
>
> - **Gross return** is calculated **before** deducting management fees and administrative expenses, but **after** deducting trading expenses (commissions, bid-ask spreads). Trading costs are part of executing the investment strategy.
> - **A is incorrect**: Gross return is a pre-tax nominal return; risk-adjustment is a separate concept.
> - **B is incorrect**: Trading expenses **are** included (deducted) in the gross return.
> - **C is correct**: Since gross return excludes the manager's fee, it is used to evaluate the manager's ability to generate alpha through security selection and portfolio construction.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Hệ thống phân tầng return: [[quantitative-methods/glossary/m01-rates-and-returns#Gross Return|Gross return]] (sau trading costs, trước management fees) → [[quantitative-methods/glossary/m01-rates-and-returns#Net Return|Net return]] (sau cả management fees) → [[quantitative-methods/glossary/m01-rates-and-returns#After-Tax Return|After-tax return]] (sau thuế). Trading costs được trừ khỏi gross return vì chúng là chi phí không thể tách rời của việc thực thi chiến lược.
>
> **Tại sao C đúng:** Gross return phản ánh kỹ năng chọn cổ phiếu và xây dựng danh mục của manager (alpha generation), tách biệt khỏi mức phí quản lý. So sánh gross return giữa các manager cho phép đánh giá năng lực đầu tư thuần túy.
>
> **Tại sao A sai:** Gross return là nominal, pre-tax, và không risk-adjusted.
> **Tại sao B sai:** Trading expenses (commission, bid-ask spread) **đã được trừ** trong gross return — chúng là chi phí trực tiếp của việc thực hiện giao dịch, không tách ra được.

---

## Question 12

Regarding the use of leverage to enhance investment returns, which statement is **most accurate**?

- A. Leverage amplifies gains but not losses
- B. If half the portfolio is borrowed, the net return will double
- C. Leverage increases the return to equity investors only if the portfolio return exceeds the cost of borrowing

> [!answer]- Answer
> **C. Leverage increases the return to equity investors only if the portfolio return exceeds the cost of borrowing**
>
> - **A is incorrect**: Leverage amplifies **both gains and losses** symmetrically. Downside risk is magnified just as upside return is.
> - **B is incorrect**: If half the portfolio is borrowed at a cost, the **net return to equity is not simply doubled** — borrowing costs reduce the benefit, and the leverage ratio of debt-to-equity is 1.0 (not 0.5 relative to equity).
> - **C is correct**: From the leveraged return formula $R_L = R_P + \frac{V_B}{V_E}(R_P - r_B)$, leverage is beneficial only when $R_P > r_B$. If $R_P < r_B$, leverage destroys value for equity holders.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Leveraged Return|Leverage]] hoạt động như "khuếch đại hai chiều": khi $R_P > r_B$ thì khuếch đại lợi nhuận; khi $R_P < r_B$ thì khuếch đại tổn thất. Đây là bản chất của financial leverage — không có "free lunch."
>
> **Tại sao C đúng:** Từ công thức $R_L = R_P + \frac{V_B}{V_E}(R_P - r_B)$: khi $R_P > r_B$, số hạng thứ hai dương → leverage tốt. Khi $R_P < r_B$, số hạng thứ hai âm → leverage phá hủy giá trị. Điều kiện $R_P > r_B$ là điều kiện cần để leverage có lợi.
>
> **Tại sao A sai:** Leverage khuếch đại cả hai chiều đối xứng. Nếu return âm −5% với leverage ratio 0.5 thì equity return = −5% + 0.5×(−5% − cost) — tệ hơn nhiều.
> **Tại sao B sai:** Nếu nửa danh mục đi vay (debt/equity = 1.0), leveraged return = $R_P + 1.0 \times (R_P - r_B) = 2R_P - r_B$ — không đơn giản là gấp đôi vì còn trừ borrowing cost.

---

## Question 13

A EUR 10,000 hedge fund investment is structured as follows: 25% is debt-financed at a borrowing rate of 6%. The applicable tax rate is 30%. The fund reports a [[quantitative-methods/glossary/m01-rates-and-returns#Gross Return|gross return]] of 8.46%, trading expenses of 1.10%, and management expenses of 1.60%.

The [[quantitative-methods/glossary/m01-rates-and-returns#After-Tax Return|after-tax return]] is **closest to**:

- A. 3.60%
- B. 3.98%
- C. 5.00%

> [!answer]- Answer
> **C. 5.00%**
>
> **Step 1 – [[quantitative-methods/glossary/m01-rates-and-returns#Net Return|Net return]] (after management expenses; trading costs already embedded in gross return):**
> $$R_{\text{net}} = 8.46\% - 1.60\% = 6.86\%$$
> *(Trading expenses of 1.10% are already reflected in the gross return calculation; only management expenses are deducted separately.)*
>
> **Step 2 – [[quantitative-methods/glossary/m01-rates-and-returns#Leveraged Return|Leveraged return]]:**
> - Total investment: EUR 10,000; Debt: 25% × 10,000 = EUR 2,500; Equity: EUR 7,500
> - $V_B / V_E = 2{,}500 / 7{,}500 = 1/3$
>
> $$R_L = 6.86\% + \frac{1}{3}(6.86\% - 6.00\%) = 6.86\% + \frac{1}{3}(0.86\%) = 6.86\% + 0.287\% \approx 7.15\%$$
>
> **Step 3 – After-tax return:**
> $$R_{\text{after-tax}} = 7.15\% \times (1 - 0.30) = 7.15\% \times 0.70 \approx 5.00\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Bài này tích hợp 3 bước: [[quantitative-methods/glossary/m01-rates-and-returns#Net Return|net return]] → [[quantitative-methods/glossary/m01-rates-and-returns#Leveraged Return|leveraged return]] → [[quantitative-methods/glossary/m01-rates-and-returns#After-Tax Return|after-tax return]]. Hiểu thứ tự áp dụng rất quan trọng.
>
> **Logic từng bước:**
> - **Bước 1:** Gross return 8.46% đã bao gồm trading expenses (1.10% đã embedded). Chỉ trừ management expenses 1.60% → net return = 6.86%.
> - **Bước 2:** 25% debt → $V_B$ = EUR 2,500, $V_E$ = EUR 7,500. Leverage ratio = 1/3. Spread = 6.86% − 6.00% = 0.86%. Leveraged return = 6.86% + (1/3)(0.86%) ≈ 7.15%. Đòn bẩy mang lại thêm 0.29% vì portfolio return vượt borrowing cost.
> - **Bước 3:** After-tax = 7.15% × (1 − 30%) = 5.00%.
>
> **Tại sao C đúng:** Đáp án 5.00% đến từ chuỗi tính toán chính xác cả 3 bước.
> **Tại sao A sai (3.60%):** Có thể do nhầm trừ cả trading expenses (1.10%) lẫn management expenses trước khi tính leveraged return, hoặc áp dụng sai thuế suất.
> **Tại sao B sai (3.98%):** Có thể do không áp dụng leverage hoặc tính sai leverage ratio.
