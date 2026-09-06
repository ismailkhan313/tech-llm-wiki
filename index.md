---
okf_version: "0.2"
---


A personal, LLM-maintained knowledge base on LLMs/AI. See
[CLAUDE.md](https://github.com/ismailkhan313/tech-llm-wiki/blob/main/CLAUDE.md) for how this wiki is structured and
maintained, and [references/](https://github.com/ismailkhan313/tech-llm-wiki/tree/main/references) for the raw sources
it's built from.

## Method

How this wiki itself works — the pattern it implements and the format it's
written in.

- [The LLM Wiki Pattern](/llm-wiki-pattern.md) — have an LLM incrementally
  build and maintain a persistent, interlinked wiki over your sources, instead
  of re-deriving synthesis from raw documents on every query.
- [Wiki Operations](/wiki-operations.md) — the three recurring operations over
  an LLM wiki (ingest, query, lint), plus the roles of `index.md` and
  `log.md`.
- [Open Knowledge Format (OKF)](/open-knowledge-format.md) — Google Cloud's
  open specification formalizing the LLM-wiki pattern as a portable bundle of
  markdown files with YAML frontmatter.
- [Operating This Wiki](/operating-this-wiki.md) — the operator's manual for
  this bundle: layer ownership, the prompts that drive each operation, the
  frontmatter fields in use, and how a note reaches the published site.

## Certifications

Study notes for certification exams — bullet-point summaries of official
course material, not general concept pages.

- [GAIL Module 1: Beyond the Chatbot](/google-GAIL/module-1-beyond-the-chatbot.md) — generative AI fundamentals — what gen AI is, foundation models, prompting, Google's gen AI ecosystem, and augmentation vs. automation.
- [GAIL Module 2: Unlock Foundational Concepts](/google-GAIL/module-2-foundational-concepts.md) — core AI/ML/DL definitions, data quality and types, ML lifecycle, foundation model limitations, secure and responsible AI, and legal implications.
- [GAIL Module 3: Navigate the Landscape](/google-GAIL/module-3-navigate-the-landscape.md) — the five-layer gen AI stack (Applications, Agents, Platform, Models, Infrastructure), agent categories, Google Cloud's MLOps tooling, cost, and solution selection.
- [GAIL Module 4: Gen AI Apps — Transform Your Work](/google-GAIL/module-4-genai-apps.md) — prompting techniques (zero/one/few-shot, role prompting, RAG), Google Workspace with Gemini, Gemini surfaces (Advanced, Gems, Notebook), and Gemini for Google Cloud.
- [GAIL Module 5: Gen AI Agents — Transform Your Organization](/google-GAIL/module-5-genai-agents.md) — agent architecture (foundation model, tools, reasoning loop), CoT/ReAct, RAG, Google Cloud agent tooling, and planning org-wide gen AI transformation.

## Meta

- [Wiki Update Log](/log.md) — chronological record of what changed and when.
