---
title: "M08 — Options Pricing"
type: module
subject: derivatives
module: M08
los: "8.a-8.c"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m08
  - options
  - pricing
  - valuation
  - moneyness
  - exercise-value
  - time-value
  - no-arbitrage-bounds
---

# M08: Options Pricing and Valuation

> **LOS 8.a**: Giải thích exercise value, moneyness, và time value của một option.
> **LOS 8.b**: So sánh việc sử dụng các khái niệm arbitrage và replication trong định giá forward commitments so với contingent claims.
> **LOS 8.c**: Xác định các yếu tố quyết định giá trị của một option và mô tả cách mỗi yếu tố ảnh hưởng đến giá trị đó.

## 1. Exercise Value, Time Value, và Moneyness

### Exercise Value

Exercise value đại diện cho giá trị của option nếu được thực hiện ngay (hoặc trong suốt vòng đời, là chênh lệch giữa spot price và PV của strike price).

**Trong suốt vòng đời của option** ($t < T$):

$$\text{Call exercise value} = \max\left(0,\; S_t - \frac{X}{(1+r)^{T-t}}\right)$$

$$\text{Put exercise value} = \max\left(0,\; \frac{X}{(1+r)^{T-t}} - S_t\right)$$

**Tại thời điểm đáo hạn** ($t = T$):

$$\text{Call exercise value} = \max(0,\; S_T - X)$$

$$\text{Put exercise value} = \max(0,\; X - S_T)$$

trong đó:
- $S_t$ = spot price tại thời điểm $t$
- $X$ = strike (exercise) price
- $r$ = lãi suất phi rủi ro
- $T - t$ = thời gian còn lại đến khi đáo hạn

### Phân tách Option Price

$$\text{Option Price} = \text{Exercise Value} + \text{Time Value}$$

- **Time value** phản ánh tiềm năng option trở nên có giá trị hơn trước khi đáo hạn
- Tại thời điểm đáo hạn, **time value = 0** — option chỉ đáng giá đúng bằng exercise value của nó

### Moneyness

| Moneyness | Call ($S$ vs $X$) | Put ($S$ vs $X$) |
|-----------|-------------------|-------------------|
| **In-the-money (ITM)** | $S > X$ | $S < X$ |
| **At-the-money (ATM)** | $S = X$ | $S = X$ |
| **Out-of-the-money (OTM)** | $S < X$ | $S > X$ |

- Các option **deep ITM** có exercise value cao và time value thấp
- Các option **ATM** có time value cao nhất
- Các option **deep OTM** có exercise value bằng không — toàn bộ giá trị của chúng là time value

## 2. Arbitrage và Replication: Options so với Forward Commitments

| Đặc điểm | Forward Commitments | Options (Contingent Claims) |
|---------|--------------------|-----------------------------|
| Giá trị ban đầu | $V_0 = 0$ | Dương (tức **premium**) |
| Payoff | Đối xứng | **Không đối xứng** (downside có giới hạn) |
| Phương pháp định giá | Replication chính xác theo no-arbitrage | **No-arbitrage bounds** (không phải replication chính xác) |
| Replication | Mua tài sản cơ sở + vay/cho vay | Đòi hỏi dynamic hedging |

> **Nhận thức cốt lõi**: Vì options có payoff không đối xứng, chúng không thể được định giá bằng cách replication tĩnh đơn giản như forwards. Thay vào đó, chúng ta xác định **các giới hạn trên và dưới** của giá option và sử dụng các mô hình phức tạp hơn (binomial, Black-Scholes) để định giá chính xác.

## 3. No-Arbitrage Bounds cho European Options

### Giới Hạn Dưới (Lower Bounds)

$$c_0 \geq \max\left(0,\; S_0 - \frac{X}{(1+r)^T}\right)$$

$$p_0 \geq \max\left(0,\; \frac{X}{(1+r)^T} - S_0\right)$$

**Giải thích trực quan**: Một call phải có giá trị ít nhất bằng giá cổ phiếu hiện tại trừ đi present value của strike — nếu không sẽ tồn tại cơ hội arbitrage (mua call, bán khống cổ phiếu, đầu tư PV của $X$).

### Giới Hạn Trên (Upper Bounds)

$$c_0 \leq S_0$$

$$p_0 \leq \frac{X}{(1+r)^T}$$

**Giải thích trực quan**: Một call không bao giờ có thể có giá trị hơn bản thân cổ phiếu. Một put không bao giờ có thể có giá trị hơn present value của strike (mức thanh toán tối đa của put là $X$ tại đáo hạn).

## 4. Các Yếu Tố Ảnh Hưởng đến Giá Trị Option

| Yếu tố | Giá trị Call | Giá trị Put | Giải thích |
|--------|-----------|-----------|-------------|
| Spot price $S$ $\uparrow$ | $\uparrow$ | $\downarrow$ | $S$ tăng có lợi cho người nắm giữ call, bất lợi cho người nắm giữ put |
| Strike price $X$ $\uparrow$ | $\downarrow$ | $\uparrow$ | $X$ cao hơn khiến call trả ít hơn, put trả nhiều hơn |
| Thời gian đến đáo hạn $T$ $\uparrow$ | $\uparrow$ | $\uparrow$ | Thời gian nhiều hơn = tiềm năng biến động thuận lợi cao hơn |
| Lãi suất phi rủi ro $r$ $\uparrow$ | $\uparrow$ | $\downarrow$ | $r$ cao hơn làm giảm PV của strike; có lợi cho calls |
| Volatility $\sigma$ $\uparrow$ | $\uparrow$ | $\uparrow$ | Bất định cao hơn làm tăng giá trị của optionality |
| Cổ tức/Thu nhập $\uparrow$ | $\downarrow$ | $\uparrow$ | Cổ tức làm giảm $S$ vào ngày ex-date; bất lợi cho calls, có lợi cho puts |

> **Nhận thức cốt lõi**: Volatility luôn làm tăng giá trị option cho cả calls lẫn puts. Điều này là vì options có downside giới hạn (bạn không thể mất nhiều hơn premium đã trả) nhưng có tiềm năng upside không giới hạn hoặc đáng kể.

---

**Xem thêm**: [[derivatives/modules/m09-put-call-parity/index|M09: Put-Call Parity]], [[derivatives/modules/m10-binomial-model/index|M10: Binomial Model]]

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]]