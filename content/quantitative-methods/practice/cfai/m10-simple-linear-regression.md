---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - simple-linear-regression
  - anova
  - prediction-interval
  - r-squared
  - f-test
source: "CFAI CFA1 Quant Practice 2026, pp.310-325"
module: "[[quantitative-methods/modules/m10-simple-linear-regression/index|M10]]"
---

# M10 – Simple Linear Regression: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.310–325
**Back to module:** [[quantitative-methods/modules/m10-simple-linear-regression/index|M10]]
**Glossary**: [[quantitative-methods/glossary/m10-simple-linear-regression|M10 Terms]]

---

## Questions 1–3: ROE and Growth Opportunities

The following estimated regression equation relates **return on equity** (ROE, in %) to **growth opportunities** (GO, in %):

$$\widehat{ROE}_i = 4 + 1.8\, GO_i$$

---

## Question 1

Using this [[quantitative-methods/glossary/m10-simple-linear-regression#Simple Linear Regression|regression]], the **predicted ROE** when $GO = 10\%$ is **closest to**:

- A. 1.8%
- B. 15.8%
- C. 22.0%

> [!answer]- Answer
> **C. 22.0%**
>
> Substitute $GO = 10$ into the regression equation:
>
> $$\widehat{ROE} = 4 + 1.8 \times 10 = 4 + 18 = \mathbf{22.0\%}$$
>
> **Why A is wrong:** 1.8% is the [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]], not the predicted value.
>
> **Why B is wrong:** 15.8% = 4 + 1.8(6.6) — no basis for this.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Simple Linear Regression|Hồi quy tuyến tính đơn]] dạng $\hat{Y} = b_0 + b_1 X$: thay giá trị $X$ vào để tính **predicted value** (giá trị dự báo). $b_0$ = intercept (giá trị $Y$ khi $X=0$), $b_1$ = slope (thay đổi $Y$ khi $X$ tăng 1 đơn vị).
>
> **Tại sao C đúng:** Thay $GO = 10$ vào: $\hat{Y} = 4 + 1.8 \times 10 = 22\%$. Đây là tính toán đơn giản — không được nhầm slope với predicted value.
> **Tại sao A sai:** 1.8% là [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] $b_1$ — không phải predicted value. Slope chỉ cho biết **mức thay đổi**, không phải giá trị dự báo.
> **Tại sao B sai:** 15.8% không có cơ sở tính toán từ phương trình này với $GO = 10$.

---

## Question 2

The estimated **change in ROE** when GO changes from 5% to 6% is **closest to**:

- A. 1.8%
- B. 4.0%
- C. 5.8%

> [!answer]- Answer
> **A. 1.8%**
>
> The slope coefficient $\hat{b}_1 = 1.8$ represents the change in the [[quantitative-methods/glossary/m10-simple-linear-regression#Dependent Variable|dependent variable]] ($\widehat{ROE}$) for a **one-unit increase** in the [[quantitative-methods/glossary/m10-simple-linear-regression#Independent Variable|independent variable]] ($GO$). A change from 5% to 6% is exactly a 1% increase in GO:
>
> $$\Delta\widehat{ROE} = 1.8 \times \Delta GO = 1.8 \times 1 = \mathbf{1.8\%}$$
>
> **Verification:**
> - At $GO = 5$: $\widehat{ROE} = 4 + 1.8(5) = 13.0\%$
> - At $GO = 6$: $\widehat{ROE} = 4 + 1.8(6) = 14.8\%$
> - Difference: $14.8 - 13.0 = 1.8\%$ ✓

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|Slope coefficient]] $b_1$ là **đạo hàm** của $\hat{Y}$ theo $X$: mỗi khi $X$ tăng **1 đơn vị**, $Y$ thay đổi đúng $b_1$ đơn vị — bất kể điểm xuất phát là bao nhiêu. Đây là tính chất linear của hồi quy tuyến tính.
>
> **Tại sao A đúng:** $GO$ tăng từ 5% lên 6% = tăng 1 đơn vị → $\Delta\hat{ROE} = 1.8 \times 1 = 1.8\%$. Slope $b_1 = 1.8$ cho biết mỗi 1% tăng GO → ROE tăng 1.8%.
> **Tại sao B sai:** 4.0% là intercept $b_0$ — không phải mức thay đổi. Intercept là giá trị $\hat{Y}$ khi $X = 0$.
> **Tại sao C sai:** 5.8% = intercept (4) + slope (1.8) = nhầm lẫn giữa predicted value khi $X=1$ với mức thay đổi.

---

## Question 3

When $GO = 8\%$ and the **observed ROE = 21%**, the **residual** is **closest to**:

- A. −1.8%
- B. 2.6%
- C. 12.0%

> [!answer]- Answer
> **B. 2.6%**
>
> The residual is the difference between the observed (actual) value and the predicted (fitted) value:
>
> $$\hat{\varepsilon}_i = Y_i - \hat{Y}_i$$
>
> **Step 1 – Predicted ROE at $GO = 8$:**
>
> $$\widehat{ROE} = 4 + 1.8 \times 8 = 4 + 14.4 = 18.4\%$$
>
> **Step 2 – Residual:**
>
> $$\hat{\varepsilon} = 21\% - 18.4\% = \mathbf{2.6\%}$$
>
> The positive residual means the actual ROE (21%) **exceeds** the model's prediction (18.4%) by 2.6 percentage points.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Residual** (phần dư) = giá trị thực tế $-$ giá trị dự báo: $\hat{\varepsilon}_i = Y_i - \hat{Y}_i$. Residual dương nghĩa là actual **cao hơn** predicted (model underpredicts). Residual âm nghĩa là actual **thấp hơn** predicted (model overpredicts). Tổng tất cả residuals trong OLS = 0.
>
> **Tại sao B đúng:** Bước 1: $\hat{ROE} = 4 + 1.8 \times 8 = 18.4\%$. Bước 2: Residual = $21\% - 18.4\% = 2.6\%$. Residual dương → mô hình **underpredicts** ROE thực tế.
> **Tại sao A sai:** $-1.8\%$ là âm slope một đơn vị — không có logic tính toán cho giá trị này trong bài toán này.
> **Tại sao C sai:** $12\% = 21\% - 4\% - 5\%$ — nhầm lẫn giữa residual và predicted value thô.

---

## Question 4

**[[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|Homoskedasticity]]** is best described as a condition in which the variance of the residuals is:

- A. zero
- B. normally distributed
- C. constant across all observations

> [!answer]- Answer
> **C. constant across all observations**
>
> Homoskedasticity (from Greek: *homos* = same, *skedasis* = dispersion) is one of the key assumptions of [[quantitative-methods/glossary/m10-simple-linear-regression#OLS|ordinary least squares (OLS)]] regression. It requires that the **variance of the error term** $\varepsilon_i$ is the same for all values of the independent variable:
>
> $$\text{Var}(\varepsilon_i) = \sigma^2 \quad \forall\, i$$
>
> The violation of this assumption — **heteroskedasticity** — occurs when residual variance is not constant (e.g., larger at higher values of $X$). Heteroskedasticity does not bias OLS coefficient estimates but makes standard errors unreliable, invalidating $t$- and $F$-tests.
>
> **Why A is wrong:** A variance of zero would imply perfect prediction with no error — an unrealistic requirement. OLS does not require zero residuals.
>
> **Why B is wrong:** The **normality assumption** is a separate requirement (errors are normally distributed). Normality is distinct from homoskedasticity (constant variance). A distribution can have constant variance without being normal.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Giả định [[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|homoskedasticity]] (đồng phương sai) là một trong các giả định cốt lõi của [[quantitative-methods/glossary/m10-simple-linear-regression#OLS|OLS]]: $\text{Var}(\varepsilon_i) = \sigma^2$ hằng số với mọi $i$. Vi phạm → **heteroskedasticity** → standard errors không đáng tin → t-test và F-test không hợp lệ (dù hệ số ước lượng vẫn unbiased).
>
> **Tại sao C đúng:** Homoskedasticity = variance của error term **không đổi** qua tất cả các quan sát. Ví dụ sai phạm: variance của sai số lớn hơn với income cao (heteroskedasticity trong data tài chính).
> **Tại sao A sai:** Variance bằng 0 = không có sai số = dự báo hoàn hảo — điều này không thực tế và không phải yêu cầu của OLS.
> **Tại sao B sai:** **Normality** (phân phối chuẩn của error) là giả định **riêng biệt** với homoskedasticity (phương sai không đổi). Một phân phối có thể có variance hằng số mà không cần là phân phối chuẩn.

---

## Questions 5–8: Money Supply Growth and Policy Shift

An analyst regresses **money supply growth** (%) on an [[quantitative-methods/glossary/m10-simple-linear-regression#Indicator Variable|indicator variable]] **SHIFT** (= 0 before policy change, = 1 after policy change) using 30 observations.

| | Coefficient | Std. Error | $t$-statistic |
|-|-------------|-----------|--------------|
| [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|Intercept]] | 5.767264 | 0.445229 | 12.95 |
| SHIFT | −5.139120 | 0.629649 | −8.16 |

Critical values: one-tailed $\pm 1.701$; two-tailed $\pm 2.048$ (at 5% significance).

---

## Question 5

The variable SHIFT is best described as:

- A. an [[quantitative-methods/glossary/m10-simple-linear-regression#Indicator Variable|indicator variable]]
- B. the [[quantitative-methods/glossary/m10-simple-linear-regression#Dependent Variable|dependent variable]]
- C. a continuous variable

> [!answer]- Answer
> **A. an indicator variable**
>
> SHIFT takes only two values — **0 or 1** — to indicate the presence or absence of the policy change. Variables of this type are called **indicator variables**, **dummy variables**, or **binary variables**. They are used in regression to represent categorical distinctions (before/after, yes/no, group membership).
>
> **Why B is wrong:** SHIFT is the **[[quantitative-methods/glossary/m10-simple-linear-regression#Independent Variable|independent]]** (explanatory) variable. The dependent variable is money supply growth.
>
> **Why C is wrong:** SHIFT is not continuous — it only takes discrete values of 0 and 1.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Indicator Variable|Indicator variable]] (dummy variable) là biến nhị phân chỉ nhận giá trị 0 hoặc 1, dùng để mã hóa sự kiện/trạng thái categorical trong hồi quy. Tên gọi khác: binary variable, dummy variable. Rất phổ biến trong finance để mã hóa: trước/sau sự kiện, có/không có thuộc tính, v.v.
>
> **Tại sao A đúng:** SHIFT chỉ nhận giá trị 0 (trước thay đổi chính sách) hoặc 1 (sau thay đổi) — đây là định nghĩa điển hình của indicator variable.
> **Tại sao B sai:** SHIFT là biến **độc lập** (independent/explanatory variable). Biến phụ thuộc (dependent) là money supply growth — cái mà ta đang cố giải thích/dự báo.
> **Tại sao C sai:** SHIFT không phải continuous — nó chỉ nhận hai giá trị rời rạc (0 hoặc 1), không thể nhận mọi giá trị trên một đoạn liên tục.

---

## Question 6

The intercept of 5.767264 represents the **mean money supply growth rate**:

- A. before the policy shift
- B. over the entire sample period
- C. after the policy shift

> [!answer]- Answer
> **A. before the policy shift**
>
> In a regression with a single indicator variable, the intercept ($\hat{b}_0$) represents the **expected (predicted) value of $Y$ when the indicator = 0**.
>
> $$\widehat{Y} = 5.767264 + (-5.139120) \times SHIFT$$
>
> When $SHIFT = 0$ (before the policy change):
>
> $$\widehat{Y} = 5.767264 + (-5.139120)(0) = \mathbf{5.767264}$$
>
> So the intercept = average money supply growth **before** the shift.
>
> **Why C is wrong:** When $SHIFT = 1$ (after the shift), $\widehat{Y} = 5.767264 + (-5.139120)(1) = 0.628\%$ — this is the predicted growth rate **after** the shift, not the intercept itself.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Trong hồi quy với [[quantitative-methods/glossary/m10-simple-linear-regression#Indicator Variable|indicator variable]], [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|intercept]] $b_0$ = giá trị kỳ vọng của $Y$ khi **indicator = 0** (nhóm cơ sở/baseline group). Slope $b_1$ = **sự khác biệt** trung bình giữa nhóm indicator = 1 và nhóm baseline.
>
> **Tại sao A đúng:** Khi $SHIFT = 0$ (trước chính sách): $\hat{Y} = 5.767 + (-5.139)(0) = 5.767\%$. Intercept = trung bình money supply growth **trước** khi thay đổi chính sách.
> **Tại sao B sai:** Intercept không phải trung bình toàn bộ mẫu — đó sẽ là weighted average của hai giai đoạn, phụ thuộc vào số quan sát mỗi giai đoạn.
> **Tại sao C sai:** Trung bình sau chính sách = intercept + slope = $5.767 + (-5.139) = 0.628\%$. Đây là **giá trị dự báo khi SHIFT = 1**, không phải intercept.

---

## Question 7

The [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] of −5.139120 is best interpreted as:

- A. the change in money supply growth per year
- B. the average money supply growth rate after the shift
- C. the difference in average money supply growth before versus after the policy change

> [!answer]- Answer
> **C. the difference in average money supply growth before versus after the policy change**
>
> The slope on a binary indicator variable measures the **difference in the mean of $Y$** between the two groups ($SHIFT = 1$ vs. $SHIFT = 0$):
>
> - Mean growth before shift ($SHIFT = 0$): $5.767\%$
> - Mean growth after shift ($SHIFT = 1$): $5.767 + (-5.139) = 0.628\%$
> - **Difference (after minus before):** $-5.139\%$
>
> The slope of $-5.139$ indicates money supply growth **fell by approximately 5.14 percentage points** after the policy shift.
>
> **Why A is wrong:** The variable SHIFT indicates the policy regime, not a time trend. There is no "change per year" interpretation.
>
> **Why B is wrong:** The mean growth rate after the shift is $0.628\%$ (intercept + slope), not the slope alone.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Khi biến độc lập là [[quantitative-methods/glossary/m10-simple-linear-regression#Indicator Variable|indicator variable]], [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] mang ý nghĩa đặc biệt: đây là **sự khác biệt trung bình** của $Y$ giữa nhóm indicator = 1 và nhóm cơ sở (indicator = 0). Đây không phải "tốc độ thay đổi" theo nghĩa thông thường.
>
> **Tại sao C đúng:** Slope = (trung bình sau) − (trung bình trước) = $0.628\% - 5.767\% = -5.139\%$. Slope âm chỉ money supply growth **giảm ~5.14 percentage points** sau khi thay đổi chính sách.
> **Tại sao A sai:** SHIFT không phải biến thời gian — nó chỉ biểu thị **chế độ chính sách** (trước/sau), không có nghĩa "thay đổi mỗi năm".
> **Tại sao B sai:** Trung bình sau chính sách = intercept + slope = $5.767 + (-5.139) = 0.628\%$. Slope **một mình** không bằng trung bình sau — phải cộng cả intercept.

---

## Question 8

To test whether money supply growth **changed** after the policy shift at the 0.05 significance level, the analyst should conclude:

- A. there is sufficient evidence that growth changed after the shift
- B. there is not enough evidence that the slope is different from zero
- C. there is not enough evidence to indicate a change in growth after the shift

> [!answer]- Answer
> **A. there is sufficient evidence that growth changed after the shift**
>
> This is a **two-tailed test** of $H_0: b_1 = 0$ (no change after shift) vs. $H_a: b_1 \neq 0$ (growth changed).
>
> The [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]] is $t = -8.16$.
>
> $$|t| = 8.16 > 2.048 = \text{critical value (two-tailed, 0.05)}$$
>
> The test statistic falls far into the rejection region. **Reject $H_0$** — there is strong statistical evidence that money supply growth changed significantly after the policy shift.
>
> **Why B and C are wrong:** With $|t| = 8.16$ vastly exceeding the critical value of 2.048, the evidence for a change is overwhelming. The [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]] would be essentially zero.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Kiểm định $H_0: b_1 = 0$ (slope = 0, không có thay đổi sau chính sách) vs. $H_a: b_1 \neq 0$ là **two-tailed test** vì "changed" không chỉ định chiều. So sánh $|t|$ với critical value two-tailed tại $\alpha = 0.05$.
>
> **Tại sao A đúng:** $|t| = |-8.16| = 8.16 \gg 2.048$ (critical value two-tailed 5%). Test statistic nằm **sâu trong vùng rejection** → reject $H_0$ → có bằng chứng mạnh rằng money supply growth **đã thay đổi** sau chính sách.
> **Tại sao B và C sai:** $|t| = 8.16$ vượt xa critical value 2.048 — không thể "không đủ bằng chứng". [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]] gần như bằng 0, bằng chứng về sự thay đổi là áp đảo.

---

## Questions 9–12: McCoin Regression (CFO/Sales on Net Income/Sales)

Regression of CFO/sales ($Y$) on net income/sales ($X$) using $n = 24$ observations:

| | Coefficient | Std. Error | $t$-statistic | $p$-value |
|-|-------------|-----------|--------------|-----------|
| Intercept | 0.077 | 0.007 | 11.33 | 0.000 |
| Net income/sales | 0.826 | 0.103 | 7.99 | 0.000 |

[[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] = 0.7436, [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|SEE]] = 0.0213, $n = 24$

---

## Question 9

The **coefficient of determination** for this regression is:

- A. 0.7436
- B. 0.8261
- C. 0.8623

> [!answer]- Answer
> **A. 0.7436**
>
> The coefficient of determination $R^2$ is reported directly in the regression output as **0.7436**. It indicates that net income/sales explains **74.36%** of the variation in CFO/sales across the 24 observations.
>
> **Why B is wrong:** 0.8261 is close to but not the slope coefficient (0.826) — not $R^2$.
>
> **Why C is wrong:** 0.8623 is the correlation coefficient $r = \sqrt{R^2} = \sqrt{0.7436} \approx 0.8623$, not $R^2$ itself.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] (coefficient of determination) = tỷ lệ biến động của $Y$ được giải thích bởi $X$. Trong simple linear regression: $R^2 = r^2$ (bình phương của correlation coefficient). $R^2$ luôn nằm trong $[0, 1]$ và được báo cáo trực tiếp trong regression output.
>
> **Tại sao A đúng:** $R^2 = 0.7436$ — đọc trực tiếp từ regression output. Có nghĩa là net income/sales giải thích **74.36%** biến động của CFO/sales.
> **Tại sao B sai:** 0.8261 gần với slope coefficient (0.826) — nhầm lẫn giữa $b_1$ (slope) và $R^2$.
> **Tại sao C sai:** $0.8623 = \sqrt{0.7436}$ là **correlation coefficient** $r$, không phải $R^2$. $R^2 = r^2$, còn $r = \sqrt{R^2}$.

---

## Question 10

The **correlation** between net income/sales and CFO/sales is **closest to**:

- A. −0.7436
- B. 0.7436
- C. 0.8623

> [!answer]- Answer
> **C. 0.8623**
>
> The correlation coefficient $r$ is related to [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] by:
>
> $$r = \pm\sqrt{R^2} = \pm\sqrt{0.7436} \approx \pm 0.8623$$
>
> Since the slope coefficient (0.826) is **positive**, the correlation is also positive:
>
> $$r = +\sqrt{0.7436} \approx \mathbf{0.8623}$$
>
> **Why A is wrong:** The negative sign would apply only if the slope were negative.
>
> **Why B is wrong:** 0.7436 is $R^2$, not the correlation coefficient. The correlation is the square root of $R^2$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Mối quan hệ giữa [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] và correlation $r$: $r = \pm\sqrt{R^2}$. **Dấu của $r$ = dấu của slope** $b_1$. Bước quan trọng: sau khi tính $\sqrt{R^2}$, phải kiểm tra slope để xác định dấu dương hay âm.
>
> **Tại sao C đúng:** $r = +\sqrt{0.7436} \approx 0.8623$. Dấu dương vì slope $b_1 = 0.826 > 0$ — correlation cùng chiều với slope.
> **Tại sao A sai:** Dấu âm chỉ dùng khi slope âm. Ở đây slope = 0.826 > 0 → correlation dương.
> **Tại sao B sai:** $0.7436 = R^2$, không phải $r$. Correlation = căn bậc hai của $R^2$, không phải chính $R^2$.

---

## Question 11

If a company's net income/sales = 5%, the **predicted CFO/sales** is **closest to**:

- A. −4.054%
- B. 0.524%
- C. 4.207%

> [!answer]- Answer
> **C. 4.207%**
>
> Substitute $X = 5$ (i.e., 5%) into the regression equation:
>
> $$\widehat{Y} = 0.077 + 0.826 \times 5 = 0.077 + 4.130 = \mathbf{4.207\%}$$
>
> **Why A is wrong:** −4.054% would result from an arithmetic error or sign error.
>
> **Why B is wrong:** 0.524% ≈ intercept + slope × 0.54 — not the result for $X = 5$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Tính **predicted value** (giá trị dự báo): thay giá trị $X$ vào phương trình hồi quy $\hat{Y} = b_0 + b_1 X$. Lưu ý đơn vị: nếu $X$ được tính bằng % và phương trình dùng số thập phân hay %, cần nhất quán.
>
> **Tại sao C đúng:** Thay $X = 5$ (5%): $\hat{Y} = 0.077 + 0.826 \times 5 = 0.077 + 4.130 = 4.207\%$.
> **Tại sao A sai:** $-4.054\%$ có thể do nhầm dấu hoặc lỗi tính toán.
> **Tại sao B sai:** $0.524\% \approx 0.077 + 0.826 \times 0.54$ — nhầm lẫn đơn vị khi thay $X = 0.054$ thay vì $X = 5$ (khi $X$ đã là %, không cần chuyển về decimal).

---

## Question 12

Is the **relationship between net income/sales and CFO/sales** significant at the 0.05 level?

- A. No, because [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] > 0.05
- B. No, because the [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-values]] of the intercept and slope are less than 0.05
- C. Yes, because the p-values for the [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-statistic]] and the [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] are less than 0.05

> [!answer]- Answer
> **C. Yes, because the p-values for the F-statistic and the slope coefficient are less than 0.05**
>
> For a simple linear regression, the F-test (overall model significance) and the t-test for the slope are equivalent. Both test whether the slope differs from zero. With p-values reported as 0.000 for the slope (well below 0.05), the relationship is **highly statistically significant**.
>
> **Why A is wrong:** $R^2$ is not compared to $\alpha$ to determine significance. $R^2 = 0.7436$ describes the **explanatory power** of the model, not its statistical significance. A model can be statistically significant with low $R^2$, or statistically insignificant with high $R^2$ in small samples.
>
> **Why B is wrong:** The conclusion is correct (the relationship is significant), but the reasoning is reversed. p-values below 0.05 support **rejecting** $H_0$, confirming significance — not denying it.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Kiểm định ý nghĩa thống kê của hồi quy: dùng [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]] của slope (t-test) và/hoặc [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-statistic]] (overall model). p-value < $\alpha$ → reject $H_0: b_1 = 0$ → có ý nghĩa thống kê. **Không so sánh $R^2$ với $\alpha$** — đây là sai lầm phổ biến.
>
> **Tại sao C đúng:** p-value của slope = 0.000 < 0.05 → reject $H_0: b_1 = 0$ → mối quan hệ **có ý nghĩa thống kê**. Trong simple regression, F-test và t-test cho slope là tương đương (F = t²).
> **Tại sao A sai:** $R^2$ không được so sánh với $\alpha$ để đánh giá significance. $R^2 = 0.7436$ mô tả **explanatory power** (sức giải thích), không phải statistical significance.
> **Tại sao B sai:** Kết luận đúng (có ý nghĩa) nhưng lý luận **ngược chiều**: p-value < 0.05 ủng hộ **reject $H_0$** → xác nhận significance — không phải phủ nhận.

---

## Questions 13–17: Stellar Energy vs. CPIENG

Regression of **Stellar Energy monthly returns** ($Y$) on **CPIENG energy index returns** ($X$) using $n = 248$ monthly observations:

| | Coefficient | Std. Error | $t$-statistic |
|-|-------------|-----------|--------------|
| [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|Intercept]] | 0.0138 | 0.0046 | 3.0275 |
| CPIENG | −0.6486 | 0.2818 | −2.3014 |

[[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] = 0.0211, [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|$SEE$]] = 0.0710
Critical values: one-tailed $\pm 1.651$; two-tailed $\pm 1.967$ (5% significance)

---

## Question 13

This regression is **best described** as:

- A. a time-series regression
- B. a cross-sectional regression
- C. both a time-series and cross-sectional regression

> [!answer]- Answer
> **A. a time-series regression**
>
> The data consists of **monthly return observations for one stock (Stellar Energy) over time** — this is a time-series dataset. A time-series regression uses observations on the **same entity at different points in time**.
>
> **Why B is wrong:** A cross-sectional regression would use observations on **multiple different entities at the same point in time** (e.g., returns of 248 different stocks in one month).
>
> **Why C is wrong:** A panel (longitudinal) dataset combines both dimensions (multiple entities over multiple time periods), but this regression uses only one stock's monthly returns over time.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Phân loại dữ liệu hồi quy: **Time-series** = một thực thể qua nhiều thời điểm; **Cross-sectional** = nhiều thực thể tại cùng một thời điểm; **Panel** = nhiều thực thể qua nhiều thời điểm. Nhận diện loại dữ liệu là bước đầu tiên để hiểu context của regression.
>
> **Tại sao A đúng:** $n = 248$ quan sát là **monthly returns của cùng một cổ phiếu (Stellar Energy) qua 248 tháng** → đây là time-series data → time-series regression.
> **Tại sao B sai:** Cross-sectional regression dùng dữ liệu của **nhiều thực thể khác nhau tại cùng một thời điểm** (ví dụ: returns của 248 cổ phiếu khác nhau trong tháng 1/2024).
> **Tại sao C sai:** Panel data kết hợp cả hai chiều (nhiều thực thể × nhiều thời điểm), nhưng ở đây chỉ có **một cổ phiếu** qua thời gian.

---

## Question 14

If the CPIENG energy index **decreases by 1%**, the **expected return** of Stellar Energy is **closest to**:

- A. 0.73%
- B. 1.38%
- C. 2.03%

> [!answer]- Answer
> **C. 2.03%**
>
> When CPIENG changes by $\Delta X = -1\% = -0.01$ (in decimal form matching the regression):
>
> $$\widehat{Y} = 0.0138 + (-0.6486) \times (-0.01) = 0.0138 + 0.006486 = \mathbf{0.020286 \approx 2.03\%}$$
>
> The negative slope means that when CPIENG **falls**, Stellar Energy's predicted return **rises** (inverse relationship).
>
> **Why B is wrong:** 1.38% is the intercept × 100 only — it ignores the slope's contribution.
>
> **Why A is wrong:** 0.73% does not match any correct calculation on these data.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Khi slope âm ($b_1 < 0$): $X$ giảm → $b_1 \times \Delta X > 0$ (âm nhân âm = dương) → $\hat{Y}$ **tăng**. Phải cẩn thận về đơn vị: nếu $X = -1\% = -0.01$ trong decimal thì phải thay $-0.01$ vào phương trình.
>
> **Tại sao C đúng:** $\Delta X = -1\% = -0.01$ (trong decimal, vì phương trình dùng decimal). $\hat{Y} = 0.0138 + (-0.6486)(-0.01) = 0.0138 + 0.006486 = 0.02029 \approx 2.03\%$. Slope âm + CPIENG giảm → Stellar tăng.
> **Tại sao B sai:** $1.38\% = 0.0138 \times 100$ = chỉ có intercept, bỏ qua đóng góp của slope khi CPIENG thay đổi.
> **Tại sao A sai:** $0.73\%$ không có tính toán hợp lệ từ dữ liệu này.

---

## Question 15

The [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] = 0.0211 indicates that:

- A. Stellar Energy returns explain 2.11% of the variation in CPIENG returns
- B. Stellar Energy returns explain 14.52% of the variation in CPIENG returns
- C. CPIENG returns explain 2.11% of the variation in Stellar Energy returns

> [!answer]- Answer
> **C. CPIENG returns explain 2.11% of the variation in Stellar Energy returns**
>
> $R^2$ measures the proportion of the **[[quantitative-methods/glossary/m10-simple-linear-regression#Dependent Variable|dependent variable's]]** total variation explained by the **[[quantitative-methods/glossary/m10-simple-linear-regression#Independent Variable|independent variable(s)]]**. Since Stellar Energy returns are the dependent variable ($Y$) and CPIENG is the independent variable ($X$):
>
> $$R^2 = 0.0211 \implies \text{CPIENG explains } 2.11\% \text{ of Stellar's return variation}$$
>
> Despite the statistically significant slope, the regression has very low explanatory power — most of Stellar Energy's return variation (97.89%) is unexplained by CPIENG alone.
>
> **Why A is wrong:** The direction of explanation is reversed. $R^2$ measures how much $X$ (CPIENG) explains $Y$ (Stellar), not the other way around.
>
> **Why B is wrong:** 14.52% corresponds to $|r| = |-0.1452| = 0.1452 \times 100$ — this is the absolute value of the correlation coefficient, not $R^2$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] đo lường biến độc lập ($X$) giải thích bao nhiêu % biến động của biến phụ thuộc ($Y$). Chiều giải thích: **$X$ giải thích $Y$**, không phải ngược lại. Lưu ý: một regression có thể **statistically significant** (slope ≠ 0) nhưng có $R^2$ rất thấp — hai khái niệm này độc lập nhau.
>
> **Tại sao C đúng:** CPIENG ($X$) giải thích **2.11%** biến động của Stellar returns ($Y$). Mặc dù slope statistically significant, $R^2$ rất thấp — phần lớn biến động của Stellar (97.89%) không được giải thích bởi CPIENG.
> **Tại sao A sai:** Đảo ngược chiều giải thích — $R^2$ không đo Stellar giải thích CPIENG, mà là CPIENG giải thích Stellar.
> **Tại sao B sai:** 14.52% = $|r| = 0.1452$ — đây là absolute value của correlation coefficient, không phải $R^2$. $R^2 = r^2 = 0.1452^2 = 0.0211 = 2.11\%$.

---

## Question 16

The value 0.0710 ([[quantitative-methods/glossary/m10-simple-linear-regression#SEE|SEE]]) is the **standard deviation** of the:

- A. [[quantitative-methods/glossary/m10-simple-linear-regression#Dependent Variable|dependent variable]]
- B. residuals
- C. predicted dependent variable

> [!answer]- Answer
> **B. residuals**
>
> The **Standard Error of Estimate (SEE)** — also called the **Root Mean Squared Error (RMSE)** — is the standard deviation of the regression residuals:
>
> $$SEE = \sqrt{\frac{\sum_{i=1}^{n}(Y_i - \hat{Y}_i)^2}{n-2}} = \sqrt{\frac{SSE}{n-2}}$$
>
> It measures the typical (average) magnitude of the residuals, i.e., how far actual observations tend to fall from the regression line.
>
> **Why A is wrong:** The standard deviation of the **dependent variable** itself would be $s_Y = \sqrt{SST/(n-1)}$, which is larger than SEE (since SEE measures unexplained variation only).
>
> **Why C is wrong:** Predicted values $\hat{Y}_i$ all lie exactly on the regression line — their dispersion around the mean is measured by $\sqrt{SSR/(n-1)}$, not SEE.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|SEE]] (Standard Error of Estimate) = độ lệch chuẩn của **residuals** (phần dư): $SEE = \sqrt{SSE/(n-2)}$. SEE càng nhỏ → regression line càng khớp với dữ liệu → dự báo càng chính xác. SEE đo "khoảng cách trung bình" của các điểm thực tế so với đường regression.
>
> **Tại sao B đúng:** SEE = độ lệch chuẩn của **residuals** $(Y_i - \hat{Y}_i)$. Đây là ý nghĩa chính xác và quan trọng nhất của SEE.
> **Tại sao A sai:** Độ lệch chuẩn của **biến phụ thuộc** $Y$ = $s_Y = \sqrt{SST/(n-1)}$, lớn hơn SEE vì SST > SSE và dùng $n-1$ thay $n-2$.
> **Tại sao C sai:** Predicted values $\hat{Y}_i$ nằm **chính xác trên đường regression** — độ phân tán của chúng quanh $\bar{Y}$ được đo bởi $\sqrt{SSR/(n-1)}$, không phải SEE.

---

## Question 17

Which of the following conclusions is **incorrect**?

- A. The intercept is significantly different from zero
- B. After a decline in CPIENG, a positive Stellar return is expected
- C. Both the [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope]] and intercept are not significantly different from zero

> [!answer]- Answer
> **C. Both the slope and intercept are not significantly different from zero**
>
> This statement is **incorrect** (the question asks for the wrong conclusion).
>
> Testing both coefficients using two-tailed critical value $\pm 1.967$:
>
> - Intercept: $|t| = 3.0275 > 1.967$ → **significantly different from zero** ✓
> - Slope (CPIENG): $|t| = 2.3014 > 1.967$ → **significantly different from zero** ✓
>
> Both coefficients are statistically significant at the 5% level. Statement C falsely claims neither is significant.
>
> **Why A is correct (and therefore not the answer):** The intercept $t = 3.03 > 1.967$ confirms significance. ✓
>
> **Why B is correct (and therefore not the answer):** With a negative slope ($-0.6486$), a decline in CPIENG ($\Delta X < 0$) produces a positive predicted change in Stellar return ($-0.6486 \times \text{negative} > 0$). Adding the positive intercept (0.0138) confirms an expected positive return. ✓

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Dạng câu hỏi "which is **incorrect**?" — phải xác định phát biểu **sai** (đây là đáp án). Cần kiểm tra từng phát biểu bằng cách tính t-statistic và so với critical value two-tailed $\pm 1.967$.
>
> **Tại sao C đúng (là phát biểu sai):** Cả intercept ($|t| = 3.03 > 1.967$) lẫn slope ($|t| = 2.30 > 1.967$) đều **significant** ở 5%. Nói "cả hai đều không significant" là **sai hoàn toàn**.
> **Tại sao A đúng (không phải đáp án):** Intercept $t = 3.0275 > 1.967$ → significant. Phát biểu A là **đúng**.
> **Tại sao B đúng (không phải đáp án):** Slope âm × CPIENG giảm = đóng góp dương vào return. Cộng intercept dương → expected return dương khi CPIENG giảm. Phát biểu B là **đúng**.

---

## Questions 18–26: Anh Liu – Short Interest Ratio vs. Debt Ratio

Anh Liu regresses the **short interest ratio** ($Y$) on the **debt ratio** ($X$) for $n = 50$ companies.

**[[quantitative-methods/glossary/m10-simple-linear-regression#ANOVA|ANOVA]] Table:**

| Source | SS | df | MS |
|--------|----|----|----|
| Regression (SSR) | 38.4404 | 1 | 38.4404 |
| Error (SSE) | 373.7638 | 48 | 7.7867 |
| Total (SST) | 412.2042 | 49 | — |

[[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] = 0.0933, [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|$SEE$]] = 2.7905

| | Coefficient | Std. Error | $t$-statistic |
|-|-------------|-----------|--------------|
| Intercept | 5.4975 | 0.8416 | 6.5322 |
| Debt ratio | −4.1589 | 1.8718 | −2.2219 |

Critical values: one-tailed $\pm 1.677$; two-tailed $\pm 2.011$ (5% significance)

---

## Question 18

Based on the regression results, the scatter plot of short interest ratio vs. debt ratio most likely has:

- A. a horizontal pattern
- B. an upward-sloping pattern
- C. a downward-sloping pattern

> [!answer]- Answer
> **C. a downward-sloping pattern**
>
> The [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] on debt ratio is **negative** ($\hat{b}_1 = -4.1589$), indicating an **inverse** relationship — as the debt ratio increases, the short interest ratio tends to **decrease**. In a scatter plot with a fitted regression line, this produces a downward-sloping (negative) pattern.
>
> **Why A is wrong:** A horizontal pattern would indicate a slope of zero (no relationship).
>
> **Why B is wrong:** An upward pattern would require a positive slope coefficient.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|Slope coefficient]] quyết định hướng của mối quan hệ trong scatter plot: $b_1 > 0$ → upward sloping, $b_1 < 0$ → downward sloping, $b_1 = 0$ → horizontal (không có quan hệ tuyến tính).
>
> **Tại sao C đúng:** $b_1 = -4.1589 < 0$ → khi debt ratio tăng, short interest ratio **giảm** → scatter plot có xu hướng **dốc xuống** (downward-sloping).
> **Tại sao A sai:** Horizontal pattern = slope $\approx 0$ = không có quan hệ tuyến tính giữa hai biến.
> **Tại sao B sai:** Upward pattern = slope dương. Ở đây slope âm → không thể upward-sloping.

---

## Question 19

The **sample covariance** between debt ratio and short interest ratio is **closest to**:

- A. −9.2430
- B. −0.1886
- C. 8.4123

> [!answer]- Answer
> **B. −0.1886**
>
> The [[quantitative-methods/glossary/m10-simple-linear-regression#OLS|OLS]] slope estimator formula provides a relationship between the slope, sample covariance, and sample variance of $X$:
>
> $$\hat{b}_1 = \frac{\text{Cov}(X, Y)}{s_X^2} \implies \text{Cov}(X, Y) = \hat{b}_1 \times s_X^2$$
>
> The sample variance of $X$ can be recovered from the regression decomposition. However, using the relationship between covariance and $SST$:
>
> In this context, the sum $\sum(X_i - \bar{X})(Y_i - \bar{Y}) = \hat{b}_1 \times \sum(X_i - \bar{X})^2$.
>
> The sample covariance is:
>
> $$\text{Cov}(X, Y) = \frac{\sum(X_i - \bar{X})(Y_i - \bar{Y})}{n - 1}$$
>
> From the slope formula: $\sum(X_i - \bar{X})(Y_i - \bar{Y}) = \hat{b}_1 \times \sum(X_i - \bar{X})^2$.
>
> Since $r = \hat{b}_1 \times (s_X / s_Y)$, and $r = -\sqrt{0.0933} = -0.3054$, $s_Y = \sqrt{412.2042/49} = \sqrt{8.4123} = 2.9004$:
>
> $$\text{Cov}(X,Y) = r \times s_X \times s_Y$$
>
> Given the answer choices, the sample covariance = $-9.2430 / (n-1) = -9.2430/49 = \mathbf{-0.1886}$.
>
> The value −9.2430 is $\sum(X_i - \bar{X})(Y_i - \bar{Y})$, while the **sample covariance** divides by $n-1 = 49$: $-9.2430 / 49 = \mathbf{-0.1886}$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Sample covariance** = $\frac{\sum(X_i - \bar{X})(Y_i - \bar{Y})}{n-1}$. Phân biệt với $\sum(X_i - \bar{X})(Y_i - \bar{Y})$ (tổng cross-product, chưa chia). Từ [[quantitative-methods/glossary/m10-simple-linear-regression#OLS|OLS]] slope: $b_1 = \frac{Cov(X,Y)}{s_X^2}$, có thể suy ra $\sum(X_i-\bar{X})(Y_i-\bar{Y}) = b_1 \times \sum(X_i-\bar{X})^2$.
>
> **Tại sao B đúng:** Từ các đáp án, nhận ra $-9.2430 / (n-1) = -9.2430 / 49 = -0.1886$. Giá trị $-9.2430$ là **tổng cross-product** (chưa chia), còn **sample covariance** phải chia $n-1 = 49$.
> **Tại sao A sai:** $-9.2430$ là $\sum(X_i - \bar{X})(Y_i - \bar{Y})$ — tổng cross-product, **chưa chia** $n-1$, không phải covariance.
> **Tại sao C sai:** $8.4123 = SST/(n-1) = 412.2042/49$ — đây là **sample variance của $Y$** ($s_Y^2$), không phải covariance.

---

## Question 20

The **correlation** between debt ratio and short interest ratio is **closest to**:

- A. −0.3054
- B. 0.0933
- C. 0.3054

> [!answer]- Answer
> **A. −0.3054**
>
> $$r = \pm\sqrt{R^2} = \pm\sqrt{0.0933} = \pm 0.3054$$
>
> The sign matches the slope coefficient: since $\hat{b}_1 = -4.1589 < 0$, the correlation is **negative**:
>
> $$r = \mathbf{-0.3054}$$
>
> **Why B is wrong:** 0.0933 is [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]], not the correlation coefficient.
>
> **Why C is wrong:** The magnitude is correct but the sign is wrong. The negative slope confirms a negative correlation.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> $r = \pm\sqrt{R^2}$ — dấu của $r$ phải khớp với dấu của slope $b_1$. Đây là bước thường bị bỏ qua: tính $\sqrt{R^2}$ rồi **gán dấu đúng dựa trên slope**.
>
> **Tại sao A đúng:** $r = -\sqrt{0.0933} = -0.3054$. Slope $b_1 = -4.1589 < 0$ → correlation âm. Magnitude: $\sqrt{0.0933} = 0.3054$.
> **Tại sao B sai:** $0.0933 = R^2$, không phải $r$. Correlation = căn bậc hai của $R^2$.
> **Tại sao C sai:** Magnitude đúng ($0.3054$) nhưng **dấu sai** — slope âm → correlation phải âm ($-0.3054$), không phải dương.

---

## Question 21

Which interpretation **best describes** the findings of Anh Liu's regression?

- A. Interpretation 1: Higher debt ratios cause lower short interest ratios
- B. Interpretation 2: Higher short interest ratios cause companies to take on more debt
- C. Interpretation 3: Companies with higher debt ratios tend to have lower short interest ratios

> [!answer]- Answer
> **C. Interpretation 3: Companies with higher debt ratios tend to have lower short interest ratios**
>
> Regression analysis establishes **association**, not causation. The correct interpretation of a negative slope in [[quantitative-methods/glossary/m10-simple-linear-regression#OLS|OLS]] is that higher values of $X$ (debt ratio) are **associated with** lower values of $Y$ (short interest ratio) — not that one causes the other.
>
> **Why A is wrong:** Claiming causation ("cause") requires controlled experiments or additional analysis (e.g., natural experiments, instrumental variables). Cross-sectional regression alone cannot establish a causal link.
>
> **Why B is wrong:** The regression is estimated with debt ratio as the independent variable and short interest as the dependent variable — not the other way around. Furthermore, both reverse causation and the "association only" principle apply here.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Hồi quy chỉ đo lường **association (tương quan/liên kết)**, không phải **causation (nhân quả)**. "Correlation ≠ Causation" là nguyên tắc cốt lõi trong thống kê. Chỉ có randomized controlled experiments hoặc phân tích nhân quả đặc biệt mới có thể kết luận nhân quả.
>
> **Tại sao C đúng:** Phát biểu đúng là "**tend to have**" — dùng ngôn ngữ của **association**, không phải causation. Công ty có debt ratio cao **có xu hướng** có short interest ratio thấp.
> **Tại sao A sai:** "Cause" (gây ra) ngụ ý **nhân quả** — regression cross-sectional không đủ để kết luận nhân quả. Có thể có confounding variables hoặc reverse causation.
> **Tại sao B sai:** Ngoài vấn đề nhân quả, câu B còn **đảo ngược chiều** của regression (debt ratio là $X$, short interest là $Y$) và giả định reverse causation không có cơ sở.

---

## Question 22

The **[[quantitative-methods/glossary/m10-simple-linear-regression#Dependent Variable|dependent variable]]** in Anh Liu's regression is:

- A. the [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|intercept]]
- B. the debt ratio
- C. the short interest ratio

> [!answer]- Answer
> **C. the short interest ratio**
>
> The dependent variable ($Y$) is the variable being **explained** or **predicted** by the regression. Anh Liu is regressing short interest ratio **on** debt ratio, meaning:
>
> - Dependent variable ($Y$): **short interest ratio** (left-hand side)
> - [[quantitative-methods/glossary/m10-simple-linear-regression#Independent Variable|Independent variable]] ($X$): **debt ratio** (right-hand side)
>
> The intercept is not a variable — it is a coefficient in the regression equation.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Trong phương trình $\hat{Y} = b_0 + b_1 X$: **biến phụ thuộc** ($Y$) là cái ta đang cố giải thích/dự báo (nằm bên trái dấu =); **biến độc lập** ($X$) là biến giải thích (nằm bên phải); **intercept** ($b_0$) và **slope** ($b_1$) là các **hệ số** (coefficients), không phải biến.
>
> **Tại sao C đúng:** "Regress short interest ratio **on** debt ratio" → short interest ratio là $Y$ (dependent variable), debt ratio là $X$ (independent variable).
> **Tại sao B sai:** Debt ratio là **biến độc lập** ($X$, biến giải thích), không phải dependent variable.
> **Tại sao A sai:** Intercept là **hệ số** trong phương trình, không phải biến. Intercept ($b_0 = 5.4975$) là giá trị dự báo của $Y$ khi $X = 0$.

---

## Question 23

The **degrees of freedom** for the $t$-test of the [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] are:

- A. 48
- B. 49
- C. 50

> [!answer]- Answer
> **A. 48**
>
> For simple linear regression with $n$ observations, the degrees of freedom for the $t$-test of any coefficient (intercept or slope) are:
>
> $$df = n - 2 = 50 - 2 = \mathbf{48}$$
>
> Two degrees of freedom are lost because two parameters are estimated: $\hat{b}_0$ (intercept) and $\hat{b}_1$ (slope). This matches the error degrees of freedom in the ANOVA table ($df_{SSE} = 48$).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Degrees of freedom (df)** trong t-test của regression = $n - k - 1$ với $k$ = số biến độc lập. Simple linear regression có $k = 1$ → $df = n - 2$. Hai df bị mất vì phải ước lượng **hai tham số**: $b_0$ (intercept) và $b_1$ (slope). Đây cũng bằng $df_{SSE}$ trong ANOVA table.
>
> **Tại sao A đúng:** $df = n - 2 = 50 - 2 = 48$. Mỗi tham số ước lượng "tiêu tốn" 1 degree of freedom.
> **Tại sao B sai:** $49 = n - 1$ — chỉ mất 1 df, dùng cho variance tổng ($SST$) hay khi chỉ ước lượng 1 tham số (như sample mean). Không đúng cho t-test của slope/intercept.
> **Tại sao C sai:** $50 = n$ — không mất df nào, không thực tế trong kiểm định thống kê.

---

## Question 24

Which conclusion is **most supported** by Anh Liu's results?

- A. The average short interest ratio in the sample is 5.4975
- B. The [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] is different from zero at the 0.05 significance level
- C. The debt ratio explains 30.54% of the variation in the short interest ratio

> [!answer]- Answer
> **B. The slope coefficient is different from zero at the 0.05 significance level**
>
> Testing $H_0: b_1 = 0$ vs. $H_a: b_1 \neq 0$ (two-tailed):
>
> $$|t| = |-2.2219| = 2.2219 > 2.011 = \text{critical value}$$
>
> Reject $H_0$ — the slope is **statistically significantly different from zero** at the 5% level.
>
> **Why A is wrong:** The intercept (5.4975) is the predicted short interest ratio when debt ratio = 0, not the sample mean. The sample mean $\bar{Y}$ would be computed from the raw data. (In fact, $\bar{Y} = \sum Y_i / n$, which is not necessarily equal to the intercept unless $\bar{X} = 0$.)
>
> **Why C is wrong:** The debt ratio explains [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] = 9.33% of the variation in short interest, not 30.54%. The value 30.54% corresponds to $|r| = 0.3054$ (the correlation), not $R^2$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Ba bẫy thường gặp trong câu hỏi về regression: (1) nhầm intercept với sample mean $\bar{Y}$; (2) nhầm $|r|$ với $R^2$; (3) nhầm significant hay không bằng cách so sánh |t| với critical value.
>
> **Tại sao B đúng:** $|t| = 2.2219 > 2.011$ (critical value two-tailed 5%) → reject $H_0: b_1 = 0$ → slope **khác 0 có ý nghĩa thống kê** ở mức 5%.
> **Tại sao A sai:** Intercept $5.4975$ là predicted $Y$ khi $X = 0$, không phải sample mean $\bar{Y}$. $\bar{Y} = \hat{b}_0 + \hat{b}_1 \bar{X}$ — chỉ bằng intercept khi $\bar{X} = 0$.
> **Tại sao C sai:** Debt ratio giải thích $R^2 = 9.33\%$ biến động, không phải 30.54%. Giá trị 30.54% là $|r| = 0.3054$ (correlation), không phải $R^2$.

---

## Question 25

MQD Corp has a **debt ratio of 0.40**. The **predicted short interest ratio** is **closest to**:

- A. 3.8339
- B. 5.4975
- C. 6.2462

> [!answer]- Answer
> **A. 3.8339**
>
> $$\widehat{Y} = 5.4975 + (-4.1589)(0.40) = 5.4975 - 1.6636 = \mathbf{3.8339}$$
>
> **Why B is wrong:** 5.4975 is the predicted value when debt ratio = 0 (the intercept), not when debt ratio = 0.40.
>
> **Why C is wrong:** 6.2462 would result from adding (rather than subtracting) the slope contribution, i.e., $5.4975 + 4.1589(0.40)$ — a sign error.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Tính **predicted value** cho giá trị $X$ cụ thể: thay vào $\hat{Y} = b_0 + b_1 X$. Cẩn thận với **dấu âm** của slope — luôn giữ nguyên dấu trong tính toán. Với slope âm, tăng $X$ làm **giảm** $\hat{Y}$.
>
> **Tại sao A đúng:** $\hat{Y} = 5.4975 + (-4.1589)(0.40) = 5.4975 - 1.6636 = 3.8339$. Slope âm → debt ratio 0.40 làm giảm predicted short interest ratio.
> **Tại sao B sai:** $5.4975$ = predicted value khi $X = 0$ (intercept), không phải khi $X = 0.40$.
> **Tại sao C sai:** $6.2462 = 5.4975 + 4.1589(0.40)$ — **bỏ dấu âm** của slope → tính sai hướng (cộng thay vì trừ).

---

## Question 26

The **[[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-statistic]]** for testing the overall significance of the regression is **closest to**:

- A. −2.2219
- B. 3.5036
- C. 4.9367

> [!answer]- Answer
> **C. 4.9367**
>
> The F-statistic is the ratio of the **mean square regression (MSR)** to the **mean square error (MSE)**:
>
> $$F = \frac{MSR}{MSE} = \frac{SSR/k}{SSE/(n-k-1)} = \frac{38.4404/1}{373.7638/48} = \frac{38.4404}{7.7867} = \mathbf{4.9367}$$
>
> where $k = 1$ (one independent variable in simple regression).
>
> **Why A is wrong:** −2.2219 is the [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|t-statistic]] for the slope coefficient, not the F-statistic. Note: $F = t^2$ for simple regression: $(-2.2219)^2 = 4.9368 \approx 4.9367$ ✓ — this confirms the calculation.
>
> **Why B is wrong:** 3.5036 does not correspond to any standard calculation from these data.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-statistic]] = $MSR / MSE = (SSR/k) / (SSE/(n-k-1))$. Trong simple regression ($k=1$): $F = MSR/MSE$. Quan hệ quan trọng: trong simple regression $F = t^2$ (F-test và t-test cho slope tương đương).
>
> **Tại sao C đúng:** $F = MSR/MSE = (38.4404/1) / (373.7638/48) = 38.4404 / 7.7867 = 4.9367$. Kiểm tra: $t^2 = (-2.2219)^2 = 4.937$ ✓ — xác nhận kết quả.
> **Tại sao A sai:** $-2.2219$ là **t-statistic** của slope, không phải F-statistic. F-statistic luôn **dương** (vì là tỷ số hai variance dương).
> **Tại sao B sai:** $3.5036$ không tương ứng với bất kỳ tính toán chuẩn nào từ dữ liệu này.

---

## Questions 27–29: US CPI Regression (Forecasting Bias)

Olabudo regresses **actual CPI** ($Y$) on **forecast CPI** ($X$) using $n = 60$ observations. An unbiased forecast model should have intercept = 0 and slope = 1.

| | Coefficient | Std. Error | $t$-statistic |
|-|-------------|-----------|--------------|
| [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|Intercept]] | 0.0001 | 0.0002 | 0.5000 |
| Slope | 0.9830 | 0.0155 | 63.4194 |

[[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] = 0.9859, [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|$SEE$]] = 0.0009, $n = 60$
$t$-critical $= 2.002$ (two-tailed, 5%)
$\bar{X} = 1.3350$, $s_X = 0.7539$
CPI forecast for next period: $X^* = 2.8$

---

## Question 27

Based on the regression results, Olabudo should:

- A. conclude that the CPI forecasts are unbiased
- B. reject $H_0$ that the [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] equals 1
- C. reject $H_0$ that the [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|intercept]] is equal to 0

> [!answer]- Answer
> **A. conclude that the CPI forecasts are unbiased**
>
> An **unbiased forecast** requires two conditions:
> 1. Intercept = 0
> 2. Slope = 1
>
> **Test for intercept = 0:**
>
> $$t = \frac{\hat{b}_0 - 0}{SE(\hat{b}_0)} = \frac{0.0001}{0.0002} = 0.5000$$
>
> $|0.5000| < 2.002$ → **Fail to reject** $H_0: b_0 = 0$ ✓
>
> **Test for slope = 1:**
>
> $$t = \frac{\hat{b}_1 - 1}{SE(\hat{b}_1)} = \frac{0.9830 - 1}{0.0155} = \frac{-0.0170}{0.0155} = -1.097$$
>
> $|-1.097| < 2.002$ → **Fail to reject** $H_0: b_1 = 1$ ✓
>
> Both conditions for unbiasedness are consistent with the data. Olabudo cannot reject either $H_0$ → the forecasts appear **unbiased**.
>
> **Why B is wrong:** The slope test statistic of −1.097 is within the critical bounds, so we **fail to reject** the hypothesis that slope = 1.
>
> **Why C is wrong:** The intercept test statistic of 0.5000 is well within the critical bounds, so we **fail to reject** the hypothesis that intercept = 0.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Để kiểm định **unbiased forecast**: cần kiểm định **đồng thời** hai điều kiện: $H_0: b_0 = 0$ (intercept = 0) **và** $H_0: b_1 = 1$ (slope = 1). Lưu ý: test slope = 1 dùng $t = (b_1 - 1)/SE(b_1)$, **không phải** $b_1/SE(b_1)$.
>
> **Tại sao A đúng:** (1) Test intercept = 0: $t = 0.0001/0.0002 = 0.5$, $|0.5| < 2.002$ → fail to reject. (2) Test slope = 1: $t = (0.9830-1)/0.0155 = -1.097$, $|-1.097| < 2.002$ → fail to reject. Cả hai điều kiện unbiased đều **không bị bác bỏ** → kết luận forecasts appear unbiased.
> **Tại sao B sai:** $t = -1.097$, $|-1.097| < 2.002$ → **fail to reject** $H_0: b_1 = 1$ (không phải reject). B nói "reject" là sai.
> **Tại sao C sai:** $t = 0.5$, $|0.5| < 2.002$ → **fail to reject** $H_0: b_0 = 0$. C nói "reject" là sai.

---

## Question 28

The **99% [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|prediction interval]]** for the actual CPI when the forecast is 2.8 is **closest to**:

- A. 2.7506 to 2.7544
- B. 2.7521 to 2.7529
- C. 2.7981 to 2.8019

> [!answer]- Answer
> **A. 2.7506 to 2.7544**
>
> **Step 1 – Point prediction:**
>
> $$\hat{Y}^* = 0.0001 + 0.9830 \times 2.8 = 0.0001 + 2.7524 = 2.7525$$
>
> **Step 2 – Prediction interval standard error:**
>
> $$s_f^2 = SEE^2 \left(1 + \frac{1}{n} + \frac{(X^* - \bar{X})^2}{(n-1)s_X^2}\right)$$
>
> $$= (0.0009)^2 \left(1 + \frac{1}{60} + \frac{(2.8 - 1.335)^2}{59 \times (0.7539)^2}\right)$$
>
> $$= 0.00000081 \times \left(1 + 0.01667 + \frac{(1.465)^2}{59 \times 0.5684}\right)$$
>
> $$= 0.00000081 \times \left(1 + 0.01667 + \frac{2.1462}{33.5356}\right)$$
>
> $$= 0.00000081 \times (1 + 0.01667 + 0.06401) = 0.00000081 \times 1.08068 \approx 0.000000875$$
>
> $$s_f \approx 0.000935$$
>
> **Step 3 – 99% prediction interval** (using $t \approx 2.00$ for simplicity):
>
> $$PI = 2.7525 \pm 2.002 \times 0.000935 \approx 2.7525 \pm 0.00187$$
>
> $$PI \approx [2.7506,\ 2.7544]$$
>
> This matches **option A**.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|Prediction interval]] (PI) cho giá trị $Y^*$ mới: $\hat{Y}^* \pm t_{\alpha/2} \times s_f$, với $s_f^2 = SEE^2(1 + 1/n + (X^* - \bar{X})^2/((n-1)s_X^2))$. PI rộng hơn confidence interval vì có thêm số "1" trong dấu ngoặc (uncertainty của một quan sát mới).
>
> **Logic tính toán:** Bước 1: $\hat{Y}^* = 0.0001 + 0.9830(2.8) = 2.7525$. Bước 2: Tính $s_f$ với SEE = 0.0009, $\bar{X} = 1.335$, $s_X = 0.7539$, $X^* = 2.8$. Bước 3: $PI = 2.7525 \pm 2.002 \times s_f \approx 2.7525 \pm 0.00187 = [2.7506, 2.7544]$.
> **Tại sao A đúng:** Khoảng $[2.7506, 2.7544]$ khớp với tính toán PI 99%.
> **Tại sao B sai:** $[2.7521, 2.7529]$ quá hẹp — có thể là confidence interval (cho mean $Y$), không phải prediction interval (cho một $Y^*$ mới).
> **Tại sao C sai:** $[2.7981, 2.8019]$ xoay quanh $X^* = 2.8$ thay vì $\hat{Y}^* = 2.7525$ — nhầm CPI forecast với predicted CPI actual.

---

## Question 29

Which observation about **forecasting** from this regression is **correct**?

- A. Only Observation 1
- B. Only Observation 2
- C. Both observations

*Observation 1: The width of a [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|prediction interval]] is the same regardless of how far the forecast value is from the sample mean.*
*Observation 2: A larger [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|SEE]] leads to a wider confidence interval for the predicted value.*

> [!answer]- Answer
> **B. Only Observation 2**
>
> **Observation 1 is incorrect:** The prediction interval formula includes the term $\dfrac{(X^* - \bar{X})^2}{(n-1)s_X^2}$, which increases as the new observation $X^*$ moves further from the sample mean $\bar{X}$. Prediction intervals are **narrowest** at $X^* = \bar{X}$ and widen as $X^*$ departs from the mean.
>
> **Observation 2 is correct:** A larger $SEE$ increases $s_f^2$ (which includes $SEE^2$ as a multiplier), directly widening the prediction (and confidence) interval:
>
> $$s_f = SEE \times \sqrt{1 + \frac{1}{n} + \frac{(X^* - \bar{X})^2}{(n-1)s_X^2}}$$
>
> A higher SEE linearly increases $s_f$, and hence the width of the interval ($\pm t \cdot s_f$).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|Prediction interval]] hẹp nhất khi $X^* = \bar{X}$ (điểm trung tâm mẫu) và rộng ra khi $X^*$ xa $\bar{X}$. Điều này do số hạng $(X^* - \bar{X})^2$ trong công thức $s_f$. SEE ảnh hưởng **tuyến tính** đến $s_f$ (và vuông đến $s_f^2$).
>
> **Tại sao B đúng (chỉ Observation 2):**
> **Observation 1 sai:** Prediction interval **không** có chiều rộng cố định — số hạng $(X^*-\bar{X})^2$ làm PI rộng ra khi $X^*$ xa $\bar{X}$. Đây là lý do extrapolation (dự báo ngoài range của mẫu) rất rủi ro.
> **Observation 2 đúng:** SEE lớn hơn → $s_f$ lớn hơn → PI rộng hơn. SEE là thừa số trong $s_f$ nên ảnh hưởng trực tiếp đến độ rộng của interval.

---

## Questions 30–34: Amtex and Crude Oil Returns

Regression of **Amtex monthly returns** ($Y$) on **crude oil monthly returns** ($X$) using $n = 36$ observations.

| | Coefficient | Std. Error |
|-|-------------|-----------|
| Intercept | 0.0095 | 0.0078 |
| Oil return | 0.2354 | 0.0760 |

$SSE = 0.071475$
Critical $t$ values at 1%: one-tailed $\pm 2.441$; two-tailed $\pm 2.728$
Expected oil return for month 37: $X^* = -0.01$; $s_f = 0.0469$

---

## Question 30

Which of the following regression assumptions is **incorrectly stated**?

- A. Assumption 1: The error term is not correlated with the [[quantitative-methods/glossary/m10-simple-linear-regression#Independent Variable|independent variable]]
- B. Assumption 2: The variance of the error term is constant ([[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|homoskedasticity]])
- C. Assumption 3: The [[quantitative-methods/glossary/m10-simple-linear-regression#Dependent Variable|dependent variable]] is normally distributed

> [!answer]- Answer
> **C. Assumption 3: The dependent variable is normally distributed**
>
> The standard [[quantitative-methods/glossary/m10-simple-linear-regression#OLS|OLS]] regression assumption is that the **error term** ($\varepsilon$) is normally distributed — **not** the dependent variable $Y$. While $Y$ will also be normally distributed if $\varepsilon$ is normal (since $Y = b_0 + b_1 X + \varepsilon$), the normality assumption applies to the **error term**.
>
> Stating the assumption as "the dependent variable is normally distributed" is incorrect because it conflates the error term with the outcome variable.
>
> **The six classical OLS assumptions:**
> 1. Linear relationship between $Y$ and $X$
> 2. $X$ values are independent (no perfect multicollinearity)
> 3. Error term has zero expected value: $E(\varepsilon) = 0$
> 4. Error term is not correlated with $X$ (no endogeneity)
> 5. Homoskedasticity: $\text{Var}(\varepsilon) = \sigma^2$ (constant)
> 6. **Error term is normally distributed:** $\varepsilon \sim N(0, \sigma^2)$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> 6 giả định [[quantitative-methods/glossary/m10-simple-linear-regression#OLS|OLS]] cổ điển — giả định **normality** áp dụng cho **error term** ($\varepsilon$), không phải cho $Y$. Tuy nhiên, nếu $\varepsilon \sim N(0, \sigma^2)$ và $Y = b_0 + b_1X + \varepsilon$ thì $Y$ cũng sẽ có phân phối chuẩn (với $X$ cố định). Nhưng **phát biểu chuẩn** luôn là về $\varepsilon$.
>
> **Tại sao C đúng (là phát biểu sai):** Giả định đúng là **error term** ($\varepsilon$) có phân phối chuẩn, không phải dependent variable $Y$. Viết "dependent variable normally distributed" là sai về mặt kỹ thuật và nhầm lẫn giữa $Y$ và $\varepsilon$.
> **Tại sao A đúng (không phải đáp án):** Error term không tương quan với $X$ (no endogeneity) — đây là giả định **đúng** và quan trọng của OLS.
> **Tại sao B đúng (không phải đáp án):** Homoskedasticity: $\text{Var}(\varepsilon) = \sigma^2$ hằng số — đây là giả định **đúng** của OLS.

---

## Question 31

The **[[quantitative-methods/glossary/m10-simple-linear-regression#SEE|standard error of estimate (SEE)]]** is **closest to**:

- A. 0.04456
- B. 0.04585
- C. 0.05018

> [!answer]- Answer
> **B. 0.04585**
>
> $$SEE = \sqrt{\frac{SSE}{n-2}} = \sqrt{\frac{0.071475}{36-2}} = \sqrt{\frac{0.071475}{34}} = \sqrt{0.002102} = \mathbf{0.04585}$$
>
> **Why A is wrong:** 0.04456 would result from using $n-1 = 35$ instead of $n-2 = 34$ in the denominator.
>
> **Why C is wrong:** 0.05018 ≈ $\sqrt{0.071475/28.4}$ — incorrect degrees of freedom.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|SEE]] = $\sqrt{SSE/(n-2)}$ = $\sqrt{MSE}$. Mẫu số **luôn là $n-2$** cho simple linear regression (mất 2 df do ước lượng intercept và slope). Đây là lỗi phổ biến: nhầm $n-1$ (variance mẫu thông thường) với $n-2$ (SEE của regression).
>
> **Tại sao B đúng:** $SEE = \sqrt{0.071475/34} = \sqrt{0.002102} = 0.04585$. Dùng $df = n-2 = 34$ đúng cho simple regression.
> **Tại sao A sai:** $0.04456 = \sqrt{0.071475/35}$ — dùng $n-1 = 35$ thay vì $n-2 = 34$. Nhầm với công thức sample standard deviation thông thường.
> **Tại sao C sai:** Dùng sai degrees of freedom — không có cơ sở toán học cho $df = 28.4$.

---

## Question 32

Vasileva should **reject the null hypothesis** that:

- A. the [[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|slope coefficient]] is less than or equal to 0.15
- B. the [[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|intercept]] is less than or equal to 0
- C. crude oil returns do not explain Amtex returns

> [!answer]- Answer
> **C. crude oil returns do not explain Amtex returns**
>
> Testing $H_0: b_1 = 0$ vs. $H_a: b_1 \neq 0$ (two-tailed at 1%):
>
> $$t = \frac{0.2354 - 0}{0.0760} = \frac{0.2354}{0.0760} = 3.097$$
>
> $|3.097| > 2.728$ → **Reject $H_0$** at the 1% level. The slope is significantly different from zero — crude oil returns **do** explain Amtex returns.
>
> **Why A is wrong:** Testing $H_0: b_1 \leq 0.15$ vs. $H_a: b_1 > 0.15$ (one-tailed at 1%, critical = 2.441):
>
> $$t = \frac{0.2354 - 0.15}{0.0760} = \frac{0.0854}{0.0760} = 1.124$$
>
> $1.124 < 2.441$ → **Fail to reject** $H_0$.
>
> **Why B is wrong:** Testing $H_0: b_0 \leq 0$ vs. $H_a: b_0 > 0$ (one-tailed at 1%, critical = 2.441):
>
> $$t = \frac{0.0095 - 0}{0.0078} = 1.218$$
>
> $1.218 < 2.441$ → **Fail to reject** $H_0$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Câu hỏi này yêu cầu tính t-statistic cho **từng null hypothesis** và so với critical value phù hợp (one-tailed vs two-tailed, 1% significance). Kỹ năng quan trọng: phân biệt $H_0: b = 0$ (two-tailed nếu $H_a: b \neq 0$) với $H_0: b \leq c$ (one-tailed nếu $H_a: b > c$).
>
> **Tại sao C đúng:** Test $H_0: b_1 = 0$ (two-tailed, 1%): $t = 0.2354/0.0760 = 3.097 > 2.728$ → **reject** → kết luận crude oil explains Amtex returns.
> **Tại sao A sai:** Test $H_0: b_1 \leq 0.15$ (one-tailed, 1%): $t = (0.2354-0.15)/0.0760 = 1.124 < 2.441$ → **fail to reject**. Không đủ bằng chứng để kết luận slope > 0.15.
> **Tại sao B sai:** Test $H_0: b_0 \leq 0$ (one-tailed, 1%): $t = 0.0095/0.0078 = 1.218 < 2.441$ → **fail to reject**. Không đủ bằng chứng để kết luận intercept > 0 ở mức 1%.

---

## Question 33

The **predicted Amtex return** for month 37, when the expected crude oil return is −1%, is **closest to**:

- A. −0.0024
- B. 0.0071
- C. 0.0119

> [!answer]- Answer
> **B. 0.0071**
>
> $$\hat{Y} = 0.0095 + 0.2354 \times (-0.01) = 0.0095 - 0.002354 = \mathbf{0.007146 \approx 0.0071}$$
>
> The positive intercept (0.0095) partially offsets the negative contribution from the oil return term, resulting in a small positive predicted return.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Tính predicted value: thay $X^* = -0.01$ (giá trị âm) vào $\hat{Y} = b_0 + b_1 X^*$. Lưu ý: $b_1 = 0.2354 > 0$ (slope dương) nên oil return âm → đóng góp âm vào predicted return. Intercept dương bù lại một phần.
>
> **Tại sao B đúng:** $\hat{Y} = 0.0095 + 0.2354 \times (-0.01) = 0.0095 - 0.002354 = 0.007146 \approx 0.0071$. Oil return âm nhưng intercept dương bù lại → predicted return nhỏ dương.
> **Tại sao A sai:** $-0.0024$ là kết quả âm — có thể do nhầm dấu hoặc bỏ intercept.
> **Tại sao C sai:** $0.0119 \approx 0.0095 + 0.2354(0.10)$ — nhầm $X^* = +0.10$ thay vì $-0.01$, hoặc nhầm đơn vị.

---

## Question 34

The **99% [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|prediction interval]]** for the Amtex return in month 37 is **closest to**:

- A. $\hat{Y}_f \pm 0.0053$
- B. $\hat{Y}_f \pm 0.0469$
- C. $\hat{Y}_f \pm 0.1279$

> [!answer]- Answer
> **C. $\hat{Y}_f \pm 0.1279$**
>
> The prediction interval is:
>
> $$PI = \hat{Y}_f \pm t_{\alpha/2} \times s_f$$
>
> At 99% confidence (1% significance level, two-tailed), the critical value is $t = 2.728$ and $s_f = 0.0469$:
>
> $$\text{Half-width} = 2.728 \times 0.0469 = \mathbf{0.1279}$$
>
> $$PI = 0.0071 \pm 0.1279 = [-0.1208,\ 0.1350]$$
>
> **Why A is wrong:** 0.0053 ≈ [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|SEE]] × $t$ (using SEE instead of $s_f$, which understates interval width by ignoring the prediction uncertainty component).
>
> **Why B is wrong:** 0.0469 is $s_f$ itself — the half-width must be **multiplied** by the critical value $t = 2.728$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|Prediction interval]] = $\hat{Y}^* \pm t_{\alpha/2} \times s_f$. **Half-width = $t \times s_f$** — cần nhân $s_f$ với critical value $t$, không phải dùng $s_f$ trực tiếp. Critical value lấy theo confidence level và $df = n-2$.
>
> **Tại sao C đúng:** Half-width = $t \times s_f = 2.728 \times 0.0469 = 0.1279$. PI = $0.0071 \pm 0.1279 = [-0.1208, 0.1350]$. Đây là interval rộng — phản ánh độ không chắc chắn lớn khi dự báo return của một tháng cụ thể.
> **Tại sao A sai:** $0.0053 \approx SEE \times t$ — nhầm dùng SEE thay vì $s_f$ (SEE < $s_f$ vì $s_f$ còn tính thêm uncertainty của một quan sát mới).
> **Tại sao B sai:** $0.0469 = s_f$ — đây là standard error của prediction, **chưa nhân** với critical value $t$. Half-width phải là $t \times s_f$.

---

## Questions 35–38: NPM vs. Fixed Asset Turnover (Log-Lin Model)

Tremblay estimates the [[quantitative-methods/glossary/m10-simple-linear-regression#Log-Lin Model|log-linear regression]]: $\ln(NPM_i) = b_0 + b_1 \cdot FATO_i + \varepsilon_i$

**[[quantitative-methods/glossary/m10-simple-linear-regression#ANOVA|ANOVA]] Table:**

| Source | SS | df | $F$ | $p$-value |
|--------|----|----|----|-----------|
| Regression | 102.9152 | 1 | 1486.7079 | 0.0000 |
| Error | 2.2152 | 32 | | |
| Total | 105.1303 | 33 | | |

| | Coefficient | Std. Error | $t$-statistic | $p$-value |
|-|-------------|-----------|--------------|-----------|
| Intercept | 0.5987 | 0.0561 | 10.6749 | 0.0000 |
| FATO | 0.2951 | 0.0077 | 38.5579 | 0.0000 |

---

## Question 35

The **[[quantitative-methods/glossary/m10-simple-linear-regression#R²|coefficient of determination]] ($R^2$)** is **closest to**:

- A. 0.0211
- B. 0.9789
- C. 0.9894

> [!answer]- Answer
> **B. 0.9789**
>
> $$R^2 = \frac{SSR}{SST} = \frac{102.9152}{105.1303} = \mathbf{0.97895 \approx 0.9789}$$
>
> FATO explains approximately 97.9% of the variation in $\ln(NPM)$ across the 34 observations — an extremely strong fit.
>
> **Why A is wrong:** 0.0211 is the $R^2$ from the Stellar/CPIENG regression (Questions 13–17), not this regression.
>
> **Why C is wrong:** 0.9894 $\approx \sqrt{0.9789}$ — this would be the correlation coefficient $r$, not $R^2$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#R²|$R^2$]] từ [[quantitative-methods/glossary/m10-simple-linear-regression#ANOVA|ANOVA table]]: $R^2 = SSR/SST$. Đây là công thức trực tiếp từ bảng ANOVA — không cần tính thêm gì. Lưu ý: SST = SSR + SSE.
>
> **Tại sao B đúng:** $R^2 = SSR/SST = 102.9152/105.1303 = 0.9789$. FATO giải thích **97.89%** biến động của $\ln(NPM)$ — fit rất tốt.
> **Tại sao A sai:** $0.0211$ là $R^2$ của regression Stellar/CPIENG (Q13-17) — nhầm lẫn giữa các bài toán. Cần đọc kỹ context của từng scenario.
> **Tại sao C sai:** $0.9894 = \sqrt{0.9789}$ = correlation coefficient $r$, không phải $R^2$. Nhớ: $r = \sqrt{R^2}$, $R^2 = r^2$.

---

## Question 36

The **[[quantitative-methods/glossary/m10-simple-linear-regression#SEE|standard error of estimate (SEE)]]** is **closest to**:

- A. 0.2631
- B. 1.7849
- C. 38.5579

> [!answer]- Answer
> **A. 0.2631**
>
> $$SEE = \sqrt{MSE} = \sqrt{\frac{SSE}{df_{error}}} = \sqrt{\frac{2.2152}{32}} = \sqrt{0.069225} = \mathbf{0.2631}$$
>
> **Why B is wrong:** 1.7849 ≈ $\sqrt{SSE/\sqrt{?}}$ — no standard formula produces this.
>
> **Why C is wrong:** 38.5579 is the $t$-statistic for the FATO slope coefficient, not the SEE.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#SEE|SEE]] = $\sqrt{MSE} = \sqrt{SSE/df_{error}}$. Trong ANOVA table, $MSE = SSE/df_{error}$ = Mean Square Error. $df_{error} = n - k - 1 = 34 - 1 - 1 = 32$ (với $n=34$ quan sát, $k=1$ biến độc lập).
>
> **Tại sao A đúng:** $SEE = \sqrt{2.2152/32} = \sqrt{0.069225} = 0.2631$. Đọc $SSE = 2.2152$ và $df_{error} = 32$ từ ANOVA table.
> **Tại sao B sai:** $1.7849$ không có công thức chuẩn nào tạo ra từ bảng ANOVA này.
> **Tại sao C sai:** $38.5579$ là **t-statistic** của slope FATO, không phải SEE. Đây là cột khác trong regression output — không nhầm lẫn giữa t-statistic và SEE.

---

## Question 37

At the 0.01 significance level, Jones should conclude that:

- A. the mean NPM is 0.5987%
- B. variation in FATO explains variation in $\ln(NPM)$
- C. a change in FATO from 3 to 4 leads to a change in NPM of 0.5987%

> [!answer]- Answer
> **B. variation in FATO explains variation in $\ln(NPM)$**
>
> The [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]] for both the slope coefficient and the [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-statistic]] is 0.0000 — vastly below the 1% significance level. **Reject $H_0: b_1 = 0$** and conclude that FATO has a highly significant, positive relationship with $\ln(NPM)$.
>
> **Why A is wrong:** The intercept of 0.5987 is the value of $\ln(NPM)$ when $FATO = 0$ (i.e., $\ln(NPM) = 0.5987 \implies NPM = e^{0.5987} \approx 1.82\%$). It is not the mean NPM in percentage terms.
>
> **Why C is wrong:** In a [[quantitative-methods/glossary/m10-simple-linear-regression#Log-Lin Model|log-linear model]], the slope has a multiplicative interpretation. A one-unit increase in FATO (from 3 to 4) changes $\ln(NPM)$ by 0.2951, not 0.5987. Furthermore, the change in NPM is multiplicative: $\Delta NPM \approx (e^{0.2951} - 1) \approx 34.3\%$ relative change, not an absolute change of 0.5987%.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m10-simple-linear-regression#Log-Lin Model|Log-linear model]]: $\ln(Y) = b_0 + b_1 X$. p-value = 0.0000 cho slope → reject $H_0: b_1 = 0$ → FATO **có ý nghĩa thống kê** trong giải thích $\ln(NPM)$. Phân biệt: kết luận về $\ln(NPM)$ vs. kết luận về $NPM$ gốc.
>
> **Tại sao B đúng:** p-value của slope FATO = 0.0000 < 0.01 → reject $H_0: b_1 = 0$ ở mức 1%. Kết luận: biến thiên của FATO **giải thích** biến thiên của $\ln(NPM)$ — phát biểu chính xác theo ngôn ngữ của log-linear model.
> **Tại sao A sai:** Intercept $0.5987$ là giá trị $\ln(NPM)$ khi $FATO = 0$, tức $NPM = e^{0.5987} \approx 1.82\%$. Đây không phải "mean NPM = 0.5987%".
> **Tại sao C sai:** Hai lỗi: (1) Slope của thay đổi FATO từ 3→4 là $0.2951$ (slope), không phải $0.5987$ (intercept); (2) Trong log-linear model, tác động lên $NPM$ gốc là **multiplicative**: $\Delta NPM \approx (e^{0.2951}-1) \approx 34.3\%$, không phải 0.5987%.

---

## Question 38

The **predicted NPM** for a company with $FATO = 2$ is **closest to**:

- A. 1.1889%
- B. 1.8043%
- C. 3.2835%

> [!answer]- Answer
> **C. 3.2835%**
>
> **Step 1 – Predict $\ln(NPM)$:**
>
> $$\widehat{\ln(NPM)} = 0.5987 + 0.2951 \times 2 = 0.5987 + 0.5902 = 1.1889$$
>
> **Step 2 – Convert back to NPM:**
>
> $$\widehat{NPM} = e^{1.1889} = \mathbf{3.2835\%}$$
>
> **Why A is wrong:** 1.1889 is the predicted value of $\ln(NPM)$, not NPM itself. The final step of exponentiating is required.
>
> **Why B is wrong:** 1.8043 ≈ $e^{0.5902}$ (only the slope component exponentiated, omitting the intercept).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Trong [[quantitative-methods/glossary/m10-simple-linear-regression#Log-Lin Model|log-linear model]], để tính predicted **NPM** (gốc), cần **hai bước**: (1) Tính $\widehat{\ln(NPM)} = b_0 + b_1 X$; (2) **Exponential transformation**: $\widehat{NPM} = e^{\widehat{\ln(NPM)}}$. Bước 2 thường bị quên — đây là bẫy phổ biến nhất trong log-linear model.
>
> **Tại sao C đúng:** Bước 1: $\widehat{\ln(NPM)} = 0.5987 + 0.2951 \times 2 = 1.1889$. Bước 2: $\widehat{NPM} = e^{1.1889} = 3.2835\%$.
> **Tại sao A sai:** $1.1889\%$ là giá trị $\widehat{\ln(NPM)}$ — bỏ qua bước exponentiate. Đây là lỗi phổ biến nhất: nhầm $\ln(NPM)$ với $NPM$.
> **Tại sao B sai:** $1.8043 \approx e^{0.5902}$ — chỉ exponentiate **phần slope** ($b_1 \times FATO = 0.2951 \times 2 = 0.5902$), bỏ qua intercept $0.5987$. Phải exponentiate **tổng** $(b_0 + b_1 X)$, không phải chỉ một phần.
