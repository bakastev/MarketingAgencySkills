# Landing Page & Sales Page Creator

Creates high-converting landing pages and sales pages based on Customer Avatar + Brand Strategy data.

**No generic templates.** Every page is built from avatar evidence, brand voice, and conversion science with specific benchmarks.

---

## Core Principles

1. **Avatar first, always** — Copy, structure, and conversion elements derive from avatar data (Avatar Architect Sections A–H)
2. **Brand voice is law** — Every word must match the brand voice defined in the Brand Architect output
3. **One page, one job** — Ruthless focus. One offer, one CTA, one audience segment per page
4. **Evidence-backed copy** — Use avatar's Voice of Customer (Section H), Pain/Gain (Section E), and Belief System (Section G) as source material
5. **Conversion science applied** — Every structural decision backed by benchmarks and data
6. **Mobile-first** — 82.9% of traffic is mobile. Desktop converts higher, but mobile dominates
7. **System 1 thinking** — Keep visitors in fast, emotional, instinctive mode. No cognitive friction

---

## Dependencies

**Required Input:**
- Customer Avatar (minimum Sections A–H from Avatar Architect)
  - Context Profile (Section B)
  - JTBD Core (Section C)
  - Pain/Gain/Anxiety (Section E)
  - Desire & Identity (Section F)
  - Belief System (Section G)
  - Voice of Customer (Section H)
- Brand Strategy (minimum from Brand Architect)
  - Positioning Statement
  - Brand Voice Guidelines
  - Offer Architecture
  - Messaging Hierarchy

**Optional Input:**
- Existing landing page (URL or copy for refinement)
- Competitor landing pages
- Specific product/service details
- Pricing information
- Testimonials or case studies
- Brand assets (colors, fonts, logo)

**Output feeds into:**
- Frontend Development (HTML/CSS/Next.js)
- Video Pipeline (Remotion)
- Ads (hook copy, angle extraction)
- Email Campaigns (nurture sequences)

---

## Conversion Benchmarks (2026 Data)

Reference these when making structural decisions. Source: NotebookLM Research Notebook "Landing Page Conversion Statistics and B2B ROI Calculator Strategies".

| Metric | Benchmark | Source |
|---|---|---|
| Median landing page conversion rate | **6.6%** | Involve.me 2026 |
| Average landing page conversion | **4–5%** | Involve.me 2026 |
| Top 10% conversion rate | **11.45%+** | Involve.me 2026 |
| B2B conversion rate | **1.8–2%** | Martal Group 2026 |
| Email traffic conversion | **19.3%** | Unbounce 2026 |
| Paid social conversion | **12.0%** | Unbounce 2026 |
| Paid search conversion | **10.9%** | Unbounce 2026 |
| Mobile traffic share | **82.9%** | Backlinko 2026 |
| Desktop conversion rate | **4.8–5.06%** | Multiple 2026 |
| Mobile conversion rate | **1.6–2.9%** | Multiple 2026 |
| Page load +1s impact | **-7% conversions** | Backlinko 2026 |
| Mobile 3s+ abandonment | **50%+** | Backlinko 2026 |
| Form 11→4 fields | **+120% conversions** | Involve.me 2026 |
| Single CTA vs 5+ links | **13.5% vs 10.5%** | Backlinko 2026 |
| Video explainer lift | **up to 86%** | Unbounce 2026 |
| B2B lead follow-up <5min | **2-3x conversion** | Martal Group 2026 |
| Interactive calculator lift | **40-60% over static** | Prezentor 2026 |
| 5th-7th grade copy conversion | **11.1%** | Addicted2Success 2026 |
| Complex copy conversion | **5.3%** | Addicted2Success 2026 |
| "Get/Unlock" vs "Buy/Submit" | **+3%** | Convertcart 2026 |
| Verified social proof lift | **up to 8x B2B** | UserEvidence 2026 |

---

## Page Types

This skill supports these page types. Each has different structure, copy approach, and conversion targets:

| Type | Purpose | Conversion Target | Key Section |
|---|---|---|---|
| **Squeeze Page** | Email capture, lead magnet delivery | 15–25% | Opt-in form |
| **Sales Page (Long-form)** | High-ticket offer, course, coaching | 3–8% | Full funnel |
| **Product Landing Page** | SaaS product, tool, service | 5–12% | Demo/CTA |
| **B2B Lead Gen** | Demo request, consultation booking | 2–5% | Form + ROI calc |
| **Webinar/VSL Registration** | Funnel entry for video sales | 20–40% | Registration form |
| **ROI Calculator Page** | Interactive lead qualification | 8–15% | Calculator CTA |
| **Agency Service Page** | Service description + booking | 3–7% | CTA + proof |

---

## Research Tools

| Tool | Best For | Access |
|---|---|---|
| **Firecrawl** (MCP) | Competitor landing page scraping, copy analysis | MCP Server |
| **Perplexity** (web_search) | Market benchmarks, category landing page trends | Native |
| **Reddit** (Composio) | Customer language, objections, desires | Composio |
| **NotebookLM** (CLI) | Deep research synthesis, multi-source analysis | CLI |
| **Web Fetch** | Quick competitor page extraction | Native |

---

## Workflow (6 Modules)

### Module 0: Landing Page Research (Automatic)

**Task:** Analyze competitor landing pages, category best practices, and current trends BEFORE writing a single word.

**This module runs automatically.** It ensures the page is built on real market data, not assumptions.

**Research Targets:**
1. **Top 3-5 Competitor Landing Pages** — Scrape structure, copy, CTAs, proof elements, offer presentation (Firecrawl)
2. **Category Conversion Benchmarks** — What's the average conversion rate for this type of page in this industry? (Perplexity)
3. **Winning Copy Patterns** — What headlines, hooks, and frameworks are working in this space? (Firecrawl + Perplexity)
4. **Customer Language for This Offer** — What words does the avatar use when searching for this solution? (Reddit + Perplexity)
5. **Trust Signals & Proof Standards** — What social proof, certifications, and authority signals does this category expect? (Competitor analysis)

**Research Process:**
1. **Extract search queries from avatar:**
   - Core JTBD (what job are they hiring this page for?)
   - Primary pain points (what are they trying to escape?)
   - Desired outcome (what transformation do they want?)
   - Belief blockers (what would stop them from converting?)
2. **Execute competitor analysis:**
   - Scrape top 3-5 competitor landing pages
   - Map their structure (sections, CTAs, proof elements)
   - Analyze their copy (headlines, hooks, objection handling)
   - Note their pricing and offer presentation
3. **Identify category patterns:**
   - Common section types (hero, features, proof, FAQ, CTA)
   - Typical page length (short vs long-form)
   - Standard proof elements (logos, testimonials, case studies)
   - Industry-specific trust signals (certifications, compliance)
4. **Output research brief:**

```yaml
competitor_pages:
  - url: string
    structure: [section list]
    hero_headline: string
    cta_copy: string
    proof_elements: [list]
    conversion_elements: [list]
    strengths: [list]
    weaknesses: [list]
category_benchmarks:
  avg_conversion_rate: string
  typical_page_length: short | medium | long
  expected_proof_types: [list]
  pricing_transparency: high | medium | low
copy_patterns:
  winning_headlines: [list]
  common_hooks: [list]
  objection_handling_approaches: [list]
  cta_language_patterns: [list]
trust_signal_standards:
  required: [list]
  nice_to_have: [list]
  overkill: [list]
```

**Quality Gate:**
- Minimum 3 competitor pages analyzed
- At least 1 conversion benchmark identified
- Category-specific copy patterns documented

---

### Module 1: Page Strategy & Architecture

**Task:** Define the page type, conversion goal, audience segment, and section architecture.

**Steps:**

**1A. Page Type Selection**
Based on the client's goal and avatar data:
- Lead gen → B2B Lead Gen or Squeeze Page
- Product sale → Product Landing Page or Sales Page
- Service booking → Agency Service Page
- Webinar funnel → Webinar/VSL Registration
- Lead qualification → ROI Calculator Page

**1B. Conversion Goal Definition**
```yaml
page_strategy:
  type: [page type from above]
  primary_goal: [specific conversion action]
  target_conversion_rate: [based on benchmarks]
  audience_segment: [specific segment from avatar Section I]
  traffic_source: [where will visitors come from?]
  budget_tier: low | medium | high
  funnel_position: top | middle | bottom
```

**1C. Section Architecture**
Build the page section-by-section based on the psychological conversion flow:

```
ATTENTION → INTEREST → DESIRE → TRUST → ACTION
   ↓           ↓           ↓          ↓         ↓
  Hero      Problem     Solution    Proof     CTA
  Hook      Agitation   Benefits    Case      Close
                                  Testim.
                                  FAQ
```

**Section Decision Matrix:**

| Section | When to Include | When to Skip |
|---|---|---|
| Hero + Headline | Always | Never |
| Problem/Agitation | When pain is primary driver | Pleasure-driven offers |
| Social Proof Bar | Always (logos, numbers) | Never |
| Benefits (not features) | Always | Never |
| How It Works | Complex products/services | Simple, obvious products |
| Before/After | Transformation-driven offers | Utility products |
| Case Study/Testimonials | Always (minimum 2-3) | Never |
| FAQ | When objections are common | Simple, low-friction offers |
| ROI Calculator | B2B, SaaS, services | B2C impulse buys |
| Comparison Table | Competitive markets | Blue ocean / unique offer |
| Guarantee/Risk Reversal | Always (even implicit) | Never |
| Urgency/Scarcity | When ethically available | Evergreen pages |
| Final CTA | Always | Never |

**1D. Mobile vs Desktop Strategy**
- Mobile: Simplified layout, sticky CTA, minimal form fields, above-the-fold value prop
- Desktop: More detail, side-by-side comparisons, multi-column layouts

**Output:** Complete section plan with rationale for each decision.

---

### Module 2: Copywriting — Headline & Hook

**Task:** Write the hero section — the most important 5 seconds of the page.

**The Headline Formula Stack:**

Based on avatar's JTBD (Section C), Pain (Section E), and Desire (Section F):

```
[Desired Outcome] + [Timeframe/Specificity] + [Mechanism/Uniqueness]
```

**Headline Archetypes (choose based on avatar and brand voice):**

| Archetype | Template | Best For |
|---|---|---|
| **Benefit-Driven** | [Achieve X] without [Pain Y] | Pain-avoidance avatars |
| **Transformation** | From [Before State] to [After State] | Aspirational avatars |
| **Specificity** | How to [Result] in [Timeframe] using [Method] | Expert-seeking avatars |
| **Social Proof** | Join [N] [Avatar Type] who [Achievement] | Belonging-driven avatars |
| **Contrarian** | Everything you know about [Topic] is wrong | Sophisticated avatars |
| **Question** | [Pain Question]? Here's [Solution] | Awareness-stage avatars |
| **Direct** | [Product] for [Avatar] who want [Outcome] | Bottom-funnel avatars |

**Subheadline Rules:**
- Amplifies the headline, doesn't repeat it
- Adds specificity (numbers, timeframes, details)
- Uses avatar's language patterns from Section H (VoC)
- Written at 5th–7th grade reading level

**CTA Button Copy (System 1 Language):**

| ❌ System 2 (Avoid) | ✅ System 1 (Use) |
|---|---|
| Submit | Get Instant Access |
| Buy Now | Unlock [Outcome] |
| Sign Up | Start Free |
| Download | Get Your Free [Thing] |
| Contact Us | See How It Works |
| Learn More | Discover [Benefit] |

**Micro-copy below CTA:**
- Risk reversal: "No credit card required" / "Free for 14 days" / "Cancel anytime"
- Trust signal: "Join 2,000+ [avatar type]" / "Used by [brand names]"
- Specificity: "Get your personalized [thing] in 2 minutes"

**Output:**
```yaml
hero:
  headline: string (with 2-3 variants)
  subheadline: string
  cta_primary: string
  cta_micro_copy: string
  headline_archetype: string
  avatar_evidence_links: [which avatar sections this draws from]
  readability_grade: number
```

---

### Module 3: Copywriting — Body Sections

**Task:** Write all body sections using avatar evidence and brand voice.

**Section 3A: Problem/Agitation**
- Source: Avatar Section E (Pain/Gain/Anxiety)
- Mirror the avatar's own words (Section H — VoC)
- Use "blind-but-verified" social proof pattern
- Specificity > generality ("Losing 3 hours per week on..." not "Inefficient processes")
- 2-3 pain points maximum (more dilutes focus)
- End with transition to solution

**Section 3B: Solution/Benefits**
- Source: Avatar Section C (JTBD), Section F (Desire & Identity)
- Benefits, NOT features. Every feature must connect to a benefit, every benefit to a desire
- Use the Brand Ladder: Feature → Benefit → Emotional Benefit → Identity
- Match avatar's aspiration language
- Maximum 5-7 benefits (cognitive overload beyond that)

**Section 3C: How It Works**
- 3-5 steps maximum
- Each step: short label + one-sentence description
- Visual progression (numbered, timeline, or process graphic)
- Reduce perceived complexity and risk
- Source: Avatar Section C (Job Map)

**Section 3D: Social Proof**
- **Logos/Numbers Bar:** "Trusted by X+ [avatar type]" — place above the fold
- **Testimonials:** 2-3 minimum, each following this structure:
  ```
  [Specific Result] — [Name], [Role/Company], [Timeframe]
  ```
  - Use avatar's language patterns (Section H)
  - Specific numbers over vague praise
  - "Blind-but-verified" pattern when named quotes aren't available
- **Case Studies:** 1-2 if available, structured as Before → Process → After
- **Data Points:** Internal metrics, user counts, success rates
- Source: Avatar Section H (VoC), Section E (validated gains)

**Section 3E: Objection Handling (FAQ)**
- Source: Avatar Section E (Anxiety), Section G (Belief System)
- Maximum 6-8 questions
- Order: most common/frequent objection first
- Each answer should:
  1. Acknowledge the concern (validate, don't dismiss)
  2. Reframe using avatar's belief system (Section G)
  3. Provide evidence or guarantee
- Use collapsible/accordion format for mobile

**Section 3F: ROI/Value Section (B2B specific)**
- Source: Avatar Section E (Gains), Section J (Strategic Implications)
- **Interactive Calculator Approach:**
  - 3-5 input fields maximum (progressive disclosure)
  - Input questions map to avatar's key metrics
  - Output shows: Current Cost → With Solution → Savings/ROI
  - Pre-fills with industry defaults to reduce friction
- **Static ROI Display:**
  - "Companies using [solution] save on average [X] per [period]"
  - Specific, credible numbers only
  - Third-party validation preferred
- Interactive calculators convert **40-60%** better than static content

**Section 3G: Comparison Table (if competitive market)**
- Compare on features that matter to THIS avatar (not feature count)
- 3 columns maximum: You vs Top Competitor vs "DIY / Status Quo"
- Checkmarks for parity, ✕ for gaps, ✓ highlighted for your advantages
- Source: Avatar Section J (Positioning), Brand Architect competitor analysis

**Section 3H: Guarantee/Risk Reversal**
- Always include — even if implicit
- Types by offer:
  - SaaS: Free trial, money-back guarantee
  - Service: Satisfaction guarantee, first session free
  - Product: Return policy, warranty
  - High-ticket: Specific outcome guarantee
- Frame using avatar's primary anxiety (Section E)
- Specific > vague ("30-day full refund" > "Satisfaction guaranteed")

**Section 3I: Final CTA**
- Mirror the hero CTA with added urgency/context
- Summarize the key value proposition in 1 line
- Re-state the guarantee
- Last micro-copy: urgency (if applicable) or restatement of primary benefit

**Copywriting Rules:**
- **Reading level:** 5th–7th grade (11.1% conversion vs 5.3% for complex text)
- **Sentence length:** Max 15-20 words average
- **Paragraph length:** Max 3-4 sentences
- **System 1 triggers:** Use "Get/Unlock/Discover/Guaranteed/Secure" not "Buy/Cost/Submit"
- **Loss aversion:** Frame around what they lose by NOT acting
- **Cognitive fluency:** Simple words, short sentences, clear hierarchy
- **Voice consistency:** Every section must match Brand Architect voice guidelines

**Output:** Complete copy for all sections, with avatar evidence citations.

---

### Module 4: Conversion Optimization

**Task:** Apply conversion science to every element of the page.

**4A. Form Design**
- Maximum 4 fields for initial conversion (name + email + 1-2 qualifying)
- Use progressive profiling for deeper data collection
- Label text should be conversational, not clinical
  - ❌ "Email Address" → ✅ "Where should we send your results?"
- Place CTA above the fold AND at bottom of page
- Form validation: real-time, inline, encouraging

**4B. Visual Hierarchy**
- F-Pattern for content-heavy pages
- Z-Pattern for simple/visual pages
- One dominant visual element per section
- Whitespace is not wasted space — it guides the eye
- CTA buttons: high contrast, minimum 44px tap target, single color

**4C. Speed & Performance**
- Page load under 3 seconds (50%+ mobile abandonment above 3s)
- Lazy-load images below the fold
- Minimize third-party scripts
- Optimize images (WebP, responsive sizes)

**4D. Mobile Optimization**
- Sticky header with CTA on scroll
- Collapsible sections for FAQ and details
- Phone number clickable
- Form fields large enough for thumb interaction
- Test on 375px width minimum

**4E. Trust Architecture**
- **Above the fold:** Logo bar, key metric, security badge
- **Mid-page:** Testimonials, case study, certifications
- **At CTA:** Guarantee, privacy statement, payment trust badges
- **Throughout:** Consistent brand presence, professional design

**4F. Urgency & Scarcity (Ethical Only)**
- Use real deadlines, not fake countdowns
- "Cohort starts [date]" > "Offer expires soon"
- Limited availability when genuinely limited
- Never fabricate scarcity

**Output:**
```yaml
conversion_optimization:
  form_fields: [list with labels and types]
  visual_hierarchy: string (F-pattern | Z-pattern | hybrid)
  mobile_strategy: string
  trust_elements:
    above_fold: [list]
    mid_page: [list]
    at_cta: [list]
  urgency_elements: [list or "none"]
  performance_targets:
    page_load_max: "3s"
    largest_contentful_paint: "2.5s"
    cumulative_layout_shift: "0.1"
```

---

### Module 5: Output Assembly & Quality Check

**Task:** Assemble the complete landing page document and validate against benchmarks.

**5A. Assemble Complete Page Document**

Structure the output as a complete, implementable page document:

```yaml
# === LANDING PAGE DOCUMENT ===
page_meta:
  title: string (SEO title, max 60 chars)
  meta_description: string (max 155 chars)
  url_slug: string
  page_type: string
  target_conversion_rate: string
  funnel_position: string
  traffic_source: string

# === SECTIONS ===
sections:
  - id: hero
    type: hero
    headline: string
    subheadline: string
    cta_text: string
    cta_url: string
    cta_micro_copy: string
    background_image: string (optional)
    avatar_evidence: [citations]

  - id: social_proof_bar
    type: proof_bar
    headline: "Trusted by X+ [avatar type]"
    logos: [list]
    metric_highlights: [list]

  - id: problem
    type: problem_agitation
    headline: string
    pain_points:
      - description: string
        avatar_evidence: [citations]
    transition_to_solution: string

  - id: solution
    type: benefits
    headline: string
    benefits:
      - benefit: string
        supporting_detail: string
        avatar_evidence: [citations]

  - id: how_it_works
    type: process
    headline: string
    steps:
      - step_number: 1
        title: string
        description: string

  - id: proof
    type: testimonials
    headline: string
    testimonials:
      - quote: string
        attribution: string
        metric: string (optional)
        avatar_evidence: [citations]
    case_studies: [list]

  - id: comparison (optional)
    type: comparison_table
    headline: string
    columns: [list]
    rows: [list]

  - id: faq
    type: faq
    headline: string
    questions:
      - question: string
        answer: string
        avatar_evidence: [citations]

  - id: guarantee
    type: guarantee
    headline: string
    description: string
    type: money_back | free_trial | satisfaction | outcome

  - id: final_cta
    type: cta
    headline: string
    cta_text: string
    cta_url: string
    guarantee_reminder: string
    urgency: string (optional)

# === CONVERSION OPTIMIZATION ===
conversion:
  form:
    fields: [list]
    progressive_profiling: bool
  trust_elements: [list]
  urgency_elements: [list]
  mobile_specific: [list]

# === SEO ===
seo:
  title_tag: string
  meta_description: string
  h1: string
  schema_markup: [FAQ | Product | Service]
  canonical_url: string

# === EVIDENCE TRACE ===
avatar_sections_used: [A, B, C, E, F, G, H]
brand_elements_used: [positioning, voice, offer, messaging]
research_sources: [list of URLs and tools used]
```

**5B. Quality Checklist**

Before delivering, verify every item:

**Avatar Alignment:**
- [ ] Headline addresses avatar's core job or desire
- [ ] Pain points match avatar's documented pains (Section E)
- [ ] Benefits connect to avatar's desired outcomes (Section F)
- [ ] Copy uses avatar's language patterns (Section H)
- [ ] FAQ addresses avatar's actual objections/beliefs (Section G)
- [ ] Social proof resonates with avatar's identity aspiration

**Conversion Science:**
- [ ] Single primary CTA throughout the page
- [ ] Form has ≤4 fields
- [ ] CTA uses System 1 language
- [ ] Copy is at 5th–7th grade reading level
- [ ] Page has social proof above the fold
- [ ] Risk reversal element included
- [ ] Mobile-optimized structure
- [ ] No outbound navigation links (attention ratio = 1:1)

**Brand Consistency:**
- [ ] Voice matches brand voice guidelines
- [ ] Positioning statement reflected in hero
- [ ] Offer architecture aligns with brand offer
- [ ] Visual hierarchy matches brand aesthetic
- [ ] No competitor's language accidentally adopted

**Technical:**
- [ ] SEO title ≤60 chars
- [ ] Meta description ≤155 chars
- [ ] Schema markup defined
- [ ] Page load target <3s considered
- [ ] CTA buttons meet 44px minimum tap target

---

## Pipeline Integration

### Upstream (What This Skill Needs)
1. **Customer Onboarding Agent** (`growing-brands-onboarding`)
   - Raw client data, voice recordings, call notes
2. **Customer Avatar Architect** (`growing-brands-avatar-architect`)
   - Validated avatar (Sections A–H)
   - JTBD, Pain/Gain, Belief System, VoC
3. **Brand Architect** (`brand-architect`)
   - Positioning, Voice, Offer, Messaging Hierarchy

### Downstream (What This Skill Feeds)
1. **Frontend Implementation** — Next.js / HTML/CSS
2. **Video Pipeline** — Remotion (hero section video, social proof clips)
3. **Ads** — Extract hooks and angles for paid campaigns
4. **Email Nurture** — Follow-up sequences for non-converters
5. **Analytics** — Conversion tracking, A/B test hypotheses

### Standalone Mode
If no avatar/brand data exists, the skill can operate in **research-first mode**:
1. Conduct Module 0 research with available client information
2. Create a lightweight avatar sketch based on research
3. Build the page with noted assumptions
4. Flag all assumptions for later validation

---

## Quick Reference: Avatar → Landing Page Mapping

| Avatar Section | Landing Page Section |
|---|---|
| A — Executive Snapshot | Overall page direction and priority |
| B — Context Profile | Hero targeting, traffic source alignment |
| C — JTBD Core | Solution section, How It Works |
| D — Job Map | Benefits ordering, feature prioritization |
| E — Pain/Gain/Anxiety | Problem section, FAQ, Guarantee |
| F — Desire & Identity | Headline angle, Benefit framing |
| G — Belief System | Objection handling, FAQ, Trust signals |
| H — Voice of Customer | ALL copy — language, phrases, quotes |
| I — Segmentation | Page variant strategy (if multi-segment) |
| J — Strategic Implications | Comparison table, competitive positioning |

---

## Output Formats

The skill produces:

1. **Complete Page Document** — YAML/Markdown with all sections, copy, and conversion elements
2. **Implementation Brief** — Technical notes for frontend development
3. **A/B Test Hypotheses** — 3-5 test ideas based on uncertainty areas
4. **Evidence Trace** — Links every copy element back to avatar data or research

All outputs are stored in the client's workspace:
```
growing-brands/landing-pages/{client-name}/{page-name}/
  ├── page-document.yaml      # Complete page spec
  ├── implementation-brief.md  # Frontend notes
  ├── ab-test-hypotheses.md    # Testing roadmap
  └── evidence-trace.yaml      # Source citations
```
