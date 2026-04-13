# Lead Magnet Creator — AI-Powered Lead Generation

Creates AI-powered, interactive lead magnets that convert visitors into qualified leads. Part of the Growing Brands Agency Pipeline (Position #5: after Landing Page, before Ads).

**No static PDFs.** Every lead magnet leverages interactivity, AI personalization, and instant gratification psychology to maximize conversion rates.

---

## Core Principles

1. **Interactive over static** — Interactive content captures leads at 78% higher rates than static content. AI-adaptive quizzes convert at 47.3% vs. 5-10% for PDFs (2026 benchmarks)
2. **Instant gratification** — Deliver value on-screen in <10 minutes. Email is the archive, not the delivery mechanism
3. **Minimal friction** — Maximum Name + Email at opt-in. Every additional form field drops conversion by 8-12%. Progressive profiling comes later
4. **Zero-Party Data = Währung** — Quiz answers, calculator inputs, and generator choices are more valuable than any demographic data. Collect them, don't ask for them
5. **DSGVO by design** — Double Opt-in, Kopplungsverbot, Privacy-First. Not an afterthought — a competitive advantage in DACH
6. **Alignment vor Brillanz** — Solve the problem BEFORE the main problem. Lead magnet must connect to the core offer as the logical next step
7. **Segment-first** — Every lead magnet targets one specific segment. Generalists convert at half the rate of specialists

---

## Dependencies

### Required Input

**From Landing Page Creator (Pipeline #4):**
- Live landing page URL and copy
- Conversion architecture (CTA placement, above-the-fold strategy)
- Traffic source strategy (organic vs. paid intent)

**From Customer Avatar (Pipeline #2):**
- Section C: JTBD Core (Jobs to Be Done)
- Section E: Pain/Gain/Anxiety
- Section F: Desire & Identity
- Section H: Voice of Customer (direct quotes for hooks)
- Section I: Segmentation (which segment(s) this lead magnet targets)

**From Brand Architect (Pipeline #3):**
- Positioning Statement
- Brand Voice Guidelines
- Offer Architecture (what comes AFTER the lead magnet)
- Service Inventory (to align lead magnet topic with actual services)

### Completeness Gate (MANDATORY — run BEFORE Module 1)

```yaml
completeness_gate:
  avatar_complete:
    section_e_pain_gain: yes/no   # If no → STOP (need psychological hooks)
    section_h_voc: yes/no          # If no → STOP (need copy hooks)
    section_i_segmentation: yes/no # If no → FLAG
  brand_complete:
    offer_architecture: yes/no     # If no → STOP (can't design funnel conversion step)
    brand_voice: yes/no            # If no → STOP (copy won't match)
  landing_page:
    live_url: yes/no               # If no → FLAG (need embed/redirect strategy)
    cta_placement: yes/no          # If no → FLAG (need CTA integration plan)
  tech_ready:
    supabase_project: yes/no       # If no → use patterns from this skill
    nextjs_project: yes/no         # If no → use patterns from this skill
    resend_domain: yes/no          # If no → FLAG (need email delivery setup)
```

**If ANY mandatory item is missing → STOP and request from coordinator.**

### Optional Input

- Competitor lead magnets (URLs for research)
- Existing lead magnet performance data
- Client's current email nurture sequence
- Budget constraints (determines AI vs. rule-based approach)
- Analytics tracking requirements

### Output feeds into

- **Ads (Pipeline #6):** Lead magnet as ad creative angle, landing page variant
- **Email Nurture:** 5-7 email sequence based on lead magnet topic
- **Sales Pipeline:** Lead scoring based on zero-party data
- **Retargeting:** Segment-specific audiences based on lead magnet engagement

---

## Lead Magnet Types

### Tier 1 — High Conversion (35-47% avg.)

#### AI-Adaptive Quiz
- **Conversion Rate:** 47.3% (B2B: 38.5%, Beauty: 63.8%)
- **Best for:** Assessment needs, personalization, segmentation
- **Mechanism:** 5-8 adaptive questions → AI-generated personalized report → email delivery
- **Time to complete:** 3-7 minutes
- **Viral potential:** High (share-your-score mechanics)
- **Zero-party data collected:** Preferences, challenges, maturity level, priorities

#### ROI-Kalkulator
- **Conversion Rate:** 35-45%
- **Best for:** B2B services, high-ticket offers, ROI-driven buyers
- **Mechanism:** 4-7 input fields → real-time calculation → personalized savings/potential report
- **Time to complete:** 2-5 minutes
- **Viral potential:** Medium
- **Zero-party data collected:** Current spend, team size, revenue range, pain points

#### Kontextuelles Cheat Sheet (Interaktiv)
- **Conversion Rate:** 41.7%
- **Best for:** How-to content, checklists, process frameworks
- **Mechanism:** Contextual checklist with personalized recommendations based on selections
- **Time to complete:** 3-8 minutes
- **Viral potential:** Low-Medium
- **Zero-party data collected:** Current state, priorities, knowledge gaps

### Tier 2 — Good Conversion (25-35% avg.)

#### AI-Generator / Mini-App
- **Conversion Rate:** 25-35%
- **Best for:** Creative industries, marketing, content creation
- **Mechanism:** User inputs brief → AI generates customized output (copy, plan, strategy)
- **Time to complete:** 2-4 minutes
- **Viral potential:** Medium-High (generated content is shareable)
- **Zero-party data collected:** Industry, tone, audience, current tools

#### Interaktiver Scorecard
- **Conversion Rate:** 30-40%
- **Best for:** Audits, assessments, benchmarking
- **Mechanism:** 10-15 yes/no questions → weighted score → personalized improvement plan
- **Time to complete:** 5-10 minutes
- **Viral potential:** High (competitive comparison)
- **Zero-party data collected:** Current practices, tool usage, team maturity

### Tier 3 — Avoid (Legacy)

| Type | Conversion | Why Avoid |
|------|-----------|-----------|
| Statisches PDF (Whitepaper) | 5-10% | No interactivity, cognitive overload, no zero-party data |
| Ebook (40+ Seiten) | 3-8% | Nobody reads them. Appearance > consumption |
| Webinar-Recording | 8-15% | Time commitment too high, no instant gratification |
| Email-Kurs (5+ Tage) | 10-18% | Delayed gratification, high drop-off |
| Infographic (statisch) | 5-12% | No data collection, no personalization |

---

## Psychology Framework

### Why Users Convert — The 4 Triggers

#### 1. Mikro-Commitments (Sunk Cost Bias)
Every quiz question answered, every calculator field filled, every selection made = micro-investment. By the time they see the opt-in, they've already invested 3-5 minutes. Abandoning = losing that investment.

**Implementation:**
- Start with easy, non-threatening questions
- Show a progress bar (perceived completion drives completion)
- Never ask for email BEFORE the interactive part
- Opt-in comes AFTER 60%+ of the experience

#### 2. Instant Gratification (< 10 Minutes)
The entire experience from click to result must be under 10 minutes. Results appear on screen immediately. Email is the backup/archive — not the primary delivery.

**Implementation:**
- Target 3-7 minutes for quizzes, 2-5 for calculators
- Show results on-screen FIRST, then offer email for "detailed report" or "save your results"
- The "email for full report" step is where the opt-in happens — AFTER value delivery

#### 3. Costco Strategy (Unvollständiges Sample)
Give enough value to prove expertise, but not enough to solve the full problem. The lead magnet should make the user think: "If this free thing is this good, their paid service must be incredible."

**Implementation:**
- Show the score, hide the detailed breakdown
- Show the top 3 recommendations, hide the full action plan
- Show the potential savings, hide the implementation roadmap
- The missing piece = the natural upsell to the core offer

#### 4. Reziprozität 2.0 (Personalized Reciprocity)
Generic freebies feel transactional. Personalized value creates genuine obligation. When someone receives something tailored specifically to them, the desire to reciprocate is 3x stronger.

**Implementation:**
- Use their quiz answers to personalize the report
- Reference their calculator inputs in the recommendations
- Address their specific pain points by name
- "Based on your answers about [their challenge], here's your custom plan..."

### Anti-Patterns (Psychology Fails)

| Anti-Pattern | Why It Fails | Fix |
|-------------|-------------|-----|
| Email-first opt-in | No sunk cost, no reciprocity | Interactive experience → results preview → email for full report |
| "Download our 40-page guide" | Cognitive overload before starting | "Answer 5 questions, get your custom 2-page action plan" |
| Generic assessment | No personalization = no reciprocity | Adaptive questions that change based on previous answers |
| Full solution in lead magnet | No need for paid service | Solve ONE sub-problem, point to paid for the rest |

---

## Workflow

### Module Overview

| Module | Purpose | Output | Duration |
|--------|---------|--------|----------|
| M0: Research | Analyze competitor lead magnets, identify gaps | Competitor Matrix + Opportunity Map | 30 min |
| M1: Strategy | Choose segment, format, hook | Lead Magnet Brief | 20 min |
| M2: Content Design | Build interactive flow, copy, logic | Content Blueprint + Copy | 60 min |
| M3: Tech Architecture | Next.js + Supabase + AI integration | Technical Spec + DB Schema | 45 min |
| M4: Funnel Design | Opt-in → Delivery → Nurture → Conversion | Funnel Map + Email Sequence | 30 min |
| M5: Implementation | Deployment, tracking, A/B testing | Launch Checklist + KPI Dashboard | 45 min |

---

### M0: Research — Competitor Analysis

**Goal:** Understand what competitors offer, find gaps, identify positioning opportunities.

#### Step 1: Competitor Identification
```
Sources:
- Google: "{segment} mallorca lead magnet" / "{segment} {service} kostenlos"
- Competitor landing pages (from Landing Page Creator output)
- Industry directories and associations
- Social media (LinkedIn, Instagram lead ads)
```

#### Step 2: Lead Magnet Audit (per competitor)

For each competitor lead magnet found, document:

```yaml
competitor_audit:
  competitor_name: string
  lead_magnet_type: [quiz|calculator|pdf|generator|scorecard|other]
  format_interactive: yes/no
  topic: string
  hook_copy: string (exact wording of the CTA/headline)
  required_fields: [list of form fields before value delivery]
  value_delivery: [instant|email|download|dashboard]
  personalization_level: [none|basic|advanced|ai-powered]
  dsgvo_compliant: yes/no/partial (double opt-in visible?)
  quality_assessment: [1-5] (how good is the actual value?)
  gap_opportunity: string (what could we do better?)
```

#### Step 3: Opportunity Matrix

```yaml
opportunity_matrix:
  segment: string
  underserved_topics: [list]
  format_gaps: [formats competitors are NOT using]
  personalization_gap: yes/no (is anyone doing AI-powered?)
  dsgvo_opportunity: yes/no (is privacy-first a differentiator?)
  winning_angle: string (our recommended approach)
```

#### Step 4: Output — Research Summary
- 3-5 competitor lead magnets documented
- Clear gap identified
- Recommended angle justified with data

---

### M1: Strategy — Lead Magnet Brief

**Goal:** Make the critical strategic decisions before building anything.

#### Step 1: Segment Selection
```
Rule: ONE lead magnet = ONE segment
Exception: If two segments share an identical pain point and avatar, 
           create ONE lead magnet with segment-specific personalization
```

Choose the segment based on:
1. **Revenue potential** — Which segment has the highest LTV?
2. **Gap opportunity** — Where are competitors weakest?
3. **Client capability** — Can the client deliver on the promise?
4. **Data availability** — Do we have enough avatar data?

#### Step 2: Format Selection

```yaml
format_decision_tree:
  # Does the prospect need to SEE their current state vs. potential?
  - calculator: [immobilien, tourismus, dienstleister, handwerk]
  
  # Does the prospect need to UNDERSTAND their level/readiness?
  - quiz: [coaches, digitale_nomaden, dach_ferne]
  
  # Does the prospect need a QUICK WIN / tool?
  - generator: [tourismus, coaches, dienstleister]
  
  # Does the prospect need an AUDIT / benchmark?
  - scorecard: [dienstleister, dach_ferne, handwerk]
```

#### Step 3: Hook Development

**Naming Formula:** `[Zahl] + [Ergebnis] + [Zeitrahmen]`

Examples:
- "3 Schritte zu deinem Mallorca-Immobilien-Wert in 5 Minuten"
- "Wie viel kostet deine Website wirklich? Berechnung in 2 Min."
- "Dein Immobilien-Marktwert: KI-Analyse in 3 Minuten"
- "Mallorca Umzugs-Score: Bist du bereit? Quiz in 4 Min."

**Hook Decision Matrix:**

| Segment | Best Hook Type | Example Pattern |
|---------|---------------|-----------------|
| Immobilien |好奇心 + Geldwert | "Was ist deine Immobilie WIRKLICH wert?" |
| Tourismus | Praktischer Nutzen | "Dein perfekter 7-Tage Mallorca Plan" |
| Dienstleister | Schmerz + Lösung | "Wie viel Geld verbrennst du an [Problem]?" |
| Handwerk | Status + Effizienz | "Ist dein Handwerksbetrieb digital-fit?" |
| Coaches | Selbstverständnis | "Dein Coaching-Reifegrad: Wo stehst du?" |
| DACH-Ferne | Kontrolle + Wachstum | "Wie professionell wirkt dein Remote-Setup?" |

#### Step 4: Output — Lead Magnet Brief

```yaml
lead_magnet_brief:
  name: string
  segment: string
  format: [quiz|calculator|generator|scorecard|cheat_sheet]
  hook_headline: string
  subheadline: string
  estimated_conversion_rate: number%
  estimated_completion_time: string (e.g. "4 Minuten")
  value_promise: string (what they get)
  upsell_connection: string (how it connects to the paid offer)
  personalization_points: [list of data points collected]
  viral_mechanism: string (how it spreads)
```

---

### M2: Content Design

**Goal:** Design the complete interactive experience, copy, and logic.

#### For AI-Adaptive Quiz

```
STRUCTURE:
1. Hero Section (no email yet!)
   - Headline (from Brief)
   - Subheadline
   - "Start" button
   - Social proof (X haben schon teilgenommen)

2. Questions (5-8, adaptive)
   Q1: Warm-up (easy, non-threatening) — establishes sunk cost
   Q2: Context (their current situation) — segmentation data
   Q3: Pain point (their biggest challenge) — zero-party data gold
   Q4: Aspiration (where they want to be) — qualification
   Q5: Behavior (what they've already tried) — disqualification
   Q6-Q8: Deep dive (based on Q3-Q5 answers, adaptive)

   Question Design Rules:
   - Max 4 answer options per question
   - At least 1 answer must be slightly humorous/relatable
   - Never use "none of the above" as an option
   - Each answer maps to a personalization axis
   - Show progress bar (Step 2 of 7)

3. Results Preview (instant, on-screen)
   - Personalized score (e.g., "Dein Mallorca-Umzugs-Score: 73/100")
   - Top 3 personalized insights ( teasers for full report)
   - Visual breakdown (chart, radar, bar chart)
   - "Teile deinen Score" button (virality)

4. Opt-in Gate (AFTER value delivery)
   - "Sende mir deinen vollständigen Report per Email"
   - Fields: Name (optional) + Email (required)
   - Checkbox: "Ich stimme der Datenschutzerklärung zu" (required)
   - Preview text: "Du erhältst: 2-seitiger personalisierter Report + 3 konkrete Handlungsschritte"
   - Submit → Thank you with on-screen results still visible
```

#### For ROI-Kalkulator

```
STRUCTURE:
1. Hero Section
   - Headline (from Brief)
   - "Jetzt berechnen" CTA

2. Input Fields (4-7, progressive)
   - Start with easy inputs (dropdown: Branche, Unternehmensgröße)
   - Move to specific inputs (aktueller Monatsumsatz, laufende Kosten)
   - Each field update → real-time calculation visible
   - Show running total/estimate as they type

   Input Design Rules:
   - Use sliders for range inputs (more engaging than text fields)
   - Show tooltips with "Warum fragen wir das?"
   - Provide sensible defaults (pre-filled based on segment)
   - Currency formatting live (€1.234,56)

3. Results Dashboard (instant)
   - Big number: "Dein potenzielles Einsparpotenzial: €XX.XXX/Jahr"
   - Breakdown: Where the money is going vs. where it could go
   - Comparison: "So wie 78% der Unternehmen in deiner Branche"
   - Timeline: "In 6 Monaten könntest du €X.XXX sparen"

4. Opt-in Gate
   - "Hol dir die detaillierte Analyse + Umsetzungsplan per Email"
   - Fields: Email (required), Name (optional)
   - GDPR consent (required)
```

#### For AI-Generator

```
STRUCTURE:
1. Hero Section
   - Headline: "Generiere deinen [Ergebnis] in 2 Minuten"
   - CTA: "Jetzt generieren"

2. Input Form (3-5 fields)
   - Context fields (Branche, Zielgruppe, Ziel)
   - Style/Tone selector (profesionell, locker, kreativ)
   - Optional: URL of existing asset to improve

3. Generation (AI-powered)
   - Loading animation (3-5 seconds feels intentional)
   - Generated output displayed on-screen
   - "Regenerieren" button (one more chance to engage)
   - Copy-to-clipboard button

4. Opt-in Gate
   - "Speichere dein Ergebnis + bekomm [Bonus]"
   - Bonus: extended version, more variations, template pack
```

#### Copy Templates per Segment

**IMMOBILIEN — Immobilien-Wert-Kalkulator:**
```
Headline: "Was ist deine Mallorca-Immobilie WIRKLICH wert?"
Sub: "KI-Analyse in 3 Minuten — basierend auf aktuellen Marktdaten, Lage-Faktoren und Trends"
Q1: "Wo genau befindet sich deine Immobilie?" [Dropdown: Regionen]
Q2: "Welchen Zustand hat die Immobilie?" [Dropdown: Zustände]
Q3: "Wann wurde sie zuletzt renoviert?" [Dropdown: Zeitrahmen]
Q4: "Was ist ungefähr die Wohnfläche?" [Slider: m²]
Result Preview: "Geschätzter Marktwert: €XXX.XXX - €XXX.XXX"
Opt-in: "Hol dir die detaillierte Wertanalyse mit Trend-Prognose"
```

**TOURISMUS — Mallorca-Reiseplaner:**
```
Headline: "Dein perfekter Mallorca-Urlaub in 7 Tagen"
Sub: "Interaktiver Planer — basierend auf DEINEN Vorlieben, nicht auf generischen Listen"
Q1: "Was ist deine Reise-Grundstimmung?" [Options: Entspannung, Abenteuer, Kultur, Party]
Q2: "Mit wem reist du?" [Options: Alleine, Partner, Familie, Freunde]
Q3: "Budget pro Tag?" [Slider: €50-€500]
Q4: "Liebst du versteckte Orte oder Highlights?" [Slider]
Result Preview: "Dein personalisierter 7-Tage Plan — mit 3 Secret Spots"
Opt-in: "Sende mir den Plan per Email + GPS-Routen als PDF"
```

**DIENSTLEISTER — Waste Calculator:**
```
Headline: "Wie viel Geld verbrennst du jeden Monat an [Problem]?"
Sub: "Kostenlose Berechnung — die meisten Kunden sparen im ersten Monat €XXX"
Q1: "Wie groß ist dein Team?" [Slider]
Q2: "Wie viel Zeit geht pro Woche für [Problem] drauf?" [Slider: Stunden]
Q3: "Welche Tools nutzt du aktuell?" [Multi-Select]
Result Preview: "Dein verborgener Kostenfaktor: €X.XXX/Monat = €XX.XXX/Jahr"
Opt-in: "Hol dir den Sparspielplan mit konkreten Handlungsschritten"
```

**HANDWERK — Digital-Fit Scorecard:**
```
Headline: "Ist dein Handwerksbetrieb digital-fit?"
Sub: "15 Fragen — Rate deinen Betrieb im Vergleich zur Branche"
Q1: "Hast du eine professionelle Website?" [Ja/Nein/Teils]
Q2: "Kunden buchen online?" [Ja/Nein]
Q3: "Nutzt du digitale Auftragsverwaltung?" [Ja/Nein]
... (12 more)
Result Preview: "Dein Digital-Score: XX/100 — besser als X% der Handwerksbetriebe"
Opt-in: "Hol dir den konkreten Digitalisierungs-Fahrplan für deinen Betrieb"
```

**COACHES — Coaching-Reifegrad-Assessment:**
```
Headline: "Dein Coaching-Reifegrad: Wo stehst du wirklich?"
Sub: "Wissenschaftlich fundiertes Assessment in 5 Minuten — nicht generic Quiz"
Q1: "Wie lange coachst du schon?" [Dropdown]
Q2: "Wie gewinnst du aktuell Kunden?" [Multi-Select]
Q3: "Hast du ein systematisches Sales-Prozess?" [Scale 1-5]
Q4: "Was ist dein größter Wachstums-Blocker?" [Multi-Select]
Result Preview: "Dein Coaching-Maturity Level: [Level Name] — [Beschreibung]"
Opt-in: "Erhalte deinen persönlichen Reifegrad-Report mit Entwicklungsplan"
```

**DACH-FERNE — Remote-Setup Scorecard:**
```
Headline: "Wie professionell wirkt dein Remote-Auftritt?"
Sub: "Audit in 5 Minuten — Website, Social Media, Prozesse"
Q1: "Hast du eine DACH-optimierte Website?" [Ja/Nein]
Q2: "Nutzt du .de Domain oder .com?" [Dropdown]
Q3: "Bietest du Zahlung in EUR an?" [Ja/Nein]
Q4: "Wie erreichbar bist du für DACH-Kunden?" [Scale 1-5]
Result Preview: "Dein Remote-Professionalitäts-Score: XX/100"
Opt-in: "Hol dir den Report mit konkreten Optimierungen für den DACH-Markt"
```

---

### M3: Technical Architecture

**Goal:** Define the complete technical implementation.

#### Frontend: Next.js

```
Directory Structure:
/app
  /lead-magnet
    /[slug]
      /page.tsx          # Lead magnet wrapper
      /components/
        Hero.tsx         # Headline + CTA
        Quiz.tsx         # Quiz engine (or)
        Calculator.tsx   # Calculator engine (or)
        Generator.tsx    # AI generator (or)
        Scorecard.tsx    # Scorecard engine
        Results.tsx      # Results display
        OptIn.tsx        # Email capture gate
        ThankYou.tsx     # Post-opt-in confirmation
        ShareButtons.tsx # Viral sharing
      /lib/
        quiz-engine.ts   # Quiz logic (adaptive branching)
        calculator.ts    # Calculation formulas
        scoring.ts       # Scorecard weighting
        personalization.ts # Result personalization
```

**Mobile-First Rules:**
- Touch targets: minimum 44x44px
- Single-column layout on mobile
- Font size: minimum 16px body, 24px headlines
- No horizontal scrolling
- Sticky CTA on mobile
- Loading states for AI generation (skeleton screens)

#### Data Layer: Supabase

```sql
-- Lead Magnet Core Table
CREATE TABLE lead_magnets (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  slug TEXT UNIQUE NOT NULL,
  name TEXT NOT NULL,
  segment TEXT NOT NULL,  -- immobilien, tourismus, dienstleister, handwerk, coaches, dach_ferne
  format TEXT NOT NULL,   -- quiz, calculator, generator, scorecard, cheat_sheet
  hook_headline TEXT NOT NULL,
  is_active BOOLEAN DEFAULT true,
  created_at TIMESTAMPTZ DEFAULT now()
);

-- Lead Captures (Zero-Party Data Goldmine)
CREATE TABLE lead_magnet_leads (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  lead_magnet_id UUID REFERENCES lead_magnets(id),
  email TEXT NOT NULL,
  name TEXT,
  
  -- Zero-Party Data (JSON — flexible per lead magnet format)
  responses JSONB NOT NULL DEFAULT '{}',
  -- Example for quiz: {"q1": "calvia", "q2": "gut", "q3": "2020", "score": 73}
  -- Example for calculator: {"team_size": 5, "monthly_waste": 3200, "tools": ["trello", "slack"]}
  
  -- Results (pre-computed for instant display)
  result JSONB NOT NULL DEFAULT '{}',
  -- Example: {"score": 73, "level": "fortgeschritten", "recommendations": [...]}
  
  -- Scoring
  lead_score INTEGER DEFAULT 0,  -- 0-100, computed from responses
  
  -- Metadata
  utm_source TEXT,
  utm_medium TEXT,
  utm_campaign TEXT,
  utm_content TEXT,
  referrer TEXT,
  
  -- DSGVO
  privacy_consent_at TIMESTAMPTZ,
  double_opt_in_confirmed BOOLEAN DEFAULT false,
  double_opt_in_confirmed_at TIMESTAMPTZ,
  
  -- Funnel tracking
  email_delivered BOOLEAN DEFAULT false,
  email_opened BOOLEAN DEFAULT false,
  email_clicked BOOLEAN DEFAULT false,
  nurture_stage INTEGER DEFAULT 0,  -- 0=cold, 1=warm, 2=hot, 3=converted
  
  created_at TIMESTAMPTZ DEFAULT now()
);

-- Analytics Events
CREATE TABLE lead_magnet_events (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  lead_magnet_id UUID REFERENCES lead_magnets(id),
  lead_id UUID REFERENCES lead_magnet_leads(id),
  event_type TEXT NOT NULL,  -- started, completed, opt_in_shown, opt_in_converted, shared, etc.
  event_data JSONB DEFAULT '{}',
  created_at TIMESTAMPTZ DEFAULT now()
);

-- RLS Policies
ALTER TABLE lead_magnet_leads ENABLE ROW LEVEL SECURITY;
ALTER TABLE lead_magnet_events ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Anon can insert leads" ON lead_magnet_leads 
  FOR INSERT WITH CHECK (true);
CREATE POLICY "Anon can insert events" ON lead_magnet_events 
  FOR INSERT WITH CHECK (true);
CREATE POLICY "Service can read leads" ON lead_magnet_leads 
  FOR SELECT USING (true);
```

#### AI Integration

```
Pattern: Server-Side AI for Personalized Results

/app/api/lead-magnet/[slug]/generate/route.ts

Flow:
1. Frontend sends: { responses: {...}, format: "quiz", segment: "immobilien" }
2. Backend builds personalized prompt from responses
3. OpenAI/Claude generates: { score, insights, recommendations, level }
4. Response stored in Supabase (lead_magnet_leads.result)
5. Returned to frontend for instant display

Prompt Pattern:
"""
Du bist ein Experte für {segment} auf Mallorca.
Basierend auf folgenden Antworten eines Nutzers:
{formatted_responses}

Generiere:
1. Einen Score von 0-100
2. Ein Level-Name (z.B. "Anfänger", "Fortgeschritten", "Experte")
3. 5 personalisierte Insights (jeweils 1 Satz, Bezug zu ANTWORT)
4. 3 konkrete Handlungsschritte (priorisiert)
5. Einen Abschlusstext der auf das {core_offer} hinweist

Antworte im JSON-Format.
"""
```

#### Email Integration (Double Opt-in)

```
Flow:
1. User submits email → store in lead_magnet_leads (double_opt_in_confirmed: false)
2. Send Double Opt-in Email via Resend:
   - Template: lead-magnet-double-optin
   - Contains: confirmation link with token
   - Domain: mail.growing-brands.de (Growing Brands) or mail.mallorca-expats.de (MallorcaExpats)
3. User clicks link → update double_opt_in_confirmed: true
4. Send Lead Magnet Delivery Email:
   - Template: lead-magnet-delivery
   - Contains: link to full report (hosted), summary
   - Kicks off nurture sequence (5-7 emails)
```

---

### M4: Funnel Design

**Goal:** Design the complete post-opt-in journey.

#### Funnel Architecture

```
[Landing Page] 
    ↓ CTA: "Jetzt deinen Score berechnen"
[Lead Magnet Interactive Experience]
    ↓ Complete quiz/calculator (3-7 min)
[Results Preview — on screen, instant]
    ↓ "Sende mir den vollen Report"
[Opt-in Gate: Name (optional) + Email]
    ↓ Submit
[Double Opt-in Email] ← DSGVO Pflicht
    ↓ Confirm
[Delivery Email: Full Report + Summary]
    ↓ Auto-trigger
[Nurture Sequence: 5-7 Emails, 7-14 Tage]
    ↓ Email 5-7
[Conversion: Calendar Booking / Discovery Call / Offer Page]
```

#### Opt-in Gate Design

**Critical rule:** The opt-in happens AFTER the user has seen their results preview. They've already invested 3-7 minutes and received value. Now they want MORE.

```yaml
opt_in_gate:
  position: after_results_preview
  headline: "Dein kompletter Report wartet"
  subheadline: "Sende dir {result_type} per Email — inkl. {bonus_1} und {bonus_2}"
  fields:
    email:
      required: true
      placeholder: "deine@email.de"
      type: email
    name:
      required: false
      placeholder: "Dein Vorname (optional)"
      type: text
  consent:
    required: true
    text: "Ich stimme der {privacy_url} zu und willige ein, Emails zu erhalten."
    link_label: "Datenschutzerklärung"
  submit_button: "Report kostenlos per Email"
  microcopy: "Kein Spam. Abmeldung jederzeit. Deine Daten werden verschlüsselt gespeichert."
```

#### Nurture Email Sequence (5-7 Emails, 7-14 Days)

**Structure:**
```
Email 1 (Day 0 — Delivery):
  Subject: "Dein {result_type} ist da — plus 3 Bonus-Insights"
  Content: Full report, link to hosted results, key insight highlight
  CTA: "Lese den vollständigen Report"

Email 2 (Day 2 — Value Deep-Dive):
  Subject: "Die wichtigste Erkenntnis aus deinem {result_type}"
  Content: Expand on #1 finding, provide actionable tip
  CTA: "Mehr dazu entdecken" (link to blog/content)

Email 3 (Day 4 — Social Proof):
  Subject: "So hat [Kunde] mit {Ergebnis} in {Zeit} {Ziel} erreicht"
  Content: Case study/testimonial aligned with their quiz profile
  CTA: "Ähnliche Ergebnisse erzielen"

Email 4 (Day 7 — Objection Handling):
  Subject: "{Häufige Einwand} — und warum er dich aufhält"
  Content: Address the #1 objection from their segment
  CTA: "Lass uns genau darüber sprechen"

Email 5 (Day 10 — Soft Pitch):
  Subject: "Bereit für den nächsten Schritt?"
  Content: Connect lead magnet results to the core offer
  CTA: "Kostenloses Erstgespräch buchen" (Calendar link)

Email 6 (Day 12 — Urgency/Scarcity):
  Subject: "Nur noch [X] Plätze im {Monat}"
  Content: Limited capacity, social proof of demand
  CTA: "Jetzt Platz sichern"

Email 7 (Day 14 — Final Attempt):
  Subject: "Letzte Chance: Dein personalisierter Aktionsplan"
  Content: One last valuable insight + direct offer
  CTA: "Jetzt starten oder alles aufgeben" (binary choice)
```

**Nurture Email Rules:**
- Every email delivers standalone value (even if they never buy)
- CTAs alternate between content and conversion
- Personalize using zero-party data from lead magnet responses
- Track: open rate, click rate, click-to-booking rate
- Stop sequence if they book (nurture_stage → converted)

#### Conversion Step Design

The conversion must feel like the NATURAL next step after the lead magnet:

```yaml
conversion_alignment:
  # BAD: Lead magnet about "website speed" → pitch "brand strategy"
  # GOOD: Lead magnet about "website speed" → pitch "website performance optimization package"
  
  formula: "Lead Magnet löst Teil-Problem → Paid Offer löst Gesamt-Problem"
  
  # The lead magnet should create AWARENESS of the full problem
  # The nurture emails create URGENCY to solve it
  # The conversion offer is the OBVIOUS solution
  
  transition_copy: "Dein {result_type} zeigt: {insight}. Das ist nur die Spitze des Eisbergs. 
                   {Service} hilft dir, {vollständiges_Ziel} zu erreichen."
```

---

### M5: Implementation Checklist

**Goal:** Everything needed to launch, track, and optimize.

#### Pre-Launch Checklist

```yaml
pre_launch:
  content:
    - [ ] All questions/inputs defined and copy-written
    - [ ] Results logic tested (all answer combinations)
    - [ ] Personalization prompts validated
    - [ ] German copy proofread (no English fallbacks)
    - [ ] Mobile preview tested (44x44px touch targets)
    
  technical:
    - [ ] Next.js route deployed
    - [ ] Supabase tables created with RLS
    - [ ] AI endpoint tested (latency < 5s)
    - [ ] Double opt-in flow tested end-to-end
    - [ ] Email templates created in Resend
    - [ ] Nurture sequence configured
    - [ ] Error states handled (AI timeout, network error)
    
  legal:
    - [ ] Datenschutzprüfung abgeschlossen (see DSGVO Checklist)
    - [ ] Impressum verlinkt
    - [ ] Datenschutzerklärung verlinkt und aktuell
    - [ ] Cookie-Banner vorhanden (falls Tracking)
    
  tracking:
    - [ ] Analytics events firing (started, completed, opt_in, confirmed)
    - [ ] UTM parameters captured
    - [ ] A/B test variant configured
    - [ ] Dashboard created (see KPIs section)
    
  integration:
    - [ ] Landing page CTA links to lead magnet
    - [ ] Lead magnet results page links to booking/offer
    - [ ] CRM integration active (new lead → CRM contact)
    - [ ] Nurture emails reference correct booking link
```

#### A/B Testing Framework

```yaml
ab_testing:
  what_to_test:
    - headline_variants: [2-3 variants per lead magnet]
    - question_order: [easy-first vs. pain-first]
    - opt_in_position: [after_3_questions vs. after_results]
    - cta_copy: ["Jetzt starten" vs. "Kostenlos testen" vs. "Dein Ergebnis in 3 Min"]
    - email_subject_lines: [2 variants per nurture email]
    
  sample_sizes:
    - minimum: 100 conversions per variant
    - recommended: 300+ for statistical significance
    
  tools:
    - Next.js middleware for variant assignment
    - Supabase for event tracking
    - Simple chi-squared test for significance
```

#### Deployment Pattern

```bash
# 1. Create Supabase migration
supabase migration new add_lead_magnet_tables
# Apply the SQL schema from M3

# 2. Deploy Next.js routes
# Lead magnets live under /lead-magnet/[slug]

# 3. Configure Resend email templates
# Templates: lead-magnet-double-optin, lead-magnet-delivery, nurture-1 through nurture-7

# 4. Set up webhooks for automation
# Double opt-in confirmation → trigger delivery email
# Delivery email sent → trigger nurture sequence

# 5. Analytics dashboard
# Use the KPI queries from section below
```

---

## Segment Playbook

### 1. Immobilien (Real Estate)

**Audience:** Immobilienbesitzer auf Mallorca, die verkaufen/vermieten wollen oder ihren Wert kennen möchten.

**Best Formats:** ROI-Kalkulator, AI-Bewertungstool
**Typical Conversion:** 35-42%

**Lead Magnet Ideas:**

| Idea | Format | Hook |
|------|--------|------|
| Immobilien-Wert-Kalkulator | Calculator | "Was ist deine Mallorca-Immobilie WIRKLICH wert?" |
| KI-Standortbewertung | Quiz | "Ist deine Lage ein Preistreiber oder Preiskiller?" |
| Renovierungs-ROI Rechner | Calculator | "Lohnt sich die Renovierung? Berechne deinen ROI" |
| Vermietungs-Ertragsrechner | Calculator | "Wie viel könntest du monatlich einnehmen?" |
| Selling Readiness Quiz | Quiz | "Bist du bereit zu verkaufen? 5-Min-Check" |

**Copy Template (Immobilien-Wert-Kalkulator):**
```
Hero:
  H1: "Was ist deine Mallorca-Immobilie WIRKLICH wert?"
  H2: "KI-Analyse in 3 Minuten — aktuelle Marktdaten + Lage-Faktoren + Trends"
  CTA: "Jetzt kostenlos analysieren"

Opt-in Gate:
  H1: "Deine detaillierte Wertanalyse"
  H2: "Erhalte: Marktwert-Schätzung · Trend-Prognose · Vergleich zu ähnlichen Objekten"
  CTA: "Analyse per Email — kostenlos"

Nurture Email 1:
  Subject: "Deine Immobilien-Analyse ist fertig"
  Body: "Hallo {name}, deine Mallorca-Immobilie in {region} zeigt interessante Werte.
         Der aktuelle Markttrend in {region} liegt bei +{trend}%. 
         Deine detaillierte Analyse: [Link]"
         
Nurture Email 5 (Conversion):
  Subject: "Maximiere den Wert deiner Immobilie"
  Body: "Deine Analyse zeigt Potenzial in {area}. Growing Brands hilft {Kunde} in {Ort},
         den Verkaufspreis um {X}% zu steigern durch {Methode}.
         Lass uns sprechen: [Booking Link]"
```

**Zero-Party Data to Collect:** Region, Immobilientyp, Zustand, Größe, Besitzdauer, Verkaufsabsicht, Zeithorizont

---

### 2. Tourismus (Hotels, Restaurants, Experiences)

**Audience:** Touristen die Mallorca besuchen wollen, Reiseplaner.

**Best Formats:** AI-Generator, Interaktiver Planer
**Typical Conversion:** 30-40%

**Lead Magnet Ideas:**

| Idea | Format | Hook |
|------|--------|------|
| 7-Tage Reiseplaner | Generator | "Dein perfekter Mallorca-Urlaub — generiert in 2 Min." |
| Secret-Spots Finder | Quiz | "Welche Mallorca Secrets passen zu dir?" |
| Budget-Reise Planer | Generator | "Mallorca für {Budget} — dein persönlicher Plan" |
| Aktivitäten-Matcher | Quiz | "Was MALLORCA-Vibe bist du?" |
| Packlisten-Generator | Generator | "Deine Mallorca Packliste — perfekt für {Monat}" |

**Copy Template (Reiseplaner):**
```
Hero:
  H1: "Dein perfekter Mallorca-Urlaub in 7 Tagen"
  H2: "Nicht eine generische Liste — dein persönlicher Plan, basierend auf DEINEN Vorlieben"
  CTA: "Plan erstellen"

Opt-in Gate:
  H1: "Speichere deinen Reiseplan"
  H2: "Plus: GPS-Routen als PDF · Secret-Spots-Karte · Wetter-Tipps für deine Reisezeit"
  CTA: "Plan per Email — kostenlos"

Nurture Connection to Tourismus Business:
  Email 3: "Die Unterkünfte, die zu deinem Reise-Stil passen"
  Email 5: "Buche direkt bei unseren Partnern — exklusive Konditionen für Plan-Nutzer"
```

**Zero-Party Data to Collect:** Reiseart, Budget, Begleitung, Dauer, Interessen, bevorzugte Region, Reisezeitraum

---

### 3. Expat-Dienstleister (Relocation, Legal, Financial)

**Audience:** People planning to move to Mallorca from DACH.

**Best Formats:** Quiz, Scorecard
**Typical Conversion:** 38-47%

**Lead Magnet Ideas:**

| Idea | Format | Hook |
|------|--------|------|
| Umzugs-Readiness Quiz | Quiz | "Bist du bereit für Mallorca? 5-Min-Check" |
| Kosten-Rechner | Calculator | "Was kostet der Umzug nach Mallorca WIRKLICH?" |
| Visum-Check | Scorecard | "Welches Visum passt zu dir?" |
| NIE-Checklist (Interaktiv) | Cheat Sheet | "Deine persönliche NIE-Besorgungs-Checkliste" |
| Steuer-Rechner | Calculator | "Wie viel Steuern zahlst du auf Mallorca?" |

**Copy Template (Umzugs-Readiness Quiz):**
```
Hero:
  H1: "Bist du bereit für Mallorca? Der 5-Minuten Reality-Check"
  H2: "Ehrliche Einschätzung — keine Rosenbrillen, keine Hürden-Angst. Nur Fakten."
  CTA: "Jetzt testen"

Opt-in Gate:
  H1: "Dein Mallorca-Umzugs-Report"
  H2: "Inklusive: Zeitplan · Budget-Schätzung · Checkliste · häufige Fallstricke"
  CTA: "Report per Email — kostenlos"

Nurture Email 4 (Objection):
  Subject: "Die 3 größten Ängste beim Umzug nach Mallorca (und warum sie unbegründet sind)"
  Body: Referenziert ihre Quiz-Antworten direkt.
```

**Zero-Party Data to Collect:** Herkunft, Familienstand, Beruf, Budget, Zeithorizont, Sprachkenntnisse, bisherige Mallorca-Erfahrung

---

### 4. Handwerk (Crafts, Trades, Construction)

**Audience:** Handwerksbetriebe auf Mallorca, die digitalisieren wollen oder mehr Kunden brauchen.

**Best Formats:** Scorecard, ROI-Kalkulator
**Typical Conversion:** 32-42%

**Lead Magnet Ideas:**

| Idea | Format | Hook |
|------|--------|------|
| Digital-Fit Scorecard | Scorecard | "Ist dein Handwerksbetrieb digital-fit?" |
| Kunden-Akquise Rechner | Calculator | "Wie viele Kunden verlierst du an die Konkurrenz?" |
| Online-Sichtbarkeit Check | Scorecard | "Finden dich Kunden auf Google?" |
| Preis-Kalkulator | Calculator | "Berechne deine fairMallen Stundenrate" |
| Bewertungs-Check | Scorecard | "Wie trustworthy wirkt dein Betrieb online?" |

**Copy Template (Digital-Fit Scorecard):**
```
Hero:
  H1: "Ist dein Handwerksbetrieb digital-fit?"
  H2: "15 Fragen · 3 Minuten · Dein Score im Vergleich zur Branche"
  CTA: "Jetzt testen"

Opt-in Gate:
  H1: "Dein Digitalisierungs-Fahrplan"
  H2: "Inklusive: Prioritäten-Liste · Kostenschätzung · ROI-Prognose für deine Branche"
  CTA: "Fahrplan per Email — kostenlos"

Conversion:
  Subject: "Der erste Schritt zur digitalen Transformation"
  Body: "Dein Score von {score}/100 zeigt {insight}. 
         Wir haben {Anzahl} Handwerksbetriebe auf Mallorca digitalisiert. 
         Durchschnittliche Ergebnissteigerung: {X}% mehr Anfragen in 3 Monaten."
```

**Zero-Party Data to Collect:** Betriebsgröße, Gewerk, aktuelle Digital-Tools, Website-Status, Kundenakquise-Kanäle, größter Schmerzpunkt

---

### 5. Digitale Nomaden & Coaches

**Audience:** Coaches, Berater, Freelancer die ihre Online-Präsenz professionalisieren wollen.

**Best Formats:** Quiz, AI-Generator
**Typical Conversion:** 35-47%

**Lead Magnet Ideas:**

| Idea | Format | Hook |
|------|--------|------|
| Coaching-Reifegrad-Assessment | Quiz | "Dein Coaching-Reifegrad: Wo stehst du?" |
| Client-Magnet Generator | Generator | "Generiere deinen nächsten Client-Magnet" |
| Pricing-Kalkulator | Calculator | "Was darfst du als Coach verlangen?" |
| Funnel-Audit | Scorecard | "Dein Funnel-Score: Wo verlierst du Kunden?" |
| Brand-Vibe Check | Quiz | "Was strahlt deine Marke aus?" |

**Copy Template (Reifegrad-Assessment):**
```
Hero:
  H1: "Dein Coaching-Reifegrad: Wo stehst du WIRKLICH?"
  H2: "Wissenschaftlich fundiert — keine Fluor-Questions, echte Tiefgang-Analyse"
  CTA: "Assessment starten"

Opt-in Gate:
  H1: "Dein persönlicher Reifegrad-Report"
  H2: "Inklusive: Entwicklungsplan · Ressourcen · Nächste Schritte für Level {level}"
  CTA: "Report per Email — kostenlos"

Conversion:
  Direct connection to coaching/consulting offer.
  "Dein Assessment zeigt dass du auf Level {level} bist. 
   Der nächste Level erfordert {specific_action}. 
   Genau dabei unterstützen wir."
```

**Zero-Party Data to Collect:** Coaching-Dauer, Kundenanzahl, Einkommen, größte Herausforderung, Marketing-Kanäle, Zielgruppe

---

### 6. DACH-Ferne Unternehmen

**Audience:** Unternehmen im DACH-Raum, die remote arbeiten oder nach Mallorca expandieren wollen.

**Best Formats:** Scorecard, Calculator
**Typical Conversion:** 35-42%

**Lead Magnet Ideas:**

| Idea | Format | Hook |
|------|--------|------|
| Remote-Setup Scorecard | Scorecard | "Wie professionell wirkt dein Remote-Auftritt?" |
| Standort-Vergleich | Calculator | "Mallorca vs. {Stadt} — Kosten-Vergleich" |
| DACH-Markt Audit | Scorecard | "Bist du DACH-ready?" |
| Team-Produktivität Rechner | Calculator | "Wie produktiv ist dein Remote-Team wirklich?" |
| Compliance-Check | Scorecard | "Arbeitsrecht Mallorca — Compliance-Check" |

**Copy Template (Remote-Setup Scorecard):**
```
Hero:
  H1: "Wie professionell wirkt dein Remote-Auftritt?"
  H2: "Audit in 5 Minuten — Website, Prozesse, Recht, Team"
  CTA: "Audit starten"

Opt-in Gate:
  H1: "Dein Remote-Professionalitäts-Report"
  H2: "Inklusive: Schwachstellen-Analyse · Quick-Wins · Roadmap für DACH-Markt"
  CTA: "Report per Email — kostenlos"

Conversion:
  "Dein Audit zeigt {X} Optimierungspotenziale. 
   Growing Brands hat {Anzahl} Unternehmen beim Remote-Setup geholfen.
   Durchschnittliche Effizienzsteigerung: {X}%."
```

**Zero-Party Data to Collect:** Unternehmensgröße, Branche, aktueller Standort, Team-Remote-Anteil, Website-Status, Rechtliches Setup, Budget für Professionalisierung

---

## DSGVO Checklist

**Goal:** Every lead magnet is 100% DSGVO-compliant for the DACH market. Privacy-First is a competitive advantage, not a burden.

### Mandatory Requirements

```yaml
dsgvo_checklist:
  data_minimization:
    - [ ] Only collect data that is NECESSARY for the lead magnet functionality
    - [ ] Email is the minimum required for delivery → justified
    - [ ] Name is OPTIONAL → clearly marked as optional
    - [ ] NO phone number, address, or company name at opt-in
    - [ ] Zero-party data (quiz answers) collected transparently: "Deine Antworten helfen uns, personalisierte Ergebnisse zu liefern"
    
  double_opt_in:
    - [ ] Double opt-in email sent immediately after opt-in
    - [ ] Confirmation link valid for 24-48 hours maximum
    - [ ] NO delivery email sent before double opt-in confirmed
    - [ ] Lead magnet results STILL visible on-screen (value delivered pre-opt-in)
    - [ ] Delivery email contains the full report (value ARCHIVED post-opt-in)
    
  kopplungsverbot:
    - [ ] Opt-in is NOT a condition for using the lead magnet
    - [ ] User can complete the full interactive experience WITHOUT giving email
    - [ ] Results preview is available WITHOUT email
    - [ ] Email opt-in = "send me the detailed report" → VOLUNTARY additional value
    - [ ] NO "required to continue" messaging before opt-in
    
  transparency:
    - [ ] Datenschutzerklärung linked at opt-in form
    - [ ] Clear explanation of what data is collected and why
    - [ ] Clear explanation of how long data is stored
    - [ ] Clear explanation of who processes the data
    - [ ] Link to Impressum
    
  consent:
    - [ ] Separate checkbox for privacy consent (NOT pre-checked)
    - [ ] Checkbox text links to Datenschutzerklärung
    - [ ] NO pre-checked marketing consent
    - [ ] Marketing consent (nurture emails) separate from privacy consent
    - [ ] Easy unsubscribe in every email (one-click)
    
  data_subject_rights:
    - [ ] Users can request data deletion (automated or process documented)
    - [ ] Users can request data export
    - [ ] Users can object to processing
    - [ ] Contact for data requests clearly visible
    
  data_storage:
    - [ ] Supabase RLS policies configured correctly
    - [ ] Data encrypted at rest (Supabase default)
    - [ ] Data encrypted in transit (HTTPS everywhere)
    - [ ] Retention policy defined and implemented
    - [ ] Automatic deletion after retention period (cron job or database trigger)
    
  cookies_tracking:
    - [ ] Cookie banner present if any tracking cookies used
    - [ ] Analytics tracking uses minimal necessary cookies
    - [ ] NO third-party tracking without consent
    - [ ] Consent log maintained (who consented to what, when)
```

### Privacy-First as Competitive Advantage

```
COPY THAT BUILDS TRUST:

Opt-in form microcopy:
"Deine Daten bleiben auf unseren Servern in der EU. Kein Verkauf, 
 keine Weitergabe, kein Tracking ohne deine Zustimmung."

Delivery email footer:
"Warum wir deine Email haben: Du hast unseren {lead_magnet_name} genutzt 
 und wolltest den Report per Email. Du kannst jederzeit widerrufen: 
 [Abmelden-Link] · [Daten-Löschen-Link]"

Privacy page highlights:
"Wir sammeln nur Zero-Party Data — Daten, die DU uns freiwillig gibst, 
 um personalisierte Ergebnisse zu erhalten. Kein Profil-Building, 
 keine Datenbroker, kein Tracking-Überfluss."
```

---

## Tech Stack

### Frontend: Next.js

```typescript
// Lead Magnet Page Component Pattern
// /app/lead-magnet/[slug]/page.tsx

interface LeadMagnetPageProps {
  params: { slug: string }
}

export default async function LeadMagnetPage({ params }: LeadMagnetPageProps) {
  const leadMagnet = await getLeadMagnet(params.slug)
  
  if (!leadMagnet || !leadMagnet.is_active) {
    notFound()
  }

  return (
    <main className="min-h-screen bg-gray-50">
      {/* Hero Section */}
      <HeroSection leadMagnet={leadMagnet} />
      
      {/* Interactive Section — dynamically rendered based on format */}
      <InteractiveEngine 
        leadMagnet={leadMagnet} 
        format={leadMagnet.format} 
      />
      
      {/* Results Section — shown after completion */}
      <ResultsSection />
      
      {/* Opt-in Gate — shown after results preview */}
      <OptInGate leadMagnet={leadMagnet} />
      
      {/* Thank You — shown after email submitted */}
      <ThankYouSection />
    </main>
  )
}

// Quiz Engine Component Pattern
// Uses useState for step management, useEffect for AI calls
// Progress bar shows current step
// Answers stored in state, sent to API on completion
// Results displayed instantly, opt-in gate slides up from below
```

### Backend: Supabase + Edge Functions

```typescript
// Pattern: Save lead + trigger double opt-in

// /app/api/lead-magnet/submit/route.ts
import { createClient } from '@supabase/supabase-js'

export async function POST(request: Request) {
  const { leadMagnetId, email, name, responses, result } = await request.json()
  
  const supabase = createClient(
    process.env.SUPABASE_URL!,
    process.env.SUPABASE_SERVICE_KEY! // Use service key for server-side writes
  )
  
  // 1. Save lead (double_opt_in_confirmed: false)
  const { data: lead, error } = await supabase
    .from('lead_magnet_leads')
    .insert({
      lead_magnet_id: leadMagnetId,
      email,
      name: name || null,
      responses,
      result,
      privacy_consent_at: new Date().toISOString(),
      double_opt_in_confirmed: false,
    })
    .select()
    .single()
  
  // 2. Send double opt-in email via Resend
  const confirmationToken = crypto.randomUUID()
  await supabase.from('opt_in_tokens').insert({
    lead_id: lead.id,
    token: confirmationToken,
    expires_at: new Date(Date.now() + 48 * 60 * 60 * 1000).toISOString(),
  })
  
  await fetch('https://api.resend.com/emails', {
    method: 'POST',
    headers: {
      Authorization: `Bearer ${process.env.RESEND_API_KEY}`,
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({
      from: process.env.FROM_EMAIL, // mail.growing-brands.de or mail.mallorca-expats.de
      to: email,
      subject: 'Bestätige deine Email',
      html: doubleOptInTemplate(confirmationToken, leadMagnetId),
    }),
  })
  
  return Response.json({ success: true, leadId: lead.id })
}

// /app/api/lead-magnet/confirm/route.ts
export async function GET(request: Request) {
  const { searchParams } = new URL(request.url)
  const token = searchParams.get('token')
  
  // 1. Validate token (not expired)
  const supabase = createClient(/* ... */)
  const { data: optIn } = await supabase
    .from('opt_in_tokens')
    .select('lead_id, expires_at')
    .eq('token', token)
    .single()
  
  if (!optIn || new Date(optIn.expires_at) < new Date()) {
    return redirect('/lead-magnet/confirm?error=expired')
  }
  
  // 2. Mark lead as confirmed
  await supabase
    .from('lead_magnet_leads')
    .update({ double_opt_in_confirmed: true, double_opt_in_confirmed_at: new Date().toISOString() })
    .eq('id', optIn.lead_id)
  
  // 3. Delete used token
  await supabase.from('opt_in_tokens').delete().eq('token', token)
  
  // 4. Trigger delivery email + nurture sequence
  await triggerDeliveryEmail(optIn.lead_id)
  
  return redirect('/lead-magnet/confirm?success=true')
}
```

### Email: Resend

```typescript
// Delivery Email Pattern via Resend
// Domain: mail.growing-brands.de (Growing Brands clients)
// Domain: mail.mallorca-expats.de (MallorcaExpats clients)

// Idempotency: Use format "lead-magnet-delivery/{leadId}"
const response = await fetch('https://api.resend.com/emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.RESEND_API_KEY}`,
    'Content-Type': 'application/json',
    'X-Idempotency-Key': `lead-magnet-delivery/${lead.id}`,
  },
  body: JSON.stringify({
    from: 'Growing Brands <hello@mail.growing-brands.de>',
    to: lead.email,
    subject: `Dein ${leadMagnet.name} Report ist da`,
    html: deliveryEmailTemplate(lead),
  }),
})
```

### Automation: Webhooks / Make.com

```
Trigger Flow:
1. Double opt-in confirmed → Supabase webhook → 
2. Make.com scenario: 
   - Step 1: Send delivery email (Resend)
   - Step 2: Create CRM contact (Growing Brands API or Supabase)
   - Step 3: Schedule nurture Email 2 (delayed)
   - Step 4: Schedule nurture Email 3 (delayed)
   - Step 5: Schedule nurture Email 4 (delayed)
   - Step 6: Schedule nurture Email 5 (delayed)

Alternative: All in Supabase Edge Functions (no external automation needed)
```

---

## KPIs & Optimization

### What to Measure (NOT CPL!)

```yaml
kpis:
  # Primary Metrics (North Star)
  cost_per_opportunity:
    formula: "Total Lead Magnet Spend / Number of Sales Opportunities Generated"
    target: "< €50 (varies by segment)"
    why: "Leads sind billig, Opportunities sind wertvoll"
    
  sales_accepted_leads:
    formula: "Leads that pass lead quality threshold"
    target: "> 40% of total leads"
    why: "Qualität vor Quantität"
    
  revenue_per_lead:
    formula: "Total Revenue from Lead Magnet Funnel / Total Leads"
    target: "Segment-dependent (track over time)"
    why: "Der wahre ROI-Indikator"
    
  # Secondary Metrics
  completion_rate:
    formula: "Users who complete interactive experience / Users who start"
    target: "> 65%"
    benchmark: "Quiz: 72%, Calculator: 78%, Generator: 68%"
    
  opt_in_rate:
    formula: "Users who provide email / Users who see opt-in gate"
    target: "> 45%"
    note: "High because they already received value"
    
  double_opt_in_rate:
    formula: "Confirmed emails / Submitted emails"
    target: "> 85%"
    note: "Low rate = email deliverability or subject line issue"
    
  nurture_engagement:
    formula: "Average opens per nurture sequence"
    target: "> 3.5 of 7 emails opened"
    
  conversion_to_booking:
    formula: "Booked calls / Total leads"
    target: "> 8% (varies by segment)"
    
  # Diagnostic Metrics
  drop_off_points:
    track: "Where users abandon (which question, which step)"
    
  average_completion_time:
    track: "How long users spend (target: 3-7 minutes)"
    
  share_rate:
    formula: "Users who share results / Users who complete"
    target: "> 5% (viral coefficient)"
    
  mobile_vs_desktop:
    track: "Completion rate by device (mobile typically 15% lower)"
```

### Predictive Lead Scoring

```sql
-- Lead Score Formula (computed from zero-party data)
-- Runs on insert/update of lead_magnet_leads

CREATE OR REPLACE FUNCTION compute_lead_score()
RETURNS TRIGGER AS $$
DECLARE
  score INTEGER := 0;
  resp JSONB;
BEGIN
  resp := NEW.responses;
  
  -- Segment-specific scoring
  -- Example for Immobilien:
  IF NEW.segment = 'immobilien' THEN
    -- Higher score if they plan to sell soon
    IF (resp->>'sell_intention') IN ('sofort', '6_monate') THEN
      score := score + 30;
    ELSIF (resp->>'sell_intention') = 'nur_neugierig' THEN
      score := score + 5;
    END IF;
    
    -- Higher score for high-value properties
    IF (resp->>'estimated_value')::NUMERIC > 500000 THEN
      score := score + 20;
    END IF;
    
    -- Higher score if they've already renovated
    IF (resp->>'condition') = 'renoviert' THEN
      score := score + 15;
    END IF;
  END IF;
  
  -- Engagement scoring
  IF NEW.email_opened THEN score := score + 10; END IF;
  IF NEW.email_clicked THEN score := score + 20; END IF;
  IF NEW.nurture_stage >= 2 THEN score := score + 15; END IF;
  
  -- Cap at 100
  score := LEAST(score, 100);
  
  NEW.lead_score := score;
  RETURN NEW;
END;
$$ LANGUAGE plpgsql;
```

### Optimization Loop

```
Weekly Optimization Cycle:
1. Pull KPIs from Supabase dashboard
2. Identify biggest drop-off point (diagnostic metrics)
3. Form hypothesis: "If we [change], then [metric] will [improve]"
4. Implement A/B test
5. Run for minimum 100 conversions per variant
6. Evaluate significance
7. Implement winner, kill loser
8. Document learnings in ByteRover

Common optimizations by symptom:
- Low completion rate → Reduce questions, simplify language, show progress
- Low opt-in rate → Strengthen results preview, improve bonus offer
- Low double opt-in → Check email deliverability, improve subject line
- Low nurture opens → Personalize subjects with zero-party data
- Low conversion → Improve alignment between lead magnet and offer
```

---

## Guardrails

### What NOT to Do

```yaml
never:
  # Content Sins
  - statische PDFs als Lead Magnet (Conversion: 5-10%)
  - 40-seiten Whitepapers (kognitive Überlastung, niemand liest sie)
  - generische Checklisten ohne Personalisierung (keine Reziprozität)
  - Lead Magnet der das HAUPTPROBLEM komplett löst (kein Upsell-Potenzial)
  
  # UX Sins
  - Email als erstes Feld im Formular (bevor interaktiver Teil)
  - mehr als 2 Pflichtfelder bei Opt-in (Conversion Drop: 40% → 8-12%)
  - CAPTCHA im Lead Magnet (Conversion Drop: 15-30%)
  - Desktop-only Design (82%+ Traffic ist Mobile)
  - Ladezeiten > 3 Sekunden (50% Bounce Rate Drop)
  
  # Psychology Sins
  - "kostenloses E-Book" als Hook (niemand will mehr E-Books)
  - ohne vorherigen Wert zu liefern nach Email fragen (Kopplungsverbot + Low Conversion)
  - Fake-Urgency ("Nur noch 24 Stunden!") bei Evergreen Lead Magnets
  - Über-Promise ("Du wirst X€ in Y Tagen verdienen") → Rechtliches Risiko
  
  # Funnel Sins
  - Lead Magnet der nicht zum Core Offer passt (Alignment-Desaster)
  - Nurture Emails die nur verkaufen (ohne zusätzlichen Value)
  - Conversion zu früh (Email 1 oder 2) → vernichtet Trust
  - Keine Handlungsaufforderung am Ende des Nurture
  
  # Technical Sins
  - Supabase ohne Row Level Security
  - Double Opt-in als "optional" markieren
  - Lead Data ohne Löschkonzept (DSGVO-Verletzung)
  - AI-Generation ohne Fallback (wenn OpenAI down → Lead Magnet kaputt)
  - Keine Error States (API Fehler, Timeout, Netzwerk-Ausfall)
  
  # DSGVO Sins
  - Vorausgefüllte Checkboxen (nicht valide Einwilligung)
  - "Wir verwenden Cookies" ohne Banner (DSGVO-Verletzung)
  - Daten an US-Server senden ohne Standardvertragsklauseln
  - Newsletter-Anmeldung und Privacy Consent in EINER Checkbox
  - Keine Möglichkeit Daten zu löschen (Recht auf Vergessenwerden)
```

### Red Flags — Stop and Reassess

```
🚨 STOP wenn:
- Der Lead Magnet das gleiche Problem löst wie das Hauptangebot
- Die Conversion Rate unter 15% fällt (nach 200+ Sessions)
- Die Double Opt-in Rate unter 60% fällt
- Der Lead Magnet für 2+ Segmente gleichzeitig optimiert werden soll
- Der Client möchte mehr als Name + Email als Pflichtfelder
- Es keine natürliche Verbindung zum Core Offer gibt
- Der Lead Magnet länger als 10 Minuten dauert
```

---

## Pipeline Integration

### Upstream: Landing Page (Position #4)

```
CONNECTION:
1. Landing Page CTA → Lead Magnet URL
   - CTA text: "Jetzt deinen {result} berechnen"
   - Link: /lead-magnet/{slug}
   - UTM parameters: utm_source=landing_page&utm_medium=cta

2. Lead Magnet topic MUST align with landing page messaging
   - Landing page promise → Lead magnet delivers on that promise
   - Example: LP says "Wir machen dein Handwerk digital" → LM is "Digital-Fit Scorecard"

3. Lead Magnet results page → redirect back to landing page for conversion
   - Results page CTA: "Lass uns darüber sprechen"
   - Links to landing page booking section or standalone booking page
```

### Downstream: Ads (Position #6)

```
CONNECTION:
1. Lead Magnet AS ad creative
   - Ad headline = Lead magnet hook
   - Ad CTA = "Jetzt kostenlos testen"
   - Ad landing page = Lead magnet URL (not the main landing page)
   - Lead magnets generate cheaper leads than direct-to-offer ads

2. Lead Magnet data INFORMS ad targeting
   - Zero-party data → custom audiences
   - Quiz responses → interest-based targeting
   - Lead scores → budget allocation (high-score leads get more budget)

3. Lead Magnet results AS social proof
   - "X Leute haben ihren Score berechnet"
   - "Durchschnittlicher Score: Y/100"
   - User-generated content from share buttons
```

---

## Quick Reference

### Format Selection Cheat Sheet

| Wenn der Prospect... | Dann nutze... |
|---------------------|---------------|
| ...ihren aktuellen WERT wissen will | ROI-Kalkulator |
| ...ihre REIFESTUFE einschätzen will | Quiz / Assessment |
| ...ein TOOL brauchst (Plan, Liste, Text) | AI-Generator |
| ...einen AUDIT braucht | Scorecard |
| ...einen PROZESS lernen will | Interaktives Cheat Sheet |

### Naming Formula

```
[Zahl] + [Ergebnis] + [Zeitrahmen]

✅ "3 Schritte zu deinem Immobilien-Wert in 5 Minuten"
✅ "Dein Digital-Score in 3 Minuten"
✅ "7 Handlungsschritte für mehr Kunden — sofort"

❌ "Kostenloser Guide" (generic)
❌ "Alles was du über X wissen musst" (overwhelming)
❌ "Download jetzt" (no value promise)
```

### Conversion Funnel Metrics (Benchmarks)

```
Traffic → Start LM: 40-60% (depends on CTA clarity)
Start → Complete: 65-80% (depends on duration)
Complete → Opt-in: 45-60% (depends on value delivered)
Opt-in → Double Opt-in: 85-95% (depends on email quality)
Double Opt-in → Nurture Open: 50-70% (depends on subject lines)
Nurture → Booking: 5-12% (depends on offer alignment)

Overall Funnel Conversion (Traffic → Booking): 0.5-3%
Overall Funnel Conversion (Traffic → Lead): 8-25%
```

---

*Skill Version: 1.0 | Last Updated: 2026-03-23 | Pipeline Position: #5*
*Part of: Growing Brands Agency Pipeline (Avatar → Brand → Landing Page → **Lead Magnet** → Ads → Nurture)*-e 
---

## 🧠 Learned Patterns

_This section is auto-maintained by the Skill Learning System. Do not edit manually._

<!-- No learnings yet. First task execution will populate this section. -->
