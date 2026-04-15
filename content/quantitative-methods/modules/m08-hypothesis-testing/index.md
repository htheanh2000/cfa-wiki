---
title: "M08 — Hypothesis Testing"
type: module
subject: quantitative-methods
module: M08
los: ["8.a", "8.b", "8.c"]
created: 2026-04-09
updated: 2026-04-09
tags: [hypothesis-testing, type-i-error, type-ii-error, z-test, t-test, f-test, p-value]
---

# Module 8: Hypothesis Testing

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 305–375

## Learning Outcomes

| LOS | Mô tả |
|-----|-------------|
| 8.a | Quy trình hypothesis testing, statistical significance, Type I/II errors, power |
| 8.b | Xây dựng các kiểm định, xác định mức ý nghĩa, sai lầm và power |
| 8.c | So sánh parametric và nonparametric tests |

## Quy trình Hypothesis Testing 6 bước

### Bước 1: Phát biểu Hypotheses

| | $H_0$ (Null) | $H_a$ (Alternative) |
|---|---|---|
| Two-tailed | $\mu = \mu_0$ | $\mu \neq \mu_0$ |
| Right-tail | $\mu \leq \mu_0$ | $\mu > \mu_0$ |
| Left-tail | $\mu \geq \mu_0$ | $\mu < \mu_0$ |

### Bước 2: Test Statistic

$$\text{Test stat} = \frac{\text{Sample stat} - \text{Hypothesized value}}{\text{Standard error}}$$

| $\sigma$ đã biết | $\sigma$ chưa biết |
|---|---|
| $z = \frac{\bar{X} - \mu_0}{\sigma/\sqrt{n}}$ | $t = \frac{\bar{X} - \mu_0}{s/\sqrt{n}}$ (df = n−1) |

### Bước 3: Mức ý nghĩa ($\alpha$)

Phổ biến: 10%, 5%, 1%

### Bước 4: Quy tắc quyết định

| Kiểm định | Bác bỏ $H_0$ khi | z-critical ($\alpha=5\%$) |
|---|---|---|
| Two-tailed | \|stat\| > critical | $\pm 1.96$ |
| Right-tail | stat > critical | $+1.645$ |
| Left-tail | stat < critical | $-1.645$ |

### Bước 5: Tính toán từ dữ liệu mẫu

### Bước 6: Quyết định — bác bỏ hoặc không bác bỏ $H_0$

## Type I và Type II Errors

| | $H_0$ đúng | $H_0$ sai |
|---|---|---|
| **Không bác bỏ** | Đúng ($1-\alpha$) | Type II ($\beta$) |
| **Bác bỏ** | Type I ($\alpha$) | Đúng (Power $= 1-\beta$) |

## Mối tương đương giữa CI và Hypothesis Test

Kiểm định hai phía với mức ý nghĩa $\alpha$ tương đương với confidence interval $(1-\alpha)$. Nếu $\mu_0$ nằm ngoài CI → bác bỏ $H_0$.

## Kiểm định phương sai

**Phương sai đơn (chi-square):**
$$\chi^2 = \frac{(n-1)s^2}{\sigma_0^2}, \quad df = n-1$$

**Hai phương sai (F-test):**
$$F = \frac{s_1^2}{s_2^2} \text{ (giá trị lớn hơn ở tử số)}, \quad df_1 = n_1-1, \; df_2 = n_2-1$$

## LOS 8.c — Parametric vs Nonparametric

| Parametric | Nonparametric |
|---|---|
| Giả định phân phối (chuẩn) | Không giả định phân phối |
| Sử dụng các tham số | Sử dụng thứ hạng/dấu |
| Mạnh hơn khi giả định được thỏa mãn | Ổn định khi giả định bị vi phạm |
| z-test, t-test, F-test | Spearman rank, sign test, Mann-Whitney |

## Liên kết

- Dựa trên: [[quantitative-methods/modules/m07-estimation-and-inference/index|M07 — Estimation & CI]]
- Mở rộng sang: [[quantitative-methods/modules/m09-parametric-tests/index|M09 — Tests of Independence]]
- Ứng dụng trong: [[quantitative-methods/modules/m10-simple-linear-regression/index|M10 — Regression]] (t-test on slope, F-test)