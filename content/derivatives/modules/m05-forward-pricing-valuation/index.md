---
title: "M05 — Forward Pricing"
type: module
subject: derivatives
module: M05
los: "5.a-5.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m05
  - forward-contracts
  - pricing
  - valuation
  - fra
---

# M05: Pricing and Valuation of Forward Contracts

> **LOS 5.a**: Mô tả cách forward contracts được định giá và xác định giá trị.
> **LOS 5.b**: Mô tả cách interest rate forward contracts (FRAs) được định giá và xác định giá trị.

## 1. Pricing vs Valuation

| Khái niệm | Ý nghĩa |
|-----------|---------|
| **Pricing** | Xác định forward price $F_0(T)$ tại thời điểm khởi tạo hợp đồng (sao cho giá trị = 0) |
| **Valuation** | Xác định **giá trị** $V_t(T)$ của một forward contract hiện có tại bất kỳ thời điểm nào |

## 2. Forward Price (Không có Chi phí/Lợi ích)

$$F_0(T) = S_0 \times (1 + r)^T$$

## 3. Forward Contract Value

### Tại thời điểm khởi tạo ($t = 0$)

$$V_0(T) = 0$$

Forward price được thiết lập sao cho không bên nào phải trả bất cứ khoản nào trước.

### Trong suốt vòng đời hợp đồng ($0 < t < T$)

$$V_t(T) = S_t - F_0(T) \times (1 + r)^{-(T - t)}$$

Trong đó:
- $S_t$ = giá giao ngay (spot price) tại thời điểm $t$
- $F_0(T)$ = forward price ban đầu
- $(T - t)$ = thời gian còn lại đến khi đáo hạn

> Đây là giá trị **của bên mua (long)**. Giá trị của bên bán (short) là $-V_t(T)$.

### Tại thời điểm đáo hạn ($t = T$)

$$V_T(T) = S_T - F_0(T)$$

## 4. Với Net Cost of Carry

### Forward Price

$$F_0(T) = \left[S_0 - PV_0(I) + PV_0(C)\right] \times (1 + r)^T$$

### Value trong suốt vòng đời hợp đồng

$$V_t(T) = \left[S_t - PV_t(I) + PV_t(C)\right] - F_0(T) \times (1 + r)^{-(T - t)}$$

Trong đó:
- $PV_t(I)$ = giá trị hiện tại (tại thời điểm $t$) của thu nhập/lợi ích còn lại
- $PV_t(C)$ = giá trị hiện tại (tại thời điểm $t$) của chi phí còn lại

## 5. Forward Rate Agreement (FRA)

**Forward Rate Agreement (FRA)** là một forward contract trên lãi suất (thường là MRR -- Market Reference Rate, ví dụ: SOFR).

### Đặc điểm chính

- **Bên mua (long)** = bên trả lãi suất cố định / hưởng lợi khi lãi suất tăng
- **Bên bán (short)** = bên trả lãi suất thả nổi / hưởng lợi khi lãi suất giảm
- Thanh toán bằng **tiền mặt** vào đầu kỳ vay

### Ký hiệu IFR

Một FRA được ký hiệu là "$A \times B$" có nghĩa:
- FRA đáo hạn sau **$A$ tháng**
- Khoản vay cơ sở đáo hạn sau **$B$ tháng**
- Kỳ vay có độ dài $B - A$ tháng

> Ví dụ: FRA $1 \times 4$ là hợp đồng đáo hạn sau 1 tháng trên lãi suất kỳ hạn 3 tháng.

### FRA Pricing

Lãi suất cố định của FRA là **implied forward rate (IFR)** được suy ra từ đường cong lợi suất giao ngay (spot yield curve):

$$(1 + S_A)^A \times (1 + IFR_{A,B-A})^{B-A} = (1 + S_B)^B$$

Giải ra IFR:

$$IFR_{A,B-A} = \left[\frac{(1 + S_B)^B}{(1 + S_A)^A}\right]^{\frac{1}{B-A}} - 1$$

### FRA Cash Settlement

Tại thời điểm đáo hạn, FRA được thanh toán dựa trên chênh lệch giữa lãi suất đã ký kết và MRR thực tế:

$$\text{Net payment} = \text{Notional} \times (MRR - IFR) \times \frac{\text{Period}}{360}$$

Vì FRA thanh toán vào **đầu** kỳ vay, khoản thanh toán được chiết khấu về hiện tại:

$$\text{Cash settlement (PV)} = \frac{\text{Net payment}}{1 + MRR \times \frac{\text{Period}}{360}}$$

> Giá trị **dương** có nghĩa bên mua (long) nhận được khoản thanh toán; giá trị **âm** có nghĩa bên mua phải trả.

---

**Source**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]], p.129-164