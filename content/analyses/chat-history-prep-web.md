---
title: "Chat History — CFA Prep Web Database Migration"
created: 2026-04-09
tags: [chat-history, prep-web, migration]
---

# Chat History — CFA Prep Web Database Migration

## Context
- Project: CFA Prep Web (LeaPrep)
- Neon DB: `orange-dew-36244409` (Singapore region)
- Host: `ep-floral-feather-a1dkxdqo-pooler.ap-southeast-1.aws.neon.tech`
- Database: `neondb`
- Connection: `postgresql://neondb_owner:npg_sIjxtGZhFU26@ep-floral-feather-a1dkxdqo-pooler.ap-southeast-1.aws.neon.tech/neondb?sslmode=require`

## What was done

### 1. Vietnamese explanations added (169 questions)
- SAPP practice files: 11 files, 60 questions — all have Vietnamese explanations
- CFAI practice files: 11 files, 109 questions — all have Vietnamese explanations
- Each question has 2 collapsible callouts: Answer (EN) + 📖 Giải thích chi tiết (VI)

### 2. Database architecture designed
- Saved to `analyses/database-design.md` and `analyses/database-schema.md`
- Core concept: `links` table as mini graph database for hover preview + click navigation
- 12 tables total: subjects, modules, glossary_terms, formulas, questions, question_options, explanations, concepts, links, users, user_attempts, review_schedule

### 3. Neon DB inspected — existing state
- 13 old tables with data: subjects(10), modules(116), questions(1961), answers(5868), users(3), quiz_sessions(25), quiz_answers(30), levels(3)
- Questions stored as HTML (not markdown)
- Modules not properly linked to subjects

### 4. Schema migration executed
- All 13 old tables renamed to `*_old` (archived, not deleted)
- 12 new tables created with proper schema
- Indexes created:
  - links: 3 indexes (source, target, target_id)
  - user_attempts: 3 indexes (user, question, user+date)
  - review_schedule: 1 index (user+next_review)
  - glossary_terms: GIN FTS index
  - questions: GIN FTS index

### 5. TODO — Next step
- **Write parser script** to migrate CFA-Wiki markdown files → Neon DB
- Parse: subjects, modules, glossary_terms, formulas, questions, question_options, explanations, concepts, links
- Execute parser and verify data

## New DB Schema (12 tables)

```
subjects (id, name, code, slug, level_id, display_order, description, color)
modules (id, subject_id, number, title, slug, content_md, content_html, los, summary, display_order)
glossary_terms (id, module_id, term, slug, definition_md, definition_html, formula_latex, los_ref, searchable_text)
formulas (id, module_id, name, latex, variables, description, category, display_order)
questions (id, module_id, source, source_number, question_md, question_html, correct_answer, difficulty, los_ref, tags, searchable_text)
question_options (id, question_id, label, content_md, content_html, is_correct, display_order)
explanations (id, question_id, language, content_md, content_html, why_correct, why_a, why_b, why_c)
concepts (id, title, slug, content_md, content_html, related_module_ids, tags)
links (id, source_type, source_id, target_type, target_id, target_slug, link_text, context)
users (id, email, display_name, avatar_url)
user_attempts (id, user_id, question_id, selected_answer, is_correct, time_spent_seconds, attempted_at)
review_schedule (id, user_id, question_id, next_review, interval_days, ease_factor, repetitions, last_reviewed)
```

## Wiki source files
- `/Users/sophie/Desktop/CFA-Wiki/` — root
- `glossary/` — 11 glossary files (m01-m11)
- `formulas/` — 11 formula files
- `modules/` — 11 module content files
- `practice/` — 11 SAPP practice files
- `practice/cfai/` — 11 CFAI practice files
- `concepts/` — concept pages
