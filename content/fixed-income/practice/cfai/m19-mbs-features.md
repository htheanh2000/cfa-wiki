---
type: practice
tags:
  - cfai-official
  - fixed-income
  - mbs-features
source: "CFAI CFA1 FI Practice 2026"
module: "[[m19-mbs-features]]"
---

# M19 – Mortgage-Backed Security (MBS) Instrument & Market Features: CFAI Practice Problems

---

## Question 1

A mortgage-backed security investor is concerned that falling interest rates will cause homeowners to refinance their mortgages, returning principal earlier than expected. This investor is most exposed to:

- A. Extension risk.
- B. Contraction risk.
- C. Default risk.

> [!answer]- Answer
> **B. Contraction risk.**
>
> Contraction risk is the risk that prepayments accelerate when interest rates fall, as borrowers refinance at lower rates. This shortens the MBS's average life and forces investors to reinvest the returned principal at lower prevailing rates.

> [!tip]- 📖 Giải thích chi tiết
> Prepayment risk có hai dạng:
>
> | | Contraction Risk | Extension Risk |
> |--|-----------------|----------------|
> | Lãi suất | Giảm ↓ | Tăng ↑ |
> | Hành vi người vay | Refinance (trả trước nhanh) | Giữ khoản vay (trả trước chậm) |
> | Average life | Rút ngắn | Kéo dài |
> | Rủi ro nhà đầu tư | Reinvest ở lãi suất thấp | Bị "locked in" khoản đầu tư yield thấp |
>
> - **A sai**: Extension risk xảy ra khi lãi suất tăng, không phải giảm.
> - **B đúng**: Lãi suất giảm → refinance → trả trước nhanh → contraction risk.
> - **C sai**: Default risk là rủi ro vỡ nợ, không liên quan trực tiếp đến refinancing.

---

## Question 2

Agency RMBS differ from non-agency RMBS primarily because agency RMBS:

- A. Carry a government or government-sponsored enterprise (GSE) guarantee against default losses.
- B. Are backed by subprime mortgages that have higher yields.
- C. Do not face any prepayment risk due to the agency guarantee.

> [!answer]- Answer
> **A. Carry a government or government-sponsored enterprise (GSE) guarantee against default losses.**
>
> Agency RMBS are issued or guaranteed by government agencies (Ginnie Mae) or GSEs (Fannie Mae, Freddie Mac). The guarantee protects investors against credit losses from borrower defaults. Non-agency RMBS lack this guarantee and rely on credit enhancements for protection.

> [!tip]- 📖 Giải thích chi tiết
> So sánh Agency vs Non-Agency RMBS:
>
> | | Agency RMBS | Non-Agency RMBS |
> |--|------------|-----------------|
> | Bảo lãnh | Chính phủ/GSE bảo lãnh credit risk | Không có bảo lãnh |
> | Credit risk | Gần như không có (cho nhà đầu tư) | Có — dùng credit enhancement |
> | Tài sản thế chấp | Conforming mortgages | Non-conforming, subprime, jumbo |
> | Prepayment risk | Có | Có |
>
> - **A đúng**: Agency guarantee là điểm khác biệt chính — loại bỏ credit risk cho nhà đầu tư.
> - **B sai**: Agency RMBS backed by conforming mortgages (chất lượng cao), không phải subprime.
> - **C sai**: Agency RMBS vẫn có prepayment risk — bảo lãnh chỉ che phủ credit risk.

---

## Question 3

In a CMO (Collateralized Mortgage Obligation) with sequential-pay tranches, when the underlying mortgages make principal payments, the principal is directed:

- A. Pro rata to all tranches based on their outstanding balance.
- B. Entirely to the shortest-maturity tranche until it is fully retired, then to the next tranche.
- C. First to the longest-maturity tranche to reduce overall interest rate risk.

> [!answer]- Answer
> **B. Entirely to the shortest-maturity tranche until it is fully retired, then to the next tranche.**
>
> In a sequential-pay CMO structure, all principal payments (both scheduled and prepayments) are directed to Tranche A (the first/shortest tranche) until it is completely paid off. Then principal flows to Tranche B, then C, and so on.

> [!tip]- 📖 Giải thích chi tiết
> Sequential-pay CMO (cấu trúc trả tuần tự):
>
> - **Tranche A**: Nhận tất cả gốc trước → maturity ngắn nhất → contraction risk cao
> - **Tranche B**: Nhận gốc sau khi A retired → maturity trung bình
> - **Tranche C/Z**: Nhận gốc cuối cùng → maturity dài nhất → extension risk cao
>
> Tất cả tranches nhận lãi (interest) đồng thời, nhưng gốc (principal) chỉ đến tranche đang active.
>
> - **A sai**: Pro rata là đặc điểm của pass-through, không phải sequential-pay CMO.
> - **B đúng**: Principal tuần tự từ tranche ngắn nhất đến dài nhất.
> - **C sai**: Tranche dài nhất nhận gốc cuối cùng, không phải đầu tiên.

---

## Question 4

Call protection in commercial mortgage-backed securities (CMBS) is most likely achieved through:

- A. Government agency guarantees that prevent early redemption.
- B. Structural features such as lockout periods, defeasance, and prepayment penalties.
- C. The absence of any prepayment option in commercial mortgage contracts.

> [!answer]- Answer
> **B. Structural features such as lockout periods, defeasance, and prepayment penalties.**
>
> CMBS have stronger call protection than RMBS. Common mechanisms include: lockout periods (no prepayment allowed), defeasance (borrower substitutes government securities for the mortgage), prepayment penalties (yield maintenance, fixed percentage penalties), and prepayment lockout.

> [!tip]- 📖 Giải thích chi tiết
> Call protection trong CMBS mạnh hơn RMBS, bao gồm:
>
> | Cơ chế | Mô tả |
> |--------|-------|
> | **Lockout period** | Cấm trả trước trong giai đoạn đầu |
> | **Defeasance** | Người vay thay thế mortgage bằng government securities |
> | **Yield maintenance** | Phạt trả trước = NPV chênh lệch lãi suất còn lại |
> | **Prepayment penalty** | Phí phạt cố định khi trả trước |
>
> - **A sai**: Agency guarantees liên quan đến credit risk, không phải call protection.
> - **B đúng**: CMBS sử dụng nhiều cơ chế cấu trúc để bảo vệ nhà đầu tư khỏi prepayment.
> - **C sai**: Commercial mortgages có thể trả trước, nhưng có penalties/restrictions.

---
