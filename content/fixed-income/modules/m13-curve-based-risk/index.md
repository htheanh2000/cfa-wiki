---
title: "M13 — Duration"
type: module
subject: fixed-income
module: M13
los:
  - 13.a: Define and calculate effective duration and describe its use for bonds with embedded options
  - 13.b: Calculate the percentage price change using effective duration and effective convexity
  - 13.c: Define key rate duration and describe its use in measuring bond price sensitivity to nonparallel yield curve shifts
  - 13.d: Compare and contrast analytical duration and empirical duration and describe their advantages and limitations
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - effective-duration
  - effective-convexity
  - key-rate-duration
  - analytical-duration
  - empirical-duration
  - curve-based-risk
---

# Curve-Based and Empirical Fixed-Income Risk Measures

## Effective Duration

### Definition and Formula

Effective duration đo lường mức độ nhạy cảm của giá trái phiếu đối với sự thay đổi của **đường cong lãi suất chuẩn (benchmark yield curve)**, chứ không phải YTM của chính trái phiếu đó:

$$\text{EffDur} = \frac{PV_{-} - PV_{+}}{2 \times PV_0 \times \Delta\text{Curve}}$$

trong đó:
- $PV_{-}$ = giá trái phiếu sau khi đường cong chuẩn **giảm** một lượng $\Delta\text{Curve}$
- $PV_{+}$ = giá trái phiếu sau khi đường cong chuẩn **tăng** một lượng $\Delta\text{Curve}$
- $PV_0$ = giá trái phiếu hiện tại
- $\Delta\text{Curve}$ = mức dịch chuyển song song của đường cong lãi suất chuẩn

### Tại sao dùng Effective Duration cho Embedded Options?

Yield-based duration (ModDur) **không phù hợp** cho các trái phiếu có embedded options vì:

1. **Dòng tiền thay đổi theo lãi suất** -- khi lãi suất giảm, callable bond có thể bị thu hồi sớm; khi lãi suất tăng, putable bond có thể bị bán lại. Cấu trúc dòng tiền phụ thuộc vào diễn biến lãi suất.
2. **Không có YTM xác định** -- các trái phiếu có embedded options không có một tập hợp dòng tiền tương lai chắc chắn duy nhất, do đó một YTM đơn lẻ là không rõ ràng.
3. **Effective duration phản ánh được tính quyền chọn** -- bằng cách định giá lại trái phiếu theo mô hình định giá quyền chọn sau khi dịch chuyển toàn bộ đường cong chuẩn, effective duration thể hiện được cách embedded option làm thay đổi mức độ nhạy cảm giá.

### Giá trị Effective Duration điển hình

| Loại trái phiếu | Effective Duration |
|-----------|-------------------|
| Tiền mặt | $\approx 0$ |
| Trái phiếu zero-coupon | $\approx$ kỳ hạn |
| Trái phiếu lãi suất cố định | Nằm giữa 0 và kỳ hạn |
| Callable bond | $\leq$ duration của trái phiếu tương đương không có quyền chọn |
| Putable bond | $\leq$ duration của trái phiếu tương đương không có quyền chọn |
| Floating-rate note | $\approx$ thời gian đến lần reset tiếp theo |

---

## Thay đổi giá với Effective Duration và Convexity

$$\%\Delta PV \approx (-\text{EffDur} \times \Delta\text{Curve}) + \left(\frac{1}{2} \times \text{EffCon} \times \Delta\text{Curve}^2\right)$$

trong đó:

$$\text{EffCon} = \frac{PV_{-} + PV_{+} - 2 \times PV_0}{\Delta\text{Curve}^2 \times PV_0}$$

Đây là dạng tương tự theo đường cong của công thức yield-based duration + convexity từ [[fixed-income/m12-convexity-portfolio/index|M12]].

---

## Key Rate Duration

### Định nghĩa

**Key rate duration** (còn gọi là partial duration) đo lường mức độ nhạy cảm của giá trái phiếu đối với sự thay đổi lãi suất tại một **điểm kỳ hạn cụ thể** trên đường cong lãi suất chuẩn, trong khi giữ nguyên tất cả các mức lãi suất còn lại.

$$\text{KeyRateDur}_k = \frac{PV_{-,k} - PV_{+,k}}{2 \times PV_0 \times \Delta y_k}$$

trong đó $\Delta y_k$ là mức thay đổi lãi suất chỉ tại kỳ hạn $k$.

### Tính chất

$$\sum_{k} \text{KeyRateDur}_k = \text{EffDur}$$

Tổng của tất cả các key rate duration bằng effective duration của trái phiếu (vì một dịch chuyển song song chính là tổng hợp của tất cả các dịch chuyển điểm đơn lẻ).

### Ứng dụng cho các dịch chuyển không song song

- Effective duration giả định các dịch chuyển **song song** -- toàn bộ đường cong dịch chuyển đều nhau
- Key rate duration nắm bắt mức độ nhạy cảm với các dịch chuyển **không song song** (steepening, flattening, butterfly twists)
- Đặc biệt quan trọng cho:
  - **Bullet bonds**: key rate duration tập trung gần kỳ hạn
  - **Barbell portfolios**: key rate duration tập trung ở hai đầu ngắn hạn và dài hạn
  - **Laddered portfolios**: key rate duration phân bổ đều trên các kỳ hạn

### Ví dụ: So sánh danh mục

Hai danh mục có cùng effective duration bằng 7.0:

| Điểm kỳ hạn | Bullet (7 năm) | Barbell (2 năm + 30 năm) |
|---------------|---------------|----------------------|
| KRD 2 năm | 0.1 | 3.5 |
| KRD 7 năm | 6.5 | 0.0 |
| KRD 30 năm | 0.4 | 3.5 |
| **Tổng** | **7.0** | **7.0** |

Hai danh mục này có mức độ phơi nhiễm giống hệt nhau với dịch chuyển song song nhưng **rất khác nhau** khi đường cong thay đổi hình dạng.

---

## Analytical Duration và Empirical Duration

### Analytical Duration

- Được suy ra từ **công thức toán học** và các mô hình định giá trái phiếu
- Sử dụng các giả định về mối quan hệ giữa các biến đầu vào (lãi suất, spread, v.v.)
- Giả định các biến là **độc lập** (ví dụ: credit spread độc lập với lãi suất chuẩn)

**Ưu điểm:**
- Chính xác và có thể tái tạo
- Dựa trên các mô hình được xác định rõ ràng
- Dễ tính toán cho bất kỳ trái phiếu nào có tham số đã biết

**Hạn chế:**
- Giả định sự độc lập giữa các biến có thể tương quan trong thực tế
- Các giả định mô hình có thể không đứng vững trong giai đoạn căng thẳng thị trường
- Có thể không nắm bắt được các động lực phức tạp trong thực tế

### Empirical Duration

- Được ước tính từ **dữ liệu lịch sử** thông qua hồi quy thống kê:

$$\%\Delta P = \beta_0 + \beta_1 \times \Delta y + \epsilon$$

trong đó $\beta_1$ là ước lượng empirical duration.

- Phản ánh **các mối quan hệ thực tế quan sát được**, bao gồm cả tương quan giữa các biến

**Ưu điểm:**
- Nắm bắt được các tương quan trong thực tế (ví dụ: credit spreads có xu hướng nới rộng khi lợi suất chính phủ giảm trong giai đoạn flight-to-quality)
- Thực tế hơn cho các trái phiếu có rủi ro tín dụng và rủi ro lãi suất đan xen
- Phản ánh hành vi thị trường thực tế trong giai đoạn căng thẳng

**Hạn chế:**
- Yêu cầu đủ dữ liệu lịch sử
- Kết quả **phụ thuộc vào giai đoạn** -- các giai đoạn mẫu khác nhau cho kết quả ước lượng khác nhau
- Mối quan hệ có thể thay đổi theo thời gian (thay đổi chế độ)
- Kém tin cậy hơn đối với các trái phiếu mới phát hành hoặc kém thanh khoản với lịch sử giao dịch hạn chế

### Điểm khác biệt chính: Tương quan

Điểm phân biệt quan trọng nhất là cách xử lý **tương quan**:

- **Analytical**: giả định thay đổi lãi suất chuẩn không ảnh hưởng đến credit spreads (độc lập)
- **Empirical**: nắm bắt tương quan thực tế (ví dụ: khi lợi suất chính phủ giảm 100 bp trong khủng hoảng, credit spreads có thể nới rộng 50 bp, phần nào bù trừ lại mức giảm lãi suất)

Đối với **trái phiếu chất lượng cao** (gần với phi rủi ro): analytical $\approx$ empirical.

Đối với **trái phiếu chất lượng thấp** (high-yield, thị trường mới nổi): empirical duration có thể khác đáng kể so với analytical duration do tương quan âm giữa lãi suất và spreads.

---

## Tóm tắt: Lựa chọn thước đo Duration phù hợp

| Thước đo | Dịch chuyển đầu vào | Phù hợp nhất cho | Xử lý được Options? |
|---------|------------|----------|-----------------|
| Modified Duration | YTM của trái phiếu | Trái phiếu không có quyền chọn | Không |
| Effective Duration | Đường cong chuẩn | Trái phiếu có embedded options | Có |
| Key Rate Duration | Một điểm trên đường cong | Phân tích dịch chuyển không song song | Có |
| Empirical Duration | Dữ liệu lịch sử | Trái phiếu có các yếu tố rủi ro tương quan | Ngầm định |

---

## Xem thêm

- [[fixed-income/m11-duration-measures/index|M11 - Yield-Based Duration Measures]]
- [[fixed-income/m12-convexity-portfolio/index|M12 - Convexity and Portfolio Duration]]
- [[fixed-income/m09-term-structure/index|M09 - Term Structure]]