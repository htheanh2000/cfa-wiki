---
type: practice
tags:
  - cfai-official
  - fixed-income
  - curve-based-risk
source: "CFAI CFA1 FI Practice 2026"
module: "[[m13-curve-based-risk]]"
---

# M13 – Curve-Based & Empirical Fixed-Income Risk Measures: CFAI Practice Problems

---

## Question 1

Effective duration differs from modified duration primarily because effective duration:

- A. Uses a larger yield change to calculate price sensitivity.
- B. Accounts for changes in cash flows as yields change, making it suitable for bonds with embedded options.
- C. Is always smaller than modified duration for option-free bonds.

> [!answer]- Answer
> **B. Accounts for changes in cash flows as yields change, making it suitable for bonds with embedded options.**
>
> Modified duration assumes cash flows do not change when yields change, which is invalid for bonds with embedded options (callable, putable). Effective duration uses a valuation model that allows cash flows to change with interest rate shifts, making it the appropriate measure for bonds with embedded options.

> [!tip]- 📖 Giải thích chi tiết
> So sánh Modified Duration vs Effective Duration:
>
> | | Modified Duration | Effective Duration |
> |--|------------------|-------------------|
> | Cash flows | Cố định | Có thể thay đổi |
> | Phù hợp với | Option-free bonds | Tất cả bonds (kể cả có embedded options) |
> | Dựa trên | YTM | Benchmark yield curve shift |
>
> - **A sai**: Kích thước yield change không phải điểm khác biệt chính.
> - **B đúng**: Effective duration cho phép dòng tiền thay đổi khi lãi suất thay đổi.
> - **C sai**: Với option-free bonds, effective duration ≈ modified duration.

---

## Question 2

A portfolio manager is concerned about the impact of a steepening yield curve on a bond portfolio. The most appropriate risk measure to assess this exposure is:

- A. Modified duration.
- B. Key rate duration.
- C. Effective convexity.

> [!answer]- Answer
> **B. Key rate duration.**
>
> Key rate duration (partial duration) measures a bond's sensitivity to changes in yields at specific maturities along the curve. This allows assessment of non-parallel shifts like curve steepening or flattening, which modified duration (a single number assuming parallel shifts) cannot capture.

> [!tip]- 📖 Giải thích chi tiết
> Key rate duration đo độ nhạy cảm của giá trái phiếu với sự thay đổi lãi suất tại từng điểm trên đường cong.
>
> - **A sai**: Modified duration chỉ đo tác động của parallel shift (dịch chuyển song song), không phản ánh steepening/flattening.
> - **B đúng**: Key rate duration phân tích tác động tại từng kỳ hạn cụ thể → phù hợp phân tích curve risk.
> - **C sai**: Effective convexity đo tính phi tuyến của quan hệ giá-yield, không đo riêng curve risk.

---

## Question 3

An analyst uses regression analysis to estimate the relationship between a corporate bond's price changes and changes in a government benchmark yield. This approach produces:

- A. Analytical duration, derived from mathematical formulas.
- B. Empirical duration, estimated from historical market data.
- C. Effective duration, calculated from an option pricing model.

> [!answer]- Answer
> **B. Empirical duration, estimated from historical market data.**
>
> Empirical duration is estimated by running a regression of bond price changes against benchmark yield changes using historical data. Unlike analytical duration (from formulas) or effective duration (from models), empirical duration captures real-world relationships including credit spread changes that may correlate with interest rate movements.

> [!tip]- 📖 Giải thích chi tiết
> Ba loại duration:
>
> - **Analytical duration**: Tính từ công thức toán học (Macaulay, Modified)
> - **Effective duration**: Tính từ mô hình định giá (cho bonds có embedded options)
> - **Empirical duration**: Ước lượng từ dữ liệu thị trường thực tế bằng hồi quy
>
> - **A sai**: Analytical duration dùng công thức, không dùng regression.
> - **B đúng**: Regression trên dữ liệu lịch sử → empirical duration.
> - **C sai**: Effective duration dùng option pricing model, không dùng regression.

---

## Question 4

Effective convexity is most important for valuing bonds that:

- A. Have fixed cash flows and long maturities.
- B. Have embedded options that cause cash flows to change with interest rates.
- C. Are zero-coupon bonds with high sensitivity to yield changes.

> [!answer]- Answer
> **B. Have embedded options that cause cash flows to change with interest rates.**
>
> Effective convexity, like effective duration, is calculated using a model that allows cash flows to vary with interest rates. It is essential for bonds with embedded options (callable, putable, MBS) where cash flow patterns change as rates move, potentially creating negative convexity.

> [!tip]- 📖 Giải thích chi tiết
> Effective convexity quan trọng nhất cho trái phiếu có embedded options vì:
>
> - Dòng tiền thay đổi theo lãi suất → yield-based convexity không chính xác
> - Callable bonds có thể có negative convexity ở vùng yield thấp
> - MBS có prepayment risk làm dòng tiền phụ thuộc vào lãi suất
>
> - **A sai**: Option-free bonds dùng yield-based (modified) convexity là đủ.
> - **B đúng**: Embedded options làm dòng tiền thay đổi → cần effective convexity.
> - **C sai**: Zero-coupon bonds không có embedded options, yield-based convexity phù hợp.

---
