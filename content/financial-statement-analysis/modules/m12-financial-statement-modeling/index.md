---
title: "M12 — Quality of Reports"
type: module
subject: fsa
module: M12
los: [12.a, 12.b, 12.c, 12.d]
created: 2026-04-10
updated: 2026-04-10
tags: [cfa-level-1, fsa, financial-modeling, revenue-forecast, sensitivity-analysis, scenario-analysis]
---

# M12: Financial Statement Modeling

## Tổng quan

Financial statement modeling là quá trình xây dựng các dự báo tích hợp cho income statement, balance sheet và cash flow statement. Ba báo cáo này được liên kết với nhau, do đó thay đổi ở một báo cáo sẽ ảnh hưởng đến các báo cáo còn lại. Các mô hình này được sử dụng cho mục đích định giá, phân tích tín dụng và lập kế hoạch chiến lược.

---

## 1. Revenue Modeling

### Top-Down Approach

Bắt đầu từ cấp độ vĩ mô và thu hẹp dần xuống:

$$\text{Company Revenue} = \text{GDP Growth} \rightarrow \text{Industry Growth} \rightarrow \text{Market Share} \times \text{Industry Revenue}$$

Các bước thực hiện:
1. Dự báo điều kiện kinh tế vĩ mô (GDP, lạm phát)
2. Ước tính tốc độ tăng trưởng ngành
3. Ước tính thị phần của công ty trong ngành
4. Suy ra doanh thu của công ty

### Bottom-Up Approach

Bắt đầu từ các yếu tố cụ thể của công ty:

$$\text{Revenue} = \text{Units Sold} \times \text{Average Selling Price}$$

hoặc phân tích theo dòng sản phẩm, khu vực địa lý, phân khúc khách hàng, v.v.

> **Thực hành tốt nhất:** sử dụng cả hai phương pháp và đối chiếu các kết quả khác nhau.

---

## 2. Expense Modeling

### Variable Costs

Các chi phí biến đổi theo doanh thu, thường được mô hình hóa dưới dạng tỷ lệ phần trăm:

$$\text{COGS} = \text{Revenue} \times \text{COGS \% of Revenue}$$

Sử dụng COGS margin lịch sử và điều chỉnh theo các thay đổi dự kiến trong chi phí đầu vào.

### Fixed Costs

Các chi phí không thay đổi theo doanh thu trong ngắn hạn:

- **SGA (Selling, General & Administrative)**: một phần cố định, một phần biến đổi
- **R&D**: thường được mô hình hóa dưới dạng tỷ lệ phần trăm của doanh thu hoặc một khoản cố định
- **Depreciation**: gắn liền với số dư PPE và các giả định về capital expenditure

$$\text{Depreciation} = \frac{\text{Gross PPE}}{\text{Useful Life}}$$

---

## 3. Balance Sheet Modeling

### Working Capital Items

Các khoản mục working capital thường được liên kết với doanh thu hoặc COGS thông qua các tỷ số vòng quay:

$$\text{Accounts Receivable} = \frac{\text{Revenue} \times \text{DSO}}{365}$$

$$\text{Inventory} = \frac{\text{COGS} \times \text{DOH}}{365}$$

$$\text{Accounts Payable} = \frac{\text{COGS} \times \text{Days Payable}}{365}$$

### Long-Term Assets

$$\text{PPE}_{t} = \text{PPE}_{t-1} + \text{CapEx} - \text{Depreciation}$$

### Capital Structure

- **Debt**: được mô hình hóa dựa trên lịch trả nợ hiện tại và các giả định về phát hành mới
- **Equity**: được cập nhật thông qua retained earnings từ income statement dự báo

$$\text{Retained Earnings}_{t} = \text{RE}_{t-1} + \text{Net Income} - \text{Dividends}$$

---

## 4. Cash Flow Modeling

Dòng tiền được **suy ra** từ income statement và balance sheet dự báo — không được mô hình hóa độc lập.

### CFO (Indirect Method)

$$\text{CFO} = \text{Net Income} + \text{Depreciation} - \Delta \text{Working Capital}$$

### CFI

$$\text{CFI} = -\text{CapEx} + \text{Proceeds from Asset Sales}$$

### CFF

$$\text{CFF} = \text{New Debt Issued} - \text{Debt Repaid} - \text{Dividends Paid} + \text{Equity Issued} - \text{Share Buybacks}$$

### Cân bằng mô hình

$$\text{Cash}_{t} = \text{Cash}_{t-1} + \text{CFO} + \text{CFI} + \text{CFF}$$

> Số dư tiền mặt cuối kỳ trên cash flow statement phải bằng số dư tiền mặt trên balance sheet dự báo. Đây là bước kiểm tra tính toàn vẹn quan trọng nhất của mô hình.

---

## 5. Sensitivity Analysis và Scenario Analysis

### Sensitivity Analysis

Thay đổi **một biến đầu vào tại một thời điểm** để quan sát tác động lên các kết quả đầu ra chính:

- Điều gì xảy ra với net income nếu tốc độ tăng trưởng doanh thu là 2% thay vì 5%?
- Tác động của sự thay đổi 100bps trong lãi suất đến interest expense là gì?

### Scenario Analysis

Thay đổi **nhiều biến đầu vào cùng lúc** để mô hình hóa các kịch bản nhất quán:

| Kịch bản | Revenue Growth | COGS Margin | CapEx |
|---|---|---|---|
| Bull case | 10% | 60% | Cao |
| Base case | 5% | 65% | Trung bình |
| Bear case | -2% | 70% | Thấp |

> Scenario analysis nắm bắt được **tương quan** giữa các biến số mà sensitivity analysis bỏ qua.

---

## Công thức trọng tâm

| Công thức | Biểu thức |
|---|---|
| Revenue (bottom-up) | $\text{Units} \times \text{Price}$ |
| COGS | $\text{Revenue} \times \text{COGS margin}$ |
| AR | $\dfrac{\text{Revenue} \times \text{DSO}}{365}$ |
| Inventory | $\dfrac{\text{COGS} \times \text{DOH}}{365}$ |
| PPE roll-forward | $\text{PPE}_{t-1} + \text{CapEx} - \text{Depreciation}$ |
| Kiểm tra số dư tiền mặt | $\text{Cash}_{t-1} + \text{CFO} + \text{CFI} + \text{CFF}$ |

---

## Ghi chú liên quan

- [[financial-statement-analysis/modules/m11-financial-analysis-techniques/index|M11: Financial Analysis Techniques]]
- [[financial-statement-analysis/modules/pre2-applications-of-fsa/index|Pre2: Applications of FSA]]
- [[financial-statement-analysis/modules/m04-cash-flows-i/index|M04: Cash Flow Statement (Part I)]]