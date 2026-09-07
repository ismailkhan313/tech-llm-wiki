---
type: Reference
title: "The 'context engineering' coinage tweets — Tobi Lütke and Andrej Karpathy"
description: The two June 2025 posts that named and popularized context engineering — Tobi Lütke proposing the term, and Andrej Karpathy's quote-tweet endorsing it and defining it as the art and science of filling the context window.
tags: [source, context-engineering, prompt-engineering, terminology]
resource: https://x.com/karpathy/status/1937902205765607626
author: person:andrej-karpathy
fidelity: verbatim
retrieved: 2026-09-07T00:00:00Z
generated: { by: claude-code/opus-5, at: 2026-09-07T00:00:00Z }
status: stable
---

<!--
VERBATIM text of both posts, captured through the fxtwitter API mirror
(api.fxtwitter.com) because x.com returns HTTP 402 to unauthenticated fetches.
Text, timestamps, and the quote-tweet relationship are as returned by that API.
Line breaks are preserved; nothing is paraphrased. Karpathy's post is a
quote-tweet of Lütke's, which is why both are captured here in one file —
the coinage and the endorsement are a single unit of provenance.
-->

## Tobi Lütke (@tobi) — the coinage

Posted 2025-06-19 03:01:43 UTC · <https://x.com/tobi/status/1935533422589399127>

> I really like the term "context engineering" over prompt engineering.
>
> It describes the core skill better: the art of providing all the context for
> the task to be plausibly solvable by the LLM.

## Andrej Karpathy (@karpathy) — the endorsement

Posted 2025-06-25 15:54:24 UTC · <https://x.com/karpathy/status/1937902205765607626>
· quote-tweeting the post above

> +1 for "context engineering" over "prompt engineering".
>
> People associate prompts with short task descriptions you'd give an LLM in
> your day-to-day use. When in every industrial-strength LLM app, context
> engineering is the delicate art and science of filling the context window
> with just the right information for the next step. Science because doing this
> right involves task descriptions and explanations, few shot examples, RAG,
> related (possibly multimodal) data, tools, state and history, compacting...
> Too little or of the wrong form and the LLM doesn't have the right context
> for optimal performance. Too much or too irrelevant and the LLM costs might
> go up and performance might come down. Doing this well is highly non-trivial.
> And art because of the guiding intuition around LLM psychology of people
> spirits.
>
> On top of context engineering itself, an LLM app has to:
> - break up problems just right into control flows
> - pack the context windows just right
> - dispatch calls to LLMs of the right kind and capability
> - handle generation-verification UIUX flows
> - a lot more - guardrails, security, evals, parallelism, prefetching, ...
>
> So context engineering is just one small piece of an emerging thick layer of
> non-trivial software that coordinates individual LLM calls (and a lot more)
> into full LLM apps. The term "ChatGPT wrapper" is tired and really, really
> wrong.
