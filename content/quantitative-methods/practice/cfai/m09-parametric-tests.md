---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - parametric-tests
  - correlation
  - chi-square
source: "CFAI CFA1 Quant Practice 2026, pp.261-262"
module: "[[quantitative-methods/modules/m09-parametric-tests/index|M09]]"
---

# M09 – Parametric Tests: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.261–262
**Back to module:** [[quantitative-methods/modules/m09-parametric-tests/index|M09]]
**Glossary**: [[quantitative-methods/glossary/m09-parametric-tests|M09 Terms]]

---

## Question 1

Batten is testing whether the correlation between **Stellar Energy** stock returns and the **CPIENG energy index** returns is significantly different from zero. The sample correlation is $r = -0.1452$ based on $n = 248$ monthly observations. The critical value at the 0.05 significance level is $\pm 1.96$.

Batten should conclude that the relationship between Stellar Energy and CPIENG is:

- A. significant, because the [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]] falls outside the [[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|critical value]] bounds
- B. significant, because the test statistic has a lower absolute value than the critical value
- C. insignificant, because the test statistic falls outside the critical value bounds

> [!answer]- Answer
> **A. significant, because the test statistic falls outside the critical value bounds**
>
> The test statistic for a hypothesis test of zero correlation, $H_0: \rho = 0$, is:
>
> $$t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}}$$
>
> **Step 1 – Compute the test statistic:**
>
> $$t = \frac{-0.1452 \times \sqrt{248 - 2}}{\sqrt{1 - (-0.1452)^2}}$$
>
> $$t = \frac{-0.1452 \times \sqrt{246}}{\sqrt{1 - 0.02108}}$$
>
> $$t = \frac{-0.1452 \times 15.684}{\sqrt{0.97892}}$$
>
> $$t = \frac{-2.2773}{0.98941} \approx -2.302$$
>
> **Step 2 – Compare to critical value:**
>
> $$|t| = 2.302 > 1.96 = \text{critical value}$$
>
> The test statistic falls **outside** the bounds $[-1.96, +1.96]$, which is the rejection region.
>
> **Conclusion:** Reject $H_0: \rho = 0$. The correlation between Stellar Energy and CPIENG is **statistically significant** at the 5% level.
>
> **Why B is wrong:** The absolute value of the test statistic (2.302) is **greater than** the critical value (1.96), not lower. If the test statistic had a lower absolute value than the critical value, we would fail to reject $H_0$.
>
> **Why C is wrong:** Falling outside the critical value bounds means the result is **significant** (reject $H_0$), not insignificant. C correctly identifies the location but draws the wrong conclusion.
>
> **Economic interpretation:** The negative correlation ($r = -0.1452$, $t = -2.30$) indicates a statistically significant (though weak) **inverse** relationship between Stellar Energy stock returns and CPIENG energy index returns. This may seem counterintuitive — one possible explanation is that Stellar uses significant energy as an input, so rising energy prices compress its margins and depress its stock price.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Để kiểm định correlation $\rho$ có **khác 0** không, dùng [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]]: $t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}}$, phân phối t với $df = n-2$. Với $n = 248$ lớn, critical value $\approx \pm 1.96$ (xấp xỉ z).
>
> **Tại sao A đúng:** Tính $t = \frac{-0.1452 \times \sqrt{246}}{\sqrt{1-0.0211}} = \frac{-0.1452 \times 15.684}{0.9895} \approx -2.302$. Vì $|{-2.302}| = 2.302 > 1.96$ (critical value), test statistic **nằm ngoài** bounds → **reject $H_0: \rho = 0$** → correlation là significant.
> **Tại sao B sai:** "Lower absolute value than the critical value" là điều kiện để **fail to reject** $H_0$ — ở đây $|t| = 2.302 > 1.96$, tức là **lớn hơn** critical value, không phải nhỏ hơn.
> **Tại sao C sai:** C đúng khi nói test statistic "falls outside the critical value bounds", nhưng lại kết luận "insignificant" — ngược lại! Nằm ngoài bounds = vùng rejection = **significant**.

---

## Question 2

Which of the following is **correct** about the **[[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|chi-square test of independence]]**?

- A. It has a one-sided rejection region
- B. The [[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|null hypothesis]] is that the two groups are dependent
- C. When there are two categories, each with three levels, there are six degrees of freedom

> [!answer]- Answer
> **A. It has a one-sided rejection region**
>
> The chi-square test of independence uses the statistic:
>
> $$\chi^2 = \sum_{i,j} \frac{(O_{ij} - E_{ij})^2}{E_{ij}}$$
>
> Since this statistic involves **squared deviations**, it is always non-negative ($\chi^2 \geq 0$). Large values of $\chi^2$ indicate deviation from independence. Therefore, the rejection region is **always in the right tail only** — this is a one-sided (right-tailed) test.
>
> **Why B is wrong:** The **null hypothesis** in a chi-square test of independence is that the two categorical variables are **independent** (not dependent). The alternative is that they are dependent:
>
> $$H_0: \text{The two variables are independent}$$
> $$H_a: \text{The two variables are dependent}$$
>
> **Why C is wrong:** The degrees of freedom for a chi-square test of independence in a contingency table are:
>
> $$df = (r - 1)(c - 1)$$
>
> where $r$ = number of rows (levels of first variable) and $c$ = number of columns (levels of second variable).
>
> For two categories each with three levels (a $3 \times 3$ table):
>
> $$df = (3 - 1)(3 - 1) = 2 \times 2 = \mathbf{4}$$
>
> Not 6. The value 6 would be incorrect — it may arise from multiplying $3 \times 2 = 6$ (confusing number of levels with degrees of freedom).
>
> **Degrees of freedom summary:**
> | Table dimensions | $df$ |
> |-----------------|------|
> | $2 \times 2$ | $(2-1)(2-1) = 1$ |
> | $2 \times 3$ | $(2-1)(3-1) = 2$ |
> | $3 \times 3$ | $(3-1)(3-1) = 4$ |
> | $3 \times 4$ | $(3-1)(4-1) = 6$ |

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|Chi-square test of independence]] kiểm định xem hai biến categorical có **độc lập** nhau không. Test statistic $\chi^2 = \sum \frac{(O-E)^2}{E}$ luôn $\geq 0$ (bình phương), nên rejection region chỉ ở **đuôi phải**. Degrees of freedom: $df = (r-1)(c-1)$.
>
> **Tại sao A đúng:** Vì $\chi^2$ luôn dương (bình phương) và giá trị lớn mới cho thấy sự phụ thuộc, rejection region **luôn ở đuôi phải** — đây là one-sided test (right-tail). Đây là đặc điểm cốt lõi phân biệt chi-square với t-test hay z-test (có thể two-tailed).
> **Tại sao B sai:** $H_0$ trong chi-square test of independence là hai biến **độc lập** (independent), không phải dependent. $H_a$ là dependent. Bác bỏ $H_0$ nghĩa là có bằng chứng về sự phụ thuộc.
> **Tại sao C sai:** $df = (r-1)(c-1) = (3-1)(3-1) = 4$, không phải 6. Con số 6 có thể bị nhầm từ $3 \times 2 = 6$ (nhân số levels với nhau thay vì áp dụng công thức đúng). Chỉ table $3 \times 4$ mới cho $df = 6$.
