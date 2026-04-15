---
title: "M05 — Portfolio Math"
type: module
subject: quantitative-methods
module: M05
los: ["Pre.i", "Pre.ii", "Pre.iii", "Pre.iv", "Pre.v", "Pre.vi", "Pre.viii", "5.a", "5.b", "5.c"]
created: 2026-04-09
updated: 2026-04-09
tags: [portfolio, variance, covariance, correlation, normal-distribution, safety-first]
---

# Module 5: Portfolio Mathematics

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 212–254

## Mục tiêu học tập

| LOS | Mô tả |
|-----|-------------|
| Pre.i–iv | Phân phối xác suất, rời rạc/liên tục, CDF, phân phối đều |
| Pre.v | Phân phối Bernoulli và binomial |
| Pre.vi | Phân phối Normal — xác suất trong các khoảng giá trị |
| Pre.viii | Chuẩn hóa biến ngẫu nhiên; phân phối normal chuẩn |
| 5.a | Expected value, variance, covariance, correlation của tỷ suất sinh lời danh mục |
| 5.b | Covariance và correlation sử dụng hàm xác suất đồng thời |
| 5.c | Shortfall risk, safety-first ratio, tiêu chí Roy |

## Tỷ suất sinh lời kỳ vọng danh mục — Portfolio Expected Return (LOS 5.a)

$$
E(R_p) = \sum_{i=1}^{n} w_i \cdot E(R_i)
$$

trong đó $w_i$ = tỷ trọng của tài sản $i$, $E(R_i)$ = tỷ suất sinh lời kỳ vọng của tài sản $i$

## Covariance

$$
Cov(R_i, R_j) = E\left[(R_i - E(R_i))(R_j - E(R_j))\right]
$$

**Ma trận Covariance** cho 3 tài sản: $n^2$ phần tử, đường chéo chính = variance

## Correlation

$$
\rho(R_i, R_j) = \frac{Cov(R_i, R_j)}{\sigma(R_i) \cdot \sigma(R_j)}
$$

Khoảng giá trị: $-1 \leq \rho \leq +1$

## Portfolio Variance (2 tài sản)

$$
\sigma_p^2 = w_A^2 \sigma_A^2 + w_B^2 \sigma_B^2 + 2 w_A w_B \cdot Cov(R_A, R_B)
$$

$$
= w_A^2 \sigma_A^2 + w_B^2 \sigma_B^2 + 2 w_A w_B \cdot \rho(R_A, R_B) \cdot \sigma_A \cdot \sigma_B
$$

> **Lợi ích đa dạng hóa (Diversification benefit)**: Khi $\rho < 1$, rủi ro danh mục **nhỏ hơn** bình quân gia quyền của rủi ro từng tài sản riêng lẻ. Khi $\rho < 0$, lợi ích còn lớn hơn nữa.

### Ví dụ

Danh mục: 30% cổ phiếu ($\sigma = 20\%$), 70% trái phiếu ($\sigma = 12\%$), $\rho = 0.6$

$$
\sigma_p^2 = (0.3)^2(0.20)^2 + (0.7)^2(0.12)^2 + 2(0.3)(0.7)(0.0144) = 0.0167
$$
$$
\sigma_p = \sqrt{0.0167} = 12.92\%
$$

| Kịch bản | $\rho$ | $\sigma_p$ | Ghi chú |
|----------|--------|-----------|------|
| Tương quan dương | 0.6 | 12.92% | Cơ sở |
| Độc lập | 0 | 10.32% | Rủi ro thấp hơn |
| Tương quan âm | −0.6 | 6.82% | Rủi ro thấp hơn nhiều |

## Phân phối xác suất — Probability Distributions (Prerequisites)

| Phân phối | Loại | Đặc điểm chính |
|---|---|---|
| **Discrete Uniform** | Rời rạc | Tất cả kết quả có xác suất như nhau |
| **Bernoulli** | Rời rạc | Hai kết quả: thành công ($p$) hoặc thất bại ($1-p$) |
| **Binomial** | Rời rạc | Số lần thành công trong $n$ phép thử Bernoulli |
| **Continuous Uniform** | Liên tục | Xác suất bằng nhau trên toàn khoảng $[a,b]$ |
| **Normal** | Liên tục | Hình chuông, đối xứng, $\mu \pm 1\sigma$ = 68%, $\mu \pm 2\sigma$ = 95% |

### Standard Normal (Z-score)

$$
Z = \frac{X - \mu}{\sigma}
$$

## Tiêu chí Roy's Safety-First (LOS 5.c)

$$
SFRatio = \frac{E(R_p) - R_L}{\sigma_p}
$$

trong đó $R_L$ = ngưỡng tỷ suất sinh lời tối thiểu chấp nhận được (threshold)

**Quy tắc**: Chọn danh mục có **SFRatio cao nhất** — danh mục này tối thiểu hóa xác suất tỷ suất sinh lời rơi xuống dưới ngưỡng.

## Liên kết

- Xây dựng từ: [[quantitative-methods/modules/m04-probability-trees/index|M04 — Probability]], [[quantitative-methods/modules/m03-statistical-measures/index|M03 — Statistics]]
- Ứng dụng trong: môn Portfolio Management
- Công thức: [[quantitative-methods/formulas/portfolio-math|All M05 Formulas]]