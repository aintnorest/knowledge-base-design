---
type: Study Note
title: The Importance of Percent-Done Progress Indicators for Computer-Human Interfaces
description: A 48-person database-query experiment favored percent-done feedback, but did not establish a preference for constant latency or a progress-by-variability interaction; multitasking benefits remained proposed.
resource: https://doi.org/10.1145/317456.317459
source: https://doi.org/10.1145/317456.317459
tags: [interaction-design, ux-metrics, attention, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# The Importance of Percent-Done Progress Indicators — Study Notes

**Author**: Brad A. Myers.  
**Published**: CHI '85, April 1985, pp. 11–17.  
**Status**: Peer-reviewed conference paper; read the complete seven-page CMU author-hosted scan, including figures, tables, and appendices. Numeric results below were checked against the page images, not accepted from the imperfect text extraction.

## What It Is

An early empirical argument for showing the fraction of a task completed rather than leaving people with an uninformative wait. The paper combines interface examples, an experiment on subjective preference, and proposed explanations involving reassurance and planning.

## Principle as an Idea

A **determinate** indicator communicates completed work relative to a whole. An **indeterminate** activity cue communicates only that processing continues. The paper calls the latter “random progress”; it does not mean inventing a percentage. Its examples distinguish a filling thermometer, bar, clock, or hourglass from a moving bee or flickering pattern.

The author recommends approximate graphical feedback where exact time cannot be known, with separate representations for a current stage and the overall task when appropriate. A fraction of input processed need not equal a fraction of elapsed time: nonlinear stages, newly discovered input, and multipass work complicate the estimate. These are design rationales, not comparisons experimentally validated here.

The paper argues that continuing updates can reassure users that work has not crashed. That is conditional on updates being coupled to real processing; animation alone cannot prove that useful work is advancing.

## Experiment

**Participants**: **48 unpaid volunteers**, mostly computer-science graduate students, approximately **one fifth computer novices**. Age and gender are not reported.

**Task**: use a forms-based transportation database containing about **100 entries** to answer **eight paper questions**, requiring approximately **14 queries** per version. Participants wrote answers on a separate sheet. Each used two versions in one approximately **40-minute** session.

**Conditions**: response delay was either **10 seconds constant** or uniformly variable over **1–17 seconds**, with reported empirical mean **8.601 seconds**. During the delay a percent-done indicator was present or absent. Four comparison groups varied one factor at a time: progress versus no progress at each delay regime, or constant versus variable delay with and without progress. Random assignment balanced groups; each comparison was counterbalanced for order, producing **eight groups of six**.

**Measures**: a ten-item, intuitively chosen **1–9 semantic differential** after each version, from negative to positive feelings; explicit comparison and usefulness questions; and perceived response-time variability. The study did not measure perceived duration, multitasking productivity, or a validated anxiety construct separately. The author reports few errors and easy learning qualitatively, not a task-performance effect size.

## Results

- **More favorable ratings with progress**: Table 2 reports **F(1,44) = 13.70, p = .0006**. Reported mean ratings were **5.98 variable / 5.90 constant with progress**, versus **5.41 variable / 5.73 constant without progress**. The corresponding descriptive differences are **0.57 and 0.17 points** on the 1–9 scale; no confidence intervals or standardized effect sizes are given.
- **Explicit preference**: the paper reports **86.1%** liked progress indicators, with mean usefulness **2.94** on a reverse-direction scale where **1 = very useful** and **9 = useless, annoying**. It does not give the response denominator behind 86.1%; this is not an explained count out of all 48 participants.
- **Constant latency was not significantly preferred**: **F(1,44) = 1.66, p = .2046** overall; the no-progress-only comparison also was not significant (**p = .1497**). Constant and variable delays had different means, so this is not a pure variability comparison at matched average duration.
- **No demonstrated reversal from progress**: the descriptive ordering reversed with progress, but the variability-by-progress interaction was **F(1,44) = 2.39, p = .1296**. This failed to reproduce earlier constant-time preference findings under this task; it does not establish equivalence or overturn them for every kind of delay.
- **Order mattered**: the first version received higher ratings, **F(1,44) = 10.26, p = .0025**. Boredom with repeated use is the author's interpretation, not a separately manipulated cause.
- **Perceived variability depended on feedback**: Table 4 reports variability-by-progress **F(1,44) = 12.12, p = .0011**. The author observed people watching the bar but looking away without it; this is informal observation, not eye-tracking. Better discrimination of variability is not evidence that time felt shorter.

## What the Source Recommends versus Shows

The experiment supports **subjective preference for progress feedback in this query task**. The author further proposes that progress helps novices feel reassured, lets experienced users plan other work, and lowers tension by making the wait predictable. Multitasking, scheduling efficiency, and anxiety reduction are explanations or proposed benefits, not isolated experimental results. The paper explicitly proposes a future multiprocessing experiment.

## Analyst Takeaways

1. Give a meaningful estimate when one exists; otherwise distinguish ongoing activity from known completion fraction.
2. Keep preference, duration judgment, performance, and understanding separate. This study measured favorability, not faster processing or shorter perceived waits.
3. Do not claim that progress makes variable latency preferable: the interaction was not significant.
4. Do not generalize attended query waits into evidence for long-running background-work supervision.

## Questions and Limitations

- Small, largely technically experienced volunteer sample; no accessibility-specific evaluation, field deployment comparison, stalled-operation condition, or determinate-versus-indeterminate experiment. The examples include background work, but the experiment did not test it.
- The semantic differential was assembled intuitively; distinct emotional benefits are not isolated. Counterbalancing addresses order but does not erase the significant repetition effect.
- **Source reporting issues**: 86.1% has no stated denominator. Table 4's subject sum of squares **197.1667**, **47** degrees of freedom, and printed mean square **5.507** do not agree arithmetically; its first–second row prints sum of squares **28.1667** and mean square **28.3667** with one degree of freedom. These are printed-table issues, not extraction corrections. The discussion incorrectly interprets **p = .0006** as the probability that the effect happened by random chance; retain the test result without that interpretation.
- No independent replication of this exact progress-preference experiment is established by the supplied source. Its explicit nonreplication concerns the earlier constant-versus-variable response-time claim under different conditions.
- **Redistribution**: the scan carries an ACM copyright/copying notice, not an unrestricted republication grant. Retained privately as assigned; author hosting is not permission to republish it in this public repository.

## Vault Ideas Extracted

- [Progress and Wait Feedback](/vault/progress-and-wait-feedback.md) — Supplies preference evidence and distinguishes a completion estimate from mere activity, with background-work benefits still untested.
- [Response-Time Thresholds](/vault/response-time-thresholds.md) — Adds empirical wait-feedback evidence without validating a seconds-based cutoff or universal preference for constant latency.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Separates work-in-progress meaning from activity and completion, with measured preference rather than demonstrated multitasking improvement.
