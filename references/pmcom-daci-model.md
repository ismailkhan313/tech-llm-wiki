---
type: Reference
title: "DACI Decision-Making Framework: Everything You Need to Know — project-management.com"
description: The trade-press DACI guide the user dropped; kept as a specimen of the derivative layer. Useful for its operational checklists and failure modes, unreliable on origin, and internally inconsistent in rendering DACI as a task matrix.
tags: [source, daci, decision-making, specimen, derivative-layer, trade-press]
resource: https://project-management.com/daci-model/
author: human:marianne-sison
fidelity: excerpt
retrieved: 2026-09-19T00:00:00Z
generated: { by: claude-code/opus-5, at: 2026-09-19T00:00:00Z }
status: stable
---

<!--
  Marianne Sison, "DACI Decision-Making Framework: Everything You Need to
  Know", project-management.com (TechnologyAdvice).

  EXCERPT, not a mirror. Advertising, vendor placements, affiliate template
  CTAs, newsletter forms and author bio are stripped; the substantive prose
  is quoted where it is load-bearing. Copyright TechnologyAdvice. The
  canonical page wins over this copy.

  KEPT AS A SPECIMEN, not as an authority. The page is monetised trade press
  with embedded vendor placements (ClickUp, monday.com, Smartsheet, Wrike),
  and its origin claim is unsourced. Its value here is (a) the operational
  checklists, which are sensible and which the primary vendor documentation
  omits, and (b) as a documented example of how the derivative layer garbles
  a framework. See /daci-framework.md and /daci-vs-raci.md.
-->

## Definition and origin claim

> DACI, which stands for Driver, Approver, Contributor, and Informed, is a
> decision-making framework that assigns one of four roles to each stakeholder
> based on their level of involvement in a decision. It was developed as a
> variation of the RACI matrix to clarify who is responsible for driving a
> decision and who makes the final call.
>
> **The DACI framework was developed by Intuit, a US-based financial software
> company, in the 1980s to address decision paralysis.** This issue often arises
> when a team lacks ownership, which leads to confusion about who makes the final
> call, who should be consulted, and who should simply be informed of the
> outcome.

<!--
  READER'S NOTE. The Intuit/1980s claim carries no citation here and no
  citation anywhere else it appears. Atlassian's own DACI play — the
  framework's actual populariser and the closest thing to primary
  documentation — does not mention Intuit at all. Treat as unverified.
-->

> A key principle of DACI is that each role should be assigned to a specific
> individual — not a team, department, or job title. For example, instead of
> assigning "Marketing" as a Contributor, assign "Jane Smith, Marketing Manager."
> This ensures accountability, prevents diffusion of responsibility, and avoids
> the common ambiguity seen in poorly defined RACI charts.

## The roles, as tabulated

| Role | Responsibility | Has a vote? | How many? |
|---|---|---|---|
| Driver | Manages the decision-making process, assigns tasks, and ensures a decision is reached on time | No | One |
| Approver | Makes the final call on the decision | Yes | One (ideally) |
| Contributor | Provides input, expertise, and recommendations to inform the decision | No | As many as needed |
| Informed | Notified of the outcome after the decision has been made | No | As many as needed |

On the Driver:

> Think of this as the project manager or sole coordinator for the decision
> itself. What they do have is ownership over the *process*, so the team reaches
> an outcome. They gather inputs, pull in the right people, and make sure a
> recommendation actually lands on the Approver's desk. So if the decision is
> delayed, that's on the Driver to fix.

On the Approver:

> The Approver is the person who makes the final call once the Driver has done
> the legwork and put together a recommendation. There is only one Approver for
> each decision because **the moment you have two Approvers who disagree, you're
> back to the exact problem DACI was supposed to prevent.**

On Informed:

> Getting this role right comes down to timing: share the decision early enough
> to be useful, but avoid including them in discussions they do not need to be a
> part of.

## The five steps

> **The best time to do this is after the project charter is approved and before
> the project kickoff meeting.**

1. **Name the decision precisely.** *"Write it as a single question that is
   specific enough to act on. For example, 'our marketing strategy' is too broad
   to assign roles. You can make it more detailed with, 'Do we run a paid
   acquisition campaign in Q3 targeting SMB customers in Southeast Asia?'"*
2. **List everyone connected to the decision.** *"Do not filter yet."*
3. **Assign the four roles.** *"Each person should only hold one role. The Driver
   and Approver cannot be the same individual... Choose an Approver who holds
   authority over the outcome, not just the most senior person."*
4. **Set a decision deadline.** *"Most decisions that involve multiple teams take
   one to two weeks. Three weeks is a reasonable ceiling for decisions that
   require significant data gathering and deeper analysis."*
5. **Document and share the decision.** *"This gives the Driver something to
   reference if someone tries to expand their role beyond what was agreed
   upon."*

## The task-matrix rendering

The article's second worked example plots DACI letters across tasks and people,
in the shape of a RACI matrix:

| Tasks | Project manager | Content director | Expert writer | Graphic design | Website developer |
|---|---|---|---|---|---|
| Write a new blog | A | C | D | I | I |
| Send newsletter | D | A | C | C | I |
| Update WordPress templates | D | A | I | I | C |
| Redesign website logo | D | A | I | C | I |

> Rather than a quadrant that limits information to a single process, a DACI
> chart allows for plotting multiple tasks and role assignments.

<!--
  READER'S NOTE. This is the article contradicting itself, and it is the most
  instructive thing on the page. Every row here is a recurring *task*, not a
  decision: "write a new blog" has no options to choose between and no
  decision deadline. Rendered this way DACI collapses into RACI with the
  letters relabelled, which is exactly the confusion /daci-vs-raci.md exists
  to prevent.
-->

## The five common mistakes

> 1. **Assigning more than one Approver**: This is the most common mistake. When
>    two people share the Approver role, no one has the authority... If two
>    stakeholders must sign off, split the decision into smaller parts and assign
>    one Approver to each.
> 2. **Making the Driver and Approver the same person**: This may seem efficient,
>    but it weakens the process. The Driver is meant to stay neutral and manage
>    input. If the same person also makes the final decision, Contributors may
>    hold back, and the decision loses objectivity.
> 3. **Adding Contributors too late**: Contributors are most useful early in the
>    process, when the decision is still taking shape. Bringing them in after
>    direction is set limits their impact. Set a deadline for input so everyone
>    knows when to contribute.
> 4. **Forgetting to update the Informed group**: ... Make it the Driver's
>    responsibility to share the outcome as soon as it is finalized.
> 5. **Using DACI when it is not needed**: DACI adds structure, and structure
>    takes time. Using it for simple or low-impact decisions creates unnecessary
>    overhead. Reserve it for decisions that involve multiple stakeholders and
>    require decision ownership.

## DACI vs RACI, per the article

> Most teams do not need to choose one over the other. You can use RACI to manage
> ongoing work, then apply DACI when a specific decision needs structure and
> ownership.
>
> Remember, **the biggest bottleneck in projects is not task execution but
> unclear decision authority.** That is where DACI adds the most value.

From the FAQs:

> **Can a team have more than one Approver in DACI?** Yes... but it is not
> recommended... If dual sign-off is unavoidable, split the decision into two
> separate decisions, each with its own Approver.
>
> **When should you use the DACI framework?** Use DACI when a decision involves
> multiple stakeholders or teams, such as product roadmap prioritization, vendor
> selection, or budget allocation, where no one is responsible for making the
> final call. **If a decision is straightforward and easy to reverse, you do not
> need to rely on the DACI framework.**
>
> **Is DACI suitable for agile teams?** Yes... You can use it during sprint
> planning or backlog grooming when it is unclear who should make the final
> decision. For smaller decisions, keep role assignments simple so the process
> does not slow the team down.
