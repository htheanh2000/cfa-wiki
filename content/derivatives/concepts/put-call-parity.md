---
title: Put-Call Parity
type: concept
subject: derivatives
module: "M09"
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, options, put-call-parity, synthetic, fiduciary-call, protective-put]
---

# Put-Call Parity

## Mối Quan Hệ Cốt Lõi

Put-call parity liên kết giá của các European call và put option có cùng strike price và ngày đáo hạn trên cùng một tài sản cơ sở.

### Protective Put

**Protective put** = long stock + long put:

$$\text{Payoff} = S_T + \max(0,\; X - S_T) = \max(S_T,\; X)$$

### Fiduciary Call

**Fiduciary call** = long call + trái phiếu phi rủi ro với mệnh giá $X$:

$$\text{Payoff} = \max(0,\; S_T - X) + X = \max(S_T,\; X)$$

### Công Thức Parity

Vì cả hai danh mục đều tạo ra payoff giống hệt nhau trong mọi trạng thái:

$$\boxed{S_0 + p_0 = c_0 + \frac{X}{(1+r)^T}}$$

trong đó:
- $S_0$ = giá cổ phiếu hiện tại
- $p_0$ = phí bảo hiểm European put
- $c_0$ = phí bảo hiểm European call
- $X$ = strike price (như nhau cho cả hai option)
- $r$ = lãi suất phi rủi ro
- $T$ = thời gian đến ngày đáo hạn

> Put-call parity chỉ chính xác tuyệt đối với **European** option trên tài sản không trả cổ tức.

---

## Các Vị Thế Synthetic

Bằng cách sắp xếp lại công thức parity, ta có thể tạo ra các vị thế **synthetic**:

### Synthetic Call

$$c_0 = S_0 + p_0 - \frac{X}{(1+r)^T}$$

Long stock + long put + vay PV của strike = synthetic long call

### Synthetic Put

$$p_0 = c_0 - S_0 + \frac{X}{(1+r)^T}$$

Long call + short stock + cho vay PV của strike = synthetic long put

### Synthetic Stock (Long)

$$S_0 = c_0 - p_0 + \frac{X}{(1+r)^T}$$

Long call + short put + cho vay PV của strike = synthetic long stock

### Synthetic Risk-Free Bond

$$\frac{X}{(1+r)^T} = S_0 + p_0 - c_0$$

Long stock + long put + short call = synthetic risk-free bond (covered call + long put)

---

## Put-Call Forward Parity

Khi tài sản cơ sở là một **forward contract** thay vì tài sản giao ngay:

$$\boxed{\frac{F_0(T)}{(1+r)^T} + p_0 = c_0 + \frac{X}{(1+r)^T}}$$

Sắp xếp lại:

$$p_0 - c_0 = \frac{X - F_0(T)}{(1+r)^T}$$

**Diễn giải**:
- Nếu $F_0(T) = X$: put và call có cùng giá ($p_0 = c_0$)
- Nếu $F_0(T) > X$: call có giá trị hơn put
- Nếu $F_0(T) < X$: put có giá trị hơn call

---

## Ứng Dụng Trong Corporate Finance

Put-call parity có một sự tương đồng mạnh mẽ trong corporate finance (**mô hình Merton**):

| Khái Niệm Option | Tương Đương Trong Corporate Finance |
|---|---|
| Stock ($S$) | Tổng tài sản của doanh nghiệp ($A$) |
| Strike ($X$) | Mệnh giá nợ ($D$) |
| Call option | Vốn chủ sở hữu (quyền nhận phần còn lại) |
| Put option | Quyền chọn vỡ nợ (trách nhiệm hữu hạn) |
| Risk-free bond | Nợ phi rủi ro |

$$\text{Equity} = \text{Call on firm assets with strike} = D$$

- **Cổ đông** sở hữu một call trên tài sản doanh nghiệp với strike = mệnh giá nợ
- **Trái chủ** sở hữu nợ phi rủi ro nhưng đã bán một put cho cổ đông
- **Trách nhiệm hữu hạn** = put option của cổ đông (có thể bỏ đi nếu tài sản < nợ)

---

## Arbitrage Với Put-Call Parity

Nếu parity bị vi phạm, cơ hội arbitrage xuất hiện:

**Nếu $S_0 + p_0 > c_0 + \frac{X}{(1+r)^T}$** (vế trái bị định giá cao):
- Bán protective put: short stock, bán put
- Mua fiduciary call: mua call, cho vay PV của $X$
- Thu về lợi nhuận phi rủi ro

**Nếu $S_0 + p_0 < c_0 + \frac{X}{(1+r)^T}$** (vế phải bị định giá cao):
- Mua protective put: mua stock, mua put
- Bán fiduciary call: bán call, vay PV của $X$
- Thu về lợi nhuận phi rủi ro

---

## Xem Thêm

- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/concepts/option-valuation|Option Valuation]]
- [[derivatives/concepts/arbitrage-and-replication|Arbitrage and Replication]]
- [[derivatives/formulas/der-formulas|Derivatives Formula Sheet]]
- [[derivatives/glossary/der-m09|Glossary — M09]]