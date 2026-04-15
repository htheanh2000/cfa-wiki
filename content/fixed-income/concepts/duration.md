---
title: Duration
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [duration, macaulay, modified, money-duration, PVBP, effective-duration, key-rate]
---

# Duration

Duration đo lường **mức độ nhạy cảm của trái phiếu với sự thay đổi lãi suất**. Có nhiều loại duration khác nhau phục vụ cho các mục đích khác nhau.

## Macaulay Duration

**Thời gian bình quân gia quyền** để nhận được các dòng tiền của trái phiếu, với trọng số là giá trị hiện tại của từng dòng tiền.

$$\text{MacDur} = \frac{\sum_{t=1}^{n} t \times PV(CF_t)}{PV}$$

trong đó:
- $t$ = kỳ thời gian (tính bằng năm hoặc kỳ)
- $PV(CF_t)$ = giá trị hiện tại của dòng tiền tại thời điểm $t$
- $PV$ = tổng giá trị hiện tại (giá trái phiếu)

**Diễn giải**: Macaulay duration bằng 5,2 có nghĩa là thời gian bình quân gia quyền để nhận các dòng tiền là 5,2 năm.

### Properties
- Luôn **nhỏ hơn kỳ hạn** đối với trái phiếu có coupon
- Bằng kỳ hạn đối với **zero-coupon bonds**
- Coupon thấp hơn → Macaulay duration cao hơn
- Kỳ hạn dài hơn → Macaulay duration cao hơn (nhìn chung)

## Modified Duration

Đo lường **phần trăm thay đổi giá** khi yield thay đổi 1% (100 bp).

$$\text{ModDur} = \frac{\text{MacDur}}{1 + r}$$

trong đó $r$ = yield mỗi kỳ.

**Xấp xỉ thay đổi giá:**

$$\%\Delta PV \approx -\text{ModDur} \times \Delta \text{Yield}$$

**Ví dụ**: ModDur = 7,5, yield tăng 50 bp (0,005):

$$\%\Delta PV \approx -7.5 \times 0.005 = -3.75\%$$

## Approximate Modified Duration

Khi Macaulay duration không có sẵn, có thể xấp xỉ bằng phương pháp số:

$$\text{ApproxModDur} = \frac{PV_{-} - PV_{+}}{2 \times PV_0 \times \Delta \text{Yield}}$$

trong đó:
- $PV_{-}$ = giá trái phiếu nếu yield giảm $\Delta \text{Yield}$
- $PV_{+}$ = giá trái phiếu nếu yield tăng $\Delta \text{Yield}$
- $PV_0$ = giá trái phiếu hiện tại
- $\Delta \text{Yield}$ = mức thay đổi yield (dạng thập phân)

## Money Duration (Dollar Duration)

Đo lường **mức thay đổi giá tuyệt đối theo đô la** khi yield thay đổi.

$$\text{MoneyDur} = \text{ModDur} \times PV^{\text{Full}}$$

$$\Delta PV \approx -\text{MoneyDur} \times \Delta \text{Yield}$$

## PVBP (Price Value of a Basis Point)

Mức thay đổi giá theo đô la khi yield thay đổi **1 basis point** (0,01%).

$$PVBP = \frac{PV_{-} - PV_{+}}{2}$$

trong đó $PV_{-}$ và $PV_{+}$ là giá sau khi yield giảm và tăng 1 bp.

Hoặc tính theo công thức:

$$PVBP = \text{MoneyDur} \times 0.0001$$

## Effective Duration

Được dùng cho các trái phiếu có **embedded options** (callable, putable, MBS) — những loại có dòng tiền thay đổi khi yield thay đổi.

$$\text{EffDur} = \frac{PV_{-} - PV_{+}}{2 \times PV_0 \times \Delta \text{Curve}}$$

### Điểm khác biệt so với Modified Duration
- Sử dụng mức dịch chuyển **benchmark yield curve** ($\Delta \text{Curve}$), không phải thay đổi YTM
- Tính đến việc dòng tiền có thể thay đổi khi yield thay đổi
- Bắt buộc áp dụng cho callable/putable bonds và mortgage-backed securities

### Giá trị thường gặp
- **Option-free bonds**: Effective duration ≈ Modified duration
- **Callable bonds**: Effective duration ≤ Duration của option-free bond tương đương
- **Putable bonds**: Effective duration ≤ Duration của option-free bond tương đương
- **Floaters**: Effective duration ≈ thời gian đến ngày reset lãi suất tiếp theo (gần bằng 0)

## Key Rate Duration (Partial Duration)

Đo lường mức độ nhạy cảm với sự thay đổi spot rate tại một **kỳ hạn cụ thể**, trong khi giữ nguyên tất cả các spot rate khác.

$$\text{KeyRateDur}_k = \frac{-1}{PV} \times \frac{\Delta PV}{\Delta r_k}$$

- Tổng tất cả các key rate duration ≈ effective duration
- Cho thấy phần nào của yield curve mà trái phiếu nhạy cảm nhất
- **Bullet bonds**: duration tập trung tại điểm đáo hạn
- **Coupon bonds**: duration phân bổ trải dài theo các ngày trả coupon và ngày đáo hạn

## Duration của danh mục trái phiếu

$$D_{\text{portfolio}} = \sum_{i=1}^{n} w_i \times D_i$$

trong đó $w_i$ = trọng số theo giá trị thị trường của trái phiếu $i$ và $D_i$ = duration của trái phiếu $i$.

> Portfolio duration là một **xấp xỉ tuyến tính** và giả định yield curve dịch chuyển song song.

## Related Concepts

- [[fixed-income/concepts/convexity|Convexity]]
- [[fixed-income/concepts/interest-rate-risk|Interest Rate Risk]]
- [[fixed-income/concepts/bond-valuation|Bond Valuation]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m11|Glossary: Module 11]]