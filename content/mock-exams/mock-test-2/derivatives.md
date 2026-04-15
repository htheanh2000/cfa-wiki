---
title: "Derivatives"
type: practice
subject: derivatives
source: "SAPP Mock Test 2"
created: 2026-04-14
updated: 2026-04-15
tags: [mock-test, mock-test-2, derivatives, practice]
---

# Mock Test 2 — Topic 7: Derivatives

**Kết quả**: 1/11 (9%)
**Nguồn**: SAPP CFA1 Revision Mock Test 2
**Liên kết**: [[derivatives/index|Derivatives]]

| Tổng câu | Đúng | Sai | Tỷ lệ |
|----------|------|-----|-------|
| 11 | 1 | 10 | 9% |

---

## Câu 91

**Question 91: For [[derivatives/glossary/der-m02#European option|European option]] prices, a [[derivatives/glossary/der-m04#Replicating portfolio|replicating portfolio]] is required to establish:**

(A) both lower and upper bounds.

(B) lower bounds, but not upper bounds.

(C) upper bounds, but not lower bounds.

> [!answer]- Đáp án
> **(B) lower bounds, but not upper bounds.**
> 
> Bạn chọn: (A) both lower and upper bounds.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (B) lower bounds, but not upper bounds.
> Để xác định giới hạn dưới (lower bounds) của giá quyền chọn kiểu châu Âu ([[derivatives/glossary/der-m02#European option|European option]]), người ta cần xây dựng một [[derivatives/glossary/der-m04#Replicating portfolio|replicating portfolio]] — tức là một danh mục tài sản có cùng [[derivatives/glossary/der-m02#Payoff|payoff]] với quyền chọn, từ đó suy ra giá trị tối thiểu mà quyền chọn phải có để tránh cơ hội [[derivatives/glossary/der-m04#Arbitrage|arbitrage]].
>
> Tuy nhiên, giới hạn trên (upper bounds) lại không cần replicating portfolio: upper bound của European call đơn giản là giá của tài sản cơ sở ([[derivatives/glossary/der-m01#Underlying|underlying]] asset), còn upper bound của European put là giá trị hiện tại (present value) của exercise price.
> Vì vậy, replicating portfolio chỉ cần thiết cho việc xác định lower bounds, không phải upper bounds.

---

## Câu 125

**Question 125: Natalia Coffey enters a [[derivatives/glossary/der-m02#Forward contract|forward contract]] to sell 10,000 shares of Drebin PLC for £120 per share. By entering this contract, Coffey most likely:**

(A) establishes a hedge.

(B) takes on short exposure to the underlying.

(C) agrees to deliver 10,000 shares on the settlement date.

> [!answer]- Đáp án
> **(B) takes on short exposure to the underlying.**
> 
> Bạn chọn: (C) agrees to deliver 10,000 shares on the settlement date.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (B) takes on short exposure to the [[derivatives/glossary/der-m01#Underlying|underlying]].
> Trong [[derivatives/glossary/der-m02#Forward contract|forward contract]], người bán ([[equity-investments/glossary/equity-m01-glossary#Short Position|short position]]) như Coffey đồng ý bán tài sản cơ sở (underlying) ở mức giá định trước.
>
> Nếu giá thị trường giảm xuống dưới £120, Coffey được lợi vì bán được giá cao hơn thị trường — đây là đặc trưng của short exposure.
> Ngược lại, nếu giá tăng vượt £120, Coffey bị thiệt.
>
> Forward contract có thể được dùng để hedging hoặc speculation, và có thể thanh toán bằng giao nhận thực tế (deliverable) hoặc bằng tiền mặt (cash-settled) — việc tham gia hợp đồng không xác định mục đích cụ thể là hedge hay speculate.

---

## Câu 133

**Question 133: A [[derivatives/glossary/der-m10#One-period binomial model|one-period binomial model]] for pricing a [[derivatives/glossary/der-m02#Call option|call option]] with an exercise price of 30.0 has a hedge ratio of 0.4. If the model assumes the [[derivatives/glossary/der-m01#Underlying|underlying]] price is 33.0 after an up-move, the value it assumes for the underlying after a down-move is closest to:**

(A) 25.5.

(B) 28.8

(C) 31.1

> [!answer]- Đáp án
> **(A) 25.5.**
> 
> Bạn chọn: (B) 28.8

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (A) 25.5.
> Trong [[derivatives/glossary/der-m10#Binomial model|binomial model]], hedge portfolio được xây dựng bằng cách mua 0.4 đơn vị [[derivatives/glossary/der-m01#Underlying|underlying]] và bán khống 1 [[derivatives/glossary/der-m02#Call [[derivatives/glossary/der-m02#Option|option]]|call option]], sao cho giá trị portfolio bằng nhau dù giá tăng hay giảm (đây là nguyên lý no-[[derivatives/glossary/der-m04#Arbitrage|arbitrage]]).
>
> Khi giá tăng lên 33.0, call option có giá trị nội tại là 33 – 30 = 3, nên giá trị portfolio sau up-move là 0.4 × 33 – 3 = 13.2 – 3 = 10.20.
> Khi giá giảm xuống mức X (với X < 30, tức call option hết giá trị bằng 0), giá trị portfolio là 0.4 × X – 0 = 10.20, giải ra X = 10.20 / 0.40 = 25.5.
>
> Hai đáp án còn lại (28.8 và 31.1) cho portfolio value khác nhau (lần lượt là 11.52 và 11.34), vi phạm điều kiện no-arbitrage của hedge portfolio.

---

## Câu 137

**Question 137: A 30-day forward rate agreement on 90-day LIBOR is most likely to be used by:**

(A) a lender to lock in an interest rate on a loan it has made to a third party.

(B) a borrower to lock in an interest rate on a loan it will take out in 30 days' time.

(C) an investor to offset the risk of a long position in a zero coupon bond maturing in 90 days.

> [!answer]- Đáp án
> **(B) a borrower to lock in an interest rate on a loan it will take out in 30 days' time.**

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (B) Borrower dùng để lock in lãi suất cho khoản vay trong tương lai.
> Forward rate agreement (FRA) là hợp đồng giữa hai bên để cố định lãi suất cho một khoản vay hoặc tiền gửi giả định trong một khoảng thời gian nhất định bắt đầu vào một ngày trong tương lai.
>
> Một 30-day FRA on 90-day LIBOR nghĩa là bên mua (long) FRA muốn bảo vệ mình khỏi lãi suất tăng trên khoản vay 90 ngày sẽ bắt đầu sau 30 ngày nữa — đây chính xác là nhu cầu của một borrower. [[equity-investments/glossary/equity-m01-glossary#Long Position|Long position]] trên bond và khoản vay đã thực hiện rồi đều không phù hợp vì chúng đã có exposure hiện tại, không phải exposure tương lai mà FRA được thiết kế để hedging.

---

## Câu 142

**Question 142: The price of an existing fixed-for-floating [[derivatives/glossary/der-m07#Interest rate swap|interest rate swap]] will:**

(A) be unaffected by changes in the market reference rate after the swap is initiated.

(B) increase if the market reference rate increases consistently between the first and last settlement date.

(C) increase if the market reference rate decreases consistently between the first and last settlement date.

> [!answer]- Đáp án
> **(A) be unaffected by changes in the market reference rate after the swap is initiated.**
> 
> Bạn chọn: (B) increase if the market reference rate increases consistently between the first and last settlement date.

> [!tip]- 📖 Giải thích chi tiết
> Cần phân biệt rõ price (giá) và value (giá trị) của một [[derivatives/glossary/der-m07#Interest rate swap|interest rate swap]].
> Price của swap là fixed rate được xác định tại thời điểm khởi tạo (initiation) sao cho giá trị ban đầu của hợp đồng bằng 0 — con số này không thay đổi suốt vòng đời của swap.
>
> Trong khi đó, value của swap sẽ biến động theo thời gian khi market [[fixed-income/glossary/fi-m02#Reference rate|reference rate]] thay đổi: nếu lãi suất thị trường tăng, bên trả fixed sẽ có value âm còn bên nhận fixed sẽ có value dương.
> Đáp án (A) đúng vì đề hỏi về price, không phải value.
>
> Đây là điểm dễ nhầm lẫn mà CFA thường khai thác.

---

## Câu 147

**Question 147: If [[derivatives/glossary/der-m09#Put-call parity|put-call parity]] holds, a long asset position, combined with a long [[derivatives/glossary/der-m02#Put option|put option]] and short [[derivatives/glossary/der-m02#Call option|call option]] on the same asset with the same exercise price and expiration date, will have a [[derivatives/glossary/der-m02#Payoff|payoff]] at the expiration date of the options equal to:**

(A) the asset price.

(B) the exercise price of the options.

(C) the exercise price of the options minus the asset price.

> [!answer]- Đáp án
> **(B) the exercise price of the options.**
> 
> Bạn chọn: (C) the exercise price of the options minus the asset price.

> [!tip]- 📖 Giải thích chi tiết
> [[derivatives/glossary/der-m09#Put-call parity|Put-call parity]] phát biểu: S + P = C + PV(X), trong đó S là giá tài sản, P là long put, C là long call, và PV(X) là present value của exercise price.
> Bài toán yêu cầu tính [[derivatives/glossary/der-m02#Payoff|payoff]] của vị thế: long asset + long put + short call, tức là S + P – C.
>
> Từ put-call parity, S + P = C + PV(X), suy ra S + P – C = PV(X).
> Tại ngày đáo hạn, PV(X) = X (không còn chiết khấu), nghĩa là payoff chính xác bằng exercise price bất kể giá tài sản là bao nhiêu.
>
> Đây là nguyên tắc cốt lõi: hai vị thế có cùng chi phí ban đầu phải cho cùng payoff cuối kỳ để tránh [[derivatives/glossary/der-m04#Arbitrage|arbitrage]].

---

## Câu 152

**Question 152: A similarity between [[quantitative-methods/glossary/m01-rates-and-returns#Interest Rate|interest rate]] swaps and credit default swaps is that both:**

(A) are forward commitments.

(B) specify a market reference rate.

(C) have payments based on a notional principal.

> [!answer]- Đáp án
> **(C) have payments based on a notional principal.**
> 
> Bạn chọn: (A) are forward commitments.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (C) have payments based on a [[derivatives/glossary/der-m07#Notional principal|notional principal]].
> Cả [[derivatives/glossary/der-m07#[[quantitative-methods/glossary/m01-rates-and-returns#Interest Rate|Interest rate]] [[derivatives/glossary/der-m02#Swap|swap]]|interest rate swap]] và credit default swap (CDS) đều tính toán các khoản thanh toán dựa trên một giá trị gốc danh nghĩa (notional principal), tức là một số tiền tham chiếu không được trao đổi thực sự giữa hai bên.
>
> Điểm khác biệt là CDS là một [[derivatives/glossary/der-m02#Contingent claim|contingent claim]] vì khoản thanh toán chỉ phát sinh khi xảy ra một sự kiện tín dụng (credit [[quantitative-methods/glossary/m04-probability#Event|event]]) như vỡ nợ, trong khi interest rate swap có các khoản thanh toán định kỳ dựa trên lãi suất cố định và thả nổi.
> Ngoài ra, CDS thông thường không có floating-rate payments nên không cần một market [[fixed-income/glossary/fi-m02#Reference rate|reference rate]].

---

## Câu 158

**Question 158: When put-call-forward parity for European options holds, the present value of the price of a [[derivatives/glossary/der-m02#Forward contract|forward contract]] on an asset:**

(A) plus the value of a put option is equal to the value of a long call option on the same underlying asset plus a long zero coupon risk-free bond with face value equal to the exercise price of the options.

(B) plus the value of a call option is equal to the value of a long call option on the same underlying asset plus a long zero coupon risk-free bond with face value equal to the exercise price of the options.

(C) less the value of a put option is equal to the value of a long call option on the same underlying asset plus a long zero coupon risk-free bond with face value equal to the exercise price of the option.

> [!answer]- Đáp án
> **(A) plus the value of a put option is equal to the value of a long call option on the same underlying asset plus a long zero coupon risk-free bond with face value equal to the exercise price of the options.**
> 
> Bạn chọn: (B) plus the value of a call option is equal to the value of a long call option on the same underlying asset plus a long zero coupon risk-free bond with face value equal to the exercise price of the options.

> [!tip]- 📖 Giải thích chi tiết
> Đáp án đúng: (A) plus the value of a [[derivatives/glossary/der-m02#Put option|put option]] is equal to the value of a long [[derivatives/glossary/der-m02#Call option|call option]] on the same [[derivatives/glossary/der-m01#Underlying|underlying]] asset plus a long zero coupon risk-free bond with face value equal to the exercise price of the options.
> Put-call-forward parity mở rộng [[derivatives/glossary/der-m09#Put-call parity|put-call parity]] thông thường bằng cách thay thế vị thế nắm giữ tài sản bằng một [[derivatives/glossary/der-m02#Forward contract|forward contract]].
>
> Mối quan hệ cân bằng là: PV([[derivatives/glossary/der-m05#Forward price|Forward Price]]) + Put = Call + [[fixed-income/glossary/fi-m02#Zero-coupon bond|Zero-coupon bond]] (mệnh giá = exercise price).
> Vế phải còn được gọi là "[[derivatives/glossary/der-m09#Fiduciary call|fiduciary call]]" — kết hợp một long call với một trái phiếu zero-coupon để đảm bảo đủ tiền thực hiện quyền chọn khi đáo hạn.
>
> Nếu parity này bị vi phạm, sẽ xuất hiện cơ hội [[derivatives/glossary/der-m04#Arbitrage|arbitrage]].

---

## Câu 166

**Question 166: An investor takes a [[equity-investments/glossary/equity-m01-glossary#Long Position|long position]] in a commodity [[derivatives/glossary/der-m02#Forward contract|forward contract]] at a [[derivatives/glossary/der-m05#Forward price|forward price]] of 105 when the [[derivatives/glossary/der-m01#Spot price|spot price]] is 102. One month later the spot price has increased to 110. At that time, the forward price of the contract is:**

(A) 105.

(B) Greater than 110.

(C) Between 105 and 110.

> [!answer]- Đáp án
> **(A) 105.**
> 
> Bạn chọn: (B) Greater than 110.

> [!tip]- 📖 Giải thích chi tiết
> Giá của một [[derivatives/glossary/der-m02#Forward contract|forward contract]] ([[derivatives/glossary/der-m05#Forward price|forward price]]) được cố định ngay tại thời điểm khởi tạo hợp đồng và không thay đổi trong suốt vòng đời của nó — do đó forward price vẫn là 105.
> Điều quan trọng cần phân biệt ở đây là sự khác nhau giữa price (giá) và value (giá trị) của forward contract: price thì cố định, nhưng value thì thay đổi theo thời gian tùy thuộc vào biến động của [[derivatives/glossary/der-m01#Spot price|spot price]].
>
> Khi spot price tăng từ 102 lên 110, value của hợp đồng mua ([[equity-investments/glossary/equity-m01-glossary#Long Position|long position]]) đã tăng lên vì người nắm giữ có quyền mua với giá 105 trong khi thị trường đang giao dịch ở 110, nhưng forward price vẫn là 105.

---

## Câu 175

**Question 175: Which of the following statements regarding the differences between [[quantitative-methods/glossary/m01-rates-and-returns#Interest Rate|interest rate]] swaps and forward rate agreements is most accurate?**

(A) Forward rate agreements are commitments, whereas interest rate swaps are contingent claims.

(B) Forward rate agreements have a single settlement date, whereas interest rate swaps have several settlement dates.

(C) Ignoring transactions costs, forward rate agreements require no upfront payment, whereas interest rate swaps require the payment of an upfront premium.

> [!answer]- Đáp án
> **(B) Forward rate agreements have a single settlement date, whereas interest rate swaps have several settlement dates.**
> 
> Bạn chọn: (C) Ignoring transactions costs, forward rate agreements require no upfront payment, whereas interest rate swaps require the payment of an upfront premium.

> [!tip]- 📖 Giải thích chi tiết
> Điểm khác biệt cốt lõi giữa **forward rate agreement (FRA)** và **[[derivatives/glossary/der-m07#Interest rate swap|interest rate swap]]** là số lần thanh toán: FRA chỉ có duy nhất một lần thanh toán tại ngày đáo hạn, trong khi interest rate swap có nhiều lần thanh toán định kỳ (thường là hàng quý hoặc nửa năm) trong suốt [[fixed-income/glossary/fi-m01#Tenor|tenor]] của hợp đồng.
> Thực chất, một interest rate swap có thể được xem như một chuỗi các FRA ghép lại với nhau.
>
> Cả hai đều là **[[derivatives/glossary/der-m02#Forward commitment|forward commitment]]** và không yêu cầu thanh toán trước (upfront payment), do đó đáp án nào cho rằng một trong hai cần thanh toán ban đầu đều sai.

---

## Câu 179

**Question 179: Consider an investor who writes a put on a share at X for premium of \$5 and an investor who takes a long forward position at X in the same asset for the same period. If ST is the asset price at [[equity-investments/glossary/equity-m01-glossary#Settlement|settlement]], both investors will have the same profit at settlement only if:**

(A) ST – X = \$5.

(B) ST – X ≤ 0.

(C) X – ST = \$5.

> [!answer]- Đáp án
> **(A) ST – X = \$5.**
> 
> Bạn chọn: (C) X – ST = \$5.

> [!tip]- 📖 Giải thích chi tiết
> Lợi nhuận của vị thế **short put** là: 5 − max(0, X − Sᴛ).
> Lợi nhuận của **long forward** là: Sᴛ − X.
>
> Khi put hết hạn out-of-the-money (tức Sᴛ > X), lợi nhuận short put = 5 (put vô giá trị, giữ nguyên premium).
> Để hai lợi nhuận bằng nhau, ta cần: Sᴛ − X = 5, hay Sᴛ = X + 5.
>
> Kiểm tra: lợi nhuận forward = 5, lợi nhuận short put = 5 − 0 = 5.
> Đáp án (A) đúng vì đây là điều kiện duy nhất để cả hai vị thế có cùng profit, không phải mọi giá trị Sᴛ đều thỏa mãn điều này.

---

