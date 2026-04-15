---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - simulation-methods
  - lognormal
  - bootstrap
source: "CFAI CFA1 Quant Practice 2026, pp.191-192"
module: "[[quantitative-methods/modules/m06-simulation-methods/index|M06]]"
---

# M06 – Simulation Methods: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.191–192
**Back to module:** [[quantitative-methods/modules/m06-simulation-methods/index|M06]]
**Glossary**: [[quantitative-methods/glossary/m06-simulation-methods|M06 Terms]]

---

## Question 1

Mordice Corporation had the following weekly closing prices:

| Date | Closing Price |
|------|--------------|
| 1 Aug | 112 |
| 8 Aug | 160 |
| 15 Aug | 120 |

The **[[quantitative-methods/glossary/m06-simulation-methods#Continuously Compounded Return|continuously compounded return]]** from 1 August to 15 August is **closest to**:

- A. 6.90%
- B. 7.14%
- C. 8.95%

> [!answer]- Answer
> **A. 6.90%**
>
> **Method 1 – Direct calculation (1 Aug to 15 Aug):**
>
> The continuously compounded return over any holding period equals the natural log of the ending price divided by the beginning price:
>
> $$r_{cc} = \ln\!\left(\frac{P_T}{P_0}\right) = \ln\!\left(\frac{120}{112}\right) = \ln(1.07143) \approx 6.90\%$$
>
> **Method 2 – Sum of weekly continuously compounded returns:**
>
> Continuously compounded returns are additive over time:
>
> $$r_{1} = \ln\!\left(\frac{160}{112}\right) = \ln(1.42857) \approx 35.67\%$$
>
> $$r_{2} = \ln\!\left(\frac{120}{160}\right) = \ln(0.75000) \approx -28.77\%$$
>
> $$r_{total} = r_1 + r_2 = 35.67\% + (-28.77\%) = \mathbf{6.90\%}$$
>
> Both methods confirm **6.90%**. This additive property is one of the key advantages of continuously compounded (log) returns over simple holding period returns.
>
> **Why not B or C?**
> - B (7.14%) corresponds to the simple holding period return: $(120-112)/112 = 7.14\%$, which is not a continuously compounded return.
> - C (8.95%) is a distractor — no standard return calculation on these prices produces this value.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m06-simulation-methods#Continuously Compounded Return|Continuously compounded return]] (log return) được tính bằng ln(P_T / P_0). Tính chất quan trọng nhất: log return có **additive property** — tức là log return của cả kỳ bằng tổng log return của các kỳ con. Đây là lý do log return được dùng rộng rãi trong finance thay vì simple return.
>
> **Tại sao A (6.90%) đúng:** r_cc = ln(120/112) = ln(1.07143) ≈ **6.90%**. Hoặc tính riêng từng tuần: ln(160/112) + ln(120/160) = 35.67% + (−28.77%) = 6.90%. Cả hai phương pháp cho kết quả giống nhau nhờ additive property.
> **Tại sao B (7.14%) sai:** 7.14% = (120 − 112)/112 là **simple holding period return**, không phải continuously compounded return. Simple return không có additive property và luôn lớn hơn log return một chút khi dương.
> **Tại sao C (8.95%) sai:** Không có công thức return chuẩn nào tính ra 8.95% từ các giá này — đây là distractor để kiểm tra xem thí sinh có thực sự tính hay đoán mò.

---

## Question 2

In contrast to normal distributions, [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|lognormal distributions]]:

- A. are skewed to the left
- B. have outcomes that cannot be negative
- C. are more suitable for describing asset returns than asset prices

> [!answer]- Answer
> **B. have outcomes that cannot be negative**
>
> A lognormal distribution is the distribution of a variable $X$ where $\ln(X)$ is normally distributed. Key properties distinguishing it from the normal distribution:
>
> | Property | Normal Distribution | Lognormal Distribution |
> |----------|--------------------|-----------------------|
> | Support | $(-\infty, +\infty)$ | $(0, +\infty)$ — **cannot be negative** |
> | Skewness | Symmetric (skewness = 0) | **Positively skewed** (right tail) |
> | Best for | Returns (can be negative) | **Asset prices** (bounded below by zero) |
>
> **Why A is wrong:** Lognormal distributions are positively skewed (skewed to the **right**), not to the left. The right tail is longer because prices can theoretically rise without bound but cannot fall below zero.
>
> **Why C is wrong:** Lognormal distributions are more suitable for **asset prices**, not asset returns. Returns can be negative (e.g., a stock can lose value), so the normal distribution is the standard model for returns. Since prices cannot be negative, the lognormal model is used for prices.
>
> **Key relationship:** If continuously compounded returns $r_{cc} \sim N(\mu, \sigma^2)$, then the price relative $P_t/P_0 = e^{r_{cc}}$ follows a lognormal distribution.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|Lognormal distribution]] là phân phối của biến X mà ln(X) có phân phối chuẩn (normal). Hai đặc tính phân biệt với normal: (1) chỉ nhận giá trị dương — lower bound là 0, (2) lệch phải (positively skewed). Lognormal phù hợp để mô hình hóa **asset prices** vì giá không thể âm. Normal phù hợp để mô hình hóa **returns** vì return có thể âm.
>
> **Tại sao B (cannot be negative) đúng:** Lognormal distribution có support (0, +∞) — không thể nhận giá trị âm hoặc bằng 0. Đây là đặc tính cốt lõi phân biệt lognormal với normal (support từ −∞ đến +∞).
> **Tại sao A (skewed to the left) sai:** Lognormal lệch **phải** (positively skewed), không phải trái. Đuôi phải dài hơn vì giá có thể tăng không giới hạn nhưng không thể giảm dưới 0.
> **Tại sao C (more suitable for returns) sai:** Lognormal phù hợp với **asset prices**, không phải returns. Returns có thể âm (cổ phiếu có thể mất giá) nên dùng normal distribution. Prices không thể âm nên dùng lognormal.

---

## Question 3

The [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|lognormal distribution]] is a more accurate model for stock prices than the normal distribution because stock prices are:

- A. symmetrical
- B. unbounded
- C. non-negative

> [!answer]- Answer
> **C. non-negative**
>
> Stock prices cannot fall below zero — a stockholder's liability is limited to the amount invested (limited liability). The lognormal distribution has a **lower bound of zero**, making it consistent with this real-world constraint.
>
> The normal distribution, by contrast, extends to $-\infty$, which would imply a positive probability of negative prices — an economically impossible outcome.
>
> **Why A is wrong:** Stock price distributions are **not** symmetrical. They are positively skewed — large gains are possible (no upper bound), while losses are capped at 100% of the investment.
>
> **Why B is wrong:** "Unbounded" would suggest no upper limit on prices — while prices have no theoretical ceiling, the lognormal model is chosen specifically because of its **lower** bound (non-negativity), not its upper bound.
>
> **Summary:** The lognormal distribution is preferred for modelling stock prices because:
> 1. Prices cannot be negative (lower bound = 0)
> 2. Prices are positively skewed
> 3. If $\ln(P_t/P_0)$ is normally distributed, then $P_t/P_0$ is lognormally distributed

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|Lognormal distribution]] được chọn cho asset prices dựa trên hai đặc tính thực tế: (1) **limited liability** — cổ đông chỉ mất tối đa số tiền đã đầu tư, nên giá không thể âm; (2) **positive skewness** — giá có thể tăng không giới hạn nhưng chỉ giảm tối đa 100%. Normal distribution không thỏa mãn điều kiện non-negativity này.
>
> **Tại sao C (non-negative) đúng:** Giá cổ phiếu bị giới hạn dưới bởi zero do nguyên tắc limited liability. Lognormal có lower bound = 0, phù hợp với ràng buộc thực tế này. Normal distribution cho phép giá trị âm — không phù hợp về mặt kinh tế.
> **Tại sao A (symmetrical) sai:** Giá cổ phiếu **không** đối xứng. Chúng lệch phải (positively skewed) — mức tăng không bị giới hạn nhưng mức giảm tối đa là 100%. Nếu giá đối xứng thì normal distribution sẽ phù hợp hơn, không phải lognormal.
> **Tại sao B (unbounded) sai:** "Unbounded" ám chỉ không có giới hạn trên — nhưng lý do chọn lognormal chính là giới hạn **dưới** (non-negativity), không phải giới hạn trên. Mô hình lognormal thực ra ngầm định giá có thể tăng vô hạn (không có giới hạn trên).

---

## Question 4

Analysts performing **[[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|bootstrap]] resampling**:

- A. seek to create statistical inferences of population parameters from a single sample
- B. repeatedly draw samples of the same size with replacement from the original **population**
- C. must specify probability distributions for key risk factors

> [!answer]- Answer
> **A. seek to create statistical inferences of population parameters from a single sample**
>
> Bootstrap is a resampling method that allows analysts to make statistical inferences (e.g., estimate standard errors, construct confidence intervals) using only the **original observed sample** — without requiring a theoretical distribution or access to the full population.
>
> **How bootstrap works:**
> 1. Start with one original sample of size $n$
> 2. Repeatedly draw new samples of size $n$ **with replacement** from the **original sample** (not from the population)
> 3. Compute the statistic of interest for each resample
> 4. Use the distribution of resampled statistics to make inferences about the population parameter
>
> **Why B is wrong:** Bootstrap draws with replacement from the **original sample**, not the population. The key insight is that the sample serves as a proxy for the population. Drawing from the actual population would require census-level data, defeating the purpose.
>
> **Why C is wrong:** Requiring the analyst to **specify probability distributions** for key risk factors describes **[[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]]**, not bootstrap. Bootstrap is empirical — it uses the observed data's distribution without imposing a parametric form.
>
> | Method | Source of randomness | Distribution required? |
> |--------|---------------------|----------------------|
> | Bootstrap | Resample from original sample (with replacement) | No — uses empirical distribution |
> | Monte Carlo | Random draws from specified distributions | **Yes** — analyst must specify |
> | [[quantitative-methods/glossary/m06-simulation-methods#Jackknife|Jackknife]] | Leave-one-out from original sample | No |

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|Bootstrap]] là phương pháp resampling cho phép ước tính phân phối của một statistic chỉ từ **một mẫu duy nhất**, không cần biết phân phối của tổng thể. Cơ chế: lấy mẫu lặp lại **có hoàn lại** (with replacement) từ mẫu gốc — mẫu gốc đóng vai trò proxy cho population. Phân biệt với [[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]] — phương pháp này yêu cầu analyst chỉ định phân phối xác suất trước.
>
> **Tại sao A (inferences from a single sample) đúng:** Đây chính là mục tiêu cốt lõi của bootstrap — dùng một mẫu quan sát duy nhất để suy luận về population parameter (ví dụ: ước tính standard error, xây dựng confidence interval) mà không cần dữ liệu bổ sung hay giả định về phân phối.
> **Tại sao B (from original population) sai:** Bootstrap lấy mẫu lại từ **mẫu gốc** (original sample), không phải từ population. Nếu có thể lấy mẫu trực tiếp từ population thì không cần bootstrap. Đây là điểm phân biệt quan trọng nhất.
> **Tại sao C (specify probability distributions) sai:** Yêu cầu chỉ định probability distribution cho các risk factors mô tả **Monte Carlo simulation**, không phải bootstrap. Bootstrap là phương pháp empirical — dùng phân phối thực nghiệm của dữ liệu quan sát, không áp đặt dạng tham số.
