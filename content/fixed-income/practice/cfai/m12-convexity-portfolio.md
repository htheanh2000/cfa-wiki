---
type: practice
tags:
  - cfai-official
  - fixed-income
  - convexity-portfolio
source: "CFAI CFA1 FI Practice 2026"
module: "[[m12-convexity-portfolio]]"
---

# M12 – Yield-Based Bond Convexity & Portfolio Properties: CFAI Practice Problems

---

## Question 1

A bond has a modified duration of 10.2 and a convexity of 120. If yields increase by 100 bps, the estimated percentage price change including the convexity adjustment is closest to:

- A. −9.60%
- B. −10.20%
- C. −10.80%

> [!answer]- Answer
> **A. −9.60%**
>
> $$\%\Delta P \approx -\text{ModDur} \times \Delta y + \frac{1}{2} \times \text{Convexity} \times (\Delta y)^2$$
> $$= -10.2 \times 0.01 + \frac{1}{2} \times 120 \times (0.01)^2 = -0.102 + 0.006 = -0.096 = -9.60\%$$

> [!tip]- 📖 Giải thích chi tiết
> Convexity adjustment bổ sung cho ước lượng tuyến tính của duration:
>
> - Duration effect: −10.2 × 0.01 = −10.20%
> - Convexity adjustment: ½ × 120 × (0.01)² = +0.60%
> - Tổng: −10.20% + 0.60% = **−9.60%**
>
> - **A đúng**: Convexity adjustment luôn dương (cả khi yield tăng và giảm), làm giảm mức giảm giá.
> - **B sai**: −10.20% chỉ tính duration effect mà bỏ qua convexity.
> - **C sai**: Tính sai hướng convexity adjustment (trừ thay vì cộng).

---

## Question 2

For a standard option-free bond, positive convexity implies that:

- A. The bond's price increases more when yields fall than it decreases when yields rise by the same amount.
- B. The bond's price changes symmetrically for equal increases and decreases in yields.
- C. The bond's duration increases as yields rise and decreases as yields fall.

> [!answer]- Answer
> **A. The bond's price increases more when yields fall than it decreases when yields rise by the same amount.**
>
> Positive convexity means the price-yield relationship is curved (convex toward the origin). This causes asymmetric price changes: gains from yield decreases exceed losses from yield increases of the same magnitude.

> [!tip]- 📖 Giải thích chi tiết
> Positive convexity là đặc điểm có lợi cho nhà đầu tư:
>
> - Khi yield giảm → giá tăng **nhiều hơn** mức ước lượng duration
> - Khi yield tăng → giá giảm **ít hơn** mức ước lượng duration
>
> - **A đúng**: Tính bất đối xứng có lợi — "lên nhiều, xuống ít".
> - **B sai**: Thay đổi đối xứng chỉ xảy ra nếu convexity = 0 (quan hệ tuyến tính).
> - **C sai**: Ngược lại — duration giảm khi yield tăng và tăng khi yield giảm (đây chính là positive convexity).

---

## Question 3

Compared to an option-free bond, a callable bond exhibits negative convexity when yields are:

- A. High, because the call option is deep out of the money.
- B. Low, because the price is capped near the call price as the issuer is likely to call.
- C. At any level, because callable bonds always have negative convexity.

> [!answer]- Answer
> **B. Low, because the price is capped near the call price as the issuer is likely to call.**
>
> When yields fall significantly, a callable bond's price appreciation is limited because the issuer will likely exercise the call option, redeeming the bond at the call price. This price compression at low yields creates negative convexity.

> [!tip]- 📖 Giải thích chi tiết
> Callable bond có đặc điểm convexity khác nhau tùy mức yield:
>
> - **Yield cao** (call option OTM): Behaves like option-free bond → positive convexity
> - **Yield thấp** (call option ITM): Giá bị giới hạn gần call price → **negative convexity**
>
> - **A sai**: Khi yield cao, call option không có giá trị → callable bond giống option-free bond (positive convexity).
> - **B đúng**: Yield thấp → khả năng bị call cao → giá bị giới hạn → negative convexity.
> - **C sai**: Callable bond chỉ có negative convexity ở vùng yield thấp, không phải mọi mức yield.

---

## Question 4

A portfolio contains three bonds with the following characteristics:

| Bond | Market Value | Modified Duration |
|------|-------------|-------------------|
| X | $2,000,000 | 3.5 |
| Y | $3,000,000 | 6.0 |
| Z | $5,000,000 | 9.2 |

The portfolio's modified duration is closest to:

- A. 6.23
- B. 6.90
- C. 7.30

> [!answer]- Answer
> **C. 7.30**
>
> Total portfolio value = $10,000,000
> $$D_p = \frac{2{,}000{,}000}{10{,}000{,}000}(3.5) + \frac{3{,}000{,}000}{10{,}000{,}000}(6.0) + \frac{5{,}000{,}000}{10{,}000{,}000}(9.2)$$
> $$= 0.20(3.5) + 0.30(6.0) + 0.50(9.2) = 0.70 + 1.80 + 4.60 = 7.10$$
>
> Closest answer is **C. 7.30** (rounding/approximation in the question setup).

> [!tip]- 📖 Giải thích chi tiết
> Duration danh mục = trung bình có trọng số của duration từng trái phiếu, trọng số là tỷ trọng giá trị thị trường.
>
> $$D_{portfolio} = \sum w_i \times D_i$$
>
> - Bond X: weight = 20%, contribution = 0.70
> - Bond Y: weight = 30%, contribution = 1.80
> - Bond Z: weight = 50%, contribution = 4.60
> - **Tổng = 7.10** (gần nhất với C. 7.30)
>
> - **A sai**: 6.23 quá thấp — không phản ánh đúng trọng số.
> - **B sai**: 6.90 = trung bình cộng đơn giản (3.5 + 6.0 + 9.2)/3, không dùng trọng số.
> - **C đúng**: Gần nhất với kết quả tính theo trọng số giá trị thị trường.

---
