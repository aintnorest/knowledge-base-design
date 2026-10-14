---
type: Study Note
title: "Evaluating Code Readability and Legibility: An Examination of Human-centric Studies"
description: A systematic review of 54 code-reading papers finds correctness and opinion dominate evaluation and many studies test only one cognitive activity, limiting claims about real-world comprehension or the superiority of particular code presentations.
resource: https://doi.org/10.1109/ICSME46990.2020.00041
source: https://doi.org/10.1109/ICSME46990.2020.00041
tags: [usability-evaluation, human-performance, cognitive-load, digital-interfaces, survey]
timestamp: 2026-10-14T21:32:27Z
---

# Human-Centric Code Readability and Legibility Studies — Study Notes

**Authors**: Delano Oliveira, Reydne Bruno, Fernanda Madeiral, and Fernando Castor.  
**Published**: IEEE International Conference on Software Maintenance and Evolution (ICSME), **2020, pp. 348–359**.  
**Status**: Peer-reviewed systematic literature review. Read the complete supplied twelve-page published IEEE-layout PDF, including seven figures, three tables, and references. The DOI is printed on page one.

## What It Is

A review of **how** human-subject studies evaluate different ways of writing code, not a meta-analysis of which coding style wins. It classifies tasks, response variables, and required cognitive activities, showing why a readability score, output-prediction test, memory task, and bug-fixing task cannot be treated as interchangeable evidence of understanding.

The paper distinguishes **readability**, the structural/semantic properties affecting understanding, from **legibility**, the visual properties affecting identification of code elements. These are related but different. Their terminology is an analytic convention, not an experimentally validated clean division of mental processes.

## Problem and Model

Reading source code is central to maintenance, but studies often claim “comprehension” from a narrow test. A reader may trace execution without explaining purpose, remember names without understanding behavior, or prefer formatting without correctly diagnosing a defect.

The authors adapt a learning taxonomy into two dimensions: **interpreting** (Remember, Understand, Analyze, Evaluate) and **producing** (None, Apply, Create). They add **Inspect**, identifying fine-grained static elements, and **Memorize**, reconstructing previously seen code. Other activities include Trace, Present, Recognize, Relate, Debug, Implement, and Adapt. Figures 3–7 map tasks into these activities and show concentrations in understanding without production; they do not prove the taxonomy's hierarchy or predictive validity.

Opinion is included in descriptive counts but excluded from the learning model. A feeling that code is clear or confidence in an answer is not itself demonstrated understanding. Time can indicate effort but needs an accuracy or task-success endpoint to distinguish efficient understanding from fast failure.

## Review Method

A manual search of nine major software-engineering conferences from **2016 to June 2019**, plus one known journal article, supplied **13 seed papers**. Automatic searches on **September 2, 2019** retrieved **1,926 ACM, 729 IEEE, and 1,909 Scopus** documents, deduplicated to **2,843**. Queries targeted title/keywords and omitted “legibility” and “software” terms to reduce unrelated hits.

Triage retained **523 papers**. First-round rejections were rechecked by another author; accepted triage decisions were not independently rechecked. Inclusion selection had two independent readers and **Cohen's κ = .323**, described as fair; disagreements and “maybe” decisions were resolved by discussion among four authors.

Included papers compared at least two fine-grained ways to write code and contained human-subject empirical studies. Exclusions included short/non-English work, metrics without empirical evaluation, high-level design/documentation, comprehension tools and visualizations, and **accessibility studies involving visually impaired or neurodiverse developers**. The review therefore cannot establish disability-specific code presentation advice.

Nine quality questions scored each paper from zero to nine. The threshold was **4.5**; actual scores ranged **5–9, median 8**, so none was excluded for quality. The authors also found **five additional studies** and excluded superseded versions; the reported final corpus remained **54**, but the arithmetic of additions/removals is not fully itemized in the paper. Data and questionnaires are linked in the source's research repository.

Four researchers extracted and synthesized tasks and response measures, with the first two developing groupings and the full team refining them. The unit counted is a **paper/primary study**, not a participant, trial, effect estimate, or necessarily an independent experiment. The review gives no pooled participant N or demographic distribution.

## Results / Admissions

### Tasks and outcomes

| Task family | Papers | Examples and boundaries |
|---|---|---|
| Provide information about code | **40/54** | **27** answer characteristics questions, **18** explain behavior, **7** remember code; overlaps allowed |
| Act on code | **15/54** | **10** find/fix bugs, **8** modify working code, **3** write code; overlaps allowed |
| Give personal opinion | **30/54** | Ratings, rankings, claimed understanding, confidence, or task difficulty |

| Response-variable category | Papers | Interpretation |
|---|---|---|
| Correctness | **45/54, 83.3%** | Includes objective execution/question answers and evaluator-scored explanations or reconstruction |
| Opinion | **30/54, 55.6%** | Preferences, self-reported understanding, confidence, perceived difficulty |
| Time | **27/54, 50%** | Completion, code-reading, per-question time, or attempts used as an indirect proxy |
| Visual metrics | **6/54** | **4** actual eye-tracking papers and **2** restricted-view “letterboxing” papers |
| Brain metrics | **3/54, approximately 5.6%** | One each using fMRI, fNIRS, or EEG |

**38 papers** used multiple response-variable categories; **16** used one. **Nine, 16.7%**, used opinion alone; none used time alone. Time and correctness co-occurred in **27**, opinion and correctness in **21**. Outcomes and categories overlap, so counts should not sum to 54.

Opinion appeared in **86% of legibility-only**, **43% of readability-only**, and **65% of combined** papers. A subjective correctness score means a human judged an explanation, not merely that the participant liked the code; keep that distinct from opinion. The review criticizes opinion-only evidence as inadequate for comprehension claims, not as useless evidence of aesthetic or workflow preference.

### Cognitive coverage

The narrative reports **25 Trace**, **16 Present**, **11 Inspect**, and **10 each Implement and Debug** papers. **20/54, 37%**, used only one activity/opinion classification, while **34** combined them. Figure 5 explicitly includes opinion in that accounting; saying all twenty measured one learning skill would be too strong, since some measured only opinion.

Interpretation-heavy tasks cluster around Understand, with much less Evaluate and little production beyond Apply. Explaining a program, choosing among explanations, or reconstructing it can recruit different activities despite superficially similar task labels. The authors recommend broader, contextualized evaluations reflecting actual development work rather than assuming one task measures all comprehension.

The review does **not** pool style effects, establish an optimal typeface, recommend a naming convention, or show that a particular formatting change improves review or maintenance. It explicitly describes a style-effect review as separate future research. No intervention effect sizes or replication rates are calculated here.

## Analyst Takeaways

1. **Evaluate the competence needed by the product task.** A code-change reviewer needs more than output prediction or a liking score; purpose, static structure, context, and defects may require separate assessments.
2. **Separate appearance from understanding.** Clear visual identification can aid semantic work without proving that the reader has built a correct model of behavior.
3. **Measure decisions as well as process.** Fixations, viewing time, or neural activity help explain effort, but none automatically establishes successful comprehension.
4. **Treat review application as an inference.** [Change Review Effectiveness](/vault/change-review-effectiveness.md) can use this task-measure framework, but these literature counts are not evidence that a particular review interface or oversight intervention works.
5. **Do not import prose-font findings uncritically.** [Typeface Legibility](/vault/typeface-legibility.md) concerns visible letter identification and reading thresholds; this review's legibility includes indentation, alignment, line breaks, and capitalization, and it does not compare font families.

## Questions and Limitations

- Search was limited to three engines, title/keywords, English full papers, and selected query terms. Five relevant studies missed by automatic retrieval demonstrate incomplete coverage. Google Scholar was omitted because it returned over 17,000 hits.
- Fair inclusion agreement, single-rater quality scoring/extraction, and insufficient task descriptions in some primary papers create classification uncertainty. Quality scores are not effect weighting or a guarantee against bias.
- Low-level code comparisons exclude larger codebase navigation, documentation, tools, and accessibility; those exclusions are important when applying findings to review interfaces, agent-produced patches, or disabled developers.
- **Internal accounting ambiguity:** inclusion first retains **54**, five more are added, and superseded papers removed, yet the final corpus is still **54** without an explicit subtraction total in the narrative.
- **Table/prose inconsistency:** Table II includes **[11]** under objective-binary correctness and omits it from subjective correctness, although the prose uses [11]'s evaluator-judged textual description as an example of subjective correctness. Do not treat that example's classification as settled.
- The prose loosely describes all **six visual-metric papers** as eye tracking, whereas Table II distinguishes **four eye tracking and two letterboxing**. The abstract rounds three brain-metric papers to **5%**, rather than **5.6%**.
- Figure 4 labels **Opinion = 28**, while Table I and the narrative report **30 opinion-task papers**; its learning-activity mapping and task counts therefore do not reconcile cleanly. The claimed **37% single cognitive skill** also includes opinion-only cases under Figure 5's caption.
- No statistical validation of the taxonomy, pooled style-effect sizes, publication-bias assessment, or systematic direct-replication analysis is provided. Narrow-task prevalence does not itself quantify how much a broader evaluation would change conclusions.
- **Redistribution evidence:** the first page prints **“©2020 IEEE”** with the publication price/copyright line. No explicit redistribution licence appears. Keep the published-layout PDF privately and cite its DOI URL.

## Vault Ideas Extracted

- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Adds a 54-paper measurement framework separating preference, tracing, explanation, static inspection, debugging, and contextual change work while identifying narrow-evaluation limits.
- [Typeface Legibility](/vault/typeface-legibility.md) — Adds the code-specific boundary between visual element identification and semantic comprehension without treating layout or liking as demonstrated understanding.
