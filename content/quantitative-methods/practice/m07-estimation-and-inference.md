---
title: "Practice: M07 — Estimation and Inference"
type: practice
subject: quantitative-methods
module: M07
created: 2026-04-09
updated: 2026-04-09
tags: [practice, sampling, clt, confidence-interval, bias]
---

# Practice: M07 — Estimation and Inference

**Module**: [[quantitative-methods/modules/m07-estimation-and-inference/index|M07]]
**Glossary**: [[quantitative-methods/glossary/m07-estimation-and-inference|M07 Terms]]

---

## Topic 1: Sampling Methods, CLT, and Standard Error

**Question 1**: A population has a non-normal distribution with mean and variance. The [[quantitative-methods/glossary/m07-estimation-and-inference#Sampling Distribution|sampling distribution]] of the sample mean computed from samples of large size from that population will have:

A. The same distribution as the population distribution
B. Its mean approximately equal to the population mean
C. Its variance approximately equal to the population variance

> [!answer]- Answer
> **B.** By the [[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem|Central Limit Theorem]], for large samples ($n \geq 30$), the sampling distribution of $\bar{X}$ has mean $= \mu$ (population mean) and variance $= \sigma^2/n$ (NOT equal to population variance). The distribution approaches normal regardless of the population shape.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem|Central Limit Theorem (CLT)]] — Định lý Giới hạn Trung tâm — phát biểu rằng: khi cỡ mẫu đủ lớn ($n \geq 30$), phân phối của trung bình mẫu $\bar{X}$ sẽ xấp xỉ phân phối chuẩn, **bất kể** phân phối của tổng thể ban đầu là gì. Trung bình của sampling distribution bằng $\mu$, còn phương sai bằng $\sigma^2/n$ (nhỏ hơn phương sai tổng thể).
>
> **Tại sao B đúng:** CLT đảm bảo rằng $E(\bar{X}) = \mu$ — trung bình của sampling distribution luôn bằng trung bình tổng thể. Đây là tính chất unbiasedness (không lệch) của sample mean.
>
> **Tại sao A sai:** CLT nói rằng sampling distribution tiệm cận phân phối chuẩn khi $n$ lớn, dù tổng thể có phân phối bất kỳ. Vì vậy, sampling distribution **không** giống phân phối tổng thể.
>
> **Tại sao C sai:** Phương sai của sampling distribution là $\sigma^2/n$, **nhỏ hơn** phương sai tổng thể $\sigma^2$. Cỡ mẫu càng lớn, phương sai của $\bar{X}$ càng nhỏ — đây là lý do tại sao mẫu lớn cho ước lượng chính xác hơn.

---

**Question 2**: When sampling from a population, the most appropriate sample size:

A. Minimizes the sampling error and the standard deviation of the sample statistic around its population value
B. Is at least 30
C. Involves a trade-off between the cost of increasing the sample size and the value of increasing the precision of the estimates

> [!answer]- Answer
> **C.** Larger samples are more precise but cost more. The appropriate size balances precision vs cost. While $n \geq 30$ is a CLT guideline (B), it's not always the "most appropriate" — it depends on context.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Standard Error|Standard error]] giảm khi cỡ mẫu tăng ($SE = \sigma/\sqrt{n}$), nhưng chi phí thu thập dữ liệu cũng tăng theo. Cỡ mẫu "tốt nhất" không phải lúc nào cũng là lớn nhất — đó là sự cân bằng giữa **độ chính xác** (precision) và **chi phí** (cost).
>
> **Tại sao C đúng:** Câu hỏi hỏi về cỡ mẫu "phù hợp nhất" — đây là quyết định thực tế đòi hỏi cân nhắc giữa lợi ích của độ chính xác cao hơn và chi phí tăng thêm khi thu thập thêm quan sát. Đây là nguyên tắc kinh tế cơ bản trong thiết kế nghiên cứu.
>
> **Tại sao A sai:** Không thể "tối thiểu hóa" sampling error mà không có ràng buộc — muốn minimize hoàn toàn thì cần lấy toàn bộ tổng thể (census), điều này không thực tế.
>
> **Tại sao B sai:** $n \geq 30$ là quy tắc ngón tay cái cho CLT, không phải định nghĩa cỡ mẫu "phù hợp nhất". Nhiều nghiên cứu cần cỡ mẫu lớn hơn nhiều; một số trường hợp đặc biệt có thể ổn với $n < 30$ nếu phân phối đã biết là chuẩn.

---

**Question 3**: A sample of 30 monthly returns has mean 2% and sample standard deviation 20%. Calculate the 95% [[quantitative-methods/glossary/m07-estimation-and-inference#Confidence Interval|confidence interval]] for the population mean.

> [!answer]- Answer
> Population $\sigma$ unknown → use t-statistic
> $s_{\bar{X}} = \frac{s}{\sqrt{n}} = \frac{20\%}{\sqrt{30}} = 3.65\%$
> $df = 29$, $t_{0.025}^{29} = 2.045$
> CI: $2\% \pm 2.045 \times 3.65\% = 2\% \pm 7.46\%$
> → **95% CI: −5.46% to 9.46%**

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Confidence Interval|Confidence interval (CI)]] cho trung bình tổng thể được xây dựng theo công thức: $\bar{X} \pm t_{\alpha/2} \times s_{\bar{X}}$, trong đó $s_{\bar{X}} = s/\sqrt{n}$ là [[quantitative-methods/glossary/m07-estimation-and-inference#Standard Error|standard error of the mean]]. Dùng **t-distribution** khi không biết $\sigma$ tổng thể (thực tế hầu như luôn như vậy), với $df = n - 1$.
>
> **Cách tính chi tiết:**
> - Vì $\sigma$ tổng thể **không biết**, dùng t-statistic thay vì z-statistic
> - Standard error: $s_{\bar{X}} = 20\%/\sqrt{30} = 3.65\%$
> - Degrees of freedom: $df = 30 - 1 = 29$
> - $t_{0.025, 29} = 2.045$ (tra bảng t với 5% hai đuôi, df = 29)
> - Khoảng: $2\% \pm 2.045 \times 3.65\% = 2\% \pm 7.46\%$
> - Kết quả: **−5.46% đến 9.46%**
>
> **Lưu ý quan trọng:** Khoảng rộng (±7.46%) phản ánh cỡ mẫu nhỏ (n=30) và độ biến động cao (s=20%). Nếu muốn CI hẹp hơn, cần tăng cỡ mẫu.

---

## Topic 2: Confidence Intervals

**Question 4**: Petra Munzi wants to build a 95% CI for population mean return. Population cross-sectional $\sigma = 4\%$. She wants the CI to have a total width of 1%.

A. How large a sample does she need?
B. At $10 per observation with $1,000 budget, can she build this CI?

> [!answer]- Answer
> A. Total width = 1% → half-width = 0.5%
> $0.5\% = z_{0.025} \times \frac{\sigma}{\sqrt{n}} = 1.96 \times \frac{4\%}{\sqrt{n}}$
> $\sqrt{n} = \frac{1.96 \times 4}{0.5} = 15.68$
> $n = 245.86$ → need **$n = 246$** observations
>
> B. Budget: $1,000 / $10 = 100 observations. **No**, she cannot — needs 246 but can only afford 100.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Khi biết $\sigma$ tổng thể, dùng z-statistic để tính CI. Độ rộng của CI phụ thuộc vào: (1) mức tin cậy (z-value), (2) độ lệch chuẩn tổng thể ($\sigma$), và (3) cỡ mẫu ($n$). Để xác định $n$ cần thiết: giải phương trình từ half-width mong muốn.
>
> **Tại sao dùng z thay vì t ở đây:** Vì $\sigma$ tổng thể **đã biết** ($\sigma = 4\%$), nên dùng z-distribution. $z_{0.025} = 1.96$ cho mức tin cậy 95%.
>
> **Logic tính cỡ mẫu (phần A):**
> - Total width = 1% → half-width = 0.5%
> - Half-width = $z \times \sigma/\sqrt{n}$ → giải ra $n$: $n = (z \times \sigma / \text{half-width})^2 = (1.96 \times 4 / 0.5)^2 = 15.68^2 = 245.86$
> - Làm tròn **lên** (không xuống) vì cần đủ chính xác: $n = 246$
>
> **Phần B — Ràng buộc ngân sách:** $1,000 / $10 = 100 quan sát — chỉ đủ 100 nhưng cần 246. Petra **không thể** đạt được CI có width 1% với ngân sách này.

---

## Topic 3: Resampling

**Question 5**: Compared with [[quantitative-methods/glossary/m07-estimation-and-inference#Bootstrap|bootstrap]] resampling, [[quantitative-methods/glossary/m07-estimation-and-inference#Jackknife|jackknife]] resampling:

A. Is done with replacement
B. Usually requires that the number of repetitions is equal to the sample size
C. Produces dissimilar results for every run because resamples are randomly drawn

> [!answer]- Answer
> **B.** Jackknife leaves out one observation at a time, so for a sample of $n$, there are exactly $n$ jackknife samples. Bootstrap draws **with** replacement (A describes bootstrap, not jackknife). Jackknife produces the **same** results every run because it's deterministic (C is wrong).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Jackknife|Jackknife]] và [[quantitative-methods/glossary/m07-estimation-and-inference#Bootstrap|Bootstrap]] đều là kỹ thuật resampling để ước lượng sampling distribution khi không có giả định về phân phối tổng thể. Điểm khác biệt chính:
> - **Jackknife**: loại bỏ **1 quan sát** mỗi lần → tạo ra đúng $n$ mẫu, kết quả **deterministic** (không ngẫu nhiên)
> - **Bootstrap**: lấy mẫu **có hoàn lại** (with replacement) với cỡ $n$ → kết quả **ngẫu nhiên** (khác nhau mỗi lần chạy)
>
> **Tại sao B đúng:** Jackknife tạo ra đúng $n$ sub-samples (mỗi sub-sample bỏ đi 1 quan sát khác nhau), nên số lần lặp luôn bằng $n$.
>
> **Tại sao A sai:** Lấy mẫu **có hoàn lại** (with replacement) là đặc điểm của **bootstrap**, không phải jackknife. Jackknife lấy mẫu **không hoàn lại** theo cách hệ thống.
>
> **Tại sao C sai:** Jackknife hoàn toàn **deterministic** — không có yếu tố ngẫu nhiên nào. Mỗi lần chạy trên cùng dataset sẽ cho kết quả giống hệt nhau. Chính bootstrap mới cho kết quả khác nhau mỗi lần vì yếu tố ngẫu nhiên trong sampling.

---

## Topic 4: Sampling Biases

**Question 6**: A report on long-term stock returns focused exclusively on all currently publicly traded firms in an industry is **most likely** susceptible to:

A. [[quantitative-methods/glossary/m07-estimation-and-inference#Look-Ahead Bias|Look-ahead bias]]
B. [[quantitative-methods/glossary/m07-estimation-and-inference#Survivorship Bias|Survivorship bias]]
C. Intergenerational data mining

> [!answer]- Answer
> **B. Survivorship bias.** Using only currently listed stocks excludes firms that failed, merged, or delisted. This overstates historical returns because poor performers are excluded.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m07-estimation-and-inference#Survivorship Bias|Survivorship bias]] xảy ra khi dataset chỉ bao gồm các đơn vị "sống sót" (còn tồn tại đến hiện tại) mà bỏ qua các đơn vị đã biến mất. Trong tài chính, điều này thường có nghĩa là chỉ nhìn vào các công ty đang còn niêm yết, bỏ qua các công ty đã phá sản, bị mua lại, hoặc hủy niêm yết.
>
> **Tại sao B đúng:** Báo cáo chỉ xem xét các công ty **hiện đang** giao dịch trên sàn. Các công ty hoạt động kém (và vì vậy đã bị xóa khỏi sàn) bị loại bỏ khỏi mẫu. Kết quả là lợi nhuận lịch sử bị **overstate** (ước lượng cao hơn thực tế) vì chỉ gồm các "người sống sót thành công".
>
> **Tại sao A sai:** [[quantitative-methods/glossary/m07-estimation-and-inference#Look-Ahead Bias|Look-ahead bias]] xảy ra khi dùng thông tin **chưa có tại thời điểm ra quyết định** — ví dụ: dùng báo cáo tài chính Q4 để backtest một chiến lược vào ngày 1/1 trong khi thực tế báo cáo chưa được công bố. Câu hỏi không đề cập đến vấn đề thời điểm thông tin.
>
> **Tại sao C sai:** Intergenerational data mining (hay data snooping) là việc khai thác dữ liệu quá mức để tìm patterns — không liên quan đến việc chọn mẫu chỉ từ công ty còn tồn tại.

---

**Question 7**: Which characteristic of an investment study **most likely** indicates time period bias?

A. The study is based on a short time-series
B. Information not available on the test date is used
C. A structural change occurred prior to the start of the study's time series

> [!answer]- Answer
> **A.** A short time series may give results specific to that period and not generalizable. B describes [[quantitative-methods/glossary/m07-estimation-and-inference#Look-Ahead Bias|look-ahead bias]]. C is not directly time period bias.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Time period bias** xảy ra khi kết quả nghiên cứu phụ thuộc đặc biệt vào khoảng thời gian được chọn — tức là kết quả có thể không tổng quát hóa được sang các giai đoạn khác. Có hai dạng: (1) time series **quá ngắn** → kết quả bị chi phối bởi điều kiện đặc thù của giai đoạn đó; (2) time series **quá dài** → có thể bao gồm các chế độ kinh tế khác nhau, làm mờ mối quan hệ thực sự.
>
> **Tại sao A đúng:** Time series ngắn có nguy cơ cao bị time period bias — kết quả có thể phản ánh điều kiện thị trường đặc thù của giai đoạn nghiên cứu (ví dụ: giai đoạn bong bóng dotcom, khủng hoảng 2008) và không thể tái lặp trong các giai đoạn khác.
>
> **Tại sao B sai:** Dùng thông tin chưa có tại thời điểm test là định nghĩa của [[quantitative-methods/glossary/m07-estimation-and-inference#Look-Ahead Bias|look-ahead bias]], không phải time period bias.
>
> **Tại sao C sai:** Structural change xảy ra **trước** khoảng thời gian nghiên cứu thực ra làm cho dữ liệu ổn định hơn trong giai đoạn đó (vì chế độ đã thay đổi rồi). Đây không phải dấu hiệu điển hình của time period bias. Time period bias thường liên quan đến độ dài và tính đại diện của khoảng thời gian được chọn.
