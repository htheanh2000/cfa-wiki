---
type: practice
tags:
  - cfai-official
  - fixed-income
  - interest-rate-risk-return
source: "CFAI CFA1 FI Practice 2026"
module: "[[m10-interest-rate-risk-return]]"
---

# M10 – Interest Rate Risk & Return: CFAI Practice Problems

---

## Question 1

An investor holding a fixed-rate bond to maturity has three sources of return. Which of the following is NOT a source of return for this investor?

- A. Periodic coupon payments received during the holding period.
- B. Capital gain or loss at maturity relative to the purchase price.
- C. Income earned from reinvesting coupon payments at prevailing market rates.

> [!answer]- Answer
> **B. Capital gain or loss at maturity relative to the purchase price.**
>
> The three sources of return are: (1) coupon payments, (2) reinvestment income from coupons, and (3) capital gain or loss from selling before maturity. If held to maturity, the investor receives par value, and the "gain or loss" relative to purchase price is known at purchase — but the key third source is reinvestment income, not maturity proceeds.
>
> Note: For a bond held to maturity, the capital gain/loss is the difference between par and purchase price (pull-to-par effect), which is predetermined. The uncertain component is reinvestment income.

> [!tip]- 📖 Giải thích chi tiết
> Ba nguồn lợi nhuận từ trái phiếu:
> 1. **Coupon payments**: Thu nhập lãi định kỳ
> 2. **Reinvestment income**: Lãi từ tái đầu tư coupon
> 3. **Capital gain/loss**: Chênh lệch giá khi bán (trước đáo hạn)
>
> Khi giữ đến đáo hạn, nhà đầu tư nhận par value — khoản chênh lệch với giá mua đã xác định từ đầu. Rủi ro chính là reinvestment risk (lãi suất tái đầu tư coupon không chắc chắn).
>
> - **A là nguồn lợi nhuận**: Coupon là nguồn thu nhập chính.
> - **B đúng (không phải nguồn lợi nhuận "không chắc chắn")**: Với hold-to-maturity, capital gain/loss đã biết trước.
> - **C là nguồn lợi nhuận**: Reinvestment income là nguồn lợi nhuận quan trọng, đặc biệt với kỳ hạn dài.

---

## Question 2

For a fixed-rate bond, reinvestment risk and price risk are best described as:

- A. Positively correlated: both increase when interest rates rise.
- B. Offsetting: an increase in one tends to be accompanied by a decrease in the other.
- C. Independent: changes in interest rates affect one but not the other.

> [!answer]- Answer
> **B. Offsetting: an increase in one tends to be accompanied by a decrease in the other.**
>
> When interest rates rise, reinvestment income increases (higher rates on reinvested coupons) but the bond's market price decreases. Conversely, when rates fall, reinvestment income decreases but the bond's price increases. These two effects work in opposite directions.

> [!tip]- 📖 Giải thích chi tiết
> Reinvestment risk và price risk có tác động ngược chiều:
>
> | Lãi suất | Price risk | Reinvestment income |
> |----------|-----------|-------------------|
> | Tăng ↑ | Giá giảm ↓ | Thu nhập tái đầu tư tăng ↑ |
> | Giảm ↓ | Giá tăng ↑ | Thu nhập tái đầu tư giảm ↓ |
>
> - **A sai**: Chúng không cùng chiều — price risk tăng (giá giảm) khi reinvestment income tăng.
> - **B đúng**: Hai rủi ro bù trừ nhau, đây là cơ sở của chiến lược immunization.
> - **C sai**: Cả hai đều bị ảnh hưởng bởi thay đổi lãi suất.

---

## Question 3

Macaulay duration is best described as the:

- A. Percentage change in bond price for a 1% change in yield.
- B. Weighted average time to receipt of the bond's cash flows, with weights based on present values.
- C. Approximate number of years needed for reinvestment income to offset a change in bond price.

> [!answer]- Answer
> **B. Weighted average time to receipt of the bond's cash flows, with weights based on present values.**
>
> Macaulay duration measures the weighted average time until a bond's cash flows are received. The weight for each cash flow is its present value as a proportion of the bond's total present value (price).

> [!tip]- 📖 Giải thích chi tiết
> Macaulay duration = trung bình có trọng số của thời gian nhận dòng tiền, trọng số là PV của mỗi dòng tiền / giá trái phiếu.
>
> $$\text{MacDur} = \sum_{t=1}^{n} t \times \frac{PV(CF_t)}{P}$$
>
> - **A sai**: Đây là mô tả của modified duration (phần trăm thay đổi giá khi yield thay đổi 1%).
> - **B đúng**: Macaulay duration đo thời gian trung bình có trọng số (tính bằng năm).
> - **C sai**: Đây là diễn giải ứng dụng (immunization horizon) nhưng không phải định nghĩa chính thức.

---

## Question 4

An investor plans to hold a bond for a period equal to the bond's Macaulay duration. If interest rates change immediately after purchase by a parallel shift, the investor's total return will most likely be:

- A. Greater than the initial yield to maturity.
- B. Approximately equal to the initial yield to maturity.
- C. Less than the initial yield to maturity.

> [!answer]- Answer
> **B. Approximately equal to the initial yield to maturity.**
>
> This is the immunization condition. When the investment horizon equals the Macaulay duration, the reinvestment effect and price effect approximately offset each other for a one-time parallel shift in the yield curve, locking in the initial YTM.

> [!tip]- 📖 Giải thích chi tiết
> Điều kiện immunization: **Investment horizon = Macaulay duration**.
>
> Khi điều kiện này được thỏa mãn và lãi suất thay đổi song song (parallel shift) ngay sau khi mua:
> - Nếu lãi suất tăng: price loss ≈ reinvestment gain
> - Nếu lãi suất giảm: price gain ≈ reinvestment loss
> - Kết quả: Tổng lợi nhuận ≈ YTM ban đầu
>
> - **A sai**: Không nhất thiết lớn hơn YTM.
> - **B đúng**: Immunization "khóa" lợi nhuận gần bằng YTM ban đầu.
> - **C sai**: Không nhất thiết nhỏ hơn YTM.

---
