---
title: Income Taxes Accounting
type: concept
subject: fsa
created: 2026-04-10
updated: 2026-04-10
tags: [fsa, income-taxes, dta, dtl, deferred-tax, temporary-differences, permanent-differences]
---

# Income Taxes Accounting

## Thuật Ngữ Chính

| Thuật ngữ | Định nghĩa |
|---|---|
| **Tax expense** (provision) | Thuế thu nhập được ghi nhận trên báo cáo kết quả kinh doanh |
| **Tax payable** | Số thuế thực tế phải nộp cho cơ quan thuế |
| **Taxable income** | Thu nhập được tính theo quy định thuế |
| **Pretax income** | Thu nhập theo báo cáo tài chính (thu nhập kế toán) |
| **Tax base** | Giá trị của tài sản/nợ phải trả theo mục đích thuế |
| **Carrying amount** | Giá trị trên bảng cân đối kế toán (giá trị sổ sách) |

## Mối Quan Hệ Cơ Bản

$$\text{Tax Expense} = \text{Taxes Payable} + \Delta \text{DTL} - \Delta \text{DTA}$$

$$\text{Tax Expense} = \text{Taxes Payable} + \text{Deferred Tax Expense}$$

## Temporary vs. Permanent Differences

### Temporary Differences

Sự chênh lệch giữa carrying amount và tax base mà **sẽ được hoàn nhập** trong các kỳ tương lai, tạo ra deferred taxes.

**Deferred Tax Liability (DTL):**

$$\text{DTL} = (\text{Carrying Amount} - \text{Tax Base}) \times t$$

Được tạo ra khi:
- Taxable income < pretax income **hiện tại** (sẽ cao hơn sau này)
- Doanh thu được ghi nhận theo sổ sách trước khi chịu thuế (ví dụ: installment sales)
- Chi phí được khấu trừ thuế trước khi ghi nhận vào sổ sách (ví dụ: accelerated depreciation)

**Deferred Tax Asset (DTA):**

$$\text{DTA} = (\text{Tax Base} - \text{Carrying Amount}) \times t$$

Được tạo ra khi:
- Taxable income > pretax income **hiện tại** (sẽ thấp hơn sau này)
- Doanh thu được ghi nhận cho mục đích thuế trước khi vào sổ sách (ví dụ: unearned revenue được đánh thuế khi nhận)
- Chi phí được ghi nhận vào sổ sách trước khi được khấu trừ thuế (ví dụ: warranty provisions, restructuring charges)
- Tax loss carryforwards

### Permanent Differences

Sự chênh lệch **không bao giờ hoàn nhập** — ảnh hưởng đến effective tax rate nhưng **không** tạo ra deferred taxes.

**Ví dụ:**
- Thu nhập lãi được miễn thuế (trái phiếu đô thị)
- Chi phí không được khấu trừ thuế (phạt, tiền phạt, một số chi phí giải trí)
- Tax credits
- Phí bảo hiểm nhân thọ cho nhân viên chủ chốt

## Effective vs. Statutory Tax Rate

$$\text{Effective Tax Rate} = \frac{\text{Income Tax Expense}}{\text{Pretax Income}}$$

$$\text{Statutory Tax Rate}$$ = mức thuế suất được ban hành theo luật thuế

**Effective rate khác statutory rate do:**
- Permanent differences
- Thay đổi thuế suất
- Các khu vực tài phán khác nhau với thuế suất khác nhau
- Tax credits
- Thay đổi trong valuation allowance

## Valuation Allowance (US GAAP) / Recognition Criteria (IFRS)

DTA chỉ được ghi nhận ở mức độ mà việc có taxable income trong tương lai là **probable** (IFRS) hoặc **more likely than not** (US GAAP).

- **US GAAP**: Ghi nhận toàn bộ DTA, sau đó bù trừ bằng một **valuation allowance** nếu khả năng thu hồi không đạt mức more likely than not
- **IFRS**: Chỉ ghi nhận DTA ở mức độ probable — không có tài khoản valuation allowance riêng biệt

Valuation allowance tăng lên → tax expense cao hơn → net income thấp hơn

## Thay Đổi Thuế Suất

Khi thuế suất được ban hành thay đổi:
- Các DTA và DTL hiện có được **đo lại** theo thuế suất mới
- Khoản điều chỉnh được ghi nhận qua **income tax expense** (báo cáo kết quả kinh doanh)

$$\text{Adjustment} = \text{Deferred Tax Balance} \times (\text{New Rate} - \text{Old Rate})$$

## Phân Loại Trên Bảng Cân Đối Kế Toán

| Chuẩn mực | Current/Non-Current |
|---|---|
| **IFRS** | Tất cả deferred taxes đều là **non-current** |
| **US GAAP** | Tất cả deferred taxes đều là **non-current** (sau ASU 2015-17) |

## Các Nguồn Phổ Biến Tạo DTL và DTA

| Nguồn | Tạo ra |
|---|---|
| Accelerated depreciation (thuế) so với straight-line (sổ sách) | DTL |
| Installment sale (ghi nhận thuế bị trì hoãn) | DTL |
| Lãi từ revaluation tài sản (IFRS) | DTL |
| Warranty provisions (chi phí sổ sách trước khi khấu trừ thuế) | DTA |
| Bad debt allowance (sổ sách trước khi tính thuế) | DTA |
| Pension liability (sổ sách trước khi tính thuế) | DTA |
| Tax loss carryforwards | DTA |
| Unearned revenue (đánh thuế khi nhận) | DTA |

## Lưu Ý Phân Tích

- **DTL có khả năng hoàn nhập**: Xem như nợ phải trả thực sự (ví dụ: sự kiện một lần)
- **DTL khó hoàn nhập** (liên tục tăng trưởng): Một số nhà phân tích xem như vốn chủ sở hữu (ví dụ: accelerated depreciation liên tục trong công ty đang tăng trưởng)
- **DTA với valuation allowance lớn**: Chất lượng tài sản đáng ngờ
- Cần chú ý đến sự tùy ý của ban lãnh đạo trong việc ước tính valuation allowances — có thể được dùng để điều chỉnh lợi nhuận

## Xem Thêm

- [[financial-statement-analysis/concepts/expense-recognition|Expense Recognition]]
- [[financial-statement-analysis/concepts/financial-ratios|Financial Ratios]]
- [[financial-statement-analysis/concepts/ifrs-vs-gaap|IFRS vs GAAP Differences]]
- [[financial-statement-analysis/concepts/reporting-quality|Reporting Quality]]
- [[financial-statement-analysis/formulas/fsa-formulas|FSA Master Formula Sheet]]