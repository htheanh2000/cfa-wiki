---
title: "Practice: M06 — Simulation Methods"
type: practice
subject: quantitative-methods
module: M06
created: 2026-04-09
updated: 2026-04-09
tags: [practice, simulation, lognormal, bootstrap, monte-carlo]
---

# Practice: M06 — Simulation Methods

**Module**: [[quantitative-methods/modules/m06-simulation-methods/index|M06]]
**Glossary**: [[quantitative-methods/glossary/m06-simulation-methods|M06 Terms]]

---

**Question 1**: The goal of resampling and the use of subsamples is to estimate parameters for the:

A. Various subsamples
B. Overall population
C. Original sample

> [!answer]- Answer
> **B.** Resampling uses subsamples drawn from the original sample to make statistical inferences about the **overall population** parameters.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Resampling là nhóm kỹ thuật thống kê rút các mẫu con từ dữ liệu gốc để ước tính tham số của tổng thể (population). Mục tiêu cuối cùng luôn là suy luận về **tổng thể**, không phải về mẫu con hay mẫu gốc.
>
> **Tại sao B đúng:** Các mẫu con (subsamples) chỉ là phương tiện để tạo ra nhiều ước tính của cùng một tham số, từ đó hiểu được phân phối của ước tính đó và suy luận về tổng thể.
>
> **Tại sao A sai:** Mục tiêu không phải ước tính tham số **của từng mẫu con** — mẫu con là công cụ, không phải mục tiêu.
>
> **Tại sao C sai:** Ước tính tham số của mẫu gốc (original sample) đã có trực tiếp từ mẫu đó mà không cần resampling — không cần kỹ thuật này.

---

**Question 2**: Analysts performing [[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|bootstrap]]:

A. Seek to create statistical inferences of population parameters from a single sample
B. Repeatedly draw samples of the same size, with replacement, from the original population
C. Must specify probability distributions for key risk factors that drive the underlying random variables

> [!answer]- Answer
> **A.** Bootstrap draws samples **with replacement from the original sample** (not the population) to create statistical inferences about population parameters. B is wrong because it says "from the population" — bootstrap draws from the **sample**. C describes [[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]], not bootstrap.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m06-simulation-methods#Bootstrap|Bootstrap]] là phương pháp resampling rút mẫu **có hoàn lại** (with replacement) từ **mẫu gốc** nhiều lần để ước tính phân phối của thống kê cần quan tâm. "With replacement" nghĩa là mỗi quan sát có thể được chọn nhiều lần trong cùng một mẫu con.
>
> **Tại sao A đúng:** Bootstrap đúng là mục tiêu suy luận về tham số tổng thể, xuất phát từ **một mẫu duy nhất**. Đây là ưu điểm: không cần thu thập thêm dữ liệu.
>
> **Tại sao B sai:** Bootstrap **không** rút mẫu từ tổng thể (population) — điều đó là lý tưởng nhưng thường không khả thi. Chính điểm khác biệt "từ mẫu gốc, không phải tổng thể" là bản chất của bootstrap.
>
> **Tại sao C sai:** Việc xác định trước phân phối xác suất cho các biến rủi ro là đặc trưng của [[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]], không phải bootstrap. Bootstrap không giả định phân phối — đây là lợi thế lớn (non-parametric).

---

**Question 3**: The [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|lognormal distribution]]:

A. Is unbounded
B. Is asymmetrical
C. Has the same mean as its associated normal distribution

> [!answer]- Answer
> **B.** The lognormal distribution is asymmetrical (positively skewed). It is **not** unbounded — it is bounded below by zero. It does **not** have the same mean as its associated normal distribution.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m06-simulation-methods#Lognormal Distribution|Lognormal distribution]] là phân phối của một biến mà **logarithm** của nó có phân phối chuẩn. Nếu $\ln(X) \sim N(\mu, \sigma^2)$ thì $X$ có phân phối lognormal.
>
> **Tại sao B đúng:** Lognormal bị giới hạn dưới bằng 0 (không thể âm) và có đuôi dài về phía phải → **lệch phải** (positively skewed / asymmetrical). Đây là lý do lognormal phù hợp để mô phỏng giá cổ phiếu.
>
> **Tại sao A sai:** Lognormal **không** unbounded — bị giới hạn $X > 0$. Chính phân phối chuẩn mới unbounded ($-\infty$ đến $+\infty$).
>
> **Tại sao C sai:** Mean của lognormal $= e^{\mu + \sigma^2/2}$, khác với $\mu$ (mean của phân phối chuẩn liên quan). Chỉ có $\mu$ và $\sigma^2$ là tham số của phân phối chuẩn, còn mean thực của lognormal luôn lớn hơn $e^\mu$.

---

**Question 4**: A lognormal distribution is **least likely** to be:

A. Bounded below by zero
B. Used to model stock prices
C. Negatively skewed

> [!answer]- Answer
> **C.** The lognormal distribution is always **positively** skewed (right tail). It IS bounded below by zero (A is true) and IS used to model stock prices (B is true) since prices cannot be negative.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> Câu hỏi dạng "least likely" yêu cầu xác định phát biểu **sai** về lognormal distribution. Cần nhớ 3 đặc tính cốt lõi: (1) bounded below by zero, (2) positively skewed, (3) dùng mô phỏng giá tài sản.
>
> **Tại sao C đúng (là đáp án "least likely"):** Lognormal **không bao giờ** negatively skewed — luôn lệch phải vì bị giới hạn dưới bằng 0 và đuôi phải dài vô hạn.
>
> **Tại sao A không phải đáp án:** "Bounded below by zero" là đặc tính **đúng** của lognormal → không phải điều "least likely".
>
> **Tại sao B không phải đáp án:** Lognormal được dùng rộng rãi để mô phỏng giá cổ phiếu (và nhiều tài sản khác) vì giá không thể âm — đây là ứng dụng **đúng** và phổ biến.

---

**Question 5**: A stock was purchased for $30 and sold one year later for $34.50. Calculate:
- (a) Holding period return
- (b) [[quantitative-methods/glossary/m06-simulation-methods#Continuously Compounded Return|Continuously compounded return]]

> [!answer]- Answer
> (a) $HPR = \frac{34.50}{30} - 1 = 15\%$
> (b) $r_{cc} = \ln(1 + 0.15) = \ln(1.15) = 13.98\%$
> Note: Continuously compounded return is always less than HPR for positive returns.

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> HPR (Holding Period Return) là lợi nhuận tổng thể của khoảng đầu tư. [[quantitative-methods/glossary/m06-simulation-methods#Continuously Compounded Return|Continuously compounded return]] là lãi suất ghép liên tục tương đương với HPR, tính bằng $r_{cc} = \ln(1 + HPR)$.
>
> **Tại sao đáp án đúng:**
> - HPR: $(34.50 - 30) / 30 = 4.50/30 = 15\%$ — đây là lợi nhuận thực tế trong kỳ.
> - $r_{cc} = \ln(1.15) = 13.98\%$ — đây là mức lãi suất ghép liên tục tạo ra cùng kết quả. Kiểm chứng: $30 \times e^{0.1398} = 30 \times 1.15 = \$34.50$ ✓
>
> **Tại sao $r_{cc} < HPR$:** Ghép lãi liên tục là cơ chế mạnh nhất (lãi được tái đầu tư tức thì), nên cần lãi suất **thấp hơn** để đạt cùng kết quả. Mối quan hệ: $r_{cc} = \ln(1 + HPR) < HPR$ luôn đúng khi HPR > 0.
>
> **Ứng dụng:** Continuously compounded return có tính chất cộng được qua thời gian ($r_{cc,total} = \sum r_{cc,t}$) — rất tiện cho phân tích chuỗi thời gian dài.

---

**Question 6**: Which of the following is a limitation of [[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]]?

A. It cannot value complex securities
B. It cannot provide insights that analytic methods can
C. It does not require assumptions about probability distributions

> [!answer]- Answer
> **B.** Monte Carlo simulation is fairly complex and **cannot provide analytical insights** — it only generates numerical results. It CAN value complex securities (A is wrong). It DOES require distribution assumptions (C is wrong).

> [!tip]- 📖 Giải thích chi tiết
> **Ôn lại khái niệm:**
> [[quantitative-methods/glossary/m06-simulation-methods#Monte Carlo Simulation|Monte Carlo simulation]] tạo ra hàng nghìn kịch bản ngẫu nhiên dựa trên các phân phối xác suất giả định để ước tính kết quả có thể xảy ra. Phương pháp mạnh nhưng có giới hạn quan trọng.
>
> **Tại sao B đúng:** Monte Carlo chỉ cho kết quả số (numerical results) — nó không giải thích **tại sao** kết quả như vậy hay cung cấp hiểu biết phân tích sâu hơn. Các phương pháp phân tích (analytical methods) như Black-Scholes có thể cung cấp insights toán học mà Monte Carlo không làm được.
>
> **Tại sao A sai:** Monte Carlo **có thể** định giá các chứng khoán phức tạp (options có nhiều path dependency, CDO, MBS...) — đây thực ra là một trong những **ưu điểm** lớn nhất của nó.
>
> **Tại sao C sai:** Monte Carlo **cần** giả định phân phối xác suất cho các biến đầu vào (ví dụ: lợi nhuận cổ phiếu theo phân phối chuẩn). Đây là một **hạn chế** vì kết quả nhạy cảm với giả định phân phối — nếu phân phối sai thì kết quả sai.
