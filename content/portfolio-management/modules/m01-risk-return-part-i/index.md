---
title: "M01 — Risk & Return"
type: module
subject: portfolio-management
module: M01
los: "1.a, 1.b, 1.c, 1.d, 1.e, 1.f, 1.g"
created: 2026-04-12
updated: 2026-04-12
tags:
  - cfa-level-1
  - portfolio-management
  - risk-return
  - modern-portfolio-theory
  - diversification
---

# Portfolio Risk and Return: Part I

> **Nguồn**: [[portfolio-management/sources/cfa-level1-portfolio-management|CFA L1 Portfolio Management]], tr.2-47
> **LOS**: 1.a-1.g

## LOS 1.a: Rủi ro và Lợi nhuận Lịch sử theo Nhóm Tài sản

### Các Nhóm Tài sản Chính (Phổ Rủi ro - Lợi nhuận)

| Nhóm tài sản | Rủi ro | Lợi nhuận kỳ vọng |
|-------------|------|-----------------|
| T-bills | Thấp nhất | Thấp nhất |
| Government bonds | Thấp | Thấp - trung bình |
| Corporate bonds | Trung bình | Trung bình |
| Large-cap stocks | Cao | Cao |
| Small-cap stocks | Cao nhất | Cao nhất |

**Nguyên tắc cốt lõi**: Rủi ro cao hơn $\rightarrow$ lợi nhuận kỳ vọng cao hơn (đánh đổi risk-return).

### Phân tích Lợi nhuận Kỳ vọng

$$
1 + E(R) = (1 + r_{rf}) \times [1 + E(\pi)] \times [1 + E(RP)]
$$

Trong đó:
- $r_{rf}$ = lãi suất phi rủi ro thực (real risk-free rate)
- $E(\pi)$ = lạm phát kỳ vọng
- $E(RP)$ = phần bù rủi ro kỳ vọng (expected risk premium)

### Lợi nhuận Thực (Real Return)

$$
R_{real} = \frac{1 + R_{nominal}}{1 + \pi} - 1
$$

## LOS 1.b: Đặc điểm Phân phối

### Độ lệch (Skewness)

- **Lệch dương (Positive skew)**: Đuôi phải dài hơn; mean > median > mode
- **Lệch âm (Negative skew)**: Đuôi trái dài hơn; mean < median < mode
- **Negative skewness** = rủi ro thua lỗ lớn (thường xuyên có lợi nhuận nhỏ, thỉnh thoảng thua lỗ nặng)

### Độ nhọn (Kurtosis)

- **Leptokurtic** (excess kurtosis > 0): Đuôi béo, xảy ra các kết quả cực đoan nhiều hơn phân phối chuẩn
- **Platykurtic** (excess kurtosis < 0): Đuôi mảnh
- **Mesokurtic** (excess kurtosis = 0): Phân phối chuẩn

> Đuôi béo làm tăng xác suất xảy ra kết quả cực đoan — quan trọng trong quản lý rủi ro.

## LOS 1.c: Thanh khoản và Lợi nhuận Kỳ vọng

- **Liquidity** = khả năng mua/bán nhanh chóng ở mức giá hợp lý với chi phí giao dịch thấp
- Tài sản kém thanh khoản hơn đòi hỏi một **liquidity risk premium** (lợi nhuận kỳ vọng cao hơn)
- Ảnh hưởng đến:
  - Bid-ask spread (càng rộng = thanh khoản càng thấp)
  - Tác động giá của giao dịch
  - Chi phí giao dịch

## LOS 1.d: Ngại rủi ro (Risk Aversion) và Utility

### Risk Aversion

| Loại | Hệ số $A$ | Hành vi |
|------|-----------------|----------|
| Risk averse | $A > 0$ | Yêu cầu risk premium khi chịu rủi ro |
| Risk neutral | $A = 0$ | Bàng quan với rủi ro; chỉ xét lợi nhuận kỳ vọng |
| Risk seeking | $A < 0$ | Sẵn sàng trả tiền để chấp nhận rủi ro |

### Hàm Utility

$$
U = E(R) - \frac{1}{2} A \sigma^2
$$

Trong đó:
- $U$ = utility (mức độ thỏa mãn) của khoản đầu tư
- $E(R)$ = lợi nhuận kỳ vọng
- $A$ = hệ số ngại rủi ro (risk aversion coefficient)
- $\sigma^2$ = phương sai của lợi nhuận

## LOS 1.e: Đường Bàng quan (Indifference Curves)

- Mỗi đường biểu diễn các tổ hợp $E(R)$ và $\sigma$ mang lại **utility bằng nhau**
- **Đường cao hơn** = utility cao hơn (được ưa thích hơn)
- **Nhà đầu tư risk-averse**: Độ dốc dương (nghiêng lên)
- **Đường dốc hơn** = ngại rủi ro hơn (đòi hỏi lợi nhuận lớn hơn cho mỗi đơn vị rủi ro)
- Các indifference curves **không bao giờ cắt nhau**

## LOS 1.f: Capital Allocation Line (CAL)

### Phương trình CAL

$$
E(R_p) = R_f + \left[\frac{E(R_i) - R_f}{\sigma_i}\right] \times \sigma_p
$$

Trong đó:
- $R_f$ = lãi suất phi rủi ro
- $E(R_i)$ = lợi nhuận kỳ vọng của tài sản rủi ro
- $\sigma_i$ = độ lệch chuẩn của tài sản rủi ro
- Số hạng trong ngoặc = **Sharpe ratio** = độ dốc của CAL

### Danh mục Tối ưu (Optimal Portfolio)

**Optimal portfolio** là **điểm tiếp tuyến** nơi indifference curve cao nhất có thể đạt được vừa chạm vào CAL.

- Nhà đầu tư ngại rủi ro hơn $\rightarrow$ danh mục gần $R_f$ hơn (cho vay nhiều hơn)
- Nhà đầu tư ít ngại rủi ro hơn $\rightarrow$ danh mục xa hơn trên CAL (nhiều tài sản rủi ro hơn, có thể sử dụng đòn bẩy)

## LOS 1.g: Rủi ro Danh mục với Hai Tài sản

### Phương sai và Hiệp phương sai

$$
\sigma^2 = \frac{\sum_{t=1}^{n}(R_t - \bar{R})^2}{n - 1}
$$

$$
\text{Cov}_{12} = \frac{\sum_{t=1}^{n}(R_{1,t} - \bar{R}_1)(R_{2,t} - \bar{R}_2)}{n - 1}
$$

$$
\rho_{12} = \frac{\text{Cov}_{12}}{\sigma_1 \sigma_2}
$$

Trong đó $-1 \leq \rho_{12} \leq 1$.

### Phương sai Danh mục Hai Tài sản

$$
\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2 w_1 w_2 \text{Cov}_{12}
$$

Hoặc tương đương:

$$
\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2 w_1 w_2 \rho_{12} \sigma_1 \sigma_2
$$

### Tương quan (Correlation) và Đa dạng hóa (Diversification)

| Tương quan ($\rho$) | Lợi ích Diversification |
|----------------------|------------------------|
| $\rho = +1$ | **Không có** — rủi ro danh mục bằng bình quân gia quyền rủi ro từng tài sản |
| $-1 < \rho < +1$ | **Một phần** — rủi ro giảm xuống dưới bình quân gia quyền |
| $\rho = -1$ | **Tối đa** — có thể loại bỏ hoàn toàn rủi ro |

### Efficient Frontier

- **Minimum-variance frontier**: Tập hợp các danh mục có phương sai thấp nhất tại mỗi mức lợi nhuận
- **Global minimum-variance portfolio**: Danh mục có phương sai thấp tuyệt đối nhất
- **Efficient frontier**: Phần trên của minimum-variance frontier (phía trên global minimum-variance portfolio)
- Nhà đầu tư hợp lý chọn danh mục nằm trên efficient frontier

## Điểm Mấu chốt

1. Dữ liệu lịch sử cho thấy mối quan hệ thuận chiều giữa rủi ro và lợi nhuận trên các nhóm tài sản
2. Negative skewness và excess kurtosis làm tăng rủi ro thua lỗ vượt ra ngoài những gì phương sai có thể nắm bắt
3. Nhà đầu tư risk-averse tối đa hóa $U = E(R) - \frac{1}{2}A\sigma^2$
4. Diversification làm giảm rủi ro danh mục khi $\rho < 1$
5. Optimal portfolio là nơi indifference curve cao nhất của nhà đầu tư tiếp tuyến với CAL

---

**Tiếp theo**: [[portfolio-management/modules/m02-risk-return-part-ii/index|M02: Portfolio Risk and Return: Part II]]