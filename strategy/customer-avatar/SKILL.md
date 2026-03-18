# Deep Customer Avatar Architect

## Growing Brands Edition

---

## Purpose

Erstellt evidenzbasierte Kundenavatare auf Basis von JTBD, Job Map, Verhaltenspsychologie, Belief Systems und psycholinguistischer VoC-Analyse.

**Keine fiktionalen Personas.** Priorisierte Entscheidungsmodelle mit klaren Unsicherheiten, Segmentlogik und strategischen Implikationen.

---

## Core Principles

1. **Jobs vor Demografie** — Alter, Geschlecht, Einkommen sind Nebenvariablen. Primär: Situation, Job, Motivation, Constraint, Transformation.
2. **Nur evidenzgestützte Aussagen** — Jede Aussage bekommt einen Evidenzstatus.
3. **Trenne Beobachtung, Interpretation und Hypothese** — Keine Vermischung.
4. **Berücksichtige funktionale, emotionale und soziale Jobs** — Gleichwertig.
5. **Extrahiere Desire, Identity und Belief Systems** — Das ist der Hebel.
6. **Nutze echte Sprachmuster der Zielgruppe** — Sprache ist Verhalten.
7. **Jeder Output muss aktivierbar sein** — Für Marketing, Produkt, Sales.

---

## Evidence Status Labels

| Label | Bedeutung |
|---|---|
| `belegt` | Direkt in Rohdaten gefunden (Zitat, Metrik) |
| `stark plausibel` | Mehrfache Indizien, kein Widerspruch |
| `schwach plausibel` | Einzelnes Indiz, könnte Zufall sein |
| `offene Annahme` | Logisch geschlossen, aber nicht belegt |

---

## Workflow (8 Module)

### Modul 1: Research Intake & Evidence Normalization

**Aufgabe:** Alle Inputs in ein standardisiertes Erkenntnismodell überführen.

**Akzeptierte Inputs:**
- Interviewtranskripte
- Sales Calls
- Support Tickets
- Reviews
- Reddit/Foren-Diskussionen
- Umfragen (Offene Texte)
- CRM-Notizen
- Landingpage-Kommentare
- Callcenter-VoC
- Produktnutzungsdaten
- Marktforschungsnotizen
- Konkurrenz-Claims

**Pro Output-Einheit (Evidence Unit):**
```
source_type: string
source_id: string
quote: string (Originalzitat)
category: pain | gain | desire | belief | behavior | objection
candidate_job_stage: define | locate | prepare | confirm | execute | monitor | modify | conclude
emotional_signal: string
certainty: high | medium | low
inferred_meaning: string
```

**Schritte:**
1. Datenquellen klassifizieren
2. Dopplungen entfernen
3. Rohdaten in Evidence Units zerlegen
4. Zwischen beobachtet, interpretiert und abgeleitet unterscheiden
5. Aussagekraft pro Quelle gewichten

---

### Modul 2: JTBD Extraction Engine

**Aufgabe:** Den eigentlichen Job-to-be-Done extrahieren.

**Trenne:**
- **Funktionaler Job** — Was konkret erledigt werden soll
- **Emotionaler Job** — Wie sich die Person danach fühlen will
- **Sozialer Job** — Wie sie vor anderen erscheinen will

**Leitfragen:**
- Was versucht die Person konkret zu erledigen?
- Welchen Fortschritt will sie in ihrer Lebens-/Arbeitssituation erreichen?
- Wie will sie sich danach fühlen?
- Wie will sie vor anderen erscheinen?

**Output:**
```yaml
jtbd:
  functional_job: [list]
  emotional_job: [list]
  social_job: [list]
```

**Job-Typen unterscheiden:**
- Main Job
- Related Jobs
- Consumption Jobs
- Switching Jobs (Anbieter evaluieren, Team onboarden, intern rechtfertigen, Gesichtsverlust vermeiden)

---

### Modul 3: Job Map Deconstruction

**Aufgabe:** Den Job entlang 8 Phasen zerlegen.

**Phasen:**
1. **Define** — Problem erkennen & definieren
2. **Locate** — Lösung finden
3. **Prepare** — Vorbereitung
4. **Confirm** — Entscheidung fällen
5. **Execute** — Implementierung
6. **Monitor** — Ergebnisse prüfen
7. **Modify** — Anpassen
8. **Conclude** — Evaluieren

**Pro Phase extrahieren:**
- Ziele
- Hürden
- Fehlerquellen
- Zeitverluste
- Emotionale Friktionen
- Gewünschte Verbesserung

**Output:**
```yaml
job_map:
  <phase>:
    goals: [list]
    pains: [list]
    gains: [list]
    emotional_risk: [list]
    opportunity: [list]  # Chancen für Produkt/Kommunikation
```

**Wichtig:** Pains operationalisieren, nicht generisch.
- ❌ "möchte Zeit sparen"
- ✅ "Vorbereitungszeit vor Kernaufgabe von 18 Min auf unter 7 Min reduzieren"

---

### Modul 4: Pain–Gain–Anxiety–Desired Outcome Matrix

**Aufgabe:** Nicht nur Benefits, sondern auch Adoptionsbarrieren modellieren.

**Vier Ebenen:**
- **Pains** — Was stört aktuell?
- **Gains** — Was wäre wertvoll?
- **Anxieties** — Wovor hat die Person Angst?
- **Desired Outcomes** — Woran misst sie Erfolg?

**Output:**
```yaml
decision_tension:
  pains: [list]
  gains: [list]
  anxieties: [list]
  desired_outcomes: [list]
```

---

### Modul 5: Desire & Identity Layer

**Aufgabe:** Tiefere Verlangen und Identitätsebene modellieren.

**Fragen:**
- Wer will der Kunde dabei sein?
- Welche Identität will er bestätigen oder erreichen?
- Welche Identität will er vermeiden?

**Desire-Klassen:**
Kontrolle | Sicherheit | Status | Zugehörigkeit | Selbstwirksamkeit | Vereinfachung | Freiheit | Anerkennung | Fortschritt | Distinktion | Entlastung | Transformation

**Output:**
```yaml
core_desire:
  primary: string
  secondary: [list]
identity_pull:
  toward: [list]
  away_from: [list]
product_positioning:
  - empowerment | sicherheit | prestige | entlastung | transformation | zugehörigkeit
```

---

### Modul 6: Belief System Mining

**Aufgabe:** Glaubenssätze, mentale Modelle und Adoptionslogiken extrahieren.

**Kategorien:**
- beliefs about self
- beliefs about the problem
- beliefs about existing solutions
- beliefs about the market
- beliefs about success/failure
- beliefs about risk

**Jeden Glaubenssatz klassifizieren als:**
- förderlich
- hemmend
- identitätsstabilisierend
- kaufblockierend
- messaging-hebel

**Output:**
```yaml
beliefs:
  about_self: [list]
  about_problem: [list]
  about_solutions: [list]
  about_risk: [list]
belief_classification:
  förderlich: [list]
  hemmend: [list]
  kaufblockierend: [list]
  messaging_hebel: [list]
```

---

### Modul 7: Psycholinguistic Voice Model

**Aufgabe:** Sprachlichen Fingerabdruck der Zielgruppe modellieren.

**Analyse-Dimensionen:**
- Ich-/Wir-Frame vs. Dritte-Person
- Konkret vs. Abstrakt
- Knapp-pragmatisch vs. Narrativ
- Negativ-vermeidend vs. Aspirativ-zielorientiert
- Analytisch vs. Identitär
- Intensitätsmarker (wirklich, absolut, gar nicht, ...)
- Statussprache (professionell, modern, etc.)
- Metaphern (Chaos, Ordnung, Kampf, Reise, etc.)

**Output:**
```yaml
voice_profile:
  tone: [list]
  preferred_language_patterns: [list]
  mirrored_phrases: [list]      # Zitate übernehmen
  avoid_language: [list]        # No-Go-Wörter
  headline_patterns: [list]     # Ableitbare Headlines
  cta_style: string
```

---

### Modul 8: Avatar Synthesis & Strategic Activation

**Aufgabe:** Alles in ein operatives Entscheidungsprofil überführen.

---

## Final Output Structure

### A. Executive Snapshot
6–10 Sätze: Wer, was sucht sie, was blockiert, warum kauft sie wirklich.

### B. Context Profile
Auslösende Situation, Umgebung, Zeitdruck, Verantwortlichkeiten, Stakeholder, Constraints.

### C. JTBD Core
Funktionaler Job, Emotionaler Job, Sozialer Job, Success Definition.

### D. Job Map
Pro Phase: Aufgabe, Friktion, gewünschtes Ergebnis, Chancen.

### E. Pain/Gain/Anxiety/Outcome
Priorisiert nach Relevanz und Kaufwirksamkeit.

### F. Desire & Identity
Core Desire, Identity Aspiration, Identity Avoidance, Statussignale.

### G. Belief System
Dominante Glaubenssätze, zentrale Einwände, Kaufblocker, Reframe-Chancen.

### H. Voice of Customer
Originalformulierungen, Sprachmuster, Trigger-Wörter, No-Go-Wörter, Messaging Mirrors.

### I. Segmentation Logic
Für wen gilt dieser Avatar? Abgrenzung zu benachbarten Avataren. Was macht ihn "aktiv"?

### J. Strategic Implications
Positionierung, Offer, Proof, Pricing-Kommunikation, Sales, Content, Produktpriorisierung.

### K. Confidence & Gaps
Was ist gut belegt? Wo fehlen Daten? Welche Hypothesen müssen validiert werden?

---

## Advanced Features

### 1. Contradiction Handling
Aktiv nach Widersprüchen suchen und erklären.
- Beispiel: Sagt "ich will Einfachheit", kauft aber komplexe Premium-Tools
- Analyse: Vielleicht ist nicht Einfachheit das Primärmotiv, sondern Kontrolle oder Status durch Kompetenz

### 2. Segment Split Detection
Erkennen wenn mehrere Avatare in einem Datensatz stecken.
- Nicht mitteln, sondern trennen
- "Die Daten deuten auf zwei distinkte Fortschrittslogiken hin."

### 3. Trigger Event Mapping
Wann wird die Persona kaufaktiv?
- Frustspitze | Rollenwechsel | Teamwachstum | Prozessbruch | Toolversagen | KPI-Druck | Budgetfreigabe | Peer-Vergleich

### 4. Switching Force Analysis
- **Push of the situation** — Aktueller Schmerz
- **Pull of the new solution** — Versprochener Nutzen
- **Anxiety of change** — Angst vor Umstellung
- **Habit of the present** — Gewohnheitskraft des Status quo

### 5. Message Testing Layer
3–5 Messaging-Angles mit Einschätzung (passt stark / mittel / riskant):
- kontrollorientiert
- statusorientiert
- entlastungsorientiert
- effizienzorientiert
- identitätsorientiert

---

## Guardrails

- ❌ Keine stereotype Demografie erfinden (kein "Anna, 34, liebt Kaffee")
- ❌ Keine frei erfundenen Hobbys oder Biografien
- ❌ Keine psychologischen Diagnosen
- ❌ Keine unbelegten Motive als Fakten
- ❌ Keine generischen Floskeln ("möchte Zeit sparen")
- ✅ Originalzitate klar kennzeichnen
- ✅ Widersprüche explizit dokumentieren
- ✅ Aussagen mit Evidenzstatus markieren
- ✅ Offene Fragen und Datenlücken benennen

---

## Usage

### Minimum Input
Mindestens 2-3 Datenquellen mit qualitativen Rohdaten (Interviews, Reviews, Support Tickets, Forenbeiträge).

### Quality Input
5+ Datenquellen, darunter mindestens direkte Kundenäußerungen (Interviews, Sales Calls).

### Process
1. Rohdaten bereitstellen (als Datei oder Text)
2. Skill durchläuft 8 Module
3. Output: Vollständiger Avatar als strukturiertes Dokument (Markdown)
4. Q&A zum Avatar für Verfeinerung

### Output Format
Markdown mit YAML-Frontmatter für strukturierte Daten + narrative Abschnitte.
Dateiname: `avatar-<segment-name>-<date>.md`
Speicherort: `/data/workspace/growing-brands/avatars/`

---

## The One Question This Skill Answers

> "Welche Fortschrittsbewegung versucht diese Zielgruppe unter welchem Druck zu vollziehen, welche psychologischen Kräfte beschleunigen oder blockieren diese Bewegung, und welche Sprache aktiviert Vertrauen, Handlung und Kaufbereitschaft?"
