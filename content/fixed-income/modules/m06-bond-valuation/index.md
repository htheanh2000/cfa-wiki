---
title: "M06 — Bond Valuation"
type: module
subject: fixed-income
module: M06
los: "6.a–6.c"
created: 2026-04-12
updated: 2026-04-12
tags:
  - fixed-income
  - module
  - M06
  - bond-valuation
  - bond-pricing
  - yield-to-maturity
  - accrued-interest
  - matrix-pricing
---

# M06 – Bond Valuation: Prices and Yields

> **Nguồn**: [[fixed-income/sources/sapp-fi-2026|SAPP FI 2026]], tr.195–226
> **LOS**: 6.a – Tính giá trái phiếu khi biết market discount rate
> **LOS**: 6.b – Mô tả mối quan hệ giữa giá trái phiếu, coupon rate, thời gian đáo hạn và market discount rate
> **LOS**: 6.c – Mô tả matrix pricing

## 1. Bond Pricing

Giá trái phiếu bằng **giá trị hiện tại** (present value) của toàn bộ dòng tiền kỳ vọng trong tương lai, được chiết khấu theo market discount rate (yield).

$$P = \sum_{t=1}^{n} \frac{PMT}{(1 + r)^t} + \frac{FV}{(1 + r)^n}$$

Trong đó:
- $P$ = giá trái phiếu
- $PMT$ = khoản thanh toán coupon định kỳ
- $FV$ = mệnh giá (face/par value)
- $r$ = market discount rate mỗi kỳ
- $n$ = số kỳ đến ngày đáo hạn

Đối với trái phiếu trả coupon nửa năm (thông lệ Mỹ):

$$P = \sum_{t=1}^{2N} \frac{C/2}{(1 + r/2)^t} + \frac{FV}{(1 + r/2)^{2N}}$$

## 2. Mối quan hệ Price–Yield

### Quan hệ nghịch chiều

- Khi yield thị trường **tăng**, giá trái phiếu **giảm**
- Khi yield thị trường **giảm**, giá trái phiếu **tăng**
- Mối quan hệ này mang tính **convex** (không tuyến tính)

### Premium, Par và Discount

| Điều kiện | Giá so với mệnh giá | Mô tả |
|-----------|----------------------|-------|
| $r < \text{coupon rate}$ | **Premium** ($P > FV$) | Nhà đầu tư trả nhiều hơn vì coupon vượt market rate |
| $r = \text{coupon rate}$ | **Par** ($P = FV$) | Coupon bằng đúng market rate |
| $r > \text{coupon rate}$ | **Discount** ($P < FV$) | Nhà đầu tư trả ít hơn vì coupon thấp hơn market rate |

### Pull to Par

- Khi trái phiếu tiến gần đến ngày đáo hạn, giá hội tụ về mệnh giá
- Trái phiếu premium giảm dần về mệnh giá; trái phiếu discount tăng dần về mệnh giá
- Tại ngày đáo hạn, giá = mệnh giá (giả định không có vỡ nợ)

## 3. Accrued Interest và Bond Pricing

### Full (Dirty) Price và Flat (Clean) Price

$$\text{Full Price (Dirty)} = \text{Flat Price (Clean)} + \text{Accrued Interest}$$

- **Full (dirty) price**: giá tiền mặt thực tế người mua phải trả; bao gồm accrued interest
- **Flat (clean) price**: giá niêm yết trên thị trường; không bao gồm accrued interest
- Báo giá trái phiếu thường thể hiện **clean price**, nhưng thanh toán thực hiện theo **dirty price**

### Tính Accrued Interest

$$AI = PMT \times \frac{t}{T}$$

Trong đó:
- $AI$ = accrued interest
- $PMT$ = khoản thanh toán coupon trong kỳ
- $t$ = số ngày kể từ lần trả coupon gần nhất
- $T$ = tổng số ngày trong kỳ coupon

Các quy ước tính ngày (day-count conventions):
- **Actual/Actual** — dùng cho trái phiếu chính phủ (US Treasuries)
- **30/360** — dùng cho trái phiếu doanh nghiệp (thông lệ Mỹ)
- **Actual/360** — dùng cho các công cụ thị trường tiền tệ (money market instruments)

## 4. Yield to Maturity (YTM)

YTM là **tỷ suất hoàn vốn nội bộ** (internal rate of return – IRR) mà nhà đầu tư thu được khi mua trái phiếu tại giá thị trường hiện tại và nắm giữ đến khi đáo hạn.

### Ba giả định quan trọng

1. Nhà đầu tư **nắm giữ trái phiếu đến khi đáo hạn**
2. Tổ chức phát hành **thực hiện đầy đủ và đúng hạn tất cả các khoản thanh toán** (không vỡ nợ)
3. Tất cả các khoản coupon được **tái đầu tư tại mức YTM**

> **Lưu ý quan trọng**: Giả định tái đầu tư là giả định yếu nhất. Lợi nhuận thực tế sẽ khác YTM nếu coupon được tái đầu tư ở mức lãi suất khác YTM. Đây là nguồn gốc của **reinvestment risk**.

### Quy đổi Yield về cơ sở năm

- Trái phiếu trả coupon nửa năm: $YTM_{annual} = 2 \times YTM_{semi-annual}$ (bond-equivalent yield)
- Effective annual yield: $EAY = (1 + YTM_{semi})^2 - 1$

## 5. Matrix Pricing

**Matrix pricing** là phương pháp ước tính giá hoặc yield của một trái phiếu dựa trên giá/yield của các **trái phiếu có thể so sánh** được giao dịch tích cực hơn.

### Khi nào sử dụng

- Trái phiếu cần định giá **kém thanh khoản** hoặc **chưa được giao dịch gần đây**
- Không có giá thị trường đáng tin cậy

### Phương pháp thực hiện

1. Xác định các trái phiếu có thể so sánh với các đặc điểm tương tự:
   - Chất lượng tín dụng (cùng xếp hạng)
   - Thời gian đáo hạn (bao quanh kỳ hạn mục tiêu)
   - Cấu trúc coupon
2. Sử dụng **nội suy tuyến tính** (linear interpolation) giữa yield của các trái phiếu so sánh để ước tính yield của trái phiếu mục tiêu

$$YTM_{target} = YTM_{shorter} + \frac{(T_{target} - T_{shorter})}{(T_{longer} - T_{shorter})} \times (YTM_{longer} - YTM_{shorter})$$

Trong đó $T$ đại diện cho thời gian đáo hạn.

## 6. Coupon Effect và Maturity Effect

### Coupon Effect

- Trái phiếu có **coupon thấp** **nhạy cảm hơn** với biến động lãi suất so với trái phiếu có coupon cao (các điều kiện khác bằng nhau)
- Zero-coupon bond có **mức độ nhạy cảm giá cao nhất** với cùng thời gian đáo hạn
- Lý do: phần lớn giá trị trái phiếu đến từ khoản hoàn trả mệnh giá ở thời điểm xa trong tương lai

### Maturity Effect

- Trái phiếu có **kỳ hạn dài hơn** **nhạy cảm hơn** với biến động lãi suất so với trái phiếu kỳ hạn ngắn (các điều kiện khác bằng nhau)
- Dòng tiền ở thời điểm càng xa trong tương lai càng bị chiết khấu mạnh hơn khi lãi suất thay đổi
- Ngoại lệ: với trái phiếu discount sâu, mức độ nhạy cảm có thể giảm sau một ngưỡng kỳ hạn nhất định (trường hợp hiếm gặp)

> **Kết luận tổng hợp**: Trái phiếu kỳ hạn dài, coupon thấp có **mức độ nhạy cảm lãi suất cao nhất**. Trái phiếu kỳ hạn ngắn, coupon cao có **mức độ nhạy cảm thấp nhất**.

## Related

- [[fixed-income/m01-instrument-features/index|M01 – FI Instrument Features]]
- [[fixed-income/m07-yield-spread-fixed-rate/index|M07 – Yield and Yield Spread Measures for Fixed-Rate Bonds]]
- [[fixed-income/m09-term-structure/index|M09 – Term Structure of Interest Rates]]
- [[fixed-income/m10-interest-rate-risk-return/index|M10 – Interest Rate Risk and Return]]
- [[fixed-income/m11-bond-duration/index|M11 – Yield-Based Bond Duration Measures]]