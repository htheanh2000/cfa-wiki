---
title: "Probability"
type: concept
subject: quantitative-methods
module: M04
created: 2026-04-09
updated: 2026-04-09
tags: [probability, bayes, conditional, expected-value, counting]
---

# Probability

## Overview

Probability là khung toán học để định lượng sự không chắc chắn. Trong tài chính, probability cho phép các nhà phân tích mô hình hóa các kết quả tương lai không chắc chắn — lợi suất tài sản, sự kiện vỡ nợ, kịch bản kinh tế — và đưa ra quyết định có kỷ luật trong điều kiện bất định. Chương trình CFA đề cập đến ba cách tiếp cận để gán probability, các quy tắc probability cơ bản, cùng các công cụ thực tiễn để cập nhật niềm tin và đếm kết quả.

## Types of Probability

Có ba cách tiếp cận để gán probability. **[[quantitative-methods/glossary/m04-probability#A Priori Probability|A priori probability]]** được suy ra từ phân tích logic về các kết quả có khả năng bằng nhau (ví dụ: P(mặt ngửa) = 1/2 với đồng xu cân bằng). **[[quantitative-methods/glossary/m04-probability#Empirical Probability|Empirical probability]]** được ước tính từ tần suất lịch sử quan sát được (ví dụ: cổ phiếu tăng 55% số ngày trong thập kỷ qua). **[[quantitative-methods/glossary/m04-probability#Subjective Probability|Subjective probability]]** phản ánh quan điểm cá nhân có cơ sở của một người, không phải từ quan sát có thể lặp lại (ví dụ: nhà phân tích gán 70% xác suất rằng một thương vụ sáp nhập sẽ hoàn tất). Cả ba đều phải tuân theo cùng một hệ tiên đề: probability nằm trong khoảng từ 0 đến 1, và tổng probability của tất cả các sự kiện [[quantitative-methods/glossary/m04-probability#Mutually Exclusive Events|mutually exclusive]] và [[quantitative-methods/glossary/m04-probability#Exhaustive Events|exhaustive]] bằng 1.

## Core Probability Rules

**[[quantitative-methods/glossary/m04-probability#Addition Rule|Addition rule]]** tính probability để ít nhất một trong hai sự kiện xảy ra:

$$P(A \text{ or } B) = P(A) + P(B) - P(AB)$$

Với các sự kiện [[quantitative-methods/glossary/m04-probability#Mutually Exclusive Events|mutually exclusive]], $P(AB) = 0$ nên công thức rút gọn thành $P(A) + P(B)$.

**[[quantitative-methods/glossary/m04-probability#Multiplication Rule|Multiplication rule]]** cho joint probability của hai sự kiện:

$$P(AB) = P(A|B) \times P(B)$$

Với các sự kiện [[quantitative-methods/glossary/m04-probability#Independent Events|independent]], $P(A|B) = P(A)$, nên $P(AB) = P(A) \times P(B)$.

**[[quantitative-methods/glossary/m04-probability#Total Probability Rule|Total probability rule]]** phân tách unconditional probability thành bình quân gia quyền trên các kịch bản mutually exclusive và exhaustive $S_1, \ldots, S_n$:

$$P(A) = \sum_{i=1}^{n} P(A|S_i) \times P(S_i)$$

Đây là nền tảng của phân tích kịch bản trong quản lý đầu tư.

## Conditional Probability và Bayes' Formula

[[quantitative-methods/glossary/m04-probability#Conditional Probability|Conditional probability]] là probability của sự kiện $A$ khi biết sự kiện $B$ đã xảy ra:

$$P(A|B) = \frac{P(AB)}{P(B)}$$

**[[quantitative-methods/glossary/m04-probability#Bayes' Formula|Bayes' formula]]** là công cụ cốt lõi để cập nhật niềm tin prior khi có thông tin mới:

$$P(A|B) = \frac{P(B|A) \times P(A)}{P(B)}$$

Trong phân tích đầu tư, Bayes' formula hình thức hóa quá trình kết hợp bằng chứng mới: $P(A)$ là prior probability (niềm tin trước khi có dữ liệu mới), $P(B|A)$ là likelihood (mức độ có thể xảy ra của dữ liệu mới nếu $A$ đúng), và $P(A|B)$ là posterior probability (niềm tin được cập nhật sau khi quan sát $B$). Cấu trúc này là nền tảng cho Bayesian inference được sử dụng trong quản lý danh mục định lượng.

## Expected Value và Variance

**[[quantitative-methods/glossary/m04-probability#Expected Value|Expected value]]** của một biến ngẫu nhiên rời rạc là bình quân gia quyền theo probability của tất cả các kết quả có thể xảy ra:

$$E(X) = \sum_{i=1}^{n} P(X_i) \cdot X_i$$

**[[quantitative-methods/glossary/m04-probability#Variance of Random Variable|Variance]]** đo lường mức độ phân tán của các kết quả xung quanh expected value:

$$\text{Var}(X) = E\left[(X - E(X))^2\right] = \sum_{i=1}^{n} P(X_i)\left[X_i - E(X)\right]^2$$

Đây là nền tảng để định giá tài sản rủi ro, tính toán rủi ro danh mục ([[quantitative-methods/concepts/portfolio-risk|Portfolio Risk]]), và đánh giá các kết quả đầu tư không chắc chắn.

## Counting Methods

Khi các kết quả có khả năng bằng nhau, probability thu về bài toán đếm. Ba công cụ đếm quan trọng là:

- **[[quantitative-methods/glossary/m04-probability#Factorial|Factorial]]**: $n! = n \times (n-1) \times \cdots \times 1$ — tổng số cách sắp xếp $n$ phần tử.
- **[[quantitative-methods/glossary/m04-probability#Permutation|Permutation]]**: $_nP_r = \frac{n!}{(n-r)!}$ — số cách sắp xếp $r$ phần tử từ $n$ phần tử khi thứ tự có ý nghĩa.
- **[[quantitative-methods/glossary/m04-probability#Combination|Combination]]**: $\binom{n}{r} = \frac{n!}{r!(n-r)!}$ — số cách chọn $r$ phần tử từ $n$ phần tử khi thứ tự không có ý nghĩa.

Combination được sử dụng trong công thức [[quantitative-methods/glossary/m05-portfolio-math#Binomial Distribution|binomial distribution]] và trong việc đếm số danh mục riêng biệt có thể được tạo thành từ một tập hợp chứng khoán cho trước.

## Source Modules

- [[quantitative-methods/modules/m04-probability/index|M04 — Probability Concepts]] — nội dung chính
- [[quantitative-methods/modules/m05-portfolio-math/index|M05 — Portfolio Mathematics]] — ứng dụng vào expected return và variance của danh mục