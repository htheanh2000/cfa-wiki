---
title: "M10 — Binomial Model"
type: module
subject: derivatives
module: M10
los: "10.a-10.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m10
  - binomial-model
  - option-pricing
  - risk-neutral
  - hedge-ratio
  - replication
---

# M10: Binomial Option Pricing Model

> **LOS 10.a**: Giải thích cách mô hình binomial có thể được dùng để định giá options.
> **LOS 10.b**: Mô tả cách giá trị của một option thay đổi khi các tham số đầu vào thay đổi.

## 1. Thiết lập mô hình One-Period Binomial

Giá tài sản cơ sở $S_0$ có thể di chuyển đến một trong hai giá trị trong một kỳ:

$$S_1^{+} = S_0 \times u \quad \text{(up move)}$$

$$S_1^{-} = S_0 \times d \quad \text{(down move)}$$

trong đó:
- $u$ = hệ số tăng (up factor, $u > 1$)
- $d$ = hệ số giảm (down factor, $d < 1$)
- Điều kiện $u > (1 + r) > d$ là bắt buộc để ngăn chặn arbitrage

### Giá trị Call Option tại thời điểm đáo hạn

$$c_1^{+} = \max(0,\; S_1^{+} - X) = \max(0,\; S_0 u - X)$$

$$c_1^{-} = \max(0,\; S_1^{-} - X) = \max(0,\; S_0 d - X)$$

### Giá trị Put Option tại thời điểm đáo hạn

$$p_1^{+} = \max(0,\; X - S_1^{+}) = \max(0,\; X - S_0 u)$$

$$p_1^{-} = \max(0,\; X - S_1^{-}) = \max(0,\; X - S_0 d)$$

## 2. Phương pháp Hedge Ratio (Replication)

**Hedge ratio** $h$ xác định số lượng cổ phiếu cần thiết để tái tạo (replicate) payoff của option:

$$h = \frac{c_1^{+} - c_1^{-}}{S_1^{+} - S_1^{-}}$$

trong đó:
- $h$ còn được gọi là **delta** của option
- Với call: $0 \leq h \leq 1$
- Với put: $-1 \leq h \leq 0$

### Replicating Portfolio

Một danh mục gồm $h$ cổ phiếu và một vị thế bán (short position) một call tạo thành một **risk-free hedge**:

- Trạng thái tăng: $h \times S_1^{+} - c_1^{+}$
- Trạng thái giảm: $h \times S_1^{-} - c_1^{-}$

Hai giá trị này bằng nhau (theo cấu trúc xây dựng), do đó danh mục không có rủi ro. Giá trị hiện tại của nó là:

$$V_0 = \frac{h \times S_1^{+} - c_1^{+}}{1 + r}$$

Giá call khi đó là:

$$c_0 = h \times S_0 - V_0$$

## 3. Phương pháp Risk-Neutral Probability

### Risk-Neutral Probability

$$\pi = \frac{1 + r - d}{u - d}$$

trong đó:
- $\pi$ = risk-neutral probability của một up move
- $(1 - \pi)$ = risk-neutral probability của một down move

### Risk-Neutral Pricing cho Call

$$c_0 = \frac{\pi \, c_1^{+} + (1 - \pi) \, c_1^{-}}{1 + r}$$

### Risk-Neutral Pricing cho Put

$$p_0 = \frac{\pi \, p_1^{+} + (1 - \pi) \, p_1^{-}}{1 + r}$$

> **Điểm mấu chốt**: **Xác suất thực tế (real-world probabilities)** của up move và down move ($q$ và $1 - q$) **không ảnh hưởng** đến việc định giá option. Chỉ có **risk-neutral probabilities** ($\pi$ và $1 - \pi$) được sử dụng. Lý do là option được định giá bằng phương pháp replication — danh mục hedge hoạt động bất kể xác suất thực tế là bao nhiêu.

## 4. Ví dụ số

Giả sử $S_0 = 100$, $u = 1.20$, $d = 0.80$, $r = 5\%$, $X = 100$:

**Bước 1**: Tính giá cuối kỳ và giá trị call:
- $S_1^{+} = 100 \times 1.20 = 120$, suy ra $c_1^{+} = \max(0, 120 - 100) = 20$
- $S_1^{-} = 100 \times 0.80 = 80$, suy ra $c_1^{-} = \max(0, 80 - 100) = 0$

**Bước 2**: Risk-neutral probability:

$$\pi = \frac{1.05 - 0.80}{1.20 - 0.80} = \frac{0.25}{0.40} = 0.625$$

**Bước 3**: Giá call:

$$c_0 = \frac{0.625 \times 20 + 0.375 \times 0}{1.05} = \frac{12.50}{1.05} = 11.90$$

**Kiểm chứng bằng hedge ratio**:

$$h = \frac{20 - 0}{120 - 80} = 0.50$$

$$V_0 = \frac{0.50 \times 120 - 20}{1.05} = \frac{40}{1.05} = 38.10$$

$$c_0 = 0.50 \times 100 - 38.10 = 11.90 \; \checkmark$$

## 5. Volatility và giá trị Option

Khoảng cách giữa $u$ và $d$ phản ánh **volatility** của tài sản cơ sở:

$$\text{Volatility càng cao} \iff \text{khoảng cách } u - d \text{ càng rộng} \iff \text{giá trị option càng cao}$$

| Volatility | $u$ và $d$ | Giá trị Option |
|-----------|-------------|----------------|
| Thấp | $u$ gần $d$ | Thấp hơn |
| Cao | $u$ xa $d$ | **Cao hơn** |

**Trực giác**: Volatility cao hơn làm tăng xác suất xảy ra những biến động lớn có lợi (mà option sẽ hưởng lợi từ đó), trong khi phần thua lỗ bị giới hạn ở mức phí premium đã trả. Sự bất đối xứng này có nghĩa là volatility cao hơn luôn có lợi cho người nắm giữ option.

---

**Xem thêm**: [[derivatives/modules/m08-options-pricing-valuation/index|M08: Options Pricing and Valuation]], [[derivatives/modules/m09-put-call-parity/index|M09: Put-Call Parity]]

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]]