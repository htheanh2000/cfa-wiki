---
title: "M18 — ABS & MBS"
type: module
subject: fixed-income
module: M18
los: "18.a–18.d"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M18
  - ABS
  - covered-bonds
  - credit-enhancement
  - CDO
  - securitization
---

# M18 – ABS Features

> **LOS 18.a**: Mô tả covered bonds
> **LOS 18.b**: Mô tả các loại credit enhancement
> **LOS 18.c**: Mô tả đặc điểm của non-mortgage ABS
> **LOS 18.d**: Mô tả collateralized debt obligations (CDOs)

---

## 1. Covered Bonds

Covered bonds là các nghĩa vụ nợ được đảm bảo bởi một **cover pool** tài sản (thường là thế chấp bất động sản hoặc các khoản vay khu vực công), nhưng có những điểm khác biệt quan trọng so với ABS truyền thống:

| Đặc điểm | Covered Bonds | Traditional ABS |
|---------|---------------|-----------------|
| **Vị trí tài sản** | Tài sản **vẫn nằm trên** bảng cân đối kế toán của tổ chức phát hành | Tài sản được chuyển sang SPE (ngoại bảng) |
| **Quyền truy đòi** | **Dual recourse** — có quyền đòi bồi thường cả từ tổ chức phát hành lẫn cover pool | Chỉ có quyền truy đòi vào tài sản của SPE |
| **Rủi ro trả trước** | **Không có prepayment risk** — tài sản bị trả trước được thay thế trong cover pool | Chịu prepayment risk |
| **Các lớp trái phiếu** | **Một lớp trái phiếu** cho mỗi cover pool | Nhiều tranche |
| **Khi tổ chức phát hành vỡ nợ** | Cover pool được bảo vệ riêng biệt; trái chủ được ưu tiên | SPE được cách ly khỏi rủi ro phá sản |

> Covered bonds đặc biệt phổ biến ở các thị trường **châu Âu** (Pfandbriefe của Đức, trái phiếu thế chấp của Đan Mạch).

---

## 2. Credit Enhancement

Credit enhancement cải thiện chất lượng tín dụng của các tranche ABS, giảm thiểu rủi ro tổn thất cho người nắm giữ senior tranche.

### 2.1 Internal Credit Enhancement

Các phương pháp nội bộ sử dụng **cấu trúc của chính giao dịch**:

| Phương pháp | Mô tả |
|--------|-------------|
| **Subordination / Waterfall** | Tổn thất do các junior tranche gánh chịu trước; senior tranche được bảo vệ. Dòng tiền chảy từ trên xuống (senior → mezzanine → equity) |
| **Overcollateralization** | Giá trị pool tài sản thế chấp **vượt quá** giá trị chứng khoán phát hành — phần dư hấp thụ tổn thất |
| **Excess spread** | Chênh lệch giữa lãi thu được từ tài sản thế chấp và lãi trả cho người nắm giữ ABS — phần dư đóng vai trò vùng đệm đầu tiên chống lại tổn thất |
| **Reserve accounts** | Tiền mặt dành riêng lúc đóng giao dịch để bù đắp các tổn thất hoặc thiếu hụt tiềm ẩn |

**Ví dụ về Subordination (Waterfall)**:

```
Cash Flows from Collateral Pool
         │
         ▼
   ┌─────────────┐
   │ Senior (AAA) │ ← Được thanh toán trước, rủi ro thấp nhất
   └──────┬──────┘
          ▼
   ┌──────────────┐
   │ Mezzanine (A) │ ← Được thanh toán thứ hai
   └──────┬───────┘
          ▼
   ┌──────────────┐
   │ Equity (NR)   │ ← Được thanh toán cuối, gánh chịu tổn thất đầu tiên
   └──────────────┘
```

### 2.2 External Credit Enhancement

Các phương pháp bên ngoài sử dụng **bảo lãnh từ bên thứ ba**:

| Phương pháp | Mô tả |
|--------|-------------|
| **Surety bonds** | Công ty bảo hiểm bảo đảm thanh toán cho nhà đầu tư ABS |
| **Bank guarantees** | Ngân hàng cung cấp bảo lãnh thanh toán đúng hạn |
| **Letters of credit** | Ngân hàng cam kết bù đắp các khoản thiếu hụt đến một mức nhất định |

> External enhancement tạo ra **counterparty risk** — nếu bên bảo lãnh vỡ nợ, sự bảo vệ sẽ mất đi.

---

## 3. Non-Mortgage ABS

### 3.1 Auto Loan ABS

| Đặc điểm | Mô tả |
|---------|-------------|
| **Cấu trúc** | **Amortizing** — gốc và lãi được trả trong suốt vòng đời khoản vay |
| **Prepayment risk** | Có tồn tại nhưng thường **thấp hơn** so với prepayment risk của thế chấp (số dư vay nhỏ hơn, kỳ hạn ngắn hơn) |
| **Credit enhancement** | Subordination, overcollateralization, reserve accounts |
| **Kỳ hạn điển hình** | 3–6 năm |

### 3.2 Credit Card Receivable ABS

| Đặc điểm | Mô tả |
|---------|-------------|
| **Cấu trúc** | **Revolving (non-amortizing)** trong thời gian lockout period |
| **Lockout period** | Trong giai đoạn này, các khoản hoàn trả gốc được **tái đầu tư** vào các khoản phải thu mới — không trả gốc cho nhà đầu tư |
| **Amortization period** | Sau lockout, gốc được hoàn trả cho nhà đầu tư |
| **Prepayment risk** | Tối thiểu trong thời gian lockout; early amortization có thể được kích hoạt khi chất lượng pool suy giảm |

> Điểm khác biệt chính: Auto loan ABS **amortizing** ngay từ đầu; credit card ABS **non-amortizing** trong suốt lockout period.

---

## 4. Collateralized Debt Obligations (CDOs)

**CDO** là sản phẩm có cấu trúc được đảm bảo bởi một **pool đa dạng** các công cụ nợ.

### 4.1 Cấu trúc

| Thành phần | Mô tả |
|-----------|-------------|
| **Collateral pool** | Danh mục trái phiếu, khoản vay, ABS, hoặc các công cụ nợ khác |
| **Tranches** | Senior, mezzanine và equity tranche với các hồ sơ rủi ro/lợi nhuận khác nhau |
| **CDO manager** | **Quản lý chủ động** danh mục tài sản thế chấp (mua/bán tài sản) |

### 4.2 Cấu trúc Tranche

| Tranche | Xếp hạng | Rủi ro | Lợi nhuận | Hấp thụ tổn thất |
|---------|--------|------|--------|-----------------|
| **Senior** | AAA/AA | Thấp nhất | Thấp nhất | Hấp thụ tổn thất cuối cùng |
| **Mezzanine** | A đến BB | Trung bình | Trung bình | Hấp thụ tổn thất sau equity |
| **Equity** | Không xếp hạng | Cao nhất | Cao nhất (phần dư) | **Đầu tiên** hấp thụ tổn thất |

### 4.3 Các loại CDO theo Tài sản thế chấp

| Loại | Tài sản cơ sở |
|------|-------------------|
| **CLO** (Collateralized Loan Obligation) | Các khoản vay ngân hàng có đòn bẩy |
| **CBO** (Collateralized Bond Obligation) | Trái phiếu doanh nghiệp |
| **Structured finance CDO** | ABS, RMBS, CMBS |
| **Synthetic CDO** | Credit default swaps (CDS) |

---

## 5. Time Tranching vs Credit Tranching

| Loại Tranching | Cơ chế | Mục đích |
|----------------|-----------|---------|
| **Credit tranching** | Tổn thất được phân bổ từ dưới lên (equity → mezzanine → senior) | Phân phối lại **credit risk** |
| **Time tranching** | Các khoản thanh toán gốc được phân bổ tuần tự cho các tranche khác nhau | Phân phối lại **prepayment risk** (rủi ro co rút/kéo dài) |

> Trong thực tế, nhiều sản phẩm có cấu trúc sử dụng **cả hai** credit tranching và time tranching đồng thời.

---

## See Also

- [[fixed-income/m17-securitization/index|M17 – Securitization]]
- [[fixed-income/m19-mbs-features/index|M19 – MBS Features]]
- [[fixed-income/m14-credit-risk/index|M14 – Credit Risk]]