---
type: practice
tags:
  - cfai-official
  - quantitative-methods
  - portfolio-math
  - covariance
source: "CFAI CFA1 Quant Practice 2026, pp.172-173"
module: "[[m05-portfolio-math]]"
---

# M05 – Portfolio Mathematics: CFAI Practice Problems

**Source:** CFAI CFA1 Quant Practice 2026, pp.172–173
**Back to module:** [[m05-portfolio-math]]
**Glossary**: [[quantitative-methods/glossary/m05-portfolio-math|M05 Terms]]

---

## Question 1

The joint probability function of returns for a foreign index (FI) and a domestic index (DI) is given below:

| Scenario | Probability | $R_{FI}$ | $R_{DI}$ |
|----------|-------------|----------|----------|
| 1 | 0.25 | 25% | 30% |
| 2 | 0.50 | 15% | 25% |
| 3 | 0.25 | 10% | 15% |

The **[[quantitative-methods/glossary/m05-portfolio-math#Covariance Matrix|covariance]]** between $R_{FI}$ and $R_{DI}$ is **closest to**:

- A. 26.39
- B. 26.56
- C. 28.12

> [!answer]- Answer
> **B. 26.56**
>
> **Step 1 – [[quantitative-methods/glossary/m05-portfolio-math#Portfolio Expected Return|Expected returns]]:**
>
> $$E(R_{FI}) = 0.25(25\%) + 0.50(15\%) + 0.25(10\%)$$
> $$E(R_{FI}) = 6.25 + 7.50 + 2.50 = 16.25\%$$
>
> $$E(R_{DI}) = 0.25(30\%) + 0.50(25\%) + 0.25(15\%)$$
> $$E(R_{DI}) = 7.50 + 12.50 + 3.75 = 23.75\%$$
>
> **Step 2 – Covariance calculation:**
>
> $$\text{Cov}(R_{FI}, R_{DI}) = \sum_{i} P_i \cdot [R_{FI,i} - E(R_{FI})] \cdot [R_{DI,i} - E(R_{DI})]$$
>
> | Scenario | $P_i$ | $R_{FI,i} - \bar{R}_{FI}$ | $R_{DI,i} - \bar{R}_{DI}$ | Product | $P_i \times$ Product |
> |----------|--------|---------------------------|---------------------------|---------|----------------------|
> | 1 | 0.25 | 25 − 16.25 = **+8.75** | 30 − 23.75 = **+6.25** | 54.6875 | **13.672** |
> | 2 | 0.50 | 15 − 16.25 = **−1.25** | 25 − 23.75 = **+1.25** | −1.5625 | **−0.781** |
> | 3 | 0.25 | 10 − 16.25 = **−6.25** | 15 − 23.75 = **−8.75** | 54.6875 | **13.672** |
>
> $$\text{Cov}(R_{FI}, R_{DI}) = 13.672 + (-0.781) + 13.672 = \mathbf{26.56}$$
>
> **Interpretation:** The positive covariance of 26.56 indicates that the foreign and domestic indices tend to move in the **same direction** — when one index has an above-average return, the other tends to as well. This positive co-movement limits the [[quantitative-methods/glossary/m05-portfolio-math#Diversification Benefit|diversification benefit]] of combining these two assets.
>
> **Note on units:** Covariance is expressed in units of (%)², so the covariance is 26.56 (%²). To interpret the strength of the relationship in scale-free terms, compute the correlation coefficient:
>
> $$\sigma_{FI} = \sqrt{\sum P_i(R_{FI,i} - \bar{R}_{FI})^2} = \sqrt{0.25(8.75)^2 + 0.50(-1.25)^2 + 0.25(-6.25)^2}$$
> $$= \sqrt{19.141 + 0.781 + 9.766} = \sqrt{29.688} \approx 5.449\%$$
>
> $$\sigma_{DI} = \sqrt{0.25(6.25)^2 + 0.50(1.25)^2 + 0.25(-8.75)^2}$$
> $$= \sqrt{9.766 + 0.781 + 19.141} = \sqrt{29.688} \approx 5.449\%$$
>
> $$\rho_{FI,DI} = \frac{26.56}{5.449 \times 5.449} = \frac{26.56}{29.69} \approx 0.895$$
>
> The high positive correlation (~0.90) confirms strong co-movement between the two indices.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m05-portfolio-math#Covariance Matrix|Covariance]] từ joint probability function được tính theo công thức: Cov(X,Y) = Σ Pᵢ × (Xᵢ − E(X)) × (Yᵢ − E(Y)). Quy trình gồm hai bước: tính expected return của từng tài sản trước, rồi mới tính covariance. Covariance dương cho biết hai tài sản có xu hướng cùng chiều, làm giảm [[quantitative-methods/glossary/m05-portfolio-math#Diversification Benefit|diversification benefit]].
>
> **Tại sao B (26.56) đúng:** E(R_FI) = 16.25%, E(R_DI) = 23.75%. Cov = 0.25×(8.75)(6.25) + 0.50×(−1.25)(1.25) + 0.25×(−6.25)(−8.75) = 13.672 − 0.781 + 13.672 = **26.56**. Correlation ≈ 0.895 — co-movement rất cao giữa hai index.
> **Tại sao A (26.39) sai:** Kết quả này xuất hiện nếu làm tròn sai trong quá trình tính deviation — ví dụ làm tròn E(R_FI) thành 16% hoặc E(R_DI) thành 24% trước khi tính, dẫn đến sai số tích lũy.
> **Tại sao C (28.12) sai:** Có thể do dùng sai trọng số (ví dụ gán P = 1/3 đều nhau cho mỗi scenario thay vì 0.25/0.50/0.25), hoặc quên nhân với Pᵢ ở một trong các term.
