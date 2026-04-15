---
title: "Practice: M03 — Statistical Measures"
type: practice
subject: quantitative-methods
module: M03
created: 2026-04-09
updated: 2026-04-09
tags: [practice, statistics, skewness, kurtosis, correlation]
---

# Practice: M03 — Statistical Measures

**Module**: [[quantitative-methods/modules/m03-statistical-measures/index|M03]]
**Formulas**: [[quantitative-methods/formulas/statistics|Statistics Formulas]]
**Glossary**: [[quantitative-methods/glossary/m03-statistical-measures|M03 Terms]]

---

**Question 1**: An analyst evaluates portfolio returns, bond index returns, and real estate index returns:

| | Portfolio | Bond Index | Real Estate |
|---|---|---|---|
| Arithmetic average | 5.5 | 3.2 | 7.8 |
| [[quantitative-methods/glossary/m03-statistical-measures#Standard Deviation|Standard deviation]] | 8.2 | 3.4 | 10.3 |

Combined std dev of portfolio + bond = 18.9, portfolio + real estate = −55.9.

Without calculating the [[quantitative-methods/glossary/m03-statistical-measures#Correlation|correlation coefficient]], the correlation of portfolio returns and bond index returns is:

A. Negative
B. Zero
C. Positive

> [!answer]- Answer
> **C. Positive.** The combined standard deviation (18.9) is positive, and the real estate combination is negative (−55.9), indicating the portfolio-bond correlation is positive while portfolio-real estate correlation is negative.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Correlation|Correlation]] ($\rho$) đo mức độ và chiều hướng đồng biến giữa hai biến. Trong công thức phương sai danh mục: $\sigma_p^2 = w_1^2\sigma_1^2 + w_2^2\sigma_2^2 + 2w_1w_2\sigma_1\sigma_2\rho_{12}$, dấu của $\rho$ quyết định phương sai danh mục lớn hơn hay nhỏ hơn tổng có trọng số.
>
> **Tại sao C đúng:** Số liệu kết hợp portfolio + bond là dương (18.9), cho thấy số hạng $2w_1w_2\sigma_1\sigma_2\rho$ dương → $\rho > 0$. Ngược lại, portfolio + real estate cho giá trị âm (−55.9), chứng tỏ $\rho < 0$ cho cặp đó.
>
> **Tại sao A sai:** Correlation âm sẽ làm giảm combined std dev xuống dưới mức tổng bình phương có trọng số — không khớp với kết quả dương 18.9.
>
> **Tại sao B sai:** Correlation bằng 0 chỉ đơn giản là loại bỏ số hạng tương tác, không thể tạo ra giá trị âm −55.9.

---

**Question 2**: A distribution with excess [[quantitative-methods/glossary/m03-statistical-measures#Kurtosis|kurtosis]] > 0 is called:

A. Platykurtic
B. Mesokurtic
C. [[quantitative-methods/glossary/m03-statistical-measures#Leptokurtic|Leptokurtic]]

> [!answer]- Answer
> **C. Leptokurtic** — fat tails, higher probability of extreme outcomes. Important for risk management as it means more extreme returns than a normal distribution would predict.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Kurtosis|Kurtosis]] đo độ "nhọn" của phân phối và độ dày của đuôi. Excess kurtosis = Kurtosis − 3 (so với phân phối chuẩn có kurtosis = 3).
>
> **Tại sao C đúng:** [[quantitative-methods/glossary/m03-statistical-measures#Leptokurtic|Leptokurtic]] có excess kurtosis > 0 → đuôi dày hơn (fat tails) và đỉnh nhọn hơn so với phân phối chuẩn. Trong quản lý rủi ro tài chính, đây là đặc tính quan trọng vì các sự kiện cực đoan xảy ra thường xuyên hơn mô hình chuẩn dự đoán.
>
> **Tại sao A sai:** Platykurtic có excess kurtosis < 0 → đuôi mỏng hơn, phân phối "phẳng" hơn.
>
> **Tại sao B sai:** Mesokurtic là phân phối chuẩn với excess kurtosis = 0 (kurtosis = 3).

---

**Question 3**: For a negatively [[quantitative-methods/glossary/m03-statistical-measures#Skewness|skewed]] distribution, the relationship between mean, [[quantitative-methods/glossary/m03-statistical-measures#Median|median]], and [[quantitative-methods/glossary/m03-statistical-measures#Mode|mode]] is:

A. Mean > Median > Mode
B. Mode > Median > Mean
C. Mean = Median = Mode

> [!answer]- Answer
> **B.** Negative (left) skew: Mode > Median > Mean. The left tail pulls the mean down.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Skewness|Skewness]] âm (negative skew) nghĩa là phân phối có đuôi dài về phía trái. [[quantitative-methods/glossary/m03-statistical-measures#Mode|Mode]] là giá trị xuất hiện nhiều nhất (đỉnh của phân phối), [[quantitative-methods/glossary/m03-statistical-measures#Median|Median]] là giá trị giữa, còn Mean bị kéo về phía đuôi.
>
> **Tại sao B đúng:** Khi phân phối lệch trái, đuôi trái kéo mean xuống thấp hơn median, trong khi mode nằm ở đỉnh cao nhất — xa nhất so với đuôi. Do đó: Mode > Median > Mean.
>
> **Tại sao A sai:** Mean > Median > Mode là thứ tự của phân phối lệch **phải** (positive skew) — đuôi phải kéo mean lên cao.
>
> **Tại sao C sai:** Mean = Median = Mode chỉ đúng với phân phối đối xứng hoàn toàn (như phân phối chuẩn).
>
> **Mẹo nhớ:** Đuôi kéo về đâu thì mean bị kéo về đó. Trong tài chính: lợi nhuận cổ phiếu thường có negative skew (một số thua lỗ lớn tạo đuôi trái dài).
