---
title: Long-Term Assets
type: concept
subject: fsa
created: 2026-04-10
updated: 2026-04-10
tags: [fsa, ppe, intangibles, goodwill, depreciation, impairment, revaluation]
---

# Long-Term Assets

## Property, Plant, and Equipment (PPE)

### Initial Recognition

PPE được ghi nhận theo **giá gốc (historical cost)**, bao gồm:
- Giá mua
- Chi phí vận chuyển và lắp đặt
- Thuế nhập khẩu
- Chi phí chuẩn bị mặt bằng
- Chi phí kiểm thử
- Phí chuyên môn
- Chi phí đi vay trong thời gian xây dựng (được vốn hóa)

### Subsequent Measurement

| Mô hình | IFRS | US GAAP |
|---|---|---|
| **Cost model** | Được phép | Bắt buộc |
| **Revaluation model** | Được phép | Không được phép |

**Cost model**: Ghi nhận theo giá gốc trừ khấu hao lũy kế và tổn thất giá trị (impairment losses)

**Revaluation model** (chỉ theo IFRS):
- Ghi nhận theo fair value trừ khấu hao/impairment tiếp theo
- Tăng giá trị do revaluation → OCI (vốn chủ sở hữu dưới dạng revaluation surplus)
- Giảm giá trị do revaluation → báo cáo kết quả kinh doanh (trừ khi hoàn nhập revaluation surplus trước đó)

### Depreciation Methods

**Straight-Line:**
$$\text{Depreciation} = \frac{\text{Cost} - \text{Salvage Value}}{\text{Useful Life}}$$

**Double-Declining Balance (DDB):**
$$\text{Depreciation} = \frac{2}{n} \times \text{Beginning Book Value}$$

**Units-of-Production:**
$$\text{Depreciation} = \frac{\text{Cost} - \text{Salvage}}{\text{Total Units}} \times \text{Units in Period}$$

### Component Depreciation

Theo IFRS, mỗi bộ phận trọng yếu của tài sản có thời gian sử dụng hữu ích khác nhau phải được khấu hao **riêng biệt**. US GAAP cho phép nhưng không bắt buộc áp dụng component depreciation.

## Intangible Assets

### Identifiable Intangibles

| Loại | Ví dụ | Xử lý kế toán |
|---|---|---|
| **Finite life** | Patents, copyrights, licenses, danh sách khách hàng | Phân bổ theo thời gian sử dụng hữu ích |
| **Indefinite life** | Một số trademarks, giấy phép phát sóng | Không phân bổ; kiểm tra impairment hàng năm |

### Internally Generated Intangibles

| Giai đoạn | IFRS | US GAAP |
|---|---|---|
| **Research** | Chi phí ngay khi phát sinh | Chi phí ngay khi phát sinh |
| **Development** | Vốn hóa nếu đáp ứng 6 tiêu chí | Chi phí (ngoại trừ chi phí phát triển phần mềm theo ASC 985/ASC 350-40) |

**Tiêu chí vốn hóa chi phí development theo IFRS:**
1. Có tính khả thi về mặt kỹ thuật
2. Có ý định hoàn thành
3. Có khả năng sử dụng hoặc bán
4. Có khả năng tạo ra lợi ích kinh tế trong tương lai
5. Có đủ nguồn lực để thực hiện
6. Chi phí có thể đo lường đáng tin cậy

## Goodwill

$$\text{Goodwill} = \text{Purchase Price} - \text{Fair Value of Net Identifiable Assets}$$

trong đó Fair Value of Net Identifiable Assets = Fair Value của Tài sản - Fair Value của Nợ phải trả

- Chỉ phát sinh từ **business combinations** (thâu tóm/mua lại)
- **Không phân bổ** theo cả IFRS và US GAAP
- Kiểm tra **impairment** ít nhất mỗi năm một lần

### Impairment of Goodwill

| | IFRS | US GAAP |
|---|---|---|
| **Cấp độ** | Cash-generating unit (CGU) | Reporting unit |
| **Kiểm tra** | So sánh giá trị ghi sổ của CGU (bao gồm goodwill) với recoverable amount | So sánh giá trị ghi sổ của reporting unit với fair value |
| **Recoverable amount** | Giá trị cao hơn giữa fair value trừ chi phí bán và value in use | Fair value của reporting unit |
| **Hoàn nhập** | Không được phép | Không được phép |

## Impairment of Long-Lived Assets

### IFRS (IAS 36)

**Dấu hiệu kích hoạt**: Có các dấu hiệu impairment (bên ngoài hoặc nội bộ)

$$\text{Impairment Loss} = \text{Carrying Amount} - \text{Recoverable Amount}$$

$$\text{Recoverable Amount} = \max(\text{Fair Value} - \text{Costs to Sell}, \text{Value in Use})$$

- **Cho phép hoàn nhập** đối với các tài sản không phải goodwill (tối đa bằng giá trị ghi sổ ban đầu trừ khấu hao)

### US GAAP (ASC 360)

**Kiểm tra hai bước:**

1. **Recoverability test**: Giá trị ghi sổ > dòng tiền tương lai chưa chiết khấu? Nếu có → bị impaired
2. **Đo lường**: Impairment loss = Giá trị ghi sổ - Fair value

- **Không được hoàn nhập** đối với tài sản đang sử dụng

### Assets Held for Sale

- Đo lường theo giá trị thấp hơn giữa giá trị ghi sổ và fair value trừ chi phí bán
- **Không khấu hao** trong thời gian phân loại là held for sale
- Áp dụng cho cả IFRS và US GAAP

## Derecognition

Khi thanh lý tài sản:

$$\text{Gain (Loss)} = \text{Proceeds} - \text{Carrying Amount}$$

Được ghi nhận trên báo cáo kết quả kinh doanh (thường trong phần hoạt động ngoài kinh doanh).

## Useful Ratios

$$\text{Average Age} = \frac{\text{Accumulated Depreciation}}{\text{Annual Depreciation Expense}}$$

$$\text{Average Useful Life} = \frac{\text{Historical Cost}}{\text{Annual Depreciation Expense}}$$

$$\text{Remaining Useful Life} = \frac{\text{Net PP\&E}}{\text{Annual Depreciation Expense}}$$

## See Also

- [[financial-statement-analysis/concepts/expense-recognition|Expense Recognition]]
- [[financial-statement-analysis/concepts/ifrs-vs-gaap|IFRS vs GAAP Differences]]
- [[financial-statement-analysis/concepts/income-taxes-accounting|Income Taxes Accounting]]
- [[financial-statement-analysis/formulas/fsa-formulas|FSA Master Formula Sheet]]