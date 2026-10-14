---
type: Study Note
title: "Characteristics of Useful Code Reviews: An Empirical Study at Microsoft"
description: Microsoft's interviews and classified review logs associate artifact familiarity and fewer changed files with author-useful feedback, but usefulness excludes some learning benefits and is not measured defect detection.
resource: https://doi.org/10.1109/MSR.2015.21
source: https://doi.org/10.1109/MSR.2015.21
tags: [design-process, user-research, digital-interfaces, case-study]
timestamp: 2026-10-14T21:31:18Z
---

# Characteristics of Useful Code Reviews — Study Notes

**Authors**: Amiangshu Bosu, Michaela Greiler, and Christian Bird.  
**Published**: Mining Software Repositories (MSR), 2015; DOI 10.1109/MSR.2015.21.  
**Status**: Peer-reviewed three-stage mixed-method industrial study. Read the complete supplied 11-page manuscript, including all eight figures, three tables, and references; this copy lacks a printed publication DOI or explicit redistribution licence.  

## What It Is

A study of **usefulness from the change author's perspective**: does reviewer feedback help improve the submitted code? Interviews inform a retrospective usefulness classifier, which labels a much larger comment corpus for observational comparisons. The central distinction is between **actionable feedback on this change** and the broader value of review for learning, awareness, or relationships.

## Study Design

### Interviews and labeled evidence

Seven developers from four Microsoft projects, purposively selected for experience variation, completed approximately **30-minute interviews**. They rated **145 comments** on their recent changes as not useful, somewhat useful, or useful and explained their judgments. Approximately **69%** were useful or somewhat useful. Figure 3 distinguishes functional concerns from documentation, organization, visual representation, solution approach, false positives, and other conversation.

Researchers additionally classified **844 comments** from Azure, Bing, Exchange, Office, and Visual Studio, selecting reviews with **at least two iterations and two comments** so they could inspect subsequent changes. “Somewhat useful” was merged into useful, including maintainability-oriented minor suggestions. Together these form a **989-comment oracle**. Three authors independently classified a 100-comment subsample, differing on three; reported **Fleiss' κ = .947**.

### Retrospective classification, not advance prediction

The classifier uses post-review evidence, especially whether code near the comment changed and the final discussion status, alongside discussion/iteration and sentiment attributes. The strongest feature is a subsequent modification within **one line** of the comment's anchor. Such change proximity alone had **88% precision and 78% recall** for usefulness. Figure 4 illustrates both displaced fixes and nearby unrelated comments: proximity is not proof of causation.

Repeated **100 × ten-fold cross-validation** yielded mean **89.1% precision, 85.1% recall, and 16.6% classification error**. A separate check with **five authors**, three not in the interviews, covered **125 comments**: authors labeled **97** useful; the model labeled **105**, of which **91** agreed, yielding **86.7% precision and 93.8% recall**. The study does not validate filtering comments before authors read them; the model's most informative signals do not yet exist then.

### Large-scale observational comparisons

The paper reports **1,496,340 comments from 190,050 reviews**, with **979,440 classified useful (65.5%)**, across the same five projects. Its printed project rows do not sum to those totals, detailed below. Outcome is **comment usefulness density**, the proportion classified useful, not defects per review, escaped defects, comprehension, or overall project quality. Figures compare prior file-review experience, organizational tenure, team membership, time periods, changed-file count, and file type; no randomized assignment establishes causal effects.

## Results / Admissions

### What authors count as useful

Functional defects, corner cases, applicable conventions, and better implementation approaches were valued. Minor readability/style issues were often somewhat useful and become useful in the binary model. Questions solely for the reviewer's understanding, praise, and unrelated future work were often not useful **to the author of this change**. This does not establish that they have no educational or social benefit.

A question about how a component was tested is explicitly a not-useful example in manual labeling. That narrow label is unsuitable as a universal definition of effective safety or verification review.

### Artifact familiarity matters more than organizational proximity

- Prior changes to a file associate with useful-comment density rising **66% → 74% Azure, 60% → 71% Bing, 66% → 70% Visual Studio, 67% → 72% Office, and 62% → 63% Exchange**. More prior edits beyond the first did not add a clear difference.
- Prior review experience shows the larger association: first-time file reviewers have **32–37%** useful density versus **65–71%** with prior review experience. Figure 6 rises steeply through approximately **five prior reviews**, then levels around **70–80%**. These are proportions of comments, not a twofold increase in detected bugs.
- First-year organizational tenure associates with **60% → 66% Azure, 62% → 67% Bing, 60% → 70% Visual Studio, and 60% → 68% Office**; Exchange varies **60–65%** without a steady trend. Most increase is in the first three quarters, followed by a plateau.
- **76%** of comments come from teammates. Out-of-team densities are slightly higher: Azure **68.0/69.4%**, Bing **67.8/68.6%**, Visual Studio **66.0/69.1%**, Exchange **62.5/63.7%**, Office **66.7/66.9%** (same/different team). Most differences are under 1.5 percentage points; the authors judge these practically small despite statistical significance in a large corpus. Same-team membership is not equivalent to relevant artifact knowledge.

The authors recommend including experienced reviewers **without excluding newcomers**, because participation is how newcomers gain the knowledge needed for useful review. That is a reasoned policy implication, not an experimentally validated reviewer-allocation rule.

### Scope and file type change the review challenge

Figure 8 shows an overall downward trend in usefulness density as **changed-file count** rises, with substantial fluctuations, not a universal monotonic curve or a validated cutoff. No regression coefficient or causal size effect is supplied. More files may increase comprehension burden or cursory inspection; these are proposed explanations.

Source-code comments have approximately **70%** useful density versus **65%** for build files; solution files and makefiles are low outliers at **57% and 53%**. The authors suggest that systemic impact is harder to assess and non-code files receive less attention. They recommend small incremental changes and additional explanatory context for build/configuration changes, not treating these files as harmless.

Four projects show longer-term increases in usefulness density, with short-term peaks/valleys in three. Figure 7's time axis supplies no dates or unit values, limiting reproducibility of those temporal comparisons. **83%** of comments occur in the first two iterations; later comments are less often classified useful. This is not evidence to stop reviewing after two rounds.

## Analyst Takeaways

1. **Match the metric to the review purpose.** Author-useful changes, independent verification, learning, and social coordination are different outcomes; a metric that discounts questions should not govern all of them.
2. **Choose for relevant context, not merely seniority or team membership.** Artifact familiarity has the strongest reported association; experienced review and novice learning can coexist.
3. **Keep review scope manageable.** File count is a complexity proxy, not a universal limit, and build/configuration changes may need more context than their size suggests.
4. **Do not equate uptake with correctness.** A nearby edit or resolved discussion signals author action, not proof that a valid flaw was found or the replacement is correct. Applying these proxies to agent-change approval would need separate validation.

## Questions and Limitations

- Single company and tool, five large mature products, small qualitative sample, and a selected multi-iteration oracle limit generalization. Training and large-scale evaluation share project context; no independent organizational replication is established here.
- Classification error can distort observed associations if it varies by experience, change size, or file type; the authors explicitly have no empirical evidence excluding that possibility. The oracle's narrow author-benefit definition and reliance on subsequent edits can structurally favor some comment styles.
- Reported aggregate percentages and trend plots do not provide adjusted causal estimates, confidence intervals, or an independently measured error-detection rate.
- **Internal inconsistencies**: Table II project rows sum to **183,822 reviews, 1,450,832 comments, and 948,821 useful comments**, versus its printed totals **190,050 / 1,496,340 / 979,440**. The prose describes project densities as **64–68%**, although the table prints **63.3–68.6%**. The threats section rounds classification error to approximately 15%, versus the results' **16.6%**; retain the specific result rather than silently substituting the approximation.
- **Redistribution evidence**: the supplied manuscript contains no explicit CC, public-domain, or equivalent redistribution grant. Public availability and manuscript formatting do not confer a licence; retain the raw PDF privately and cite the version-of-record DOI.

## Vault Ideas Extracted

- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Adds author-defined usefulness evidence linking file familiarity and bounded scope to more useful comments, while showing why uptake-based proxies omit learning and do not establish error detection.
