---
title: "Practice: M02 — Time Value of Money"
type: practice
subject: quantitative-methods
module: M02
created: 2026-04-09
updated: 2026-04-09
tags: [practice, tvm, pv, fv, annuity]
---

# Practice: M02 — Time Value of Money

**Module**: [[quantitative-methods/modules/m02-time-value-of-money/index|M02]]
**Formulas**: [[quantitative-methods/formulas/time-value-of-money|TVM Formulas]]
**Glossary**: [[quantitative-methods/glossary/m02-time-value-of-money|M02 Terms]]

---

## Topic 1: FV and PV of Lump Sum

**Question 1**: A pension fund manager estimates a $10M contribution 5 years from now. Rate of return is 9%. What is the [[quantitative-methods/glossary/m02-time-value-of-money#Future Value (FV)|FV]] at year 15 (10 years after contribution)?

> [!answer]- Answer
> Annual compounding: $FV_{10} = PV \times (1+r)^N = 10 \times (1.09)^{10} = \$23.67M$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Future Value (FV)|Future Value (FV)]] là giá trị tương lai của một khoản tiền hiện tại khi được tích lũy với lãi suất nhất định. Công thức: $FV = PV \times (1+r)^N$.
>
> **Tại sao đáp án đúng:** Câu hỏi có hai mốc thời gian — khoản đóng góp $10M xảy ra ở năm 5, và cần tính FV tại năm 15 (tức là 10 năm sau đó). Vì vậy $N = 10$ (không phải 15). Áp dụng: $10 \times (1.09)^{10} = \$23.67M$.
>
> **Lưu ý quan trọng:** Đây là bài tập kinh điển về "mốc thời gian kép" — luôn xác định rõ khoảng cách giữa thời điểm bắt đầu và kết thúc tính lãi, không nhầm với mốc tuyệt đối trên trục thời gian.

---

**Question 2**: Given a [[quantitative-methods/glossary/m02-time-value-of-money#Present Value (PV)|discount rate]] of 10%, calculate the PV of a $200 cash flow to be received in 2 years. Interest is [[quantitative-methods/glossary/m02-time-value-of-money#Compounding|compounded]] quarterly.

> [!answer]- Answer
> $PV = \frac{FV}{(1+\frac{r}{m})^{N \times m}} = \frac{200}{(1+\frac{0.10}{4})^{2 \times 4}} = \frac{200}{(1.025)^8} = \$164.15$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Compounding|Compounding]] theo kỳ (periodic compounding) điều chỉnh lãi suất năm theo số kỳ ghép lãi trong năm. Khi lãi ghép theo quý: lãi suất mỗi kỳ = $r/m$, tổng số kỳ = $N \times m$.
>
> **Tại sao đáp án đúng:** Lãi suất năm 10% ghép theo quý ($m = 4$) → lãi suất quý = $10\%/4 = 2.5\%$. Thời gian 2 năm = $2 \times 4 = 8$ kỳ. Do đó: $PV = \frac{200}{(1.025)^8} = \$164.15$.
>
> **Lưu ý:** Ghép lãi càng nhiều lần trong năm → PV càng nhỏ hơn (vì lãi tích lũy nhanh hơn, giá trị hiện tại của cùng một FV sẽ thấp hơn so với ghép lãi năm).

---

## Topic 2: Annuity and Perpetuity

**Question 3**: Calculate the FV and PV of a 3-year [[quantitative-methods/glossary/m02-time-value-of-money#Ordinary Annuity|ordinary annuity]] of $100/year at 10%.

> [!answer]- Answer
> $FV = 100 \times \frac{(1.10)^3 - 1}{0.10} = \$331$
> $PV = 100 \times \frac{1 - (1.10)^{-3}}{0.10} = \$248.69$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Ordinary Annuity|Ordinary annuity]] là chuỗi thanh toán đều đặn vào **cuối** mỗi kỳ. Công thức FV và PV có dạng nhân hệ số annuity với khoản thanh toán định kỳ (PMT).
>
> **Tại sao đáp án đúng:**
> - FV annuity: tính tổng giá trị tương lai tại cuối năm 3 của 3 khoản $100. Khoản năm 1 được ghép lãi 2 năm, năm 2 ghép 1 năm, năm 3 không ghép → tổng = $110 + $121 + $100 = $331.
> - PV annuity: chiết khấu mỗi khoản $100 về hiện tại và cộng lại → $90.91 + $82.64 + $75.13 = $248.69.
>
> **Phân biệt Ordinary Annuity vs Annuity Due:** Annuity due thanh toán vào **đầu** kỳ → FV và PV cao hơn ordinary annuity một hệ số $(1+r)$.

---

**Question 4**: Kodon Corporation issues preferred stock paying $4.50/year in dividends beginning 4 years from now, forever. Rate of return = 8%. What is the value today?

> [!answer]- Answer
> Step 1: $PV_{\text{perpetuity (year 3)}} = \frac{4.50}{0.08} = \$56.25$
> Step 2: $PV_{\text{today}} = \frac{56.25}{(1.08)^3} = \$44.65$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Perpetuity|Perpetuity]] là dòng tiền vĩnh viễn đều đặn mỗi kỳ. $PV = \frac{PMT}{r}$. Điều quan trọng: công thức này cho ra PV tại **một kỳ trước** khoản thanh toán đầu tiên.
>
> **Tại sao đáp án đúng:** Dividend bắt đầu từ năm 4, nên $PV = \frac{4.50}{0.08}$ cho giá trị tại **cuối năm 3** (một kỳ trước năm 4). Sau đó chiết khấu $56.25 về hôm nay qua 3 năm: $\frac{56.25}{(1.08)^3} = \$44.65$.
>
> **Bẫy thường gặp:** Nhiều người nhầm chiết khấu về năm 4 thay vì năm 3, hoặc dùng $N = 4$ thay vì $N = 3$. Nhớ: công thức perpetuity luôn cho PV tại kỳ **ngay trước** dòng tiền đầu tiên.

---

## Topic 3: Cash Flow Additivity

**Question 5**: An investor purchases a stock on January 1. Annual dividends for 4 years: $50, $75, $100, $125. Based on [[quantitative-methods/glossary/m02-time-value-of-money#Cash Flow Additivity|cash flow additivity]], the PV is equivalent to a $50 annuity plus:

A. $0, $0, $125, and $125
B. $75, $50, $25, and $0
C. $0, $25, $50, and $75

> [!answer]- Answer
> **C.** Subtract $50 from each: $50+0, $50+25, $50+50, $50+75. The PV equals a $50 annuity plus PV of ($0, $25, $50, $75).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Cash Flow Additivity|Cash flow additivity]] phát biểu rằng PV của một chuỗi dòng tiền bằng tổng PV của từng dòng tiền riêng lẻ. Điều này cho phép tách một chuỗi phức tạp thành các phần đơn giản hơn.
>
> **Tại sao C đúng:** Dòng tiền gốc: $50, $75, $100, $125. Tách mỗi khoản thành $50 + phần còn lại: ($50+$0), ($50+$25), ($50+$50), ($50+$75). Phần $50 mỗi năm chính là một ordinary annuity. Phần còn lại là chuỗi $0, $25, $50, $75 — đúng với đáp án C.
>
> **Tại sao A sai:** $0, $0, $125, $125 — không khớp khi cộng lại: năm 1 = $50+$0 = $50 ✓ nhưng năm 3 = $50+$125 = $175 ✗ (phải là $100).
>
> **Tại sao B sai:** $75, $50, $25, $0 — năm 1 = $50+$75 = $125 ✗ (phải là $50).

---

**Question 6**: The current exchange rate is USD/EUR 1.025. Risk-free rates: EUR 0.75%, USD 3.25%. The 1-year [[quantitative-methods/glossary/m02-time-value-of-money#Implied Forward Rate|forward rate]] that best prevents arbitrage is:

A. USD/EUR 1.051
B. USD/EUR 1.025
C. USD/EUR 0.975

> [!answer]- Answer
> **A.** Forward = Spot × $\frac{(1+r_{USD})}{(1+r_{EUR})} = 1.025 \times \frac{1.0325}{1.0075} = 1.0504 \approx 1.051$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m02-time-value-of-money#Implied Forward Rate|Implied forward rate]] (trong ngoại hối) là tỷ giá kỳ hạn ngụ ý từ ngang giá lãi suất (Interest Rate Parity). Nguyên tắc: không có cơ hội arbitrage khi tỷ giá kỳ hạn phản ánh chênh lệch lãi suất giữa hai đồng tiền.
>
> **Tại sao A đúng:** Tỷ giá kỳ hạn = Spot × (1 + lãi suất đồng tiền định giá) / (1 + lãi suất đồng tiền cơ sở). USD/EUR nghĩa là 1 EUR = X USD, EUR là base currency, USD là price currency. Forward = $1.025 \times \frac{1.0325}{1.0075} \approx 1.051$.
>
> **Tại sao B sai:** Tỷ giá 1.025 giữ nguyên không phản ánh chênh lệch lãi suất — sẽ tạo cơ hội arbitrage (vay EUR lãi thấp, đổi sang USD, đầu tư lãi cao hơn).
>
> **Tại sao C sai:** 0.975 là chiều ngược lại — tỷ giá USD/EUR không thể giảm khi USD có lãi suất cao hơn (USD phải depreciate kỳ hạn để ngăn arbitrage, tức là EUR lên giá so với USD → tỷ giá USD/EUR tăng).
