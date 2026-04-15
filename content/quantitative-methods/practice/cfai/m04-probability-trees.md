---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - probability
  - probability-trees
source: "CFAI CFA1 Quant Practice 2026, pp.149-150"
module: "[[m04-probability-trees]]"
---

# M04 – Probability Trees and Expected Value: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.149–150
**Back to module:** [[m04-probability-trees]]
**Glossary**: [[quantitative-methods/glossary/m04-probability|M04 Terms]]

---

## Question 1

A bank has USD 100,000 in defaulted loans. Recovery proceeds depend on two scenarios:

**Scenario 1** (probability = 40%):
- Recover USD 50,000 with probability 60%
- Recover USD 30,000 with probability 40%

**Scenario 2** (probability = 60%):
- Recover USD 80,000 with probability 90%
- Recover USD 60,000 with probability 10%

The [[quantitative-methods/glossary/m04-probability#Expected Value|expected recovery]] is **closest to**:

- A. USD 36,400
- B. USD 55,000
- C. USD 63,600

> [!answer]- Answer
> **C. USD 63,600**
>
> **Probability tree:**
>
> ```
>                         ┌─ 50,000 (p = 0.60)
>          Scenario 1 ───┤
>         (p = 0.40)     └─ 30,000 (p = 0.40)
> ROOT ───┤
>         │              ┌─ 80,000 (p = 0.90)
>          Scenario 2 ───┤
>         (p = 0.60)     └─ 60,000 (p = 0.10)
> ```
>
> **Step 1 – Expected recovery within each scenario:**
>
> $$E(\text{Recovery} \mid S_1) = 0.60 \times 50{,}000 + 0.40 \times 30{,}000 = 30{,}000 + 12{,}000 = 42{,}000$$
>
> $$E(\text{Recovery} \mid S_2) = 0.90 \times 80{,}000 + 0.10 \times 60{,}000 = 72{,}000 + 6{,}000 = 78{,}000$$
>
> **Step 2 – Unconditional expected recovery ([[quantitative-methods/glossary/m04-probability#Total Probability Rule|law of total expectation]]):**
>
> $$E(\text{Recovery}) = P(S_1) \times E(S_1) + P(S_2) \times E(S_2)$$
>
> $$E(\text{Recovery}) = 0.40 \times 42{,}000 + 0.60 \times 78{,}000 = 16{,}800 + 46{,}800 = \mathbf{USD\ 63{,}600}$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Bài này dùng [[quantitative-methods/glossary/m04-probability#Expected Value|expected value]] kết hợp với [[quantitative-methods/glossary/m04-probability#Total Probability Rule|total probability rule]] (quy tắc xác suất toàn phần) thông qua một probability tree (cây xác suất) hai tầng. Giá trị kỳ vọng có điều kiện được tính trong từng scenario, rồi kết hợp lại bằng trọng số xác suất của mỗi scenario.
>
> **Tại sao C (USD 63,600) đúng:** Tính E(Recovery | S1) = 0.60 × 50,000 + 0.40 × 30,000 = 42,000. Tính E(Recovery | S2) = 0.90 × 80,000 + 0.10 × 60,000 = 78,000. Áp dụng total probability rule: E(Recovery) = 0.40 × 42,000 + 0.60 × 78,000 = 16,800 + 46,800 = **63,600**.
> **Tại sao A (USD 36,400) sai:** Đây không phải kết quả của bất kỳ phép tính chuẩn nào — có thể do nhầm trọng số xác suất của hai scenario (dùng 0.60 cho S1 và 0.40 cho S2 thay vì ngược lại).
> **Tại sao B (USD 55,000) sai:** USD 55,000 là trung bình đơn giản không có trọng số của các outcome (50,000 + 30,000 + 80,000 + 60,000) / 4 = 55,000 — bỏ qua hoàn toàn xác suất của từng nhánh.

---

## Question 2

An analyst estimates the following probability distribution for a company's annual sales:

| Probability | Sales |
|-------------|-------|
| 0.05 | USD 70 million |
| 0.70 | USD 40 million |
| 0.25 | USD 25 million |

The standard deviation of sales is **closest to**:

- A. USD 9.81 million
- B. USD 12.20 million
- C. USD 32.40 million

> [!answer]- Answer
> **A. USD 9.81 million**
>
> **Step 1 – [[quantitative-methods/glossary/m04-probability#Expected Value|Expected sales]]:**
>
> $$E(\text{Sales}) = 0.05 \times 70 + 0.70 \times 40 + 0.25 \times 25$$
>
> $$E(\text{Sales}) = 3.50 + 28.00 + 6.25 = \text{USD } 37.75 \text{ million}$$
>
> **Step 2 – Variance:**
>
> | Outcome | $P_i$ | $S_i - E(S)$ | $(S_i - E(S))^2$ | $P_i \times (S_i - E(S))^2$ |
> |---------|--------|--------------|------------------|-----------------------------|
> | 70M | 0.05 | +32.25 | 1,040.0625 | 52.0031 |
> | 40M | 0.70 | +2.25 | 5.0625 | 3.5438 |
> | 25M | 0.25 | −12.75 | 162.5625 | 40.6406 |
> | **Total** | | | | **96.1875** |
>
> $$\sigma^2 = 96.1875 \text{ (million}^2\text{)}$$
>
> **Step 3 – Standard deviation:**
>
> $$\sigma = \sqrt{96.1875} \approx \mathbf{USD\ 9.81 \text{ million}}$$
>
> Note: Answer C (USD 32.40M) would result from confusing the range (70 − 25 = 45) with the standard deviation — a common error. Answer B may result from an arithmetic mistake in weighting.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m04-probability#Expected Value|Standard deviation]] của một random variable rời rạc được tính qua ba bước: (1) tính expected value E(X), (2) tính variance σ² = Σ Pᵢ × (Xᵢ − E(X))², (3) lấy căn bậc hai. Đây là công thức [[quantitative-methods/glossary/m04-probability#Variance|variance của random variable]] có trọng số xác suất — khác với sample variance thông thường.
>
> **Tại sao A (USD 9.81 million) đúng:** E(Sales) = 0.05×70 + 0.70×40 + 0.25×25 = 37.75M. Variance = 0.05×(32.25)² + 0.70×(2.25)² + 0.25×(−12.75)² = 52.00 + 3.54 + 40.64 = 96.19. Standard deviation = √96.19 ≈ **9.81M**.
> **Tại sao B (USD 12.20 million) sai:** Kết quả này có thể do lỗi tính toán khi weighting các deviation — ví dụ dùng sai xác suất hoặc tính (Sᵢ − E(S)) không chính xác. Không có đường tắt nào dẫn đến 12.20 với số liệu này.
> **Tại sao C (USD 32.40 million) sai:** USD 32.40M ≈ (70 − 25) × 0.72 — nhầm standard deviation với một bội số của range (khoảng cách giữa giá trị lớn nhất và nhỏ nhất). Range không phản ánh xác suất nên không thể dùng thay thế standard deviation.
