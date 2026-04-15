---
title: "Hypothesis Testing"
type: concept
subject: quantitative-methods
module: M08
created: 2026-04-09
updated: 2026-04-09
tags: [hypothesis-testing, type-i-error, type-ii-error, p-value, parametric, nonparametric]
---

# Hypothesis Testing

## Tổng quan

Hypothesis testing là quy trình thống kê chính thức dùng dữ liệu mẫu để đánh giá một nhận định về tham số tổng thể. Đây là một trong những công cụ được sử dụng rộng rãi nhất trong tài chính thực nghiệm — được áp dụng để kiểm tra xem excess return có có ý nghĩa thống kê hay không, liệu một nhân tố có khả năng dự báo hay không, hai danh mục đầu tư có mean khác nhau không, và mô hình hồi quy có giải thích được sự biến động của return hay không. Chương trình CFA nhấn mạnh một quy trình gồm sáu bước có tính kỷ luật cao.

## Quy trình Sáu Bước

**Bước 1 — Phát biểu các giả thuyết.** Xác định [[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|null hypothesis]] $H_0$ (hiện trạng, được giả định là đúng) và [[quantitative-methods/glossary/m08-hypothesis-testing#Alternative Hypothesis|alternative hypothesis]] $H_a$ (điều ta tìm kiếm bằng chứng để chứng minh). Lựa chọn giữa [[quantitative-methods/glossary/m08-hypothesis-testing#Two-Tailed Test|two-tailed test]] ($H_a: \mu \neq \mu_0$) hoặc [[quantitative-methods/glossary/m08-hypothesis-testing#One-Tailed Test|one-tailed test]] ($H_a: \mu > \mu_0$ hoặc $H_a: \mu < \mu_0$) dựa trên lý luận kinh tế.

**Bước 2 — Chọn mức ý nghĩa $\alpha$.** [[quantitative-methods/glossary/m08-hypothesis-testing#Level of Significance|Level of significance]] xác định xác suất mắc phải [[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I error]] (false positive). Các lựa chọn phổ biến: $\alpha = 0.10$, $0.05$, $0.01$. Giá trị này được chọn trước khi xem dữ liệu.

**Bước 3 — Xác định test statistic và phân phối của nó.** Lựa chọn giữa [[quantitative-methods/glossary/m08-hypothesis-testing#z-Test|z-test]], [[quantitative-methods/glossary/m08-hypothesis-testing#t-Test|t-test]], [[quantitative-methods/glossary/m08-hypothesis-testing#Chi-Square Test|chi-square test]], hoặc [[quantitative-methods/glossary/m08-hypothesis-testing#F-Test|F-test]] dựa trên tham số đang được kiểm định, phương sai tổng thể có được biết hay không, và cỡ mẫu.

**Bước 4 — Phát biểu quy tắc quyết định.** Xác định [[quantitative-methods/glossary/m08-hypothesis-testing#Critical Value|critical value(s)]] định nghĩa [[quantitative-methods/glossary/m08-hypothesis-testing#Rejection Region|rejection region]]. Ví dụ: bác bỏ $H_0$ nếu $|t| > 1.96$ với two-tailed test tại $\alpha = 5\%$ và cỡ mẫu lớn.

**Bước 5 — Tính toán test statistic.**

$$\text{Test statistic} = \frac{\text{Sample statistic} - \text{Hypothesized value}}{\text{Standard error of statistic}}$$

**Bước 6 — Đưa ra quyết định thống kê và kết luận kinh tế.** So sánh test statistic với critical value (hoặc so sánh [[quantitative-methods/glossary/m08-hypothesis-testing#p-Value|p-value]] với $\alpha$). "Bác bỏ $H_0$" hoặc "không bác bỏ $H_0$." Sau đó diễn giải kết quả trong bối cảnh tài chính cụ thể.

## Type I và Type II Errors

Hai loại sai lầm có thể xảy ra trong hypothesis testing có sự đánh đổi vốn có:

| Quyết định | $H_0$ Đúng | $H_0$ Sai |
|----------|-----------|------------|
| Không bác bỏ $H_0$ | Đúng ($1-\alpha$) | **Type II Error** ($\beta$) |
| Bác bỏ $H_0$ | **Type I Error** ($\alpha$) | Đúng (Power = $1-\beta$) |

- **[[quantitative-methods/glossary/m08-hypothesis-testing#Type I Error|Type I Error]]** (false positive): Bác bỏ $H_0$ khi $H_0$ đúng. Xác suất = $\alpha$.
- **[[quantitative-methods/glossary/m08-hypothesis-testing#Type II Error|Type II Error]]** (false negative): Không bác bỏ $H_0$ khi $H_0$ sai. Xác suất = $\beta$.
- **[[quantitative-methods/glossary/m08-hypothesis-testing#Power of a Test|Power]]** = $1 - \beta$. Tăng cỡ mẫu sẽ tăng power trong khi giữ nguyên $\alpha$.

Giảm $\alpha$ (ví dụ từ 5% xuống 1%) làm giảm Type I error nhưng tăng $\beta$ (và giảm power), khiến việc phát hiện các hiệu ứng thực sự trở nên khó hơn. Sự đánh đổi phù hợp phụ thuộc vào chi phí tương đối của từng loại sai lầm.

## Ý nghĩa Thống kê vs. Ý nghĩa Kinh tế

Đây là một sự phân biệt quan trọng trong tài chính: **[[quantitative-methods/glossary/m08-hypothesis-testing#Statistical Significance|Statistical significance]]** có nghĩa là kết quả khó có khả năng xảy ra do ngẫu nhiên (p-value $< \alpha$), nhưng không hàm ý rằng kết quả đủ lớn để có ý nghĩa thực tiễn. **[[quantitative-methods/glossary/m08-hypothesis-testing#Economically Significant|Economic significance]]** đòi hỏi độ lớn của hiệu ứng phải đủ lớn để có lợi nhuận sau khi trừ chi phí giao dịch, thuế và điều chỉnh rủi ro.

Với các mẫu rất lớn, ngay cả những chênh lệch nhỏ không đáng kể (ví dụ: excess return 0.001%) cũng có thể có statistical significance. Ngược lại, các mẫu nhỏ có thể không phát hiện được những hiệu ứng lớn về mặt kinh tế. Luôn đánh giá cả hai chiều.

## Parametric vs. Nonparametric Tests

**[[quantitative-methods/glossary/m08-hypothesis-testing#Parametric Test|Parametric tests]]** — như t-test, F-test và z-test — giả định rằng dữ liệu xuất phát từ một họ phân phối đã biết (thường là phân phối chuẩn) và kiểm định giả thuyết về các tham số cụ thể. Chúng có power cao hơn nonparametric tests khi các giả định phân phối được thỏa mãn.

**[[quantitative-methods/glossary/m08-hypothesis-testing#Nonparametric Test|Nonparametric tests]]** không đưa ra giả định về phân phối. Sử dụng khi:
1. Dữ liệu được đo trên thang thứ tự (ranked scale).
2. Tổng thể không có phân phối chuẩn và cỡ mẫu nhỏ.
3. Giả thuyết liên quan đến tính độc lập thay vì một tham số (ví dụ: [[quantitative-methods/glossary/m09-parametric-tests#Chi-Square Test of Independence|chi-square test of independence]]).
4. Dữ liệu chứa các outliers đáng kể có thể làm méo lệch parametric tests.

Nonparametric test quan trọng cần biết: **[[quantitative-methods/glossary/m09-parametric-tests#Spearman Rank Correlation|Spearman rank correlation]]** — kiểm định xem hai biến có quan hệ đơn điệu hay không, sử dụng thứ hạng của các quan sát thay vì giá trị thực của chúng.

## Các Module Nguồn

- [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — Hypothesis Testing]] — nội dung chính về quy trình sáu bước, các loại sai lầm, lựa chọn kiểm định
- [[quantitative-methods/modules/m09-parametric-tests/index|M09 — Parametric and Nonparametric Tests]] — Spearman rank correlation, chi-square test of independence
- [[quantitative-methods/modules/m07-estimation-and-inference/index|M07 — Estimation and Inference]] — confidence intervals như một phương pháp thay thế cho hypothesis testing