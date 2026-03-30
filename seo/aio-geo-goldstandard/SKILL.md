---
name: aio-geo-goldstandard
description: End-to-end workflow for AI visibility (AIO, GEO, AEO)—answer-first, citation-ready copy plus crawlable markup and valid structured data. Use when drafting or refactoring marketing pages, articles, docs, or front-end implementations (HTML, MDX, React, Next.js, static sites); when the user asks for GEO, AEO, LLM SEO, AI Overviews, Perplexity, ChatGPT visibility, JSON-LD, entity clarity, or a pass/fail quality audit before ship.
---

# AIO / GEO / AEO Gold Standard

## Goal

Ship content and code that models can **quote cleanly**, crawlers can **parse**, and humans can **scan**—with explicit **pass/fail** QA.

## Collect first (or state assumptions)

- Target URL or topic, primary search intent, audience
- **Vertical / industry** (if unknown: state best guess and mark risk)
- **Subject entity / brand** (organization, product, person) and **canonical spelling** when the page must resolve a named entity
- **Target AI surfaces** (if known): e.g. ChatGPT, Perplexity, Google AI Overviews / AI Mode—citation patterns differ
- Source artifact (draft, live HTML, component, CMS export)
- Deliverable: copy only, code only, or both

For vertical- and platform-specific tuning, load [references/vertical-platform-heuristics.md](references/vertical-platform-heuristics.md).

## Workflow

1. **Mode** — `new-build` (from brief) or `upgrade` (existing asset).
2. **Entity map** — Primary entity (page intent); supporting entities (tools, orgs, products, metrics); trust entities (author, publisher, evidence).
3. **Answer-first copy** — See [references/goldstandard-checklist.md](references/goldstandard-checklist.md).
4. **Technical layer** — Server-rendered (or otherwise crawlable) core answers; JSON-LD aligned with visible text; internal links to canonical “entity home” hubs; honest `dateModified` / visible update signal; `llms.txt` only as a **supplement**, never the whole plan.
5. **QA** — Run checklist + Quick Gates; report FAIL items with fixes.
6. **Deliver** — Meet **Output contract** below.

## Non-negotiables (high-leverage)

**Declarative opening.** The first 1–2 sentences must state a clear proposition (e.g. “X is …”, “X requires …”, “Rule: …”). No throat-clearing (“In this article…”, “With the rise of…”) before the claim.

**Structure: all-in or flat.** Either use a **deliberate flat** flow (minimal headings) or a **full** hierarchy where **each H2 answers one question** and the **direct answer sits in the first 40–60 words** of that section. A **weak middle ground** (only three or four arbitrary H2s) is an explicit **FAIL**—it reads as fake structure.

**Universal negative signals in the lead (first ~120 words).**

- **Price-first**: Opening dominated by amounts, deals, or packages (unless the page intent is explicitly **pricing/finance/commerce**).
- **Hedging**: “might”, “could help”, “perhaps”, “may”, “it’s possible” as the main move—remove from the lead first.

Details and examples: [references/anti-patterns.md](references/anti-patterns.md).

## Companion skill

For **platform-scale** work (semantic graph ops in the database, entity governance across many URLs, KPI pipelines), hand off to **`ai-search-knowledge-graph-ops`** wherever that skill is installed in your agent environment (e.g. Codex or Cursor skills path). This skill stays on **page-level** copy + markup quality.

## Output contract

Always include:

- `Applied Mode` — `new-build` or `upgrade`
- `Vertical` — Named industry, or `unknown` + assumption
- `Target AI surfaces` — If known; otherwise `n/a`
- `Subject entity / brand` — If relevant; otherwise `n/a`
- `Key Changes` — Bullet list of substantive edits
- `Optimized Output` — Revised copy and/or code patch
- `Gold Standard QA (Pass/Fail)` — Checklist outcome + failed gates + fixes
- `Open Risks` — Residual gaps, missing data, or blocked validation

## Rules

- Prefer **extractable** answers over narrative filler.
- Prefer **specific, testable** claims; tie them to named entities and context.
- Do **not** fabricate citations, statistics, authors, or dates.
- Avoid manipulative “freshness” (fake updates).

## Quick gates (FAIL the deliverable if any is true)

- No direct answer **near the top** of the page or key sections.
- **Non-declarative** opening or **hedge-led** opening (see Non-negotiables).
- **Price-dominated** opening without explicit price intent.
- **Shallow heading set** (arbitrary 3–4 H2s) instead of flat or full structure.
- JSON-LD **missing**, **invalid**, or **inconsistent** with visible content.
- **Weak entity linkage** (unclear subject, inconsistent naming, orphan claims).
- **High-stakes** claims with no evidence or experience signal.
- **Cosmetic** SEO tweaks only—no retrieval or extraction improvement.
- **Missing “answer capsule”:** A substantive **H2** has no compact, extractable answer in its **first** block (unless the page is **deliberately** flat for vertical reasons—state that explicitly in QA).
- **Branded / navigational intent** without **on-page binding:** The brief targets a **specific** brand, organization, or person, but the **canonical name** is missing, inconsistent, or **not tied to the main facts** in the lead answer (ghost-citation risk).
- **Thin orphan:** Page is a single-intent **island** with **no** sensible cluster role or internal link to a hub (when a hub exists in the same site).

## References (load as needed)

| File | Use when |
|------|----------|
| [goldstandard-checklist.md](references/goldstandard-checklist.md) | Scoring and full pass/conditional/fail rubric |
| [anti-patterns.md](references/anti-patterns.md) | Symptom → fix library |
| [schema-snippets.md](references/schema-snippets.md) | Baseline JSON-LD templates |
| [vertical-platform-heuristics.md](references/vertical-platform-heuristics.md) | Industry + AI-surface tuning; third-party / “ghost citation” context |
