---
title: "M02 — Market Indexes"
type: module
subject: equity-investments
module: m02
los: [2.a, 2.b, 2.c, 2.d, 2.e, 2.f, 2.g, 2.h, 2.i, 2.j, 2.k]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, m02, security-market-indexes, index-construction]
---

# M02: Security Market Indexes

**Nguồn**: [[equity-investments/sources/sapp-equity-2026|SAPP Slide 2026]], trang 56–96
**LOS**: 2.a–2.k

---

## LOS 2.a — Định nghĩa Security Market Index

Một **security market index** đại diện cho giá trị của một nhóm chứng khoán (**constituent securities**) được chọn để đại diện cho một thị trường hoặc phân khúc mục tiêu.

### Price Return Index vs Total Return Index

| Loại | Phản ánh |
|------|----------|
| **Price return index** | Chỉ biến động giá của các constituent |
| **Total return index** | Biến động giá + thu nhập (cổ tức, lãi suất) — giả định tái đầu tư |

> Total return index sẽ luôn $\geq$ price return index theo thời gian (giả định thu nhập dương).

---

## LOS 2.b — Tính toán lợi nhuận của Index

### Single-Period Price Return

**Cách 1 — Từ giá trị index:**

$$R_{\text{price}} = \frac{V_1 - V_0}{V_0}$$

**Cách 2 — Từ lợi nhuận của các constituent:**

$$R_{\text{price}} = \sum_{i=1}^{N} w_i \cdot R_i$$

Trong đó:
- $w_i$ = tỷ trọng của chứng khoán $i$ trong index
- $R_i$ = price return của chứng khoán $i$

### Single-Period Total Return

**Cách 1 — Từ giá trị index (bao gồm thu nhập):**

$$R_{\text{total}} = \frac{V_1 - V_0 + \text{Income}}{V_0}$$

**Cách 2 — Từ total return của các constituent:**

$$R_{\text{total}} = \sum_{i=1}^{N} w_i \cdot R_{\text{total},i}$$

### Multi-Period Return (Linking)

$$R_{\text{multi}} = \prod_{t=1}^{T}(1 + R_t) - 1$$

---

## LOS 2.c — Các lựa chọn trong việc xây dựng Index

Khi xây dựng một index, cần đưa ra năm quyết định:

1. **Target market** — Index đại diện cho thị trường hoặc phân khúc nào?
2. **Security selection** — Chứng khoán nào được đưa vào? (Tiêu chí khách quan hay do ủy ban quyết định)
3. **Weighting method** — Tỷ trọng của mỗi constituent được xác định như thế nào?
4. **Rebalancing** — Tần suất điều chỉnh lại tỷ trọng về mức mục tiêu? (Hàng quý, nửa năm)
5. **Reconstitution** — Tần suất thêm/loại bỏ constituent? (Hàng năm, hàng quý)

---

## LOS 2.d & 2.e — Các phương pháp tính tỷ trọng

### Price-Weighted Index

$$\text{Index value} = \frac{\sum_{i=1}^{N} P_i}{\text{Divisor}}$$

- Tỷ trọng tỷ lệ thuận với **giá cổ phiếu**
- Cổ phiếu có giá cao hơn sẽ có ảnh hưởng lớn hơn
- Việc chia tách cổ phiếu yêu cầu **điều chỉnh divisor**
- Ví dụ: DJIA, Nikkei 225

### Equal-Weighted Index

$$w_i = \frac{1}{N}$$

- Mỗi constituent có **tỷ trọng bằng nhau**
- Yêu cầu **rebalancing** thường xuyên (khi giá thay đổi, tỷ trọng sẽ bị lệch)
- Nghiêng về **cổ phiếu vốn hóa nhỏ (small-cap)** so với cách tính theo market-cap
- Ví dụ: S&P 500 Equal Weight Index

### Market-Capitalization-Weighted Index

$$w_i = \frac{P_i \times Q_i}{\sum_{j=1}^{N} P_j \times Q_j}$$

Trong đó:
- $P_i$ = giá của chứng khoán $i$
- $Q_i$ = tổng số cổ phiếu đang lưu hành của chứng khoán $i$

- Tỷ trọng tỷ lệ thuận với **market cap**
- Phương pháp phổ biến nhất; đại diện cho "market portfolio"
- **Tự cân bằng (self-rebalancing)** — không cần hành động khi giá thay đổi
- Thiên lệch: tập trung vào cổ phiếu **large-cap**
- Ví dụ: S&P 500 (market-cap weighted), MSCI World

### Float-Adjusted Market-Cap-Weighted Index

$$w_i = \frac{P_i \times Q_i^{\text{float}}}{\sum_{j=1}^{N} P_j \times Q_j^{\text{float}}}$$

- Chỉ sử dụng **cổ phiếu có thể giao dịch tự do** (loại trừ cổ phiếu bị khóa, do chính phủ nắm giữ, cổ phiếu nội bộ)
- Phản ánh tốt hơn tập hợp cơ hội **có thể đầu tư thực tế**
- Ví dụ: Hầu hết các index hiện đại (S&P 500 sử dụng float-adjusted)

### Fundamental-Weighted Index

- Tỷ trọng dựa trên **các yếu tố cơ bản**: doanh thu, lợi nhuận, cổ tức, giá trị sổ sách
- Thiên hướng contrarian: overweight cổ phiếu **bị định giá thấp** (những cổ phiếu có chỉ số cơ bản cao so với giá)
- Yêu cầu **rebalancing** định kỳ
- Ví dụ: FTSE RAFI Index Series

---

## LOS 2.f — Rebalancing và Reconstitution

### Rebalancing
- Điều chỉnh **tỷ trọng** của các constituent về mức mục tiêu
- Bắt buộc đối với equal-weighted và fundamental-weighted index
- Market-cap-weighted index **tự cân bằng** khi giá thay đổi
- Tần suất: thường là hàng quý

### Reconstitution
- Thay đổi **danh sách constituent** — thêm hoặc loại bỏ chứng khoán
- Dựa trên các tiêu chí lựa chọn (ngưỡng market cap, thanh khoản, v.v.)
- Gây ra **hiệu ứng giá**: cổ phiếu được thêm vào có xu hướng tăng, cổ phiếu bị loại có xu hướng giảm
- Tần suất: thường là hàng năm hoặc nửa năm

---

## LOS 2.g — Các ứng dụng của Market Index

1. **Đo lường tâm lý thị trường** — Đánh giá xu hướng chung của thị trường và niềm tin của nhà đầu tư
2. **Benchmarking** — Đánh giá hiệu suất của quản lý đầu tư chủ động so với benchmark thụ động
3. **Đầu tư thụ động** — Các quỹ index và ETF sao chép lợi nhuận của index
4. **Asset allocation** — Mô hình tỷ trọng danh mục đầu tư theo các lớp tài sản
5. **Đo lường rủi ro hệ thống** — Beta được đo lường tương đối so với một market index
6. **Nghiên cứu các yếu tố thị trường** — Các nghiên cứu học thuật về risk premium, các bất thường

---

## LOS 2.h — Equity Indexes

Các loại equity index:

| Loại | Mô tả |
|------|-------|
| **Broad market** | Đại diện toàn bộ thị trường cổ phiếu của một quốc gia (ví dụ: Wilshire 5000, Russell 3000) |
| **Multi-market** | Trải rộng nhiều quốc gia (ví dụ: MSCI World, MSCI ACWI, FTSE All-World) |
| **Sector** | Tập trung vào các ngành công nghiệp cụ thể (ví dụ: S&P 500 IT, MSCI Healthcare) |
| **Style** | Growth vs Value (ví dụ: Russell 1000 Growth, Russell 1000 Value) |

---

## LOS 2.i — Fixed-Income Indexes

Đặc điểm của fixed-income index:
- Vũ trụ chứng khoán lớn hơn nhiều so với cổ phiếu (nhiều đợt phát hành trái phiếu trên mỗi tổ chức phát hành)
- Kém thanh khoản hơn — trái phiếu giao dịch OTC, không thường xuyên
- Trái phiếu đáo hạn — thành phần index thay đổi liên tục (reconstitution thường xuyên hơn)
- Các danh mục: chính phủ, doanh nghiệp, chứng khoán hóa, tổng hợp, gắn với lạm phát

---

## LOS 2.j — Alternative Investment Indexes

| Danh mục | Ví dụ | Lưu ý |
|----------|-------|-------|
| **Commodity** | S&P GSCI, Bloomberg Commodity | Dựa trên hợp đồng tương lai, không phải giá giao ngay (spot) |
| **Real estate** | FTSE NAREIT, S&P Global REIT | REITs (niêm yết công khai) vs dựa trên thẩm định giá (tư nhân) |
| **Hedge fund** | HFRI, Credit Suisse HF Index | Thiên lệch do tự báo cáo, survivorship bias |
| **Private equity** | Cambridge Associates PE Index | Dựa trên thẩm định giá, định giá có độ trễ |
| **Infrastructure** | S&P Global Infrastructure | Kết hợp tiện ích công cộng, vận tải, năng lượng |

---

## LOS 2.k — Những thách thức với Alternative Investment Indexes

- **Survivorship bias**: Các quỹ/tài sản thất bại bị loại khỏi index, làm tăng ảo lợi nhuận lịch sử
- **Self-reporting / selection bias**: Chỉ các quỹ thành công mới tự nguyện báo cáo
- **Appraisal-based valuation**: Làm mượt lợi nhuận, đánh giá thấp biến động (bất động sản, private equity)
- **Backfill bias**: Khi một quỹ gia nhập index, lợi nhuận lịch sử tốt của quỹ đó được thêm vào hồi tố
- **Illiquidity**: Các constituent có thể không dễ dàng đầu tư được