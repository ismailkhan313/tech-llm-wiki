---
type: Reference
title: "Pareto Chart: Focusing Improvement Efforts Where They Matter — Kaizen Institute"
description: The Kaizen Institute's Pareto chart explainer; solid on construction, chart anatomy, update cadence and limitations, and a clean specimen of the Pareto misattribution that Juran spent an essay trying to stop.
tags: [source, pareto-chart, pareto-principle, kaizen, lean, quality-management, continuous-improvement, dmaic]
resource: https://kaizen.com/insights/pareto-chart-improvement-efforts/
author: org:kaizen-institute
fidelity: excerpt
retrieved: 2026-09-19T00:00:00Z
generated: { by: claude-code/opus-5, at: 2026-09-19T00:00:00Z }
status: stable
---

<!--
  Kaizen Institute, "Pareto Chart: Focusing Improvement Efforts Where They
  Matter" (Insights). https://kaizen.com/insights/pareto-chart-improvement-efforts/

  EXCERPT. Site navigation, two figures, inline product/consulting CTAs
  ("Talk to an expert", "Start improving your processes today") and the
  currency banner are dropped; the substantive prose and the full FAQ are
  quoted. Kaizen Institute copyright; the canonical page wins.

  STANDING. Better than trade-press filler — Kaizen Institute is Masaaki
  Imai's organisation and this is a competent explainer — but it is still
  marketing-adjacent content with consulting CTAs, it cites nothing, and its
  history is wrong in the specific way Juran publicly asked people to stop
  being wrong. Used for construction mechanics and limitations; not used for
  provenance. See /pareto-chart.md.
-->

## What is a Pareto Chart

> The Pareto Chart, also known as the Pareto Diagram, is a key analytical tool in
> Kaizen, Lean, and quality management that identifies the few causes with the
> most significant impact on process performance. It displays categories of
> problems, delays, or defects in descending order of magnitude. It accompanies
> them with a cumulative line that reveals how quickly a small share of causes
> accounts for most of the observed effect. **This pattern reflects the work of
> Vilfredo Pareto, whose studies showed that a minority of factors often
> determine the majority of outcomes, a phenomenon widely known as the 80/20
> rule.** In operational environments, this principle becomes evident when a small
> number of defects or deviations produces the majority of quality losses.

<!--
  READER'S NOTE. The bolded sentence is precisely the claim Juran retracted in
  "The Non-Pareto Principle; Mea Culpa": Pareto studied the distribution of
  wealth and did not generalise it, the generalisation was Juran's own, and
  the cumulative curve belongs to Lorenz. The page also uses "vital few"
  below without Juran's later correction of "trivial many" to "useful many".
  Neither error is unusual — that is why it is worth recording one.
-->

## Understanding the Pareto Chart

> A Pareto Chart is used to present process data in a structured manner,
> clarifying the relative importance of different categories. **The vertical bars
> represent the magnitude or frequency of each category. At the same time, the
> cumulative line shows how each additional category contributes to the total
> effect as they appear from left to right.** Because these categories are ordered
> from the biggest contributor to the smallest, the chart immediately highlights
> which issues dominate the overall results. This visual structure helps
> practitioners to differentiate between the vital few and the many less
> significant sources of variation.

> The chart draws on the Pareto Principle, which states that a small proportion
> of causes typically accounts for a large share of the observed effects. **The
> exact ratio may differ depending on the context, yet the pattern is consistent
> enough to provide a reliable basis for prioritization.** ... **By observing how
> rapidly the cumulative line rises and where it begins to flatten**, teams can
> identify the categories that require immediate attention and those that may be
> addressed later without compromising performance goals.

## How to build a Pareto Chart

> A Pareto Chart is typically built through the following steps:
>
> 1. Defining the problem and the scope of the data.
> 2. Collecting and categorizing information consistently.
> 3. Summarizing each category by frequency or impact.
> 4. Ordering the categories from highest to lowest.
> 5. Calculating cumulative percentages.
> 6. Constructing the bars and cumulative line on the chart.

> Data must be collected consistently and categorized in a way that ensures
> comparability. These categories may include **defect types, delay reasons,
> customer complaints, failure modes, or other measurable sources of variation.**
> Once data is gathered, each category is summarized by its total frequency or
> impact.

> The visual is constructed by plotting the bars on a **primary vertical axis
> representing magnitude** and the cumulative percentage line on a **secondary
> vertical axis.** Together, these elements show both the absolute and relative
> contribution of each category in a single, unified view.

> Accuracy and clarity are critical in this process. **Categories must be mutually
> exclusive, data collection should be objective, and labels should follow a
> consistent naming convention.** When these conditions are met, the resulting
> chart becomes a reliable tool for identifying improvement priorities and
> guiding effective resource deployment.

On tooling:

> Most organizations construct Pareto Charts using standard analytical tools such
> as Microsoft Excel, Google Sheets, Power BI, or other business intelligence
> platforms that include built-in chart functions. Statistical software packages
> such as Minitab also offer dedicated Pareto Chart capabilities... Regardless of
> the tool selected, the essential requirements remain consistent: reliable data
> collection, accurate categorization, and correct ordering of categories by
> magnitude.

## Relevance in continuous improvement

> **Pareto Analysis is the methodological process of examining data to determine
> which causes account for the majority of the observed effect. The Pareto Chart
> provides the visual basis for this analysis** and helps teams understand how
> problems are distributed across categories. By highlighting the areas with the
> greatest impact, the chart shifts organizations away from broad corrective
> actions toward focused, high-leverage interventions.

> In Kaizen and Lean Management methodologies, the Pareto Chart plays a
> foundational role in structured problem-solving. **It informs the early stages
> of analysis by directing teams toward issues warranting deeper investigation
> through tools such as root cause analysis, the fishbone diagram, process
> mapping, or standardization reviews.** When integrated into Lean Six Sigma
> practices, including DMAIC cycles, the chart enhances prioritization, supports
> evidence-based decisions, and accelerates the identification of improvement
> opportunities.

Applications named: manufacturers on defect types generating scrap or rework;
service organisations on customer complaint patterns; maintenance departments on
downtime events and failure modes; healthcare on incidents and delays.

## Limitations and considerations

Reproduced closely, because this is the most useful section on the page:

> **The chart reflects the quality of the data collected; incomplete or
> inconsistent data may distort the distribution of categories and lead to
> inaccurate conclusions.** Clear definitions, disciplined data gathering, and
> appropriate categorization are therefore essential.
>
> Operating systems also change over time. **A Pareto distribution observed during
> one period may shift as processes evolve, external conditions change, or
> improvement actions take effect.** Continuous monitoring is necessary to validate
> that priorities remain accurate and that interventions are producing expected
> results.
>
> Another important consideration is that **the Pareto Chart highlights relative
> frequency or impact but does not evaluate absolute risk. A low-frequency
> category may still require immediate action if it poses safety, regulatory, or
> compliance risks.** It is therefore essential to interpret Pareto results in the
> light of contextual knowledge, operational constraints, and strategic
> objectives.

## FAQ

**What does the 80/20 rule mean in a Pareto Chart?**

> In many processes, approximately 20 percent of the categories account for
> around 80 percent of defects, delays, or losses... Although the principle is
> commonly expressed as an 80/20 ratio, the exact percentages vary depending on
> the context. Some processes may show a 70/30, 90/10, or other distribution.
> **The specific numbers are less important than the underlying concept: impact is
> not distributed evenly across categories.**

**What is the difference between a Pareto Chart and a histogram?**

> A histogram organizes **continuous numerical data** into ranges to reveal
> distribution patterns such as central tendency, variation, or skewness... A
> Pareto Chart, by contrast, arranges **discrete categories** in descending order
> of magnitude and includes a cumulative percentage line. Its purpose is not to
> analyze distribution but to identify which categories contribute most to the
> problem's overall impact... the histogram clarif[ies] how data behaves and the
> Pareto Chart clarif[ies] where improvement efforts should be focused.

**How often should Pareto Charts be updated?**

> In stable processes with consistent performance patterns, periodic updates
> aligned with regular reporting cycles may be sufficient. In contrast, processes
> undergoing active improvement, experiencing frequent variation, or operating
> under short feedback loops benefit from more frequent updates...
>
> Within continuous improvement and Lean Daily Management systems, **Pareto Charts
> may be reviewed weekly or even daily** when they support problem-solving routines
> or monitor the effects of newly implemented actions. **In DMAIC projects, updates
> typically occur at key milestones in the Measure, Analyze, and Control phases**
> to confirm that improvement efforts are addressing the dominant contributors.
> The critical requirement is maintaining a cadence that reflects real process
> behavior.

## What the page does not cover

Recorded because the absences shaped the concept page built on it:

- **No sourcing at all.** No citation to Juran, Ishikawa, ASQ or any standard.
- **No guidance on weighting.** Categories are summarised "by frequency or
  impact" with no discussion of when counting occurrences misleads, which is the
  central practical decision in defect analysis.
- **No software or IT examples.** Manufacturing, services, maintenance and
  healthcare only.
- **No treatment of the categorisation scheme itself** beyond "mutually
  exclusive" — yet the choice of categories determines the answer.
