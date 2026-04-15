---
title: "M07 — Long-Term Assets"
type: module
subject: fsa
module: M07
los: [2.b, Pre.i, Pre.ii, Pre.iii, Pre.iv, 7.a, 7.b, 7.c]
created: 2026-04-10
updated: 2026-04-10
tags: [cfa-level-1, fsa, long-term-assets, ppe, intangibles, depreciation, impairment, goodwill, revaluation]
---

# M07: Long-Term Assets

## Overview

Long-term assets bao gồm tài sản hữu hình (PPE), tài sản vô hình, và bất động sản đầu tư. Các quyết định then chốt xoay quanh **capitalize vs expense**, các mô hình đo lường, phương pháp depreciation/amortization, và kiểm tra impairment.

---

## 1. Capitalize vs Expense

### Quy Tắc Quyết Định

**Capitalize** nếu khoản chi mang lại **lợi ích kinh tế trong tương lai qua nhiều kỳ**.

**Expense** nếu lợi ích được tiêu thụ **chỉ trong kỳ hiện tại**.

### Ảnh Hưởng lên Báo Cáo Tài Chính

| Tác động | Capitalize | Expense |
|---|---|---|
| Assets (Kỳ 1) | **Cao hơn** | Thấp hơn |
| Net Income (Kỳ 1) | **Cao hơn** (chỉ tính depreciation) | Thấp hơn (toàn bộ chi phí ghi nhận ngay) |
| Net Income (Các kỳ sau) | **Thấp hơn** (depreciation tiếp diễn) | Cao hơn (không có chi phí tương lai) |
| Tổng NI suốt đời tài sản | **Như nhau** | Như nhau |
| CFO | **Cao hơn** (chi phí nằm ở CFI) | Thấp hơn (chi phí nằm ở CFO) |
| CFI | **Thấp hơn** (dòng ra CAPEX) | Cao hơn (không ảnh hưởng CFI) |
| Tổng CF | **Như nhau** | Như nhau |

---

## 2. Capitalizing Interest During Construction

Khi doanh nghiệp tự xây dựng tài sản để sử dụng:
- **Cả IFRS và US GAAP** đều yêu cầu capitalize borrowing costs trong quá trình xây dựng
- IFRS: capitalize borrowing costs trực tiếp phát sinh; bù trừ bất kỳ khoản thu nhập đầu tư nào từ vốn vay
- US GAAP: capitalize **avoidable interest** (lãi sẽ không phát sinh nếu không có xây dựng)

$$\text{Capitalized Interest} = \text{Average Expenditure} \times \text{Interest Rate}$$

---

## 3. Tangible Assets: Property, Plant & Equipment (PPE)

### Ghi Nhận Ban Đầu

$$\text{Cost} = \text{Purchase price} + \text{Directly attributable costs to bring asset to intended use}$$

### Đo Lường Sau Ghi Nhận

| Mô hình | IFRS | US GAAP |
|---|---|---|
| **Cost Model** | Cost $-$ Accumulated Depreciation $-$ Impairment | Cost $-$ Accumulated Depreciation $-$ Impairment |
| **Revaluation Model** | Fair value $-$ Subsequent depreciation $-$ Impairment | **Không được phép** |

#### Revaluation Model (chỉ áp dụng theo IFRS)

- Tăng giá trị khi revaluation: ghi vào **OCI** (revaluation surplus trong equity)
- Giảm giá trị khi revaluation: ghi nhận vào **profit or loss** (trừ khi đảo ngược khoản tăng trước đó)
- Phải revalue **toàn bộ nhóm (class)** tài sản một cách thường xuyên

---

## 4. Intangible Assets

### Intangibles Mua Ngoài

- **Capitalize** theo giá mua (cả IFRS và US GAAP)
- Ví dụ: patents, trademarks, licenses, franchises

### Internally Developed Intangibles

| Giai đoạn | IFRS | US GAAP |
|---|---|---|
| **Research** | Expense khi phát sinh | Expense khi phát sinh |
| **Development** | **Capitalize** nếu đáp ứng đủ 6 tiêu chí (tính khả thi kỹ thuật, ý định, năng lực, lợi ích tương lai có khả năng xảy ra, nguồn lực, đo lường tin cậy) | **Expense** toàn bộ chi phí R&D |
| **Software development** | Capitalize sau khi đạt technological feasibility | Capitalize sau khi đạt technological feasibility |

### Intangibles từ Business Combinations

| Loại | Cách xử lý |
|---|---|
| **Identifiable intangibles** | Ghi nhận riêng biệt theo **fair value** |
| **Unidentifiable intangibles** | Ghi nhận là **goodwill** ($= \text{Purchase Price} - \text{FV of Net Identifiable Assets}$) |

---

## 5. Depreciation Methods

### Straight-Line

$$\text{Annual Depreciation} = \frac{\text{Cost} - \text{Residual Value}}{\text{Useful Life}}$$

### Declining Balance (ví dụ: Double Declining Balance)

$$\text{Depreciation}_t = \text{Book Value}_{t-1} \times \frac{2}{\text{Useful Life}}$$

- Bỏ qua residual value trong tính toán (nhưng không depreciate xuống dưới residual value)
- **Phương pháp accelerated:** chi phí cao hơn trong các năm đầu

### Units of Production

$$\text{Depreciation}_t = \frac{\text{Cost} - \text{Residual Value}}{\text{Total Estimated Units}} \times \text{Units Produced}_t$$

> Thay đổi ước tính về useful life hoặc residual value là **change in accounting estimate** -- áp dụng prospectively (không restatement).

---

## 6. Amortization of Intangible Assets

| Loại | Cách xử lý |
|---|---|
| **Finite-life intangibles** | Amortize theo useful life (các phương pháp tương tự depreciation) |
| **Indefinite-life intangibles** | Không amortize; yêu cầu **kiểm tra impairment hàng năm** |
| **Goodwill** | Không amortize; yêu cầu **kiểm tra impairment hàng năm** |

---

## 7. Impairment of Long-Term Assets

### IFRS Impairment

**Dấu hiệu kích hoạt:** tồn tại các chỉ báo impairment (đánh giá tại mỗi ngày báo cáo)

$$\text{Recoverable Amount} = \max(\text{FV} - \text{Costs of Disposal},\ \text{Value in Use})$$

- Nếu $\text{Carrying Value} > \text{Recoverable Amount}$ → ghi giảm xuống recoverable amount
- **Cho phép hoàn nhập** với mọi tài sản **ngoại trừ goodwill**

### US GAAP Impairment (Hai Bước cho Long-Lived Assets)

**Bước 1 -- Recoverability test:**
- Nếu $\text{Carrying Value} > \text{Undiscounted Future Cash Flows}$ → tài sản bị impaired

**Bước 2 -- Đo lường:**
- Ghi giảm xuống **fair value**
- Impairment loss $= \text{Carrying Value} - \text{Fair Value}$
- **Không cho phép hoàn nhập**

### Goodwill Impairment

| Chuẩn mực | Cách tiếp cận |
|---|---|
| IFRS | So sánh carrying amount của CGU (bao gồm goodwill) với recoverable amount |
| US GAAP | So sánh FV của reporting unit với carrying amount (bao gồm goodwill); ghi giảm goodwill theo phần vượt trội |

---

## 8. Investment Property

Investment property là bất động sản nắm giữ để kiếm **thu nhập cho thuê** hoặc vì mục đích **tăng giá vốn** (không phải để sử dụng trong hoạt động kinh doanh hoặc bán trong chu kỳ kinh doanh thông thường).

| Mô hình | IFRS | US GAAP |
|---|---|---|
| **Cost Model** | Được phép | **Bắt buộc** (lựa chọn duy nhất) |
| **Fair Value Model** | Được phép (lãi/lỗ ghi vào P&L) | Không được phép |

---

## Key Formulas

| Công thức | Biểu thức |
|---|---|
| Straight-line depreciation | $\frac{\text{Cost} - \text{RV}}{\text{Useful Life}}$ |
| DDB depreciation | $\text{BV}_{t-1} \times \frac{2}{\text{UL}}$ |
| Recoverable amount (IFRS) | $\max(\text{FV} - \text{Costs},\ \text{VIU})$ |
| Goodwill | $\text{Purchase Price} - \text{FV Net Identifiable Assets}$ |

---

## Related Notes

- [[financial-statement-analysis/modules/m06-inventories/index|M06: Inventories]]
- [[financial-statement-analysis/modules/m08-liabilities-and-equity/index|M08: Liabilities and Equity]]
- [[financial-statement-analysis/modules/m05-cash-flows-ii/index|M05: Cash Flow Statement (Part II)]]