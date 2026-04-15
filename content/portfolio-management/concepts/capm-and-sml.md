---
title: CAPM and Security Market Line
type: concept
subject: portfolio-management
module: "M02"
created: 2026-04-12
updated: 2026-04-12
tags: [CAPM, SML, CML, beta, systematic-risk, market-model]
---

# CAPM and Security Market Line

## Capital Market Line (CML)

Khi tất cả nhà đầu tư có **kỳ vọng đồng nhất** (homogeneous expectations), danh mục rủi ro tối ưu chính là **market portfolio**. Đường CAL kẻ qua market portfolio trở thành **CML**:

$$E(R_p) = R_f + \left[\frac{E(R_m) - R_f}{\sigma_m}\right] \sigma_p$$

trong đó:
- $E(R_m)$ = lợi suất kỳ vọng của market portfolio
- $\sigma_m$ = độ lệch chuẩn của market portfolio
- Độ dốc = **market Sharpe ratio**

Đặc điểm chính:
- Chỉ có **danh mục hiệu quả** (efficient portfolios) mới nằm trên CML
- Chứng khoán đơn lẻ và danh mục không hiệu quả nằm **bên dưới** CML
- CML sử dụng **rủi ro tổng thể** ($\sigma_p$) trên trục x

## Systematic vs Unsystematic Risk

$$\text{Total risk} = \text{Systematic risk} + \text{Unsystematic risk}$$

| | Systematic (Market) Risk | Unsystematic (Specific) Risk |
|---|---|---|
| Nguồn gốc | Các yếu tố kinh tế vĩ mô | Sự kiện đặc thù của doanh nghiệp |
| Có thể đa dạng hóa? | Không | Có |
| Đo lường bằng | $\beta$ | Phương sai phần dư |
| Được bù đắp? | Có (định giá trong trạng thái cân bằng) | Không (có thể loại bỏ bằng đa dạng hóa) |

## Beta

$$\beta_i = \frac{\text{Cov}(R_i, R_m)}{\sigma_m^2} = \rho_{im} \times \frac{\sigma_i}{\sigma_m}$$

trong đó:
- $\text{Cov}(R_i, R_m)$ = hiệp phương sai của tài sản $i$ với thị trường
- $\sigma_m^2$ = phương sai của lợi suất thị trường
- $\rho_{im}$ = tương quan của tài sản $i$ với thị trường

| $\beta$ | Diễn giải |
|---|---|
| $\beta = 1$ | Rủi ro hệ thống bằng với thị trường |
| $\beta > 1$ | Tích cực (khuếch đại biến động thị trường) |
| $0 < \beta < 1$ | Phòng thủ (giảm nhẹ biến động thị trường) |
| $\beta = 0$ | Tài sản phi rủi ro |
| $\beta < 0$ | Biến động ngược chiều thị trường (hiếm gặp) |

**Portfolio beta** là bình quân gia quyền:

$$\beta_p = \sum w_i \times \beta_i$$

## Capital Asset Pricing Model (CAPM)

$$E(R_i) = R_f + \beta_i [E(R_m) - R_f]$$

trong đó:
- $E(R_i)$ = lợi suất yêu cầu của tài sản $i$
- $R_f$ = lãi suất phi rủi ro
- $\beta_i$ = beta của tài sản $i$
- $E(R_m) - R_f$ = **market risk premium**

### CAPM Assumptions

1. Nhà đầu tư ngại rủi ro, tối đa hóa độ thỏa dụng, hành động hợp lý
2. Thị trường không có ma sát (không thuế, không chi phí giao dịch)
3. Tất cả nhà đầu tư lập kế hoạch cho cùng một kỳ nắm giữ duy nhất
4. Kỳ vọng đồng nhất (cùng $E(R)$, $\sigma$, $\rho$ cho tất cả tài sản)
5. Tất cả khoản đầu tư có thể chia nhỏ vô hạn
6. Nhà đầu tư là người chấp nhận giá (không tác động đến thị trường)

## Security Market Line (SML)

SML là biểu diễn đồ thị của CAPM:
- **Trục x**: $\beta_i$ (chỉ rủi ro hệ thống)
- **Trục y**: $E(R_i)$
- **Giao điểm với trục y**: $R_f$
- **Độ dốc**: $E(R_m) - R_f$ (market risk premium)

### SML vs CML

| Đặc điểm | CML | SML |
|---|---|---|
| Thước đo rủi ro | Rủi ro tổng thể ($\sigma$) | Rủi ro hệ thống ($\beta$) |
| Áp dụng cho | Chỉ danh mục hiệu quả | Tất cả chứng khoán và danh mục |
| Phương trình | $E(R_p) = R_f + \frac{E(R_m)-R_f}{\sigma_m}\sigma_p$ | $E(R_i) = R_f + \beta_i[E(R_m)-R_f]$ |

### Mispricing on the SML

| Vị trí | Ý nghĩa | Hành động |
|---|---|---|
| Trên SML | Định giá thấp (alpha dương) | Mua |
| Trên SML | Định giá hợp lý | Giữ |
| Dưới SML | Định giá cao (alpha âm) | Bán / Short |

## Market Model (Single-Index Model)

$$R_i = \alpha_i + \beta_i R_m + e_i$$

trong đó:
- $\alpha_i$ = hệ số chặn (lợi suất bất thường)
- $\beta_i$ = độ nhạy cảm với thị trường
- $e_i$ = lợi suất đặc thù của doanh nghiệp (phần dư, $E(e_i) = 0$)

Đây là mô hình **dựa trên hồi quy** (thực nghiệm), trong khi CAPM là mô hình **cân bằng** (lý thuyết).

## Multi-Factor Models

Mở rộng CAPM bằng cách thêm các nhân tố rủi ro ngoài lợi suất thị trường:

**Fama-French Three-Factor Model**:

$$E(R_i) - R_f = \beta_{i,\text{mkt}}(R_m - R_f) + \beta_{i,\text{SMB}} \cdot \text{SMB} + \beta_{i,\text{HML}} \cdot \text{HML}$$

trong đó:
- SMB = Small Minus Big (phần bù quy mô)
- HML = High Minus Low (phần bù giá trị)

**Carhart Four-Factor Model** bổ sung thêm:
- WML = Winners Minus Losers (nhân tố động lượng)

## See Also

- [[portfolio-management/concepts/portfolio-risk-return|Portfolio Risk and Return]]
- [[portfolio-management/concepts/performance-measurement|Performance Measurement]]
- [[portfolio-management/formulas/pm-formulas|PM Master Formula Sheet]]
- [[portfolio-management/glossary/pm-m02|Glossary M02]]