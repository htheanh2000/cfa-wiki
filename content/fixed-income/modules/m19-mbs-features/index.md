---
title: "M19 — Credit Analysis"
type: module
subject: fixed-income
module: M19
los: "19.a–19.d"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M19
  - MBS
  - RMBS
  - CMBS
  - CMO
  - prepayment-risk
  - mortgage
---

# M19 – MBS Features

> **LOS 19.a**: Mô tả các đặc điểm của khoản vay thế chấp nhà ở
> **LOS 19.b**: Mô tả các loại chứng khoán thế chấp nhà ở (residential mortgage-backed securities)
> **LOS 19.c**: Mô tả prepayment risk và cấu trúc CMO
> **LOS 19.d**: Mô tả các đặc điểm của chứng khoán thế chấp thương mại (commercial mortgage-backed securities)

---

## 1. Residential Mortgage Loans

### 1.1 Các Đặc Điểm Chính

| Đặc điểm | Mô tả |
|---------|-------------|
| **Loan-to-Value (LTV)** | $\text{LTV} = \frac{\text{Mortgage Amount}}{\text{Property Value}}$ — LTV càng cao = rủi ro tín dụng càng lớn |
| **Fixed rate** | Lãi suất cố định trong suốt thời hạn khoản vay |
| **Adjustable rate (ARM)** | Lãi suất được điều chỉnh định kỳ dựa trên lãi suất tham chiếu + spread |
| **Recourse** | Người cho vay có thể truy đòi các tài sản khác của người vay ngoài bất động sản |
| **Non-recourse** | Quyền đòi nợ của người cho vay chỉ giới hạn ở chính bất động sản thế chấp |
| **Interest-only** | Người vay chỉ trả lãi trong giai đoạn đầu; gốc được hoãn lại |
| **Prepayment** | Người vay có thể trả gốc trước hạn (tạo ra prepayment risk) |

### 1.2 Tỷ Lệ Loan-to-Value

$$
\text{LTV} = \frac{\text{Mortgage Amount}}{\text{Property Value}}
$$

trong đó:
- LTV > 80% thường yêu cầu **bảo hiểm thế chấp tư nhân (private mortgage insurance — PMI)**
- LTV thấp hơn = vốn chủ sở hữu đệm nhiều hơn = rủi ro tín dụng thấp hơn cho người cho vay

---

## 2. Prepayment Risk

Prepayment risk có hai thành phần:

### 2.1 Contraction Risk

- Xảy ra khi lãi suất **giảm**
- Người vay **tái cấp vốn (refinance)** ở mức lãi suất thấp hơn → trả nợ trước hạn nhanh hơn
- Nhà đầu tư nhận lại gốc **sớm hơn** dự kiến
- Phải tái đầu tư ở mức lãi suất **thấp hơn** hiện hành (reinvestment risk)

### 2.2 Extension Risk

- Xảy ra khi lãi suất **tăng**
- Người vay **không có động lực** tái cấp vốn → trả nợ trước hạn chậm hơn
- Vốn của nhà đầu tư bị **giam giữ lâu hơn** dự kiến
- Effective duration của trái phiếu **tăng**, khiến nó nhạy cảm hơn với các thay đổi lãi suất tiếp theo

| Kịch bản | Tốc độ trả trước hạn | Loại rủi ro | Tác động đến nhà đầu tư |
|----------|-----------------|-----------|-----------------|
| Lãi suất giảm | Nhanh hơn | **Contraction** | Nhận gốc sớm, phải tái đầu tư ở lãi suất thấp hơn |
| Lãi suất tăng | Chậm hơn | **Extension** | Vốn bị giam giữ lâu hơn, duration tăng |

---

## 3. Agency RMBS

**Agency RMBS** được bảo lãnh bởi chính phủ hoặc tổ chức được chính phủ bảo trợ chống lại **default risk** (nhưng KHÔNG bảo lãnh prepayment risk):

| Cơ quan | Loại | Bảo lãnh |
|--------|------|-----------|
| **Ginnie Mae** (GNMA) | Cơ quan chính phủ | Tín nhiệm đầy đủ của chính phủ Hoa Kỳ |
| **Fannie Mae** (FNMA) | Doanh nghiệp được chính phủ bảo trợ (GSE) | Bảo lãnh ngầm của chính phủ |
| **Freddie Mac** (FHLMC) | Doanh nghiệp được chính phủ bảo trợ (GSE) | Bảo lãnh ngầm của chính phủ |

> Agency RMBS về cơ bản **không có rủi ro tín dụng** nhưng vẫn chịu **prepayment risk**.

---

## 4. Mortgage Pass-Through Securities

**Pass-through** là hình thức RMBS đơn giản nhất:

- Tập hợp các khoản thế chấp được đóng gói thành một chứng khoán duy nhất
- Dòng tiền (gốc + lãi − phí dịch vụ) được **chuyển qua (passed through)** cho nhà đầu tư trên cơ sở **pro-rata**
- Tất cả nhà đầu tư cùng chia sẻ **prepayment risk** như nhau

$$
\text{Pass-Through Rate} = \text{Weighted Average Coupon} - \text{Servicing Fee}
$$

Đặc điểm chính:
- Dòng tiền hàng tháng bao gồm **gốc theo lịch**, **lãi**, và **các khoản trả trước**
- Prepayment risk không được phân phối lại — tất cả nhà đầu tư cùng chịu như nhau

---

## 5. CMOs (Collateralized Mortgage Obligations)

CMO **phân phối lại** dòng tiền từ mortgage pass-through thành các **tranche** với các hồ sơ prepayment risk khác nhau.

### 5.1 Sequential-Pay Tranches

- Các khoản thanh toán gốc đi đến **Tranche A trước**, sau đó đến Tranche B, rồi Tranche C, v.v.
- Mỗi tranche có **effective maturity** và duration khác nhau
- Các tranche ngắn hơn chịu nhiều **contraction risk** hơn; các tranche dài hơn chịu nhiều **extension risk** hơn

```
Mortgage Pool Cash Flows
         │
    Principal payments
         │
         ▼
   ┌───────────┐
   │ Tranche A  │ ← Nhận TOÀN BỘ gốc trước tiên (kỳ đáo hạn ngắn nhất)
   └─────┬─────┘
         ▼
   ┌───────────┐
   │ Tranche B  │ ← Nhận gốc sau khi A đã tất toán
   └─────┬─────┘
         ▼
   ┌───────────┐
   │ Tranche C  │ ← Nhận gốc cuối cùng (kỳ đáo hạn dài nhất)
   └───────────┘
```

### 5.2 PAC Tranches (Planned Amortization Class)

PAC tranche cung cấp dòng tiền **có thể dự đoán hơn**:

| Loại tranche | Prepayment Risk | Khả năng dự đoán dòng tiền |
|-------------|-----------------|-------------------------|
| **PAC tranche** | **Thấp** — dòng tiền tuân theo lịch đã lên kế hoạch trong một dải prepayment | **Cao** — các khoản thanh toán gốc có thể dự đoán miễn là tốc độ trả trước nằm trong dải |
| **Support tranche** (companion) | **Cao** — hấp thụ phần dư thừa hoặc thiếu hụt trong các khoản trả trước | **Thấp** — dòng tiền biến động mạnh |

- PAC tranche có một **prepayment collar** (giới hạn trên và dưới)
- Trong phạm vi collar, PAC nhận các khoản thanh toán gốc theo lịch
- **Support tranche** hấp thụ các sai lệch — chúng gánh chịu cả contraction risk và extension risk để bảo vệ PAC

> PAC tranche có **yield thấp hơn** support tranche, phản ánh dòng tiền có thể dự đoán hơn của chúng.

---

## 6. Non-Agency RMBS

| Đặc điểm | Mô tả |
|---------|-------------|
| **Tổ chức phát hành** | Nhãn riêng tư (ngân hàng, tổ chức tài chính) — KHÔNG được chính phủ bảo lãnh |
| **Bảo lãnh chính phủ** | **Không có** — nhà đầu tư chịu rủi ro tín dụng |
| **Tăng cường tín dụng (credit enhancement)** | Bắt buộc — subordination, overcollateralization, excess spread, bảo hiểm thế chấp |
| **Tài sản đảm bảo** | Thường là các khoản vay không đủ tiêu chuẩn (jumbo, subprime, Alt-A) không đáp ứng tiêu chuẩn của agency |

> Non-agency RMBS cung cấp **yield cao hơn** để bù đắp rủi ro tín dụng, nhưng mang rủi ro đáng kể hơn nhiều so với agency RMBS.

---

## 7. Commercial MBS (CMBS)

CMBS được đảm bảo bởi các khoản vay **bất động sản thương mại** (văn phòng, bán lẻ, công nghiệp, chung cư, khách sạn).

### 7.1 Các Đặc Điểm Chính

| Đặc điểm | Mô tả |
|---------|-------------|
| **Non-recourse** | Quyền đòi nợ của người cho vay chỉ giới hạn ở bất động sản thương mại — không truy đòi các tài sản khác của người vay |
| **Balloon payments** | Các khoản vay thường yêu cầu một **khoản thanh toán gốc một lần lớn** khi đáo hạn |
| **Balloon risk** | Rủi ro người vay không thể tái cấp vốn hoặc bán bất động sản để thực hiện khoản thanh toán balloon |
| **Cấu trúc khoản vay** | Thường chỉ trả lãi hoặc khấu hao một phần với khoản thanh toán balloon |

### 7.2 Call Protection

CMBS có các cơ chế **call protection mạnh** để giảm prepayment risk:

| Loại bảo vệ | Mô tả |
|----------------|-------------|
| **Lockout period** | Người vay **bị cấm** trả trước trong một thời gian nhất định (ví dụ: 2–5 năm) |
| **Defeasance** | Người vay thay thế tài sản đảm bảo của khoản vay bằng danh mục **chứng khoán chính phủ** tái tạo các dòng tiền còn lại — khoản vay vẫn còn hiệu lực |
| **Prepayment penalty** | Người vay phải trả **phí phạt** (ví dụ: phần trăm số dư còn lại) để trả trước hạn |
| **Yield maintenance** | Người vay trả một khoản phạt được thiết kế để bảo đảm người cho vay **không bị thiệt** — bù đắp thu nhập lãi bị mất do trả trước hạn |

> Nhà đầu tư CMBS đối mặt với **prepayment risk thấp hơn** so với nhà đầu tư RMBS nhờ các tính năng call protection mạnh này, nhưng đối mặt với **rủi ro tín dụng cao hơn** (rủi ro tập trung vào bất động sản, balloon risk).

### 7.3 So Sánh CMBS và RMBS

| Đặc điểm | RMBS | CMBS |
|---------|------|------|
| Tài sản đảm bảo | Thế chấp nhà ở | Thế chấp thương mại |
| Recourse | Recourse hoặc non-recourse | Thường là **non-recourse** |
| Prepayment risk | Đáng kể | Thấp hơn (call protection) |
| Rủi ro tín dụng | Thấp (agency) hoặc trung bình (non-agency) | Cao hơn (balloon risk, rủi ro tập trung) |
| Cấu trúc khoản vay | Khấu hao đầy đủ (thông thường) | Thanh toán balloon khi đáo hạn |

---

## See Also

- [[fixed-income/m17-securitization/index|M17 – Securitization]]
- [[fixed-income/m18-abs-features/index|M18 – ABS Features]]
- [[fixed-income/m14-credit-risk/index|M14 – Credit Risk]]
- [[fixed-income/m11-duration-measures/index|M11 – Duration Measures]]