---
type: practice
tags:
  - cfai-official
  - alternative-investments
  - digital-assets
source: "CFAI CFA1 Alternative Investments Practice 2026"
module: "[[m07-digital-assets]]"
---

# M07 – Digital Assets: CFAI Practice Problems

**Source:** CFAI CFA1 Alternative Investments Practice 2026
**Back to module:** [[m07-digital-assets]]

---

## Question 1

The mechanism by which participants in a blockchain network agree on the validity of transactions and the current state of the distributed ledger is best described as:

- A. Cryptographic hashing
- B. Consensus protocol
- C. Smart contract execution

> [!answer]- Answer
> **B. Consensus protocol**
>
> A **consensus protocol** (such as Proof of Work or Proof of Stake) is the mechanism by which network participants (nodes) agree on which transactions are valid and the current state of the blockchain. This ensures all copies of the distributed ledger are synchronized without requiring a central authority.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> **Consensus protocol** = giao thức đồng thuận:
> - **Proof of Work (PoW):** Miners giải bài toán tính toán phức tạp → tiêu tốn năng lượng (Bitcoin)
> - **Proof of Stake (PoS):** Validators stake token → tiết kiệm năng lượng hơn (Ethereum 2.0)
> - **Delegated PoS, Byzantine Fault Tolerance,** etc.
>
> **Tại sao B đúng:** "Agree on validity of transactions" + "current state of distributed ledger" = consensus protocol. Đây là xương sống của mọi blockchain.
>
> **Tại sao A sai:** Cryptographic hashing tạo "fingerprint" cho data (bảo mật), nhưng không phải cơ chế đồng thuận.
> **Tại sao C sai:** Smart contracts là chương trình tự động thực thi trên blockchain — không phải cơ chế đồng thuận.

---

## Question 2

A blockchain's structure in which each block contains a cryptographic hash of the previous block, creating an immutable chain, is best described as:

- A. A distributed database
- B. A consensus mechanism
- C. A set of rules for cryptographic linking of blocks

> [!answer]- Answer
> **C. A set of rules for cryptographic linking of blocks**
>
> The fundamental structure of a blockchain is defined by **cryptographic linking** — each block contains the hash of the previous block, creating a tamper-evident chain. If any block is altered, its hash changes, breaking the link with the next block and invalidating the entire subsequent chain.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Cấu trúc blockchain:
> ```
> Block 1          Block 2          Block 3
> ┌──────────┐    ┌──────────┐    ┌──────────┐
> │ Data     │    │ Data     │    │ Data     │
> │ Hash: A1 │←───│ Prev: A1 │←───│ Prev: B2 │
> │          │    │ Hash: B2 │    │ Hash: C3 │
> └──────────┘    └──────────┘    └──────────┘
> ```
>
> - Mỗi block chứa hash của block trước → tạo "chuỗi" (chain)
> - Nếu ai đó thay đổi data trong Block 1 → Hash A1 thay đổi → Block 2 trở nên invalid → toàn bộ chain sau đó invalid
> - Đây là lý do blockchain được gọi là **immutable** (bất biến)
>
> **Tại sao C đúng:** "Cryptographic hash of previous block" + "immutable chain" = cryptographic linking rules.
>
> **Tại sao A sai:** Distributed database mô tả cách dữ liệu được lưu trữ (nhiều node), không phải cấu trúc liên kết block.
> **Tại sao B sai:** Consensus mechanism là cách nodes đồng thuận, không phải cấu trúc liên kết cryptographic.

---

## Question 3

A key advantage of blockchain technology for financial transactions is that it enables:

- A. Guaranteed price stability of digital assets
- B. Complete anonymity for all participants
- C. Time-efficient transactions without the need for a central intermediary

> [!answer]- Answer
> **C. Time-efficient transactions without the need for a central intermediary**
>
> Blockchain technology enables **peer-to-peer transactions** without requiring a trusted central intermediary (such as a bank, clearinghouse, or broker). This can significantly reduce transaction time (especially for cross-border payments) and lower costs by eliminating intermediary fees.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Lợi ích chính của blockchain trong tài chính:
> - **Disintermediation:** Không cần trung gian (ngân hàng, clearing house)
> - **Speed:** Giao dịch xuyên biên giới trong vài phút thay vì vài ngày
> - **Lower costs:** Giảm phí trung gian
> - **Transparency:** Mọi giao dịch được ghi lại công khai trên ledger
> - **Security:** Cryptographic protection
>
> **Tại sao C đúng:** "Time-efficient" + "without central intermediary" — đây là value proposition cốt lõi của blockchain.
>
> **Tại sao A sai:** Blockchain KHÔNG đảm bảo price stability — crypto prices cực kỳ volatile.
> **Tại sao B sai:** Blockchain không hoàn toàn anonymous — hầu hết blockchain là **pseudonymous** (địa chỉ ví công khai, identity có thể được truy vết).

---

## Question 4

Cryptocurrencies differ from traditional financial assets in that cryptocurrencies are most likely:

- A. Backed by physical assets
- B. Not valued based on expected cash flows
- C. Regulated by central banking authorities

> [!answer]- Answer
> **B. Not valued based on expected cash flows**
>
> Unlike traditional financial assets (stocks generate dividends, bonds pay coupons, real estate produces rent), most **cryptocurrencies do not generate cash flows**. Their value is derived from supply-demand dynamics, network effects, utility, and market sentiment rather than discounted expected cash flows.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> So sánh valuation approach:
>
> | Asset | Valuation Basis | Cash Flows |
> |-------|----------------|------------|
> | Stocks | DCF, P/E, DDM | Dividends, earnings ✓ |
> | Bonds | PV of coupons + principal | Coupons ✓ |
> | Real Estate | NOI / Cap rate | Rent ✓ |
> | **Crypto** | **Supply/demand, network effects** | **Không có ✗** |
>
> **Tại sao B đúng:** Crypto không tạo cash flow → không thể dùng DCF model truyền thống → "not valued based on expected cash flows."
>
> **Tại sao A sai:** Hầu hết crypto KHÔNG backed by physical assets. Một số stablecoin (USDC, USDT) được back bởi USD reserves, nhưng đây là ngoại lệ.
> **Tại sao C sai:** Crypto phần lớn CHƯA được quản lý bởi central banks — đây thực ra là đặc điểm của crypto (decentralization).

---

## Question 5

A digital asset that maintains a stable value relative to a reference asset (such as a fiat currency like the US dollar) through various mechanisms is best described as a:

- A. Utility token
- B. Stablecoin
- C. Governance token

> [!answer]- Answer
> **B. Stablecoin**
>
> A **stablecoin** is a type of cryptocurrency designed to maintain a **stable value** relative to a reference asset, typically a fiat currency (USD, EUR). Stability mechanisms include:
> - **Fiat-collateralized:** Backed 1:1 by fiat reserves (e.g., USDC, USDT)
> - **Crypto-collateralized:** Over-collateralized by other crypto assets (e.g., DAI)
> - **Algorithmic:** Supply adjusted by algorithm to maintain peg

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Các loại digital assets:
>
> | Loại | Mục đích | Ví dụ |
> |------|----------|-------|
> | **Stablecoin** | **Giữ giá ổn định, dùng làm phương tiện thanh toán/lưu trữ** | **USDC, USDT, DAI** |
> | Utility token | Truy cập dịch vụ/sản phẩm trên platform | ETH (gas fees), BNB |
> | Governance token | Quyền vote trong DAO/protocol | UNI, AAVE, MKR |
> | Security token | Đại diện quyền sở hữu tài sản thực | Tokenized real estate |
>
> **Tại sao B đúng:** "Stable value relative to reference asset (fiat currency)" = stablecoin. Đây là định nghĩa chính xác.
>
> **Tại sao A sai:** Utility token cung cấp quyền sử dụng dịch vụ, giá biến động theo thị trường.
> **Tại sao C sai:** Governance token cho quyền biểu quyết, giá không ổn định.

---

## Question 6

An investor who gains exposure to cryptocurrency markets through regulated exchange-traded futures contracts is most likely using:

- A. Indirect investment in digital assets
- B. Direct investment in digital assets
- C. Decentralized finance (DeFi) strategy

> [!answer]- Answer
> **A. Indirect investment in digital assets**
>
> Investing through **crypto futures contracts** (such as Bitcoin futures on CME) is an **indirect** method of gaining crypto exposure. The investor does not own the underlying cryptocurrency directly but gains price exposure through a regulated derivatives contract.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Phương thức đầu tư crypto:
>
> | Phương thức | Loại | Ví dụ |
> |-------------|------|-------|
> | Mua crypto trực tiếp trên exchange | Direct | Mua BTC trên Coinbase |
> | Giữ crypto trong wallet | Direct | Hardware wallet |
> | **Crypto futures (CME)** | **Indirect** | **BTC futures contract** |
> | **Crypto ETF** | **Indirect** | **Bitcoin ETF** |
> | **Crypto fund (Grayscale)** | **Indirect** | **GBTC trust** |
>
> **Tại sao A đúng:** Futures = phái sinh = không sở hữu trực tiếp crypto → indirect investment.
>
> **Tại sao B sai:** Direct investment nghĩa là mua và sở hữu crypto thực sự.
> **Tại sao C sai:** DeFi là tham gia vào protocols phi tập trung (lending, staking), không phải mua futures trên sàn regulated.

---

## Question 7

The decentralized nature of most cryptocurrency networks makes them:

- A. Easier for governments to regulate than traditional financial markets
- B. Harder for governments to regulate than traditional financial markets
- C. Equally easy to regulate as traditional financial markets

> [!answer]- Answer
> **B. Harder for governments to regulate than traditional financial markets**
>
> The **decentralized** structure of cryptocurrency networks — with no single entity controlling the network, nodes distributed globally, and pseudonymous participants — makes it significantly **harder for governments to regulate** compared to traditional financial markets where centralized exchanges, banks, and brokers serve as regulatory touchpoints.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Tại sao crypto khó quản lý:
> - **No central authority:** Không có tổ chức trung tâm nào để chính phủ ra lệnh
> - **Global & borderless:** Mạng lưới hoạt động xuyên biên giới, không thuộc quyền tài phán nào
> - **Pseudonymous:** Người dùng ẩn danh (một phần), khó xác minh danh tính
> - **Code is law:** Smart contracts tự động thực thi, không cần sự cho phép
>
> So sánh:
> - Traditional finance: SEC quản lý sàn NYSE, FDIC quản lý ngân hàng → có "chốt kiểm soát" rõ ràng
> - Crypto: DEX (sàn phi tập trung) không có chủ sở hữu → ai chịu trách nhiệm?
>
> **Tại sao B đúng:** Decentralization = không có trung tâm → khó áp đặt quy định.
>
> **Tại sao A sai:** Ngược lại — decentralization làm regulation KHÓ hơn, không dễ hơn.
> **Tại sao C sai:** Không bằng nhau — traditional finance có cấu trúc tập trung dễ quản lý hơn nhiều.

---

## Question 8

Including digital assets such as cryptocurrencies in a diversified investment portfolio:

- A. Always reduces portfolio risk
- B. May provide diversification benefits due to low correlations with traditional assets
- C. Eliminates the need for traditional asset allocation

> [!answer]- Answer
> **B. May provide diversification benefits due to low correlations with traditional assets**
>
> Cryptocurrencies have historically exhibited **low correlations** with traditional asset classes (stocks, bonds, commodities), which **may** provide diversification benefits when added to a portfolio. However, correlations can change over time, especially during market stress, so the diversification benefit is not guaranteed.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Crypto và diversification:
> - **Low correlation** với stocks/bonds → thêm vào portfolio có thể giảm overall risk
> - **"May"** rất quan trọng — correlation không cố định:
>   - 2020–2021: Crypto và stocks tương quan thấp
>   - 2022: Crypto crash cùng lúc stock market decline → correlation tăng
> - Crypto có volatility rất cao → thêm vào portfolio có thể tăng risk
>
> **Tại sao B đúng:** "May provide diversification benefits" + "low correlations" — phát biểu thận trọng và chính xác.
>
> **Tại sao A sai:** "Always reduces" là quá tuyệt đối. Crypto cực kỳ volatile → có thể TĂNG portfolio risk nếu allocation quá lớn.
> **Tại sao C sai:** Crypto không thay thế traditional asset allocation — nó chỉ là một phần bổ sung nhỏ trong portfolio.

---

## Question 9

Digital assets as an asset class are best characterized by:

- A. Low returns, low risk, and high correlations with equities
- B. High returns, high risk, and low correlations with traditional assets
- C. Moderate returns, moderate risk, and stable correlations

> [!answer]- Answer
> **B. High returns, high risk, and low correlations with traditional assets**
>
> Digital assets (particularly cryptocurrencies) are characterized by:
> - **High historical returns** (Bitcoin has been one of the best-performing assets over certain periods)
> - **High risk** (extreme price volatility, regulatory uncertainty, technology risk)
> - **Low correlations** with traditional assets (stocks, bonds) — though this can vary over time

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Risk-return profile của digital assets:
>
> | Đặc điểm | Digital Assets | Traditional Assets |
> |----------|---------------|-------------------|
> | Return | Rất cao (nhưng biến động) | Trung bình, ổn định hơn |
> | Risk (volatility) | Rất cao (50–100%+ annualized) | Thấp-trung bình (15–20%) |
> | Correlation với S&P 500 | Thấp (thay đổi theo thời kỳ) | N/A |
> | Regulation | Đang phát triển, không chắc chắn | Rõ ràng, established |
>
> **Tại sao B đúng:** Ba đặc điểm chính: high return + high risk + low correlation. Đây là lý do crypto hấp dẫn nhưng cũng rất nguy hiểm.
>
> **Tại sao A sai:** Low returns, low risk — hoàn toàn ngược với thực tế crypto. High correlations cũng sai.
> **Tại sao C sai:** Moderate returns/risk — understate mức độ biến động thực sự. "Stable correlations" cũng sai vì correlations thay đổi đáng kể theo thời gian.
