---
type: practice
tags:
  - cfai-official
  - derivatives
  - option-valuation
source: "CFAI CFA1 Derivatives Practice 2026 – Volume 7"
module: "[[m08-option-valuation]]"
---

# M08 – Option Valuation: CFAI Practice Problems

**Source:** CFAI CFA1 Derivatives Practice 2026 – Volume 7
**Back to module:** [[m08-option-valuation]]

---

> **Exhibit: SAPP**
>
> Sarah Park (SAPP) continues her derivatives training by covering option valuation concepts. She discusses the factors affecting option values, the boundaries on option prices, and the impact of changes in key variables (underlying price, risk-free rate, volatility, time to expiration) on call and put option values.

---

## Question 1

The minimum value of a European put option at expiration is:

- A. Zero
- B. The underlying price minus the exercise price
- C. The greater of zero or the exercise price minus the underlying price

> [!answer]- Answer
> **C. The greater of zero or the exercise price minus the underlying price**
>
> At expiration, a European put option's value equals its intrinsic value:
> $$p_T = \max(0, X - S_T)$$
> If $S_T < X$, the put is in the money and worth $X - S_T$. If $S_T \geq X$, the put expires worthless (value = 0). The minimum value is the greater of zero or $X - S_T$.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Payoff tại expiration:
> - **Call**: $c_T = \max(0, S_T - X)$
> - **Put**: $p_T = \max(0, X - S_T)$
>
> Option value không bao giờ âm (negative) vì holder có quyền không exercise.
>
> **Tại sao C đúng:** Put option payoff = $\max(0, X - S_T)$. Đây chính xác là "greater of zero or exercise price minus underlying price."
>
> **Tại sao A sai:** Zero chỉ là giá trị khi put OTM ($S_T \geq X$). Khi ITM, put có giá trị dương.
> **Tại sao B sai:** $S_T - X$ là payoff của call option, không phải put. Put payoff = $X - S_T$ (ngược lại).

---

## Question 2

All else being equal, an increase in the risk-free rate will most likely cause the value of a European put option to:

- A. Decrease
- B. Increase
- C. Remain unchanged

> [!answer]- Answer
> **A. Decrease**
>
> An increase in the risk-free rate reduces the present value of the exercise price, which is the maximum payoff a put holder can receive. Since the put holder benefits from receiving $X$ at expiration, a higher discount rate reduces the present value of this payoff, decreasing the put's value.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Tác động của risk-free rate ($r$) lên option values:
>
> | Factor tăng | Call value | Put value |
> |---|---|---|
> | $r$ tăng | Tăng ↑ | Giảm ↓ |
> | $r$ giảm | Giảm ↓ | Tăng ↑ |
>
> **Intuition:**
> - Put holder nhận $X$ khi exercise → PV of $X$ = $\frac{X}{(1+r)^T}$
> - $r$ tăng → $PV(X)$ giảm → put value giảm
>
> **Cách nhớ qua put-call parity:**
> $$p = c - S + \frac{X}{(1+r)^T}$$
> $r$ tăng → $\frac{X}{(1+r)^T}$ giảm → $p$ giảm (giữ nguyên các yếu tố khác)
>
> **Tại sao A đúng:** Risk-free rate tăng → PV of exercise price giảm → put value giảm.
>
> **Tại sao B sai:** Put value giảm (không tăng) khi $r$ tăng.
> **Tại sao C sai:** Risk-free rate là một factor ảnh hưởng đến option value — không phải unchanged.
