# Brand Architect — Evidence-Based Brand Strategy

Translates a validated Customer Avatar into a complete brand strategy: Identity, Voice, Positioning, and Offer Design.

**No branding without evidence.** Every brand decision traces back to avatar data — pains, gains, beliefs, desires, and voice patterns.

---

## Core Principles

1. **Avatar first** — Brand exists to serve the customer. No avatar, no brand work.
2. **Evidence-driven** — Every positioning claim, voice decision, and offer element must connect to avatar data.
3. **Consistency over creativity** — A boring consistent brand beats a creative inconsistent one.
4. **Positioning is a choice** — You can't be everything to everyone. Pick a lane.
5. **Voice is behavior, not decoration** — How you talk IS your brand. The avatar's language patterns define the voice.
6. **Offers solve jobs** — Products exist to get a job done. Design offers around JTBD, not features.
7. **Category before brand** — If you can, define the category. The category leader owns the brand.

---

## Dependencies

**Required Input:**
- Customer Avatar (minimum Sections A–H from the Avatar Architect output)
  - JTBD Core (Section C)
  - Pain/Gain/Anxiety/Outcome (Section E)
  - Desire & Identity (Section F)
  - Belief System (Section G)
  - Voice of Customer (Section H)
  - Strategic Implications (Section J)

**Optional Input:**
- Existing brand materials (logo, website, social media, ads)
- Competitor analysis
- Market/category context
- Customer interview transcripts
- Sales call recordings

**Output feeds into:**
- Content Strategist (messaging matrix, content pillars)
- Ads Strategist (hooks, ad angles, audience targeting)
- Social Media Manager (tone guidelines, content calendar)
- Landing Page Agent (copy, structure, conversion elements)
- Lead Magnet Agent (lead magnet concepts, formats)

---

## Framework Stack

This skill draws on established frameworks — applied specifically to AI-agent-driven marketing:

| Framework | Used For | Source |
|---|---|---|
| **Kapferer Brand Identity Prism** | Brand identity structure | Kapferer (2012) |
| **Aaker Brand Equity Model** | Brand asset architecture | Aaker (1991) |
| **Category Design** | Market positioning & category creation | Play Bigger (2016) |
| **Brand Positioning Canvas** | Competitive positioning | Zoom/GE |
| **Value Proposition Canvas** | Offer-customer fit | Strategyzer |
| **Brand Messaging Framework** | Messaging hierarchy | Vital Design / WRITER |
| **Brand Alignment Strategy** | Internal-external consistency | LaunchNotes |

---

## Workflow (7 Modules)

### Module 0: Brand Research (Automatic)

**Task:** Research the competitive landscape, category positioning, and validate avatar evidence BEFORE building the brand strategy.

**This module runs automatically.** It fills the gap between "we know the customer" and "we know the market."

**Research Targets:**
1. **Competitor Brand Analysis** — Who else targets this avatar? What positions do they own? How do they talk? (Firecrawl)
2. **Category Language** — What vocabulary, metaphors, and frames dominate the category? How can we differentiate? (Perplexity + Firecrawl)
3. **Social Proof Mining** — What do real customers say about similar products/services? What language do they use? (Reddit via Composio)
4. **Pricing Intelligence** — What does the market charge for similar offers? What's the price anchoring? (Perplexity)
5. **Brand Archetype Analysis** — What brand personalities exist in this category? Where is whitespace? (NotebookLM synthesis)

**Available Research Tools:**

| Tool | Best For | Access |
|---|---|---|
| **Firecrawl** (MCP) | Competitor website scraping, landing page copy, ad copy analysis | MCP Server |
| **Perplexity** (web_search) | Category research, competitor overview, pricing benchmarks | Native — `web_search` |
| **Reddit** (Composio) | Customer opinions on competitors, organic language, pain points | Composio — reddit tools |
| **NotebookLM** (CLI) | Synthesize competitor landscape into strategic insights | CLI — `notebooklm` |
| **Web Fetch** | Quick competitor page extraction | Native — `web_fetch` |

**Research Process:**
1. **Extract research queries from avatar:**
   - Target audience keywords (from Section I — Segmentation)
   - Competitor names (from Section J — if mentioned)
   - Category terms (from Section J — Positioning)
   - Belief keywords (from Section G — for social proof validation)
2. **Execute research** — Prioritized by avatar data gaps:
   - First: Perplexity (broad competitive landscape)
   - Second: Firecrawl (top 3-5 competitor websites — copy, positioning, pricing)
   - Third: Reddit (customer sentiment, organic language)
   - Fourth: NotebookLM (optional — synthesize if complex competitive landscape)
3. **Output research brief** — Structured competitive analysis:
```yaml
competitor_landscape:
  - name: string
    position: string
    pricing: string
    voice_tone: string
    strengths: [list]
    weaknesses: [list]
    avatar_alignment: high | medium | low
category_language:
  dominant_frames: [list]
  competitor_vocabulary: [list]
  whitespace_opportunities: [list]
pricing_intelligence:
  market_range: string
  anchor_points: [list]
  positioning_vs_price: string
social_proof_signals:
  common_praise: [list]
  common_complaints: [list]
  language_patterns: [list]
```

**Quality Gate:**
- Minimum 3 competitors analyzed
- At least 1 pricing data point
- Social proof signals from at least 2 sources
- If research is insufficient, flag in Module 6 (Section I)

---

### Module 1: Brand Diagnosis

**Task:** Assess the current state — is there an existing brand or a blank slate?

**Steps:**
1. **Input Review** — Read the avatar thoroughly. Highlight:
   - Core Desire and Identity Pull (Section F)
   - Messaging Levers (Section G)
   - Voice Patterns (Section H)
   - Positioning Implications (Section J)
2. **Existing Brand Audit** (if brand exists):
   - Website, social profiles, ads, collateral
   - Compare brand expression against avatar expectations
   - Identify gaps between what the brand says and what the avatar needs
3. **Competitive Landscape** (if data available):
   - Who else serves this avatar?
   - What positions are taken?
   - Where is whitespace?
4. **Verdict:** Fresh build or refinement?

**Output:**
```yaml
diagnosis:
  status: fresh | refinement | pivot
  current_brand_score: 1-10
  avatar_alignment: high | medium | low
  key_gaps: [list]
  competitive_position: [description]
```

---

### Module 2: Brand Positioning

**Task:** Define WHERE the brand lives in the customer's mind.

**Using Category Design + Brand Positioning Canvas:**

**2A. Category Assessment**
- Is this an existing category or a new one?
- If existing: Who is the category king? What's the point of difference?
- If new: What's the "category design problem"? What needs to be renamed/redefined?

**2B. Positioning Statement**
```
For [target avatar] who [core job + struggle],
[brand name] is the [category] that [key differentiator]
because [reason to believe].
Unlike [primary alternative], we [unique value].
```

**2C. Brand Ladder**
```
Emotional Benefit → Functional Benefit → Attribute/Feature → Proof
```

Map this using the avatar's Desire & Identity (Section F):
- What identity does the avatar aspire to? → Emotional Benefit
- What job gets done? → Functional Benefit
- What specifically do we deliver? → Attributes
- Why should they believe us? → Proof points (from avatar evidence)

**2D. Competitive Moat**
- What makes this defensible?
- Connect to avatar's purchase-blocking beliefs — how do we overcome them?

**Output:**
```yaml
positioning:
  category: string
  category_type: existing | new | sub-category
  positioning_statement: string
  brand_ladder:
    emotional_benefit: string
    functional_benefit: string
    attributes: [list]
    proof_points: [list]
  anti_position: string  # What we are NOT
  competitive_moat: string
```

---

### Module 3: Brand Identity

**Task:** Define WHO the brand is — its personality, values, and visual direction.

**Using Kapferer's Brand Identity Prism + Aaker's Brand Equity Model:**

**3A. Brand Prism (6 Facets)**

| Facet | Question | Source |
|---|---|---|
| **Physique** | What does the brand look/sound like? | Avatar Voice (Section H) |
| **Personality** | If the brand were a person, who? | Avatar Identity Pull (Section F) |
| **Culture** | What values does it embody? | Avatar Beliefs (Section G) — enabling beliefs |
| **Relationship** | How does it relate to the customer? | Avatar Desired Outcomes (Section E) |
| **Reflection** | What kind of customer uses it? | Avatar Segmentation (Section I) |
| **Self-Image** | How does the customer see themselves? | Avatar Identity Toward (Section F) |

**3B. Core Values**
- Derive from avatar's enabling beliefs and messaging levers
- Max 5 values. Each must connect to avatar data.
- For each: value name, definition, avatar connection, behavioral expression

**3C. Brand Personality Traits**
- Based on avatar voice patterns (Section H) and tone preferences
- Define 5-7 personality traits with scale (e.g., "Direct — not corporate")
- Include: DO and DON'T examples for each trait

**3D. Visual Direction (guidance, not design)**
- Mood direction based on personality (not specific colors/fonts)
- Logo direction (wordmark vs. symbol vs. combination)
- Photography/Illustration style
- Connect to avatar's aesthetic expectations

**Output:**
```yaml
identity:
  prism:
    physique: string
    personality: string
    culture: [list]
    relationship: string
    reflection: string
    self_image: string
  values:
    - name: string
      definition: string
      avatar_connection: string
      behavioral_expression: string
  personality_traits:
    - trait: string
      scale: string
      do: [list]
      dont: [list]
  visual_direction:
    mood: string
    logo_direction: string
    imagery_style: string
```

---

### Module 4: Brand Voice & Messaging

**Task:** Define HOW the brand talks — and build the messaging hierarchy.

**This is the highest-leverage module.** Avatar Section H (Voice of Customer) is the primary input.

**4A. Voice System**

Define voice across 4 dimensions:

| Dimension | Spectrum | Avatar-Driven Choice |
|---|---|---|
| **Formality** | Casual ←→ Formal | From avatar tone (Section H) |
| **Intensity** | Calm ←→ Urgent | From avatar anxieties (Section E) |
| **Expertise** | Peer ←→ Authority | From avatar beliefs about self (Section G) |
| **Emotion** | Analytical ←→ Emotional | From avatar desires (Section F) |

For each dimension: pick the position, explain WHY (avatar data), give examples.

**4B. Vocabulary Map**
- Adopted phrases: From avatar mirrored phrases (Section H)
- Trigger words: From avatar messaging levers (Section G)
- Avoid list: From avatar avoid-language (Section H)
- Power phrases: 10-15 brand-specific phrases derived from avatar data

**4C. Messaging Hierarchy**

Build a 3-level messaging framework:

```
Level 1: BRAND PROMISE
  One sentence that captures everything. The North Star.
  → Derived from: Emotional Benefit + Core Desire

Level 2: VALUE PILLARS (3-5)
  Supporting claims that prove the promise.
  → Each maps to a functional benefit + proof point

Level 3: MESSAGING ANGLES (per pillar)
  Specific angles for different contexts (ads, social, email, LP).
  → Derived from: Belief reframes, switching forces, voice patterns
```

**4D. Messaging Angles (5 Types)**
From the avatar's belief system (Section G) and pain/gain matrix (Section E):

1. **Control Angle** — addresses desire for control/autonomy
2. **Relief Angle** — addresses anxieties, removes friction
3. **Identity Angle** — addresses who they want to become
4. **Efficiency Angle** — addresses time/effort pains
5. **Proof Angle** — addresses skepticism, purchase-blocking beliefs

For each angle:
- Hook (derived from avatar pain/belief)
- Core message
- Supporting evidence
- CTA style

**Output:**
```yaml
voice:
  dimensions:
    formality: string
    intensity: string
    expertise: string
    emotion: string
  vocabulary:
    adopted_phrases: [list]
    trigger_words: [list]
    avoid_list: [list]
    power_phrases: [list]
messaging:
  brand_promise: string
  value_pillars:
    - name: string
      claim: string
      proof: string
  angles:
    - type: string
      hook: string
      message: string
      evidence: string
      cta: string
```

---

### Module 5: Offer Architecture

**Task:** Design the offer stack — what to sell, how to price, how to structure.

**Using Value Proposition Canvas + Avatar JTBD:**

**5A. Offer-Avatar Fit**

Map each offer element to the avatar:
```
Offer Element → Avatar Job → Pain Solved → Gain Delivered → Belief Reframed
```

**5B. Offer Stack Design**

```
TRIPWIRE (Entry)
  Purpose: Remove purchase-blocking belief "can this help me?"
  Price: Low-friction (avatar-desired outcome for minimal risk)
  Deliverable: Quick win, tangible result
  → Connects to: Avatar Confirm phase (Job Map Phase 4)

CORE OFFER
  Purpose: Deliver the main transformation
  Price: Market-aligned, value-stacked
  Deliverable: Complete job fulfillment
  → Connects to: Avatar Execute phase (Job Map Phase 5)

MAXIMIZER (Upsell)
  Purpose: Ongoing support / advanced transformation
  Price: Premium, relationship-based
  Deliverable: Monitoring, refinement, community
  → Connects to: Avatar Monitor/Modify phases (Job Map Phases 6-7)
```

**5C. Pricing Strategy**
- Price anchoring using avatar's desired outcomes
- Cost-of-inaction framing (from avatar anxieties)
- Risk reversal tactics (from avatar purchase-blocking beliefs)
- Value stacking (each stack element maps to a specific pain/gain)

**5D. Funnel Integration Points**
Where does each offer live in the customer journey?
- Lead Magnet → Tripwire → Core Offer → Maximizer
- Each step maps to a Job Map phase
- Each transition overcomes a specific belief barrier

**Output:**
```yaml
offers:
  tripwire:
    name: string
    price: string
    deliverable: string
    avatar_job_phase: string
    belief_overcome: string
  core_offer:
    name: string
    price: string
    deliverable: string
    avatar_job_phase: string
  maximizer:
    name: string
    price: string
    deliverable: string
    avatar_job_phase: string
  pricing_strategy:
    anchoring: string
    cost_of_inaction: string
    risk_reversal: string
  funnel_map:
    lead_magnet: string
    tripwire: string
    core_offer: string
    maximizer: string
```

---

### Module 6: Brand Strategy Document

**Task:** Synthesize everything into a actionable brand brief.

**Sections:**

### A. Executive Summary
3-5 sentences: Positioning, promise, target, key differentiator.

### B. Positioning
Category, positioning statement, anti-position, competitive moat.

### C. Brand Identity
Prism, values, personality traits, visual direction.

### D. Brand Voice
Voice dimensions, vocabulary map, tone guidelines with DO/DON'T.

### E. Messaging Framework
Brand promise, value pillars, messaging angles.

### F. Offer Architecture
Offer stack, pricing strategy, funnel map.

### G. Avatar-to-Brand Traceability
Table mapping every brand decision back to avatar data:
```
Brand Decision | Avatar Source | Evidence Status
Positioning "X" | Section F - Identity Pull | verified
Voice "Y" | Section H - Tone | strongly plausible
Offer "Z" | Section E - Pain | verified
```

### H. Recommendations
- Priority actions for brand launch/refinement
- Content pillars derived from messaging
- Suggested channels based on avatar behavior
- Next skill triggers (Content Strategist, Ads Strategist, etc.)

### I. Confidence & Gaps
What is well-grounded? Where is data missing?
- Map to avatar's Confidence & Gaps (Section K)
- Brand-specific gaps (competitor data, market validation, pricing testing)

---

## Advanced Features

### 1. Brand Refinement Mode
When an existing brand is provided:
- Compare brand expression against avatar expectations
- Score consistency (voice, visual, messaging, offer)
- Identify drift: where has the brand deviated from its avatar?
- Provide specific fixes, not vague recommendations

### 2. Multi-Avatar Brand Architecture
When multiple avatars exist for the same brand:
- Identify shared elements (common desires, voice patterns)
- Identify conflicting elements (different beliefs, different tones)
- Recommend: unified brand + segment-specific messaging, or sub-brands
- Never average avatars — separate what needs separating

### 3. Category Design Mode
When the opportunity exists to create a new category:
- Identify the "category design problem" — what's broken about the current frame?
- Name the new category using avatar language (Section H)
- Design the "legend" and "lightning strikes" (category creation moments)
- Map the POV (point of view) based on avatar beliefs

### 4. Brand Voice Stress Test
Test all messaging against the avatar's belief system:
- Does this angle reinforce enabling beliefs?
- Does it avoid triggering hindering beliefs?
- Does it reframe purchase-blocking beliefs?
- Flag any messaging that contradicts avatar data

### 5. Offer-Validation Check
Before finalizing offers:
- Does each offer solve a specific JTBD?
- Is the pricing anchored in avatar anxieties (cost of inaction)?
- Does the risk reversal address the #1 purchase-blocking belief?
- Does the funnel map match the customer's actual decision journey (Job Map)?

---

## Guardrails

- ❌ No generic brand personality without avatar connection
- ❌ No "creative" positioning that ignores avatar data
- ❌ No offer design without JTBD mapping
- ❌ No voice definition without avatar language patterns
- ❌ No pricing strategy without avatar anxiety/gain framing
- ❌ No brand promise that can't be traced to avatar Section F (Desire)
- ❌ No competing with category kings on their terms — find a different angle
- ❌ No averaging multiple avatars into one brand — separate if needed
- ✅ Every brand decision must reference a specific avatar section
- ✅ Evidence status labels where applicable
- ✅ Explicitly flag assumptions and gaps
- ✅ Brand refinement must show before/after with avatar alignment score

---

## Usage

### Minimum Input
A completed Customer Avatar (Sections A–H minimum, ideally A–K).

### Quality Input
Completed Avatar + existing brand materials + competitor data + customer interview transcripts.

### Process
1. Provide avatar document (file or text)
2. Optionally provide existing brand materials
3. Skill runs through all 6 modules
4. Output: Complete Brand Strategy Document (Markdown)
5. Q&A and refinement

### Output Format
Markdown with YAML frontmatter for structured data + narrative sections.

---

## The One Question This Skill Answers

> "Given who this customer is, what they need, what they believe, and how they talk — what brand would they trust, what would it say, and what should it offer?"
