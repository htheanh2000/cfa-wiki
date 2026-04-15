---
title: "M01 — Rates & Returns"
type: module
subject: quantitative-methods
module: M01
los: ["1.a", "1.b", "1.c", "1.d", "1.e"]
created: 2026-04-09
updated: 2026-04-09
tags: [rates, returns, interest-rate, hpr, mwr, twr]
---

# Module 1: Rates and Returns

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 3–32

## Learning Outcomes

| LOS | Mô tả |
|-----|-------|
| 1.a | Diễn giải interest rates là required rates of return, discount rates, hoặc opportunity costs |
| 1.b | Tính toán và diễn giải các phương pháp đo lường return theo thời gian |
| 1.c | So sánh money-weighted và time-weighted rates of return |
| 1.d | Tính toán annualized return measures và continuously compounded returns |
| 1.e | Tính toán và diễn giải các return measures chính |

## Tổng quan

```
Interest Rate
├── Định nghĩa và Diễn giải (LOS 1.a)
│   ├── Discount rate
│   ├── Opportunity cost
│   └── Required rate of return
├── Đo lường — Tổng quát (LOS 1.b, 1.c)
│   ├── HPR (Holding Period Return)
│   ├── Arithmetic mean return
│   ├── Geometric mean return
│   ├── Harmonic mean return
│   ├── Money-weighted return (MWR)
│   └── Time-weighted return (TWR)
└── Đo lường — Tài sản Đặc biệt (LOS 1.d, 1.e)
    ├── Gross and Net Return
    ├── Pretax and After-tax Nominal Return
    ├── Real Return and Nominal Return
    └── Leverage Return
```

## LOS 1.a — Interest Rates

### Định nghĩa
Interest rate là khoản phí người cho vay tính cho việc sử dụng tài sản, được biểu thị theo phần trăm của số tiền gốc.

### Ba Cách Diễn Giải

| Cách diễn giải | Ý nghĩa |
|----------------|---------|
| **Discount rate** | Tỷ lệ nhà đầu tư chiết khấu dòng tiền tương lai về giá trị hiện tại |
| **Opportunity cost** | Giá trị nhà đầu tư bỏ lỡ khi lựa chọn một hành động cụ thể |
| **Required rate of return** | Tỷ lệ tối thiểu nhà đầu tư phải nhận được để chấp nhận khoản đầu tư |

### Thành Phần của Required Rate of Return

$$
r = r_f + \text{Default RP} + \text{Liquidity RP} + \text{Maturity RP}
$$

trong đó:
- $r_f$ = **Nominal risk-free rate** = Real risk-free rate + Inflation premium
- Default RP = khoản bù đắp cho rủi ro vỡ nợ của người đi vay
- Liquidity RP = khoản bù đắp cho khó khăn khi bán nhanh tài sản theo giá trị hợp lý
- Maturity RP = khoản bù đắp cho độ nhạy cảm với biến động lãi suất khi kỳ hạn kéo dài

## LOS 1.b — Đo Lường Return

### Một Kỳ: Holding Period Return (HPR)

$$
HPR = \frac{P_1 - P_0 + I_1}{P_0} = \frac{\text{Ending value}}{\text{Beginning value}} - 1
$$

trong đó $P_0$ = giá đầu kỳ, $P_1$ = giá cuối kỳ, $I_1$ = thu nhập (cổ tức, coupon)

### Các Chỉ Số Đo Lường Return Nhiều Kỳ

| Chỉ số | Công thức | Ứng dụng |
|--------|-----------|----------|
| **Holding Period** | $R = (1+R_1)(1+R_2)\cdots(1+R_n) - 1$ | Tổng return trong toàn bộ giai đoạn |
| **Arithmetic Mean** | $\bar{R} = \frac{R_1 + R_2 + \cdots + R_n}{n}$ | Trung bình đơn giản; ước lượng không chệch của mean thực |
| **Geometric Mean** | $\bar{R}_G = \sqrt[n]{(1+R_1)(1+R_2)\cdots(1+R_n)} - 1$ | Tỷ lệ tăng trưởng kép theo kỳ; $\bar{R}_G < \bar{R}$ khi return biến động |
| **Harmonic Mean** | $\bar{X}_H = \frac{n}{\sum_{i=1}^{n} \frac{1}{X_i}}$ | Xu hướng trung tâm khi có ngoại lệ; tỷ số P/E, cost averaging |

> **Quan hệ quan trọng**: $\bar{R}_H \leq \bar{R}_G \leq \bar{R}$ (bằng nhau chỉ khi tất cả return đều giống nhau)

### Ví dụ: Các Chỉ Số Đo Lường Return

Nhà đầu tư mua $1,000 quỹ tương hỗ. Return qua 3 năm: +5%, +8%, +12%.

- **HPR** = $(1.05)(1.08)(1.12) - 1 = 27\%$
- **Arithmetic mean** = $\frac{5\% + 8\% + 12\%}{3} = 8.33\%$
- **Geometric mean** = $\sqrt[3]{(1.05)(1.08)(1.12)} - 1 = 8.29\%$
- **Harmonic mean** = $\frac{3}{\frac{1}{1.05} + \frac{1}{1.08} + \frac{1}{1.12}} - 1 = 8.26\%$

## LOS 1.c — MWR vs TWR

| | Money-Weighted Return (MWR) | Time-Weighted Return (TWR) |
|---|---|---|
| **Định nghĩa** | Internal rate of return (IRR) của toàn bộ dòng tiền | Tỷ lệ tăng trưởng kép của $1 đầu tư ban đầu |
| **Chịu ảnh hưởng bởi** | Thời điểm và quy mô dòng tiền | Không bị ảnh hưởng bởi dòng tiền |
| **Các bước** | 1. Liệt kê tất cả dòng tiền vào (+) và ra (−) | 1. Chia thành các tiểu kỳ tại mỗi thời điểm có dòng tiền |
| | 2. Giải để tìm IRR | 2. Tính HPR cho mỗi tiểu kỳ |
| | | 3. Ghép nối: $TWR = (1+HPR_1)(1+HPR_2)\cdots(1+HPR_n) - 1$ |
| **Phù hợp nhất để** | Đánh giá trải nghiệm thực tế của nhà đầu tư | Đánh giá kỹ năng của portfolio manager |

## LOS 1.e — Các Return Measures Đặc Biệt

| Chỉ số | Công thức |
|--------|-----------|
| **Net Return** | Gross return − Phí |
| **After-tax Return** | Pretax return × $(1 - \text{tax rate})$ |
| **Real Return** | $\frac{1 + R_{\text{nominal}}}{1 + \text{Inflation}} - 1$ |
| **Leveraged Return** | $R_L = R_p + \frac{V_B}{V_E}(R_p - r_D)$ |

trong đó $V_B$ = số tiền vay, $V_E$ = vốn chủ sở hữu, $r_D$ = cost of debt

## Liên kết

- Liên quan: [[quantitative-methods/concepts/interest-rates|Interest Rates]], [[quantitative-methods/concepts/time-value-of-money|TVM]]
- Mở rộng sang: [[quantitative-methods/modules/m02-time-value-of-money/index|M02 — TVM]] (annualized returns, continuous compounding)
- Công thức: [[quantitative-methods/formulas/rates-and-returns|All M01 Formulas]]