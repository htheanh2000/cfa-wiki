---
title: Arbitrage and Replication
type: concept
subject: derivatives
module: "M04"
created: 2026-04-12
updated: 2026-04-12
tags: [derivatives, arbitrage, replication, no-arbitrage, cost-of-carry]
---

# Arbitrage and Replication

## Law of One Price

Hai tài sản (hoặc danh mục) có **dòng tiền tương lai giống hệt nhau** phải có **cùng mức giá** hiện tại. Nếu không, một cơ hội arbitrage sẽ tồn tại.

$$\text{If } \text{CF}_A = \text{CF}_B \text{ in all states} \implies P_A = P_B$$

## Arbitrage

**Arbitrage** là lợi nhuận không rủi ro với mức đầu tư ròng bằng không. Chiến lược này bao gồm việc đồng thời mua tài sản bị định giá thấp và bán tài sản tương đương bị định giá cao.

**Điều kiện để arbitrage tồn tại**:
1. **Không có đầu tư ròng** (self-financing)
2. **Không có rủi ro** (kết quả chắc chắn)
3. **Lợi nhuận dương**

> Trong thị trường hiệu quả, các cơ hội arbitrage thường **rất ngắn** — chúng nhanh chóng bị khai thác và loại bỏ bởi các thành phần tham gia thị trường.

### Cơ chế Arbitrage

Nếu một phái sinh **bị định giá cao** so với danh mục replicating của nó:
- **Bán** phái sinh
- **Mua** danh mục replicating
- Khóa lợi nhuận không rủi ro

Nếu một phái sinh **bị định giá thấp**:
- **Mua** phái sinh
- **Bán** danh mục replicating
- Khóa lợi nhuận không rủi ro

## No-Arbitrage Pricing

Giá phái sinh được xác định bởi nguyên tắc **no-arbitrage**: giá phái sinh phải bằng chi phí của danh mục replicating tương ứng.

$$\text{Derivative Price} = \text{Cost of Replicating Portfolio}$$

Đây là nền tảng của mọi mô hình định giá phái sinh.

## Replication

**Replication** là việc xây dựng một danh mục từ các tài sản đang giao dịch sao cho tạo ra **cùng khoản thanh toán** như phái sinh trong mọi trạng thái tương lai.

### Ví dụ: Replicating a Forward

Một long forward trên cổ phiếu không trả cổ tức có thể được replicate bằng cách:
1. **Vay** $S_0$ theo lãi suất phi rủi ro
2. **Mua** cổ phiếu tại mức giá $S_0$

Tại thời điểm $T$:
- Cổ phiếu có giá trị $S_T$
- Hoàn trả khoản vay: $S_0(1+r)^T = F_0(T)$
- Khoản thanh toán ròng: $S_T - F_0(T)$ (giống với long forward)

Vì vậy:

$$F_0(T) = S_0 \times (1 + r)^T$$

## Cost of Carry Model

Mô hình **cost of carry** định giá forward bằng cách tính đến tất cả chi phí và lợi ích của việc nắm giữ tài sản cơ sở cho đến ngày giao hàng:

$$F_0(T) = \bigl[S_0 + PV_0(C) - PV_0(I)\bigr] \times (1 + r)^T$$

hoặc tương đương:

$$F_0(T) = S_0 \times (1 + r)^T + FV_0(C) - FV_0(I)$$

trong đó:
- $PV_0(C)$ / $FV_0(C)$ = giá trị hiện tại/tương lai của **carrying costs** (lưu kho, bảo hiểm)
- $PV_0(I)$ / $FV_0(I)$ = giá trị hiện tại/tương lai của **lợi ích** (cổ tức, coupon, convenience yield)

### Net Cost of Carry

$$\text{Net Cost of Carry} = \text{Carrying Costs} - \text{Benefits of Holding}$$

- Nếu net cost of carry > 0: giá forward > giá spot (**contango**)
- Nếu net cost of carry < 0: giá forward < giá spot (**backwardation**)

### Convenience Yield

Đối với hàng hóa, **convenience yield** đại diện cho lợi ích phi tiền tệ khi nắm giữ hàng hóa thực tế (ví dụ: đảm bảo tính liên tục của nguồn cung):

$$F_0(T) = S_0 \times (1 + r)^T + FV(C) - FV(I) - FV(\text{Convenience Yield})$$

Convenience yield cao có thể đẩy giá forward xuống thấp hơn giá spot.

## Những Hệ Quả Quan Trọng

1. **Giá forward KHÔNG phải là dự báo** về giá spot tương lai — nó được xác định bởi no-arbitrage
2. **Lãi suất phi rủi ro** đóng vai trò trung tâm trong định giá — nó đại diện cho chi phí cơ hội của vốn
3. Định giá theo **no-arbitrage** đòi hỏi khả năng **bán khống** và **vay/cho vay** theo lãi suất phi rủi ro
4. **Chi phí giao dịch** tạo ra một **dải giá** quanh mức lý thuyết, trong đó arbitrage không mang lại lợi nhuận

---

## See Also

- [[derivatives/concepts/forward-commitments|Forward Commitments]]
- [[derivatives/concepts/option-valuation|Option Valuation]]
- [[derivatives/concepts/put-call-parity|Put-Call Parity]]
- [[derivatives/formulas/der-formulas|Derivatives Formula Sheet]]
- [[derivatives/glossary/der-m04|Glossary — M04]]