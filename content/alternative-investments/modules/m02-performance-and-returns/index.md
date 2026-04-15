---
title: "M02 — Performance & Returns"
type: module
subject: alternative-investments
module: m02-performance-and-returns
los:
  - 2.a
  - 2.b
created: 2026-04-12
updated: 2026-04-12
tags:
  - module
  - alternative-investments
  - performance
  - returns
  - j-curve
  - IRR
  - MOIC
  - CFA-L1
---

# M02 – AI Performance and Returns

> **LOS 2.a–2.b** | Pages 167+ | Source: [[alternative-investments/sources/sapp-ai-2026|SAPP 2026]]
>
> *Được đặt cuối trong thứ tự học SAPP.*

---

## 1. Thách Thức Trong Đo Lường Hiệu Suất (LOS 2.a)

Đo lường hiệu suất của alternative investment khó hơn so với các tài sản truyền thống do:

| Thách thức | Mô tả |
|-----------|-------------|
| **Timing of cash flows** | Capital calls và phân phối không đều; không có lịch cố định |
| **Leverage** | Khuếch đại lợi nhuận và rủi ro; gây khó khăn khi so sánh với các benchmark không dùng đòn bẩy |
| **Không có giá thị trường quan sát được** | Tài sản kém thanh khoản không có báo giá hằng ngày; phụ thuộc vào thẩm định giá |
| **Cấu trúc phí phức tạp** | Nhiều lớp phí ảnh hưởng đến việc so sánh gross và net |

### Hiệu Ứng J-Curve

Vòng đời điển hình của một quỹ tư nhân theo mô hình lợi nhuận hình chữ J:

```
Return
  │         ╱───────
  │        ╱
  │       ╱
  0 ──────────────── Time
  │  ╲  ╱
  │   ╲╱
  │
```

1. **Capital commitment** — LP cam kết vốn; phí quản lý bắt đầu tính
2. **Giai đoạn triển khai (Deployment phase)** — Vốn được gọi và đầu tư; chi phí và phí chiếm ưu thế, lợi nhuận âm
3. **Tạo ra giá trị (Value creation)** — Các công ty trong danh mục tăng trưởng; định giá tăng
4. **Giai đoạn phân phối (Distribution phase)** — Các lần thoát vốn tạo ra tiền mặt; lợi nhuận trở nên dương và tăng tốc

---

## 2. Các Chỉ Số Đo Lường Lợi Nhuận (LOS 2.a)

### Internal Rate of Return (IRR)

- **Chỉ số ưu tiên** cho các khoản đầu tư dài hạn, kém thanh khoản với dòng tiền không đều
- Tỷ lệ chiết khấu khiến NPV của tất cả dòng tiền bằng không:

$$
0 = \sum_{t=0}^{T} \frac{CF_t}{(1 + IRR)^t}
$$

- Tính đến timing và quy mô của dòng tiền
- Hạn chế: giả định tái đầu tư ở mức IRR

### Multiple on Invested Capital (MOIC)

$$
\text{MOIC} = \frac{\text{Realized Value} + \text{Unrealized Value}}{\text{Total Invested Capital}}
$$

| MOIC | Ý nghĩa |
|------|---------------|
| $< 1.0\times$ | Lỗ — thu về ít hơn số đã đầu tư |
| $= 1.0\times$ | Hòa vốn |
| $> 1.0\times$ | Lãi — ví dụ, $2.5\times$ nghĩa là lợi nhuận gấp 2.5 lần vốn đầu tư |

- MOIC **không** tính đến time value of money
- Sử dụng IRR và MOIC cùng nhau để có cái nhìn toàn diện

---

## 3. Gross vs Net Returns (LOS 2.b)

### Gross Returns

- Lợi nhuận **trước** khi khấu trừ management fee và performance fee
- Phản ánh năng lực đầu tư của GP
- Hữu ích để so sánh hiệu suất của các nhà quản lý trên các quỹ khác nhau

### Net Returns

- Lợi nhuận **sau** tất cả các phí (management fee + performance fee + chi phí quỹ)
- Đại diện cho lợi nhuận thực tế mà LP nhận được
- Luôn thấp hơn gross returns

$$
R_{\text{net}} = R_{\text{gross}} - \text{Management Fee} - \text{Performance Fee} - \text{Expenses}
$$

### Cơ Sở Tính Management Fee

| Cơ sở | Phí tính trên | Ảnh hưởng |
|-------|---------------|--------|
| **Committed capital** | Tổng cam kết vốn của LP từ ngày đầu | Tổng phí cao hơn; phí không giảm khi vốn được hoàn trả |
| **Invested capital** | Chỉ phần vốn thực sự được triển khai | Tổng phí thấp hơn; phù hợp với cơ sở đầu tư đang hoạt động |

### Tính Toán Performance Fee

#### Với Hard Hurdle

$$
\text{Performance Fee} = \text{Incentive Rate} \times \max(0,\ R_{\text{fund}} - R_{\text{hurdle}}) \times \text{Capital}
$$

> GP chỉ nhận phí trên phần lợi nhuận **vượt quá** hurdle.

#### Với Soft Hurdle

$$
\text{Performance Fee} = \begin{cases} 0 & \text{if } R_{\text{fund}} < R_{\text{hurdle}} \\ \text{Incentive Rate} \times R_{\text{fund}} \times \text{Capital} & \text{if } R_{\text{fund}} \geq R_{\text{hurdle}} \end{cases}
$$

> Khi đã vượt hurdle, GP nhận phí trên **toàn bộ** lợi nhuận, không chỉ phần vượt trội.

#### High-Water Mark

$$
\text{Fee Base} = \max(0,\ \text{Current NAV} - \text{Previous High-Water Mark})
$$

- Ngăn chặn việc tính phí hai lần trên các khoản lỗ đã được phục hồi.

---

## 4. Net Returns Ở Cấp Độ Quỹ vs Cấp Độ Giao Dịch

| Góc nhìn | Mô tả |
|-------------|-------------|
| **Deal-level** | Net return trên từng khoản đầu tư riêng lẻ trong quỹ |
| **Fund-level** | Net return tổng hợp trên tất cả các giao dịch, sau tổng phí và chi phí |

- Fund-level returns bao gồm tác động của:
  - Tiền mặt chưa đầu tư (cash drag)
  - Chi phí cấp quỹ
  - Bù trừ lãi và lỗ giữa các giao dịch
- Phương thức waterfall theo từng giao dịch có thể phóng đại khoản bồi thường của GP so với phương thức whole-of-fund

---

## Tóm Tắt Các Công Thức Quan Trọng

| Chỉ số | Công thức |
|--------|---------|
| IRR | $0 = \sum_{t=0}^{T} \frac{CF_t}{(1+IRR)^t}$ |
| MOIC | $\frac{\text{Realized} + \text{Unrealized}}{\text{Total Invested}}$ |
| Net Return | $R_{\text{gross}} - \text{Mgmt Fee} - \text{Perf Fee} - \text{Expenses}$ |

---

## Điều Hướng

- **Mục Lục Chủ Đề:** [[alternative-investments/index|Alternative Investments Index]]
- **Module Trước (SAPP):** [[alternative-investments/modules/m07-digital-assets/index|M07 – Digital Assets]]
- **Module Đầu Tiên:** [[alternative-investments/modules/m01-features-methods-structures/index|M01 – Features, Methods and Structures]]