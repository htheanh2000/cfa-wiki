---
type: practice
tags:
  - cfai-official
  - fixed-income
  - yield-spread-floating-rate
source: "CFAI CFA1 FI Practice 2026"
module: "[[m08-yield-spread-floating-rate]]"
---

# M08 – Yield & Spread for Floating-Rate Notes: CFAI Practice Problems

---

## Question 1

A floating-rate note (FRN) was issued at par with a quoted margin of 200 bps over a reference rate. Since issuance, the issuer's credit quality has deteriorated and the market now requires a discount margin of 250 bps. The FRN is most likely trading:

- A. At par, because the reference rate resets periodically.
- B. At a premium, because the quoted margin exceeds current expectations.
- C. At a discount, because the discount margin exceeds the quoted margin.

> [!answer]- Answer
> **C. At a discount, because the discount margin exceeds the quoted margin.**
>
> When the required discount margin exceeds the quoted (fixed) margin, the FRN's coupon payments are insufficient to compensate investors for the credit risk, causing the bond to trade below par.

> [!tip]- 📖 Giải thích chi tiết
> Với FRN, giá so với par phụ thuộc vào quan hệ giữa quoted margin và discount margin:
>
> - Discount margin > Quoted margin → giá < par (discount)
> - Discount margin < Quoted margin → giá > par (premium)
> - Discount margin = Quoted margin → giá = par
>
> - **A sai**: Dù reference rate reset, spread cố định nên giá vẫn bị ảnh hưởng khi tín dụng thay đổi.
> - **B sai**: Quoted margin thấp hơn yêu cầu thị trường → giá giảm, không tăng.
> - **C đúng**: Thị trường yêu cầu 250 bps nhưng chỉ nhận được 200 bps → giá giảm dưới par.

---

## Question 2

A money market instrument with a face value of $100,000 is quoted at a bank discount yield of 3.60% and has 90 days to maturity. The purchase price of this instrument is closest to:

- A. $99,000
- B. $99,100
- C. $99,112

> [!answer]- Answer
> **B. $99,100**
>
> $$\text{Price} = \text{Face Value} \times \left(1 - \frac{D_r \times t}{360}\right) = 100{,}000 \times \left(1 - \frac{0.036 \times 90}{360}\right) = 100{,}000 \times 0.991 = \$99{,}100$$

> [!tip]- 📖 Giải thích chi tiết
> Bank discount yield (BDY) tính lợi suất dựa trên mệnh giá (face value), không phải giá mua, và sử dụng quy ước 360 ngày.
>
> - Discount = $100,000 × 0.036 × (90/360) = $900
> - Price = $100,000 − $900 = **$99,100**
>
> - **A sai**: $99,000 tương ứng discount $1,000 — tính sai.
> - **B đúng**: Áp dụng đúng công thức BDY.
> - **C sai**: Có thể nhầm với money market yield (tính trên giá mua).

---

## Question 3

An analyst needs to convert a bank discount yield to a money market yield. Compared to the bank discount yield, the money market yield for the same instrument will most likely be:

- A. Lower, because the money market yield uses a smaller denominator.
- B. Higher, because the money market yield is based on the purchase price rather than face value.
- C. Equal, because both yields use the same 360-day convention.

> [!answer]- Answer
> **B. Higher, because the money market yield is based on the purchase price rather than face value.**
>
> $$r_{MM} = \frac{360 \times r_{BD}}{360 - (r_{BD} \times t)}$$
>
> The money market yield uses the purchase price (which is less than face value) as the denominator, producing a higher yield than the bank discount yield.

> [!tip]- 📖 Giải thích chi tiết
> Bank discount yield tính return trên face value, trong khi money market yield tính return trên purchase price (giá mua).
>
> - Vì purchase price < face value → cùng một khoản lãi nhưng chia cho mẫu số nhỏ hơn → money market yield > bank discount yield.
>
> - **A sai**: Mẫu số nhỏ hơn (purchase price) tạo ra yield cao hơn, không thấp hơn.
> - **B đúng**: Money market yield dùng purchase price làm cơ sở → yield cao hơn BDY.
> - **C sai**: Dù cả hai dùng 360 ngày, cơ sở tính (face value vs purchase price) khác nhau.

---

## Question 4

An FRN resets its coupon quarterly based on a reference rate. On the coupon reset date, the quoted margin equals the required discount margin. The FRN's price on this reset date is most likely:

- A. Above par value.
- B. Equal to par value.
- C. Below par value.

> [!answer]- Answer
> **B. Equal to par value.**
>
> At a reset date, the FRN's coupon adjusts to the current reference rate. If the quoted margin equals the discount margin required by the market, the FRN provides exactly the return demanded by investors, so it trades at par.

> [!tip]- 📖 Giải thích chi tiết
> Tại ngày reset, coupon của FRN được cập nhật theo lãi suất tham chiếu hiện tại. Nếu quoted margin = discount margin:
>
> - FRN trả đúng mức lợi suất thị trường yêu cầu
> - Không có lý do để giá lệch khỏi par
> - Giá = Par value
>
> - **A sai**: Giá > par chỉ khi quoted margin > discount margin.
> - **B đúng**: Quoted margin = discount margin tại ngày reset → giá = par.
> - **C sai**: Giá < par chỉ khi quoted margin < discount margin.

---
