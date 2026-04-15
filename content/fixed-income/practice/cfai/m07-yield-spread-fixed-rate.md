---
type: practice
tags:
  - cfai-official
  - fixed-income
  - yield-spread-fixed-rate
source: "CFAI CFA1 FI Practice 2026"
module: "[[m07-yield-spread-fixed-rate]]"
---

# M07 – Yield & Spread for Fixed-Rate Bonds: CFAI Practice Problems

---

## Question 1

A bond has a stated annual yield of 6% compounded semiannually. The effective annual rate (EAR) is closest to:

- A. 6.00%
- B. 6.09%
- C. 6.18%

> [!answer]- Answer
> **B. 6.09%**
>
> $$\text{EAR} = \left(1 + \frac{0.06}{2}\right)^2 - 1 = (1.03)^2 - 1 = 1.0609 - 1 = 6.09\%$$

> [!tip]- 📖 Giải thích chi tiết
> EAR (lãi suất hiệu dụng hàng năm) phản ánh lợi suất thực tế khi tính đến hiệu ứng lãi kép. APR (annual percentage rate) không tính lãi kép.
>
> - **A sai**: 6.00% là APR (stated rate), chưa tính lãi kép.
> - **B đúng**: EAR = $(1 + 0.03)^2 - 1 = 6.09\%$.
> - **C sai**: Có thể nhầm với công thức ghép lãi khác tần suất.

---

## Question 2

A corporate bond has a yield to maturity of 5.50%, and a government benchmark bond with the same maturity has a yield of 3.80%. The G-spread on this corporate bond is closest to:

- A. 145 bps
- B. 170 bps
- C. 210 bps

> [!answer]- Answer
> **B. 170 bps**
>
> G-spread = Corporate bond YTM − Government benchmark YTM = 5.50% − 3.80% = 1.70% = 170 basis points.

> [!tip]- 📖 Giải thích chi tiết
> G-spread là chênh lệch lợi suất giữa trái phiếu doanh nghiệp và trái phiếu chính phủ cùng kỳ hạn. Đây là thước đo spread đơn giản nhất.
>
> - **A sai**: 145 bps không khớp phép tính 5.50% − 3.80%.
> - **B đúng**: G-spread = 550 bps − 380 bps = 170 bps.
> - **C sai**: 210 bps quá cao so với chênh lệch thực tế.
>
> **So sánh**: G-spread dùng benchmark chính phủ, trong khi I-spread dùng swap rate làm tham chiếu.

---

## Question 3

A bond analyst states: "The Z-spread is the constant spread that, when added to each spot rate on the government yield curve, makes the present value of the bond's cash flows equal to its market price." This statement is:

- A. Incorrect, because the Z-spread uses the par curve rather than the spot curve.
- B. Correct, and the Z-spread is always equal to the G-spread for any bond.
- C. Correct, and the Z-spread better captures the term structure compared to the G-spread.

> [!answer]- Answer
> **C. Correct, and the Z-spread better captures the term structure compared to the G-spread.**
>
> The Z-spread (zero-volatility spread) is the constant basis point spread added to each spot rate on the government spot curve so that the present value of a bond's cash flows equals its market price. It accounts for the shape of the term structure, unlike the G-spread which uses a single benchmark yield.

> [!tip]- 📖 Giải thích chi tiết
> Z-spread là spread cố định cộng vào mỗi spot rate trên đường cong lãi suất spot, sao cho PV của dòng tiền = giá thị trường.
>
> - **A sai**: Z-spread sử dụng spot curve, không phải par curve.
> - **B sai**: Z-spread và G-spread chỉ bằng nhau khi đường cong lãi suất phẳng (flat). Khi đường cong dốc, chúng khác nhau.
> - **C đúng**: Z-spread phản ánh hình dạng đường cong lãi suất tốt hơn G-spread vì dùng từng spot rate riêng biệt.

---

## Question 4

Compared to the Z-spread, the OAS (option-adjusted spread) for a callable bond is most likely:

- A. Higher, because the OAS adds the value of the embedded option to the Z-spread.
- B. Lower, because the OAS removes the cost of the embedded call option from the Z-spread.
- C. Equal, because embedded options do not affect yield spread measures.

> [!answer]- Answer
> **B. Lower, because the OAS removes the cost of the embedded call option from the Z-spread.**
>
> For a callable bond: Z-spread = OAS + Option cost. The call option has value to the issuer (cost to the investor), so the OAS strips out this option cost. Therefore, OAS < Z-spread for callable bonds.

> [!tip]- 📖 Giải thích chi tiết
> Công thức: **Z-spread = OAS + Option cost**
>
> - Với callable bond, quyền chọn mua có giá trị cho nhà phát hành → option cost > 0 → OAS < Z-spread.
> - Với putable bond, quyền chọn bán có giá trị cho nhà đầu tư → option cost < 0 → OAS > Z-spread.
>
> - **A sai**: OAS thấp hơn (không cao hơn) Z-spread cho callable bond.
> - **B đúng**: OAS loại bỏ chi phí quyền chọn, nên thấp hơn Z-spread.
> - **C sai**: Quyền chọn nhúng ảnh hưởng đáng kể đến spread.

---
