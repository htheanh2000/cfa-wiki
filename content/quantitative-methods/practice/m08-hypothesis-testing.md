---
title: "Practice: M08 — Hypothesis Testing"
type: practice
subject: quantitative-methods
module: M08
created: 2026-04-09
updated: 2026-04-09
tags: [practice, hypothesis-testing, t-test, chi-square, f-test, p-value]
---

# Practice: M08 — Hypothesis Testing

**Module**: [[quantitative-methods/modules/m08-hypothesis-testing/index|M08]]
**Glossary**: [[quantitative-methods/glossary/m08-hypothesis-testing|M08 Terms]]

---

## Topic 1: Process of Hypothesis Testing

**Question 1**: State the hypotheses for testing whether:
- (i) Population mean return equals 6%
- (ii) Population mean return is greater than 6%
- (iii) Population mean return is less than 6%

> [!answer]- Answer
> (i) Two-tailed: $H_0: \mu = 6$, $H_a: \mu \neq 6$
> (ii) Right-tail: $H_0: \mu \leq 6$, $H_a: \mu > 6$
> (iii) Left-tail: $H_0: \mu \geq 6$, $H_a: \mu < 6$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Trong [[quantitative-methods/glossary/m08-hypothesis-testing#Hypothesis Testing|hypothesis testing]], [[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|null hypothesis]] ($H_0$) luôn chứa dấu bằng (=, ≤, hoặc ≥). [[quantitative-methods/glossary/m08-hypothesis-testing#Alternative Hypothesis|Alternative hypothesis]] ($H_a$) là điều nhà phân tích muốn **chứng minh** và chứa dấu ≠, >, hoặc <. Chiều của $H_a$ quyết định loại test: hai đuôi (two-tailed) hay một đuôi (one-tailed).
>
> **Tại sao (i) là two-tailed:** "Bằng 6%" không xác định hướng lệch → $H_a: \mu \neq 6$ → test hai đuôi. Vùng bác bỏ nằm ở cả hai phía của phân phối.
>
> **Tại sao (ii) là right-tail:** Muốn chứng minh mean **lớn hơn** 6% → $H_a: \mu > 6$ → vùng bác bỏ nằm ở đuôi phải. $H_0$ là $\mu \leq 6$ (giả thuyết ngược lại — không có bằng chứng mean > 6).
>
> **Tại sao (iii) là left-tail:** Muốn chứng minh mean **nhỏ hơn** 6% → $H_a: \mu < 6$ → vùng bác bỏ nằm ở đuôi trái. $H_0$ là $\mu \geq 6$.
>
> **Nguyên tắc quan trọng:** Dấu bằng luôn thuộc về $H_0$. Nếu test one-tailed, $H_0$ dùng ≤ (right-tail test) hoặc ≥ (left-tail test), không dùng dấu = đơn thuần.

---

**Question 2**: A two-tailed test at 5% significance has z-[[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|critical value]] = ±1.96. The calculated [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]] is 2.15. The decision is:

A. Fail to reject $H_0$
B. Reject $H_0$
C. Accept $H_0$

> [!answer]- Answer
> **B.** |2.15| > 1.96 → reject $H_0$. Never say "accept $H_0$" — we either reject or fail to reject.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Quy tắc quyết định trong hypothesis testing: **Bác bỏ $H_0$** nếu |test statistic| > critical value (two-tailed). Test statistic rơi vào **rejection region** (vùng bác bỏ) → đủ bằng chứng thống kê để bác bỏ $H_0$.
>
> **Tại sao B đúng:** $|2.15| = 2.15 > 1.96$ → test statistic nằm trong vùng bác bỏ (bên ngoài ±1.96) → **Reject $H_0$**. Ở mức ý nghĩa 5%, có đủ bằng chứng thống kê để bác bỏ giả thuyết null.
>
> **Tại sao A sai:** "Fail to reject" xảy ra khi |test statistic| ≤ critical value. Ở đây 2.15 > 1.96 nên không phải trường hợp này.
>
> **Tại sao C sai — quy tắc ngôn ngữ CFA quan trọng:** Không bao giờ nói "accept $H_0$" trong hypothesis testing. Khi không đủ bằng chứng bác bỏ, ta chỉ "fail to reject" (không bác bỏ được) — điều này không có nghĩa là $H_0$ đúng, chỉ là không có đủ bằng chứng để bác bỏ nó. Đây là lỗi ngôn ngữ thường gặp mà CFA exam rất hay hỏi.

---

## Topic 2: Test of Single Mean

**Question 3**: ACE High Yield Total Return Index — test if mean daily returns differ between two periods:

| | Period 1 | Period 2 |
|---|---|---|
| Mean | 0.01775% | 0.01134% |
| Std Dev | 0.31580% | 0.38760% |
| Sample size | 445 days | 859 days |

Test at 5% significance whether means are different.

> [!answer]- Answer
> $H_0: \mu_1 - \mu_2 = 0$, $H_a: \mu_1 - \mu_2 \neq 0$
> $s_p^2 = \frac{(444)(0.3158^2) + (858)(0.3876^2)}{445 + 859 - 2} = 0.133$
> $t = \frac{0.01775 - 0.01134}{\sqrt{0.133(\frac{1}{445} + \frac{1}{859})}} = 0.3009$
> df = 1302, $t_{\text{critical}} = \pm 1.960$
> $0.3009 < 1.960$ → **Do not reject $H_0$**. No sufficient evidence that means differ.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Two-sample t-test** kiểm định xem hai tổng thể có trung bình bằng nhau không. Khi giả định **pooled variance** (phương sai bằng nhau), tính $s_p^2$ là phương sai gộp từ cả hai mẫu, rồi dùng nó để tính standard error của hiệu trung bình.
>
> **Logic tính toán:**
> - $s_p^2 = \frac{(n_1-1)s_1^2 + (n_2-1)s_2^2}{n_1+n_2-2}$ — phương sai gộp có trọng số theo df
> - t-statistic = (hiệu trung bình quan sát) / (standard error của hiệu) = $0.0064 / 0.0213 = 0.3009$
> - df = $445 + 859 - 2 = 1302$ → với df lớn, $t_{\text{critical}} \approx z = 1.960$
>
> **Tại sao không bác bỏ $H_0$:** $|0.3009| \ll 1.960$ — test statistic nằm sâu trong vùng không bác bỏ. Sự chênh lệch nhỏ về trung bình (0.00641%) không đủ lớn so với biến động trong dữ liệu. Không có bằng chứng thống kê cho thấy trung bình hai giai đoạn khác nhau.
>
> **Lưu ý thực tế:** Mặc dù giai đoạn 2 có std dev lớn hơn, điều này không ảnh hưởng đến kết luận về mean — hai câu hỏi (mean có bằng nhau không? variance có bằng nhau không?) được kiểm định riêng biệt.

---

## Topic 3: Test of Single Variance (Chi-Square)

**Question 4**: Sendar Equity Fund, 24 months, mean monthly return = 1.50%, std dev = 3.60%. Test whether $\sigma < 4\%$ at 5% significance.

> [!answer]- Answer
> $H_0: \sigma^2 \geq 16 \; (\%^2)$, $H_a: \sigma^2 < 16 \; (\%^2)$
> $\chi^2 = \frac{(n-1)s^2}{\sigma_0^2} = \frac{(23)(3.60)^2}{(4.0)^2} = \frac{23 \times 12.96}{16} = 18.63$
> df = 23, one-tailed (left), $\alpha = 5\%$
> Lower critical value = 13.091 (from chi-square table, 0.95 probability in right tail)
> $18.63 > 13.091$ → **Do not reject $H_0$**. Insufficient evidence that $\sigma < 4\%$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|Chi-square test]] dùng để kiểm định **phương sai** của một tổng thể. Test statistic: $\chi^2 = \frac{(n-1)s^2}{\sigma_0^2}$, phân phối theo chi-square với $df = n-1$. Phân phối chi-square **không đối xứng** và chỉ nhận giá trị dương — cần tra bảng cẩn thận cho one-tailed test.
>
> **Logic của bài toán:**
> - Muốn chứng minh $\sigma < 4\%$ → $H_a: \sigma^2 < 16$ → **left-tail test**
> - $H_0: \sigma^2 \geq 16$ (giả thuyết null: phương sai vẫn cao)
> - $\chi^2 = (23 \times 12.96) / 16 = 298.08/16 = 18.63$
> - Left-tail, $\alpha = 5\%$, df = 23: critical value = 13.091 (tức là 5% probability nằm bên trái 13.091)
> - Vùng bác bỏ: $\chi^2 < 13.091$. Nhưng $18.63 > 13.091$ → **không bác bỏ $H_0$**
>
> **Tại sao không bác bỏ:** Mặc dù $s = 3.60\% < 4\%$, sự chênh lệch này không đủ lớn về mặt thống kê với chỉ 24 quan sát. Cần bằng chứng mạnh hơn để kết luận phương sai tổng thể thực sự nhỏ hơn 4%.

---

## Topic 4: Test of Variance Equality (F-Test)

**Question 5**: You investigate whether population variance of returns changed after a market disruption:

| | Before | After |
|---|---|---|
| n | 120 | 120 |
| Mean monthly return | 1.416% | 1.436% |
| Variance | 22.367 | 15.795 |

Test at 0.05 significance. [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-test]] critical values: 0.6969 and 1.4349.

> [!answer]- Answer
> A. $H_0: \sigma_1^2 = \sigma_2^2$, $H_a: \sigma_1^2 \neq \sigma_2^2$
> B. $F = \frac{s_1^2}{s_2^2} = \frac{22.367}{15.795} = 1.416$, df₁ = df₂ = 119
> C. Two-tailed F-test: reject if F > 1.4349 or F < 0.6969
> $F = 1.416$ is between 0.6969 and 1.4349
> → **Do not reject $H_0$**. Insufficient evidence that variance changed.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-test]] so sánh **hai phương sai** từ hai tổng thể độc lập. F-statistic = $s_1^2 / s_2^2$, phân phối theo F-distribution với $(df_1, df_2) = (n_1 - 1, n_2 - 1)$. Thông thường đặt phương sai lớn hơn ở tử số để F ≥ 1 (simplifies one-tailed lookup), nhưng ở đây bài cho sẵn critical values hai phía.
>
> **Tại sao không bác bỏ $H_0$:** $F = 1.416$ nằm **giữa** hai critical values (0.6969 và 1.4349) → nằm trong vùng không bác bỏ. Dù variance trước disruption (22.367) cao hơn sau disruption (15.795) — một sự chênh lệch đáng kể về mặt kinh tế — nhưng với $n = 120$ cho mỗi giai đoạn, sự chênh lệch này vẫn **chưa đủ** ý nghĩa thống kê ở mức 5%.
>
> **Tại sao A sai (nếu ai viết $H_a: \sigma_1^2 > \sigma_2^2$):** Đây là two-tailed test vì câu hỏi hỏi liệu variance có "thay đổi" không — không chỉ định hướng. Nếu biết trước disruption thường làm tăng volatility, mới dùng one-tailed.
>
> **Lưu ý:** F-distribution không đối xứng; critical values hai phía không bằng nhau. Critical value phía dưới (0.6969) là nghịch đảo xấp xỉ của critical value phía trên cho các df tương đương.

---

## Topic 5: p-Value

**Question 6**: If a test has a [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]] of 0.03, which of the following is correct?

A. Reject $H_0$ at 1% significance
B. Reject $H_0$ at 5% significance
C. Fail to reject $H_0$ at 10% significance

> [!answer]- Answer
> **B.** Reject $H_0$ when p-value < $\alpha$. p = 0.03 < 0.05 → reject at 5%. But 0.03 > 0.01 → do not reject at 1%. And 0.03 < 0.10 → also reject at 10% (so C is wrong).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]] là xác suất thu được kết quả **cực đoan như quan sát hoặc cực đoan hơn**, giả sử $H_0$ đúng. Quy tắc: **Bác bỏ $H_0$ khi p-value < $\alpha$** (mức ý nghĩa). p-value nhỏ hơn → bằng chứng mạnh hơn chống lại $H_0$.
>
> **Kiểm tra từng đáp án với p = 0.03:**
> - Tại $\alpha = 1\%$: $0.03 > 0.01$ → **không bác bỏ** $H_0$ → A **sai**
> - Tại $\alpha = 5\%$: $0.03 < 0.05$ → **bác bỏ** $H_0$ → B **đúng**
> - Tại $\alpha = 10\%$: $0.03 < 0.10$ → **bác bỏ** $H_0$ → C **sai** (C nói "fail to reject" nhưng thực ra phải bác bỏ)
>
> **Cách nhớ:** p-value = 0.03 có nghĩa là nếu $H_0$ đúng, chỉ có 3% cơ hội thấy kết quả này hoặc cực đoan hơn. Mức ý nghĩa 5% nói rằng chúng ta chấp nhận 5% nguy cơ Type I error → 3% < 5% → đủ cơ sở bác bỏ. Nhưng ở mức 1%, 3% vẫn cao hơn ngưỡng chấp nhận.
>
> **Tổng kết:** p = 0.03 có ý nghĩa ở $\alpha = 5\%$ và $\alpha = 10\%$, nhưng **không** có ý nghĩa ở $\alpha = 1\%$.
