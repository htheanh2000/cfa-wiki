---
title: Derivative Instruments
type: concept
subject: derivatives
module: "M01"
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, instruments, OTC, ETD, clearinghouse]
---

# Derivative Instruments

## Định nghĩa

**Derivative** (công cụ phái sinh) là một công cụ tài chính có giá trị được *phái sinh từ* hiệu suất của một tài sản cơ sở, chỉ số, lãi suất, hoặc sự kiện. Bản thân derivative là một hợp đồng giữa hai hoặc nhiều bên.

$$\text{Derivative Value} = f(\text{Underlying})$$

## Thị trường Spot vs Thị trường Derivative

| Đặc điểm | Thị trường Spot (Cash) | Thị trường Derivative |
|---|---|---|
| Thanh toán | Ngay lập tức (T+1, T+2) | Ngày trong tương lai |
| Giao hàng | Trao đổi vật lý ngay | Trao đổi theo thỏa thuận trong tương lai |
| Cơ sở giá | Cung cầu hiện tại | Giá trị kỳ vọng trong tương lai |
| Đòn bẩy | Hạn chế | Đáng kể |

- **Spot price** ($S_0$): giá thị trường hiện tại của tài sản cơ sở
- **Derivative price**: được xác định bởi spot price, thời gian, lãi suất phi rủi ro, và các yếu tố khác

## Các loại Underlying

Derivative có thể được viết trên hầu hết mọi loại underlying:

| Danh mục | Ví dụ |
|---|---|
| Equities | Cổ phiếu đơn lẻ, chỉ số cổ phiếu |
| Fixed Income | Trái phiếu, lãi suất, MRR |
| Currencies | USD/EUR, JPY/GBP |
| Commodities | Dầu, vàng, lúa mì, khí tự nhiên |
| Credit | Mức độ tín nhiệm của người vay (CDS) |
| Khác | Thời tiết, biến động (VIX), lạm phát |

## OTC vs Exchange-Traded Derivatives (ETD)

### Over-the-Counter (OTC)

- **Thương lượng riêng** giữa hai bên
- **Có thể tùy chỉnh**: bất kỳ điều khoản nào (notional, kỳ hạn, underlying)
- **Counterparty risk**: mỗi bên chịu rủi ro tín dụng của bên kia
- Ví dụ: forwards, swaps, exotic options
- Cải cách sau 2008: nhiều OTC derivatives hiện được thanh toán bù trừ tập trung

### Exchange-Traded Derivatives (ETD)

- Hợp đồng **tiêu chuẩn hóa** (quy mô, ngày đáo hạn, tick size)
- Giao dịch trên **sàn giao dịch có tổ chức** (CME, ICE, Eurex)
- **Clearinghouse** đóng vai trò là đối tác trung tâm (CCP)
- **Mark-to-market** hàng ngày với yêu cầu ký quỹ
- Ví dụ: futures, listed options

| Đặc điểm | OTC | ETD |
|---|---|---|
| Tùy chỉnh | Cao | Thấp (tiêu chuẩn hóa) |
| Counterparty risk | Có (giảm thiểu bằng tài sản thế chấp) | Gần như bị loại bỏ (CCP) |
| Thanh khoản | Biến động | Thường cao |
| Minh bạch | Thấp | Cao |
| Quy định | Ngày càng tăng sau GFC | Được quản lý chặt chẽ |

## Clearinghouse (Central Counterparty — CCP)

Clearinghouse tự đặt mình vào giữa người mua và người bán, trở thành:
- **Người mua của mọi người bán** và **người bán của mọi người mua**

Các chức năng chính:
1. **Novation**: thay thế hợp đồng song phương bằng hai hợp đồng (mỗi bên với CCP)
2. **Margin collection**: initial margin + variation margin (thanh toán hàng ngày)
3. **Quản lý vỡ nợ**: quỹ bảo lãnh, phân bổ tổn thất chung
4. **Netting**: giảm các vị thế gộp xuống còn vị thế ròng

> CCP **không** loại bỏ rủi ro — nó **tập trung hóa và quản lý** counterparty risk thông qua margin, các bộ đệm vốn, và cơ chế xử lý vỡ nợ theo tầng.

## See Also

- [[derivatives/concepts/forward-commitments|Forward Commitments]]
- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/concepts/derivative-risks-and-benefits|Derivative Risks and Benefits]]
- [[derivatives/glossary/der-m01|Glossary — M01]]