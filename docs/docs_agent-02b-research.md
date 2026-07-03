# Agent 02b · Research (do)

*Companion to the "02 — Listen" video. What the Research agent is, how to work with it, and what goes in and comes out.*

**Listen is two agents**: **02a designs the research, 02b runs it.** This page covers 02b; see the Agent 02a page for the design agent. Each is its own Project — and 02b needs the **Exa Search** connector enabled.

---

## ✅ Before you start — install checklist (Agent 02b · Research)

*Uses the same three file types as every agent; only the Agent KBs differ. The three Shared KBs are identical across all agents.*

**Instructions field:**

- [ ] `02b_Research_Instructions.md`

**Agent KBs (upload):**

- [ ] `KB_02b_Research_Module.md`
- [ ] `KB_02b_Research_Actions.md`
- [ ] `KB_02b_Research_Prompting.md`
- [ ] `KB_02b_Research_Tools.md`
- [ ] `KB_02b_Research_MultiInquiry.md`

**Shared KBs (upload — same in every agent):**

- [ ] `KB_CHL_Method.md`
- [ ] `KB_AI_Fluency.md`
- [ ] `KB_Agent_Directory.md`

⚠ **Also:** [ ] enable the **Exa Search** connector for this Project.

---

## 1. What it is

**Agent 02b · Research** takes the Big Listening Inquiry from 02a and **executes the Big Listening**: large-scale digital research, plus processing any Small Listening data your team gathers. Its outputs are evidence-based and structural — it surfaces *what is there*, with a source for every claim. Interpretation is Agent 03's job.

Two ideas to hold onto:

- **Big vs Small Listening.** Big Listening is what AI can scan across the open web; Small Listening is community interviews, observation, and relationship-based research your team does. Big gives the structural map; Small fills what the map can't reach. You need both.
- **02b's non-negotiable rule: it does not invent anything.** Every statement it makes traces to a source in its CSV. If it can't source something, it flags it as an *unverified pattern* for Small Listening to confirm — it never states it as a finding. This matters because the Narrative Report becomes the baseline the whole cycle is measured against.

---

## 2. General instructions

**Tools:** it uses the **Exa Search** connector (deep web search) and Claude **Research mode** to synthesise. **Enable Exa in your account before running 02b.** In other chatbots without Exa, run the search with a separate tool (Perplexity, Tavily, or manually) and paste results in — the process stays the same.

**Modes:** Hacking ⚡, Learning 🌱, **Iteration 🔄** (extend the existing CSV, don't replace it), **Multi-Inquiry 🔀** (run several inquiries into one combined report), and **Small-Listening-only 🎙️** (process community material directly when no Big Listening Inquiry exists).

**How a session flows:** confirm the Inquiry is specific enough → execute Big Listening, assigning a **Folio ID** to every source in the CSV as it goes → fold in any Small Listening data, flagging where it confirms or contradicts the digital picture → draft **3–5 narrative communities** (observations only, no interpretation) → flag the strongest sources per community into the **ANP Source Library** → produce the three outputs → end with a **Handoff Checklist** of 4–6 open questions for Agent 03.

*Starter prompt:* "Here's my Big Listening Inquiry from 02a: [paste]. Run the Big Listening and produce the outputs."

**Fluency reminder for this phase:** search results reflect what's indexed and ranked — marginalised communities and non-English content are under-represented. Name those gaps in the report rather than treating the data as complete, and apply the community test to every community description.

---

## 3. Input → Output

- **Receives from 02a:** the Big Listening Inquiry. *(Also: Small Listening material; a previous CSV + report for iteration; multiple inquiries for Multi-Inquiry mode.)*
- **Produces:** **(A) Narrative Report · (B) CSV Database · (C) ANP Source Library.**
- **Passes to 03:** all three, plus the Handoff Checklist.

**The handoff in one line:** 01 → Short POV → 02a → Big Listening Inquiry → **02b → Narrative Report + CSV Database + ANP Source Library → 03**.

---

*Built on the Culture Hack Method by [Culture Hack Labs](https://www.culturehack.io/). Part of the CHL AI Agent System. Next: Agent 03 · Understand.*
