---
title: "M16 — Credit Risk"
type: module
subject: fixed-income
module: M16
los: "16.a–16.c"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M16
  - corporate-bonds
  - credit-analysis
  - seniority
  - notching
---

# M16 – Credit Analysis: Corporate Issuers

> **LOS 16.a**: Mô tả các yếu tố định tính và định lượng trong phân tích tín dụng doanh nghiệp
> **LOS 16.b**: Mô tả thứ tự ưu tiên (seniority ranking) của nợ doanh nghiệp
> **LOS 16.c**: Mô tả xếp hạng tổ chức phát hành và xếp hạng từng đợt phát hành, notching, và cross-default provisions

---

## 1. Yếu tố định tính (Qualitative Factors)

### 1.1 Mô hình kinh doanh & Ngành

| Yếu tố | Câu hỏi trọng tâm |
|--------|---------------|
| **Business model** | Doanh thu có đa dạng không? Có tính định kỳ hay chu kỳ? Lợi thế cạnh tranh (moat)? |
| **Cạnh tranh ngành** | Cấu trúc thị trường, rào cản gia nhập, sức mạnh định giá, môi trường pháp lý |
| **Business risk** | Operating leverage, mức độ tập trung khách hàng, rủi ro gián đoạn công nghệ |

### 1.2 Quản trị doanh nghiệp (Corporate Governance)

- **Debt covenants**: Mức độ chặt chẽ và khả năng thực thi của các điều khoản bảo vệ
- **Chính sách kế toán**: Ghi nhận doanh thu thận trọng hay tích cực, các khoản mục ngoại bảng (off-balance-sheet items)
- **Chất lượng ban lãnh đạo**: Lịch sử hoạt động, tầm nhìn chiến lược, kỷ luật phân bổ vốn
- **Tính độc lập của hội đồng quản trị**: Hiệu quả giám sát, mức độ gắn kết với lợi ích của chủ nợ

---

## 2. Yếu tố định lượng (Quantitative Factors)

### 2.1 Khả năng sinh lời (Profitability)

$$
\text{EBIT Margin} = \frac{\text{EBIT}}{\text{Revenue}}
$$

trong đó:
- $\text{EBIT}$ = Lợi nhuận trước lãi vay và thuế (Earnings Before Interest and Taxes)
- Biên lợi nhuận càng cao, khả năng tạo thu nhập để trả nợ càng mạnh

### 2.2 Đòn bẩy tài chính (Leverage)

$$
\text{Debt-to-EBITDA} = \frac{\text{Total Debt}}{\text{EBITDA}}
$$

trong đó:
- $\text{EBITDA}$ = Lợi nhuận trước lãi vay, thuế, khấu hao tài sản hữu hình và vô hình (Earnings Before Interest, Taxes, Depreciation, and Amortization)
- Tỷ lệ **thấp hơn** cho thấy đòn bẩy ít hơn và chất lượng tín dụng **tốt hơn**
- Các công ty investment-grade thường có Debt/EBITDA < 3–4x

### 2.3 Khả năng trả lãi (Coverage)

$$
\text{Interest Coverage} = \frac{\text{EBIT}}{\text{Interest Expense}}
$$

trong đó:
- Tỷ lệ coverage càng cao, **khả năng trả nợ** càng mạnh
- Các công ty investment-grade thường có coverage > 4–5x

### 2.4 Mức độ đầy đủ dòng tiền (Cash Flow Adequacy)

$$
\text{RCF-to-Net Debt} = \frac{\text{Retained Cash Flow}}{\text{Net Debt}}
$$

trong đó:
- $\text{RCF}$ = Retained Cash Flow (dòng tiền hoạt động trừ đi cổ tức)
- $\text{Net Debt}$ = Tổng nợ − Tiền mặt và các khoản tương đương tiền
- Đo lường khả năng giảm đòn bẩy từ dòng tiền nội sinh

### 2.5 Tóm tắt các tỷ số chính

| Tỷ số | Đo lường | Tín dụng tốt hơn khi = |
|-------|-----------------|-----------------|
| EBIT Margin | Khả năng sinh lời | Cao hơn |
| Debt / EBITDA | Đòn bẩy | Thấp hơn |
| EBIT / Interest | Coverage | Cao hơn |
| RCF / Net Debt | Mức độ đầy đủ dòng tiền | Cao hơn |

---

## 3. Thứ tự ưu tiên (Seniority Ranking)

Trong trường hợp **vỡ nợ và thanh lý (default and liquidation)**, các chủ nợ được thanh toán theo **seniority** (thứ tự ưu tiên về quyền đòi nợ):

| Thứ tự ưu tiên | Mức seniority | Tỷ lệ thu hồi điển hình |
|----------|----------------|----------------------|
| 1 (Cao nhất) | **Senior secured** | Cao nhất (60–80%) |
| 2 | **Senior unsecured** | Trung bình (40–60%) |
| 3 | **Senior subordinated** | Thấp hơn (20–40%) |
| 4 | **Subordinated** | Thấp (10–30%) |
| 5 (Thấp nhất) | **Junior subordinated** | Thấp nhất |

> Tỷ lệ thu hồi biến động đáng kể tùy theo ngành, điều kiện kinh tế và tài sản thế chấp cụ thể. Các con số trên là mức bình quân lịch sử xấp xỉ.

---

## 4. Issuer Rating và Issue Rating

| Loại xếp hạng | Còn gọi là | Phạm vi |
|-------------|---------------|-------|
| **Issuer rating** | Corporate Family Rating (CFR) | Phản ánh mức độ tín nhiệm tổng thể của **tổ chức phát hành** |
| **Issue rating** | Corporate Credit Rating (CCR) | Xếp hạng một **nghĩa vụ nợ cụ thể**, có tính đến seniority và các đặc điểm cấu trúc |

### 4.1 Notching

**Notching** là việc điều chỉnh issue rating so với issuer rating:

- **Secured debt**: Có thể được notch **lên** (cao hơn CFR) do có tài sản thế chấp bảo vệ
- **Subordinated debt**: Được notch **xuống** (thấp hơn CFR) do kỳ vọng thu hồi thấp hơn
- Mức notching điển hình: 1–2 bậc cho mỗi cấp độ subordination

> **Ví dụ**: Nếu issuer rating (CFR) = BBB:
> - Đợt phát hành senior secured → BBB+ (notch lên 1 bậc)
> - Đợt phát hành senior unsecured → BBB (bằng CFR)
> - Đợt phát hành subordinated → BBB− hoặc BB+ (notch xuống 1–2 bậc)

### 4.2 Cross-Default Provisions

**Cross-default provision** quy định rằng việc vỡ nợ trên **bất kỳ** nghĩa vụ nợ nào của tổ chức phát hành cũng cấu thành vỡ nợ đối với nghĩa vụ có chứa điều khoản này.

- **Mục đích**: Ngăn tổ chức phát hành chọn lọc vỡ nợ trên một nghĩa vụ trong khi vẫn tiếp tục thanh toán các nghĩa vụ khác
- **Tác động**: Đảm bảo **đối xử bình đẳng** với các chủ nợ trong tình huống kiệt quệ tài chính
- Thường xuất hiện trong bond indentures và loan agreements

---

## See Also

- [[fixed-income/m14-credit-risk/index|M14 – Credit Risk]]
- [[fixed-income/m15-credit-analysis-government/index|M15 – Credit Analysis: Government]]
- [[fixed-income/m04-corporate-issuers/index|M04 – Corporate Issuers]]
- [[fixed-income/concepts/credit-spread|Credit Spread]]