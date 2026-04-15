---
title: "M10 — Yield Spreads"
type: module
subject: fixed-income
module: M10
los:
  - 10.a: Describe the sources of return from investing in a fixed-rate bond
  - 10.b: Explain how changes in interest rates affect the components of return
  - 10.c: Define, calculate, and interpret Macaulay duration and explain its role in immunization
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - interest-rate-risk
  - reinvestment-risk
  - market-price-risk
  - macaulay-duration
  - immunization
---

# Interest Rate Risk and Return

## Ba Nguồn Lợi Nhuận

1. **Coupon payments** -- lãi định kỳ nhận được từ trái phiếu
2. **Reinvestment income** -- lãi kiếm được từ việc tái đầu tư các coupon
3. **Capital gain or loss** -- chênh lệch giữa giá mua và giá bán/giá đáo hạn

---

## Interest Rate Risk

Interest rate risk có hai thành phần đối lập nhau:

| Thành phần | Khi lãi suất tăng | Khi lãi suất giảm |
|-----------|------------------------|------------------------|
| **Reinvestment risk** | Thu nhập tái đầu tư tăng | Thu nhập tái đầu tư giảm |
| **Market price risk** | Giá trái phiếu giảm (lỗ vốn) | Giá trái phiếu tăng (lãi vốn) |

Hai rủi ro này hoạt động theo **chiều ngược nhau**, tạo ra một sự căng thẳng tự nhiên.

---

## Tác Động Của Thay Đổi Lãi Suất Đến Lợi Nhuận Thực Tế

### Nếu Lãi Suất Không Đổi

$$\text{Realized return} = \text{YTM} \quad \text{(với mọi nhà đầu tư)}$$

### Nếu Lãi Suất Tăng

| Loại nhà đầu tư | Lợi nhuận thực tế so với YTM | Lý do |
|--------------|------------------------|--------|
| **Buy-and-hold** (chân trời dài) | Lợi nhuận **> YTM** | Lãi tái đầu tư > lỗ giá thị trường |
| Nhà đầu tư **ngắn hạn** | Lợi nhuận **< YTM** | Lỗ giá thị trường chiếm ưu thế |

### Nếu Lãi Suất Giảm

| Loại nhà đầu tư | Lợi nhuận thực tế so với YTM | Lý do |
|--------------|------------------------|--------|
| **Buy-and-hold** (chân trời dài) | Lợi nhuận **< YTM** | Lỗ tái đầu tư > lãi giá thị trường |
| Nhà đầu tư **ngắn hạn** | Lợi nhuận **> YTM** | Lãi giá thị trường chiếm ưu thế |

---

## Macaulay Duration

### Định Nghĩa

**Macaulay duration** là **thời gian bình quân gia quyền** để nhận toàn bộ dòng tiền của trái phiếu, trong đó trọng số là giá trị hiện tại của từng dòng tiền tính theo tỷ lệ trên tổng giá trái phiếu.

### Công Thức

$$\text{MacDur} = \frac{\sum_{t=1}^{N} t \times \frac{CF_t}{(1+r)^t}}{\sum_{t=1}^{N} \frac{CF_t}{(1+r)^t}} = \frac{\sum_{t=1}^{N} t \times PV(CF_t)}{PV_{\text{total}}}$$

trong đó:
- $t$ = kỳ thời gian (tính bằng năm hoặc kỳ)
- $CF_t$ = dòng tiền tại thời điểm $t$
- $r$ = lợi suất mỗi kỳ

### Diễn Giải

Macaulay duration được đo bằng **đơn vị thời gian** (năm). Nó đại diện cho điểm mà tại đó reinvestment risk và market price risk triệt tiêu nhau hoàn toàn.

---

## Duration và Immunization

### Duration Gap

$$\text{Duration Gap} = \text{MacDur} - \text{Investment Horizon}$$

### Điều Kiện Immunization

Khi **investment horizon = Macaulay duration**, nhà đầu tư được **immunized** trước những thay đổi nhỏ, song song trong lãi suất:

$$\text{Investment Horizon} = \text{MacDur} \implies \text{Duration Gap} = 0$$

Tại điểm này, bất kỳ khoản lãi (lỗ) nào từ tái đầu tư đều được bù đắp chính xác bởi khoản lỗ (lãi) trong giá thị trường.

### Các Kịch Bản Duration Gap

| Duration Gap | Yếu tố chiếm ưu thế | Khi lãi suất tăng | Khi lãi suất giảm |
|-------------|-----------|-----------|-----------|
| **Dương** (MacDur > Horizon) | Market price risk | Lợi nhuận < YTM | Lợi nhuận > YTM |
| **Bằng không** (MacDur = Horizon) | Immunized | Lợi nhuận $\approx$ YTM | Lợi nhuận $\approx$ YTM |
| **Âm** (MacDur < Horizon) | Reinvestment risk | Lợi nhuận > YTM | Lợi nhuận < YTM |

### Duration Gap Dương

- Chân trời đầu tư của nhà đầu tư ngắn hơn MacDur
- **Market price risk chiếm ưu thế** so với reinvestment risk
- Nhà đầu tư hành xử như người nắm giữ ngắn hạn: bị thiệt hại khi lãi suất tăng, được lợi khi lãi suất giảm

### Duration Gap Âm

- Chân trời đầu tư của nhà đầu tư dài hơn MacDur
- **Reinvestment risk chiếm ưu thế** so với market price risk
- Nhà đầu tư hành xử như người nắm giữ dài hạn: được lợi khi lãi suất tăng, bị thiệt hại khi lãi suất giảm

---

## Xem Thêm

- [[fixed-income/m09-term-structure/index|M09 - Term Structure]]
- [[fixed-income/m11-duration-measures/index|M11 - Yield-Based Duration Measures]]
- [[fixed-income/m12-convexity-portfolio/index|M12 - Convexity and Portfolio Duration]]