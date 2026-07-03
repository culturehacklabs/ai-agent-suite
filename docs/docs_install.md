# Install

*How to set each agent up as its own project. The pattern is identical for every agent — only the middle group of files changes.*

Each agent becomes its own **Project** in Claude. A Project holds a system prompt plus reference files the agent reads automatically.

**Accounts.** You can create Projects on a free Claude account (currently capped at around five). If you'll run the full cycle regularly, a paid plan gives more Projects and higher usage. [**Always turn off**](https://claude.ai/new#settings/data-privacy-controls) **metadata location and data sharing** so your personal information isn't used to train other models. Sign up at claude.ai.

## The three kinds of file

Every agent is built from three kinds of file. The structure is identical for every agent — only the middle group changes.

| File type | What it is | Where it goes |
| ----- | ----- | ----- |
| **1 · Instructions** (`[ID]_Instructions.md`) | The agent's identity, modes, and workflow — its "brain." One per agent. | Pasted into the Project's **Instructions / system prompt** field. |
| **2 · Agent KBs** (`KB_[ID]_*.md`) | This agent's own reference files — phase theory, output templates, prompts, tools. *This is the only group that differs between agents.* | **Uploaded** as Project knowledge. |
| **3 · Shared KBs** (3 files) | The same three files in **every** agent: `KB_CHL_Method.md`, `KB_AI_Fluency.md`, `KB_Agent_Directory.md`. | **Uploaded** as Project knowledge. |

## Set up one agent (the pattern repeats for all of them)

1. **Create a new Project.** Name it after the agent — e.g. *"CHL Agent 00 — Q&A."* *(This is shown in Claude, but the pattern — system prompt + knowledge files — works in any tool.)*
2. **Paste the Instructions** (file type 1) into the Project's **Instructions** field.
3. **Upload the Agent KBs + the 3 Shared KBs** (file types 2 and 3) as Project knowledge.
4. **Test it** with a starter prompt.

Always check `INDEX.md` for the exact Agent-KB list per agent, and use only the current files — every file is now versioned in its footer (look for `v2.0.0`). There are no old "v#"-suffixed copies to worry about; filenames are unversioned and the footer carries the version.

## Moving between agents is manual

When an agent finishes, copy its output and paste it into the next agent's Project as input, with a short preamble:

```
Here is the output from the previous phase: [paste output]
I'm ready to continue to [next phase]. Additional context: [context]
```

## Using other tools

**Other chatbots (Gemini, ChatGPT).** The agents are model-agnostic: paste the Instructions file as the system prompt / custom instruction, then paste the knowledge files into the project or chat as needed — the Module always, the Actions file when producing an output. *(Note: Agent 02b's live research uses the Exa Search connector in Claude; elsewhere, run research with a separate tool and paste results in.)*

**Local LLMs (Ollama, Hugging Face).** The system is model-agnostic and designed to work with local inference. Pair a local inference system (like Ollama) with a Web UI platform (like Open WebUI) to recreate the "Claude Project" capacity: the Instructions file becomes the system prompt and the KBs become the memory. Every KB is designed to stay under 2–4k tokens, to allow local use of the agents for technological autonomy.

---

*Built on the Culture Hack Method by [Culture Hack Labs](https://www.culturehack.io/). Part of the CHL AI Agent System. Next: Agent 00 · Q&A.*
