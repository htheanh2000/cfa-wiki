---
title: "M11 — Employee Compensation"
type: module
subject: fsa
module: M11
los: [Pre.i, 11.a, 11.b, 11.c, 11.d, 11.e, 11.f]
created: 2026-04-10
updated: 2026-04-10
tags: [cfa-level-1, fsa, ratio-analysis, dupont, liquidity, solvency, profitability, activity-ratios, valuation-ratios]
---

# M11: Financial Analysis Techniques

## Tổng quan

Các kỹ thuật phân tích tài chính chuyển đổi dữ liệu tài chính thô thành các chỉ số có ý nghĩa để so sánh theo thời gian, giữa các công ty và giữa các ngành. Các công cụ chính bao gồm ratio analysis, common-size analysis, phân tích đồ thị và regression analysis.

---

## 1. Công cụ Phân tích

| Công cụ | Mô tả |
|---|---|
| **Ratio analysis** | Tính toán mối quan hệ giữa các khoản mục trên báo cáo tài chính |
| **Common-size analysis** | Biểu thị các khoản mục dưới dạng phần trăm (so với doanh thu trên IS, so với tổng tài sản trên BS) |
| **Graphical analysis** | Trực quan hóa xu hướng theo thời gian |
| **Regression analysis** | Mô hình thống kê về mối quan hệ giữa các biến số |

---

## 2. Activity Ratios

Activity ratios đo lường mức độ hiệu quả trong việc sử dụng tài sản của một công ty.

| Chỉ số | Công thức |
|---|---|
| Receivables turnover | $\dfrac{\text{Revenue}}{\text{Average Accounts Receivable}}$ |
| Days sales outstanding (DSO) | $\dfrac{365}{\text{Receivables Turnover}}$ |
| Inventory turnover | $\dfrac{\text{COGS}}{\text{Average Inventory}}$ |
| Days of inventory on hand (DOH) | $\dfrac{365}{\text{Inventory Turnover}}$ |
| Payables turnover | $\dfrac{\text{Purchases}}{\text{Average Accounts Payable}}$ |
| Days payable outstanding | $\dfrac{365}{\text{Payables Turnover}}$ |
| Working capital turnover | $\dfrac{\text{Revenue}}{\text{Average Working Capital}}$ |
| Fixed asset turnover | $\dfrac{\text{Revenue}}{\text{Average Net Fixed Assets}}$ |
| Total asset turnover | $\dfrac{\text{Revenue}}{\text{Average Total Assets}}$ |

---

## 3. Liquidity Ratios

Liquidity ratios đo lường khả năng đáp ứng các nghĩa vụ ngắn hạn.

| Chỉ số | Công thức |
|---|---|
| Current ratio | $\dfrac{\text{Current Assets}}{\text{Current Liabilities}}$ |
| Quick ratio | $\dfrac{\text{Cash} + \text{Short-term Investments} + \text{Receivables}}{\text{Current Liabilities}}$ |
| Cash ratio | $\dfrac{\text{Cash} + \text{Short-term Investments}}{\text{Current Liabilities}}$ |
| Defensive interval ratio | $\dfrac{\text{Cash} + \text{Short-term Investments} + \text{Receivables}}{\text{Daily Cash Expenditures}}$ |

### Cash Conversion Cycle

$$\text{CCC} = \text{DOH} + \text{DSO} - \text{Days Payable Outstanding}$$

trong đó:
- $\text{DOH}$ = số ngày tồn kho bình quân
- $\text{DSO}$ = số ngày thu tiền bình quân
- **CCC càng ngắn** thì thường càng tốt — tiền mặt bị ràng buộc trong hoạt động kinh doanh ít thời gian hơn

---

## 4. Solvency Ratios

Solvency ratios đo lường khả năng đáp ứng các nghĩa vụ dài hạn.

### Leverage Ratios

| Chỉ số | Công thức |
|---|---|
| Debt-to-assets | $\dfrac{\text{Total Debt}}{\text{Total Assets}}$ |
| Debt-to-capital | $\dfrac{\text{Total Debt}}{\text{Total Debt} + \text{Equity}}$ |
| Debt-to-equity | $\dfrac{\text{Total Debt}}{\text{Total Equity}}$ |
| Financial leverage ratio | $\dfrac{\text{Average Total Assets}}{\text{Average Total Equity}}$ |

### Coverage Ratios

| Chỉ số | Công thức |
|---|---|
| Interest coverage | $\dfrac{\text{EBIT}}{\text{Interest Expense}}$ |
| Fixed charge coverage | $\dfrac{\text{EBIT} + \text{Lease Payments}}{\text{Interest Expense} + \text{Lease Payments}}$ |

---

## 5. Profitability Ratios

| Chỉ số | Công thức |
|---|---|
| Gross profit margin | $\dfrac{\text{Gross Profit}}{\text{Revenue}}$ |
| Operating profit margin | $\dfrac{\text{Operating Income}}{\text{Revenue}}$ |
| Net profit margin | $\dfrac{\text{Net Income}}{\text{Revenue}}$ |
| ROA | $\dfrac{\text{Net Income}}{\text{Average Total Assets}}$ |
| ROE | $\dfrac{\text{Net Income}}{\text{Average Total Equity}}$ |
| Return on total capital | $\dfrac{\text{EBIT}}{\text{Average Total Capital}}$ |

---

## 6. DuPont Analysis

### Phân tích 3 nhân tố

$$\text{ROE} = \underbrace{\frac{\text{Net Income}}{\text{Revenue}}}_{\text{Net Profit Margin}} \times \underbrace{\frac{\text{Revenue}}{\text{Average Total Assets}}}_{\text{Asset Turnover}} \times \underbrace{\frac{\text{Average Total Assets}}{\text{Average Equity}}}_{\text{Financial Leverage}}$$

### Phân tích mở rộng 5 nhân tố

$$\text{ROE} = \underbrace{\frac{\text{Net Income}}{\text{EBT}}}_{\text{Tax Burden}} \times \underbrace{\frac{\text{EBT}}{\text{EBIT}}}_{\text{Interest Burden}} \times \underbrace{\frac{\text{EBIT}}{\text{Revenue}}}_{\text{EBIT Margin}} \times \underbrace{\frac{\text{Revenue}}{\text{Avg Assets}}}_{\text{Asset Turnover}} \times \underbrace{\frac{\text{Avg Assets}}{\text{Avg Equity}}}_{\text{Leverage}}$$

> Phân tích 5 nhân tố tách biệt tác động của **chính sách thuế**, **cấu trúc vốn**, **hiệu quả hoạt động**, **hiệu suất sử dụng tài sản** và **financial leverage** lên ROE.

---

## 7. Valuation Ratios

| Chỉ số | Công thức |
|---|---|
| Price-to-earnings (P/E) | $\dfrac{\text{Price per Share}}{\text{EPS}}$ |
| Price-to-book (P/B) | $\dfrac{\text{Price per Share}}{\text{Book Value per Share}}$ |
| Price-to-sales (P/S) | $\dfrac{\text{Price per Share}}{\text{Sales per Share}}$ |
| Price-to-cash-flow (P/CF) | $\dfrac{\text{Price per Share}}{\text{Cash Flow per Share}}$ |
| Dividend yield | $\dfrac{\text{Dividends per Share}}{\text{Price per Share}}$ |
| Earnings yield | $\dfrac{\text{EPS}}{\text{Price per Share}}$ |

---

## 8. Segment Reporting

Các công ty phải công bố dữ liệu tài chính theo **operating segment**:

- **Doanh thu** theo phân khúc
- **Lợi nhuận/lỗ** theo phân khúc
- **Tài sản** theo phân khúc

Hữu ích khi đánh giá các tập đoàn đa ngành, nơi các chỉ số tổng hợp có thể che khuất hiệu quả hoạt động của từng mảng kinh doanh riêng lẻ.

---

## 9. Dự báo với Ratios

- Sử dụng các chỉ số lịch sử để **dự báo** báo cáo tài chính tương lai
- Cách tiếp cận phổ biến: dự báo doanh thu trước, sau đó áp dụng các tỷ suất lợi nhuận và activity ratios lịch sử
- Sensitivity analysis: thay đổi các giả định chính để đánh giá phạm vi kết quả có thể xảy ra
- Ratios cung cấp cơ sở cho việc so sánh **cross-sectional** (so với các công ty cùng ngành) và **time-series** (so với lịch sử của chính công ty)

---

## Công thức Trọng tâm

| Công thức | Biểu thức |
|---|---|
| CCC | $\text{DOH} + \text{DSO} - \text{Days Payable}$ |
| ROE (DuPont 3) | $\text{NPM} \times \text{Asset Turnover} \times \text{Leverage}$ |
| Interest coverage | $\dfrac{\text{EBIT}}{\text{Interest Expense}}$ |
| Current ratio | $\dfrac{\text{CA}}{\text{CL}}$ |

---

## Ghi chú Liên quan

- [[financial-statement-analysis/modules/m10-financial-reporting-quality/index|M10: Financial Reporting Quality]]
- [[financial-statement-analysis/modules/m12-financial-statement-modeling/index|M12: Financial Statement Modeling]]
- [[financial-statement-analysis/modules/pre2-applications-of-fsa/index|Pre2: Applications of FSA]]