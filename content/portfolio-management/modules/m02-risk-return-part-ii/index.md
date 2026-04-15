---
title: "M02 — CML & CAPM"
type: module
subject: portfolio-management
module: M02
los: "2.a, 2.b, 2.c, 2.d, 2.e, 2.f, 2.g, 2.h, 2.i"
created: 2026-04-12
updated: 2026-04-12
tags:
  - cfa-level-1
  - portfolio-management
  - capm
  - sml
  - cml
  - beta
  - performance-measures
---

# Portfolio Risk and Return: Part II

> **Nguồn**: [[portfolio-management/sources/cfa-level1-portfolio-management|CFA L1 Portfolio Management]], tr.48-82
> **LOS**: 2.a-2.i

## LOS 2.a: Tài Sản Phi Rủi Ro và CAL

Kết hợp một **tài sản phi rủi ro** (risk-free asset) với một **danh mục rủi ro** (risky portfolio) tạo ra một **Capital Allocation Line (CAL)** vượt trội so với đường biên hiệu quả.

- CAL là một đường thẳng từ $R_f$ đi qua danh mục rủi ro
- Mọi điểm trên CAL đều cho tỷ lệ rủi ro-lợi suất tốt hơn so với đường biên hiệu quả đơn thuần (ngoại trừ điểm tiếp xúc)

## LOS 2.b: Capital Market Line (CML)

**CML** là trường hợp đặc biệt của CAL khi danh mục rủi ro là **danh mục thị trường** (market portfolio).

$$
E(R_p) = R_f + \left[\frac{E(R_m) - R_f}{\sigma_m}\right] \times \sigma_p
$$

### Homogeneity of Expectations

Dưới giả định rằng tất cả nhà đầu tư đều có **kỳ vọng đồng nhất** (ước tính giống nhau về lợi suất kỳ vọng, phương sai và hiệp phương sai):
- Tất cả nhà đầu tư đều xác định **danh mục rủi ro tối ưu giống nhau** = **market portfolio**
- Tất cả nhà đầu tư nắm giữ cùng một danh mục rủi ro; điểm khác biệt duy nhất là tỷ lệ phân bổ giữa tài sản phi rủi ro và tài sản rủi ro

### Lending vs Borrowing Portfolios

| Loại Danh Mục | Tỷ Trọng Tài Sản Phi Rủi Ro ($w_1$) | Vị Thế |
|---------------|--------------------------------------|--------|
| Lending | $w_1 > 0$ | Nằm giữa $R_f$ và market portfolio trên CML |
| Borrowing | $w_1 < 0$ | Vượt ra ngoài market portfolio trên CML (đòn bẩy) |

> **Kinked CAL**: Nếu lãi suất vay (borrowing rate) $>$ lãi suất cho vay (lending rate), CAL sẽ có một điểm gãy tại market portfolio (độ dốc lớn hơn ở phía dưới, thấp hơn ở phía trên).

## LOS 2.c: Systematic vs Nonsystematic Risk

$$
\text{Total Risk} = \text{Systematic Risk} + \text{Nonsystematic Risk}
$$

| | Systematic (Market) Risk | Nonsystematic (Specific) Risk |
|---|---|---|
| **Nguồn gốc** | Các yếu tố thị trường toàn diện | Các yếu tố đặc thù của doanh nghiệp |
| **Có thể đa dạng hóa?** | Không | Có |
| **Được định giá/bù đắp?** | Có | Không |
| **Ví dụ** | Lãi suất, GDP, lạm phát | Kiện tụng, thay đổi ban lãnh đạo |

- Đa dạng hóa (diversification) chỉ giảm được **nonsystematic risk**
- Khoảng **30 cổ phiếu** trong một danh mục có thể loại bỏ phần lớn nonsystematic risk
- Chỉ có **systematic risk** mới được bù đắp bằng lợi suất kỳ vọng cao hơn

## LOS 2.d: Return Generating Models

### Single-Factor Model (Market Model)

$$
R_i = \alpha_i + \beta_i R_m + e_i
$$

Trong đó:
- $\alpha_i$ = hệ số chặn (lợi suất đặc thù của doanh nghiệp)
- $\beta_i$ = độ nhạy cảm với lợi suất thị trường
- $e_i$ = phần dư (thành phần nonsystematic)

### Multi-Factor Models

| Mô Hình | Các Nhân Tố |
|---------|-------------|
| **Fama-French 3-Factor** | Market, Size (SMB), Value (HML) |
| **Carhart 4-Factor** | Market, Size, Value, Momentum (WML) |

## LOS 2.e: Beta

$$
\beta_i = \frac{\text{Cov}(R_i, R_m)}{\sigma_m^2} = \rho_{i,m} \times \frac{\sigma_i}{\sigma_m}
$$

| Giá Trị Beta | Diễn Giải |
|-------------|-----------|
| $\beta = 0$ | Tài sản phi rủi ro |
| $\beta = 1$ | Có systematic risk bằng với thị trường |
| $\beta > 1$ | Biến động mạnh hơn thị trường (aggressive) |
| $0 < \beta < 1$ | Biến động yếu hơn thị trường (defensive) |

**Portfolio beta**: $\beta_p = \sum w_i \beta_i$ (bình quân gia quyền của các beta thành phần)

## LOS 2.f: Capital Asset Pricing Model (CAPM)

$$
E(R_i) = R_f + \beta_i \times [E(R_m) - R_f]
$$

Trong đó $[E(R_m) - R_f]$ = **market risk premium** (phần bù rủi ro thị trường).

### CAPM Assumptions

- Vay và cho vay phi rủi ro tại cùng một mức lãi suất
- Thị trường không ma sát (không có thuế, không có chi phí giao dịch)
- Kỳ vọng đồng nhất (homogeneous expectations)
- Chân trời đầu tư một kỳ (single-period investment horizon)
- Nhà đầu tư là người chấp nhận giá (price takers)
- Tất cả tài sản đều có thể mua bán và phân chia được

## LOS 2.g: Security Market Line (SML)

**SML** là biểu diễn đồ họa của CAPM:
- **Trục X**: $\beta$ (systematic risk)
- **Trục Y**: $E(R)$ (lợi suất kỳ vọng)
- **Độ dốc**: Market risk premium $= E(R_m) - R_f$
- **Hệ số chặn**: $R_f$

**Tín hiệu định giá sai**:
- Tài sản **nằm trên** SML $\rightarrow$ bị định giá thấp (lợi suất kỳ vọng > lợi suất yêu cầu)
- Tài sản **nằm dưới** SML $\rightarrow$ bị định giá cao (lợi suất kỳ vọng < lợi suất yêu cầu)
- Tài sản **nằm trên** SML $\rightarrow$ được định giá hợp lý

## LOS 2.h: CML vs SML

| Đặc Điểm | CML | SML |
|----------|-----|-----|
| Thước đo rủi ro | Rủi ro tổng thể ($\sigma$) | Systematic risk ($\beta$) |
| Áp dụng cho | Chỉ các danh mục hiệu quả | Tất cả tài sản và danh mục |
| Trục X | $\sigma$ | $\beta$ |
| Độ dốc | $\frac{E(R_m) - R_f}{\sigma_m}$ (Sharpe ratio) | $E(R_m) - R_f$ (market risk premium) |

## LOS 2.i: Performance Measures

### Sharpe Ratio

$$
\text{Sharpe} = \frac{R_p - R_f}{\sigma_p}
$$

- Sử dụng **rủi ro tổng thể** ($\sigma$)
- Phù hợp để đánh giá **toàn bộ danh mục đầu tư** của một nhà đầu tư

### Treynor Ratio

$$
\text{Treynor} = \frac{R_p - R_f}{\beta_p}
$$

- Sử dụng **systematic risk** ($\beta$)
- Phù hợp để đánh giá một danh mục là **một phần trong danh mục lớn hơn**

### M-Squared ($M^2$)

$$
M^2 = (R_p - R_f) \times \frac{\sigma_m}{\sigma_p} - (R_m - R_f)
$$

- Điều chỉnh danh mục về cùng mức rủi ro tổng thể với thị trường
- Được biểu diễn dưới dạng **phần trăm** (dễ diễn giải hơn Sharpe ratio)
- $M^2 > 0 \Rightarrow$ vượt trội so với thị trường

### Jensen's Alpha

$$
\alpha_p = R_p - [R_f + \beta_p (R_m - R_f)]
$$

- Lợi suất vượt trội so với mức CAPM dự đoán
- $\alpha > 0 \Rightarrow$ hiệu suất điều chỉnh rủi ro dương

### Tổng Hợp Các Thước Đo Hiệu Suất

| Thước Đo | Cơ Sở Rủi Ro | Phù Hợp Nhất Cho |
|----------|-------------|-----------------|
| Sharpe | Tổng thể ($\sigma$) | Toàn bộ danh mục |
| Treynor | Systematic ($\beta$) | Danh mục con |
| $M^2$ | Tổng thể ($\sigma$) | Toàn bộ danh mục (dạng %) |
| Jensen's $\alpha$ | Systematic ($\beta$) | Danh mục con |

## Điểm Mấu Chốt

1. CML sử dụng market portfolio làm danh mục rủi ro tối ưu dưới giả định kỳ vọng đồng nhất
2. Chỉ systematic risk mới được định giá; nonsystematic risk có thể loại bỏ bằng đa dạng hóa
3. CAPM: $E(R_i) = R_f + \beta_i [E(R_m) - R_f]$
4. SML áp dụng cho tất cả tài sản; CML chỉ áp dụng cho các danh mục hiệu quả
5. Sharpe và $M^2$ sử dụng rủi ro tổng thể; Treynor và Jensen's $\alpha$ sử dụng systematic risk

---

**Trước**: [[portfolio-management/modules/m01-risk-return-part-i/index|M01: Portfolio Risk and Return: Part I]]
**Tiếp theo**: [[portfolio-management/modules/m03-portfolio-management-overview/index|M03: Portfolio Management: An Overview]]