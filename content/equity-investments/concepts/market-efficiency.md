---
title: Market Efficiency
type: concept
subject: equity-investments
module: M03
los: ["3.a", "3.b", "3.c", "3.d"]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, market-efficiency, EMH, anomalies, behavioral-finance]
---

# Market Efficiency

## Efficient Market Hypothesis (EMH)

**Thị trường hiệu quả về mặt thông tin** là thị trường mà giá chứng khoán phản ánh nhanh chóng và đầy đủ tất cả thông tin hiện có. Trong một thị trường hiệu quả, nhà đầu tư không thể liên tục kiếm được lợi nhuận bất thường (vượt trên mức kỳ vọng đã điều chỉnh rủi ro).

**Abnormal return**:

$$\text{Abnormal Return} = R_{\text{actual}} - E(R)$$

trong đó $E(R)$ = lợi suất kỳ vọng tương ứng với mức độ rủi ro.

## Ba Dạng của Fama

### Dạng Yếu (Weak Form)
- Giá phản ánh **toàn bộ dữ liệu thị trường trong quá khứ** (giá, khối lượng, lợi suất lịch sử)
- Hàm ý: **Technical analysis không thể tạo ra abnormal return**
- Fundamental analysis vẫn có thể có tác dụng
- Kiểm định: serial correlation tests, runs tests, filter rules

### Dạng Bán Mạnh (Semi-Strong Form)
- Giá phản ánh **toàn bộ thông tin công khai** (báo cáo tài chính, tin tức, báo cáo phân tích, dữ liệu kinh tế)
- Hàm ý: Cả **technical analysis lẫn fundamental analysis** đều không thể tạo ra abnormal return
- Chỉ có thông tin riêng tư (nội bộ) mới có thể tạo ra lợi thế
- Kiểm định: event studies (tốc độ điều chỉnh giá khi có thông tin công khai mới)

### Dạng Mạnh (Strong Form)
- Giá phản ánh **TẤT CẢ thông tin** — cả công khai lẫn riêng tư (thông tin nội gián)
- Hàm ý: **Không ai** có thể liên tục kiếm được abnormal return, kể cả người có thông tin nội gián
- Đây là dạng mạnh nhất; nhìn chung **KHÔNG được ủng hộ** bởi bằng chứng thực nghiệm
  - Nghiên cứu về insider trading cho thấy người trong cuộc thực sự kiếm được abnormal return
- Kiểm định: hiệu suất của người nội gián, hiệu suất của các fund manager

### Bảng Tóm Tắt

| Dạng | Tập thông tin | Technical Analysis | Fundamental Analysis | Insider Info |
|------|----------------|-------------------|---------------------|-------------|
| Yếu | Giá/khối lượng quá khứ | Vô dụng | Có thể hiệu quả | Có thể hiệu quả |
| Bán mạnh | Toàn bộ thông tin công khai | Vô dụng | Vô dụng | Có thể hiệu quả |
| Mạnh | Toàn bộ thông tin (công khai + riêng tư) | Vô dụng | Vô dụng | Vô dụng |

## Hàm Ý đối với Quản lý Đầu tư

### Active vs Passive Management

| | Active Management | Passive Management |
|---|---|---|
| Quan điểm | Thị trường KHÔNG hoàn toàn hiệu quả | Thị trường HOÀN TOÀN hiệu quả |
| Chiến lược | Lựa chọn chứng khoán, định thời thị trường | Tái tạo chỉ số (mua và nắm giữ) |
| Chi phí | Cao (nghiên cứu, giao dịch) | Thấp (giao dịch tối thiểu) |
| Cơ sở | Có thể tìm thấy chứng khoán định giá sai | Không thể liên tục đánh bại thị trường |

Nếu thị trường hiệu quả ở dạng bán mạnh, passive management là tối ưu vì:
- Không có lợi thế từ fundamental analysis
- Phí và chi phí giao dịch thấp hơn
- Lợi suất ổn định theo thị trường

## Các Bất Thường Thị Trường (Market Anomalies)

Bằng chứng có thể mâu thuẫn với EMH:

### Bất Thường Theo Chuỗi Thời Gian (Time-Series Anomalies)
- **Calendar effects**: Hiệu ứng tháng Giêng — cổ phiếu vốn hóa nhỏ vượt trội trong tháng 1, hiệu ứng ngày trong tuần
- **Momentum**: Cổ phiếu đã hoạt động tốt tiếp tục duy trì đà tốt trong khoảng 3–12 tháng
- **Overreaction**: Cổ phiếu hoạt động kém trong 3–5 năm có xu hướng đảo chiều (long-term reversal)

### Bất Thường Theo Mặt Cắt Ngang (Cross-Sectional Anomalies)
- **Size effect**: Cổ phiếu vốn hóa nhỏ (small-cap) đạt lợi suất điều chỉnh rủi ro cao hơn cổ phiếu large-cap
- **Value effect**: Cổ phiếu có P/E thấp, P/B thấp, hoặc tỷ suất cổ tức cao có xu hướng vượt trội
- **Neglected-firm effect**: Các cổ phiếu ít được theo dõi có xu hướng vượt trội

### Các Bất Thường Khác
- **Earnings surprise (PEAD)**: Post-earnings announcement drift — giá tiếp tục dịch chuyển theo chiều của bất ngờ lợi nhuận
- **IPO underperformance**: IPO có xu hướng hoạt động kém trong 3–5 năm sau mức tăng ban đầu
- **Closed-end fund discount**: Quỹ đóng (closed-end fund) thường giao dịch dưới NAV

> **Lưu ý**: Các bất thường có thể phản ánh (1) data mining, (2) survivorship bias, (3) cỡ mẫu nhỏ, (4) các yếu tố rủi ro chưa được mô hình nắm bắt, hoặc (5) chi phí giao dịch làm triệt tiêu khả năng sinh lời.

## Behavioral Finance

Những thách thức đối với EMH xuất phát từ tâm lý học:

### Cognitive Biases
- **Overconfidence**: Đánh giá quá cao khả năng định giá chứng khoán của bản thân
- **Confirmation bias**: Tìm kiếm thông tin xác nhận niềm tin hiện có
- **Anchoring**: Phụ thuộc quá mức vào thông tin ban đầu
- **Availability bias**: Đánh giá quá cao thông tin dễ nhớ lại
- **Hindsight bias**: Tin rằng các sự kiện quá khứ hoàn toàn có thể dự đoán được

### Emotional Biases
- **Loss aversion**: Nỗi đau khi mất mát lớn hơn niềm vui khi có được lượng tương đương (prospect theory)
- **Herding**: Đi theo đám đông thay vì tự phân tích
- **Mental accounting**: Đối xử với tiền bạc khác nhau tùy theo nguồn gốc hoặc mục đích sử dụng
- **Status quo bias**: Ưa thích trạng thái hiện tại, kháng cự thay đổi

### Tác Động ở Cấp Độ Thị Trường
- **Bubbles**: Giá bị đẩy lên cao hơn nhiều so với giá trị cơ bản do sự phấn khích phi lý trí
- **Crashes**: Giá sụp đổ đột ngột, thường được kích hoạt bởi hoảng loạn bán tháo
- **Limits to arbitrage**: Nhà đầu tư duy lý có thể không sửa chữa được định giá sai do rủi ro, chi phí, hoặc các ràng buộc khác

## Trang Liên Quan

- [[equity-investments/concepts/security-market-indexes|Security Market Indexes]]
- [[equity-investments/concepts/equity-valuation|Equity Valuation Models]]
- [[equity-investments/concepts/company-analysis|Company Analysis]]