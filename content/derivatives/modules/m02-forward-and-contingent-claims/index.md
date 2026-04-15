---
title: "M02 — Forwards & Contingent Claims"
type: module
subject: derivatives
module: M02
los: "2.a-2.c"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m02
  - forward-commitments
  - contingent-claims
  - forwards
  - futures
  - swaps
  - options
---

# M02: Forward Commitment and Contingent Claim Features and Instruments

> **LOS 2.a**: Mô tả forward commitments và contingent claims.
> **LOS 2.b**: Mô tả các đặc điểm cơ bản và payoff của forward commitments và contingent claims.
> **LOS 2.c**: Mô tả mục đích và các tranh cãi liên quan đến thị trường phái sinh.

## 1. Hai Loại Công Cụ Chính

### Forward Commitments (Nghĩa vụ)

Cả hai bên đều **có nghĩa vụ** thực hiện giao dịch vào một ngày trong tương lai. Payoff có tính **đối xứng** (tuyến tính).

- **Forwards**
- **Futures**
- **Swaps**

### Contingent Claims (Quyền, Không Phải Nghĩa Vụ)

Một bên có **quyền** (nhưng không có nghĩa vụ) thực hiện giao dịch. Payoff có tính **bất đối xứng** (phi tuyến tính).

- **Options** (calls, puts)
- **Credit derivatives**

## 2. Forward Contracts

**Forward** là một thỏa thuận OTC riêng tư để mua/bán một tài sản tại mức giá xác định $F_0(T)$ vào một ngày trong tương lai $T$.

- Được thỏa thuận tại $t = 0$, thanh toán tại $t = T$
- **Không phát sinh chi phí ban đầu** (giá trị tại thời điểm khởi tạo = 0)
- **Các hình thức thanh toán**:
  - **Physical settlement**: giao nhận tài sản cơ sở thực tế
  - **Cash settlement**: thanh toán/nhận phần chênh lệch $S_T - F_0(T)$

### Payoff tại Ngày Đáo Hạn

$$\text{Long payoff} = S_T - F_0(T)$$

$$\text{Short payoff} = F_0(T) - S_T$$

> Bên long có lợi khi giá giao ngay tăng vượt giá forward; bên short có lợi khi giá giao ngay giảm xuống dưới giá forward.

## 3. Futures Contracts

Tương tự forward nhưng có một số khác biệt cấu trúc quan trọng:

| Đặc điểm | Forward | Futures |
|---------|---------|---------|
| Địa điểm giao dịch | OTC | Giao dịch trên sàn |
| Tiêu chuẩn hóa | Tùy chỉnh | Được tiêu chuẩn hóa |
| Thanh toán | Khi đáo hạn | **Mark-to-market hàng ngày** |
| Rủi ro đối tác | Có | Clearinghouse bảo lãnh |
| Ký quỹ | Có thể thương lượng | Bắt buộc |

### Cơ Chế Margin

1. **Initial margin**: khoản ký quỹ bắt buộc để mở một vị thế futures
2. **Maintenance margin**: số dư tài khoản tối thiểu (thường khoảng ~75% của initial margin)
3. **Margin call**: được kích hoạt khi số dư tài khoản giảm xuống dưới maintenance margin
   - Phải nộp thêm tiền để khôi phục số dư về mức **initial margin** (không phải maintenance margin)

### Ví Dụ về Daily MTM

Nếu bạn đang giữ một vị thế long futures và giá giảm \$5:
- Tài khoản ký quỹ của bạn bị **ghi nợ** \$5
- Tài khoản ký quỹ của bên short được **ghi có** \$5

## 4. Swaps

**Swap** là thỏa thuận trao đổi một **chuỗi dòng tiền** theo thời gian.

Về bản chất: swap = một chuỗi các forward contracts được gộp lại với nhau.

### Interest Rate Swap

- **Fixed-rate payer** trả lãi suất cố định, nhận lãi suất thả nổi (dựa trên MRR)
- **Floating-rate payer** trả lãi suất thả nổi, nhận lãi suất cố định
- Chỉ trao đổi phần **chênh lệch ròng**
- Notional principal **không** được trao đổi (đối với interest rate swaps)

### Các Loại Swap Khác

- **Equity swap**: trao đổi lợi suất cổ phiếu lấy lãi suất cố định/thả nổi
- **Currency swap**: trao đổi dòng tiền bằng các đồng tiền khác nhau (notional **được** trao đổi tại thời điểm khởi tạo và đáo hạn)

## 5. Options

**Option** cho phép người nắm giữ có **quyền, nhưng không có nghĩa vụ**, mua hoặc bán một tài sản cơ sở tại một mức giá xác định (strike price $X$) vào hoặc trước một ngày xác định.

### Call Option (Quyền Mua)

$$\text{Long call payoff} = \max(0,\ S_T - X)$$

- Có lợi nhuận khi $S_T > X$ (in-the-money)
- Khoản lỗ tối đa = phí option đã trả

### Put Option (Quyền Bán)

$$\text{Long put payoff} = \max(0,\ X - S_T)$$

- Có lợi nhuận khi $S_T < X$ (in-the-money)
- Khoản lỗ tối đa = phí option đã trả

### European vs American

| Đặc điểm | European | American |
|---------|----------|---------|
| Thực hiện quyền | Chỉ tại ngày đáo hạn | Bất kỳ thời điểm nào cho đến và bao gồm ngày đáo hạn |
| Định giá | Thường rẻ hơn | Phí $\geq$ European |

### Option Premium

**Option premium** (giá option) là khoản chi phí người mua trả cho người bán (writer) để có được quyền mà option cấp. Khoản phí này được thanh toán **trước** tại thời điểm khởi tạo hợp đồng.

## 6. Credit Derivatives

Các công cụ chuyển giao **rủi ro tín dụng** từ bên này sang bên khác:

- **Credit Default Swap (CDS)**: người mua trả phí định kỳ; người bán thanh toán nếu một sự kiện tín dụng xảy ra (vỡ nợ, tái cơ cấu)
- **Credit-Linked Note (CLN)**: một trái phiếu được gắn kèm CDS -- nhà đầu tư chịu rủi ro tín dụng của một tổ chức tham chiếu
- **Credit Spread Option**: option trên credit spread của một trái phiếu so với một benchmark

---

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]], p.21-86