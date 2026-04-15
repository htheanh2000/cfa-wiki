---
title: Interest Rate Risk and Return
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [interest-rate-risk, reinvestment-risk, market-price-risk, duration-gap, immunization]
---

# Interest Rate Risk and Return

## Hai Thành Phần của Rủi Ro Lãi Suất

### 1. Market Price Risk
- Giá trái phiếu **giảm** khi lãi suất **tăng**
- Ảnh hưởng đến nhà đầu tư có thể bán trước khi đáo hạn
- Tác động lớn hơn đối với trái phiếu có **duration dài hơn**

### 2. Reinvestment Risk
- Các khoản coupon có thể được tái đầu tư ở **mức lãi suất thấp hơn** khi lãi suất giảm
- Làm giảm tổng lợi nhuận từ việc tái đầu tư coupon
- Tác động lớn hơn đối với trái phiếu có **coupon rate cao hơn** và **kỳ hạn dài hơn**

> Hai rủi ro này hoạt động theo **chiều ngược nhau**: lãi suất tăng gây bất lợi cho giá nhưng có lợi cho tái đầu tư, và ngược lại.

## Ba Nguồn Lợi Nhuận từ Trái Phiếu

1. **Coupon payments**: Lãi định kỳ nhận được
2. **Reinvestment income**: Lãi kiếm được từ việc tái đầu tư các khoản coupon
3. **Capital gain/loss**: Chênh lệch giữa giá mua và giá bán/mệnh giá

Tổng lợi nhuận phụ thuộc vào thời hạn đầu tư và diễn biến lãi suất.

## Duration Gap

**Duration gap** là chênh lệch giữa Macaulay duration của trái phiếu và thời hạn đầu tư của nhà đầu tư.

$$\text{Duration Gap} = \text{Macaulay Duration} - \text{Investment Horizon}$$

### Tác Động Khi Lãi Suất Thay Đổi

| Duration Gap | Lãi Suất Tăng | Lãi Suất Giảm |
|-------------|---------------|---------------|
| **Dương** (MacDur > Horizon) | Market price risk chiếm ưu thế → lợi nhuận **thấp hơn** | Market price risk chiếm ưu thế → lợi nhuận **cao hơn** |
| **Âm** (MacDur < Horizon) | Reinvestment risk chiếm ưu thế → lợi nhuận **cao hơn** | Reinvestment risk chiếm ưu thế → lợi nhuận **thấp hơn** |
| **Bằng 0** (MacDur = Horizon) | Hai rủi ro triệt tiêu nhau → lợi nhuận ≈ YTM | Hai rủi ro triệt tiêu nhau → lợi nhuận ≈ YTM |

## Immunization

**Immunization** là chiến lược khớp Macaulay duration của danh mục trái phiếu với thời hạn đầu tư, để lợi nhuận danh mục được **cố định** ở mức YTM ban đầu bất kể lãi suất thay đổi như thế nào.

### Điều Kiện cho Classical Immunization
1. **Macaulay duration = Investment horizon**
2. **Giá trị danh mục** ≥ Giá trị hiện tại của khoản nợ
3. **Dịch chuyển song song đơn** trên đường cong lãi suất (giả định đơn giản hóa)

### Hạn Chế của Classical Immunization
- Chỉ hiệu quả với các dịch chuyển **song song** trên đường cong lãi suất
- Cần **tái cân bằng** khi duration thay đổi theo thời gian
- Duration thay đổi khi:
  - Thời gian trôi qua (duration "trôi dạt")
  - Lãi suất thay đổi
  - Các khoản coupon được nhận

### Cash Flow Matching
Một phương án thay thế cho immunization:
- Mua các trái phiếu có dòng tiền **khớp chính xác** với các khoản thanh toán nợ
- Không cần tái cân bằng
- Hạn chế hơn và có thể tốn kém hơn so với immunization

## Realized Return vs. YTM

**Realized return** trong suốt thời hạn đầu tư phụ thuộc vào:

1. Tỷ lệ tái đầu tư của các khoản coupon
2. Giá bán trái phiếu (nếu bán trước khi đáo hạn)

$$\text{Realized Return} = \left(\frac{\text{Total Future Value}}{\text{Purchase Price}}\right)^{1/n} - 1$$

- Nếu tỷ lệ tái đầu tư = YTM và giữ trái phiếu đến đáo hạn → Realized return = YTM
- Trong thực tế, tỷ lệ tái đầu tư thay đổi → Realized return ≠ YTM

## Structural Risk

Ngay cả khi duration tổng thể của danh mục khớp với thời hạn đầu tư, danh mục vẫn có thể chịu tác động từ các dịch chuyển **không song song** trên đường cong lãi suất:

- **Bullet portfolio**: Dòng tiền tập trung quanh thời hạn đầu tư → rủi ro cấu trúc thấp hơn
- **Barbell portfolio**: Dòng tiền ở các kỳ hạn ngắn và dài → rủi ro cấu trúc cao hơn
- **Ladder portfolio**: Dòng tiền trải đều → rủi ro cấu trúc trung bình

Bullet portfolio miễn dịch tốt hơn trước các dịch chuyển không song song vì nó có **độ phân tán dòng tiền thấp hơn** (convexity thấp hơn).

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/duration|Duration]]
- [[fixed-income/concepts/convexity|Convexity]]
- [[fixed-income/concepts/term-structure|Term Structure]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m10|Glossary: Module 10]]