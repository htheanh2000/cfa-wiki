---
title: Risk Management
type: concept
subject: portfolio-management
module: "M06"
created: 2026-04-12
updated: 2026-04-12
tags: [risk-management, risk-governance, risk-tolerance, risk-budgeting, VaR]
---

# Risk Management

## Risk Management Framework

Một framework quản lý rủi ro toàn diện có **bảy yếu tố cốt lõi**:

1. **Governance** — giám sát cấp hội đồng quản trị, xác định cơ sở hạ tầng quản lý rủi ro
2. **Identification** — lập danh mục tất cả các rủi ro (tài chính và phi tài chính)
3. **Measurement** — định lượng các rủi ro (VaR, stress tests, scenario analysis)
4. **Management** — quyết định chấp nhận, giảm thiểu, chuyển giao, hoặc né tránh từng loại rủi ro
5. **Monitoring** — theo dõi liên tục các rủi ro và tuân thủ giới hạn đặt ra
6. **Communication** — báo cáo cho các bên liên quan (hội đồng quản trị, cơ quan quản lý, khách hàng)
7. **Strategic analysis / integration** — gắn kết quản lý rủi ro với chiến lược kinh doanh

## Risk Governance

- **Hội đồng quản trị (Board of directors)** chịu trách nhiệm tối cao trong việc giám sát rủi ro
- **Chief Risk Officer (CRO)** lãnh đạo bộ phận quản lý rủi ro
- **Enterprise risk management (ERM)** tích hợp rủi ro trên toàn tổ chức (không phân mảnh theo từng bộ phận)
- **Risk governance** bao gồm các chính sách, quy trình, và cơ chế trách nhiệm giải trình

### Cấu trúc Governance

| Cấp độ | Vai trò |
|---|---|
| Hội đồng quản trị | Xác định khẩu vị rủi ro, phê duyệt chính sách rủi ro |
| Ban lãnh đạo cấp cao / CRO | Triển khai framework rủi ro, thiết lập giới hạn |
| Ủy ban Rủi ro | Giám sát rủi ro tổng hợp |
| Các đơn vị kinh doanh | Hoạt động trong phạm vi giới hạn rủi ro |

## Risk Tolerance

Risk tolerance có hai thành phần:

### Ability to Bear Risk (Khách quan)

Được xác định bởi:
- Tình hình tài chính (tài sản, mức độ ổn định thu nhập)
- Thời gian đầu tư (dài hơn → khả năng chịu rủi ro cao hơn)
- Nhu cầu thanh khoản (nhu cầu thấp hơn → khả năng chịu rủi ro cao hơn)
- Mục tiêu đầu tư (thiết yếu so với kỳ vọng)

### Willingness to Take Risk (Chủ quan)

Được xác định bởi:
- Mức độ thoải mái về tâm lý trước sự bất định
- Kinh nghiệm trong quá khứ với các khoản lỗ
- Các yếu tố hành vi (loss aversion, overconfidence)

**Giải quyết mâu thuẫn**: Khi ability và willingness mâu thuẫn nhau, đánh giá **thận trọng hơn** thường được ưu tiên áp dụng, đồng thời cung cấp thêm thông tin để đưa willingness về phù hợp với ability.

## Risk Budgeting

Risk budgeting là quá trình **phân bổ tổng risk tolerance** cho các nguồn rủi ro khác nhau:

- **Các lớp tài sản (asset classes)**: mỗi phần phân bổ đóng góp bao nhiêu rủi ro
- **Active risk budget**: cho phép bao nhiêu tracking error so với benchmark
- **Factor exposures**: phân bổ theo từng nhân tố rủi ro (lãi suất, tín dụng, cổ phiếu, tiền tệ)

Khái niệm then chốt: **marginal contribution to risk** của mỗi vị thế phải tỷ lệ thuận với marginal contribution kỳ vọng của nó đối với lợi suất.

## Financial Risks

| Loại rủi ro | Mô tả |
|---|---|
| **Market risk** | Tổn thất do biến động bất lợi của giá thị trường (cổ phiếu, lãi suất, FX, hàng hóa) |
| **Credit risk** | Tổn thất do đối tác vỡ nợ hoặc chất lượng tín dụng suy giảm |
| **Liquidity risk** | Không thể giao dịch theo giá trị hợp lý hoặc không đáp ứng được nghĩa vụ đến hạn |

## Non-Financial Risks

| Loại rủi ro | Mô tả |
|---|---|
| **Operational risk** | Tổn thất từ quy trình, con người, hệ thống bị lỗi, hoặc các sự kiện bên ngoài |
| **Model risk** | Tổn thất do sai sót trong các mô hình định giá hoặc đo lường rủi ro |
| **Tail risk** | Tổn thất cực đoan vượt ngoài dự đoán của phân phối chuẩn |
| **Settlement risk** | Thất bại trong việc trao đổi tiền/chứng khoán vào thời điểm thanh toán (Herstatt risk) |
| **Regulatory risk** | Thay đổi bất lợi trong luật pháp hoặc quy định |
| **Legal / contract risk** | Tổn thất từ các hợp đồng không thể thực thi hoặc kiện tụng |
| **Political risk** | Hành động của chính phủ (tịch thu tài sản, trừng phạt, thay đổi chính sách) |
| **Accounting risk** | Sai lệch hoặc diễn giải sai báo cáo tài chính |
| **ESG / reputational risk** | Tổn thất từ các thất bại về môi trường, xã hội, hoặc quản trị |

## Risk Interactions

Các rủi ro không xảy ra độc lập:

- **Chained (cascading) risk**: một sự kiện rủi ro kéo theo sự kiện khác (ví dụ: thị trường sụp đổ → khủng hoảng thanh khoản → vỡ nợ tín dụng)
- **Adverse risk interaction**: các rủi ro khuếch đại lẫn nhau trong giai đoạn căng thẳng; tương quan tăng lên, đa dạng hóa thất bại đúng lúc cần nhất
- **Wrong-way risk**: mức độ rủi ro với một đối tác có tương quan âm với chất lượng tín dụng của chính đối tác đó

## Risk Measurement

| Phương pháp | Mô tả |
|---|---|
| **Standard deviation / variance** | Tổng rủi ro của lợi suất |
| **Beta** | Rủi ro hệ thống so với thị trường |
| **Value at Risk (VaR)** | Khoản lỗ tối đa kỳ vọng tại một mức độ tin cậy cho trước trong một khoảng thời gian xác định |
| **Conditional VaR (CVaR)** | Khoản lỗ kỳ vọng khi lỗ vượt quá VaR (expected shortfall) |
| **Stress testing** | Tác động của các kịch bản cực đoan nhưng có thể xảy ra |
| **Scenario analysis** | Tác động của các sự kiện giả định cụ thể hoặc lịch sử |
| **Sensitivity analysis** | Tác động của sự thay đổi một nhân tố rủi ro (giữ nguyên các yếu tố còn lại) |

### Ví dụ về VaR

"1-day 95% VaR là \$1 triệu" có nghĩa là: có xác suất 5% rằng danh mục sẽ lỗ hơn \$1 triệu trong một ngày.

**Hạn chế của VaR**:
- Không mô tả mức độ tổn thất vượt ra ngoài VaR
- Phụ thuộc vào các giả định (phân phối chuẩn, giai đoạn lịch sử)
- Có thể đánh giá thấp tail risk

## Risk Modification

| Phương pháp | Mô tả | Ví dụ |
|---|---|---|
| **Risk avoidance** | Không chấp nhận rủi ro | Tránh đầu tư vào lớp tài sản rủi ro cao |
| **Risk acceptance** | Giữ nguyên rủi ro (tự bảo hiểm) | Duy trì vị thế, chấp nhận khoản lỗ tiềm năng |
| **Risk transfer** | Chuyển giao rủi ro cho bên thứ ba | Bảo hiểm, phòng hộ bằng derivatives, chứng khoán hóa |
| **Risk mitigation / reduction** | Giảm xác suất hoặc mức độ tác động | Đa dạng hóa, giới hạn vị thế, tài sản thế chấp |

## See Also

- [[portfolio-management/concepts/portfolio-management-process|Portfolio Management Process]]
- [[portfolio-management/concepts/portfolio-risk-return|Portfolio Risk and Return]]
- [[portfolio-management/glossary/pm-m06|Glossary M06]]