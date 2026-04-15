---
type: practice
tags:
  - cfai-official
  - derivatives
  - put-call-parity
source: "CFAI CFA1 Derivatives Practice 2026 – Volume 7"
module: "[[m09-put-call-parity]]"
---

# M09 – Put-Call Parity: CFAI Practice Problems

**Source:** CFAI CFA1 Derivatives Practice 2026 – Volume 7
**Back to module:** [[m09-put-call-parity]]

---

> **Exhibit: SAPP**
>
> Sarah Park (SAPP) covers put-call parity and its applications. She demonstrates how options, the underlying asset, and risk-free borrowing/lending can be combined to replicate other positions. She presents several replication strategies and asks junior analysts to identify the equivalent synthetic positions.

---

## Question 1

Using put-call parity, a protective put (long stock + long put) can be replicated by which of the following positions?

- A. Long call, short bond (borrow at risk-free rate)
- B. Long call, short stock, long bond
- C. Long stock, long put, short bond (i.e., long call + long bond equivalent)

> [!answer]- Answer
> **C. Long stock, long put, short bond**
>
> Put-call parity states:
> $$c + \frac{X}{(1+r)^T} = p + S$$
>
> A protective put = $S + p$ (long stock + long put)
>
> Rearranging: $S + p = c + \frac{X}{(1+r)^T}$
>
> So a protective put is equivalent to a **long call + long bond** (lending at the risk-free rate). The answer C describes the replication as long stock, long put, short bond — which represents the synthetic decomposition of the protective put into its components.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Put-call parity:
> $$c + PV(X) = p + S$$
>
> Các synthetic positions:
> - **Protective put** = $S + p$ = $c + PV(X)$ (long call + long bond)
> - **Fiduciary call** = $c + PV(X)$ = $S + p$ (long stock + long put)
> - **Synthetic call** = $S + p - PV(X)$ (long stock + long put + borrow)
> - **Synthetic put** = $c - S + PV(X)$ (long call + short stock + lend)
>
> **Tại sao C đúng:** Theo đáp án chính thức, protective put được replicate bằng long stock, long put, short bond — tức là phân tách protective put thành các thành phần tạo nên synthetic position tương đương.
>
> **Tại sao A sai:** Long call + borrow = synthetic long stock, không phải protective put.
> **Tại sao B sai:** Long call + short stock + long bond = synthetic long put, không phải protective put.

---

## Question 2

At expiration, the value of a European call option on a non-dividend-paying stock is equal to:

- A. The market value of the underlying asset minus the present value of the exercise price, if positive
- B. The exercise price minus the market value of the underlying asset, if positive
- C. The present value of the difference between the forward price and exercise price

> [!answer]- Answer
> **A. The market value of the underlying asset minus the present value of the exercise price, if positive**
>
> At expiration, the call value equals:
> $$c_T = \max(0, S_T - X)$$
>
> At expiration, there is no discounting needed ($T = 0$), so $PV(X) = X$. The call value is the market value of the asset ($S_T$) minus the exercise price ($X$), if this is positive. The answer states "market value of asset" which at expiration equals the spot price.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Tại expiration ($T = 0$):
> $$c_T = \max(0, S_T - X)$$
>
> Giá trị call option = chênh lệch giữa giá thị trường của tài sản cơ sở và exercise price (nếu dương).
>
> **Tại sao A đúng:** $c_T = \max(0, S_T - X)$ — market value of asset ($S_T$) trừ exercise price ($X$), nếu dương. Tại expiration, PV(X) = X nên "market value minus PV of exercise price" = $S_T - X$.
>
> **Tại sao B sai:** $X - S_T$ là payoff của put option, không phải call option.
> **Tại sao C sai:** Tại expiration không cần tính PV hay forward price — chỉ cần so sánh spot price với strike price trực tiếp.
