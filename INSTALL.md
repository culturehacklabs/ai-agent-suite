# INSTALL — Deploying the CHL AI Agents

This guide explains how to set up and use the CHL AI Agent System across different platforms and contexts.

---

## How the Agent Architecture Works

Each agent is built from two types of files:

**Instructions file** (`[ID]_Instructions.md`)
This is the **system prompt** — the agent's identity, operating modes, workflow, and KB load logic. In any platform, this is what you paste into the system prompt field.

**Knowledge Base files** (`KB_[ID]_*.md`)
These are the **reference documents** the agent draws on: phase theory, output templates, prompt library, tool guidance. In Claude Projects they are uploaded as project files. In other contexts they are pasted into the conversation when needed.

The split is intentional: the Instructions file is lean and stable; the KB files are modular and loaded on demand.

**A note on file sets:** the KB set is not identical across agents. Some agents split their Actions KB (Agent 04: A/B/C; Agent 05: A/B; Agent 06: A/B/C/D), and some add specialised KBs (Agent 02a: `KB_02a_SmallListening.md`; Agent 02b: `KB_02b_MultiInquiry.md`; Agent 03: `KB_03_MapCheck.md`). Always upload the files that actually exist for that agent — see `INDEX.md` for the authoritative per-agent file list.

---

## Option 1 — Claude Projects (Recommended)

Each agent becomes its own Project.

### Setup steps

**1. Create a new Project in Claude** — name it after the agent (e.g. "CHL Agent 01 — Point of View").

**2. Set the system prompt** — paste the contents of `[ID]_Instructions.md` into the Project "Instructions" field.

**3. Upload the KB files** for that agent (per `INDEX.md`), plus the three shared KBs:
- The agent's own `KB_[ID]_*.md` files (Module, Actions or Actions_A/B/C…, Prompting and Tools **where they exist**, and any specialised KBs)
- Shared: `KB_CHL_Method.md`, `KB_AI_Fluency.md`, `KB_Agent_Directory.md`

The Instructions file tells the agent which KBs to load for which task — you do not need to paste them manually.

**4. Test with a starter prompt** from the agent's `KB_[ID]_Prompting.md` (where present).

### Repeat for each agent
Each agent has its own Project. Handoffs are manual: copy the output from one agent's conversation and paste it into the next agent's Project as input.

---

## Option 2 — Other LLM Services (ChatGPT, Gemini, Mistral, etc.)

The agents are model-agnostic. Paste the Instructions file as the system prompt, then paste the relevant KB files into the conversation as context (Module KB always; Actions KB when producing outputs). Paste `KB_CHL_Method.md` for methodology questions and `KB_Agent_Directory.md` for navigation.

---

## Option 3 — Self-Hosted LLMs (Ollama, LM Studio, etc.)

Same approach: Instructions as system prompt, KB files as context.

### Important note for Agent 02b (Research)
Agent 02b executes Big Listening. The Claude-native version uses **Exa Search MCP** and **Claude Research Mode**. On a self-hosted LLM or a service without web access:
- Run web research manually and paste results in, or
- Use a separate research tool (Perplexity, Tavily, SerpAPI, etc.) and bring outputs into the agent, or
- Configure a web-search tool / RAG pipeline and update `KB_02b_Tools.md` accordingly.

The 02b KBs describe the *process and outputs* — what to collect, how to structure the CSV — regardless of which tool searches. Swap the tool, keep the process.

---

## Option 4 — Single-Chat Use (No Project Setup)

Run any agent in one conversation: paste a brief version of the Instructions, then paste the Module + Actions KBs you need, then your input. Works well for one-off tasks and workshops.

**Works well in single-chat:** POV development (01), Decode/Recode of a message (04 stand-alone), Hacking Tree for a campaign action (05 stand-alone), case study reconstruction (06).
**Works less well:** Agent 02b (web research tools unavailable without separate configuration) and Agent 03 (full ANP analysis works best with the complete KB set and iterative conversation).

---

## Passing Outputs Between Agents

Handoffs are manual — copy outputs from one agent and paste them into the next.

| From | Passes | To |
|------|--------|----|
| Agent 01 | Short POV | Agent 02a |
| Agent 02a | Big Listening Inquiry | Agent 02b |
| Agent 02b | Narrative Report + CSV Database + ANP Source Library | Agent 03 |
| Agent 03 | Community Analysis Report + Narrative Map (incl. Narrative Intentions + Window of Discourse) | Agent 04 |
| Agent 04 | Narrative Strategy + Recoded Narrative (with Message) | Agent 05 |
| Agent 05 | Hacking Tree + Logistics Plan | Agent 06 |
| Agent 06 | Case Study + updated POV | Agent 02a or 04 |

A simple preamble helps orient the next agent:

```
Here is the output from the previous phase:

[paste output]

I'm ready to continue to [next phase]. Additional context: [context]
```

---

## Shared KBs — When to Load

Loaded conditionally, never by default:

| File | Load when |
|------|-----------|
| `KB_CHL_Method.md` | Methodology, narrative theory, political stance, or the method's foundations |
| `KB_AI_Fluency.md` | Ethical AI use, data responsibility, the 4Ds framework |
| `KB_Agent_Directory.md` | Navigating between agents, confirming handoffs, checking I/O contracts |

---

## Phased Rollout (current)

Agents 00, 01, 02a, and 02b are deployment-ready. Agents 03, 04, and 05 have open items (see the audit / change log): Agent 03 has two content fixes pending, and Agent 04 is missing its Prompting and Tools KBs. Deploy the ready agents first; add 03–06 as their fixes land.

---

## Tips for Effective Use

**Be specific about context.** Vague inputs produce vague outputs.
**Use the prompt library** where it exists (`KB_[ID]_Prompting.md`).
**Iterate, don't perfect.** Every phase has an iteration workflow.
**The agent is a collaborator, not a decision-maker.** Community knowledge, political judgment, and creative vision are yours.

---

*For the full agent and file index, see [`INDEX.md`](INDEX.md). For multi-agent architecture design, see [`ARCHITECTURE.md`](ARCHITECTURE.md).*
