---
title: "M12 — Interest Rate Risk"
type: module
subject: fixed-income
module: M12
los:
  - 12.a: Calculate and interpret convexity and describe how it improves duration-based price estimates
  - 12.b: Describe the factors that affect convexity and how they relate to embedded options
  - 12.c: Calculate and interpret portfolio duration and convexity and explain their limitations
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - convexity
  - portfolio-duration
  - callable-bonds
  - putable-bonds
  - effective-convexity
---

# Bond Convexity and Portfolio Duration and Convexity

## Convexity Adjustment

Duration một mình chỉ cho xấp xỉ **tuyến tính** của mối quan hệ giá-lợi suất. Convexity nắm bắt **độ cong** và cải thiện ước tính:

$$\%\Delta PV \approx (-\text{ModDur} \times \Delta\text{Yield}) + \left(\frac{1}{2} \times \text{Convexity} \times \Delta\text{Yield}^2\right)$$

Số hạng convexity luôn **dương** đối với các trái phiếu không có embedded options bất kể lợi suất tăng hay giảm, nghĩa là:
- Duration **ước tính cao hơn** mức giảm giá khi lợi suất tăng
- Duration **ước tính thấp hơn** mức tăng giá khi lợi suất giảm

Convexity hiệu chỉnh cả hai sai số này.

---

## Tính Convexity

### Approximate Convexity

$$\text{ApproxCon} = \frac{PV_{-} + PV_{+} - 2 \times PV_0}{\Delta\text{Yield}^2 \times PV_0}$$

trong đó:
- $PV_{-}$ = giá nếu lợi suất giảm một lượng $\Delta\text{Yield}$
- $PV_{+}$ = giá nếu lợi suất tăng một lượng $\Delta\text{Yield}$
- $PV_0$ = giá hiện tại

### Money Convexity

$$\text{MoneyCon} = \text{AnnConvexity} \times PV_{\text{full}}$$

Dùng để tính thay đổi giá tuyệt đối (theo đô la) phát sinh từ tác động của convexity.

---

## Effective Convexity

Đối với các trái phiếu có embedded options, sử dụng dịch chuyển **đường cong lợi suất chuẩn** thay vì YTM:

$$\text{EffCon} = \frac{PV_{-} + PV_{+} - 2 \times PV_0}{\Delta\text{Curve}^2 \times PV_0}$$

Điều này cần thiết vì dòng tiền thay đổi khi lãi suất thay đổi (ví dụ: thực hiện quyền call/put).

---

## Các Yếu Tố Ảnh Hưởng đến Convexity

| Yếu tố | Tác động đến Convexity |
|--------|-------------------|
| Kỳ hạn dài hơn | Convexity cao hơn |
| Lãi suất coupon thấp hơn | Convexity cao hơn |
| Mức lợi suất thấp hơn | Convexity cao hơn |
| Dòng tiền phân tán nhiều hơn | Convexity cao hơn |

Với cùng duration, một trái phiếu có dòng tiền **phân tán hơn** (ví dụ: trái phiếu coupon so với zero-coupon bond) sẽ có convexity cao hơn.

---

## Convexity và Embedded Options

### Option-Free Bonds

- Convexity luôn **dương**
- Đường cong giá-lợi suất là convex (cong lên trên)
- Nhà đầu tư hưởng lợi từ convexity: giá tăng nhiều hơn khi lợi suất giảm so với mức giảm khi lợi suất tăng

### Callable Bonds

- Ở **lợi suất cao**: hoạt động giống option-free bond (convexity dương) -- quyền call far out of the money
- Ở **lợi suất thấp**: thể hiện **negative convexity** -- quyền call in the money, giới hạn mức tăng giá

$$\text{Callable bond price} \leq \text{Call price}$$

Khi lợi suất giảm, giá callable bond tiếp cận call price và ngừng tăng, tạo ra vùng "nén giá" đặc trưng.

### Putable Bonds

- **Luôn có convexity dương** (thậm chí hơn cả option-free bonds)
- Ở **lợi suất cao**: quyền put in the money, tạo ra sàn giá
- Quyền put bảo vệ nhà đầu tư khỏi sự sụt giảm giá, tăng cường convexity

$$\text{Putable bond price} \geq \text{Put price}$$

---

## Portfolio Duration

$$D_{\text{portfolio}} = \sum_{i=1}^{n} w_i \times D_i$$

trong đó:
- $w_i$ = tỷ trọng theo giá trị thị trường của trái phiếu $i$
- $D_i$ = duration của trái phiếu $i$

### Portfolio Convexity

$$\text{Con}_{\text{portfolio}} = \sum_{i=1}^{n} w_i \times \text{Con}_i$$

### Xấp Xỉ Giá Danh Mục

$$\%\Delta PV_{\text{portfolio}} \approx (-D_{\text{portfolio}} \times \Delta\text{Yield}) + \left(\frac{1}{2} \times \text{Con}_{\text{portfolio}} \times \Delta\text{Yield}^2\right)$$

---

## Hạn Chế của Portfolio Duration và Convexity

1. **Giả định dịch chuyển song song** -- portfolio duration/convexity giả định đường cong lợi suất dịch chuyển cùng một lượng ở tất cả các kỳ hạn. Trên thực tế, các dịch chuyển thường không song song (dốc lên, dốc xuống, xoắn).

2. **Xấp xỉ bình quân gia quyền** -- tổng hợp duration của từng trái phiếu thành một portfolio duration duy nhất là một xấp xỉ làm mất thông tin về phân phối dòng tiền.

3. **Tính nhất quán của thước đo lợi suất** -- mỗi trái phiếu có thể có lợi suất khác nhau; "portfolio yield" là một bình quân phức tạp, không đơn giản là bình quân gia quyền của các lợi suất riêng lẻ.

4. **Embedded options** -- nếu một số trái phiếu có embedded options, duration và convexity của chúng phụ thuộc vào lãi suất, làm phức tạp quá trình tổng hợp.

---

## Xem Thêm

- [[fixed-income/m11-duration-measures/index|M11 - Yield-Based Duration Measures]]
- [[fixed-income/m13-curve-based-risk/index|M13 - Curve-Based Risk Measures]]