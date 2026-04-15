---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - big-data
  - machine-learning
  - text-analytics
source: "CFAI CFA1 Quant Practice 2026, pp.339-340"
module: "[[quantitative-methods/modules/m11-big-data-techniques/index|M11]]"
---

# M11 – Big Data Techniques: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.339–340
**Back to module:** [[quantitative-methods/modules/m11-big-data-techniques/index|M11]]
**Glossary**: [[quantitative-methods/glossary/m11-big-data-techniques|M11 Terms]]

---

## Question 1

Which of the following is a **characteristic of [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big Data]]**?

- A. It involves diverse format structures
- B. One traditional source of Big Data is business processes
- C. Real-time communication is uncommon because of the vast amount of content

> [!answer]- Answer
> **A. It involves diverse format structures**
>
> Big Data is typically characterised by the **three Vs** (and often extended to five or more):
>
> | Characteristic | Description |
> |----------------|-------------|
> | **Volume** | Massive quantities of data |
> | **Velocity** | Generated and processed at high speed, often in real-time |
> | **Variety** | **Diverse format structures** — structured, semi-structured, and unstructured data (e.g., text, images, audio, sensor data, social media) |
> | Veracity | Accuracy and trustworthiness of data |
> | Value | Actionable insights extractable from data |
>
> "Diverse format structures" directly corresponds to the **Variety** dimension, making A correct.
>
> **Why B is wrong:** Business processes (e.g., transaction records, accounting data) are a **traditional** source of *structured* data — they predate the Big Data era. **Alternative (non-traditional) sources** of Big Data include: social media, sensor/IoT data, satellite imagery, web-scraped data, and electronic communications.
>
> **Why C is wrong:** **Velocity** — the rapid generation and availability of data, including **real-time** streaming — is one of the defining features of Big Data. Real-time communication is very much a characteristic of Big Data, not an uncommon feature.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m11-big-data-techniques#Big Data|Big Data]] được định nghĩa bởi **3 Vs** (và mở rộng đến 5 Vs): **Volume** (khối lượng lớn), **Velocity** (tốc độ cao, real-time), **Variety** (đa dạng định dạng — structured, semi-structured, unstructured), Veracity (độ chính xác), Value (giá trị). "Diverse format structures" = **Variety**.
>
> **Tại sao A đúng:** "Diverse format structures" mô tả đúng chiều **Variety** — Big Data bao gồm nhiều loại định dạng: dữ liệu cấu trúc (bảng), bán cấu trúc (JSON, XML), và phi cấu trúc (text, hình ảnh, âm thanh, sensor data).
> **Tại sao B sai:** Business processes (giao dịch kế toán, dữ liệu ERP) là nguồn dữ liệu **truyền thống** — có trước kỷ nguyên Big Data. Big Data thường liên quan đến các nguồn **phi truyền thống**: mạng xã hội, IoT, satellite imagery, web scraping.
> **Tại sao C sai:** **Velocity** là đặc trưng cốt lõi của Big Data — dữ liệu được tạo ra và xử lý ở tốc độ cao, thường **real-time** (streaming). Real-time communication là đặc tính của Big Data, không phải ngoại lệ.

---

## Question 2

Which of the following statements about **[[quantitative-methods/glossary/m11-big-data-techniques#Machine Learning|machine learning]] (ML)** is **true**?

- A. Some ML techniques are considered "[[quantitative-methods/glossary/m11-big-data-techniques#Black Box|black boxes]]" because they are affected by data biases
- B. Human judgment is not needed when using machine learning models
- C. Training data can be learned too precisely, resulting in poor out-of-sample performance

> [!answer]- Answer
> **C. Training data can be learned too precisely, resulting in poor out-of-sample performance**
>
> This statement describes **[[quantitative-methods/glossary/m11-big-data-techniques#Overfitting|overfitting]]** — one of the primary challenges in machine learning. An overfitted model learns the noise and idiosyncratic patterns in the training data so thoroughly that it fails to generalise to new (out-of-sample) data. The model performs very well in-sample but poorly out-of-sample.
>
> **Techniques to mitigate overfitting:**
> - Cross-validation (e.g., $k$-fold)
> - Regularisation (e.g., LASSO, Ridge regression)
> - Pruning (for decision trees)
> - Reducing model complexity
>
> **Why A is wrong:** Some ML models (e.g., deep neural networks, ensemble methods) are described as **"black boxes"** because their internal workings are complex and difficult to interpret — **not** because of data biases. Data biases are a separate issue (garbage-in-garbage-out) that affect the model's outputs but are not why models are called black boxes.
>
> **Why B is wrong:** **Human judgment** remains essential in ML workflows — for feature selection, model architecture choices, hyperparameter tuning, interpreting results, identifying data quality issues, and setting the problem framing. ML automates pattern recognition but does not eliminate the need for human expertise.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m11-big-data-techniques#Overfitting|Overfitting]] là hiện tượng model "học thuộc" training data quá mức — bao gồm cả noise — nên **hoạt động tốt in-sample nhưng kém out-of-sample**. Đây là thách thức trung tâm trong machine learning. "Black box" trong ML là vấn đề về **interpretability** (khó hiểu cách model ra quyết định), không liên quan đến data bias.
>
> **Tại sao C đúng:** Overfitting = training data được học quá chính xác → model không generalise tốt sang dữ liệu mới. Ví dụ: mô hình dự báo return học thuộc các pattern ngẫu nhiên trong lịch sử → backtest tốt nhưng live trading kém.
> **Tại sao A sai:** "Black box" trong ML mô tả sự **thiếu interpretability** (khó giải thích cơ chế bên trong của deep neural networks). Data biases là vấn đề riêng (garbage-in, garbage-out) — không phải lý do gọi là "black box".
> **Tại sao B sai:** Human judgment **vẫn cần thiết** trong ML: chọn features, thiết kế kiến trúc model, tuning hyperparameters, diễn giải kết quả, phát hiện data quality issues. ML tự động hóa nhận diện pattern nhưng không loại bỏ expertise của người dùng.

---

## Question 3

**[[quantitative-methods/glossary/m11-big-data-techniques#Text Analytics|Text analytics]]** is most appropriate for:

- A. analysing large structured datasets
- B. extracting insights from public information sources but not private information
- C. identifying short-term trend indicators in financial markets

> [!answer]- Answer
> **C. identifying short-term trend indicators in financial markets**
>
> Text analytics — also called **[[quantitative-methods/glossary/m11-big-data-techniques#NLP|natural language processing (NLP)]]** — processes and analyses **unstructured text data** (news articles, earnings call transcripts, social media posts, analyst reports, regulatory filings) to extract sentiment, trends, and signals. In finance, text analytics is commonly used to:
>
> - Analyse central bank communications for hawkish/dovish signals
> - Extract sentiment from earnings call transcripts
> - Monitor social media for short-term market sentiment shifts
> - Track news flow for event-driven trading signals
>
> These applications are well-suited to identifying **short-term trend indicators**.
>
> **Why A is wrong:** Text analytics is specifically designed for **unstructured** (and semi-structured) data — such as text, HTML, and JSON — not large structured datasets. For structured data (e.g., databases, spreadsheets), traditional statistical and quantitative methods are more appropriate.
>
> **Why B is wrong:** Text analytics can be applied to **both public** (news feeds, social media, company filings) **and private** (internal emails, call centre transcripts, proprietary research) information sources. The distinction between public and private does not define the scope of text analytics.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m11-big-data-techniques#Text Analytics|Text analytics]] (hay [[quantitative-methods/glossary/m11-big-data-techniques#NLP|NLP]] — Natural Language Processing) xử lý dữ liệu **phi cấu trúc dạng văn bản**: tin tức, transcript earnings call, mạng xã hội, báo cáo analyst, hồ sơ pháp lý. Trong finance, text analytics được dùng để: trích xuất sentiment, phát hiện signals ngắn hạn, phân tích tín dụng từ văn bản.
>
> **Tại sao C đúng:** Text analytics trên dữ liệu financial text (news, social media, earnings calls) rất phù hợp để **xác định short-term trend indicators** — phân tích sentiment thị trường, phát hiện signals ngắn hạn từ thông tin phi cấu trúc.
> **Tại sao A sai:** Text analytics được thiết kế cho dữ liệu **phi cấu trúc** (unstructured text), không phải large structured datasets (dữ liệu cấu trúc như bảng, spreadsheet). Structured data dùng statistical/quantitative methods truyền thống.
> **Tại sao B sai:** Text analytics áp dụng được cho cả nguồn thông tin **công khai** (tin tức, social media, SEC filings) lẫn **nội bộ/riêng tư** (email nội bộ, transcript call center, nghiên cứu độc quyền). Phân biệt public/private không định nghĩa phạm vi của text analytics.
