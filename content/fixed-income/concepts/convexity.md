---
title: Convexity
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [convexity, duration, price-yield, callable, putable, effective-convexity]
---

# Convexity

Convexity đo lường **độ cong** của mối quan hệ giá-lợi suất và cung cấp **hiệu chỉnh bậc hai** cho ước tính thay đổi giá dựa trên duration.

## Tại Sao Convexity Quan Trọng

Duration (một thước đo tuyến tính) đánh giá thấp mức tăng giá và đánh giá quá cao mức giảm giá. Convexity hiệu chỉnh điều này bằng cách nắm bắt độ cong:

$$\%\Delta PV \approx (-\text{ModDur} \times \Delta \text{Yield}) + \left(\frac{1}{2} \times \text{Convexity} \times \Delta \text{Yield}^2\right)$$

- Thành phần convexity **luôn dương** đối với trái phiếu không có quyền chọn (positive convexity)
- Điều chỉnh convexity trở nên quan trọng hơn khi **biến động lợi suất lớn hơn**

## Approximate Convexity

$$\text{ApproxCon} = \frac{PV_{-} + PV_{+} - 2 \times PV_0}{\Delta \text{Yield}^2 \times PV_0}$$

trong đó:
- $PV_{-}$ = giá khi lợi suất giảm $\Delta \text{Yield}$
- $PV_{+}$ = giá khi lợi suất tăng $\Delta \text{Yield}$
- $PV_0$ = giá hiện tại

## Money Convexity

$$\text{MoneyCon} = \text{Convexity} \times PV^{\text{Full}}$$

Điều chỉnh dollar convexity:

$$\Delta PV \approx (-\text{MoneyDur} \times \Delta \text{Yield}) + \left(\frac{1}{2} \times \text{MoneyCon} \times \Delta \text{Yield}^2\right)$$

## Effective Convexity

Đối với trái phiếu có **embedded options**, effective convexity tính đến sự thay đổi trong dòng tiền:

$$\text{EffCon} = \frac{PV_{-} + PV_{+} - 2 \times PV_0}{\Delta \text{Curve}^2 \times PV_0}$$

Sử dụng mức dịch chuyển đường cong tham chiếu ($\Delta \text{Curve}$) thay vì thay đổi YTM.

## Positive vs. Negative Convexity

### Positive Convexity (Trái Phiếu Không Có Quyền Chọn)
- Đường cong giá-lợi suất có dạng lồi (cong lên trên)
- Giá **tăng nhiều hơn** khi lợi suất giảm so với mức **giảm** khi lợi suất tăng
- Nhà đầu tư **được lợi** từ positive convexity
- Tất cả trái phiếu không có quyền chọn đều thể hiện positive convexity

### Negative Convexity (Callable Bonds)

Khi lợi suất giảm đáng kể:
- Callable bonds thể hiện **negative convexity** (giá bị giới hạn gần call price)
- Mức tăng giá bị hạn chế vì tổ chức phát hành có khả năng sẽ call trái phiếu
- Đường cong giá-lợi suất trở nên **lõm** ở mức lợi suất thấp

| Mức Lợi Suất | Hành Vi của Callable Bond |
|-------------|----------------------|
| Lợi suất cao (cao hơn nhiều so với coupon) | Hoạt động như trái phiếu không có quyền chọn; positive convexity |
| Gần ngưỡng call | Vùng chuyển tiếp |
| Lợi suất thấp (dưới coupon) | Negative convexity; giá bị giới hạn gần call price |

### Putable Bonds
- Luôn thể hiện **positive convexity**
- Có **price floor** gần put price
- Mức giảm giá bị hạn chế vì người nắm giữ có thể put trái phiếu trở lại cho tổ chức phát hành
- Effective convexity có thể cao hơn so với trái phiếu không có quyền chọn tương đương ở mức lợi suất cao

## Các Yếu Tố Ảnh Hưởng Đến Convexity

| Yếu Tố | Tác Động Đến Convexity |
|--------|-------------------|
| Kỳ hạn dài hơn | Convexity cao hơn |
| Coupon thấp hơn | Convexity cao hơn |
| Lợi suất thấp hơn | Convexity cao hơn |
| Dòng tiền phân tán | Convexity cao hơn |

## Convexity Như Một Đặc Tính Đáng Mong Muốn

- Nhà đầu tư **ưa thích** convexity cao hơn (khi các yếu tố khác bằng nhau)
- Convexity cao hơn đồng nghĩa với mức tăng giá lớn hơn khi lợi suất giảm và tổn thất nhỏ hơn khi lợi suất tăng
- Trái phiếu có convexity cao hơn thường có **lợi suất thấp hơn** (nhà đầu tư trả giá cho lợi ích này)

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/duration|Duration]]
- [[fixed-income/concepts/bond-valuation|Bond Valuation]]
- [[fixed-income/concepts/interest-rate-risk|Interest Rate Risk]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m12|Glossary: Module 12]]