---
title: "M01 — Instruments & Markets"
type: module
subject: derivatives
module: M01
los: "1.a-1.b"
created: 2026-04-12
updated: 2026-04-12
tags:
  - derivatives
  - module
  - m01
  - derivative-instruments
  - markets
---

# M01: Derivative Instrument and Market Features

> **LOS 1.a**: Định nghĩa derivative và mô tả các đặc điểm cơ bản của một derivative instrument.
> **LOS 1.b**: Mô tả các đặc điểm chính của các loại derivative chính và sự khác biệt giữa exchange-traded và over-the-counter derivatives.

## 1. Derivative là gì?

**Derivative** là một hợp đồng tài chính có giá trị được **phái sinh từ** hiệu suất của một tài sản cơ sở, chỉ số hoặc lãi suất.

- Bản thân derivative không phải là một tài sản theo nghĩa truyền thống -- nó là một **hợp đồng** giữa hai bên.
- Tài sản cơ sở (underlying) có thể là hầu hết mọi thứ: cổ phiếu, trái phiếu, lãi suất, tiền tệ, hàng hóa, hoặc thậm chí một sự kiện tín dụng.

## 2. Spot Markets vs Derivative Markets

| Đặc điểm | Spot Market | Derivative Market |
|---------|------------|-------------------|
| Thanh toán | Ngay lập tức (T+1, T+2) | Ngày trong tương lai |
| Xác định giá | Cung/cầu hiện tại | Dựa trên spot price + các yếu tố carry |
| Mục đích | Mua/bán tài sản thực tế | Hedge, đầu cơ, arbitrage |

## 3. Các loại Underlying Assets

Derivatives có thể được viết trên nhiều loại underlying:

- **Equities**: cổ phiếu đơn lẻ, chỉ số chứng khoán (ví dụ: S&P 500 futures)
- **Fixed Income**: trái phiếu, lãi suất (ví dụ: interest rate swaps, bond futures)
- **Currencies**: tỷ giá hối đoái (ví dụ: FX forwards, currency options)
- **Commodities**: hàng hóa vật chất -- dầu mỏ, vàng, nông sản
- **Credit**: sự kiện tín dụng, rủi ro vỡ nợ (ví dụ: credit default swaps)

## 4. OTC vs Exchange-Traded Derivatives (ETD)

| Đặc điểm | OTC | Exchange-Traded (ETD) |
|---------|-----|----------------------|
| Tiêu chuẩn hóa | Điều khoản tùy chỉnh | Hợp đồng tiêu chuẩn hóa |
| Tính linh hoạt | Cao -- điều chỉnh theo nhu cầu đối tác | Thấp -- thông số kỹ thuật cố định |
| Rủi ro đối tác | **Có** -- tiếp xúc trực tiếp với bên kia | **Tối thiểu** -- clearinghouse bảo lãnh |
| Minh bạch | Thấp -- thỏa thuận song phương riêng tư | Cao -- giá công khai |
| Thanh khoản | Khác nhau | Thường cao |
| Quy định | Ít được quy định hơn | Được quy định chặt chẽ hơn |
| Ví dụ | Forwards, swaps, exotic options | Futures, listed options |

## 5. Central Clearinghouse

**Central clearinghouse** (CCP) đóng vai trò là đối tác cho cả hai phía của mọi giao dịch trên sàn giao dịch:

- **Bảo đảm thực hiện**: loại bỏ rủi ro tín dụng đối tác giữa các nhà giao dịch cá nhân
- **Mark-to-market (MTM)**: thanh toán hàng ngày các khoản lãi và lỗ
- **Yêu cầu ký quỹ**:
  - **Initial margin**: khoản tiền đặt cọc cần thiết để mở một vị thế
  - **Maintenance margin**: số dư tối thiểu phải được duy trì
  - **Margin call**: nếu số dư giảm xuống dưới maintenance margin, phải nạp thêm tiền để khôi phục về mức initial margin

> **Điểm mấu chốt**: Các cải cách sau năm 2008 đã thúc đẩy nhiều OTC derivatives (đặc biệt là các swaps tiêu chuẩn hóa) hướng tới thanh toán bù trừ tập trung nhằm giảm thiểu rủi ro hệ thống.

---

**Nguồn**: [[derivatives/sources/sapp-der-2026|SAPP Derivatives 2026]], tr.2-20