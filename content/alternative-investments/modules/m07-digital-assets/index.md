---
title: "M07 — Digital Assets"
type: module
subject: alternative-investments
module: m07-digital-assets
los:
  - 7.a
  - 7.b
  - 7.c
  - 7.d
created: 2026-04-12
updated: 2026-04-12
tags:
  - module
  - alternative-investments
  - digital-assets
  - blockchain
  - cryptocurrency
  - DeFi
  - NFT
  - CFA-L1
---

# M07 – Introduction to Digital Assets

> **LOS 7.a–7.d** | Pages 135–166 | Source: [[alternative-investments/sources/sapp-ai-2026|SAPP 2026]]

---

## 1. Distributed Ledger Technology (LOS 7.a)

### DLT — Distributed Ledger Technology

![Centralized vs Distributed Ledger Technology](/alternative-investments/diagrams/m07-centralized-vs-dlt.png)

**Distributed ledger** là cơ sở dữ liệu được chia sẻ và đồng bộ hóa trên nhiều nút (node) mà không cần có cơ quan quản lý trung tâm.

| Lợi ích | Mô tả |
|---------|-------------|
| **Accuracy** | Các cơ chế đồng thuận (consensus mechanisms) đảm bảo tính toàn vẹn của dữ liệu |
| **Transparency** | Tất cả các bên tham gia đều có thể xem sổ cái |
| **Speed** | Thanh toán gần như tức thời (so với T+1 hoặc T+2 trong tài chính truyền thống) |
| **Peer-to-peer** | Không cần trung gian; giao dịch trực tiếp giữa các bên |

| Hạn chế | Mô tả |
|------------|-------------|
| **Security risks** | Tấn công 51%, lỗ hổng smart contract, quản lý khóa bí mật |
| **Energy consumption** | Proof-of-Work đòi hỏi năng lượng tính toán khổng lồ |
| **Scalability** | Thông lượng giao dịch hạn chế so với hệ thống tập trung |
| **Regulatory uncertainty** | Quy định toàn cầu đang thay đổi và thiếu nhất quán |

### Blockchain

![How Blockchain Works](/alternative-investments/diagrams/m07-blockchain-how.png)

Đây là một loại DLT cụ thể, tổ chức dữ liệu thành các **khối tuần tự (sequential blocks)** được liên kết với nhau bằng **cryptographic hashes**.

```
Block N-1          Block N            Block N+1
┌────────────┐    ┌────────────┐    ┌────────────┐
│ Hash(N-2)  │◄───│ Hash(N-1)  │◄───│ Hash(N)    │
│ Timestamp  │    │ Timestamp  │    │ Timestamp  │
│ Txns       │    │ Txns       │    │ Txns       │
│ Nonce      │    │ Nonce      │    │ Nonce      │
└────────────┘    └────────────┘    └────────────┘
```

- Mỗi khối chứa hash của khối trước đó, tạo thành một **chuỗi bất biến (immutable chain)**
- Nếu giả mạo bất kỳ khối nào, toàn bộ các khối phía sau sẽ bị vô hiệu hóa

### Consensus Mechanisms

![DLT Consensus Mechanisms](/alternative-investments/diagrams/m07-dlt-consensus.png)

![Proof of Work vs Proof of Stake](/alternative-investments/diagrams/m07-pow-vs-pos.png)

| Cơ chế | Proof of Work (PoW) | Proof of Stake (PoS) |
|-----------|--------------------|--------------------|
| **Cách hoạt động** | Thợ đào giải các bài toán toán học phức tạp | Validator đặt cọc token làm tài sản thế chấp |
| **Tiêu thụ năng lượng** | Rất cao | Thấp |
| **Mô hình bảo mật** | Sức mạnh tính toán | Stake kinh tế |
| **Tốc độ** | Chậm hơn (Bitcoin: ~7 TPS) | Nhanh hơn (Ethereum PoS: ~30 TPS) |
| **Ví dụ** | Bitcoin | Ethereum (sau Merge) |
| **Phần cứng** | Chuyên dụng (ASICs) | Phần cứng thông thường |
| **Rủi ro tập trung hóa** | Tập trung vào mining pool | Tập trung vào tài sản lớn |

### Smart Contracts

- **Mã tự thực thi (self-executing code)** được triển khai trên blockchain
- Tự động thực thi các điều khoản khi điều kiện được đáp ứng
- Cho phép tài chính lập trình được (DeFi), phát hành token, quản trị
- Rủi ro: lỗi hoặc lỗ hổng trong mã có thể dẫn đến bị khai thác

### Network Types

| Loại | Permissioned | Permissionless |
|------|-------------|----------------|
| **Truy cập** | Giới hạn cho các bên tham gia được ủy quyền | Mở cho tất cả mọi người |
| **Danh tính** | Người tham gia đã biết trước | Ẩn danh một phần (pseudonymous) |
| **Trường hợp sử dụng** | Doanh nghiệp, ngân hàng, chuỗi cung ứng | Tiền mã hóa công khai |
| **Ví dụ** | Hyperledger, Corda | Bitcoin, Ethereum |

---

## 2. Digital Asset Types (LOS 7.b)

![Digital Asset Types Overview](/alternative-investments/diagrams/m07-digital-asset-types.png)

### Cryptocurrencies

| Loại | Mô tả | Ví dụ |
|------|-------------|---------|
| **Bitcoin** | Tiền mã hóa đầu tiên; lưu trữ giá trị, "vàng kỹ thuật số" | BTC |
| **Altcoins** | Các tiền mã hóa thay thế với chức năng bổ sung | Ethereum (ETH) — nền tảng smart contract |
| **Stablecoins** | Gắn với tiền fiat hoặc tài sản khác; duy trì giá trị ổn định | USDT, USDC, DAI |
| **Memecoins** | Được cộng đồng thúc đẩy, không có giá trị sử dụng cơ bản | DOGE, SHIB |
| **CBDCs** | Central Bank Digital Currencies — tiền fiat kỹ thuật số do ngân hàng trung ương phát hành | Nhân dân tệ kỹ thuật số, Euro kỹ thuật số (thí điểm) |

### Tokens

| Loại | Mô tả |
|------|-------------|
| **NFT (Non-Fungible Token)** | Tài sản kỹ thuật số độc nhất đại diện cho quyền sở hữu một vật phẩm cụ thể (nghệ thuật, đồ sưu tầm, bất động sản) |
| **Utility token** | Cung cấp quyền truy cập vào sản phẩm hoặc dịch vụ trên nền tảng blockchain |
| **Security token** | Đại diện cho quyền sở hữu tài sản trong thế giới thực; chịu sự quản lý của luật chứng khoán |
| **Governance token** | Cấp quyền bỏ phiếu trong một giao thức phi tập trung |

---

## 3. Digital vs Traditional Assets (LOS 7.c)

| Thuộc tính | Digital Assets | Traditional Assets |
|-----------|---------------|-------------------|
| **Giờ giao dịch** | 24/7/365 | Chỉ trong giờ thị trường |
| **Thanh toán** | Gần tức thời (vài phút) | T+1 hoặc T+2 |
| **Trung gian** | Tùy chọn (P2P có thể thực hiện) | Bắt buộc (môi giới, custodians) |
| **Minh bạch** | On-chain, có thể xác minh công khai | Hạn chế; phụ thuộc vào báo cáo |
| **Quy định** | Đang phát triển, phân mảnh | Đã được thiết lập tốt |
| **Biến động** | Rất cao | Thấp hơn (nhìn chung) |
| **Custody** | Self-custody hoặc bên thứ ba | Custodians tổ chức |
| **Khả năng chia nhỏ** | Rất cao (8+ chữ số thập phân) | Hạn chế (theo từng cổ phần) |

---

## 4. Investment Forms (LOS 7.c)

### Direct Investment

| Phương thức | Mô tả |
|--------|-------------|
| **On-blockchain** | Mua và nắm giữ tài sản kỹ thuật số trực tiếp trên blockchain |
| **Wallet** | Hot wallet (trực tuyến, tiện lợi) và cold wallet (ngoại tuyến, an toàn) |
| **Self-custody** | Nhà đầu tư kiểm soát private keys; toàn quyền sở hữu nhưng có rủi ro mất mát |

### Indirect Investment

| Phương tiện | Mô tả |
|---------|-------------|
| **Coin trusts** | Quỹ đóng (closed-end trusts) nắm giữ các loại tiền mã hóa cụ thể (ví dụ: Grayscale) |
| **Futures** | Hợp đồng tương lai được quản lý trên các sàn giao dịch crypto (CME) |
| **ETPs / ETFs** | Sản phẩm giao dịch trao đổi theo dõi giá crypto |
| **Stocks** | Cổ phần trong các công ty liên quan đến crypto (sàn giao dịch, thợ đào) |
| **Hedge funds** | Quỹ phòng hộ tập trung vào crypto với quản lý chủ động |

---

## 5. Asset-Backed Tokens và DeFi (LOS 7.d)

### Asset-Backed Tokens

- Token đại diện cho quyền sở hữu tài sản trong thế giới thực (bất động sản, hàng hóa, nghệ thuật)
- Cho phép **sở hữu phân đoạn (fractional ownership)** và cải thiện thanh khoản cho các tài sản vốn kém thanh khoản
- Phân loại pháp lý khác nhau tùy theo từng khu vực pháp lý

### DeFi (Decentralized Finance)

- Các dịch vụ tài chính được xây dựng trên blockchain mà không cần các trung gian truyền thống
- Các ứng dụng chính:
  - **Lending/borrowing** — gửi crypto để kiếm lợi suất; vay mượn dựa trên tài sản thế chấp
  - **Decentralized exchanges (DEXs)** — automated market makers (AMMs)
  - **Yield farming** — cung cấp thanh khoản để đổi lấy phần thưởng
  - **Insurance** — giao thức bảo hiểm phi tập trung

---

## 6. Risk/Return Characteristics (LOS 7.d)

| Đặc điểm | Mô tả |
|----------------|-------------|
| **High return potential** | Lịch sử ghi nhận mức lợi nhuận vượt trội (kèm theo các đợt sụt giảm cực lớn) |
| **High volatility** | Biến động đáng kể hơn so với các tài sản truyền thống |
| **Low correlation** | Nhìn chung tương quan thấp với cổ phiếu và trái phiếu (dù có thể tăng đột biến trong khủng hoảng) |
| **Regulatory risk** | Lệnh cấm, hạn chế, hoặc quy định mới có thể ảnh hưởng mạnh đến giá trị |
| **Technology risk** | Lỗi smart contract, thất bại giao thức, tấn công mạng |
| **Custody risk** | Mất private keys = mất tài sản vĩnh viễn |
| **Market structure** | Thanh khoản phân mảnh, chất lượng sàn giao dịch không đồng đều, khả năng bị thao túng |

> **Nhận xét quan trọng:** Tài sản kỹ thuật số có thể cải thiện đa dạng hóa danh mục đầu tư nhờ tương quan thấp với tài sản truyền thống, nhưng mức biến động cực cao và các rủi ro đặc thù đòi hỏi phải định cỡ vị thế (position sizing) cẩn thận.

---

## Navigation

- **Subject Index:** [[alternative-investments/index|Alternative Investments Index]]
- **Previous Module (SAPP):** [[alternative-investments/modules/m06-hedge-funds/index|M06 – Hedge Funds]]
- **Next Module (SAPP):** [[alternative-investments/modules/m02-performance-and-returns/index|M02 – AI Performance and Returns]]