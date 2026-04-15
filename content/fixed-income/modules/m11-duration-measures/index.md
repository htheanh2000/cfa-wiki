---
title: "M11 — Bond Valuation & Yields"
type: module
subject: fixed-income
module: M11
los:
  - 11.a: Define, calculate, and interpret modified duration, money duration, and the price value of a basis point (PVBP)
  - 11.b: Describe the properties of duration and their implications for bond price sensitivity
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - modified-duration
  - money-duration
  - PVBP
  - duration-properties
---

# Yield-Based Bond Duration Measures

## Modified Duration

### Định nghĩa và Công thức

Modified duration đo lường **độ nhạy giá theo phần trăm** của một trái phiếu đối với sự thay đổi trong yield:

$$\text{ModDur} = \frac{\text{MacDur}}{1 + r}$$

trong đó $r$ = yield theo kỳ (nếu coupon trả nửa năm, $r = \text{YTM}/2$).

### Xấp xỉ Thay đổi Giá

$$\%\Delta PV \approx -\text{ModDur} \times \Delta\text{Yield}$$

Dấu âm phản ánh **mối quan hệ nghịch chiều** giữa giá và yield.

### Approximate Modified Duration

Khi MacDur không có sẵn, ModDur có thể được ước tính bằng phương pháp số:

$$\text{ApproxModDur} = \frac{PV_{-} - PV_{+}}{2 \times PV_0 \times \Delta\text{Yield}}$$

trong đó:
- $PV_{-}$ = giá trái phiếu nếu yield **giảm** một lượng $\Delta\text{Yield}$
- $PV_{+}$ = giá trái phiếu nếu yield **tăng** một lượng $\Delta\text{Yield}$
- $PV_0$ = giá trái phiếu hiện tại (full price)

---

## Money Duration

### Định nghĩa

Money duration chuyển đổi modified duration thành thay đổi giá **tuyệt đối theo đơn vị tiền tệ**:

$$\text{MoneyDur} = \text{ModDur} \times PV_{\text{full}}$$

### Xấp xỉ Thay đổi Giá

$$\Delta PV \approx -\text{MoneyDur} \times \Delta\text{Yield}$$

Công thức này cho ra **thay đổi bằng tiền** trong giá trị trái phiếu ứng với một mức thay đổi yield nhất định.

---

## Price Value of a Basis Point (PVBP)

### Định nghĩa

PVBP (còn gọi là DV01) là **thay đổi giá tuyệt đối** ứng với sự thay đổi 1 basis point (0.01%) trong yield:

$$\text{PVBP} = \frac{PV_{-} - PV_{+}}{2}$$

trong đó $PV_{-}$ và $PV_{+}$ là giá sau khi giảm và tăng yield lần lượt 1 bp.

### Công thức tương đương

$$\text{PVBP} = \text{MoneyDur} \times 0.0001$$

---

## Các Tính chất của Duration

### Coupon Rate

$$\text{Higher coupon} \implies \text{Lower duration}$$

Coupon cao hơn có nghĩa là tỷ trọng lớn hơn của giá trị trái phiếu được nhận về sớm hơn, làm giảm thời gian bình quân gia quyền.

### Time to Maturity

$$\text{Longer maturity} \implies \text{Higher duration (generally)}$$

Ngoại lệ: đối với trái phiếu deep-discount, duration có thể giảm ở các kỳ hạn rất dài (hiếm gặp trong thực tế).

### Yield Level

$$\text{Lower yield} \implies \text{Higher duration}$$

Yield thấp hơn làm tăng trọng số tương đối của các dòng tiền ở xa, từ đó làm tăng duration.

---

## Các Trường hợp Đặc biệt

### Zero-Coupon Bond

$$\text{MacDur}_{\text{zero}} = N$$

trong đó $N$ = số năm đến khi đáo hạn. Macaulay duration của một zero-coupon bond bằng chính kỳ hạn của nó (toàn bộ giá trị đến từ một khoản thanh toán duy nhất tại ngày đáo hạn).

$$\text{ModDur}_{\text{zero}} = \frac{N}{1 + r}$$

### Perpetuity (Consol)

$$\text{MacDur}_{\text{perpetuity}} = \frac{1 + r}{r}$$

Ví dụ, nếu $r = 5\%$: MacDur $= \frac{1.05}{0.05} = 21$ năm.

$$\text{ModDur}_{\text{perpetuity}} = \frac{1}{r}$$

### Floating-Rate Note (FRN)

$$\text{MacDur}_{\text{FRN}} = \frac{T - t}{T}$$

trong đó:
- $T$ = tổng thời gian giữa các ngày reset coupon
- $t$ = thời gian đã trôi qua kể từ lần reset gần nhất

Tại ngày reset ($t = 0$): MacDur = 1 kỳ coupon đầy đủ (ví dụ: 0.5 năm với coupon nửa năm).
Ngay trước khi reset ($t \to T$): MacDur $\to 0$.

FRN có duration rất thấp vì coupon được reset theo lãi suất thị trường định kỳ.

---

## Bảng Tóm tắt

| Thước đo | Công thức | Đơn vị | Trường hợp sử dụng |
|---------|---------|-------|----------|
| Modified Duration | $\frac{\text{MacDur}}{1+r}$ | % trên mỗi 1% thay đổi yield | Độ nhạy giá tương đối |
| Money Duration | $\text{ModDur} \times PV$ | Tiền tệ | Độ nhạy giá tuyệt đối |
| PVBP | $\frac{PV_{-} - PV_{+}}{2}$ | Tiền tệ trên mỗi 1 bp | Hedging, quản lý rủi ro |

---

## Xem thêm

- [[fixed-income/m10-interest-rate-risk-return/index|M10 - Interest Rate Risk and Return]]
- [[fixed-income/m12-convexity-portfolio/index|M12 - Convexity and Portfolio Duration]]
- [[fixed-income/m13-curve-based-risk/index|M13 - Curve-Based Risk Measures]]