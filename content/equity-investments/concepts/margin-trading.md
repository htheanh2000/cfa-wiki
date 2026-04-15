---
title: Margin Trading and Leverage
type: concept
subject: equity-investments
module: M01
los: ["1.e", "1.f"]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, margin-trading, leverage, short-selling, margin-call]
---

# Margin Trading and Leverage

## Long Position on Margin

Nhà đầu tư vay một phần giá mua từ nhà môi giới (broker).

### Thiết lập Ban đầu

$$\text{Margin} = \frac{\text{Equity}}{\text{Total Asset Value}} = \frac{V_0 - \text{Loan}}{V_0}$$

trong đó:
- $V_0$ = giá trị ban đầu của vị thế
- Loan = số tiền vay từ broker

### Leverage Ratio

$$\text{Leverage Ratio} = \frac{1}{\text{Initial Margin \%}} = \frac{\text{Total Asset Value}}{\text{Equity}}$$

Ví dụ: Nếu yêu cầu initial margin = 55%, thì:

$$\text{Max Leverage Ratio} = \frac{1}{0.55} = 1.82\times$$

### Return on Margin (Leveraged Return)

$$R_{\text{margin}} = \frac{(P_1 - P_0) \times Q - \text{Interest on Loan}}{P_0 \times Q \times m_0}$$

trong đó:
- $P_0, P_1$ = giá ban đầu và giá kết thúc
- $Q$ = số lượng cổ phiếu
- $m_0$ = tỷ lệ initial margin
- Interest on Loan = số tiền vay $\times$ lãi suất

Cách tính khác:

$$R_{\text{margin}} = R_{\text{asset}} \times \text{Leverage Ratio} - r_b \times \frac{1 - m_0}{m_0}$$

trong đó:
- $R_{\text{asset}}$ = tỷ suất sinh lợi trên tài sản
- $r_b$ = lãi suất vay
- Leverage khuếch đại cả lợi nhuận LẪN thua lỗ

### Margin Call Price (Long Position)

Margin call xảy ra khi equity giảm xuống dưới mức yêu cầu **maintenance margin**.

$$P_{\text{margin call}} = P_0 \times \frac{1 - \text{Initial Margin}}{1 - \text{Maintenance Margin}}$$

Ví dụ: Mua tại \$100, initial margin 50%, maintenance margin 25%:

$$P_{\text{margin call}} = 100 \times \frac{1 - 0.50}{1 - 0.25} = 100 \times \frac{0.50}{0.75} = \$66.67$$

Nếu giá giảm xuống dưới \$66.67, broker phát lệnh margin call.

## Short Position on Margin

Nhà đầu tư vay cổ phiếu, bán chúng ra thị trường, và kỳ vọng mua lại ở mức giá thấp hơn.

### Quy trình Short Sale
1. Vay cổ phiếu từ broker
2. Bán cổ phiếu trên thị trường (nhận tiền về)
3. Ký quỹ (tài sản thế chấp) với broker
4. Mua lại cổ phiếu sau đó để trả cho người cho vay ("cover" the short)
5. Hoàn trả cổ phiếu cho người cho vay

### Short Position Return

$$R_{\text{short}} = \frac{P_0 - P_1 - \text{Dividends Paid}}{P_0 \times m_0}$$

- Short sellers **phải trả cổ tức** cho người cho vay cổ phiếu
- Có lợi nhuận khi giá giảm; thua lỗ khi giá tăng
- **Lợi nhuận tối đa**: cổ phiếu về \$0 (có giới hạn)
- **Thua lỗ tối đa**: không giới hạn (giá có thể tăng vô hạn)

### Margin Call Price (Short Position)

$$P_{\text{margin call}} = P_0 \times \frac{1 + \text{Initial Margin}}{1 + \text{Maintenance Margin}}$$

Ví dụ: Short tại \$100, initial margin 50%, maintenance margin 30%:

$$P_{\text{margin call}} = 100 \times \frac{1 + 0.50}{1 + 0.30} = 100 \times \frac{1.50}{1.30} = \$115.38$$

Nếu giá tăng vượt \$115.38, broker phát lệnh margin call.

## Điểm Khác Biệt Chính: Long vs Short Margin

| | Long on Margin | Short on Margin |
|---|---|---|
| Có lợi nhuận khi | Giá tăng | Giá giảm |
| Lợi nhuận tối đa | Không giới hạn | Có giới hạn (giá về 0) |
| Thua lỗ tối đa | Số tiền đầu tư | Không giới hạn |
| Margin call khi | Giá giảm | Giá tăng |
| Cổ tức | Được nhận | Phải trả cho người cho vay |

## Ví dụ: Tính Return on Margin

Mua 1.000 cổ phiếu tại \$50 với initial margin 50%. Cổ phiếu tăng lên \$60.

- Tổng giá trị đầu tư = 1.000 $\times$ \$50 = \$50.000
- Equity = 50% $\times$ \$50.000 = \$25.000
- Số tiền vay = \$25.000
- Asset return = $\frac{60-50}{50}$ = 20%
- Leveraged return = $\frac{(60-50) \times 1{,}000}{25{,}000}$ = $\frac{10{,}000}{25{,}000}$ = **40%**
- Leverage đã nhân đôi tỷ suất sinh lợi (chưa tính chi phí vay)

Với chi phí vay 5%: Lợi nhuận ròng = $40\% - 5\% \times \frac{25{,}000}{25{,}000}$ = $40\% - 5\%$ = **35%**

## Trang Liên Quan

- [[equity-investments/concepts/market-organization|Market Organization and Structure]]
- [[equity-investments/concepts/equity-securities|Equity Securities]]
- [[equity-investments/practice/cfai/equity-m01-market-organization|CFAI Practice: M01]]