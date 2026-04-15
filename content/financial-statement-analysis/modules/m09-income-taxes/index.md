---
title: "M09 — Income Taxes"
type: module
subject: fsa
module: M09
los: [Pre.i, Pre.ii, Pre.iii, Pre.iv, 9.a, 9.b, 9.c, 9.d]
created: 2026-04-10
updated: 2026-04-10
tags: [cfa-level-1, fsa, income-taxes, deferred-tax, dta, dtl, temporary-differences, permanent-differences]
---

# M09: Income Taxes

## Tổng quan

Kế toán thuế thu nhập là cầu nối giữa **lợi nhuận kế toán** (báo cáo trên báo cáo thu nhập theo GAAP/IFRS) và **thu nhập chịu thuế** (khai báo trên tờ khai thuế). Các quy tắc ghi nhận doanh thu và chi phí khác nhau tạo ra những chênh lệch có thể là tạm thời hoặc vĩnh viễn.

---

## 1. Accounting Profit vs Taxable Income

| Khái niệm | Định nghĩa |
|---|---|
| Accounting profit (pre-tax income) | Lợi nhuận theo báo cáo thu nhập, tuân theo GAAP/IFRS |
| Taxable income | Thu nhập được tính theo luật thuế, dùng để xác định số thuế phải nộp |

> Hai con số này khác nhau vì cơ quan thuế và chuẩn mực kế toán có **các quy tắc khác nhau** về thời điểm ghi nhận doanh thu và thời điểm được khấu trừ chi phí.

---

## 2. Tax Expense, Tax Payable, và Deferred Tax

**Tax expense** (trên báo cáo thu nhập) bao gồm hai phần:

$$\text{Tax Expense} = \text{Tax Payable} + \text{Deferred Tax Expense}$$

trong đó:
- $\text{Tax Payable} = \text{Taxable Income} \times \text{Tax Rate}$ (số thuế thực tế phải nộp cho cơ quan thuế)
- $\text{Deferred Tax Expense} = \Delta DTL - \Delta DTA$ (thay đổi trong số dư deferred tax)

---

## 3. Temporary Differences

Temporary differences là chênh lệch giữa lợi nhuận kế toán và thu nhập chịu thuế mà **được kỳ vọng sẽ đảo ngược** trong các kỳ tương lai. Chúng tạo ra deferred tax assets (DTA) hoặc deferred tax liabilities (DTL).

### Deferred Tax Liability (DTL)

Phát sinh khi **taxable income < accounting profit** trong kỳ hiện tại, nghĩa là công ty sẽ phải nộp **nhiều** thuế hơn trong các kỳ tương lai.

**Ví dụ phổ biến:** Khấu hao nhanh cho mục đích thuế so với khấu hao đường thẳng cho mục đích kế toán.

$$DTL = (\text{Carrying Amount} - \text{Tax Base}) \times \text{Tax Rate}$$

trong đó công thức này áp dụng cho tài sản có $\text{CA} > \text{TB}$.

### Deferred Tax Asset (DTA)

Phát sinh khi **taxable income > accounting profit** trong kỳ hiện tại, nghĩa là công ty sẽ phải nộp **ít** thuế hơn trong các kỳ tương lai.

**Ví dụ phổ biến:** Dự phòng bảo hành, nghĩa vụ hưu trí, tax loss carryforwards.

$$DTA = (\text{Tax Base} - \text{Carrying Amount}) \times \text{Tax Rate}$$

---

## 4. Permanent Differences

Permanent differences là chênh lệch giữa lợi nhuận kế toán và thu nhập chịu thuế mà **KHÔNG đảo ngược** trong các kỳ tương lai.

- **Không** tạo ra DTA hay DTL
- **Ảnh hưởng đến effective tax rate** (khiến nó khác với statutory rate)

**Ví dụ:**
- Thu nhập lãi suất miễn thuế (ví dụ: trái phiếu đô thị)
- Tiền phạt và hình phạt không được khấu trừ thuế
- Chi phí tiếp khách không được khấu trừ thuế

---

## 5. Balance Sheet Approach vs P&L Approach

### Balance Sheet Approach

Tính số dư deferred tax trực tiếp từ chênh lệch giữa carrying amount và tax base của tài sản/nợ phải trả:

$$DTL = (\text{Carrying Amount}_{\text{asset}} - \text{Tax Base}_{\text{asset}}) \times t$$

$$DTA = (\text{Tax Base}_{\text{asset}} - \text{Carrying Amount}_{\text{asset}}) \times t$$

trong đó $t$ là thuế suất đã được ban hành.

### P&L Approach

Deferred tax expense là **sự thay đổi** trong số dư deferred tax:

$$\text{Deferred Tax Expense} = \Delta DTL - \Delta DTA$$

---

## 6. Effective Tax Rate vs Statutory Tax Rate

| Chỉ số | Công thức |
|---|---|
| Statutory tax rate | Thuế suất được quy định bởi pháp luật |
| Effective tax rate | $\dfrac{\text{Tax Expense}}{\text{Pre-tax Income}}$ |
| Cash tax rate | $\dfrac{\text{Taxes Paid (cash)}}{\text{Pre-tax Income}}$ |

- **Permanent differences** khiến effective rate khác với statutory rate
- **Temporary differences** khiến cash tax rate khác với effective rate

---

## 7. Ảnh hưởng của Thay đổi Thuế suất lên DTA/DTL

Khi thuế suất thay đổi, số dư DTA và DTL hiện có phải được **tính lại** theo thuế suất đã được ban hành mới:

$$\text{New DTL} = \text{Temporary Difference} \times t_{\text{new}}$$

- Nếu thuế suất **tăng**: số dư DTL và DTA tăng lên
- Nếu thuế suất **giảm**: số dư DTL và DTA giảm xuống

Khoản điều chỉnh này được phản ánh qua **income tax expense** trên báo cáo thu nhập.

---

## 8. Valuation Allowance cho DTA

DTA chỉ được ghi nhận trong phạm vi mà việc có đủ thu nhập chịu thuế để sử dụng lợi ích thuế hoãn lại là **có thể xảy ra** (IFRS) hoặc **nhiều khả năng xảy ra hơn là không** (US GAAP).

- Nếu việc thu hồi không có khả năng xảy ra, một **valuation allowance** được thiết lập để giảm DTA
- Valuation allowance được đánh giá lại vào mỗi kỳ báo cáo

$$\text{Net DTA} = \text{Gross DTA} - \text{Valuation Allowance}$$

---

## 9. Khác biệt giữa IFRS và US GAAP

| Nội dung | IFRS | US GAAP |
|---|---|---|
| Phân loại DTA/DTL | Chỉ dài hạn (non-current) | Chỉ dài hạn (non-current) |
| Ngưỡng ghi nhận DTA | "Probable" rằng lợi ích sẽ được thu hồi | "More likely than not" (>50%) |
| Đánh giá lại tài sản | Tax base không thay đổi; tạo ra temporary difference | Việc đánh giá lại thường không được phép |
| Lợi nhuận chưa phân phối của công ty con | Ghi nhận DTL trừ khi công ty mẹ kiểm soát thời điểm và việc đảo ngược là không có khả năng | Ghi nhận DTL trừ khi được tái đầu tư vô thời hạn |
| Thuế suất sử dụng | Thuế suất đã ban hành hoặc về cơ bản đã ban hành | Chỉ thuế suất đã ban hành |

---

## Công thức Tóm tắt

| Công thức | Biểu thức |
|---|---|
| Tax expense | $\text{Tax Payable} + \text{Deferred Tax Expense}$ |
| Tax payable | $\text{Taxable Income} \times t$ |
| DTL (balance sheet) | $(\text{CA} - \text{TB}) \times t$ |
| DTA (balance sheet) | $(\text{TB} - \text{CA}) \times t$ |
| Deferred tax expense | $\Delta DTL - \Delta DTA$ |
| Effective tax rate | $\dfrac{\text{Tax Expense}}{\text{Pre-tax Income}}$ |
| Cash tax rate | $\dfrac{\text{Taxes Paid}}{\text{Pre-tax Income}}$ |

---

## Ghi chú Liên quan

- [[financial-statement-analysis/modules/m08-liabilities-and-equity/index|M08: Liabilities and Equity]]
- [[financial-statement-analysis/modules/m10-financial-reporting-quality/index|M10: Financial Reporting Quality]]
- [[financial-statement-analysis/modules/m11-financial-analysis-techniques/index|M11: Financial Analysis Techniques]]