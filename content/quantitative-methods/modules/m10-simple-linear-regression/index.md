---
title: "M10 — Linear Regression"
type: module
subject: quantitative-methods
module: M10
los: ["10.a", "10.b", "10.c", "10.d", "10.e", "10.f"]
created: 2026-04-09
updated: 2026-04-09
tags: [regression, ols, r-squared, anova, see, f-test, prediction-interval]
---

# Module 10: Simple Linear Regression

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 396–451

## Learning Outcomes

| LOS | Mô tả |
|-----|-------|
| 10.a | Mô hình simple linear regression, OLS, diễn giải hệ số |
| 10.b | Các giả định và phân tích phần dư |
| 10.c | Đo lường độ phù hợp ($R^2$), kiểm định độ phù hợp (F-test, t-test trên hệ số) |
| 10.d | ANOVA trong regression, SEE |
| 10.e | Giá trị dự báo và prediction interval |
| 10.f | Các dạng hàm khác nhau (log-lin, lin-log, log-log) |

## LOS 10.a — Mô Hình

**Simple linear regression:**

$$Y_i = b_0 + b_1 X_i + \epsilon_i, \quad i = 1, \ldots, n$$

**Đường hồi quy ước lượng:**

$$\hat{Y}_i = \hat{b}_0 + \hat{b}_1 X_i$$

**Hệ số OLS:**

$$\hat{b}_1 = \frac{Cov_{XY}}{\sigma_X^2} \qquad \hat{b}_0 = \bar{Y} - \hat{b}_1\bar{X}$$

**Diễn giải:**
- $\hat{b}_0$ (intercept) = giá trị của $Y$ khi $X = 0$
- $\hat{b}_1$ (slope) = sự thay đổi trong $Y$ khi $X$ thay đổi 1 đơn vị

**Cross-sectional vs Time-series:**
- Cross-sectional: nhiều đơn vị tại cùng một thời điểm ($P/E_i = b_0 + b_1 \cdot EPS_i$)
- Time-series: một đơn vị theo thời gian ($\text{Rate}_t = b_0 + b_1 \cdot \text{Inflation}_t$)

## LOS 10.b — Bốn Giả Định Cốt Lõi

| Giả định | Mô tả |
|----------|-------|
| **Linearity** | Mối quan hệ giữa X và Y là tuyến tính |
| **Homoskedasticity** | Phương sai của phần dư là hằng số: $\sigma_\epsilon^2 = \text{constant}$ |
| **Independence** | Các quan sát không tương quan với nhau: $\rho_{\epsilon_i, \epsilon_j} = 0$ |
| **Normality** | Phần dư phân phối chuẩn: $\epsilon \sim N(\mu, \sigma^2)$ |

Các vi phạm được phát hiện thông qua **residual plots**.

## LOS 10.c — Đo Lường và Kiểm Định Độ Phù Hợp

### Phân Rã Tổng Bình Phương

$$SST = SSR + SSE$$

| Thành phần | Công thức | Đo lường |
|------------|-----------|----------|
| **SST** (Total) | $\sum(Y_i - \bar{Y})^2$ | Tổng biến động trong Y |
| **SSR** (Regression) | $\sum(\hat{Y}_i - \bar{Y})^2$ | Biến động được giải thích |
| **SSE** (Error) | $\sum(Y_i - \hat{Y}_i)^2$ | Biến động chưa được giải thích |

### $R^2$ (Coefficient of Determination)

$$R^2 = \frac{SSR}{SST}$$

$R^2$ càng cao → độ phù hợp càng tốt (từ 0 đến 1)

### F-Test (kiểm định ý nghĩa tổng thể của mô hình)

$$F = \frac{MSR}{MSE} = \frac{SSR/k}{SSE/(n-k-1)}$$

Với simple regression: $k=1$, do đó $df_1 = 1$, $df_2 = n-2$

- $H_0$: $b_1 = 0$ so với $H_a$: $b_1 \neq 0$
- Bác bỏ $H_0$ nếu $F > F_{\text{critical}}$ (luôn là kiểm định một phía)

### t-Test trên Slope ($b_1$)

$$t = \frac{\hat{b}_1 - B_1}{s_{\hat{b}_1}}, \quad df = n - 2$$

### t-Test trên Correlation ($\rho$)

$$t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}}, \quad df = n - 2$$

### t-Test trên Intercept ($b_0$)

$$t = \frac{\hat{b}_0 - B_0}{s_{\hat{b}_0}}, \quad df = n - 2$$

## LOS 10.d — Bảng ANOVA

| Nguồn | df | Tổng bình phương | Bình phương trung bình | F |
|-------|-----|------------------|------------------------|---|
| Regression | $k = 1$ | SSR | $MSR = \frac{SSR}{1}$ | $\frac{MSR}{MSE}$ |
| Error | $n-2$ | SSE | $MSE = \frac{SSE}{n-2}$ | |
| Total | $n-1$ | SST | | |

**Standard Error of Estimate:**

$$SEE = \sqrt{MSE} = \sqrt{\frac{SSE}{n-2}}$$

SEE càng nhỏ → độ phù hợp càng tốt.

## LOS 10.f — Các Dạng Hàm

| Mô hình | Phương trình | Diễn giải $b_1$ |
|---------|-------------|-----------------|
| **Lin-lin** | $Y = b_0 + b_1 X$ | X tăng 1 đơn vị → Y tăng $b_1$ đơn vị |
| **Log-lin** | $\ln Y = b_0 + b_1 X$ | X tăng 1 đơn vị → Y tăng $b_1 \times 100\%$ |
| **Lin-log** | $Y = b_0 + b_1 \ln X$ | X tăng 1% → Y tăng $b_1/100$ đơn vị |
| **Log-log** | $\ln Y = b_0 + b_1 \ln X$ | X tăng 1% → Y tăng $b_1\%$ (elasticity) |

## Connections

- Xây dựng trên: [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — t-test, F-test]]
- Sử dụng: [[quantitative-methods/modules/m03-statistical-measures/index|M03 — Correlation, Variance]]
- Liên quan: [[quantitative-methods/modules/m09-parametric-tests/index|M09 — Testing correlation significance]]