---
title: "M04 — Cash Flows I"
type: module
subject: fsa
module: M04
los: [Pre.i, Pre.ii, Pre.iii, 4.a, 4.b, 4.c, 4.d]
created: 2026-04-10
updated: 2026-04-10
tags: [cfa-level-1, fsa, cash-flows, cfo, cfi, cff, direct-method, indirect-method]
---

# M04: Cash Flow Statement (Part I)

## Tổng quan

Báo cáo lưu chuyển tiền tệ đối chiếu net income với dòng tiền thực tế được tạo ra và sử dụng trong kỳ. Báo cáo phân loại tất cả dòng tiền thành ba hoạt động:

$$\text{CFO} + \text{CFI} + \text{CFF} = \Delta \text{Cash}$$

---

## 1. Phân loại Dòng tiền

### Hoạt động kinh doanh (CFO)

Dòng tiền từ các giao dịch **ảnh hưởng đến net income** — các hoạt động tạo doanh thu cốt lõi của doanh nghiệp.

| Ví dụ dòng tiền vào | Ví dụ dòng tiền ra |
|---|---|
| Tiền thu từ khách hàng | Tiền trả cho nhà cung cấp |
| Interest received (tùy theo chuẩn mực) | Tiền trả cho nhân viên |
| Dividends received (tùy theo chuẩn mực) | Thuế đã nộp |

### Hoạt động đầu tư (CFI)

Dòng tiền từ việc mua và thanh lý **tài sản dài hạn** và các khoản đầu tư.

| Ví dụ dòng tiền vào | Ví dụ dòng tiền ra |
|---|---|
| Bán PPE | Mua PPE |
| Bán chứng khoán đầu tư | Mua chứng khoán đầu tư |
| Thu hồi gốc từ các khoản cho vay | Cho vay đối với bên khác |

### Hoạt động tài chính (CFF)

Dòng tiền từ các giao dịch **thay đổi cơ cấu vốn** — nợ và vốn chủ sở hữu.

| Ví dụ dòng tiền vào | Ví dụ dòng tiền ra |
|---|---|
| Phát hành cổ phiếu | Mua lại cổ phiếu |
| Phát hành trái phiếu/nợ | Trả gốc nợ vay |
| | Dividend payments (tùy theo chuẩn mực) |

---

## 2. Sự khác biệt phân loại giữa IFRS và US GAAP

| Khoản mục | IFRS | US GAAP |
|---|---|---|
| Interest received | CFO hoặc CFI | CFO |
| Interest paid | CFO hoặc CFF | CFO |
| Dividends received | CFO hoặc CFI | CFO |
| Dividends paid | CFO hoặc CFF | CFF |
| Taxes paid | CFO (trừ khi xác định cụ thể thuộc CFI/CFF) | CFO |
| Bank overdrafts | Thuộc tiền và tương đương tiền | CFF |

> **Điểm mấu chốt:** IFRS cho phép **linh hoạt** trong phân loại; US GAAP mang tính **quy định cụ thể**.

---

## 3. Phương pháp trực tiếp (Direct Method)

Direct method điều chỉnh **từng khoản mục trên income statement** từ cơ sở dồn tích sang cơ sở tiền mặt.

### Các công thức chuyển đổi chính

**Tiền thu từ khách hàng:**

$$\text{Cash from customers} = \text{Revenue} - \Delta \text{Accounts Receivable}$$

**Tiền trả cho nhà cung cấp:**

$$\text{Cash to suppliers} = \text{COGS} + \Delta \text{Inventory} - \Delta \text{Accounts Payable}$$

**Tiền trả cho chi phí hoạt động:**

$$\text{Cash for OpEx} = \text{Operating Expenses} - \Delta \text{Accrued Liabilities} + \Delta \text{Prepaid Expenses}$$

---

## 4. Phương pháp gián tiếp (Indirect Method)

Indirect method bắt đầu từ **net income** và thực hiện ba loại điều chỉnh:

$$\text{CFO} = \text{Net Income} + \text{Non-cash charges} \pm \Delta \text{Working Capital}$$

### Các điều chỉnh

1. **Cộng lại các chi phí không bằng tiền mặt:** depreciation, amortization, impairment losses
2. **Loại bỏ các khoản lãi/lỗ không thuộc hoạt động kinh doanh:** gain/loss on sale of assets (phân loại lại vào CFI)
3. **Điều chỉnh theo biến động working capital:**

| Biến động Working Capital | Điều chỉnh vào NI |
|---|---|
| $\uparrow$ Tài sản ngắn hạn (ví dụ: AR, inventory) | Trừ đi |
| $\downarrow$ Tài sản ngắn hạn | Cộng vào |
| $\uparrow$ Nợ ngắn hạn (ví dụ: AP) | Cộng vào |
| $\downarrow$ Nợ ngắn hạn | Trừ đi |

---

## 5. Chuyển đổi từ Indirect Method sang Direct Method

Để chuyển đổi từ indirect sang direct, đảo ngược các điều chỉnh và tái cấu trúc từng khoản mục tiền mặt:

1. Bắt đầu từ CFO theo indirect method
2. Đối với từng dòng trên income statement, áp dụng các biến động tương ứng trên balance sheet
3. Tính toán tiền thu được, tiền trả nhà cung cấp, tiền trả chi phí, v.v.

> Cả hai phương pháp đều cho ra **cùng một giá trị CFO**. Chỉ khác nhau ở cách trình bày.

---

## 6. Mối liên hệ: Cash Flow Statement, Income Statement và Balance Sheet

```
Income Statement          Balance Sheet              Cash Flow Statement
─────────────────         ──────────────             ───────────────────
Revenue            ──→    Accounts Receivable  ──→   CFO adjustments
COGS               ──→    Inventory / AP       ──→   CFO adjustments
Depreciation       ──→    Accumulated Depr.    ──→   Add back (indirect)
Interest Expense   ──→    Interest Payable     ──→   CFO or CFF
Net Income         ──→    Retained Earnings    ──→   Starting point (indirect)
                          PPE (net)            ──→   CFI
                          Debt / Equity        ──→   CFF
                          Cash                 ──→   Net change = CFO+CFI+CFF
```

---

## Công thức tổng hợp

| Công thức | Biểu thức |
|---|---|
| Biến động tiền thuần | $\text{CFO} + \text{CFI} + \text{CFF}$ |
| Tiền thu từ khách hàng | $\text{Revenue} - \Delta AR$ |
| Tiền trả nhà cung cấp | $\text{COGS} + \Delta \text{Inv} - \Delta AP$ |
| CFO (indirect) | $\text{NI} + \text{Non-cash} \pm \Delta WC$ |

---

## Ghi chú liên quan

- [[financial-statement-analysis/modules/m05-cash-flows-ii/index|M05: Cash Flow Statement (Part II)]]
- [[financial-statement-analysis/modules/m06-inventories/index|M06: Inventories]]
- [[financial-statement-analysis/modules/m08-liabilities-and-equity/index|M08: Liabilities and Equity]]