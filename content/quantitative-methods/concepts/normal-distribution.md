---
title: "Normal Distribution"
type: concept
subject: quantitative-methods
module: M05
created: 2026-04-09
updated: 2026-04-09
tags: [normal-distribution, z-score, confidence-interval, lognormal, t-distribution]
---

# Normal Distribution

## Tổng quan

Normal distribution là phân phối xác suất quan trọng nhất trong tài chính và thống kê. Vai trò trung tâm của nó xuất phát từ [[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem (CLT)|Central Limit Theorem]], định lý đảm bảo rằng trung bình mẫu hội tụ về normal distribution bất kể phân phối của tổng thể gốc là gì. Normal distribution là nền tảng cho confidence intervals, hypothesis testing, đo lường rủi ro danh mục, và các mô hình định giá quyền chọn.

## Tính chất của Normal Distribution

Một biến ngẫu nhiên phân phối chuẩn $X \sim N(\mu, \sigma^2)$ có hàm mật độ xác suất đối xứng hình chuông, được mô tả hoàn toàn bởi hai tham số: trung bình $\mu$ và phương sai $\sigma^2$.

$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)$$

Các tính chất chính:
- **Symmetry**: Phân phối đối xứng hoàn toàn quanh $\mu$; mean = median = mode.
- **Tails**: Hai đuôi kéo dài vô tận về hai phía (nhưng phần lớn xác suất tập trung quanh mean).
- **Xác định bởi hai tham số**: Được xác định hoàn toàn bởi $\mu$ (vị trí) và $\sigma^2$ (độ phân tán). [[quantitative-methods/glossary/m03-statistical-measures#Skewness|Skewness]] bằng 0 và [[quantitative-methods/glossary/m03-statistical-measures#Excess Kurtosis|excess kurtosis]] bằng 0 ([[quantitative-methods/glossary/m03-statistical-measures#Mesokurtic|mesokurtic]]).
- **Tổ hợp tuyến tính**: Mọi tổ hợp tuyến tính của các biến normal độc lập cũng tuân theo normal distribution.

## Quy tắc 68-95-99 (Confidence Intervals)

Với bất kỳ phân phối $N(\mu, \sigma^2)$ nào, xấp xỉ:

$$P(\mu - \sigma \leq X \leq \mu + \sigma) \approx 68\%$$
$$P(\mu - 2\sigma \leq X \leq \mu + 2\sigma) \approx 95\%$$
$$P(\mu - 3\sigma \leq X \leq \mu + 3\sigma) \approx 99.7\%$$

Chính xác hơn theo các mức confidence phổ biến trong CFA:

| Confidence Level | $\pm z$ |
|-----------------|---------|
| 90% | $\pm 1.645$ |
| 95% | $\pm 1.960$ |
| 99% | $\pm 2.576$ |

Các giá trị này được dùng trực tiếp khi xây dựng [[quantitative-methods/glossary/m07-estimation-and-inference#Confidence Interval|confidence intervals]] cho trung bình tổng thể.

## Chuẩn hóa và Z-Score

Bất kỳ biến phân phối chuẩn nào cũng có thể chuyển đổi sang [[quantitative-methods/glossary/m05-portfolio-math#Standard Normal Distribution|standard normal distribution]] $N(0,1)$ bằng cách tính [[quantitative-methods/glossary/m05-portfolio-math#Z-Score|z-score]]:

$$Z = \frac{X - \mu}{\sigma}$$

Việc chuẩn hóa này cho phép sử dụng bảng standard normal để tính xác suất. Ví dụ:
- $P(X \leq x) = P\left(Z \leq \frac{x-\mu}{\sigma}\right) = \Phi(z)$

trong đó $\Phi(\cdot)$ là CDF của standard normal. Z-score cũng là cơ sở cho **[[quantitative-methods/glossary/m05-portfolio-math#Safety-First Ratio|Safety-First Ratio]]** ([[quantitative-methods/glossary/m05-portfolio-math#Roy's Safety-First Criterion|Roy's criterion]]) — tiêu chí lựa chọn danh mục dựa trên rủi ro giảm giá.

## Lognormal Distribution và Giá Tài Sản

Trong khi tỷ suất sinh lời có thể xấp xỉ theo normal distribution, **giá** tài sản phải không âm. Nếu tỷ suất sinh lời liên tục $r = \ln(S_t/S_0)$ tuân theo normal distribution, thì tỷ lệ giá $S_t/S_0$ tuân theo [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|lognormal distribution]].

$$\text{If } r \sim N(\mu, \sigma^2) \Rightarrow S_t = S_0 e^r \text{ is lognormally distributed.}$$

Lognormal distribution lệch phải (right-skewed) và bị chặn dưới bởi zero — phù hợp với hành vi của giá cổ phiếu. Mối quan hệ này là nền tảng của mô hình định giá quyền chọn Black-Scholes.

## Các Phân Phối Liên Quan

Normal distribution là gốc của một số phân phối quan trọng khác dùng trong suy diễn thống kê:

- **[[quantitative-methods/glossary/m06-simulation-methods#Student's t-Distribution|Student's t-Distribution]]**: Dùng khi phương sai tổng thể chưa biết; tiến gần về normal khi [[quantitative-methods/glossary/m06-simulation-methods#Degrees of Freedom|degrees of freedom]] tăng. Có đuôi dày hơn — xác suất ở các cực lớn hơn. Dùng trong [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-tests]] và [[quantitative-methods/glossary/m10-simple-linear-regression#t-Test for Slope|kiểm định hệ số hồi quy]].

- **[[quantitative-methods/glossary/m06-simulation-methods#Chi-Square Distribution|Chi-Square Distribution]]**: Tổng bình phương của các biến standard normal. Lệch phải, không âm. Dùng để kiểm định [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|independence]] và giả thuyết về phương sai.

- **[[quantitative-methods/glossary/m06-simulation-methods#F-Distribution|F-Distribution]]**: Tỷ số của hai biến chi-square. Dùng để so sánh phương sai và kiểm định ý nghĩa tổng thể của mô hình hồi quy ([[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-Statistic]]).

Hiểu rõ các phân phối này và biết khi nào dùng từng loại là cốt lõi của framework kiểm định giả thuyết được trình bày trong [[quantitative-methods/modules/m08-hypothesis-testing/index|M08]].

## Các Module Nguồn

- [[quantitative-methods/modules/m05-portfolio-math/index|M05 — Portfolio Mathematics and Distributions]] — nội dung chính về normal, lognormal, binomial distributions
- [[quantitative-methods/modules/m06-simulation-methods/index|M06 — Simulation Methods]] — lognormal, t, chi-square, F distributions; Monte Carlo sử dụng đầu vào normal
- [[quantitative-methods/modules/m07-estimation-and-inference/index|M07 — Estimation and Inference]] — CLT và confidence intervals dựa trên normal distribution