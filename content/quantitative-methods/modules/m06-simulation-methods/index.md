---
title: "M06 — Simulation Methods"
type: module
subject: quantitative-methods
module: M06
los: ["6.a", "6.b", "6.c", "Pre.i", "Pre.ii"]
created: 2026-04-09
updated: 2026-04-09
tags: [lognormal, t-distribution, chi-square, f-distribution, monte-carlo, bootstrap]
---

# Module 6: Simulation Methods

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 255–273

## Learning Outcomes

| LOS | Mô tả |
|-----|-------|
| 6.a | Mối quan hệ giữa phân phối chuẩn và lognormal; tại sao lognormal được dùng để mô hình hóa giá tài sản |
| Pre.i | Tính chất của Student's t-distribution và degrees of freedom |
| Pre.ii | Tính chất của Chi-square và F-distribution và degrees of freedom |
| 6.b | Monte Carlo simulation và ứng dụng trong đầu tư |
| 6.c | Bootstrap resampling trong simulation |

## LOS 6.a — Lognormal Distribution

**Định nghĩa**: Được tạo ra bởi $e^X$ trong đó $X$ có phân phối chuẩn.

**Tại sao dùng lognormal cho giá tài sản?**
- Phân phối chuẩn cho phép giá trị âm → không thực tế với giá tài sản
- Lognormal bị chặn dưới bởi không → luôn dương
- Lệch phải (positively skewed)

**Mô hình giá cổ phiếu:**

$$S_T = S_0 \times e^{r_{0,T}}$$

trong đó $r_{0,T}$ = lợi suất kép liên tục (continuously compounded return) từ thời điểm 0 đến T

**Continuously compounded return:**

$$r_{t,t+1} = \ln\left(\frac{S_{t+1}}{S_t}\right) = \ln(1 + HPR_{t,t+1})$$

**Tính chất chính** (giả định lợi suất i.i.d.):
- $E(r_{0,T}) = \mu \times T$
- $\sigma(r_{0,T}) = \sigma \times \sqrt{T}$ (độ biến động (volatility) tỷ lệ với căn bậc hai của thời gian)

## Pre.i — Student's t-Distribution

| Tính chất | Chi tiết |
|-----------|---------|
| Hình dạng | Đối xứng, hình chuông (đuôi dày hơn phân phối chuẩn) |
| Degrees of freedom | $df = n - 1$ |
| Khi $df \to \infty$ | Tiệm cận phân phối chuẩn |
| Trường hợp sử dụng | Mẫu nhỏ, phương sai tổng thể chưa biết |

## Pre.ii — Chi-Square và F-Distribution

### Chi-Square ($\chi^2$)

$$\chi^2 = Z_1^2 + Z_2^2 + \cdots + Z_k^2$$

- Tổng của $k$ biến chuẩn hóa bình phương, $df = k$
- Không đối xứng (lệch phải), bị chặn dưới bởi 0

### F-Distribution

$$F = \frac{\chi_1^2 / m}{\chi_2^2 / n}$$

- Tỷ lệ giữa hai biến chi-square chia cho degrees of freedom tương ứng
- $df_{\text{num}} = m$, $df_{\text{den}} = n$, bị chặn dưới bởi 0

## LOS 6.b — Monte Carlo Simulation

**Ứng dụng**: Định giá chứng khoán phức tạp, mô phỏng VaR, mô hình hóa quỹ hưu trí, danh mục có phân phối không chuẩn

**Các bước thực hiện:**
1. Xác định mô hình với các nhân tố rủi ro
2. Xác định phân phối xác suất cho từng nhân tố rủi ro
3. Rút các số ngẫu nhiên cho từng chu kỳ con
4. Chuyển đổi thành giá mô phỏng
5. Tính payoff
6. Lặp lại nhiều lần → tính toán thống kê tổng hợp

**Hạn chế**: Kết quả chỉ tốt khi giả định đúng; không cung cấp hiểu biết phân tích; tốn nhiều tài nguyên tính toán

## LOS 6.c — Bootstrap Resampling

| Phương pháp | Cơ chế |
|-------------|--------|
| **Bootstrap** | Rút mẫu **có hoàn lại (with replacement)** từ dữ liệu gốc → xây dựng phân phối lấy mẫu |
| **Jackknife** | Loại bỏ một quan sát mỗi lần (**không hoàn lại, without replacement**) |

**Bootstrap**: Đơn giản, đại diện tốt cho tổng thể, nhưng chỉ cung cấp ước lượng thống kê

## Connections

- Xây dựng từ: [[quantitative-methods/modules/m05-portfolio-mathematics/index|M05 — Normal Distribution]]
- Mở rộng sang: [[quantitative-methods/modules/m07-estimation-and-inference/index|M07 — Estimation]]
- Các phân phối được dùng trong: [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — Hypothesis Testing]]