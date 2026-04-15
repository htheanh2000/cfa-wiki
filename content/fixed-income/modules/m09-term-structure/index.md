---
title: "M09 — Term Structure"
type: module
subject: fixed-income
module: M09
los:
  - 9.a: Define and describe spot rates, forward rates, and par rates
  - 9.b: Calculate and interpret spot, forward, and par rates
  - 9.c: Describe the shape of the yield curve and relate it to spot, forward, and par rates
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - term-structure
  - spot-rates
  - forward-rates
  - par-curve
  - yield-curve
---

# The Term Structure of Interest Rates

## Spot Rates

### Định nghĩa

**Spot rate** ($S_t$) là yield của một trái phiếu zero-coupon (discount bond) đáo hạn tại thời điểm $t$. Tập hợp các spot rate cho các kỳ hạn khác nhau tạo thành **spot rate curve** (còn gọi là **strip curve** hoặc **zero curve**).

### Định giá trái phiếu bằng Spot Rates (No-Arbitrage Pricing)

Mỗi dòng tiền được chiết khấu theo spot rate tương ứng với kỳ hạn của nó:

$$\text{PV} = \sum_{t=1}^{N} \frac{CF_t}{(1 + S_t)^t}$$

Cách này cho ra **no-arbitrage price** — loại bỏ mọi khả năng kiếm lợi nhuận không rủi ro thông qua việc tách (stripping) và bán riêng lẻ các dòng tiền.

---

## Par Curve

**Par curve** là chuỗi YTM của các trái phiếu được định giá ở mệnh giá (Price = Face Value). Với một par bond:

$$100 = \sum_{t=1}^{N} \frac{C_{\text{par}}}{(1 + S_t)^t} + \frac{100}{(1 + S_N)^N}$$

trong đó $C_{\text{par}}$ là coupon rate khiến trái phiếu giao dịch ở mệnh giá.

### Suy ra Par Rates từ Spot Rates

$$C_{\text{par}} = \frac{1 - \frac{1}{(1+S_N)^N}}{\sum_{t=1}^{N} \frac{1}{(1+S_t)^t}}$$

Par rate cho kỳ hạn $N$ là một dạng trung bình phức tạp của các spot rate đến kỳ hạn $N$.

---

## Forward Rates

### Ký hiệu

$_AY_BY$ = forward rate cho một khoản vay bắt đầu sau $A$ năm và kéo dài $B$ năm.

Ví dụ:
- $_{0}Y_{1}Y = S_1$ (spot rate 1 năm hiện tại)
- $_{1}Y_{1}Y$ = lãi suất 1 năm, bắt đầu sau 1 năm
- $_{2}Y_{3}Y$ = lãi suất 3 năm, bắt đầu sau 2 năm

### Quan hệ No-Arbitrage

Spot rates và forward rates liên kết với nhau qua no-arbitrage:

$$(1 + S_n)^n = (1 + S_1)(1 + {_1Y_{1}Y})(1 + {_2Y_{1}Y}) \cdots (1 + {_{(n-1)}Y_{1}Y})$$

Tổng quát hơn:

$$(1 + S_{A+B})^{A+B} = (1 + S_A)^A \times (1 + {_AY_{B}Y})^B$$

### Tính Forward Rates từ Spot Rates

$$(1 + {_AY_{B}Y})^B = \frac{(1 + S_{A+B})^{A+B}}{(1 + S_A)^A}$$

### Tính Spot Rates từ Forward Rates

$$(1 + S_n)^n = \prod_{k=0}^{n-1}(1 + {_kY_{1}Y})$$

$$S_n = \left[\prod_{k=0}^{n-1}(1 + {_kY_{1}Y})\right]^{1/n} - 1$$

---

## Định giá trái phiếu bằng Forward Rates

Một trái phiếu có thể được định giá bằng cách chiết khấu từng dòng tiền qua chuỗi forward rates:

$$\text{PV} = \frac{CF_1}{(1 + {_0Y_{1}Y})} + \frac{CF_2}{(1 + {_0Y_{1}Y})(1 + {_1Y_{1}Y})} + \cdots + \frac{CF_N}{\prod_{k=0}^{N-1}(1 + {_kY_{1}Y})}$$

Cách này cho ra cùng no-arbitrage price như khi chiết khấu bằng spot rates.

---

## Hình dạng Yield Curve và Mối quan hệ giữa các Rates

### Đường cong dốc lên (Normal)

| Mối quan hệ | Thứ tự |
|-------------|--------|
| Par curve | Thấp nhất |
| Spot curve | Trung bình |
| Forward curve | Cao nhất |

$$\text{Par rate} < \text{Spot rate} < \text{Forward rate}$$

Trực giác: spot rates là trung bình nhân của các forward rates. Nếu forward rates đang tăng, trung bình (spot) sẽ thấp hơn, và par rates còn thấp hơn nữa.

### Đường cong phẳng (Flat)

$$\text{Par rate} = \text{Spot rate} = \text{Forward rate}$$

Cả ba đường cong đều trùng nhau.

### Đường cong nghịch — dốc xuống (Inverted)

| Mối quan hệ | Thứ tự |
|-------------|--------|
| Par curve | Cao nhất |
| Spot curve | Trung bình |
| Forward curve | Thấp nhất |

$$\text{Forward rate} < \text{Spot rate} < \text{Par rate}$$

---

## Bootstrapping Spot Rates

Spot rates được rút ra từ par rates theo từng bước:

1. $S_1 = \text{Par}_1$ (par rate kỳ hạn 1 = spot rate)
2. Dùng $S_1$ và par bond 2 năm để giải tìm $S_2$
3. Tiếp tục lặp lại cho từng kỳ hạn

$$100 = \frac{C_2}{(1+S_1)} + \frac{100 + C_2}{(1+S_2)^2} \implies \text{solve for } S_2$$

---

## See Also

- [[fixed-income/m07-yield-spread-fixed-rate/index|M07 - Yield Spread for Fixed-Rate Bonds]]
- [[fixed-income/m10-interest-rate-risk-return/index|M10 - Interest Rate Risk and Return]]
- [[fixed-income/m13-curve-based-risk/index|M13 - Curve-Based Risk Measures]]