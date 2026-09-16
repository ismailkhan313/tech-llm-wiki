---
type: Reference
title: "Impact of Personnel Factors on the Recovery of Delayed Software Projects — Farshchi, Jusoh & Azmi Murad (2012)"
description: A system-dynamics study of the decision to add people to a late software project, parameterised by COCOMO II's six personnel factors — the one paper that treats who you add, rather than how many, as the variable.
tags: [source, brooks-law, staffing, system-dynamics, cocomo, personnel-factors, software-estimation]
resource: https://doi.org/10.2298/CSIS110525003F
author: human:mostafa-farshchi
fidelity: excerpt
retrieved: 2026-09-15T23:50:00Z
generated: { by: claude-code/opus-5, at: 2026-09-16T00:00:00Z }
status: stable
---

<!--
  Mostafa Farshchi, Yusmadi Yah Jusoh and Masrah Azrifah Azmi Murad,
  "Impact of Personnel Factors on the Recovery of Delayed Software Projects:
  A System Dynamics Approach", Computer Science and Information Systems
  (ComSIS) 9(2):627-652, June 2012. doi:10.2298/CSIS110525003F

  Open access. ComSIS is published by the ComSIS Consortium under
  CC BY-NC-ND 4.0; this file reproduces quoted passages only, with
  attribution, and is not a substitute for the article.

  EXCERPT. Text was extracted from the journal PDF, which carries per-run
  language tags and renders equations, figures and tables as graphics. The
  equations and all seven figures are therefore ABSENT here, and the
  numbers below were read out of table cells that the extraction flattened.
  The canonical PDF wins over this copy in every case; verify before quoting.

  Free PDF: http://elib.mi.sanu.ac.rs/files/journals/csis/22/090206.pdf
  Landing page: https://doiserbia.nb.rs/Article.aspx?ID=1820-02141200003F
-->

## Abstract (verbatim)

> Delay in a software project may result in the loss of a market opportunity or
> the postponement of a dependent project. Therefore, software project managers
> take various steps to ensure that their project is completed on time, such as
> adding new members to the project team. However, adding new manpower to a
> delayed project may cause a negative impact on the team's productivity due to
> assimilation time, training overhead and communication overhead. Consequently,
> project managers have difficulty in making the decision on whether or not to
> add new members to the team. Thus, this research aims to examine whether a
> significant schedule improvement can be achieved with consideration of the new
> manpower capabilities, skills and experience. A System Dynamics Model is
> proposed to simulate the behaviour of a project progress when new members are
> added. The proposed model was evaluated through experiments using two types of
> case studies. The results of the experiments indicate that a significant
> schedule improvement of a late project can be achieved if people with certain
> levels of personnel factors are added to the project.

**Keywords:** software project management, personnel factors, system dynamics,
schedule delay.

## The three effects, as the paper states them

> As mentioned in the previous section, adding more manpower to a delayed
> software project would likely increase its completion time. This was explained
> as a consequence of the following three effects: (i) new staff need training
> and they need to be trained by experienced staff; (ii) there is an
> assimilation delay for new staff to become productive in a project; (iii)
> adding new people increases the communication overhead among the members of a
> project team.

## On Abdel-Hamid

> The study by Abdel-Hamid et al. revealed that adding more people to a late
> project did not always cause it to complete later. He assumed in his study
> that there is, in general, a desire among project managers to change the
> composition of their workforce. However, if the perceived remaining time is
> shorter than the anticipated hiring and assimilation delay, then the project
> manager would not add new manpower.

## On Stutzke's mathematical model

> Stutzke [9] investigated the possible situations in which a project may
> benefit by adding new members to the workforce. Results derived from his
> mathematical model indicate that adding new staff would not necessarily have a
> negative impact on a project if certain constraints are taken into account.
> These constraints are: […] where f = fractional increase in the staff;
> r = remaining time to complete project, a = assimilation time, and
> m = mentoring cost (fraction of staff member's time spent mentoring […])

**The inequalities themselves are rendered as an equation graphic in the PDF and
did not survive extraction.** As reported elsewhere, the two constraints are
`r > a` (remaining time must exceed effective assimilation time) and `f < 1/m`
(the fractional staff increase must stay below the reciprocal of per-hire
mentoring cost). Confirm against the PDF or against Stutzke (1994) before
relying on the exact form.

## Prior-model parameters (from the comparison table)

Read out of a flattened table; treat as approximate.

| Model | New-staff productivity | Assimilation time (days) | Mentoring / training load |
|---|---|---|---|
| Stutzke [9] | not differentiated | 33.4 | 25.0% of an experienced person's time during mentoring |
| Hsia et al. [10] | EP = 1 task/person-day; NP = 0.5 task/person-day | 80 | 20.2% of an experienced person's time during assimilation |

## Why personnel factors, and which ones

> […] the productivity drivers of COCOMO II.2000 [20] present the most
> appropriate values that can be employed as input variables of the personnel
> capabilities of our System Dynamics simulation model. The data range of
> productivity factors in COCOMO II shows that the combination of human factors
> provides the highest productivity range compared to all other types of
> factors, such as process, product, project and organisation. Six personnel
> factors from COCOMO.II(2000) [20] were employed for our study, namely, Analyst
> Capability (ACAP), Programmer Capability (PCAP), Personnel Continuity (PCON),
> Applications Experience (APEX), Platform Experience (PLEX), and Language and
> Tools Experience (LTEX).

On the mechanism linking capability to assimilation:

> […] it is rational to assume that a more capable and more experienced person
> would need less training and would become assimilated sooner than a person who
> is less capable and less experienced. Therefore, we have attempted to represent
> the impact of personnel factors on training overhead and assimilation time.

The paper also notes, citing Trendowicz and Münch's review of 249 productivity
factors, that *"team capability and experience (personnel factors) were the most
commonly cited factors."*

## Conclusion (verbatim)

> In order to fulfil the objectives of the study, a System Dynamics model was
> designed and constructed. Experiments were performed to verify and validate
> the model, and to explore the effects of adding new manpower with different
> personnel capabilities, skills and experiences to delayed software projects.
> Experiments with two case studies demonstrated that the negative effects of
> adding new manpower to the progress of a project can be considerably minimised
> when new manpower with certain levels of personnel factors is added. The
> results obtained show a significant improvement in project schedule for both
> the case studies.

> The proposed System Dynamics model can be employed for trade-off analysis of a
> software project and to forecast the impact of different decisions on changing
> manpower in a project. It has significant benefits for the software project
> managers, namely providing better clarification on the status of a project,
> forecasting the optimum staff level required to meet a deadline, and reducing
> the risk of decision making.

A caution the paper itself supplies, on the earlier case: adding people

> […] would accelerate the progress of a project only if the number of people
> added is reasonable.

## Selected references, as printed

- [3] Abdel-Hamid, T. and S. E. Madnick. *Software Project Dynamics: An
  Integrated Approach*. Upper Saddle River, Prentice-Hall. (1991)
- [8] Brooks, F. P. *The Mythical Man-Month* (Anniversary Ed.), Addison-Wesley
  Longman Publishing Co., Inc. (1995)
- [9] Stutzke, R. *A Mathematical Expression of Brooks' Law.* 9th International
  Forum on COCOMO and Cost Modeling, Los Angeles, CA, 1–24. (1994)
- [10] Hsia, P., C. Hsu and D. Kung. *Brooks' Law Revisited: A System Dynamics
  Approach.* Proceedings of 23rd Annual IEEE Computer Software and Applications
  Conference, COMPSAC, Phoenix, USA, IEEE Computer Society. (1999)
- [20] COCOMO II.2000 productivity drivers (USC Center for Software Engineering)
- [21] Trendowicz, A. and J. Münch. Factors influencing software development
  productivity — state of the art and industrial experiences.
