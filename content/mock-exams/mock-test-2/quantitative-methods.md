---
title: "Quantitative Methods"
type: practice
subject: quantitative-methods
source: "SAPP Mock Test 2"
created: 2026-04-14
updated: 2026-04-15
tags: [mock-test, mock-test-2, quantitative-methods, practice]
---

# Mock Test 2 — Topic 1: Quantitative Methods

**Kết quả**: 7/13 (54%)
**Nguồn**: SAPP CFA1 Revision Mock Test 2
**Liên kết**: [[quantitative-methods/index|Quantitative Methods]]

| Tổng câu | Đúng | Sai | Tỷ lệ |
|----------|------|-----|-------|
| 13 | 7 | 6 | 54% |

---

## Câu 33

**Question 33: Jon Pelker plans to retire in six years and will require \$950,000. Today, Pelker will deposit \$100,000 into an interest bearing account and will deposit an additional \$100,000 at the end of each of the next six years. What annual percentage return must Pelker earn to achieve his goal of \$950,000 for his retirement?**

(A) 8%.

(B) 10%.

(C) 18%.

> [!answer]- Đáp án
> **(B) 10%.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (B) 10%.
> Đây là bài toán tính lãi suất với một [[quantitative-methods/glossary/m02-time-value-of-money#Annuity Due|annuity due]] kết hợp với lump sum ban đầu: Pelker gửi \$100,000 ngay hôm nay (PV = –100,000) và thêm \$100,000 mỗi cuối năm trong 6 năm (PMT = –100,000, N = 6), mục tiêu là đạt FV = \$950,000.
>
> Nhập các giá trị này vào máy tính tài chính và tính CPT I/Y sẽ ra kết quả 10%.
> Lưu ý rằng cả PV và PMT đều âm (dòng tiền ra) trong khi FV dương (dòng tiền vào), điều này đảm bảo tính nhất quán về chiều dòng tiền khi sử dụng máy tính.

---

## Câu 36

**Question 36: A [[quantitative-methods/glossary/m07-estimation-and-inference#Sample|sample]] of 250 observations has the following properties: Mean 8.6 [[quantitative-methods/glossary/m03-statistical-measures#Standard Deviation|Standard deviation]] 4.9 Sample [[quantitative-methods/glossary/m03-statistical-measures#Kurtosis|kurtosis]] 3.0 [[quantitative-methods/glossary/m03-statistical-measures#Median|Median]] 8.3 [[quantitative-methods/glossary/m03-statistical-measures#Mode|Mode]] 8.1 This sample most likely has:**

(A) positive excess kurtosis.

(B) sample skewness greater than zero.

(C) at least one observation equal to 8.3.

> [!answer]- Đáp án
> **(B) sample skewness greater than zero.**
> 
> Bạn chọn: (C) at least one observation equal to 8.3.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (B) [[quantitative-methods/glossary/m07-estimation-and-inference#Sample|sample]] [[quantitative-methods/glossary/m03-statistical-measures#Skewness|skewness]] lớn hơn không.
> Dữ liệu cho thấy mean (8.6) > [[quantitative-methods/glossary/m03-statistical-measures#Median|median]] (8.3) > mode (8.1), đây là dấu hiệu điển hình của phân phối lệch phải (right-skewed hay positively skewed), nên sample skewness dương (> 0).
>
> Các đáp án khác sai vì: [[quantitative-methods/glossary/m03-statistical-measures#Excess [[quantitative-methods/glossary/m03-statistical-measures#Kurtosis|Kurtosis]]|excess kurtosis]] = sample kurtosis – 3 = 3.0 – 3.0 = 0, tức không phải [[quantitative-methods/glossary/m03-statistical-measures#Leptokurtic|leptokurtic]] hay [[quantitative-methods/glossary/m03-statistical-measures#Platykurtic|platykurtic]] mà là [[quantitative-methods/glossary/m03-statistical-measures#Mesokurtic|mesokurtic]] (tương đương phân phối chuẩn).
> Cần phân biệt rõ: sample kurtosis = 3 không có nghĩa là excess kurtosis = 3; trong tài chính, excess kurtosis mới là thước đo so sánh với phân phối chuẩn.

---

## Câu 42

**Quesiton 42: An investor observes that a 12-month United States Treasury bill has a quoted rate of 5.3%. If the [[quantitative-methods/glossary/m01-rates-and-returns#Inflation Premium|inflation premium]] is 4.1%, the:**

(A) real-risk free rate is approximately 1.2%.

(B) nominal risk-free rate is approximately 9.4%.

(C) real-risk free rate of 5.3% incorporates the inflation premium.

> [!answer]- Đáp án
> **(A) real-risk free rate is approximately 1.2%.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (A) [[quantitative-methods/glossary/m01-rates-and-returns#Real Risk-Free Rate|real risk-free rate]] xấp xỉ 1.2%.
> Lãi suất danh nghĩa (nominal rate) của U.S.
>
> Treasury bill bao gồm hai thành phần: real risk-free rate và [[quantitative-methods/glossary/m01-rates-and-returns#Inflation Premium|inflation premium]].
> Áp dụng xấp xỉ tuyến tính: real risk-free rate ≈ nominal rate − inflation premium = 5.3% − 4.1% = 1.2%.
>
> Lưu ý rằng đây là phép tính gần đúng; công thức chính xác theo Fisher equation là (1 + nominal) = (1 + real) × (1 + inflation), cho kết quả xấp xỉ tương đương ở mức lãi suất thấp.
> U.S.
>
> Treasury bill được coi là không có [[fixed-income/glossary/fi-m14#Default risk|default risk]] hay [[portfolio-management/glossary/pm-m06#Liquidity risk|liquidity risk]], nên toàn bộ spread trên real risk-free rate phản ánh inflation premium.

---

## Câu 46

**Question 46: A [[quantitative-methods/glossary/m10-simple-linear-regression#Simple Linear Regression|simple linear regression]] model assumes that the model's residuals:**

(A) are positively correlated.

(B) have a constant variance.

(C) are distributed lognormally.

> [!answer]- Đáp án
> **(B) have a constant variance.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (B) residuals có phương sai không đổi (constant [[portfolio-management/glossary/pm-m01#Variance|variance]]), hay còn gọi là [[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|homoskedasticity]].
> Các giả định cơ bản của [[quantitative-methods/glossary/m10-simple-linear-regression#Simple Linear Regression|simple linear regression]] bao gồm: (1) residuals có phương sai không đổi với mọi quan sát, (2) residuals không tương quan với nhau (no autocorrelation), và (3) residuals tuân theo phân phối chuẩn (normally distributed) với kỳ vọng bằng 0.
>
> Khi giả định phương sai không đổi bị vi phạm, hiện tượng này gọi là [[quantitative-methods/glossary/m10-simple-linear-regression#Heteroskedasticity|heteroskedasticity]], làm cho các kiểm định thống kê của mô hình mất độ tin cậy.

---

## Câu 48

**Question 48: A [[quantitative-methods/glossary/m04-probability#Probability Tree|probability tree]] shows that a company's expected earnings per share for the next period is \$2.75. If three of the four potential outcomes used to construct the tree show a 20% probability of \$2.00, a 25% probability of \$2.60, and a 30% probability of \$2.80, the remaining possible [[quantitative-methods/glossary/m04-probability#Outcome|outcome]] is:**

(A) \$3.28.

(B) \$3.36.

(C) \$3.44.

> [!answer]- Đáp án
> **(C) \$3.44.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (C) \$3.44.
> Tổng xác suất của tất cả các kết quả phải bằng 100%, nên xác suất còn lại là 100% − 20% − 25% − 30% = 25%.
>
> Gọi kết quả chưa biết là X, ta lập phương trình kỳ vọng: 0.20(2.00) + 0.25(2.60) + 0.30(2.80) + 0.25(X) = 2.75, tức là 0.40 + 0.65 + 0.84 + 0.25X = 2.75, suy ra 0.25X = 0.86, vậy X = \$3.44.
> Kết quả này hợp lý vì để kéo expected EPS lên \$2.75 khi ba kết quả kia đều thấp hơn, kết quả thứ tư cần phải đủ cao.

---

## Câu 60

**Question 60: If [[quantitative-methods/glossary/m07-estimation-and-inference#Simple Random Sampling|simple random sampling]] is used on a [[quantitative-methods/glossary/m07-estimation-and-inference#Population|population]] with 20 data points, the [[quantitative-methods/glossary/m04-probability#Probability|probability]] that any individual data point is selected first in a 10 data point [[quantitative-methods/glossary/m07-estimation-and-inference#Sample|sample]] is:**

(A) 0.05.

(B) 0.10.

(C) 0.50.

> [!answer]- Đáp án
> **(A) 0.05.**
> 
> Bạn chọn: (C) 0.50.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (A) 0.05.
> Lưu ý: Lời giải gốc có nhầm lẫn khi đề cập "50 data points" trong khi câu hỏi nêu rõ tổng thể có 20 điểm dữ liệu.
>
> Với [[quantitative-methods/glossary/m07-estimation-and-inference#Simple Random Sampling|simple random sampling]] (lấy mẫu ngẫu nhiên đơn giản), mỗi điểm dữ liệu trong tổng thể có xác suất bằng nhau để được chọn.
> Với tổng thể 20 điểm, xác suất để bất kỳ điểm nào được chọn đầu tiên là 1/20 = 0.05.
>
> Điểm quan trọng cần ghi nhớ là kích thước mẫu ([[quantitative-methods/glossary/m07-estimation-and-inference#Sample|sample]] size = 10) không ảnh hưởng đến xác suất được chọn đầu tiên — xác suất này chỉ phụ thuộc vào kích thước của tổng thể ([[quantitative-methods/glossary/m07-estimation-and-inference#Population|population]] size = 20).
> Đây là đặc tính cơ bản của simple random sampling: mỗi phần tử đều có cơ hội như nhau để được đưa vào mẫu.

---

## Câu 63

**Question 63: An analyst is evaluating [[quantitative-methods/glossary/m07-estimation-and-inference#Sample|sample]] [[quantitative-methods/glossary/m03-statistical-measures#Correlation|correlation]] coefficients to test the hypothesis that a population [[portfolio-management/glossary/pm-m01#Correlation coefficient|correlation coefficient]] is equal to zero. Which of the following independent actions will increase the likelihood that she will reject the hypothesis?**

(A) Increasing the sample size.

(B) Decreasing the sample correlation coefficient.

(C) Decreasing the level of significance from 10% to 5%.

> [!answer]- Đáp án
> **(A) Increasing the sample size.**
> 
> Bạn chọn: (C) Decreasing the level of significance from 10% to 5%.

> [!tip]- 📖 Giải thích chi tiết
> Tăng [[quantitative-methods/glossary/m07-estimation-and-inference#Sample|sample]] size (cỡ mẫu) làm tăng giá trị của [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]] (thống kê kiểm định) đồng thời làm giảm critical value (giá trị tới hạn), từ đó tăng khả năng bác bỏ [[quantitative-methods/glossary/m08-hypothesis-testing#Null Hypothesis|null hypothesis]] rằng [[quantitative-methods/glossary/m07-estimation-and-inference#Population|population]] [[portfolio-management/glossary/pm-m01#[[quantitative-methods/glossary/m03-statistical-measures#Correlation|Correlation]] coefficient|correlation coefficient]] bằng 0.
> Nói đơn giản hơn: mẫu càng lớn, bằng chứng càng mạnh, kiểm định càng có lực (statistical power) cao hơn.
>
> Ngược lại, giảm sample correlation coefficient sẽ làm giảm test statistic — ít bằng chứng hơn để bác bỏ H₀.
> Còn giảm [[quantitative-methods/glossary/m07-estimation-and-inference#Level of Significance|level of significance]] (mức ý nghĩa, ví dụ từ 5% xuống 1%) sẽ làm tăng critical value, khiến việc bác bỏ H₀ trở nên khó hơn chứ không dễ hơn.

---

## Câu 69

**Question 69: Which of the following statistics is used to test a hypothesis concerning the difference between the variances of two normally distributed populations?**

(A) Z-statistic.

(B) F-statistic.

(C) Chi-square statistic.

> [!answer]- Đáp án
> **(B) F-statistic.**
> 
> Bạn chọn: (A) Z-statistic.

> [!tip]- 📖 Giải thích chi tiết
> [[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-statistic]] (thống kê F) được sử dụng để kiểm định giả thuyết về sự bằng nhau giữa variances (phương sai) của hai tổng thể phân phối chuẩn.
> F-statistic được tính là tỷ số giữa hai [[quantitative-methods/glossary/m07-estimation-and-inference#Sample|sample]] variances: F = s₁²/s₂².
>
> Trong khi đó, z-statistic dùng để kiểm định về [[quantitative-methods/glossary/m07-estimation-and-inference#Population|population]] mean khi biết phương sai tổng thể (hoặc mẫu lớn), còn chi-square statistic dùng để kiểm định về [[portfolio-management/glossary/pm-m01#Variance|variance]] của một tổng thể đơn lẻ.
> Việc nhớ đúng loại [[quantitative-methods/glossary/m08-hypothesis-testing#Test Statistic|test statistic]] cho từng tình huống là kỹ năng căn bản trong phần Quantitative Methods của CFA.

---

## Câu 73

**Question 73: With [[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|bootstrap]] [[quantitative-methods/glossary/m06-simulation-methods#Resampling|resampling]], what happens to the sampled observations with every repeated draw?**

(A) They are removed and not used again.

(B) They are purposefully included in future samples.

(C) They are replaced so they may be redrawn in another sample.

> [!answer]- Đáp án
> **(C) They are replaced so they may be redrawn in another sample.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (C) Các quan sát được đưa trả lại để có thể được rút lại trong lần lấy mẫu khác.
> [[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|Bootstrap]] [[quantitative-methods/glossary/m06-simulation-methods#Resampling|resampling]] là kỹ thuật lấy mẫu có hoàn lại (sampling with replacement) từ bộ dữ liệu gốc, nghĩa là sau mỗi lần rút, quan sát đó được đặt lại vào tập dữ liệu và hoàn toàn có thể xuất hiện trong các mẫu tiếp theo.
> Điều này khác với lấy mẫu không hoàn lại (sampling without replacement), trong đó quan sát đã rút sẽ bị loại khỏi các lần rút sau.
>
> Phương pháp này cho phép ước tính phân phối của một thống kê mà không cần giả định về phân phối tổng thể.

---

## Câu 77

**Question 77: An ANOVA table shows an explained variation of 0.0135 and an unexplained variation of 0.0640. The sum of squares regression is:**

(A) 0.0135.

(B) 0.0640.

(C) 0.0775.

> [!answer]- Đáp án
> **(A) 0.0135.**
> 
> Bạn chọn: (C) 0.0775.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (A) 0.0135.
> Trong bảng ANOVA (Analysis of [[portfolio-management/glossary/pm-m01#Variance|Variance]]), sum of squares regression (SSR) chính là phần biến động của biến phụ thuộc được giải thích bởi biến độc lập, tức là explained variation = 0.0135.
>
> Phần unexplained variation là sum of squared errors (SSE) = 0.0640.
> Tổng hai phần này cho ra total sum of squares (SST) = 0.0135 + 0.0640 = 0.0775.
>
> Cần phân biệt rõ: SSR đo lường mức độ mô hình hồi quy giải thích được biến động dữ liệu, còn SSE đo lường phần biến động còn lại mà mô hình chưa giải thích được.

---

## Câu 79

**Question 79: A 5.8% [[equity-investments/glossary/equity-m04-glossary#Preferred Stock|preferred stock]] with a par value of \$1,000 has an annual yield of 5.4%. A [[fixed-income/glossary/fi-m02#Zero-coupon bond|zero-coupon bond]] with a face value of \$1,000 will mature in 3 years and has a yield of 4.7% on a semiannual-bond [[derivatives/glossary/der-m03#Basis|basis]]. Which security has a higher price today?**

(A) The preferred stock.

(B) The zero-coupon bond.

(C) Their prices today are equal.

> [!answer]- Đáp án
> **(A) The preferred stock.**
> 
> Bạn chọn: (B) The zero-coupon bond.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (A) [[equity-investments/glossary/equity-m04-glossary#Preferred Stock|Preferred stock]] có giá cao hơn.
> Preferred stock trả cổ tức \$58/năm (\$1,000 × 5.8%) với yield yêu cầu là 5.4%, nên giá hiện tại = \$58 / 0.054 = \$1,074.07 — cao hơn mệnh giá \$1,000. [[fixed-income/glossary/fi-m02#Zero-coupon bond|Zero-coupon bond]] với face value \$1,000, kỳ hạn 3 năm và yield 4.7% (semiannual-bond [[derivatives/glossary/der-m03#Basis|basis]]) có giá = \$1,000 / (1 + 0.047/2)^6 = \$869.91.
>
> Ngay cả khi không tính cụ thể, ta có thể suy luận nhanh: preferred stock có giá > \$1,000 (vì yield < dividend rate), trong khi zero-coupon bond luôn có giá < \$1,000 (vì không có coupon), nên preferred stock chắc chắn có giá cao hơn.

---

## Câu 86

**Question 86: Zach Mann is examining stock performance after classifying stocks according to their [[equity-investments/glossary/equity-m04-glossary#Market Capitalization|market capitalization]] (firm size) and P/E ratio. First, Mann ranks stocks based on market capitalization by grouping stocks into deciles. Then, for each firm size [[quantitative-methods/glossary/m03-statistical-measures#Decile|decile]], he classifies stocks into P/E ratio quintiles. The total number of classifications created by Mann equals:**

(A) 5.

(B) 10.

(C) 50.

> [!answer]- Đáp án
> **(C) 50.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (C) 50.
> Mann đầu tiên chia cổ phiếu thành 10 nhóm theo [[equity-investments/glossary/equity-m04-glossary#Market Capitalization|market capitalization]] (deciles).
>
> Sau đó, trong mỗi nhóm đó, ông lại chia tiếp thành 5 nhóm theo P/E ratio (quintiles).
> Tổng số phân loại = 10 × 5 = 50.
>
> Đây là ví dụ về phân loại nhiều chiều (multivariate classification) — mỗi nhóm ở cấp trên được chia nhỏ thêm theo tiêu chí khác ở cấp dưới, tạo ra ma trận phân loại tổng hợp.

---

## Câu 90

**Question 90: An investor plans to divide her funds evenly between two assets. Assets 1 and 2 have standard deviations of 10% and 30%, respectively. If the two assets are perfectly positively correlated, the [[quantitative-methods/glossary/m03-statistical-measures#Standard Deviation|standard deviation]] of returns of the portfolio is closest to:**

(A) 10%.

(B) 15%.

(C) 20%.

> [!answer]- Đáp án
> **(C) 20%.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (C) 20%.
> Khi [[quantitative-methods/glossary/m03-statistical-measures#Correlation|correlation]] ρ = +1 (tương quan hoàn toàn dương), độ lệch chuẩn của danh mục chính bằng trung bình có trọng số của độ lệch chuẩn hai tài sản: σp = 0.5 × 10% + 0.5 × 30% = 20%.
>
> Đây là trường hợp đặc biệt: khi ρ = +1, không có lợi ích đa dạng hóa nào cả, vì vậy rủi ro của danh mục không giảm so với mức trung bình.
> Nếu ρ < 1, độ lệch chuẩn danh mục sẽ thấp hơn 20%, phản ánh lợi ích của diversification.

---

