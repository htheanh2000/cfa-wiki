---
title: "M17 — Securitization"
type: module
subject: fixed-income
module: M17
los: "17.a–17.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M17
  - securitization
  - ABS
  - SPE
  - structured-finance
---

# M17 – Securitization

> **LOS 17.a**: Mô tả các lợi ích và rủi ro của securitization
> **LOS 17.b**: Mô tả quy trình securitization, các bên liên quan, và vai trò của SPE

---

## 1. Lợi ích của Securitization

### 1.1 Lợi ích cho Issuer (Originator)

| Lợi ích | Mô tả |
|---------|-------------|
| **Mở rộng hoạt động kinh doanh** | Giải phóng vốn để phát hành thêm các khoản vay mới |
| **Cải thiện lợi nhuận** | Kiếm phí origination và servicing mà không cần giữ tài sản trên bảng cân đối kế toán |
| **Giảm yêu cầu dự trữ vốn** | Loại bỏ tài sản khỏi bảng cân đối kế toán giúp giảm yêu cầu vốn theo quy định |
| **Tăng thanh khoản** | Chuyển đổi tài sản kém thanh khoản (các khoản vay) thành chứng khoán có thể giao dịch |

### 1.2 Lợi ích cho Nhà đầu tư

| Lợi ích | Mô tả |
|---------|-------------|
| **Tùy chỉnh risk/return** | Tranching cho phép nhà đầu tư lựa chọn mức độ rủi ro phù hợp |
| **Khả năng tiếp cận** | Tiếp xúc với các loại tài sản khó đầu tư trực tiếp (ví dụ: cho vay mua ô tô, các khoản phải thu từ thẻ tín dụng) |
| **Thanh khoản** | ABS thường có thanh khoản cao hơn so với các pool khoản vay cơ sở |

### 1.3 Lợi ích cho Nền kinh tế

| Lợi ích | Mô tả |
|---------|-------------|
| **Giảm chi phí vốn** | Securitization có thể giảm chi phí vay vốn cho người đi vay cuối cùng |
| **Cải thiện thanh khoản** | Phân bổ vốn hiệu quả hơn trong toàn hệ thống tài chính |
| **Đa dạng hóa** | Rủi ro được phân tán cho nhiều nhà đầu tư thay vì tập trung trên bảng cân đối kế toán của các ngân hàng |

---

## 2. Rủi ro của Securitization

### 2.1 Thời điểm Nhận Dòng Tiền

Thời điểm nhận dòng tiền không chắc chắn vì người vay có thể **trả nợ trước hạn (prepay)** hoặc **vỡ nợ (default)**:

| Rủi ro | Mô tả |
|------|-------------|
| **Contraction risk** | Người vay trả nợ trước hạn nhanh hơn dự kiến (ví dụ: khi lãi suất giảm) → nhà đầu tư nhận gốc sớm, phải tái đầu tư ở mức lãi suất thấp hơn |
| **Extension risk** | Người vay trả nợ trước hạn chậm hơn dự kiến (ví dụ: khi lãi suất tăng) → vốn của nhà đầu tư bị khóa lâu hơn dự kiến |

### 2.2 Rủi ro Tín dụng Nội tại

- Pool tài sản đảm bảo cơ sở có **rủi ro vỡ nợ (default risk)**
- Credit enhancement giúp giảm thiểu nhưng không loại bỏ hoàn toàn rủi ro này
- Correlation risk: suy thoái kinh tế có thể gây ra **vỡ nợ đồng thời** trên toàn pool

---

## 3. Quy trình Securitization

Dòng chảy cơ bản của securitization:

```
Originator → bán tài sản → SPE (Issuer/Trust) → phát hành ABS → Nhà đầu tư
                                    ↑
                              Tiền mặt thu về
                                    ↓
                              Originator nhận được nguồn tài trợ
```

### Các bước thực hiện

1. **Originator** tổng hợp các tài sản tài chính (thế chấp bất động sản, cho vay mua ô tô, các khoản phải thu từ thẻ tín dụng)
2. Originator **bán** (true sale) pool tài sản cho **SPE**
3. SPE **phát hành** asset-backed securities cho nhà đầu tư
4. Dòng tiền từ các tài sản cơ sở được dùng để thanh toán cho nhà đầu tư ABS
5. **Servicer** thu các khoản thanh toán từ người vay và chuyển đến SPE

---

## 4. Các Bên Liên quan

### 4.1 Các Bên Chính

| Bên | Vai trò |
|-------|------|
| **Originator / Seller** | Tạo ra các khoản vay, bán chúng cho SPE |
| **Issuer / Trust (SPE)** | Special Purpose Entity nắm giữ tài sản và phát hành chứng khoán |
| **Servicer** | Thu các khoản thanh toán từ người vay, xử lý các khoản nợ quá hạn; thường chính là originator |

### 4.2 Các Bên Thứ Ba

| Bên | Vai trò |
|-------|------|
| **Accountants** | Kiểm toán báo cáo tài chính của SPE |
| **Lawyers** | Cấu trúc giao dịch, đảm bảo true sale và bankruptcy remoteness |
| **Trustees** | Đại diện cho lợi ích của nhà đầu tư, đảm bảo tuân thủ thỏa thuận tín thác |
| **Underwriters** | Tiếp thị và phân phối ABS đến nhà đầu tư |
| **Rating agencies** | Đánh giá chất lượng tín dụng của từng tranche |

---

## 5. Vai trò Cốt lõi của SPE

**Special Purpose Entity (SPE)** là nền tảng của securitization:

### 5.1 Bankruptcy Remoteness

- SPE là một thực thể **độc lập về mặt pháp lý** so với originator
- Nếu originator phá sản, tài sản của SPE **không** thuộc về khối tài sản phá sản
- Cấu trúc **true sale** này đảm bảo nhà đầu tư ABS được bảo vệ khỏi rủi ro tín dụng của originator

### 5.2 Ảnh hưởng đến Xếp hạng Tín dụng

Nhờ bankruptcy remoteness:

$$
\text{ABS credit rating} \geq \text{Originator credit rating}
$$

- ABS có thể đạt được **xếp hạng tín dụng cao hơn** so với originator
- Xếp hạng dựa trên **chất lượng của pool tài sản đảm bảo** và **credit enhancements**, không phải mức tín nhiệm của originator
- Đây là lợi thế then chốt — cho phép các originator có xếp hạng thấp hơn tiếp cận nguồn vốn rẻ hơn

---

## See Also

- [[fixed-income/m18-abs-features/index|M18 – ABS Features]]
- [[fixed-income/m19-mbs-features/index|M19 – MBS Features]]
- [[fixed-income/m14-credit-risk/index|M14 – Credit Risk]]