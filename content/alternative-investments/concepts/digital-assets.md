---
title: Digital Assets
type: concept
subject: alternative-investments
created: 2026-04-12
updated: 2026-04-12
tags: [digital-assets, blockchain, DLT, cryptocurrency, DeFi, smart-contracts, tokens]
---

# Digital Assets

## Distributed Ledger Technology (DLT)

**Distributed ledger** là cơ sở dữ liệu được chia sẻ và đồng bộ hóa trên nhiều nodes (máy tính) trong một mạng lưới. Không có cơ quan trung ương nào kiểm soát sổ cái này.

### Các Thuộc Tính Chính của DLT
- **Decentralization**: không có điểm lỗi hay điểm kiểm soát duy nhất
- **Immutability**: một khi đã ghi lại, dữ liệu cực kỳ khó bị thay đổi
- **Transparency**: tất cả người tham gia đều có thể xem sổ cái (trong các mạng permissionless)
- **Consensus-driven**: các thay đổi đòi hỏi sự đồng thuận giữa các thành viên mạng lưới

## Blockchain

**Blockchain** là một loại DLT cụ thể, trong đó các giao dịch được nhóm thành các **blocks** được liên kết bằng mật mã theo trình tự thời gian thành một chuỗi.

### Cách Blockchain Hoạt Động
1. Một giao dịch được khởi tạo và phát sóng đến mạng lưới
2. Các nodes xác thực giao dịch theo quy tắc đồng thuận
3. Các giao dịch hợp lệ được nhóm thành một block
4. Block được thêm vào chuỗi với một cryptographic hash liên kết với block trước đó
5. Sổ cái đã cập nhật được phân phối đến tất cả các nodes

### Các Loại Mạng Lưới

| Loại | Quyền Truy Cập | Validators | Ví Dụ |
|---|---|---|---|
| **Permissionless** (public) | Ai cũng có thể tham gia, đọc, ghi | Mở cho tất cả | Bitcoin, Ethereum |
| **Permissioned** (private) | Truy cập bị hạn chế | Các thành viên được chọn | Hyperledger, R3 Corda |

## Consensus Mechanisms

### Proof of Work (PoW)
- Các miners cạnh tranh để giải các bài toán tính toán phức tạp
- Người giải đầu tiên thêm block và nhận phần thưởng
- **Tiêu tốn nhiều năng lượng** nhưng có tính bảo mật cao
- Được sử dụng bởi: Bitcoin

### Proof of Stake (PoS)
- Các validators "stake" tiền điện tử như tài sản thế chấp
- Được chọn dựa trên quy mô stake và các yếu tố khác (thời gian, ngẫu nhiên hóa)
- **Tiết kiệm năng lượng** hơn so với PoW
- Được sử dụng bởi: Ethereum (sau sự kiện Merge)

## Smart Contracts

Các chương trình tự thực thi được lưu trữ trên blockchain, tự động thực thi các điều khoản của một thỏa thuận khi các điều kiện xác định trước được đáp ứng.

### Đặc Điểm
- **Deterministic**: cùng đầu vào luôn tạo ra cùng đầu ra
- **Trustless**: không cần bên trung gian
- **Immutable**: một khi đã triển khai, code không thể thay đổi (trong hầu hết các trường hợp)
- **Composable**: các smart contracts có thể tương tác với nhau

### Ứng Dụng
- Decentralized exchanges (DEXs)
- Các giao thức cho vay và đi vay
- Hợp đồng bảo hiểm
- Quản lý chuỗi cung ứng
- Phát hành token

## Cryptocurrencies và Tokens

### Cryptocurrencies
Các đồng tiền kỹ thuật số gốc của một mạng blockchain.

| Loại | Mô Tả | Ví Dụ |
|---|---|---|
| **Bitcoin** | Cryptocurrency đầu tiên; lưu trữ giá trị, phương tiện trao đổi | BTC |
| **Altcoins** | Tất cả cryptocurrencies ngoài Bitcoin | ETH, SOL, ADA |
| **Stablecoins** | Neo với một đồng tiền fiat hoặc hàng hóa | USDT, USDC, DAI |
| **Meme coins** | Được thúc đẩy bởi cộng đồng, không có tiện ích cơ bản | DOGE, SHIB |
| **CBDC** | Central Bank Digital Currency; được phát hành bởi ngân hàng trung ương | Nhân dân tệ kỹ thuật số, Euro kỹ thuật số |

### Tokens
Các tài sản kỹ thuật số được tạo ra trên một blockchain có sẵn (ví dụ: ERC-20 tokens trên Ethereum).

| Loại | Mô Tả |
|---|---|
| **Utility token** | Cung cấp quyền truy cập vào một sản phẩm hoặc dịch vụ trong một nền tảng |
| **Security token** | Đại diện quyền sở hữu trong một tài sản; chịu sự điều tiết của luật chứng khoán |
| **Governance token** | Cấp quyền biểu quyết trong các quyết định của giao thức |
| **Non-fungible token (NFT)** | Tài sản kỹ thuật số độc nhất đại diện quyền sở hữu của một vật phẩm cụ thể (nghệ thuật, đồ sưu tầm) |

## Các Hình Thức Đầu Tư vào Digital Assets

| Hình Thức | Mô Tả |
|---|---|
| **Direct ownership** | Mua và nắm giữ thông qua ví cryptocurrency (hot hoặc cold storage) |
| **Cryptocurrency funds** | Các quỹ được quản lý đầu tư vào tài sản kỹ thuật số |
| **Futures and derivatives** | Bitcoin/crypto futures trên các sàn giao dịch được quản lý (CME) |
| **ETFs / ETPs** | Các sản phẩm giao dịch trên sàn theo dõi giá crypto |
| **Equity of crypto companies** | Cổ phiếu của các sàn giao dịch, miners, công ty blockchain |
| **ICO / Token sales** | Initial Coin Offerings; gây quỹ bằng cách phát hành tokens mới |

## Decentralized Finance (DeFi)

Một hệ sinh thái các ứng dụng tài chính được xây dựng trên blockchain, nhằm mục tiêu tái tạo các dịch vụ tài chính truyền thống mà không cần bên trung gian.

### Các Ứng Dụng DeFi Chính

| Ứng Dụng | Mô Tả |
|---|---|
| **DEX** (Decentralized Exchange) | Giao dịch ngang hàng không qua trung gian; automated market makers (AMMs) |
| **Lending/Borrowing** | Các giao thức cho vay và đi vay tài sản crypto (Aave, Compound) |
| **Yield farming** | Cung cấp thanh khoản để kiếm lợi nhuận (phí, phần thưởng token) |
| **Staking** | Khóa tokens để xác thực giao dịch và nhận phần thưởng |
| **Derivatives** | Tài sản tổng hợp và options/futures phi tập trung |

### Rủi Ro của DeFi
- **Smart contract risk**: lỗi hoặc khai thác trong code
- **Regulatory risk**: quy định đang phát triển và chưa chắc chắn
- **Liquidity risk**: thị trường mỏng, impermanent loss
- **Oracle risk**: phụ thuộc vào các nguồn dữ liệu bên ngoài

## Các Trang Liên Quan

- [[alternative-investments/concepts/alternative-investment-overview|Alternative Investment Overview]]
- [[alternative-investments/glossary/ai-m07|Glossary: Digital Assets Terms]]