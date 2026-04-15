---
title: Inventory Valuation
type: concept
subject: fsa
created: 2026-04-10
updated: 2026-04-10
tags: [fsa, inventory, fifo, lifo, weighted-average, cogs, nrv]
---

# Inventory Valuation

## Phương Trình Dòng Chảy Chi Phí Hàng Tồn Kho

$$\text{COGS} = \text{Beginning Inventory} + \text{Purchases} - \text{Ending Inventory}$$

$$\text{Ending Inventory} = \text{Beginning Inventory} + \text{Purchases} - \text{COGS}$$

## Giả Định Dòng Chảy Chi Phí

### FIFO (First-In, First-Out)

- Chi phí hàng tồn kho cũ nhất được ghi nhận vào COGS trước
- Ending inventory phản ánh chi phí mua **gần nhất**
- Được chấp nhận theo cả **IFRS và US GAAP**

### LIFO (Last-In, First-Out)

- Chi phí hàng tồn kho mới nhất được ghi nhận vào COGS trước
- Ending inventory phản ánh chi phí **cũ nhất**
- Chỉ được chấp nhận theo **US GAAP** (bị cấm theo IFRS)

### Weighted Average Cost (WAC)

$$\text{WAC per unit} = \frac{\text{Cost of Goods Available for Sale}}{\text{Total Units Available for Sale}}$$

- COGS và ending inventory được tính dựa trên chi phí bình quân gia quyền
- Được chấp nhận theo cả **IFRS và US GAAP**

### Specific Identification

- Chi phí thực tế của từng đơn vị hàng được theo dõi và ghi nhận riêng lẻ
- Áp dụng cho các mặt hàng độc nhất, giá trị cao (trang sức, nghệ thuật, bất động sản)
- Được chấp nhận theo cả **IFRS và US GAAP**

## So Sánh FIFO và LIFO: Tác Động Khi Giá Tăng (Lạm Phát)

| Chỉ số | FIFO | LIFO |
|---|---|---|
| COGS | Thấp hơn (chi phí cũ, rẻ hơn) | Cao hơn (chi phí mới, đắt hơn) |
| Ending Inventory | Cao hơn (chi phí gần đây) | Thấp hơn (chi phí cũ) |
| Gross Profit | Cao hơn | Thấp hơn |
| Net Income | Cao hơn | Thấp hơn |
| Income Taxes | Cao hơn | Thấp hơn |
| Cash Flow (sau thuế) | Thấp hơn | Cao hơn (tiết kiệm thuế) |

> Trong giai đoạn **giảm phát** (deflation — giá giảm), tất cả các tác động trên đều đảo ngược.

## LIFO Reserve

$$\text{LIFO Reserve} = \text{Inventory}_{FIFO} - \text{Inventory}_{LIFO}$$

Dùng để chuyển đổi từ LIFO sang FIFO để so sánh:

$$\text{Inventory}_{FIFO} = \text{Inventory}_{LIFO} + \text{LIFO Reserve}$$

$$\text{COGS}_{FIFO} = \text{COGS}_{LIFO} - \Delta \text{LIFO Reserve}$$

### Điều Chỉnh Báo Cáo Tài Chính (Từ LIFO Sang FIFO)

| Khoản mục | Điều chỉnh |
|---|---|
| Inventory (BS) | Cộng LIFO Reserve |
| COGS (IS) | Trừ phần thay đổi của LIFO Reserve |
| Retained Earnings | Cộng LIFO Reserve $\times (1 - t)$ |
| Deferred Tax Liability | Cộng LIFO Reserve $\times t$ |
| Cash | Không thay đổi (thuế đã được thanh toán) |

## LIFO Liquidation

Xảy ra khi một doanh nghiệp áp dụng LIFO **bán ra nhiều đơn vị hơn số lượng mua vào**, khiến các lớp hàng tồn kho cũ với chi phí thấp bị đưa vào tiêu thụ.

**Tác động:**
- COGS **giảm giả tạo** (chi phí cũ được đưa vào báo cáo kết quả kinh doanh)
- Gross profit và net income được báo cáo **cao hơn** thực tế
- Thanh toán thuế **cao hơn**
- Kết quả **không bền vững** — đây là hiện tượng tăng thu nhập chỉ xảy ra một lần

## Định Giá Hàng Tồn Kho Trên Bảng Cân Đối Kế Toán

### IFRS: Lower of Cost or Net Realizable Value (NRV)

$$\text{NRV} = \text{Estimated Selling Price} - \text{Costs to Complete and Sell}$$

- Ghi giảm xuống NRV nếu giá gốc > NRV
- **Được phép hoàn nhập** (tối đa bằng giá gốc ban đầu) nếu NRV phục hồi

### US GAAP: Lower of Cost or Market

- **Market** = Chi phí thay thế (replacement cost), nhưng bị giới hạn bởi:
  - Trần (Ceiling) = NRV
  - Sàn (Floor) = NRV - Biên lợi nhuận thông thường (normal profit margin)
- Ghi giảm nếu giá gốc > market
- **Không được phép hoàn nhập** (ngoại trừ phương pháp LIFO/bán lẻ; FIFO/WAC sử dụng NRV theo ASU 2015-11)

## Các Chỉ Số Hàng Tồn Kho

$$\text{Inventory Turnover} = \frac{\text{COGS}}{\text{Average Inventory}}$$

$$\text{Days of Inventory on Hand (DOH)} = \frac{365}{\text{Inventory Turnover}}$$

## Tác Động Đến Phân Tích Tài Chính

| Điểm phân tích | Lưu ý |
|---|---|
| So sánh giữa các công ty | Chuyển đổi các công ty dùng LIFO sang FIFO bằng LIFO reserve |
| Phân tích xu hướng | Chú ý các thay đổi trong phương pháp tính hàng tồn kho |
| LIFO liquidation | Điều chỉnh thu nhập để loại bỏ các khoản lợi nhuận không bền vững |
| Ghi giảm hàng tồn kho | Có thể là dấu hiệu hàng lỗi thời hoặc nhu cầu giảm sút |
| Hàng tồn kho tăng so với doanh thu | Cảnh báo tiềm ẩn về nhu cầu suy yếu |

## Xem Thêm

- [[financial-statement-analysis/concepts/expense-recognition|Expense Recognition]]
- [[financial-statement-analysis/concepts/ifrs-vs-gaap|IFRS vs GAAP Differences]]
- [[financial-statement-analysis/concepts/financial-ratios|Financial Ratios]]
- [[financial-statement-analysis/formulas/fsa-formulas|FSA Master Formula Sheet]]