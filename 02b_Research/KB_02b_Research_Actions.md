# KB: Actions — Research Output Templates
**Agent 02b · CHL AI Agent System**
*Load when producing any output: Narrative Report, CSV Database, or ANP Source Library.*

---

## The Folio ID System

Every entry in the CSV gets a unique Folio ID assigned at the moment of retrieval. This is the audit trail that links every claim in the Narrative Report to a specific source in the CSV.

**Format:** `[Inquiry Tag]-[Community Initial]-[Number]`

| Component | Options | Example |
|---|---|---|
| Inquiry Tag | BL (Big Listening) or SL (Small Listening) | `BL` |
| Community Initial | H (Hegemonic), A (Alternative), C (Catalytic), U (Unassigned) | `H` |
| Number | Sequential three-digit number per community | `001` |

**Examples:**
- `BL-H-001` — Big Listening, Hegemonic community, first entry
- `SL-A-003` — Small Listening, Alternative community, third entry
- `BL-U-007` — Big Listening, community not yet assigned, seventh unassigned entry
- `BL-C2-H-001` — Cycle 2, Big Listening, Hegemonic community, first new entry (Iteration Mode)

In the Narrative Report, Folio IDs appear in brackets after every claim: `[BL-H-001, BL-H-004]`. The reader can take any sentence in the report, locate the cited Folio IDs in the CSV, and verify the source directly.

---

## Output B — CSV Database

Built during research, not after. Every source retrieved gets a row. The CSV is the single source of truth for all research outputs.

**Columns (13 total):**

```
1.  Folio ID              — unique reference code [BL-H-001]
2.  Inquiry Tag           — which Big Listening Inquiry this entry belongs to
                            (relevant in Multi-Inquiry and Iteration modes)
3.  What (Theme/Topic)    — narrative theme or keyword this entry relates to
4.  Who (Actor/Source)    — organisation, individual, publication, or community
5.  When (Date)           — date or period of the content
6.  Where (Platform)      — platform, media outlet, geography, or physical space
7.  How (Listening Mode)  — Big Listening or Small Listening
8.  Community Assignment  — which narrative community this entry belongs to
                            (or Unassigned if not yet clear)
9.  Content Sample        — headline, post excerpt, or direct quote
                            (under 15 words if quoting directly)
10. Reach/Engagement      — metrics if available (shares, followers, views)
11. Source Link           — full URL or reference
12. Notes                 — frames observed, anomalies, open questions,
                            divergences with Small Listening
13. ANP Source            — Yes / No
                            Has this entry been used in the ANP Source Library?
```

**Notes on the CSV:**
- The CSV is a living document. Small Listening data is added as it arrives.
- In Iteration Mode, new entries are appended — existing entries are never deleted or overwritten.
- The practitioner should review all Small Listening entries before handoff to Agent 03.
- Entries marked `ANP Source = Yes` feed directly into Output C.

---

## Output A — Narrative Report

The main research document. Every claim cites Folio IDs. Unverified patterns are flagged explicitly.

```
# Narrative Report
## [Project Name / Pathway]

**Research Question:** [restated from Big Listening Inquiry]
**Timeframe:** [period covered]
**Platforms / Geography:** [scope]
**Listening Modes:** Big Listening [tools used] · Small Listening [methods used, if applicable]
**Total CSV entries:** [number] · **Sources cited in this report:** [number]
**Report date:** [date produced]

---

## 1. Narrative Landscape Summary

[2–4 paragraphs describing the overall shape of the narrative space.
What is most present? What is marginal? What are the dominant dynamics?
Every factual claim cites Folio IDs in brackets.
Unverified patterns are flagged: ⚑ Unverified pattern — Small Listening confirmation needed.]

---

## 2. Narrative Patterns Timeline

[How has this narrative space evolved over the research period?
What shifted — in volume, in actors, in framing?
If the timeframe is too short or data too thin to show a meaningful timeline,
state that explicitly rather than omitting the section.]

Key moments observed:
- [Date / period]: [what happened in the narrative space] [Folio IDs]
- [Date / period]: [what happened] [Folio IDs]
[Continue as data supports]

---

## 3. Identified Narrative Communities — First Draft

*This is an initial picture based on digital data only. These community descriptions
are observations, not conclusions — they will be confirmed, deepened, and potentially
revised in Agent 03 once Small Listening findings and analytical frameworks are applied.*

### Community 1: [Working Name]
- **Description:** [one sentence — what this cluster is]
- **Actors and nodes:** [key organisations, individuals, publications] [Folio IDs]
- **Language observed:** [recurring terms, phrases, hashtags] [Folio IDs]
- **Platform presence:** [where most active, geographic spread] [Folio IDs]
- **Initial type:** Hegemonic / Alternative / Catalytic
- **Reasoning:** [brief — based on observed reach and position in the data, not interpretation]

[Repeat for each community — 3 to 5 total]

---

## 4. Key Narrative Dynamics

[What is in tension in this space? What appears to be moving?
What connections or conflicts between communities are visible in the data?
State what the data shows — not what it means.
Every claim cites Folio IDs.]

---

## 5. Big Listening / Small Listening Integration

*[Include only if Small Listening data was processed in this session.
If not, note: "Small Listening data not yet integrated — this section will be
completed when the practitioner's team submits their findings."]*

**Where Big and Small Listening align:**
[What patterns appear in both streams] [Folio IDs from both BL and SL entries]

**Where they diverge:**
[What Small Listening found that Big Listening did not surface, or vice versa]
[Folio IDs] — *these divergences are flagged for Agent 03 as priority analysis areas*

**⚑ Unverified patterns from Big Listening requiring Small Listening confirmation:**
[List any patterns observed in digital data that could not be verified —
e.g. a community that appears active but left few retrievable traces]

---

## 6. Sources

**Total entries in CSV:** [number]
**Entries cited in this report:** [number]
**ANP Source Library entries (ANP Source = Yes):** [number]

| Folio ID | Actor / Source | Platform | Date | Link |
|---|---|---|---|---|
| [BL-H-001] | [source name] | [platform] | [date] | [URL] |
[Continue for all cited entries]

*Full CSV available as Output B. Cross-reference any claim in this report
using the Folio IDs cited in brackets.*

---

## Handoff Checklist for Agent 03

*The following questions emerged from this research. The practitioner should answer
as many as possible before passing to Agent 03. Unanswered questions are marked ⚑
and Agent 03 will address them before beginning analysis.*

1. [Specific question about a community identification — e.g. "Community 2 was identified
   primarily through [actors] — does this match what your team observed in Small Listening?"]
   **Answer:** [practitioner fills in, or leaves blank]

2. [Specific question about a data gap — e.g. "[Community name] appears active in the space
   but left few digital traces. Do you have Small Listening material on them?"]
   **Answer:**

3. [Specific question about a divergence — e.g. "Big Listening suggests X pattern, but
   Small Listening note [SL-A-002] suggests Y. Can you clarify?"]
   **Answer:**

4. [Specific question about a missing voice — e.g. "The research parameters included
   [actor/community] but they did not appear in the data. Do you know why?"]
   **Answer:**

[Add up to 6 questions total — generated from this specific research, not generic]
```

---

## Output C — ANP Source Library

Drawn from CSV entries flagged `ANP Source = Yes`. Organised by community. Ready for Agent 03's ANP analysis.

Standard is 5 entries per community. The practitioner can request more at any time — see `KB_02b_Research_Prompting.md`.

```
# ANP Source Library
## [Project Name / Pathway]

*Sourced extracts drawn from the CSV Database for use in Agent 03's ANP analysis.
Each entry is traceable to a Folio ID in the CSV.
Standard: 5 entries per community. Additional entries available on request.*

---

## Community 1: [Name] — [Hegemonic / Alternative / Catalytic]

### [BL-H-001]
- **Source:** [Actor / Publication name]
- **Platform:** [platform]
- **Date:** [date]
- **Link:** [URL]
- **Extract:** "[direct quote or close paraphrase — under 15 words if quoting directly]"
- **ANP relevance:** [one line — what this entry reveals about Attention, Network, or Power]

### [BL-H-002]
[Repeat structure]

[5 entries per community as standard]

---

## Community 2: [Name] — [type]

[Repeat structure]

---

*To request additional entries for a specific community, see `KB_02b_Research_Prompting.md`.*
*Full source data for each entry is in the CSV Database (Output B).*
```

---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System. See `KB_Agent_Directory.md` for the full system map.*
