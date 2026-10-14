---
type: Study Note
title: "Algorithm Aversion: People Erroneously Avoid Algorithms After Seeing Them Err"
description: Five forecasting studies find that observing imperfect algorithm performance reduces incentivized algorithm selection despite its superior accuracy, but do not establish universal human preference or a tested remedy for error-induced disuse.
resource: https://doi.org/10.1037/xge0000033
source: https://doi.org/10.1037/xge0000033
tags: [delegation, trust, decision-making, human-performance, digital-interfaces]
timestamp: 2026-10-14T21:30:34Z
---

# Algorithm Aversion — Study Notes

**Authors**: Berkeley J. Dietvorst, Joseph P. Simmons, and Cade Massey.  
**Published**: Journal of Experimental Psychology: General **144(1), 114–126 (2015)**; online first November 17, 2014; accepted September 25, 2014.  
**Status**: Peer-reviewed article reporting five controlled forecasting studies. Read the complete 13-page publication-layout PDF, including both stimulus illustrations, choice/confidence figures, all seven tables, payment appendices, and references. Supplemental materials/data are linked by the paper but were not independently reanalyzed here.  

## What It Is

A demonstration of **error-experience-induced disuse**: seeing an imperfect statistical model perform makes people less likely to select its future forecasts, even when it outperforms the human alternative. The key evidence is not that everyone initially prefers humans, nor that skepticism about any algorithm is irrational. It is the change in incentivized choice caused by seeing comparatively useful but fallible predictions.

[Algorithm appreciation](/dossiers/algorithm-appreciation.md) provides a complementary boundary: before prior accuracy feedback, people can prefer algorithmic advice to equivalent advice attributed to other people. Whether the comparator is **oneself or another person**, and whether **performance feedback has already occurred**, must be specified before calling a finding appreciation or aversion.

## Problem and Motivation

Humans can forgive their own errors while treating a model's visible mistakes as evidence that it should not be used. Where a model is more accurate, refusing it has an opportunity cost. The authors propose that people lose confidence more readily in algorithms than in humans after imperfect performance; the experiments manipulate exposure to performance and measure later choices, confidence, and beliefs.

“Algorithm” here means an evidence-based forecasting rule/statistical model, not a generative conversational system. Greater intolerance of algorithm error is the authors' interpretation; the study does not hold every individual human and model error numerically identical or independently manipulate confidence as the mechanism.

## Study Design

### Participants and tasks

| Study | Retained participants | Forecasting task and design |
|---|---|---|
| 1 | **361**, Wharton lab | MBA-student success percentile; randomized control, human, model, or model-and-human performance experience; **15** practice forecasts where applicable, then choose whose forecasts determine **10** incentivized outcomes |
| 2 | **206**, Wharton lab | All see both their own and model performance on **15** practice cases; randomized incentives for being within **5 percentiles (n = 70)**, within **20 (n = 69)**, or minimizing average absolute error **(n = 67)** |
| 3a | **410**, MTurk | U.S.-state airline-passenger departure rank, 1–50; four experience conditions, **10** practice cases where applicable, then one incentivized forecast |
| 3b | **1,036**, MTurk | Higher-powered direct replication of 3a, with some belief-measure/timing differences |
| 4 | **354**, Wharton lab | MBA task, but choose a previous participant's forecasts versus the model; each participant yoked to a unique Study 1 participant and shown that person's exact practice information |

Lab samples averaged **21–24 years**, **58–62% female**; online samples averaged **33–34**, **46–53% female**. Lab participants received $10 for a session of experiments and could earn up to $10 extra here; online participants received $1 plus up to $1 extra. Lab withdrawals before the key measure were **8, 4, and 0** in Studies 1, 2, and 4. Online reading-check exclusions were **77/217** and additional noncompletion **70/187** in 3a/3b. These retained samples total **2,367**; outcome-specific denominators can be smaller.

MBA success combined GPA, peer respect, employer prestige, and job success two years after graduation. Participants saw applicant features such as degree, GMAT, interview/essay evaluations, work experience, salary, and parental education; they predicted a success percentile. The model used the same available predictors. This tests forecasting a constructed outcome, not the fairness or normative desirability of using those predictors for admission.

The state task supplied airport count and ranked population, counties, household income, and domestic travel expenditure; its model used historical airline-passenger data from **2006–2010** to predict **2011**. Cases were randomly sampled without replacement from **115** MBA applicants or **50** states.

### Exposure, choice, and measures

The four experience conditions were:

- **Control:** no practice performance information before selecting a forecaster.
- **Human:** make/observe human forecasts and see the realized outcome.
- **Model:** see model forecasts and outcomes, without human performance.
- **Model-and-human:** see both forecasts and the same outcome.

After practice, participants choose **only the human or only the model** to determine their incentive for the subsequent forecast(s). There is no blending or correction condition. All then make forecasts and see model forecasts without new outcome feedback during that stage. Studies 1–3b compare the model with **oneself**; Study 4 compares it with **another participant**.

Outcomes include model selection, counterfactual bonuses under each forecaster, **average absolute error (AAE)**, five-point confidence, and performance beliefs. Tables 1–2 distinguish measurement timing; confidence is collected **after forecaster selection**, even where it precedes the incentivized forecasting stage. Thus mediation analyses do not by themselves establish confidence as a causally isolated pathway.

## Results / Admissions

### Seeing the model perform reduces selection

Figure 3 prints the following percentages; the last column tests seeing model performance versus not seeing it, pooling across the human-exposure factor.

| Study | Control | Human only | Model only | Both | Effect of seeing model |
|---|---|---|---|---|---|
| 1 | **65%** | **63%** | **26%** | **23%** | **χ²(1,N = 361) = 57.48, p < .001** |
| 3a | **57%** | **56%** | **41%** | **43%** | **χ²(1,N = 410) = 8.82, p = .003** |
| 3b | **54%** | **60%** | **44%** | **42%** | **χ²(1,N = 1,036) = 21.72, p < .001** |
| 4 | **69%** | **76%** | **38%** | **49%** | **χ²(1,N = 354) = 30.52, p < .001** |

The pattern replicates internally across two domains, online/lab samples, and self/other alternatives. Seeing human performance did **not significantly affect selection** in these four studies (**p = .706, .844, .576, .082** respectively). Initial preference is often algorithmic; the results do not support an undifferentiated “people always prefer humans” account.

In Study 2, model selection after both forecasters' performance was **34% under AAE incentives, 26% under 5-percentile incentives, and 13% under 20-percentile incentives**; **χ²(2,N = 206) = 8.50, p = .014**. A more forgiving success criterion did not remove disuse; it increased confidence in one's own forecasts. The AAE-versus-20-percentile comparison was significant (**p = .003**), whereas 5-versus-20 was **p = .059**. This study has no no-feedback arm and therefore tests robustness and incentive differences, not a new randomized exposure contrast.

### The rejected model was useful

Stage-2 model/human AAE was **22.07/26.61** in Study 1, **22.61/28.64** in 2, **4.54/8.89** in 3a, **4.32/8.34** in 3b, and **22.02/26.64** in 4; all paired differences **p < .001**. Human error was roughly **15–29% greater** on the MBA task and **90–97% greater** on the state task. Forecast–outcome correlations were **.53 model/.16 human** for MBA success and **.92/.69** for airline ranks.

Mean counterfactual bonuses favored the model in every study: **$1.78/$1.38**, **$1.77/$1.09**, **$.48/$.31**, **$.49/$.30**, and **$1.79/$1.38** respectively, all **p < .001**. These compare what forecasts would have earned, not a universal financial value for automation.

Among both-exposure participants, **610/741 (83%)** saw the model outperform the human on practice AAE. Restricting to people who saw that superiority still produces reduced selection in Studies 1, 3b, and 4 (**p < .001, .002, .022**), but **not significantly in 3a (p = .111)**. The article's broad “even among those” claim is therefore supported across several studies, not a significant result in every restricted subgroup.

### Confidence, choice, and beliefs are distinct

Seeing the model significantly reduced model confidence in all four exposure experiments (pooled-factor tests **p < .001, .029, < .001, < .001**). Seeing the human significantly reduced human confidence only in Study 4 (**p = .023**). Study 3a's row-wise Tukey comparisons show no significant pairwise condition differences in model confidence even though its pooled exposure contrast is significant; those are different tests.

Confidence in the model statistically mediated exposure's effect on selection in all four studies; human confidence did not. Nonetheless, behavior was not reducible to confidence ratings. Figure 4 shows model selection among people reporting **equal confidence** in both forecasters was **45% without** versus **25% with model-performance exposure**; these are pooled, post-treatment groups, not a randomized equal-confidence comparison.

The “humans have a better chance of being perfect” explanation was unsupported. Participants generally rated the model more likely to predict perfectly. In 3b, even among those believing the model more perfect, model selection fell **63% → 55%, χ²(1,N = 795) = 4.92, p = .027**. Control participants expected perfect ranks for **30.4/50 states by the model** and **16.7/50 by humans**; actual perfect-rank rates were only **6.0/50 and 2.2/50**. Both baselines were strikingly overoptimistic.

Exploratory attribute ratings favored models for consistency, appropriate weighting, and avoiding obvious mistakes, and favored humans for learning from mistakes and improving with practice. Educating people about these properties is a **proposed remedy**, not an intervention tested by this article.

## Analyst Takeaways

1. **Compare alternatives, not perfection.** A visible error can prompt rejection of an imperfect system that still beats the replacement; measure the replacement's errors and joint outcome.
2. **Separate first impressions from post-error reliance.** [Logg et al.](/dossiers/algorithm-appreciation.md) primarily examine advice before accuracy feedback and show stronger algorithm preference against a peer than against self. Neither paper cancels the other.
3. **Do not optimize reliance by hiding failures.** Reduced uptake after disclosure is an empirical finding, not an ethical or tested design justification for suppressing performance evidence.
4. **Measure actual selection alongside attitudes.** Equal reported confidence does not imply equal use; source-specific confidence and performance beliefs only partly account for the observed choice pattern.
5. **Software-agent transfer remains a hypothesis.** Choosing one forecaster for an incentive block differs from reviewing, editing, or rejecting individual proposed code changes; the study does not establish a review-interface remedy.

## Questions and Limitations

- Five studies provide internal replication, including a larger direct replication **3b** motivated by weaker earlier similar-study results (footnote 5). No external replication was assessed here; supplemental earlier studies were not independently read or reanalyzed.
- Only two short forecasting domains, low-stakes incentives, and binary whole-forecaster selection. Results do not establish the same response for adaptive models, repeated long-term feedback, mixed human–model answers, explanations, or user-adjustable outputs.
- Exposure changes access to actual performance information as well as making errors salient; it is not an isolated manipulation of one error's severity or a fully identified cognitive mechanism. Confidence is measured after selection, limiting causal mediation claims.
- **Reporting qualifications:** the restricted superiority subgroup in 3a is nonsignificant (**p = .111**) despite broad discussion wording. Table 3 uses fewer cases for some Stage-2 outcomes than retained choice samples (**205 vs 206; 406 vs 410; 1,029 vs 1,036**) without explaining these particular losses in the main text; do not substitute those denominators for the choice sample.
- Footnote 9 prints the self-confidence mediation interval as **[−.057, −.190]**, endpoints in reverse numerical order. The discussion's **13–97%** human-error range differs from the main results' **15–29% / 90–97%** summary; the concrete AAE values are safer than treating those ranges as identical.
- No tested strategy for reducing error-induced aversion is provided. Claims about humans' greater capacity to learn are participants' beliefs, not measured comparative learning performance.
- **Redistribution evidence**: the file states **“© 2014 American Psychological Association”** and repeatedly **“This article is intended solely for the personal use of the individual user and is not to be disseminated broadly.”** No public redistribution grant appears; keep the immutable copy private and use the DOI as source.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Supplies replicated reductions in selection after observing imperfect but superior forecasts and separates behavioral disuse from confidence, initial preference, and actual alternative performance.
