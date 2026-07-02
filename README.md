# CHL AI Agent System
### A modular AI toolkit for narrative-led systems change

---

## What This Is

This is an open toolkit of AI agents built on the **Culture Hack Method**, developed by [Culture Hack Labs (CHL)](https://www.culturehack.io). Each agent supports a specific phase of the method — from developing a collective Point of View, to researching narrative spaces, to designing cultural interventions, to evaluating impact and iterating.

The agents are designed for **narrative practitioners, facilitators, and Rhizome Fellows** doing the work of cultural transformation. They are tools, not oracles — they accelerate research, structure thinking, and help produce outputs. The political judgment, community knowledge, and creative vision remain human.

---

## The Culture Hack Method

Culture hacking is a practice of strategic narrative intervention — seeding new frames, metaphors, and stories that shift what is thinkable and possible in a given cultural space. CHL developed this methodology for practitioners working on the frontlines of systems change: dismantling narratives that justify oppression and building narratives that make regenerative, just futures thinkable.

The method is not a linear process. It is an **iterative cycle**:

```
        ┌──────────────────────────────────────────────┐
        ↓                                              ↑
Ask → Listen → Understand → Recode → Hack + Evaluate
 01    02a→02b      03          04        05 + 06
```

Each cycle deepens the practice. Practitioners do not restart from scratch — they update their listening, sharpen their strategy, and refine their message based on what the previous hack revealed.

For the full theoretical foundation — metacrisis, narrative theory, the political stance of Justice + Onto-shift — see [`KB_CHL_Method.md`](KB_CHL_Method.md).

---

## The Five Phases and Eight Agents

| Agent | Phase | What it does |
|-------|-------|-------------|
| **00 · Q&A** | Entry / Navigation | Answers questions about the method, routes to the right agent |
| **01 · Ask** | Point of View | Develops the collective POV — who you are, what narrative you're challenging, your theory of change |
| **02a · Listen** | Listening Model | Designs the research framework: research question + five parameters |
| **02b · Research** | Research | Executes large-scale digital research and organises Small Listening data |
| **03 · Understand** | Analysis | ANP analysis, language/frame analysis, community mapping, Window of Discourse |
| **04 · Recode** | Narrative Strategy | Decodes dominant narratives, builds alternative reframes, produces the message |
| **05 · Hack** | Hacking Tree | Translates the message into a cultural intervention: Media, Meme, Tone, Space, Scale, Moment |
| **06 · Impact** | Evaluate + Iterate | Assesses impact at three levels, produces case study, feeds the next cycle |

---

## Modes

Every agent runs in at least two modes:

**Hacking Mode ⚡ (default)** — executes directly, produces outputs without extended explanation, asks only for what is genuinely missing. For practitioners who know the method and want to move fast.

**Learning Mode 🌱 (activated on request)** — works step by step, explaining each concept and decision. For newcomers, facilitators, or anyone who wants to understand *why*. Activated by including "learning mode" anywhere in your prompt.

Some agents add specialised modes documented in their own Instructions — for example, Agent 01's Poetic Manifesto, the Iteration mode in Agents 02a/02b/03, Agent 02b's Multi-Inquiry and Small-Listening-only modes, and the Stand-alone mode in Agents 04/05.

The Culture Hack Method was designed to be learned through doing. The agents should accelerate that learning, not shortcut it.

---

## Political Stance

This toolkit is not neutral. It is built explicitly for **Justice + Onto-shift**:

- **Justice (systemic/transformative)** — supporting communities challenging structures of oppression. Not supporting narratives that maintain the status quo, even with progressive language.
- **Onto-shift (ontological shift)** — supporting a fundamental shift in how we relate to the world. Centering plural ways of knowing: Indigenous epistemologies, community knowledge, embodied experience, relational understanding.

The agents will not produce outputs misaligned with this stance. If you encounter outputs that drift from it, that is a signal to push back — the practitioner's judgment takes precedence.

---

## Files and Structure

Files are named by agent ID and role:

```
[ID]_Instructions.md        ← System prompt (the agent's identity + workflow)
KB_[ID]_Module.md           ← Phase theory, key concepts, documentation questions
KB_[ID]_Actions.md          ← Output templates and formats (split into _A/_B/_C where large)
KB_[ID]_Prompting.md        ← Starter prompts, power prompts, mode examples
KB_[ID]_Tools.md            ← Tools and external integrations (only where the agent uses them)

Shared (loaded conditionally, never by default):
KB_CHL_Method.md            ← Full method theory, political stance, vocabulary
KB_AI_Fluency.md            ← Ethical AI use, the 4Ds framework
KB_Agent_Directory.md       ← System map, handoff chain, I/O contracts
```

The exact file set varies by agent — some split their Actions KB and some add specialised KBs (e.g. `KB_02a_SmallListening.md`, `KB_02b_MultiInquiry.md`, `KB_03_MapCheck.md`). A few agents do not need a Tools or Prompting file. See [`INDEX.md`](INDEX.md) for the authoritative, up-to-date list, and [`INSTALL.md`](INSTALL.md) for deployment.

---

## Credit and Curriculum

This toolkit is built on the Culture Hack Method curriculum developed by [Culture Hack Labs](https://www.culturehack.io/curriculum/the-culture-hack-method/). The method, concepts, and political framework are CHL's. The agents translate that curriculum into AI-assisted practice.

Rhizome Fellowship practitioners: these agents are designed with your context in mind, including the Five Pathways to Regenerative Futures as an optional framework in Agent 01.

---

## Contributing

This toolkit is designed to grow with practice. If you use these agents, encounter something that doesn't work, or develop new prompts, templates, or adaptations, contributions are welcome via pull request or issue.

---

*Built for the practitioners working to rewild the narrative space.*
