# Ad Angles & Hooks Architect

Creates systematic, avatar-driven ad angles and hooks for any business — from a validated Customer Avatar and optional Brand Strategy.

**No generic slogans.** Every angle traces back to avatar pains, gains, anxieties, and beliefs. Every hook is a scroll-stopper built on copywriting science.

---

## Core Principles

1. **Avatar first** — Angles emerge from avatar data (Pains, Gains, Anxieties, Beliefs, Voice of Customer). No avatar, no angles.
2. **Framework-driven** — PAS, BAB, HSO, AIDA, FAB, 4Ps are tools, not templates. Pick based on psychological fit, not habit.
3. **Angle ≠ Copy** — An angle is a strategic perspective. A hook is the scroll-stopper. Full ad copy is a downstream task, NOT this skill's job.
4. **Psychology over creativity** — Loss Aversion, Social Proof, Authority, Scarcity, Curiosity Gap, Autonomy Bias, Framing, Cognitive Ease — these are the engines.
5. **Segment-aware** — Different segments respond to different angles. Map every angle to its primary segment.
6. **Funnel-staged** — TOFU hooks differ from BOFU hooks. Prioritize angles by funnel stage.
7. **Quantified variety** — Minimum 15 angles, 30+ hooks. Volume produces quality through testing.
8. **Test-ready output** — Every angle/hook is structured so a media buyer can plug it into Meta/Google Ads immediately.

---

## Dependencies

**Required Input:**
- Customer Avatar (minimum Sections A–H from Avatar Architect output)
  - Context Profile (Section B) — for segment understanding
  - JTBD Core (Section C) — for functional/emotional job mapping
  - Pain/Gain/Anxiety/Desired Outcomes (Section E) — primary source for angles
  - Desire & Identity (Section F) — for emotional/lifestyle angles
  - Belief System (Section G) — for reframes and contrarian angles
  - Voice of Customer (Section H) — for hook language, quotes, trigger words
  - Segmentation Logic (Section I) — for segment-mapping
  - Strategic Implications (Section J) — for prioritization

**Optional Input:**
- Brand Strategy (from Brand Architect)
  - Positioning Statement
  - Brand Voice Guidelines
  - Messaging Hierarchy
  - Offer Architecture
  - Competitive Landscape
- Existing ad creatives (for audit/refinement)
- Competitor ads (for differentiation)

**Output feeds into:**
- Landing Page Creator (hero hooks, social proof sections, CTA copy)
- Ads Strategist (campaign structure, audience-angle mapping)
- Content Strategist (content pillars from top angles)
- Email Campaigns (subject lines, preview text from hooks)

---

## Framework Stack

### Copywriting Frameworks (for angle construction)

| Framework | Structure | Best For | Funnel Stage |
|-----------|-----------|----------|-------------|
| **PAS** (Problem-Agitate-Solution) | Pain → Consequence → Relief | Pain-heavy offers, urgency-driven | All stages |
| **BAB** (Before-After-Bridge) | Current pain → Ideal state → How to get there | Transformation, aspiration | TOFU, MOFU |
| **HSO** (Hook-Story-Offer) | Attention → Connection → Proposition | Story-driven, personal brand | TOFU, MOFU |
| **AIDA** (Attention-Interest-Desire-Action) | Awareness → Engagement → Wanting → Doing | Traditional, full-funnel | All stages |
| **FAB** (Feature-Advantage-Benefit) | What → So what → What it means | Product/service features | MOFU, BOFU |
| **4Ps** (Promise-Picture-Proof-Push) | Claim → Vision → Evidence → CTA | Trust-building, proof-heavy | MOFU, BOFU |

### Psychological Triggers (for hook potency)

| Trigger | Mechanism | Hook Application |
|---------|-----------|-----------------|
| **Loss Aversion** | Pain of losing > pleasure of gaining | Frame as "avoid losing X" not "gain Y" |
| **Social Proof** | People follow the crowd | "X others already..." testimonials, numbers |
| **Authority** | Expert opinion signals trust | Cite expertise, credentials, experience |
| **Scarcity** | Limited availability = higher value | Time limits, spots, exclusive access |
| **Curiosity Gap** | Open loops demand closure | "The #1 mistake...", "What nobody tells you..." |
| **Autonomy Bias** | People want control | "You decide. We deliver." dashboard/visibility |
| **Framing Effect** | Same fact, different perception | "Save 3 months" vs "Don't waste 3 months" |
| **Cognitive Ease** | Simple = true | Clear, concrete language over abstract complexity |
| **Status Quo Bias** | Change feels risky | "Already 50+ families made the leap" |
| **Specificity Effect** | Specific > general | "Save 80 hours" > "Save time", "47 families" > "many" |

### Hook Types (for scroll-stop classification)

| Type | Pattern | Example | Best For |
|------|---------|---------|----------|
| **Question** | Direct question addressing pain/desire | "Waste noch Stunden auf Ämtern?" | TOFU awareness |
| **Statement** | Bold claim or fact | "Die spanische Bürokratie kostet dich Monate." | TOFU/MOFU |
| **Shock** | Surprising statistic or consequence | "183 Tage und du bist steuerpflichtig." | TOFU (high impact) |
| **Story-Opener** | First line of a narrative | "Wir standen vor dem Notar und verstanden kein Wort." | TOFU/MOFU |
| **Contrarian** | Challenge common belief | "Warum 40% der Auswanderer zurückkehren." | TOFU (curiosity) |
| **Specific Number** | Concrete data point | "80 Stunden Recherche gespart." | All stages (credibility) |
| **Testimonial** | Real customer quote | "Wir hätten das nie alleine geschafft!" | MOFU/BOFU (trust) |
| **Curiosity Gap** | Hint without reveal | "Der eine Fehler, der deinen Traum kostet." | TOFU (click-through) |
| **Challenge** | Question competence or readiness | "Traust du dich, den ersten Schritt zu machen?" | BOFU (commitment) |
| **If/Then** | Conditional benefit | "Wenn du in 3 Monaten einziehen willst..." | MOFU/BOFU (solution) |

---

## Output Structure

The skill produces ONE document with four sections:

### Section A — Ad Angles (15–25)

For each angle:
```yaml
angle:
  id: A1-A25
  name: "Human-readable name (e.g. 'Der Bürokratie-Exit')"
  avatar_insight: "Which P/G/A/D/Section it draws from"
  psychological_trigger: "Primary trigger (e.g. Loss Aversion)"
  framework: "Primary framework (e.g. PAS)"
  description: "2-3 sentences explaining the angle"
  primary_segment: "Which segment responds best"
  funnel_stage: "TOFU | MOFU | BOFU"
```

### Section B — Hooks (30–50)

For each hook:
```yaml
hook:
  id: H1-H50
  text: "The actual hook text (language: client's market language)"
  char_count: "Must be ≤125 for Meta, ≤90 for Google headline"
  angle_ref: "Which angle (A1-A25) this hook serves"
  hook_type: "Question|Statement|Shock|Story-Opener|Contrarian|Specific Number|Testimonial|Curiosity Gap|Challenge|If-Then"
  platform: "Meta|Google|LinkedIn|TikTok|Universal"
  segment_fit: "Which segment(s) this resonates with"
```

### Section C — Funnel Prioritization

```yaml
funnel:
  tofu_top_5: [angle_ids]  # Awareness, cold audiences
  mofu_top_5: [angle_ids]  # Consideration, warm audiences
  bofu_top_5: [angle_ids]  # Conversion, hot audiences
  rationale: "Why this ordering based on avatar data"
```

### Section D — Segment × Angle Matrix + Trigger Words

```yaml
matrix:
  segments: [segment names from avatar]
  segment_mapping:
    - segment: "Name"
      primary_angles: [angle_ids]
      secondary_angles: [angle_ids]
      trigger_words: [from avatar Voice of Customer]
  cross_sell_note: "Which angles from segment A could work for segment B"
```

---

## Execution Rules

### 1. Avatar Mining (extract angle seeds)

Before writing a single angle, systematically extract from the avatar:

```
PAINS → Pain Relief Angles (PAS)
GAINS → Aspiration Angles (BAB)
ANXIETIES → Risk Reversal Angles (4Ps)
DESIRED OUTCOMES → Velocity/Promise Angles (BAB/HSO)
BELIEFS (hindering) → Contrarian/Reframe Angles (HSO)
BELIEFS (enabling) → Reinforcement Angles (AIDA)
VOICE OF CUSTOMER (quotes) → Testimonial Hooks
TRIGGER WORDS → Hook vocabulary pool
DESIRED IDENTITY (toward) → Aspiration Hooks
DESIRED IDENTITY (away from) → Fear Hooks
REFRAME OPPORTUNITIES → Perspective-shift Angles
```

### 2. Angle Generation Rules

- **Minimum 15 angles** — aim for 20
- Every angle MUST reference a specific avatar element (not vague "we're great")
- Every angle MUST name its psychological trigger
- Every angle MUST name its framework
- Angles must be mutually distinguishable — no two angles saying the same thing differently
- Include at least 2 contrarian angles (challenge common beliefs)
- Include at least 2 emotional/lifestyle angles (desire/identity driven)
- Include at least 2 authority/trust angles (social proof, expertise)
- Include at least 2 risk-reversal angles (guarantees, transparency)

### 3. Hook Generation Rules

- **Minimum 30 hooks** — aim for 40+
- Language must match the avatar's Voice of Customer section (their words, not yours)
- Maximum 125 characters for Meta text hooks
- Maximum 90 characters for Google headline hooks
- Maximum 30 characters for Google description hooks
- Every hook tagged with angle, type, platform, segment
- No marketing fluff words (innovativ, revolutionär, einzigartig) unless avatar uses them
- Include hooks in avatar's market language (German for DACH, English for US, etc.)
- At least 3 hooks per angle (test variations)
- Every trigger word from the avatar must appear in at least one hook

### 4. Funnel Stage Rules

**TOFU (Awareness):**
- Lead with pain, curiosity, or contrarian angles
- Hooks: Question, Shock, Curiosity Gap, Story-Opener
- Goal: Stop scroll, create "I need to know more"
- No selling — only problem acknowledgment

**MOFU (Consideration):**
- Lead with solution-oriented, authority, and comparison angles
- Hooks: Statement, Specific Number, Testimonial, If/Then
- Goal: "This could work for me" → demonstrate expertise
- Soft CTA acceptable

**BOFU (Conversion):**
- Lead with trust, urgency, and risk-reversal angles
- Hooks: Testimonial, Specific Number, Challenge, Statement
- Goal: "I should act now" → remove last objection
- Strong CTA required

### 5. Quality Checklist (before delivering)

```yaml
quality_gate:
  angles:
    total: "≥15"
    all_have_avatar_ref: yes
    all_have_psych_trigger: yes
    all_have_framework: yes
    no_duplicates: yes
    has_contrarian: yes  # ≥2
    has_emotional: yes  # ≥2
    has_authority: yes  # ≥2
    has_risk_reversal: yes  # ≥2
  hooks:
    total: "≥30"
    all_under_125_chars: yes
    all_tagged: yes  # angle, type, platform, segment
    uses_trigger_words: yes
    matches_avatar_language: yes
  funnel:
    tofu_top_5: yes
    mofu_top_5: yes
    bofu_top_5: yes
    segment_matrix: yes
    trigger_words_mapped: yes
```

---

## NotebookLM Integration

For deep research support, use the NotebookLM research notebook:

- **Notebook:** `🪝 Hooks & Ad Angles — Avatar-Driven Research`
- **ID:** `df3b2ed0-e9dd-4c4c-96a6-5b9daebeedf4`
- **Sources:** 21 (15 web articles, 5 YouTube videos, avatar + brand docs)
- **Usage:** Query for framework details, psychological principles, and hook best practices during angle/hook generation

---

## Pipeline Position

```
Lead → Onboarding → Avatar → Brand → Angles & Hooks → Landing Page → Lead Magnet → Content → Ads → SEO → Analytics
                                          ↑ NEU
```

The Angles & Hooks Architect sits **after Brand** and **before Landing Page**:

- **Input from Brand:** Positioning, Voice, Messaging Hierarchy, Offer Architecture
- **Output to Landing Page:** Hero hooks, social proof angles, CTA language
- **Output to Ads:** Campaign angles, hook variations for A/B testing
- **Output to Content:** Content pillars derived from top-performing angles

---

## 🧠 Learned Patterns

### 2026-04-10 — Initial Build
- Scope clarification: Skill is GENERIC (avatar-agnostic), not client-specific. Never hardcode client data.
- Angle ≠ Copy: An angle is strategic direction. A hook is the scroll-stopper. Full ad copy is a different task entirely.
- NotebookLM sources are generic copywriting/psychology references — not client content.
- Always generate in the avatar's market language (check Voice of Customer for language cues).
- Minimum output: 15 angles, 30 hooks. Volume enables testing.
