---
title: "M11 — Big Data"
type: module
subject: quantitative-methods
module: M11
los: ["11.a", "11.b", "11.c"]
created: 2026-04-09
updated: 2026-04-09
tags: [fintech, big-data, ai, machine-learning, nlp, text-analytics]
---

# Module 11: Introduction to Big Data Techniques

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 452–470

## Learning Outcomes

| LOS | Mô tả |
|-----|-------------|
| 11.a | Các khía cạnh của "fintech" liên quan đến thu thập và phân tích dữ liệu tài chính |
| 11.b | Big Data, artificial intelligence và machine learning |
| 11.c | Ứng dụng của Big Data và Data Science trong quản lý đầu tư |

## LOS 11.a — Fintech

**Định nghĩa**: Đổi mới trong dịch vụ và sản phẩm tài chính được thúc đẩy bởi công nghệ.

**Các lĩnh vực liên quan đến tài chính:**
- **Phân tích tập dữ liệu lớn** — xử lý dữ liệu khổng lồ từ nhiều nguồn khác nhau
- **Công cụ phân tích** — AI và ML để phân tích các tập dữ liệu phi tuyến tính hoặc rất lớn

## LOS 11.b — Big Data, AI, và ML

### Big Data

**Nguồn dữ liệu:**

| Truyền thống | Phi truyền thống (Alternative) |
|---|---|
| Thị trường tài chính (giá, khối lượng) | Mạng xã hội, đánh giá, lượt truy cập website |
| Dữ liệu doanh nghiệp (hồ sơ nộp, thu nhập) | Corporate exhaust (hồ sơ ngân hàng, dữ liệu máy quét) |
| Thống kê kinh tế chính phủ | Cảm biến IoT |

**3 V's của Big Data:**

| Đặc điểm | Mô tả |
|---|---|
| **Volume** | Hàng triệu hoặc hàng tỷ điểm dữ liệu (MB → PB) |
| **Velocity** | Tốc độ dữ liệu theo thời gian thực hoặc gần thời gian thực |
| **Variety** | Định dạng có cấu trúc, bán cấu trúc và phi cấu trúc |

**Data Processing Pipeline:** Capture → Curation → Storage → Search → Transfer

**Thách thức trong phân tích đầu tư:**
- Vấn đề chất lượng (selection bias, dữ liệu thiếu, outliers)
- Khối lượng dữ liệu có thể không đủ
- Dữ liệu phi cấu trúc khó làm sạch và tổ chức
- Các phương pháp truyền thống có thể không phù hợp

### Artificial Intelligence

Các hệ thống AI mô phỏng nhận thức của con người và có khả năng ra quyết định.

| Neural Networks | Machine Learning |
|---|---|
| Được lập trình để xử lý thông tin như não người | Trích xuất kiến thức từ dữ liệu **mà không cần lập trình tường minh** |

### Machine Learning

**Cách hoạt động:**
1. **Training dataset** — học các mối quan hệ giữa đầu vào/đầu ra
2. **Validation dataset** — tinh chỉnh mô hình
3. **Testing dataset** — đánh giá trên dữ liệu chưa thấy
4. Triển khai mô hình thành công trên dữ liệu mới

**Các loại:**

| Loại | Mô tả | Ví dụ |
|---|---|---|
| **Supervised** | Dữ liệu huấn luyện có nhãn → dự đoán kết quả | Dự báo lợi suất cổ phiếu |
| **Unsupervised** | Dữ liệu không có nhãn → khám phá cấu trúc | Phân nhóm các công ty thành các cụm tương đồng |
| **Deep Learning** | Neural networks với nhiều hidden layers | Nhận dạng hình ảnh, nhận dạng giọng nói |

**Thách thức:**

| Thách thức | Mô tả |
|---|---|
| **Overfitting** | Mô hình học cả nhiễu → dự đoán kém trên dữ liệu mới (quá phức tạp) |
| **Underfitting** | Mô hình quá đơn giản → bỏ qua các mẫu thực sự |
| **Black box** | Kết quả không thể giải thích hoặc diễn giải đầy đủ |

## LOS 11.c — Ứng dụng trong Đầu tư

| Ứng dụng | Định nghĩa | Trường hợp sử dụng |
|---|---|---|
| **Text Analytics** | Phân tích dữ liệu văn bản/giọng nói phi cấu trúc | Đánh giá hồ sơ nộp, cuộc gọi thu nhập, mạng xã hội, khảo sát |
| **NLP (Natural Language Processing)** | Các chương trình AI phân tích và diễn giải ngôn ngữ con người | Dịch thuật, text mining, phân tích cảm xúc, nhận dạng giọng nói |

## Connections

- Xây dựng trên: [[quantitative-methods/concepts/data-types|Data Types]] (structured vs unstructured từ M03)
- Liên quan: Tất cả các phương pháp định lượng — các kỹ thuật Big Data bổ sung và mở rộng quy mô phân tích thống kê truyền thống
- Đặc trưng trong chương trình 2026: phản ánh tầm quan trọng ngày càng tăng của ML/AI trong thực hành CFA