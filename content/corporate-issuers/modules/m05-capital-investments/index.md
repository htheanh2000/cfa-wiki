---
title: "M05 — Capital Investments"
type: module
subject: corporate-issuers
module: M05
los: ["5.a", "5.b", "5.c", "5.d"]
created: 2026-04-10
updated: 2026-04-10
tags: [corporate-issuers, capital-budgeting, npv, irr, real-options]
---

# M05: Capital Investments and Capital Allocation

## Learning Outcomes
- **5.a**: Mô tả các loại hình đầu tư vốn (capital investments)
- **5.b**: Mô tả quy trình phân bổ vốn (capital allocation), tính toán NPV, IRR, và ROIC, và so sánh cách sử dụng chúng
- **5.c**: Mô tả các nguyên tắc của capital allocation và những sai lầm phổ biến
- **5.d**: Mô tả các loại real options liên quan đến capital investments

## Key Concepts

### Types of Capital Investments (LOS 5.a)
| Loại | Mô tả | Mức độ rủi ro |
|---|---|---|
| Going concern projects | Duy trì hoạt động hiện tại (thay thế thiết bị, bảo trì IT) | Thấp |
| Regulatory/compliance | Đáp ứng các tiêu chuẩn an toàn và quy định pháp lý | Thấp |
| Expansion projects | Mở rộng quy mô kinh doanh, sản phẩm/dịch vụ mới | Thấp đến trung bình |
| New lines of business | Đổi mới sáng tạo, ngành mới, khởi nghiệp | Cao |

### Capital Allocation Process (LOS 5.b)
1. **Tạo ý tưởng** (Idea generation)
2. **Phân tích đầu tư** (Investment analysis) — dự báo dòng tiền, đánh giá khả năng sinh lời
3. **Lập kế hoạch và ưu tiên** (Planning and prioritization) — xếp hạng dự án, phân bổ nguồn lực
4. **Giám sát và đánh giá sau đầu tư** (Monitoring and post-investment review) — so sánh thực tế với kế hoạch

### Important Capital Budgeting Concepts
- **Sunk cost**: Chi phí đã phát sinh, không thể tránh khỏi → loại trừ khỏi phân tích
- **Opportunity cost**: Giá trị của phương án tốt nhất bị bỏ qua → đưa vào phân tích
- **Incremental cash flow**: Dòng tiền khi có dự án trừ dòng tiền khi không có dự án
- **Externality**: Tác động đến các bộ phận khác của công ty (tích cực hoặc tiêu cực)
- **Cannibalization**: Đầu tư mới lấy đi doanh số của sản phẩm hiện có (negative externality)
- **Conventional cash flows**: Một lần đổi dấu (dòng tiền ra ban đầu, sau đó là dòng tiền vào)
- **Non-conventional**: Nhiều lần đổi dấu → có thể có nhiều IRR
- **Independent projects**: Chấp nhận tất cả dự án có NPV dương
- **Mutually exclusive**: Chọn dự án có NPV cao nhất

### Net Present Value (NPV)
$$NPV = CF_0 + \frac{CF_1}{(1+r)^1} + \frac{CF_2}{(1+r)^2} + \cdots + \frac{CF_n}{(1+r)^n} = \sum_{t=0}^{n} \frac{CF_t}{(1+r)^t}$$

trong đó $CF_0$ = chi phí đầu tư ban đầu (âm), $CF_t$ = dòng tiền sau thuế tại thời điểm $t$, $r$ = tỷ suất sinh lời yêu cầu

**Quy tắc quyết định**: $NPV \geq 0$ → đầu tư; $NPV < 0$ → không đầu tư

### Internal Rate of Return (IRR)
Tỷ lệ chiết khấu làm cho $NPV = 0$:
$$0 = \sum_{t=0}^{n} \frac{CF_t}{(1+IRR)^t}$$

**Quy tắc quyết định**: $IRR \geq r$ → đầu tư; $IRR < r$ → không đầu tư

**Hạn chế**: Có nhiều IRR với non-conventional cash flows; có thể mâu thuẫn với NPV đối với mutually exclusive projects

### Return on Invested Capital (ROIC)
$$ROIC = \frac{\text{After-tax operating profit}}{\text{Average book value of invested capital}}$$

### NPV vs. IRR
- Với **independent** projects: NPV và IRR cho cùng kết quả chấp nhận/từ chối
- Với **mutually exclusive** projects: Sử dụng NPV (đo lường trực tiếp giá trị tạo ra)
- NPV giả định tái đầu tư tại tỷ suất yêu cầu; IRR giả định tái đầu tư tại chính IRR

### Principles of Capital Allocation (LOS 5.c)
- Quyết định dựa trên incremental cash flows sau thuế
- Dòng tiền được tính dựa trên opportunity costs
- Thời điểm của dòng tiền có vai trò quan trọng
- Dòng tiền được phân tích trên cơ sở sau thuế
- Chi phí tài trợ được phản ánh trong tỷ lệ chiết khấu

### Common Pitfalls
- Không tính đến phản ứng của thị trường (đối thủ cạnh tranh phản ứng)
- Lạm dụng các mẫu phân tích chuẩn hóa
- Dự án được ưu tiên theo ý kiến chủ quan của ban lãnh đạo cấp cao
- Ra quyết định dựa trên EPS hoặc lợi nhuận ròng thay vì dòng tiền
- Không xử lý đúng sunk costs hoặc opportunity costs

### Real Options (LOS 5.d)
| Loại | Mô tả |
|---|---|
| Timing option | Trì hoãn đầu tư để thu thập thêm thông tin |
| Sizing option | Mở rộng hoặc từ bỏ dự án dựa trên kết quả thực tế |
| Flexibility option | Thay đổi đầu vào, đầu ra hoặc quy trình |
| Fundamental options | Các quyết định cơ bản của dự án (định giá, công nghệ) |

Real options làm tăng giá trị → $NPV_{\text{adjusted}} = NPV_{\text{base}} + \text{Value of real options}$

## Related Pages
- [[corporate-issuers/concepts/capital-allocation|Capital Investments and Allocation]]
- [[corporate-issuers/formulas/corporate-finance|Corporate Finance Formulas]]
- [[corporate-issuers/glossary/ci-m05-capital-investments|Glossary: M05]]