---
title: Alternative Investment Performance Measurement
type: concept
subject: alternative-investments
created: 2026-04-12
updated: 2026-04-12
tags: [performance, J-curve, IRR, MOIC, fees, hurdle-rate, high-water-mark, clawback, waterfall]
---

# Alternative Investment Performance Measurement

## Hiệu Ứng J-Curve

**J-curve** mô tả mô hình lợi nhuận điển hình của một quỹ PE/VC trong suốt vòng đời của nó:

1. **Những năm đầu (Năm 1-3)**: lợi nhuận âm do management fees, chi phí quỹ, và các khoản đầu tư chưa thực hiện được định giá bằng hoặc thấp hơn giá vốn
2. **Giai đoạn giữa (Năm 3-5)**: lợi nhuận cải thiện khi các công ty trong danh mục trưởng thành và các đợt thoái vốn đầu tiên diễn ra
3. **Những năm cuối (Năm 5-10+)**: lợi nhuận dương và thường rất cao khi các khoản đầu tư thành công được thoái vốn

Mô hình này giống hình chữ "J" khi vẽ đồ thị lợi nhuận tích lũy theo thời gian.

## Các Thước Đo Lợi Nhuận

### Internal Rate of Return (IRR)

Tỷ lệ chiết khấu làm cho NPV của tất cả các dòng tiền bằng không:

$$\sum_{t=0}^{T} \frac{CF_t}{(1 + IRR)^t} = 0$$

trong đó:
- $CF_t$ = dòng tiền tại thời điểm $t$ (âm cho các khoản đóng góp vốn, dương cho các khoản phân phối)
- $T$ = tổng số kỳ

**Đặc điểm chính**:
- Tính đến thời điểm của các dòng tiền
- Thước đo tiêu chuẩn cho hiệu suất PE/VC
- Có thể bị điều chỉnh bởi thời điểm gọi vốn/phân phối
- Có thể xuất hiện vấn đề multiple IRR với các dòng tiền không thông thường

### Multiple on Invested Capital (MOIC)

$$\text{MOIC} = \frac{\text{Realized Value} + \text{Unrealized Value}}{\text{Total Amount Invested}}$$

| MOIC | Ý nghĩa |
|---|---|
| < 1.0x | Lỗ |
| 1.0x | Hòa vốn |
| > 1.0x | Có lãi |
| 2.0x | Gấp đôi khoản đầu tư |

**Đặc điểm chính**:
- Đơn giản và trực quan
- **Không** tính đến giá trị thời gian của tiền
- **Không** phản ánh thời điểm của các dòng tiền
- Nên sử dụng kết hợp với IRR để có bức tranh đầy đủ

### Gross vs. Net Returns

| Thước đo | Định nghĩa |
|---|---|
| **Gross return** | Lợi nhuận từ đầu tư trước khi trừ management fees và performance fees |
| **Net return** | Lợi nhuận sau khi trừ tất cả phí và chi phí; là khoản LP thực sự nhận được |

$$\text{Net Return} = \text{Gross Return} - \text{Management Fee} - \text{Performance Fee}$$

## Cấu Trúc Phí

### Management Fee

$$\text{Management Fee} = \text{Fee Rate} \times \text{AUM (or Committed Capital)}$$

- Thường là **1.5% - 2.0%** mỗi năm
- Trong **giai đoạn đầu tư**: thường tính trên **committed capital**
- Sau giai đoạn đầu tư: thường tính trên **invested capital** (hoặc NAV)
- Dùng để trang trải chi phí vận hành của quỹ

### Performance Fee (Carried Interest / Carry)

Phần lợi nhuận của GP, thường là **20%** lợi nhuận vượt trên hurdle rate.

#### Hard Hurdle Rate

GP chỉ nhận performance fee **trên phần lợi nhuận vượt quá** hurdle rate:

$$\text{Performance Fee} = \text{Fee Rate} \times (\text{Return} - \text{Hurdle Rate}) \times \text{Capital}$$

*Chỉ áp dụng nếu Return > Hurdle Rate*

#### Soft Hurdle Rate

Nếu vượt hurdle rate, GP nhận performance fee trên **toàn bộ lợi nhuận** (không chỉ phần vượt):

$$\text{Performance Fee} = \text{Fee Rate} \times \text{Total Return} \times \text{Capital}$$

*Chỉ áp dụng nếu Return > Hurdle Rate*

### Hurdle Rate

- Mức lợi nhuận tối thiểu quỹ phải đạt được trước khi GP được nhận performance fees
- Thường là **6-8%** mỗi năm
- Còn được gọi là **preferred return**
- Bảo vệ LP bằng cách đảm bảo mức lợi nhuận tối thiểu trước khi GP chia sẻ lợi nhuận

### High-Water Mark

- Mức NAV tích lũy cao nhất mà quỹ đã đạt được trước đó
- GP chỉ nhận performance fees trên các khoản tăng **vượt trên** high-water mark
- Ngăn GP thu phí trên khoản lợi nhuận phục hồi từ thua lỗ trước đó
- Chủ yếu được sử dụng bởi **hedge funds**

### Catch-up Clause

Sau khi hurdle rate được đáp ứng, GP nhận một tỷ lệ lợi nhuận bổ sung không cân xứng cho đến khi performance fee của họ "bắt kịp" mức lẽ ra được nhận nếu không có hurdle rate.

**Ví dụ**: Với hurdle rate 8% và catch-up 100%:
1. 8% lợi nhuận đầu tiên thuộc hoàn toàn về LP
2. Phần lợi nhuận tiếp theo thuộc hoàn toàn về GP cho đến khi GP nhận được 20% tổng lợi nhuận
3. Phần lợi nhuận còn lại chia theo tỷ lệ 80/20 (LP/GP)

### Clawback Provision

- Yêu cầu GP **hoàn trả performance fees** nếu các khoản đầu tư sau đó hoạt động kém
- Đảm bảo tổng carried interest của GP không vượt quá tỷ lệ đã thỏa thuận trên tổng lợi nhuận của quỹ
- Thường được quyết toán khi quỹ kết thúc
- Bảo vệ LP khỏi việc nộp thừa carry dựa trên các đợt thoái vốn sớm

## Distribution Waterfall

Thứ tự phân phối lợi nhuận của quỹ giữa GP và LP.

### Deal-by-Deal (American) Waterfall

1. Hoàn trả vốn đầu tư cho từng thương vụ
2. Preferred return trên từng thương vụ
3. Carry cho GP trên từng thương vụ

- GP nhận carry sớm hơn
- Có lợi hơn cho GP
- Clawback provision là cần thiết

### Whole-of-Fund (European) Waterfall

1. Hoàn trả **toàn bộ** vốn đầu tư trên toàn bộ quỹ trước
2. Preferred return trên toàn bộ vốn đầu tư
3. Catch-up (nếu có)
4. Lợi nhuận còn lại chia theo thỏa thuận carry

- GP nhận carry muộn hơn
- Có lợi hơn cho LP
- Tiêu chuẩn trong hầu hết các quỹ PE

## Trang Liên Quan

- [[alternative-investments/concepts/alternative-investment-overview|Alternative Investment Overview]]
- [[alternative-investments/concepts/private-capital|Private Capital]]
- [[alternative-investments/formulas/ai-formulas|AI Formulas]]
- [[alternative-investments/glossary/ai-m02|Glossary: Performance Measurement Terms]]