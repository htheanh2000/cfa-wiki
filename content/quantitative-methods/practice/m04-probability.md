---
title: "Practice: M04 — Probability"
type: practice
subject: quantitative-methods
module: M04
created: 2026-04-09
updated: 2026-04-09
tags: [practice, probability, bayes, counting]
---

# Practice: M04 — Probability

**Module**: [[quantitative-methods/modules/m04-probability-trees/index|M04]]
**Formulas**: [[quantitative-methods/formulas/probability|Probability Formulas]]
**Glossary**: [[quantitative-methods/glossary/m04-probability|M04 Terms]]

---

**Question 1**: Himari Fukumoto is selecting mutual funds from 10 available. She plans to select 4. How many different sets can she choose?

A. 210
B. 720
C. 5,040

> [!answer]- Answer
> **A.** Order doesn't matter → [[quantitative-methods/glossary/m04-probability#Combination|Combination]]: $C(10,4) = \frac{10!}{4! \times 6!} = 210$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m04-probability#Combination|Combination]] dùng khi chọn $k$ phần tử từ $n$ phần tử mà **thứ tự không quan trọng**. Ngược lại, Permutation dùng khi thứ tự quan trọng.
>
> **Tại sao A đúng:** Himari chọn 4 quỹ từ 10, không quan tâm thứ tự (tập hợp quỹ A, B, C, D giống với D, C, B, A). Áp dụng combination: $C(10,4) = \frac{10!}{4! \times 6!} = \frac{10 \times 9 \times 8 \times 7}{4 \times 3 \times 2 \times 1} = 210$.
>
> **Tại sao B sai:** 720 = $P(10,3)$ hoặc $6!$ — không phải combination 4 từ 10.
>
> **Tại sao C sai:** 5,040 = $P(7,4) = 7!/(7-4)!$ — đây là permutation, nghĩa là nếu thứ tự chọn quỹ quan trọng.
>
> **Mẹo nhớ:** "Combination" → không quan tâm thứ tự → chia thêm $k!$ để loại bỏ các hoán vị trùng nhau.

---

**Question 2**: $P(B) = 0.5$, $P(AB) = 0.1$. What is $P(A|B)$?

> [!answer]- Answer
> $P(A|B) = \frac{P(AB)}{P(B)} = \frac{0.1}{0.5} = 0.2$ or 20%

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m04-probability#Conditional Probability|Conditional probability]] $P(A|B)$ là xác suất xảy ra A **biết rằng** B đã xảy ra. Công thức: $P(A|B) = \frac{P(A \cap B)}{P(B)}$.
>
> **Tại sao đáp án đúng:** Thay số trực tiếp: $P(A|B) = \frac{0.1}{0.5} = 0.20$. Ý nghĩa: trong không gian xác suất đã thu hẹp về B (xác suất 0.5), tỷ lệ giao nhau A và B là 0.1 — tức 20% trong không gian đó.
>
> **Lưu ý quan trọng:** $P(A|B) \neq P(B|A)$. Đây là lỗi logic phổ biến. $P(B|A) = \frac{P(AB)}{P(A)}$ — cần biết $P(A)$ để tính (bài không cho). Nhầm lẫn này gọi là "base rate fallacy".

---

**Question 3**: $P(I) = 0.4$ (interest rate increase), $P(R) = 0.34$ (recession), $P(RI) = 0.28$. What is $P(R \text{ or } I)$?

> [!answer]- Answer
> Not mutually exclusive: $P(R \cup I) = P(R) + P(I) - P(RI) = 0.34 + 0.40 - 0.28 = 0.46$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m04-probability#Addition Rule|Addition rule]] (quy tắc cộng xác suất): $P(A \cup B) = P(A) + P(B) - P(A \cap B)$. Phải trừ đi phần giao nhau để tránh đếm hai lần. Nếu hai sự kiện **loại trừ nhau** (mutually exclusive) thì $P(A \cap B) = 0$ và công thức đơn giản thành $P(A) + P(B)$.
>
> **Tại sao đáp án đúng:** Suy thoái và tăng lãi suất có thể xảy ra đồng thời → không loại trừ nhau → phải áp dụng công thức đầy đủ. $P(R \cup I) = 0.34 + 0.40 - 0.28 = 0.46$.
>
> **Bẫy thường gặp:** Nếu cộng thẳng $0.34 + 0.40 = 0.74$ mà không trừ phần giao, kết quả vượt quá xác suất thực vì trường hợp "vừa suy thoái vừa tăng lãi suất" bị tính hai lần.

---

**Question 4**: A random variable $X = \{5, 10\}$ with $P(5) = 40\%$, $P(10) = 60\%$. Calculate $E(X)$, $\sigma^2(X)$, $\sigma(X)$.

> [!answer]- Answer
> $E(X) = 0.4 \times 5 + 0.6 \times 10 = 8$
> $\sigma^2 = 0.4(5-8)^2 + 0.6(10-8)^2 = 0.4(9) + 0.6(4) = 6$
> $\sigma = \sqrt{6} \approx 2.45$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m04-probability#Expected Value|Expected value]] $E(X)$ là trung bình có xác suất làm trọng số: $E(X) = \sum p_i x_i$. [[quantitative-methods/glossary/m04-probability#Variance|Variance]] $\sigma^2$ đo mức độ phân tán quanh kỳ vọng: $\sigma^2 = \sum p_i (x_i - E(X))^2$.
>
> **Tại sao đáp án đúng:**
> - $E(X) = 0.4(5) + 0.6(10) = 2 + 6 = 8$ — kỳ vọng nghiêng về 10 vì xác suất 60% cao hơn.
> - $\sigma^2 = 0.4(5-8)^2 + 0.6(10-8)^2 = 0.4(9) + 0.6(4) = 3.6 + 2.4 = 6$
> - $\sigma = \sqrt{6} \approx 2.45$
>
> **Lưu ý về variance:** Phương sai luôn **không âm** vì dùng bình phương độ lệch. Standard deviation $\sigma$ có cùng đơn vị với $X$, trong khi variance có đơn vị bình phương — vì vậy standard deviation dễ giải thích hơn trong thực tế.
