---
title: Term Structure of Interest Rates
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [spot-rate, forward-rate, par-curve, yield-curve, bootstrapping]
---

# Term Structure of Interest Rates

## Ba Đường Cong Cơ Bản

### 1. Spot Curve (Zero-Coupon Curve)

**Spot rate** $S_t$ là lợi suất của một trái phiếu zero-coupon đáo hạn tại thời điểm $t$.

- Đại diện cho **lợi suất hàng năm** của một khoản thanh toán một lần tại ngày đáo hạn
- Mỗi dòng tiền cần được chiết khấu theo spot rate tương ứng với kỳ hạn của nó
- Spot curve thể hiện spot rate tại các kỳ hạn khác nhau

**Định giá trái phiếu không có cơ hội kinh doanh chênh lệch giá (no-arbitrage) bằng spot rates:**

$$PV = \frac{PMT}{(1+S_1)^1} + \frac{PMT}{(1+S_2)^2} + \cdots + \frac{PMT + FV}{(1+S_n)^n}$$

### 2. Par Curve

**Par rate** là coupon rate khiến giá trái phiếu bằng đúng mệnh giá (par) tại mỗi kỳ hạn.

- Được suy ra từ spot curve
- Mỗi điểm trên par curve là coupon rate của một trái phiếu **định giá ngang mệnh giá** tại kỳ hạn đó
- Dùng để định giá các đợt phát hành trái phiếu mới tại mệnh giá

### 3. Forward Curve

**Forward rate** là lãi suất cho một khoảng thời gian trong tương lai, được ngụ ý bởi các spot rate hiện tại.

## Ký Hiệu Forward Rate

Ký hiệu $AyBy$ (hoặc $f_{A,B}$) có nghĩa là:

> Lãi suất hàng năm của một **khoản vay $B$ năm** bắt đầu **sau $A$ năm kể từ hiện tại**

**Ví dụ:**
- $1y1y$: lãi suất 1 năm, bắt đầu 1 năm kể từ hiện tại
- $2y3y$: lãi suất 3 năm, bắt đầu 2 năm kể từ hiện tại
- $0y1y$: spot rate 1 năm (bắt đầu ngay hiện tại) = $S_1$

## Mối Quan Hệ Giữa Spot Rate và Forward Rate

### Forward Rate từ Spot Rates

$$(1 + S_n)^n = (1 + S_1)^1 \times (1 + f_{1,1})^1 \times (1 + f_{2,1})^1 \times \cdots \times (1 + f_{n-1,1})^1$$

**Công thức tổng quát cho forward rate một kỳ:**

$$(1 + S_n)^n = (1 + S_{n-1})^{n-1} \times (1 + f_{n-1,1})$$

Suy ra:

$$f_{n-1,1} = \frac{(1 + S_n)^n}{(1 + S_{n-1})^{n-1}} - 1$$

**Công thức tổng quát cho forward rate nhiều kỳ:**

$$(1 + S_{A+B})^{A+B} = (1 + S_A)^A \times (1 + f_{A,B})^B$$

## Bootstrapping

Quá trình suy ra spot rates từ par curve:

1. Par rate 1 năm = spot rate 1 năm: $S_1 = \text{Par}_1$
2. Dùng $S_1$ để giải tìm $S_2$ từ trái phiếu par kỳ hạn 2 năm
3. Dùng $S_1, S_2$ để giải tìm $S_3$ từ trái phiếu par kỳ hạn 3 năm
4. Tiếp tục lặp lại theo thứ tự

## Mối Quan Hệ Giữa Các Đường Cong

### Khi Spot Curve Dốc Lên (Upward Sloping):
- Forward curve nằm **trên** spot curve
- Par curve nằm **dưới** spot curve
- Thứ tự: Forward > Spot > Par

### Khi Spot Curve Dốc Xuống (Inverted):
- Forward curve nằm **dưới** spot curve
- Par curve nằm **trên** spot curve
- Thứ tự: Par > Spot > Forward

### Khi Spot Curve Phẳng (Flat):
- Cả ba đường cong hoàn toàn trùng nhau
- Forward = Spot = Par

## Forward Rates và Lợi Suất Trái Phiếu

- Nếu forward rates **được hiện thực hóa**: tất cả trái phiếu đều mang lại **cùng mức lợi suất** (tức là spot rate kỳ 1)
- Nếu spot rates thực tế **thấp hơn** forward rates ngụ ý: trái phiếu dài hạn vượt trội hơn
- Nếu spot rates thực tế **cao hơn** forward rates ngụ ý: trái phiếu ngắn hạn vượt trội hơn

## Các Lý Thuyết về Yield Curve

| Lý thuyết | Ý tưởng cốt lõi |
|--------|----------|
| **Pure Expectations** | Forward rates = spot rates kỳ vọng trong tương lai |
| **Local Expectations** | Trong ngắn hạn, tất cả trái phiếu đều mang lại lợi suất bằng lãi suất phi rủi ro |
| **Liquidity Preference** | Forward rates = spot rates kỳ vọng + phần bù thanh khoản (liquidity premium) |
| **Segmented Markets** | Cung và cầu trong từng phân khúc kỳ hạn độc lập xác định lãi suất |
| **Preferred Habitat** | Tương tự Segmented Markets nhưng nhà đầu tư sẵn sàng chuyển sang phân khúc khác nếu nhận được phần bù đủ lớn |

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/bond-valuation|Bond Valuation]]
- [[fixed-income/concepts/yield-spreads|Yield Spreads]]
- [[fixed-income/concepts/interest-rate-risk|Interest Rate Risk]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m09|Glossary: Module 09]]