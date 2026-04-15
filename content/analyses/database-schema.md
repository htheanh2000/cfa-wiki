---
title: "CFA Prep Web — Database Schema"
type: analysis
created: 2026-04-09
updated: 2026-04-09
tags: [database, schema, prep-web]
---

# CFA Prep Web — Database Schema

## Tổng quan: 12 bảng

```
subjects ──< modules ──< glossary_terms
                    ├──< formulas
                    ├──< questions ──< question_options
                    │               ├──< explanations
                    │               └──< user_attempts
                    └──< concepts

links (đồ thị liên kết giữa mọi entity)
users
review_schedule (spaced repetition)
```

---

## 1. subjects

Bảng gốc — 10 môn CFA Level 1.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | TEXT | PK | `quantitative-methods` |
| name | TEXT | NOT NULL | `Quantitative Methods` |
| name_vi | TEXT | | `Các phương pháp định lượng` |
| order_num | INTEGER | NOT NULL, UNIQUE | `1` (thứ tự trong curriculum) |
| total_modules | INTEGER | DEFAULT 0 | `11` |
| status | TEXT | DEFAULT 'not_started' | `not_started`, `in_progress`, `completed` |
| icon | TEXT | | `📊` |

**Ví dụ dữ liệu:**

| id | name | order_num | total_modules |
|----|------|-----------|---------------|
| quantitative-methods | Quantitative Methods | 1 | 11 |
| economics | Economics | 2 | 0 |
| financial-statement-analysis | Financial Statement Analysis | 3 | 0 |

---

## 2. modules

11 modules mỗi subject. Chứa nội dung bài học chính.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | TEXT | PK | `quant-m01` |
| subject_id | TEXT | FK → subjects.id | `quantitative-methods` |
| number | INTEGER | NOT NULL | `1` |
| title | TEXT | NOT NULL | `Rates and Returns` |
| slug | TEXT | UNIQUE | `m01-rates-and-returns` |
| content_md | TEXT | | Nội dung markdown gốc |
| content_html | TEXT | | HTML đã render (KaTeX, links) |
| los | TEXT | | JSON: `["1.a","1.b","1.c","1.d","1.e"]` |
| page_start | INTEGER | | `3` (trang bắt đầu trong PDF) |
| page_end | INTEGER | | `32` |

---

## 3. glossary_terms ⭐

Từ điển CFA — 254 thuật ngữ. Đây là bảng quan trọng nhất cho hover/click.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | TEXT | PK | `quant-m01-inflation-premium` |
| module_id | TEXT | FK → modules.id | `quant-m01` |
| term | TEXT | NOT NULL | `Inflation Premium` |
| slug | TEXT | UNIQUE | `inflation-premium` |
| definition | TEXT | NOT NULL | Định nghĩa ngắn (1-3 câu) |
| definition_html | TEXT | | HTML đã render |
| formula_latex | TEXT | NULL | `r_f = r_{real} + IP` |
| formula_variables | TEXT | NULL | JSON: `[{"sym":"r_f","desc":"Nominal risk-free rate"},...]` |
| los_ref | TEXT | | `1.a` |
| note | TEXT | NULL | Ghi chú thêm |
| related_term_ids | TEXT | NULL | JSON: `["quant-m01-real-risk-free-rate","quant-m01-nominal-risk-free-rate"]` |

**Ví dụ dữ liệu:**

| id | term | definition | formula_latex |
|----|------|-----------|---------------|
| quant-m01-inflation-premium | Inflation Premium | Phần bù lạm phát — bù đắp cho mất sức mua do lạm phát | `r_f = r_{real} + IP` |
| quant-m01-hpr | Holding Period Return (HPR) | Lợi suất trong một kỳ nắm giữ | `HPR = \frac{P_1 - P_0 + I_1}{P_0}` |
| quant-m08-type-i-error | Type I Error | Bác bỏ giả thuyết null đúng (false positive) | NULL |

---

## 4. formulas

Công thức tách riêng — dễ filter, search, render.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | TEXT | PK | `quant-m01-hpr` |
| module_id | TEXT | FK → modules.id | `quant-m01` |
| name | TEXT | NOT NULL | `Holding Period Return` |
| slug | TEXT | UNIQUE | `hpr` |
| latex | TEXT | NOT NULL | `HPR = \frac{P_1 - P_0 + I_1}{P_0}` |
| variables | TEXT | | JSON: `[{"sym":"P_0","desc":"Beginning price"},{"sym":"P_1","desc":"Ending price"},{"sym":"I_1","desc":"Income"}]` |
| description | TEXT | | `Lợi suất nắm giữ trong một kỳ` |
| category | TEXT | | `return-measures` |
| los_ref | TEXT | | `1.b` |

---

## 5. questions

169 câu hỏi. Tách question text ra khỏi options và explanations.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | TEXT | PK | `cfai-m01-q03` |
| module_id | TEXT | FK → modules.id | `quant-m01` |
| source | TEXT | NOT NULL | `cfai` hoặc `sapp` |
| number | INTEGER | NOT NULL | `3` |
| topic | TEXT | NULL | `Return Measures` |
| question_md | TEXT | NOT NULL | Nội dung câu hỏi (markdown) |
| question_html | TEXT | | HTML đã render |
| exhibit_md | TEXT | NULL | Bảng/exhibit đi kèm (nếu có) |
| exhibit_html | TEXT | NULL | |
| correct_answer | TEXT | NOT NULL | `A`, `B`, hoặc `C` |
| difficulty | TEXT | DEFAULT 'medium' | `easy`, `medium`, `hard` |
| los_ref | TEXT | NULL | `1.b` |
| tags | TEXT | NULL | JSON: `["geometric-mean","return-measures"]` |

---

## 6. question_options

3 đáp án cho mỗi câu hỏi.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | INTEGER | PK, AUTO | |
| question_id | TEXT | FK → questions.id | `cfai-m01-q03` |
| label | TEXT | NOT NULL | `A`, `B`, `C` |
| text_md | TEXT | NOT NULL | `14.9 percent` |
| text_html | TEXT | | |
| is_correct | BOOLEAN | DEFAULT FALSE | `TRUE` cho đáp án đúng |

---

## 7. explanations

Giải thích song ngữ — mỗi câu có 2 rows (en + vi).

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | INTEGER | PK, AUTO | |
| question_id | TEXT | FK → questions.id | `cfai-m01-q03` |
| lang | TEXT | NOT NULL | `en` hoặc `vi` |
| content_md | TEXT | NOT NULL | Nội dung giải thích |
| content_html | TEXT | | HTML đã render |
| why_correct | TEXT | NULL | Tại sao đáp án đúng (tách riêng) |
| why_a_wrong | TEXT | NULL | Tại sao A sai (nếu A không phải đáp án đúng) |
| why_b_wrong | TEXT | NULL | Tại sao B sai |
| why_c_wrong | TEXT | NULL | Tại sao C sai |

---

## 8. concepts

11 concept pages — giải thích sâu hơn glossary.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | TEXT | PK | `probability` |
| title | TEXT | NOT NULL | `Probability` |
| slug | TEXT | UNIQUE | `probability` |
| content_md | TEXT | | Nội dung đầy đủ |
| content_html | TEXT | | |
| related_module_ids | TEXT | | JSON: `["quant-m04"]` |
| tags | TEXT | | JSON: `["probability","bayes","counting"]` |

---

## 9. links ⭐⭐

Bảng đồ thị — LƯU MỌI LIÊN KẾT giữa mọi entity. Đây là bảng quan trọng nhất cho hover preview và click navigation.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | INTEGER | PK, AUTO | |
| source_type | TEXT | NOT NULL | `question`, `glossary`, `module`, `concept`, `formula`, `explanation` |
| source_id | TEXT | NOT NULL | `cfai-m01-q04` |
| target_type | TEXT | NOT NULL | `glossary`, `module`, `concept`, `formula` |
| target_id | TEXT | NOT NULL | `quant-m01-inflation-premium` |
| anchor_text | TEXT | NULL | `inflation premium` (text hiển thị) |
| context | TEXT | NULL | `question_text`, `option_a`, `explanation_vi`, `definition` |

**Indexes:**
```sql
CREATE INDEX idx_links_source ON links(source_type, source_id);
CREATE INDEX idx_links_target ON links(target_type, target_id);
CREATE INDEX idx_links_target_id ON links(target_id);
```

**Ví dụ dữ liệu:**

| source_type | source_id | target_type | target_id | anchor_text | context |
|-------------|-----------|-------------|-----------|-------------|---------|
| question | sapp-m01-q04 | glossary | quant-m01-gross-return | gross return | question_text |
| question | sapp-m01-q04 | glossary | quant-m01-net-return | net return | question_text |
| glossary | quant-m01-inflation-premium | glossary | quant-m01-nominal-risk-free-rate | nominal risk-free rate | definition |
| glossary | quant-m01-inflation-premium | module | quant-m01 | M01 | definition |
| module | quant-m01 | formula | quant-m01-hpr | HPR | content |
| concept | interest-rates | module | quant-m01 | M01 | content |

**Cách query:**

```sql
-- Hover preview: lấy định nghĩa term
SELECT term, definition, formula_latex, los_ref
FROM glossary_terms WHERE id = 'quant-m01-inflation-premium';

-- Click: lấy tất cả backlinks (ai nhắc đến term này?)
SELECT source_type, source_id, anchor_text, context
FROM links WHERE target_id = 'quant-m01-inflation-premium';
-- → Trả về: Q1 (SAPP), Q1 (CFAI), Module M01, Concept interest-rates

-- Graph view: lấy tất cả connections của 1 entity
SELECT * FROM links 
WHERE source_id = 'quant-m01-inflation-premium' 
   OR target_id = 'quant-m01-inflation-premium';

-- Tìm related terms (cùng module, cùng LOS)
SELECT * FROM glossary_terms 
WHERE module_id = 'quant-m01' AND los_ref = '1.a';
```

---

## 10. users

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | TEXT | PK | UUID hoặc `default` |
| name | TEXT | | `Sophie` |
| email | TEXT | UNIQUE, NULL | |
| created_at | DATETIME | DEFAULT NOW | |
| settings | TEXT | NULL | JSON: `{"lang":"vi","theme":"dark"}` |

---

## 11. user_attempts

Lưu lịch sử trả lời.

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | INTEGER | PK, AUTO | |
| user_id | TEXT | FK → users.id | `default` |
| question_id | TEXT | FK → questions.id | `cfai-m01-q03` |
| selected | TEXT | NOT NULL | `A`, `B`, hoặc `C` |
| is_correct | BOOLEAN | NOT NULL | `TRUE` |
| time_spent | INTEGER | NULL | Giây (seconds) |
| attempted_at | DATETIME | DEFAULT NOW | |

---

## 12. review_schedule

Spaced Repetition (SM-2 algorithm).

| Column | Type | Constraint | Mô tả |
|--------|------|-----------|--------|
| id | INTEGER | PK, AUTO | |
| user_id | TEXT | FK → users.id | |
| question_id | TEXT | FK → questions.id | |
| next_review | DATETIME | NOT NULL | Thời điểm ôn lại |
| interval_days | REAL | DEFAULT 1.0 | Khoảng cách giữa các lần ôn (ngày) |
| ease_factor | REAL | DEFAULT 2.5 | Hệ số dễ/khó (SM-2) |
| repetitions | INTEGER | DEFAULT 0 | Số lần đã ôn đúng liên tiếp |
| last_quality | INTEGER | NULL | 0-5 (chất lượng trả lời lần cuối) |

---

## Tổng kết

| Bảng | Số rows ước tính | Vai trò |
|------|-----------------|---------|
| subjects | 10 | 10 môn CFA L1 |
| modules | 11+ | Nội dung bài học |
| glossary_terms | 254 | Từ điển — hover preview |
| formulas | 66+ | Công thức — render KaTeX |
| questions | 169 | Câu hỏi practice |
| question_options | 507 (169×3) | 3 đáp án mỗi câu |
| explanations | 338 (169×2) | Giải thích EN + VI |
| concepts | 11 | Khái niệm tổng hợp |
| **links** | **~1500+** | **Đồ thị liên kết — core của hover/click** |
| users | 1+ | Người dùng |
| user_attempts | 0→∞ | Lịch sử trả lời |
| review_schedule | 0→169 | Lịch ôn spaced repetition |
