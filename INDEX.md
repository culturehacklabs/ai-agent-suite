# INDEX — CHL AI Agent System

Complete reference for all agents, files, and capabilities. Reflects the current file inventory as of the v2.0.0 release (July 2026).

---

## System Map

```
        ┌──────────────────────────────────────────────┐
        ↓                                              ↑
Ask → Listen → Understand → Recode → Hack + Evaluate
 01    02a→02b      03          04        05a + 05b
```

Entry point for any question or navigation: **Agent 00 · Q&A**

---

## Shared Files

These files are shared across all agents. They are never loaded by default — only when a specific need arises. (They carry their canonical, unversioned names; the older `_v#` files and the duplicate Agent Directory were retired in the June 2026 cleanup, and `KB_AI_Fluency_v3.md` was renamed to `KB_AI_Fluency.md` in v2.0.0.)

| File | Purpose | Load when |
|------|---------|-----------|
| `KB_CHL_Method.md` | Full method theory, political stance, vocabulary | Questions about methodology, narrative theory, political stance |
| `KB_AI_Fluency.md` | Ethical AI use, the 4Ds framework, responsible research | Questions about AI ethics, data responsibility, research practice |
| `KB_Agent_Directory.md` | System map, handoff chain, I/O contracts | Navigating between agents, confirming handoffs |

---

## Agent 00 · General Q&A

**Phase:** Entry point / navigation
**Primary users:** Anyone — newcomers, practitioners mid-process, facilitators
**Stand-alone use:** Yes — this is the starting point for anyone new to the system

**What it does:** Answers questions about the Culture Hack Method, defines concepts, clarifies which phase does what, and routes practitioners to the right agent. Does not produce phase outputs.

| File | Contents |
|------|---------|
| `00_QA_Instructions.md` | System prompt: identity, KB index, routing table, what the agent does not do |
| `KB_00_QA_Module.md` | Quick reference: phase summaries, common questions, navigation guide, "when stuck" map |
| `KB_00_QA_Documentation.md` | Documentation requirements per phase: required vs. optional fields |
| `KB_00_QA_Prompting.md` | Starter prompts for newcomers and mid-process practitioners |

**Receives:** Any question · **Produces:** Answers, concept explanations, routing to phase agents
*(4 files. No Tools file — this agent calls no external tools.)*

---

## Agent 01 · Ask — Point of View

**Phase:** Ask · **Primary users:** Collectives beginning a new hack or refining a previous one · **Stand-alone:** Yes

**What it does:** Guides development of the collective Point of View (POV): who they are, what narrative problem they observe, what they want to shift, and their theory of change. Produces Extended POV + Short POV. Also supports a Poetic Manifesto mode from assembly transcripts.

| File | Contents |
|------|---------|
| `01_Ask_Instructions.md` | System prompt: three modes (Hacking, Learning, Poetic Manifesto), KB index, 5-step workflow |
| `KB_01_Ask_Module.md` | Ask phase theory, four-part POV format, documentation questions, iteration workflow |
| `KB_01_Ask_Actions.md` | POV templates (Extended + Short), iteration format, Poetic Manifesto section, quality checklist |
| `KB_01_Ask_Prompting.md` | Starter and power prompts, reference POV example |
| `KB_01_Ask_Tools.md` | No external tools; elicitation approach and AI-use principles |

**Receives:** Any — draft, context, transcript, or nothing · **Produces:** Extended POV + Short POV (+ optional Poetic Manifesto) · **Passes to:** Agent 02a (Short POV)
*(5 files.)*

---

## Agent 02a · Listen — Listening Model

**Phase:** Listen · **Primary users:** Practitioners ready to begin research · **Stand-alone:** Yes

**What it does:** Transforms the Short POV into a research question, then builds a Listening Model (five parameters: What/Who/When/Where/How) for Small and Big Listening. Output — the Big Listening Inquiry — is the brief handed to Agent 02b. Includes Small Listening instrument design on request.

| File | Contents |
|------|---------|
| `02a_Listen_Instructions.md` | System prompt: modes (incl. Iteration), KB index, workflow, feasibility check |
| `KB_02a_Listen_Module.md` | Listen phase theory, Listening Model structure, five parameters, documentation questions, iteration |
| `KB_02a_Listen_Actions.md` | Listening Model template, Big Listening Inquiry template, Iteration Cycle update |
| `KB_02a_Listen_Prompting.md` | Starter and power prompts for new and iterating practitioners |
| `KB_02a_Listen_Tools.md` | No execution tools at this stage; describes what travels to 02b |
| `KB_02a_Listen_SmallListening.md` | Small Listening instrument design: interview guides, observation frameworks, survey design |

**Receives:** Short POV (or updated POV + Case Study on iteration) · **Produces:** Listening Model + Big Listening Inquiry · **Passes to:** Agent 02b
*(6 files.)*

---

## Agent 02b · Research

**Phase:** Listen · **Primary users:** Practitioners executing or processing research · **Stand-alone:** Partial (Big Listening needs web research tools)

**What it does:** Executes Big Listening and structures Small Listening data. Applies the NO INVENTION principle — every claim traces to a Folio ID in the CSV. Produces the Narrative Report, CSV Database, and ANP Source Library, plus a Handoff Checklist for Agent 03.

**Tools note:** The Claude-native version uses Exa Search MCP + Claude Research Mode. On other platforms, web research is handled separately (Perplexity, SerpAPI, Tavily, etc.) and fed in. The process and CSV structure stay the same.

| File | Contents |
|------|---------|
| `02b_Research_Instructions.md` | System prompt: NO INVENTION, five modes, KB index, 7-step workflow |
| `KB_02b_Research_Module.md` | Research phase theory, key concepts, research process, iteration + Small-Listening-only paths, boundary with 03 |
| `KB_02b_Research_Actions.md` | Narrative Report (A), CSV Database (B), ANP Source Library (C), Handoff Checklist templates |
| `KB_02b_Research_Prompting.md` | Starter and power prompts for Big and Small Listening workflows |
| `KB_02b_Research_Tools.md` | Exa Search MCP + Claude Research Mode; guidance for alternative tools |
| `KB_02b_Research_MultiInquiry.md` | Multi-Inquiry Mode workflow — multiple Big Listening Inquiries combined into one report |

**Receives:** Big Listening Inquiry (+ Small Listening data) · **Produces:** Narrative Report + CSV Database + ANP Source Library + Handoff Checklist · **Passes to:** Agent 03
*(6 files.)*

---

## Agent 03 · Understand — Narrative Communities + Mapper

**Phase:** Understand · **Primary users:** Practitioners analysing research and mapping communities · **Stand-alone:** No (needs 02b outputs)

**What it does:** Applies four tools in sequence — ANP Analysis, Language Analysis, Justice/Ontology Community Mapping (with a Map Check-in co-creation moment), and Window of Discourse — to produce the Community Analysis Report and Narrative Map. Includes a critical note on Ontofake communities (automated analysis is biased toward misreading cooptation; practitioner knowledge is essential).

| File | Contents |
|------|---------|
| `03_Understand_Instructions.md` | System prompt: modes, 6-step analytical sequence, Map Check-in as mandatory step, KB index |
| `KB_03_Understand_Module.md` | Understand phase theory, all key concepts (ANP, frame analysis, Justice/Ontology map with Ontofake note, Acupuncture Points, Window of Discourse), Strategic Insights vs. Narrative Intentions, iteration |
| `KB_03_Understand_Actions.md` | Community Analysis Report template, ANP/Language/Window templates, Narrative Map JSON, axis-conversion note |
| `KB_03_Understand_Prompting.md` | Starter and power prompts (Ontofake identification, missing ANP sources, fit issues) |
| `KB_03_Understand_Tools.md` | Narrative mapper guidance, JSON schema, Mermaid format, axis conversion formula |
| `KB_03_Understand_MapCheck.md` | Map Check-in protocol — the co-creation moment between ANP and Language Analysis |

**Receives:** Narrative Report + CSV Database + ANP Source Library + Handoff Checklist · **Produces:** Community Analysis Report + Narrative Map · **Passes to:** Agent 04
*(6 files.)*

---

## Agent 04 · Recode — Narrative Strategy

**Phase:** Recode · **Primary users:** Practitioners developing strategy and message · **Stand-alone:** Yes (Decode/Recode on any message)

**What it does:** Five moments — Audience + Objectives, Decode (eight lenses), Recode (eight lenses), Message (full structure of meaning), Narrative Strategy (short-term actions + long-term hypotheses). The distilled framing synthesis is the most actionable output.

| File | Contents |
|------|---------|
| `04_Recode_Instructions.md` | System prompt: modes, 5-moment workflow, stand-alone path, KB index |
| `KB_04_Recode_Module.md` | Recode phase theory, key concepts, the eight lenses, documentation questions, iteration |
| `KB_04_Recode_Actions_A.md` | Audience + Audience Profile templates |
| `KB_04_Recode_Actions_B.md` | Decode table + Recode table (eight lenses), Message block, framing synthesis |
| `KB_04_Recode_Actions_C.md` | Narrative Strategy template |
| `KB_04_Recode_Prompting.md` | Starter and power prompts (finding the message, metaphor lens, slogan-vs-message, audience coherence) |
| `KB_04_Recode_Tools.md` | No external tools; generative approach and the 4Ds applied to recoding |

**Receives:** Community Analysis Report + Narrative Map + Window of Discourse · **Produces:** Narrative Strategy + Recoded Narrative (with Message) + Audience Profile(s) · **Passes to:** Agent 05a
*(7 files.)*

---

## Agent 05a · Hack — Hacking Tree

**Phase:** Hack (05a) · **Primary users:** Practitioners designing a cultural intervention · **Stand-alone:** Yes (needs a light Audience Profile)

**What it does:** Translates the recoded message into a concrete intervention through the Hacking Tree (Media, Meme, Tone, Hack: Space/Scale/Moment) plus a Logistics Plan. Available in Lean or Full Logistics modes.

| File | Contents |
|------|---------|
| `05a_Hack_Instructions.md` | System prompt: modes, stand-alone path with Audience Profile, 4-branch + logistics workflow, KB index |
| `KB_05a_Hack_Module.md` | Hack phase theory, four branches, stickiness test, Point of Intervention, Lean vs. Full Logistics, documentation |
| `KB_05a_Hack_Actions_A.md` | Hacking Tree output template (four branches) |
| `KB_05a_Hack_Actions_B.md` | Lean Logistics + Full Logistics templates |
| `KB_05a_Hack_Prompting.md` | Starter and power prompts for full-cycle and stand-alone use |
| `KB_05a_Hack_Tools.md` | No external tools; when to bring in creative collaborators |

**Receives:** Narrative Strategy + Recoded Narrative (with Message) + Audience Profile(s) · **Produces:** Hacking Tree + Logistics Plan · **Passes to:** Agent 05b
*(6 files. Status: good enough — verified in the v2.0.0 audit; Module + Actions A/B read in full and confirmed coherent.)*

---

## Agent 05b · Impact — Evaluate + Iterate

**Phase:** Hack (05b) — Evaluate + Iterate (nested in Hack) · **Primary users:** Practitioners post-launch or building pre-launch docs · **Stand-alone:** Yes

**What it does:** Four outputs — (A) Pre-Hack Documentation Plan, (B) Post-Hack Evaluation (three-level impact + A/B + iteration strategy), (C) Hack Database (nine-section synthesis; **this is the home of the full documentation database**), (D) Case Study. All close with three personal reflection questions. Iteration logic routes to the right next agent.

| File | Contents |
|------|---------|
| `05b_Impact_Instructions.md` | System prompt: four outputs with activation logic, dependency table, 4-step workflow, iteration routing |
| `KB_05b_Impact_Module.md` | Phase theory, three-level evaluation, closing questions, iteration logic table |
| `KB_05b_Impact_Actions_A.md` | Output A — Pre-Hack Documentation Plan |
| `KB_05b_Impact_Actions_B.md` | Output B — Post-Hack Evaluation |
| `KB_05b_Impact_Actions_C.md` | Output C — Hack Database (full documentation database) |
| `KB_05b_Impact_Actions_D.md` | Output D — Case Study |
| `KB_05b_Impact_Prompting.md` | Starter and power prompts per output |

**Receives:** Hacking Tree + Logistics Plan + full prior documentation · **Produces:** Output A, B, C, or D · **Passes to:** Agent 02a or 04
*(7 files. No Tools file — none required.)*

---

## Handoff Chain Summary

| From | What is handed off | To |
|------|-------------------|----|
| Agent 01 | Short POV | Agent 02a |
| Agent 02a | Big Listening Inquiry | Agent 02b |
| Agent 02b | Narrative Report + CSV Database + ANP Source Library | Agent 03 |
| Agent 03 | Community Analysis Report + Narrative Map (incl. Narrative Intentions + Window of Discourse) | Agent 04 |
| Agent 04 | Narrative Strategy + Recoded Narrative (with Message) + Audience Profile(s) | Agent 05a |
| Agent 05a | Hacking Tree + Logistics Plan | Agent 05b |
| Agent 05b | Case Study + updated POV | Agent 02a or 04 |

---

## File Count

| Group | Files |
|-------|-------|
| Shared (`KB_CHL_Method`, `KB_AI_Fluency`, `KB_Agent_Directory`) | 3 |
| Shared skill (`KB_Tutorial_Builder`) | 1 |
| Agent 00 | 4 |
| Agent 01 | 5 |
| Agent 02a | 6 |
| Agent 02b | 6 |
| Agent 03 | 6 |
| Agent 04 | 7 (Actions split A/B/C; `KB_04_Recode_Prompting.md` + `KB_04_Recode_Tools.md` created in v2.0.0) |
| Agent 05a | 6 |
| Agent 05b | 7 |
| **Agent + shared subtotal** | **51** |
| Meta (INDEX, INSTALL, README, ARCHITECTURE) | 4 |
| **Total** | **55** |

*Note: `KB_Tutorial_Builder.md` is counted as a shared skill.*

---

## Version Manifest

*Single source of truth for file versions. A file's footer must match its row here. Before any release, diff footers against this table — a mismatch means a file didn't land. Version = the release in which the file last changed; untouched files keep their earlier version.*

**Release v2.0.0 — 2026-07-05.** All files listed below are at **v2.0.0 · 2026-07-05** unless a later row says otherwise.

Scope of the v2.0.0 release: introduced file versioning; renamed `KB_AI_Fluency_v3.md` → `KB_AI_Fluency.md` and re-landed the corrected `KB_00_QA_Module.md`; renumbered Agent 05→05a (Hack) and Agent 06→05b (Impact), folding Evaluate into the Hack phase; added phase words to the 02a/02b/03 stems (`02a_Listen_`, `02b_Research_`, `03_Understand_`); aligned handoff labels across the chain (Community Analysis Report · Recoded Narrative (with Message) · Logistics Plan · Post-Hack Evaluation); "AI Agent Suite" → "AI Agent System"; created Agent 04's Prompting + Tools KBs; and applied the Agent 03 content fixes. Full detail in `CHL_Agent_System_Changelog.md` (Session 4).

| File | Version | Updated |
|------|---------|---------|
| *All shared, agent, and meta files* | v2.0.0 | 2026-07-05 |

*(When only some files change in a later release, replace this single row with per-file rows for the changed files and leave the rest at their last-touched version.)*

---

*For deployment instructions, see [`INSTALL.md`](INSTALL.md). For multi-agent architecture, see [`ARCHITECTURE.md`](ARCHITECTURE.md).*

*v2.0.0 · updated 2026-07-05 · CHL AI Agent System.*
