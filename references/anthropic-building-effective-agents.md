---
type: Reference
title: "Building effective agents — Erik S. and Barry Zhang, Anthropic (2024)"
description: The post that fixed the working definitions of agentic system, workflow and agent, set out the five composable workflow patterns, and argued for finding the simplest solution that works before reaching for an agent.
tags: [source, agents, workflows, agentic-systems, design-patterns, anthropic]
resource: https://www.anthropic.com/engineering/building-effective-agents
author: anthropic:erik-s,anthropic:barry-zhang
fidelity: excerpt
retrieved: 2026-09-16T15:40:00Z
generated: { by: claude-code/opus-5, at: 2026-09-16T15:40:00Z }
status: stable
---

<!--
  Erik S. and Barry Zhang, "Building effective agents," Engineering at
  Anthropic, published 2024-12-19.

  EXCERPT. The definitional sections, the five workflow patterns with their
  "when to use" guidance, the agents section and the summary are reproduced
  in full; Appendix 1 ("Agents in practice") and Appendix 2 ("Prompt
  engineering your tools") are summarized rather than reproduced, and the
  post's eight diagrams are not reproduced at all. The canonical copy wins.

  Note carried by the live page as of retrieval, above the body:

    "Note: Much of the tooling landscape described in this post has changed
    since December 2024. For our current approach, see how we built Claude
    Managed Agents and the Managed Agents documentation."

  The definitions and patterns are what this wiki uses the post for, and
  that note does not disturb them — but it is why the post should be read
  as the origin of a vocabulary rather than as current tooling advice.
-->

> We've worked with dozens of teams building LLM agents across industries.
> Consistently, the most successful implementations use simple, composable
> patterns rather than complex frameworks.

## What are agents?

> "Agent" can be defined in several ways. Some customers define agents as fully
> autonomous systems that operate independently over extended periods, using
> various tools to accomplish complex tasks. Others use the term to describe
> more prescriptive implementations that follow predefined workflows. At
> Anthropic, we categorize all these variations as **agentic systems**, but draw
> an important architectural distinction between **workflows** and **agents**:
>
> **Workflows** are systems where LLMs and tools are orchestrated through
> predefined code paths.
>
> **Agents**, on the other hand, are systems where LLMs dynamically direct their
> own processes and tool usage, maintaining control over how they accomplish
> tasks.

## When (and when not) to use agents

> When building applications with LLMs, we recommend finding the simplest
> solution possible, and only increasing complexity when needed. This might mean
> not building agentic systems at all. Agentic systems often trade latency and
> cost for better task performance, and you should consider when this tradeoff
> makes sense.
>
> When more complexity is warranted, workflows offer predictability and
> consistency for well-defined tasks, whereas agents are the better option when
> flexibility and model-driven decision-making are needed at scale. For many
> applications, however, optimizing single LLM calls with retrieval and
> in-context examples is usually enough.

## When and how to use frameworks

The post names the Claude Agent SDK, the Strands Agents SDK by AWS, Rivet and
Vellum, then warns:

> These frameworks make it easy to get started by simplifying standard low-level
> tasks like calling LLMs, defining and parsing tools, and chaining calls
> together. However, they often create extra layers of abstraction that can
> obscure the underlying prompts and responses, making them harder to debug.
> They can also make it tempting to add complexity when a simpler setup would
> suffice.
>
> We suggest that developers start by using LLM APIs directly: many patterns can
> be implemented in a few lines of code. If you do use a framework, ensure you
> understand the underlying code. Incorrect assumptions about what's under the
> hood are a common source of customer error.

## Building block: the augmented LLM

> The basic building block of agentic systems is an LLM enhanced with
> augmentations such as retrieval, tools, and memory. Our current models can
> actively use these capabilities—generating their own search queries, selecting
> appropriate tools, and determining what information to retain.

The post points at the Model Context Protocol as one way to implement those
augmentations, and assumes for the rest of the post that every LLM call has
access to them.

## Workflow: prompt chaining

> Prompt chaining decomposes a task into a sequence of steps, where each LLM call
> processes the output of the previous one. You can add programmatic checks (see
> "gate" in the diagram below) on any intermediate steps to ensure that the
> process is still on track.
>
> **When to use this workflow:** This workflow is ideal for situations where the
> task can be easily and cleanly decomposed into fixed subtasks. The main goal is
> to trade off latency for higher accuracy, by making each LLM call an easier
> task.

Examples given: generating marketing copy then translating it; writing an
outline, checking it against criteria, then writing the document from it.

## Workflow: routing

> Routing classifies an input and directs it to a specialized followup task. This
> workflow allows for separation of concerns, and building more specialized
> prompts. Without this workflow, optimizing for one kind of input can hurt
> performance on other inputs.
>
> **When to use this workflow:** Routing works well for complex tasks where there
> are distinct categories that are better handled separately, and where
> classification can be handled accurately, either by an LLM or a more
> traditional classification model/algorithm.

Examples given: directing customer service query types down different
downstream processes; routing easy questions to a smaller, cost-efficient model
and hard ones to a more capable model.

## Workflow: parallelization

> LLMs can sometimes work simultaneously on a task and have their outputs
> aggregated programmatically. This workflow, parallelization, manifests in two
> key variations:
>
> **Sectioning**: Breaking a task into independent subtasks run in parallel.
>
> **Voting:** Running the same task multiple times to get diverse outputs.
>
> **When to use this workflow:** Parallelization is effective when the divided
> subtasks can be parallelized for speed, or when multiple perspectives or
> attempts are needed for higher confidence results. For complex tasks with
> multiple considerations, LLMs generally perform better when each consideration
> is handled by a separate LLM call, allowing focused attention on each specific
> aspect.

Examples given — sectioning: a guardrail instance screening queries while
another answers them; automated evals where each call scores a different
aspect. Voting: several differently-prompted reviews of the same code for
vulnerabilities; multiple content-moderation passes with different vote
thresholds to balance false positives and negatives.

## Workflow: orchestrator-workers

> In the orchestrator-workers workflow, a central LLM dynamically breaks down
> tasks, delegates them to worker LLMs, and synthesizes their results.
>
> **When to use this workflow:** This workflow is well-suited for complex tasks
> where you can't predict the subtasks needed (in coding, for example, the number
> of files that need to be changed and the nature of the change in each file
> likely depend on the task). Whereas it's topographically similar, the key
> difference from parallelization is its flexibility—subtasks aren't pre-defined,
> but determined by the orchestrator based on the specific input.

Examples given: coding products making complex changes across multiple files;
search tasks gathering and analyzing information from multiple sources.

## Workflow: evaluator-optimizer

> In the evaluator-optimizer workflow, one LLM call generates a response while
> another provides evaluation and feedback in a loop.
>
> **When to use this workflow:** This workflow is particularly effective when we
> have clear evaluation criteria, and when iterative refinement provides
> measurable value. The two signs of good fit are, first, that LLM responses can
> be demonstrably improved when a human articulates their feedback; and second,
> that the LLM can provide such feedback. This is analogous to the iterative
> writing process a human writer might go through when producing a polished
> document.

Examples given: literary translation, where an evaluator LLM can critique
nuances the translator missed; complex search needing multiple rounds, where
the evaluator decides whether to search again.

## Agents

> Agents are emerging in production as LLMs mature in key capabilities—
> understanding complex inputs, engaging in reasoning and planning, using tools
> reliably, and recovering from errors. Agents begin their work with either a
> command from, or interactive discussion with, the human user. Once the task is
> clear, agents plan and operate independently, potentially returning to the
> human for further information or judgement. During execution, it's crucial for
> the agents to gain "ground truth" from the environment at each step (such as
> tool call results or code execution) to assess its progress. Agents can then
> pause for human feedback at checkpoints or when encountering blockers. The task
> often terminates upon completion, but it's also common to include stopping
> conditions (such as a maximum number of iterations) to maintain control.
>
> Agents can handle sophisticated tasks, but their implementation is often
> straightforward. They are typically just LLMs using tools based on
> environmental feedback in a loop. It is therefore crucial to design toolsets
> and their documentation clearly and thoughtfully.
>
> **When to use agents:** Agents can be used for open-ended problems where it's
> difficult or impossible to predict the required number of steps, and where you
> can't hardcode a fixed path. The LLM will potentially operate for many turns,
> and you must have some level of trust in its decision-making. Agents' autonomy
> makes them ideal for scaling tasks in trusted environments.
>
> The autonomous nature of agents means higher costs, and the potential for
> compounding errors. We recommend extensive testing in sandboxed environments,
> along with the appropriate guardrails.

Examples given, both Anthropic's own: a coding agent resolving SWE-bench tasks,
and the "computer use" reference implementation.

## Combining and customizing these patterns

> These building blocks aren't prescriptive. They're common patterns that
> developers can shape and combine to fit different use cases. The key to
> success, as with any LLM features, is measuring performance and iterating on
> implementations. To repeat: you should consider adding complexity **only** when
> it demonstrably improves outcomes.

## Summary

> Success in the LLM space isn't about building the most sophisticated system.
> It's about building the **right** system for your needs. Start with simple
> prompts, optimize them with comprehensive evaluation, and add multi-step
> agentic systems only when simpler solutions fall short.
>
> When implementing agents, we try to follow three core principles:
>
> 1. Maintain **simplicity** in your agent's design.
> 2. Prioritize **transparency** by explicitly showing the agent's planning steps.
> 3. Carefully craft your agent-computer interface (ACI) through thorough tool
>    documentation and testing.
>
> Frameworks can help you get started quickly, but don't hesitate to reduce
> abstraction layers and build with basic components as you move to production.

## Appendices (summarized, not reproduced)

**Appendix 1, "Agents in practice"**, gives two domains where agents earned
their keep — customer support and coding — and generalizes: agents add most
value for tasks that "require both conversation and action, have clear success
criteria, enable feedback loops, and integrate meaningful human oversight." The
coding case leans on verifiability: code is testable, so the agent can iterate
against test results, and quality can be measured objectively. Human review is
still described as crucial for alignment with broader system requirements.

**Appendix 2, "Prompt engineering your tools"**, argues tool definitions deserve
as much prompt-engineering attention as prompts themselves, since formats that
are cosmetically equivalent to a human are not equally easy for a model to
write (a diff needs line counts in the chunk header before the code; JSON needs
escaping that markdown doesn't). Its three suggestions: give the model enough
tokens to think before it writes itself into a corner; keep the format close to
what naturally occurs in internet text; and remove formatting overhead. It
closes on the agent-computer interface (ACI) — invest in it as much as you
would in an HCI.
