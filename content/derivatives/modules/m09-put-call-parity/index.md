---
title: "M09 — Put-Call Parity"
type: module
subject: derivatives
module: M09
los: "9.a-9.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m09
  - put-call-parity
  - synthetic-positions
  - protective-put
  - fiduciary-call
  - corporate-finance
---

# M09: Put-Call Parity and Synthetic Positions

> **LOS 9.a**: Giải thích put-call parity cho các quyền chọn kiểu châu Âu.
> **LOS 9.b**: Giải thích put-call forward parity cho các quyền chọn kiểu châu Âu.

## 1. Protective Put

**Protective put** kết hợp một vị thế mua (long position) tài sản cơ sở với một long put option:

$$\text{Protective Put} = S_0 + p_0$$

**Payoff tại ngày đáo hạn:**

$$\text{Payoff} = \max(X,\; S_T)$$

- Nếu $S_T > X$: put option hết giá trị, payoff = $S_T$
- Nếu $S_T < X$: thực hiện put, payoff = $X$

Protective put đảm bảo một **giá trị danh mục tối thiểu** bằng $X$.

## 2. Fiduciary Call

**Fiduciary call** kết hợp một long call option với một trái phiếu phi rủi ro trả $X$ tại đáo hạn:

$$\text{Fiduciary Call} = c_0 + \frac{X}{(1+r)^T}$$

**Payoff tại ngày đáo hạn:**

$$\text{Payoff} = \max(X,\; S_T)$$

- Nếu $S_T > X$: thực hiện call, payoff = $S_T - X + X = S_T$
- Nếu $S_T < X$: call option hết giá trị, payoff = $X$ (từ trái phiếu)

> **Điểm mấu chốt**: Protective put và fiduciary call có **payoff hoàn toàn giống nhau** trong mọi trạng thái thị trường. Theo quy luật một giá (law of one price), chúng phải có chi phí bằng nhau tại thời điểm hiện tại.

## 3. Put-Call Parity

Vì protective put = fiduciary call:

$$\boxed{S_0 + p_0 = c_0 + \frac{X}{(1+r)^T}}$$

trong đó:
- $S_0$ = giá spot hiện tại
- $p_0$ = phí bảo hiểm European put
- $c_0$ = phí bảo hiểm European call
- $X$ = giá thực hiện chung
- $r$ = lãi suất phi rủi ro
- $T$ = thời gian đến đáo hạn

Mối quan hệ này chỉ áp dụng cho **quyền chọn kiểu châu Âu** (cùng tài sản cơ sở, cùng giá thực hiện, cùng ngày đáo hạn).

## 4. Synthetic Equivalents

Bằng cách sắp xếp lại put-call parity, ta có thể tạo ra các phiên bản **synthetic** của bất kỳ thành phần nào:

| Vị thế Synthetic | Công thức | Cách xây dựng |
|-------------------|---------|--------------|
| **Synthetic call** | $c_0 = S_0 + p_0 - \frac{X}{(1+r)^T}$ | Long asset + Long put + Short bond |
| **Synthetic put** | $p_0 = c_0 + \frac{X}{(1+r)^T} - S_0$ | Long call + Long bond + Short asset |
| **Synthetic bond** | $\frac{X}{(1+r)^T} = S_0 + p_0 - c_0$ | Long asset + Long put + Short call |
| **Synthetic asset** | $S_0 = c_0 - p_0 + \frac{X}{(1+r)^T}$ | Long call + Short put + Long bond |

> **Điểm mấu chốt**: Nếu bất kỳ synthetic nào có chi phí rẻ hơn công cụ thực tế, một **cơ hội arbitrage** sẽ xuất hiện. Trong thực tế, các nhà kinh doanh chênh lệch giá (arbitrageurs) sẽ duy trì put-call parity.

## 5. Put-Call Forward Parity

Khi sử dụng **hợp đồng kỳ hạn (forward contract)** thay vì tài sản cơ sở:

$$\frac{F_0(T)}{(1+r)^T} + p_0 = c_0 + \frac{X}{(1+r)^T}$$

trong đó:
- $F_0(T)$ = giá kỳ hạn để giao nhận tại thời điểm $T$

Công thức này được suy ra bằng cách thay thế giá kỳ hạn không có arbitrage $F_0(T) = S_0(1+r)^T$ vào put-call parity.

### Synthetic Protective Put (với Forward)

$$\text{Synthetic Protective Put} = \text{Long Put} + \text{Long Forward} + \text{Bond with par} = F_0(T)$$

Cách này tái tạo payoff của một protective put mà không cần trực tiếp nắm giữ tài sản cơ sở.

## 6. Ứng dụng trong Corporate Finance

Put-call parity cung cấp một khung phân tích mạnh mẽ để hiểu **cấu trúc vốn (capital structure)** của doanh nghiệp:

### Vốn chủ sở hữu (Equity) như một Call Option

$$\text{Equity} = \text{Long Call on Firm's Assets}$$

- Giá thực hiện $X$ = mệnh giá nợ
- Nếu giá trị doanh nghiệp $V > X$ tại đáo hạn: cổ đông nhận được $V - X$ (thực hiện call)
- Nếu giá trị doanh nghiệp $V < X$: cổ đông bỏ qua, nhận 0 (quyền chọn hết giá trị)

### Nợ có rủi ro (Risky Debt) như một Covered Position

$$\text{Risky Debt} = \text{Long Risk-Free Bond} + \text{Short Put on Firm's Assets}$$

- Chủ nợ nhận được $X$ trừ khi doanh nghiệp vỡ nợ
- Nếu $V < X$: chủ nợ gánh chịu khoản lỗ $X - V$ (short put bị thực hiện ngược lại họ)
- **Credit spread** trên nợ có rủi ro phản ánh giá trị của short put ẩn chứa này

> **Điểm mấu chốt**: Khung phân tích này giải thích tại sao cổ đông ưa thích các dự án rủi ro hơn (biến động cao làm tăng giá trị call) trong khi chủ nợ ưa thích các dự án an toàn hơn (biến động cao làm tăng nghĩa vụ của embedded put).

---

**Xem thêm**: [[derivatives/modules/m08-options-pricing-valuation/index|M08: Options Pricing and Valuation]], [[derivatives/modules/m10-binomial-model/index|M10: Binomial Model]]

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]]