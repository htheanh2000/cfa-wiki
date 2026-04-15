---
title: "Practice: M05 — Portfolio Mathematics"
type: practice
subject: quantitative-methods
module: M05
created: 2026-04-09
updated: 2026-04-09
tags: [practice, portfolio, variance, safety-first]
---

# Practice: M05 — Portfolio Mathematics

**Module**: [[quantitative-methods/modules/m05-portfolio-mathematics/index|M05]]
**Formulas**: [[quantitative-methods/formulas/portfolio-math|Portfolio Math Formulas]]
**Glossary**: [[quantitative-methods/glossary/m05-portfolio-math|M05 Terms]]

---

**Question 1**: Portfolio: 30% stocks ($\sigma = 20\%$), 70% bonds ($\sigma = 12\%$), $\rho = 0.6$. Calculate [[quantitative-methods/glossary/m05-portfolio-math#Portfolio Variance|portfolio standard deviation]].

> [!answer]- Answer
> $\sigma_p^2 = (0.3)^2(0.20)^2 + (0.7)^2(0.12)^2 + 2(0.3)(0.7)(0.20)(0.12)(0.6)$
> $= 0.0036 + 0.00706 + 0.00605 = 0.01671$
> $\sigma_p = \sqrt{0.01671} = 12.92\%$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m05-portfolio-math#Portfolio Variance|Portfolio variance]] của danh mục 2 tài sản: $\sigma_p^2 = w_1^2\sigma_1^2 + w_2^2\sigma_2^2 + 2w_1w_2\sigma_1\sigma_2\rho_{12}$. Số hạng thứ ba (số hạng tương tác) phụ thuộc vào correlation — đây là nguồn gốc của lợi ích đa dạng hóa.
>
> **Tại sao đáp án đúng:** Thay số: $(0.3)^2(0.20)^2 = 0.0036$; $(0.7)^2(0.12)^2 = 0.007056$; số hạng tương tác $= 2(0.3)(0.7)(0.20)(0.12)(0.6) = 0.006048$. Tổng = $0.01670 \to \sigma_p = 12.92\%$.
>
> **Điểm quan trọng về đa dạng hóa:** Weighted average std dev = $0.3(20\%) + 0.7(12\%) = 14.4\%$. Portfolio std dev thực tế 12.92% **thấp hơn** mức trung bình có trọng số — đây chính là lợi ích đa dạng hóa. Nếu $\rho = 1$, portfolio std dev sẽ đúng bằng 14.4%.

---

**Question 2**: A client has £1,350,000 portfolio and wants to withdraw £50,000 without reducing principal. The shortfall level $R_L = \frac{50,000}{1,350,000} = 3.70\%$.

| Allocation | A   | B   | C   | D   |
| ---------- | --- | --- | --- | --- |
| $E(R)$     | 16% | 12% | 10% | 9%  |
| $\sigma$   | 24% | 17% | 12% | 11% |

Which allocation is best by [[quantitative-methods/glossary/m05-portfolio-math#Roy's Safety-First Criterion|Safety-First criterion]]?

> [!answer]- Answer
> $SFRatio_A = \frac{16 - 3.70}{24} = 0.513$
> $SFRatio_B = \frac{12 - 3.70}{17} = 0.488$
> $SFRatio_C = \frac{10 - 3.70}{12} = 0.525$ ← **Highest**
> $SFRatio_D = \frac{9 - 3.70}{11} = 0.482$
> **Allocation C** — highest [[quantitative-methods/glossary/m05-portfolio-math#Safety-First Ratio|SFRatio]] minimizes probability of shortfall.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m05-portfolio-math#Roy's Safety-First Criterion|Roy's Safety-First Criterion]] chọn danh mục có xác suất thấp nhất để lợi nhuận rơi xuống dưới mức tối thiểu (shortfall level $R_L$). [[quantitative-methods/glossary/m05-portfolio-math#Safety-First Ratio|SFRatio]] = $\frac{E(R_p) - R_L}{\sigma_p}$ — giống Sharpe ratio nhưng thay risk-free rate bằng shortfall level.
>
> **Tại sao C đúng:** Shortfall level = $50,000 / £1,350,000 = 3.70\%$. Tính SFRatio cho 4 phương án, Allocation C đạt cao nhất (0.525). SFRatio cao hơn → khoảng cách giữa expected return và $R_L$ lớn hơn so với rủi ro → xác suất shortfall thấp hơn.
>
> **Lưu ý:** Allocation A có expected return cao nhất (16%) nhưng SFRatio thấp hơn C vì độ biến động rất lớn (24%). Đây là ví dụ điển hình: lợi nhuận cao không tự động là tốt nhất cho mục tiêu bảo toàn vốn. Cần cân bằng giữa return và risk so với threshold.

---

**Question 3**: If two assets have $\rho = -1$, the portfolio standard deviation:

A. Is always zero
B. Can be reduced to zero with the right weights
C. Equals the weighted average of individual standard deviations

> [!answer]- Answer
> **B.** With $\rho = -1$, there exist weights that make $\sigma_p = 0$ (perfect negative correlation allows full risk elimination).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Correlation hoàn hảo âm ($\rho = -1$) là trường hợp lý tưởng nhất của đa dạng hóa. Khi đó tồn tại một bộ trọng số cụ thể để $\sigma_p = 0$, nghĩa là toàn bộ rủi ro được triệt tiêu.
>
> **Tại sao B đúng:** Với $\rho = -1$, công thức portfolio std dev trở thành: $\sigma_p = |w_1\sigma_1 - w_2\sigma_2|$. Đặt bằng 0: $w_1 = \frac{\sigma_2}{\sigma_1 + \sigma_2}$ và $w_2 = \frac{\sigma_1}{\sigma_1 + \sigma_2}$. Các trọng số này luôn tồn tại và hợp lệ (dương, tổng = 1).
>
> **Tại sao A sai:** Không phải **luôn luôn** bằng 0 — chỉ bằng 0 với **đúng bộ trọng số** xác định. Với trọng số khác, $\sigma_p > 0$ ngay cả khi $\rho = -1$.
>
> **Tại sao C sai:** $\sigma_p$ bằng weighted average chỉ khi $\rho = +1$ (tương quan dương hoàn hảo — không có lợi ích đa dạng hóa). Đây là trường hợp tệ nhất.
>
> **Thực tế:** Trong thị trường thực, $\rho = -1$ gần như không tồn tại — nhưng assets với correlation âm (như trái phiếu và cổ phiếu trong một số giai đoạn) vẫn mang lại lợi ích đa dạng hóa đáng kể.
