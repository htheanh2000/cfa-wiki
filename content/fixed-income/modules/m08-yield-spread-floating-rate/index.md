---
title: "M08 — Yield Measures (Float)"
type: module
subject: fixed-income
module: M08
los:
  - 8.a: Calculate and interpret yield and yield spread measures for floating-rate notes
  - 8.b: Calculate and interpret yield measures for money market instruments
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - floating-rate
  - FRN
  - discount-margin
  - money-market
  - bank-discount-yield
---

# Yield and Yield Spread Measures for Floating-Rate Instruments

## Định Giá Floating-Rate Note (FRN)

### Cấu Trúc Coupon

$$\text{Coupon Rate} = \text{MRR} + \text{Quoted Margin (QM)}$$

trong đó MRR = Market Reference Rate (ví dụ: SOFR, Euribor).

**Quoted margin** được xác định tại thời điểm phát hành và giữ nguyên trong suốt vòng đời của FRN.

### Discount Margin (DM)

**Discount margin** (còn gọi là required margin) là spread trên MRR mà thị trường hiện tại yêu cầu. Đây là yield spread làm cho giá FRN bằng với giá trị hiện tại của các dòng tiền kỳ vọng:

$$\text{PV} = \sum_{t=1}^{N} \frac{(\text{MRR} + \text{QM}) \times \frac{\text{FV}}{m}}{(1 + \frac{\text{MRR} + \text{DM}}{m})^t} + \frac{\text{FV}}{(1 + \frac{\text{MRR} + \text{DM}}{m})^N}$$

trong đó $m$ = số lần trả coupon mỗi năm.

---

## Chất Lượng Tín Dụng và Định Giá FRN

| Tình huống | Mối quan hệ | Giá |
|----------|-------------|-------|
| Chất lượng tín dụng **không đổi** | DM $\approx$ QM | Giá $\approx$ mệnh giá tại ngày reset |
| Chất lượng tín dụng **cải thiện** | DM < QM | Giá > mệnh giá |
| Chất lượng tín dụng **xấu đi** | DM > QM | Giá < mệnh giá |

### Điểm Mấu Chốt

- Tại mỗi ngày reset, coupon được điều chỉnh lại theo MRR + QM hiện tại
- Nếu tín dụng của tổ chức phát hành không thay đổi, required margin bằng quoted margin, do đó FRN sẽ reset về xấp xỉ mệnh giá
- Nếu tín dụng xấu đi, nhà đầu tư yêu cầu **spread cao hơn** (DM > QM), đẩy giá xuống dưới mệnh giá ngay cả sau khi reset

---

## Công Cụ Thị Trường Tiền Tệ (Money Market Instruments)

Money market instruments là các công cụ ngắn hạn (kỳ hạn $\leq$ 1 năm) và có thể được yết giá theo **discount basis** hoặc **add-on basis**.

### Bank Discount Yield (BDY)

$$\text{BDY} = \frac{\text{Face} - \text{Price}}{\text{Face}} \times \frac{360}{\text{Days}}$$

- Được yết theo **discount basis** sử dụng **mệnh giá (face value)** làm mẫu số
- Sử dụng năm 360 ngày
- Đánh giá thấp hơn lợi suất thực tế (dùng Face thay vì Price ở mẫu số)
- Phổ biến cho U.S. T-bills

### Holding Period Yield (HPY)

$$\text{HPY} = \frac{\text{Face} - \text{Price}}{\text{Price}} = \frac{D}{\text{Price}}$$

trong đó $D$ = dollar discount = Face $-$ Price.

### Money Market Yield (MMY)

$$\text{MMY} = \text{HPY} \times \frac{360}{\text{Days}}$$

- Được hóa hàng năm theo năm **360 ngày**
- Sử dụng **Price** làm mẫu số (khác với BDY dùng Face)
- Còn được gọi là CD-equivalent yield

### Bond Equivalent Yield (BEY)

$$\text{BEY} = \text{HPY} \times \frac{365}{\text{Days}}$$

- Được hóa hàng năm theo năm **365 ngày**
- Cho phép so sánh với lợi suất trái phiếu trả coupon nửa năm một lần

---

## Mối Quan Hệ Chuyển Đổi Giữa Các Yield

$$\text{MMY} = \frac{360 \times \text{BDY}}{360 - (\text{Days} \times \text{BDY})}$$

$$\text{BEY} = \text{MMY} \times \frac{365}{360}$$

### Thứ Tự Của Các Yield

Đối với discount instruments:

$$\text{BDY} < \text{MMY} < \text{BEY}$$

BDY thấp nhất vì sử dụng Face (lớn hơn) ở mẫu số và năm 360 ngày. BEY cao nhất vì sử dụng Price (nhỏ hơn) ở mẫu số và năm 365 ngày.

---

## Ví Dụ

T-bill kỳ hạn 90 ngày với Face = \$100,000 và Price = \$99,000:

$$D = 100{,}000 - 99{,}000 = 1{,}000$$

$$\text{HPY} = \frac{1{,}000}{99{,}000} = 1.0101\%$$

$$\text{BDY} = \frac{1{,}000}{100{,}000} \times \frac{360}{90} = 4.00\%$$

$$\text{MMY} = 1.0101\% \times \frac{360}{90} = 4.0404\%$$

$$\text{BEY} = 1.0101\% \times \frac{365}{90} = 4.0965\%$$

---

## Xem Thêm

- [[fixed-income/m07-yield-spread-fixed-rate/index|M07 - Yield Spread for Fixed-Rate Bonds]]
- [[fixed-income/m09-term-structure/index|M09 - Term Structure]]