---
type: Reference
title: "Brooks' Law Repealed? — Steve McConnell, IEEE Software (1999)"
description: McConnell's "From the Editor" column arguing that Brooks's Law is an artefact of bad estimation and worse tracking, and that the point at which adding staff turns counterproductive arrives far later than the law implies.
tags: [source, brooks-law, staffing, software-estimation, project-tracking, ieee-software]
resource: https://web.archive.org/web/20191119004015/https://stevemcconnell.com/articles/brooks-law-repealed/
author: human:steve-mcconnell
fidelity: excerpt
retrieved: 2026-09-16T00:00:00Z
generated: { by: claude-code/opus-5, at: 2026-09-16T00:00:00Z }
status: stable
---

<!--
  Steve McConnell, "Brooks' Law Repealed?", IEEE Software 16(6):6-8,
  November/December 1999, "From the Editor" column.

  EXCERPT, not a mirror. This is a copyrighted IEEE Software column
  (Copyright Steve McConnell / IEEE); only the load-bearing passages are
  reproduced here, as quotation. The canonical text wins over this copy.

  Canonical URL note: the original stevemcconnell.com/ieeesoftware/eic08.htm
  now 404s and the live site sits behind a bot challenge, so the Internet
  Archive capture recorded in `resource` is the readable copy. That fragility
  is the reason this file exists at all.
-->

## Framing

> For more than 20 years, industry experts have been reciting Brooks' Law as
> gospel: Adding people to a late software project is like pouring gasoline on a
> fire — it just makes it later. Twenty years after the initial publication of
> *The Mythical Man-Month*, Fred Brooks reiterated that Brooks' Law was still
> "the best zeroth order approximation to the truth." […] I have evangelized
> this well-worn software engineering chestnut many times myself, but I no
> longer think it's true.

## The prevalence of the practice

> In spite of Brooks' Law, adding people to a late project remains commonplace.
> A study of software projects in the United Kingdom found that about half of
> the managers of "runaway projects" (projects that exceeded their planned
> schedules or budgets by more than 30 percent) attempted to bring their
> projects under control by adding staff.

McConnell's reference 2 for that figure: A. Cole, "Runaway Projects — Cause and
Effects," *Software World*, Vol. 26, No. 3, pp. 3–5, 1995.

## Estimation

> At Month 11, without effective project estimation in place, the plan to
> release the software at the 14-month mark is an exercise in ungrounded
> fantasy. When the software is finally released at Month 16, everyone knows
> that the project was completed later than its revised target of 14 months, but
> what no one can know with any certainty is what would have happened if new
> hires hadn't been added to the project. The claim is that adding staff to a
> late project makes it later — but later than what? Later than a systematic,
> well-founded estimate, or later than an estimate that was optimistic by more
> than 100 percent in the first place?

## Project tracking

> If we begin a 12-month project with five people instead of three, we incur
> some per-person reduction in productivity, but total productivity will be
> higher. What if we add two people to a 12-month project at the end of Month 2?
> That's still early in the project and Brooks' Law doesn't apply. Organizations
> such as NASA's Software Engineering Laboratory recommend starting software
> projects with a small senior staff and adding staff after initial requirements
> and architecture work is mostly complete. Obviously it's beneficial to add
> staff until some point in the project's schedule, after which adding staff
> becomes detrimental. Implicit in Brooks' Law is that it applies only to the
> final phases of a project. The question is, How do you know whether you're in
> a project's final phases?

> We've all participated in projects in which we arrived at the planned release
> date, took a three-week schedule slip, then continued slipping for six months
> or more after that. At the time of the first schedule slip, we don't want to
> add new staff to the "late project" because three weeks wouldn't be enough
> time for them to become productive. But six months later we wish that we had
> added the new staff, because six months would have been more than enough time
> for them to become productive. At Month 9 in the scenario above, without
> effective project tracking in place, the project manager can't know with any
> clarity whether the project is 75 percent complete or 25 percent complete.
> […] Most projects think they're 90 percent complete for the last 50 percent
> of the project, which obviously can't be the case. Because of widespread poor
> tracking, people think they're at risk from Brooks' Law for significantly
> longer periods than they really are.

## Training

> For Brooks' Law to be true, the amount of training effort required from
> existing staff must be significant. The amount of effort lost to training must
> exceed the productivity contributed by new staff when they eventually become
> productive. In Brooks' example, three people work for two months, then two more
> people are brought into the project, requiring one month of training each. This
> is absurdly conservative. How could the first three people possibly have done
> enough work in just two months to require a whole month of training for new
> staff members? […] But the loss is nothing like the ratio needed for Brooks'
> Law to be true.

## Conclusion

> "Late" chaotic projects are likely to be much later than the project manager
> thinks — project completion isn't three weeks away, it's six months away. Go
> ahead and add staff. You'll have time for them to become productive. Your
> project will still be later than your plan, but that's not a result of Brooks'
> Law. It's a result of underestimating the project in the first place. The
> additional people will help, not hurt.

> Controlled projects are less susceptible to Brooks' Law than chaotic projects.
> Their better tracking allows them to know when they can safely add staff and
> when they can't. Their better documentation and better designs make tasks more
> partitionable and training less labor intensive. They can add staff later in
> the project with less risk to the project.

> Is Brooks' Law the best zeroth-order approximation to the truth? I don't think
> so. Every project eventually reaches a point at which adding staff is
> counterproductive, but that point occurs later than Brooks' law states and in
> limited circumstances that are easily identified and avoided.

## McConnell's references, as printed

1. F.P. Brooks, Jr., *The Mythical Man-Month*, anniversary ed., Addison-Wesley,
   Reading, Mass., 1995.
2. A. Cole, "Runaway Projects — Cause and Effects," *Software World*, Vol. 26,
   No. 3, pp. 3–5, 1995.
3. The Standish Group, *Charting the Seas of Information Technology*, The
   Standish Group, Dennis, Mass., 1994.
4. *Recommended Approach to Software Development, Revision 3*, Tech. Report
   SEL-81-305, NASA Goddard Space Flight Center, Greenbelt, Md., 1992.
5. Software Eng. Inst., *Process Maturity Profile of the Software Community —
   1998 Year End Update*, Software Eng. Inst., Pittsburgh, Pa., Mar. 1999.
