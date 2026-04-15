---
title: Equity Valuation Models
type: concept
subject: equity-investments
module: M07
los: ["7.a", "7.b", "7.c", "7.d"]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, valuation, DDM, Gordon-growth, multiples, NAV]
---

# Equity Valuation Models

## Các Nhóm Mô Hình Định Giá

1. **Discounted Cash Flow (DCF)** — Giá trị hiện tại của dòng tiền kỳ vọng trong tương lai
2. **Multiplier (Relative Valuation)** — So sánh các bội số giá với công ty cùng ngành hoặc lịch sử
3. **Asset-Based** — Định giá dựa trên tài sản cơ sở trừ đi nợ phải trả

## Mô Hình Discounted Cash Flow

### General DDM (Dividend Discount Model)

$$V_0 = \sum_{t=1}^{\infty} \frac{D_t}{(1+r)^t}$$

trong đó:
- $V_0$ = giá trị nội tại tại thời điểm hiện tại
- $D_t$ = cổ tức kỳ vọng tại thời điểm $t$
- $r$ = tỷ suất sinh lời yêu cầu trên vốn cổ phần

### Gordon Growth Model (Constant Growth DDM)

Giả định cổ tức tăng trưởng với **tốc độ không đổi** $g$ mãi mãi:

$$V_0 = \frac{D_1}{r - g} = \frac{D_0(1+g)}{r - g}$$

trong đó:
- $D_0$ = cổ tức gần nhất đã trả
- $D_1$ = cổ tức kỳ vọng năm tới = $D_0(1+g)$
- $r$ = tỷ suất sinh lời yêu cầu ($r > g$)
- $g$ = tốc độ tăng trưởng cổ tức không đổi

**Ước tính $g$** (tốc độ tăng trưởng bền vững):

$$g = b \times ROE$$

trong đó:
- $b$ = tỷ lệ giữ lại lợi nhuận (retention ratio) = $1 - \text{payout ratio}$
- $ROE$ = tỷ suất sinh lời trên vốn chủ sở hữu

### Two-Stage DDM

Dành cho các công ty có giai đoạn tăng trưởng cao, sau đó chuyển sang tăng trưởng ổn định:

$$V_0 = \sum_{t=1}^{n} \frac{D_t}{(1+r)^t} + \frac{V_n}{(1+r)^n}$$

trong đó:
- $n$ = độ dài giai đoạn tăng trưởng cao
- $V_n = \frac{D_{n+1}}{r - g_L}$ = giá trị cuối kỳ (Gordon Growth tại tốc độ ổn định $g_L$)

### Quy Tắc Ra Quyết Định
- Nếu $V_0 > P_0$ (giá thị trường) $\Rightarrow$ **định giá thấp (undervalued)** $\Rightarrow$ Mua
- Nếu $V_0 < P_0$ $\Rightarrow$ **định giá cao (overvalued)** $\Rightarrow$ Bán
- Nếu $V_0 = P_0$ $\Rightarrow$ **định giá hợp lý (fairly valued)** $\Rightarrow$ Giữ

## Mô Hình Multiplier (Relative Valuation)

So sánh bội số giá của một công ty với các công ty cùng ngành, trung bình ngành, hoặc lịch sử của chính nó.

### Price-to-Earnings (P/E)

$$\text{Trailing P/E} = \frac{P_0}{EPS_0}$$

$$\text{Forward P/E} = \frac{P_0}{EPS_1}$$

**Justified P/E** (từ Gordon Growth):

$$\frac{P_0}{E_1} = \frac{D_1/E_1}{r - g} = \frac{1 - b}{r - g}$$

- $g$ cao hơn $\Rightarrow$ justified P/E cao hơn
- $r$ cao hơn $\Rightarrow$ justified P/E thấp hơn
- $b$ thấp hơn (payout cao hơn) $\Rightarrow$ justified P/E cao hơn

### Price-to-Book (P/B)

$$\text{P/B} = \frac{P_0}{\text{Book Value per Share}}$$

- Hữu ích cho các tổ chức tài chính (tài sản gần với giá trị thị trường)
- P/B thấp có thể cho thấy cổ phiếu giá trị (value stock) hoặc công ty đang gặp khó khăn
- Book value có thể âm (khiến P/B trở nên vô nghĩa)

### Price-to-Sales (P/S)

$$\text{P/S} = \frac{P_0}{\text{Revenue per Share}}$$

- Hữu ích cho các công ty có lợi nhuận âm
- Doanh thu khó bị thao túng hơn lợi nhuận
- KHÔNG phản ánh sự khác biệt về cấu trúc chi phí

### Price-to-Cash Flow (P/CF)

$$\text{P/CF} = \frac{P_0}{\text{Cash Flow per Share}}$$

- Dòng tiền khó bị thao túng hơn lợi nhuận
- Định nghĩa CF có thể khác nhau: CFO, FCF, EBITDA trên mỗi cổ phiếu

### EV/EBITDA

$$\text{EV/EBITDA} = \frac{\text{Market Cap} + \text{Debt} - \text{Cash}}{\text{EBITDA}}$$

- **Enterprise Value (EV)** đại diện cho tổng giá trị doanh nghiệp
- Trung lập với cấu trúc vốn (bao gồm cả nợ)
- Hữu ích để so sánh các công ty có mức độ đòn bẩy khác nhau
- EBITDA = ước tính dòng tiền hoạt động (trước capex)

## Asset-Based Valuation

### Net Asset Value (NAV)

$$\text{NAV} = \text{Market Value of Assets} - \text{Market Value of Liabilities}$$

$$\text{NAV per share} = \frac{\text{NAV}}{\text{Shares Outstanding}}$$

- Phù hợp với: công ty holding, bất động sản (REITs), công ty tài nguyên thiên nhiên
- Điều chỉnh book value về giá trị thị trường
- Hạn chế: khó định giá tài sản vô hình (thương hiệu, bằng sáng chế, goodwill)
- **Floor value** — giá trị thanh lý cung cấp ước tính tối thiểu

## So Sánh Các Mô Hình

| Mô hình | Phù hợp nhất | Ưu điểm | Hạn chế |
|---------|--------------|---------|---------|
| DDM | Công ty trưởng thành, trả cổ tức | Có cơ sở lý thuyết vững chắc | Cần dự báo cổ tức, giả định $g$ |
| P/E | Công ty có lợi nhuận | Được hiểu và sử dụng rộng rãi | Lợi nhuận có thể bị thao túng |
| P/B | Công ty tài chính | Chỉ số ổn định | BV có thể khác giá trị thị trường |
| P/S | Công ty chưa có lợi nhuận | Luôn dương | Bỏ qua chi phí |
| EV/EBITDA | So sánh qua các mức đòn bẩy | Trung lập với cấu trúc vốn | Bỏ qua capex, vốn lưu động |
| NAV | Công ty nặng về tài sản | Tài sản theo giá thị trường | Khó định giá tài sản vô hình |

## Trang Liên Quan

- [[equity-investments/concepts/company-analysis|Company Analysis]]
- [[equity-investments/concepts/equity-securities|Equity Securities]]
- [[corporate-issuers/concepts/capital-structure|Capital Structure and WACC]]