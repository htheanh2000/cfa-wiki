---
title: "M03 — Statistical Measures"
type: module
subject: quantitative-methods
module: M03
los: ["Pre.i", "Pre.ii", "Pre.iii", "Pre.iv", "Pre.v", "Pre.vi", "3.a", "3.b", "3.c", "3.d"]
created: 2026-04-09
updated: 2026-04-09
tags: [statistics, mean, variance, standard-deviation, skewness, kurtosis, correlation]
---

# Module 3: Statistical Measures of Asset Returns

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] trang 113–178

## Learning Outcomes

| LOS | Mô tả |
|-----|-------------|
| Pre.i | Xác định và so sánh các loại dữ liệu |
| Pre.ii | Cách tổ chức dữ liệu cho phân tích định lượng |
| Pre.iii | Phân phối tần số và các phân phối liên quan |
| Pre.iv–vi | Bảng phân loại chéo (contingency tables), trực quan hóa dữ liệu, các loại biểu đồ |
| 3.a | Các thước đo xu hướng trung tâm và vị trí |
| 3.b | Các thước đo phân tán |
| 3.c | Skewness và kurtosis |
| 3.d | Correlation giữa hai biến |

## Phân Loại Dữ Liệu

### Theo Góc Độ Thống Kê

| Numerical (Định lượng) | Categorical (Định tính) |
|---|---|
| **Discrete**: có thể đếm được, số lượng hữu hạn (ví dụ: số lượng cổ phiếu) | **Nominal**: không có thứ tự logic (ví dụ: ngành của cổ phiếu) |
| **Continuous**: có thể đo lường, phạm vi vô hạn (ví dụ: lượng mưa) | **Ordinal**: có thứ tự logic (ví dụ: xếp hạng top 100 cổ phiếu) |

### Theo Phương Thức Thu Thập

| Time Series | Cross-Sectional | Panel |
|---|---|---|
| Cùng một biến theo thời gian | Nhiều biến tại một thời điểm | Nhiều biến theo thời gian cho nhiều đối tượng |
| Ví dụ: lợi suất hàng tháng của FPT 2017–2022 | Ví dụ: lợi suất của FPT, MWG,... ngày 1/1 | Ví dụ: tỷ lệ D/E của 20 công ty trong 24 quý |

### Theo Cách Tổ Chức

- **Structured**: có tổ chức, mẫu lặp lại (dữ liệu thị trường, báo cáo tài chính)
- **Unstructured**: không có định dạng chuẩn (mạng xã hội, ảnh vệ tinh)

## Các Thước Đo Xu Hướng Trung Tâm (LOS 3.a)

| Thước đo | Công thức | Phù hợp nhất |
|---------|---------|----------|
| **Arithmetic Mean** | $\bar{X} = \frac{\sum X_i}{n}$ | Tính trung bình thông thường |
| **Trimmed Mean** | Loại bỏ $x\%$ cao nhất/thấp nhất, rồi lấy trung bình | Giảm tác động của giá trị ngoại lai |
| **Winsorized Mean** | Thay các giá trị cực đoan bằng giá trị không cực đoan gần nhất, rồi lấy trung bình | Giữ nguyên toàn bộ điểm dữ liệu |
| **Median** | Giá trị ở giữa khi sắp xếp theo thứ tự | Phân phối lệch (skewed distributions) |
| **Mode** | Giá trị xuất hiện nhiều nhất | Dữ liệu định tính |

## Các Thước Đo Phân Tán (LOS 3.b)

| Thước đo | Công thức |
|---------|---------|
| **Range** | $\text{Range} = X_{\max} - X_{\min}$ |
| **MAD** | $MAD = \frac{\sum \|X_i - \bar{X}\|}{n}$ |
| **Population Variance** | $\sigma^2 = \frac{\sum (X_i - \mu)^2}{N}$ |
| **Sample Variance** | $s^2 = \frac{\sum (X_i - \bar{X})^2}{n-1}$ |
| **Standard Deviation** | $\sigma = \sqrt{\sigma^2}$ hoặc $s = \sqrt{s^2}$ |
| **CV (Coefficient of Variation)** | $CV = \frac{s}{\bar{X}}$ |
| **Target Downside Deviation** | $s_{\text{target}} = \sqrt{\frac{\sum_{\text{for all } X_i < B}(X_i - B)^2}{n-1}}$ |

## Skewness và Kurtosis (LOS 3.c)

**Skewness** đo lường tính bất đối xứng:
- $S_k > 0$: lệch phải (positive skew) — mean > median > mode
- $S_k < 0$: lệch trái (negative skew) — mean < median < mode
- $S_k = 0$: phân phối đối xứng

**Kurtosis** đo lường độ dày của đuôi phân phối:
- **Leptokurtic** (excess kurtosis > 0): đuôi béo, nhiều kết quả cực đoan hơn
- **Mesokurtic** (excess kurtosis = 0): phân phối chuẩn (normal distribution)
- **Platykurtic** (excess kurtosis < 0): đuôi mỏng

> **Đối với nhà đầu tư**: phân phối leptokurtic đồng nghĩa với xác suất cao hơn để xảy ra các mức lợi suất cực đoan (cả lãi lớn lẫn lỗ lớn)

## Correlation (LOS 3.d)

$$
\rho(X,Y) = \frac{Cov(X,Y)}{\sigma_X \cdot \sigma_Y}
$$

- $\rho = +1$: tương quan dương tuyệt đối (perfect positive linear relationship)
- $\rho = 0$: không có mối quan hệ tuyến tính
- $\rho = -1$: tương quan âm tuyệt đối (perfect negative linear relationship)

> **Hạn chế**: correlation chỉ đo lường mối quan hệ *tuyến tính* và có thể bị bóp méo bởi các giá trị ngoại lai

## Liên Kết

- Liên quan: [[quantitative-methods/concepts/data-types|Data Types]], [[quantitative-methods/concepts/frequency-distribution|Frequency Distribution]]
- Mở rộng sang: [[quantitative-methods/modules/m05-portfolio-mathematics/index|M05 — Portfolio Math]] (covariance, correlation trong bối cảnh danh mục đầu tư)
- Công thức: [[quantitative-methods/formulas/statistics|All M03 Formulas]]