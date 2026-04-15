---
title: "Big Data and Machine Learning"
type: concept
subject: quantitative-methods
module: M11
created: 2026-04-09
updated: 2026-04-09
tags: [big-data, machine-learning, fintech, NLP, alternative-data, overfitting]
---

# Big Data and Machine Learning

## Tổng quan

Sự tăng trưởng nhanh chóng của dữ liệu và sức mạnh tính toán đã tạo ra những cơ hội và thách thức mới cho phân tích đầu tư. [[quantitative-methods/glossary/m11-big-data-techniques#Fintech|Fintech]] đã thay đổi cách thức cung cấp dịch vụ tài chính, và [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|big data]] kết hợp với [[quantitative-methods/glossary/m11-big-data-techniques#Machine Learning (ML)|machine learning]] đã mở rộng bộ công cụ phân tích cho các nhà đầu tư. Chương trình CFA tập trung vào việc hiểu các công nghệ này là gì, cách chúng hoạt động ở mức độ tổng quát, cũng như các cân nhắc thực tiễn và đạo đức liên quan đến các chuyên gia đầu tư.

## Big Data: 4 Vs

**[[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big data]]** được đặc trưng bởi các thuộc tính phân biệt nó với dữ liệu truyền thống:

- **[[quantitative-methods/glossary/m11-big-data-techniques#Volume|Volume]]**: Các tập dữ liệu quá lớn so với khả năng của cơ sở dữ liệu truyền thống. Thị trường tài chính tạo ra hàng tỷ quan sát ở cấp độ tick mỗi ngày; thương mại điện tử, cảm biến IoT và mạng xã hội liên tục sản sinh ra hàng petabyte dữ liệu.
- **[[quantitative-methods/glossary/m11-big-data-techniques#Velocity|Velocity]]**: Dữ liệu đến và cần được xử lý trong thời gian thực hoặc gần thực. Giao dịch tần suất cao khai thác dữ liệu giá ở cấp độ mili giây; luồng giao dịch thẻ tín dụng cập nhật liên tục.
- **[[quantitative-methods/glossary/m11-big-data-techniques#Variety|Variety]]**: Dữ liệu tồn tại ở nhiều dạng — [[quantitative-methods/glossary/m03-statistical-measures#Structured Data|structured]] (cơ sở dữ liệu, bảng tính), [[quantitative-methods/glossary/m03-statistical-measures#Unstructured Data|unstructured]] (văn bản, hình ảnh, âm thanh, video), và semi-structured (JSON, XML). Phân tích tài chính truyền thống gần như chỉ dựa vào dữ liệu có cấu trúc.
- **[[quantitative-methods/glossary/m11-big-data-techniques#Veracity|Veracity]]**: Big data thường nhiễu, không đầy đủ và có thể chứa sai sót. Kiểm soát chất lượng và làm sạch dữ liệu là các bước quan trọng trước khi phân tích.

**[[quantitative-methods/glossary/m11-big-data-techniques#Traditional Data|Traditional data]]** (báo cáo tài chính, giá thị trường, các công bố kinh tế) có cấu trúc, định kỳ và được hiểu rõ. **[[quantitative-methods/glossary/m11-big-data-techniques#Alternative Data|Alternative data]]** — hình ảnh vệ tinh về bãi đậu xe của các trung tâm mua sắm, chi tiêu thẻ tín dụng theo danh mục người bán, tin tuyển dụng được thu thập từ web, theo dõi container vận chuyển — có thể tiết lộ thông tin về hiệu suất công ty trước khi chúng xuất hiện trong các báo cáo chính thức. Alternative data là nguồn lợi thế cạnh tranh cho các nhà quản lý đầu tư, nhưng cũng đặt ra những thách thức mới về chất lượng dữ liệu, pháp lý và đạo đức.

## Machine Learning: Phân loại

**[[quantitative-methods/glossary/m11-big-data-techniques#Machine Learning (ML)|Machine learning]]** cho phép hệ thống học các mẫu từ dữ liệu mà không cần lập trình quy tắc tường minh. Ba mô hình chính liên quan đến thí sinh CFA:

**[[quantitative-methods/glossary/m11-big-data-techniques#Supervised Learning|Supervised learning]]** huấn luyện mô hình trên các ví dụ có nhãn (cặp đầu vào - đầu ra) để đưa ra dự báo:
- *Classification*: Dự báo kết quả phân loại (vỡ nợ hay không vỡ nợ; tín hiệu mua/giữ/bán).
- *Regression*: Dự báo kết quả liên tục (lợi nhuận quý tới; tỷ suất sinh lợi tương lai).
- Ứng dụng: Chấm điểm tín dụng, phát hiện gian lận, dự báo lợi nhuận.

**[[quantitative-methods/glossary/m11-big-data-techniques#Unsupervised Learning|Unsupervised learning]]** tìm kiếm cấu trúc trong dữ liệu không có nhãn:
- *Clustering*: Nhóm các cổ phiếu tương tự theo hành vi tỷ suất sinh lợi hoặc mức độ tiếp xúc với nhân tố.
- *Dimensionality reduction*: Nén một tập đặc trưng lớn (ví dụ: 1.000 chỉ số tài chính → 5 thành phần chính).
- *Anomaly detection*: Xác định các mẫu giao dịch bất thường hoặc gian lận.

**[[quantitative-methods/glossary/m11-big-data-techniques#Deep Learning|Deep learning]]** sử dụng [[quantitative-methods/glossary/m11-big-data-techniques#Neural Network|neural networks]] nhiều lớp để học các biểu diễn phân cấp từ dữ liệu thô. Đặc biệt hiệu quả cho [[quantitative-methods/glossary/m11-big-data-techniques#Natural Language Processing (NLP)|NLP]] (xử lý văn bản) và nhận dạng hình ảnh (ảnh vệ tinh). Yêu cầu lượng dữ liệu lớn và tài nguyên tính toán đáng kể.

## Huấn luyện mô hình, Kiểm định và vấn đề Overfitting

Các mô hình machine learning được phát triển qua ba giai đoạn sử dụng các phần dữ liệu tách biệt:

1. **[[quantitative-methods/glossary/m11-big-data-techniques#Training Dataset|Training dataset]]**: Dùng để khớp mô hình (ước lượng tham số).
2. **[[quantitative-methods/glossary/m11-big-data-techniques#Validation Dataset|Validation dataset]]**: Dùng để điều chỉnh siêu tham số và lựa chọn giữa các mô hình ứng viên.
3. **[[quantitative-methods/glossary/m11-big-data-techniques#Testing Dataset|Testing dataset]]**: Dùng để đánh giá cuối cùng, không thiên lệch cho mô hình đã chọn.

Rủi ro quan trọng nhất là **[[quantitative-methods/glossary/m11-big-data-techniques#Overfitting|overfitting]]**: một mô hình quá phức tạp ghi nhớ dữ liệu huấn luyện (bao gồm cả nhiễu) thay vì học mẫu nền tảng. Mô hình bị overfitting hoạt động tốt trong mẫu nhưng kém ngoài mẫu — một dạng thất bại gần với [[quantitative-methods/glossary/m07-estimation-and-inference#Data Snooping Bias|data snooping bias]]. **[[quantitative-methods/glossary/m11-big-data-techniques#Underfitting|Underfitting]]** là vấn đề ngược lại: mô hình quá đơn giản bỏ qua các mẫu thực sự.

Các biện pháp khắc phục overfitting bao gồm: regularization (phạt độ phức tạp của mô hình), cross-validation, early stopping trong huấn luyện neural network, và sử dụng tập dữ liệu đủ lớn.

## Text Analytics và NLP trong Tài chính

Phần lớn thông tin tài chính — báo cáo của chuyên viên phân tích, bản ghi cuộc gọi kết quả kinh doanh, bài báo tin tức, hồ sơ pháp lý, mạng xã hội — là văn bản phi cấu trúc. **[[quantitative-methods/glossary/m11-big-data-techniques#Text Analytics|Text analytics]]** và **[[quantitative-methods/glossary/m11-big-data-techniques#Natural Language Processing (NLP)|NLP]]** chuyển đổi văn bản này thành các tín hiệu định lượng.

**[[quantitative-methods/glossary/m11-big-data-techniques#Sentiment Analysis|Sentiment analysis]]** là ứng dụng trực tiếp nhất: phân loại sắc thái của văn bản là tích cực, tiêu cực hay trung tính. Một chuyên viên phân tích có thể đo lường mức độ lạc quan của ban lãnh đạo trong các cuộc gọi kết quả kinh doanh hoặc theo dõi sự thay đổi tâm lý thị trường trên mạng xã hội. Các kỹ thuật NLP như nhận dạng thực thể có tên (xác định công ty, con người và địa điểm) và topic modeling cho phép trích xuất thông tin có cấu trúc hơn từ các kho văn bản lớn.

Bản chất **[[quantitative-methods/glossary/m11-big-data-techniques#Black Box|black box]]** của các mô hình deep learning đặt ra những vấn đề quan trọng trong một ngành được quản lý chặt chẽ: quản lý rủi ro và cơ quan quản lý đòi hỏi khả năng giải thích mô hình, và nghĩa vụ fiduciary yêu cầu phải hiểu và biện hộ cho các quyết định đầu tư. Các chuyên gia đầu tư sử dụng mô hình ML phải hiểu những hạn chế của chúng, dù không nhất thiết phải hiểu toàn bộ cơ chế nội tại.

## Các Module Nguồn

- [[quantitative-methods/modules/m11-big-data-techniques/index|M11 — Big Data and Machine Learning Techniques]] — nội dung chính
- [[quantitative-methods/modules/m03-statistical-measures/index|M03 — Statistical Measures]] — dữ liệu có cấu trúc và phi cấu trúc; nền tảng các loại dữ liệu
- [[quantitative-methods/modules/m07-estimation-and-inference/index|M07 — Estimation and Inference]] — data snooping và overfitting như những thiên lệch song song trong mô hình thống kê và ML