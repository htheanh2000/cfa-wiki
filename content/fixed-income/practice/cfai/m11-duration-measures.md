---
type: practice
tags:
  - cfai-official
  - fixed-income
  - duration-measures
source: "CFAI CFA1 FI Practice 2026"
module: "[[m11-duration-measures]]"
---

# M11 – Yield-Based Bond Duration Measures: CFAI Practice Problems

---

## Question 1

A bond has a Macaulay duration of 7.2 years and a yield to maturity of 5% (compounded semiannually). The modified duration of this bond is closest to:

- A. 6.86
- B. 7.02
- C. 7.20

> [!answer]- Answer
> **B. 7.02**
>
> $$\text{ModDur} = \frac{\text{MacDur}}{1 + \frac{r}{m}} = \frac{7.2}{1 + \frac{0.05}{2}} = \frac{7.2}{1.025} = 7.024 \approx 7.02$$

> [!tip]- 📖 Giải thích chi tiết
> Modified duration được tính từ Macaulay duration bằng cách chia cho $(1 + r/m)$, trong đó $r$ là YTM và $m$ là số kỳ trả coupon trong năm.
>
> - **A sai**: 6.86 có thể tính nhầm chia cho $(1 + 0.05)$ thay vì $(1 + 0.025)$.
> - **B đúng**: ModDur = 7.2 / 1.025 = 7.02 (dùng periodic yield 2.5%).
> - **C sai**: 7.20 là Macaulay duration, chưa điều chỉnh.

---

## Question 2

A bond has a full price of $1,025 at a yield of 5.00%, a price of $1,060 if the yield decreases by 25 bps, and a price of $991 if the yield increases by 25 bps. The approximate modified duration of this bond is closest to:

- A. 6.73
- B. 13.46
- C. 27.32

> [!answer]- Answer
> **B. 13.46**
>
> $$\text{ApproxModDur} = \frac{P_{-} - P_{+}}{2 \times \Delta y \times P_0} = \frac{1{,}060 - 991}{2 \times 0.0025 \times 1{,}025} = \frac{69}{5.125} = 13.46$$

> [!tip]- 📖 Giải thích chi tiết
> Công thức approximate modified duration sử dụng hai giá trái phiếu khi yield thay đổi đều nhau lên và xuống.
>
> - $P_{-} = 1{,}060$ (giá khi yield giảm 25 bps)
> - $P_{+} = 991$ (giá khi yield tăng 25 bps)
> - $P_0 = 1{,}025$ (giá ban đầu)
> - $\Delta y = 0.0025$ (25 bps)
>
> - **A sai**: 6.73 = 13.46/2, có thể nhầm quên nhân 2 ở mẫu số.
> - **B đúng**: ApproxModDur = 69 / 5.125 = 13.46.
> - **C sai**: 27.32 có thể quên chia cho $P_0$ hoặc nhân sai.

---

## Question 3

A bond portfolio manager wants to estimate the price change for a small yield increase. A bond with a modified duration of 8.5 and a current price of $1,040 experiences a yield increase of 30 bps. The approximate price change is closest to:

- A. −$26.52
- B. −$27.30
- C. −$35.10

> [!answer]- Answer
> **A. −$26.52**
>
> $$\%\Delta P \approx -\text{ModDur} \times \Delta y = -8.5 \times 0.0030 = -0.0255 = -2.55\%$$
> $$\Delta P = -2.55\% \times \$1{,}040 = -\$26.52$$

> [!tip]- 📖 Giải thích chi tiết
> Duration ước lượng tuyến tính sự thay đổi giá khi yield thay đổi nhỏ.
>
> - Phần trăm thay đổi giá = −ModDur × Δy = −8.5 × 0.003 = −2.55%
> - Thay đổi giá tuyệt đối = −2.55% × $1,040 = **−$26.52**
>
> - **A đúng**: Tính chính xác −8.5 × 0.003 × $1,040.
> - **B sai**: Có thể nhầm cách tính hoặc dùng sai Δy.
> - **C sai**: Có thể dùng nhầm Δy = 0.0035 hoặc tính sai.

---

## Question 4

All else being equal, modified duration is highest for a bond with:

- A. A high coupon rate, long maturity, and low yield to maturity.
- B. A low coupon rate, long maturity, and low yield to maturity.
- C. A low coupon rate, short maturity, and high yield to maturity.

> [!answer]- Answer
> **B. A low coupon rate, long maturity, and low yield to maturity.**
>
> Duration is higher when: (1) coupon rate is lower (more weight on the final payment), (2) maturity is longer (cash flows received later), and (3) yield is lower (distant cash flows have higher present values).

> [!tip]- 📖 Giải thích chi tiết
> Ba yếu tố ảnh hưởng đến duration:
>
> | Yếu tố | Tác động lên Duration |
> |--------|---------------------|
> | Coupon rate ↓ | Duration ↑ (nhiều trọng số hơn ở dòng tiền cuối cùng) |
> | Maturity ↑ | Duration ↑ (dòng tiền nhận muộn hơn) |
> | YTM ↓ | Duration ↑ (PV dòng tiền xa tăng tương đối) |
>
> - **A sai**: Coupon cao làm giảm duration.
> - **B đúng**: Kết hợp cả ba yếu tố làm tăng duration tối đa.
> - **C sai**: Maturity ngắn và yield cao đều làm giảm duration.

---
