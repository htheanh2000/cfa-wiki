---
type: practice
tags:
  - cfai-official
  - alternative-investments
  - hedge-funds-index-biases
source: "CFAI CFA1 Alternative Investments Practice 2026"
module: "[[m06-hedge-funds-index-biases]]"
---

# M06 – Hedge Funds and Index Biases: CFAI Practice Problems

**Source:** CFAI CFA1 Alternative Investments Practice 2026
**Back to module:** [[m06-hedge-funds-index-biases]]

---

## Question 1

A hedge fund index that does not include funds that have closed or stopped reporting due to poor performance most likely suffers from:

- A. Survivorship bias
- B. Backfill bias
- C. Selection bias

> [!answer]- Answer
> **A. Survivorship bias**
>
> **Survivorship bias** occurs when a hedge fund index only includes funds that are currently operating and reporting. Funds that have failed, liquidated, or stopped reporting due to poor performance are excluded. This causes the index to **overestimate** average returns because only the "survivors" (typically better performers) remain in the dataset.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Survivorship bias** = thiên lệch sống sót:
> - Quỹ hoạt động kém → đóng cửa → bị loại khỏi index
> - Chỉ quỹ thành công còn lại → average return bị thổi phồng
> - Ước tính return cao hơn thực tế, risk thấp hơn thực tế
>
> **Ví dụ:**
> - 100 quỹ bắt đầu hoạt động
> - 20 quỹ thất bại và đóng cửa (return trung bình −15%)
> - Index chỉ tính 80 quỹ còn lại → bỏ qua 20 quỹ lỗ → return trung bình bị overestimate
>
> **Tại sao A đúng:** "Does not include funds that have closed or stopped reporting due to poor performance" — đây chính xác là định nghĩa survivorship bias.
>
> **Tại sao B sai:** Backfill bias xảy ra khi quỹ mới được thêm vào index và lịch sử return (thường tốt) được backfill vào database.
> **Tại sao C sai:** Selection bias xảy ra khi quỹ tự chọn có tham gia index hay không (self-selection).

---

## Question 2

A hedge fund database that allows fund managers to choose whether or not to report their performance data most likely exhibits:

- A. Survivorship bias
- B. Selection bias
- C. Backfill bias

> [!answer]- Answer
> **B. Selection bias**
>
> **Selection bias** (also called self-selection bias or self-reporting bias) arises because hedge fund reporting to databases is **voluntary**. Fund managers with strong performance are more likely to report (to attract investors), while those with poor performance may choose not to report. This **inconsistent allocation** of funds into the database creates a biased sample.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Selection bias** = thiên lệch lựa chọn:
> - Hedge fund KHÔNG bắt buộc báo cáo vào database (khác cổ phiếu niêm yết)
> - Manager có performance tốt → tự nguyện báo cáo để marketing
> - Manager có performance kém → không báo cáo để tránh "xấu hổ"
> - Kết quả: database chỉ gồm phần lớn quỹ có return tốt → overestimate
>
> **Lưu ý:** Selection bias có hai chiều:
> 1. Quỹ mới muốn huy động vốn → báo cáo return tốt
> 2. Quỹ đã đủ lớn, đóng cửa với nhà đầu tư mới → ngừng báo cáo (performance có thể tốt hoặc xấu)
>
> **Tại sao B đúng:** "Choose whether or not to report" = voluntary reporting = self-selection bias. Inconsistent allocation vào database.
>
> **Tại sao A sai:** Survivorship bias liên quan đến quỹ đóng cửa/thất bại bị loại, không phải tự chọn báo cáo.
> **Tại sao C sai:** Backfill bias liên quan đến việc thêm dữ liệu lịch sử khi quỹ mới tham gia.

---

## Question 3

A hedge fund index that suffers from both backfill bias and survivorship bias will most likely:

- A. Overestimate historical returns
- B. Underestimate historical returns
- C. Have no impact on reported returns

> [!answer]- Answer
> **A. Overestimate historical returns**
>
> Both **backfill bias** and **survivorship bias** cause an **upward bias** in reported returns:
> - **Backfill bias:** When a fund joins an index, its historical (typically good) performance is added retroactively, inflating past returns.
> - **Survivorship bias:** Failed funds are removed, leaving only successful funds in the index.
>
> Together, these biases cause the index to **overestimate** historical hedge fund returns.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Tổng hợp các biases trong hedge fund index:
>
> | Bias | Nguyên nhân | Tác động |
> |------|------------|---------|
> | **Survivorship** | Quỹ thất bại bị loại | Overestimate return ↑ |
> | **Backfill** | Lịch sử tốt được thêm vào khi quỹ mới tham gia | Overestimate return ↑ |
> | **Selection** | Quỹ tự chọn có báo cáo hay không | Overestimate return ↑ |
>
> **Khi kết hợp cả ba:**
> - Return lịch sử bị thổi phồng đáng kể
> - Risk bị đánh giá thấp
> - Sharpe ratio bị overestimate
> - Nhà đầu tư có thể đưa ra quyết định sai lầm dựa trên dữ liệu thiên lệch
>
> **Tại sao A đúng:** Cả backfill và survivorship đều tạo upward bias → overestimate returns.
>
> **Tại sao B sai:** Không có cơ chế nào trong hai biases này gây underestimate.
> **Tại sao C sai:** Cả hai biases đều có tác động rõ ràng, không phải "no impact."
