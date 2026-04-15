---
title: "M08 — Valuation Applications"
type: module
subject: equity-investments
module: M08
los: ["8.a", "8.b", "8.c", "8.d", "8.e"]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, valuation, DDM, gordon-growth, multiplier, asset-based, intrinsic-value]
---

# Module 08: Equity Valuation — Concepts and Basic Tools

## Tổng quan

Module này giới thiệu các khái niệm cốt lõi của định giá cổ phiếu, bao gồm sự phân biệt giữa giá trị ước tính và giá thị trường, ba nhóm mô hình định giá chính, cùng với ứng dụng của dividend discount models, multiplier models, và asset-based models.

**Nguồn**: [[equity-investments/sources/sapp-equity-2026|SAPP CFA1 Equity Investments Slide 2026]] — Trang 318+

---

## LOS Coverage

### LOS 8.a: Estimated Value vs Market Price

**Intrinsic value** (giá trị cơ bản) là giá trị của một tài sản dựa trên sự hiểu biết hoàn chỉnh (về mặt lý thuyết) về các đặc tính đầu tư của nó.

$$V_0 = \text{Intrinsic Value (ước tính của analyst)}$$

$$P_0 = \text{Market Price (quan sát được trên thị trường)}$$

#### Các mối quan hệ chính

| Điều kiện | Hàm ý | Hành động |
|-----------|--------|-----------|
| $V_0 > P_0$ | Định giá thấp (Undervalued) | Mua |
| $V_0 < P_0$ | Định giá cao (Overvalued) | Bán / Short |
| $V_0 = P_0$ | Định giá hợp lý (Fairly valued) | Nắm giữ |

**Nguyên nhân dẫn đến mispricing**:
- Ước tính của analyst có thể sai (model risk, lỗi đầu vào)
- Thị trường có thể không hiệu quả (xem [[equity-investments/modules/m03-market-efficiency/index|M03: Market Efficiency]])
- Giá có thể mất nhiều thời gian để hội tụ về intrinsic value (catalyst risk)

> **Margin of safety** là chênh lệch giữa intrinsic value và giá thị trường. Margin càng lớn thì càng có đệm bảo vệ trước các sai số ước tính.

---

### LOS 8.b: Categories of Equity Valuation Models

#### 1. Present Value (Discounted Cash Flow) Models
- Ước tính intrinsic value bằng cách tính **present value của các dòng tiền kỳ vọng trong tương lai**
- Mô hình chính: **Dividend Discount Model (DDM)**
- Ngoài ra còn có: Free Cash Flow to Equity (FCFE), Free Cash Flow to Firm (FCFF)

#### 2. Multiplier (Relative Valuation) Models
- Định giá công ty so với một **benchmark** (các công ty tương đương, dữ liệu lịch sử, hoặc giá trị lý thuyết)
- Các bội số phổ biến: P/E, P/B, P/S, P/CF, EV/EBITDA

#### 3. Asset-Based Models
- Định giá công ty dựa trên **giá trị ước tính của tài sản trừ đi nợ phải trả**
- Phương pháp chính: **Net Asset Value (NAV)**

| Nhóm mô hình | Phù hợp nhất với | Hạn chế |
|-------------|-----------------|---------|
| Present Value | Công ty có dòng tiền dự đoán được | Nhạy cảm với giả định discount rate và tăng trưởng |
| Multiplier | So sánh nhanh giữa các công ty | Giả định rằng các công ty tương đương được định giá đúng |
| Asset-Based | Công ty nhiều tài sản, phân tích thanh lý | Có thể bỏ qua going-concern value, tài sản vô hình |

---

### LOS 8.c: Dividend Discount Model (DDM)

DDM định giá cổ phiếu bằng present value của tất cả các cổ tức kỳ vọng trong tương lai.

#### One-Period DDM

$$V_0 = \frac{D_1 + P_1}{1 + r}$$

trong đó:
- $V_0$ = intrinsic value hiện tại
- $D_1$ = cổ tức kỳ vọng cuối kỳ 1
- $P_1$ = giá kỳ vọng cuối kỳ 1
- $r$ = required rate of return

#### Multi-Period DDM

$$V_0 = \sum_{t=1}^{n} \frac{D_t}{(1+r)^t} + \frac{P_n}{(1+r)^n}$$

trong đó:
- $D_t$ = cổ tức kỳ vọng tại thời điểm $t$
- $P_n$ = giá terminal kỳ vọng tại thời điểm $n$
- $r$ = required rate of return

#### Gordon Growth Model (GGM) — Constant Growth DDM

Giả định cổ tức tăng trưởng với **tốc độ không đổi** $g$ mãi mãi:

$$\boxed{V_0 = \frac{D_1}{r - g}}$$

trong đó:
- $D_1 = D_0 \times (1 + g)$ = cổ tức kỳ vọng kỳ tiếp theo
- $r$ = required rate of return (phải thỏa mãn $> g$)
- $g$ = tốc độ tăng trưởng cổ tức không đổi

**Ước tính $g$**:

$$g = \text{ROE} \times b$$

trong đó:
- $\text{ROE}$ = Return on Equity
- $b$ = retention ratio = $1 - \text{Dividend Payout Ratio}$

#### Giả định và hạn chế của GGM
- Cổ tức tăng trưởng với **tốc độ không đổi** mãi mãi — không thực tế với nhiều công ty
- Điều kiện $r > g$ phải thỏa mãn; nếu không mô hình sẽ không hợp lệ
- Thay đổi nhỏ trong $r$ hoặc $g$ tạo ra biến động lớn trong $V_0$
- Không áp dụng được cho các công ty không trả cổ tức

#### Implied Required Return từ GGM

Sắp xếp lại:

$$r = \frac{D_1}{P_0} + g$$

Công thức này phân tách required return thành **dividend yield** + **capital gains yield**.

---

### LOS 8.d: Multiplier Models

Multiplier models so sánh giá cổ phiếu hoặc enterprise value của công ty với một chỉ số tài chính.

#### Price-to-Earnings (P/E)

**Trailing P/E** (dựa trên 12 tháng gần nhất):

$$\text{Trailing P/E} = \frac{P_0}{E_0}$$

**Leading (Forward) P/E** (dựa trên dự báo):

$$\text{Leading P/E} = \frac{P_0}{E_1}$$

**Justified P/E từ GGM**:

$$\frac{P_0}{E_1} = \frac{D_1 / E_1}{r - g} = \frac{1 - b}{r - g}$$

trong đó $b$ = retention ratio, nên $(1-b)$ = payout ratio.

#### Price-to-Book (P/B)

$$\text{P/B} = \frac{P_0}{\text{Book Value per Share}}$$

trong đó:

$$\text{Book Value per Share} = \frac{\text{Total Equity} - \text{Preferred Equity}}{\text{Shares Outstanding}}$$

**Justified P/B**:

$$\frac{P_0}{B_0} = \frac{\text{ROE} - g}{r - g}$$

#### Price-to-Sales (P/S)

$$\text{P/S} = \frac{P_0}{\text{Sales per Share}}$$

- Hữu ích cho các công ty có lợi nhuận âm
- Ít bị ảnh hưởng bởi thao túng kế toán hơn so với P/E

#### Price-to-Cash Flow (P/CF)

$$\text{P/CF} = \frac{P_0}{\text{Cash Flow per Share}}$$

trong đó cash flow có thể là operating cash flow, free cash flow, hoặc EBITDA trên mỗi cổ phiếu.

#### Enterprise Value to EBITDA (EV/EBITDA)

$$\text{EV/EBITDA} = \frac{\text{Enterprise Value}}{\text{EBITDA}}$$

trong đó:

$$\text{EV} = \text{Market Cap} + \text{Total Debt} - \text{Cash \& Equivalents}$$

**Ưu điểm của EV/EBITDA**:
- Trung lập với cấu trúc vốn (EV phản ánh cả nợ lẫn vốn chủ sở hữu)
- Không bị ảnh hưởng bởi chính sách khấu hao
- Hữu ích khi so sánh các công ty có mức độ đòn bẩy khác nhau

#### Justified vs Market Multiples

| Loại | Định nghĩa |
|------|-----------|
| **Justified multiple** | Được suy ra từ mô hình định giá (ví dụ: GGM) dựa trên các yếu tố cơ bản |
| **Market multiple** | Quan sát được từ các công ty tương đương trên thị trường |

> Nếu **justified multiple > market multiple**, cổ phiếu có thể đang bị **định giá thấp (undervalued)**.

---

### LOS 8.e: Asset-Based Models

#### Phương pháp Net Asset Value (NAV)

$$\text{NAV} = \text{Market Value of Assets} - \text{Market Value of Liabilities}$$

$$\text{NAV per Share} = \frac{\text{NAV}}{\text{Shares Outstanding}}$$

#### Khi nào nên dùng Asset-Based Models
- **Bất động sản** và **công ty đầu tư** — Tài sản có tính thanh khoản cao và có giá trị thị trường quan sát được
- **Công ty tài nguyên thiên nhiên** — Giá trị gắn liền với trữ lượng
- **Công ty tài chính** — Tài sản được ghi nhận theo giá thị trường (marked to market)
- **Phân tích thanh lý** — Xác định giá trị sàn trong các tình huống kiệt quệ tài chính

#### Hạn chế
- **Tài sản vô hình** (thương hiệu, sở hữu trí tuệ, vốn nhân lực) khó định giá
- **Going-concern value** có thể khác với tổng giá trị từng phần
- **Giá trị thị trường** của tài sản có thể không dễ xác định
- **Synergies** giữa các tài sản không được phản ánh

---

## Điểm mấu chốt

1. Intrinsic value là ước tính của analyst; so sánh với giá thị trường để xác định mispricing
2. Ba nhóm mô hình định giá: Present value (DDM), Multiplier, và Asset-based
3. Gordon Growth Model ($V_0 = D_1/(r-g)$) là nền tảng của DDM
4. Multiplier models (P/E, P/B, P/S, P/CF, EV/EBITDA) cho phép so sánh tương đối
5. Asset-based models định giá công ty theo tài sản trừ nợ — phù hợp nhất với các công ty nhiều tài sản

---

## Các trang liên quan

- [[equity-investments/modules/m05-company-analysis-past/index|M05: Company Analysis — Past and Present]]
- [[equity-investments/modules/m06-industry-analysis/index|M06: Industry and Competitive Analysis]]
- [[equity-investments/modules/m07-company-forecasting/index|M07: Company Analysis — Forecasting]]
- [[equity-investments/glossary/equity-m08-glossary|Glossary: M08]]
- [[equity-investments/formulas/equity-formulas|Equity Formulas]]