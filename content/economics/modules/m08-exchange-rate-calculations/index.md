---
title: "M08 — Exchange Rates"
type: module
subject: economics
module: M08
los: ["8.a", "8.b", "8.c"]
created: 2026-04-10
updated: 2026-04-10
tags: [economics, exchange-rates, forward-rates, cross-rates]
---

# M08: Exchange Rate Calculations

## Learning Outcomes
- **8.a**: Tính toán và diễn giải cross rates giữa các đồng tiền
- **8.b**: Giải thích mối quan hệ arbitrage giữa spot exchange rates, forward exchange rates và lãi suất
- **8.c**: Tính toán và diễn giải forward discount hoặc forward premium; chuyển đổi các báo giá forward được biểu thị theo points basis hoặc theo phần trăm

## Key Concepts

### Exchange Rate Quotations
- **Direct quote** (price currency/base currency): Đồng tiền nội địa trên mỗi đơn vị đồng tiền nước ngoài
- **Indirect quote**: Đồng tiền nước ngoài trên mỗi đơn vị đồng tiền nội địa
- **Bid-ask spread**: $\text{Ask} - \text{Bid}$; đại diện cho lợi nhuận của dealer

### Cross Rates
Để tìm $A/C$ khi biết $A/B$ và $B/C$:
$$\frac{A}{C} = \frac{A}{B} \times \frac{B}{C}$$

### Covered Interest Rate Parity
$$\frac{F_{A/B}}{S_{A/B}} = \frac{1 + r_A}{1 + r_B}$$

trong đó $F$ = forward rate, $S$ = spot rate, $r_A$ và $r_B$ = lãi suất tương ứng

### Forward Premium/Discount
$$\text{Forward premium (discount)} = \frac{F - S}{S} \times \frac{360}{\text{days}}$$

- **Premium**: Forward rate > Spot rate (base currency được kỳ vọng sẽ tăng giá)
- **Discount**: Forward rate < Spot rate (base currency được kỳ vọng sẽ giảm giá)

### Forward Points
$$F = S + \text{Forward points}$$

Forward points được biểu thị dưới dạng pips hoặc phần trăm của spot rate.

## Related Pages
- [[economics/concepts/exchange-rates|Exchange Rates]]
- [[economics/formulas/economics-international|International Economics Formulas]]
- [[economics/glossary/econ-m08-exchange-rate-calculations|Glossary: M08]]