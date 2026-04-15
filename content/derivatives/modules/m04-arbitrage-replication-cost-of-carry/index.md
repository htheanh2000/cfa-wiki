---
title: "M04 — Arbitrage & Replication"
type: module
subject: derivatives
module: M04
los: "4.a-4.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m04
  - arbitrage
  - replication
  - cost-of-carry
  - pricing
---

# M04: Arbitrage, Replication, and Cost of Carry in Pricing Derivatives

> **LOS 4.a**: Giải thích cách các khái niệm arbitrage, replication, và risk neutrality được sử dụng trong định giá derivatives.
> **LOS 4.b**: Giải thích cách cost of carry model được sử dụng để định giá forward commitments.

## 1. Arbitrage

**Arbitrage** = kiếm lợi nhuận không có rủi ro mà không cần đầu tư ròng, bằng cách khai thác sự chênh lệch giá.

### Law of One Price

Hai tài sản (hoặc danh mục) có **dòng tiền tương lai giống hệt nhau** phải có **cùng một mức giá** hiện tại. Nếu không, arbitrage tồn tại.

### Hai Loại Arbitrage Opportunities

| Loại | Mô tả |
|------|-------------|
| **Case 1** | Hai tài sản có dòng tiền giống nhau nhưng giao dịch ở mức giá khác nhau. Mua tài sản rẻ hơn, bán tài sản đắt hơn. |
| **Case 2** | Giá hiện tại của tài sản không bằng giá trị hiện tại của mức giá tương lai chắc chắn. Mua/bán và khóa lợi nhuận không có rủi ro. |

> Trong các thị trường hiệu quả, các arbitrage opportunities bị khai thác và loại bỏ nhanh chóng.

## 2. Replication

**Replication** = xây dựng một danh mục từ các công cụ khác tạo ra **dòng tiền giống hệt nhau** với derivative.

- Nếu hai danh mục có cùng dòng tiền trong mọi trạng thái tương lai, chúng phải có cùng mức giá hiện tại (theo nguyên tắc no-arbitrage).
- Nguyên tắc cốt lõi: **Asset + Derivative = Risk-free asset** (hoặc bất kỳ cách sắp xếp lại nào).

### Các Mối Quan Hệ Cơ Bản

$$\text{Asset} + \text{Derivative} = \text{Risk-free asset}$$

Sắp xếp lại:

$$\text{Derivative} = \text{Risk-free asset} - \text{Asset}$$

$$\text{Asset} = \text{Risk-free asset} - \text{Derivative}$$

## 3. Mối Quan Hệ Giữa Arbitrage và Replication

- Replication cung cấp **giá lý thuyết** của một derivative
- Nếu giá thị trường lệch khỏi chi phí replication, một **arbitrage opportunity** xuất hiện
- Các arbitrageurs khai thác điều này cho đến khi giá hội tụ

## 4. Cost of Carry Model

### Forward Price Cơ Bản (Không Có Chi Phí, Không Có Lợi Ích)

$$F_0(T) = S_0 \times (1 + r)^T$$

Trong đó:
- $F_0(T)$ = forward price được thỏa thuận tại $t = 0$ để giao nhận tại $T$
- $S_0$ = spot price hiện tại
- $r$ = lãi suất phi rủi ro (risk-free rate)
- $T$ = thời gian đến khi đáo hạn (tính bằng năm)

### Forward Price Có Tính Đến Chi Phí và Lợi Ích

$$F_0(T) = \left[S_0 - PV_0(I) + PV_0(C)\right] \times (1 + r)^T$$

Trong đó:
- $PV_0(I)$ = giá trị hiện tại của thu nhập/lợi ích nhận được từ việc nắm giữ tài sản cơ sở (cổ tức, coupon, convenience yield)
- $PV_0(C)$ = giá trị hiện tại của chi phí nắm giữ tài sản cơ sở (lưu kho, bảo hiểm)

### Diễn Giải Net Cost of Carry

| Tình huống | Ảnh hưởng đến Forward Price |
|----------|----------------------|
| Lợi ích $>$ Chi phí | Forward price **thấp hơn** $S_0 \times (1+r)^T$ |
| Chi phí $>$ Lợi ích | Forward price **cao hơn** $S_0 \times (1+r)^T$ |

### Lãi Kép Liên Tục (Cổ Phiếu Có Continuous Dividend Yield)

Đối với tài sản cơ sở trả continuous dividend yield $\delta$:

$$F_0(T) = S_0 \times e^{(r_f - \delta) \cdot T}$$

Trong đó:
- $r_f$ = lãi suất phi rủi ro tính theo lãi kép liên tục (continuously compounded risk-free rate)
- $\delta$ = continuous dividend yield

> **Điểm Mấu Chốt**: Forward price KHÔNG phải là dự báo về spot price trong tương lai. Đó là **no-arbitrage price** được xác định bởi cost of carry.

---

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]], tr.102-128