---
type: practice
tags:
  - cfai-official
  - derivatives
  - contingent-claims
source: "CFAI CFA1 Derivatives Practice 2026 – Volume 7"
module: "[[m03-contingent-claims]]"
---

# M03 – Contingent Claims: CFAI Practice Problems

**Source:** CFAI CFA1 Derivatives Practice 2026 – Volume 7
**Back to module:** [[m03-contingent-claims]]

---

> **Exhibit: Baywhite Structured Note**
>
> Baywhite Financial Advisors is reviewing a structured note issued by a large investment bank. The note has a maturity of 3 years and pays a coupon linked to the performance of a broad equity index. At maturity, the investor receives par value plus any appreciation in the equity index above a specified strike level. If the index declines, the investor receives only par value (subject to the credit risk of the issuer). The structured note is not listed on any exchange and trades only in the secondary OTC market.

---

## Question 1

The structured note described in the exhibit most likely contains which embedded derivative?

- A. An embedded short put on the equity index
- B. An embedded long call on the equity index
- C. An embedded long forward on the equity index

> [!answer]- Answer
> **B. An embedded long call on the equity index**
>
> The structured note pays par plus any index appreciation above a strike level at maturity. This payoff profile — upside participation with downside protection at par — is equivalent to owning a bond plus a long call option on the equity index. The investor participates in gains above the strike but is protected from losses below it.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Structured note = bond + embedded derivative. Cấu trúc payoff quyết định loại derivative được nhúng vào.
> - Nhận par + upside nếu index tăng trên strike → giống bond + long call
> - Nhận par nếu index giảm → downside protection (giống payoff call option khi OTM = 0)
>
> **Tại sao B đúng:** Payoff = par + max(0, Index − Strike). Phần $\max(0, Index - Strike)$ chính là payoff của long call option.
>
> **Tại sao A sai:** Short put tạo nghĩa vụ mua khi giá giảm → không phù hợp vì investor được bảo vệ khi index giảm.
> **Tại sao C sai:** Long forward bắt buộc nhận cả lời lẫn lỗ → không có downside protection. Structured note chỉ nhận upside.

---

## Question 2

The credit risk associated with the structured note described in the exhibit is best described as:

- A. Diversified across multiple issuers through the equity index
- B. Limited to 50% of the principal investment
- C. 100% credit risk of the issuer

> [!answer]- Answer
> **C. 100% credit risk of the issuer**
>
> The structured note is a debt obligation of the issuing investment bank. If the issuer defaults, the investor could lose the entire principal regardless of the equity index performance. The credit risk is concentrated entirely with the single issuer, not diversified through the index.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Structured note là trái phiếu do một tổ chức phát hành (issuer) → toàn bộ credit risk nằm ở issuer. Equity index chỉ quyết định return, không ảnh hưởng credit risk.
>
> **Tại sao C đúng:** Investor mua structured note = cho issuer vay tiền. Nếu issuer phá sản, investor mất toàn bộ vốn (100% credit exposure to issuer), bất kể index performance.
>
> **Tại sao A sai:** Equity index diversification chỉ ảnh hưởng market risk (return), không phải credit risk. Credit risk vẫn tập trung ở issuer duy nhất.
> **Tại sao B sai:** Không có cơ chế giới hạn credit risk ở 50% — nếu issuer default, investor có thể mất toàn bộ principal.

---

## Question 3

Compared with a direct investment in the equity index, the structured note described in the exhibit is most likely:

- A. More liquid due to its OTC trading
- B. Equally liquid since it tracks the same index
- C. Less liquid because structured notes trade in OTC markets with limited secondary market activity

> [!answer]- Answer
> **C. Less liquid because structured notes trade in OTC markets with limited secondary market activity**
>
> The exhibit states the structured note is not listed on any exchange and trades only in the secondary OTC market. OTC markets for structured notes typically have fewer participants, wider bid-ask spreads, and less transparency than exchange-traded index funds or ETFs.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Liquidity phụ thuộc vào nơi giao dịch và số lượng participants:
> - Exchange-traded (ETF, index fund): Thanh khoản cao, bid-ask spread hẹp
> - OTC (structured notes): Thanh khoản thấp, ít người tham gia, spread rộng
>
> **Tại sao C đúng:** Structured note giao dịch OTC, không niêm yết sàn → ít buyer/seller → khó mua bán → less liquid. Đề bài nói rõ "not listed on any exchange."
>
> **Tại sao A sai:** OTC trading không có nghĩa là more liquid — ngược lại, thường kém thanh khoản hơn exchange-traded.
> **Tại sao B sai:** Tracking cùng index không đảm bảo cùng liquidity. Liquidity phụ thuộc vào cơ chế giao dịch, không phải underlying asset.

---

## Question 4

An investor purchases the Baywhite structured note at par for $100. The note offers a 2% annual coupon plus participation in any index appreciation above the strike. If the equity index declines by 20% over the note's life, the investor's maximum loss is closest to:

- A. 20% of principal — the full index decline
- B. 0% — the investor is fully protected at par
- C. 2% premium plus 20% of principal at risk if the issuer defaults

> [!answer]- Answer
> **C. 2% premium plus 20% of principal at risk if the issuer defaults**
>
> Under normal conditions (no default), the investor receives par at maturity regardless of index decline — the embedded call simply expires worthless. However, the investor bears the opportunity cost of the 2% coupon (below market rates) which effectively pays for the embedded option. If the issuer defaults, the investor could lose principal. The maximum at-risk amount considers both the premium paid (embedded in the below-market coupon) and the credit risk on the principal.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Structured note risk có hai thành phần:
> 1. **Opportunity cost / premium**: Coupon thấp hơn thị trường → "trả" cho embedded option
> 2. **Credit risk**: Nếu issuer default → mất principal
>
> **Tại sao C đúng:** Investor chịu: (1) premium 2% (coupon dưới market rate để "mua" call option) + (2) 20% principal at risk nếu issuer default trong kịch bản xấu nhất. Đáp án phản ánh tổng exposure.
>
> **Tại sao A sai:** Investor không chịu 20% loss từ index decline trực tiếp — structured note có downside protection (nhận par nếu index giảm, miễn issuer không default).
> **Tại sao B sai:** "Fully protected" bỏ qua credit risk của issuer và opportunity cost của premium đã trả qua coupon thấp.
