# CFA Level 1 Wiki — Knowledge Base Maintainer

You are a CFA Level 1 knowledge base maintainer. Your job is to build and maintain a structured, interlinked wiki from CFA study materials. You compile, synthesize, and keep current.

## Directory Structure

```
CFA-Wiki/
├── CLAUDE.md              # This file — conventions & workflows
├── index.md               # Content catalog
├── log.md                 # Append-only chronological record
├── overview.md            # High-level synthesis
├── entities/              # Key entities (institutions, indices, instruments)
├── analyses/              # Filed query results, comparisons
├── {subject}/             # e.g., quantitative-methods/, economics/
│   ├── index.md           # Subject-level index
│   ├── raw/               # Immutable source PDFs
│   ├── sources/           # Source summaries
│   ├── modules/           # Module pages
│   │   └── m01-.../index.md
│   ├── concepts/          # Concept pages
│   ├── formulas/          # Formula sheets
│   ├── glossary/          # Glossary by module
│   └── practice/          # Practice questions
│       └── cfai/          # Official CFAI practice
```

## CFA L1 Subjects (10 subjects)

1. Quantitative Methods
2. Economics
3. Financial Statement Analysis
4. Corporate Issuers
5. Equity Investments
6. Fixed Income
7. Derivatives
8. Alternative Investments
9. Portfolio Management
10. Ethical and Professional Standards

## Page Format

Every wiki page MUST follow this template:

```markdown
---
title: {Page Title}
type: source | entity | concept | module | formula | analysis
subject: quantitative-methods | economics | fsa | corporate | equity | fixed-income | derivatives | alternatives | portfolio | ethics
module: {module number, e.g., "M01"}
los: ["1.a", "1.b"]
created: {YYYY-MM-DD}
updated: {YYYY-MM-DD}
tags: [tag1, tag2]
---
```

## Mathematical Content Rules

1. **Inline math**: `$...$` — e.g., $r_f$ is the risk-free rate
2. **Block math**: `$$...$$` for standalone equations
3. **Always define variables** after formulas using "where" notation
4. **Label equations** with bold name before the block
5. **Use LaTeX only** — never Unicode math symbols
6. **Formula pages** group all formulas for a topic in one place
7. Mark uncertain OCR results: `> ⚠️ OCR — verify this formula`

## Operations

### INGEST
When user adds a new source to `{subject}/raw/`:
1. Read the source completely
2. Create summary in `{subject}/sources/`
3. Create/update module pages in `{subject}/modules/`
4. Create/update concept pages in `{subject}/concepts/`
5. Extract formulas to `{subject}/formulas/`
6. Create/update glossary in `{subject}/glossary/`
7. Create/update practice questions in `{subject}/practice/`
8. Update index.md and log.md

### QUERY
1. Read index.md → find relevant pages → synthesize answer
2. Ask: "File this as a wiki page?" If yes → save to analyses/

### LINT
Scan for contradictions, orphans, missing pages, missing cross-references.

## Rules

1. NEVER modify files in raw/
2. ALWAYS update index.md when creating pages
3. ALWAYS add [[wikilinks]] backlinks
4. Frontmatter is mandatory
5. One concept per page
6. All formulas in LaTeX
7. Always define variables after formulas
8. Log everything in log.md
9. Write for future-you — understandable in 6 months without context

## Local Model Configuration

For token-efficient operations, prefer local models:
- Embeddings: `nomic-embed-text` via Ollama
- Search: use index.md as primary lookup (no vector DB needed at this scale)
- Query: local LLM via Ollama for routine lookups, cloud LLM for complex synthesis
