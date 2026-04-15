---
type: practice
tags:
  - cfai-official
  - portfolio-management
  - risk-return
  - CAPM
  - CML
  - SML
  - beta
  - systematic-risk
source: "CFAI CFA1 Portfolio Management Practice 2026, Volume 9"
module: "[[m02-risk-return-part-ii]]"
---

# M02 – Portfolio Risk and Return: Part II — CFAI Practice Problems

**Source:** CFAI CFA1 Portfolio Management Practice 2026, Volume 9
**Back to module:** [[m02-risk-return-part-ii]]
**Glossary**: [[portfolio-management/glossary/m02-risk-return-part-ii|M02 Terms]]

---

## Question 1

The line that represents all possible combinations of the risk-free asset and an optimal risky portfolio is **best described** as the:

- A. security market line (SML).
- B. capital allocation line (CAL).
- C. efficient frontier.

> [!answer]- Answer
> **B. capital allocation line (CAL).**
>
> The **CAL** is a straight line from the risk-free rate through the optimal risky portfolio, representing all combinations of lending/borrowing at the risk-free rate and investing in the risky portfolio. The SML (A) plots expected return vs. beta. The efficient frontier (C) shows only risky portfolios.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** CAL (Capital Allocation Line) nối $R_f$ với optimal risky portfolio trên đồ thị $E(R)$ vs. $\sigma$. Mỗi điểm trên CAL là một tổ hợp (mix) giữa risk-free asset và risky portfolio.
> **Tại sao A sai:** SML (Security Market Line) dùng trục $\beta$ (không phải $\sigma$), vẽ mối quan hệ expected return vs. systematic risk theo CAPM.
> **Tại sao C sai:** Efficient frontier chỉ chứa risky portfolios, không bao gồm risk-free asset.

---

## Question 2

The **maximum diversification benefit** occurs when the correlation between two assets is:

- A. $\rho = -1.0$.
- B. $\rho = 0.0$.
- C. $\rho = +1.0$.

> [!answer]- Answer
> **A. $\rho = -1.0$.**
>
> When $\rho = -1.0$ (perfectly negatively correlated), the two assets move in perfectly opposite directions. This allows construction of a **zero-variance portfolio** — the maximum possible diversification benefit.
>
> $$\text{When } \rho = -1: \quad \sigma_p = |w_1 \sigma_1 - w_2 \sigma_2|$$

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** $\rho = -1.0$ cho diversification benefit tối đa. Có thể tạo portfolio với $\sigma_p = 0$ bằng cách chọn $w_1 = \frac{\sigma_2}{\sigma_1 + \sigma_2}$.
> **Tại sao B sai:** $\rho = 0$ cho diversification tốt nhưng không tối đa — vẫn có residual risk.
> **Tại sao C sai:** $\rho = +1.0$ → không có diversification benefit. Portfolio σ = weighted average σ.

---

## Question 3

An investor's **indifference curve** represents combinations of risk and return that provide the investor with:

- A. the highest return.
- B. equal utility (satisfaction).
- C. the lowest risk.

> [!answer]- Answer
> **B. equal utility (satisfaction).**
>
> An **indifference curve** shows all risk–return combinations that give an investor the **same level of utility**. The investor is "indifferent" among all points on the same curve. Higher curves (northwest) represent higher utility.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Indifference curve (đường bàng quan) = tập hợp các điểm $(σ, E(R))$ cho cùng mức utility. Nhà đầu tư "bàng quan" (indifferent) giữa các điểm trên cùng một đường vì chúng mang lại satisfaction như nhau.
> **Tại sao A sai:** Highest return chỉ là một điểm, không phải một đường cong.
> **Tại sao C sai:** Lowest risk cũng chỉ là một điểm (GMV portfolio).
>
> **Đặc điểm:** Risk-averse investors có indifference curves dốc lên (slope dương) và cong lên (convex). Risk aversion càng cao → curves càng dốc.

---

## Question 4

In the capital market theory, homogeneous expectations mean that all investors agree on expectations about returns, variances, and covariances. Under this assumption, all investors hold the same optimal risky portfolio and combine it with:

- A. other risky portfolios.
- B. risk-free assets.
- C. only domestic assets.

> [!answer]- Answer
> **B. risk-free assets.**
>
> Under **homogeneous expectations**, all investors identify the **same** optimal risky portfolio (the market portfolio). They then combine this portfolio with the **risk-free asset** in different proportions based on their individual risk preferences. This is the **Separation Theorem**.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Separation Theorem (Tobin): tách quyết định đầu tư thành 2 bước: (1) Chọn optimal risky portfolio (giống nhau cho mọi người = market portfolio). (2) Phân bổ giữa risky portfolio và risk-free asset (khác nhau tùy risk aversion). Vậy mọi người kết hợp market portfolio với risk-free assets.
> **Tại sao A sai:** Không cần kết hợp nhiều risky portfolios — chỉ cần một (market portfolio).
> **Tại sao C sai:** "Only domestic" là hạn chế không cần thiết — market portfolio bao gồm tất cả investable assets.

---

## Question 5

Under the assumptions of CAPM, the optimal risky portfolio for all investors is the:

- A. global minimum-variance portfolio.
- B. market portfolio.
- C. equally weighted portfolio.

> [!answer]- Answer
> **B. market portfolio.**
>
> Under CAPM assumptions (including homogeneous expectations, no taxes, no transaction costs), all investors hold the **market portfolio** as their optimal risky portfolio. The market portfolio contains **all investable assets** weighted by their market capitalization.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Trong CAPM, homogeneous expectations → mọi người có cùng efficient frontier → cùng tangency portfolio → đó chính là market portfolio (chứa tất cả tài sản theo market-cap weight).
> **Tại sao A sai:** GMV portfolio có σ thấp nhất nhưng không phải optimal (Sharpe ratio không cao nhất).
> **Tại sao C sai:** Equally weighted portfolio gán trọng số bằng nhau cho mọi tài sản — không phải kết quả của CAPM optimization (CAPM dùng market-cap weights).

---

## Question 6

The market portfolio in CAPM theory includes:

- A. only stocks and bonds.
- B. only publicly traded securities.
- C. all investable assets (stocks, bonds, real estate, etc.).

> [!answer]- Answer
> **C. all investable assets (stocks, bonds, real estate, etc.).**
>
> In theory, the **market portfolio** contains **every investable asset** in the world — stocks, bonds, real estate, commodities, human capital, etc. — each weighted by its relative market value. In practice, a broad market index (like a global equity index) is used as a proxy.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao C đúng:** Market portfolio theo lý thuyết CAPM bao gồm TẤT CẢ tài sản có thể đầu tư (investable assets): cổ phiếu, trái phiếu, bất động sản, hàng hóa, v.v. — mỗi loại theo tỷ trọng vốn hóa thị trường.
> **Tại sao A sai:** Chỉ stocks và bonds là quá hẹp — thiếu real estate, commodities, v.v.
> **Tại sao B sai:** "Publicly traded" loại trừ private equity, real estate, v.v.
>
> **Thực tế:** Market portfolio "thật" không thể quan sát được (unobservable). Các nhà đầu tư dùng broad market index (MSCI World, S&P 500) làm proxy. Đây là Roll's Critique — CAPM không thể kiểm chứng hoàn toàn vì true market portfolio không biết.

---

## Question 7

When all investors have homogeneous expectations, the CAL that uses the market portfolio as the optimal risky portfolio:

- A. is the market portfolio itself.
- B. is called the security market line (SML).
- C. is called the capital market line (CML).

> [!answer]- Answer
> **A. is the market portfolio.**
>
> Wait — the answer key says A. The question asks about the CAL that uses the market portfolio. Under homogeneous expectations, this special CAL **is** called the CML. However, the answer key indicates A — "is the market portfolio" — meaning the tangency portfolio on this CAL is the market portfolio itself. The CAL drawn from $R_f$ through the market portfolio defines the CML, and the risky portfolio on it **is** the market portfolio.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** Khi mọi nhà đầu tư có homogeneous expectations, optimal risky portfolio trên CAL chính là market portfolio. CAL này được gọi là CML (Capital Market Line), và risky portfolio duy nhất trên đó **là** market portfolio.
> **Tại sao B sai:** SML (Security Market Line) vẽ E(R) vs. β, khác CML (vẽ E(R) vs. σ).
> **Tại sao C sai:** CML là tên gọi đúng của đường CAL đặc biệt này, nhưng câu hỏi hỏi về bản chất — tangency portfolio trên CML chính là market portfolio.

---

## Question 8

A portfolio that plots **above** the CML is:

- A. an efficient portfolio.
- B. an undervalued portfolio.
- C. unachievable given current assumptions.

> [!answer]- Answer
> **C. unachievable given current assumptions.**
>
> The **CML** represents the **best possible** risk–return combinations (highest Sharpe ratio). No portfolio can plot above the CML under CAPM assumptions — such a portfolio would offer a higher return per unit of risk than is possible, making it **unachievable**.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao C đúng:** CML là đường hiệu quả nhất (highest Sharpe ratio). Không portfolio nào nằm phía trên CML vì CML đã đại diện cho maximum return tại mỗi mức risk. Điểm trên CML → unachievable.
> **Tại sao A sai:** Efficient portfolios nằm **trên** CML (on the CML), không phải above it.
> **Tại sao B sai:** "Undervalued" là khái niệm dùng cho SML (khi actual return > expected return theo CAPM). Trên CML, không có khái niệm undervalued.

---

## Question 9

An investor who **borrows** at the risk-free rate and invests more than 100% in the market portfolio holds a:

- A. lending portfolio.
- B. borrowing portfolio.
- C. minimum-variance portfolio.

> [!answer]- Answer
> **B. borrowing portfolio.**
>
> A **borrowing portfolio** is created when the investor borrows money at $R_f$ and invests the total (own funds + borrowed) in the market portfolio. The weight in the risky portfolio exceeds 1.0 ($w_m > 1$, $w_f < 0$). This portfolio lies on the CML **to the right** of the market portfolio — higher expected return but also higher risk.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Borrowing portfolio = vay tại $R_f$ để đầu tư thêm vào market portfolio. Ví dụ: vay 30% → $w_m = 1.30$, $w_f = -0.30$. Portfolio nằm bên phải market portfolio trên CML → rủi ro và return đều cao hơn market.
> **Tại sao A sai:** Lending portfolio = cho vay tại $R_f$ (tức đầu tư một phần vào risk-free asset). $w_m < 1$, $w_f > 0$. Nằm bên trái market portfolio trên CML.
> **Tại sao C sai:** Minimum-variance portfolio có σ thấp nhất trên efficient frontier, không liên quan đến leverage.

---

## Question 10

An investor who invests **part** of the portfolio in the risk-free asset and the remainder in the market portfolio holds a:

- A. lending portfolio.
- B. borrowing portfolio.
- C. leveraged portfolio.

> [!answer]- Answer
> **A. lending portfolio.**
>
> A **lending portfolio** has $0 < w_m < 1$ and $w_f > 0$. The investor "lends" money to the government (buys T-bills) with part of the portfolio and invests the rest in the market portfolio. This portfolio lies on the CML **between** $R_f$ and the market portfolio — lower risk and lower return than the market portfolio.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** Lending portfolio = đầu tư một phần vào risk-free asset (= "cho vay" cho chính phủ qua T-bills) và phần còn lại vào market portfolio. $w_f > 0$, $w_m < 1$. Nằm giữa $R_f$ và $M$ trên CML.
> **Tại sao B sai:** Borrowing = vay để đầu tư thêm → $w_m > 1$.
> **Tại sao C sai:** Leveraged portfolio = borrowing portfolio ($w_m > 1$).
>
> **So sánh Q9 & Q10:** Lending portfolio (trái market M trên CML, ít rủi ro hơn) vs. Borrowing portfolio (phải market M, rủi ro hơn). Cả hai đều nằm trên CML.

---

## Question 11

Diversification **eliminates** which type of risk?

- A. Systematic risk.
- B. Total risk.
- C. Nonsystematic risk.

> [!answer]- Answer
> **C. Nonsystematic risk.**
>
> **Nonsystematic risk** (also called unsystematic, specific, idiosyncratic, or diversifiable risk) is unique to individual companies or industries. By holding many assets, these firm-specific risks cancel each other out. **Systematic risk** (market risk) cannot be eliminated through diversification.
>
> $$\text{Total Risk} = \text{Systematic Risk} + \text{Nonsystematic Risk}$$

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao C đúng:** Nonsystematic risk (rủi ro phi hệ thống) = rủi ro riêng của từng công ty/ngành (CEO từ chức, sản phẩm lỗi, kiện tụng). Khi đa dạng hóa đủ, các sự kiện riêng lẻ triệt tiêu nhau → risk này biến mất.
> **Tại sao A sai:** Systematic risk (rủi ro hệ thống) = market risk (lãi suất, lạm phát, suy thoái) — ảnh hưởng toàn thị trường, KHÔNG thể diversify away.
> **Tại sao B sai:** Total risk = systematic + nonsystematic. Diversification chỉ loại bỏ phần nonsystematic, không loại bỏ toàn bộ total risk.

---

## Question 12

Which of the following events is **most likely** an example of **nonsystematic risk**?

- A. An unexpected increase in inflation.
- B. The resignation of a company's CEO.
- C. A global recession.

> [!answer]- Answer
> **B. The resignation of a company's CEO.**
>
> The CEO resignation is a **company-specific** event that affects only that particular company — this is **nonsystematic risk**. Inflation (A) and recession (C) affect the entire market and are examples of **systematic risk**.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** CEO từ chức chỉ ảnh hưởng đến một công ty cụ thể → nonsystematic (firm-specific) risk. Có thể diversify away bằng cách nắm nhiều cổ phiếu.
> **Tại sao A sai:** Lạm phát bất ngờ ảnh hưởng toàn bộ thị trường → systematic risk.
> **Tại sao C sai:** Suy thoái toàn cầu ảnh hưởng mọi tài sản → systematic risk.
>
> **Mẹo phân biệt:** Hỏi "sự kiện này ảnh hưởng một công ty hay toàn thị trường?" Một công ty → nonsystematic. Toàn thị trường → systematic.

---

## Question 13

Investors are compensated only for bearing:

- A. nonsystematic risk.
- B. systematic risk.
- C. total risk.

> [!answer]- Answer
> **B. systematic risk.**
>
> In equilibrium, investors are compensated **only** for **systematic risk** (beta risk) because nonsystematic risk can be eliminated through diversification. Since nonsystematic risk is "free" to eliminate, the market does not reward investors for bearing it.
>
> $$E(R_i) = R_f + \beta_i [E(R_m) - R_f]$$
>
> Only $\beta$ (systematic risk) determines expected return — not total risk ($\sigma$).

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Theo CAPM, chỉ systematic risk (đo bằng β) được "trả giá" (priced). Return kỳ vọng chỉ phụ thuộc β, không phụ thuộc σ. Lý do: nonsystematic risk có thể loại bỏ miễn phí bằng diversification → thị trường không thưởng cho rủi ro mà nhà đầu tư tự chọn gánh chịu.
> **Tại sao A sai:** Nonsystematic risk không được compensated — diversify away nên không cần phần bù.
> **Tại sao C sai:** Total risk bao gồm cả nonsystematic — phần này không được bù đắp.
>
> **Implication:** Một cổ phiếu có σ rất cao nhưng β thấp sẽ có expected return thấp. Ngược lại, β cao → expected return cao bất kể σ.

---

## Question 14

The **total variance** of a security's returns can be decomposed into:

- A. market risk and credit risk.
- B. systematic risk only.
- C. systematic variance and nonsystematic variance.

> [!answer]- Answer
> **C. systematic variance and nonsystematic variance.**
>
> $$\sigma_i^2 = \beta_i^2 \sigma_m^2 + \sigma_{\varepsilon_i}^2$$
>
> where:
> - $\beta_i^2 \sigma_m^2$ = systematic variance (explained by market)
> - $\sigma_{\varepsilon_i}^2$ = nonsystematic variance (firm-specific, unexplained)

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao C đúng:** Total variance phân tách thành: (1) Systematic variance ($\beta_i^2 \sigma_m^2$) — phần do thị trường gây ra. (2) Nonsystematic variance ($\sigma_{\varepsilon}^2$) — phần riêng của tài sản. Công thức: $\sigma_i^2 = \beta_i^2 \sigma_m^2 + \sigma_{\varepsilon}^2$.
> **Tại sao A sai:** "Credit risk" là loại rủi ro cụ thể (trái phiếu), không phải cách phân tách variance theo CAPM.
> **Tại sao B sai:** Nếu chỉ có systematic risk thì total variance = systematic variance, bỏ sót nonsystematic.

---

## Question 15

Consider the following data for three securities:

| Security | Expected Return | Standard Deviation ($\sigma$) | Beta ($\beta$) |
|----------|----------------:|------------------------------:|----------------:|
| 1        | 10%             | 25%                           | 0.6             |
| 2        | 12%             | 20%                           | 0.7             |
| 3        | 14%             | 15%                           | 0.8             |

Which security has the **highest total risk**?

- A. Security 1.
- B. Security 2.
- C. Security 3.

> [!answer]- Answer
> **A. Security 1.**
>
> **Total risk** is measured by **standard deviation** ($\sigma$). Security 1 has the highest $\sigma = 25\%$, therefore the highest total risk.
>
> Note: Security 3 has the highest beta (highest systematic risk) but the **lowest** total risk. This means Security 1 has substantial nonsystematic risk.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** Total risk = σ (standard deviation). Security 1: σ = 25% > Security 2: σ = 20% > Security 3: σ = 15%. Security 1 rủi ro tổng thể cao nhất.
> **Tại sao B, C sai:** σ thấp hơn Security 1.
>
> **Insight quan trọng:** Security 1 có σ cao nhất nhưng β thấp nhất! Điều này nghĩa là phần lớn risk của Security 1 là **nonsystematic risk** (không được compensated). Security 3 ngược lại: σ thấp nhất nhưng β cao nhất → hầu hết risk là systematic.

---

## Question 16

Using the same data from Question 15, which security has the **highest systematic risk**?

- A. Security 1.
- B. Security 2.
- C. Security 3.

> [!answer]- Answer
> **C. Security 3.**
>
> **Systematic risk** is measured by **beta** ($\beta$). Security 3 has the highest $\beta = 0.8$, therefore the highest systematic risk (highest sensitivity to market movements).

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao C đúng:** Systematic risk đo bằng β. Security 3: β = 0.8 > Security 2: β = 0.7 > Security 1: β = 0.6. Security 3 nhạy cảm nhất với biến động thị trường.
> **Tại sao A sai:** Security 1 có β thấp nhất (0.6) dù σ cao nhất — phần lớn risk là nonsystematic.
> **Tại sao B sai:** Security 2 có β = 0.7, nằm giữa.
>
> **So sánh Q15 & Q16:** Total risk ≠ systematic risk. Một cổ phiếu có thể có total risk cao nhưng systematic risk thấp (nhiều nonsystematic risk chưa diversify).

---

## Question 17

Using the same data from Question 15, which security has the **least market risk**?

- A. Security 1.
- B. Security 2.
- C. Security 3.

> [!answer]- Answer
> **A. Security 1.**
>
> **Market risk** = **systematic risk**, measured by beta. Security 1 has the **lowest** $\beta = 0.6$, indicating the least sensitivity to market movements.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** Market risk = systematic risk = β. Security 1 có β = 0.6, thấp nhất → ít bị ảnh hưởng bởi biến động thị trường nhất. Khi market tăng/giảm 1%, Security 1 chỉ tăng/giảm ~0.6%.
> **Tại sao B, C sai:** β cao hơn → market risk cao hơn.

---

## Question 18

In the **single-index model** (market model), the **intercept** ($\alpha_i$) represents:

- A. the security's beta.
- B. the security's alpha (abnormal return when market excess return is zero).
- C. the security's total return.

> [!answer]- Answer
> **B. the security's alpha (abnormal return when market excess return is zero).**
>
> The **market model** is:
>
> $$R_i = \alpha_i + \beta_i R_m + \varepsilon_i$$
>
> The intercept $\alpha_i$ represents the security's **alpha** — the return component that is independent of the market. If the market has zero return, the security is expected to earn $\alpha_i$.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Trong market model $R_i = \alpha_i + \beta_i R_m + \varepsilon_i$, intercept ($\alpha_i$) = alpha = phần return không phụ thuộc vào thị trường. Nếu $R_m = 0$, expected return = $\alpha_i$. Alpha dương nghĩa là security "outperform" so với mức dự đoán bởi CAPM.
> **Tại sao A sai:** Beta là slope (hệ số góc), không phải intercept.
> **Tại sao C sai:** Total return = $\alpha_i + \beta_i R_m + \varepsilon_i$, bao gồm cả market component và error term.

---

## Question 19

In the market model, the **slope** coefficient represents:

- A. nonsystematic risk.
- B. systematic risk (beta).
- C. total risk.

> [!answer]- Answer
> **B. systematic risk (beta).**
>
> The slope of the market model regression ($\beta_i$) measures the sensitivity of the security's return to market returns — this is **systematic risk** (beta).
>
> $$\beta_i = \frac{\text{Cov}(R_i, R_m)}{\sigma_m^2}$$

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Slope = $\beta_i$ = độ nhạy cảm của return tài sản với return thị trường. $\beta_i = \frac{\text{Cov}(R_i, R_m)}{\text{Var}(R_m)}$. Đây chính là thước đo systematic risk.
> **Tại sao A sai:** Nonsystematic risk được phản ánh qua error term ($\varepsilon_i$), không phải slope.
> **Tại sao C sai:** Total risk = σ, bao gồm cả systematic và nonsystematic.

---

## Question 20

The **CAPM** equation gives the:

- A. expected return of an asset based on its systematic risk.
- B. actual return of an asset.
- C. total risk of an asset.

> [!answer]- Answer
> **A. expected return of an asset based on its systematic risk.**
>
> $$E(R_i) = R_f + \beta_i [E(R_m) - R_f]$$
>
> CAPM determines the **expected (required) return** based solely on the asset's **beta** (systematic risk). It does not predict actual returns, and it does not measure total risk.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** CAPM: $E(R_i) = R_f + \beta_i [E(R_m) - R_f]$. Expected return chỉ phụ thuộc vào $\beta$ (systematic risk). Risk premium = $\beta_i \times$ market risk premium.
> **Tại sao B sai:** CAPM cho expected return, không phải actual return. Actual return có thể cao hơn hoặc thấp hơn expected.
> **Tại sao C sai:** CAPM không đo total risk. Total risk = σ, trong khi CAPM chỉ dùng β.

---

## Question 21

The **beta** of the **market portfolio** is:

- A. 0.
- B. equal to 1.0.
- C. greater than 1.0.

> [!answer]- Answer
> **B. equal to 1.0.**
>
> By definition, the market portfolio has $\beta_m = 1.0$:
>
> $$\beta_m = \frac{\text{Cov}(R_m, R_m)}{\text{Var}(R_m)} = \frac{\text{Var}(R_m)}{\text{Var}(R_m)} = 1.0$$

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** β của market portfolio luôn = 1.0 theo định nghĩa. $\beta_m = \frac{\text{Cov}(R_m, R_m)}{\sigma_m^2} = \frac{\sigma_m^2}{\sigma_m^2} = 1$. Market portfolio là benchmark — mọi tài sản khác so sánh với nó.
> **Tại sao A sai:** β = 0 là risk-free asset.
> **Tại sao C sai:** β > 1 = tài sản rủi ro hơn thị trường (aggressive stock).
>
> **Benchmark:** $\beta < 1$: defensive (ít biến động hơn market). $\beta = 1$: market. $\beta > 1$: aggressive (biến động hơn market).

---

## Question 22

According to CAPM, the expected return of an asset is determined by the:

- A. asset's beta (systematic risk).
- B. asset's standard deviation (total risk).
- C. asset's nonsystematic risk.

> [!answer]- Answer
> **A. asset's beta (systematic risk).**
>
> CAPM states that **only beta** determines expected return. Standard deviation (total risk) and nonsystematic risk are **not** priced — only systematic risk is compensated.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** $E(R_i) = R_f + \beta_i[E(R_m) - R_f]$. Chỉ có β quyết định expected return. Hai tài sản có cùng β sẽ có cùng expected return, bất kể σ khác nhau thế nào.
> **Tại sao B sai:** Standard deviation bao gồm nonsystematic risk — phần không được compensated.
> **Tại sao C sai:** Nonsystematic risk có thể diversify away → thị trường không thưởng cho nó.

---

## Question 23

An asset with a **negative beta** ($\beta < 0$) is expected to have a return that is:

- A. less than the risk-free rate ($E(R_i) < R_f$).
- B. equal to the risk-free rate.
- C. greater than the market return.

> [!answer]- Answer
> **A. less than the risk-free rate ($E(R_i) < R_f$).**
>
> Using CAPM with $\beta < 0$:
>
> $$E(R_i) = R_f + \beta_i [E(R_m) - R_f]$$
>
> Since $[E(R_m) - R_f] > 0$ (market risk premium is positive) and $\beta_i < 0$, the product is **negative**, making $E(R_i) < R_f$.
>
> Example: If $R_f = 4\%$, $E(R_m) = 10\%$, $\beta = -0.5$:
> $$E(R_i) = 4\% + (-0.5)(10\% - 4\%) = 4\% - 3\% = 1\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao A đúng:** Negative beta → return kỳ vọng thấp hơn risk-free rate. Nhà đầu tư chấp nhận return thấp vì tài sản negative-beta hoạt động như **hedge** — tăng giá khi thị trường giảm. Giá trị bảo hiểm (insurance value) bù đắp cho return thấp.
> **Tại sao B sai:** $E(R_i) = R_f$ chỉ khi $\beta = 0$ (risk-free asset).
> **Tại sao C sai:** $E(R_i) > E(R_m)$ chỉ khi $\beta > 1$.
>
> **Ví dụ thực tế:** Gold, put options, VIX futures thường có β âm hoặc gần 0 — chúng tăng giá khi thị trường suy giảm.

---

## Question 24

An asset with $\beta = 1.0$ is expected to have a return:

- A. equal to the risk-free rate.
- B. equal to the expected market return (excess market return from risk-free).
- C. double the market return.

> [!answer]- Answer
> **B. equal to the expected market return.**
>
> $$E(R_i) = R_f + 1.0 \times [E(R_m) - R_f] = E(R_m)$$
>
> An asset with $\beta = 1.0$ has the same systematic risk as the market and is expected to earn the **same return** as the market portfolio.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** Khi $\beta = 1.0$: $E(R_i) = R_f + 1.0 \times [E(R_m) - R_f] = R_f + E(R_m) - R_f = E(R_m)$. Tài sản di chuyển 1:1 với thị trường → expected return = market return.
> **Tại sao A sai:** $E(R_i) = R_f$ chỉ khi $\beta = 0$.
> **Tại sao C sai:** "Double the market return" không phải kết quả của CAPM với $\beta = 1$.

---

## Question 25

The **Security Market Line (SML)** plots:

- A. expected return vs. standard deviation.
- B. expected return vs. beta.
- C. actual return vs. total risk.

> [!answer]- Answer
> **B. expected return vs. beta.**
>
> The **SML** is the graphical representation of CAPM. It plots **expected return** on the y-axis against **beta** ($\beta$) on the x-axis:
>
> $$E(R_i) = R_f + \beta_i [E(R_m) - R_f]$$
>
> The slope of the SML is the **market risk premium** $[E(R_m) - R_f]$, and the y-intercept is $R_f$.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** SML vẽ $E(R)$ vs. $\beta$. Mọi tài sản và portfolio (efficient hay không) đều phải nằm trên SML nếu thị trường cân bằng (equilibrium). Slope = market risk premium.
> **Tại sao A sai:** $E(R)$ vs. σ là đồ thị CML (Capital Market Line), không phải SML.
> **Tại sao C sai:** "Actual return vs. total risk" không phải đồ thị nào trong CAPM.
>
> **Phân biệt CML vs. SML:**
> | | CML | SML |
> |---|---|---|
> | Trục x | σ (total risk) | β (systematic risk) |
> | Áp dụng cho | Efficient portfolios only | Tất cả assets & portfolios |
> | Đo lường | Risk–return of efficient portfolios | Pricing of any asset |

---

## Question 26

The SML applies to:

- A. efficient portfolios only.
- B. all individual assets and portfolios.
- C. the market portfolio only.

> [!answer]- Answer
> **B. all individual assets and portfolios.**
>
> Unlike the CML (which applies only to efficient portfolios), the **SML applies to ALL** individual securities and portfolios — efficient or not. Every asset should be priced according to its beta. If it plots above the SML, it is **undervalued**; if below, it is **overvalued**.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao B đúng:** SML áp dụng cho TẤT CẢ tài sản và portfolios. Trong equilibrium, mọi tài sản nằm trên SML. Nếu asset nằm trên SML → undervalued (alpha dương, nên mua). Nếu dưới → overvalued (alpha âm, nên bán).
> **Tại sao A sai:** "Efficient portfolios only" là CML, không phải SML.
> **Tại sao C sai:** Market portfolio chỉ là một điểm trên SML (tại $\beta = 1$).
>
> **Đây là khác biệt quan trọng nhất giữa CML và SML:** CML chỉ cho efficient portfolios, SML cho tất cả.

---

## Question 27

Given the following information:
- Risk-free rate: $R_f = 4\%$
- Expected market return: $E(R_m) = 10\%$
- Beta of Stock A: $\beta_A = 1.33$

The **expected return** of Stock A according to CAPM is **closest to**:

- A. 10.0%.
- B. 12.0%.
- C. 14.0%.

> [!answer]- Answer
> **B. 12.0%.**
>
> $$E(R_A) = R_f + \beta_A [E(R_m) - R_f]$$
>
> $$E(R_A) = 4\% + 1.33 \times (10\% - 4\%)$$
>
> $$= 4\% + 1.33 \times 6\% = 4\% + 7.98\% = 11.98\% \approx 12.0\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Bước tính:**
> 1. Market risk premium: $E(R_m) - R_f = 10\% - 4\% = 6\%$
> 2. Risk premium của Stock A: $\beta_A \times 6\% = 1.33 \times 6\% = 7.98\%$
> 3. Expected return: $R_f + 7.98\% = 4\% + 7.98\% = 11.98\% \approx 12.0\%$
>
> **Tại sao B đúng (12.0%):** Tính toán chính xác theo CAPM.
> **Tại sao A sai (10.0%):** Đây là market return — chỉ đúng nếu $\beta = 1.0$.
> **Tại sao C sai (14.0%):** Có thể do nhân sai: dùng $\beta = 1.67$ hoặc market premium = 7.5%.

---

## Question 28

A stock has the following characteristics:
- Expected return: $E(R_i) = 12\%$
- Risk-free rate: $R_f = 3\%$
- Beta: $\beta_i = 1.5$

The **expected market return** $E(R_m)$ implied by CAPM is **closest to**:

- A. 6.0%.
- B. 9.0%.
- C. 12.0%.

> [!answer]- Answer
> **B. 9.0%.**
>
> Solving CAPM for $E(R_m)$:
>
> $$E(R_i) = R_f + \beta_i [E(R_m) - R_f]$$
>
> $$12\% = 3\% + 1.5 \times [E(R_m) - 3\%]$$
>
> $$9\% = 1.5 \times [E(R_m) - 3\%]$$
>
> $$6\% = E(R_m) - 3\%$$
>
> $$E(R_m) = 9\%$$

> [!tip]- 📖 Giải thích chi tiết
> **Bước giải ngược CAPM:**
> 1. $12\% = 3\% + 1.5 \times [E(R_m) - 3\%]$
> 2. $12\% - 3\% = 1.5 \times [E(R_m) - 3\%]$
> 3. $9\% = 1.5 \times [E(R_m) - 3\%]$
> 4. $\frac{9\%}{1.5} = E(R_m) - 3\%$
> 5. $6\% = E(R_m) - 3\%$
> 6. $E(R_m) = 9\%$
>
> **Tại sao B đúng (9.0%):** Market risk premium = 6%, $E(R_m) = 3\% + 6\% = 9\%$.
> **Tại sao A sai (6.0%):** Đây là market risk premium, không phải $E(R_m)$. Nhầm lẫn giữa premium và return.
> **Tại sao C sai (12.0%):** Đây là return của stock, không phải market. Chỉ đúng nếu $\beta = 1$.

---

## Question 29

Consider three securities with the following betas:

| Security | Beta ($\beta$) |
|----------|---------------:|
| 1        | 0.8            |
| 2        | 1.2            |
| 3        | 1.6            |

If the market risk premium is 5% and the risk-free rate is 3%, which security has the **highest expected return** according to CAPM?

- A. Security 1.
- B. Security 2.
- C. Security 3.

> [!answer]- Answer
> **C. Security 3.**
>
> | Security | $E(R_i) = R_f + \beta_i [E(R_m) - R_f]$ | Expected Return |
> |----------|------------------------------------------|-----------------|
> | 1 | $3\% + 0.8 \times 5\% = 3\% + 4\%$ | **7.0%** |
> | 2 | $3\% + 1.2 \times 5\% = 3\% + 6\%$ | **9.0%** |
> | 3 | $3\% + 1.6 \times 5\% = 3\% + 8\%$ | **11.0%** |
>
> Security 3 has the highest beta ($\beta = 1.6$) and therefore the highest expected return (11.0%).

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao C đúng:** Theo CAPM, expected return tỷ lệ thuận với β. β cao nhất → E(R) cao nhất. Security 3: β = 1.6 → E(R) = 3% + 1.6 × 5% = 11.0%.
> **Tại sao A sai:** Security 1: β = 0.8 (defensive) → E(R) = 7.0%, thấp nhất.
> **Tại sao B sai:** Security 2: β = 1.2 → E(R) = 9.0%, nằm giữa.
>
> **Key insight:** Trên SML, securities được xếp hạng theo β. β càng cao → nằm càng xa bên phải trên SML → E(R) càng cao. Nhà đầu tư chấp nhận systematic risk nhiều hơn sẽ được thưởng return cao hơn.

---

## Question 30

Using the same data from Question 29, if the market drops by 10%, which security is **most likely** to experience the **largest decline**?

- A. Security 1.
- B. Security 2.
- C. Security 3.

> [!answer]- Answer
> **C. Security 3.**
>
> Beta measures sensitivity to market movements. If the market declines by 10%:
>
> | Security | $\beta$ | Expected Decline |
> |----------|--------:|-----------------:|
> | 1 | 0.8 | $0.8 \times 10\% = 8.0\%$ |
> | 2 | 1.2 | $1.2 \times 10\% = 12.0\%$ |
> | 3 | 1.6 | $1.6 \times 10\% = 16.0\%$ |
>
> Security 3, with the **highest beta** (1.6), is expected to decline the most — approximately **16%**.

> [!tip]- 📖 Giải thích chi tiết
> **Tại sao C đúng:** β cao nhất = nhạy cảm nhất với thị trường. Khi market giảm 10%, Security 3 (β = 1.6) dự kiến giảm ~16%. Đây là "dao hai lưỡi" (double-edged sword) của high beta: gain nhiều khi market tăng, nhưng lose nhiều khi market giảm.
> **Tại sao A sai:** Security 1 (β = 0.8) chỉ giảm ~8% — defensive stock, ít biến động.
> **Tại sao B sai:** Security 2 (β = 1.2) giảm ~12%.
>
> **Tổng kết Q29–Q30:** High beta = high expected return (Q29) nhưng cũng = high downside risk (Q30). Risk–return tradeoff luôn hiện diện. Nhà đầu tư cần cân nhắc khả năng chịu đựng loss trước khi chọn high-beta securities.
