---
type: practice
tags:
  - cfai-official
  - derivatives
  - derivatives-benefits-risks
source: "CFAI CFA1 Derivatives Practice 2026 – Volume 7"
module: "[[m05-derivatives-benefits-risks]]"
---

# M05 – Derivatives Benefits and Risks: CFAI Practice Problems

**Source:** CFAI CFA1 Derivatives Practice 2026 – Volume 7
**Back to module:** [[m05-derivatives-benefits-risks]]

---

> **Exhibit: Baywhite Financial**
>
> Baywhite Financial is a multi-strategy asset management firm. The firm's portfolio managers use a variety of derivative instruments across asset classes including equities, fixed income, currencies, and commodities. The firm's risk management team regularly reviews derivative positions to assess hedging effectiveness, mark-to-market gains and losses, and counterparty exposures. The following scenarios describe specific derivative positions and market conditions being evaluated by Baywhite's team.

---

## Question 1

Match each of the following derivative use cases with the most appropriate benefit of derivatives:

| Use Case | |
|---|---|
| 1. A portfolio manager uses equity index futures to quickly increase equity exposure without purchasing individual stocks | |
| 2. An analyst uses option-implied volatility to assess market expectations for future price movements | |
| 3. A corporate treasurer enters into an interest rate swap to convert floating-rate debt to fixed-rate debt | |

Benefits:
- A. Risk management
- B. Operational efficiency
- C. Price discovery / information

> [!answer]- Answer
> **1 → B (Operational efficiency), 2 → C (Price discovery / information), 3 → A (Risk management)**
>
> - Using futures to adjust portfolio exposure quickly and cheaply = operational efficiency
> - Extracting information from option-implied volatility = price discovery / information
> - Converting floating to fixed rate to reduce interest rate uncertainty = risk management

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Ba lợi ích chính của derivatives:
> 1. **Risk management**: Chuyển giao rủi ro không mong muốn (hedging)
> 2. **Operational efficiency**: Thực hiện chiến lược nhanh, rẻ hơn giao dịch trực tiếp trên thị trường cash
> 3. **Price discovery**: Thị trường derivative cung cấp thông tin về kỳ vọng giá tương lai
>
> **Use Case 1 → B:** Dùng futures để tăng equity exposure nhanh chóng thay vì mua từng cổ phiếu → tiết kiệm thời gian và chi phí giao dịch = operational efficiency.
>
> **Use Case 2 → C:** Implied volatility từ options phản ánh kỳ vọng thị trường → price discovery / information.
>
> **Use Case 3 → A:** Chuyển floating-rate thành fixed-rate để loại bỏ rủi ro lãi suất biến động → risk management.

---

## Question 2

Baywhite holds a long forward contract on a commodity. If the spot price of the commodity declines significantly before the contract's settlement date, Baywhite most likely faces:

- A. A gain on the forward contract
- B. A loss because the forward price was set higher than the current spot price
- C. No impact because forward contracts are not marked to market

> [!answer]- Answer
> **B. A loss because the forward price was set higher than the current spot price**
>
> The holder of a long forward is obligated to buy at the predetermined forward price. If the spot price declines, the forward contract has negative value to the long party — they are locked into paying more than the current market price.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Long forward: Nghĩa vụ mua tài sản tại forward price $F_0$ vào ngày settlement.
> - Nếu $S_T < F_0$: Long party lỗ = $S_T - F_0 < 0$ (mua đắt hơn thị trường)
> - Nếu $S_T > F_0$: Long party lãi = $S_T - F_0 > 0$ (mua rẻ hơn thị trường)
>
> **Tại sao B đúng:** Spot price giảm mạnh → $S_T \ll F_0$ → Baywhite phải mua tại giá $F_0$ cao hơn giá thị trường hiện tại → thua lỗ.
>
> **Tại sao A sai:** Long forward lãi khi spot price tăng, không phải giảm.
> **Tại sao C sai:** Mặc dù forward contracts không daily mark-to-market như futures, giá trị hợp đồng vẫn thay đổi và tạo unrealized gain/loss. Tại settlement, lỗ sẽ được hiện thực hóa.

---

## Question 3

Baywhite's Mexico-based subsidiary enters into a forward contract to sell MXN and buy USD at a forward rate of 17.50 MXN/USD. At settlement, the spot rate is 18.00 MXN/USD. MTL (the subsidiary) most likely experiences:

- A. A gain because MXN weakened relative to USD
- B. No gain or loss because the forward rate equals the expected future spot rate
- C. A loss because MTL locked in selling MXN at 17.50 when the market rate moved to 18.00

> [!answer]- Answer
> **C. A loss because MTL locked in selling MXN at 17.50 when the market rate moved to 18.00**
>
> MTL agreed to sell MXN and buy USD at 17.50 MXN/USD. At settlement, the spot rate is 18.00 MXN/USD, meaning MTL could have received 18.00 MXN per USD in the spot market. By being locked into the forward at 17.50, MTL receives fewer MXN per USD than the market rate — a loss on the forward position.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Forward rate lock: Cố định tỷ giá trao đổi. Lãi/lỗ phụ thuộc vào so sánh forward rate với spot rate tại settlement.
>
> **Phân tích chi tiết:**
> - MTL sell MXN, buy USD tại forward rate 17.50 MXN/USD
> - Spot tại settlement: 18.00 MXN/USD (MXN yếu hơn so với kỳ vọng)
> - Nếu MTL giao dịch trên spot market: nhận 18.00 MXN cho mỗi USD bán ra
> - Nhưng forward lock ở 17.50 → MTL "mất" 0.50 MXN/USD so với thị trường
>
> **Tại sao C đúng:** MTL bị khóa ở tỷ giá bất lợi 17.50 thay vì 18.00 → lỗ trên forward contract.
>
> **Tại sao A sai:** MXN yếu đi (18.00 vs 17.50) nhưng MTL đang sell MXN → cần MXN mạnh để có lợi. MXN yếu = bất lợi cho MTL.
> **Tại sao B sai:** Forward rate hiếm khi bằng đúng spot rate tương lai. Kết quả lãi/lỗ phụ thuộc vào chênh lệch thực tế.

---

## Question 4

A portfolio manager uses a derivative position to exactly offset the risk of an existing cash market exposure. At expiration, the combined position (cash + derivative) results in neither a gain nor a loss relative to the hedged price. This outcome is best described as:

- A. An imperfect hedge with basis risk
- B. A speculative position generating excess returns
- C. A breakeven outcome from effective hedging — the derivative offsets the cash position

> [!answer]- Answer
> **C. A breakeven outcome from effective hedging — the derivative offsets the cash position**
>
> When a hedge perfectly offsets the cash position, the combined P&L is zero relative to the hedged price. This is the intended outcome of hedging — locking in a price and eliminating uncertainty, resulting in breakeven reinvestment.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Perfect hedge: Derivative position hoàn toàn bù đắp rủi ro từ cash position → tổng P&L = 0. Đây là mục tiêu của hedging — loại bỏ uncertainty, không phải tạo profit.
>
> **Tại sao C đúng:** Cash position loss = derivative gain (hoặc ngược lại) → net P&L = 0 → breakeven. Đây là kết quả mong muốn khi hedging hiệu quả.
>
> **Tại sao A sai:** Imperfect hedge có basis risk (chênh lệch giữa spot và futures không ổn định) → P&L không bằng 0. Ở đây, hedge hoàn hảo.
> **Tại sao B sai:** Hedging không phải speculation. Mục tiêu là loại bỏ rủi ro, không phải tạo excess returns. Breakeven = thành công.

---

## Question 5

A corporate treasurer expects interest rates (MRR — market reference rate) to rise over the next two years. The company has floating-rate debt tied to MRR. To hedge this exposure, the treasurer should most likely enter a swap as:

- A. A fixed-rate payer (receive floating) — No. Correction: A fixed-rate payer to hedge rising MRR
- B. A floating-rate payer to benefit from rising rates
- C. Neither — swaps cannot hedge interest rate risk

> [!answer]- Answer
> **A. The treasurer should become a fixed-rate payer in an interest rate swap**
>
> Wait — if the company has floating-rate debt and fears rising rates, the treasurer wants to convert floating to fixed. To do this via a swap, the company would **pay fixed and receive floating**. The floating received from the swap offsets the floating paid on the debt, leaving the company with an effective fixed-rate obligation.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Interest rate swap hedging:
> - Có floating-rate debt + lo lãi suất tăng → vào swap **pay fixed, receive floating**
> - Floating nhận từ swap bù floating trả trên debt → net = fixed rate
>
> **Cơ chế:**
> | Dòng tiền | Trước swap | Sau swap |
> |---|---|---|
> | Debt payment | Pay MRR + spread | Pay MRR + spread |
> | Swap: receive | — | + Receive MRR |
> | Swap: pay | — | − Pay fixed rate |
> | **Net** | **MRR + spread** | **Fixed rate + spread** |
>
> **Tại sao A đúng:** Pay fixed, receive floating → convert floating debt thành fixed → bảo vệ khỏi MRR tăng.
>
> **Tại sao B sai:** Pay floating trong swap + pay floating trên debt = double floating exposure → rủi ro tăng gấp đôi khi MRR tăng.
> **Tại sao C sai:** Swap là công cụ hedging interest rate risk phổ biến nhất.

---

## Question 6

Based on current market data, the 1-year spot rate is 1.50% and the 2-year spot rate is 1.65%. The 1-year forward rate one year from now (1y1y forward rate) is closest to:

- A. 1.80%
- B. 1.58%
- C. 1.65%

> [!answer]- Answer
> **A. 1.80%**
>
> Using the no-arbitrage relationship:
> $$(1 + s_2)^2 = (1 + s_1)(1 + f_{1,1})$$
> $$(1.0165)^2 = (1.015)(1 + f_{1,1})$$
> $$1.03322 = 1.015 \times (1 + f_{1,1})$$
> $$1 + f_{1,1} = \frac{1.03322}{1.015} = 1.01800$$
> $$f_{1,1} = 1.80\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Forward rate được tính từ spot rates bằng nguyên tắc no-arbitrage:
> $$(1 + s_n)^n = (1 + s_{n-1})^{n-1} \times (1 + f_{n-1,1})$$
>
> **Tính toán chi tiết:**
> $$f_{1,1} = \frac{(1 + s_2)^2}{(1 + s_1)} - 1 = \frac{(1.0165)^2}{1.015} - 1$$
> $$= \frac{1.033272}{1.015} - 1 = 1.01800 - 1 = 0.0180 = 1.80\%$$
>
> **Tại sao A đúng:** Forward rate 1.80% > spot rate 2 năm 1.65% vì yield curve dốc lên (upward sloping) → forward rate phải cao hơn để "bù đắp" cho giai đoạn sau.
>
> **Tại sao B sai:** 1.58% là trung bình cộng đơn giản $(1.50 + 1.65)/2$ — sai phương pháp.
> **Tại sao C sai:** 1.65% là spot rate 2 năm, không phải forward rate. Forward rate khác spot rate trừ khi yield curve phẳng.
