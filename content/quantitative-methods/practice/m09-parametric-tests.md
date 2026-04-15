---
title: "Practice: M09 — Parametric and Non-parametric Tests"
type: practice
subject: quantitative-methods
module: M09
created: 2026-04-09
updated: 2026-04-09
tags: [practice, chi-square, independence, spearman, correlation-test]
---

# Practice: M09 — Parametric and Non-parametric Tests

**Module**: [[quantitative-methods/modules/m09-parametric-tests/index|M09]]
**Glossary**: [[quantitative-methods/glossary/m09-parametric-tests|M09 Terms]]

---

## Topic 1: Test of Correlation

**Question 1**: An analyst examines annual returns for Investment One and Investment Two over 33 years. The correlation coefficient is 0.43051. Test whether there is a significant positive correlation at 1% significance.

> [!answer]- Answer
> $H_0: \rho \leq 0$, $H_a: \rho > 0$ (right-tail)
> $t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}} = \frac{0.43051\sqrt{31}}{\sqrt{1-0.43051^2}} = \frac{0.43051 \times 5.568}{0.9026} = 2.656$
> df = 31, one-tailed, $\alpha = 1\%$ → $t_{\text{critical}} = 2.453$
> $2.656 > 2.453$ → **Reject $H_0$**
> Sufficient evidence that the correlation is positive at 1% significance.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Để kiểm định xem **hệ số tương quan** có khác không (hoặc có hướng cụ thể) hay không, dùng t-test với công thức đặc biệt: $t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}}$, phân phối theo t với $df = n - 2$ (mất 2 bậc tự do vì ước lượng 2 tham số). Đây là **parametric test** — giả định dữ liệu bình thường.
>
> **Logic tính toán:**
> - $r = 0.43051$, $n = 33$ → $df = 31$
> - $t = \frac{0.43051 \times \sqrt{31}}{\sqrt{1 - 0.43051^2}} = \frac{0.43051 \times 5.568}{\sqrt{1 - 0.18534}} = \frac{2.397}{\sqrt{0.8147}} = \frac{2.397}{0.9026} = 2.656$
> - Right-tail test ($H_a: \rho > 0$), $\alpha = 1\%$, df = 31 → $t_{\text{critical}} = 2.453$
> - $2.656 > 2.453$ → **Bác bỏ $H_0$** → tương quan dương có ý nghĩa thống kê ở mức 1%
>
> **Ý nghĩa thực tế:** Dù $r = 0.431$ không phải là tương quan đặc biệt mạnh, với 33 năm dữ liệu, chúng ta có đủ bằng chứng để kết luận rằng tương quan dương tồn tại trong tổng thể — không phải chỉ do ngẫu nhiên trong mẫu.

---

**Question 2**: The [[quantitative-methods/glossary/m09-parametric-tests#Spearman Rank Correlation|Spearman rank correlation]] test statistic is calculated as:

$$r_S = 1 - \frac{6\sum d_i^2}{n(n^2-1)}$$

When should you use Spearman rank instead of the parametric t-test for correlation?

> [!answer]- Answer
> Use Spearman rank when:
> - Data does **not** meet distributional assumptions (non-normal)
> - There are **outliers**
> - Data is given in **ranks** or uses an **ordinal scale**
> - The hypothesis does not concern a specific parameter
> - You want to test **monotonic** relationships (not just linear)

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m09-parametric-tests#Spearman Rank Correlation|Spearman rank correlation]] ($r_S$) là phiên bản **nonparametric** của Pearson correlation. Thay vì dùng giá trị thực, nó dùng **thứ hạng** (ranks) của các quan sát. Khi tính $r_S$: xếp hạng mỗi biến riêng lẻ, tính $d_i$ = hiệu thứ hạng cho mỗi cặp, rồi áp công thức trên.
>
> **Tại sao dùng Spearman thay vì Pearson t-test:**
> - **Non-normal data:** Parametric correlation t-test giả định dữ liệu bình thường. Nếu phân phối lệch hoặc có đuôi dày, kết quả bị sai lệch.
> - **Outliers:** Spearman dùng ranks nên một giá trị cực đoan chỉ có thứ hạng cao nhất/thấp nhất — không ảnh hưởng quá mức như với Pearson.
> - **Dữ liệu ordinal:** Nếu dữ liệu đã ở dạng thứ hạng (e.g., credit ratings, survey scores), Spearman là lựa chọn tự nhiên.
> - **Monotonic relationship:** Spearman đo lường xem hai biến có **cùng chiều** không (khi X tăng thì Y tăng/giảm), không nhất thiết phải tuyến tính như Pearson.
>
> **Hạn chế của Spearman:** Khi điều kiện của parametric test được thỏa mãn, Pearson t-test **mạnh hơn** (more powerful) vì dùng nhiều thông tin hơn từ dữ liệu.

---

## Topic 2: Chi-Square Test of Independence

**Question 3**: A contingency table of 1,594 ETFs classified by investment type (Value, Growth, Blend) and market cap (Small, Medium, Large):

| | Small | Medium | Large | Total |
|---|---|---|---|---|
| **Value** | 50 | 110 | 343 | 503 |
| **Growth** | 42 | 122 | 202 | 366 |
| **Blend** | 56 | 149 | 520 | 725 |
| **Total** | 148 | 381 | 1,065 | 1,594 |

Test independence at 5% significance using the [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|chi-square test of independence]].

> [!answer]- Answer
> $H_0$: Size and Investment type are independent
> $H_a$: Size and Investment type are not independent
> $df = (3-1)(3-1) = 4$
> $\alpha = 5\%$ → $\chi^2_{\text{critical}} = 9.488$ (from chi-square table)
>
> Expected values: $E_{ij} = \frac{\text{Row total} \times \text{Column total}}{\text{Grand total}}$
> Example: $E_{1,1} = \frac{148 \times 503}{1594} = 46.703$
>
> After computing all expected values and $\frac{(O-E)^2}{E}$ for each cell:
> $\chi^2 = 0.233 + 0.870 + 0.143 + 1.892 + 13.620 + 7.399 + 1.902 + 3.405 + 2.617 = 32.081$
>
> $32.081 > 9.488$ → **Reject $H_0$**
> Size and Investment type of ETFs are **not independent** at 5% significance.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|Chi-square test of independence]] kiểm định xem hai biến phân loại (categorical) có **độc lập** với nhau không. Dùng **contingency table** (bảng chéo). Test statistic: $\chi^2 = \sum \frac{(O_{ij} - E_{ij})^2}{E_{ij}}$, phân phối theo chi-square với $df = (r-1)(c-1)$ trong đó $r$ = số hàng, $c$ = số cột.
>
> **Logic của bài toán:**
> - **Degrees of freedom:** $(3-1)(3-1) = 4$ — bảng 3×3 có 4 bậc tự do
> - **Expected value** = (Row total × Column total) / Grand total — giá trị kỳ vọng **nếu** hai biến thực sự độc lập
> - Ví dụ: Nếu size và type độc lập, tỷ lệ ETF Small trong nhóm Value phải bằng tỷ lệ Small trong toàn bộ (148/1594 = 9.29%) → $E_{Value, Small} = 503 \times 9.29\% = 46.7$
> - Thực tế: 50 > 46.7 → nhóm Value có **hơi thiên về** Small cap
> - $\chi^2 = 32.081 \gg 9.488$ → **bác bỏ mạnh** $H_0$
>
> **Ý nghĩa thực tế:** Investment type (Value/Growth/Blend) và market cap size **không độc lập** — có sự liên hệ có hệ thống. Nhìn vào bảng: Growth ETF có tỷ lệ Medium cap cao bất thường (122/366 = 33.3% vs 381/1594 = 23.9% trung bình) — đây là nguồn đóng góp lớn nhất cho chi-square (13.620).

---

## Topic 3: Parametric vs Nonparametric

**Question 4**: An analyst examines monthly returns for two funds over one year. Both funds' returns are non-normally distributed. To test whether the mean return of one fund is greater than the other, the analyst can use:

A. A [[quantitative-methods/glossary/m08-hypothesis-testing#Parametric Test|parametric test]] only
B. A [[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|nonparametric test]] only
C. Both parametric and nonparametric tests

> [!answer]- Answer
> **B.** With non-normal distributions and small sample (12 months < 30), parametric tests that assume normality are not appropriate. Only nonparametric tests should be used.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **[[quantitative-methods/glossary/m08-hypothesis-testing#Parametric Test|Parametric tests]]** (như t-test) dựa trên giả định về phân phối của dữ liệu — thường là **normal distribution**. Khi giả định này bị vi phạm **và** cỡ mẫu nhỏ (CLT chưa phát huy tác dụng), parametric test không đáng tin cậy. **[[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|Nonparametric tests]]** không đòi hỏi giả định về phân phối — an toàn hơn trong trường hợp này.
>
> **Tại sao B đúng:** Hai điều kiện cùng vi phạm: (1) phân phối non-normal, (2) $n = 12 < 30$ (CLT chưa có hiệu lực). Với cỡ mẫu nhỏ và phân phối lệch, t-test sẽ cho kết quả không đáng tin cậy. Chỉ có thể dùng nonparametric test (như Wilcoxon rank-sum test hoặc Mann-Whitney U test).
>
> **Tại sao A sai:** Parametric test **không phù hợp** khi cả hai điều kiện trên đều bị vi phạm.
>
> **Tại sao C sai:** Không phải lúc nào cũng có thể dùng cả hai. Nếu giả định của parametric test bị vi phạm đáng kể, không nên dùng parametric test, dù nonparametric test có thể áp dụng bất kỳ lúc nào (với chi phí là power thấp hơn khi giả định được thỏa).
>
> **Quy tắc thực hành:** Nếu $n \geq 30$ (CLT), có thể dùng t-test kể cả khi non-normal. Nếu $n < 30$ và non-normal → phải dùng nonparametric.

---

**Question 5**: Which of the following is **not** a situation where nonparametric tests are appropriate?

A. The data are given in ranks
B. The sample is large and normally distributed
C. There are outliers in the dataset

> [!answer]- Answer
> **B.** When data is large and normal, parametric tests are more powerful and preferred. Nonparametric tests are used when distributional assumptions are violated (A and C).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Nonparametric tests được dùng khi: dữ liệu ordinal/ranks, phân phối non-normal với mẫu nhỏ, có outliers mạnh, hoặc hypothesis không về tham số cụ thể. Nhưng nonparametric tests **kém hiệu quả hơn** (less powerful) so với parametric tests khi điều kiện của parametric tests được thỏa mãn — tức là chúng cần mẫu lớn hơn để đạt cùng mức power.
>
> **Tại sao B đúng (không phải tình huống dùng nonparametric):** Khi mẫu **lớn và bình thường**, parametric tests có **statistical power cao hơn** — nghĩa là chúng nhạy hơn trong việc phát hiện sự khác biệt thực sự. Dùng nonparametric trong trường hợp này là "lãng phí" thông tin từ dữ liệu.
>
> **Tại sao A là tình huống dùng nonparametric:** Khi dữ liệu đã ở dạng ranks (ordinal), không có giá trị liên tục để áp dụng parametric test. Spearman correlation hoặc các rank-based tests là lựa chọn tự nhiên.
>
> **Tại sao C là tình huống dùng nonparametric:** Outliers làm méo mó các parametric tests (vì chúng ảnh hưởng mạnh đến mean và variance). Rank-based tests chỉ quan tâm đến thứ hạng nên robust với outliers.
