---
title: Contingent Claims
type: concept
subject: derivatives
module: "M02"
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, options, call, put, CDS, contingent-claim]
---

# Contingent Claims

**Contingent claim** là một loại công cụ phái sinh mà khoản thanh toán phụ thuộc vào việc một sự kiện hoặc điều kiện cụ thể có xảy ra hay không. Khác với forward commitments, người nắm giữ có **quyền nhưng không có nghĩa vụ** phải thực hiện giao dịch.

---

## Options

**Option** trao cho người mua (holder) quyền — nhưng không phải nghĩa vụ — để mua hoặc bán tài sản cơ sở tại một mức giá định trước (strike/exercise price) vào hoặc trước một ngày xác định.

### Call Option

- **Quyền mua** tài sản cơ sở tại strike price $X$
- Người mua có lãi khi $S_T > X$

**Payoff (long call)**:

$$c_T = \max(0,\; S_T - X)$$

**Payoff (short call)**:

$$-c_T = -\max(0,\; S_T - X)$$

### Put Option

- **Quyền bán** tài sản cơ sở tại strike price $X$
- Người mua có lãi khi $S_T < X$

**Payoff (long put)**:

$$p_T = \max(0,\; X - S_T)$$

**Payoff (short put)**:

$$-p_T = -\max(0,\; X - S_T)$$

### Profit = Payoff - Premium

$$\text{Profit}_{\text{long call}} = \max(0,\; S_T - X) - c_0$$

$$\text{Profit}_{\text{long put}} = \max(0,\; X - S_T) - p_0$$

trong đó $c_0$ và $p_0$ là option premium phải trả tại thời điểm khởi tạo hợp đồng.

### European vs American Options

| Đặc điểm | European | American |
|---|---|---|
| Thời điểm thực hiện | Chỉ tại ngày đáo hạn ($T$) | Bất kỳ lúc nào đến $T$ |
| Định giá | Dễ mô hình hóa hơn | Phức tạp hơn (early exercise premium) |
| Quan hệ giá trị | $\text{American} \geq \text{European}$ | Luôn có giá trị ít nhất bằng |
| Ứng dụng phổ biến | Index options, FX | Equity options |

> American option **có giá trị ít nhất bằng** European option có cùng điều kiện, vì nó có tất cả quyền như nhau cộng thêm quyền thực hiện sớm (early exercise).

### Moneyness

| Trạng thái | Call ($S$ so với $X$) | Put ($S$ so với $X$) | Ý nghĩa |
|---|---|---|---|
| **In-the-money (ITM)** | $S > X$ | $S < X$ | Giá trị thực hiện dương |
| **At-the-money (ATM)** | $S = X$ | $S = X$ | Giá trị thực hiện bằng không |
| **Out-of-the-money (OTM)** | $S < X$ | $S > X$ | Giá trị thực hiện âm (sẽ không thực hiện) |
| **Deep ITM** | $S \gg X$ | $S \ll X$ | Giá trị thực hiện rất cao |
| **Deep OTM** | $S \ll X$ | $S \gg X$ | Rất khó được thực hiện |

### Các thành phần giá trị của Option

$$\text{Option Premium} = \text{Exercise (Intrinsic) Value} + \text{Time Value}$$

- **Exercise value**: khoản thanh toán nếu thực hiện ngay lập tức = $\max(0, S - X)$ đối với call
- **Time value**: giá trị bổ sung xuất phát từ khả năng option trở nên có giá trị hơn trước khi đáo hạn

> Time value luôn $\geq 0$ đối với American options. Với European options, time value đôi khi có thể âm đối với deep ITM put.

---

## Credit Derivatives

### Credit Default Swap (CDS)

**CDS** là hợp đồng cung cấp bảo vệ tương tự bảo hiểm trước các credit events (vỡ nợ, phá sản, tái cơ cấu) của một reference entity.

**Cấu trúc**:
- **Protection buyer**: trả định kỳ phí (CDS spread) cho bên bán
- **Protection seller**: bồi thường cho người mua khi credit event xảy ra

$$\text{CDS Spread} \approx \text{Probability of Default} \times \text{Loss Given Default}$$

**Thanh toán khi xảy ra credit event**:
- **Physical settlement**: người mua giao nộp trái phiếu vỡ nợ, người bán trả mệnh giá (par)
- **Cash settlement**: người bán trả phần chênh lệch giữa par và recovery value

### Credit-Linked Note (CLN)

**CLN** là funded credit derivative — về bản chất là một trái phiếu mà việc hoàn trả gốc phụ thuộc vào tình hình tín dụng của một reference entity.

- Nếu **không có credit event**: nhà đầu tư nhận toàn bộ gốc + coupon
- Nếu **có credit event**: gốc của nhà đầu tư bị giảm theo mức tổn thất

> CLN = trái phiếu phi rủi ro (risk-free bond) + short CDS (nhà đầu tư bán credit protection)

---

## Forward Commitments vs Contingent Claims

| Đặc điểm | Forward Commitment | Contingent Claim |
|---|---|---|
| Nghĩa vụ | Cả hai bên đều bị ràng buộc | Chỉ bên bán bị ràng buộc |
| Chi phí ban đầu | Bằng không (thông thường) | Premium do người mua trả |
| Hình dạng payoff | Đối xứng (tuyến tính) | Bất đối xứng (phi tuyến) |
| Lỗ tối đa (người mua) | Có thể không giới hạn | Giới hạn ở mức premium |
| Ví dụ | Forwards, futures, swaps | Options, CDS, CLN |

---

## See Also

- [[derivatives/concepts/derivative-instruments|Derivative Instruments]]
- [[derivatives/concepts/forward-commitments|Forward Commitments]]
- [[derivatives/concepts/option-valuation|Option Valuation]]
- [[derivatives/concepts/put-call-parity|Put-Call Parity]]
- [[derivatives/glossary/der-m02|Glossary — M02]]