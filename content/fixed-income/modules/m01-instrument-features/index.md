---
title: "M01 — Bond Features"
type: module
subject: fixed-income
module: M01
los: "1.a–1.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M01
  - bond-features
  - covenants
---

# M01 – FI Instrument Features

> **Nguồn**: [[fixed-income/sources/sapp-fi-2026|SAPP FI 2026]], tr.3–39
> **LOS**: 1.a – Mô tả chứng khoán thu nhập cố định và các đặc điểm của chúng
> **LOS**: 1.b – Mô tả nội dung của bond indenture

## 1. Fixed-Income Securities là gì?

Fixed-income securities là các **nghĩa vụ hợp đồng** yêu cầu tổ chức phát hành thực hiện các khoản thanh toán đã định (lãi và/hoặc gốc) cho người nắm giữ trái phiếu.

Điểm khác biệt then chốt so với cổ phiếu:
- Người nắm giữ FI có **quyền ưu tiên cao hơn** trong việc đòi tài sản và dòng tiền so với cổ đông
- Lợi nhuận FI thường **dự đoán được hơn** (được xác định theo hợp đồng)
- Người nắm giữ FI là **chủ nợ**, không phải chủ sở hữu

## 2. Đặc điểm trái phiếu (Bond Features)

### 2.1 Issuer (Tổ chức phát hành)

Ba nhóm lớn:
- **Government** — sovereign, non-sovereign, quasi-government, supranational
- **Corporate** — công ty tài chính và phi tài chính
- **Structured finance** — công cụ chứng khoán hóa (ABS, MBS)

### 2.2 Maturity (Kỳ hạn)

| Phân loại | Kỳ hạn | Ví dụ |
|-----------|--------|-------|
| **Money market** | < 1 năm | T-bills, commercial paper |
| **Capital market** | > 1 năm | T-notes, T-bonds, corporate bonds |
| **Perpetual** | Không có ngày đáo hạn | Một số preferred securities, consols |

### 2.3 Par Value (Face Value — Mệnh giá)

- Số tiền gốc được hoàn trả khi đáo hạn
- Thường là \$1,000 mỗi trái phiếu (thị trường Mỹ)
- Giá trái phiếu được niêm yết theo phần trăm của par

### 2.4 Coupon Rate & Frequency (Lãi suất coupon & tần suất thanh toán)

| Loại | Mô tả |
|------|-------|
| **Fixed-rate** | Coupon cố định trong suốt vòng đời trái phiếu |
| **Floating-rate (FRN)** | Coupon = Market Reference Rate (MRR) + spread |
| **Zero-coupon** | Không có khoản thanh toán định kỳ; phát hành chiết khấu so với par |

Tần suất coupon: hàng năm, nửa năm một lần (chuẩn Mỹ), hàng quý, hoặc hàng tháng.

### 2.5 Seniority (Thứ tự ưu tiên trong đòi bồi thường)

Từ ưu tiên cao nhất đến thấp nhất:

1. **Senior secured** — được đảm bảo bằng tài sản thế chấp cụ thể
2. **Senior unsecured** — không có tài sản thế chấp, nhưng là quyền đòi ưu tiên
3. **Subordinated (junior)** — được thanh toán sau các khoản senior
4. **Subordinated unsecured** — ưu tiên thấp nhất trong số các chủ nợ

### 2.6 Contingency Provisions (Embedded Options — Điều khoản có điều kiện)

| Option | Bên hưởng lợi | Mô tả |
|--------|---------------|-------|
| **Callable** | Issuer | Issuer có thể mua lại trái phiếu trước khi đáo hạn |
| **Putable** | Nhà đầu tư | Nhà đầu tư có thể bán lại trái phiếu cho issuer trước khi đáo hạn |
| **Convertible** | Nhà đầu tư | Nhà đầu tư có thể chuyển đổi trái phiếu thành cổ phần |

## 3. Các thước đo lợi suất (Yield Measures)

### Current Yield

$$\text{Current Yield} = \frac{\text{Annual Coupon Payment}}{\text{Current Market Price}}$$

- Thước đo đơn giản; bỏ qua lãi/lỗ vốn và giá trị thời gian của tiền

### Yield to Maturity (YTM)

$$P = \sum_{t=1}^{n} \frac{PMT}{(1 + YTM)^t} + \frac{FV}{(1 + YTM)^n}$$

- YTM = **internal rate of return** (IRR) của dòng tiền trái phiếu
- Giả định: nắm giữ đến đáo hạn, tất cả coupon được tái đầu tư tại YTM, không có vỡ nợ

## 4. Bond Indenture

**Bond indenture** (trust deed) là hợp đồng pháp lý giữa tổ chức phát hành và người nắm giữ trái phiếu, quy định tất cả các điều khoản và điều kiện.

### 4.1 Affirmative Covenants (Giao ước xác nhận)

Các nghĩa vụ mà issuer **phải** thực hiện:
- Duy trì tài sản trong tình trạng tốt
- Nộp thuế và các nghĩa vụ khác
- Cung cấp báo cáo tài chính đã kiểm toán
- Tuân thủ các quy định pháp luật hiện hành

### 4.2 Negative Covenants (Giao ước hạn chế)

Các hạn chế đối với hành động của issuer:
- **Hạn chế phát hành thêm nợ**
- **Hạn chế chi trả cổ tức** cho cổ đông
- **Hạn chế bán tài sản** hoặc cầm cố tài sản
- Duy trì một số tỷ lệ tài chính nhất định (ví dụ: debt-to-equity)

> **Nhận xét quan trọng**: Negative covenants bảo vệ người nắm giữ trái phiếu bằng cách ngăn issuer thực hiện các hành động có thể làm suy giảm khả năng thực hiện nghĩa vụ nợ của họ.

## Related

- [[fixed-income/m02-cash-flows-and-types/index|M02 – FI Cash Flows and Types]]
- [[fixed-income/m03-issuance-and-trading/index|M03 – FI Issuance and Trading]]
- [[fixed-income/concepts/]] — Bond features, covenants