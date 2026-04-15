---
title: "Simulation Methods"
type: concept
subject: quantitative-methods
module: M06
created: 2026-04-09
updated: 2026-04-09
tags: [simulation, monte-carlo, bootstrap, jackknife, resampling, VaR]
---

# Simulation Methods

## Tổng quan

Suy diễn thống kê cổ điển dựa vào các công thức dạng đóng và phân phối đã biết. Khi bài toán trở nên quá phức tạp để giải tích phân — hoặc khi phân phối của một thống kê là chưa biết — các phương pháp simulation cung cấp một giải pháp tính toán mạnh mẽ. Chương trình CFA bao gồm ba phương pháp chính: [[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]], [[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|bootstrap]], và [[quantitative-methods/glossary/m06-simulation-methods#Jackknife|jackknife]]. Mỗi phương pháp có điểm mạnh riêng và phù hợp với các bài toán khác nhau.

## Monte Carlo Simulation

**[[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]]** tạo ra một phân phối các kết quả bằng cách:
1. Xác định phân phối xác suất cho tất cả các biến đầu vào (ví dụ: lợi suất, biến động, tương quan).
2. Rút giá trị ngẫu nhiên từ các phân phối đó cho mỗi lần thử.
3. Tính toán kết quả cần quan tâm (ví dụ: giá trị danh mục, payoff của quyền chọn) cho mỗi bộ giá trị được rút.
4. Lặp lại bước 2–3 hàng nghìn hoặc hàng triệu lần.
5. Phân tích phân phối thực nghiệm của các kết quả.

Monte Carlo yêu cầu một **mô hình** — nhà phân tích phải xác định đầy đủ quá trình tạo dữ liệu (tất cả các phân phối và tham số của chúng). Nếu mô hình bị xác định sai, kết quả sẽ không đáng tin cậy ("garbage in, garbage out").

**Các ứng dụng chính trong tài chính**:
- Ước tính **[[quantitative-methods/glossary/m06-simulation-methods#Value at Risk (VaR)|Value at Risk (VaR)]]**: ngưỡng tổn thất bị vượt qua với xác suất $\alpha$ trong một khoảng thời gian cho trước.
- Định giá các derivatives phức tạp với payoff phụ thuộc vào đường đi (ví dụ: barrier options, Asian options).
- Mô hình hóa khả năng thanh toán của quỹ hưu trí trong điều kiện lợi suất tương lai và mức tăng trưởng nợ phải trả không chắc chắn.
- Stress-testing hiệu suất danh mục qua nhiều kịch bản kinh tế.

**Hạn chế**: Monte Carlo không thể xác định *nguyên nhân* của một kết quả — đây là simulation của một mô hình, không phải bằng chứng. Kết quả chỉ đáng tin cậy khi các phân phối giả định là chính xác.

## Bootstrap Resampling

**[[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|Bootstrap]]** xây dựng phân phối lấy mẫu của một thống kê theo cách thực nghiệm — không giả định bất kỳ phân phối nền nào — bằng cách lấy mẫu lại **có hoàn lại** từ dữ liệu quan sát:

1. Rút một bootstrap sample kích thước $n$ từ dữ liệu gốc (có hoàn lại).
2. Tính thống kê cần quan tâm (ví dụ: trung bình, Sharpe ratio, hệ số hồi quy).
3. Lặp lại $B$ lần (thông thường $B = 1{,}000$ đến $10{,}000$).
4. Sử dụng phân phối thực nghiệm của $B$ thống kê tính được để suy diễn (sai số chuẩn, khoảng tin cậy).

**Ưu điểm so với Monte Carlo**: Bootstrap không đưa ra giả định tham số về phân phối tổng thể. Nó sử dụng chính dữ liệu quan sát như là ước tính của tổng thể. Điều này giúp phương pháp này vững chắc khi phân phối chưa biết hoặc không chuẩn — phổ biến trong lợi suất tài chính có [[quantitative-methods/glossary/m03-statistical-measures#Leptokurtic|fat tails]] và [[quantitative-methods/glossary/m03-statistical-measures#Skewness|skewness]].

**Ứng dụng chính**: Ước tính phân phối lấy mẫu của các estimator phức tạp mà không tồn tại công thức sai số chuẩn dạng đóng (ví dụ: median, hệ số quantile regression, Sharpe ratio của danh mục).

## Jackknife Resampling

**[[quantitative-methods/glossary/m06-simulation-methods#Jackknife|Jackknife]]** lần lượt bỏ từng quan sát một, tính thống kê trên $n-1$ quan sát còn lại:

1. Tính thống kê trên tất cả $n$ quan sát: $\hat{\theta}$.
2. Với $i = 1, 2, \ldots, n$: loại bỏ quan sát $i$, tính $\hat{\theta}_{(-i)}$.
3. Sử dụng $n$ giá trị leave-one-out để ước tính bias và phương sai của $\hat{\theta}$.

$$\hat{\theta}_{\text{bias}} = (n-1)\left(\bar{\hat{\theta}}_{(.)} - \hat{\theta}\right) \qquad \bar{\hat{\theta}}_{(.)} = \frac{1}{n}\sum_{i=1}^{n} \hat{\theta}_{(-i)}$$

**Điểm khác biệt chính so với bootstrap**: Jackknife mang tính tất định (không có yếu tố ngẫu nhiên), trong khi bootstrap mang tính ngẫu nhiên (yêu cầu rút mẫu ngẫu nhiên). Jackknife tính đúng $n$ ước tính leave-one-out; bootstrap tính $B$ resample ngẫu nhiên.

**Khi nào nên dùng jackknife thay vì bootstrap**: Ước tính bias; các thống kê tuyến tính mà jackknife đơn giản hơn về mặt tính toán.

## So sánh Tổng hợp

| Đặc điểm | Monte Carlo | Bootstrap | Jackknife |
|---------|------------|-----------|-----------|
| Yêu cầu giả định phân phối | Có | Không | Không |
| Sử dụng trực tiếp dữ liệu quan sát | Không | Có | Có |
| Phương pháp lấy mẫu | Ngẫu nhiên (từ mô hình) | Có hoàn lại | Có hệ thống (leave-one-out) |
| Mục đích chính | Kết quả phức tạp, derivatives, VaR | Phân phối lấy mẫu, khoảng tin cậy | Ước tính bias |
| Tính toán chuyên sâu | Rất nhiều | Vừa phải | Ít hơn |
| Có thể xử lý dữ liệu không chuẩn | Nếu mô hình cho phép | Có | Có |

## Ứng dụng trong Phân tích Đầu tư

Cả ba phương pháp được sử dụng khi các công thức chuẩn không áp dụng được:
- **Monte Carlo**: Simulation danh mục cho kế hoạch hưu trí, định giá quyền chọn ngoài phạm vi Black-Scholes, stress testing.
- **Bootstrap**: Backtesting các chiến lược giao dịch có tính đến sai số ước tính; xây dựng khoảng tin cậy cho các chỉ số hiệu suất như information ratio.
- **Jackknife**: Đánh giá độ ổn định của các ước tính hồi quy; phát hiện các quan sát có ảnh hưởng lớn.

## Các Module Nguồn

- [[quantitative-methods/modules/m06-simulation-methods/index|M06 — Simulation Methods]] — nội dung chính
- [[quantitative-methods/modules/m05-portfolio-math/index|M05 — Portfolio Mathematics]] — khung phương sai danh mục mà Monte Carlo mô phỏng
- [[quantitative-methods/modules/m07-estimation-and-inference/index|M07 — Estimation and Inference]] — bootstrap như một giải pháp thay thế cho sai số chuẩn phân tích