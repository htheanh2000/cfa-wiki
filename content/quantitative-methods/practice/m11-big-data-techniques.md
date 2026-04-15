---
title: "Practice: M11 — Big Data Techniques"
type: practice
subject: quantitative-methods
module: M11
created: 2026-04-09
updated: 2026-04-09
tags: [practice, big-data, fintech, machine-learning, nlp]
---

# Practice: M11 — Introduction to Big Data Techniques

**Module**: [[quantitative-methods/modules/m11-big-data-techniques/index|M11]]
**Glossary**: [[quantitative-methods/glossary/m11-big-data-techniques|M11 Terms]]

---

**Question 1**: "[[quantitative-methods/glossary/m11-big-data-techniques#Fintech|Fintech]]" is best described as:

A. A technology-driven innovation in the financial service industry
B. The collection of large quantities of financial data from a variety of sources in multiple formats
C. The use of technical models to describe patterns in financial markets and make trading decisions

> [!answer]- Answer
> **A.** Fintech refers to technology-driven innovation in the **design and delivery** of financial services and products. B describes [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big Data]]. C describes quantitative trading.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m11-big-data-techniques#Fintech|Fintech]] (Financial Technology) là thuật ngữ chỉ sự đổi mới công nghệ trong **thiết kế và cung cấp** dịch vụ tài chính. Fintech bao gồm: thanh toán kỹ thuật số, robo-advisors, blockchain, peer-to-peer lending, insurtech, v.v. Đây là thuật ngữ rộng về **ngành và mô hình kinh doanh**, không chỉ đề cập đến dữ liệu hay kỹ thuật phân tích cụ thể.
>
> **Tại sao A đúng:** Định nghĩa chuẩn của CFA: Fintech = "technology-driven innovation in the design and delivery of financial services and products." Từ khóa: innovation (đổi mới), financial services (dịch vụ tài chính), technology-driven (được thúc đẩy bởi công nghệ).
>
> **Tại sao B sai:** Mô tả B là định nghĩa của [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big Data]] — thu thập lượng lớn dữ liệu từ nhiều nguồn đa dạng. Big Data là một **công cụ/tài nguyên** mà fintech có thể sử dụng, không phải định nghĩa của fintech.
>
> **Tại sao C sai:** Mô tả của C gần với **quantitative trading** (giao dịch định lượng) hoặc algorithmic trading — dùng mô hình toán học để tìm patterns và ra quyết định giao dịch. Đây là một ứng dụng cụ thể, không phải định nghĩa tổng quát của fintech.

---

**Question 2**: Which of the following statements is true in the use of [[quantitative-methods/glossary/m11-big-data-techniques#Machine Learning|Machine Learning]] (ML)?

A. Some techniques are termed "[[quantitative-methods/glossary/m11-big-data-techniques#Black Box|black box]]" due to data biases
B. Human judgment is not needed because algorithms continuously learn from data
C. Training data can be learned too precisely, resulting in inaccurate predictions when used with different datasets

> [!answer]- Answer
> **C.** This describes **[[quantitative-methods/glossary/m11-big-data-techniques#Overfitting|overfitting]]** — the model memorizes noise in training data and fails to generalize. A is wrong — "black box" is because outcomes are not fully explainable, not due to biases. B is wrong — human judgment is still needed for model design, feature selection, and interpretation.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m11-big-data-techniques#Overfitting|Overfitting]] là khi mô hình ML học quá kỹ trên training data — bao gồm cả "nhiễu" (noise) ngẫu nhiên — đến mức mất khả năng tổng quát hóa (generalize) sang dữ liệu mới. Kết quả: performance rất tốt trên training set nhưng kém trên test/validation set.
>
> **Tại sao C đúng:** Mô tả chính xác overfitting: "learned too precisely" = ghi nhớ cả noise trong training data, "inaccurate on different datasets" = không generalize được.
>
> **Tại sao A sai:** [[quantitative-methods/glossary/m11-big-data-techniques#Black Box|Black box]] problem xảy ra vì **thiếu khả năng giải thích** (interpretability) — không thể biết tại sao mô hình ra quyết định đó. Nguyên nhân là kiến trúc phức tạp (như deep neural networks), không phải data biases. Data biases là vấn đề riêng (garbage in, garbage out).
>
> **Tại sao B sai:** Human judgment vẫn **không thể thiếu** trong ML: chọn features, thiết kế kiến trúc mô hình, quyết định training/test split, diễn giải kết quả, giám sát model drift, và đảm bảo kết quả có ý nghĩa kinh tế. Không có ML system nào hoàn toàn tự động không cần con người.

---

**Question 3**: [[quantitative-methods/glossary/m11-big-data-techniques#Text Analytics|Text analytics]] is appropriate for application to:

A. Large, structured datasets
B. Public but not private information
C. Identifying possible short-term indicators of coming trends

> [!answer]- Answer
> **C.** Text analytics analyzes **unstructured** text data (not structured — A is wrong) from any source including private data (B is wrong) to identify patterns, sentiment, and indicators of trends.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m11-big-data-techniques#Text Analytics|Text analytics]] (còn gọi là text mining hay NLP-based analysis) xử lý **dữ liệu văn bản phi cấu trúc** (unstructured text) — như tin tức, báo cáo, social media, earnings call transcripts, legal documents — để trích xuất thông tin, đo sentiment, hoặc phát hiện xu hướng.
>
> **Tại sao C đúng:** Đây là ứng dụng cốt lõi của text analytics trong đầu tư: phân tích tin tức, tweet của CEO, bình luận khách hàng để phát hiện sớm tín hiệu thay đổi sentiment hoặc xu hướng thị trường — trước khi chúng được phản ánh vào giá.
>
> **Tại sao A sai:** Text analytics xử lý dữ liệu **phi cấu trúc** (unstructured), không phải structured. Structured data (bảng số liệu có cột/hàng rõ ràng) đã có các công cụ thống kê truyền thống. Điểm mạnh của text analytics chính là xử lý được văn bản tự nhiên.
>
> **Tại sao B sai:** Text analytics có thể áp dụng cho **cả** nguồn công khai lẫn riêng tư. Ví dụ: phân tích email nội bộ (private), call transcripts từ IR meetings (semi-private), hay social media (public). Không có giới hạn về nguồn dữ liệu.

---

**Question 4**: The three characteristics of [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big Data]] are best described as:

A. Volume, Velocity, Variety
B. Volume, Variance, Visualization
C. Validity, Velocity, Value

> [!answer]- Answer
> **A.** The **3 V's of Big Data**: Volume (massive amounts), Velocity (speed of data generation/processing), Variety (structured, semi-structured, unstructured formats).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big Data]] được đặc trưng bởi **3 V's** — một framework tiêu chuẩn trong ngành:
> - **Volume (Khối lượng):** Lượng dữ liệu khổng lồ — terabytes đến petabytes — vượt khả năng xử lý của hệ thống truyền thống
> - **Velocity (Tốc độ):** Dữ liệu được tạo ra và cần được xử lý **rất nhanh** — real-time streaming (giao dịch HFT, social media feeds)
> - **Variety (Đa dạng):** Nhiều **định dạng** khác nhau — structured (databases), semi-structured (JSON, XML), unstructured (text, images, video)
>
> **Tại sao A đúng:** Volume + Velocity + Variety là bộ 3 V tiêu chuẩn được CFA Institute định nghĩa. Đây là câu hỏi thuần ghi nhớ — cần thuộc lòng.
>
> **Tại sao B sai:** "Variance" là khái niệm thống kê (phương sai), không phải đặc trưng của Big Data. "Visualization" là công cụ trình bày dữ liệu, không phải đặc điểm định nghĩa Big Data.
>
> **Tại sao C sai:** "Validity" và "Value" đôi khi được đề cập là V thứ 4 và 5 (trong các framework mở rộng 5V), nhưng **không** nằm trong bộ 3 V chuẩn. CFA chỉ yêu cầu 3 V: Volume, Velocity, Variety.

---

**Question 5**: Machine learning that uses **labeled** training data to predict outcomes for new datasets is called:

A. [[quantitative-methods/glossary/m11-big-data-techniques#Supervised Learning|Supervised learning]]
B. [[quantitative-methods/glossary/m11-big-data-techniques#Unsupervised Learning|Unsupervised learning]]
C. [[quantitative-methods/glossary/m11-big-data-techniques#Deep Learning|Deep learning]]

> [!answer]- Answer
> **A. Supervised learning** — given labeled input-output pairs, the algorithm learns the mapping to predict outcomes on new data. Unsupervised uses unlabeled data to discover structure. Deep learning uses neural networks and can be either supervised or unsupervised.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Ba loại machine learning chính:
> - **[[quantitative-methods/glossary/m11-big-data-techniques#Supervised Learning|Supervised learning]]:** Có **labeled data** (dữ liệu có nhãn — biết input và output). Thuật toán học mối quan hệ X→Y để dự đoán Y cho X mới. Ví dụ: dự đoán credit default (Y = default/no-default), phân loại email spam.
> - **[[quantitative-methods/glossary/m11-big-data-techniques#Unsupervised Learning|Unsupervised learning]]:** **Không** có nhãn. Thuật toán tự tìm cấu trúc ẩn trong dữ liệu. Ví dụ: clustering khách hàng, dimensionality reduction (PCA).
> - **[[quantitative-methods/glossary/m11-big-data-techniques#Deep Learning|Deep learning]]:** Dùng **neural networks nhiều lớp** (deep neural networks). Có thể là supervised hoặc unsupervised — đây là về **kiến trúc mô hình**, không phải loại học.
>
> **Tại sao A đúng:** "Labeled training data to predict outcomes" = định nghĩa chính xác của supervised learning — học từ cặp (input, label) để dự đoán label cho input mới.
>
> **Tại sao B sai:** Unsupervised learning **không có** labeled outputs. Không có "ground truth" để học từ đó — thuật toán tự khám phá patterns.
>
> **Tại sao C sai:** Deep learning là một **phương pháp/kiến trúc** (dùng neural networks nhiều lớp), không phải một loại học theo nghĩa có/không có nhãn. Deep learning có thể supervised (e.g., image classification) hoặc unsupervised (e.g., generative models).

---

**Question 6**: An ML model performs excellently on training data but poorly on new data. This is most likely due to:

A. [[quantitative-methods/glossary/m11-big-data-techniques#Underfitting|Underfitting]]
B. [[quantitative-methods/glossary/m11-big-data-techniques#Overfitting|Overfitting]]
C. [[quantitative-methods/glossary/m11-big-data-techniques#Black Box|Black box]] problem

> [!answer]- Answer
> **B. Overfitting** — the model learned the training data too precisely, including noise and spurious patterns, making it too complex to generalize. Underfitting would perform poorly on BOTH training and new data. Black box is an interpretability issue, not a performance issue.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Bias-variance tradeoff trong ML:
> - **[[quantitative-methods/glossary/m11-big-data-techniques#Overfitting|Overfitting]]** (high variance, low bias): Mô hình **quá phức tạp** — fit tốt training data (kể cả noise) nhưng không generalize. Kết quả: training error thấp, test error cao.
> - **[[quantitative-methods/glossary/m11-big-data-techniques#Underfitting|Underfitting]]** (high bias, low variance): Mô hình **quá đơn giản** — không nắm bắt được pattern thực sự. Kết quả: cả training error và test error đều cao.
>
> **Tại sao B đúng:** "Tốt trên training, kém trên new data" = triệu chứng điển hình của overfitting. Mô hình đã "ghi nhớ" training data thay vì "học" pattern thực sự.
>
> **Tại sao A sai:** [[quantitative-methods/glossary/m11-big-data-techniques#Underfitting|Underfitting]] sẽ cho kết quả **kém trên cả hai** — training data và new data. Nếu training performance tốt, loại trừ underfitting ngay.
>
> **Tại sao C sai:** [[quantitative-methods/glossary/m11-big-data-techniques#Black Box|Black box]] problem là vấn đề về **khả năng giải thích** (interpretability/explainability) — không biết tại sao mô hình ra quyết định đó. Đây không liên quan đến việc mô hình perform tốt hay kém. Một black box model vẫn có thể generalize tốt.
>
> **Giải pháp cho overfitting:** regularization (L1/L2), cross-validation, pruning, dropout (neural networks), thu thập thêm training data.

---

**Question 7**: Which is **not** a traditional source of financial data?

A. Government economic statistics
B. Social media posts and online reviews
C. Company annual reports and filings

> [!answer]- Answer
> **B.** Social media is a **non-traditional (alternative)** data source. Government statistics (A) and company filings (C) are traditional sources.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Traditional data** (dữ liệu truyền thống) trong tài chính bao gồm: báo cáo tài chính doanh nghiệp, dữ liệu giá/khối lượng giao dịch, thống kê kinh tế vĩ mô của chính phủ. **Alternative data** (dữ liệu thay thế/phi truyền thống) là dữ liệu từ các nguồn không thông thường, thường là unstructured và ở quy mô lớn.
>
> **Tại sao B đúng (không phải truyền thống):** Social media posts và online reviews là **alternative data** — nguồn dữ liệu phi cấu trúc, không được tạo ra với mục đích tài chính ban đầu. Đây thuộc Big Data và thường được khai thác qua text analytics/NLP.
>
> **Tại sao A là traditional:** Government economic statistics (GDP, CPI, unemployment rate) là nguồn dữ liệu kinh tế được thiết lập từ lâu, có phương pháp luận chuẩn, và được các nhà đầu tư sử dụng thường xuyên trong nhiều thập kỷ.
>
> **Tại sao C là traditional:** Company annual reports (10-K, 20-F) và regulatory filings (SEC filings) là nguồn dữ liệu tài chính tiêu chuẩn nhất — tất cả nhà phân tích cơ bản đều dùng. Đây là dữ liệu **structured** và **có quy định pháp lý**.
>
> **Ví dụ alternative data khác:** satellite imagery (đo lượng xe ở bãi đậu xe), credit card transactions, web scraping, weather data, geolocation data.

---

**Question 8**: The correct order of the Big Data processing pipeline is:

A. Capture → Storage → Curation → Search → Transfer
B. Capture → Curation → Storage → Search → Transfer
C. Curation → Capture → Search → Storage → Transfer

> [!answer]- Answer
> **B.** Capture (collect data) → Curation (clean/quality check) → Storage (archive) → Search (find information) → Transfer (move where needed).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Pipeline xử lý [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big Data]] theo thứ tự logic: thu thập → làm sạch → lưu trữ → tìm kiếm → truyền tải. Đây là quy trình "data lifecycle" chuẩn trong Big Data engineering.
>
> **Giải thích từng bước:**
> 1. **Capture (Thu thập):** Thu thập dữ liệu từ các nguồn — sensors, APIs, web scraping, databases
> 2. **Curation (Chắt lọc/Làm sạch):** Kiểm tra chất lượng, làm sạch lỗi, chuẩn hóa định dạng, xử lý missing values — **phải làm trước khi lưu** để đảm bảo data quality
> 3. **Storage (Lưu trữ):** Lưu trữ dữ liệu đã làm sạch — data warehouse, data lake, cloud storage
> 4. **Search (Tìm kiếm):** Truy vấn và tìm thông tin từ kho dữ liệu đã lưu
> 5. **Transfer (Truyền tải):** Chuyển dữ liệu đến nơi cần thiết — dashboards, models, end users
>
> **Tại sao B đúng và A sai:** Điểm khác biệt then chốt: **Curation phải đến TRƯỚC Storage** (B), không phải sau (A). Lưu dữ liệu bẩn trước rồi mới làm sạch là thực hành kém — tốn chi phí lưu trữ và có thể gây ô nhiễm dữ liệu trong kho.
>
> **Tại sao C sai:** Không thể Curation trước khi Capture — không có dữ liệu để làm sạch. Thứ tự C hoàn toàn vô lý về mặt logic.
