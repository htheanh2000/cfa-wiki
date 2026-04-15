---
title: Yield Spreads
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [G-spread, I-spread, Z-spread, OAS, benchmark, risk-premium]
---

# Yield Spreads

## Các Thành Phần Cấu Thành Benchmark Rate

Lợi suất yêu cầu của một trái phiếu phản ánh nhiều thành phần rủi ro:

$$\text{Required Yield} = \text{Real Risk-Free Rate} + \text{Expected Inflation} + \text{Risk Premiums}$$

### Risk Premiums Bao Gồm:
- **Credit risk** premium (rủi ro vỡ nợ)
- **Liquidity** premium
- **Maturity (term)** premium
- Các yếu tố **thuế**
- **Option** risk premium (đối với callable/putable bonds)

## G-Spread (Government Spread)

$$G\text{-spread} = YTM_{\text{bond}} - YTM_{\text{govt}}$$

- Spread so với **trái phiếu chính phủ** có cùng (hoặc gần giống) kỳ hạn
- Là spread lợi suất đơn giản; sử dụng một điểm benchmark duy nhất
- Trái phiếu chính phủ phải có kỳ hạn tương đương (có thể cần nội suy)

## I-Spread (Interpolated Spread)

$$I\text{-spread} = YTM_{\text{bond}} - \text{Swap Rate}$$

- Spread so với **đường cong lãi suất hoán đổi** (LIBOR/SOFR swap rates)
- Swap rate được nội suy để khớp với kỳ hạn của trái phiếu
- Swap curve mượt và liên tục hơn so với đường cong trái phiếu chính phủ
- Hữu ích khi nguồn cung trái phiếu chính phủ hạn chế

## Z-Spread (Zero-Volatility Spread)

Là spread không đổi được cộng vào từng **spot rate** trên đường cong benchmark sao cho giá trị hiện tại của các dòng tiền bằng với giá thị trường của trái phiếu:

$$PV = \sum_{t=1}^{n} \frac{CF_t}{(1 + S_t + Z)^t}$$

trong đó:
- $S_t$ = benchmark spot rate cho kỳ $t$
- $Z$ = Z-spread (không đổi qua tất cả các kỳ hạn)
- $CF_t$ = dòng tiền tại thời điểm $t$

### Z-Spread vs. G-Spread
- Z-spread sử dụng **toàn bộ đường cong spot**; G-spread chỉ dùng một điểm
- Z-spread chính xác hơn đối với trái phiếu khi đường cong lợi suất không phẳng
- Khi đường cong lợi suất phẳng: Z-spread ≈ G-spread

## OAS (Option-Adjusted Spread)

$$OAS = Z\text{-spread} - \text{Option Value (in spread terms)}$$

- Loại bỏ ảnh hưởng của **embedded options** khỏi spread
- Đối với **callable bonds**: OAS < Z-spread (quyền chọn có lợi cho tổ chức phát hành)
- Đối với **putable bonds**: OAS > Z-spread (quyền chọn có lợi cho trái chủ)
- Đối với **option-free bonds**: OAS = Z-spread

### Diễn Giải
- OAS đại diện cho spread phản ánh **credit risk và liquidity** mà thôi
- Cho phép so sánh các trái phiếu có embedded options khác nhau
- OAS cao hơn nghĩa là mức bù đắp lớn hơn cho rủi ro tín dụng và thanh khoản

## Tổng Hợp So Sánh Các Spread

| Spread | Benchmark | Tính Đến Term Structure? | Tính Đến Options? |
|--------|-----------|----------------------------|-----------------------|
| G-spread | Government bond YTM | Không (một điểm duy nhất) | Không |
| I-spread | Swap rate | Không (một điểm duy nhất) | Không |
| Z-spread | Spot curve | Có | Không |
| OAS | Spot curve + volatility model | Có | Có |

## Các Yếu Tố Ảnh Hưởng Đến Spread

Spread nới rộng cho thấy:
- Rủi ro tín dụng được nhận định cao hơn
- Thanh khoản thấp hơn
- Thị trường căng thẳng / tâm lý ngại rủi ro
- Kỳ hạn dài hơn (nhìn chung)
- Xếp hạng tín dụng thấp hơn

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/yield-measures|Yield Measures]]
- [[fixed-income/concepts/term-structure|Term Structure]]
- [[fixed-income/concepts/credit-risk|Credit Risk]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m07|Glossary: Module 07]]