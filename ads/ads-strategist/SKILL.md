# Meta Ads Campaign Architect

Erstellt vollständige, production-ready Meta Ads Kampagnen aus validierten Angles & Hooks — mit Kampagnenstruktur, Targeting, Copy, Creative-Plan, technischem Setup, Performance-Framework und DACH-Compliance.

**Ein Media Buyer muss das direkt umsetzen können. Keine Platzhalter.**

---

## Pipeline-Position

```
Avatar → Brand → Angles & Hooks → META ADS → Landing Page → Lead Magnet
                              ↑ DU HIER
```

**Input:** Customer Avatar (A-K), Ad Angles & Hooks (≥15 Angles, ≥30 Hooks), Brand Strategy (optional)
**Output:** Vollständige Meta Ads Kampagne als Markdown-Dokument (Sections A–H)

---

## Dependencies

### Required Input

| Input | Quelle | Mindestanforderung |
|-------|--------|-------------------|
| Customer Avatar | Avatar Architect | Sections A–K (mindestens B, E, F, H, I) |
| Ad Angles & Hooks | Angles & Hooks Architect | ≥15 Angles, ≥30 Hooks, Segment-Matrix, Funnel-Priorisierung |
| Brand Strategy | Brand Architect (optional) | Positioning, Voice, Messaging Hierarchy |

### Was aus dem Avatar gebraucht wird

- **Section B (Context Profile):** Segment-Definitionen, Firmengröße, Branche
- **Section E (Pain/Gain/Anxiety):** Primäre Schmerzpunkte für Copy
- **Section F (Desire & Identity):** Aspirations-Trigger
- **Section G (Belief System):** Hindernisse für Objection-Handling
- **Section H (Voice of Customer):** Trigger-Wörter, echte Sprache, Zitate
- **Section I (Segmentation):** Segment-Namen und -Gewichtung

### Was aus Angles & Hooks gebraucht wird

- Alle Angles mit ID, Name, Funnel-Stufe, Segment, Trigger
- Alle Hooks mit ID, Text, Angle-Ref, Char-Count, Hook-Typ, Segment
- Funnel-Priorisierung (TOFU/MOFU/BOFU Top 5)
- Segment × Angle Matrix mit Trigger-Wörtern

---

## Technologische Grundlage (Meta Ads 2026)

### Algorithmus-Stack

| Komponente | Funktion | Relevanz für Setup |
|------------|----------|-------------------|
| **Andromeda Retrieval** | Ad-Verteilung (NVIDIA GH200, 100x schneller) | Confident setzen — Algorithmus verteilt besser als manuell |
| **GEM Model** | Prädiktive Genauigkeit 87%, 3.5% Lift Ad Clicks | Genug Conversion-Daten füttern → bessere Verteilung |
| **Meta Lattice** | 12% Anzeigenqualitäts-Steigerung | Advantage+ Creative nutzen |
| **Advantage+ AI** | 22% ROAS-Verbesserung vs. manuell | CBO + Advantage+ Audience als Default |

### Implikation für Kampagnen-Setup

- **Weniger Ad Sets, mehr Creatives** — Algorithmus braucht Varianten, nicht Segmentierung
- **Creative = Targeting** — Meta scannt visuelle Elemente, Audio, Text zur Audience-Zuordnung
- **Broad Targeting bevorzugen** — 1-3% Targeting-Expansion in Settings
- **Frequenz von Meta steuern lassen** — Cold + Warm in einer Kampagne, Meta trennt automatisch

---

## Output Structure

Das Skill produziert **EINE Markdown-Datei** mit folgenden Sections:

```
A — Kampagnenarchitektur
B — Ad Sets & Audience Mapping
C — Creative Production Plan
D — Full Ad Copy (Meta-ready)
E — Technical Setup Checklist
F — Performance Framework
G — DACH Compliance
H — Scaling Playbook
🧠 — Learned Patterns
```

---

## Section A — Kampagnenarchitektur

### A1 — Campaign Structure (Power of One)

**Grundregel:** Maximal 3 Kampagnen gleichzeitig. Konsolidieren statt fragmentieren.

| Kampagne | Objective | Budgeting | Zweck |
|----------|-----------|-----------|-------|
| **Sales Campaign** | Conversions (Sales/Leads) | CBO / Advantage+ | Haupt-Umsatztreiber, 60-70% Budget |
| **Testing Campaign** | Conversions | ABO | Neue Angles/Creatives testen, 20-30% Budget |
| **Awareness Campaign** (optional) | Reach / Video Views | CBO | Retargeting-Funnel befüllen, 10-20% Budget |

**Regeln:**
- Sales Campaign: Advantage+ Audience aktiviert, mindestens 5 Ad Sets, je 3-5 Creatives
- Testing Campaign: ABO für kontrollierte Tests, je 1 Angle pro Ad Set, 2-3 Creatives
- Awareness Campaign: Nur wenn Retargeting-Pool < 10.000 Personen in 7 Tagen
- **Never:** Mehr als 3 aktive Kampagnen gleichzeitig

### A2 — Budget Allocation

| Phase | Sales | Testing | Awareness | Woche |
|-------|-------|---------|-----------|-------|
| **Launch (Woche 1-2)** | 50% | 40% | 10% | Algorithmus-Lernen |
| **Optimize (Woche 3-4)** | 65% | 25% | 10% | Winner konsolidieren |
| **Scale (Woche 5+)** | 70% | 20% | 10% | Konzepte skalieren |

**Minimum Budget für Lernphase:**
- Ad Set braucht 50-70 Konversionen/Woche → CPA × 70 = min. Weekly Budget pro Ad Set
- Beispiel: CPA €35 → min. €2.450/Woche pro Ad Set
- Bei kleiner Budgets: Weniger Ad Sets, nicht weniger Budget pro Ad Set

### A3 — Targeting Strategy

| Layer | Targeting-Typ | Größe | Einsatz |
|-------|--------------|-------|---------|
| **Broad** | Advantage+ Audience | 1M+ | Default für Sales Campaign |
| **Lookalike** | 1%, 3%, 5% LAL auf Kundenliste | 2M-10M | Wenn ≥1.000 Customer-Seed |
| **Interest** | 3-5 Interessen pro Ad Set | 500K-2M | Nur für Testing Campaign |
| **Custom** | Website-Visitor, Engager, CRM-List | Variabel | Retargeting/Funnel-Step |
| **Exclusions** | Kunden (365d), Recent Converter (7d) | — | IMMER setzen |

**Targeting-Regeln:**
- Broad + Advantage+ = Default für Sales. Nicht komplizierter machen als nötig.
- Lookalike: Seed-List muss ≥1.000 Nutzer haben, Top-Kunden bevorzugen (nicht alle)
- Interest-Targeting: Max 3-5 Interessen pro Ad Set. Keine Interest-Stacking-Simulation.
- Custom Audiences ≥300 für Retargeting, ≥1.000 für Lookalike-Seeds

### A4 — Funnel Integration

```
TOFU (Awareness)          MOFU (Consideration)      BOFU (Conversion)
     │                          │                          │
     ▼                          ▼                          ▼
Awareness Campaign       Testing Campaign          Sales Campaign
(Retargeting befüllen)   (Neue Angles testen)      (Hauptumsatz)
     │                          │                          │
  Broad/LAL               Interest + LAL            Custom + LAL
  Pain Hooks              Solution Hooks            Trust Hooks
  Story-Opener            Specific Number           Testimonial
  Question                Statement                 Challenge
```

**TOFU-Creatives → MOFU-Testing → BOFU-Sales.** Nicht mischen in einem Ad Set.

---

## Section B — Ad Sets & Audience Mapping

### B1 — Audience-Definition pro Funnel-Stufe

#### TOFU Ad Sets (Awareness)

| Ad Set | Targeting | Size Guide | Exclusions | Events |
|--------|-----------|------------|------------|--------|
| Broad DE/AT/CH | Advantage+ Audience, Geo: DACH | 5M+ | Kunden 365d | PageView, ViewContent |
| LAL 3% | Lookalike 3% auf Customer-Liste | 2-5M | Kunden 365d | PageView, ViewContent |
| Interest Stack | 3-5 branchennahe Interessen | 500K-2M | Kunden 365d, Website-Visitor | PageView, ViewContent |

#### MOFU Ad Sets (Consideration)

| Ad Set | Targeting | Size Guide | Exclusions | Events |
|--------|-----------|------------|------------|--------|
| Website Visitor 7d | Custom: PageView letzte 7 Tage | Variabel | Recent Converter 7d | AddToCart, InitiateCheckout, Lead |
| Engager 30d | Custom: IG/FB Engagement letzte 30d | Variabel | Kunden 365d | Lead, ViewContent |
| Video Viewer 75% | Custom: Video ≥75% gesehen, 30d | Variabel | Kunden 365d | AddToCart, Lead |

#### BOFU Ad Sets (Conversion)

| Ad Set | Targeting | Size Guide | Exclusions | Events |
|--------|-----------|------------|------------|--------|
| Cart Abandoner 3d | Custom: InitiateCheckout, keine Purchase 3d | Klein | Recent Converter 7d | Purchase, CompleteRegistration |
| LAL 1% | Lookalike 1% auf Customer-Liste | 1-2M | Kunden 365d | Purchase, CompleteRegistration |
| CRM Re-Engage | Custom: CRM-Liste (inactive 30-90d) | Variabel | Active Kunden 30d | Purchase, Lead |

### B2 — Segment × Ad Set Matrix

| Segment | TOFU Ad Set | MOFU Ad Set | BOFU Ad Set | Priority |
|---------|-------------|-------------|-------------|----------|
| Seg A (Primary) | Broad + Interest | Website Visitor + Engager | LAL 1% + Cart | 1 |
| Seg B (Secondary) | Broad + LAL 3% | Video Viewer + Engager | CRM Re-Engage | 2 |
| Seg C (Tertiary) | Interest Stack | Engager | LAL 1% | 3 |

**Regel:** Segmente werden NICHT als separates Targeting gesetzt. Stattdessen: Creatives pro Segment produzieren, Algorithmus.matched durch visuelle Signale.

### B3 — CAPI Event Mapping

| Funnel-Stufe | Meta Pixel Event | CAPI Event | Parameter | Hashing |
|-------------|-----------------|------------|-----------|---------|
| TOFU | PageView | page_view | url, user_agent | ✓ |
| TOFU | ViewContent | view_content | content_ids, content_type, currency, value | ✓ |
| MOFU | AddToCart | add_to_cart | content_ids, content_name, currency, value | ✓ |
| MOFU | AddToWishlist | add_to_wishlist | content_ids, value | ✓ |
| MOFU | InitiateCheckout | initiate_checkout | content_ids, num_items, currency, value | ✓ |
| MOFU | Lead | lead | currency, value | ✓ |
| BOFU | Purchase | purchase | content_ids, num_items, currency, value | ✓ |
| BOFU | CompleteRegistration | complete_registration | currency, value, status | ✓ |

**Alle Parameter die PII enthalten (email, phone, first_name, last_name, city, zip, country, gender, dob) MÜSSEN SHA-256 gehasht werden.**

---

## Section C — Creative Production Plan

### C1 — Creative Archetypes

| Archetyp | Beschreibung | Funnel-Stufe | Performance |
|----------|-------------|-------------|-------------|
| **Ugly Ad** | Low-Fi, authentic, handgemacht | TOFU | Shock-Wert, hohe CTR |
| **Founder Story** | Persönliche Erzählung, Behind-the-Scenes | TOFU/MOFU | Vertrauensaufbau, hohe Engagement-Rate |
| **Us vs. Them** | Kontrast: Problem-Solution, Before-After | MOFU | Klare Wert-Kommunikation |
| **Problem-Aggregator** | Multiple Pain-Points aufgelistet | TOFU | Resonanz durch Wiedererkennung |
| **Review-Stack** | Mehrere Testimonials/Reviews aggregiert | MOFU/BOFU | Social Proof, hohes Vertrauen |
| **UGC (User Generated)** | Echte Nutzer, Smartphone-Qualität | Alle Stufen | 40% bessere Performance als Studio |

### C2 — Visuelle Specs 2026

**Mobile-First: 94-98% Traffic ist mobil → 9:16 ist der Standard.**

| Format | Auflösung | Aspect Ratio | Einsatz |
|--------|-----------|-------------|---------|
| Stories/Reels | 1080×1920 | 9:16 | Primäres Format (80%+) |
| Feed | 1080×1080 | 1:1 | Secondary Format |
| Landscape | 1200×628 | ~1.91:1 | Desktop/Premium Placements |

### C3 — Safe Zones (9:16 — Stories/Reels)

```
┌─────────────────────────┐
│     SAFE ZONE (TOP)     │ ← Top 250px frei halten
│     250px               │    (Swipe-Indicator, Username, Zeit)
│─────────────────────────│
│                         │
│    CONTENT AREA         │ ← Hauptinhalt hier platzieren
│    (Zentral, 5-10%      │
│     Seitenpuffer)       │
│                         │
│─────────────────────────│
│     CTA ZONE            │ ← Bottom 340px für CTA
│     340px               │    (CTA-Button, Text, Link)
└─────────────────────────┘
```

**Safe Zone Checkliste:**
- [ ] Top 250px: KEIN Text, KEIN Logo, KEIN wichtiges Element
- [ ] Bottom 340px: CTA-Button sichtbar, Description lesbar
- [ ] Seiten: 5-10% Puffer links/rechts (54-108px bei 1080px Breite)
- [ ] Text-Overlay: Min 40px Schriftgröße für Lesbarkeit auf Mobile
- [ ] Duration: 15-30s optimal, max 60s für Reels

### C4 — Angle → Creative Mapping

Für jeden Angle aus dem Angles & Hooks Dokument:

```yaml
creative_plan:
  angle_id: "A1"
  angle_name: "Name des Angles"
  funnel_stage: "TOFU|MOFU|BOFU"
  primary_segment: "Segment-Name"
  
  variants:
    - variant: 1
      archetype: "Ugly Ad|Founder Story|Us vs. Them|..."
      format: "9:16 Video|9:16 Static|1:1 Static"
      hook_visual: "Beschreibung des visuellen Hooks in < 2 Sekunden"
      ugc_or_studio: "UGC|Studio|Hybrid"
      video_spec:
        duration: "15s"
        hook_timing: "0-2s: [visueller Hook beschreiben]"
        caption_style: "groß, zentriert, gelb auf dunkel"
        cta_timing: "12-15s"
      static_spec:
        headline_overlay: "max 6 Wörter, Arial Bold 48px"
        color_scheme: "Brand-Farben"
        text_position: "Zentral, Safe Zone gewahrt"
      safe_zone_compliance: "✓|✕ [Begründung bei ✕]"
```

### C5 — UGC vs. Studio Empfehlung

| Kriterium | UGC bevorzugen | Studio bevorzugen |
|-----------|---------------|-------------------|
| Budget | < €5.000 Production-Budget | ≥ €5.000 |
| Produkt | Dienstleistung, Beratung, Software | Lifestyle, Beauty, Food |
| Zielgruppe | < 35 Jahre, Social-Native | ≥ 35 Jahre, Premium |
| Funnel | TOFU/MOFU | BOFU |
| Test-Phase | Ja — schnell, günstig, authentisch | Nein — zu teuer für Tests |

**KI-gestützte Produktion (CRAFTED-Ansatz):**
- C = Concept (aus Angles & Hooks)
- R = Render (Remotion Templates, V4-Serie)
- A = Audio (ElevenLabs, AI Voiceover)
- F = Faces (Nano Banana für KI-generierte Gesichter)
- T = Text (Copy aus Section D)
- E = Edit (Schnitte, Safe Zones, Captions)
- D = Deliver (Meta-ready, alle Formate)

---

## Section D — Full Ad Copy (Meta-ready)

### D1 — Character Limits (STRIKT)

| Element | Limit | Sichtbar | Regel |
|---------|-------|----------|-------|
| Primary Text | 2.200 Zeichen | **≤125 Zeichen** | Hook in den ersten 125 Zeichen! |
| Headline | 40 Zeichen | 40 Zeichen | Komplett sichtbar |
| Description | 30 Zeichen | 30 Zeichen | Ergänzend zur Headline |
| URL Display | 40 Zeichen | 40 Zeichen | Klare Domain/Pfad |

### D2 — Copy Template pro Angle

Für jeden Angle ≥3 Ad Variants:

```yaml
ad_variant:
  angle_ref: "A1"
  variant_id: "A1-V1"
  segment_tag: "Segment A, Segment B"
  funnel_stage: "TOFU"
  
  primary_text: "Hook in ≤125 Zeichen. Rest des Textes ist Zusatzinfo..."
  primary_text_visible_chars: 122
  headline: "≤40 Zeichen Headline"
  headline_chars: 38
  description: "≤30 Zeichen Desc"
  description_chars: 28
  call_to_action: "Mehr erfahren|Jetzt starten|Angebot ansehen|Kostenlos testen"
  
  platform_tags: ["Feed", "Stories", "Reels"]
  hook_ref: "H3"
  hook_type: "Question"
  
  quality_checks:
    primary_text_under_125: true
    headline_under_40: true
    description_under_30: true
    no_marketing_fluff: true
    avatar_language_match: true
```

### D3 — Copywriting-Regeln

**BOFU: "Why I Finally Bought" Einwandbehandlung**
- 3-4x höhere Konversion als reguläre BOFU-Copy
- Struktur: Einwand erkennen → Eigener Zweifel → Warum es trotzdem geklappt hat → CTA
- Beispiel: "Ich dachte auch, das geht nicht. Bis ich X gesehen habe..."

**Hook < 2 Sekunden:**
- Erste 125 Zeichen des Primary Text = Hook
- Visueller Hook im Video < 2 Sekunden
- Headline muss allein Sinn ergeben (wird ohne Context gelesen)

**CTA-Auswahl:**

| Funnel | CTA-Optionen | Wann |
|--------|-------------|-----|
| TOFU | Mehr erfahren, Jetzt ansehen | Awareness, kein Kauf |
| MOFU | Jetzt starten, Angebot ansehen | Consideration, Soft-Commit |
| BOFU | Jetzt kaufen, Kostenlos testen | Conversion, Clear Intent |

### D4 — BOFU-Einwand-Handling Copy

Für BOFU-Variants: Max 3 Einwände aus dem Avatar (Section G — Belief System) adressieren:

| Einwand | Copy-Pattern | Beispiel |
|---------|-------------|---------|
| Preis zu hoch | ROI-Reframe | "Die Investition hat sich in 6 Wochen rentiert." |
| Zu kompliziert | Einfachheits-Beweis | "Alles erledigt, ohne einen Finger zu rühren." |
| Vertrauen | Social Proof Stack | "Über 200 Familien haben uns vertraut." |
| Zeit | Geschwindigkeits-Versprechen | "In 2 Wochen everything online." |
| Risiko | Garantie/Risiko-Umkehr | "30 Tage Geld-zurück, kein Risiko." |

---

## Section E — Technical Setup Checklist

### E1 — Pixel Installation

```yaml
pixel_setup:
  meta_pixel_id: "[PIXEL_ID]"
  installation_method: "Tag Manager empfohlen"
  base_code: "Auf ALLEN Seiten im <head>"
  event_code: "Nach Base Code, auf relevanten Seiten"
  
  pages:
    - page: "Alle Seiten"
      event: "PageView"
      trigger: "automatisch"
    - page: "/produkt/*"
      event: "ViewContent"
      trigger: "automatisch"
    - page: "/warenkorb"
      event: "AddToCart"
      trigger: "Button-Click oder Page Load"
    - page: "/checkout"
      event: "InitiateCheckout"
      trigger: "Page Load"
    - page: "/danke"
      event: "Purchase"
      trigger: "Page Load"
    - page: "/kontakt/*"
      event: "Lead"
      trigger: "Form Submit"
  
  checks:
    - pixel_fires_on_all_pages: "[ ] getestet"
    - events_fire_correctly: "[ ] getestet mit Meta Pixel Helper"
    - no_duplicate_pixels: "[ ] geprüft"
    - page_load_impact: "[ ] < 100ms 추가 Latenz gemessen"
```

### E2 — CAPI Configuration (Conversions API)

**CAPI ist obligatorisch.** Ohne CAPI gehen 60% der Conversions durch ATT, Ad-Blocker, Post-Cookie verloren.

```yaml
capi_setup:
  endpoint: "https://graph.facebook.com/v21.0/{PIXEL_ID}/events"
  access_token: "[CAPI_TOKEN]"
  method: "POST"
  
  required_parameters:
    - "event_name (string)"
    - "event_time (unix timestamp)"
    - "event_source_url (string)"
    - "user_data (object — hashed)"
    - "action_source (string: website|physical_store|other)"
    - "event_id (string — für Deduplikation)"
  
  hashing:
    method: "SHA-256"
    lowercase_first: true
    trim_whitespace: true
    fields_to_hash: ["email", "phone", "first_name", "last_name", "city", "zip", "country", "gender", "dob"]
  
  deduplication:
    method: "event_id Übereinstimmung"
    rule: "Gleiche event_id im Pixel und CAPI = 1 Conversion zählen"
    format: "uuid4 oder deterministic: {timestamp}_{user_email_hash}_{event_name}"
```

### E3 — Event Match Quality Guide

**Ziel: Score > 8. Unter 7 = deutlicher Datenverlust.**

| Parameter | Impact auf Score | Aktion |
|-----------|-----------------|--------|
| email (hashed) | +++ | IMMER senden wenn verfügbar |
| phone (hashed) | +++ | Auf Checkout-Seite erfassen |
| fbp Cookie | ++ | Automatisch vom Pixel |
| fbc Cookie | ++ | Automatisch vom Pixel |
| client_ip_address | ++ | Server-seitig erfassen |
| client_user_agent | ++ | Server-seitig erfassen |
| city (hashed) | + | Adresse erfassen |
| zip (hashed) | + | PLZ erfassen |
| country (hashed) | + | Automatisch |
| dob (hashed) | + | Nur wenn verfügbar |
| gender (hashed) | + | Nur wenn verfügbar |
| external_id | ++ | CRM-ID wenn vorhanden |

**Score-Formel:**
- Alle 5 „+++" Felder → Score 9-10
- email + fbp/fbc + ip + ua → Score 8
- Nur email → Score 6-7
- Keine PII → Score 1-3 (unbrauchbar)

### E4 — Domain Verification & AEM

```yaml
domain_setup:
  domain_verification:
    method: "DNS TXT Record"
    check: "Meta Business Manager → Brand Safety → Domains"
  
  aggregated_event_measurement:
    priority_events: "Purchase, Lead, CompleteRegistration (Top 3)"
    setup: "Events Manager → Aggregated Event Measurement"
    note: "Nur 8 Events konfigurierbar. Conversion-Events oben priorisieren."
```

### E5 — UTM Structure

```
utm_source=facebook
utm_medium=cpc
utm_campaign=[KAMPAGNENNAME]
utm_content=[AD_SET_NAME]_[ANGLE_ID]_[VARIANT_ID]
utm_term=[AUDIENCE_TYPE]

Beispiel:
utm_source=facebook&utm_medium=cpc&utm_campaign=sales_q2_2026&utm_content=broad_tofu_a1_v2&utm_term=advantage_plus
```

**Regeln:**
- utm_source: IMMER "facebook" (auch für Instagram)
- utm_medium: IMMER "cpc"
- utm_campaign: Kampagnenname aus Meta Ads Manager
- utm_content: Kombination aus Ad Set + Angle + Variant für granulares Tracking
- utm_term: Targeting-Typ (broad, lal_3pct, retarget_web_7d, etc.)

---

## Section F — Performance Framework

### F1 — KPIs pro Funnel-Stufe

| Funnel | Kampagne | Primary KPI | Secondary KPIs | DACH Benchmark |
|--------|----------|-------------|----------------|----------------|
| TOFU | Awareness | CPM | Reach, Video View Rate (ThruPlay) | CPM: $6.50-$12 |
| MOFU | Testing | CPC, CTR | Frequency, Landing Page View Rate | CPC: $0.65-$1.30, CTR: 1.8-2.4% |
| BOFU | Sales | CPA, ROAS | Conversion Rate, BLT (Best Landing Time) | CPA E-Commerce: $28-$42 |
| Overall | — | CAC ( blended) | LTV:CAC Ratio | ROAS 2.5x-4.5x |

### F2 — Reporting Cadence

| Frequenz | Was | Wer | Tool |
|----------|-----|-----|------|
| Täglich | Spend-Pacing, Anomalien | Media Buyer | Meta Ads Manager |
| Wöchentlich (Montag) | KPIs vs. Target, Top/Bottom Ads, Frequency | Media Buyer | Meta + GA4 Dashboard |
| 2-Wöchentlich | Attribution-Vergleich (Meta vs. GA4), CPMr-Trend | Strategie | Custom Dashboard |
| Monatlich | Kampagnen-ROAS, Creative Fatigue Analyse, Skalierungs-Review | Lead + Media Buyer | Vollständiger Report |

### F3 — CPMr Frühwarnsystem

**CPMr = Cost Per Mille Reached** (nicht CPM = Cost Per Mille Impressions)

```
CPMr = (Spend / Reach) × 1.000

Normale Woche:       CPMr stabil (±10%)
Creative Fatigue:    CPMr steigt >20% Woche-über-Woche
Aktion bei Fatigue:  Neue Creatives starten, fatigue Ad pausieren
```

| CPMr-Woche | Veränderung | Status | Aktion |
|-----------|------------|--------|--------|
| Woche 1 | — | Baseline | Merken |
| Woche 2 | ±10% | Normal | Nichts |
| Woche 3 | +10-20% | Warning | Neue Creatives in Produktion geben |
| Woche 4 | >+20% | Fatigue | Alte Creatives pausieren, neue starten |
| Woche 5 | >+30% | Kritisch | Sofort-Refresh, Budget temporär reduzieren |

### F4 — Inkrementelle Attribution

Meta-Attribution überzeichnet um 30-50%. Inkrementelle Messung liefert echte Geschäftsergebnisse (+46% Genauigkeit).

**Setup:**
1. **Geo-Lift Test:** 2 Regionen, eine mit Ads, eine ohne → Conversion-Delta = inkrementeller Effekt
2. **Conversion Lift:** Meta-eigenes Tool (Events Manager → Conversions API → Test & Learn)
3. **Marketing Mix Modeling (MMM):** Für Budget ≥ €10.000/Monat sinnvoll

**Minimum Voraussetzung:**
- 14+ Tage Laufzeit
- ≥50 Conversions in Test-Region
- Max 30% des Budgets in Test

### F5 — Budget-Optimierung (20%-Regel)

**Max 20% Budget-Änderung pro Woche pro Ad Set.** Mehr → Algorithmus-Reset.

| Aktion | Max Änderung | Wartezeit vor nächster Änderung |
|--------|-------------|-------------------------------|
| Budget erhöhen | +20% | 3 Tage |
| Budget senken | -20% | 3 Tage |
| Budget verdoppeln | +20% → 3 Tage → +20% → 3 Tage → ... | Stufenweise! |
| Ad Set pausieren | -100% | Neuer Ad Set → neue Lernphase |
| Neuer Ad Set | +100% (neu) | 7 Tage Lernphase minimum |

### F6 — Creative Refresh Cadence

| Spend-Level | Aktive Creatives | Refresh-Zyklus |
|-------------|-----------------|----------------|
| < €500/Tag | 10-15 | Alle 3 Wochen |
| €500-€1.000/Tag | 15-30 | Alle 2 Wochen |
| > €1.000/Tag | 30-50 | Wöchentlich |

**Regel:** Jede Woche 3-5 neue Creatives hinzufügen, 2-3 fatigue Ads entfernen.

---

## Section G — DACH Compliance

### G1 — DSGVO Checkliste

- [ ] **Privacy Policy aktualisiert** — Meta Pixel und CAPI explizit erwähnt
- [ ] **Cookie Banner implementiert** — Consent vor Pixel-Aktivierung
- [ ] **Datenschutzerklärung** — Empfänger: Meta Platforms Ireland Ltd. aufgeführt
- [ ] **Verarbeitungsverzeichnis** — Meta Ads als Datenverarbeitungstätigkeit erfasst
- [ ] **Auftragsverarbeitungsvertrag (AVV)** — mit Meta abgeschlossen (in Business Settings)
- [ ] **Datenminimierung** — Nur notwendige Parameter an Meta senden
- [ ] **Löschkonzept** — User-identifizierende Daten regelmäßig löschen
- [ ] **Consent-Management** — CMP (Cookiebot, Usercentrics, etc.) korrekt integriert
- [ ] **Server-Side Tracking** — CAPI nur mit Consent oder legitimate interest (DACH: Consent empfohlen)

### G2 — DMA Compliance (Digital Markets Act)

- [ ] **Consent-for-Ads implementiert** — 3 Stufen:
  - Personalisierte Werbung (volles Targeting, CAPI, Pixel)
  - Weniger personalisierte Werbung (kontextbezogen)
  - Werbefrei
- [ ] **Opt-out Mechanismus** klar kommuniziert und funktional
- [ ] **Keine Cross-App-Tracking-Defaults** — User muss aktiv zustimmen
- [ ] **Transparenzbericht** — User können einsehen, welche Daten geteilt werden

**Auswirkung auf Performance:**
- 15-30% der User wählen „weniger personalisiert" oder „werbefrei"
- Nur Consent-User → kleinerer Pool, aber qualitativ besser
- CAPI funktioniert NUR bei Consent → kein Workaround legal

### G3 — Special Ad Categories

Meta unterteilt in Special Ad Categories mit Einschränkungen:

| Category | Einschränkung | Relevant wenn |
|----------|--------------|---------------|
| **Housing** | Kein Targeting nach Alter, Geschlecht, PLZ | Immobilien, Miete |
| **Employment** | Kein Targeting nach Alter, Geschlecht | Jobs, Recruiting |
| **Credit** | Kein Targeting nach Alter, Geschlecht | Finanzprodukte, Kredite |
| **Social Issues** | Label-Pflicht | Politik, gesellschaftliche Themen |
| **Keine Special Category** | Normales Targeting | Die meisten B2B/B2C Kampagnen |

**Aktion:** Bei Kampagnen-Setup prüfen ob Special Ad Category zutrifft → entsprechend taggen.

### G4 — Impressum & Disclaimer Requirements

**Deutschland (TMG §5):**
- [ ] Impressum auf Landing Page erreichbar
- [ ] Werbe-Posts auf FB/IG als Werbung gekennzeichnet („Anzeige" oder „Werbung")
- [ ] Bei Preisangaben: Grundpreis, Versandkosten, Verfügbarkeit
- [ ] Bei Testimonials: Echtheit nachweisbar
- [ ] Bei Vergleichswerbung: Nach TMG §6 sachlich, nicht irreführend
- [ ] Kennzeichnung von KI-generierten Inhalten (KI-VO ab 2026 beachten)

**Österreich & Schweiz:**
- Ö: Impressumspflicht nach ECG
- CH: Impressum nach UWG (nur bei kaufmännischem Verkehr)

### G5 — DACH-spezifische Benchmarks

| Metrik | Deutschland | Österreich | Schweiz | USA (Vergleich) |
|--------|------------|-----------|---------|-----------------|
| CPM | $6.50-$12 | $5.50-$10 | $7-$14 | $5-$9 |
| CPC | $0.65-$1.30 | $0.55-$1.10 | $0.70-$1.40 | $0.50-$1.00 |
| CTR | 1.8-2.4% | 1.6-2.2% | 1.5-2.1% | 1.5-2.5% |
| CPA (E-Commerce) | $28-$42 | $24-$38 | $30-$48 | $18-$30 |

**Erklärung für höhere DACH-CPMs:** Consent-Modell reduziert Targetable-Audience um 15-30%, dafür aber kein Abo-Modell in DACH → höhere competition auf kleinere Pools.

---

## Section H — Scaling Playbook

### H1 — Konzept-Skalierung (NICHT Anzeigen-Skalierung)

**Der häufigste Fehler:** Eine gute Anzeige mit mehr Budget pushen → Algorithmus-Reset.

**Richtiges Vorgehen:**

```
1. Winning Angle identifizieren (nicht winning Ad)
2. Konzept skalieren: 5-10 neue Creatives für denselben Angle
3. In Testing Campaign starten (ABO)
4. Wenn konstant gut → in Sales Campaign überführen
5. Budget stufenweise +20% alle 3 Tage
```

| Was tun | Was NICHT tun |
|---------|--------------|
| Konzepte testen → Winner skalieren | Einzelne Ads pushen |
| 5-10 Varianten pro Konzept | 1-2 Varianten mit hohem Budget |
| Stufenweise +20% Budget | Budget über Nacht verdoppeln |
| Neue Creatives vor Fatigue | Fatigue abwarten |
| Advantage+ nutzen | Micro-Targeting optimieren |

### H2 — Wöchentlicher Kadenz-Plan

| Tag | Aktivität | Wer | Dauer |
|-----|-----------|-----|-------|
| **Montag** | Performance Review, KPIs checken, CPMr-Trend | Media Buyer | 1-2h |
| **Dienstag** | Neue Angles/Hooks ableiten aus Performance-Daten | Strategie | 1h |
| **Mittwoch** | Creative-Produktion (UGC-Aufnahmen, Remotion-Render) | Creative Team | 2-4h |
| **Donnerstag** | Neue Creatives hochladen, neue Tests starten | Media Buyer | 1h |
| **Freitag** | Wochen-Report, Learnings dokumentieren | Media Buyer | 30min |
| **Wochenende** | **NO-TOUCH** — Algorithmus braucht Ruhe | — | — |

### H3 — Budget-Tapering Regeln

**Für Skalierung über €5.000/Woche:**

```
Woche 1: €2.500 (Baseline)
Woche 2: €3.000 (+20%)
Woche 3: €3.600 (+20%)
Woche 4: €4.320 (+20%)
Woche 5: €5.184 (+20%)
Woche 6: €6.220 (+20%)
```

**Oder: Horizontal Scale (bevorzugt bei Budget > €10.000/Woche):**
- Neue Kampagne mit gleichem Setup, geteiltem Budget
- Beide Kampagnen parallel laufen lassen
- Gewinner nach 14 Tagen konsolidieren

### H4 — Creative Testing Roadmap (4-Week Rotation)

| Woche | Fokus | Neue Creatives | Pausierte Creatives |
|-------|-------|----------------|-------------------|
| Woche 1 | Neue Angles testen | 5-7 (alle TOFU) | 0 |
| Woche 2 | Winners tiefer testen | 3-5 (MOFU Varianten von W1-Winnern) | 2 (W1 Flops) |
| Woche 3 | BOFU-Varianten + Cross-Segment | 3-5 (BOFU, andere Segmente) | 2 (W2 Flops) |
| Woche 4 | Consolidation + Refresh | 3-5 (Refresh der W1-Winner) | 2 (Fatigue) |

**Am Ende von Woche 4:** Alle Learnings dokumentieren → neue Angles für nächste Runde ableiten → Zyklus beginnt von vorn.

---

## Execution Flow

### Step 1 — Input sammeln

```
 Lies Customer Avatar → Sections B, E, F, G, H, I
 Lies Angles & Hooks → Alle Angles, Hooks, Matrix
 Lies Brand Strategy → Positioning, Voice (optional)
```

### Step 2 — Kampagnenstruktur definieren (Section A)

```
 1. Campaign Structure festlegen (Sales + Testing + optional Awareness)
 2. Budget-Allocation berechnen
 3. Targeting-Strategy bestimmen (Broad/LAL/Interest/Custom)
 4. Funnel-Integration planen (TOFU→MOFU→BOFU)
```

### Step 3 — Audience Mapping (Section B)

```
 1. Ad Sets pro Funnel-Stufe definieren
 2. Segment × Ad Set Matrix erstellen
 3. CAPI Events zuordnen
 4. Exclusions definieren
```

### Step 4 — Creative Plan (Section C)

```
 1. Pro Angle: Archetyp, Format, Hook-Visual festlegen
 2. Safe Zone Check für jedes Creative
 3. UGC vs. Studio Entscheidung
 4. Video & Static Specs definieren
```

### Step 5 — Copy schreiben (Section D)

```
 1. Pro Angle ≥3 Ad Variants erstellen
 2. ALLE Character Limits validieren
 3. BOFU: Einwand-Handling Copy
 4. Hook-Referenz prüfen (jeder Hook muss verwendet werden)
```

### Step 6 — Technical Setup (Section E)

```
 1. Pixel-Checkliste ausfüllen
  2. CAPI Events + Hashing definieren
  3. Event Match Quality Score berechnen
  4. UTM Structure definieren
```

### Step 7 — Performance & Compliance (Sections F-G)

```
 1. KPIs pro Funnel/Kampagne
  2. CPMr System definieren
  3. DACH Compliance Checkliste durchgehen
  4. Scaling Playbook anpassen
```

### Step 8 — Quality Gates

```
 □ Jeder Hook aus Angles & Hooks in mindestens einer Ad Variant?
 □ Alle Character Limits validiert (Primary ≤125, Headline ≤40, Desc ≤30)?
 □ Alle Safe Zones eingehalten?
 □ DACH Compliance gecheckt (DSGVO, DMA, Special Ad Categories)?
 □ CAPI Events vollständig definiert?
 □ BOFU Einwand-Handling Copy vorhanden?
 □ Mindestens 1 UGC-Empfehlung pro Angle?
 □ Segment-Tags auf allen Ad Variants?
```

---

## Quality Gates (zusammengefasst)

| Gate | Check | Methode |
|------|-------|---------|
| **Hook Coverage** | Jeder Hook ≥1x in Ad Copy | Hook-IDs aus Angles & Hooks abgleichen |
| **Character Limits** | Primary ≤125, Headline ≤40, Desc ≤30 | Automatischer Count pro Variant |
| **Safe Zones** | Top 250px frei, Bottom 340px CTA, 5-10% Seitenpuffer | Visueller Check pro Creative |
| **DACH Compliance** | DSGVO, DMA, Special Ad Categories, Impressum | Checkliste durchgehen |
| **CAPI Events** | Alle Funnel-Events definiert, SHA-256 Hashing | Event-Mapping abgleichen |
| **Einwand-Handling** | BOFU Copy adressiert Avatar-Beliefs | Section G Beliefs × BOFU Variants |
| **Segment Coverage** | Jedes Segment hat ≥2 Angles | Matrix-Check |
| **Platform Tags** | Jede Variant hat Feed/Stories/Reels Tags | Variant-Check |

---

## Remotion Integration

Für Video-Creative-Produktion die bestehende Remotion Pipeline nutzen:

- **Templates:** ITSecurityAdV4.tsx, Glassmorphism-Template, Safe Zone Templates
- **Skill:** `/data/workspace/skills/remotion-creative-pipeline/SKILL.md`
- **Workspace:** `/data/workspace/remotion-test`
- **Render:** `npx remotion render src/Root.tsx <CompositionID> --output file.mp4`
- **Stills:** `npx remotion still src/Root.tsx <CompositionID> --frame N --output file.png`

**Workflow:**
1. Angle + Hook → Copy aus Section D
2. Copy → Remotion Template (via CRAFTED-Ansatz)
3. Render als 9:16 Video + 1:1 Static (Still)
4. Safe Zone Check → Upload to Meta Ads Manager

---

## 🧠 Learned Patterns

### 2026-04-13 — Skill nicht gelesen = Halluzination
- **KRITISCH:** Wenn ein SubAgent diesen Skill nicht liest, produziert er Interest-Targeting im Sales Campaign und ignoriert UGC. Das sind die zwei häufigsten Fehler.
- **FIX:** Coordinator MUSS im SubAgent-Prompt den Skill-Path explizit nennen und die Kernregeln (Broad Default, UGC First) als STRIKT-Markierung wiederholen.
- **Pattern:** SubAgent greift auf generisches LLM-Wissen zurück → "Interest-Targeting ist valide" → Interest-Ad-Sets überall → Algorithmus hat zu wenig Daten → Performance einbricht.
- Interest-Targeting ist NUR für die Testing Campaign (ABO), NIEMALS für die Sales Campaign (CBO/Advantage+).
- UGC konvertiert 40% besser als Studio-Production (nachgewiesen 2026). IMMER als Default-Archetype setzen.

### 2026-04-10 — Initial Build
- Skill ist GENERIC (avatar-agnostisch), nicht client-spezifisch. Niemals Client-Daten hartcodieren.
- „Power of One" = maximal 3 Kampagnen. Nicht fragmentieren.
- Creative Fatigue ist der größte Killer bei Skalierung. CPMr überwachen.
- DACH-CPMs sind 30-50% höher als US wegen Consent-Modell. Budget entsprechend planen.
- BOFU „Why I Finally Bought" → 3-4x höhere Konversion. IMMER einbauen.
- CAPI ist kein Nice-to-Have mehr. Ohne CAPI geht 60% der Daten verloren.
- Remotion V4 Templates für Video-Creative verfügbar. CRAFTED-Ansatz nutzen.
