# KB: Agent Directory
**CHL AI Agent System — Shared Reference**
*Load this file only when navigating handoffs or confirming I/O contracts.*

---

## System Map

The Culture Hack Method is a **cycle**, not a linear sequence. Phases can be revisited and updated rather than restarted from scratch on subsequent iterations.

```
        ┌─────────────────────────────────────────┐
        ↓                                         ↑
Ask → Listen → Understand → Recode → Hack + Evaluate
 01   02a→02b      03          04       05a + 05b
```

Entry point for any question: **00 Q&A Agent**

---

## Agent Registry

| ID | Name | Phase | Input | Output |
|----|------|-------|-------|--------|
| 00 | General Q&A | — | Any question | Answers + agent navigation |
| 01 | Point of View | Ask | POV answers / transcript | Extended POV + Short POV |
| 02a | Listening Model | Listen | Short POV | Listening Model + Big Listening Inquiry |
| 02b | Research | Listen | Big Listening Inquiry | Narrative Report + CSV Database + ANP Source Library |
| 03 | Narrative Communities + Mapper | Understand | Narrative Report + CSV + ANP Source Library + POV | Community Analysis Report (incl. Window of Discourse + Narrative Intentions) + Narrative Map |
| 04 | Decode & Recode | Recode | Community Analysis Report + Narrative Map + POV | Narrative Strategy + Recoded Narrative (with Message) |
| 05a | Hacking Tree | Hack | Narrative Strategy + Recoded Narrative (with Message) | Hacking Tree + Logistics Plan |
| 05b | Impact & Iteration | Hack (Evaluate) | Hacking Tree + Logistics Plan + prior documentation | Post-Hack Evaluation + Hack Database + Case Study (Outputs A–D as needed) |

---

## Handoff Chain

| From | Passes to | What is handed off |
|------|-----------|-------------------|
| 01 | 02a | Short POV |
| 02a | 02b | Big Listening Inquiry (research question + parameters) |
| 02b | 03 | Narrative Report + CSV Database + ANP Source Library |
| 03 | 04 | Community Analysis Report + Narrative Map (incl. Narrative Intentions + Window of Discourse) |
| 04 | 05a | Narrative Strategy + Recoded Narrative (with Message) |
| 05a | 05b | Hacking Tree + Logistics Plan |
| 05b | 02a or 04 | Case Study + updated POV (cycle continues) |

**Note on the 03 → 04 boundary:** Agent 03 produces *Narrative Intentions* — options for what the strategy could pursue. Agent 04 turns these into *Narrative Objectives* — the committed strategic decisions. Analysis is not strategy; the decision belongs to 04.

**On iteration:** In a second or later cycle, the narrative practitioner does not restart at 01. They update the existing Listening Model (02a) with new parameters, run new research (02b), and update community profiles (03). The POV may also be refined based on what was learned, but it is not rebuilt from scratch.

---

## Modes (All Agents)

**Hacking Mode ⚡ (default)** — executes directly, asks only for what is missing.
**Learning Mode 🌱 (on request)** — step-by-step, explanatory, teaches as it goes.

All agents ask for missing context before proceeding regardless of mode. Some agents add specialized modes (e.g. 01 Poetic Manifesto; 02a/02b/03 Iteration; 02b Multi-Inquiry and Small-Listening-only; 04/05a Stand-alone) — these are documented in each agent's own Instructions file.

---

## 00 Q&A Agent — Module KB Index

The Q&A agent is the only agent that references all module KBs. These are loaded on demand based on the topic of the question.

| KB | Loaded when asked about |
|----|------------------------|
| `KB_CHL_Method.md` | Method overview, narrative theory, political stance, metacrisis, cycles |
| `KB_AI_Fluency.md` | AI use, ethics, responsible research, the 4Ds framework |
| `KB_Agent_Directory.md` | Agent system map, handoffs, I/O contracts |
| `KB_00_QA_Module.md` | Quick definitions, phase summaries, navigation, "when stuck" guidance |
| `KB_00_QA_Documentation.md` | What to document at each phase, required vs. optional fields |
| `KB_01_Ask_Module.md` | Ask phase, POV development |
| `KB_02a_Listen_Module.md` | Listening Model design |
| `KB_02b_Research_Module.md` | Big Listening, research process |
| `KB_03_Understand_Module.md` | Understand phase, ANP, community mapping, Window of Discourse |
| `KB_04_Recode_Module.md` | Recode phase, decode/recode, narrative strategy |
| `KB_05a_Hack_Module.md` | Hack phase, hacking tree, logistics |
| `KB_05b_Impact_Module.md` | Impact, evaluation, case study, iteration |

---

## Platform Setup Notes

**Claude Project:** Each agent = one Project. Instructions file = System Prompt. KB files = Project Knowledge.

**Other LLMs:** Paste Instructions as system prompt. Paste relevant KBs into context on demand.

**Orchestration (future):** Each agent is a callable sub-agent. The handoff table above defines the I/O contract. The 00 Q&A Agent functions as the routing layer.

---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System.*
