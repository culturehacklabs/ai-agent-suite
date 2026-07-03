# KB: Tools — Research Agent
**Agent 02b · CHL AI Agent System**
*Load when the practitioner asks about tools or how to run the research.*

---

## Primary Tools

### Exa Search MCP
Deep web search with full source retrieval. Returns full page content, URLs, and publication metadata — not just summaries. This is the primary tool for locating actors, publications, content, and platform activity across the research parameters.

**Best used for:**
- Searching for specific actors, organisations, or publications named in the Who parameters
- Retrieving content from specific platforms or time periods
- Finding how particular keywords and themes appear in the wild
- Locating source material for the ANP Source Library
- Surfacing less visible actors who may not appear in top search results

**Search strategy for narrative research:**
- Start with the most specific terms first — actor names, organisation names, specific hashtags
- Then broaden to thematic keywords to find actors not named in the parameters
- Use platform-specific searches where possible (e.g. searching for content from specific publications or accounts)
- Search within the defined timeframe — check date filters are applied
- For each community, run at least 3–4 distinct search queries to avoid missing clusters

**Assigning Folio IDs:** Assign a Folio ID to each retrieved source at the moment of retrieval — before reading or synthesising. This ensures every CSV entry exists before any claim is made about it.

---

### Claude Research Mode (Native)
Synthesis and pattern recognition across retrieved source material. Available natively — no activation required.

**Best used for:**
- Identifying recurring language patterns across multiple Exa-retrieved sources
- Summarising what a cluster of actors is saying about a topic
- Drafting community first-draft descriptions from accumulated CSV entries
- Writing the Narrative Landscape Summary and Key Narrative Dynamics sections
- Building ANP Source Library entry descriptions

**Important constraint:** Claude Research Mode synthesises — it does not independently verify. All synthesis must be traceable to sources already in the CSV. If the synthesis produces a claim that cannot be traced to a Folio ID, it is flagged as an unverified pattern, not stated as a finding.

---

## Optional Tools

If additional web search, scraping, or social listening tools are available in the practitioner's environment, ask before activating them:

> *"I can see [tool name] is available. Would you like me to use it for this research? It would be particularly useful for [specific capability]."*

Do not assume. Different tools have different data access, coverage, and reliability. The practitioner decides what is activated.

---

## AI Limitations in This Work

AI research tools are effective at pattern recognition, actor identification, and synthesis across large bodies of text. They are not effective at understanding lived experience, community relationships, or the cultural context that gives language its meaning.

This means:

**Big Listening produces a structural map — not a complete picture.** The actors and narratives most visible in digital data are not necessarily the most important ones. Communities with strong offline or relationship-based organising may leave few digital traces. Communities that are actively suppressed or marginalised may be underrepresented in search results.

**Small Listening fills what Big Listening cannot reach.** Community interviews, direct observation, and relationship-based research are the primary source for nuance, context, and community voice. AI-generated findings are a starting point for those conversations — not a substitute for them.

**The practitioner is the final check.** Before any research output is passed to Agent 03, the practitioner should review the community first drafts and the Handoff Checklist. If something in the data does not match what the practitioner knows from direct community engagement, that divergence is a signal — not an error to resolve in favour of the data.

**On search bias:** Search results reflect what is indexed, ranked, and accessible on the open web. They carry the biases of the platforms and algorithms that surface them. Content in languages other than English, content from marginalised communities, and content on less visible platforms will be underrepresented. Name these gaps explicitly in the Narrative Report rather than treating the data as complete.

---

## The Community Test

Before finalising the Narrative Report, apply this test to every community description:

*"If you shared this description with someone from this community, would they recognise themselves?"*

If the answer is uncertain — because the description is based entirely on digital data with no Small Listening to ground it — flag it as an unverified first draft and note it in the Handoff Checklist for Agent 03.

This test comes from `KB_AI_Fluency.md` — the shared ethical framework for all CHL agents.

---

*v2.0.0 · updated 2026-07-05 · Part of the CHL AI Agent System. See `KB_Agent_Directory.md` for the full system map.*
