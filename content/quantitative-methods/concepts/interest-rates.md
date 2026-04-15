---
title: "Interest Rates"
type: concept
subject: quantitative-methods
created: 2026-04-09
updated: 2026-04-09
tags: [interest-rate, discount-rate, opportunity-cost, required-return, risk-free-rate]
---

# Interest Rates

## Định nghĩa

**Interest rate** là khoản bù đắp mà người cho vay (hoặc nhà đầu tư) yêu cầu cho việc sử dụng vốn trong một khoảng thời gian. Trong tài chính, interest rate có ba cách diễn giải tương đương nhau tùy theo ngữ cảnh.

## Ba Cách Diễn Giải

| Cách diễn giải | Mô tả |
|----------------|-------------|
| **Discount rate** | Tỷ lệ dùng để tính present value của các dòng tiền tương lai; tỷ lệ càng cao thì dòng tiền tương lai càng ít giá trị ở hiện tại |
| **Opportunity cost** | Khoản lợi nhuận bị bỏ qua khi chọn một khoản đầu tư thay vì lựa chọn tốt nhất tiếp theo |
| **Required rate of return** | Mức lợi nhuận tối thiểu mà nhà đầu tư phải nhận được để chấp nhận chịu đựng rủi ro của một khoản đầu tư |

## Các Thành Phần của Required Rate of Return

$$
r = r_{f,\text{real}} + \text{Inflation Premium} + \text{Default Risk Premium} + \text{Liquidity Premium} + \text{Maturity Premium}
$$

| Thành phần | Mô tả |
|-----------|-------------|
| Real risk-free rate ($r_{f,\text{real}}$) | Lợi nhuận yêu cầu cho khoản đầu tư không có rủi ro và không có lạm phát |
| Inflation premium | Bù đắp cho sự sụt giảm dự kiến của sức mua |
| Default risk premium | Bù đắp cho rủi ro người vay không trả được nợ |
| Liquidity premium | Bù đắp cho việc không thể bán nhanh tài sản ở mức giá hợp lý |
| Maturity premium | Bù đắp cho độ nhạy cảm với sự thay đổi interest rate theo thời gian |

## Các Khái Niệm Liên Quan

- [[quantitative-methods/concepts/time-value-of-money|Time Value of Money]] — interest rate là cơ chế mà qua đó các phép tính TVM chiết khấu hoặc tích lũy dòng tiền
- Nominal rate và real rate: $(1 + r_{\text{nominal}}) = (1 + r_{\text{real}})(1 + \text{inflation})$

## Các Module Nguồn

- [[quantitative-methods/modules/m01-rates-and-returns/index|M01 — Rates and Returns]] — nội dung chính về các cách diễn giải interest rate và đo lường lợi nhuận
- [[quantitative-methods/modules/m02-time-value-of-money/index|M02 — Time Value of Money]] — ứng dụng interest rate vào chiết khấu và tích lũy