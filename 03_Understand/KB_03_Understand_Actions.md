# KB: Actions — Understand Phase Output Templates
**Agent 03 · CHL AI Agent System**
*Load when producing any output: Community Analysis Report or Narrative Map.*

---

## Output A — Community Analysis Report

One flowing document covering all four analytical layers. Produced after the Map Check-in is complete.

```
# Community Analysis Report
## [Project Name / Pathway]

**POV (Short):** [restated from Agent 01]
**Research basis:** Narrative Report + ANP Source Library from Agent 02b
**Date:** [date produced]
**Communities analysed:** [number]

---

## 1. Community Profiles

*Initial community identifications from Agent 02b have been confirmed and reviewed
with the practitioner. Profiles below reflect the agreed community picture.*

### Community [#]: [Name]

**Description:** [1–2 sentences — what this community is]
**Community Type:** Hegemonic / Alternative / Catalytic
*[If this community uses progressive or pluralistic language while its practices
reinforce systems of oppression, note: "Positioned Injustice + Ontofake —
see Language Analysis for discourse/practice gap analysis"]*

**Core Narrative:**
[The central story this community tells — how it explains the issue,
its causes, and its solutions. What worldview does this narrative assume?]

**Key Actors:** [organisations, individuals, publications, platforms]

**Language Patterns:**
- Vocabulary: [specific recurring terms and keywords]
- Slogans / Hashtags: [if applicable]

**Platform Presence:** [where most active, geographic spread]

[Repeat for each community — 3 to 5 total]

---

## 2. ANP Assessment

*This section is evidence-based. All claims cite Folio IDs from the ANP Source Library.*

### [Community Name] — ANP Assessment

**Attention**
- Content volume: [frequency of narrative production — High / Medium / Low] [Folio IDs]
- Reach: [how far narratives travel beyond the community] [Folio IDs]
- Resonance: [which themes generate most activity] [Folio IDs]
- Temporal pattern: [growing / stable / declining over the research period] [Folio IDs]
- Comparative: [how this community's attention compares to others in the space]

**Network**
- Key nodes: [most central actors or organisations] [Folio IDs]
- Density: [tight / loose internal connections]
- Topology: [centralised / decentralised / distributed]
- Bridge actors: [who moves between this community and others — strategic note] [Folio IDs]
- Information flow: [how ideas spread within and beyond this community]

**Power**
- Institutional power: [media access, economic resources, policy influence — High / Medium / Low] [Folio IDs]
- Cultural power: [legitimacy, credibility, whose framing is treated as common sense] [Folio IDs]
- Network power: [coalition capacity, mobilisation ability] [Folio IDs]
- **Overall power level:** High / Medium / Low — [reasoning]

[Repeat ANP Assessment for each community]

**Cross-community observations:**
- Bridge actors identified: [actors who appear across multiple communities]
- Power differential: [which community dominates, which is marginalised]
- Network connections: [where communities are linked, where they are isolated]

---

## 3. Language Analysis

*The following analysis is interpretive — it draws on research data and practitioner
knowledge but involves analytical judgment. The practitioner should review this
section before passing to Agent 04.*

### [Community Name] — Language Analysis

**Frames:**
- Inside the frame: [what is included, made visible, centred — what this community talks about]
- Outside the frame: [what is excluded, made invisible, dismissed — what doesn't get said]
- How common sense is constructed: [the underlying logic — what makes this community's view feel natural, inevitable, or acceptable. What assumptions must already be held for this narrative to make sense?]
- Ideological logic: [the worldview tying frames together — what larger belief system this serves, what future it implies, what it protects]

**Dominant Metaphors:**
- [Metaphor 1]: [what it maps — source domain → target domain. What does this metaphor make thinkable? What does it foreclose?]
- [Metaphor 2]: [same structure]
[Be specific — use actual language from the research, not generic descriptions]

**What is absent:**
[What topics, actors, or perspectives never appear in this community's discourse.
What would feel strange or inappropriate to say here. What is treated as unthinkable.]

**Discourse / Practice gap** *(include only for communities positioned Injustice + Ontofake):*
[What does this community say versus what does it structurally do?
Who benefits from the narrative it produces?
Does the language of change function to absorb dissent rather than enable transformation?
What practices or structures remain intact despite the progressive framing?]

[Repeat Language Analysis for each community]

---

## 4. Window of Discourse

**Current positions:**

*Mainstream/Acceptable:*
[Which narratives are dominant and treated as common sense.
Which communities maintain them. What frames define the centre of public debate.]

*Emerging/Contested:*
[Which narratives are gaining traction but not yet mainstream.
Who is pushing them. What would tip them into mainstream.]

*Radical/Unacceptable:*
[Which narratives are currently marginalised or treated as extreme.
Who holds them. What would bring them into the Emerging position.]

**Position of the desired reframe:**
[Where does the narrative change the POV points toward currently sit —
Mainstream / Emerging / Radical? Why?]

**Catalytic communities and window movement:**
[Which Catalytic communities are already pushing in the desired direction.
What would amplify their impact. Are there moments, movements, or crises
that could accelerate window movement?]

**Window of Discourse coordinates (for Narrative Map):**
- left: [X position of window's left edge, 0–100]
- top: [Y position of window's top edge, 0–100 — 100 = Onto-shift, top of map]
- width: [width as % of map]
- height: [height as % of map]
*[Reasoning: which part of the Justice/Ontology map does mainstream discourse
currently occupy?]*

---

## 5. Strategic Insights + Narrative Intentions

*Strategic Insights describe what the analysis observes about the narrative space.
Narrative Intentions are possible directions that emerge from those insights — options,
not commitments. Agent 04 turns Narrative Intentions into Narrative Objectives:
the committed strategic plan.*

**Communities with movement potential:**
[Which communities show potential for shift toward Justice + Onto-shift, and why.
What would need to happen for movement to occur. What the analysis suggests
about realistic vs aspirational movement.]

**Frame openings:**
[Where are the contradictions, tensions, or unresolved questions in existing frames
that a reframe could work through? Which frames are most amenable to recoding?
Which currently-circulating alternative frames could be amplified?]

**Bridge opportunities:**
[Which bridge actors or community connections could be activated.
Where are communities close enough on the map that connection seems possible.]

**Window leverage:**
[What the Window of Discourse analysis suggests about timing and approach.
What is close to the edge of acceptable. What early signals of movement are visible.]

**Acupuncture Points:**
[Specific communities, actors, moments, or connections where a targeted culture hack
could have disproportionate impact — small pressure, significant shift.
Each Acupuncture Point should be named specifically: which community, what kind of
intervention, why this is the right pressure point in the system right now.
These are the most concrete and actionable outputs of this section.]

**Narrative Intentions — possible directions for Agent 04:**
[Options emerging from the analysis — possible communities to engage, frames to
challenge or amplify, directions of movement to pursue. Presented as options,
not decisions. Agent 04 selects and commits.]

**Gaps and risks:**
[What the analysis doesn't yet answer. What risks the strategy should account for.
Where the data is thin and more listening may be needed before strategy.]
```

---

## Output B — Narrative Map

Kept as a separate document. Three components: JSON (for the CHL Narrative Mapper tool), Mermaid (lightweight visual render), and summary table.

### Component 1 — Narrative Map JSON

```json
{
  "customTitle": "[Project name]",
  "communities": [
    {
      "name": "[Community name]",
      "justice": [0–100 float — 0=Injustice, 100=Justice],
      "ontology": [0–100 float — 0=Monoculture/Singular, 100=Onto-shift/Plural],
      "influence": "[high | medium | low]",
      "customSize": null,
      "description": "[1–2 sentence description]",
      "communityType": "[hegemonic | catalytic | alternative]",
      "keyFrames": "[2–3 key frames, comma separated]",
      "color": "[hex — defaults: hegemonic #e74c3c, catalytic #27ae60, alternative #f39c12]"
    }
  ],
  "windowOfDiscourse": {
    "left": [X position of left edge, 0–100],
    "top": [Y position of top edge, 0–100],
    "width": [width as % of map],
    "height": [height as % of map]
  }
}
```

**⚠️ Mapper tool conversion:** Until the mapper tool is updated to match the intuitive axis convention, apply this conversion when exporting JSON for the current tool: `mapper_ontology = 100 - ontology`. Keep your analytical values intuitive (100 = Onto-shift) and convert only for the JSON. See `KB_03_Understand_Tools.md`.

**Axis reference — intuitive convention:**
- justice 0–50 = Injustice side · justice 50–100 = Justice side
- ontology 0–50 = lower half (Monoculture / Reform) · ontology 50–100 = upper half (Onto-shift / Ontofake)
- Upper Right (Justice + Onto-shift): justice > 50, ontology > 50
- Upper Left (Injustice + Ontofake): justice < 50, ontology > 50
- Lower Right (Justice + Reform): justice > 50, ontology < 50
- Lower Left (Injustice + Monoculture): justice < 50, ontology < 50

*To use this JSON: paste into the CHL Narrative Mapper tool (with conversion applied). The tool renders the map visually and allows further adjustment. Export the revised JSON and paste back — remember to reverse the conversion on import.*

---

### Component 2 — Mermaid Render

A lightweight text-based visual. Use when the mapper tool is not available or for quick reference.

```
quadrantChart
    title Narrative Map — [Project Name]
    x-axis Injustice --> Justice
    y-axis Monoculture --> Onto-shift
    [Community Name]: [justice/100], [ontology/100]
```

*Mermaid y-axis matches the intuitive convention — no conversion needed. Plot directly as justice/100 and ontology/100.*

---

### Component 3 — Summary Table

```
## Community Map Summary

| Community | Type | Quadrant | Justice | Ontology | Influence | Strategic Potential |
|---|---|---|---|---|---|---|
| [Name] | [type] | [UR/UL/LR/LL] | [value] | [value] | [H/M/L] | [brief note] |

**Clusters:** [which communities group together and what that means]
**Distances:** [which communities are far apart — tensions or opportunities]
**Gaps:** [empty spaces in the map — what is absent]
**Window of Discourse:** [which communities and narratives sit inside the current window]
**Leverage points:** [where intervention could create movement]
```

---

## Iteration — Output Markers

In a second or later cycle, use `[Updated]` markers to show what changed. Example:

```
**Attention:** High [Updated — reach increased significantly after the hack period,
new actors entering the conversation — BL-C2-H-004]
```

For communities that were split from a previous cycle, add a note:

```
*[Split from "Community X" in Cycle 2 — the hack revealed this was two distinct
communities with different frames and positions. See Cycle 1 profiles for original.]*
```

---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System. See `KB_Agent_Directory.md` for the full system map.*
