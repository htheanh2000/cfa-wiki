---
title: "Practice: M01 — Rates and Returns"
type: practice
subject: quantitative-methods
module: M01
created: 2026-04-09
updated: 2026-04-09
tags: [practice, rates, returns]
---

# Practice: M01 — Rates and Returns

**Module**: [[quantitative-methods/modules/m01-rates-and-returns/index|M01]]
**Formulas**: [[quantitative-methods/formulas/rates-and-returns|Rates and Returns]]
**Glossary**: [[quantitative-methods/glossary/m01-rates-and-returns|M01 Terms]]

---

## Topic 1: Return Measures

**Question 1**: An investor purchased $1,000 of a mutual fund's shares. The fund had the following total returns over a 3-year period: +5%, +8%, +12%. Calculate:
- (a) [[quantitative-methods/glossary/m01-rates-and-returns#Holding Period Return (HPR)|Holding period return]]
- (b) [[quantitative-methods/glossary/m01-rates-and-returns#Arithmetic Mean Return|Arithmetic mean]] annual return
- (c) [[quantitative-methods/glossary/m01-rates-and-returns#Geometric Mean Return|Geometric mean]] annual return
- (d) [[quantitative-methods/glossary/m01-rates-and-returns#Harmonic Mean|Harmonic mean]] annual return

> [!answer]- Answer
> (a) $HPR = (1.05)(1.08)(1.12) - 1 = 27\%$
> (b) $\bar{R} = \frac{5\% + 8\% + 12\%}{3} = 8.33\%$
> (c) $\bar{R}_G = \sqrt[3]{(1.05)(1.08)(1.12)} - 1 = 8.29\%$
> (d) $\bar{X}_H = \frac{3}{\frac{1}{1.05} + \frac{1}{1.08} + \frac{1}{1.12}} - 1 = 8.26\%$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Câu hỏi kiểm tra 4 cách đo lường lợi suất đa kỳ — mỗi cách có ý nghĩa khác nhau:
> - **HPR** (Holding Period Return): lợi suất tổng cộng qua toàn bộ 3 năm. Nhân chuỗi $(1+R)$ rồi trừ 1.
> - **Arithmetic Mean**: trung bình cộng đơn giản — là ước lượng không chệch (unbiased) của lợi suất kỳ vọng thực, nhưng KHÔNG phản ánh đúng tăng trưởng gộp.
> - **Geometric Mean**: trung bình nhân — đo tốc độ tăng trưởng gộp thực tế. Luôn ≤ arithmetic mean (bằng nhau chỉ khi mọi lợi suất giống nhau).
> - **Harmonic Mean**: nghịch đảo của trung bình cộng các nghịch đảo — luôn ≤ geometric mean.
> 
> **Quan hệ quan trọng cần nhớ:** $\bar{R}_H \leq \bar{R}_G \leq \bar{R}$ (Harmonic ≤ Geometric ≤ Arithmetic)

---

**Question 2**: The [[quantitative-methods/glossary/m01-rates-and-returns#Harmonic Mean|harmonic mean]] is **most appropriate** for averaging:

A. Time-series returns
B. Price-to-earnings (P/E) ratios
C. Standard deviations

> [!answer]- Answer
> **B.** Harmonic mean is used most often when data consists of rates and ratios (e.g., P/E). A well-known application is **dollar cost averaging**.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Harmonic Mean|Harmonic mean]] cho trọng số bằng nhau cho mỗi đơn vị đầu tư, phù hợp khi dữ liệu là tỷ lệ (ratio).
> 
> **Tại sao B đúng:** Khi tính trung bình P/E của nhiều cổ phiếu, harmonic mean giảm ảnh hưởng của outlier (cổ phiếu P/E cực cao). Ví dụ: nếu 10 cổ phiếu có P/E từ 7.20 đến 22.29, harmonic mean = 10.82 — thấp hơn arithmetic mean vì giảm trọng số các giá trị lớn.
> 
> **Tại sao A sai:** Time-series returns dùng geometric mean (đo tăng trưởng gộp) hoặc arithmetic mean (ước lượng kỳ vọng).
> 
> **Tại sao C sai:** Standard deviations không phải ratio — dùng arithmetic mean hoặc phương pháp pooling.

---

## Topic 2: MWR vs TWR

**Question 3**: An investor buys a share at $100 at t=0, buys another at $120 at t=1. At t=2, sells both for $130 each. Dividend of $2 per share each year. What is the [[quantitative-methods/glossary/m01-rates-and-returns#Money-Weighted Return (MWR)|money-weighted return]]?

> [!answer]- Answer
> Cash flows: $CF_0 = -100$, $CF_1 = +2 - 120 = -118$, $CF_2 = 260 + 4 = 264$
> Solve: $-100 + \frac{-118}{(1+r)} + \frac{264}{(1+r)^2} = 0$
> $IRR = 13.86\%$ → $MWR = 13.86\%$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Money-Weighted Return (MWR)|MWR]] chính là IRR (Internal Rate of Return) của toàn bộ dòng tiền vào/ra portfolio. Nó bị ảnh hưởng bởi thời điểm và quy mô dòng tiền.
> 
> **Cách giải:**
> 1. Liệt kê dòng tiền: t=0 mua 1 cổ phiếu (−$100), t=1 nhận cổ tức +$2 nhưng mua thêm −$120 (net = −$118), t=2 bán 2 cổ phiếu +$260 và nhận cổ tức +$4 (net = +$264)
> 2. Giải IRR bằng máy tính BA II Plus: CF₀=−100, CF₁=−118, CF₂=+264, CPT IRR = 13.86%
> 
> **So sánh với TWR:** TWR sẽ khác vì không bị ảnh hưởng bởi việc mua thêm cổ phiếu ở t=1. MWR phản ánh trải nghiệm thực tế của nhà đầu tư, TWR phản ánh kỹ năng quản lý quỹ.

---

## Topic 3: Measurements for Special Assets

**Question 4**: A security portfolio earns a [[quantitative-methods/glossary/m01-rates-and-returns#Gross Return|gross return]] of 7.0% and a [[quantitative-methods/glossary/m01-rates-and-returns#Net Return|net return]] of 6.5%. The difference of 0.5% most likely results from:

A. Inflation
B. Fees
C. Taxes

> [!answer]- Answer
> **B.** Net return = Gross return − Fees. The 0.5% difference represents management fees and expenses.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Chuỗi các loại lợi suất từ cao → thấp:
> - [[quantitative-methods/glossary/m01-rates-and-returns#Gross Return|Gross return]]: lợi suất trước phí quản lý (nhưng SAU phí giao dịch — trading expenses đã tính trong gross)
> - [[quantitative-methods/glossary/m01-rates-and-returns#Net Return|Net return]]: gross return − phí quản lý/hành chính
> - [[quantitative-methods/glossary/m01-rates-and-returns#After-Tax Return|After-tax return]]: net return × (1 − thuế suất)
> - [[quantitative-methods/glossary/m01-rates-and-returns#Real Return|Real return]]: sau khi trừ lạm phát
> 
> **Tại sao B đúng:** Chênh lệch giữa gross và net = phí quản lý và hành chính (management & administrative fees).
> 
> **Tại sao A sai:** Inflation ảnh hưởng đến real return, không phải chênh lệch gross-net.
> 
> **Tại sao C sai:** Taxes ảnh hưởng đến after-tax return, không phải chênh lệch gross-net.

---

**Question 5**: The value of an investment increases 5% before commissions and fees. This 5% increase represents:

A. The investment's [[quantitative-methods/glossary/m01-rates-and-returns#Net Return|net return]]
B. The investment's [[quantitative-methods/glossary/m01-rates-and-returns#Gross Return|gross return]]
C. Neither the investment's gross return nor its net return

> [!answer]- Answer
> **B.** Gross return is the return before deducting fees and commissions.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** "Trước commissions và fees" = gross return. Đây là lợi suất mà fund manager tạo ra, chưa trừ các khoản phí mà nhà đầu tư phải trả.
> 
> **Tại sao A sai:** Net return = gross return − phí → luôn thấp hơn gross return.
> 
> **Tại sao C sai:** 5% trước phí chính xác là định nghĩa của gross return.
> 
> **Lưu ý:** Gross return thường dùng để đánh giá kỹ năng fund manager vì nó loại bỏ các khoản phí mà manager không kiểm soát được.

---

**Question 6**: The strategy of using leverage to enhance investment returns:

A. Amplifies gains but not losses
B. Doubles the net return if half of the invested capital is borrowed
C. Increases total investment return only if the return earned exceeds the borrowing cost

> [!answer]- Answer
> **C.** [[quantitative-methods/glossary/m01-rates-and-returns#Leveraged Return|Leveraged return]]: $R_L = R_p + \frac{V_B}{V_E}(R_p - r_D)$. Leverage only increases return when $R_p > r_D$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m01-rates-and-returns#Leveraged Return|Leveraged return]] = lợi suất khi dùng vốn vay để đầu tư. Công thức: $R_L = R_p + \frac{V_B}{V_E}(R_p - r_D)$
> - $R_p$ = lợi suất danh mục, $V_B$ = vốn vay, $V_E$ = vốn tự có, $r_D$ = chi phí vay
> 
> **Tại sao C đúng:** Phần $(R_p - r_D)$ quyết định: nếu $R_p > r_D$ → leverage tăng lợi suất; nếu $R_p < r_D$ → leverage GIẢM lợi suất (lỗ thêm).
> 
> **Tại sao A sai:** Leverage khuếch đại CẢ lãi VÀ lỗ. Ví dụ: portfolio lỗ 5%, vay 50% vốn → leveraged return = −5% + 0.5×(−5%−6%) = −10.5% (lỗ nặng hơn).
> 
> **Tại sao B sai:** Nếu vay 50% vốn, gross return được nhân đôi nhưng net return thì KHÔNG — vì phải trừ chi phí vay. Chỉ khi chi phí vay = 0% thì B mới đúng (không thực tế).
