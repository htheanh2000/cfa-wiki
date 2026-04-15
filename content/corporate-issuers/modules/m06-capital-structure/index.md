---
title: "M06 — Capital Structure"
type: module
subject: corporate-issuers
module: M06
los: ["6.a", "6.b", "6.c", "6.d"]
created: 2026-04-10
updated: 2026-04-10
tags: [corporate-issuers, capital-structure, wacc, modigliani-miller, cost-of-capital]
---

# M06: Capital Structure

## Learning Outcomes
- **6.a**: Tính toán và diễn giải weighted-average cost of capital (WACC) của một công ty
- **6.b**: Giải thích các yếu tố ảnh hưởng đến capital structure và WACC
- **6.c**: Giải thích các mệnh đề Modigliani-Miller liên quan đến capital structure
- **6.d**: Mô tả optimal và target capital structures

## Key Concepts

### Weighted Average Cost of Capital (WACC)
$$WACC = w_d \times r_d \times (1-t) + w_e \times r_e + w_p \times r_p$$

trong đó:
- $w_d, w_e, w_p$ = tỷ trọng mục tiêu của debt, equity, preferred stock
- $r_d$ = chi phí nợ cận biên trước thuế (before-tax marginal cost of debt)
- $t$ = thuế suất cận biên (marginal tax rate)
- $r_e$ = chi phí vốn cổ phần cận biên (marginal cost of equity)
- $r_p$ = chi phí cổ phiếu ưu đãi cận biên (marginal cost of preferred stock)
- Sử dụng **target** capital structure, không dùng cơ cấu hiện tại

### After-Tax Cost of Debt
$$r_d(1-t) = \text{after-tax cost of debt}$$

Chi phí lãi vay được khấu trừ thuế → tạo ra **tax shield** = $r_d \times t$

### Cost of Debt Estimation
- **YTM approach**: Giải tìm lợi suất sao cho giá trái phiếu bằng PV của các khoản thanh toán
- **Debt-rating approach**: Dùng lợi suất của trái phiếu có hệ số tín nhiệm tương đương (khi không có giá thị trường)

### Cost of Equity Estimation
**CAPM**:
$$r_e = R_F + \beta_i[E(R_M) - R_F]$$

trong đó $R_F$ = lãi suất phi rủi ro (risk-free rate), $\beta_i$ = equity beta, $E(R_M) - R_F$ = market risk premium

**Bond Yield Plus Risk Premium (BYPRP)**:
$$r_e = r_d + \text{Risk premium}$$

### Factors Affecting Capital Structure (LOS 6.b)
- Business risk (mức độ biến động doanh thu/lợi nhuận)
- Bản chất tài sản (tài sản hữu hình → khả năng vay nợ cao hơn)
- Các cân nhắc về thuế (lợi ích tax shield từ nợ)
- Nhu cầu linh hoạt tài chính (financial flexibility)
- Chuẩn mực ngành (industry norms)

### Modigliani-Miller Propositions (LOS 6.c)

**MM không có thuế (thị trường hoàn hảo)**:
- **Proposition I**: Capital structure không liên quan — $V_L = V_U$
- **Proposition II**: Cost of equity tăng tuyến tính theo đòn bẩy: $r_e = r_0 + (r_0 - r_d) \times \frac{D}{E}$
- WACC không đổi bất kể mức độ đòn bẩy

**MM có thuế**:
- **Proposition I**: $V_L = V_U + t \times D$ (giá trị tăng theo nợ nhờ tax shield)
- **Proposition II**: $r_e = r_0 + (r_0 - r_d)(1-t) \times \frac{D}{E}$
- WACC giảm khi tăng nợ (đến một mức nhất định)
- Ngụ ý 100% nợ là tối ưu — nhưng điều này bỏ qua chi phí kiệt quệ tài chính (costs of financial distress)

### Optimal and Target Capital Structure (LOS 6.d)
- **Static trade-off theory**: Cân bằng giữa lợi ích tax shield và chi phí kiệt quệ tài chính → đòn bẩy tối ưu
- **Pecking order theory**: Doanh nghiệp ưu tiên nguồn tài trợ nội bộ > nợ > vốn cổ phần (dựa trên information asymmetry)
- **Target capital structure**: Cơ cấu nợ và vốn cổ phần mà ban quản lý lựa chọn

## Related Pages
- [[corporate-issuers/concepts/capital-structure|Capital Structure and WACC]]
- [[corporate-issuers/formulas/corporate-finance|Corporate Finance Formulas]]
- [[corporate-issuers/glossary/ci-m06-capital-structure|Glossary: M06]]