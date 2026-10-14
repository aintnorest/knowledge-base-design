---
type: Study Note
title: "Eye-Tracking Data: New Insights on Response Order Effects and Other Cognitive Shortcuts in Survey Responding"
description: A laboratory web-survey study links early and initially visible options to greater attention and selection, while persistent definitions reach more respondents but gaze alone does not establish comprehension.
resource: https://doi.org/10.1093/poq/nfn059
source: https://doi.org/10.1093/poq/nfn059
tags: [attention, decision-making, forms, user-research, digital-interfaces]
timestamp: 2026-10-14T21:31:53Z
---

# Response Order, Hidden Options, and Attention — Study Notes

**Authors**: Mirta Galesic, Roger Tourangeau, Mick P. Couper, and Frederick G. Conrad.  
**Published**: Public Opinion Quarterly **72(5), 892–913 (2008)**; the PMC page dates publication December 12, 2008.  
**Status**: Peer-reviewed laboratory study with three web-questionnaire experiments. Read the complete 25-page PMC article-page print captured October 14, 2026, including tables, figures, question appendix, footnotes, and references; the live PMC article supplies the full width of Table 1 clipped in the print. All four figure images were inspected. Use the version-of-record DOI as source key, not the PMC page URL.

## What It Is

An eye-tracking investigation of **how visual order and access costs influence questionnaire responses**. Instead of inferring attention solely from answers, it records fixation allocation while varying option order, visible versus hidden choices, and persistent versus on-request definitions.

The findings distinguish two mechanisms: later options can receive **less attention**, or **no recorded fixation at all**. Making information available somewhere is not equivalent to people encountering or understanding it.

## Study Design and Measures

In **February–March 2006**, **120 people** were recruited through University of Maryland campus fliers and local newspaper advertisements. Four recordings failed technically; a further ten recordings per experiment were judged unreliable. The source reports **108 people with usable recordings in at least one experiment, 106 in all three**; these counts do not straightforwardly reconcile with the per-experiment exclusion description.

Of the 108, **50% were 18–24, 35% 25–34, 15% 35–64; 51% male**. **35%** had a college degree, **52%** some college; **83%** used the Internet daily and **77%** had taken a web survey before. A roughly **10-minute, 20-question** questionnaire was followed by an unrelated experiment; total participation earned **$20**. Five experiments were embedded, three reported here.

Recorded fixations had a principal threshold of **100 ms and 20 pixels**; a 50-ms sensitivity analysis reportedly preserved conclusions. Mean fixation duration was **242 ms (SD 182)**. Tracking resolution was insufficient to identify exactly which ordinary-size words were read. Analyses also removed fixation time associated with clicking radio buttons, preventing response execution from being mistaken entirely for option evaluation.

## Results / Admissions

### Experiment 1: earlier options get more attention

For a random half of respondents, order was reversed on four questions: desirable child qualities (**12 options**), police trust (**5**), crime attribution (**2**), and responsibility for morality (**2**). Each appeared on its own screen in the questionnaire's second half.

**60%** chose a child quality from the first half (**χ²(1) = 4.20, p = .04**). For police trust, **58%** chose the first two versus last two after excluding the middle response (**n = 80, p = .12**). First-option shares for crime and morality were **54% and 51%**, nonsignificant. Thus a directional primacy pattern was not a significant choice effect for every question.

Corrected first-half/second-half fixation times were:

| Question | First half | Second half |
|---|---|---|
| Child qualities | 6,191 ms | 4,834 ms |
| Police trust | 1,227 ms | 685 ms |
| Crime | 1,214 ms | 901 ms |
| Morality | 1,077 ms | 734 ms |

Repeated-measures tests for attention differences gave **F(1,104) = 18.55, 24.10, 8.42, 10.63**, respectively, all reported significant; there were no order × list-half interactions. More top-half attention was associated with top-half selection (**OR = 2.08, 2.19, 4.62, 1.60**, all printed **p = .01**). These regressions do not establish that experimentally increasing gaze would cause the preference change.

With 12 child qualities, **10%** did not fixate either of the final two; only **54%** fixated the police scale's last option. Just **26%** fixated every point of that ordered scale, which could reflect inferring familiar intermediate labels rather than misunderstanding them. The gaze examples illustrate full traversal versus omitted final options, not a prevalence estimate by themselves.

### Experiment 2: partial visibility creates unequal exposure

Two questions asked which of **10 substantive cereal nutrients or car attributes** mattered most; “None of the above” stayed last. Order was reversed for half the sample. A third saw all options as radio buttons, a third a list showing the first five, and a third a collapsed dropdown showing none initially. This **replicates the response-format comparison of Couper et al. (2004)** with added eye tracking, not an independent replication of every gaze mechanism.

Top-half choice shares for cereal/cars were **52%/69% with all visible**, **63%/78% with five visible**, and **52%/53% with none visible**. Overall cereal primacy (**55%**) was nonsignificant; car primacy (**66%**) was significant (**χ²(1) = 10.78, p = .001**).

When five options were initially visible:

- **43%** on cereal and **41%** on cars never activated the list to see the lower options.
- Top-half fixation shares were **76% and 69%**; corresponding corrected first/second-half times were **3,537/1,142 ms** and **3,891/1,785 ms**.
- Even among those revealing the lower half, **64% and 60%** of fixation time went to the initially visible half (**p = .03 and .006**).

With all visible, top-half time shares were **59%/54%**, neither significant; with none visible, **48%/51%**, also not significantly unequal. Format effects on time allocation were significant (**F(2,89) = 16.84; F(2,98) = 6.51**, printed **p = .01**). Among only those who opened the partially visible list, between-format differences persisted for cereal (**p = .02**) but not cars. More top-half attention predicted top-half selection controlling format (**OR = 15.00 and 5.43**, printed **p = .01**).

The important comparison is **asymmetric initial visibility**, not evidence that every dropdown is worse than every radio group or that all information must always be displayed.

### Experiment 3: reach and reading depth diverge

A random half saw persistent definitions for eight nutrient terms in two grids; the other half had to reveal them by pointer rollover. Definitions averaged **29 words (range 20–32)** and sometimes contained surprising claims. They are experimental stimuli, not dietary advice endorsed by this dossier.

Each definition received a fixation from **78% on average when persistent versus 10% on request**. At least one was encountered by **all persistent-condition respondents versus 28% on request**; **45%** in the persistent condition saw all eight, versus **one person** in the rollover condition.

Conditional on encountering a definition, reading lasted **2.5 seconds persistent versus 4.2 seconds on request**, with the source reporting **t(14) = 2.35, p = .03**. Those who elect to request help are a selected subset: this is not proof that imposing an access cost improves the same person's comprehension. Longer fixation correlated with changed consumption judgments for supplements (**r = −.27, p = .01**) and grains (**r = .23, p = .02**), not an independently scored improvement in factual accuracy.

### Individual styles

Only **23%** fixated every option in all four order questions. People doing so opened more optional definitions (**1.9 versus .4**) and read initial instructions longer (**11.7 versus 7.7 seconds**). The average cross-question correlation in number of options fixated was **r = .57**. However, the proportion of attention directed to the top half was much less stable (largest **r = .24**). The study did not identify significant demographic or prior-survey-experience differences between these groups.

## Analyst Takeaways

1. **Do not interpret selection as evidence of equal consideration.** Choice distributions can reflect order and exposure rather than just underlying preference.
2. **Avoid presenting an arbitrary subset as if it were the whole choice set.** In these lists, revealing later items did not completely remove the first-visible advantage.
3. **Keep essential clarification at the decision point when broad reach matters.** Optional help can receive deeper attention from fewer people; reach, duration, comprehension, and decision quality are different outcomes.
4. **Counterbalance unordered responses without destroying meaningful scale order.** The authors recommend rotating options and making materials visible; this does not justify randomizing ordered ratings.

## Questions and Limitations

- A small, young, relatively Internet-experienced convenience sample and short desktop questionnaire constrain generalization to mobile, disabled participants, consequential purchases, or long-term behavior.
- Eye fixation is evidence of attention allocation, not direct proof of semantic processing; absent fixation can coexist with peripheral perception or inference. Associations between gaze and answers can reflect choice-directed looking as well as gaze-driven choice.
- The source reports no independent comprehension measure, objective gold-standard dietary consumption, or independent replication of its definition comparison. Its speculative suggestion to motivate requests while retaining small access costs was not experimentally tested.
- **Internal inconsistencies**: four failures plus ten poor-quality recordings per experiment imply 106 usable recordings per experiment, but the reported union of 108 and intersection of 106 cannot both follow if excluded people vary by experiment. Keep these reported counts rather than invent an exclusion flow.
- The appendix asks respondents to choose **three** child qualities, while the analysis describes choosing “a quality” and a 60% respondent-level result without explaining how three selections were summarized. Exact reconstruction is not possible from the text alone.
- Several tests with different statistics are printed as exactly **p = .01**, and the definition-time comparison is called a **paired** t-test despite between-person format assignment. Preserve the source's labels without treating them as verified analysis details.
- **Redistribution evidence**: the print exposes a “Copyright and License information” label but no explicit CC or public-domain grant; PMC availability and its general library disclaimer do not grant redistribution. The accessed PMC page also provides no explicit reusable licence in its rendered text. Keep the immutable print private.

## Vault Ideas Extracted

- [Choice Architecture Effects](/vault/choice-architecture-effects.md) — Adds randomized order/format comparisons linking early and initially visible choices with unequal gaze allocation, including later options that remain disadvantaged after disclosure.
- [Recognition over Recall](/vault/recognition-over-recall.md) — Adds a qualification that available-but-hidden clarification reaches far fewer people than persistent information, while longer conditional viewing is not demonstrated comprehension.
