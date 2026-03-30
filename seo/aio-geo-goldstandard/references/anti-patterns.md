# Anti-patterns and fixes

## 1) Keyword-heavy intros without an answer

- **Symptom:** Long intro; no direct response.
- **Fix:** First 40–60 words answer the core question; use a **declarative** sentence up front.

## 2) Throat-clearing or “essay” opening

- **Symptom:** “In today’s digital landscape…”, “More and more companies are…” before the claim.
- **Fix:** Replace with one clear proposition: what the thing **is**, **requires**, or **does**.

## 3) Hedge-led lead

- **Symptom:** “This **might** help…”, “**Could** improve visibility…”, “**Perhaps** worth considering…” in the opening.
- **Fix:** State the strongest supportable fact first; qualify later if needed—not in the lead.

## 4) Price-dominated lead (wrong intent)

- **Symptom:** Amounts, tiers, or “starting at” language before the topic is explained—on non-pricing pages.
- **Fix:** Explain the entity/decision first; move commercial detail below or to a dedicated pricing section. (Skip this fix when the page intent **is** price or finance.)

## 5) Fake heading structure

- **Symptom:** Three or four generic H2s (“Introduction”, “Benefits”, “Conclusion”) that do not map to distinct user questions.
- **Fix:** Go **flat** (fewer headings) **or** rewrite each H2 as a real question and answer it immediately.

## 6) Generic “AI-friendly” claims without evidence

- **Symptom:** Vague tips with no proof context.
- **Fix:** Add measurable detail, method, or grounded example.

## 7) Schema mismatch

- **Symptom:** JSON-LD claims FAQ/Article facts that are not visible on the page.
- **Fix:** Align schema fields with rendered content exactly.

## 8) Pure client-side critical content

- **Symptom:** Key answers appear only after heavy client execution.
- **Fix:** Server-render (or static-render) core answer blocks and entity facts.

## 9) Topical drift

- **Symptom:** Multiple intents mixed without hierarchy.
- **Fix:** One primary intent per page; split secondary intents.

## 10) Entity ambiguity

- **Symptom:** Unclear who or what the page is about.
- **Fix:** Explicit naming, consistent terms, canonical internal links.

## 11) Thin trust signals

- **Symptom:** No author or org context on consequential YMYL-style claims.
- **Fix:** Add identity and evidence context proportional to risk.

## 12) Link stuffing

- **Symptom:** Many links with weak semantic relation.
- **Fix:** Fewer, higher-relevance links to hub pages.

## 13) Cosmetic refresh only

- **Symptom:** Date bumps without substantive updates.
- **Fix:** Meaningful factual and answer-block revisions.

## 14) `llms.txt` over-reliance

- **Symptom:** Treating `llms.txt` as the whole optimization plan.
- **Fix:** Treat as optional; prioritize page content + structured data + crawlability.

## 15) Citation gaming

- **Symptom:** Fabricated references or manipulative freshness.
- **Fix:** Remove deception; use verifiable, ethical sourcing.

## 16) No QA gate

- **Symptom:** “Optimized” text shipped without checklist review.
- **Fix:** Run the checklist; ship failures and fixes with the artifact.
