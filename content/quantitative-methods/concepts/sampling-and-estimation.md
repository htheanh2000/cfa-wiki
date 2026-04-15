---
title: "Sampling and Estimation"
type: concept
subject: quantitative-methods
module: M07
created: 2026-04-09
updated: 2026-04-09
tags: [sampling, CLT, confidence-interval, estimation, bias, standard-error]
---

# Sampling and Estimation

## Tổng quan

Thống kê suy luận cho phép các nhà phân tích rút ra kết luận về tổng thể từ một mẫu. Trong phân tích đầu tư, việc quan sát toàn bộ tổng thể (ví dụ: tất cả cổ phiếu, toàn bộ lợi nhuận quỹ từ trước đến nay) hầu như không khả thi. Các phương pháp lấy mẫu xác định cách chọn một tập con đại diện; lý thuyết ước lượng cung cấp công cụ để suy luận về [[quantitative-methods/glossary/m07-estimation-and-inference#Parameter|tham số]] tổng thể từ [[quantitative-methods/glossary/m07-estimation-and-inference#Statistic|thống kê]] mẫu. Hiểu rõ cả hai yếu tố này là điều kiện cần thiết để đánh giá độ tin cậy của các nghiên cứu đầu tư.

## Các Phương Pháp Lấy Mẫu

Bốn phương pháp lấy mẫu xác suất đảm bảo mọi thành viên trong tổng thể đều có xác suất được chọn đã biết:

| Phương pháp | Mô tả | Ứng dụng tốt nhất |
|-------------|-------|-------------------|
| **[[quantitative-methods/glossary/m07-estimation-and-inference#Simple Random Sampling|Simple random]]** | Mỗi thành viên có xác suất được chọn như nhau | Tổng thể đồng nhất |
| **[[quantitative-methods/glossary/m07-estimation-and-inference#Systematic Sampling|Systematic]]** | Chọn mỗi phần tử thứ $k$ sau một điểm bắt đầu ngẫu nhiên | Tổng thể lớn, có thứ tự |
| **[[quantitative-methods/glossary/m07-estimation-and-inference#Stratified Random Sampling|Stratified random]]** | Chia thành các nhóm con; lấy mẫu từ mỗi nhóm | Đảm bảo đại diện cho từng nhóm con (ví dụ: xây dựng chỉ số trái phiếu) |
| **[[quantitative-methods/glossary/m07-estimation-and-inference#Cluster Sampling|Cluster]]** | Chia thành các cụm; lấy mẫu toàn bộ cụm | Tổng thể phân tán theo địa lý |

Các phương pháp phi xác suất ([[quantitative-methods/glossary/m07-estimation-and-inference#Convenience Sampling|convenience]], [[quantitative-methods/glossary/m07-estimation-and-inference#Judgmental Sampling|judgmental]]) nhanh hơn và ít tốn kém hơn nhưng dễ dẫn đến selection bias và hạn chế khả năng tổng quát hóa.

## Central Limit Theorem

**[[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem (CLT)|Central Limit Theorem (CLT)]]** là kết quả quan trọng nhất trong thống kê suy luận. Định lý này phát biểu rằng với bất kỳ tổng thể nào có giá trị kỳ vọng $\mu$ và phương sai hữu hạn $\sigma^2$, phân phối lấy mẫu của giá trị trung bình mẫu $\bar{X}$ tiệm cận phân phối chuẩn khi $n$ tăng lên:

$$\bar{X} \xrightarrow{d} N\!\left(\mu,\, \frac{\sigma^2}{n}\right) \quad \text{as } n \to \infty$$

Trong thực tế, xấp xỉ này đủ tốt khi $n \geq 30$. CLT có nghĩa là ngay cả khi các quan sát lợi nhuận riêng lẻ không phân phối chuẩn (thường có [[quantitative-methods/glossary/m03-statistical-measures#Skewness|skewness]] và [[quantitative-methods/glossary/m03-statistical-measures#Leptokurtic|fat tails]]), giá trị trung bình mẫu vẫn sẽ xấp xỉ phân phối chuẩn với cỡ mẫu đủ lớn. Đây là cơ sở để áp dụng confidence interval dựa trên phân phối chuẩn và các kiểm định t.

**[[quantitative-methods/glossary/m07-estimation-and-inference#Standard Error|Standard error]]** của giá trị trung bình mẫu — độ lệch chuẩn của phân phối lấy mẫu — được tính như sau:

$$\sigma_{\bar{X}} = \frac{\sigma}{\sqrt{n}} \qquad \text{or estimated as} \qquad s_{\bar{X}} = \frac{s}{\sqrt{n}}$$

Cỡ mẫu lớn hơn cho standard error nhỏ hơn, nghĩa là ước lượng chính xác hơn.

## Point Estimates và Confidence Intervals

**[[quantitative-methods/glossary/m07-estimation-and-inference#Point Estimate|Point estimate]]** cho một giá trị ước lượng tốt nhất duy nhất cho một tham số (ví dụ: $\bar{X} = 8.3\%$ là ước lượng lợi nhuận trung bình hàng năm). **[[quantitative-methods/glossary/m07-estimation-and-inference#Confidence Interval|Confidence interval]]** bổ sung thêm thước đo độ chính xác:

$$\bar{X} \pm z_{\alpha/2} \frac{\sigma}{\sqrt{n}} \quad \text{(} \sigma \text{ đã biết)} \qquad \bar{X} \pm t_{\alpha/2,\, n-1} \frac{s}{\sqrt{n}} \quad \text{(} \sigma \text{ chưa biết)}$$

[[quantitative-methods/glossary/m07-estimation-and-inference#Student's t-Distribution|t-distribution]] được dùng trong thực tế vì độ lệch chuẩn tổng thể $\sigma$ hầu như không bao giờ được biết trước. Khi $n$ tăng, giá trị tới hạn t tiệm cận giá trị tới hạn z.

**Lưu ý về diễn giải**: Confidence interval 95% không có nghĩa là "có 95% xác suất giá trị trung bình thực sự nằm trong khoảng này." Đúng hơn, nếu thực hiện quy trình này nhiều lần, 95% số khoảng tin cậy được xây dựng sẽ chứa giá trị trung bình thực.

## Các Tính Chất Mong Muốn của Estimator

Ba tính chất xác định một estimator chất lượng cao:
- **[[quantitative-methods/glossary/m07-estimation-and-inference#Unbiased Estimator|Unbiased]]**: $E(\hat{\theta}) = \theta$ — không có xu hướng ước lượng cao hay thấp một cách hệ thống. (Ví dụ: $\bar{X}$ là unbiased cho $\mu$; $s^2$ với mẫu số $n-1$ là unbiased cho $\sigma^2$.)
- **[[quantitative-methods/glossary/m07-estimation-and-inference#Efficient Estimator|Efficient]]**: Trong số các unbiased estimator, có phương sai nhỏ nhất — độ chính xác tối đa.
- **[[quantitative-methods/glossary/m07-estimation-and-inference#Consistent Estimator|Consistent]]**: Hội tụ về giá trị thực khi cỡ mẫu tăng lên. Đây là yêu cầu tối thiểu cho bất kỳ estimator nào có giá trị thực tiễn.

## Các Loại Bias Trong Nghiên Cứu Đầu Tư

Một số bias có hệ thống có thể làm mất tính hợp lệ của các suy luận dựa trên mẫu trong tài chính:

- **[[quantitative-methods/glossary/m07-estimation-and-inference#Data Snooping Bias|Data snooping bias]]**: Kiểm tra nhiều chiến lược trên cùng một bộ dữ liệu lịch sử cho đến khi có kết quả "hoạt động được" — kết quả đó có thể chỉ là ngẫu nhiên.
- **[[quantitative-methods/glossary/m07-estimation-and-inference#Survivorship Bias|Survivorship bias]]**: Loại trừ các quỹ hay công ty đã thất bại khỏi mẫu khiến hiệu suất lịch sử bị đánh giá cao hơn thực tế.
- **[[quantitative-methods/glossary/m07-estimation-and-inference#Look-Ahead Bias|Look-ahead bias]]**: Sử dụng thông tin chưa có tại thời điểm ra quyết định làm tăng lợi nhuận backtested một cách giả tạo.
- **[[quantitative-methods/glossary/m07-estimation-and-inference#Time Period Bias|Time-period bias]]**: Sử dụng một cửa sổ lịch sử không đại diện — một chiến lược có thể trông tốt chỉ trong giai đoạn thị trường tăng trưởng.
- **[[quantitative-methods/glossary/m07-estimation-and-inference#Backfill Bias|Backfill bias]]**: Thêm lịch sử hiệu suất trước khi gia nhập của một quản lý quỹ vào cơ sở dữ liệu chỉ sau khi họ tham gia, tạo ra selection bias nghiêng về hiệu suất tốt trong giai đoạn đầu.

Mỗi loại bias có xu hướng làm cho các chiến lược đầu tư trông có vẻ sinh lời hơn so với thực tế, khiến chúng đặc biệt nguy hiểm khi đánh giá các sản phẩm đầu tư định lượng.

## Các Module Liên Quan

- [[quantitative-methods/modules/m07-estimation-and-inference/index|M07 — Estimation and Inference]] — nội dung chính
- [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — Hypothesis Testing]] — sử dụng standard errors và confidence intervals từ M07