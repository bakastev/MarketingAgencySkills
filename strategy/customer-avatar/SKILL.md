# Deep Customer Avatar Architect

Creates evidence-based customer avatars using JTBD, Job Map, behavioral psychology, Belief Systems, and psycholinguistic VoC analysis.

**No fictional personas.** Prioritized decision models with clear uncertainties, segment logic, and strategic implications.

---

## Core Principles

1. **Jobs over demographics** — Age, gender, income are secondary variables. Primary: Situation, Job, Motivation, Constraint, Transformation.
2. **Evidence-backed statements only** — Every statement gets an evidence status label.
3. **Separate observation, interpretation, and hypothesis** — No mixing.
4. **Address functional, emotional, and social jobs** — Equally.
5. **Extract Desire, Identity, and Belief Systems** — That's the leverage point.
6. **Use real language patterns from the target group** — Language is behavior.
7. **Every output must be actionable** — For marketing, product, sales.

---

## Evidence Status Labels

| Label | Meaning |
|---|---|
| `verified` | Directly found in raw data (quote, metric) |
| `strongly plausible` | Multiple indicators, no contradiction |
| `weakly plausible` | Single indicator, could be coincidence |
| `open assumption` | Logically inferred, but unverified |

---

## Workflow (9 Modules)

### Module 0: Deep Research (Automatic)

**Task:** Supplement provided raw data with external research BEFORE analysis begins.

**This module runs automatically.** It is NOT optional — it ensures the evidence base goes beyond what was manually provided.

**Research Targets (based on client context):**
1. **Competitor Voice of Customer** — Scrape competitor reviews, testimonials, social media comments (Firecrawl)
2. **Reddit & Forum Discussions** — Search relevant subreddits/forums for organic customer language, complaints, desires (Reddit via Composio)
3. **Market & Category Intelligence** — Category trends, positioning of competitors, market gaps (Perplexity web search)
4. **Customer Language Corpus** — Collect real quotes from reviews (Google, Trustpilot, G2), social media, Q&A sites (Firecrawl + Perplexity)
5. **Industry Pain Points** — Industry reports, common complaints, emerging trends (Perplexity + NotebookLM)

**Available Research Tools:**

| Tool | Best For | Access |
|---|---|---|
| **Firecrawl** (MCP) | Website scraping, competitor analysis, review sites | MCP Server — scrape any URL |
| **Perplexity** (web_search) | Market research, trends, category analysis, finding sources | Native — `web_search` tool |
| **Reddit** (Composio) | Organic customer discussions, pain points, language patterns | Composio — reddit tools |
| **NotebookLM** (CLI) | Deep research synthesis, multi-source analysis | CLI — `notebooklm source add` + `notebooklm ask` |
| **Web Fetch** | Quick URL extraction, lightweight scraping | Native — `web_fetch` tool |

**Research Process:**
1. **Identify research gaps** — What do we NOT have in the provided raw data?
2. **Build search queries** — Based on:
   - Target audience description
   - Product/service keywords
   - Competitor names (if known)
   - Industry/category terms
3. **Execute research** — Use tools in order of relevance:
   - First: Perplexity (broad market/category context)
   - Second: Firecrawl (competitor sites, review pages, testimonials)
   - Third: Reddit/Composio (organic discussions)
   - Fourth: NotebookLM (synthesize findings into structured knowledge)
4. **Normalize findings** — Convert all research into Evidence Units (same format as Module 1)
5. **Merge with provided data** — Combined evidence base feeds into Module 1

**Research Output (per source):**
```yaml
source_type: research | competitor_scrape | reddit | review | market_report | notebooklm
source_id: string (URL or tool reference)
quotes: [list of verbatim quotes from target group]
category: pain | gain | desire | belief | behavior | objection | competitor_claim | market_trend
certainty: high | medium | low
notes: string
```

**Quality Gate:**
- Minimum 5 additional external sources for a new avatar
- Minimum 3 additional sources for avatar refinement
- Every quote must have a source URL
- If research returns insufficient results, explicitly flag in Module 8 (Section K)

---

### Module 1: Research Intake & Evidence Normalization

**Task:** Convert all inputs (provided raw data + Module 0 research) into a standardized knowledge model.

**Accepted Inputs:**
- Interview transcripts
- Sales calls
- Support tickets
- Reviews
- Reddit/Forum discussions
- Surveys (open text)
- CRM notes
- Landing page comments
- Call center VoC
- Product usage data
- Market research notes
- Competitor claims

**Per Output Unit (Evidence Unit):**
```
source_type: string
source_id: string
quote: string (verbatim quote)
category: pain | gain | desire | belief | behavior | objection
candidate_job_stage: define | locate | prepare | confirm | execute | monitor | modify | conclude
emotional_signal: string
certainty: high | medium | low
inferred_meaning: string
```

**Steps:**
1. Classify data sources
2. Remove duplicates
3. Break raw data into Evidence Units
4. Distinguish between observed, interpreted, and inferred
5. Weight source reliability

---

### Module 2: JTBD Extraction Engine

**Task:** Extract the actual Job-to-be-Done.

**Separate:**
- **Functional job** — What specifically needs to get done
- **Emotional job** — How the person wants to feel afterwards
- **Social job** — How they want to appear to others

**Guiding questions:**
- What is the person specifically trying to accomplish?
- What progress do they want in their life/work situation?
- How do they want to feel afterwards?
- How do they want to appear to others?

**Output:**
```yaml
jtbd:
  functional_job: [list]
  emotional_job: [list]
  social_job: [list]
```

**Distinguish Job types:**
- Main Job
- Related Jobs
- Consumption Jobs
- Switching Jobs (evaluate providers, onboard team, justify internally, avoid loss of face)

---

### Module 3: Job Map Deconstruction

**Task:** Break down the job along 8 phases.

**Phases:**
1. **Define** — Recognize & define the problem
2. **Locate** — Find a solution
3. **Prepare** — Preparation
4. **Confirm** — Make a decision
5. **Execute** — Implementation
6. **Monitor** — Check results
7. **Modify** — Adjust
8. **Conclude** — Evaluate

**Extract per phase:**
- Goals
- Obstacles
- Error sources
- Time losses
- Emotional friction
- Desired improvement

**Output:**
```yaml
job_map:
  <phase>:
    goals: [list]
    pains: [list]
    gains: [list]
    emotional_risk: [list]
    opportunity: [list]  # Opportunities for product/communication
```

**Important:** Operationalize pains, don't keep them generic.
- ❌ "wants to save time"
- ✅ "reduce preparation time before core task from 18 min to under 7 min"

---

### Module 4: Pain–Gain–Anxiety–Desired Outcome Matrix

**Task:** Model adoption barriers alongside benefits.

**Four levels:**
- **Pains** — What's bothering them right now?
- **Gains** — What would be valuable?
- **Anxieties** — What are they afraid of?
- **Desired Outcomes** — How do they measure success?

**Output:**
```yaml
decision_tension:
  pains: [list]
  gains: [list]
  anxieties: [list]
  desired_outcomes: [list]
```

---

### Module 5: Desire & Identity Layer

**Task:** Model deeper desires and identity level.

**Questions:**
- Who does the customer want to be while doing this?
- Which identity do they want to confirm or achieve?
- Which identity do they want to avoid?

**Desire classes:**
Control | Security | Status | Belonging | Self-efficacy | Simplification | Freedom | Recognition | Progress | Distinction | Relief | Transformation

**Output:**
```yaml
core_desire:
  primary: string
  secondary: [list]
identity_pull:
  toward: [list]
  away_from: [list]
product_positioning:
  - empowerment | security | prestige | relief | transformation | belonging
```

---

### Module 6: Belief System Mining

**Task:** Extract beliefs, mental models, and adoption logics.

**Categories:**
- beliefs about self
- beliefs about the problem
- beliefs about existing solutions
- beliefs about the market
- beliefs about success/failure
- beliefs about risk

**Classify each belief as:**
- enabling
- hindering
- identity-stabilizing
- purchase-blocking
- messaging lever

**Output:**
```yaml
beliefs:
  about_self: [list]
  about_problem: [list]
  about_solutions: [list]
  about_risk: [list]
belief_classification:
  enabling: [list]
  hindering: [list]
  purchase_blocking: [list]
  messaging_levers: [list]
```

---

### Module 7: Psycholinguistic Voice Model

**Task:** Model the linguistic fingerprint of the target group.

**Analysis dimensions:**
- I/We-frame vs. third person
- Concrete vs. abstract
- Brief-pragmatic vs. narrative
- Negativity-avoidant vs. aspirational-goal-oriented
- Analytical vs. identity-driven
- Intensity markers (really, absolutely, not at all, ...)
- Status language (professional, modern, etc.)
- Metaphors (chaos, order, battle, journey, etc.)

**Output:**
```yaml
voice_profile:
  tone: [list]
  preferred_language_patterns: [list]
  mirrored_phrases: [list]      # Quotes to adopt
  avoid_language: [list]        # No-go words
  headline_patterns: [list]     # Derivable headlines
  cta_style: string
```

---

### Module 8: Avatar Synthesis & Strategic Activation

**Task:** Convert everything into an actionable decision profile.

---

## Final Output Structure

### A. Executive Snapshot
6–10 sentences: Who, what are they looking for, what's blocking them, why do they really buy.

### B. Context Profile
Triggering situation, environment, time pressure, responsibilities, stakeholders, constraints.

### C. JTBD Core
Functional job, emotional job, social job, success definition.

### D. Job Map
Per phase: task, friction, desired result, opportunities.

### E. Pain/Gain/Anxiety/Outcome
Prioritized by relevance and purchase impact.

### F. Desire & Identity
Core desire, identity aspiration, identity avoidance, status signals.

### G. Belief System
Dominant beliefs, central objections, purchase blockers, reframe opportunities.

### H. Voice of Customer
Original formulations, language patterns, trigger words, no-go words, messaging mirrors.

### I. Segmentation Logic
Who does this avatar apply to? Differentiation from adjacent avatars. What makes them "active"?

### J. Strategic Implications
Positioning, offer, proof, pricing communication, sales, content, product prioritization.

### K. Confidence & Gaps
What is well-evidenced? Where is data missing? Which hypotheses need validation?

---

## Advanced Features

### 1. Contradiction Handling
Actively search for and explain contradictions.
- Example: Says "I want simplicity" but purchases complex premium tools
- Analysis: Perhaps simplicity isn't the primary motivator — control or status through competence is.

### 2. Segment Split Detection
Recognize when multiple avatars are hidden in a dataset.
- Don't average — separate them.
- "The data suggests two distinct progress logics."

### 3. Trigger Event Mapping
When does the persona become purchase-active?
- Frustration peak | Role change | Team growth | Process break | Tool failure | KPI pressure | Budget approval | Peer comparison

### 4. Switching Force Analysis
- **Push of the situation** — Current pain
- **Pull of the new solution** — Promised benefit
- **Anxiety of change** — Fear of transition
- **Habit of the present** — Inertia of the status quo

### 5. Message Testing Layer
3–5 messaging angles with assessment (strong fit / moderate / risky):
- Control-oriented
- Status-oriented
- Relief-oriented
- Efficiency-oriented
- Identity-oriented

---

## Pipeline Integration Rules

### Critical Dependencies ( downstream skills depend on ALL of these!)
The following sections are MANDATORY and must be complete before any downstream skill (Brand Architect, Landing Page, etc.) processes this avatar:

**Tier 1 — Blocking (incomplete = STOP, do not proceed):**
- Section A (Executive Snapshot) — downstream needs the core narrative
- Section C (JTBD Core) — functional/emotional/social jobs drive all messaging
- Section E (Pain/Gain/Anxiety/Outcome) — foundation for all copy and offers
- Section F (Desire & Identity) — drives positioning and emotional messaging
- Section G (Belief System) — drives objection handling and FAQ
- Section H (Voice of Customer) — drives brand voice and copy style

**Tier 2 — Important (incomplete = flag, may proceed with caution):**
- Section B (Context Profile) — enriches targeting
- Section D (Job Map) — enriches funnel design
- Section I (Segmentation Logic) — critical for multi-segment avatars
- Section J (Strategic Implications) — guides offer architecture
- Section K (Confidence & Gaps) — guides validation priorities

### Time Management
When running as subagent with time constraints:
1. Write Sections A, C, E, F, G, H FIRST (Tier 1)
2. Write Sections B, D, I, J, K SECOND (Tier 2)
3. Google Doc upload is LAST — local file has priority
4. If time runs out during Tier 2: save what you have, flag incomplete sections explicitly

### Save Early
Write the Markdown file incrementally. Do NOT build everything in memory and save once. Save after each section to prevent data loss on timeout.

---

## Guardrails

- ❌ No stereotypical demographics (no "Anna, 34, loves coffee")
- ❌ No invented hobbies or biographies
- ❌ No psychological diagnoses
- ❌ No unsubstantiated motives stated as facts
- ❌ No generic platitudes ("wants to save time")
- ✅ Clearly mark original quotes
- ✅ Explicitly document contradictions
- ✅ Mark statements with evidence status
- ✅ Name open questions and data gaps
- ✅ Save incrementally — never hold everything in memory

---

## Usage

### Minimum Input
At least 2–3 data sources with qualitative raw data (interviews, reviews, support tickets, forum posts).

### Quality Input
5+ data sources, including at least direct customer statements (interviews, sales calls).

### Process
1. Provide raw data (as files or text)
2. Skill runs through all 8 modules
3. Output: Complete avatar as a structured document (Markdown)
4. Q&A on the avatar for refinement

### Output Format
Markdown with YAML frontmatter for structured data + narrative sections.

---

## The One Question This Skill Answers

> "What progress movement is this target group attempting under what pressure, which psychological forces accelerate or block this movement, and which language activates trust, action, and purchase readiness?"
-e 
---

## 🧠 Learned Patterns

_This section is auto-maintained by the Skill Learning System. Do not edit manually._

<!-- No learnings yet. First task execution will populate this section. -->
