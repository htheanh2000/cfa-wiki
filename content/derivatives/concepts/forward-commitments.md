---
title: Forward Commitments
type: concept
subject: derivatives
module: "M02"
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, forwards, futures, swaps, forward-commitment]
---

# Forward Commitments

**Forward commitment** là một loại phái sinh trong đó cả hai bên đều có **nghĩa vụ** thực hiện giao dịch vào một ngày trong tương lai theo các điều khoản đã thỏa thuận hôm nay. Không bên nào được phép rút lui.

Ba loại chính:
1. **Forward contracts**
2. **Futures contracts**
3. **Swaps**

---

## 1. Forward Contracts

**Forward** là một thỏa thuận OTC để mua hoặc bán tài sản cơ sở vào một ngày trong tương lai xác định ($T$) tại mức giá đã thỏa thuận hôm nay ($F_0(T)$).

### Pricing

**No-arbitrage forward price** đảm bảo hợp đồng có giá trị bằng không tại thời điểm khởi tạo:

$$F_0(T) = S_0 \times (1 + r)^T$$

Khi có thu nhập ($I$) và chi phí lưu trữ/carry ($C$):

$$F_0(T) = \bigl[S_0 - PV_0(I) + PV_0(C)\bigr] \times (1 + r)^T$$

trong đó:
- $S_0$ = giá giao ngay hiện tại
- $r$ = lãi suất phi rủi ro (mỗi kỳ)
- $T$ = thời gian đến ngày đáo hạn
- $PV_0(I)$ = giá trị hiện tại của thu nhập (cổ tức, coupon)
- $PV_0(C)$ = giá trị hiện tại của chi phí lưu giữ (lưu trữ, bảo hiểm)

### Payoff at Expiration

**Long forward** (bên mua):

$$\text{Payoff}_{\text{long}} = S_T - F_0(T)$$

**Short forward** (bên bán):

$$\text{Payoff}_{\text{short}} = F_0(T) - S_T$$

> Payoff của forward có tính **đối xứng** — lợi nhuận của bên này bằng đúng tổn thất của bên kia (trò chơi tổng bằng không).

### Valuation During Life

$$V_t(\text{long}) = S_t - \frac{F_0(T)}{(1 + r)^{T-t}}$$

Tại thời điểm khởi tạo: $V_0 = 0$. Tại ngày đáo hạn: $V_T = S_T - F_0(T)$.

### Settlement

- **Physical settlement**: giao hàng thực tế tài sản cơ sở
- **Cash settlement**: bên thua trả cho bên thắng phần chênh lệch $|S_T - F_0(T)|$

---

## 2. Futures Contracts

**Futures contract** là một forward commitment được chuẩn hóa, giao dịch trên sàn, với cơ chế thanh toán hàng ngày (mark-to-market).

### Điểm Khác Biệt So Với Forwards

| Đặc điểm | Forward | Futures |
|---|---|---|
| Địa điểm giao dịch | OTC | Sàn giao dịch |
| Tiêu chuẩn hóa | Tùy chỉnh | Chuẩn hóa |
| Rủi ro đối tác | Song phương | CCP (clearinghouse) |
| Thanh toán | Tại ngày đáo hạn | Hàng ngày (MTM) |
| Margin | Tài sản thế chấp thỏa thuận | Initial + maintenance margin |
| Thanh khoản | Thấp hơn | Cao hơn |

### Mark-to-Market (Daily Settlement)

Mỗi ngày, futures price được so sánh với settlement price của ngày hôm trước:
- **Lãi** → được ghi có vào tài khoản margin
- **Lỗ** → bị ghi nợ từ tài khoản margin

Nếu tài khoản margin giảm xuống dưới mức **maintenance margin**, một **margin call** yêu cầu nhà giao dịch nạp thêm tiền về mức **initial margin**.

### Margin Mechanics

| Thuật ngữ | Định nghĩa |
|---|---|
| Initial margin | Khoản tiền đặt cọc cần có để mở vị thế |
| Maintenance margin | Số dư tối thiểu trước khi bị margin call |
| Variation margin | Lãi/lỗ hàng ngày từ MTM settlement |
| Margin call | Yêu cầu bổ sung tiền về mức initial margin |

### Interest Rate Futures

Đối với interest rate futures (ví dụ: Eurodollar, SOFR futures):

$$f = 100 - \text{yield}$$

**Basis Point Value (BPV)**:

$$\text{BPV} = \text{Notional} \times 0.01\% \times \text{Period}$$

---

## 3. Swaps

**Swap** là một thỏa thuận OTC để trao đổi một chuỗi dòng tiền theo thời gian — về bản chất là một danh mục các forward contracts.

### Interest Rate Swap (Plain Vanilla)

Loại swap phổ biến nhất: một bên trả **lãi suất cố định (fixed)**, bên kia trả **lãi suất thả nổi (floating)** (dựa trên MRR như SOFR).

**Thanh toán ròng mỗi kỳ**:

$$\text{Settlement}_n = (\text{MRR}_n - F) \times \text{Notional} \times \text{Period}$$

trong đó:
- $\text{MRR}_n$ = market reference rate được xác định vào *đầu* kỳ $n$
- $F$ = fixed swap rate (par swap rate)
- Period = phân số tính ngày (ví dụ: $\frac{90}{360}$)

> Chỉ có **khoản ròng** được trao đổi — vốn gốc danh nghĩa (notional principal) **không bao giờ** được trao đổi trong interest rate swap.

### Swap Structure

- **Fixed-rate payer** (long swap): hưởng lợi khi lãi suất tăng
- **Floating-rate payer** (short swap): hưởng lợi khi lãi suất giảm
- **Par swap rate**: mức lãi suất cố định khiến giá trị swap bằng không tại thời điểm khởi tạo

### Xác Định Par Swap Rate

Par swap rate được tính từ cấu trúc kỳ hạn của spot rates, đảm bảo:

$$\sum_{i=1}^{N} \frac{F \times \text{Period}}{(1 + z_i)^i} + \frac{1}{(1 + z_N)^N} = 1$$

trong đó $z_i$ = spot rate cho kỳ $i$.

---

## See Also

- [[derivatives/concepts/derivative-instruments|Derivative Instruments]]
- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/concepts/arbitrage-and-replication|Arbitrage and Replication]]
- [[derivatives/formulas/der-formulas|Derivatives Formula Sheet]]
- [[derivatives/glossary/der-m02|Glossary — M02]]