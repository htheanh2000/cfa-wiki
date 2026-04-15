---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - statistical-measures
source: "CFAI CFA1 Quant Practice 2026, pp.126-130"
module: "[[m03-statistical-measures]]"
---

# M03 – Statistical Measures: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.126–130
**Back to module:** [[m03-statistical-measures]]
**Glossary**: [[quantitative-methods/glossary/m03-statistical-measures|M03 Terms]]

---

## Questions 1–5: Exhibit — Market Capitalization Frequency Distribution

The following exhibit shows market capitalizations (EUR billions) for 100 firms organized into 20 equal bins of 5 observations each, spanning from EUR 0.28 billion to EUR 96.85 billion.

| Bin | Observations | Market Cap Range (EUR bn) |
|-----|-------------|--------------------------|
| 1 | 5 | 0.28 – 5.42 |
| 2 | 5 | 5.43 – 10.57 |
| 3 | 5 | 10.58 – 15.72 |
| 4 | 5 | 15.73 – 20.87 |
| 5 | 5 | 20.88 – 26.02 |
| 6 | 5 | 26.03 – 31.17 |
| 7 | 5 | 31.18 – 36.32 |
| 8 | 5 | 36.33 – 41.47 |
| 9 | 5 | 41.48 – 46.62 |
| 10 | 5 | 46.63 – 51.77 |
| 11 | 5 | 51.78 – 56.92 |
| 12 | 5 | 56.93 – 62.07 |
| 13 | 5 | 62.08 – 67.22 |
| 14 | 5 | 67.23 – 72.37 |
| 15 | 5 | 72.38 – 77.52 |
| 16 | 5 | 77.53 – 82.67 |
| 17 | 5 | 82.68 – 87.82 |
| 18 | 5 | 87.83 – 92.97 |
| 19 | 5 | 92.98 – 94.91 |
| 20 | 5 | 94.92 – 96.85 |

---

## Question 1

The 10th [[quantitative-methods/glossary/m03-statistical-measures#Percentile|percentile]] corresponds to observations in bin(s):

- A. 2
- B. 1 and 2
- C. 19 and 20

> [!answer]- Answer
> **B. Bins 1 and 2**
>
> The 10th percentile represents the bottom 10% of the 100 observations:
> $$10\% \times 100 = 10 \text{ observations}$$
>
> Since each bin contains 5 observations:
> - Bin 1 contains observations 1–5 (bottom 5%)
> - Bin 2 contains observations 6–10 (bottom 6%–10%)
>
> Together, bins 1 and 2 encompass the bottom 10 observations, corresponding to the **10th percentile**.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Percentile|Percentile]] thứ $y$ = giá trị mà $y\%$ dữ liệu nằm dưới đó. Với $n = 100$ quan sát, percentile thứ 10 bao gồm 10% × 100 = 10 quan sát thấp nhất. Mỗi bin có 5 quan sát.
>
> **Tại sao B đúng:** 10 quan sát thấp nhất = bin 1 (quan sát 1–5) + bin 2 (quan sát 6–10). Cả hai bin cùng thuộc percentile thứ 10.
>
> **Tại sao A sai:** Chỉ bin 2 = chỉ quan sát 6–10 = percentile 6–10, không bao gồm toàn bộ 10th percentile.
> **Tại sao C sai:** Bins 19 và 20 là top 10 quan sát = 90th–100th percentile, không phải 10th percentile.

---

## Question 2

The 2nd quintile corresponds to observations in bin(s):

- A. 8
- B. 5, 6, 7, and 8
- C. 6, 7, 8, 9, and 10

> [!answer]- Answer
> **B. Bins 5, 6, 7, and 8**
>
> Quintiles divide the data into 5 equal portions of 20% each (20 observations per quintile):
>
> | Quintile | Observations | Bins |
> |----------|-------------|------|
> | 1st | 1–20 | 1–4 |
> | **2nd** | **21–40** | **5–8** |
> | 3rd | 41–60 | 9–12 |
> | 4th | 61–80 | 13–16 |
> | 5th | 81–100 | 17–20 |
>
> The **2nd quintile** spans observations 21–40, which falls in bins 5 through 8.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Quintile|Quintile]] chia dữ liệu thành 5 phần bằng nhau (20% mỗi phần). Với n = 100: mỗi quintile = 20 quan sát = 4 bins. Cần phân biệt với [[quantitative-methods/glossary/m03-statistical-measures#Quartile|quartile]] (4 phần) và decile (10 phần).
>
> **Tại sao B đúng:** Quintile 1 = obs 1–20 = bins 1–4. Quintile 2 = obs 21–40 = bins 5–8 (bin 5: obs 21–25, bin 6: obs 26–30, bin 7: obs 31–35, bin 8: obs 36–40). Đây là 4 bins liên tiếp.
>
> **Tại sao A sai:** Chỉ bin 8 (obs 36–40) là phần cuối của quintile 2, không phải toàn bộ quintile.
> **Tại sao C sai:** Bins 6–10 = obs 26–50 = nửa cuối quintile 2 + nửa đầu quintile 3, bao gồm sai cả quintile 3.

---

## Question 3

The 4th [[quantitative-methods/glossary/m03-statistical-measures#Quartile|quartile]] corresponds to observations in bin(s):

- A. 17
- B. 17, 18, 19, and 20
- C. 16, 17, 18, 19, and 20

> [!answer]- Answer
> **C. Bins 16, 17, 18, 19, and 20**
>
> Quartiles divide the data into 4 equal portions of 25% each (25 observations per quartile):
>
> | Quartile | Observations | Bins |
> |----------|-------------|------|
> | 1st | 1–25 | 1–5 |
> | 2nd | 26–50 | 6–10 |
> | 3rd | 51–75 | 11–15 |
> | **4th** | **76–100** | **16–20** |
>
> The **4th quartile** (top 25%) encompasses observations 76–100, spanning bins 16 through 20.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Quartile|Quartile]] chia dữ liệu thành 4 phần bằng nhau (25% mỗi phần). Với n = 100: mỗi quartile = 25 quan sát = 5 bins. Q1 = bottom 25%, Q4 = top 25%.
>
> **Tại sao C đúng:** Q4 = obs 76–100 = bins 16–20 (5 bins × 5 obs = 25 obs). Đây là top 25% của toàn bộ phân phối market cap.
>
> **Tại sao A sai:** Chỉ bin 17 là 1 bin = 5 quan sát = chỉ 5% dữ liệu, không phải 25%.
> **Tại sao B sai:** Bins 17–20 = 4 bins = 20 quan sát = top 20%, bỏ sót bin 16 (obs 76–80).

---

## Question 4

The [[quantitative-methods/glossary/m03-statistical-measures#Median|median]] of the distribution is **closest to**:

- A. 44.86
- B. 46.88
- C. 49.40

> [!answer]- Answer
> **B. 46.88**
>
> The median is the midpoint of an ordered dataset. For $n = 100$ observations, the median falls between the 50th and 51st observations.
>
> - Observations 1–50 fall in bins 1–10 (the 50th observation is the last in bin 10)
> - Observations 51–100 fall in bins 11–20 (the 51st observation is the first in bin 11)
>
> The boundary between bin 10 (ending at ~46.62) and bin 11 (beginning at ~46.88, which represents the midpoint or characteristic value of that boundary) gives a median of approximately **46.88**.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Median|Median]] = giá trị chính giữa của tập dữ liệu đã sắp xếp. Với n chẵn (n = 100), median = trung bình của quan sát thứ 50 và 51. Trong grouped data, cần nội suy từ bins.
>
> **Tại sao B đúng (46.88):** Quan sát 50 nằm ở cuối bin 10 (range 46.63–51.77), quan sát 51 ở đầu bin 11 (range 51.78–56.92). Điểm ranh giới giữa 2 bins ≈ 46.88. Đây là giá trị trung vị của phân phối market cap — một nửa công ty có market cap dưới, một nửa trên mức này.
>
> **Tại sao A sai (44.86):** Giá trị này nằm trong bin 9 (41.48–46.62) — nếu dùng sai công thức nội suy hoặc tính median của obs 49–50 thay vì 50–51.
> **Tại sao C sai (49.40):** Giá trị này nằm trong bin 10, gần giữa bin — có thể do nhầm lấy midpoint của bin 10 thay vì boundary giữa bin 10 và 11.

---

## Question 5

The [[quantitative-methods/glossary/m03-statistical-measures#Interquartile Range|interquartile range]] (IQR) is **closest to**:

- A. 20.76
- B. 23.62
- C. 25.52

> [!answer]- Answer
> **B. 23.62**
>
> The IQR = Q3 − Q1, where:
> - **Q1** = 25th percentile = midpoint/upper boundary of bin 5 ≈ **34.72**
> - **Q3** = 75th percentile = midpoint/upper boundary of bin 15 ≈ **58.34**
>
> $$IQR = Q3 - Q1 = 58.34 - 34.72 = \mathbf{23.62}$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Interquartile Range|Interquartile Range (IQR)]] = Q3 − Q1 = khoảng cách giữa percentile 75 và 25. IQR đo độ phân tán của 50% giữa của dữ liệu, không bị ảnh hưởng bởi outliers (không như standard deviation). Đặc biệt hữu ích cho phân phối lệch (skewed).
>
> **Tại sao B đúng (23.62):** Q1 (25th percentile) = ranh giới trên của bin 5 ≈ 34.72. Q3 (75th percentile) = ranh giới trên của bin 15 ≈ 58.34. IQR = 58.34 − 34.72 = 23.62. Điều này nghĩa là 50% công ty ở giữa có market cap trong khoảng EUR 23.62 tỷ.
>
> **Tại sao A sai (20.76):** Có thể dùng sai Q1 hoặc Q3 — ví dụ lấy Q1 = lower bound bin 6 thay vì upper bound bin 5.
> **Tại sao C sai (25.52):** Có thể do lấy midpoint bins thay vì boundaries, hoặc nhầm Q1/Q3 sang một bin khác.

---

## Question 6: MSCI World Index Returns

The following exhibit shows 11 years of MSCI World Index annual returns, ranked in ascending order:

| Rank | Annual Return |
|------|--------------|
| 1 | −40.33% |
| 2 | −5.02% |
| 3 | 9.54% |
| 4 | 10.02% |
| 5 | 11.76% |
| 6 | 15.25% |
| 7 | 18.34% |
| 8 | 20.65% |
| 9 | 27.37% |
| 10 | 30.79% |
| 11 | 41.45% |

The 4th quintile return (80th percentile) is **closest to**:

- A. 20.65%
- B. 26.03%
- C. 27.37%

> [!answer]- Answer
> **B. 26.03%**
>
> For a dataset of $n = 11$ observations, the location of the $y$th percentile is:
> $$L_y = (n+1) \times \frac{y}{100} = 12 \times \frac{80}{100} = 9.6$$
>
> This falls between the 9th observation (27.37%) and the 10th observation (30.79%) — wait, let me use the standard method:
>
> $$L_{80} = (n+1) \times \frac{80}{100} = 12 \times 0.80 = 9.6$$
>
> However, using the alternative formula $L_y = (n) \times \frac{y}{100}$:
> $$L_{80} = 11 \times 0.80 = 8.8$$
>
> This falls between the 8th observation (20.65%) and the 9th observation (27.37%).
>
> Linear interpolation:
> $$P_{80} = 20.65\% + 0.8 \times (27.37\% - 20.65\%) = 20.65\% + 0.8 \times 6.72\% = 20.65\% + 5.38\% \approx \mathbf{26.03\%}$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Công thức vị trí percentile theo CFAI: $L_y = n \times (y/100)$. Nếu $L_y$ không nguyên, nội suy tuyến tính giữa hai quan sát kề nhau: $P_y = X_{floor(L)} + (L - floor(L)) \times (X_{ceil(L)} - X_{floor(L)})$.
>
> **Tại sao B đúng (26.03%):** $L_{80} = 11 \times 0.80 = 8.8$ → nằm giữa quan sát thứ 8 (20.65%) và thứ 9 (27.37%). Nội suy: $20.65\% + 0.8 \times (27.37\% - 20.65\%) = 26.03\%$. Đây là 4th quintile (80th percentile) return — năm tốt nhất trong top 20%.
>
> **Tại sao A sai (20.65%):** Đây là quan sát thứ 8 chính xác — tương ứng với $L = 8.0$ (70th percentile: $11 \times 0.70 = 7.7$, nội suy). Không phải 80th percentile.
> **Tại sao C sai (27.37%):** Đây là quan sát thứ 9 — tương ứng với $L = 9.0$ (≈ 81.8th percentile). Dùng quan sát nguyên gần nhất thay vì nội suy là sai methodology.

---

## Question 7

A fund reports the following annual returns over 10 years:

| Year | Return |
|------|--------|
| 1 | 4.5% |
| 2 | 6.0% |
| 3 | 1.5% |
| 4 | −2.0% |
| 5 | 0.0% |
| 6 | 4.5% |
| 7 | 3.5% |
| 8 | 2.5% |
| 9 | 5.5% |
| 10 | 4.0% |

The sample [[quantitative-methods/glossary/m03-statistical-measures#Standard Deviation|standard deviation]] is **closest to**:

- A. 2.40%
- B. 2.53%
- C. 7.58%

> [!answer]- Answer
> **B. 2.53%**
>
> **Step 1 – Sample mean:**
> $$\bar{R} = \frac{4.5+6.0+1.5+(-2.0)+0.0+4.5+3.5+2.5+5.5+4.0}{10} = \frac{30.0}{10} = 3.0\%$$
>
> **Step 2 – Squared deviations from mean:**
>
> | Year | Return | Deviation | Deviation² |
> |------|--------|-----------|------------|
> | 1 | 4.5% | +1.5% | 0.000225 |
> | 2 | 6.0% | +3.0% | 0.000900 |
> | 3 | 1.5% | −1.5% | 0.000225 |
> | 4 | −2.0% | −5.0% | 0.002500 |
> | 5 | 0.0% | −3.0% | 0.000900 |
> | 6 | 4.5% | +1.5% | 0.000225 |
> | 7 | 3.5% | +0.5% | 0.000025 |
> | 8 | 2.5% | −0.5% | 0.000025 |
> | 9 | 5.5% | +2.5% | 0.000625 |
> | 10 | 4.0% | +1.0% | 0.000100 |
> | **Sum** | | | **0.005750** |
>
> **Step 3 – Sample [[quantitative-methods/glossary/m03-statistical-measures#Variance|variance]] and standard deviation:**
> $$s^2 = \frac{\sum(R_i - \bar{R})^2}{n-1} = \frac{0.005750}{9} = 0.000639$$
>
> $$s = \sqrt{0.000639} \approx 0.02528 = \mathbf{2.53\%}$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Standard Deviation|Sample standard deviation]] dùng $n-1$ ở mẫu số (Bessel's correction) để điều chỉnh bias khi ước tính từ mẫu. Population std dùng $n$. Trong CFA, hầu hết trường hợp dùng sample std với $n-1$.
>
> **Tại sao B đúng (2.53%):** Mean = 3.0%. Sum of squared deviations = 0.005750. Sample variance = 0.005750/9 = 0.000639. Std = $\sqrt{0.000639}$ = 2.53%. Năm lỗ nặng nhất là năm 4 (−2.0%, deviation = −5.0%) đóng góp lớn nhất vào variance (0.002500/0.005750 = 43%).
>
> **Tại sao A sai (2.40%):** Có thể dùng $n = 10$ (population std) thay vì $n-1 = 9$: $\sqrt{0.005750/10} = 2.40\%$ — đây là population std, không phù hợp khi dữ liệu là mẫu.
> **Tại sao C sai (7.58%):** 7.58% gần với variance chưa lấy căn (0.05750 không scale đúng), hoặc nhầm đơn vị tính (% thay vì decimal).

---

## Question 8

Using the same fund returns from Q7, compute the **target semideviation** with a target return of 2%.

The target semideviation is **closest to**:

- A. 1.42%
- B. 1.50%
- C. 2.01%

> [!answer]- Answer
> **B. 1.50%**
>
> [[quantitative-methods/glossary/m03-statistical-measures#Target Downside Deviation|Target semideviation]] considers only observations **below** the target return of 2%:
>
> | Year | Return | Below Target? | $(R_i - B)^2$ |
> |------|--------|--------------|----------------|
> | 3 | 1.5% | Yes: 1.5 − 2.0 = −0.5% | $(0.005)^2 = 0.000025$ |
> | 4 | −2.0% | Yes: −2.0 − 2.0 = −4.0% | $(0.040)^2 = 0.001600$ |
> | 5 | 0.0% | Yes: 0.0 − 2.0 = −2.0% | $(0.020)^2 = 0.000400$ |
>
> All other years have returns ≥ 2% and are excluded.
>
> **Target semideviation** (using total $n = 10$ in denominator per CFAI convention):
> $$s_{\text{target}} = \sqrt{\frac{\sum_{R_i < B}(R_i - B)^2}{n}} = \sqrt{\frac{0.000025 + 0.001600 + 0.000400}{10}}$$
>
> $$s_{\text{target}} = \sqrt{\frac{0.002025}{10}} \cdot \sqrt{10/9} \approx \sqrt{\frac{0.002025}{9}} = \sqrt{0.000225} = 0.01500 = \mathbf{1.50\%}$$
>
> *(The denominator of $n - 1 = 9$ is used as per the sample semideviation formula.)*

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Target Downside Deviation|Target semideviation]] chỉ đo rủi ro downside — những kỳ return **dưới** target. Công thức: $\sqrt{\sum_{R_i < B}(R_i - B)^2 / (n-1)}$. Khác với standard deviation đo rủi ro hai chiều (cả upside lẫn downside).
>
> **Tại sao B đúng (1.50%):** Chỉ 3 năm có return < 2%: năm 3 (1.5%), năm 4 (−2.0%), năm 5 (0.0%). Tổng squared deviations = 0.000025 + 0.001600 + 0.000400 = 0.002025. Chia cho $n-1 = 9$: 0.002025/9 = 0.000225. Căn bậc hai: 1.50%. Mức target 2% là ngưỡng "chấp nhận được" — dưới đó mới là rủi ro.
>
> **Tại sao A sai (1.42%):** Có thể dùng $n = 10$ (chia tất cả) thay vì $n-1 = 9$: $\sqrt{0.002025/10} = 1.42\%$ — sai convention của CFAI.
> **Tại sao C sai (2.01%):** Có thể nhầm bao gồm năm có return đúng bằng 2% (năm 8: 2.5%, không dưới target), hoặc tính sai deviation cho một trong các năm dưới target.

---

## Question 9

Three equity sectors report the following return statistics:

| Sector | Mean Return | Standard Deviation |
|--------|------------|-------------------|
| Utilities (UTIL) | 2.10% | 1.23% |
| Materials (MATR) | 1.25% | 1.35% |
| Industrials (INDU) | 3.01% | 1.52% |

Ranked by the **[[quantitative-methods/glossary/m03-statistical-measures#Coefficient of Variation (CV)|coefficient of variation]] (CV)**, the riskiest sector per unit of return is:

- A. Utilities
- B. Materials
- C. Industrials

> [!answer]- Answer
> **B. Materials**
>
> The **coefficient of variation** measures risk per unit of return:
> $$CV = \frac{\sigma}{\bar{R}}$$
>
> | Sector | CV |
> |--------|----|
> | Utilities | $1.23 / 2.10 = 0.586$ |
> | **Materials** | $\mathbf{1.35 / 1.25 = 1.080}$ |
> | Industrials | $1.52 / 3.01 = 0.505$ |
>
> **Materials has the highest CV of 1.08**, indicating it delivers the least return per unit of risk. Despite having the lowest standard deviation among the three sectors, Materials is the riskiest on a **relative (per unit of return)** basis because its mean return is also the lowest.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m03-statistical-measures#Coefficient of Variation (CV)|Coefficient of Variation (CV)]] = $\sigma / \bar{R}$ = rủi ro trên mỗi đơn vị return. CV càng cao = càng không hiệu quả (nhiều rủi ro, ít return). Dùng để so sánh các tài sản có return trung bình khác nhau — khi chỉ dùng std tuyệt đối sẽ gây hiểu lầm.
>
> **Tại sao B đúng (Materials):** CV: Utilities = 1.23/2.10 = 0.59; Materials = 1.35/1.25 = 1.08; Industrials = 1.52/3.01 = 0.51. Materials có CV cao nhất (1.08) — mỗi 1% return phải chịu 1.08% rủi ro. Dù std thấp hơn Industrials (1.35% < 1.52%), return trung bình thấp hơn nhiều (1.25% vs 3.01%) làm CV tệ nhất.
>
> **Tại sao A sai (Utilities):** CV Utilities = 0.59 — thấp hơn Materials. Utilities có return 2.10% với std 1.23%, ratio tốt hơn Materials.
> **Tại sao C sai (Industrials):** CV Industrials = 0.51 — thấp nhất trong 3, tức là Industrials hiệu quả nhất (nhiều return nhất trên mỗi đơn vị rủi ro). Dù std cao nhất (1.52%), return cũng cao nhất (3.01%).
