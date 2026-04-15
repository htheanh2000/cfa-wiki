---
title: "M01 — Market Organization"
type: module
subject: equity-investments
module: m01
los: [1.a, 1.b, 1.c, 1.d, 1.e, 1.f, 1.g, 1.h, 1.i, 1.j, 1.k, 1.l]
created: 2026-04-10
updated: 2026-04-10
tags: [equity-investments, m01, market-organization, market-structure]
---

# M01: Market Organization and Structure

**Nguồn**: [[equity-investments/sources/sapp-equity-2026|SAPP Slide 2026]], trang 2–55
**LOS**: 1.a–1.l

---

## LOS 1.a — Chức năng của Hệ thống Tài chính

Hệ thống tài chính thực hiện **ba chức năng chính**:

1. **Tiết kiệm, vay mượn, đầu tư, quản lý rủi ro** — Cho phép các chủ thể (cá nhân, doanh nghiệp, chính phủ) tiết kiệm và vay tiền, huy động vốn cổ phần, đầu tư, quản lý rủi ro và giao dịch tài sản
2. **Xác định lãi suất cân bằng** — Xác định tỷ suất sinh lợi giúp cân bằng tổng tiết kiệm với tổng đi vay
3. **Phân bổ vốn hiệu quả** — Dẫn vốn đến những nơi có năng suất cao nhất (allocational efficiency)

---

## LOS 1.b — Phân loại Thị trường

Thị trường có thể được phân loại theo nhiều chiều:

| Chiều phân loại | Các loại |
|-----------------|----------|
| **Thời điểm giao hàng** | Spot markets (giao ngay) vs Forward/Future markets (giao trong tương lai) |
| **Tính phát hành** | Primary markets (phát hành mới) vs Secondary markets (chứng khoán đã phát hành) |
| **Tính đổi mới** | Traditional investments vs Alternative investments |
| **Kỳ hạn** | Money markets ($\leq$ 1 năm) vs Capital markets ($>$ 1 năm) |

---

## LOS 1.c — Các loại Tài sản

### Chứng khoán (Securities)
- **Fixed-income**: Trái phiếu, kỳ phiếu, commercial paper — cam kết hoàn trả tiền vay
- **Equity**: Cổ phiếu thường, cổ phiếu ưu đãi — quyền sở hữu
- **Pooled investments**: Quỹ tương hỗ (mutual funds), ETF, hedge funds, asset-backed securities

### Tiền tệ (Currencies)
- Ngoại hối được giao dịch trên thị trường spot và forward

### Hợp đồng (Contracts)
- **Forward contracts**: Tùy chỉnh, giao dịch OTC, nghĩa vụ mua/bán tại ngày trong tương lai
- **Futures contracts**: Chuẩn hóa, giao dịch trên sàn, là dạng forward được chuẩn hóa
- **Swap contracts**: Chuỗi các forward contracts (ví dụ: interest rate swap, currency swap)
- **Option contracts**: Quyền (không phải nghĩa vụ) mua (call) hoặc bán (put) tại một mức giá xác định

### Hàng hóa (Commodities)
- Kim loại quý, năng lượng, nông sản — giao dịch qua hợp đồng spot hoặc phái sinh

### Tài sản thực (Real Assets)
- Bất động sản, thiết bị, cơ sở hạ tầng — thường kém thanh khoản

---

## LOS 1.d — Trung gian Tài chính

| Trung gian | Chức năng |
|------------|-----------|
| **Brokers** | Kết nối người mua và người bán; KHÔNG giữ vị thế; kiếm hoa hồng |
| **Dealers** | Giao dịch từ danh mục tự có; cung cấp thanh khoản; kiếm bid-ask spread |
| **Arbitrageurs** | Khai thác chênh lệch giá giữa các thị trường; thúc đẩy tính nhất quán về giá |
| **ATS / Exchanges** | Cung cấp nền tảng giao dịch; thực thi quy tắc; price discovery |
| **Securitizers** | Gộp các tài sản (ví dụ: thế chấp) và phát hành chứng khoán được bảo đảm bởi chúng |
| **Insurance companies** | Chuyển giao và gộp rủi ro; tạo lợi ích đa dạng hóa |
| **Depositories / Custodians** | Lưu ký tài sản; hỗ trợ thanh toán bù trừ |
| **Clearinghouses** | Đóng vai trò đối tác cho cả hai phía (CCP); giảm rủi ro đối tác; yêu cầu ký quỹ |

---

## LOS 1.e — Vị thế: Long vs Short

- **Long position**: Sở hữu tài sản; lợi nhuận khi giá tăng
- **Short position**: Bán tài sản đi vay; lợi nhuận khi giá giảm; phải hoàn trả tài sản sau đó

### Quy trình Short Selling
1. Vay chứng khoán từ người cho vay
2. Bán chứng khoán vay được trên thị trường
3. Ký gửi tiền thu được cộng với margin cho người cho vay
4. Mua lại chứng khoán sau đó để hoàn trả

> **Rủi ro**: Short selling có tiềm năng **thua lỗ không giới hạn** về mặt lý thuyết (giá có thể tăng vô hạn)

---

## LOS 1.f — Đòn bẩy và Margin

### Leverage Ratio

$$\text{Leverage ratio} = \frac{1}{\text{Margin requirement \%}}$$

- Nếu margin = 50%, leverage = $\frac{1}{0.50} = 2\times$

### Return on Margin (Leveraged Return)

$$r_{\text{margin}} = r_{\text{asset}} \times \text{Leverage ratio} = \frac{r_{\text{asset}}}{\text{Margin \%}}$$

### Margin Call Price (Long Position)

$$P_{\text{margin call}} = P_0 \times \frac{1 - \text{Initial margin}}{1 - \text{Maintenance margin}}$$

Trong đó:
- $P_0$ = giá mua ban đầu
- Initial margin = vốn chủ sở hữu ban đầu / tổng giá trị vị thế
- Maintenance margin = tỷ lệ vốn chủ sở hữu tối thiểu được yêu cầu

### Margin Call Price (Short Position)

$$P_{\text{margin call}} = P_0 \times \frac{1 + \text{Initial margin}}{1 + \text{Maintenance margin}}$$

---

## LOS 1.g — Lệnh giao dịch và Hướng dẫn

Lệnh giao dịch chứa ba loại hướng dẫn:

1. **Execution instructions** — **Cách** giao dịch (market order, limit order, v.v.)
2. **Validity instructions** — **Thời gian** lệnh có hiệu lực (day order, GTC, IOC, FOK)
3. **Clearing instructions** — **Cách** thanh toán bù trừ (tài khoản nào, custodian, phương thức thanh toán)

---

## LOS 1.h — Market Orders vs Limit Orders

| Đặc điểm | Market Order | Limit Order |
|----------|-------------|-------------|
| **Chắc chắn về giá** | Không — khớp lệnh theo giá tốt nhất hiện có | Có — chỉ định giá tối đa (mua) hoặc tối thiểu (bán) |
| **Chắc chắn khớp lệnh** | Có — khớp ngay lập tức | Không — có thể không khớp nếu giá limit chưa đạt |
| **Phù hợp nhất khi** | Ưu tiên tốc độ khớp lệnh | Ưu tiên mức giá |

### Các loại lệnh đặc biệt
- **Stop order (stop-loss)**: Trở thành market order khi đạt đến stop price
- **Stop-limit order**: Trở thành limit order khi đạt đến stop price

---

## LOS 1.i — Primary vs Secondary Markets

### Primary Markets (Phát hành mới)
- **IPO (Initial Public Offering)**: Phát hành lần đầu ra công chúng; được bảo lãnh phát hành bởi ngân hàng đầu tư
- **Seasoned offering (SEO / follow-on)**: Phát hành cổ phiếu bổ sung của công ty đã niêm yết
- **Private placement**: Bán cho nhà đầu tư có đủ điều kiện/tổ chức; ít quy định hơn, chi phí thấp hơn
- **Shelf registration**: Được phê duyệt trước để phát hành chứng khoán theo thời gian (tối đa 2–3 năm)
- **Rights offering**: Cổ đông hiện hữu được quyền mua cổ phiếu mới với giá chiết khấu

### Secondary Markets
- Giao dịch chứng khoán đã phát hành giữa các nhà đầu tư
- Cung cấp **thanh khoản** và **price discovery**
- Công ty phát hành KHÔNG nhận tiền thu được

---

## LOS 1.j — Cấu trúc Thị trường

| Cấu trúc | Mô tả | Ví dụ |
|----------|-------|-------|
| **Quote-driven** | Dealers đăng bid/ask; nhà đầu tư giao dịch với dealers | Thị trường trái phiếu OTC, forex |
| **Order-driven** | Lệnh được khớp theo quy tắc (ưu tiên giá/thời gian); không cần dealers | Sàn chứng khoán (NYSE, HKEX) |
| **Brokered** | Brokers tìm đối tác cho các giao dịch lớn hoặc độc đáo | Bất động sản, giao dịch block lớn |

### Quy tắc khớp lệnh trong Order-Driven Market
- **Price priority**: Giá tốt nhất được khớp trước
- **Time priority (display priority)**: Lệnh đặt trước tại cùng mức giá được khớp trước

---

## LOS 1.k — Hệ thống Tài chính Hoạt động Tốt

Một hệ thống tài chính hoạt động tốt cần:
- Có giá **informationally efficient** (phản ánh thông tin sẵn có)
- Cung cấp thị trường **operationally efficient** (chi phí giao dịch thấp)
- Đạt được triển khai vốn **allocationally efficient** (vốn được phân bổ đến nơi có giá trị sử dụng cao nhất)
- Đảm bảo **complete markets** (có đầy đủ công cụ cho mọi giao dịch mong muốn)

---

## LOS 1.l — Mục tiêu của Quy định Thị trường

Các mục tiêu quy định chính:
1. **Bảo vệ nhà đầu tư** khỏi gian lận, thông tin sai lệch và các hành vi không công bằng
2. **Đảm bảo sự công bằng, hiệu quả và minh bạch** của thị trường
3. **Giảm thiểu rủi ro hệ thống** trong hệ thống tài chính

Các cơ quan quản lý bao gồm:
- Cơ quan chính phủ (SEC, FCA, SFC)
- Tổ chức tự quản (SROs) — sàn giao dịch, FINRA
- Các nhóm ngành thiết lập tiêu chuẩn và thông lệ tốt nhất