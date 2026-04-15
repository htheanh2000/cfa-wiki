---
title: Securitization
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [securitization, SPE, ABS, MBS, CMO, CDO, credit-enhancement]
---

# Securitization

## Tổng quan

**Securitization** là quá trình gộp các tài sản tài chính (khoản vay, các khoản phải thu) thành một pool và phát hành chứng khoán được bảo đảm bằng pool tài sản đó cho các nhà đầu tư.

### Các Bên Tham Gia Chính

| Vai trò | Mô tả |
|------|-------------|
| **Originator** | Tạo ra các khoản vay/tài sản cơ sở |
| **SPE/SPV** | Special Purpose Entity — thực thể pháp lý riêng biệt nắm giữ tài sản và phát hành chứng khoán |
| **Servicer** | Thu tiền thanh toán và quản lý pool tài sản |
| **Trustee** | Bảo vệ quyền lợi của nhà đầu tư |
| **Underwriter** | Cấu trúc và phân phối chứng khoán |
| **Rating agency** | Xếp hạng tín nhiệm cho các tranche được phát hành |

## Bankruptcy Remoteness

SPE được cấu trúc để **tách biệt về mặt pháp lý** khỏi originator:

- Nếu originator phá sản, **tài sản của SPE được bảo vệ**
- Quyền đòi nợ của nhà đầu tư gắn với pool tài sản, không phải với originator
- Đây là nền tảng giúp securitization giảm thiểu rủi ro
- Yêu cầu phải có **true sale** — chuyển nhượng tài sản thực sự từ originator sang SPE

## Credit Enhancement

### Internal Credit Enhancement

| Loại | Mô tả |
|------|-------------|
| **Subordination (tranching)** | Các junior tranche hấp thụ tổn thất trước, bảo vệ senior tranche |
| **Overcollateralization** | Giá trị pool tài sản lớn hơn giá trị chứng khoán phát hành |
| **Excess spread** | Chênh lệch giữa lãi suất thu được từ tài sản và lãi suất trả cho nhà đầu tư |
| **Reserve account** | Quỹ tiền mặt dự phòng để bù đắp tổn thất tiềm năng |

### External Credit Enhancement

| Loại | Mô tả |
|------|-------------|
| **Surety bond** | Công ty bảo hiểm đảm bảo việc thanh toán |
| **Bank letter of credit** | Ngân hàng cung cấp thanh khoản dự phòng |
| **Cash collateral account** | Tiền mặt ký quỹ bởi một bên thứ ba |

> External credit enhancement mang theo **rủi ro từ bên thứ ba (counterparty risk)**.

## Các Loại Sản Phẩm Securitized

### ABS (Asset-Backed Securities)

Được bảo đảm bằng pool các tài sản không phải thế chấp:
- **Auto loan ABS**: Cấu trúc khấu hao (amortizing); rủi ro trả trước (prepayment risk) thấp
- **Credit card ABS**: Cấu trúc revolving với lockout period (ban đầu chưa hoàn trả gốc)
- **Student loan ABS**
- **Equipment lease ABS**

### MBS (Mortgage-Backed Securities)

#### Residential MBS (RMBS)
- **Agency MBS**: Được bảo lãnh bởi các cơ quan chính phủ (Ginnie Mae) hoặc GSEs (Fannie Mae, Freddie Mac)
- **Non-agency MBS**: Không có bảo lãnh chính phủ; rủi ro tín dụng cao hơn

#### Mortgage Pass-Through Securities
- Nhà đầu tư nhận **phần chia theo tỷ lệ (pro-rata share)** của toàn bộ gốc và lãi từ pool thế chấp
- Chịu **prepayment risk**:
  - **Contraction risk**: Người vay trả trước nhanh hơn dự kiến (khi lãi suất giảm)
  - **Extension risk**: Người vay trả trước chậm hơn dự kiến (khi lãi suất tăng)

#### CMO (Collateralized Mortgage Obligation)
Phân phối lại dòng tiền thế chấp thành các **tranches** với hồ sơ rủi ro khác nhau:

| Loại Tranche | Mô tả |
|-------------|-------------|
| **Sequential-pay** | Các tranche nhận gốc theo thứ tự tuần tự (A trước, rồi B, v.v.) |
| **PAC tranche** | Planned Amortization Class — dòng tiền ổn định trong một biên độ prepayment nhất định |
| **Support (companion) tranche** | Hấp thụ biến động prepayment; bảo vệ PAC tranche |
| **Z-tranche (accrual)** | Không nhận dòng tiền cho đến khi các tranche trước đó được tất toán |

#### Commercial MBS (CMBS)
- Được bảo đảm bằng các khoản vay bất động sản thương mại
- **Loan-level call protection**: Prepayment lockout, defeasance, yield maintenance, phí trả trước
- **CMBS-level call protection**: Cấu trúc sequential-pay
- Chỉ số quan trọng: Tỷ lệ **Loan-to-Value (LTV)** và **Debt Service Coverage Ratio (DSCR)**

### CDO (Collateralized Debt Obligation)

Được bảo đảm bằng pool đa dạng các nghĩa vụ nợ:
- **CLO**: Collateralized Loan Obligation (khoản vay đòn bẩy — leveraged loans)
- **CBO**: Collateralized Bond Obligation
- **Synthetic CDO**: Sử dụng credit default swaps thay vì trái phiếu thực tế

Cấu trúc CDO:
- **Senior tranche**: Ưu tiên thanh toán cao nhất, lợi suất thấp nhất, xếp hạng tín nhiệm cao nhất
- **Mezzanine tranche**: Mức độ ưu tiên và rủi ro trung gian
- **Equity tranche**: Chịu tổn thất đầu tiên (first loss position), lợi suất cao nhất, không được xếp hạng

### Covered Bonds
- Trái phiếu được bảo đảm bằng một **cover pool** tài sản vẫn nằm trên bảng cân đối kế toán của tổ chức phát hành
- **Dual recourse**: Nhà đầu tư có quyền đòi nợ đối với cả cover pool lẫn tổ chức phát hành
- Không có bankruptcy remote — khác biệt so với ABS
- Phổ biến tại các thị trường châu Âu

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/credit-risk|Credit Risk]]
- [[fixed-income/concepts/interest-rate-risk|Interest Rate Risk]]
- [[fixed-income/concepts/bond-features|Bond Features]]
- [[fixed-income/glossary/fi-m17|Glossary: Module 17]]
- [[fixed-income/glossary/fi-m18|Glossary: Module 18]]
- [[fixed-income/glossary/fi-m19|Glossary: Module 19]]