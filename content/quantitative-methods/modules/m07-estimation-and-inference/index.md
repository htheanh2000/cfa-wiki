---
title: "M07 — Estimation & Inference"
type: module
subject: quantitative-methods
module: M07
los: ["7.a", "7.b", "7.c", "Pre.i", "Pre.ii", "Pre.iii"]
created: 2026-04-09
updated: 2026-04-09
tags: [sampling, clt, confidence-interval, standard-error, bias, resampling]
---

# Module 7: Estimation and Inference

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 274–304

## Learning Outcomes

| LOS | Mô tả |
|-----|-------|
| 7.a | So sánh các phương pháp lấy mẫu và ảnh hưởng đến sampling error |
| 7.b | Central limit theorem, sampling distribution, standard error |
| Pre.i | Point estimate vs confidence interval |
| Pre.ii | Confidence interval cho trung bình tổng thể |
| 7.c | Resampling (bootstrap, jackknife) để xác định sampling distribution |
| Pre.iii | Các loại bias: data snooping, selection, survivorship, look-ahead, time period |

## LOS 7.a — Sampling Methods

### Probability Sampling

| Phương pháp | Cơ chế |
|-------------|--------|
| **Simple Random** | Mỗi quan sát được chọn ngẫu nhiên |
| **Systematic** | Mỗi phần tử thứ $n$ (thứ 10, 20, 30...) |
| **Stratified Random** | Chia thành các strata → lấy mẫu ngẫu nhiên từ mỗi strata |
| **Cluster** | Chia thành các cluster → chọn toàn bộ cluster |

### Non-Probability Sampling

| **Convenience** | Dựa trên mức độ dễ tiếp cận (sampling error cao hơn) |
| **Judgmental** | Dựa trên kinh nghiệm của nhà nghiên cứu |

## LOS 7.b — Central Limit Theorem

$$\bar{X} \sim N\left(\mu, \frac{\sigma^2}{n}\right) \quad \text{for } n \geq 30$$

**Standard Error:**

| $\sigma$ đã biết | $\sigma$ chưa biết |
|---|---|
| $\sigma_{\bar{X}} = \frac{\sigma}{\sqrt{n}}$ | $s_{\bar{X}} = \frac{s}{\sqrt{n}}$ |

**Các tính chất mong muốn của estimator**: Unbiased ($E(\hat\theta) = \theta$), Efficient (phương sai nhỏ nhất), Consistent (hội tụ khi $n \to \infty$)

## Confidence Intervals (Pre.i, Pre.ii)

### Công thức

| $\sigma$ đã biết | $\sigma$ chưa biết |
|---|---|
| $\bar{X} \pm z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}$ | $\bar{X} \pm t_{\alpha/2} \cdot \frac{s}{\sqrt{n}}$ |

| Mức độ tin cậy | $z_{\alpha/2}$ |
|--|--|
| 90% | 1.645 |
| 95% | 1.960 |
| 99% | 2.576 |

### Lựa chọn Test Statistic

| Tổng thể | Nhỏ ($n<30$) | Lớn ($n \geq 30$) |
|---|---|---|
| Normal, $\sigma$ đã biết | z | z |
| Normal, $\sigma$ chưa biết | t | t* |
| Non-normal, $\sigma$ đã biết | N/A | z |
| Non-normal, $\sigma$ chưa biết | N/A | t* |

## Pre.iii — Sampling Biases

| Bias | Mô tả |
|------|-------|
| **Data snooping** | Kiểm định lặp đi lặp lại cho đến khi tình cờ đạt "mức ý nghĩa" |
| **Sample selection** | Loại trừ có hệ thống một số dữ liệu nhất định |
| **Survivorship** | Chỉ bao gồm các đối tượng còn tồn tại (bỏ qua những đối tượng đã thất bại) |
| **Look-ahead** | Sử dụng thông tin không có sẵn tại thời điểm ra quyết định |
| **Time period** | Kết quả chỉ phản ánh đúng cho giai đoạn được nghiên cứu |

## Connections

- Xây dựng từ: [[quantitative-methods/modules/m06-simulation-methods/index|M06 — Distributions, Resampling]]
- Mở rộng sang: [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — Hypothesis Testing]]