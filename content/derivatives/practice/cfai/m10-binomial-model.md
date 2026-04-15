---
type: practice
tags:
  - cfai-official
  - derivatives
  - binomial-model
source: "CFAI CFA1 Derivatives Practice 2026 – Volume 7"
module: "[[m10-binomial-model]]"
---

# M10 – Binomial Model: CFAI Practice Problems

**Source:** CFAI CFA1 Derivatives Practice 2026 – Volume 7
**Back to module:** [[m10-binomial-model]]

---

> **Exhibit: SAPP**
>
> Sarah Park (SAPP) introduces the one-period binomial option pricing model to junior analysts. She explains how to construct a replicating portfolio, calculate risk-neutral probabilities, and price options using the binomial framework. She presents several scenarios involving changes in model inputs and asks analysts to evaluate the impact on option values.

---

## Question 1

In a one-period binomial model, all else being equal, if the size of the down move increases (i.e., the down factor $d$ decreases), the value of a European put option will most likely:

- A. Decrease
- B. Increase
- C. Remain unchanged

> [!answer]- Answer
> **A. Decrease**
>
> When the down factor $d$ decreases (larger down move), the risk-neutral probability of an up move ($\pi_u$) increases (since $\pi_u = \frac{(1+r) - d}{u - d}$ and a smaller $d$ increases the numerator). A higher probability of an up move means less weight on the down-state payoff, which is where the put has value. This decreases the expected payoff of the put under risk-neutral probabilities, reducing its value.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Binomial model — Risk-neutral probability:
> $$\pi_u = \frac{(1+r) - d}{u - d}$$
> $$\pi_d = 1 - \pi_u$$
>
> Option value:
> $$p_0 = \frac{\pi_u \cdot p_u + \pi_d \cdot p_d}{1 + r}$$
>
> **Phân tích khi $d$ giảm:**
> 1. $\pi_u = \frac{(1+r) - d}{u - d}$ — tử số $(1+r) - d$ tăng khi $d$ giảm
> 2. Mẫu số $u - d$ cũng tăng, nhưng tử số tăng nhanh hơn → $\pi_u$ tăng
> 3. $\pi_d = 1 - \pi_u$ giảm
> 4. Put có payoff cao ở down state → $\pi_d$ giảm → expected payoff giảm → **put value giảm**
>
> **Tại sao A đúng:** $d$ giảm → $\pi_u$ tăng → ít trọng số vào down state (nơi put ITM) → put value giảm.
>
> **Tại sao B sai:** Mặc dù down move lớn hơn tạo payoff put cao hơn trong down state, risk-neutral probability $\pi_d$ giảm đủ để net effect là put value giảm.
> **Tại sao C sai:** Thay đổi $d$ ảnh hưởng trực tiếp đến risk-neutral probabilities và do đó ảnh hưởng option value.

---

## Question 2

In the one-period binomial model, option values are determined by:

- A. Actual (real-world) probabilities of up and down moves discounted at the expected return
- B. Risk-neutral probabilities of up and down moves discounted at the risk-free rate
- C. Risk-neutral probabilities of up and down moves discounted at the expected return on the underlying

> [!answer]- Answer
> **B. Risk-neutral probabilities of up and down moves discounted at the risk-free rate**
>
> The binomial model uses risk-neutral pricing: expected payoffs are calculated using risk-neutral probabilities ($\pi_u$ and $\pi_d$) and then discounted at the risk-free rate. This approach gives the same result as the replicating portfolio method and does not require knowledge of actual probabilities or expected returns.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Risk-neutral pricing principle:
> $$V_0 = \frac{\pi_u \cdot V_u + \pi_d \cdot V_d}{1 + r_f}$$
>
> Trong đó:
> - $\pi_u, \pi_d$: **Risk-neutral** probabilities (không phải actual probabilities)
> - $r_f$: **Risk-free rate** (không phải expected return)
> - $V_u, V_d$: Option payoffs in up/down states
>
> **Tại sao B đúng:** Binomial model sử dụng risk-neutral framework:
> 1. Tính risk-neutral probabilities từ $u, d, r_f$
> 2. Tính expected payoff dưới risk-neutral measure
> 3. Discount bằng risk-free rate
>
> Ưu điểm: Không cần biết actual probabilities hay risk preferences của investors.
>
> **Tại sao A sai:** Actual probabilities + expected return là real-world pricing — phức tạp hơn và cho cùng kết quả. Binomial model dùng risk-neutral approach đơn giản hơn.
> **Tại sao C sai:** Risk-neutral probabilities phải discount bằng risk-free rate, không phải expected return. Sử dụng expected return sẽ "double count" risk adjustment.
