---
title: "Portfolio Risk"
type: concept
subject: quantitative-methods
module: M05
created: 2026-04-09
updated: 2026-04-09
tags: [portfolio, variance, covariance, correlation, diversification, safety-first]
---

# Portfolio Risk

## Tổng quan

Lý thuyết danh mục hiện đại (Modern portfolio theory) dựa trên nhận thức rằng việc kết hợp các tài sản có thể giảm rủi ro danh mục xuống dưới mức bình quân gia quyền của rủi ro từng tài sản riêng lẻ — miễn là các tài sản không cùng biến động hoàn toàn đồng bộ. Toán học về rủi ro danh mục, tập trung vào [[quantitative-methods/glossary/m05-portfolio-math#Covariance (Portfolio)|covariance]] và [[quantitative-methods/glossary/m05-portfolio-math#Correlation (Portfolio)|correlation]] giữa lợi suất các tài sản, là công cụ định lượng cốt lõi trong xây dựng danh mục, phân bổ tài sản và quản lý rủi ro.

## Portfolio Expected Return

[[quantitative-methods/glossary/m05-portfolio-math#Portfolio Expected Return|Portfolio expected return]] là bình quân gia quyền đơn giản:

$$E(R_p) = \sum_{i=1}^{n} w_i E(R_i)$$

trong đó $w_i$ là trọng số danh mục của tài sản $i$. Khác với portfolio variance, expected return chỉ phụ thuộc vào expected return và trọng số của từng tài sản riêng lẻ — không phụ thuộc vào mối quan hệ giữa các tài sản.

## Portfolio Variance và Vai trò của Covariance

Portfolio variance **không** đơn thuần là bình quân gia quyền của các variance riêng lẻ. Nó phụ thuộc vào tất cả các cặp [[quantitative-methods/glossary/m05-portfolio-math#Covariance (Portfolio)|covariance]]:

$$\sigma_p^2 = \sum_{i=1}^{n} \sum_{j=1}^{n} w_i w_j \text{Cov}(R_i, R_j)$$

Với **danh mục hai tài sản**, công thức mở rộng thành:

$$\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2w_1 w_2 \text{Cov}(R_1, R_2)$$

Thay $\text{Cov}(R_1, R_2) = \rho_{12} \sigma_1 \sigma_2$:

$$\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2w_1 w_2 \rho_{12} \sigma_1 \sigma_2$$

[[quantitative-methods/glossary/m05-portfolio-math#Correlation (Portfolio)|Correlation]] $\rho_{12}$ là yếu tố then chốt. Khi $\rho_{12}$ giảm, portfolio variance giảm với cùng một bộ trọng số tài sản. Ba trường hợp biên là:

| Correlation | Ảnh hưởng đến rủi ro danh mục |
|-------------|-------------------------------|
| $\rho = +1$ | Không có lợi ích đa dạng hóa; rủi ro danh mục = bình quân gia quyền rủi ro từng tài sản |
| $0 < \rho < 1$ | Lợi ích đa dạng hóa một phần; rủi ro < bình quân gia quyền |
| $\rho = -1$ | Đa dạng hóa tối đa; có thể xây dựng danh mục zero-variance với trọng số phù hợp |

## Diversification Benefit

**[[quantitative-methods/glossary/m05-portfolio-math#Diversification Benefit|Diversification benefit]]** là mức giảm portfolio standard deviation so với bình quân gia quyền standard deviation của các tài sản riêng lẻ:

$$\text{Diversification benefit} = \bar{\sigma}_w - \sigma_p \qquad \bar{\sigma}_w = \sum_i w_i \sigma_i$$

Khi số lượng tài sản tăng lên, rủi ro phi hệ thống (idiosyncratic risk, tức rủi ro đặc thù của từng công ty) được đa dạng hóa triệt tiêu. Rủi ro còn lại — **systematic risk** — không thể loại bỏ thông qua đa dạng hóa và được bù đắp bởi market risk premium. Với danh mục gồm $n$ tài sản:

$$\sigma_p^2 = \frac{1}{n}\bar{\sigma}^2 + \frac{n-1}{n}\overline{\text{Cov}}$$

Khi $n \to \infty$, portfolio variance hội tụ về average covariance $\overline{\text{Cov}}$ — ngưỡng sàn của đa dạng hóa. Điều này cho thấy chính correlation (covariance), chứ không phải variance của từng tài sản riêng lẻ, mới là yếu tố quyết định cuối cùng của rủi ro không thể đa dạng hóa.

## Covariance và Correlation Matrices

Với danh mục gồm $n$ tài sản, [[quantitative-methods/glossary/m05-portfolio-math#Covariance Matrix|covariance matrix]] $\Sigma$ chứa toàn bộ thông tin cần thiết để tính portfolio variance:

$$\sigma_p^2 = \mathbf{w}^\top \Sigma \mathbf{w}$$

Ma trận có $n$ phần tử trên đường chéo (variances) và $\frac{n(n-1)}{2}$ phần tử ngoài đường chéo duy nhất (covariances). Khi $n$ tăng, các phần tử ngoài đường chéo chiếm ưu thế — khẳng định rằng covariances quan trọng hơn variance của từng tài sản riêng lẻ đối với các danh mục lớn.

## Các Thước đo Downside Risk

Ngoài variance, các chuyên gia thực tiễn còn sử dụng các thước đo rủi ro chỉ tính phía giảm giá trị (downside-only):
- **[[quantitative-methods/glossary/m03-statistical-measures#Target Downside Deviation|Target downside deviation]]**: Standard deviation của lợi suất dưới mức mục tiêu; chỉ phạt các kết quả bất lợi.
- **[[quantitative-methods/glossary/m05-portfolio-math#Shortfall Risk|Shortfall risk]]**: Xác suất lợi suất rơi xuống dưới mức chấp nhận được tối thiểu.
- **[[quantitative-methods/glossary/m05-portfolio-math#Roy's Safety-First Criterion|Roy's safety-first criterion]]**: Chọn danh mục có safety-first ratio cao nhất $= (E(R_p) - R_L)/\sigma_p$, tối thiểu hóa xác suất rơi xuống dưới ngưỡng $R_L$.
- **[[quantitative-methods/glossary/m06-simulation-methods#Value at Risk (VaR)|Value at Risk (VaR)]]**: Mức tổn thất tối thiểu dự kiến bị vượt qua với xác suất $\alpha$ trong một khoảng thời gian cho trước.

## Các Module Nguồn

- [[quantitative-methods/modules/m05-portfolio-math/index|M05 — Portfolio Mathematics and Distributions]] — nội dung chính
- [[quantitative-methods/modules/m03-statistical-measures/index|M03 — Statistical Measures]] — nền tảng covariance và correlation
- [[quantitative-methods/modules/m06-simulation-methods/index|M06 — Simulation Methods]] — mô phỏng Monte Carlo về rủi ro danh mục