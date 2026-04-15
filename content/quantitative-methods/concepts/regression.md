---
title: "Simple Linear Regression"
type: concept
subject: quantitative-methods
module: M10
created: 2026-04-09
updated: 2026-04-09
tags: [regression, OLS, R-squared, ANOVA, prediction, assumptions]
---

# Simple Linear Regression

## Tổng quan

Simple linear regression mô hình hóa mối quan hệ tuyến tính giữa một [[quantitative-methods/glossary/m10-simple-linear-regression#Dependent Variable|biến phụ thuộc]] $Y$ và một [[quantitative-methods/glossary/m10-simple-linear-regression#Independent Variable|biến độc lập]] $X$ duy nhất. Đây là nền tảng cho toàn bộ phân tích hồi quy trong tài chính — được dùng để ước tính mức độ phơi nhiễu nhân tố (factor exposures), dự báo lợi suất, phân tích mối quan hệ giữa các biến kinh tế, và kiểm định xem một biến dự báo có sức giải thích thống kê có ý nghĩa hay không.

## Mô hình và Ước lượng OLS

Mô hình hồi quy tổng thể là:

$$Y_i = b_0 + b_1 X_i + \varepsilon_i$$

trong đó $b_0$ là hệ số chặn (intercept), $b_1$ là hệ số góc (slope), và $\varepsilon_i$ là sai số (error term) — được giả định có kỳ vọng bằng không, phương sai không đổi, và không tương quan với nhau giữa các quan sát. Mô hình ước lượng là:

$$\hat{Y}_i = \hat{b}_0 + \hat{b}_1 X_i$$

**[[quantitative-methods/glossary/m10-simple-linear-regression#Ordinary Least Squares (OLS)|Ordinary Least Squares (OLS)]]** ước lượng $\hat{b}_0$ và $\hat{b}_1$ bằng cách tối thiểu hóa [[quantitative-methods/glossary/m10-simple-linear-regression#Sum of Squares Error (SSE)|tổng bình phương phần dư]]. Ước lượng OLS có nghiệm dạng đóng:

$$\hat{b}_1 = \frac{\text{Cov}(X,Y)}{s_X^2} \qquad \hat{b}_0 = \bar{Y} - \hat{b}_1 \bar{X}$$

Hệ số góc ước lượng bằng tỷ số giữa hiệp phương sai mẫu của $X$ và $Y$ so với phương sai mẫu của $X$. Khi các giả định cổ điển được thỏa mãn (tuyến tính, độc lập, [[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|homoskedasticity]], phân phối chuẩn), OLS là **Best Linear Unbiased Estimator (BLUE)** — ước lượng tuyến tính không chệch hiệu quả nhất.

## Diễn giải Hệ số

- **[[quantitative-methods/glossary/m10-simple-linear-regression#Intercept|Intercept]] $\hat{b}_0$**: Giá trị dự báo của $Y$ khi $X = 0$. Có thể không mang ý nghĩa kinh tế nếu $X=0$ nằm ngoài phạm vi dữ liệu.
- **[[quantitative-methods/glossary/m10-simple-linear-regression#Slope Coefficient|Slope $\hat{b}_1$]]**: Khi $X$ tăng một đơn vị, $Y$ thay đổi trung bình $\hat{b}_1$ đơn vị, trong điều kiện các yếu tố khác không đổi. Dấu cho biết chiều của mối quan hệ; độ lớn cho biết mức độ mạnh yếu.
- **[[quantitative-methods/glossary/m10-simple-linear-regression#Residual|Residual]] $\hat{\varepsilon}_i = Y_i - \hat{Y}_i$**: Phần của $Y_i$ không được mô hình hồi quy giải thích. Tổng các residual bằng không; phân tích residual giúp phát hiện vi phạm các giả định.

## Độ phù hợp: R² và SEE

Biến động trong $Y$ được phân tích như sau:

$$\underbrace{SST}_{\text{Tổng}} = \underbrace{SSR}_{\text{Giải thích được}} + \underbrace{SSE}_{\text{Không giải thích được}}$$

**[[quantitative-methods/glossary/m10-simple-linear-regression#Coefficient of Determination (R²)|Hệ số xác định R²]]** đo tỷ lệ tổng biến động trong $Y$ được giải thích bởi $X$:

$$R^2 = \frac{SSR}{SST} = 1 - \frac{SSE}{SST} \in [0,1]$$

Trong simple linear regression, $R^2 = r_{XY}^2$ (bình phương của hệ số tương quan Pearson). $R^2$ càng cao thì mô hình càng khớp tốt, nhưng $R^2$ cao một mình không đủ để xác nhận mô hình là hợp lệ.

**[[quantitative-methods/glossary/m10-simple-linear-regression#Standard Error of Estimate (SEE)|Standard error of estimate (SEE)]]** đo kích thước trung bình của residual:

$$SEE = \sqrt{\frac{SSE}{n-2}}$$

SEE càng nhỏ thì đường hồi quy càng gần với các điểm dữ liệu thực tế. SEE được dùng để xây dựng [[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|prediction intervals]].

## Kiểm định Ý nghĩa: ANOVA và t-Tests

**[[quantitative-methods/glossary/m10-simple-linear-regression#ANOVA (Analysis of Variance)|Bảng ANOVA]]** tổ chức phân tích phương sai và tạo ra **[[quantitative-methods/glossary/m10-simple-linear-regression#F-Statistic|F-statistic]]** để kiểm định ý nghĩa tổng thể của mô hình:

$$H_0: b_1 = 0 \qquad F = \frac{MSR}{MSE} = \frac{SSR/1}{SSE/(n-2)}$$

Bác bỏ $H_0$ (mô hình không có sức giải thích) khi $F > F_{\text{critical}}$.

Các hệ số riêng lẻ được kiểm định bằng **[[quantitative-methods/glossary/m10-simple-linear-regression#t-Test for Slope|t-tests]]**:

$$t = \frac{\hat{b}_1}{s_{\hat{b}_1}} \qquad df = n-2$$

Trong simple linear regression, $F = t_{\hat{b}_1}^2$ — F-test và slope t-test là tương đương nhau.

## Các Giả định Cổ điển và Vi phạm

Bốn giả định cổ điển phải được thỏa mãn để OLS cho ra ước lượng hợp lệ và hiệu quả:

1. **[[quantitative-methods/glossary/m10-simple-linear-regression#Linearity Assumption|Tuyến tính (Linearity)]]**: Mối quan hệ thực sự là tuyến tính. Các vi phạm thường có thể khắc phục bằng cách biến đổi biến ([[quantitative-methods/glossary/m10-simple-linear-regression#Log-Log Model|log-log]], [[quantitative-methods/glossary/m10-simple-linear-regression#Log-Lin Model|log-lin]], [[quantitative-methods/glossary/m10-simple-linear-regression#Lin-Log Model|lin-log]]).
2. **[[quantitative-methods/glossary/m10-simple-linear-regression#Independence Assumption|Độc lập (Independence)]]**: Các sai số không tương quan với nhau và với $X$. Vi phạm bởi serial correlation (phổ biến trong chuỗi thời gian), làm lệch sai số chuẩn.
3. **[[quantitative-methods/glossary/m10-simple-linear-regression#Homoskedasticity|Homoskedasticity]]**: Phương sai sai số là hằng số. **[[quantitative-methods/glossary/m10-simple-linear-regression#Heteroskedasticity|Heteroskedasticity]]** (phương sai không ổn định) khiến sai số chuẩn OLS không đáng tin cậy.
4. **[[quantitative-methods/glossary/m10-simple-linear-regression#Normality Assumption|Phân phối chuẩn (Normality)]]**: Sai số tuân theo phân phối chuẩn. Quan trọng khi suy diễn với mẫu nhỏ; ít quan trọng hơn với mẫu lớn do [[quantitative-methods/glossary/m07-estimation-and-inference#Central Limit Theorem (CLT)|CLT]].

## Dự báo

Với giá trị mới $X_0$, giá trị dự báo của $Y$ là $\hat{Y}_0 = \hat{b}_0 + \hat{b}_1 X_0$. **[[quantitative-methods/glossary/m10-simple-linear-regression#Prediction Interval|Prediction interval]]** tính đến cả sự không chắc chắn của mô hình (confidence interval cho giá trị trung bình) lẫn phương sai của từng quan sát riêng lẻ:

$$\hat{Y}_0 \pm t_{\alpha/2, n-2} \times s_f \qquad s_f = SEE\sqrt{1 + \frac{1}{n} + \frac{(X_0 - \bar{X})^2}{\sum(X_i - \bar{X})^2}}$$

Prediction intervals luôn rộng hơn confidence intervals cho giá trị trung bình. Khoảng tin cậy mở rộng khi $X_0$ càng xa $\bar{X}$ — đây là giới hạn quan trọng khi ngoại suy ngoài phạm vi dữ liệu.

## Các Module Nguồn

- [[quantitative-methods/modules/m10-simple-linear-regression/index|M10 — Simple Linear Regression]] — nội dung chính
- [[quantitative-methods/modules/m08-hypothesis-testing/index|M08 — Hypothesis Testing]] — t-tests và F-tests dùng trong hồi quy
- [[quantitative-methods/modules/m06-simulation-methods/index|M06 — Simulation Methods]] — phân phối F và t dùng cho suy diễn hồi quy