# references

Raw source materials for the wiki: articles, papers, transcripts, and
links, kept as-is. Immutable — concepts derive from these, but nothing
here gets edited to fit the wiki.

Each entry notes whether the local copy is verbatim or an agent transcription;
for anything not verbatim, the canonical URL in the file header wins.

## Sources

- [karpathy-llm-wiki.md](karpathy-llm-wiki.md) — Andrej Karpathy, "LLM Wiki"
  (gist). The originating statement of the pattern. *Verbatim.*
- [okf-announcement-google-cloud.md](okf-announcement-google-cloud.md) — Sam
  McVeety & Amir Hormati, "Introducing the Open Knowledge Format," Google
  Cloud blog, 2026-06-12. Describes OKF v0.1. *Agent transcription, not
  verbatim.*
- [google-cloud-agentic-design-patterns.md](google-cloud-agentic-design-patterns.md) —
  Samantha He, "Choose a design pattern for your agentic AI system," Google
  Cloud Architecture Center, last reviewed 2026-05-28. The twelve agent
  design patterns and the framework for choosing between them. *Verbatim
  prose; site chrome dropped, diagrams referenced by URL.*
- [mcp-getting-started-intro.md](mcp-getting-started-intro.md) — "What is the
  Model Context Protocol (MCP)?", MCP documentation version 2026-07-28. The
  USB-C analogy, what MCP enables, and who benefits. *Verbatim, from the
  markdown source the docs site serves at the same path with a `.md` suffix.*
- [mcp-architecture-overview.md](mcp-architecture-overview.md) — "Architecture
  overview," MCP documentation version 2026-07-28. Participants, the data and
  transport layers, statelessness and discovery, primitives, notifications, and
  a full JSON-RPC worked example. Note this revision deprecates the sampling and
  logging client primitives and replaces the `initialize` handshake with
  `server/discover`. *Verbatim, same source form as above.*
- [context-engineering-coinage-tweets.md](context-engineering-coinage-tweets.md) —
  the two June 2025 posts on X that named context engineering: Tobi Lütke
  proposing the term, and Andrej Karpathy's quote-tweet endorsing it and
  supplying the definition that stuck. *Verbatim, captured via the fxtwitter
  API mirror — x.com refuses unauthenticated fetches.*
- [anthropic-effective-context-engineering.md](anthropic-effective-context-engineering.md) —
  Anthropic Applied AI team, "Effective context engineering for AI agents,"
  2025-09-29. Context rot and the attention budget, the anatomy of effective
  context, just-in-time retrieval, and the long-horizon techniques.
  *Verbatim prose; site chrome and the two diagrams dropped, inline links
  preserved.*
- [wikipedia-prompt-engineering.md](wikipedia-prompt-engineering.md) —
  Wikipedia's "Prompt engineering," revision 1373316427 (2026-09-05). The
  techniques catalog, model sensitivity, automated prompt generation,
  limitations, history, and prompt injection. *Excerpt — prose unmodified but
  tables, figures, and ~250 citations dropped; the canonical article wins.*
- [a2a-protocol-what-is-a2a.md](a2a-protocol-what-is-a2a.md) — "What is A2A?",
  the A2A protocol's own introduction, retrieved 2026-09-06. The problems it
  solves, its benefits and design principles, its relationship to MCP and ADK,
  and the request lifecycle. *Verbatim; image and intra-docs links absolutized.*
- [anthropic-agent-skills-overview.md](anthropic-agent-skills-overview.md) —
  "Agent Skills," Claude Platform documentation, retrieved 2026-09-07. Why
  Skills exist, the three levels of progressive disclosure, the architecture,
  the surfaces they run on, `SKILL.md` structure, security, and platform
  limits. *Verbatim, from the markdown source the docs site serves at the same
  path with a `.md` suffix; the docs' own frontmatter replaced by the OKF
  block.*
- [anthropic-agent-skills-best-practices.md](anthropic-agent-skills-best-practices.md) —
  "Skill authoring best practices," Claude Platform documentation, retrieved
  2026-09-07. Conciseness, degrees of freedom, naming and descriptions,
  progressive-disclosure patterns, workflows and feedback loops,
  evaluation-driven development, anti-patterns, and executable-code guidance.
  *Verbatim, same source form as above.*
- [claude-code-skills.md](claude-code-skills.md) — "Extend Claude with skills,"
  Claude Code documentation, retrieved 2026-09-07. Bundled skills, where skills
  live and how name conflicts resolve, the full frontmatter reference including
  Claude Code's extensions to the open spec, invocation control, arguments and
  substitutions, dynamic context injection, forked subagent skills, sharing,
  and troubleshooting. *Verbatim; the site's "Documentation Index" banner for
  automated fetchers dropped.*
- [agentskills-io-specification.md](agentskills-io-specification.md) —
  "Specification," agentskills.io, retrieved 2026-09-07. The open Agent Skills
  format: directory layout, the six frontmatter fields and their constraints,
  the `scripts/`/`references/`/`assets/` conventions, progressive-disclosure
  budgets, and validation. *Verbatim, banner dropped.*
- [agentskills-io-best-practices.md](agentskills-io-best-practices.md) — "Best
  practices for skill creators," agentskills.io, retrieved 2026-09-07.
  Grounding skills in real expertise, refining with real execution, scoping
  skills as coherent units, calibrating control to fragility, and the
  instruction patterns — gotchas, templates, checklists, validation loops,
  plan-validate-execute. *Verbatim, banner dropped.*
- [anthropic-ai-native-sdlc-playbook.md](anthropic-ai-native-sdlc-playbook.md) —
  "The AI-Native SDLC Playbook," Claude Academy, retrieved 2026-09-08. All
  fourteen lesson pages of Anthropic's Applied AI team's course, concatenated in
  course order under the six stage headings: the case that the bottleneck moved
  out of the build phase, the twelve plays, and the regulated-enterprise
  managed-settings configuration. *Verbatim prose; converted from each lesson's
  server-rendered article element, site chrome and copy buttons dropped,
  headings demoted one level, the three figures referenced by URL.*
- [genai-leader-module-1-slides.md](genai-leader-module-1-slides.md) through
  [module-5](genai-leader-module-5-slides.md) — Google Cloud Skills Boost,
  "Generative AI Leader (ILT)" course slide decks. *Agent transcription of
  the official PDFs.*
