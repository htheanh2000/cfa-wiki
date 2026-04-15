---
title: "M06 — Futures Pricing"
type: module
subject: derivatives
module: M06
los: "6.a-6.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m06
  - futures
  - pricing
  - valuation
  - mark-to-market
  - interest-rate-futures
  - FRA
---

# M06: Futures Pricing and Valuation

> **LOS 6.a**: So sánh giá trị (value) và giá (price) của hợp đồng forward và futures.
> **LOS 6.b**: Giải thích tại sao giá forward và giá futures có thể khác nhau.

## 1. Futures Pricing tại thời điểm khởi tạo

Tại thời điểm ký kết hợp đồng, **giá trị** của một hợp đồng futures bằng không:

$$V_0(T) = 0$$

**Giá futures** tại thời điểm khởi tạo bằng giá forward khi không có chi phí hay lợi ích carry:

$$f_0(T) = S_0 \times (1 + r)^T$$

trong đó:
- $f_0(T)$ = giá futures tại thời điểm 0 cho việc giao hàng tại thời điểm $T$
- $S_0$ = giá spot hiện tại của tài sản cơ sở
- $r$ = lãi suất phi rủi ro
- $T$ = thời gian đến khi đáo hạn

**Khi có chi phí và lợi ích carry:**

$$f_0(T) = \left[ S_0 - PV_0(I) + PV_0(C) \right] \times (1 + r)^T$$

trong đó:
- $PV_0(I)$ = giá trị hiện tại của thu nhập/lợi ích từ tài sản cơ sở (ví dụ: cổ tức, coupon)
- $PV_0(C)$ = giá trị hiện tại của chi phí carry (ví dụ: chi phí lưu kho, bảo hiểm)

## 2. Futures so với Forwards theo thời gian

| Đặc điểm | Futures | Forwards |
|---------|---------|----------|
| Giá theo thời gian | Thay đổi hàng ngày | **Cố định** từ khi khởi tạo |
| Giá trị theo thời gian | Reset về 0 hàng ngày (MTM) | Biến động liên tục |
| Thanh toán | Mark-to-market hàng ngày | Khi đáo hạn |
| Dòng tiền | Điều chỉnh margin hàng ngày | Một lần thanh toán tại $T$ |

> **Điểm mấu chốt**: Với futures, cả **giá** lẫn **giá trị** đều thay đổi mỗi ngày. Việc thanh toán hàng ngày (mark-to-market) reset giá trị hợp đồng về không sau mỗi ngày. Với forwards, **giá** được khóa cố định từ khi khởi tạo và không bao giờ thay đổi — chỉ có **giá trị** mới biến động.

## 3. MTM: Realized vs Unrealized

- **Futures MTM** = lãi/lỗ đã **realized** — dòng tiền thực tế phát sinh hàng ngày thông qua tài khoản margin
- **Forward MTM** = lãi/lỗ **unrealized** — không có tiền thực tế chuyển tay cho đến khi đáo hạn; giá trị là lãi/lỗ trên giấy tờ

Sự phân biệt này rất quan trọng trong quản lý dòng tiền và rủi ro tín dụng.

## 4. Interest Rate Futures

### Quy ước giá

Interest rate futures sử dụng quy ước **báo giá nghịch đảo**:

$$\text{Futures Price} = 100 - \text{Yield}$$

Ví dụ, nếu implied yield là 4,50%, thì futures price là $100 - 4{,}50 = 95{,}50$.

### Basis Point Value (BPV)

$$BPV = \text{Notional} \times 0{,}01\% \times \text{Period}$$

trong đó:
- $\text{Period}$ = phần năm tương ứng (ví dụ: $90/360$ cho hợp đồng 90 ngày)

Với notional \$1.000.000, hợp đồng 90 ngày:

$$BPV = 1{,}000{,}000 \times 0.0001 \times \frac{90}{360} = \$25$$

## 5. Cash Settlement của FRA

### Khoản thanh toán ròng tại thời điểm settlement

$$\text{Net Payment} = (\text{MRR} - \text{IFR}) \times \text{Notional} \times \text{Period}$$

trong đó:
- $\text{MRR}$ = market reference rate tại thời điểm settlement
- $\text{IFR}$ = implied forward rate (lãi suất đã thỏa thuận)
- $\text{Period}$ = phần năm tương ứng

### Cash Settlement (đã chiết khấu)

Vì FRA thanh toán vào **đầu** kỳ vay (không phải cuối kỳ), khoản thanh toán ròng được chiết khấu:

$$\text{Cash Settlement} = \frac{\text{Net Payment}}{1 + \text{MRR} \times \text{Period}}$$

> **Ví dụ**: Nếu MRR = 5%, IFR = 4%, Notional = \$10M, Period = 180/360:
> - Net Payment $= (0{,}05 - 0{,}04) \times 10{,}000{,}000 \times 0{,}5 = \$50{,}000$
> - Cash Settlement $= \frac{50{,}000}{1 + 0{,}05 \times 0{,}5} = \frac{50{,}000}{1{,}025} = \$48{,}780{,}49$

## 6. Sự khác biệt giữa giá Futures và Forward

Yếu tố then chốt là **tương quan giữa giá tài sản cơ sở và lãi suất**:

| Tương quan | Mối quan hệ | Vị thế được ưa chuộng |
|-------------|-------------|-------------------|
| Dương (giá tài sản $\uparrow$ khi $r \uparrow$) | $f_0(T) > F_0(T)$ | Ưa chuộng long **futures** |
| Âm (giá tài sản $\uparrow$ khi $r \downarrow$) | $f_0(T) < F_0(T)$ | Ưa chuộng long **forwards** |
| Bằng không | $f_0(T) = F_0(T)$ | Không có sự khác biệt |

**Lý giải trực quan**: Khi tài sản cơ sở tăng giá và lãi suất cũng tăng đồng thời, các khoản lãi MTM hàng ngày trên futures có thể được tái đầu tư ở mức lãi suất cao hơn — đây là lợi thế cho vị thế long futures.

## 7. Convexity Bias

Có một sự khác biệt căn bản giữa FRA và interest rate futures:

- **FRA**: Có mối quan hệ giá-lợi suất **phi tuyến (lồi)** — tương tự như trái phiếu
- **Interest rate futures**: Có mối quan hệ giá-lợi suất **tuyến tính** (do quy ước $100 - \text{yield}$)

Sự khác biệt này được gọi là **convexity bias**:

$$\text{Futures Rate} > \text{Forward Rate (from FRA)}$$

Futures rate phải được điều chỉnh giảm xuống (gọi là "convexity adjustment") để suy ra forward rate tương đương. Mức điều chỉnh tăng theo kỳ hạn và độ biến động.

---

**Xem thêm**: [[derivatives/modules/m05-forward-pricing-valuation/index|M05: Forward Pricing and Valuation]], [[derivatives/modules/m07-swaps-pricing-valuation/index|M07: Swaps Pricing and Valuation]]

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]]