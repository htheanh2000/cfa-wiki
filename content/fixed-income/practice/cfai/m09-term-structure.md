---
type: practice
tags:
  - cfai-official
  - fixed-income
  - term-structure
source: "CFAI CFA1 FI Practice 2026"
module: "[[m09-term-structure]]"
---

# M09 – Term Structure of Interest Rates: CFAI Practice Problems

---

## Question 1

The 1-year spot rate is 3.0% and the 2-year spot rate is 3.5%. The implied 1-year forward rate one year from now, $f(1,1)$, is closest to:

- A. 3.25%
- B. 3.50%
- C. 4.00%

> [!answer]- Answer
> **C. 4.00%**
>
> $$(1 + S_2)^2 = (1 + S_1)(1 + f(1,1))$$
> $$(1.035)^2 = (1.03)(1 + f(1,1))$$
> $$f(1,1) = \frac{(1.035)^2}{1.03} - 1 = \frac{1.071225}{1.03} - 1 = 0.04002 \approx 4.00\%$$

> [!tip]- 📖 Giải thích chi tiết
> Forward rate được suy ra từ spot rates dựa trên nguyên tắc no-arbitrage: đầu tư 2 năm liên tục phải cho cùng kết quả với đầu tư 1 năm rồi tái đầu tư 1 năm.
>
> - **A sai**: 3.25% là trung bình cộng đơn giản, không đúng cách tính forward rate.
> - **B sai**: 3.50% là spot rate 2 năm, không phải forward rate.
> - **C đúng**: Forward rate phải cao hơn cả hai spot rates khi đường cong dốc lên.

---

## Question 2

A par rate is best described as the coupon rate at which a bond is priced at:

- A. A discount to face value using spot rates for discounting.
- B. Face value when each cash flow is discounted at its respective spot rate.
- C. Face value when all cash flows are discounted at a single yield to maturity.

> [!answer]- Answer
> **B. Face value when each cash flow is discounted at its respective spot rate.**
>
> The par rate for a given maturity is the coupon rate that makes the bond price equal to par (100) when each cash flow is discounted at the appropriate spot rate for its timing.

> [!tip]- 📖 Giải thích chi tiết
> Par rate là coupon rate mà tại đó trái phiếu có giá bằng mệnh giá khi chiết khấu bằng spot rates tương ứng.
>
> - **A sai**: Par rate làm giá bằng par (không phải discount).
> - **B đúng**: Mỗi dòng tiền được chiết khấu bằng spot rate tương ứng, và giá = par.
> - **C sai**: YTM là một lãi suất duy nhất cho tất cả dòng tiền, khác với spot rates.

---

## Question 3

An analyst prices a 2-year, 4% annual coupon bond using spot rates: $S_1 = 3\%$ and $S_2 = 3.5\%$. The no-arbitrage price of this bond is closest to:

- A. $1,005.47
- B. $1,009.59
- C. $1,014.82

> [!answer]- Answer
> **B. $1,009.59**
>
> $$P = \frac{40}{(1.03)^1} + \frac{1{,}040}{(1.035)^2} = 38.83 + 970.76 = \$1{,}009.59$$

> [!tip]- 📖 Giải thích chi tiết
> Định giá no-arbitrage sử dụng spot rate riêng cho từng dòng tiền, thay vì một YTM duy nhất.
>
> - Coupon năm 1: $40 / (1.03)^1 = \$38.83$
> - Coupon + Par năm 2: $1,040 / (1.035)^2 = \$970.76$
> - Tổng giá: $38.83 + 970.76 = **\$1,009.59**$
>
> - **A sai**: Tính sai do dùng sai spot rate.
> - **B đúng**: Áp dụng đúng từng spot rate cho từng dòng tiền.
> - **C sai**: Có thể nhầm dùng coupon rate thay spot rate để chiết khấu.

---

## Question 4

An upward-sloping yield curve most likely indicates that:

- A. Short-term rates are expected to decrease in the future.
- B. Forward rates implied by the curve are higher than current short-term spot rates.
- C. The central bank is implementing an expansionary monetary policy.

> [!answer]- Answer
> **B. Forward rates implied by the curve are higher than current short-term spot rates.**
>
> An upward-sloping (normal) yield curve means longer-term spot rates exceed shorter-term spot rates. Mathematically, the implied forward rates must be higher than current short-term rates to produce this upward slope.

> [!tip]- 📖 Giải thích chi tiết
> Đường cong lợi suất dốc lên (normal yield curve) có đặc điểm:
>
> - Spot rates dài hạn > spot rates ngắn hạn
> - Forward rates > spot rates ngắn hạn hiện tại
>
> - **A sai**: Đường cong dốc lên thường phản ánh kỳ vọng lãi suất tăng hoặc term premium, không phải giảm.
> - **B đúng**: Về mặt toán học, đường cong dốc lên đòi hỏi forward rates cao hơn spot rates ngắn hạn.
> - **C sai**: Chính sách tiền tệ mở rộng thường làm giảm lãi suất ngắn hạn, có thể tạo đường cong dốc lên nhưng không phải luôn luôn.

---
