---
title: Option Valuation
type: concept
subject: derivatives
module: "M08"
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, options, valuation, binomial, bounds]
---

# Option Valuation

## Giới Hạn Giá Quyền Chọn

### Giới Hạn Trên

**Call option**: một call không bao giờ có giá trị lớn hơn chính tài sản cơ sở.

$$c_0 \leq S_0 \quad \text{(European and American)}$$

**Put option**: một put không bao giờ có giá trị lớn hơn giá strike (đối với European: giá trị hiện tại của strike).

$$p_0 \leq \frac{X}{(1+r)^T} \quad \text{(European)}$$

$$P_0 \leq X \quad \text{(American)}$$

### Giới Hạn Dưới

**European call** (không trả cổ tức):

$$c_0 \geq \max\!\left(0,\; S_0 - \frac{X}{(1+r)^T}\right)$$

**European put** (không trả cổ tức):

$$p_0 \geq \max\!\left(0,\; \frac{X}{(1+r)^T} - S_0\right)$$

> Giới hạn dưới bằng **giá trị thực hiện (exercise value) đã điều chỉnh theo giá trị thời gian của tiền**. Nếu quyền chọn giao dịch dưới giới hạn này, cơ hội arbitrage sẽ xuất hiện.

---

## Các Yếu Tố Ảnh Hưởng Đến Giá Trị Quyền Chọn

| Yếu tố | Giá trị Call | Giá trị Put | Lý giải |
|---|---|---|---|
| $S_0$ (giá spot) $\uparrow$ | $\uparrow$ | $\downarrow$ | Spot tăng → call sâu hơn ITM, put kém ITM hơn |
| $X$ (strike price) $\uparrow$ | $\downarrow$ | $\uparrow$ | Strike tăng → call kém ITM hơn, put sâu hơn ITM |
| $T$ (thời gian đến đáo hạn) $\uparrow$ | $\uparrow$ | $\uparrow$* | Nhiều thời gian hơn → nhiều cơ hội biến động thuận lợi hơn |
| $r$ (lãi suất phi rủi ro) $\uparrow$ | $\uparrow$ | $\downarrow$ | $r$ cao hơn làm giảm PV của strike |
| $\sigma$ (volatility) $\uparrow$ | $\uparrow$ | $\uparrow$ | Bất ổn nhiều hơn → giá trị quyền chọn cao hơn |
| Cổ tức $\uparrow$ | $\downarrow$ | $\uparrow$ | Cổ tức làm giảm giá cổ phiếu vào ngày ex-date |

*Đối với European put, tác động của thời gian có thể không rõ ràng với các put sâu trong ITM.

### Tác Động Của Volatility

Volatility là yếu tố **quan trọng nhất** đặc trưng riêng cho quyền chọn (so với forwards). Quyền chọn có payoff bất đối xứng, do đó:
- Volatility cao hơn làm tăng xác suất xảy ra các biến động lớn theo chiều có lợi
- Tổn thất tối đa được giới hạn ở mức phí quyền chọn (premium) đã trả
- Do đó, **cả call lẫn put** đều tăng giá trị khi volatility tăng

### Tác Động Của Lãi Suất Phi Rủi Ro

- **Call**: $r$ cao hơn → PV của strike thấp hơn → call có giá trị cao hơn
- **Put**: $r$ cao hơn → PV của strike thấp hơn → put có giá trị thấp hơn

---

## Mô Hình Binomial Một Kỳ

Mô hình binomial định giá quyền chọn bằng cách xây dựng một danh mục sao chép (replicating portfolio) trong khung thời gian rời rạc.

### Thiết Lập

Tại thời điểm $T$, cổ phiếu có thể di chuyển đến một trong hai giá trị:

$$S^+ = S_0 \times u \quad \text{(trạng thái tăng)}$$
$$S^- = S_0 \times d \quad \text{(trạng thái giảm)}$$

trong đó $u$ = hệ số tăng ($u > 1$) và $d$ = hệ số giảm ($d < 1$).

### Giá Trị Quyền Chọn Tại Mỗi Trạng Thái

$$c^+ = \max(0,\; S^+ - X) \quad \text{(payoff của call ở trạng thái tăng)}$$
$$c^- = \max(0,\; S^- - X) \quad \text{(payoff của call ở trạng thái giảm)}$$

### Hedge Ratio

**Hedge ratio** (delta, $h$) là số cổ phiếu cần thiết để sao chép quyền chọn:

$$h = \frac{c^+ - c^-}{S^+ - S^-}$$

### Xác Suất Trung Tính Rủi Ro

$$\pi = \frac{(1 + r) - d}{u - d}$$

trong đó:
- $\pi$ = xác suất trung tính rủi ro của một lần tăng giá
- $(1 - \pi)$ = xác suất trung tính rủi ro của một lần giảm giá
- $r$ = lãi suất phi rủi ro mỗi kỳ

> $\pi$ **không phải** là xác suất thực tế của việc giá tăng. Đây là xác suất khiến lợi suất kỳ vọng của cổ phiếu bằng lãi suất phi rủi ro.

### Giá Quyền Chọn

$$c_0 = \frac{\pi \cdot c^+ + (1 - \pi) \cdot c^-}{1 + r}$$

Đây là công thức **risk-neutral pricing**: chiết khấu payoff kỳ vọng (theo xác suất trung tính rủi ro) tại lãi suất phi rủi ro.

### Replicating Portfolio

Quyền chọn có thể được sao chép bằng cách:
- Nắm giữ $h$ cổ phiếu của tài sản cơ sở
- Vay hoặc cho vay tại lãi suất phi rủi ro

$$c_0 = h \cdot S_0 + \frac{h \cdot S^- - c^-}{-(1+r)}$$

> Mô hình binomial cũng hoạt động với **put** — chỉ cần thay payoff của call bằng payoff của put: $p^+ = \max(0, X - S^+)$ và $p^- = \max(0, X - S^-)$.

---

## Những Điểm Chính Cần Ghi Nhớ

1. **No-arbitrage** đảm bảo quyền chọn giao dịch trong phạm vi giới hạn giá của chúng
2. **Volatility** luôn làm tăng giá trị quyền chọn (đặc trưng riêng của quyền chọn so với các công cụ phái sinh tuyến tính)
3. **Mô hình binomial** định giá quyền chọn bằng phương pháp sao chép — không giả định về xác suất thực tế của các biến động giá
4. **Risk-neutral pricing** là một công cụ toán học thuận tiện, không phải là tuyên bố về sở thích của nhà đầu tư

---

## Xem Thêm

- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/concepts/put-call-parity|Put-Call Parity]]
- [[derivatives/concepts/arbitrage-and-replication|Arbitrage and Replication]]
- [[derivatives/formulas/der-formulas|Derivatives Formula Sheet]]
- [[derivatives/glossary/der-m08|Glossary — M08]]
- [[derivatives/glossary/der-m10|Glossary — M10 (Binomial Model)]]