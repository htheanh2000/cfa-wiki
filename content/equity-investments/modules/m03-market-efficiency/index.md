---
title: "M03 — Market Efficiency"
type: module
subject: equity-investments
module: m03
los: [3.a, 3.b, 3.c, 3.d, 3.e, 3.f, 3.g]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, m03, market-efficiency, emh, behavioral-finance]
---

# M03: Market Efficiency

**Nguồn**: [[equity-investments/sources/sapp-equity-2026|SAPP Slide 2026]], trang 97–124
**LOS**: 3.a–3.g

---

## LOS 3.a — Informationally Efficient Market

Một **informationally efficient market** là thị trường trong đó giá tài sản **phản ánh đầy đủ, nhanh chóng và hợp lý** tất cả thông tin hiện có.

Hệ quả quan trọng:
- Giá điều chỉnh **nhanh chóng** theo thông tin mới
- Nhà đầu tư không thể kiếm **abnormal returns** (lợi nhuận vượt trội so với benchmark đã điều chỉnh rủi ro) một cách nhất quán
- Biến động giá là **không thể dự đoán** — tuân theo random walk

> Trong một thị trường hiệu quả, **active management** không thể liên tục đánh bại thị trường sau khi trừ chi phí.

---

## LOS 3.b — Market Value vs Intrinsic Value

| Khái niệm | Định nghĩa |
|-----------|-----------|
| **Market value** | Giá hiện tại mà tài sản đang được giao dịch trên thị trường |
| **Intrinsic value** | Giá trị "thực" hay giá trị cơ bản dựa trên toàn bộ thông tin liên quan và phương pháp định giá phù hợp |

- Trong thị trường hoàn toàn hiệu quả: $\text{Market value} = \text{Intrinsic value}$
- Các nhà quản lý chủ động (active managers) tin rằng: $\text{Market value} \neq \text{Intrinsic value}$ (ít nhất là trong ngắn hạn)
- Lợi nhuận từ giao dịch phụ thuộc vào:
  1. **Khoảng chênh lệch** giữa market value và intrinsic value ước tính
  2. Ước tính của nhà đầu tư phải **chính xác**
  3. Khoảng chênh lệch phải **thu hẹp lại** trong thời hạn đầu tư

---

## LOS 3.c — Factors Contributing to / Impeding Market Efficiency

### Các yếu tố THÚC ĐẨY hiệu quả thị trường:
- **Số lượng lớn người tham gia thị trường** — quan điểm đa dạng, phân tích nhiều hơn
- **Thông tin phổ biến rộng rãi** — chi phí thấp, phân phối kịp thời
- **Ít rào cản giao dịch** — dễ dàng long hoặc short
- **Chi phí giao dịch thấp** — có lợi nhuận khi hành động trên những mispricings nhỏ

### Các yếu tố CẢN TRỞ hiệu quả thị trường:
- **Ít người tham gia thị trường** — thị trường mỏng, ít phân tích
- **Thông tin bị hạn chế** — thông tin tốn kém hoặc bị trễ
- **Giới hạn giao dịch** — hạn chế short-selling, kiểm soát vốn
- **Chi phí giao dịch cao** — mispricings tồn tại dai dẳng vì việc điều chỉnh không mang lại lợi nhuận

---

## LOS 3.d — Fama's Three Forms of Market Efficiency

### Efficient Market Hypothesis (EMH) — Eugene Fama (1970)

| Dạng | Thông tin phản ánh trong giá | Hàm ý |
|------|------------------------------|-------|
| **Weak form** | Tất cả **dữ liệu thị trường trong quá khứ** (giá, khối lượng, dữ liệu giao dịch) | Technical analysis không thể kiếm abnormal returns |
| **Semi-strong form** | Tất cả **thông tin công khai** (báo cáo tài chính, tin tức, báo cáo phân tích) | Cả technical analysis lẫn fundamental analysis đều không thể kiếm abnormal returns |
| **Strong form** | **Tất cả thông tin** — công khai VÀ riêng tư (insider) | Ngay cả insiders cũng không thể kiếm abnormal returns |

### Phân cấp
- Strong $\supset$ Semi-strong $\supset$ Weak
- Nếu semi-strong form đúng, weak form cũng đúng
- Nếu strong form đúng, cả semi-strong form và weak form đều đúng

### Bằng chứng thực nghiệm
- **Weak form**: Được hỗ trợ phần lớn — kiểm định tương quan chuỗi (serial correlation tests), filter rules
- **Semi-strong form**: Được hỗ trợ đáng kể — event studies (giá điều chỉnh nhanh chóng)
- **Strong form**: Nhìn chung KHÔNG được hỗ trợ — insiders thực sự kiếm được abnormal returns

---

## LOS 3.e — Implications for Investment Strategies

| Dạng EMH | Technical Analysis | Fundamental Analysis | Active Management | Passive Management |
|----------|--------------------|---------------------|-------------------|-------------------|
| **Weak** | Vô dụng | Có thể tạo giá trị | Có thể tạo giá trị | Phù hợp |
| **Semi-strong** | Vô dụng | Vô dụng | Vô dụng (sau chi phí) | Phù hợp |
| **Strong** | Vô dụng | Vô dụng | Vô dụng | Phù hợp |

> Nếu thị trường hiệu quả ở dạng semi-strong, nhà đầu tư nên sử dụng **passive (index) investing** vì chi phí active management (phí, giao dịch) không thể bù đắp bằng khả năng phân tích vượt trội.

---

## LOS 3.f — Market Anomalies

Market anomalies là các mẫu hình dường như mâu thuẫn với EMH. Chúng có thể đại diện cho:
- Sự kém hiệu quả thực sự của thị trường, HOẶC
- Lỗi đo lường, data mining, hoặc các yếu tố rủi ro chưa được mô hình nắm bắt

### Time-Series Anomalies

| Anomaly | Mô tả |
|---------|-------|
| **Calendar effects (January effect)** | Cổ phiếu vốn hóa nhỏ (small-cap) có xu hướng vượt trội trong tháng 1 (do bán lỗ để khấu trừ thuế vào tháng 12, rồi mua lại vào tháng 1) |
| **Momentum effect** | Chứng khoán có hiệu suất tốt (kém) trong quá khứ gần đây tiếp tục có hiệu suất tốt (kém) trong 3–12 tháng tiếp theo |
| **Overreaction effect** | Chứng khoán có hiệu suất tốt (kém) trong 3–5 năm có xu hướng đảo chiều (tạo ra lợi nhuận contrarian) |

### Cross-Sectional Anomalies

| Anomaly | Mô tả |
|---------|-------|
| **Size effect** | Cổ phiếu small-cap có xu hướng vượt trội so với cổ phiếu large-cap trên cơ sở đã điều chỉnh rủi ro |
| **Value effect** | Cổ phiếu có P/E thấp, P/B thấp, hoặc dividend yield cao có xu hướng vượt trội so với growth stocks |

### Các Anomalies Khác

| Anomaly | Mô tả |
|---------|-------|
| **Closed-end fund discount** | Closed-end funds thường giao dịch ở mức chiết khấu so với NAV |
| **Earnings surprise (PEAD)** | Post-earnings-announcement drift — giá tiếp tục trôi dạt theo hướng của earnings surprise sau khi công bố |
| **IPO underperformance** | IPOs có xu hướng kém hiệu suất trong dài hạn (3–5 năm) mặc dù có underpricing ban đầu |

---

## LOS 3.g — Behavioral Finance

Behavioral finance nghiên cứu cách **các thiên kiến tâm lý (psychological biases)** ảnh hưởng đến hành vi nhà đầu tư và giá thị trường.

### Các Behavioral Biases Chính

| Bias | Mô tả |
|------|-------|
| **Loss aversion** | Nỗi đau từ thua lỗ lớn hơn niềm vui từ lợi nhuận tương đương — nhà đầu tư giữ cổ phiếu thua lỗ quá lâu, bán cổ phiếu thắng quá sớm |
| **Overconfidence** | Nhà đầu tư đánh giá quá cao khả năng dự đoán của mình — giao dịch quá thường xuyên, đầu tư thiếu đa dạng hóa |
| **Herding** | Đi theo đám đông thay vì phân tích độc lập — khuếch đại xu hướng, tạo ra bong bóng |
| **Information cascades** | Bỏ qua thông tin của bản thân và hành động dựa trên hành vi quan sát được của người khác |
| **Narrow framing (mental accounting)** | Đánh giá các khoản đầu tư riêng lẻ thay vì xét chúng như một phần của toàn bộ danh mục |
| **Representativeness** | Đánh giá xác suất dựa trên sự giống nhau với một khuôn mẫu — ngoại suy các xu hướng gần đây |
| **Anchoring** | Quá phụ thuộc vào một thông tin ban đầu (ví dụ: mức giá cao nhất 52 tuần) |
| **Availability bias** | Đánh giá quá cao thông tin dễ nhớ lại (sự kiện gần đây, tin tức gây chú ý) |

### Hàm ý
- Behavioral biases có thể gây ra **mispricings dai dẳng** ngay cả khi có nhiều người tham gia thị trường
- Thị trường có thể không hoàn toàn hiệu quả do **hành vi phi lý trí** mang tính hệ thống (không ngẫu nhiên)
- Thách thức giả định của EMH rằng các sai lầm là ngẫu nhiên và tự triệt tiêu lẫn nhau