---
title: "M08 — Long-Term Liabilities"
type: module
subject: fsa
module: M08
los: [Pre.i, Pre.ii, Pre.iii, Pre.iv, Pre.v, Pre.vi, 8.a, 8.b, 8.c]
created: 2026-04-10
updated: 2026-04-10
tags: [cfa-level-1, fsa, bonds, leases, pensions, leverage, debt-covenants, stock-compensation]
---

# M08: Liabilities and Equity

## Tổng quan

Module này đề cập đến việc ghi nhận và đo lường **bonds**, **leases**, **pensions**, và **stock-based compensation**, cùng với các tỷ số leverage và coverage quan trọng.

---

## 1. Thuật ngữ Bond

| Thuật ngữ | Định nghĩa |
|---|---|
| Face (par) value | Mệnh giá được hoàn trả khi đáo hạn |
| Coupon rate | Lãi suất danh nghĩa áp dụng trên face value |
| Effective (market) interest rate | Lãi suất mà nhà đầu tư yêu cầu tại thời điểm phát hành |
| Carrying (book) value | Giá trị được ghi nhận trên bảng cân đối kế toán |

---

## 2. Phát hành Bond

Mối quan hệ giữa coupon rate và market rate quyết định giá phát hành:

| Điều kiện | Phát hành | BV ban đầu so với Face |
|---|---|---|
| Market rate $=$ Coupon rate | Theo **mệnh giá (par)** | $BV = \text{Face}$ |
| Market rate $<$ Coupon rate | Theo **premium** | $BV > \text{Face}$ |
| Market rate $>$ Coupon rate | Theo **discount** | $BV < \text{Face}$ |

$$\text{Bond Price} = \sum_{t=1}^{n} \frac{C}{(1+r)^t} + \frac{FV}{(1+r)^n}$$

Trong đó $C$ = khoản thanh toán coupon, $r$ = market rate mỗi kỳ, $FV$ = face value, $n$ = số kỳ.

---

## 3. Effective Interest Method

Theo cả IFRS và US GAAP, **effective interest method** được sử dụng để phân bổ:

$$\boxed{\text{Interest Expense} = \text{Carrying Value}_{t-1} \times \text{Market Rate at Issuance}}$$

$$\text{Coupon Payment} = \text{Face Value} \times \text{Coupon Rate}$$

$$\text{Amortization} = \text{Interest Expense} - \text{Coupon Payment}$$

### Premium Bond ($BV > \text{Face}$)

- Interest expense $<$ Coupon payment
- Carrying value **giảm dần** về face value theo thời gian
- Amortization làm giảm premium mỗi kỳ

### Discount Bond ($BV < \text{Face}$)

- Interest expense $>$ Coupon payment
- Carrying value **tăng dần** về face value theo thời gian
- Amortization làm giảm discount mỗi kỳ

### Zero-Coupon Bond

- Không có khoản thanh toán coupon định kỳ; được phát hành với **deep discount**
- Interest expense $=$ Carrying value $\times$ Market rate (toàn bộ được tích lũy, không có tiền mặt thanh toán cho đến khi đáo hạn)
- Toàn bộ lợi tức đến từ sự tăng giá

---

## 4. Chi phí Phát hành (Issuance Costs)

| Chuẩn mực | Xử lý |
|---|---|
| **IFRS** | **Khấu trừ** khỏi carrying value của khoản nợ (làm tăng effective rate) |
| **US GAAP** | Có thể **vốn hóa** như một deferred charge (tài sản) hoặc khấu trừ khỏi khoản nợ |

---

## 5. Xóa ghi nhận Nợ (Derecognition of Debt)

Khi nợ được thanh toán trước hạn:

$$\text{Gain/Loss} = \text{Carrying Value} - \text{Repurchase Price}$$

- Nếu $\text{CV} > \text{Price}$ → **Lãi** khi xóa nợ (Gain on extinguishment)
- Nếu $\text{CV} < \text{Price}$ → **Lỗ** khi xóa nợ (Loss on extinguishment)

---

## 6. Debt Covenants

| Loại | Mô tả | Ví dụ |
|---|---|---|
| **Affirmative** | Các hành động bên vay **phải** thực hiện | Duy trì bảo hiểm, cung cấp báo cáo tài chính đã kiểm toán, duy trì các tỷ số tối thiểu |
| **Negative** | Các hành động bên vay **không được** thực hiện | Hạn chế vay thêm nợ, bán tài sản, thanh toán cổ tức |

> Vi phạm covenant có thể kích hoạt **technical default**, có khả năng đẩy nhanh việc hoàn trả nợ.

---

## 7. Leases

### IFRS 16

**Lessees (bên thuê):** hầu hết **tất cả các leases** đều được ghi nhận trên bảng cân đối kế toán:
- **Right-of-use (ROU) asset** và **Lease liability** theo giá trị hiện tại của các khoản thanh toán thuê
- Depreciation expense trên ROU asset + Interest expense trên lease liability
- Ngoại lệ: short-term leases ($\leq$ 12 tháng) và tài sản có giá trị thấp

**Lessors (bên cho thuê):** phân loại là operating hoặc finance lease (tương tự IAS 17 cũ)

### US GAAP (ASC 842)

**Lessees (bên thuê):** hai loại:

| Loại Lease | Bảng cân đối kế toán | Báo cáo kết quả kinh doanh |
|---|---|---|
| **Finance lease** | ROU asset + Lease liability | Depreciation + Interest (chi phí dồn về đầu kỳ) |
| **Operating lease** | ROU asset + Lease liability | Một khoản **straight-line lease expense** duy nhất |

> Điểm khác biệt chính: IFRS xử lý tất cả lessee leases tương tự nhau (như finance leases); US GAAP phân biệt giữa finance và operating lease trong cách trình bày báo cáo kết quả kinh doanh.

---

## 8. Pensions

### Defined Contribution Plans

- Người sử dụng lao động đóng góp **một khoản cố định** vào tài khoản của người lao động
- **Không có khoản nợ trên bảng cân đối kế toán** ngoài các khoản đóng góp chưa thanh toán
- Rủi ro đầu tư do **người lao động** chịu

### Defined Benefit Plans

- Người sử dụng lao động cam kết một **khoản trợ cấp cụ thể** khi nghỉ hưu
- Bảng cân đối kế toán ghi nhận **net pension asset/liability** = Plan assets $-$ Defined benefit obligation (DBO)
- Rủi ro đầu tư và tuổi thọ do **người sử dụng lao động** chịu

$$\text{Pension Expense (P\&L)} = \text{Service Cost} + \text{Net Interest}$$

$$\text{Remeasurements} \to \text{OCI (IFRS)} \text{ or various (US GAAP)}$$

---

## 9. Stock-Based Compensation

### Stock Options

- Được đo lường theo **fair value** tại ngày cấp (grant date) (ví dụ: mô hình Black-Scholes)
- Chi phí được ghi nhận trong suốt **vesting period**
- Ghi có vào **equity** (additional paid-in capital)

### Restricted Stock

- Cổ phiếu được cấp kèm theo các điều kiện hạn chế (ví dụ: phải tiếp tục làm việc trong $n$ năm)
- Fair value $=$ Giá cổ phiếu tại grant date
- Chi phí được ghi nhận trong suốt **vesting/restriction period**

$$\text{Annual Compensation Expense} = \frac{\text{Fair Value of Award}}{\text{Vesting Period}}$$

---

## 10. Leverage Ratios

| Tỷ số | Công thức | Diễn giải |
|---|---|---|
| Debt-to-Equity | $\dfrac{\text{Total Debt}}{\text{Total Equity}}$ | Đòn bẩy tài chính từ chủ nợ so với chủ sở hữu |
| Debt-to-Assets | $\dfrac{\text{Total Debt}}{\text{Total Assets}}$ | Tỷ lệ tài sản được tài trợ bởi nợ |
| Financial Leverage | $\dfrac{\text{Average Total Assets}}{\text{Average Total Equity}}$ | Hệ số nhân tài sản; giá trị cao hơn = đòn bẩy cao hơn |

---

## 11. Coverage Ratios

| Tỷ số | Công thức | Diễn giải |
|---|---|---|
| Interest Coverage | $\dfrac{\text{EBIT}}{\text{Interest Expense}}$ | Khả năng thanh toán lãi vay từ lợi nhuận hoạt động |
| Fixed Charge Coverage | $\dfrac{\text{EBIT} + \text{Lease Payments}}{\text{Interest Expense} + \text{Lease Payments}}$ | Khả năng thanh toán toàn bộ các nghĩa vụ tài chính cố định |

> Coverage ratios cao hơn cho thấy **rủi ro tín dụng thấp hơn** và khả năng trả nợ lớn hơn.

---

## Các Công thức Chính

| Công thức | Biểu thức |
|---|---|
| Bond price | $\sum \frac{C}{(1+r)^t} + \frac{FV}{(1+r)^n}$ |
| Interest expense | $BV_{t-1} \times r_{\text{market}}$ |
| Amortization | $\text{Interest Expense} - \text{Coupon Payment}$ |
| Gain/loss on retirement | $\text{CV} - \text{Repurchase Price}$ |
| Debt-to-Equity | $\text{Total Debt} \div \text{Total Equity}$ |
| Interest Coverage | $\text{EBIT} \div \text{Interest Expense}$ |

---

## Ghi chú Liên quan

- [[financial-statement-analysis/modules/m07-long-term-assets/index|M07: Long-Term Assets]]
- [[financial-statement-analysis/modules/m04-cash-flows-i/index|M04: Cash Flow Statement (Part I)]]
- [[financial-statement-analysis/modules/m06-inventories/index|M06: Inventories]]