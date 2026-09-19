---
type: Reference
title: "Project dependencies: Types & ways to manage them effectively — Atlassian"
description: Atlassian's Agile Coach page on the four logical relationship types and how to identify and manage dependencies; clear on definitions, and carrying a worked example that reverses itself between consecutive paragraphs.
tags: [source, dependency-mapping, dependencies, atlassian, agile, project-management, critical-path, precedence, vendor-content]
resource: https://www.atlassian.com/agile/project-management/project-management-dependencies
author: org:atlassian
fidelity: excerpt
retrieved: 2026-09-19T00:00:00Z
generated: { by: claude-code/opus-5, at: 2026-09-19T00:00:00Z }
status: stable
---

<!--
  Atlassian, "Project dependencies: Types & ways to manage them effectively",
  Agile Coach / project management guide. Byline "By Atlassian", undated.
  https://www.atlassian.com/agile/project-management/project-management-dependencies

  EXCERPT. The page is roughly 90% site navigation by line count; the
  article body is reproduced here close to complete, with the Jira CTAs and
  the "Recommended for you" block dropped. Atlassian copyright; the
  canonical page wins. Atlassian revises these pages without changelogs, so
  treat as a dated snapshot.

  STANDING. Despite the "Agile Coach" home, this is a generic project
  management explainer, not agile guidance — it never mentions cross-team
  dependencies, PI planning, Scrum of Scrums or any scaled mechanism. Its
  definitions of the four logical relationships are correct; three of its
  four examples are not. Recorded below because the errors are instructive.
-->

## Key takeaways, as printed

> - Dependencies in project management are tasks that rely on outputs from other
>   tasks, affecting sequencing and scheduling.
> - Types include finish-to-start, start-to-start, finish-to-finish, and
>   start-to-finish relationships.
> - Managing dependencies improves planning accuracy, reduces delays, and
>   enhances risk management.
> - Identify, map, and communicate dependencies to keep projects on track and
>   optimize resource allocation.

## What are project dependencies?

> Whether you're developing software, manufacturing physical products, or
> providing services, projects consist of interrelated, sequenced tasks.
> **Dependencies are tasks within a project that provide output or information
> necessary for other tasks.**

> For example, a landscaping project will likely fail if you plant the shrubs
> first. **Before planting, you must install underground sprinklers, and before
> placing the sprinklers, you need to connect to a water source.**
>
> In this example, **the water source is dependent on installing sprinklers, and
> installing sprinklers is dependent on planting the shrubs.**

<!--
  READER'S NOTE. Those two sentences are consecutive on the page and they
  contradict each other. The first establishes the order water source ->
  sprinklers -> shrubs. The second states the dependencies in exactly the
  reverse direction: water source depends on sprinklers, sprinklers depend
  on shrubs. Direction is the entire content of a dependency statement, so
  this is not a typo in a minor detail. Reproduced verbatim so the error is
  on the record rather than silently corrected.
-->

## The four types

> **Finish-to-start** means the dependent task cannot start before another task
> is complete. For example, the design of a new product feature cannot begin
> until the requirements are ready. This type is easy to sequence in the project
> plan.

> **Start-to-start** means that the dependent task cannot begin until another
> task also begins. For example, writing technical documentation for a product
> cannot begin until QA testing also begins. *This ensures that product
> development—or coding—is complete, and changes to the scope that may impact
> the documentation are less likely to occur.*

> **Finish-to-finish** means the team cannot finish the dependent task until
> another one is completed. *An underground sprinkler system, for example,
> cannot proceed until after planting all the shrubs because you need to test
> and tune the sprinkler system to ensure all plants receive water.*

> **Start-to-finish** means that the dependent task remains incomplete until
> another task begins. This is common in sequences requiring smooth handoff from
> one task to another. For example, **a security guard cannot finish their shift
> until the next guard arrives for their shift.** Often, this includes
> transferring information from the team that is completing their task to the
> team beginning the next task.

<!--
  READER'S NOTES on the examples (the four definitions themselves are
  correct and standard):

  - Start-to-start: the definition is right, the justification is not. The
    reason given ("this ensures that coding is complete") describes a
    finish-to-start relationship with development, not a start-to-start
    relationship with QA.
  - Finish-to-finish: "cannot proceed until after planting all the shrubs"
    states a start constraint, not a finish constraint, and reverses the
    sprinklers-before-planting order the page established two sections
    earlier.
  - Start-to-finish: this one is good, and is the clearest short statement
    of the rarest relationship type found anywhere in the sources read.
-->

## Benefits

> **Better project planning.** Identifying each task and its dependencies helps
> teams adhere more closely to project scope, improves decision-making, and
> optimizes forecasting resource needs.
>
> **Improved scheduling accuracy.** Sequencing tasks based on their dependencies
> gives teams a clear view of the project schedule... **When making hard
> decisions midway through the project, it's easier to see the consequences of
> changes when you understand the task dependencies.**
>
> **Reduced project delays.** Defining task dependencies and sequencing the work
> during the planning phase reduces surprises that can result in delays after
> the project has begun.
>
> **Improved risk management.** Dependency mapping helps identify project risks
> during planning. Early awareness of the risks provides more time to develop
> mitigation plans should risks become a reality.

## How to identify dependencies

> A dependency is any task in the project that provides information or output to
> another task. **This may be a deliverable, such as an API or database
> structure, or a handoff point, such as completing code and moving into QA
> testing.**

> **Review project tasks.** During project planning, review each task to identify
> whether it requires output or information from any other task in the project.
> **Ask what tasks you need to start or finish before the task can begin.**
>
> **Collaborate with team members.** Consult with all team members, including
> stakeholders, partners, customers, and business members. **Each person brings
> experience and awareness of hidden dependencies that could delay the
> project.** For example, awareness that a task in finance provides necessary
> output for a task in development, such as purchasing new equipment, allows the
> team to work together...
>
> **Analyze task requirements.** When identifying dependencies, analyze the
> requirements for each task. Requirements define the output or information the
> dependency task provides. For example, if the output is an API used for a
> dependent task, define the requirements of the API. **Are there specific data
> restrictions or field formats that must be met? Analyzing task requirements can
> help identify missing tasks.**

## How to manage dependencies

> **Dependency charts** help the team visualize the workflow and timeline.
> Waterfall-style project timelines and flowcharts effectively depict tasks and
> their dependencies visually.
>
> **Dependency mapping** provides a rich, single source of detailed information
> about each task. **It can include system impacts, risks, mitigation plans, and
> assigned owners.**
>
> **Communication** is the key to successful dependency management. Team members
> need to know when they can begin working on their tasks, who is responsible
> for dependent tasks, and when things change. **Consider a tiered approach to
> communication, such as including dependencies in your standard project
> dashboard reports and push-style notices when things change.**
>
> **Critical paths** identify the longest elapsed time for all dependent tasks,
> from start to finish.

## Impact on project success

> A dependency may be obvious to some and not to others, especially if they lack
> direct involvement with tasks that require the information or output.
> **Regardless of the task's size or output, never assume that everyone knows its
> importance.**

> For example, writing technical documentation may depend on the completion of
> product development and its handoff to testing. **If the team does not identify
> and monitor that task, the technical writer may not know when the handoff will
> happen, which can cause a delay.** That delay could ultimately result in a
> postponed release to the customer, especially for highly technical or
> regulated products.

## What the page does not cover

- **No dependency taxonomy beyond the four logical relationships.** No
  mandatory vs. discretionary, no internal vs. external — so nothing tells a
  reader which dependencies are removable.
- **No leads and lags**, which are the standard modifiers of all four
  relationship types.
- **Nothing on cross-team or cross-project dependencies**, despite sitting in
  an agile guide; no PI planning, no Scrum of Scrums, no program board.
- **No treatment of cyclic dependencies**, and the recommended visualizations
  (waterfall timelines, flowcharts) cannot represent them.
- **No register, owner, cadence or escalation mechanics** — "assigned owners"
  is mentioned once as a field and never developed.
