---
title: Credit Risk
type: concept
subject: fixed-income
created: 2026-04-12
updated: 2026-04-12
tags: [credit-risk, POD, LGD, expected-loss, credit-rating, recovery-rate, notching]
---

# Credit Risk

## Các Thành Phần của Credit Risk

### Probability of Default (POD)
Xác suất mà người đi vay sẽ không thực hiện được các khoản thanh toán đã cam kết.

### Loss Given Default (LGD)
Mức tổn thất phát sinh nếu xảy ra default.

$$LGD = 1 - \text{Recovery Rate}$$

### Expected Loss

$$\text{Expected Loss} = POD \times LGD \times \text{Exposure at Default}$$

Hoặc tương đương:

$$\text{Expected Loss} = POD \times (1 - \text{Recovery Rate}) \times \text{Exposure}$$

### Recovery Rate
Tỷ lệ phần trăm giá trị trái phiếu mà nhà đầu tư thu hồi được sau khi xảy ra default.

| Thứ tự ưu tiên | Recovery Rate điển hình |
|-----------|--------------------|
| First lien / Secured | 50–65% |
| Senior unsecured | 35–45% |
| Senior subordinated | 25–35% |
| Subordinated | 15–25% |
| Junior subordinated | 10–20% |

## Credit Ratings

### Các Tổ Chức Xếp Hạng Tín Dụng Lớn
- **Moody's**: Aaa, Aa, A, Baa, Ba, B, Caa, Ca, C
- **S&P / Fitch**: AAA, AA, A, BBB, BB, B, CCC, CC, C, D

### Investment Grade vs. High Yield

| Phân loại | Moody's | S&P/Fitch |
|----------|---------|-----------|
| **Investment grade** | Aaa to Baa3 | AAA to BBB- |
| **High yield (speculative)** | Ba1 and below | BB+ and below |

**Fallen angel**: Trái phiếu bị hạ bậc từ investment grade xuống high yield.

**Rising star**: Trái phiếu được nâng bậc từ high yield lên investment grade.

## 8 Cs trong Phân Tích Tín Dụng

| Yếu tố | Mô tả |
|--------|-------------|
| **Capacity** | Khả năng thực hiện các khoản thanh toán nợ (phân tích dòng tiền) |
| **Capital** | Sức mạnh bảng cân đối kế toán và vùng đệm vốn chủ sở hữu |
| **Collateral** | Chất lượng và giá trị tài sản thế chấp |
| **Character** | Chất lượng quản lý, thành tích hoạt động, quản trị doanh nghiệp |
| **Conditions** | Điều kiện kinh tế và ngành |
| **Country** | Rủi ro quốc gia và chính trị |
| **Currency** | Mức độ tiếp xúc với rủi ro tỷ giá ngoại hối |
| **Covenants** | Sức mạnh của các điều khoản bảo vệ |

## Notching

Các tổ chức xếp hạng tín dụng có thể gán **các mức xếp hạng khác nhau** cho các đợt phát hành khác nhau của cùng một tổ chức phát hành, dựa trên:

- **Seniority**: Nợ cấp cao được xếp hạng cao hơn nợ subordinated
- **Security**: Nợ có bảo đảm được xếp hạng cao hơn nợ không có bảo đảm
- **Structural subordination**: Nợ của công ty mẹ (holding company) có thể được xếp hạng thấp hơn nợ của công ty con hoạt động (operating company)

**Notching điển hình:**
- Secured debt: +1 đến +2 notches cao hơn issuer rating
- Senior unsecured: Bằng với issuer rating
- Subordinated: -1 đến -2 notches thấp hơn issuer rating
- Các tổ chức phát hành high-yield thường có **notching rộng hơn** (khoảng cách notch lớn hơn giữa secured và subordinated)

## Credit Spread

Phần bù lợi suất so với lãi suất chuẩn (benchmark rate) nhằm bù đắp cho nhà đầu tư về credit risk:

$$\text{Credit Spread} = YTM_{\text{bond}} - YTM_{\text{benchmark}}$$

### Biến Động Credit Spread

- Spread **nới rộng** → giá trái phiếu giảm (tin xấu, suy giảm kinh tế)
- Spread **thu hẹp** → giá trái phiếu tăng (tin tốt, cải thiện kinh tế)
- Biến động spread ảnh hưởng đến trái phiếu **xếp hạng thấp hơn** nhiều hơn so với trái phiếu xếp hạng cao

## Credit Transition Matrix

Thể hiện xác suất thay đổi xếp hạng của một trái phiếu trong một khoảng thời gian nhất định:
- Các phần tử trên đường chéo: xác suất **duy trì** xếp hạng hiện tại
- Ngoài đường chéo: xác suất được **nâng hạng** hoặc **hạ hạng**
- Trái phiếu investment-grade có xác suất **cao** duy trì ở mức investment grade
- Trái phiếu xếp hạng thấp hơn có xác suất default **cao hơn**

## Cross-Default Provision

Nếu tổ chức phát hành default trên **bất kỳ** nghĩa vụ nợ nào, điều đó sẽ kích hoạt default trên trái phiếu có cross-default provision. Điều này bảo vệ trái chủ khỏi bị đặt sau các chủ nợ khác về thứ tự ưu tiên.

## Các Khái Niệm Liên Quan

- [[fixed-income/concepts/yield-spreads|Yield Spreads]]
- [[fixed-income/concepts/bond-features|Bond Features]]
- [[fixed-income/concepts/securitization|Securitization]]
- [[fixed-income/formulas/fi-formulas|Fixed Income Formulas]]
- [[fixed-income/glossary/fi-m14|Glossary: Module 14]]