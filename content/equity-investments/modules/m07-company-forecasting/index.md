---
title: "M07 — Equity Valuation"
type: module
subject: equity-investments
module: M07
los: ["7.a", "7.b", "7.c"]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, forecasting, revenue-forecast, cost-forecast, capital-requirements]
---

# Module 07: Company Analysis — Forecasting

## Tổng quan

Module này đề cập đến việc dự báo tài chính doanh nghiệp, bao gồm doanh thu, chi phí hoạt động và nhu cầu vốn. Đồng thời xem xét ảnh hưởng của cạnh tranh và công nghệ đến các giả định trong dự báo.

**Nguồn**: [[equity-investments/sources/sapp-equity-2026|SAPP CFA1 Equity Investments Slide 2026]] — Trang 268–317

---

## Phạm vi LOS

### LOS 7.a: Phương pháp dự báo — Top-Down vs Bottom-Up

#### Top-Down Forecasting
1. Bắt đầu từ **dự báo kinh tế vĩ mô** (tăng trưởng GDP, lạm phát, lãi suất)
2. Ước tính **tăng trưởng ngành** dựa trên triển vọng vĩ mô
3. Ước tính **thị phần của công ty** trong ngành
4. Suy ra **doanh thu công ty** = Doanh thu ngành $\times$ Thị phần

$$\text{Revenue}_{\text{company}} = \text{GDP Growth} \times \text{Industry Sensitivity} \times \text{Market Share}$$

**Ưu điểm**: Nắm bắt được xu hướng vĩ mô, nhất quán giữa các công ty trong cùng ngành
**Hạn chế**: Có thể bỏ qua các yếu tố đặc thù của công ty, giả định thị phần ổn định

#### Bottom-Up Forecasting
1. Bắt đầu từ **từng dòng sản phẩm** hoặc phân khúc kinh doanh riêng lẻ
2. Dự báo **sản lượng và giá bán** cho từng phân khúc
3. Tổng hợp lên thành doanh thu toàn công ty

$$\text{Revenue}_{\text{company}} = \sum_{i=1}^{n} (Q_i \times P_i)$$

trong đó $Q_i$ = sản lượng tiêu thụ của phân khúc $i$, $P_i$ = giá bán bình quân của phân khúc $i$.

**Ưu điểm**: Chi tiết, phản ánh được động lực riêng của từng phân khúc
**Hạn chế**: Đòi hỏi nhiều dữ liệu, có thể bỏ qua các yếu tố thuận lợi/bất lợi vĩ mô

#### Phương pháp kết hợp (Hybrid Approach)
Hầu hết các nhà phân tích sử dụng **kết hợp cả hai** — top-down để kiểm tra tính hợp lý tổng thể, bottom-up để đi vào chi tiết.

---

### LOS 7.b: Dự báo Doanh thu, Chi phí hoạt động và Nhu cầu Vốn

#### Dự báo Doanh thu (Revenue Forecasting)

Các đầu vào chính:
- **Tốc độ tăng trưởng lịch sử** — Phân tích xu hướng
- **Hướng dẫn từ ban lãnh đạo** — Các phát biểu định hướng tương lai
- **Tốc độ tăng trưởng ngành** — Từ phân tích ngành ([[equity-investments/modules/m06-industry-analysis/index|M06]])
- **Sản phẩm/thị trường mới** — Tiềm năng mở rộng
- **Xu hướng giá** — Lạm phát, áp lực cạnh tranh

Các phương pháp phổ biến:
1. **Dự báo theo tốc độ tăng trưởng** — Áp dụng tốc độ tăng trưởng lịch sử hoặc kỳ vọng
2. **Xây dựng từng phân khúc** — Dự báo độc lập cho từng phân khúc
3. **Phân tích hồi quy** — Doanh thu là hàm số của các biến kinh tế

#### Dự báo Chi phí hoạt động (Operating Cost Forecasting)

| Loại chi phí | Phương pháp dự báo |
|-----------|-------------------|
| **COGS** | Tính theo % doanh thu (giả định gross margin) hoặc chi phí trên đơn vị $\times$ sản lượng |
| **SGA** | Thành phần cố định + thành phần biến đổi (% doanh thu) |
| **R&D** | Tính theo % doanh thu hoặc số tuyệt đối dựa trên chiến lược công ty |
| **D&A** | Dựa trên cơ sở tài sản hiện có + CapEx mới, theo lịch khấu hao |

**Operating leverage** — Chi phí cố định cao làm khuếch đại biến động lợi nhuận:

$$\text{DOL} = \frac{\%\Delta \text{Operating Income}}{\%\Delta \text{Revenue}}$$

trong đó $\text{DOL}$ = Degree of Operating Leverage (đòn bẩy hoạt động).

#### Dự báo Nhu cầu Vốn (Capital Requirements Forecasting)

**Capital Expenditures (CapEx)**:
- **Maintenance CapEx** $\approx$ Khấu hao (để duy trì công suất hiện tại)
- **Growth CapEx** — Đầu tư thêm cho mục đích mở rộng
- Dự báo theo % doanh thu hoặc dựa trên các dự án đã công bố

**Nhu cầu Vốn lưu động (Working Capital Requirements)**:

$$\Delta \text{Working Capital} = \Delta \text{Current Assets} - \Delta \text{Current Liabilities}$$

- Các công ty tăng trưởng thường đòi hỏi vốn lưu động **ngày càng tăng**
- Dự báo sử dụng các tỷ số lịch sử (DSO, DIO, DPO) áp dụng lên doanh thu/COGS dự kiến

**Cơ cấu vốn (Capital Structure)**:
- Dự báo mức nợ dựa trên tỷ lệ đòn bẩy mục tiêu
- Xem xét lịch đáo hạn nợ và nhu cầu tái cấp vốn

---

### LOS 7.c: Ảnh hưởng của Cạnh tranh và Công nghệ đến Dự báo

#### Ảnh hưởng của Cạnh tranh

| Yếu tố cạnh tranh | Tác động lên dự báo |
|-------------------|---------------------|
| **Đối thủ mới gia nhập (New entrants)** | Tạo áp lực lên thị phần và biên lợi nhuận |
| **Cạnh tranh về giá (Price competition)** | Tăng trưởng doanh thu thấp hơn, biên lợi nhuận bị thu hẹp |
| **Hợp nhất ngành (Industry consolidation)** | Có thể cải thiện quyền định giá cho các công ty còn lại |
| **Sản phẩm thay thế (Substitute products)** | Suy giảm cầu, cần đổi mới sáng tạo |
| **Thay đổi quy định (Regulatory changes)** | Có thể tạo ra hoặc phá hủy lợi thế cạnh tranh |

#### Ảnh hưởng của Công nghệ

| Yếu tố công nghệ | Tác động lên dự báo |
|-------------------|---------------------|
| **Công nghệ đột phá (Disruption)** | Có thể nhanh chóng làm lỗi thời các mô hình kinh doanh |
| **Tự động hóa (Automation)** | Có thể giảm chi phí hoạt động nhưng đòi hỏi CapEx ban đầu |
| **Chuyển đổi số (Digital transformation)** | Thay đổi mô hình doanh thu (ví dụ: thuê bao thay vì mua một lần) |
| **Hiệu ứng mạng lưới (Network effects)** | Động lực "người thắng lấy tất", tăng trưởng phi tuyến |
| **Chu kỳ sản phẩm rút ngắn** | Tăng yêu cầu R&D, giảm quyền định giá |

#### Điều chỉnh Dự báo

Các nhà phân tích cần:
1. **Phân tích kịch bản (Scenario analysis)** — Kịch bản cơ sở, lạc quan và bi quan phản ánh rủi ro cạnh tranh/công nghệ
2. **Phân tích độ nhạy (Sensitivity analysis)** — Tác động của các yếu tố then chốt lên định giá
3. **Biên an toàn (Margin of safety)** — Chiết khấu cho sự không chắc chắn trong dự báo
4. **Theo dõi các chỉ số dẫn đầu (Leading indicators)** — Tốc độ áp dụng công nghệ, đăng ký bằng sáng chế, hành động của đối thủ

> Dự báo càng xa trong tương lai, sự không chắc chắn từ cạnh tranh và công nghệ càng tích lũy và khuếch đại.

---

## Điểm mấu chốt

1. Top-down forecasting bắt đầu từ vĩ mô; bottom-up xây dựng từ chi tiết phân khúc; phương pháp kết hợp là thực hành tốt nhất
2. Revenue forecasting kết hợp tốc độ tăng trưởng, phân tích phân khúc và bối cảnh ngành
3. Chi phí hoạt động được dự báo sử dụng các giả định về biên lợi nhuận và phân tích chi phí cố định/biến đổi
4. Nhu cầu vốn bao gồm CapEx (maintenance + growth) và thay đổi vốn lưu động
5. Cạnh tranh và công nghệ tạo ra sự không chắc chắn cần được phản ánh trong các giả định và phân tích kịch bản

---

## Các trang liên quan

- [[equity-investments/modules/m05-company-analysis-past/index|M05: Company Analysis — Past and Present]]
- [[equity-investments/modules/m06-industry-analysis/index|M06: Industry and Competitive Analysis]]
- [[equity-investments/modules/m08-equity-valuation/index|M08: Equity Valuation]]
- [[equity-investments/glossary/equity-m07-glossary|Glossary: M07]]
- [[equity-investments/formulas/equity-formulas|Equity Formulas]]