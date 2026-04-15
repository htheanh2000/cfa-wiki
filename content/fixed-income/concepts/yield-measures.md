---
title: Yield Measures
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [yield, YTM, YTC, YTW, current-yield, EAR, APR]
---

# Yield Measures

## Current Yield

$$\text{Current Yield} = \frac{\text{Annual Coupon}}{\text{Bond Price}}$$

- Thước đo đơn giản; bỏ qua lãi/lỗ vốn và giá trị thời gian của tiền
- Phóng đại lợi suất thực tế với trái phiếu premium, đánh giá thấp với trái phiếu discount

## Yield to Maturity (YTM)

**Internal rate of return** (IRR) của trái phiếu được nắm giữ đến ngày đáo hạn, giả định tất cả coupon được tái đầu tư ở mức YTM.

$$PV = \sum_{t=1}^{n} \frac{PMT}{(1 + YTM)^t} + \frac{FV}{(1 + YTM)^n}$$

### Giả định và Hạn chế
- Giả định trái phiếu được **nắm giữ đến ngày đáo hạn**
- Giả định tất cả coupon được **tái đầu tư ở mức YTM**
- Giả định tái đầu tư hiếm khi phản ánh thực tế
- YTM là **promised yield**, không nhất thiết là lợi suất thực hiện được

## Yield to Call (YTC)

Với trái phiếu callable, được tính tương tự YTM nhưng sử dụng:
- **Call price** thay vì mệnh giá
- **Call date** thay vì ngày đáo hạn

$$PV = \sum_{t=1}^{n_c} \frac{PMT}{(1 + YTC)^t} + \frac{\text{Call Price}}{(1 + YTC)^{n_c}}$$

trong đó $n_c$ = số kỳ đến call date.

## Yield to Worst (YTW)

$$YTW = \min(YTM, YTC_1, YTC_2, \ldots)$$

Giá trị **thấp nhất** trong YTM và tất cả các giá trị YTC có thể. Đây là thước đo thận trọng dành cho trái phiếu callable.

## Simple Yield

$$\text{Simple Yield} = \frac{\text{Annual Coupon} + \frac{\text{Par} - \text{Price}}{\text{Years to Maturity}}}{\text{Price}}$$

- Phép xấp xỉ được sử dụng ở một số thị trường (ví dụ: Nhật Bản)
- Có tính đến lãi/lỗ vốn nhưng không tính giá trị thời gian của tiền

## EAR vs. APR

### Stated Annual Rate (APR)
Lãi suất năm chưa điều chỉnh ghép lãi. Lợi suất trái phiếu trả coupon nửa năm là 3%/kỳ có APR (BEY) là 6%.

### Effective Annual Rate (EAR)

$$EAR = \left(1 + \frac{APR}{m}\right)^m - 1$$

trong đó $m$ = số kỳ ghép lãi trong một năm.

### Chuyển đổi APR giữa các kỳ ghép lãi

$$\left(1 + \frac{APR_m}{m}\right)^m = \left(1 + \frac{APR_n}{n}\right)^n$$

**Ví dụ**: Chuyển đổi YTM nửa năm 6% sang tương đương theo quý:

$$\left(1 + \frac{0.06}{2}\right)^2 = \left(1 + \frac{APR_4}{4}\right)^4$$

## Government Equivalent Yield

- Điều chỉnh lợi suất trái phiếu doanh nghiệp (thường được báo giá theo cơ sở 30/360) sang quy ước **actual/actual** dùng cho trái phiếu chính phủ
- Cho phép so sánh spread giữa trái phiếu doanh nghiệp và trái phiếu chính phủ trên cùng một cơ sở
- Điều chỉnh sự khác biệt về quy ước tính ngày

## Street Convention vs. True Yield

| Thước đo | Giả định |
|---------|-----------|
| **Street convention** | Giả định ngày coupon theo lịch (không điều chỉnh cuối tuần/ngày lễ) |
| **True yield** | Điều chỉnh theo ngày thanh toán thực tế (cuối tuần, ngày lễ làm trễ thanh toán) |

True yield ≤ Street convention yield (thanh toán trễ làm giảm lợi suất thực tế).

## Money Market Yields

### Bank Discount Yield

$$r_{BD} = \frac{D}{FV} \times \frac{360}{\text{Days}}$$

### Money Market Yield (CD equivalent)

$$r_{MM} = \frac{D}{PV} \times \frac{360}{\text{Days}}$$

### Bond Equivalent Yield (BEY)

$$r_{BEY} = \frac{D}{PV} \times \frac{365}{\text{Days}}$$

trong đó $D$ = dollar discount = $FV - PV$.

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/bond-valuation|Bond Valuation]]
- [[fixed-income/concepts/yield-spreads|Yield Spreads]]
- [[fixed-income/concepts/term-structure|Term Structure]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m07|Glossary: Module 07]]