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
- [govs-002-project-delivery.md](govs-002-project-delivery.md) — *Government
  Functional Standard GovS 002: Project delivery*, UK Cabinet Office /
  Infrastructure and Projects Authority, version 2.1 (September 2025).
  Mandatory across UK government; clause 3.3 defines portfolio, programme,
  project and work package in one place. *Excerpt — clause 3.3 and the
  benefits-management clause only, out of a ~60-page standard. Crown
  copyright under the Open Government Licence v3.0, so reproducible with
  attribution.*
- [nasa-npr-7120-5f.md](nasa-npr-7120-5f.md) — NASA NPR 7120.5F, *NASA Space
  Flight Program and Project Management Requirements*, effective 2021-08-03.
  Its definitions of program and project, and the four program types
  (single-project, uncoupled, loosely coupled, tightly coupled) with worked
  examples. *Excerpt — Appendix A definitions and section 2.1.2 only. US
  federal work, not subject to domestic copyright. Extracted from the official
  PDF; subset-font spacing artifacts closed up, which is why it's marked
  excerpt rather than verbatim.*
- [omb-m-18-19-pmiaa.md](omb-m-18-19-pmiaa.md) — OMB M-18-19, *Improving the
  Management of Federal Programs and Projects through Implementing the PMIAA*,
  June 2018. Kept for Appendix 7, whose federal definition of "program" — a
  permanent entity defined by statutory authority — is the opposite of the
  temporary organisation PMI, MSP and GovS 002 mean by the word. *Excerpt —
  Appendix 7 only. US federal work, not subject to domestic copyright;
  bullet glyphs and apostrophes normalized.*
- [mcconnell-brooks-law-repealed.md](mcconnell-brooks-law-repealed.md) — Steve
  McConnell, "Brooks' Law Repealed?", *IEEE Software* 16(6):6–8,
  November/December 1999. The standing counter-argument: Brooks's Law is largely
  an artefact of bad estimation and worse tracking, and the point at which
  adding staff turns counterproductive arrives far later than the law implies.
  *Excerpt — the load-bearing passages only. Copyright Steve McConnell / IEEE,
  so quoted rather than mirrored. The original URL now 404s and the live site is
  behind a bot challenge; the canonical copy is an Internet Archive capture,
  which is why this excerpt exists.*
- [farshchi-personnel-factors-delayed-projects.md](farshchi-personnel-factors-delayed-projects.md)
  — Farshchi, Jusoh & Azmi Murad, "Impact of Personnel Factors on the Recovery
  of Delayed Software Projects: A System Dynamics Approach," *ComSIS*
  9(2):627–652, 2012. The one study that treats *who* you add to a late project,
  rather than how many, as the variable, parameterised by COCOMO II's six
  personnel factors. *Excerpt — abstract, conclusion and the passages on
  Stutzke's and Abdel-Hamid's prior models. Open access under CC BY-NC-ND 4.0;
  equations and figures are graphics in the PDF and did not survive extraction,
  so the canonical PDF wins.*
- [anthropic-building-effective-agents.md](anthropic-building-effective-agents.md)
  — Erik S. and Barry Zhang, "Building effective agents," Engineering at
  Anthropic, 2024-12-19. The post that fixed the working definitions of agentic
  system, workflow and agent, set out the five composable workflow patterns,
  and argued for building neither until a simpler solution fails. *Excerpt — the
  definitions, the five patterns with their "when to use" guidance, the agents
  section and the summary in full; both appendices summarized; the eight
  diagrams not reproduced. Note that the live page now carries a publisher's
  note that the tooling landscape it describes has changed since 2024.*
- [hf-virtualoasis-agents-vs-workflows.md](hf-virtualoasis-agents-vs-workflows.md)
  — VirtualOasis, "Agents vs. Workflows," Hugging Face community article,
  2025-05-06. A short secondary post whose nine citations are seven blogs, one
  vendor doc and a diagram tool, and which attributes Anthropic's definition of
  an agent to LangChain. Kept as a specimen of how the distinction travels, not
  as an authority on it. *Agent transcription — prose complete; the Mermaid
  diagram did not survive extraction, and inline link targets are preserved as
  the trailing citation list.*
- [atlassian-daci-play.md](atlassian-daci-play.md) — Atlassian Team Playbook,
  "DACI Decision-Making Framework." The closest thing to primary documentation
  for DACI: the four role definitions, the 15-minute prep / 60-minute run sheet,
  and the document template. Also the origin of the uncited "McKinsey found 25%"
  claim, and notably silent on where DACI came from. *Agent transcription — page
  body complete in original order; site navigation, product marketing and
  template CTAs dropped. Atlassian revises Playbook pages without changelogs, so
  treat as a dated snapshot.*
- [rogers-blenko-who-has-the-d.md](rogers-blenko-who-has-the-d.md) — Paul Rogers
  & Marcia Blenko, "Who Has the D? How Clear Decision Roles Enhance
  Organizational Performance," *Harvard Business Review*, January 2006, reprint
  R0601D. Introduces RAPID and the four decision bottlenecks; the serious
  statement of the decision-roles idea that RACI and DACI both gesture at.
  *Excerpt — the definitional and prescriptive passages only, as quotation. HBR
  is a paid reprint; extracted from the free full text hosted by USC's Center
  for Effective Organizations.*
- [mckinsey-limits-of-raci-dare.md](mckinsey-limits-of-raci-dare.md) — Aaron De
  Smet, Caitlin Hewes & Mengwei Luo, "The limits of RACI—and a better way to
  make decisions," McKinsey, 2022-07-25. Four pitfalls of RACI and the DARE
  replacement, ending "don't use RACI." Kept partly because it is what McKinsey
  *actually* published about this family of frameworks, against which the DACI
  statistic attributed to them does not survive. *Agent transcription — short
  post, reproduced in full apart from author bios. mckinsey.com refuses
  automated requests; recovered from an Internet Archive capture.*
- [pmcom-daci-model.md](pmcom-daci-model.md) — Marianne Sison, "DACI
  Decision-Making Framework: Everything You Need to Know,"
  project-management.com. Kept as a **specimen** of the trade-press layer rather
  than as an authority: monetised, vendor-placed, unsourced on origin, and
  internally inconsistent in rendering DACI as a task matrix. Its operational
  checklists and failure modes are genuinely useful and are what the page draws
  on. *Excerpt — substantive prose quoted; advertising and affiliate placements
  stripped.*
- [pmcom-raci-matrix.md](pmcom-raci-matrix.md) — Marianne Sison, "Understanding
  the Responsibility Assignment Matrix (RACI Matrix)," project-management.com.
  Same basis: a specimen, kept for its construction steps, four named
  practitioner quotes and an unusually honest limitations list. Silent on origin
  and on PMBOK, ITIL and COBIT. *Excerpt — substantive prose quoted; advertising
  and affiliate placements stripped.*
