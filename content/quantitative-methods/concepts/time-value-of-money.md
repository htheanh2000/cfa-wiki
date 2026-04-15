---
title: "Time Value of Money"
type: concept
subject: quantitative-methods
created: 2026-04-09
updated: 2026-04-09
tags: [TVM, present-value, future-value, annuity, perpetuity, compounding, discounting]
---

# Time Value of Money (TVM)

## Nguyên Lý Cốt Lõi

Một đồng nhận được ngày hôm nay có giá trị hơn một đồng nhận được trong tương lai vì tiền sẵn có ngày nay có thể được đầu tư để tạo ra lợi nhuận. Đây chính là **time value of money**.

TVM là khái niệm nền tảng của toàn bộ tài chính — từ định giá trái phiếu và định giá cổ phần đến lập ngân sách vốn và phái sinh.

## Các Thành Phần Chính

| Khái niệm | Mô tả |
|---------|-------------|
| **Present Value (PV)** | Giá trị tương đương ngày hôm nay của một dòng tiền tương lai, được chiết khấu theo tỷ lệ r |
| **Future Value (FV)** | Giá trị của một khoản tiền hiện tại sau khi tích lũy lợi nhuận theo thời gian |
| **Discount rate (r)** | Lãi suất dùng để chuyển đổi dòng tiền tương lai về giá trị hiện tại |
| **Number of periods (N)** | Khoảng thời gian đầu tư |
| **Annuity** | Chuỗi các dòng tiền bằng nhau tại các khoảng thời gian đều đặn |
| **Perpetuity** | Annuity kéo dài mãi mãi |

## Các Mối Quan Hệ Cốt Lõi

$$
FV = PV \times (1 + r)^N \quad \Leftrightarrow \quad PV = \frac{FV}{(1+r)^N}
$$

**Ordinary annuity PV:**
$$
PV = PMT \times \frac{1 - (1+r)^{-N}}{r}
$$

**Perpetuity PV:**
$$
PV = \frac{PMT}{r}
$$

## Tần Suất Ghép Lãi (Compounding Frequency)

Khi lãi được ghép $m$ lần mỗi năm với lãi suất danh nghĩa $r_s$:

$$
FV = PV \times \left(1 + \frac{r_s}{m}\right)^{mN}
$$

**Continuous compounding:**
$$
FV = PV \times e^{r_s \cdot N}
$$

## Liên Hệ với Lãi Suất

Discount rate được áp dụng trong các phép tính TVM bản thân nó là một [[quantitative-methods/concepts/interest-rates|interest rate]] phản ánh lợi suất yêu cầu, bao gồm lãi suất phi rủi ro, lạm phát và các phần bù rủi ro.

## Các Module Liên Quan

- [[quantitative-methods/modules/m02-time-value-of-money/index|M02 — Time Value of Money]] — nội dung chính bao gồm toàn bộ các phép tính TVM
- [[quantitative-methods/modules/m01-rates-and-returns/index|M01 — Rates and Returns]] — lợi suất hàng năm và continuous compounding liên kết trở lại với TVM