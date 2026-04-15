---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - estimation-and-inference
  - sampling
  - central-limit-theorem
  - bootstrap
  - jackknife
source: "CFAI CFA1 Quant Practice 2026, pp.212-213"
module: "[[quantitative-methods/modules/m07-estimation-and-inference/index|M07]]"
---

# M07 – Estimation and Inference: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.212–213
**Back to module:** [[quantitative-methods/modules/m07-estimation-and-inference/index|M07]]
**Glossary**: [[quantitative-methods/glossary/m07-estimation-and-inference|M07 Terms]]

---

## Question 1

Which of the following statements is **true** about **non-probability sampling**?

- A. There is a significant risk that the sample is not representative of the population
- B. Every member of the population has an equal chance of being selected
- C. Using judgment when selecting sample members guarantees representativeness

> [!answer]- Answer
> **A. There is a significant risk that the sample is not representative of the population**
>
> Non-probability sampling relies on factors other than random chance — such as convenience, researcher judgment, or voluntary participation — rather than probabilistic selection rules. Because selection is not governed by probability, there is **no guarantee** that the sample reflects the true characteristics of the population, creating significant risk of a non-representative (biased) sample.
>
> **Why B is wrong:** Having equal probability of selection describes **simple random sampling**, which is a form of *probability* sampling — the opposite of non-probability sampling.
>
> **Why C is wrong:** Using judgment actually *increases* the risk of bias, not eliminates it. Researchers may unconsciously favour certain observations, leading to systematic under- or over-representation of subgroups.
>
> **Types of non-probability sampling:**
> | Type | Description |
> |------|-------------|
> | Convenience sampling | Select whoever is easiest to reach |
> | Judgmental (purposive) | Analyst selects based on own criteria |
> | Quota sampling | Fill pre-set quotas by category |
>
> **Contrast with probability sampling:** In probability sampling (simple random, stratified, cluster, systematic), every population member has a known, non-zero probability of selection, reducing selection bias.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Non-Probability Sampling|Non-probability sampling]] là các phương pháp lấy mẫu không dựa trên quy tắc xác suất — bao gồm convenience sampling (lấy mẫu tiện lợi), judgmental sampling (lấy mẫu theo phán đoán), và quota sampling. Vì không có cơ chế xác suất, không thể đảm bảo tính đại diện của mẫu, dẫn đến nguy cơ **selection bias** cao.
>
> **Tại sao A (significant risk of non-representative sample) đúng:** Khi selection không dựa trên xác suất, không có gì đảm bảo mẫu phản ánh đúng tổng thể. Các nhóm con có thể bị over- hoặc under-represented một cách hệ thống, tạo ra bias trong kết quả nghiên cứu.
> **Tại sao B (equal chance of selection) sai:** Mọi thành viên có xác suất được chọn bằng nhau mô tả **simple random sampling** — đây là dạng probability sampling, ngược hoàn toàn với non-probability sampling.
> **Tại sao C (judgment guarantees representativeness) sai:** Judgment (phán đoán chủ quan) thực ra **tăng** nguy cơ bias, không loại trừ nó. Researcher có thể vô thức thiên vị về phía các quan sát dễ tiếp cận hoặc phù hợp với kỳ vọng sẵn có.

---

## Question 2

The **best approach** for constructing a **stratified random sample** is:

- A. drawing an equal number of simple random samples from each subpopulation
- B. selecting every $k$th member of the population
- C. drawing simple random samples from each subpopulation proportional to the relative size of each subpopulation

> [!answer]- Answer
> **C. drawing simple random samples from each subpopulation proportional to the relative size of each subpopulation**
>
> In stratified random sampling, the population is divided into mutually exclusive, exhaustive **strata** (subgroups). A simple random sample is then drawn from each stratum. For the combined sample to be **representative** of the population, each stratum should contribute observations in proportion to its share of the population.
>
> **Example:** If a bond index consists of 60% investment-grade and 40% high-yield bonds, a stratified sample of 100 bonds should include approximately 60 investment-grade and 40 high-yield bonds — maintaining the population proportions.
>
> **Why A is wrong:** Drawing equal numbers from each stratum (regardless of stratum size) creates a **disproportionate** stratified sample. This can be used deliberately to ensure enough observations in small strata, but it is not the standard definition and requires re-weighting for population-level inferences.
>
> **Why B is wrong:** Selecting every $k$th member describes **systematic (interval) sampling** — a different probability sampling method.
>
> **Key advantage of stratified sampling:** Ensures adequate representation of all subgroups, reducing sampling error compared to simple random sampling, especially when strata differ substantially in their characteristics.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Stratified Random Sampling|Stratified random sampling]] chia tổng thể thành các **strata** (tầng/nhóm con) có tính chất tương đồng nội bộ, rồi lấy simple random sample từ mỗi stratum. Để mẫu đại diện cho tổng thể, số quan sát từ mỗi stratum phải **tỷ lệ thuận với kích thước** của stratum đó trong tổng thể — gọi là proportional stratified sampling.
>
> **Tại sao C (proportional to relative size) đúng:** Lấy mẫu theo tỷ lệ kích thước của từng stratum đảm bảo cấu trúc mẫu phản ánh đúng cấu trúc tổng thể. Ví dụ: nếu bond index gồm 60% investment-grade và 40% high-yield, mẫu 100 trái phiếu nên có 60 investment-grade và 40 high-yield.
> **Tại sao A (equal number from each stratum) sai:** Lấy số lượng bằng nhau từ mỗi stratum tạo ra **disproportionate stratified sample** — tốt để đảm bảo đủ quan sát từ các nhóm nhỏ, nhưng không phải cách tiêu chuẩn và cần re-weighting khi suy luận về tổng thể.
> **Tại sao B (every kth member) sai:** Chọn mỗi phần tử thứ k mô tả **systematic (interval) sampling** — một phương pháp probability sampling khác hoàn toàn với stratified sampling.

---

## Question 3

A population has a **non-normal** distribution with mean $\mu$ and variance $\sigma^2$. The **[[quantitative-methods/glossary/m07-estimation-and-inference#Sampling Distribution|sampling distribution]]** of the sample mean $\bar{X}$ based on **large samples** is:

- A. the same distribution as the population distribution
- B. approximately normally distributed with mean approximately equal to the population mean
- C. approximately normally distributed with variance approximately equal to the population variance

> [!answer]- Answer
> **B. approximately normally distributed with mean approximately equal to the population mean**
>
> This is a direct application of the **[[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem|Central Limit Theorem]] (CLT)**: regardless of the shape of the underlying population distribution, the sampling distribution of the sample mean approaches a normal distribution as the sample size $n$ increases (typically $n \geq 30$ is considered sufficient).
>
> **Sampling distribution of $\bar{X}$:**
>
> $$\bar{X} \xrightarrow{d} N\!\left(\mu,\ \frac{\sigma^2}{n}\right) \quad \text{as } n \to \infty$$
>
> where:
> - $\mu$ = population mean (mean of $\bar{X}$ equals population mean)
> - $\dfrac{\sigma^2}{n}$ = variance of the sampling distribution (standard error squared)
>
> **Why A is wrong:** The sampling distribution of $\bar{X}$ is *not* the same as the population distribution. The CLT says it converges to a *normal* distribution regardless of the population's shape.
>
> **Why C is wrong:** The variance of $\bar{X}$ is $\dfrac{\sigma^2}{n}$, **not** $\sigma^2$. As sample size increases, the sampling distribution becomes more tightly concentrated around $\mu$ — the variance shrinks by the factor $1/n$.
>
> **Key CLT results:**
> | Property | Value |
> |----------|-------|
> | $E(\bar{X})$ | $\mu$ |
> | $\text{Var}(\bar{X})$ | $\sigma^2/n$ |
> | Shape (large $n$) | Approximately normal |
> | Shape requirement | None on population |

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem|Central Limit Theorem (CLT)]] là một trong những định lý quan trọng nhất trong thống kê: với sample size đủ lớn (thông thường n ≥ 30), sampling distribution của sample mean **xấp xỉ normal** bất kể phân phối gốc của tổng thể. Mean của sampling distribution bằng population mean μ, còn variance bằng σ²/n (nhỏ hơn population variance theo hệ số 1/n).
>
> **Tại sao B (approximately normal, mean ≈ population mean) đúng:** CLT đảm bảo X̄ ~ N(μ, σ²/n) khi n lớn. Mean của sampling distribution bằng đúng μ (X̄ là unbiased estimator). Đây là kết quả trực tiếp của CLT.
> **Tại sao A (same distribution as population) sai:** CLT khẳng định sampling distribution của X̄ **hội tụ về normal** bất kể dạng phân phối của tổng thể. Nếu tổng thể có phân phối non-normal, sampling distribution của X̄ vẫn normal khi n đủ lớn — không phải cùng dạng với tổng thể.
> **Tại sao C (variance ≈ population variance) sai:** Variance của X̄ là σ²/n, **không phải** σ². Khi n tăng, sampling distribution thu hẹp lại xung quanh μ — đây chính là lý do mẫu lớn hơn cho ước tính chính xác hơn. Nhầm σ²/n với σ² là lỗi rất phổ biến trong kỳ thi.

---

## Question 4

The **sample mean** is computed from a population with **variance** of 2.45 and a **sample size** of 40. The **[[quantitative-methods/glossary/m07-estimation-and-inference#Standard Error|standard error]]** of the sample mean is **closest to**:

- A. 0.039
- B. 0.247
- C. 0.387

> [!answer]- Answer
> **B. 0.247**
>
> The standard error of the sample mean is the standard deviation of the sampling distribution of $\bar{X}$:
>
> $$\sigma_{\bar{X}} = \frac{\sigma}{\sqrt{n}}$$
>
> where $\sigma$ is the population standard deviation and $n$ is the sample size.
>
> **Step 1 – Compute population standard deviation:**
>
> $$\sigma = \sqrt{\sigma^2} = \sqrt{2.45} \approx 1.5652$$
>
> **Step 2 – Compute standard error:**
>
> $$\sigma_{\bar{X}} = \frac{1.5652}{\sqrt{40}} = \frac{1.5652}{6.3246} \approx \mathbf{0.2474} \approx 0.247$$
>
> **Why A is wrong:** 0.039 corresponds to $\sigma^2/n = 2.45/40 / \sqrt{?}$ — this is not a standard formula for standard error.
>
> **Why C is wrong:** 0.387 would result from dividing $\sigma = 1.565$ by $\sqrt{n} \approx \sqrt{16}$, not $\sqrt{40}$.
>
> **Note:** If the population standard deviation is unknown (which is common in practice), the sample standard deviation $s$ is substituted, giving the estimated standard error $s/\sqrt{n}$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Standard Error|Standard error]] của sample mean đo lường mức độ biến động của X̄ quanh μ, tức là độ chính xác của ước tính. Công thức: σ_X̄ = σ/√n, trong đó σ là population standard deviation và n là sample size. Lưu ý: bài cho **variance** (σ² = 2.45), nên phải lấy căn bậc hai để có σ trước khi tính standard error.
>
> **Tại sao B (0.247) đúng:** σ = √2.45 ≈ 1.5652. Standard error = 1.5652/√40 = 1.5652/6.3246 ≈ **0.247**. Bước quan trọng: chuyển variance → standard deviation trước, rồi mới chia cho √n.
> **Tại sao A (0.039) sai:** 0.039 ≈ 2.45/40/√(?) — không có công thức standard error chuẩn nào cho kết quả này. Có thể do nhầm: tính σ²/n = 0.0613 rồi chia thêm một lần nữa cho √n, hoặc lỗi tính toán khác.
> **Tại sao C (0.387) sai:** 0.387 ≈ 1.565/√(16.35) — tương đương việc dùng n ≈ 16 thay vì n = 40. Lỗi có thể do nhầm √40 ≈ 4.0 thay vì 6.32, hoặc tính nhầm căn bậc hai của 40.

---

## Question 5

Compared with **[[quantitative-methods/glossary/m07-estimation-and-inference#Bootstrap|bootstrap]]** resampling, **[[quantitative-methods/glossary/m07-estimation-and-inference#Jackknife|jackknife]]** resampling:

- A. is done with replacement
- B. usually requires the number of repetitions equal to the sample size
- C. produces dissimilar results every time it is run

> [!answer]- Answer
> **B. usually requires the number of repetitions equal to the sample size**
>
> **Jackknife resampling** works by systematically leaving out one observation at a time from the original sample of size $n$, computing the statistic of interest on the remaining $n-1$ observations, and repeating this for every observation. This results in exactly $n$ resamples — one for each observation that is left out.
>
> **Comparison of resampling methods:**
>
> | Feature | Bootstrap | Jackknife |
> |---------|-----------|-----------|
> | Method | Draw $n$ obs **with replacement** from original sample | Leave out **one** observation at a time |
> | Number of repetitions | Analyst-specified (e.g., 1,000+) | Always exactly $n$ |
> | Deterministic? | **No** — random draws vary each run | **Yes** — always same result |
> | Distribution assumed? | No | No |
>
> **Why A is wrong:** Sampling with replacement describes **bootstrap**, not jackknife. Jackknife uses leave-one-out subsamples drawn **without** replacement from the original sample.
>
> **Why C is wrong:** Jackknife is **deterministic** — because it systematically leaves out each observation in turn (rather than drawing randomly), it produces the **same** results every time it is run on the same data. Bootstrap, by contrast, uses random draws and will produce slightly different results across runs.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Jackknife|Jackknife]] và [[quantitative-methods/glossary/m07-estimation-and-inference#Bootstrap|bootstrap]] đều là resampling methods nhưng khác nhau về cơ chế. Jackknife: loại bỏ **một** quan sát mỗi lần, tạo ra đúng n sub-samples — **deterministic** (kết quả giống nhau mỗi lần chạy). Bootstrap: lấy mẫu ngẫu nhiên **có hoàn lại** từ mẫu gốc, số lần lặp do analyst chọn — **stochastic** (kết quả có thể khác nhau giữa các lần chạy).
>
> **Tại sao B (repetitions = sample size) đúng:** Jackknife leave-one-out tạo ra đúng **n sub-samples** — một sub-sample cho mỗi quan sát bị loại. Với sample size n = 100, jackknife chạy đúng 100 lần. Đây là đặc trưng deterministic của jackknife.
> **Tại sao A (done with replacement) sai:** Sampling **with replacement** mô tả **bootstrap**, không phải jackknife. Jackknife dùng leave-one-out — loại bỏ một quan sát mà không hoàn lại, tạo sub-samples kích thước n−1.
> **Tại sao C (dissimilar results every time) sai:** Jackknife là **deterministic** — vì loại bỏ từng quan sát theo thứ tự cố định, nó luôn cho kết quả giống nhau trên cùng dữ liệu. Chính bootstrap mới cho kết quả hơi khác nhau giữa các lần chạy do tính ngẫu nhiên của sampling.
