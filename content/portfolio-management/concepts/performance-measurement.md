---
title: Performance Measurement
type: concept
subject: portfolio-management
module: "M02"
created: 2026-04-12
updated: 2026-04-12
tags: [Sharpe, Treynor, Jensen-alpha, M-squared, performance]
---

# Performance Measurement

## Overview

Các thước đo hiệu suất đánh giá lợi nhuận đã điều chỉnh theo rủi ro. Việc lựa chọn thước đo phụ thuộc vào việc danh mục đầu tư đại diện cho **toàn bộ khoản đầu tư** của nhà đầu tư (dùng total risk) hay chỉ là một **sub-portfolio** (dùng systematic risk).

## Sharpe Ratio

$$\text{Sharpe ratio} = \frac{R_p - R_f}{\sigma_p}$$

trong đó:
- $R_p$ = lợi nhuận danh mục
- $R_f$ = lãi suất phi rủi ro
- $\sigma_p$ = total risk (độ lệch chuẩn)

**Khi nào dùng**: Đánh giá một danh mục là **toàn bộ** khoản đầu tư của nhà đầu tư (total risk là yếu tố quan trọng).

- Giá trị càng cao càng tốt
- Là độ dốc của CAL
- Sử dụng **total risk** ở mẫu số

## Treynor Ratio

$$\text{Treynor ratio} = \frac{R_p - R_f}{\beta_p}$$

trong đó $\beta_p$ = beta của danh mục (systematic risk).

**Khi nào dùng**: Đánh giá một **sub-portfolio** hoặc quỹ trong một danh mục đa dạng hóa rộng hơn (chỉ systematic risk là quan trọng vì unsystematic risk đã được đa dạng hóa đi ở cấp độ tổng danh mục).

- Giá trị càng cao càng tốt
- Sử dụng **systematic risk** ở mẫu số

## M-Squared ($M^2$)

$$M^2 = (R_p - R_f) \frac{\sigma_m}{\sigma_p} - (R_m - R_f)$$

trong đó:
- $\sigma_m$ = độ lệch chuẩn của thị trường
- $\sigma_p$ = độ lệch chuẩn của danh mục

**Diễn giải**:
- Tăng hoặc giảm đòn bẩy của danh mục để khớp với mức rủi ro thị trường, sau đó so sánh lợi nhuận
- Được biểu thị theo **đơn vị phần trăm** (dễ diễn giải hơn Sharpe)
- $M^2 > 0$ → danh mục vượt trội thị trường trên cơ sở điều chỉnh rủi ro
- $M^2 < 0$ → danh mục kém hơn thị trường

**Khi nào dùng**: Giống các trường hợp dùng Sharpe (total risk), nhưng cung cấp cách diễn giải theo **lợi nhuận phần trăm**.

**Mối quan hệ với Sharpe**:

$$M^2 = (\text{Sharpe}_p - \text{Sharpe}_m) \times \sigma_m$$

Xếp hạng theo $M^2$ luôn đồng nhất với xếp hạng theo Sharpe ratio.

## Jensen's Alpha

$$\alpha_p = R_p - [R_f + \beta_p (R_m - R_f)]$$

trong đó phần trong ngoặc là lợi nhuận kỳ vọng theo CAPM.

**Diễn giải**:
- $\alpha > 0$ → nhà quản lý tạo ra giá trị thặng dư (vượt dự báo CAPM)
- $\alpha = 0$ → hiệu suất đúng như CAPM dự báo
- $\alpha < 0$ → nhà quản lý làm giảm giá trị

**Khi nào dùng**: Đánh giá kỹ năng của nhà quản lý trên cơ sở **điều chỉnh theo systematic risk** (trong ngữ cảnh sub-portfolio).

## Summary Comparison

| Thước đo | Loại rủi ro | Mẫu số | Phù hợp nhất | Đầu ra |
|---|---|---|---|---|
| Sharpe | Total ($\sigma$) | $\sigma_p$ | Tổng danh mục | Ratio |
| Treynor | Systematic ($\beta$) | $\beta_p$ | Sub-portfolio | Ratio |
| $M^2$ | Total ($\sigma$) | — (đòn bẩy hóa) | Tổng danh mục | Phần trăm |
| Jensen's $\alpha$ | Systematic ($\beta$) | — (phần dư CAPM) | Sub-portfolio / nhà quản lý | Phần trăm |

## Key Distinctions

- **Thước đo total risk** (Sharpe, $M^2$): phù hợp khi danh mục được đánh giá là khoản nắm giữ **duy nhất** của nhà đầu tư
- **Thước đo systematic risk** (Treynor, Jensen's $\alpha$): phù hợp khi danh mục là một trong **nhiều** khoản nắm giữ và unsystematic risk đã được đa dạng hóa đi
- Sharpe và Treynor cung cấp **xếp hạng tương đối** (ratio)
- $M^2$ và Jensen's $\alpha$ cung cấp **thước đo tuyệt đối** (phần trăm lợi nhuận)

## See Also

- [[portfolio-management/concepts/capm-and-sml|CAPM and SML]]
- [[portfolio-management/formulas/pm-formulas|PM Master Formula Sheet]]
- [[portfolio-management/glossary/pm-m02|Glossary M02]]