---
title: "M09 — Parametric Tests"
type: module
subject: quantitative-methods
module: M09
los: ["9.a", "9.b"]
created: 2026-04-09
updated: 2026-04-09
tags: [chi-square, independence, contingency-table, spearman, nonparametric]
---

# Module 9: Parametric and Non-parametric Tests of Independence

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 376–395

## Learning Outcomes

| LOS | Mô tả |
|-----|-------------|
| 9.a | Kiểm định độc lập sử dụng dữ liệu contingency table (chi-square) |
| 9.b | Kiểm định tương quan (parametric t-test và nonparametric Spearman rank) |

## LOS 9.a — Chi-Square Test of Independence

Kiểm định xem hai biến phân loại có độc lập với nhau hay không, sử dụng dữ liệu contingency table.

**Giả thuyết:**
- $H_0$: Các biến độc lập với nhau
- $H_a$: Các biến không độc lập với nhau

**Thống kê kiểm định:**

$$\chi^2 = \sum \frac{(O_{ij} - E_{ij})^2}{E_{ij}}$$

trong đó:
- $O_{ij}$ = tần suất quan sát tại ô $(i,j)$
- $E_{ij} = \frac{\text{Row total}_i \times \text{Column total}_j}{\text{Grand total}}$
- $df = (r-1)(c-1)$ với $r$ = số hàng, $c$ = số cột

**Quyết định**: Bác bỏ $H_0$ nếu $\chi^2 > \chi^2_{\text{critical}}$ (luôn kiểm định một đuôi phải)

## LOS 9.b — Tests of Correlation

### Parametric: t-test for Correlation

$$t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}}, \quad df = n - 2$$

- $H_0$: $\rho = 0$ (không có mối quan hệ tuyến tính)
- Yêu cầu tổng thể phân phối chuẩn

### Nonparametric: Spearman Rank Correlation

$$r_S = 1 - \frac{6\sum d_i^2}{n(n^2 - 1)}$$

trong đó $d_i$ = chênh lệch giữa thứ hạng của mỗi cặp quan sát

- Không yêu cầu phân phối chuẩn
- Kiểm định mối quan hệ đơn điệu (monotonic), không chỉ tuyến tính
- Dùng khi dữ liệu là thứ hạng (ordinal) hoặc không phân phối chuẩn

## Khi Nào Dùng Phương Pháp Nào?

| Điều kiện | Dùng |
|---|---|
| Dữ liệu phân phối chuẩn | Parametric t-test trên $r$ |
| Dữ liệu không chuẩn hoặc dạng ordinal | Spearman rank correlation |
| Kiểm định hai biến phân loại | Chi-square test of independence |

## Liên Kết

- Xây dựng từ: [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — Hypothesis Testing framework]]
- Liên quan: [[quantitative-methods/modules/m03-statistical-measures/index|M03 — Correlation]] (khái niệm)
- Mở rộng sang: [[quantitative-methods/modules/m10-simple-linear-regression/index|M10 — Regression]] (kiểm định ý nghĩa thống kê của $r$)