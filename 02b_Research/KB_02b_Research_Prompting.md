# KB: Prompting Guide — Research Agent
**Agent 02b · CHL AI Agent System**
*Load when the practitioner is stuck or asks for prompt guidance.*

---

## How to Use This Guide

The Research Agent works best when given the complete Big Listening Inquiry from Agent 02a. The more specific the parameters, the more focused and auditable the research output.

The agent always assigns Folio IDs and cites sources. If you receive output without Folio IDs, ask the agent to re-run with citations before accepting the report.

---

## Starter Prompts

### Small Listening Mode — Processing Community Research Only

Use this when your project has no Big Listening and you want to process your team's qualitative research directly into the standardised outputs.

> *"Small Listening mode. I have no Big Listening Inquiry — my research is based entirely on community interviews and qualitative material. Here is my Small Listening data: [paste interview notes / transcripts / observation notes / survey responses]. Process this into the CSV, produce a Narrative Report based on Small Listening only, and generate the ANP Source Library."*

---

### First Cycle — Standard Big Listening

Use this when you have a completed Big Listening Inquiry from Agent 02a and are ready to run research.

> *"Here is my Big Listening Inquiry: [paste inquiry]. Run the Big Listening, build the CSV, and produce the Narrative Report, CSV Database, and ANP Source Library."*

---

### First Cycle — Big Listening Only (No Small Listening Yet)

Use this when your team's Small Listening is still in progress and you want to run Big Listening first.

> *"Here is my Big Listening Inquiry: [paste]. Run the Big Listening now and produce the three outputs. I'll add Small Listening data when my team has collected it. Leave Section 5 of the Narrative Report as a placeholder."*

---

### Processing Small Listening Data

Use this when your team has collected Small Listening material and you want to integrate it into the CSV and Narrative Report.

> *"Here is my existing CSV: [paste or attach]. Here is my Small Listening material: [paste interview notes / transcripts / media scans]. Help me structure this into the CSV and update Section 5 of the Narrative Report with what the Small Listening found."*

---

### Iteration Mode

Use this when returning for a second or later cycle.

> *"Iteration mode. Here is my existing CSV from Cycle 1: [attach]. Here is my existing Narrative Report from Cycle 1: [attach]. Here is my updated Big Listening Inquiry from Agent 02a: [paste]. Extend the CSV with new research, and produce an updated Narrative Report that includes a What Has Changed section."*

---

## Power Prompts

### Request More ANP Source Library Entries

Use when you want more than the standard 5 entries per community for Agent 03's ANP analysis.

> *"Give me 10 ANP Source Library entries for [community name]. Flag the new entries as ANP Source = Yes in the CSV."*

> *"Give me the maximum available entries for all communities — I want a comprehensive ANP Source Library for a deep analysis cycle."*

---

### Audit a Specific Claim

Use when you want to verify that a specific statement in the Narrative Report has proper source support.

> *"Show me the CSV entries behind this claim from the Narrative Report: [paste claim]. What Folio IDs support it?"*

---

### Flag Unverified Patterns

Use when you want to explicitly surface what the research couldn't confirm — for Small Listening follow-up.

> *"What patterns appeared in the Big Listening that could not be sourced or verified? List them as unverified patterns with a note on what Small Listening action would confirm or challenge each."*

---

### Expand a Community Description

Use when a community first draft feels thin and you want more data before passing to Agent 03.

> *"The first draft for [community name] feels thin. Run additional searches to surface more actors, language patterns, and platform activity for this community. Add new entries to the CSV and update the community description in the Narrative Report."*

---

### Generate the Handoff Checklist Only

Use when you want to produce the Handoff Checklist as a standalone document — for example to share with your team before they answer the questions.

> *"Generate the Handoff Checklist for Agent 03 from the current Narrative Report. List the open questions without answers — I'll fill them in before passing to Agent 03."*

---

### Check for Missing Voices

Use when you want to verify that the parameters were searched thoroughly and expected actors were found.

> *"The Big Listening Inquiry included [actor / community] in the Who parameters but I don't see them in the CSV. Did they appear in the research? If not, what might explain their absence?"*

---

## Prompt Tips

**Always pass a complete Big Listening Inquiry.** The agent can work from a partial one but will ask for what is missing — which slows the process. A complete inquiry from Agent 02a means research can start immediately.

**Review Folio IDs before accepting the report.** Every claim in the Narrative Report should have at least one Folio ID in brackets. If you see a claim without a citation, ask the agent to source it or flag it as unverified before proceeding.

**Add Small Listening incrementally.** You don't have to wait for all Small Listening to be complete before starting. The CSV is a living document — you can add Small Listening entries in batches as your team collects material, and ask the agent to update Section 5 of the Narrative Report each time.

**Answer the Handoff Checklist before passing to Agent 03.** The more of the checklist you complete, the more efficiently Agent 03 can proceed. Unanswered questions don't block Agent 03 — but they slow it down.

**Request more ANP sources when the space is complex.** Five entries per community is the standard for most projects. For Pathways with many active actors or fast-moving narrative spaces, 10 entries gives Agent 03 richer material to work from.


---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System. See `KB_Agent_Directory.md` for the full system map.*
