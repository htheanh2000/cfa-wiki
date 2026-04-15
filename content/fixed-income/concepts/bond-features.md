---
title: Bond Features
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [bond, indenture, coupon, maturity, seniority, covenants]
---

# Bond Features

## Các Thành Phần Cơ Bản của Bond

Một **bond** (fixed-income security) là một nghĩa vụ hợp đồng trong đó tổ chức phát hành cam kết thực hiện các khoản thanh toán cụ thể cho trái chủ theo thời gian.

### Các Yếu Tố Chính

| Yếu tố | Mô tả |
|---------|-------------|
| **Issuer** | Tổ chức đi vay vốn (chính phủ, doanh nghiệp, tổ chức siêu quốc gia) |
| **Maturity (term)** | Ngày hoàn trả vốn gốc; tenor = thời gian còn lại đến maturity |
| **Par value (face value)** | Số tiền gốc được hoàn trả khi đáo hạn (thường là \$1,000) |
| **Coupon rate** | Lãi suất hằng năm tính trên par value |
| **Coupon frequency** | Tần suất trả coupon (hằng năm, nửa năm, hằng quý) |
| **Currency** | Đơn vị tiền tệ của các khoản thanh toán |
| **Seniority** | Thứ tự ưu tiên đối với tài sản khi thanh lý |

## Bond Indenture (Trust Deed)

**Indenture** là hợp đồng pháp lý giữa tổ chức phát hành và trái chủ, quy định:

- Coupon rate và các ngày thanh toán
- Ngày đáo hạn và par value
- Tài sản bảo đảm hoặc đảm bảo (nếu có)
- Covenants (các hạn chế đối với tổ chức phát hành)
- Các điều khoản call/put
- Yêu cầu về sinking fund

**Trustee** (thường là một tổ chức tài chính) giám sát việc tuân thủ indenture thay mặt cho các trái chủ.

## Covenants

### Affirmative Covenants
Các hành động tổ chức phát hành **bắt buộc phải** thực hiện:
- Thanh toán lãi và gốc đúng hạn
- Duy trì bảo hiểm cho tài sản
- Tuân thủ các quy định pháp luật hiện hành
- Nộp thuế khi đến hạn

### Negative (Restrictive) Covenants
Các hành động tổ chức phát hành **không được** thực hiện (hoặc bị giới hạn):
- Hạn chế phát hành thêm nợ
- Giới hạn chi trả cổ tức
- Hạn chế bán tài sản
- Hạn chế sáp nhập/mua lại
- Negative pledge clause (không được thế chấp tài sản cho chủ nợ khác)

## Phân Loại Bond theo Coupon

| Loại | Mô tả |
|------|-------------|
| **Fixed-rate** | Coupon rate cố định trong suốt vòng đời bond |
| **Floating-rate (FRN)** | Coupon = Reference rate + Quoted margin |
| **Zero-coupon** | Không có khoản thanh toán định kỳ; bán ở mức chiết khấu, hoàn trả theo par |
| **Step-up coupon** | Coupon rate tăng theo lịch trình định trước |
| **Payment-in-kind (PIK)** | Lãi được trả bằng cách phát hành thêm bond |
| **Deferred coupon** | Không có coupon trong giai đoạn đầu, sau đó thanh toán định kỳ bình thường |

## Phân Loại Bond theo Hình Thức Hoàn Trả Vốn Gốc

| Loại | Mô tả |
|------|-------------|
| **Bullet bond** | Toàn bộ vốn gốc được hoàn trả khi đáo hạn |
| **Amortizing bond** | Vốn gốc được hoàn trả dần trong suốt vòng đời bond |
| **Sinking fund** | Tổ chức phát hành thu hồi một phần bond định kỳ |

## Embedded Options

| Option | Lợi ích cho | Mô tả |
|--------|----------|-------------|
| **Callable** | Issuer | Issuer có thể mua lại trước hạn theo một call price nhất định |
| **Putable** | Bondholder | Bondholder có thể bán lại cho issuer trước khi đáo hạn |
| **Convertible** | Bondholder | Bondholder có thể chuyển đổi thành cổ phần của issuer |

- Callable bonds có **yield cao hơn** so với non-callable bonds tương đương (nhà đầu tư chịu call risk)
- Putable bonds có **yield thấp hơn** (nhà đầu tư được bảo vệ ở chiều giảm)
- Convertible bonds có **yield thấp hơn** (nhà đầu tư được hưởng lợi khi cổ phiếu tăng)

## Seniority và Bảo Đảm

### Secured vs. Unsecured

- **Secured bonds**: Được bảo đảm bằng tài sản cụ thể (mortgage bonds, equipment trust certificates)
- **Unsecured bonds (debentures)**: Chỉ được bảo đảm bằng uy tín tín dụng chung của issuer

### Thứ Tự Ưu Tiên Seniority (từ cao đến thấp)

1. First lien / First mortgage
2. Senior secured
3. Senior unsecured
4. Senior subordinated
5. Subordinated
6. Junior subordinated

> Seniority càng cao → yield càng thấp (rủi ro đối với nhà đầu tư càng thấp)

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/bond-valuation|Bond Valuation]]
- [[fixed-income/concepts/credit-risk|Credit Risk]]
- [[fixed-income/concepts/yield-measures|Yield Measures]]
- [[fixed-income/glossary/fi-m01|Glossary: Module 01]]
- [[fixed-income/glossary/fi-m02|Glossary: Module 02]]