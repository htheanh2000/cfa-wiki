---
title: Bond Valuation
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [bond-pricing, present-value, yield, premium, discount, accrued-interest]
---

# Bond Valuation

## Nguyên Tắc Định Giá Cơ Bản

Giá trị của một trái phiếu bằng **giá trị hiện tại của các dòng tiền kỳ vọng trong tương lai**, được chiết khấu theo market discount rate (required yield).

**Công thức định giá trái phiếu:**

$$PV = \sum_{t=1}^{n} \frac{PMT}{(1+r)^t} + \frac{FV}{(1+r)^n}$$

trong đó:
- $PV$ = giá trái phiếu (present value)
- $PMT$ = khoản thanh toán coupon định kỳ
- $FV$ = mệnh giá (face/par value)
- $r$ = market discount rate theo từng kỳ
- $n$ = số kỳ đến khi đáo hạn

## Mối Quan Hệ Giá — Yield

### Quan Hệ Nghịch Chiều
- Khi yield **tăng**, giá trái phiếu **giảm**
- Khi yield **giảm**, giá trái phiếu **tăng**

### Convexity của Đường Cong Price-Yield
- Mối quan hệ này **không tuyến tính** — mà có dạng **convex**
- Với cùng một mức thay đổi yield:
  - Mức **tăng** giá khi yield giảm **lớn hơn**
  - Mức **giảm** giá khi yield tăng cùng biên độ

### Các Tính Chất Quan Trọng
1. Giá trái phiếu có quan hệ **nghịch chiều** với market discount rate
2. Với cùng coupon rate, **maturity càng dài** → độ nhạy giá với sự thay đổi yield càng lớn
3. Với cùng maturity, **coupon càng thấp** → độ nhạy giá với sự thay đổi yield càng lớn
4. Phần trăm thay đổi giá **lớn hơn** khi yield giảm so với khi yield tăng cùng biên độ (hiệu ứng convexity)

## Premium, Par và Discount Bonds

| Điều kiện | Trái phiếu giao dịch ở mức | Hiệu ứng theo thời gian |
|-----------|---------------------------|------------------------|
| Coupon rate > Market rate | **Premium** (Giá > Par) | "Pull to par" — giá giảm dần về par |
| Coupon rate = Market rate | **Par** (Giá = Par) | Giá duy trì ở mức par |
| Coupon rate < Market rate | **Discount** (Giá < Par) | "Pull to par" — giá tăng dần về par |

**Constant-yield price trajectory**: Khi trái phiếu tiến gần đến ngày đáo hạn, giá của nó hội tụ về mệnh giá par (giả định không có vỡ nợ).

## Accrued Interest

Khi một trái phiếu được giao dịch giữa hai ngày trả coupon, người mua phải bồi hoàn cho người bán phần lãi đã tích lũy nhưng chưa được nhận.

**Công thức Accrued Interest:**

$$AI = PMT \times \frac{t}{T}$$

trong đó:
- $AI$ = accrued interest (lãi tích lũy)
- $PMT$ = khoản coupon của kỳ đó
- $t$ = số ngày kể từ lần trả coupon gần nhất
- $T$ = tổng số ngày trong kỳ coupon

### Các Quy Ước Day Count

| Quy ước | Mô tả | Sử dụng phổ biến |
|---------|-------|-----------------|
| **Actual/Actual** | Số ngày thực tế / Số ngày thực tế trong kỳ | Trái phiếu chính phủ |
| **30/360** | Giả định mỗi tháng 30 ngày / năm 360 ngày | Trái phiếu doanh nghiệp |
| **Actual/360** | Số ngày thực tế / năm 360 ngày | Công cụ thị trường tiền tệ |
| **Actual/365** | Số ngày thực tế / năm 365 ngày | Một số thị trường |

## Full Price và Flat (Clean) Price

$$\text{Full Price (Dirty Price)} = \text{Flat Price (Clean Price)} + \text{Accrued Interest}$$

- **Full price** (dirty price, invoice price): Mức giá người mua thực sự phải trả
- **Flat price** (clean price, quoted price): Mức giá được niêm yết trên thị trường

**Tính full price giữa hai ngày trả coupon:**

$$PV^{\text{Full}} = PV \times (1 + r)^{t/T}$$

trong đó $PV$ là giá trị tại ngày trả coupon gần nhất, $t/T$ là tỷ lệ phần kỳ đã trôi qua.

Hoặc theo cách khác:

$$PV^{\text{Full}} = \sum_{t=1}^{n} \frac{PMT}{(1+r)^{t - t/T}} + \frac{FV}{(1+r)^{n - t/T}}$$

## Matrix Pricing

Khi một trái phiếu không được giao dịch thường xuyên, giá của nó có thể được ước tính dựa trên yield của các **trái phiếu có thể so sánh** đang được giao dịch:
- Đối chiếu theo chất lượng tín dụng, maturity, coupon rate và các embedded options
- Nội suy yield từ các trái phiếu tương tự đang giao dịch
- Hữu ích cho các trái phiếu kém thanh khoản và private placements

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/yield-measures|Yield Measures]]
- [[fixed-income/concepts/duration|Duration]]
- [[fixed-income/concepts/convexity|Convexity]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m06|Glossary: Module 06]]