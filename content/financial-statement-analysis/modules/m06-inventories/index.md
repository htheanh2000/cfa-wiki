---
title: "M06 — Financial Ratios"
type: module
subject: fsa
module: M06
los: [Pre.i, Pre.ii, Pre.iii, Pre.iv, 6.a, 6.b, 6.c]
created: 2026-04-10
updated: 2026-04-10
tags: [cfa-level-1, fsa, inventories, fifo, lifo, weighted-average, nrv, lifo-reserve]
---

# M06: Inventories

## Tổng quan

Hàng tồn kho là tài sản ngắn hạn đại diện cho hàng hóa được giữ để bán. Việc lựa chọn phương pháp định giá hàng tồn kho ảnh hưởng đáng kể đến **COGS, lợi nhuận gộp, lợi nhuận ròng, tài sản và nghĩa vụ thuế** được báo cáo.

---

## 1. Phân loại Hàng tồn kho

| Loại | Mô tả |
|---|---|
| Nguyên vật liệu thô (Raw materials) | Đầu vào chưa đưa vào sản xuất |
| Sản phẩm dở dang (Work-in-process / WIP) | Hàng hóa đã hoàn thành một phần |
| Thành phẩm (Finished goods) | Hàng hóa đã hoàn thành, sẵn sàng để bán |

---

## 2. Chi phí được vốn hóa vs. Ghi nhận ngay vào chi phí

**Vốn hóa** (tính vào giá trị hàng tồn kho):
- Giá mua, thuế nhập khẩu, chi phí vận chuyển đầu vào (freight-in), chi phí bốc xếp
- Chi phí chuyển đổi: lao động trực tiếp + chi phí sản xuất chung

**Ghi nhận ngay vào chi phí** khi phát sinh:
- Hao phí bất thường, chi phí lưu kho (trừ khi là một phần của sản xuất), chi phí quản lý hành chính, chi phí bán hàng

---

## 3. Phương trình Dòng chảy Chi phí Hàng tồn kho

$$\boxed{\text{COGS} = \text{Beginning Inventory} + \text{Purchases} - \text{Ending Inventory}}$$

Phương pháp được sử dụng để **phân bổ chi phí** cho hàng tồn kho cuối kỳ và COGS quyết định tác động tài chính.

---

## 4. Các phương pháp Định giá Hàng tồn kho

### FIFO (First-In, First-Out)

- Chi phí cũ nhất được phân bổ vào COGS; chi phí mới nhất còn lại trong hàng tồn kho cuối kỳ
- Hàng tồn kho cuối kỳ xấp xỉ **giá thay thế hiện tại**
- Được phép theo cả IFRS và US GAAP

### LIFO (Last-In, First-Out)

- Chi phí mới nhất được phân bổ vào COGS; chi phí cũ nhất còn lại trong hàng tồn kho cuối kỳ
- COGS xấp xỉ **chi phí hiện tại**
- Chỉ được phép theo **US GAAP** (bị cấm theo IFRS)

### Weighted Average Cost (Giá trung bình gia quyền)

$$\text{WAC per unit} = \frac{\text{Cost of Goods Available for Sale}}{\text{Total Units Available}}$$

- Làm trơn biến động giá
- Được phép theo cả IFRS và US GAAP

### Specific Identification (Nhận dạng cụ thể)

- Chi phí thực tế của từng đơn vị được theo dõi riêng lẻ
- Dùng cho các mặt hàng độc nhất, giá trị cao (ví dụ: trang sức, bất động sản, thiết bị đặt hàng riêng)

---

## 5. FIFO vs LIFO: Tác động khi Giá tăng

| Chỉ tiêu Báo cáo Tài chính | FIFO | LIFO |
|---|---|---|
| Hàng tồn kho cuối kỳ (Ending Inventory) | **Cao hơn** (chi phí mới hơn, cao hơn) | Thấp hơn (chi phí cũ hơn, thấp hơn) |
| COGS | **Thấp hơn** (chi phí cũ hơn, thấp hơn) | Cao hơn (chi phí mới hơn, cao hơn) |
| Lợi nhuận gộp (Gross Profit) | **Cao hơn** | Thấp hơn |
| Lợi nhuận ròng (Net Income) | **Cao hơn** | Thấp hơn |
| Thuế | **Cao hơn** | Thấp hơn |
| Dòng tiền (từ thuế thấp hơn) | Thấp hơn | **Cao hơn** |

> Khi **giá giảm**, các tác động sẽ đảo ngược.

---

## 6. LIFO Reserve và LIFO Liquidation

### LIFO Reserve

$$\text{LIFO Reserve} = \text{Inventory}_{\text{FIFO}} - \text{Inventory}_{\text{LIFO}}$$

Dùng để chuyển đổi báo cáo tài chính theo LIFO sang tương đương FIFO:

$$\text{Inventory}_{\text{FIFO}} = \text{Inventory}_{\text{LIFO}} + \text{LIFO Reserve}$$

$$\text{COGS}_{\text{FIFO}} = \text{COGS}_{\text{LIFO}} - \Delta \text{LIFO Reserve}$$

### LIFO Liquidation

Xảy ra khi doanh nghiệp dùng LIFO **bán ra nhiều đơn vị hơn số mua vào**, phải dùng đến các lớp hàng tồn kho cũ với chi phí thấp:
- Làm **giảm COGS** và **thổi phồng lợi nhuận** một cách nhân tạo
- Dẫn đến **nghĩa vụ thuế cao hơn**
- Không bền vững và là dấu hiệu của các vấn đề vận hành tiềm ẩn

---

## 7. Ghi giảm Hàng tồn kho (Inventory Write-Downs)

### IFRS: Lower of Cost and Net Realizable Value (NRV)

$$\text{Carrying Value} = \min(\text{Cost}, \text{NRV})$$

Trong đó $\text{NRV} = \text{Giá bán ước tính} - \text{Chi phí ước tính để hoàn thành và bán}$

- Ghi giảm được ghi nhận là chi phí
- **Được phép hoàn nhập** (tối đa đến giá gốc ban đầu) nếu NRV tăng trở lại sau đó

### US GAAP: Lower of Cost or Market

$$\text{Market} = \text{Replacement Cost}$$

Chịu ràng buộc bởi:
- **Mức trần (Ceiling):** NRV (giá thị trường không được vượt quá NRV)
- **Mức sàn (Floor):** NRV $-$ Biên lợi nhuận thông thường (giá thị trường không được thấp hơn mức sàn)

- Ghi giảm được ghi nhận là chi phí
- **Không được phép hoàn nhập** sau khi đã ghi giảm

---

## Các Công thức Quan trọng

| Công thức | Biểu thức |
|---|---|
| COGS | $\text{BI} + \text{Purchases} - \text{EI}$ |
| LIFO Reserve | $\text{Inv}_{\text{FIFO}} - \text{Inv}_{\text{LIFO}}$ |
| FIFO COGS from LIFO | $\text{COGS}_{\text{LIFO}} - \Delta \text{LIFO Reserve}$ |
| Weighted Average Cost | $\frac{\text{COGAFS}}{\text{Units Available}}$ |
| NRV | $\text{Selling Price} - \text{Costs to Complete \& Sell}$ |

---

## Ghi chú Liên quan

- [[financial-statement-analysis/modules/m04-cash-flows-i/index|M04: Cash Flow Statement (Part I)]]
- [[financial-statement-analysis/modules/m07-long-term-assets/index|M07: Long-Term Assets]]
- [[financial-statement-analysis/modules/m08-liabilities-and-equity/index|M08: Liabilities and Equity]]