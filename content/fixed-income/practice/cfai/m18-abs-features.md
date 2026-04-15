---
type: practice
tags:
  - cfai-official
  - fixed-income
  - abs-features
source: "CFAI CFA1 FI Practice 2026"
module: "[[m18-abs-features]]"
---

# M18 – Asset-Backed Security (ABS) Instrument & Market Features: CFAI Practice Problems

---

## Question 1

Subordination in a securitized structure is a form of credit enhancement that:

- A. Provides external insurance against losses from borrower defaults.
- B. Creates a waterfall structure where junior tranches absorb losses before senior tranches.
- C. Requires the originator to deposit additional cash reserves with the trustee.

> [!answer]- Answer
> **B. Creates a waterfall structure where junior tranches absorb losses before senior tranches.**
>
> Subordination (also called credit tranching) is an internal credit enhancement. Losses are allocated first to the most junior (equity/subordinated) tranches, protecting the senior tranches. The senior tranches receive higher credit ratings as a result.

> [!tip]- 📖 Giải thích chi tiết
> Subordination là cơ chế tăng cường tín dụng nội bộ (internal credit enhancement):
>
> - **Tranche cấp cao (Senior)**: Được bảo vệ, nhận thanh toán trước, rating cao
> - **Tranche trung gian (Mezzanine)**: Hấp thụ tổn thất sau subordinated
> - **Tranche cấp thấp (Equity/Subordinated)**: Hấp thụ tổn thất đầu tiên, lợi nhuận cao nhất
>
> - **A sai**: Bảo hiểm bên ngoài là external credit enhancement (surety bond, letter of credit).
> - **B đúng**: Subordination tạo waterfall — junior tranche chịu tổn thất trước.
> - **C sai**: Cash reserve là một dạng internal enhancement khác (overcollateralization), không phải subordination.

---

## Question 2

Covered bonds differ from asset-backed securities (ABS) primarily because covered bonds:

- A. Are backed by a segregated pool of assets that remains on the issuer's balance sheet, providing dual recourse.
- B. Are always structured with multiple tranches to accommodate different investor risk preferences.
- C. Transfer the underlying assets to a bankruptcy-remote SPE, eliminating recourse to the issuer.

> [!answer]- Answer
> **A. Are backed by a segregated pool of assets that remains on the issuer's balance sheet, providing dual recourse.**
>
> Covered bonds offer dual recourse: investors have a claim on both the cover pool of assets and the issuing financial institution. The assets remain on the issuer's balance sheet, unlike ABS where assets are transferred to an SPE.

> [!tip]- 📖 Giải thích chi tiết
> So sánh Covered Bonds vs ABS:
>
> | | Covered Bonds | ABS |
> |--|--------------|-----|
> | Tài sản | Ở trên bảng cân đối issuer | Chuyển sang SPE |
> | Recourse | Dual (tài sản + issuer) | Chỉ có tài sản trong SPE |
> | Phá sản issuer | Nhà đầu tư có claim lên issuer | Bankruptcy remote (không ảnh hưởng) |
>
> - **A đúng**: Dual recourse là đặc điểm chính phân biệt covered bonds với ABS.
> - **B sai**: Covered bonds thường không có nhiều tranches.
> - **C sai**: Đây mô tả ABS (chuyển tài sản sang SPE), không phải covered bonds.

---

## Question 3

An ABS backed by auto loans differs from an ABS backed by credit card receivables primarily in that auto loan ABS:

- A. Has a revolving period during which principal repayments are used to purchase new receivables.
- B. Is a fully amortizing structure with scheduled principal and interest payments throughout its life.
- C. Does not face any prepayment risk because auto loans have fixed payment schedules.

> [!answer]- Answer
> **B. Is a fully amortizing structure with scheduled principal and interest payments throughout its life.**
>
> Auto loan ABS are amortizing structures — the underlying loans have fixed monthly payments of principal and interest. Credit card ABS have a revolving period (new receivables replace paid-off ones) followed by an amortization/accumulation period.

> [!tip]- 📖 Giải thích chi tiết
> So sánh Auto Loan ABS vs Credit Card ABS:
>
> | | Auto Loan ABS | Credit Card ABS |
> |--|-------------|-----------------|
> | Cấu trúc | Amortizing (trả dần) | Revolving → Amortization |
> | Gốc | Trả dần theo lịch | Revolving period: mua receivables mới |
> | Prepayment | Có (trả trước xe) | Không đáng kể trong revolving period |
> | Maturity | Ngắn hơn (3-5 năm) | Có lockout period |
>
> - **A sai**: Revolving period là đặc điểm của credit card ABS, không phải auto loan ABS.
> - **B đúng**: Auto loans amortize với gốc và lãi trả đều đặn.
> - **C sai**: Auto loan ABS vẫn có prepayment risk (người vay trả trước).

---

## Question 4

A collateralized debt obligation (CDO) differs from a traditional ABS primarily because a CDO:

- A. Is always backed by residential mortgages.
- B. Has an asset manager who actively manages the underlying portfolio of debt obligations.
- C. Does not use credit tranching to allocate risk among investors.

> [!answer]- Answer
> **B. Has an asset manager who actively manages the underlying portfolio of debt obligations.**
>
> CDOs typically have a collateral manager (asset manager) who buys and sells assets in the underlying portfolio, subject to certain constraints. Traditional ABS pools are static — once created, the assets in the pool do not change (except for amortization and defaults).

> [!tip]- 📖 Giải thích chi tiết
> CDO (Collateralized Debt Obligation) có đặc điểm:
>
> - **Quản lý chủ động**: Asset manager mua/bán tài sản trong pool
> - **Tài sản đa dạng**: Corporate bonds, loans, ABS, MBS, hoặc synthetic (CDS)
> - **Cấu trúc tranche**: Senior, Mezzanine, Equity (giống ABS)
>
> Phân loại CDO:
> - **CLO**: Collateralized Loan Obligation (backed by leveraged loans)
> - **CBO**: Collateralized Bond Obligation (backed by bonds)
> - **Synthetic CDO**: Backed by CDS, không phải tài sản thực
>
> - **A sai**: CDO được backed bởi nhiều loại debt, không chỉ mortgages.
> - **B đúng**: Active management là điểm khác biệt chính với traditional ABS.
> - **C sai**: CDO sử dụng credit tranching tương tự ABS.

---
