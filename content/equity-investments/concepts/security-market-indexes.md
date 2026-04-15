---
title: Security Market Indexes
type: concept
subject: equity-investments
module: M02
los: ["2.a", "2.b", "2.c", "2.d", "2.e"]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, indexes, weighting-methods, rebalancing]
---

# Security Market Indexes

## Định nghĩa

**Security market index** là thước đo giá trị của một nhóm chứng khoán cụ thể (gọi là **constituent securities**). Giá trị chỉ số được tính từ giá (hoặc tỷ suất sinh lợi) của các chứng khoán thành phần.

## Price Return vs Total Return

**Price Return Index** — phản ánh chỉ biến động giá:

$$R_{PI} = \frac{V_1 - V_0}{V_0}$$

**Total Return Index** — bao gồm cả biến động giá VÀ thu nhập (cổ tức, lãi coupon):

$$R_{TRI} = \frac{V_1 - V_0 + \text{Income}}{V_0}$$

trong đó:
- $V_1$ = giá trị chỉ số cuối kỳ
- $V_0$ = giá trị chỉ số đầu kỳ
- $\text{Income}$ = cổ tức hoặc lãi nhận được trong kỳ

Theo thời gian, total return index luôn $\geq$ price return index (giả sử thu nhập dương).

## Weighting Methods

### Price-Weighted Index

$$I = \frac{\sum_{i=1}^{N} P_i}{D}$$

trong đó:
- $P_i$ = giá của cổ phiếu $i$
- $D$ = divisor (được điều chỉnh khi có stock split, thay đổi thành phần)
- $N$ = số lượng chứng khoán thành phần

- Cổ phiếu có giá cao hơn có ảnh hưởng lớn hơn
- Đơn giản để tính toán
- Thiên lệch: stock split làm giảm trọng số của cổ phiếu đó (mang tính tuỳ tiện)
- Ví dụ: DJIA, Nikkei 225

### Equal-Weighted Index

Mỗi chứng khoán thành phần có trọng số bằng nhau $w_i = \frac{1}{N}$

$$R_{EW} = \frac{1}{N}\sum_{i=1}^{N} R_i$$

- Trung bình đơn giản của tất cả tỷ suất sinh lợi
- Cần **rebalancing** thường xuyên (đưa về trọng số bằng nhau)
- Thiên lệch về small-cap (cổ phiếu nhỏ có trọng số bằng cổ phiếu lớn)

### Market-Capitalization-Weighted Index

$$w_i = \frac{P_i \times Q_i}{\sum_{j=1}^{N} P_j \times Q_j}$$

trong đó:
- $P_i$ = giá của cổ phiếu $i$
- $Q_i$ = số lượng cổ phiếu đang lưu hành của cổ phiếu $i$

- Phản ánh danh mục tổng hợp của thị trường
- Không cần rebalancing khi giá thay đổi (tự điều chỉnh)
- Thiên lệch momentum: cổ phiếu tăng giá được tăng trọng số
- Ví dụ: S&P 500, FTSE 100

### Float-Adjusted Market-Cap-Weighted

$$w_i = \frac{P_i \times f_i \times Q_i}{\sum_{j=1}^{N} P_j \times f_j \times Q_j}$$

trong đó $f_i$ = tỷ lệ cổ phiếu có thể giao dịch công khai (float factor, $0 < f_i \leq 1$)

- Loại trừ cổ phiếu nắm giữ bởi insiders, chính phủ, cổ đông chiến lược
- Phản ánh tốt hơn thị trường có thể đầu tư được
- Ví dụ: S&P 500 (từ năm 2005), các chỉ số MSCI

### Fundamental-Weighted Index

Trọng số dựa trên các chỉ số cơ bản:
- Giá trị sổ sách, lợi nhuận, cổ tức, dòng tiền, doanh thu, hoặc chỉ số tổng hợp
- Thiên về value: tăng trọng số cổ phiếu "rẻ" (book value cao so với giá)
- Hiệu ứng contrarian: khi rebalancing sẽ mua cổ phiếu đã giảm, bán cổ phiếu đã tăng
- Ví dụ: FTSE RAFI indexes

## Rebalancing và Reconstitution

### Rebalancing
- Điều chỉnh trọng số các chứng khoán thành phần về mức mục tiêu
- Cần thiết với: equal-weighted (thường xuyên), fundamental-weighted (định kỳ)
- KHÔNG cần thiết với: market-cap-weighted (tự điều chỉnh)
- Phát sinh chi phí giao dịch

### Reconstitution
- Thay đổi danh sách chứng khoán trong chỉ số
- Dựa trên tiêu chí lựa chọn (vốn hoá thị trường, thanh khoản, ngành)
- Tần suất: hàng quý, nửa năm, hoặc hàng năm
- Tạo ra **reconstitution effect**: cổ phiếu được thêm vào thấy giá tăng; cổ phiếu bị loại ra thấy giá giảm

## Công dụng của Market Indexes

1. **Gauging market sentiment** — xác định xu hướng chung của thị trường
2. **Benchmarking** — đánh giá hiệu quả hoạt động của nhà quản lý danh mục
3. **Đo lường tỷ suất sinh lợi điều chỉnh rủi ro** — Sharpe ratio, alpha, beta
4. **Asset allocation** — đại diện cho tỷ suất sinh lợi của từng lớp tài sản
5. **Đầu tư thụ động** — index funds và ETFs tái tạo theo chỉ số
6. **Nghiên cứu** — các nghiên cứu học thuật về hành vi thị trường

## Các loại Indexes

| Loại | Mô tả |
|------|------------|
| Broad market | Đại diện cho toàn bộ thị trường (ví dụ: Wilshire 5000) |
| Multi-market | Trải rộng nhiều quốc gia (ví dụ: MSCI World) |
| Sector | Ngành cụ thể (ví dụ: S&P 500 Health Care) |
| Style | Growth so với value (ví dụ: Russell 1000 Growth) |
| Fixed-income | Chỉ số trái phiếu (ví dụ: Bloomberg Aggregate) |
| Alternative | Hàng hoá, bất động sản, quỹ phòng hộ |

## Trang liên quan

- [[equity-investments/concepts/market-organization|Market Organization and Structure]]
- [[equity-investments/concepts/market-efficiency|Market Efficiency]]
- [[equity-investments/practice/cfai/equity-m02-security-market-indexes|CFAI Practice: M02]]