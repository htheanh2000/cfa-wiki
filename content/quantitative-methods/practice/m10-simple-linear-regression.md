---
title: "Practice: M10 — Simple Linear Regression"
type: practice
subject: quantitative-methods
module: M10
created: 2026-04-09
updated: 2026-04-09
tags: [practice, regression, ols, anova, r-squared, prediction-interval]
---

# Practice: M10 — Simple Linear Regression

**Module**: [[quantitative-methods/modules/m10-simple-linear-regression/index|M10]]
**Glossary**: [[quantitative-methods/glossary/m10-simple-linear-regression|M10 Terms]]

---

## Topic 1: Introduction to Linear Regression

**Question 1**: Stellar Energy [[quantitative-methods/glossary/m10-simple-linear-regression#Simple Linear Regression|regression]] with CPIENG (energy price index):

| | Coefficients | Standard error | t-statistic |
|---|---|---|---|
| [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|Intercept]] | 0.0138 | 0.0046 | 3.0275 |
| CPIENG (%) | −0.6486 | 0.2818 | −2.3014 |

[[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] = 0.0211, [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|Standard error]] = 0.0710, n = 248

Critical values: one-sided ±1.651, two-sided ±1.967

If CPIENG decreases by 1.0%, the expected return on Stellar is closest to:

A. 0.0073 (0.73%)
B. 0.0138 (1.38%)
C. 0.0203 (2.03%)

> [!answer]- Answer
> **C.** $\hat{Y} = 0.0138 + (-0.6486)(-0.01) = 0.0138 + 0.006486 = 0.0203$ or 2.03%
> When CPIENG decreases 1%, the negative slope means Stellar returns increase.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Trong [[quantitative-methods/glossary/m10-simple-linear-regression#Simple Linear Regression|simple linear regression]], phương trình dự đoán là $\hat{Y} = b_0 + b_1 X$, trong đó $b_0$ là [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|intercept]] và $b_1$ là [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope]]. Khi $X$ thay đổi 1 đơn vị, $\hat{Y}$ thay đổi $b_1$ đơn vị. Dấu của slope quan trọng: slope âm nghĩa là quan hệ nghịch chiều.
>
> **Tại sao C đúng — cách tính:**
> - $b_1 = -0.6486$ (slope âm: khi CPIENG tăng, return Stellar giảm, và ngược lại)
> - CPIENG giảm 1% → $\Delta X = -0.01$
> - $\hat{Y} = 0.0138 + (-0.6486)(-0.01) = 0.0138 + 0.006486 = 0.02029 \approx 2.03\%$
> - Hai số âm nhân nhau ra dương → CPIENG giảm → return Stellar **tăng**
>
> **Tại sao B sai:** 0.0138 = 1.38% chỉ là intercept ($b_0$) — giá trị này là expected return khi CPIENG = 0, không phải khi CPIENG giảm 1%.
>
> **Tại sao A sai:** 0.0073 là kết quả sai dấu — bằng $0.0138 - 0.006486$. Lỗi này xảy ra nếu tính $\hat{Y} = 0.0138 + (-0.6486)(+0.01)$, nhầm lẫn chiều thay đổi của X.

---

**Question 2**: Which of the following is **least likely** an assumption of simple linear regression?

A. The variance of the error terms each period remains the same
B. The error terms from a regression are positively correlated
C. Values of the [[quantitative-methods/glossary/m10-simple-linear-regression#Independent Variable|independent variable]] are not correlated with the error term

> [!answer]- Answer
> **B.** One key assumption is that residuals are **uncorrelated** (independence). Positively correlated errors would violate this assumption. A describes [[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|homoskedasticity]] (true assumption). C is also a valid assumption.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Các giả định cơ bản của [[quantitative-methods/glossary/m10-simple-linear-regression#Simple Linear Regression|OLS regression]] (Gauss-Markov assumptions):
> 1. Quan hệ tuyến tính giữa Y và X
> 2. **Homoskedasticity** — phương sai sai số không đổi: $Var(\epsilon_i) = \sigma^2$ (hằng số)
> 3. **Independence** — sai số độc lập với nhau: $Cov(\epsilon_i, \epsilon_j) = 0$ cho $i \neq j$
> 4. Sai số độc lập với biến độc lập X
> 5. Sai số phân phối chuẩn (cho inference)
>
> **Tại sao B là "least likely an assumption" (vi phạm giả định):** Giả định thực sự là sai số **không tương quan** với nhau. Nếu sai số dương tương quan (positively correlated residuals), đây là **serial correlation / autocorrelation** — vi phạm giả định independence. B mô tả một **vi phạm**, không phải một giả định.
>
> **Tại sao A là giả định đúng:** Phương sai sai số không đổi = [[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|homoskedasticity]] — đây là giả định chuẩn của OLS. Vi phạm gọi là heteroskedasticity.
>
> **Tại sao C là giả định đúng:** Nếu X tương quan với sai số $\epsilon$, OLS ước lượng sẽ bị **biased** (lệch) — đây là vấn đề nghiêm trọng. Giả định $Cov(X_i, \epsilon_i) = 0$ là cần thiết để OLS unbiased.

---

## Topic 2: Goodness of Fit

**Question 3**: Regression of mid-cap stock returns on S&P 500 returns:

| | Coefficients | Std Error | t-value |
|---|---|---|---|
| Intercept | 1.71 | 2.950 | 0.58 |
| S&P 500 | 1.52 | 0.130 | 11.69 |

$R^2 = 0.599$

The correlation coefficient between mid-cap returns and S&P 500 returns was:

A. 0.599
B. 0.774
C. 0.130

> [!answer]- Answer
> **B.** For simple linear regression: $r = \sqrt{R^2} = \sqrt{0.599} = 0.774$
> (Positive because slope is positive)

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Trong **simple linear regression** (chỉ một biến độc lập), [[quantitative-methods/glossary/m10-simple-linear-regression#R²|R²]] = $r^2$ (bình phương của correlation coefficient). Do đó: $r = \sqrt{R^2}$. Dấu của $r$ được xác định bởi dấu của slope coefficient $b_1$.
>
> **Tại sao B đúng:** $r = \sqrt{0.599} = 0.7740$. Vì slope = 1.52 > 0 (dương), correlation cũng dương → $r = +0.774$.
>
> **Tại sao A sai:** 0.599 là $R^2$, không phải $r$. Đây là lỗi nhầm lẫn phổ biến — $R^2$ và $r$ là hai đại lượng khác nhau ($R^2 = r^2$, không phải $R^2 = r$).
>
> **Tại sao C sai:** 0.130 là standard error của slope coefficient — không liên quan đến correlation coefficient.
>
> **Lưu ý quan trọng:** Mối quan hệ $r = \sqrt{R^2}$ **chỉ đúng với simple linear regression**. Trong multiple regression (nhiều biến X), R² không còn bằng bình phương của một correlation coefficient đơn lẻ.

---

**Question 4**: From the Stellar/CPIENG regression, which conclusion is **incorrect**?

A. The intercept is statistically different from zero at 0.05 level
B. In the month after CPIENG declines, Stellar's common stock is expected to exhibit a positive return
C. The [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope]] and intercept coefficients are not statistically different from zero at 0.05

> [!answer]- Answer
> **C.** The intercept t-stat = 3.0275 > 1.967 → significant. The slope t-stat = |−2.3014| > 1.967 → also significant. So C is incorrect — both ARE statistically different from zero.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Kiểm định ý nghĩa thống kê của hệ số hồi quy: so sánh |t-statistic| với critical value. Nếu |t-stat| > $t_{\text{critical}}$, hệ số **có ý nghĩa thống kê** (statistically different from zero). Dùng two-sided critical value (±1.967) vì kiểm định $H_a: b \neq 0$.
>
> **Tại sao C là kết luận sai (và đây là đáp án):**
> - Intercept: |t| = 3.0275 > 1.967 → **có ý nghĩa** → khác 0
> - Slope: |t| = |-2.3014| = 2.3014 > 1.967 → **có ý nghĩa** → khác 0
> - Vậy C nói "không có ý nghĩa" là **sai hoàn toàn**
>
> **Tại sao A đúng (không phải đáp án):** Intercept t-stat = 3.0275 > 1.967 → intercept có ý nghĩa ở mức 5% → A là kết luận **đúng**.
>
> **Tại sao B đúng (không phải đáp án):** Slope = −0.6486 < 0 → khi CPIENG giảm ($\Delta X < 0$), $b_1 \times \Delta X > 0$ → expected return tăng → B là kết luận **đúng**.
>
> **Mẹo làm bài:** Câu hỏi "which is incorrect" → tìm statement mâu thuẫn với số liệu. Luôn kiểm tra từng phát biểu bằng dữ liệu trong bảng.

---

## Topic 3: ANOVA Table

**Question 5**: Regression with 5 observations. SSR = 88.0, SSE = 7.2. Complete the [[quantitative-methods/glossary/m10-simple-linear-regression#ANOVA|ANOVA]] table and answer:

A. Sample variance of dependent variable?
B. Coefficient of determination ($R^2$)?
C. What hypothesis does [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-test]] test?
D. Is F-test significant at 0.05?
E. [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|Standard error of estimate (SEE)]]?

> [!answer]- Answer
> SST = 88.0 + 7.2 = 95.2
> A. Sample variance = $\frac{SST}{n-1} = \frac{95.2}{4} = 23.8$
> B. $R^2 = \frac{SSR}{SST} = \frac{88.0}{95.2} = 0.9244$ or 92.44%
> C. F-test tests $H_0: b_1 = 0$ (slope = 0, no linear relationship)
> D. $MSR = \frac{88.0}{1} = 88.0$, $MSE = \frac{7.2}{3} = 2.4$
>    $F = \frac{88.0}{2.4} = 36.67$
>    $F_{\text{critical}}(1, 3, 0.05)$ ≈ 10.13 → $36.67 > 10.13$ → **Reject $H_0$**, significant
> E. $SEE = \sqrt{MSE} = \sqrt{2.4} = 1.549$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#ANOVA|ANOVA table]] trong regression phân tách tổng biến thiên của Y thành: SST (total) = SSR (explained by regression) + SSE (unexplained/residual). Các degrees of freedom: SSR có df = k (số biến X = 1), SSE có df = n - k - 1, SST có df = n - 1.
>
> **Bảng ANOVA hoàn chỉnh (n=5, k=1):**
> | Source | SS | df | MS | F |
> |---|---|---|---|---|
> | Regression (SSR) | 88.0 | 1 | 88.0 | 36.67 |
> | Error (SSE) | 7.2 | 3 | 2.4 | |
> | Total (SST) | 95.2 | 4 | | |
>
> **Giải thích từng phần:**
> - **A — Sample variance:** $s^2_Y = SST/(n-1) = 95.2/4 = 23.8$ — đây là variance của Y trước khi hồi quy
> - **B — R²:** $R^2 = SSR/SST = 88.0/95.2 = 92.4\%$ — mô hình giải thích 92.4% biến thiên của Y
> - **C — F-test hypothesis:** Luôn kiểm định $H_0: b_1 = 0$ (không có quan hệ tuyến tính). Trong multiple regression: $H_0: b_1 = b_2 = ... = b_k = 0$
> - **D — F significance:** $F = MSR/MSE = 88.0/2.4 = 36.67 \gg 10.13$ → bác bỏ mạnh $H_0$ → mô hình có ý nghĩa
> - **E — SEE:** $SEE = \sqrt{MSE} = \sqrt{2.4} = 1.549$ — đơn vị giống Y, đo lường sai số dự đoán trung bình

---

## Topic 4: Prediction Interval

**Question 6**: US CPI regression: $R^2 = 0.9859$, SEE = 0.0009, n = 60, intercept = 0.0001, slope = 0.9830. For a CPI consensus forecast of 2.8, calculate the 95% [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|prediction interval]].

Additional info: t-critical = 2.002, $s_f = 0.7539 \times 0.001 = 0.00075$, $\bar{X} = 1.3350$

> [!answer]- Answer
> Predicted value: $\hat{Y} = 0.0001 + 0.9830 \times 2.8 = 2.7525$
> Prediction interval: $\hat{Y} \pm t_{\text{critical}} \times s_f$
> $= 2.7525 \pm 2.002 \times 0.00075$
> $= 2.7525 \pm 0.0015$
> → **95% PI: 2.7510 to 2.7540**
> Closest to answer A: 2.7506 to 2.7544

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|Prediction interval (PI)]] cho một **giá trị Y cụ thể** (individual observation) tại $X = X^*$ rộng hơn confidence interval cho mean Y vì nó phải tính cả uncertainty của: (1) ước lượng conditional mean, và (2) sai số ngẫu nhiên của cá thể đó. Công thức: $\hat{Y} \pm t_{\text{critical}} \times s_f$, trong đó $s_f$ bao gồm cả SEE.
>
> **Cách tính chi tiết:**
> - **Bước 1 — Predicted value:** $\hat{Y} = 0.0001 + 0.9830 \times 2.8 = 0.0001 + 2.7524 = 2.7525$
> - **Bước 2 — Prediction interval:** $2.7525 \pm 2.002 \times 0.00075 = 2.7525 \pm 0.0015$
> - → 95% PI: **2.7510 đến 2.7540**
>
> **Phân biệt Confidence Interval vs Prediction Interval:**
> - **CI cho mean Y:** Khoảng tin cậy cho **giá trị trung bình** của Y tại $X = X^*$ — hẹp hơn
> - **PI cho individual Y:** Khoảng dự đoán cho **một quan sát cụ thể** tại $X = X^*$ — rộng hơn vì thêm variance của sai số ngẫu nhiên $\epsilon$
>
> **Ý nghĩa của $R^2 = 98.6\%$:** Mô hình rất tốt, giải thích gần như toàn bộ biến thiên. Vì vậy PI rất hẹp (±0.0015 là rất nhỏ so với giá trị 2.75) — model fit tốt dẫn đến dự đoán chính xác.
