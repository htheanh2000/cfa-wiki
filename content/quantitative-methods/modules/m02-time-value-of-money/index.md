---
title: "M02 — Time Value of Money"
type: module
subject: quantitative-methods
module: M02
los: ["Pre.i", "Pre.ii", "2.a", "2.b", "1.d", "2.c"]
created: 2026-04-09
updated: 2026-04-09
tags: [tvm, present-value, future-value, annuity, perpetuity, compounding]
---

# Module 2: Time Value of Money in Finance

**Nguồn**: [[quantitative-methods/sources/sapp-quant-2026|SAPP Quant 2026]] pp. 33–112

## Learning Outcomes

| LOS | Mô tả |
|-----|-------------|
| Pre.i | Tính FV và PV của một khoản tiền một lần (lump sum), ordinary annuity, annuity due, perpetuity, và các dòng tiền không đều |
| Pre.ii | Sử dụng timeline để mô hình hóa các bài toán TVM |
| 2.a | PV của các công cụ fixed-income |
| 2.b | PV của các công cụ vốn cổ phần |
| 1.d | Các thước đo lợi suất hàng năm và lợi suất compounding liên tục |
| 2.c | Nguyên tắc cash flow additivity, implied forward rates, forward exchange rates, định giá option |

## Các Khái Niệm Cốt Lõi

### Simple vs Compound Interest

| | Simple Interest | Compound Interest |
|---|---|---|
| **Cơ sở tính** | Chỉ trên vốn gốc | Vốn gốc + lãi tích lũy |
| **Tái đầu tư** | Không | Có |
| **FV sau 4 năm** ($100, 10%) | $140 | $146.41 |

### FV và PV của một Lump Sum

| Phương thức Compounding | Future Value | Present Value |
|-------------|-------------|---------------|
| **Hàng năm** | $FV = PV \times (1+r)^N$ | $PV = \frac{FV}{(1+r)^N}$ |
| **Theo kỳ** $(m$ lần/năm$)$ | $FV = PV \times \left(1+\frac{r}{m}\right)^{N \times m}$ | $PV = \frac{FV}{\left(1+\frac{r}{m}\right)^{N \times m}}$ |
| **Liên tục** | $FV = PV \times e^{r \times N}$ | $PV = \frac{FV}{e^{r \times N}}$ |

trong đó $r$ = lãi suất danh nghĩa hàng năm, $N$ = số năm, $m$ = số kỳ compounding mỗi năm

> **Lưu ý quan trọng**: $FV_{\text{annual}} < FV_{\text{periodic}} < FV_{\text{continuous}}$ — compounding càng thường xuyên → FV càng cao

### Annuities

|  | Ordinary Annuity | Annuity Due |
|--|---|---|
| **Khoản thanh toán đầu tiên** | Tại $t_1$ (cuối kỳ) | Tại $t_0$ (đầu kỳ) |
| **FV** | $FV = PMT \times \frac{(1+r)^N - 1}{r}$ | $FV_{\text{due}} = FV_{\text{ordinary}} \times (1+r)$ |
| **PV** | $PV = PMT \times \frac{1-(1+r)^{-N}}{r}$ | $PV_{\text{due}} = PV_{\text{ordinary}} \times (1+r)$ |

### Perpetuity

$$
PV_0 = \frac{PMT_1}{r}
$$

trong đó $PMT_1$ = khoản thanh toán vào cuối kỳ đầu tiên

Đối với **deferred perpetuity** (khoản thanh toán đầu tiên vào năm thứ $n$):

$$
PV_0 = \frac{PMT}{r} \times \frac{1}{(1+r)^{n-1}}
$$

### Continuous Compounding — Chứng Minh

$$
FV_{\text{continuous}} = \lim_{m \to \infty} PV \times \left(1+\frac{r}{m}\right)^{Nm} = PV \times e^{rN}
$$

Công thức này sử dụng đồng nhất thức toán học: $\lim_{y \to \infty}\left(1+\frac{1}{y}\right)^y = e \approx 2.718$

## Các Phím Chức Năng Máy Tính BA II Plus

| Phím | Chức năng |
|-----|----------|
| **N** | Số kỳ |
| **I/Y** | Lãi suất mỗi kỳ |
| **PV** | Present value (dòng tiền tại $t=0$) |
| **PMT** | Khoản thanh toán mỗi kỳ |
| **FV** | Future value |
| **CPT** | Tính toán biến chưa biết |

> **Quy ước dấu**: Dòng tiền ra (cash outflows) mang dấu âm, dòng tiền vào (inflows) mang dấu dương

## Liên Kết

- Xây dựng từ: [[quantitative-methods/modules/m01-rates-and-returns/index|M01 — Rates and Returns]]
- Liên quan: [[quantitative-methods/concepts/interest-rates|Interest Rates]], [[quantitative-methods/concepts/time-value-of-money|TVM]]
- Ứng dụng trong: [[quantitative-methods/modules/m05-portfolio-mathematics/index|M05 — Portfolio Math]]
- Công thức: [[quantitative-methods/formulas/time-value-of-money|All M02 Formulas]]