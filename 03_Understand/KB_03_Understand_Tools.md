# KB: Tools — Understand Agent
**Agent 03 · CHL AI Agent System**
*Load when the practitioner asks about tools, evidence use, or the mapper.*

---

## Agent 03 Has No Active Search Tools

Agent 03 is an analytical agent. Its primary inputs are the Agent 02b research package and practitioner knowledge. It does not run new searches. If the analysis reveals that the research base is insufficient — too few sources for a community, missing voices, critical gaps — the agent flags this and asks the practitioner to return to Agent 02b for more material before proceeding.

---

## Using the ANP Source Library

The ANP Source Library from Agent 02b is the evidence base for the ANP Assessment. Each entry has a Folio ID, a source, a platform, a date, a link, an extract, and a note on ANP relevance.

**How to use it:**
- For each ANP sub-lens (volume, reach, resonance, key nodes, etc.), identify which Source Library entries provide evidence
- Cite the Folio IDs in brackets after the claim: `[BL-H-003, BL-H-007]`
- If a claim cannot be supported by at least one Folio ID, either flag it as an unverified observation or return to Agent 02b for more sources

**When to request more sources:**
If a community has fewer than 5 entries in the ANP Source Library, or if the available entries only cover one dimension (e.g. all Attention, no Network or Power), the analysis will be thin. Request more entries from Agent 02b using this prompt:

> *"I need more ANP Source Library entries for [community name], specifically for [Attention / Network / Power]. Can you flag 5 more entries from the CSV for this community with ANP Source = Yes?"*

---

## When to Cite vs. When to Interpret

**Cite Folio IDs in:** ANP Assessment — every claim about volume, reach, key nodes, power levels. This is evidence-based work and must be auditable.

**Do not cite in:** Language Analysis, Community Mapping, Window of Discourse, Strategic Insights / Narrative Intentions. These sections involve interpretive judgment that goes beyond what individual sources can prove. They are grounded in the data but not reducible to it.

This distinction matters for practitioners reading the output: they know which parts are evidence-based and which require their own review and judgment.

---

## The `[Updated]` Marker System

In Iteration Mode, any field in a Community Profile that has changed from the previous cycle gets an `[Updated]` marker. Format:

```
[Updated — brief note on what changed and why, with Folio IDs from new cycle if applicable]
```

Example:
```
**Overall power level:** Medium [Updated — institutional power has grown since Cycle 1,
new policy involvement noted — BL-C2-H-008]
```

This creates a longitudinal record of how communities are shifting — which is evidence of narrative change over time and feeds directly into Agent 05b's impact evaluation.

Never silently overwrite previous analysis. If something changed, the `[Updated]` marker is how you show it.

---

## The CHL Narrative Mapper Tool

The CHL Narrative Mapper is a web-based tool that renders the Justice/Ontology map visually. It accepts JSON import and exports JSON. It allows practitioners to drag communities to adjust positioning, resize bubbles by changing influence, and place the Window of Discourse rectangle.

**JSON schema** (use exactly these field names):

```json
{
  "customTitle": "Project name",
  "communities": [
    {
      "name": "Community Name",
      "justice": 0-100,
      "ontology": 0-100,
      "influence": "high | medium | low",
      "customSize": null,
      "description": "1-2 sentence description",
      "communityType": "hegemonic | catalytic | alternative",
      "keyFrames": "key frames comma separated",
      "color": "#hex"
    }
  ],
  "windowOfDiscourse": {
    "left": 0-100,
    "top": 0-100,
    "width": 0-100,
    "height": 0-100
  }
}
```

**Critical: axis convention and mapper tool conversion**
The agent uses the **intuitive axis convention**: ontology 100 = top of map = Onto-shift/Plural. This is what the agent produces analytically and what gets stored in the Community Analysis Report.

However, the **current mapper tool** uses an inverted ontology axis (high value renders at bottom). Until the tool is updated, apply this conversion when generating JSON for export to the current mapper:

`mapper_ontology = 100 - ontology`

Example: a community analysed at ontology = 72 (genuinely plural, upper half) exports as mapper_ontology = 28 to render correctly in the current tool.

When the practitioner returns an exported JSON from the mapper tool, reverse the conversion before storing analytical values: `ontology = 100 - mapper_ontology`.

**Quadrant reference (intuitive convention — use this for analysis):**

| Quadrant | Justice | Ontology |
|---|---|---|
| Justice + Onto-shift (UR) | > 50 | > 50 |
| Injustice + Ontofake (UL) | < 50 | > 50 |
| Justice + Reform (LR) | > 50 | < 50 |
| Injustice + Monoculture (LL) | < 50 | < 50 |

**Default colors by community type:**
- Hegemonic: `#e74c3c` (red)
- Catalytic: `#27ae60` (green)
- Alternative: `#f39c12` (orange)
- Override with any hex if a community needs a different color for clarity

**windowOfDiscourse positioning:**
- `left` and `top` use the same coordinate system as communities
- `width` and `height` are percentages of the full map area
- A typical Window of Discourse rectangle covers 30–50% of the map area
- Position it to reflect where mainstream/acceptable discourse currently sits

---

**Mermaid for the Lite Pathway**

When the mapper tool is not available, use a Mermaid quadrant chart for the visual layer.

```
quadrantChart
    title Narrative Map — [Project Name]
    x-axis Injustice --> Justice
    y-axis Monoculture --> Onto-shift
    Community Name: [justice/100], [ontology/100]
```

The Mermaid y-axis matches the intuitive convention — no conversion needed. Plot directly as `justice/100` and `ontology/100`.

---

## When to Flag Insufficient Data

Flag and pause analysis when:
- A community has fewer than 3 entries in the ANP Source Library
- All entries for a community are from a single source or platform
- The community was identified in Big Listening only with no Small Listening grounding and the Handoff Checklist flags this as a concern
- The practitioner expresses uncertainty about whether a community is real or an artefact of search parameters

In these cases: name the gap, describe what additional research would be needed, and ask whether to proceed with caveats or return to Agent 02b first.

---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System. See `KB_Agent_Directory.md` for the full system map.*
