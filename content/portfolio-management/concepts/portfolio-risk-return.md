---
title: Portfolio Risk and Return
type: concept
subject: portfolio-management
module: "M01"
created: 2026-04-12
updated: 2026-04-12
tags: [risk-return, utility, indifference-curve, CAL, efficient-frontier]
---

# Portfolio Risk and Return

## Risk-Return Tradeoff

Nhà đầu tư yêu cầu expected return cao hơn khi chấp nhận thêm rủi ro. **Risk premium** bù đắp cho sự không chắc chắn:

$$E(R_p) = R_f + \text{Risk Premium}$$

Phương pháp building-block phân tách expected return như sau:

$$1 + E(R) = (1 + r_{rf})(1 + E(\pi))(1 + E(RP))$$

trong đó:
- $r_{rf}$ = lãi suất phi rủi ro thực (real risk-free rate)
- $E(\pi)$ = kỳ vọng phần bù lạm phát (expected inflation premium)
- $E(RP)$ = kỳ vọng phần bù rủi ro (expected risk premium)

## Real vs Nominal Returns

$$R_{\text{real}} = \frac{1 + R_{\text{nominal}}}{1 + \pi} - 1$$

## Utility Function

Utility của nhà đầu tư risk-averse được mô hình hóa như sau:

$$U = E(R) - \frac{1}{2} A \sigma^2$$

trong đó:
- $U$ = utility (tương đương lợi suất chắc chắn — certainty-equivalent return)
- $E(R)$ = expected return
- $A$ = hệ số ngại rủi ro (risk aversion coefficient, $A > 0$ với nhà đầu tư risk-averse)
- $\sigma^2$ = phương sai của lợi suất (variance of returns)

| Loại nhà đầu tư | $A$ | Ý nghĩa |
|---|---|---|
| Risk-averse | $A > 0$ | Phạt phương sai (penalizes variance) |
| Risk-neutral | $A = 0$ | Chỉ quan tâm đến $E(R)$ |
| Risk-seeking | $A < 0$ | Ưa thích phương sai (rewards variance) |

## Indifference Curves

**Indifference curve** biểu diễn tất cả các tổ hợp $E(R)$-$\sigma$ mang lại cùng một mức utility $U$.

- Nhà đầu tư **risk-averse**: đường cong dốc lên, lồi (upward-sloping, convex)
- $A$ càng cao → đường càng dốc (cần nhiều return hơn cho mỗi đơn vị rủi ro)
- Đường càng cao (về phía tây-bắc) → utility càng cao
- Các đường không bao giờ cắt nhau với cùng một nhà đầu tư

## Portfolio Variance (Two Assets)

$$\sigma_p^2 = w_1^2 \sigma_1^2 + w_2^2 \sigma_2^2 + 2 w_1 w_2 \rho_{12} \sigma_1 \sigma_2$$

trong đó:
- $w_i$ = tỷ trọng của tài sản $i$
- $\sigma_i$ = độ lệch chuẩn của tài sản $i$
- $\rho_{12}$ = tương quan giữa tài sản 1 và 2 (correlation)

### Tác động của Correlation lên rủi ro danh mục

| $\rho_{12}$ | Tác động |
|---|---|
| $+1$ | Không có lợi ích đa dạng hóa; $\sigma_p$ là bình quân gia quyền |
| $0 < \rho < 1$ | Đa dạng hóa một phần |
| $0$ | Không tương quan; đa dạng hóa tốt |
| $-1$ | Có thể phòng ngừa hoàn toàn (perfect hedge); $\sigma_p$ có thể đạt về không |

## Covariance and Correlation

$$\text{Cov}_{12} = \frac{\sum (R_{1t} - \bar{R}_1)(R_{2t} - \bar{R}_2)}{n - 1}$$

$$\rho_{12} = \frac{\text{Cov}_{12}}{\sigma_1 \sigma_2}$$

trong đó $-1 \le \rho_{12} \le +1$.

## Capital Allocation Line (CAL)

CAL biểu diễn tất cả các tổ hợp giữa tài sản phi rủi ro và một danh mục rủi ro $i$:

$$E(R_p) = R_f + \left[\frac{E(R_i) - R_f}{\sigma_i}\right] \sigma_p$$

- Độ dốc = **Sharpe ratio** của danh mục rủi ro
- Giao điểm trục tung = $R_f$
- Nhà đầu tư chọn một điểm trên CAL dựa theo mức độ ngại rủi ro (risk aversion)

## Minimum-Variance Frontier

Tập hợp các danh mục có **phương sai thấp nhất** ứng với mỗi mức expected return, được tạo thành từ tất cả các tổ hợp tài sản rủi ro có thể.

- **Global minimum-variance portfolio (GMV)**: danh mục duy nhất có phương sai thấp nhất trong tất cả các tổ hợp tài sản rủi ro
- Frontier là một parabol trong không gian $E(R)$-$\sigma^2$ (hoặc một hyperbol trong không gian $E(R)$-$\sigma$)

## Efficient Frontier

**Phần phía trên** của minimum-variance frontier (từ GMV portfolio trở lên).

- Các nhà đầu tư hợp lý chỉ xem xét các danh mục nằm trên efficient frontier
- Mỗi danh mục hiệu quả tối đa hóa $E(R)$ với một mức $\sigma$ cho trước (hoặc tối thiểu hóa $\sigma$ với một mức $E(R)$ cho trước)

## Optimal Portfolio Selection

**Optimal risky portfolio** là điểm tiếp xúc (tangency point) nơi CAL tiếp tuyến với efficient frontier — đây là danh mục có **Sharpe ratio cao nhất**.

**Optimal complete portfolio** của nhà đầu tư là nơi indifference curve đạt được cao nhất tiếp tuyến với CAL:
- Ngại rủi ro hơn → điểm nằm gần $R_f$ hơn (cho vay nhiều hơn — more lending)
- Ít ngại rủi ro hơn → điểm nằm xa hơn trên CAL (vay mượn nhiều hơn — more borrowing)

## Diversification Ratio

$$\text{Diversification ratio} = \frac{\sigma(\text{equally-weighted portfolio})}{\sigma(\text{randomly selected security})}$$

Tỷ số càng thấp cho thấy lợi ích đa dạng hóa càng lớn.

## See Also

- [[portfolio-management/concepts/capm-and-sml|CAPM and SML]]
- [[portfolio-management/formulas/pm-formulas|PM Master Formula Sheet]]
- [[portfolio-management/glossary/pm-m01|Glossary M01]]