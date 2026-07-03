# KB: Multi-Inquiry Mode
**Agent 02b · CHL AI Agent System**
*Load only when Multi-Inquiry Mode is activated — two or more Big Listening Inquiries provided.*

---

## What Multi-Inquiry Mode Does

Multi-Inquiry Mode runs two or more Big Listening Inquiries in sequence and combines the findings into a single Narrative Report. Each inquiry gets its own section in the report. A cross-inquiry synthesis at the top identifies patterns, shared communities, and tensions that cut across all inquiries.

This mode is most useful when:
- Multiple fellows or practitioners on the same Pathway need research run together
- A project has distinct sub-questions that each require their own parameter set
- A grouped pathway research session covers several related narrative spaces at once

---

## Folio ID Convention in Multi-Inquiry Mode

Each inquiry is assigned a short tag that becomes part of the Folio ID. This keeps entries attributable across the combined CSV.

**Format:** `[Listening Mode]-[Inquiry Tag]-[Community Initial]-[Number]`

Examples:
- `BL-P1-H-001` — Big Listening, Pathway Inquiry 1, Hegemonic community, entry 1
- `BL-P2-A-003` — Big Listening, Pathway Inquiry 2, Alternative community, entry 3
- `SL-P1-C-002` — Small Listening, Pathway Inquiry 1, Catalytic community, entry 2

When an entry is relevant to more than one inquiry, it appears in the CSV once with a note in the Inquiry Tag column listing all relevant inquiries (e.g. `P1, P2`). It is cited in both relevant sections of the Narrative Report.

---

## Workflow

**Step 1 — Receive and confirm all inquiries**
Take in all Big Listening Inquiries. Assign a short tag to each (P1, P2, P3 — or named tags if the practitioner prefers, e.g. `BCG`, `EoR`). Confirm each inquiry's parameters before beginning. If any are underspecified, ask before proceeding.

**Step 2 — Run inquiries in sequence**
Run each inquiry separately using Exa Search and Claude Research Mode. Build the CSV continuously — each entry tagged to its inquiry. Assign Folio IDs as entries are retrieved.

After each inquiry, do a brief check: are there communities, actors, or themes appearing across multiple inquiries? Note these as cross-inquiry overlaps for the synthesis section.

**Step 3 — Identify communities per inquiry**
Produce a community first draft for each inquiry separately. Some communities may appear across inquiries — if so, note them as shared communities and describe them once in the cross-inquiry synthesis rather than repeating separately in each section.

**Step 4 — Select ANP Source Library entries**
Flag 5 entries per community per inquiry as `ANP Source = Yes`. For shared communities that appear across inquiries, flag 5 entries per inquiry they appear in — the practitioner or Agent 03 can decide how to consolidate.

**Step 5 — Produce the combined Narrative Report**

See the template below. Structure is:
1. Cross-Inquiry Synthesis (top)
2. Inquiry sections (one per inquiry, each with full Narrative Report structure)
3. Combined Sources
4. Handoff Checklist (covers all inquiries)

**Step 6 — Produce a single combined CSV**
All entries from all inquiries in one CSV, distinguished by Inquiry Tag column. This is the baseline for the full research session — Agent 03 receives one CSV covering all inquiries.

**Step 7 — Produce ANP Source Library per inquiry**
Each inquiry gets its own ANP Source Library section. Shared communities are noted across sections with cross-references.

---

## Combined Narrative Report Template

```
# Narrative Report — Multi-Inquiry
## [Project Name / Pathway]

**Inquiries covered:** [number] — [Inquiry 1 name / tag] · [Inquiry 2 name / tag] · [etc.]
**Total CSV entries:** [number] · **Report date:** [date]

---

## Cross-Inquiry Synthesis

[2–3 paragraphs identifying what cuts across all inquiries:
- Shared narrative communities appearing in multiple inquiry spaces
- Recurring language, actors, or dynamics across the inquiries
- Key tensions or connections between the different narrative spaces
- What the inquiries together reveal that no single inquiry shows alone
Every claim cites Folio IDs.]

**Shared communities identified:**
- [Community name] — appears across [Inquiry tags] — [brief note on how it shows up differently across spaces]

---

## Inquiry 1: [Name / Tag]

**Research Question:** [restated]
**Timeframe:** [period] · **Platforms / Geography:** [scope]

### 1.1 Narrative Landscape Summary
[Full landscape summary for this inquiry — Folio IDs throughout]

### 1.2 Narrative Patterns Timeline
[Timeline for this inquiry's narrative space]

### 1.3 Identified Narrative Communities — First Draft
[Community first drafts for this inquiry]

### 1.4 Key Narrative Dynamics
[Dynamics specific to this inquiry's space]

### 1.5 Big Listening / Small Listening Integration
[If applicable]

---

## Inquiry 2: [Name / Tag]

[Repeat full structure]

---

[Add sections for each additional inquiry]

---

## Combined Sources

**Total entries across all inquiries:** [number]
**Entries cited in this report:** [number]
**ANP Source Library entries:** [number]

| Folio ID | Inquiry | Actor / Source | Platform | Date | Link |
|---|---|---|---|---|---|
| [BL-P1-H-001] | P1 | [source] | [platform] | [date] | [URL] |
[Continue for all cited entries]

---

## Handoff Checklist for Agent 03

*Questions from all inquiries — practitioner answers what they can before passing to Agent 03.*

**Cross-inquiry questions:**
1. [Question about a shared community or cross-inquiry dynamic]
   **Answer:**

**Inquiry 1 — [Name]:**
2. [Specific question from this inquiry's research]
   **Answer:**

**Inquiry 2 — [Name]:**
3. [Specific question from this inquiry's research]
   **Answer:**

[Continue — up to 6 questions total across all inquiries]
```

---

## When to Keep Inquiries Separate

If two inquiries are about completely different narrative spaces with no shared actors, communities, or dynamics — and combining them produces no useful synthesis — it may be cleaner to produce separate Narrative Reports. In that case, exit Multi-Inquiry Mode and run each inquiry as a standard single-inquiry session.

Ask the practitioner before combining: *"These two inquiries don't appear to share communities or dynamics. Would you prefer a separate Narrative Report for each, or a combined report with minimal synthesis?"*

---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System. See `KB_Agent_Directory.md` for the full system map.*
