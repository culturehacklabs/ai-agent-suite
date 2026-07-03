# KB: Map Check-in
**Agent 03 · CHL AI Agent System**
*Load only during the Map Check-in — after ANP analysis, before Language Analysis.*

---

## What the Map Check-in Is

The Map Check-in is the single co-creation moment in Agent 03. It happens after the ANP Assessment — when the evidence-based work is complete — and before Language Analysis, which is interpretive. This is the pivot point.

The practitioner reviews the draft community positioning on the Justice/Ontology map and either confirms it or adjusts it. Their direct community knowledge is the authority here — the AI-generated positioning is a starting point, not a verdict.

**Critical — Ontofake / Cooptation communities:**
Automated analysis is structurally biased toward misreading Ontofake communities as Catalytic or Justice + Onto-shift. Their language looks right. Their metaphors can look right. Only practitioner knowledge of actual practices, structural effects, and community context reveals the cooptation. During the Map Check-in, the agent should specifically flag any community it has placed in the upper right quadrant and ask: "Does this community's actual practice match its language — or could this be an Ontofake/Cooptation community that belongs in the upper left?" This question should always be asked, not left to the practitioner to raise.

The output of the Map Check-in is a **practitioner-reviewed JSON** that becomes the authoritative version of the Narrative Map. The final Community Analysis Report and Narrative Map both note: *"Map positioning reflects practitioner-reviewed analysis."*

---

## Two Pathways

Both pathways produce the same JSON output. The practitioner chooses based on their preference and context.

---

### Pathway 1 — Lite (Table + Mermaid)

**When to use:** Fast, text-based, works in any environment. Best for practitioners comfortable reading tables and numbers.

**Step 1 — Agent presents draft positioning**

The agent presents the draft map in two forms simultaneously:

*Editable table:*
```
| # | Community | Type | Justice (0–100) | Ontology (0–100) | Influence |
|---|---|---|---|---|---|
| 1 | [Name] | hegemonic | [value] | [value] | high |
| 2 | [Name] | catalytic | [value] | [value] | medium |
| 3 | [Name] | alternative | [value] | [value] | low |
```

*Axis reminder:*
- Justice: 0 = Injustice · 100 = Justice
- Ontology: 0 = Monoculture/Singular (bottom) · 100 = Onto-shift/Plural (top)
- Influence: high / medium / low (controls bubble size)

*Note: when you confirm values, the agent handles the mapper tool conversion automatically.*

*Mermaid render for spatial view:*
```
quadrantChart
    title Draft Narrative Map
    x-axis Injustice --> Justice
    y-axis Monoculture --> Onto-shift
    [Community name]: [justice/100], [ontology/100]
```

**Step 2 — Practitioner reviews**

The agent asks:
*"Does this positioning match your understanding of these communities? You can:*
- *Adjust any number — Justice or Ontology value*
- *Change a community's influence (high / medium / low)*
- *Change a community's type (hegemonic / catalytic / alternative)*
- *Rename a community*
- *Split a community into two*
- *Confirm as-is"*

**Step 3 — Practitioner responds**

Options:
- *"Looks right, proceed"* → agent generates final JSON and proceeds to Language Analysis
- *"Change community 2 to justice: 80"* → agent updates the table, re-renders Mermaid, asks for confirmation
- *"Community 3 should be two communities: X and Y"* → agent asks for positioning and type of each, updates table and Mermaid, confirms

**Step 4 — Agent generates final JSON**

Once confirmed, the agent produces the final Narrative Map JSON (see template in `KB_03_Understand_Actions.md`), states *"Map confirmed — proceeding to Language Analysis,"* and continues.

---

### Pathway 2 — Visual (CHL Narrative Mapper Tool)

**When to use:** When the practitioner wants to adjust community positions visually, drag-and-drop style. Requires access to the CHL Narrative Mapper tool.

**Step 1 — Agent produces draft JSON**

The agent produces a complete Narrative Map JSON using the confirmed schema:

```json
{
  "customTitle": "[Project name]",
  "communities": [
    {
      "name": "[Community name]",
      "justice": [value — 0=Injustice, 100=Justice],
      "ontology": [value — 0=Monoculture, 100=Onto-shift. Agent converts for current mapper tool automatically],
      "influence": "[high | medium | low]",
      "customSize": null,
      "description": "[description]",
      "communityType": "[hegemonic | catalytic | alternative]",
      "keyFrames": "[key frames from ANP analysis]",
      "color": "[hex]"
    }
  ],
  "windowOfDiscourse": null
}
```

*Note: `windowOfDiscourse` is left null at this stage — it will be populated after Window of Discourse analysis in Step 5.*

**Step 2 — Agent instructs the practitioner**

*"Here is the draft Narrative Map JSON. To review and adjust visually:*
1. *Open the CHL Narrative Mapper tool*
2. *Import this JSON file (or paste the JSON directly)*
3. *Drag communities to adjust positioning*
4. *Adjust bubble size using the influence setting (high / medium / low)*
5. *Change community type if needed*
6. *When satisfied, export the JSON*
7. *Paste the exported JSON back here"*

**Step 3 — Practitioner adjusts and exports**

The practitioner works in the mapper tool and pastes back the revised JSON.

**Step 4 — Agent receives revised JSON**

The agent reads the revised JSON, notes any changes from the draft, and confirms:
*"Received. Here are the changes you made: [list changes]. Does this look right?"*

Practitioner confirms → agent proceeds to Language Analysis using the revised positioning.

---

## Window of Discourse — Added After Step 5

After Window of Discourse analysis is complete (Step 5 in the main workflow), the agent adds the `windowOfDiscourse` rectangle to the JSON and presents it for confirmation:

*"Based on the Window of Discourse analysis, I'm proposing this rectangle position — it places mainstream discourse in the [quadrant description] area of the map. Does this match your assessment?"*

```json
"windowOfDiscourse": {
  "left": [X position],
  "top": [Y position],
  "width": [width],
  "height": [height]
}
```

If using the Visual pathway, the practitioner can import the updated JSON into the mapper tool to adjust the window rectangle directly, then export and return.

---

## What the Map Check-in Is Not

It is not a full re-opening of the analysis. ANP findings are not re-discussed here. The check-in is specifically about positioning, sizing, and typing — the spatial argument about where communities sit politically.

If the practitioner wants to substantially revise an ANP finding during the check-in, note it and revisit it in the Community Analysis Report — but do not restart the ANP process.

---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System. See `KB_Agent_Directory.md` for the full system map.*
