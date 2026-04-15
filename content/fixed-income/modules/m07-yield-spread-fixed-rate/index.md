---
title: "M07 — Yield Measures (Fixed)"
type: module
subject: fixed-income
module: M07
los:
  - 7.a: Calculate and interpret annual yield on a bond for varying compounding periods in a year
  - 7.b: Compare and contrast different yield and yield spread measures for fixed-rate bonds
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - yield
  - yield-spread
  - EAR
  - APR
  - G-spread
  - I-spread
  - Z-spread
  - OAS
---

# Yield and Yield Spread Measures for Fixed-Rate Bonds

## Chuyển đổi Yield theo năm

### Effective Annual Rate (EAR)

$$\text{EAR} = \left(1 + \frac{\text{APR}}{n}\right)^n - 1$$

trong đó $n$ = số kỳ ghép lãi trong một năm.

### Chuyển đổi APR giữa các kỳ hạn ghép lãi

Để chuyển đổi từ $m$ kỳ/năm sang $n$ kỳ/năm:

$$\left(1 + \frac{\text{APR}_m}{m}\right)^m = \left(1 + \frac{\text{APR}_n}{n}\right)^n$$

Giải cho $\text{APR}_n$:

$$\text{APR}_n = n \times \left[\left(1 + \frac{\text{APR}_m}{m}\right)^{m/n} - 1\right]$$

---

## Các thước đo Yield cho trái phiếu không có quyền chọn (Option-Free Bonds)

### Street Convention Yield (YTM)

- Yield-to-maturity tính dựa trên các khoản thanh toán coupon và gốc theo **lịch trình**
- Sử dụng quy ước tính ngày của trái phiếu (thường là 30/360 cho trái phiếu doanh nghiệp)
- Giả định tái đầu tư coupon ở mức YTM
- Loại yield được niêm yết phổ biến nhất trên thị trường

### True Yield

- Tương tự street convention yield nhưng sử dụng ngày thanh toán **thực tế** đã điều chỉnh theo lịch
- Tính đến các ngày cuối tuần/ngày lễ khiến thanh toán bị dời sang ngày làm việc tiếp theo
- True yield $\leq$ street convention yield (thanh toán trễ hơn làm giảm yield)

### Current Yield

$$\text{Current Yield} = \frac{\text{Annual Coupon Payment}}{\text{Current Bond Price}}$$

- Bỏ qua lãi/lỗ vốn và thu nhập từ tái đầu tư
- Thước đo đơn giản dựa trên thu nhập hiện tại

### Simple Yield

$$\text{Simple Yield} = \frac{\text{Annual Coupon} + \frac{\text{Par} - \text{Price}}{N}}{\text{Price}}$$

trong đó $N$ = số năm đến ngày đáo hạn. Bao gồm phần phân bổ tuyến tính (straight-line amortization) của lãi/lỗ.

---

## Các thước đo Yield cho trái phiếu có quyền chọn (Option-Embedded Bonds)

### Yield-to-Call (YTC)

- YTM được tính với giả định trái phiếu được thu hồi (called) tại **ngày call sớm nhất** theo call price
- Phù hợp với các trái phiếu callable đang giao dịch ở mức giá cao hơn mệnh giá (premium)

### Yield-to-Worst (YTW)

$$\text{YTW} = \min(\text{YTM}, \text{YTC}_1, \text{YTC}_2, \ldots)$$

- **Thấp nhất** trong tất cả các yield có thể có qua các ngày call và đáo hạn
- Thước đo thận trọng dùng để đánh giá rủi ro

### Option-Adjusted Yield

- Yield yêu cầu sau khi loại trừ giá trị của quyền chọn nhúng (embedded option)
- Với trái phiếu callable: option-adjusted yield > YTM (nhà đầu tư đang short quyền call)
- Với trái phiếu putable: option-adjusted yield < YTM (nhà đầu tư đang long quyền put)

---

## Government Equivalent Yield

Chuyển đổi yield của trái phiếu doanh nghiệp (quy ước ngày 30/360) sang yield tương đương trên cơ sở actual/actual, phù hợp với quy ước trái phiếu chính phủ. Điều này giúp so sánh trực tiếp (apples-to-apples) giữa trái phiếu doanh nghiệp và trái phiếu chính phủ.

---

## Các thước đo Yield Spread

### G-Spread (Government Spread)

$$\text{G-spread} = \text{YTM}_{\text{bond}} - \text{YTM}_{\text{government}}$$

- Spread so với yield của **trái phiếu chính phủ nội suy** cùng kỳ hạn
- Nominal spread đơn giản; không tính đến hình dạng của đường cong yield

### I-Spread (Interpolated Spread)

$$\text{I-spread} = \text{YTM}_{\text{bond}} - \text{Swap Rate}$$

- Spread so với **đường cong lãi suất hoán đổi (interest rate swap curve)** dựa trên MRR
- Hữu ích khi benchmark trái phiếu chính phủ kém thanh khoản hoặc bị méo mó

---

## Yield Spread so với Đường cong Benchmark

### Z-Spread (Zero-Volatility Spread)

Z-spread là **spread không đổi** cộng thêm vào mỗi spot rate trên đường cong benchmark sao cho giá trị hiện tại của các dòng tiền bằng giá thị trường của trái phiếu:

$$\text{Price} = \sum_{t=1}^{N} \frac{CF_t}{(1 + S_t + Z)^t}$$

- Tính đến **hình dạng** của toàn bộ cấu trúc kỳ hạn (term structure)
- Chính xác hơn G-spread hoặc I-spread
- Phù hợp với trái phiếu **không có quyền chọn (option-free)**

### Option-Adjusted Spread (OAS)

$$\text{OAS} = \text{Z-spread} - \text{Option Value (in spread terms)}$$

| Loại trái phiếu | Quan hệ |
|-----------|-------------|
| Trái phiếu option-free | OAS = Z-spread |
| Trái phiếu callable | OAS < Z-spread (option value > 0 với tổ chức phát hành) |
| Trái phiếu putable | OAS > Z-spread (option value > 0 với nhà đầu tư) |

- OAS loại bỏ ảnh hưởng của quyền chọn nhúng
- Đại diện cho spread phản ánh **rủi ro tín dụng và rủi ro thanh khoản** mà thôi
- Dùng để so sánh các trái phiếu có quyền chọn khác nhau trên cùng một cơ sở

---

## Tổng hợp các Quan hệ Chính

| Thước đo | Benchmark | Tính đến hình dạng đường cong? | Tính đến quyền chọn? |
|---------|-----------|--------------------------|----------------------|
| G-spread | Government YTM | Không | Không |
| I-spread | Swap rate | Không | Không |
| Z-spread | Spot rate curve | Có | Không |
| OAS | Spot rate curve | Có | Có |

---

## Xem thêm

- [[fixed-income/m06-bond-valuation/index|M06 - Bond Valuation]]
- [[fixed-income/m08-yield-spread-floating-rate/index|M08 - Yield Spread for Floating-Rate Notes]]
- [[fixed-income/m09-term-structure/index|M09 - Term Structure]]