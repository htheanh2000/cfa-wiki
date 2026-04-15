---
title: "M07 — Swaps Pricing"
type: module
subject: derivatives
module: M07
los: "7.a-7.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m07
  - swaps
  - interest-rate-swaps
  - pricing
  - valuation
  - par-swap-rate
---

# M07: Swaps Pricing and Valuation

> **LOS 7.a**: Mô tả sự tương đồng và khác biệt giữa hợp đồng swap và một chuỗi hợp đồng forward.
> **LOS 7.b**: Phân biệt giá trị (value) và giá (price) của swaps.

## 1. Swaps vs Forwards

### Điểm tương đồng

| Đặc điểm | Cả Swaps và Forwards |
|---------|------------------------|
| Loại | Forward commitments |
| Cấu trúc lợi nhuận | Đối xứng (cả hai bên đều có thể lãi/lỗ) |
| Giá trị ban đầu | $V_0 = 0$ tại thời điểm khởi tạo |
| Rủi ro đối tác | Cả hai đều tiềm ẩn credit risk |

### Điểm khác biệt

| Đặc điểm | Swap | Forward |
|---------|------|---------|
| Dòng tiền | **Chuỗi** thanh toán định kỳ | **Một** khoản thanh toán duy nhất khi đáo hạn |
| Thời điểm thanh toán | Vào **đầu** mỗi kỳ | Vào **cuối** (ngày đáo hạn) |
| Lãi suất cố định | **Cùng một mức cố định** xuyên suốt tất cả các kỳ | **Khác nhau** cho mỗi kỳ đáo hạn |

## 2. Swap như một Chuỗi Off-Market Forwards

Swap tương đương với một **chuỗi các FRA (forward rate agreements)**, mỗi FRA có **cùng lãi suất cố định** nhưng bao phủ **các kỳ forward khác nhau** với các implied forward rates (IFRs) khác nhau.

- Mỗi FRA riêng lẻ trong chuỗi là **off-market** — tự nó không có giá trị bằng không
- Một số FRA có **giá trị dương** (lãi suất cố định > IFR cho kỳ đó), một số có **giá trị âm** (lãi suất cố định < IFR)
- **Tổng giá trị của tất cả FRA bằng không** tại thời điểm khởi tạo

> **Điểm mấu chốt**: Lãi suất cố định của swap là **bình quân gia quyền** của các forward rates riêng lẻ. Đây là mức lãi suất duy nhất khiến toàn bộ gói FRA có net present value bằng không.

## 3. Thanh Toán Định Kỳ (Periodic Settlement)

Tại mỗi ngày thanh toán, khoản thanh toán định kỳ được tính như sau:

$$\text{Periodic Settlement} = (\text{MRR}_n - F) \times \text{Notional} \times \text{Period}$$

trong đó:
- $\text{MRR}_n$ = market reference rate quan sát tại kỳ $n$
- $F$ = lãi suất cố định của swap (par swap rate)
- $\text{Notional}$ = mệnh giá danh nghĩa
- $\text{Period}$ = phân số tính ngày (ví dụ: $90/360$)

Nếu kết quả **dương**, bên trả lãi suất cố định (fixed-rate payer) **nhận** khoản thanh toán ròng. Nếu **âm**, fixed-rate payer **trả** khoản ròng đó.

## 4. Par Swap Rate (Xác Định Lãi Suất Cố Định)

Par swap rate là lãi suất cố định $F$ khiến giá trị swap bằng không tại thời điểm khởi tạo. Nó được tìm bằng cách đặt:

$$PV(\text{floating payments}) = PV(\text{fixed payments})$$

### Công Thức Lãi Suất Cố Định Theo No-Arbitrage

Sử dụng spot (zero) rates $z_i$ cho mỗi kỳ:

$$\sum_{i=1}^{N} \frac{\text{MRR}_i}{(1 + z_i)^i} = \sum_{i=1}^{N} \frac{F}{(1 + z_i)^i}$$

Giải ra $F$:

$$F = \frac{\sum_{i=1}^{N} \frac{\text{MRR}_i}{(1 + z_i)^i}}{\sum_{i=1}^{N} \frac{1}{(1 + z_i)^i}}$$

trong đó:
- $\text{MRR}_i$ = implied forward rate cho kỳ $i$
- $z_i$ = spot rate cho kỳ đáo hạn $i$
- $N$ = tổng số kỳ thanh toán

Tương đương, sử dụng discount factors $DF_i = \frac{1}{(1+z_i)^i}$:

$$F = \frac{1 - DF_N}{\sum_{i=1}^{N} DF_i}$$

## 5. Giá Trị Swap Trong Suốt Vòng Đời

### Tại Thời Điểm Khởi Tạo

$$V_0 = 0$$

### Trong Suốt Vòng Đời Swap

Giá trị swap bằng **khoản thanh toán hiện tại** (nếu có) cộng với **giá trị hiện tại của các khoản thanh toán tương lai còn lại** dựa trên cấu trúc lãi suất mới:

$$V_t = \text{Current Settlement} + \sum_{i=t+1}^{N} \frac{(\text{MRR}_i^{\text{new}} - F) \times \text{Notional} \times \text{Period}}{(1 + z_i^{\text{new}})^{i-t}}$$

trong đó:
- $\text{MRR}_i^{\text{new}}$ = các implied forward rates mới từ cấu trúc lãi suất cập nhật
- $z_i^{\text{new}}$ = spot rates mới

> **Lưu ý**: Khi lãi suất thay đổi, PV của các khoản thanh toán cố định còn lại sẽ khác với PV của các khoản thanh toán thả nổi còn lại, tạo ra giá trị swap khác không.

## 6. Swaps và Fixed-Income Exposure

| Vị thế | Hưởng lợi khi | Exposure tương đương |
|----------|-----------|-------------------|
| **Fixed-rate payer** (nhận floating) | Lãi suất **tăng** | Short trái phiếu lãi suất cố định, long trái phiếu lãi suất thả nổi |
| **Floating-rate payer** (nhận fixed) | Lãi suất **giảm** | Long trái phiếu lãi suất cố định, short trái phiếu lãi suất thả nổi |

> **Điểm mấu chốt**: Tham gia vào swap pay-fixed, receive-floating về mặt kinh tế tương tự với **vay ở lãi suất cố định và cho vay ở lãi suất thả nổi** — có lợi khi lãi suất tăng.

---

**Xem thêm**: [[derivatives/modules/m06-futures-pricing-valuation/index|M06: Futures Pricing and Valuation]], [[derivatives/modules/m08-options-pricing-valuation/index|M08: Options Pricing and Valuation]]

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]]