---
type: practice
tags:
  - cfai-official
  - derivatives
  - pricing-valuation
source: "CFAI CFA1 Derivatives Practice 2026 – Volume 7"
module: "[[m07-pricing-valuation]]"
---

# M07 – Pricing and Valuation: CFAI Practice Problems

**Source:** CFAI CFA1 Derivatives Practice 2026 – Volume 7
**Back to module:** [[m07-pricing-valuation]]

---

> **Exhibit: SAPP**
>
> Sarah Park (SAPP) continues her derivatives training series with modules on pricing and valuation of forwards, futures, and swaps. She presents scenarios involving mark-to-market gains and losses, zero-coupon rate calculations, and the structure of forward-starting swaps and FRAs. Junior analysts are asked to evaluate specific positions and compute prices/values using no-arbitrage principles.

---

## Question 1

SAPP presents the following scenario: Ace Corp entered into a receive-fixed interest rate swap six months ago. Since inception, interest rates have risen significantly. SAPP asks the junior analysts to assess the mark-to-market impact and Ace's credit exposure. The most likely outcome is:

- A. MTM loss for Ace, and Ace's credit exposure to the counterparty decreases
- B. MTM gain for Ace, and Ace's credit exposure to the counterparty increases
- C. MTM loss for Ace, and Ace's credit exposure to the counterparty increases

> [!answer]- Answer
> **A. MTM loss for Ace, and Ace's credit exposure to the counterparty decreases**
>
> Ace is the fixed-rate receiver. When rates rise, the fixed rate Ace receives is below the new market rate — the swap has negative value (MTM loss) for Ace. When a derivative has negative value to a party, that party does not face credit exposure from the counterparty (the counterparty owes nothing); rather, the counterparty faces exposure to Ace. Therefore, Ace's credit exposure decreases.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Interest rate swap MTM:
> - **Receive fixed**: Lợi khi rates giảm (nhận fixed rate cao hơn market), lỗ khi rates tăng
> - **Pay fixed**: Lợi khi rates tăng, lỗ khi rates giảm
>
> Credit exposure trong swap:
> - Bên có MTM gain → có credit exposure (đối tác nợ mình tiền)
> - Bên có MTM loss → không có credit exposure (mình nợ đối tác tiền)
>
> **Tại sao A đúng:**
> 1. Ace receive fixed + rates tăng → fixed rate Ace nhận thấp hơn market rate mới → **MTM loss**
> 2. Swap có giá trị âm đối với Ace → Ace nợ counterparty → Ace **không** có credit exposure → exposure giảm
>
> **Tại sao B sai:** Receive fixed + rates tăng = MTM loss, không phải gain.
> **Tại sao C sai:** MTM loss đúng, nhưng credit exposure tăng là sai — khi Ace lỗ, Ace nợ counterparty nên Ace không có credit exposure.

---

## Question 2

Given the following zero-coupon rates, SAPP asks analysts to calculate the 3-year spot rate ($s_3$):

| Maturity | Zero Rate |
|---|---|
| 1 year | 2.50% |
| 2 years | 2.75% |
| 3 years | ? |

A 3-year annual coupon bond with a 3% coupon trades at par (100). Using the given zero rates and the par bond, the 3-year spot rate ($s_3$) is closest to:

- A. 2.85%
- B. 2.95%
- C. 3.009%

> [!answer]- Answer
> **C. 3.009%**
>
> Discount each cash flow at the appropriate zero rate:
> $$100 = \frac{3}{(1.025)^1} + \frac{3}{(1.0275)^2} + \frac{103}{(1 + s_3)^3}$$
>
> $$100 = 2.9268 + 2.8412 + \frac{103}{(1 + s_3)^3}$$
>
> $$100 - 2.9268 - 2.8412 = \frac{103}{(1 + s_3)^3}$$
>
> $$94.2320 = \frac{103}{(1 + s_3)^3}$$
>
> $$(1 + s_3)^3 = \frac{103}{94.2320} = 1.09298$$
>
> $$s_3 = (1.09298)^{1/3} - 1 \approx 3.009\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Bootstrapping zero-coupon rates: Sử dụng giá par bond và các spot rates đã biết để tìm spot rate chưa biết.
>
> **Tính toán chi tiết:**
> 1. Cash flows của 3-year par bond: C = 3 mỗi năm, FV = 100
> 2. PV năm 1: $\frac{3}{1.025} = 2.9268$
> 3. PV năm 2: $\frac{3}{(1.0275)^2} = \frac{3}{1.05576} = 2.8412$
> 4. Tổng PV năm 1+2: $2.9268 + 2.8412 = 5.7680$
> 5. PV năm 3 phải = $100 - 5.7680 = 94.2320$
> 6. $\frac{103}{(1+s_3)^3} = 94.2320$
> 7. $(1+s_3)^3 = 1.09298$
> 8. $s_3 = 3.009\%$
>
> **Tại sao C đúng:** Bootstrapping cho $s_3 = 3.009\%$. Spot rate năm 3 cao hơn năm 2 (2.75%) phù hợp với upward-sloping yield curve.
>
> **Tại sao A, B sai:** Các giá trị này không thỏa mãn phương trình no-arbitrage khi discount par bond.

---

## Question 3

SAPP presents a forward contract on a stock that pays an unknown dividend yield. Given only the current stock price, the risk-free rate, and the forward price, she asks whether the dividend yield can be determined. The most likely answer is:

- A. Yes — the dividend yield can be solved from the cost-of-carry formula
- B. No — additional information about the stock's beta is required
- C. Not enough information — while the cost-of-carry formula includes the dividend yield, the question does not provide sufficient data to isolate it without additional assumptions

> [!answer]- Answer
> **C. Not enough information**
>
> While the cost-of-carry model $F_0 = S_0 \times e^{(r-q)T}$ can theoretically be used to solve for $q$ if $F_0$, $S_0$, $r$, and $T$ are known, the question states the dividend yield is "unknown" and the context suggests insufficient information is provided to determine the exact relationship without additional data or assumptions.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Forward pricing với dividend yield:
> $$F_0 = S_0 \times e^{(r - q)T}$$
>
> Về mặt lý thuyết, nếu biết $F_0, S_0, r, T$ thì có thể giải cho $q$. Tuy nhiên, câu hỏi nhấn mạnh rằng không đủ thông tin trong bối cảnh cụ thể được đưa ra.
>
> **Tại sao C đúng:** Trong context của câu hỏi, thông tin cung cấp không đủ để xác định chính xác dividend yield. Có thể cần thêm assumptions về timing, discrete vs continuous dividends, v.v.
>
> **Tại sao A sai:** Mặc dù về mặt toán học có thể giải, nhưng context cụ thể không đủ thông tin.
> **Tại sao B sai:** Beta không liên quan đến cost-of-carry model — beta là CAPM, không phải derivative pricing.

---

## Question 4

A portfolio manager wants to hedge against rising interest rates starting in 2 years, for a 5-year period. The most appropriate instrument is:

- A. A spot-starting 5-year interest rate swap
- B. A pay-fixed 5-year forward-starting swap beginning in 2 years
- C. A 2-year interest rate cap

> [!answer]- Answer
> **B. A pay-fixed 5-year forward-starting swap beginning in 2 years**
>
> A forward-starting swap allows the manager to lock in a fixed rate today for a swap that begins at a future date. By paying fixed in a 5-year swap starting in 2 years (a 2y5y forward swap), the manager hedges against rising rates during the specific future period of concern.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Forward-starting swap: Swap bắt đầu tại thời điểm trong tương lai, nhưng fixed rate được lock-in ngay hôm nay.
> - **Pay fixed**: Hedge against rates tăng (nhận floating sẽ tăng theo market, trả fixed đã lock)
> - **2y5y**: Bắt đầu sau 2 năm, kéo dài 5 năm
>
> **Tại sao B đúng:** Manager lo rates tăng bắt đầu từ 2 năm sau, trong 5 năm tiếp → forward-starting swap (2y5y) pay fixed phù hợp chính xác. Lock fixed rate hôm nay cho giai đoạn năm 2-7.
>
> **Tại sao A sai:** Spot-starting swap bắt đầu ngay → hedge 5 năm từ hôm nay, không phải từ 2 năm sau. Timing không khớp.
> **Tại sao C sai:** 2-year cap chỉ bảo vệ 2 năm đầu, không bảo vệ giai đoạn 5 năm bắt đầu từ năm thứ 2.

---

## Question 5

A company wants to borrow at a fixed rate but can only access floating-rate markets at attractive terms. To achieve synthetic fixed-rate borrowing, the company should most likely:

- A. Borrow at the floating rate and enter into a series of zero-value FRAs to lock in future rates
- B. Borrow at the floating rate and buy interest rate puts
- C. Borrow at the floating rate and sell interest rate caps

> [!answer]- Answer
> **A. Borrow at the floating rate and enter into a series of zero-value FRAs to lock in future rates**
>
> By borrowing floating and entering into FRAs (forward rate agreements) for each reset period, the company locks in the interest rate for each future period, effectively creating a synthetic fixed-rate loan. Each FRA has zero value at initiation, and together they convert the floating obligation to fixed.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Synthetic fixed-rate borrowing:
> - Floating-rate loan + FRAs = Synthetic fixed-rate loan
> - FRA: Hợp đồng lock lãi suất cho một giai đoạn tương lai cụ thể
> - Chuỗi FRAs (strip of FRAs) ≈ Interest rate swap (pay fixed)
>
> **Tại sao A đúng:** Floating borrowing + FRAs → lock mỗi floating reset → tổng hợp = fixed rate. FRAs tại inception có zero value (fair pricing).
>
> **Tại sao B sai:** Mua interest rate puts bảo vệ khi rates giảm (cho investors). Borrower cần bảo vệ khi rates tăng → nên mua caps, không phải puts.
> **Tại sao C sai:** Bán caps tạo thu nhập premium nhưng không bảo vệ khỏi rates tăng — ngược lại, bán cap = nhận premium nhưng chấp nhận rủi ro nếu rates tăng quá cap strike.

---

## Question 6

At the initiation of a plain vanilla interest rate swap, the values of the fixed-rate and floating-rate legs are set such that:

- A. The values at initiation sum to zero — the swap has zero net value
- B. The fixed leg has a higher present value than the floating leg
- C. The floating leg has a higher present value than the fixed leg

> [!answer]- Answer
> **A. The values at initiation sum to zero — the swap has zero net value**
>
> At initiation, a plain vanilla swap is priced so that the present value of the fixed leg equals the present value of the floating leg. The swap rate is set to make the net value zero — neither party pays the other at inception.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Swap pricing tại initiation:
> $$PV(\text{fixed leg}) = PV(\text{floating leg})$$
> $$\Rightarrow V_{\text{swap}} = PV(\text{fixed}) - PV(\text{floating}) = 0$$
>
> Swap rate là fixed rate duy nhất thỏa mãn điều kiện trên. Đây là nguyên tắc no-arbitrage — không bên nào phải trả tiền cho bên kia khi ký hợp đồng.
>
> **Tại sao A đúng:** Swap được thiết kế để fair tại inception → zero value → cả hai bên đồng ý vì không ai bị thiệt.
>
> **Tại sao B sai:** Nếu PV(fixed) > PV(floating), fixed payer sẽ yêu cầu được bù đắp → swap rate sẽ được điều chỉnh cho đến khi PV bằng nhau.
> **Tại sao C sai:** Tương tự, floating leg cao hơn cũng không xảy ra tại inception khi swap được priced fairly.
