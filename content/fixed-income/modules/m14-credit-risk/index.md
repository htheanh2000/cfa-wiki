---
title: "M14 — Key Rate Duration"
type: module
subject: fixed-income
module: M14
los: "14.a–14.d"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M14
  - credit-risk
  - credit-analysis
  - yield-spreads
  - credit-ratings
---

# M14 – Credit Risk

> **LOS 14.a**: Mô tả credit risk và các thành phần của nó
> **LOS 14.b**: Mô tả các yếu tố ảnh hưởng đến yield spreads
> **LOS 14.c**: Mô tả tác động của sự thay đổi spread lên giá trái phiếu
> **LOS 14.d**: Mô tả credit ratings và rủi ro khi phụ thuộc vào đánh giá của các tổ chức xếp hạng

---

## 1. Các Phương Pháp Phân Tích Tín Dụng

### 1.1 Bottom-Up Analysis

Bottom-up credit analysis đánh giá từng **nhà phát hành riêng lẻ**. Khung phân tích truyền thống sử dụng **8 Cs**:

| Yếu tố | Mô tả |
|--------|-------|
| **Capacity** | Khả năng trả nợ từ dòng tiền |
| **Capital** | Nguồn lực tài chính / vốn đệm |
| **Collateral** | Tài sản thế chấp để đảm bảo khoản nợ |
| **Covenants** | Các điều khoản hợp đồng bảo vệ (affirmative & negative) |
| **Character** | Chất lượng ban lãnh đạo, tính chính trực, lịch sử hoạt động |
| **Conditions** | Môi trường kinh tế / ngành bên ngoài |
| **Country** | Rủi ro chủ quyền / chính trị của quốc gia đặt trụ sở |
| **Currency** | Rủi ro tỷ giá ngoại hối nếu khoản nợ bằng ngoại tệ |

### 1.2 Top-Down Analysis

Top-down analysis bắt đầu từ **môi trường kinh tế vĩ mô** và đi xuống đến cấp ngành và nhà phát hành:

1. Triển vọng toàn cầu / vĩ mô
2. Phân tích ngành
3. Đánh giá cụ thể từng nhà phát hành

---

## 2. Các Thành Phần của Credit Risk

Credit risk là rủi ro **tổn thất** phát sinh khi người đi vay không thực hiện nghĩa vụ thanh toán đã cam kết.

### 2.1 Các Thành Phần Chính

| Thành phần | Định nghĩa |
|-----------|------------|
| **Expected exposure** | Số tiền có nguy cơ rủi ro (vốn gốc còn lại + lãi tích lũy) |
| **Probability of default (POD)** | Xác suất nhà phát hành không thực hiện nghĩa vụ thanh toán |
| **Recovery rate** | Tỷ lệ phần trăm thu hồi được sau khi vỡ nợ |
| **Loss given default (LGD)** | Tỷ lệ phần trăm bị mất sau khi vỡ nợ |

**Loss Given Default**:

$$
\text{LGD} = 1 - \text{Recovery Rate}
$$

### 2.2 Expected Loss

$$
\text{Expected Loss} = \text{POD} \times \text{LGD} \times \text{Exposure}
$$

trong đó:
- $\text{POD}$ = xác suất vỡ nợ
- $\text{LGD}$ = tỷ lệ tổn thất khi vỡ nợ = $1 - \text{Recovery Rate}$
- $\text{Exposure}$ = mức độ rủi ro dự kiến tại thời điểm vỡ nợ

> **Ví dụ**: Nếu POD = 2%, Recovery Rate = 40%, và Exposure = \$1,000,000:
> - LGD = $1 - 0.40 = 0.60$ (60%)
> - Expected Loss = $0.02 \times 0.60 \times 1{,}000{,}000 = \$12{,}000$

---

## 3. Các Yếu Tố Ảnh Hưởng đến Yield Spreads

**Yield spread** (hay credit spread) là chênh lệch giữa yield của một trái phiếu và yield của một benchmark phi rủi ro có kỳ hạn tương đương.

### 3.1 Yếu Tố Kinh Tế Vĩ Mô

- **Chu kỳ kinh doanh**: Spreads **thu hẹp** trong giai đoạn tăng trưởng (rủi ro vỡ nợ thấp hơn) và **mở rộng** trong giai đoạn suy thoái
- **Chính sách tiền tệ**: Thắt chặt chính sách → spreads mở rộng; nới lỏng → spreads thu hẹp

### 3.2 Yếu Tố Thị Trường

- **Tính thanh khoản**: Trái phiếu kém thanh khoản → spreads mở rộng để bù đắp liquidity risk
- **Cung / cầu**: Phát hành mới tăng → spreads mở rộng; nhu cầu nhà đầu tư mạnh → spreads thu hẹp

### 3.3 Yếu Tố Đặc Thù Nhà Phát Hành

- **Kết quả tài chính**: Doanh thu, biên lợi nhuận, dòng tiền suy giảm → spreads mở rộng
- **Đòn bẩy**: Tỷ lệ debt/equity hoặc debt/EBITDA cao hơn → spreads mở rộng
- **Triển vọng ngành**: Rủi ro đặc thù của từng lĩnh vực ảnh hưởng đến mức spread

---

## 4. Tác Động của Sự Thay Đổi Spread lên Giá Trái Phiếu

Khi **credit spread mở rộng**, yield yêu cầu của trái phiếu tăng lên và **giá giảm**. Khi spread **thu hẹp**, giá **tăng**.

Tác động ước tính lên giá khi spread thay đổi:

$$
\Delta P \approx -\text{Duration} \times \Delta \text{Spread} \times P
$$

trong đó:
- $\Delta P$ = sự thay đổi giá trái phiếu
- $\text{Duration}$ = modified hoặc effective duration
- $\Delta \text{Spread}$ = mức thay đổi spread (dạng thập phân)
- $P$ = giá trái phiếu hiện tại

Nhận xét quan trọng: Trái phiếu có **duration cao hơn** sẽ có **độ nhạy cảm về giá lớn hơn** khi spread thay đổi.

| Thay đổi Spread | Tác động lên Giá |
|-----------------|-----------------|
| Spread mở rộng | Giá **giảm** |
| Spread thu hẹp | Giá **tăng** |
| Duration cao + spread thay đổi | Tác động lên giá **lớn hơn** |

---

## 5. Credit Ratings

### 5.1 Các Tổ Chức Xếp Hạng Lớn

| Hạng mục | Moody's | S&P | Fitch |
|----------|---------|-----|-------|
| **Chất lượng cao nhất** | Aaa | AAA | AAA |
| **Chất lượng cao** | Aa1, Aa2, Aa3 | AA+, AA, AA− | AA+, AA, AA− |
| **Trên trung bình** | A1, A2, A3 | A+, A, A− | A+, A, A− |
| **Trung bình** | Baa1, Baa2, Baa3 | BBB+, BBB, BBB− | BBB+, BBB, BBB− |
| **Đầu cơ** | Ba1, Ba2, Ba3 | BB+, BB, BB− | BB+, BB, BB− |
| **Đầu cơ cao** | B1, B2, B3 | B+, B, B− | B+, B, B− |
| **Rủi ro vỡ nợ** | Caa–C | CCC–D | CCC–D |

- **Investment grade**: Baa3 / BBB− trở lên
- **High yield (junk)**: Ba1 / BB+ trở xuống

### 5.2 Issuer Rating vs Issue Rating

| Loại Rating | Còn Gọi Là | Đối Tượng Xếp Hạng |
|-------------|------------|---------------------|
| **Issuer rating** | Corporate Family Rating (CFR) | Mức độ tín nhiệm tổng thể của tổ chức phát hành |
| **Issue rating** | Corporate Credit Rating (CCR) | Nghĩa vụ nợ cụ thể, có tính đến thứ tự ưu tiên và tài sản đảm bảo |

### 5.3 Notching

**Notching** điều chỉnh issue rating so với issuer rating dựa trên:

- **Subordination**: Khoản nợ cấp thấp hơn bị notched **xuống** (rating thấp hơn)
- **Collateral**: Khoản nợ có bảo đảm có thể được notched **lên** (rating cao hơn)
- **Đặc điểm cấu trúc**: Bảo lãnh, covenants

### 5.4 Cross-Default Provisions

**Cross-default provision** quy định rằng việc vỡ nợ đối với **bất kỳ** nghĩa vụ nào cũng sẽ kích hoạt vỡ nợ đối với nghĩa vụ chứa điều khoản này. Điều này bảo vệ trái chủ bằng cách ngăn nhà phát hành vỡ nợ có chọn lọc.

### 5.5 Structural vs Reduced-Form Models

| Mô hình | Cách tiếp cận |
|---------|--------------|
| **Structural models** | Mô hình hóa vỡ nợ dựa trên **bảng cân đối kế toán** của nhà phát hành — vỡ nợ xảy ra khi giá trị tài sản giảm xuống dưới giá trị nợ (mô hình Merton) |
| **Reduced-form models** | Mô hình hóa vỡ nợ như một **quy trình thống kê** — vỡ nợ có thể xảy ra bất kỳ lúc nào với một xác suất nhất định, không gắn với bảng cân đối kế toán |

---

## 6. Rủi Ro Khi Phụ Thuộc vào Đánh Giá của Tổ Chức Xếp Hạng

Agency credit ratings có những **hạn chế** quan trọng:

1. **Phản ánh chậm so với điều kiện kinh tế** — Ratings thường **nhìn về quá khứ** và có thể không phản ánh sự suy giảm hiện tại
2. **Transition risk** — Thay đổi rating có thể xảy ra đột ngột; **transition matrices** thể hiện xác suất lịch sử của sự dịch chuyển rating
3. **Event risk** — Ratings có thể không nắm bắt được các sự kiện bất lợi đột ngột (M&A, kiện tụng, thay đổi quy định)
4. **Mô hình issuer-pays** — Tiềm ẩn xung đột lợi ích vì chính nhà phát hành chi trả cho việc xếp hạng
5. **Phạm vi hạn chế** — Ratings chỉ đánh giá **credit risk**, không bao gồm interest rate risk, liquidity risk, hay market risk

---

## See Also

- [[fixed-income/m15-credit-analysis-government/index|M15 – Credit Analysis: Government]]
- [[fixed-income/m16-credit-analysis-corporate/index|M16 – Credit Analysis: Corporate]]
- [[fixed-income/m07-yield-spread-fixed-rate/index|M07 – Yield & Spread: Fixed Rate]]
- [[fixed-income/concepts/credit-spread|Credit Spread]]