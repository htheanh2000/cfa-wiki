---
title: "M02 — Cash Flows & Types"
type: module
subject: fixed-income
module: M02
los: "2.a–2.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M02
  - cash-flows
  - bond-types
  - embedded-options
---

# M02 – FI Cash Flows and Types

> **Nguồn**: [[fixed-income/sources/sapp-fi-2026|SAPP FI 2026]], tr.40–102
> **LOS**: 2.a – Mô tả các cấu trúc dòng tiền phổ biến của công cụ fixed-income
> **LOS**: 2.b – Mô tả các điều khoản dự phòng (contingency provisions) và hàm ý của chúng

## 1. Cấu trúc hoàn trả vốn gốc (Repayment Structures)

### 1.1 Bullet Bond

- **Toàn bộ vốn gốc** được hoàn trả một lần duy nhất vào ngày đáo hạn
- Thanh toán coupon định kỳ trong suốt vòng đời trái phiếu
- Cấu trúc phổ biến nhất đối với trái phiếu doanh nghiệp và trái phiếu chính phủ

### 1.2 Fully Amortized Bond

- Mỗi khoản thanh toán bao gồm **cả lãi lẫn gốc**
- Vốn gốc được hoàn trả hoàn toàn vào ngày đáo hạn thông qua các khoản thanh toán theo lịch định sẵn
- Ví dụ: khoản vay thế chấp lãi suất cố định

$$PMT = \frac{P \times r}{1 - (1 + r)^{-n}}$$

### 1.3 Partially Amortized Bond (Balloon Payment)

- Các khoản thanh toán định kỳ đã bao gồm một phần vốn gốc được khấu trừ dần
- Một **balloon payment** (khoản tiền lớn một lần) phải được thanh toán vào ngày đáo hạn
- Giảm nhưng không loại bỏ hoàn toàn rủi ro tái tài trợ

### 1.4 Sinking Fund

- Tổ chức phát hành thực hiện **hoàn trả vốn gốc theo lịch định kỳ** theo thời gian
- Giảm rủi ro tín dụng cho nhà đầu tư (vốn gốc còn lại thấp hơn)
- Có thể thực hiện bằng cách mua lại trái phiếu trên thị trường mở hoặc gọi trái phiếu theo mệnh giá

## 2. Cấu trúc Coupon

| Cấu trúc | Mô tả |
|-----------|-------|
| **Fixed-rate** | Lãi suất coupon cố định trong suốt vòng đời trái phiếu |
| **Floating-rate (FRN)** | Coupon = MRR + quoted margin; được đặt lại định kỳ |
| **Step-up coupon** | Lãi suất coupon tăng dần theo lịch được xác định trước |
| **Payment-in-kind (PIK)** | Lãi được trả bằng cách phát hành thêm trái phiếu thay vì tiền mặt |
| **Deferred coupon** | Không có coupon trong giai đoạn đầu, sau đó bắt đầu thanh toán định kỳ |
| **Index-linked** | Coupon và/hoặc vốn gốc gắn với một chỉ số (ví dụ: trái phiếu liên kết lạm phát như TIPS) |

### Floating-Rate Notes (FRN)

$$\text{Coupon}_t = \text{MRR}_t + \text{Quoted Margin (Spread)}$$

- **MRR** (Market Reference Rate): ví dụ SOFR, EURIBOR
- Coupon được đặt lại tại mỗi ngày reset dựa trên MRR hiện hành
- Giá luôn gần với mệnh giá tại mỗi ngày reset (rủi ro lãi suất thấp hơn)

### Index-Linked Bonds

- **Inflation-linked** (ví dụ: TIPS): vốn gốc điều chỉnh theo CPI; coupon = lãi suất cố định $\times$ vốn gốc đã điều chỉnh
- Bảo vệ nhà đầu tư khỏi **rủi ro lạm phát**

## 3. Các điều khoản dự phòng (Contingency Provisions)

### 3.1 Callable Bonds (Lợi ích → Tổ chức phát hành)

- Tổ chức phát hành có **quyền mua lại** trái phiếu trước ngày đáo hạn theo một mức giá call được xác định trước
- Tổ chức phát hành thực hiện quyền này khi lãi suất **giảm** (tái tài trợ với chi phí thấp hơn)
- Nhà đầu tư chịu **rủi ro tái đầu tư**
- Giá callable bond < trái phiếu tương đương không có quyền gọi (nhà đầu tư yêu cầu bù đắp)

$$\text{Value of callable bond} = \text{Value of straight bond} - \text{Value of call option}$$

### 3.2 Putable Bonds (Lợi ích → Nhà đầu tư)

- Nhà đầu tư có **quyền bán lại** trái phiếu cho tổ chức phát hành trước ngày đáo hạn
- Nhà đầu tư thực hiện quyền này khi lãi suất **tăng** (tái đầu tư với lãi suất cao hơn)
- Bảo vệ trước **rủi ro lãi suất**

$$\text{Value of putable bond} = \text{Value of straight bond} + \text{Value of put option}$$

### 3.3 Convertible Bonds (Lợi ích → Nhà đầu tư)

- Nhà đầu tư có thể **chuyển đổi trái phiếu thành cổ phần** (cổ phiếu phổ thông) theo tỷ lệ chuyển đổi được xác định trước
- Mang lại khả năng **tham gia vào tăng trưởng** khi giá cổ phiếu tăng
- Convertible bonds có **lãi suất coupon thấp hơn** so với trái phiếu không có quyền chuyển đổi tương đương

$$\text{Conversion value} = \text{Conversion ratio} \times \text{Market price of stock}$$

## 4. Các yếu tố pháp lý, quy định và thuế

### 4.1 Phân loại trái phiếu theo thị trường

| Loại | Mô tả |
|------|-------|
| **Domestic bond** | Phát hành tại quốc gia của tổ chức phát hành, bằng đồng nội tệ |
| **Foreign bond** | Phát hành tại quốc gia nước ngoài, bằng đồng tiền của quốc gia đó |
| **Eurobond** | Phát hành bằng đồng tiền khác với đồng tiền của quốc gia nơi bán |

### 4.2 Các vấn đề về thuế

- **Original Issue Discount (OID)**: chênh lệch giữa mệnh giá và giá phát hành đối với trái phiếu phát hành dưới mệnh giá; được tính là thu nhập lãi tích lũy trong suốt vòng đời trái phiếu
- **Capital gains vs. interest income**: có thể bị đánh thuế theo các mức khác nhau tùy thuộc vào quy định từng quốc gia
- **Tax-exempt bonds**: một số trái phiếu đô thị (municipal bonds) được miễn thuế liên bang (và đôi khi cả thuế tiểu bang/địa phương)

## Liên quan

- [[fixed-income/m01-instrument-features/index|M01 – FI Instrument Features]]
- [[fixed-income/m03-issuance-and-trading/index|M03 – FI Issuance and Trading]]
- [[fixed-income/m06-bond-valuation/index|M06 – Bond Valuation: Prices and Yields]]