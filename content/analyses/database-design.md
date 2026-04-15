---
title: "CFA Prep Web — Database Design"
type: analysis
created: 2026-04-09
updated: 2026-04-09
tags: [architecture, database, prep-web]
---

# CFA Prep Web — Database Design

## Core Requirement

Mọi thuật ngữ, concept, formula đều có thể **hover preview** và **click navigate** — giống Obsidian wikilinks nhưng trên web.

## Entity-Relationship Diagram

```
┌──────────┐     ┌──────────┐     ┌──────────────┐
│ subjects │────<│ modules  │────<│ module_los   │
└──────────┘     └────┬─────┘     └──────────────┘
                      │
          ┌───────────┼───────────────┐
          │           │               │
    ┌─────┴────┐ ┌────┴─────┐  ┌─────┴──────┐
    │ glossary │ │ formulas │  │ questions  │
    │ _terms   │ │          │  │            │
    └────┬─────┘ └──────────┘  └─────┬──────┘
         │                           │
    ┌────┴─────┐              ┌──────┴──────┐
    │  links   │              │  question   │
    │ (edges)  │              │  _options   │
    └──────────┘              └──────┬──────┘
                                     │
                              ┌──────┴──────┐
                              │explanations │
                              │ (en + vi)   │
                              └─────────────┘

    ┌──────────┐     ┌───────────────┐
    │ concepts │     │ user_progress │
    └──────────┘     └───────────────┘
```

## Tables

### 1. subjects
```sql
CREATE TABLE subjects (
  id          TEXT PRIMARY KEY,  -- 'quantitative-methods'
  name        TEXT NOT NULL,     -- 'Quantitative Methods'
  order_num   INTEGER NOT NULL,  -- 1
  status      TEXT DEFAULT 'not_started'  -- 'in_progress', 'completed'
);
```

### 2. modules
```sql
CREATE TABLE modules (
  id          TEXT PRIMARY KEY,  -- 'quant-m01'
  subject_id  TEXT REFERENCES subjects(id),
  number      INTEGER NOT NULL,  -- 1
  title       TEXT NOT NULL,     -- 'Rates and Returns'
  slug        TEXT UNIQUE,       -- 'm01-rates-and-returns'
  content_md  TEXT,              -- raw markdown
  content_html TEXT,             -- rendered HTML with links
  los_json    TEXT               -- ["1.a", "1.b", "1.c", "1.d", "1.e"]
);
```

### 3. glossary_terms ⭐ (core of linking)
```sql
CREATE TABLE glossary_terms (
  id          TEXT PRIMARY KEY,  -- 'quant-m01-inflation-premium'
  module_id   TEXT REFERENCES modules(id),
  term        TEXT NOT NULL,     -- 'Inflation Premium'
  slug        TEXT UNIQUE,       -- 'inflation-premium'
  definition  TEXT NOT NULL,     -- 'The compensation investors require...'
  definition_html TEXT,          -- rendered with internal links
  formula     TEXT,              -- '$$r_f = r_{real} + IP$$'
  los_ref     TEXT,              -- '1.a'
  related     TEXT               -- JSON array of related term IDs
);
```

### 4. links ⭐ (the graph — enables hover + click)
```sql
CREATE TABLE links (
  id          INTEGER PRIMARY KEY AUTOINCREMENT,
  source_type TEXT NOT NULL,     -- 'question', 'glossary', 'module', 'concept'
  source_id   TEXT NOT NULL,     -- 'cfai-m01-q02'
  target_type TEXT NOT NULL,     -- 'glossary'
  target_id   TEXT NOT NULL,     -- 'quant-m01-inflation-premium'
  anchor_text TEXT,              -- 'inflation premium' (display text)
  context     TEXT               -- 'option_a', 'question_text', 'explanation'
);

-- Index for fast hover/click lookup
CREATE INDEX idx_links_target ON links(target_type, target_id);
CREATE INDEX idx_links_source ON links(source_type, source_id);
```

### 5. formulas
```sql
CREATE TABLE formulas (
  id          TEXT PRIMARY KEY,  -- 'quant-m01-hpr'
  module_id   TEXT REFERENCES modules(id),
  name        TEXT NOT NULL,     -- 'Holding Period Return'
  slug        TEXT UNIQUE,
  latex       TEXT NOT NULL,     -- 'HPR = \\frac{P_1 - P_0 + I_1}{P_0}'
  variables   TEXT,              -- JSON: [{"sym":"P_0","desc":"Beginning price"}, ...]
  category    TEXT               -- 'return-measures'
);
```

### 6. questions
```sql
CREATE TABLE questions (
  id          TEXT PRIMARY KEY,  -- 'cfai-m01-q01'
  module_id   TEXT REFERENCES modules(id),
  source      TEXT NOT NULL,     -- 'cfai' or 'sapp'
  number      INTEGER,
  question_md TEXT NOT NULL,
  question_html TEXT,
  exhibit_md  TEXT,              -- shared exhibit/table if any
  exhibit_html TEXT,
  difficulty  TEXT,              -- 'easy', 'medium', 'hard'
  los_ref     TEXT               -- '1.a'
);
```

### 7. question_options
```sql
CREATE TABLE question_options (
  id          INTEGER PRIMARY KEY AUTOINCREMENT,
  question_id TEXT REFERENCES questions(id),
  label       TEXT NOT NULL,     -- 'A', 'B', 'C'
  text_md     TEXT NOT NULL,
  text_html   TEXT,
  is_correct  BOOLEAN DEFAULT FALSE
);
```

### 8. explanations (bilingual)
```sql
CREATE TABLE explanations (
  id          INTEGER PRIMARY KEY AUTOINCREMENT,
  question_id TEXT REFERENCES questions(id),
  lang        TEXT NOT NULL,     -- 'en' or 'vi'
  content_md  TEXT NOT NULL,
  content_html TEXT
);
```

### 9. concepts
```sql
CREATE TABLE concepts (
  id          TEXT PRIMARY KEY,
  title       TEXT NOT NULL,
  slug        TEXT UNIQUE,
  content_md  TEXT,
  content_html TEXT
);
```

### 10. user_progress
```sql
CREATE TABLE user_progress (
  id          INTEGER PRIMARY KEY AUTOINCREMENT,
  user_id     TEXT DEFAULT 'default',
  question_id TEXT REFERENCES questions(id),
  selected    TEXT,              -- 'A', 'B', or 'C'
  is_correct  BOOLEAN,
  time_spent  INTEGER,          -- seconds
  attempted_at DATETIME DEFAULT CURRENT_TIMESTAMP
);
```

### 11. review_schedule (Spaced Repetition)
```sql
CREATE TABLE review_schedule (
  id          INTEGER PRIMARY KEY AUTOINCREMENT,
  user_id     TEXT DEFAULT 'default',
  question_id TEXT REFERENCES questions(id),
  next_review DATETIME,
  interval    REAL DEFAULT 1.0,  -- days
  ease_factor REAL DEFAULT 2.5,
  reps        INTEGER DEFAULT 0
);
```

## How Linking Works (Hover + Click)

### Step 1: Parse markdown wikilinks → links table

```
[[glossary/m01-rates-and-returns#Inflation Premium|inflation premium]]
                ↓ parser extracts ↓
links table: {
  source_type: 'question',
  source_id:   'sapp-m01-q04',
  target_type: 'glossary',
  target_id:   'quant-m01-inflation-premium',
  anchor_text: 'inflation premium'
}
```

### Step 2: Render as interactive HTML

```html
<span 
  class="wiki-link"
  data-target-type="glossary" 
  data-target-id="quant-m01-inflation-premium"
  @mouseenter="showPreview"
  @click="navigate"
>
  inflation premium
</span>
```

### Step 3: Hover → API call → preview popup

```
GET /api/preview?type=glossary&id=quant-m01-inflation-premium
→ Returns: { term, definition_html, formula, los_ref, related }
→ Render as floating card (like Obsidian hover preview)
```

### Step 4: Click → navigate to full page

```
/glossary/inflation-premium → full glossary entry page
/modules/m01-rates-and-returns → full module page
/formulas/rates-and-returns#hpr → formula with context
```

## API Endpoints

```
GET /api/modules                    → list all modules
GET /api/modules/:slug              → module content + links
GET /api/glossary?module=m01        → terms for module
GET /api/glossary/:slug             → single term + related
GET /api/preview?type=X&id=Y        → hover preview data
GET /api/questions?module=m01&source=cfai  → filtered questions
GET /api/questions/:id              → single question + options + explanations
POST /api/progress                  → save answer attempt
GET /api/progress/stats             → accuracy per module
GET /api/review/due                 → spaced repetition queue
POST /api/review/answer             → update SM-2 schedule
GET /api/search?q=inflation         → full-text search across all content
GET /api/graph                      → all links for graph visualization
```

## Key Design Decisions

| Decision | Choice | Reason |
|----------|--------|--------|
| Database | SQLite (Drizzle ORM) | Portable, no server needed, fast reads |
| Linking | Separate `links` table | Enables bidirectional traversal, graph view, hover preview |
| Content | Store both MD + HTML | MD for editing, HTML for fast rendering |
| Bilingual | Separate `explanations` rows per lang | Clean toggle EN/VI without duplication |
| IDs | Slugs (human-readable) | Easy debugging, URL-friendly |
| Search | SQLite FTS5 | Full-text search without external service |

## Graph View (Optional)

The `links` table enables a graph visualization similar to Obsidian:

```sql
-- Get all connections for a term
SELECT l.source_type, l.source_id, l.target_type, l.target_id
FROM links l
WHERE l.target_id = 'quant-m01-inflation-premium'
   OR l.source_id = 'quant-m01-inflation-premium';

-- This returns all questions, modules, and other terms 
-- that reference "Inflation Premium"
```

Render with D3.js force-directed graph or vis-network.
