---
title: Revenue Recognition
type: concept
subject: fsa
created: 2026-04-10
updated: 2026-04-10
tags: [fsa, revenue, ifrs-15, accrual, unearned-revenue]
---

# Revenue Recognition

## Accrual Principle

Doanh thu được ghi nhận khi **được kiếm ra (earned)**, bất kể thời điểm nhận tiền mặt. Đây là nền tảng của kế toán dồn tích (accrual accounting) và khác với kế toán tiền mặt (cash-basis accounting).

- **Accrual basis**: Doanh thu được ghi nhận khi performance obligation được thực hiện xong
- **Cash basis**: Doanh thu được ghi nhận khi nhận tiền mặt

## IFRS 15: Revenue from Contracts with Customers

IFRS 15 (hội tụ với ASC 606 theo US GAAP) thiết lập một **mô hình 5 bước** thống nhất cho việc ghi nhận doanh thu:

### Step 1: Identify the Contract with a Customer

Một hợp đồng tồn tại khi:
- Các bên đã phê duyệt và cam kết thực hiện
- Quyền lợi của mỗi bên có thể xác định được
- Điều khoản thanh toán có thể xác định được
- Có bản chất thương mại (commercial substance)
- Khả năng thu tiền là có thể xảy ra (probable)

### Step 2: Identify Performance Obligations

Một performance obligation là lời hứa chuyển giao một hàng hóa hoặc dịch vụ **riêng biệt (distinct)**. Hàng hóa/dịch vụ là distinct nếu:
- Khách hàng có thể hưởng lợi từ nó một mình (hoặc cùng với các nguồn lực sẵn có)
- Nó có thể tách biệt khỏi các cam kết khác trong hợp đồng

### Step 3: Determine the Transaction Price

Transaction price là khoản thù lao dự kiến nhận được để đổi lấy hàng hóa/dịch vụ. Cần xem xét:
- **Variable consideration** (chiết khấu, hoàn tiền, thưởng) — dùng giá trị kỳ vọng hoặc giá trị khả năng cao nhất
- **Significant financing component** — điều chỉnh nếu thời hạn thanh toán > 1 năm
- **Non-cash consideration** — đo lường theo fair value
- **Consideration payable to customer** — giảm trừ transaction price

### Step 4: Allocate the Transaction Price

Phân bổ cho mỗi performance obligation dựa trên **relative standalone selling prices**. Các phương pháp ước tính standalone price:
- Adjusted market assessment approach
- Expected cost plus margin approach
- Residual approach (sử dụng hạn chế)

### Step 5: Recognize Revenue When (or As) Performance Obligations Are Satisfied

**Point in time**: Quyền kiểm soát được chuyển giao tại một thời điểm cụ thể (ví dụ: giao hàng hóa)
**Over time**: Quyền kiểm soát được chuyển giao liên tục nếu:
- Khách hàng đồng thời nhận và tiêu thụ lợi ích
- Việc thực hiện của công ty tạo ra/nâng cao một tài sản mà khách hàng kiểm soát
- Việc thực hiện của công ty không tạo ra tài sản có công dụng thay thế, và công ty có quyền thanh toán cho phần đã thực hiện đến nay

Các phương pháp đo lường tiến độ (over time):
- **Output methods**: Số đơn vị đã giao, các mốc đã đạt được
- **Input methods**: Chi phí đã phát sinh, giờ lao động, giờ máy móc

## Credit Sales and Accounts Receivable

Khi hàng hóa được bán chịu (on credit):
- **Doanh thu** được ghi nhận tại thời điểm bán (performance obligation đã được thực hiện)
- **Accounts receivable** được tạo ra (tài sản)
- Tiền mặt được thu về sau

$$\text{Revenue (accrual)} \neq \text{Cash received}$$

**Ước tính nợ xấu (bad debt estimation)**: Doanh nghiệp phải ước tính các khoản không thu hồi được:
- Allowance method (bắt buộc theo GAAP/IFRS)
- Giảm AR theo allowance for doubtful accounts

## Unearned (Deferred) Revenue

Tiền mặt nhận được **trước** khi performance obligation được thực hiện:
- Ghi nhận là **nợ phải trả (liability)** (unearned revenue / deferred revenue)
- Được ghi nhận là doanh thu khi hàng hóa/dịch vụ được cung cấp

**Ví dụ**: Đăng ký tạp chí, bán vé trước, giấy phép phần mềm, thẻ quà tặng

**Journal entries:**
1. Nhận tiền mặt: Dr. Cash / Cr. Unearned Revenue
2. Cung cấp dịch vụ: Dr. Unearned Revenue / Cr. Revenue

## Special Revenue Recognition Topics

### Bill-and-Hold Arrangements
Doanh thu được ghi nhận trước khi giao hàng nếu khách hàng đã yêu cầu thỏa thuận này, rủi ro sở hữu đã được chuyển giao, và hàng hóa được xác định riêng biệt.

### Long-Term Contracts
- **Percentage-of-completion** (IFRS và GAAP cho over-time): Doanh thu được ghi nhận theo tỷ lệ
- **Completed-contract** (chỉ theo US GAAP cũ, không còn được phép theo ASC 606): Doanh thu ghi nhận khi hoàn thành

### Barter Transactions
Doanh thu được ghi nhận theo **fair value** của hàng hóa/dịch vụ trao đổi (nếu xác định được).

### Gross vs. Net Reporting
- **Principal** (kiểm soát hàng hóa trước khi chuyển giao): Báo cáo doanh thu **gross**
- **Agent** (sắp xếp thay mặt bên khác): Báo cáo doanh thu hoa hồng **net**

## IFRS vs. US GAAP

| Topic | IFRS (IFRS 15) | US GAAP (ASC 606) |
|---|---|---|
| Framework | Mô hình 5 bước | Mô hình 5 bước (hội tụ) |
| Reversals of revenue | Cho phép khi highly probable | Cho phép khi probable |
| Industry guidance | Ít chi tiết hơn | Chi tiết hơn (ASC subtopics) |

## See Also

- [[financial-statement-analysis/concepts/expense-recognition|Expense Recognition]]
- [[financial-statement-analysis/concepts/financial-statements-overview|Financial Statements Overview]]
- [[financial-statement-analysis/concepts/ifrs-vs-gaap|IFRS vs GAAP Differences]]
- [[financial-statement-analysis/glossary/fsa-m02-income-statements|Income Statement Glossary]]