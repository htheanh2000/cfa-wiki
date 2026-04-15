---
type: practice
tags:
  - cfai-official
  - derivatives
  - arbitrage
  - replication
  - law-of-one-price
  - cost-of-carry
  - forward-pricing
source: "CFAI CFA1 Derivatives Practice 2026 – Volume 7"
module: "[[m04-arbitrage-replication]]"
---

# M04 – Arbitrage, Replication, and the Cost of Carry — CFAI Practice Problems

**Source:** CFAI CFA1 Derivatives Practice 2026 – Volume 7
**Back to module:** [[m04-arbitrage-replication]]
**Glossary**: [[derivatives/glossary/m04-arbitrage-replication|M04 Terms]]

---

## Question 1

The **law of one price** states that:

- A. all assets in the same asset class must have the same expected return.
- B. two assets or portfolios with identical future cash flows must sell for the same price today.
- C. the price of an asset must equal its book value in an efficient market.

> [!answer]- Answer
> **B. two assets or portfolios with identical future cash flows must sell for the same price today.**
>
> The **law of one price** is a foundational principle of derivative pricing: if two assets produce identical cash flows in all future states of the world, they must have the same current price. If they do not, an arbitrage opportunity exists — market participants would buy the cheaper asset and sell the more expensive one until prices converge.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Law of one price: hai tài sản/portfolio có cùng cash flows trong mọi tình huống tương lai → phải có cùng giá hiện tại. Nếu giá khác nhau → cơ hội arbitrage → thị trường sẽ tự điều chỉnh.
> **Tại sao A sai:** Law of one price nói về **giá**, không phải expected return. Các tài sản cùng asset class có thể có expected return khác nhau tùy rủi ro riêng.
> **Tại sao C sai:** Giá thị trường không nhất thiết bằng book value. Law of one price so sánh hai tài sản có cùng cash flows, không phải so sánh giá với book value.

---

## Question 2

An analyst observes that an asset trades at different prices on two exchanges at the same time. The analyst can **most likely** earn a risk-free profit by:

- A. buying on the exchange with the higher price and selling on the exchange with the lower price.
- B. buying on the exchange with the lower price and selling on the exchange with the higher price.
- C. buying on both exchanges simultaneously and waiting for prices to converge.

> [!answer]- Answer
> **B. buying on the exchange with the lower price and selling on the exchange with the higher price.**
>
> This is a classic **arbitrage** opportunity. The analyst buys the asset where it is cheap and simultaneously sells it where it is expensive, locking in a risk-free profit equal to the price difference (minus transaction costs). Arbitrage requires no net investment and no risk — the positions offset each other.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Arbitrage = buy low, sell high đồng thời trên hai thị trường:
> - Mua ở sàn giá thấp → chi phí thấp
> - Bán ở sàn giá cao → thu nhập cao
> - Lợi nhuận = chênh lệch giá (trừ transaction costs) → risk-free
>
> **Tại sao A sai:** Mua giá cao, bán giá thấp → thua lỗ chắc chắn — ngược hoàn toàn với arbitrage.
> **Tại sao C sai:** Mua ở cả hai sàn → có net long position → chịu rủi ro giá giảm. Arbitrage yêu cầu vị thế đối nghịch (mua ở sàn này, bán ở sàn kia).

---

## Question 3

A forward contract on a non-dividend-paying stock can be **replicated** by:

- A. buying the stock today and borrowing the purchase price at the risk-free rate.
- B. selling the stock short today and lending the proceeds at the risk-free rate.
- C. buying a call option and selling a put option with the same strike price.

> [!answer]- Answer
> **A. buying the stock today and borrowing the purchase price at the risk-free rate.**
>
> A **long forward** can be replicated by: (1) buying the underlying asset at its current spot price $S_0$, and (2) borrowing $S_0$ at the risk-free rate $r$ for the contract period $T$. At expiration, the investor owns the asset and owes $S_0 \times (1 + r)^T$, which replicates the payoff of a long forward with forward price $F_0 = S_0 \times (1 + r)^T$.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** Replication of long forward:
> - Bước 1: Mua stock ở giá $S_0$ (spot price)
> - Bước 2: Vay $S_0$ với lãi suất $r$ trong thời gian $T$
> - Tại thời điểm $T$: có stock (giá trị = $S_T$), nợ $S_0(1+r)^T$
> - Payoff = $S_T - S_0(1+r)^T$ → giống long forward với $F_0 = S_0(1+r)^T$
>
> **Tại sao B sai:** Short stock + lend = replication of **short forward**, không phải long forward.
> **Tại sao C sai:** Long call + short put = synthetic forward (qua put-call parity), nhưng câu hỏi hỏi về replication bằng spot + borrowing — phương pháp cơ bản nhất.

---

## Question 4

According to the **cost of carry model**, the forward price of an asset is given by:

$$F_0 = S_0 \times (1 + r)^T$$

This formula assumes the underlying asset has:

- A. continuous dividend payments and storage costs.
- B. no interim cash flows, no benefits, and no carrying costs other than financing.
- C. a convenience yield that exceeds the risk-free rate.

> [!answer]- Answer
> **B. no interim cash flows, no benefits, and no carrying costs other than financing.**
>
> The basic cost of carry formula $F_0 = S_0 \times (1 + r)^T$ applies to an asset with **no carrying costs** beyond the financing cost (risk-free rate) and **no benefits** (dividends, coupon payments, convenience yield). If the asset had benefits or costs, the formula would adjust to: $F_0 = S_0 \times (1 + r)^T - \text{FV(Benefits)} + \text{FV(Costs)}$.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Công thức cơ bản $F_0 = S_0(1+r)^T$ giả định:
> - Không có interim cash flows (cổ tức, coupon)
> - Không có benefits (convenience yield)
> - Không có carrying costs khác ngoài chi phí tài trợ (financing = lãi suất $r$)
> - Ví dụ: cổ phiếu không trả cổ tức, vàng không có storage cost
>
> **Tại sao A sai:** Nếu có dividend và storage costs, công thức phải điều chỉnh: $F_0 = (S_0 + \text{FV(Costs)} - \text{FV(Benefits)}) \times (1+r)^T$ hoặc tương đương.
> **Tại sao C sai:** Convenience yield là một benefit → làm giảm forward price so với công thức cơ bản. Công thức trên không bao gồm convenience yield.

---

## Question 5

A commodity has a spot price of \$100, the annual risk-free rate is 5%, and the contract expires in one year. The commodity has annual storage costs of \$3 (paid at end of year) and provides a convenience yield with a present value of \$2. The **net cost of carry** and the theoretical forward price are **closest to**:

- A. Net cost of carry = \$6; Forward price = \$106.
- B. Net cost of carry = \$8; Forward price = \$108.
- C. Net cost of carry = \$3; Forward price = \$103.

> [!answer]- Answer
> **A. Net cost of carry = \$6; Forward price = \$106.**
>
> **Step 1:** Financing cost = $S_0 \times r = 100 \times 0.05 = \$5$
> **Step 2:** Storage costs = \$3
> **Step 3:** Total carrying costs = $5 + 3 = \$8$
> **Step 4:** Benefits = convenience yield FV = $2 \times (1.05) = \$2.10 \approx \$2$
> **Step 5:** Net cost of carry = Total costs − Benefits = $8 - 2 = \$6$
> **Step 6:** Forward price = $S_0 + \text{Net cost of carry} = 100 + 6 = \$106$
>
> Alternatively: $F_0 = S_0(1+r)^T + \text{FV(Storage)} - \text{FV(Convenience yield)} = 105 + 3 - 2.10 \approx \$106$.

> [!tip]- 📖 Giải thích chi tiết
> **Công thức cost of carry mở rộng:**
> $$F_0 = S_0(1+r)^T + \text{FV(Costs)} - \text{FV(Benefits)}$$
>
> **Tính toán chi tiết:**
> - $S_0 = \$100$, $r = 5\%$, $T = 1$ năm
> - Financing cost: $100 \times 0.05 = \$5$
> - Storage cost (cuối năm): \$3
> - Convenience yield PV = \$2 → FV = $2 \times 1.05 = \$2.10$
> - $F_0 = 105 + 3 - 2.10 = \$105.90 \approx \$106$
>
> **Net cost of carry** = (financing + storage) − benefits = $(5 + 3) - 2 = \$6$
>
> **Tại sao B sai:** \$108 không trừ convenience yield — quên benefit.
> **Tại sao C sai:** \$103 chỉ tính storage cost, quên financing cost.
