---
title: "M04 — Probability"
type: module
subject: quantitative-methods
module: M04
los: ["Pre.i", "Pre.ii", "Pre.iii", "Pre.iv", "Pre.v", "Pre.vi", "Pre.vii", "4.a", "4.b", "4.c"]
created: 2026-04-09
updated: 2026-04-09
tags: [probability, bayes, expected-value, variance, conditional, counting]
---

# Module 4: Probability Trees and Conditional Expectations

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 179–211

## Learning Outcomes

| LOS | Mô tả |
|-----|-------------|
| Pre.i–iii | Biến ngẫu nhiên, sự kiện, mutually exclusive/exhaustive, các loại xác suất, odds |
| Pre.iv | Conditional probabilities |
| Pre.v | Quy tắc nhân và cộng xác suất; sự kiện phụ thuộc và độc lập |
| Pre.vi | Total probability rule |
| Pre.vii | Factorial, combination, permutation |
| 4.a | Expected values, variances, standard deviations trong các bài toán đầu tư |
| 4.b | Probability trees và conditional expectations |
| 4.c | Bayes' formula |

## Khái Niệm Cơ Bản

| Thuật ngữ | Định nghĩa |
|------|-----------|
| **Random variable** | Đại lượng mà giá trị trong tương lai còn chưa chắc chắn |
| **Outcome** | Một giá trị có thể xảy ra của random variable |
| **Event** | Một outcome hoặc một tập hợp outcome xác định |
| **Probability** | Khả năng xảy ra của một event: $0 \leq P(E) \leq 1$ |

## Các Loại Probability

| Loại | Cách xác định |
|------|---------------|
| **Subjective** | Dựa trên phán đoán cá nhân ("Tôi tin có 70% khả năng...") |
| **Empirical** | Phân tích dữ liệu quá khứ (tần suất lịch sử) |
| **A priori** | Lập luận hình thức (ví dụ: $P = \frac{1}{6}$ cho một con xúc xắc cân bằng) |

## Odds

$$
\text{Odds for } E = \frac{P(E)}{1 - P(E)} \qquad \text{Odds against } E = \frac{1 - P(E)}{P(E)}
$$

## Các Quy Tắc Probability

### Conditional Probability

$$
P(A|B) = \frac{P(AB)}{P(B)}
$$

### Addition Rule

- Không mutually exclusive: $P(A \text{ or } B) = P(A) + P(B) - P(AB)$
- Mutually exclusive: $P(A \text{ or } B) = P(A) + P(B)$

### Multiplication Rule

- Sự kiện phụ thuộc (dependent events): $P(AB) = P(A|B) \cdot P(B)$
- Sự kiện độc lập (independent events): $P(AB) = P(A) \cdot P(B)$

### Total Probability Rule

$$
P(A) = \sum_{i=1}^{N} P(A|B_i) \cdot P(B_i)
$$

trong đó $B_1, B_2, \ldots, B_N$ là mutually exclusive và exhaustive

## Expected Value và Variance (LOS 4.a)

**Expected Value:**

$$
E(X) = \sum_{i=1}^{n} P(X_i) \cdot X_i
$$

**Variance:**

$$
\sigma^2(X) = \sum_{i=1}^{n} P(X_i) \cdot [X_i - E(X)]^2
$$

**Standard Deviation:**

$$
\sigma(X) = \sqrt{\sigma^2(X)}
$$

## Bayes' Formula (LOS 4.c)

$$
P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}
$$

Dùng để **cập nhật xác suất** khi có thông tin mới. Mẫu số được tính bằng total probability rule.

## Counting Principles (Pre.vii)

| Phương pháp | Công thức | Thứ tự có quan trọng? | Trường hợp sử dụng |
|--------|---------|----------------|----------|
| **Factorial** | $n!$ | Có | Tổng số cách sắp xếp $n$ phần tử |
| **Permutation** | $P(n,r) = \frac{n!}{(n-r)!}$ | Có | Chọn $r$ từ $n$ phần tử có quan tâm thứ tự |
| **Combination** | $C(n,r) = \frac{n!}{r!(n-r)!}$ | Không | Chọn $r$ từ $n$ phần tử, không quan tâm thứ tự |

## Liên Kết

- Xây dựng từ: [[quantitative-methods/modules/m03-statistical-measures/index|M03 — Statistics]]
- Mở rộng sang: [[quantitative-methods/modules/m05-portfolio-mathematics/index|M05 — Portfolio Math]] (expected values của danh mục đầu tư)
- Ứng dụng trong: [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — Hypothesis Testing]]
- Công thức: [[quantitative-methods/formulas/probability|All M04 Formulas]]