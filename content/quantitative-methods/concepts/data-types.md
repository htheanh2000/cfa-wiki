---
title: "Data Types"
type: concept
subject: quantitative-methods
created: 2026-04-09
updated: 2026-04-09
tags: [data-types, numerical, categorical, time-series, cross-sectional, panel-data, structured, unstructured]
---

# Data Types

## Tổng quan

Hiểu về các loại dữ liệu là nền tảng để lựa chọn phương pháp thống kê và kiểm định phù hợp. Chương trình CFA phân loại dữ liệu theo hai chiều chính: **thang đo** (measurement scale) và **cấu trúc/tổ chức** (structure/organization).

## Phân loại theo Thang Đo

| Loại | Phân nhóm | Mô tả | Ví dụ |
|------|-----------|-------|-------|
| **Numerical (Quantitative)** | Continuous | Có thể nhận bất kỳ giá trị nào trong một khoảng | Lợi suất, giá, tỷ số |
| | Discrete | Chỉ nhận các giá trị đếm được | Số lượng giao dịch, số lần vỡ nợ |
| **Categorical (Qualitative)** | Nominal | Không có thứ tự tự nhiên; chỉ là nhãn | Ngành, quốc gia, đơn vị tiền tệ |
| | Ordinal | Có thứ tự tự nhiên, nhưng các khoảng cách không bằng nhau | Xếp hạng tín dụng (AAA > AA > A), điểm khảo sát |

> **Điểm phân biệt quan trọng**: Các phép toán số học có ý nghĩa với dữ liệu numerical, nhưng không có ý nghĩa với dữ liệu categorical.

## Phân loại theo Tổ Chức / Cấu Trúc

| Loại | Mô tả | Ví dụ |
|------|-------|-------|
| **Time-series** | Quan sát một thực thể qua nhiều khoảng thời gian | Lợi suất hàng ngày của cổ phiếu Apple từ 2020–2025 |
| **Cross-sectional** | Quan sát nhiều thực thể tại một thời điểm duy nhất | Chỉ số P/E của 500 cổ phiếu tính đến ngày 31/12/2025 |
| **Panel data** | Nhiều thực thể được quan sát qua nhiều khoảng thời gian (kết hợp hai loại trên) | EPS hàng năm của 100 công ty trong 10 năm |

## Dữ liệu Structured và Unstructured

| Loại | Mô tả | Ví dụ |
|------|-------|-------|
| **Structured** | Được tổ chức theo hàng/cột; dễ lưu trữ trong cơ sở dữ liệu | Báo cáo tài chính, dữ liệu giá, chỉ số kinh tế |
| **Unstructured** | Không có định dạng xác định trước; cần NLP hoặc các kỹ thuật khác để trích xuất | Bản ghi cuộc họp thu nhập, bài báo, hình ảnh vệ tinh |
| **Semi-structured** | Có tổ chức một phần | Dữ liệu JSON/XML, bảng dữ liệu thu thập từ web |

## Ảnh hưởng đến Phân Tích Thống Kê

- **Dữ liệu Nominal/Ordinal** → kiểm định phi tham số (non-parametric tests) (chi-square, Spearman rank): xem [[quantitative-methods/modules/m09-parametric-tests/index|M09]]
- **Dữ liệu Numerical liên tục** → kiểm định tham số (parametric tests) (z-test, t-test, hồi quy): xem [[quantitative-methods/modules/m08-hypothesis-testing/index|M08]], [[quantitative-methods/modules/m10-simple-linear-regression/index|M10]]
- **Dữ liệu Unstructured/Big Data** → học máy (machine learning), kỹ thuật NLP: xem [[quantitative-methods/modules/m11-big-data-techniques/index|M11]]

## Các Module Nguồn

- [[quantitative-methods/modules/m03-statistical-measures/index|M03 — Statistical Measures of Asset Returns]] — nội dung chính về các loại dữ liệu và thang đo
- [[quantitative-methods/modules/m09-parametric-tests/index|M09 — Parametric and Non-parametric Tests]] — lựa chọn kiểm định phụ thuộc vào loại dữ liệu
- [[quantitative-methods/modules/m11-big-data-techniques/index|M11 — Introduction to Big Data Techniques]] — dữ liệu structured và unstructured trong bối cảnh ML/NLP