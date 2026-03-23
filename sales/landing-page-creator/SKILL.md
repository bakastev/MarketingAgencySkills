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
  - **⚠️ Service Inventory** (from Brand Diagnosis Module 1)

---

### ⚠️ Pre-Build Completeness Gate (MANDATORY — run BEFORE writing any copy!)

**Before starting Module 1, verify:**

```yaml
completeness_gate:
  avatar_complete:
    sections_a_through_h_present: yes/no  # If no → STOP
    section_i_segmentation_present: yes/no  # If no → FLAG for multi-segment
    section_j_strategic_present: yes/no  # If no → FLAG for offer design
  brand_complete:
    positioning_statement_present: yes/no  # If no → STOP
    service_inventory_present: yes/no  # If no → STOP (ask coordinator)
    offer_architecture_present: yes/no  # If no → STOP
    all_services_in_offers: yes/no  # Cross-check: every service from inventory appears in at least one offer tier
  capability_check:
    list_all_client_services: [string]  # Extract from brand identity or client brief
    each_service_has_section: yes/no  # Each service must have a Benefit card, mention in Capabilities, representation in Comparison, and FAQ coverage
```

**If ANY mandatory item is missing → STOP and request from coordinator.**
Do NOT proceed with incomplete inputs. Building a landing page without a complete Service Inventory creates missing capabilities in the final output.

### Common Completeness Failures (LEARN FROM THESE):
- ❌ Brand Identity lists "Google Ads" as traffic channel but NOT as service → Landing Page won't mention Ads
- ❌ Avatar only covers tourism segment but brand targets 6 segments → Landing Page will be tourism-only
- ❌ Service Inventory exists in Brand Diagnosis but Offer Architecture doesn't include all services → some capabilities vanish from the page

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

---

---

## HIGH-TICKET DESIGN GOLDSTANDARD 2026

> **Design ist kein ästhetisches Nice-to-have.** Bei High-Ticket-Dienstleistungen (5–6stellige Investitionen) fungiert UX als primärer Filter für wahrgenommene Kompetenz und Seriosität. Diese Sektion definiert evidenzbasierte Design-Vorgaben für konvertierende High-Ticket-Pages.
>
> **Quelle:** Research-Bericht mit 56 Quellen (Nielsen Norman Group 2024, Google Core Web Vitals, UX-Conversion-Studien).
> **Design = "Margin Protector" und "Financial Instrument". Exzellentes Design = letzte Bastion der menschlichen Differenzierung.**

---

### 1. Design Philosophy

#### 1.1 Cognitive Load Theory

Das menschliche Arbeitsgedächtnis kann nur eine begrenzte Menge gleichzeitig verarbeiten. Jedes überflüssige Element — Farben, Schriftarten, blinkende Animationen, konkurrierende CTAs — erhöht kognitive Last und führt zu Entscheidungsmüdigkeit und Abbruch.

**Minimalistische Layouts sind 2026 eine neurologische Notwendigkeit, kein Trend.**

**Benchmarks (Nielsen Norman Group 2024 u.a.):**

| Metrik | Benchmark | Quelle |
|--------|-----------|--------|
| Aufgabenabschlussrate | **+30%** bei reduzierter Komplexität | NNGroup 2024 |
| Konversionsrate | **+13%** bei einem einzigen primären CTA | Backlinko 2026 |
| Abbruchrate Formulare | **-18%** durch Vereinfachung | Involve.me 2026 |
| Markenvertrauen | **75%** der Nutzer urteilen basierend auf Design | Stanford Web Credibility |
| Ladezeit-Konversionsverlust | **-7% pro Sekunde** Verzögerung | Backlinko 2026 |

**Regel:** Führe den Nutzer durch den "Messy Middle" (Exploration + Evaluation überlappen) mit klarer Hierarchie, nicht mit Reizüberflutung.

#### 1.2 Bold Minimalism ("Minimalism with Muscle")

Der Goldstandard 2026 ist eine Hybridlösung: **Bold Minimalism** — radikale Reduktion bei selbstbewusster Präsenz.

**Drei Stil-Richtungen für High-Ticket:**

| Stil | Signalwirkung | Geeignet für | Frameworks |
|------|---------------|--------------|------------|
| **Monochrome (Zinc/Slate)** | Technologische Reife, Stabilität, Konzentration auf Ergebnis | Strategische Beratung, Software-Agenturen, Finanzdienstleistungen, DFY-Services | shadcn/ui, Tailwind CSS |
| **Bold Minimalism** | Selbstbewusstsein, Modernität, klare Kante | Kreativagenturen, High-End Coaching, innovative DFY-Services | Tailwind CSS, Framer Motion |
| **Immersive (3D/AR)** | Faszination, Greifbarkeit, Innovation | E-Commerce, Luxusgüter, Erlebnismarketing | Three.js, Spline |

> ⚠️ **Immersive 3D/AR bei DFY-Dienstleistungen KONTRAPRODUKTIV** — wenn als Ablenkung von fehlender Substanz wahrgenommen. Nur einsetzen wenn 3D das Angebot ERGÄNZT, nicht ersetzt.

**WOW-Faktor als Delight Factor (nicht als Ablenkung):**
- Mikro-Interaktionen: flüssige Hover-Übergänge, dezente Fortschrittsanzeigen
- Nutzer fühlt Kontrolle und Fortschritt — NICHT "entertainment"
- Einsatz als "Polishing", nicht als Feature

#### 1.3 Anti-AI-Fluff Stance

Digitale Fatigue durch massenhaft produzierte, seelenlose KI-Inhalte ist real. Nutzer entwickeln instinktive Abneigung gegen "zu perfekte" KI-Bilder und generische Texte.

**Soul Gap:** Kampagnen mit standardisierter KI-Generierung erzeugen keine emotionale Resonanz.

**Lösungsansätze:**
1. **Candid Photography** — Ungestellte, fast unvollkommene Bilder konvertieren besser als Stockfotos/AI-Bilder
2. **Textur und Haptik** — Digitales Filmkorn, Papierstrukturen, JPEG Artifacting als bewusstes Gestaltungselement
3. **High-Fidelity AI Cinematography** — KI für "unmögliche Welten" als künstlerisches Statement, NICHT als billige Abkürzung

---

### 2. Visual System

#### 2.1 Farbpalette: Zinc/Slate (Monochrome Goldstandard)

Für High-Ticket-Dienstleistungen ist eine monochrome Zinc/Slate-Palette der Goldstandard 2026. Signalisiert technologische Reife, Stabilität und Konzentration auf Ergebnis.

**Tailwind CSS Zinc/Slate Palette:**

```css
/* Primär — Hintergrund */
--bg-primary:     theme('colors.zinc.950');   /* #09090b — Hauptschirm, Hero */
--bg-secondary:   theme('colors.zinc.900');   /* #18181b — Cards, Sections */
--bg-tertiary:    theme('colors.zinc.800');   /* #27272a — Hover-States, Borders */
--bg-elevated:    theme('colors.zinc.50');    /* #fafafa — Light Cards (Alternierend) */

/* Text */
--text-primary:   theme('colors.zinc.50');    /* #fafafa — H1, H2 auf Dark BG */
--text-secondary: theme('colors.zinc.400');   /* #a1a1aa — Body-Text auf Dark BG */
--text-muted:     theme('colors.zinc.500');   /* #71717a — Captions, Labels */

/* Akzent (einziges Farbsignal!) */
--accent-primary: theme('colors.teal.500');   /* #14b8a6 — CTAs, Links, Highlights */
--accent-hover:   theme('colors.teal.400');   /* #2dd4bf — Hover-Stand */

/* Social Proof / Trust */
--success:        theme('colors.emerald.500'); /* #10b981 — Positive Metriken */
--warning:        theme('colors.amber.500');   /* #f59e0b — Caveats */

/* Border & Divider */
--border:         theme('colors.zinc.800');   /* #27272a — Subtile Trennlinien */
--border-focus:   theme('colors.zinc.700');   /* #3f3f46 — Input-Fokus */
```

**Regeln:**
- **MAXIMAL 1 Akzentfarbe** auf der gesamten Page (z.B. Teal für CTAs)
- Zinc/Slate für 90% der Fläche
- Weißraum (Zinc-50 oder weiß) als strategisches Gestaltungselement — nicht als "leerer Raum"

#### 2.2 Typografie-System

Typografie ist der "stille Motor der Markenautorität". 2026 erleben wir eine Renaissance der Serifenschriften — Historie, Eleganz und Tradition erzeugen Vertrauen. Variable Fonts bieten Performance + visuelle Konsistenz.

**Font-Trends 2026:**

| Typ | Charakteristik | Einsatz |
|-----|----------------|---------|
| **Elegante Serifen** (Verona, Manierlich) | Raffiniert, "teuer" | Luxus, Consulting, Editorial |
| **Wide Sans-Serif** (Triumph Wide) | Geometrisch, massiv | Tech-Startups, Architektur |
| **Variable Fonts** | Flexibel, performant | Responsive UI/UX |
| **Retro Serif** | Nostalgisch, charaktervoll | Lifestyle, Personal Branding |

**Growing Brands Empfehlung (AI-first Agency):**

```css
/* Typografie-Hierarchie */
--font-display: 'Inter Tight', 'Space Grotesk', system-ui;  /* Wide Sans-Serif für H1-H3 */
--font-body:    'Inter', system-ui;                            /* Clean Sans-Serif für Body */
--font-accent:  'Playfair Display', Georgia, serif;           /* Serif für Quotes, Accents */
--font-mono:    'JetBrains Mono', monospace;                  /* Code, Daten, Metriken */

/* Größen-Skala (Tailwind + Custom) */
--text-hero:     clamp(2.5rem, 5vw, 4.5rem);    /* H1 — 40–72px responsive */
--text-section:  clamp(1.75rem, 3vw, 3rem);     /* H2 — 28–48px */
--text-card:     clamp(1.25rem, 2vw, 1.5rem);   /* H3 — 20–24px */
--text-body:     1rem (16px);                    /* Body — 16px baseline */
--text-small:    0.875rem (14px);                /* Captions, Labels */

/* Gewichte */
--weight-display: 700–800;   /* Headlines — Bold mit Präsenz */
--weight-body:    400;       /* Body — Regular für Lesbarkeit */
--weight-accent:  500;       /* Subheadlines — Medium */

/* Zeilenabstand */
--leading-tight:  1.1;      /* Headlines */
--leading-normal: 1.6;      /* Body */
--leading-loose:  1.8;      /* Lange Absätze */
```

**Regeln:**
- MAXIMAL 2 Font-Familien + 1 Accent-Font
- Variable Fonts bevorzugen (1 HTTP-Request statt 4)
- Body-Text IMMER 16px minimum (nie kleiner auf Mobile)

#### 2.3 Weißraum-Regeln

Weißraum ist kein "leerer Raum" sondern ein strategisches Gestaltungselement das Luxus signalisiert und kognitive Last reduziert.

**Spacing System (basierend auf 8px-Grid):**

```css
/* Tailwind Spacing Tokens */
--space-xs:   0.5rem;   /* 8px — Icons, Inline-Abstände */
--space-sm:   1rem;     /* 16px — Elemente innerhalb einer Card */
--space-md:   1.5rem;   /* 24px — Card-Padding */
--space-lg:   2rem;     /* 32px — Section-Elemente */
--space-xl:   3rem;     /* 48px — Zwischen Sections */
--space-2xl:  4rem;     /* 64px — Major Sections */
--space-3xl:  6rem;     /* 96px — Hero-Bereich */
--space-4xl:  8rem;     /* 128px — Hero-Top-Bottom */

/* Regeln */
section > section { margin-top: var(--space-2xl); }     /* Min 64px zwischen Sections */
.hero          { padding: var(--space-4xl) 0; }          /* 128px Top/Bottom */
.card          { padding: var(--space-md); }              /* 24px intern */
.cta-section   { padding: var(--space-3xl) 0; }          /* 96px */
```

**Prinzip:** Jeder Abschnitt soll "atmen". Wenn ein Abschnitt zu voll wirkt → Element entfernen, nicht Weißraum reduzieren.

---

### 3. Layout Patterns

#### 3.1 Bento Grid (Capabilities/Services)

Der Bento Grid ist das dominante Layout-Pattern 2026 für Service-Darstellungen. Asymmetrische Cards mit variablen Größen erzeugen visuelle Hierarchie ohne Monotonie.

```html
<!-- Tailwind CSS Bento Grid -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6">
  <!-- Hero Card (2 Spalten) -->
  <div class="md:col-span-2 lg:col-span-2 bg-zinc-900 rounded-2xl p-8 md:p-12">
    <h3>AI-Powered Growth Engine</h3>
    <p>Primärer Service mit ausführlicher Beschreibung</p>
  </div>
  <!-- Standard Cards -->
  <div class="bg-zinc-900 rounded-2xl p-8">
    <h3>Google Ads</h3>
    <p>Service-Kurzbeschreibung</p>
  </div>
  <div class="bg-zinc-900 rounded-2xl p-8">
    <h3>Meta Ads</h3>
    <p>Service-Kurzbeschreibung</p>
  </div>
  <!-- Wide Card (2 Spalten) -->
  <div class="md:col-span-2 lg:col-span-2 bg-zinc-900 rounded-2xl p-8">
    <h3>AI Agent Development</h3>
    <p>Breiterer Service mit mehr Raum für Erklärung</p>
  </div>
  <div class="bg-zinc-900 rounded-2xl p-8">
    <h3>SEO</h3>
    <p>Service-Kurzbeschreibung</p>
  </div>
</div>
```

**Regeln:**
- MAXIMAL 1 Hero-Card pro Grid (visueller Ankerpunkt)
- Abwechselnde Größen (2:1, 1:1, 1:2) für visuellen Rhythmus
- Jede Card = EIN Service, EIN Icon, EINE KPI
- Cards mit subtilen Hover-Übergängen (`transition-all duration-300 hover:bg-zinc-800`)

#### 3.2 F-Pattern für Content-Heavy Pages

Für Long-Form Sales Pages und B2B Lead Gen Pages:

```
┌─────────────────────────────────┐
│  H1 Headline (linksbündig)     │  ← Eye starts top-left
│  Subheadline                    │
│  [CTA Button]                   │
├─────────────────────────────────┤
│  ┌──────────┐ ┌──────────────┐ │
│  │ Sidebar  │ │ Primary Copy │ │  ← Vertical scanning
│  │ Nav/     │ │               │
│  │ Proof    │ │               │
│  │          │ │               │
│  └──────────┘ └──────────────┘ │
├─────────────────────────────────┤
│  Social Proof | Testimonials    │  ← Horizontal scan
│  ┌─────┐ ┌─────┐ ┌─────┐      │
│  │  1  │ │  2  │ │  3  │      │
│  └─────┘ └─────┘ └─────┘      │
├─────────────────────────────────┤
│  [Final CTA — Full Width]      │
└─────────────────────────────────┘
```

**Regeln:**
- H1 IMMER linksbündig bei F-Pattern (zentriert = Z-Pattern)
- Primärer Content-Block links (60-70% Breite auf Desktop)
- Social Proof IMMER unterhalb des "fold" in horizontaler Anordnung

#### 3.3 Social Proof Placement

**Placement-Strategie basierend auf Trust-Timing:**

| Position | Element | Zweck |
|----------|---------|-------|
| **Hero (oben)** | Logo-Bar + eine Kernmetrik | Sofortige Glaubwürdigkeit vor Scrollen |
| **Nach Problem** | "X Unternehmen haben dasselbe Problem gelöst" | Empathie + Machbarkeit |
| **Nach Benefits** | Testimonial mit spezifischer Zahl | Glaubhaftmachung der Claims |
| **Vor CTA** | Case Study mit messbarem Impact | Letzter Vertrauensschub vor Konversion |
| **Bei Final CTA** | Garantie + Anzahl zufriedener Kunden | Risikominimierung |

#### 3.4 CTA-Hierarchie

```
Primary CTA:   Hoher Kontrast auf Zinc-Background (z.B. Teal-500 Button)
               → "Start Your Growth Strategy" oder "Book Discovery Call"

Secondary CTA: Ghost-Button (Border-only, kein Fill)
               → "View Case Study" oder "Download Benchmark"

Tertiary:      Text-Link mit Akzentfarbe
               → "Learn more about our approach"
```

**Regeln:**
- MAXIMAL 1 Primary CTA pro Viewport (keine konkurrierenden CTAs)
- CTA-Button MINIMUM 48px Höhe auf Mobile (44px absolute Minimum)
- Micro-Copy unter jedem CTA (Risk Reversal: "Free consultation · No commitment")

---

### 4. Anti-AI-Fluff Guidelines

#### 4.1 Candid Photography

**Regel:** Echte, ungestellte Bilder konvertieren besser als perfekte Stockfotos oder KI-generierte Bilder.

**Checkliste für Bildauswahl:**
- ✅ Reale Menschen in realen Umgebungen (Büro, Meeting, Laptop)
- ✅ Leichte Unvollkommenheit — kein "perfektes" Lighting
- ✅ Verschiedene Altersgruppen und Ethnien wenn möglich
- ✅ Bilder die die Avatar-Segment-Situation widerspiegeln
- ❌ Generische "Handshake auf Glas" Stockfotos
- ❌ "Zu perfekte" AI-generierte Gesichter (Uncanny Valley)
- ❌ Hero-Shots die nichts mit dem Angebot zu tun haben
- ❌ Überlagerte Tech-Grafiken auf Menschenbildern

#### 4.2 Texturen als Gestaltungselement

Digital-Organische Texturen vermitteln Echtheit und brechen die "sterile KI-Ästhetik":

```css
/* Subtiles Filmkorn — overlay auf Hero-Bereich */
.hero-texture::after {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,...");
  opacity: 0.03;
  pointer-events: none;
  mix-blend-mode: overlay;
}

/* Papier-Textur für Case Study Cards */
.case-study-card {
  background-image: url('/textures/paper-subtle.webp');
  background-size: cover;
}

/* Bewusstes "Nicht-Perfekt" — dezente JPEG-Artefakte bei Backgrounds */
.grainy-bg {
  filter: contrast(1.05) brightness(1.02);
}
```

**Einsatz:** Nur als subtile Akzente (2-5% Opacity). Die Textur darf NIEMALS Lesbarkeit beeinträchtigen.

#### 4.3 Soul Gap Check

Bevor ein visuelles Element oder Text auf die Page kommt:

1. **Empathy Check** — Würde ein echter Mensch dieses Bild/diesen Text so produzieren?
2. **Specificity Check** — Ist das Ergebnis spezifisch genug um "echt" zu wirken?
3. **Emotion Check** — Erzeugt es eine echte emotionale Reaktion oder nur "nett"?
4. **Differentiation Check** — Könnte das jeder andere Anbieter genauso verwenden?

Wenn >2 Checks fehlen → Element überarbeiten oder entfernen.

---

### 5. Looping Funnel Design

#### 5.1 Post-Linear Funnel Modell

**Klassisch (TOT):** Awareness → Interest → Desire → Action — LINEAR
**2026:** Looping Funnel — High-Ticket-Käufer sind "Investigatoren", springen zwischen Phasen hin-her.

**Konsequenz für Page-Design:**
- Keine strikt-lineare "Story" erzwingen
- Mehrere Entry-Points für verschiedene Phasen (Research, Social Proof, CTA)
- Navigation die Sprünge erlaubt (Anchor-Links, Jump-to-Section)
- "Zurück"-Navigation ohne Page-Reload

#### 5.2 Strategic Nudges statt Lead-Zwang

**Keine aggressiven Pop-ups. Keine Gate-Kräfte vor allem Content.**

| Nudge-Typ | Beschreibung | Placement | Benchmark |
|-----------|-------------|-----------|-----------|
| **Research Nudge** | Ungated Whitepaper, Benchmarks, Checklisten | Nach Problem-Section | Vertrauensaufbau durch eigene Recherche |
| **Social Proof Nudge** | Kontextrelevante Case Studies nahe Entscheidungspunkten | Vor jedem CTA | Spezifischer Impact (nicht generisch) |
| **Personalization Nudge** | Layout + Content in Echtzeit an Verhalten/Herkunft/Branche anpassen | Hero + Benefits | **Engagement +40%** |

**Personalization at Scale Beispiele:**
- Hero-Headline ändert sich basierend auf Traffic-Source (Organic → "Discover..." vs. Paid → "Transform...")
- Industry-Selector im Hero ("I'm in E-Commerce / SaaS / Consulting")
- Dynamische Social Proof basierend auf Visitor-Herkunft

#### 5.3 Page-Struktur für Looping Funnel

```
┌─────────────────────────────────────┐
│  HERO + Primary CTA                 │  ← Entry Point 1 (Action-ready)
├─────────────────────────────────────┤
│  Problem + Research Nudge           │  ← Entry Point 2 (Researchers)
│  [↓ Download Benchmark (Ungated)]   │
├─────────────────────────────────────┤
│  Benefits (Personalized)            │  ← Loop-back möglich
├─────────────────────────────────────┤
│  Case Study + Social Proof Nudge    │  ← Entry Point 3 (Social Proof Seeker)
├─────────────────────────────────────┤
│  How It Works + Process             │  ← Loop-back für Evaluators
├─────────────────────────────────────┤
│  FAQ + Objection Handling           │  ← Entry Point 4 (Skeptiker)
├─────────────────────────────────────┤
│  FINAL CTA + Guarantee              │  ← Alle Loops konvergieren hier
└─────────────────────────────────────┘
```

---

### 6. Case Study Design Standards

**Case Study Goldstandard 2026:**

| Element | Zweck | Erwartung |
|---------|--------|-----------|
| **Problem-Kontext** | Empathie, Identifikation | Realistische Herausforderungen, kein Jargon |
| **Strategischer Prozess** | Denkfähigkeit beweisen | Wireframes, Entscheidungsgründe, Alternativen |
| **Messbarer Impact** | ROI beweisen | Spezifische Daten ("+91% in 8 Monaten") |
| **Multimedia** | Glaubwürdigkeit | Video-Testimonials, interaktive Charts, Vorher-Nachher |

**Case Study Layout Pattern:**

```
┌──────────────────────────────────┐
│  Client Logo + Branche           │
│  ┌──────────┐ ┌──────────────┐  │
│  │ CHALLENGE │ │     RESULT   │  │
│  │ Text      │ │  +91% Leads  │  │
│  │           │ │  in 8 Monaten│  │
│  └──────────┘ └──────────────┘  │
├──────────────────────────────────┤
│  APPROACH (3 Steps)              │
│  ① Analysis → ② Strategy → ③   │
│     Execution                    │
├──────────────────────────────────┤
│  [Video Testimonial oder Quote]  │
│  "Growing Brands hat unsere..."  │
├──────────────────────────────────┤
│  Impact Chart (Vorher → Nachher) │
│  [═════════►═══════════════]    │
└──────────────────────────────────┘
```

**Regeln:**
- IMMER spezifische Zahlen (niemals "deutlich gesteigert")
- Challenge aus Sicht des Clients formulieren (nicht des Agenten)
- Prozess zeigt Denkfähigkeit, nicht nur "wir haben X gemacht"
- Video-Testimonial wenn möglich — konvertiert signifikant besser als Text

---

### 7. Agentic UX Patterns

95% der Kundeninteraktionen sind 2026 KI-gestützt → Die KI-Schnittstelle selbst ist ein Vertrauensfaktor. Landing Pages die KI-Services anbieten MÜSSEN diese Patterns implementieren.

#### 7.1 Intent Preview

Zeige dem Nutzer WAS die KI tun wird VOR der Ausführung.

```
✅ "Ich analysiere jetzt Ihre Website und identifiziere die 5 wichtigsten
    Conversion-Blocker. Das dauert etwa 30 Sekunden."

✅ "Basierend auf Ihrer Branche (SaaS) berechne ich Ihren
    potenziellen ROI mit AI-Powered Lead Generation."
```

**Implementation:**
```html
<div class="bg-zinc-800/50 border border-zinc-700 rounded-lg p-4">
  <div class="flex items-center gap-2 text-zinc-400 text-sm">
    <span class="animate-pulse text-teal-400">●</span>
    <span>Analyzing your website for conversion blockers...</span>
  </div>
  <div class="mt-2 text-zinc-500 text-xs">
    1. Crawling page structure · 2. Checking Core Web Vitals · 3. Identifying CTAs
  </div>
</div>
```

#### 7.2 Explainable Rationale

Begründe WARUM die KI etwas tut oder empfiehlt.

```
✅ "Weil Sie 'B2B SaaS' als Branche angegeben haben, fokussiere ich
    auf Demo-Request-Conversions statt E-Commerce-Patterns."

✅ "Ihr Google Ads Budget von €5.000/Monat lässt 3 Campaign-Kombinationen
    zu. Ich empfehle Variante B wegen..."
```

#### 7.3 Confidence Signals

Zeige die Sicherheit/Konfidenz der KI-Antwort transparent an.

```html
<div class="flex items-center gap-2">
  <div class="h-1.5 flex-1 bg-zinc-800 rounded-full overflow-hidden">
    <div class="h-full bg-teal-500 rounded-full" style="width: 87%"></div>
  </div>
  <span class="text-xs text-zinc-500">87% confidence</span>
</div>

<!-- oder als Badge -->
<span class="inline-flex items-center gap-1 text-xs bg-emerald-500/10 text-emerald-400 px-2 py-1 rounded-full">
  <span class="h-1.5 w-1.5 bg-emerald-400 rounded-full"></span>
  High confidence · Based on 23 data points
</span>
```

**Regeln:**
- Confidence NIE erfinden — muss auf echten Daten/Fallbacks basieren
- Bei Low Confidence → ehrlich kommunizieren: "Ich bin mir hier nicht sicher. Lassen Sie uns das besprechen."
- Agentic Patterns ERGÄNZEN die Page, sie ersetzen nicht die menschliche Komponente

---

### 8. Technical Performance Standards

#### 8.1 Core Web Vitals Targets

| Metrik | Target | Impact wenn verfehlt |
|--------|--------|---------------------|
| **LCP** (Largest Contentful Paint) | **< 2.0s** | Bounce-Rate **-25%** bei Erreichung |
| **FID** (First Input Delay) | **< 100ms** | Interaktionsverzögerung fühlt sich "langsam" an |
| **CLS** (Cumulative Layout Shift) | **< 0.1** | Verschiebende Elemente → Frustration + Abbruch |
| **INP** (Interaction to Next Paint) | **< 200ms** | Ersatz für FID (Chrome 2024+) |
| **TTFB** (Time to First Byte) | **< 800ms** | Server-Response — CDN + Edge essential |

#### 8.2 Accessibility (WCAG 2.2 Level AA)

**Minimum Requirements:**
- Text-Contrast-Verhältnis: **4.5:1** für normalen Text, **3:1** für großen Text
- Tap-Target-Größe: **44x44px** minimum
- Keyboard-Navigation: Alle interaktiven Elemente erreichbar
- Screen-Reader: Alt-Text für alle Images, ARIA-Labels für interaktive Elemente
- Focus-Indikatoren: Sichtbar auf allen interaktiven Elementen

```css
/* Contrast-Sicher (Zinc-Palette auf Dark BG) */
.text-on-dark { color: #fafafa; }     /* Zinc-50 auf Zinc-950 → 19.3:1 ✅ */
.text-muted-dark { color: #a1a1aa; }  /* Zinc-400 auf Zinc-950 → 7.0:1 ✅ */
.caption-dark { color: #71717a; }     /* Zinc-500 on Zinc-950 → 4.6:1 ✅ */

/* Focus-Indikator */
*:focus-visible {
  outline: 2px solid theme('colors.teal.500');
  outline-offset: 2px;
  border-radius: 4px;
}
```

#### 8.3 Mobile Performance

**Mobile-first ist nicht optional (62.5% Marktanteil mobile):**
- Mobile Performance Score: **95%+** (Lighthouse)
- Viewport-Resize: Kein horizontaler Scroll
- Touch-Targets: Minimum **48px** (44px absolute Minimum)
- Font-Sizing: Minimum **16px** body text
- Image-Optimization: Responsive `srcset`, WebP/AVIF, Lazy-Loading
- JavaScript: Minimal Bundle Size (< 100KB initial)

#### 8.4 Security & Transparency

- **HTTPS** zwingend
- **C2PA-Labels** für KI-generierte Inhalte (Transparenz)
- **Cookie-Consent** GDPR-konform
- **Data-Privacy** Statement nahe allen Formularen
- **Third-Party Scripts** auf Minimum reduzieren (Performance + Privacy)

---

### 9. Design Do / Don't Quick Reference

| ✅ DO | ❌ DON'T |
|-------|---------|
| Maximale **1 Akzentfarbe** (Zinc/Slate + 1) | Mehrere Farben, Regenbogen-Paletten |
| **Einziger primärer CTA** pro Viewport | Konkurrierende CTAs nebeneinander |
| **Weißraum als strategisches Element** | Jeden Pixel füllen — "busy" Layouts |
| **Echte Fotos** (candid, ungestellt) | Generische Stockfotos / AI-Bilder mit Uncanny Valley |
| **Wide Sans-Serif** als Display-Font | Mehr als 2 Font-Familien |
| **Variable Fonts** für Performance | Separate Font-Files pro Weight |
| **Bento Grid** für Services | Langweilige 3-Spalten-Grids ohne Hierarchie |
| **F-Pattern** bei Content-Heavy Pages | Zentrierte Text-Wüsten |
| **Strategic Nudges** (ungated Content) | Aggressive Pop-ups / Exit-Intent |
| **Looping Funnel** (sprungfähige Navigation) | Strikt-lineare "Story" erzwingen |
| **Spezifische Metriken** in Case Studies | "Deutlich gesteigert" / "Vielfältige Erfolge" |
| **Agentic UX** (Intent Preview, Confidence) | Schwarze-Kasten-KI ohne Transparenz |
| **LCP < 2.0s** anstreben | Überladene Pages mit 5s+ Ladezeit |
| **WCAG 2.2 Level AA** | Ignorieren von Accessibility |
| **Textur als subtilen Akzent** (2-5% Opacity) | Texturen die Lesbarkeit beeinträchtigen |
| **Micro-Interaktionen** als Delight | Ablenkende Animationen / Autoplay-Videos |
| **Personalization** basierend auf Traffic-Source | One-size-fits-all für alle Segmente |
| **Confidence Signals** bei KI-Features | Fake-Confidence erfinden |

---

### 10. Goldstandard Zusammenfassung

1. **Radikale Reduktion kognitiver Last** durch klare Hierarchien — +30% Aufgabenabschlussrate
2. **Typografie + Weißraum** für Luxus und Autorität — stiller Motor der Markenautorität
3. **Echte Bilder, menschliche Geschichten**, KEINE generischen KI-Muster — Soul Gap vermeiden
4. **Looping Funnel** mit strategischen Nudges statt aggressiver Pop-ups — Engagement +40%
5. **Bold Minimalism** (Monochrome Zinc/Slate) als Default für High-Ticket DFY-Services
6. **Agentic UX Patterns** für KI-Services — Vertrauen durch Transparenz
7. **Design = "Margin Protector" und "Financial Instrument"**
8. **Exzellentes Design = letzte Bastion der menschlichen Differenzierung**

---

*Diese Design-Vorgaben gelten für alle Landing Pages die über diesen Skill erstellt werden. Sie ERGÄNZEN die bestehenden Copy- und Conversion-Module, sie ersetzen sie nicht.*
