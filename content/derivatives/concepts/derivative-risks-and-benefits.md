---
title: Derivative Risks and Benefits
type: concept
subject: derivatives
module: "M03"
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, risk-management, hedging, leverage, systemic-risk]
---

# Derivative Risks and Benefits

## Lợi ích của Derivatives

### 1. Chuyển giao rủi ro (Hedging)

Derivatives cho phép các bên tham gia thị trường **chuyển giao những rủi ro không mong muốn** sang cho những bên sẵn sàng chịu đựng chúng.

- **Hedgers** giảm thiểu rủi ro trước những biến động giá bất lợi
- **Speculators** chấp nhận rủi ro để tìm kiếm lợi nhuận
- Kết quả: phân bổ rủi ro hiệu quả hơn trên toàn nền kinh tế

### 2. Price Discovery

Thị trường derivative đóng góp vào quá trình **price discovery** — quá trình xác định mức giá hợp lý:

- Giá futures phản ánh kỳ vọng về cung và cầu trong tương lai
- Giá options tiết lộ kỳ vọng của thị trường về volatility
- Forward rates chứa đựng kỳ vọng về lãi suất trong tương lai

> Giá derivative thường đi trước giá spot trong việc phản ánh thông tin mới.

### 3. Ưu điểm vận hành

| Ưu điểm | Mô tả |
|---|---|
| **Chi phí giao dịch thấp hơn** | Derivatives thường rẻ hơn để giao dịch so với tài sản cơ sở |
| **Thanh khoản cao hơn** | Các derivatives được chuẩn hoá có thể thanh khoản hơn tài sản cơ sở |
| **Leverage** | Số vốn bỏ ra nhỏ nhưng kiểm soát được một notional exposure lớn |
| **Dễ dàng bán khống** | Việc lấy vị thế short qua derivatives dễ hơn so với short-selling tài sản cơ sở trực tiếp |
| **Market completeness** | Cho phép tạo ra các khoản thanh toán không có sẵn từ các tài sản hiện hữu |

---

## Rủi ro của Derivatives

### 1. Leverage Risk

Derivatives cung cấp **leverage ngầm định** — những biến động giá nhỏ của tài sản cơ sở tạo ra những thay đổi phần trăm lớn trong giá trị derivative.

- Khuếch đại cả lợi nhuận lẫn thua lỗ
- Giao dịch dựa trên margin có nghĩa là thua lỗ tiềm năng có thể vượt quá số vốn ban đầu
- Có thể dẫn đến cạn kiệt vốn nhanh chóng và nghiêm trọng

### 2. Transparency Risk

- Các cấu trúc phức tạp có thể khó định giá và khó hiểu
- Thị trường OTC trước đây thiếu tính minh bạch (đang được cải thiện sau các cải cách hậu 2008)
- Các rủi ro ẩn có thể tích lũy mà không được chú ý

### 3. Basis Risk

**Basis risk** phát sinh khi tài sản cơ sở của derivative không khớp hoàn toàn với rủi ro đang được phòng ngừa.

$$\text{Basis} = \text{Spot Price} - \text{Futures Price}$$

- Một hedge hoàn hảo yêu cầu basis = 0 tại thời điểm đáo hạn
- Cross-hedging (tài sản cơ sở khác nhau) làm tăng thêm basis risk

### 4. Liquidity Risk

- Một số derivatives (đặc biệt là OTC, exotic) có thể khó đóng vị thế hoặc tất toán
- Chênh lệch bid-ask rộng trong giai đoạn thị trường căng thẳng
- Rủi ro tập trung nếu có ít market makers

### 5. Counterparty Risk (Credit Risk)

- **OTC derivatives**: mỗi bên chịu credit risk của bên kia
- Việc một bên vỡ nợ có thể khiến bên còn lại ở vào vị thế không được hedge
- Các biện pháp giảm thiểu: thỏa thuận tài sản đảm bảo (collateral), netting, thanh toán bù trừ tập trung (CCP)

### 6. Systemic Risk

- **Tính liên kết (Interconnectedness)**: derivatives tạo ra mạng lưới các nghĩa vụ giữa các tổ chức tài chính
- **Contagion**: sự thất bại của một bên tham gia lớn có thể lan rộng ra toàn hệ thống
- **Too big to fail**: sự tập trung các rủi ro derivative vào một vài dealer lớn

> Cuộc khủng hoảng tài chính 2008 đã làm nổi bật systemic risks từ OTC derivatives (ví dụ: danh mục CDS của AIG).

---

## Cách sử dụng: Bên phát hành vs Bên đầu tư

### Issuers (Doanh nghiệp)

| Mục đích sử dụng | Ví dụ |
|---|---|
| **Hedge chi phí đầu vào** | Hãng hàng không dùng jet fuel futures |
| **Cố định chi phí vay** | Interest rate swap (trả cố định, nhận thả nổi) |
| **Quản lý rủi ro ngoại tệ (FX exposure)** | Currency forward để hedge doanh thu nước ngoài |
| **Giảm biến động lợi nhuận** | Các chương trình hedging hàng hoá |

### Investors (Quản lý tài sản)

| Mục đích sử dụng | Ví dụ |
|---|---|
| **Portfolio hedging** | Mua index puts làm bảo vệ trước rủi ro giảm giá |
| **Tăng cường lợi nhuận** | Bán covered calls để thu phí premium |
| **Lấy exposure** | Mua futures thay vì mua tài sản vật chất |
| **Điều chỉnh rủi ro danh mục** | Quản lý duration thông qua interest rate futures |
| **Phân bổ chiến thuật** | Thay đổi exposure nhanh chóng và tiết kiệm chi phí |

---

## Hedge Accounting

Theo các chuẩn mực kế toán (IFRS 9 / ASC 815), **hedge accounting** giúp căn chỉnh thời điểm ghi nhận lãi/lỗ trên công cụ phòng ngừa với khoản mục được phòng ngừa.

### Cash Flow Hedge

- Phòng ngừa sự biến động của **dòng tiền trong tương lai**
- Phần có hiệu quả của lãi/lỗ hedge → ghi nhận vào **Other Comprehensive Income (OCI)**
- Được chuyển sang P&L khi dòng tiền được phòng ngừa ảnh hưởng đến lợi nhuận
- Ví dụ: phòng ngừa khoản nợ lãi suất thả nổi bằng interest rate swap

### Fair Value Hedge

- Phòng ngừa sự thay đổi **fair value** của một tài sản/nợ phải trả đã được ghi nhận
- Lãi/lỗ trên công cụ phòng ngừa → ghi nhận vào **P&L ngay lập tức**
- Sự thay đổi fair value bù trừ trên khoản mục được phòng ngừa cũng được ghi nhận vào P&L
- Ví dụ: phòng ngừa rủi ro lãi suất của trái phiếu lãi suất cố định

### Điều kiện để áp dụng Hedge Accounting

1. Chỉ định chính thức và lập tài liệu từ thời điểm khởi đầu
2. Hedge phải được kỳ vọng là **có hiệu quả cao**
3. Hiệu quả phải được đánh giá **liên tục**

---

## See Also

- [[derivatives/concepts/derivative-instruments|Derivative Instruments]]
- [[derivatives/concepts/forward-commitments|Forward Commitments]]
- [[derivatives/concepts/contingent-claims|Contingent Claims]]
- [[derivatives/glossary/der-m03|Glossary — M03]]