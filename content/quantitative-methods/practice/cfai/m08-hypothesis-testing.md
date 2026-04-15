---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - hypothesis-testing
  - type-i-error
  - type-ii-error
  - test-statistics
  - nonparametric
source: "CFAI CFA1 Quant Practice 2026, pp.236-241"
module: "[[quantitative-methods/modules/m08-hypothesis-testing/index|M08]]"
---

# M08 – Hypothesis Testing: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.236–241
**Back to module:** [[quantitative-methods/modules/m08-hypothesis-testing/index|M08]]
**Glossary**: [[quantitative-methods/glossary/m08-hypothesis-testing|M08 Terms]]

---

## Question 1

An analyst suspects that a fund's excess returns are **less than 5%**. The **most appropriate** hypotheses to test this are:

- A. $H_0: \mu = 5\%$ vs. $H_a: \mu \neq 5\%$
- B. $H_0: \mu \geq 5\%$ vs. $H_a: \mu < 5\%$
- C. $H_0: \mu \leq 5\%$ vs. $H_a: \mu > 5\%$

> [!answer]- Answer
> **B. $H_0: \mu \geq 5\%$ vs. $H_a: \mu < 5\%$**
>
> The analyst's **suspicion** (the claim she wants to establish) is that excess returns are **less than 5%**. In hypothesis testing, the condition the analyst wants to demonstrate evidence for is placed in the **[[quantitative-methods/glossary/m08-hypothesis-testing#Alternative Hypothesis|alternative hypothesis]]** $H_a$.
>
> This is a **one-tailed (left-tail) test** because the alternative specifies a direction (less than).
>
> **Why A is wrong:** A two-tailed test ($H_a: \mu \neq 5\%$) is appropriate when the analyst suspects the mean is **different from** 5% in either direction, with no prior directional belief. Here the analyst has a directional suspicion (less than), making a one-tailed test more powerful and appropriate.
>
> **Why C is wrong:** $H_a: \mu > 5\%$ is a right-tail test — the opposite direction from the analyst's suspicion.
>
> **Decision rule for B:** Reject $H_0$ if the test statistic falls in the left tail, i.e., test statistic $< -t_{\alpha}$ (or $< -z_{\alpha}$ for large samples).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Trong [[quantitative-methods/glossary/m08-hypothesis-testing#Alternative Hypothesis|kiểm định giả thuyết]], **điều analyst muốn chứng minh** luôn được đặt vào $H_a$ (alternative hypothesis). $H_0$ là giả thuyết mặc định (status quo) — giả sử đúng cho đến khi có bằng chứng đủ mạnh để bác bỏ.
>
> **Tại sao B đúng:** Analyst nghi ngờ excess returns **nhỏ hơn 5%** → đây là chiều analyst muốn chứng minh → $H_a: \mu < 5\%$. Để $H_0$ và $H_a$ bao phủ toàn bộ giá trị có thể, $H_0: \mu \geq 5\%$. Đây là **one-tailed test (đuôi trái)** vì $H_a$ chỉ định một chiều cụ thể.
> **Tại sao A sai:** $H_a: \mu \neq 5\%$ là two-tailed test — chỉ dùng khi không có định hướng trước. Analyst ở đây có định hướng rõ ràng (nhỏ hơn), nên one-tailed test phù hợp hơn và mạnh hơn.
> **Tại sao C sai:** $H_a: \mu > 5\%$ là đuôi phải — ngược chiều với nghi ngờ của analyst (đuôi trái).

---

## Question 2

Which of the following is **correct** about hypothesis testing?

- A. The [[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|null hypothesis]] is the condition the researcher hopes to support
- B. The [[quantitative-methods/glossary/m08-hypothesis-testing#Alternative Hypothesis|alternative hypothesis]] is the proposition considered true without contrary evidence
- C. The alternative hypothesis exhausts all parameter values not covered by the null hypothesis

> [!answer]- Answer
> **C. The alternative hypothesis exhausts all parameter values not covered by the null hypothesis**
>
> Together, $H_0$ and $H_a$ must cover **all possible values** of the parameter — they are mutually exclusive and collectively exhaustive. Any value of the parameter that is not included in the null must be covered by the alternative.
>
> **Why A is wrong:** The null hypothesis is what the researcher **starts with as true** (the default/status quo position). It is the **alternative hypothesis** that the researcher hopes to find evidence to support. Researchers design tests to reject $H_0$ in favour of $H_a$.
>
> **Why B is wrong:** The proposition "considered true without contrary evidence" is the **null hypothesis** — not the alternative. The null is maintained unless sufficient statistical evidence exists to reject it.
>
> **Summary of roles:**
> | | Null $H_0$ | Alternative $H_a$ |
> |--|-----------|-----------------|
> | Default assumption | Yes — assumed true initially | No |
> | Researcher's goal | To reject | To support |
> | Contains equality | Always | Never (uses $<$, $>$, or $\neq$) |

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|Null hypothesis]] ($H_0$) và [[quantitative-methods/glossary/m08-hypothesis-testing#Alternative Hypothesis|alternative hypothesis]] ($H_a$) phải cùng nhau bao phủ **mọi giá trị có thể** của tham số (collectively exhaustive) và không chồng lấn nhau (mutually exclusive).
>
> **Tại sao C đúng:** $H_a$ chứa tất cả các giá trị **không nằm trong** $H_0$. Ví dụ: nếu $H_0: \mu = 5\%$ thì $H_a: \mu \neq 5\%$ bao gồm mọi giá trị còn lại — không sót trường hợp nào.
> **Tại sao A sai:** $H_0$ là giả thuyết **mặc định/status quo** mà researcher giả sử đúng ban đầu. Chính $H_a$ mới là điều researcher muốn tìm bằng chứng ủng hộ — A đã đảo ngược vai trò của hai giả thuyết.
> **Tại sao B sai:** "Được coi là đúng khi không có bằng chứng ngược lại" mô tả đúng $H_0$, không phải $H_a$. $H_0$ được duy trì trừ khi có bằng chứng thống kê đủ mạnh để bác bỏ.

---

## Question 3

Which of the following is **correct** about the **[[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|null hypothesis]]**?

- A. It can be a "not equal to" statement if the alternative is an "equal to" statement
- B. Along with the alternative hypothesis, it covers all possible parameter values
- C. In a two-tailed test, it is rejected when evidence supports equality of the parameter to the hypothesised value

> [!answer]- Answer
> **B. Along with the alternative hypothesis, it covers all possible parameter values**
>
> The null and alternative hypotheses together form an exhaustive partition of the parameter space — every possible value of the parameter falls under exactly one of the two hypotheses.
>
> **Why A is wrong:** The null hypothesis **always includes the equality sign** (e.g., $=$, $\leq$, or $\geq$). A null of "not equal to" is never used in standard hypothesis testing because the null represents the default or status quo position, which requires a specific (or boundary) value.
>
> **Why C is wrong:** A two-tailed test rejects $H_0$ when there is **strong evidence that the parameter differs from the hypothesised value** (i.e., the test statistic falls far in either tail). When evidence supports equality — meaning the test statistic is close to zero — we **fail to reject** $H_0$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|Null hypothesis]] phải luôn chứa dấu bằng (=, ≤, hoặc ≥) vì đó là giả thuyết mà ta cần một giá trị cụ thể để tính [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]]. $H_0$ và $H_a$ cùng nhau phải bao phủ toàn bộ tham số.
>
> **Tại sao B đúng:** Đây là định nghĩa cơ bản — $H_0$ và $H_a$ cùng nhau tạo thành một phân vùng hoàn chỉnh của không gian tham số.
> **Tại sao A sai:** $H_0$ **luôn phải chứa dấu bằng** (=, ≤, ≥). Không bao giờ viết $H_0$ với dấu "khác" ($\neq$) vì ta không thể tính test statistic nếu $H_0$ không có giá trị cụ thể để so sánh.
> **Tại sao C sai:** Two-tailed test bác bỏ $H_0$ khi bằng chứng cho thấy **tham số khác biệt** với giá trị giả thuyết (test statistic nằm xa ở cả hai đuôi). Khi bằng chứng ủng hộ sự bằng nhau (test statistic gần 0), ta **fail to reject** $H_0$, không phải reject.

---

## Question 4

Regarding a **one-tailed hypothesis test**, which of the following is **correct**?

- A. The rejection region increases in size as the significance level becomes smaller
- B. A one-tailed test more strongly reflects the prior beliefs of the researcher than a two-tailed test
- C. The absolute value of the [[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|critical value]] in a one-tailed test is larger than in a two-tailed test

> [!answer]- Answer
> **B. A one-tailed test more strongly reflects the prior beliefs of the researcher than a two-tailed test**
>
> A one-tailed test embeds a **directional hypothesis** — the researcher has a prior belief about which direction the parameter deviates from the null. This is a stronger statement than a two-tailed test, which only asks "is it different?" without specifying direction.
>
> **Why A is wrong:** A **smaller** significance level $\alpha$ means a **smaller** rejection region (stricter standard for rejection), not a larger one. For example, $\alpha = 0.01$ has a smaller critical region than $\alpha = 0.05$.
>
> **Why C is wrong:** For the same $\alpha$, the absolute critical value in a one-tailed test is **smaller** than in a two-tailed test:
>
> | Test | $\alpha = 0.05$ critical value (normal) |
> |------|-----------------------------------------|
> | One-tailed | $\pm 1.645$ |
> | Two-tailed | $\pm 1.960$ |
>
> In a one-tailed test, all $\alpha$ probability is in one tail, so the cutoff is less extreme than when $\alpha/2$ is in each tail for a two-tailed test.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|Critical value]] là ngưỡng mà test statistic phải vượt qua để reject $H_0$. Với one-tailed test, toàn bộ xác suất $\alpha$ dồn vào **một đuôi** — critical value do đó gần với trung tâm phân phối hơn (dễ reject hơn) so với two-tailed test.
>
> **Tại sao B đúng:** One-tailed test thể hiện niềm tin có định hướng của researcher — researcher đã có prior belief về chiều của hiệu ứng, điều mà two-tailed test không có.
> **Tại sao A sai:** Significance level nhỏ hơn → vùng rejection **nhỏ hơn** (tiêu chuẩn nghiêm ngặt hơn). $\alpha = 0.01$ có vùng rejection nhỏ hơn $\alpha = 0.05$.
> **Tại sao C sai:** Với cùng $\alpha$, critical value tuyệt đối của one-tailed test **nhỏ hơn** của two-tailed test. Ví dụ $\alpha = 0.05$: one-tailed $z = 1.645$ < two-tailed $z = 1.960$. One-tailed test dồn toàn bộ $\alpha$ vào một đuôi nên cutoff gần trung tâm hơn.

---

## Question 5

A test uses a **5% significance level**. The corresponding **[[quantitative-methods/glossary/m07-estimation-and-inference#Confidence Interval|confidence level]]** is:

- A. 2.5%
- B. 5%
- C. 95%

> [!answer]- Answer
> **C. 95%**
>
> The confidence level is the complement of the significance level:
>
> $$\text{Confidence level} = 1 - \alpha = 1 - 0.05 = 0.95 = 95\%$$
>
> **Intuition:** A 5% significance level means we accept a 5% probability of incorrectly rejecting a true null hypothesis ([[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]]). We are therefore "95% confident" in the non-rejection region. The corresponding 95% confidence interval for the parameter will include the null value exactly when the hypothesis test fails to reject at the 5% level.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Significance level]] ($\alpha$) và [[quantitative-methods/glossary/m07-estimation-and-inference#Confidence Interval|confidence level]] là hai mặt của cùng một đồng xu: confidence level = $1 - \alpha$. Hai khái niệm này liên kết chặt chẽ — confidence interval và hypothesis test cho kết quả nhất quán với nhau.
>
> **Tại sao C đúng:** $1 - \alpha = 1 - 0.05 = 0.95 = 95\%$. Confidence level 95% có nghĩa là nếu lấy mẫu nhiều lần, 95% các confidence interval sẽ chứa giá trị tham số thực.
> **Tại sao A sai:** 2.5% là $\alpha/2$ — phần xác suất ở **mỗi đuôi** của two-tailed test, không phải confidence level.
> **Tại sao B sai:** 5% là chính significance level $\alpha$, không phải confidence level. Confidence level luôn là phần bù của $\alpha$.

---

## Question 6

A hypothesis test for a **normal population** at a **0.05 significance level** implies:

- A. a 95% probability of rejecting a true null hypothesis
- B. a 95% [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]] for a two-tailed test
- C. a 5% critical value rejection region for a one-tailed test

> [!answer]- Answer
> **C. a 5% critical value rejection region for a one-tailed test**
>
> At significance level $\alpha = 0.05$, the rejection region contains exactly 5% of the probability under the null. For a one-tailed test, all 5% is placed in one tail (left or right), defined by the critical value (e.g., $z = -1.645$ for a left-tailed test).
>
> **Why A is wrong:** The significance level defines the probability of rejecting a **true** null (Type I error) as **5%**, not 95%. A 95% probability of rejection would correspond to $\alpha = 0.95$, which is an absurdly large Type I error.
>
> **Why B is wrong:** The Type I error probability is $\alpha = 5\%$, not 95%. For a two-tailed test, this 5% is split as 2.5% in each tail — but the total Type I error probability remains 5%.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Significance level $\alpha = 0.05$ nghĩa là xác suất phạm [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]] (reject $H_0$ đúng) là **5%**. Rejection region chứa đúng $\alpha = 5\%$ diện tích phân phối dưới $H_0$.
>
> **Tại sao C đúng:** Với $\alpha = 0.05$, one-tailed test có rejection region là **5%** ở một đuôi — được xác định bởi critical value (ví dụ $z = -1.645$ cho đuôi trái). Đây là mô tả chính xác.
> **Tại sao A sai:** Xác suất reject $H_0$ đúng là **5%** (= $\alpha$), không phải 95%. Xác suất 95% là để **không reject** $H_0$ đúng (= $1 - \alpha$).
> **Tại sao B sai:** [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]] probability là $\alpha = 5\%$, không phải 95%. Với two-tailed test, 5% được chia đều thành 2.5% mỗi đuôi, nhưng tổng vẫn là 5%.

---

## Question 7

A **[[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]]** is best described as the basis for deciding whether to:

- A. reject the null hypothesis
- B. accept the null hypothesis
- C. reject the alternative hypothesis

> [!answer]- Answer
> **A. reject the null hypothesis**
>
> The test statistic is a standardised measure computed from sample data that is compared against a critical value (or used to compute a [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]]) to determine whether to **reject $H_0$**. The decision rule is: reject $H_0$ if the test statistic falls in the rejection region.
>
> **Why B is wrong:** In formal hypothesis testing, we never "accept" $H_0$ — we only **fail to reject** it. Failing to reject does not mean $H_0$ is true; it means there is insufficient evidence to conclude it is false.
>
> **Why C is wrong:** The test statistic is used to evaluate the null, not the alternative. Rejecting $H_0$ provides evidence in favour of $H_a$, but the decision is framed as "reject or fail to reject $H_0$."

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|Test statistic]] là giá trị tính từ dữ liệu mẫu, được chuẩn hóa theo phân phối chuẩn. Nó là cầu nối giữa dữ liệu quan sát và quyết định thống kê: so sánh với [[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|critical value]] hoặc dùng để tính [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]].
>
> **Tại sao A đúng:** Test statistic là cơ sở để quyết định có **reject $H_0$** hay không — so với critical value (nếu vượt quá → reject) hoặc p-value (nếu < $\alpha$ → reject).
> **Tại sao B sai:** Trong kiểm định giả thuyết, ta **không bao giờ "accept" $H_0$** — chỉ có "fail to reject" (không đủ bằng chứng bác bỏ). Fail to reject không có nghĩa $H_0$ đúng, chỉ là bằng chứng chưa đủ mạnh.
> **Tại sao C sai:** Test statistic dùng để đánh giá $H_0$, không phải $H_a$. Khi reject $H_0$ ta có bằng chứng ủng hộ $H_a$, nhưng framework luôn là "reject hay fail to reject $H_0$".

---

## Question 8

A **[[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]]** is best described as:

- A. rejecting a true null hypothesis
- B. rejecting a false null hypothesis
- C. failing to reject a false null hypothesis

> [!answer]- Answer
> **A. rejecting a true null hypothesis**
>
> A Type I error (also called a **false positive**) occurs when the null hypothesis is actually true but the test incorrectly rejects it. The probability of committing a Type I error is $\alpha$, the significance level.
>
> **Error taxonomy:**
>
> | | $H_0$ is True | $H_0$ is False |
> |--|--------------|----------------|
> | **Reject $H_0$** | **Type I error** ($\alpha$) | Correct decision (Power = $1-\beta$) |
> | **Fail to reject $H_0$** | Correct decision ($1-\alpha$) | **[[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]]** ($\beta$) |
>
> **Why B is wrong:** Correctly rejecting a false null is the ideal outcome — this is the **[[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|power]]** of the test ($1-\beta$), not an error.
>
> **Why C is wrong:** Failing to reject a false null is a **Type II error** ($\beta$), not a Type I error.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Ma trận lỗi trong [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|kiểm định giả thuyết]]:
> - **[[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]]** (false positive, $\alpha$): reject $H_0$ khi $H_0$ đúng
> - **[[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]]** (false negative, $\beta$): fail to reject $H_0$ khi $H_0$ sai
>
> **Tại sao A đúng:** Type I error = reject $H_0$ đúng = "false alarm" — ta kết luận có hiệu ứng trong khi thực ra không có. Xác suất này là $\alpha$ (significance level).
> **Tại sao B sai:** Reject $H_0$ sai là quyết định **đúng** — đây chính là [[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|power]] của test ($1-\beta$), không phải lỗi.
> **Tại sao C sai:** Fail to reject $H_0$ sai là **Type II error** ($\beta$) — ta bỏ lỡ hiệu ứng thực sự có tồn tại. Đây không phải Type I error.

---

## Question 9

A **[[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]]** is best described as:

- A. rejecting a true null hypothesis
- B. failing to reject a false null hypothesis
- C. failing to reject a false alternative hypothesis

> [!answer]- Answer
> **B. failing to reject a false null hypothesis**
>
> A Type II error (also called a **false negative**) occurs when $H_0$ is actually false but the test fails to reject it. The probability of a Type II error is $\beta$, and the **[[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|power]]** of the test is $1 - \beta$.
>
> **Why A is wrong:** Rejecting a true null is a **Type I error** ($\alpha$).
>
> **Why C is wrong:** "Failing to reject a false alternative" is not standard terminology — hypothesis tests are framed around rejecting or failing to reject $H_0$, not $H_a$. The concept described in C is not a recognised error type in classical hypothesis testing.
>
> **Reducing Type II error:** Increase sample size $n$ (increases power), raise significance level $\alpha$ (but this increases Type I error), or increase the true effect size.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]] ($\beta$) là "bỏ lỡ" — fail to reject $H_0$ khi $H_0$ thực ra sai. Đây là lỗi "false negative". [[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|Power]] = $1 - \beta$ đo lường khả năng phát hiện $H_0$ sai.
>
> **Tại sao B đúng:** Fail to reject $H_0$ sai = Type II error. Ví dụ: một loại thuốc thực sự hiệu quả nhưng test không phát hiện được — đây là Type II error.
> **Tại sao A sai:** Reject $H_0$ đúng là [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]] ($\alpha$), không phải Type II.
> **Tại sao C sai:** "Fail to reject a false alternative hypothesis" không phải thuật ngữ chuẩn — framework kiểm định luôn xoay quanh $H_0$, không phải $H_a$. Không có khái niệm lỗi liên quan đến việc reject/fail to reject $H_a$.

---

## Question 10

The **significance level** is best used to:

- A. calculate the [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]]
- B. define the test's rejection points ([[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|critical values]])
- C. specify the probability of a [[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]]

> [!answer]- Answer
> **B. define the test's rejection points (critical values)**
>
> The significance level $\alpha$ determines the **critical values** that separate the rejection region from the non-rejection region. For example, $\alpha = 0.05$ for a two-tailed $z$-test gives critical values $\pm 1.96$ — the rejection region is $|z| > 1.96$.
>
> **Why A is wrong:** The test statistic is calculated from the **sample data** using the sample mean, hypothesised value, standard error, and degrees of freedom — not from the significance level.
>
> **Why C is wrong:** The significance level $\alpha$ specifies the probability of a **Type I error**, not Type II. The probability of a Type II error ($\beta$) depends on the true parameter value, sample size, and $\alpha$, but is not directly specified by $\alpha$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|Critical value]] được xác định bởi $\alpha$ và phân phối của test statistic (t, z, F, $\chi^2$). Đây là bước "stating the decision rule" trong quy trình kiểm định — phải thực hiện **trước** khi thu thập dữ liệu.
>
> **Tại sao B đúng:** Significance level $\alpha$ xác định **vùng rejection** và do đó xác định **critical value** — ngưỡng mà test statistic phải vượt qua. Ví dụ $\alpha = 0.05$ two-tailed z-test → critical values $\pm 1.96$.
> **Tại sao A sai:** Test statistic tính từ **dữ liệu mẫu** ($\bar{X}$, $s$, $n$, và giá trị giả thuyết), không phải từ significance level.
> **Tại sao C sai:** $\alpha$ xác định xác suất **Type I error**, không phải [[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]]. Xác suất Type II error ($\beta$) phụ thuộc vào giá trị tham số thực, $n$, và $\alpha$ — nhưng không được trực tiếp xác định bởi $\alpha$.

---

## Question 11

The **probability of correctly rejecting a false null hypothesis** is:

- A. the [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]]
- B. the [[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|power of the test]]
- C. the level of significance

> [!answer]- Answer
> **B. the power of the test**
>
> The **power** of a hypothesis test is defined as:
>
> $$\text{Power} = 1 - \beta = P(\text{Reject } H_0 \mid H_0 \text{ is false})$$
>
> where $\beta$ is the probability of a [[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]]. Power measures the test's ability to detect a false null hypothesis.
>
> **Why A is wrong:** The p-value is the probability of observing a test statistic at least as extreme as the one calculated, assuming $H_0$ is true. It is used to evaluate evidence against $H_0$, not to measure the test's ability to detect falseness.
>
> **Why C is wrong:** The level of significance $\alpha$ is the probability of incorrectly rejecting a **true** $H_0$ ([[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]]) — the opposite of what the question asks.
>
> **Factors that increase power:** larger sample size, higher $\alpha$, larger true effect size, lower population variability.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|Power]] = $P(\text{Reject } H_0 \mid H_0 \text{ sai}) = 1 - \beta$. Power đo lường **khả năng phát hiện** $H_0$ sai — test tốt phải có power cao. Power phụ thuộc vào: sample size $n$, $\alpha$, effect size thực, và variance của population.
>
> **Tại sao B đúng:** $\beta$ = xác suất Type II error. Power = $1 - \beta$ = xác suất **không phạm** Type II error = xác suất reject đúng khi $H_0$ sai.
> **Tại sao A sai:** Power và significance level là hai khái niệm khác nhau: $\alpha$ = Type I error rate, power = $1 -$ Type II error rate. Tăng $\alpha$ thì power tăng, nhưng chúng không bằng nhau.
> **Tại sao C sai:** Tăng sample size $n$ **tăng power** — mẫu lớn hơn cung cấp nhiều thông tin hơn, giảm sampling error, dễ phát hiện $H_0$ sai hơn. Đây là lý do các nghiên cứu đủ mạnh cần cỡ mẫu đủ lớn.

---

## Question 12

The **[[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|power of a hypothesis test]]** is:

- A. equivalent to the significance level
- B. the probability of not making a [[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II error]]
- C. unchanged by increasing the sample size

> [!answer]- Answer
> **B. the probability of not making a Type II error**
>
> Power $= 1 - \beta = P(\text{Reject } H_0 \mid H_0 \text{ false})$. Since $\beta$ is the probability of a Type II error (failing to reject a false null), power is precisely the probability of **avoiding** a Type II error.
>
> **Why A is wrong:** Power and significance level are different concepts that trade off against each other. Increasing $\alpha$ (significance level) does increase power, but they are not equivalent — significance level is the Type I error rate while power is $1 -$ Type II error rate.
>
> **Why C is wrong:** Increasing sample size $n$ **increases power**. A larger sample provides more information about the population, reducing sampling error and making it easier to detect a false null hypothesis. This is why large samples can detect even very small, practically insignificant effects.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|Power]] = $1 - \beta$ = xác suất reject $H_0$ khi $H_0$ sai. Power là thước đo **hiệu quả** của test — test tốt phải có power cao. Power tăng khi: (1) $n$ tăng, (2) $\alpha$ tăng, (3) effect size thực lớn hơn, (4) variance thấp hơn.
>
> **Tại sao B đúng:** $\beta$ = xác suất Type II error. Power = $1 - \beta$ = xác suất **không phạm** Type II error. Đây là định nghĩa trực tiếp nhất của power.
> **Tại sao A sai:** Power và significance level là hai khái niệm **khác nhau**: $\alpha$ = Type I error rate (reject $H_0$ đúng), power = $1 - \beta$ = tránh Type II error. Tăng $\alpha$ có thể tăng power, nhưng chúng không bằng nhau.
> **Tại sao C sai:** Tăng sample size $n$ **tăng power** — mẫu lớn hơn giảm sampling error, dễ phát hiện $H_0$ sai hơn. Đây là lý do các study cần power analysis để xác định $n$ tối thiểu.

---

## Question 13

In the "**stating the decision rule**" step of hypothesis testing, the analyst must specify:

- A. the [[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|critical value]]
- B. the [[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|power of the test]]
- C. the value of the [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]]

> [!answer]- Answer
> **A. the critical value**
>
> The decision rule specifies the **critical value(s)** — the threshold(s) against which the test statistic will be compared. The decision rule states: "Reject $H_0$ if [test statistic] exceeds [critical value] in absolute value (two-tailed) or in one direction (one-tailed)."
>
> The critical value is determined by the significance level $\alpha$, the distribution of the test statistic (e.g., $t$, $z$, $F$, $\chi^2$), and the degrees of freedom.
>
> **Why B is wrong:** Power is not part of the decision rule — it is a property of the test that can be computed but is not stated as part of the formal decision procedure.
>
> **Why C is wrong:** The test statistic is computed from the **sample data** after data collection. The decision rule is stated *before* computing the test statistic, specifying what value the test statistic must exceed to reject $H_0$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Quy trình kiểm định giả thuyết gồm các bước: (1) Đặt giả thuyết, (2) Chọn test và significance level, (3) **Xác định decision rule** (critical value), (4) Thu thập dữ liệu và tính test statistic, (5) Kết luận.
>
> **Tại sao A đúng:** Bước "stating the decision rule" yêu cầu xác định **critical value** — ngưỡng quyết định trước khi xem dữ liệu. Critical value phụ thuộc vào $\alpha$, loại test statistic, và degrees of freedom.
> **Tại sao B sai:** [[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|Power]] không phải là một phần của decision rule — đó là thuộc tính của test có thể tính được nhưng không được phát biểu trong quy tắc quyết định chính thức.
> **Tại sao C sai:** Test statistic được tính **từ dữ liệu mẫu** sau khi thu thập dữ liệu. Decision rule phải được xác định **trước** khi tính test statistic để tránh bias trong kết luận.

---

## Question 14

A **pooled estimator** is used when testing the:

- A. equality of two population variances
- B. difference in means of two populations with unknown but assumed equal variances
- C. difference in means of two populations with unknown and unequal variances

> [!answer]- Answer
> **B. difference in means of two populations with unknown but assumed equal variances**
>
> When testing $H_0: \mu_1 = \mu_2$ and the population variances are unknown but assumed equal ($\sigma_1^2 = \sigma_2^2$), the two sample variances are **pooled** into a single estimate:
>
> $$s_p^2 = \frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2}$$
>
> This pooled variance is used in the [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-test]] statistic:
>
> $$t = \frac{(\bar{X}_1 - \bar{X}_2) - (\mu_1 - \mu_2)_0}{s_p\sqrt{\dfrac{1}{n_1} + \dfrac{1}{n_2}}}$$
>
> with $df = n_1 + n_2 - 2$.
>
> **Why A is wrong:** Testing equality of variances uses the **[[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-test]]** (ratio of two sample variances), not a pooled estimator.
>
> **Why C is wrong:** When variances are unequal (Welch's $t$-test), the two sample variances are **not** pooled — they are kept separate, and the degrees of freedom are adjusted (Welch-Satterthwaite approximation).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|Pooled t-test]] dùng khi: (1) so sánh trung bình hai tổng thể độc lập, (2) variance **chưa biết nhưng giả định bằng nhau**. Pooled variance kết hợp thông tin từ cả hai mẫu để ước lượng chính xác hơn variance chung.
>
> **Tại sao B đúng:** Khi $\sigma_1^2 = \sigma_2^2$ (unknown), ta **gộp** hai sample variance thành một ước lượng chung: $s_p^2 = \frac{(n_1-1)s_1^2 + (n_2-1)s_2^2}{n_1+n_2-2}$. Đây là trường hợp dùng pooled estimator.
> **Tại sao A sai:** Testing equality of variances dùng **[[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-test]]** (tỷ số hai sample variances), không phải pooled estimator.
> **Tại sao C sai:** Khi variances không bằng nhau (unequal), dùng **Welch's t-test** — hai variances được giữ riêng, không gộp lại. Degrees of freedom được điều chỉnh bằng Welch-Satterthwaite approximation.

---

## Question 15

For evaluating the **mean differences of two dependent (paired) samples**, the most appropriate test is:

- A. [[quantitative-methods/glossary/m08-hypothesis-testing#z-Test|z-test]]
- B. [[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|chi-square test]]
- C. paired comparisons test

> [!answer]- Answer
> **C. paired comparisons test**
>
> When two samples are **dependent** (i.e., each observation in one sample is naturally paired with an observation in the other — e.g., before/after measurements on the same subject, or matched pairs), the appropriate test is the **paired comparisons [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-test]]**.
>
> **Procedure:**
> 1. Compute the difference $d_i = X_{1i} - X_{2i}$ for each pair
> 2. Test $H_0: \mu_d = 0$ (or some other value) using:
> $$t = \frac{\bar{d} - \mu_{d,0}}{s_d / \sqrt{n}}$$
> with $df = n - 1$ (where $n$ = number of pairs)
>
> **Why A is wrong:** A z-test requires known population variances or very large samples, and does not account for the paired structure of the data.
>
> **Why B is wrong:** The chi-square test is used for testing a **single population variance** or **independence/goodness of fit** — not for comparing means of paired samples.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Paired comparisons t-test** (kiểm định cặp đôi) dùng khi hai mẫu **phụ thuộc nhau** — mỗi quan sát trong mẫu 1 được ghép cặp tự nhiên với một quan sát trong mẫu 2. Ví dụ: đo lường trước/sau điều trị trên cùng một đối tượng.
>
> **Tại sao C đúng:** Dữ liệu **phụ thuộc** (paired) yêu cầu paired comparisons t-test. Cách làm: tính $d_i = X_{1i} - X_{2i}$ cho từng cặp, rồi kiểm định $H_0: \mu_d = 0$ với $t = \bar{d}/(s_d/\sqrt{n})$, $df = n-1$.
> **Tại sao A sai:** Z-test yêu cầu variance đã biết hoặc mẫu rất lớn, và không xử lý cấu trúc paired của dữ liệu.
> **Tại sao B sai:** [[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|Chi-square test]] dùng để kiểm định **variance của một tổng thể** hoặc **independence/goodness of fit** — không dùng để so sánh trung bình của paired samples.

---

## Question 16

A **[[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|chi-square test]]** is most appropriate for testing:

- A. a single population variance
- B. the difference in means of two populations with equal variances
- C. the difference in means of two populations with unequal variances

> [!answer]- Answer
> **A. a single population variance**
>
> The chi-square ($\chi^2$) distribution arises naturally when testing hypotheses about a **single population variance**. The test statistic is:
>
> $$\chi^2 = \frac{(n-1)s^2}{\sigma_0^2}$$
>
> with $df = n - 1$, where $s^2$ is the sample variance and $\sigma_0^2$ is the hypothesised population variance.
>
> **Other uses of chi-square:** Testing independence in contingency tables and goodness-of-fit tests.
>
> **Why B is wrong:** Testing the difference in means with equal variances uses the **pooled [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-test]]**.
>
> **Why C is wrong:** Testing the difference in means with unequal variances uses **Welch's t-test**.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|Chi-square test]] ($\chi^2$) với **variance của một tổng thể** dùng test statistic: $\chi^2 = \frac{(n-1)s^2}{\sigma_0^2}$, phân phối chi-square với $df = n-1$. Phân phối $\chi^2$ chỉ nhận giá trị dương và lệch phải.
>
> **Tại sao A đúng:** Chi-square test phù hợp nhất để kiểm định **variance của một tổng thể** — ví dụ $H_0: \sigma^2 = \sigma_0^2$. Đây là ứng dụng cốt lõi của chi-square trong thống kê suy luận.
> **Tại sao B sai:** So sánh trung bình hai tổng thể với equal variances dùng **pooled t-test**.
> **Tại sao C sai:** So sánh trung bình hai tổng thể với unequal variances dùng **Welch's t-test**.

---

## Question 17

To test the **difference between the variances of two normal populations**, the most appropriate test is:

- A. [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-test]]
- B. [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-test]]
- C. paired comparisons test

> [!answer]- Answer
> **B. F-test**
>
> The $F$-statistic is the ratio of two sample variances, and follows an $F$-distribution under the null hypothesis of equal population variances:
>
> $$F = \frac{s_1^2}{s_2^2}$$
>
> where $s_1^2 \geq s_2^2$ by convention (so $F \geq 1$). The test has degrees of freedom $(n_1 - 1, n_2 - 1)$.
>
> $H_0: \sigma_1^2 = \sigma_2^2$ vs. $H_a: \sigma_1^2 \neq \sigma_2^2$ (two-tailed)
>
> **Why A is wrong:** The t-test is used for testing hypotheses about **means** (one sample or two samples), not variances.
>
> **Why C is wrong:** The paired comparisons t-test is used for testing mean differences in **dependent** samples, not for comparing variances.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-test]] so sánh **hai variances** bằng cách tính tỷ số $F = s_1^2/s_2^2$ (quy ước đặt variance lớn hơn ở tử số để $F \geq 1$). Phân phối F có hai bộ degrees of freedom: $(n_1-1, n_2-1)$.
>
> **Tại sao B đúng:** F-statistic = tỷ số hai sample variances, dùng để kiểm định $H_0: \sigma_1^2 = \sigma_2^2$. Phân phối F (Fisher) sinh ra tự nhiên từ tỷ số hai chi-square distributions.
> **Tại sao A sai:** T-test dùng để kiểm định **trung bình** (một mẫu hoặc hai mẫu), không phải variances.
> **Tại sao C sai:** Paired comparisons t-test dùng cho **mean differences** của dependent samples — không liên quan đến so sánh variances.

---

## Question 18

A **[[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|nonparametric test]]** is most appropriate when the:

- A. data consist of ranked values
- B. test's validity depends on many assumptions
- C. sample is large and drawn from a possibly non-normal population

> [!answer]- Answer
> **A. data consist of ranked values**
>
> Nonparametric tests are designed for **ordinal (ranked) data** or situations where the data do not meet the distributional assumptions required by [[quantitative-methods/glossary/m08-hypothesis-testing#Parametric Test|parametric tests]]. When data are expressed as ranks rather than precise numerical measurements, parametric tests (which assume interval or ratio-scale data) are inappropriate.
>
> **Common situations for nonparametric tests:**
> - Data are ordinal (ranked)
> - Population is heavily non-normal and sample is small
> - Data contain outliers that distort parametric results
> - No strong parametric model is available
>
> **Why B is wrong:** Parametric tests require many distributional assumptions (normality, known variance, etc.). Nonparametric tests are chosen when these assumptions **cannot** be met — but the reason for using them is not that "the test's validity depends on many assumptions" (that describes parametric tests themselves).
>
> **Why C is wrong:** For **large** samples from a non-normal population, the **[[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem|Central Limit Theorem]]** applies, and parametric tests (particularly the z-test) are valid. Nonparametric tests are most needed for **small** samples where the CLT does not apply.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|Nonparametric tests]] phù hợp khi: dữ liệu là **ordinal (ranked)**, hoặc tổng thể **không chuẩn** với **mẫu nhỏ**, hoặc dữ liệu có outliers làm sai lệch kết quả parametric. Nonparametric tests ít giả định hơn nhưng thường kém powerful hơn parametric tests khi giả định được thỏa mãn.
>
> **Tại sao A đúng:** Dữ liệu **ranked (ordinal)** không phù hợp với parametric tests vốn giả định dữ liệu interval/ratio. Nonparametric tests như Spearman rank correlation hay Mann-Whitney U được thiết kế cho dữ liệu rank.
> **Tại sao B sai:** Mẫu từ **tổng thể chuẩn** → giả định của parametric tests được thỏa mãn → parametric tests phù hợp hơn (có higher power).
> **Tại sao C sai:** Parametric tests mới là loại phụ thuộc nhiều giả định phân phối. Nonparametric tests được chọn **khi các giả định đó không thể biện minh**, không phải vì "validity phụ thuộc nhiều giả định".

---

## Question 19

A nonparametric test is most likely used when the:

- A. sample data are ranked by magnitude
- B. sample is drawn from a normal population
- C. test's validity depends on many population assumptions

> [!answer]- Answer
> **A. sample data are ranked by magnitude**
>
> This question reinforces the same core concept as Question 18. When data are expressed as **ranks** (ordinal scale) rather than exact values, [[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|nonparametric tests]] such as the [[quantitative-methods/glossary/m09-parametric-tests#Spearman Rank Correlation|Spearman rank correlation]], Mann-Whitney $U$, or Wilcoxon signed-rank test are appropriate.
>
> **Why B is wrong:** If the sample comes from a **normal** population, the distributional assumptions for parametric tests (such as the [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-test]]) are satisfied, making parametric tests preferable due to their greater power.
>
> **Why C is wrong:** Parametric tests are the ones whose validity depends on distributional assumptions. Nonparametric tests make fewer assumptions — they are chosen precisely when those parametric assumptions cannot be justified.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Câu hỏi này củng cố Q18 với một góc nhìn khác: khi dữ liệu là **ranked by magnitude** (được sắp xếp theo thứ tự), ta chỉ biết thứ hạng chứ không biết giá trị chính xác — parametric tests không phù hợp vì cần giá trị numerical.
>
> **Tại sao A đúng:** Dữ liệu ranked là dữ liệu ordinal — chỉ biết "A > B > C" nhưng không biết khoảng cách giữa chúng. Nonparametric tests như Spearman rank correlation, Mann-Whitney U, Wilcoxon signed-rank được thiết kế để xử lý loại dữ liệu này.
> **Tại sao B sai:** Tổng thể **chuẩn** → thỏa mãn giả định của parametric tests → nên dùng parametric tests (powerful hơn).
> **Tại sao C sai:** [[quantitative-methods/glossary/m08-hypothesis-testing#Parametric Test|Parametric tests]] mới là loại có validity phụ thuộc vào nhiều giả định phân phối (normality, known variance...). Nonparametric tests **ít giả định hơn** — được chọn chính xác khi những giả định parametric đó không thể biện minh.

---

## Question 20

Two funds have **non-normal return distributions**. An analyst has **1 year of monthly data** (12 observations) and wants to test whether the mean return of one fund is greater than the other. The most appropriate test is:

- A. [[quantitative-methods/glossary/m08-hypothesis-testing#Parametric Test|parametric tests]] only
- B. [[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|nonparametric tests]] only
- C. either parametric or nonparametric tests

> [!answer]- Answer
> **B. nonparametric tests only**
>
> This scenario has two characteristics that require a nonparametric approach:
>
> 1. **Non-normal distributions:** The standard parametric two-sample [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-test]] requires approximately normal populations (or large samples for CLT to apply).
> 2. **Small sample size ($n = 12$):** With only 12 monthly observations per fund, the sample is too small for the [[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem|Central Limit Theorem]] to reliably normalise the sampling distribution of the mean.
>
> With non-normal returns and a small sample, the assumptions of parametric tests are violated, making **nonparametric tests** (such as the **Mann-Whitney $U$ test** for comparing two independent group means) the only appropriate choice.
>
> **Why A is wrong:** Parametric tests require either normality or large samples. Neither condition holds here.
>
> **Why C is wrong:** Because the parametric test assumptions are clearly violated (non-normal + small $n$), parametric tests are **not** appropriate. The choice is not arbitrary.
>
> **Appropriate test:** The **Mann-Whitney $U$ test** (also called the Wilcoxon rank-sum test) compares the central tendency of two independent groups without assuming normality. It uses ranked data and is valid for small samples.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Khi chọn test thống kê, cần đánh giá hai yếu tố: (1) **Phân phối của tổng thể** (chuẩn hay không?), (2) **Cỡ mẫu** (lớn đủ để CLT áp dụng?). Nếu cả hai đều không thuận lợi → chỉ còn [[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|nonparametric tests]].
>
> **Tại sao B đúng:** Hai điều kiện **cùng lúc vi phạm** giả định parametric: (1) non-normal distributions + (2) $n = 12$ (mẫu nhỏ, CLT chưa đủ mạnh). Với non-normal + small sample, **Mann-Whitney U test** là lựa chọn duy nhất phù hợp để so sánh trung bình hai nhóm độc lập.
> **Tại sao A sai:** Parametric tests yêu cầu normality hoặc mẫu lớn. Ở đây cả hai điều kiện đều không thỏa mãn.
> **Tại sao C sai:** Vì parametric tests rõ ràng không phù hợp (non-normal + small $n$), lựa chọn **không phải tùy ý**. Chỉ nonparametric tests mới hợp lệ — C sai khi nói "either" (cái nào cũng được).
