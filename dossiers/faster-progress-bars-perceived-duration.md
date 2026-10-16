---
type: Study Note
title: "Faster Progress Bars: Manipulating Perceived Duration with Visual Augmentations"
description: Four small experiments show visual texture and pulsation can change attended progress-bar duration judgments, with backward-decelerating ribbing matching longer actual durations to plain bars, not speeding work or establishing background-task benefits.
resource: https://doi.org/10.1145/1753326.1753556
source: https://doi.org/10.1145/1753326.1753556
tags: [visual-perception, motion, interaction-design, ux-metrics, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Faster Progress Bars — Study Notes

**Authors**: Chris Harrison, Zhiquan Yeo, and Scott E. Hudson.  
**Published**: CHI 2010, April 10–15, Atlanta, pp. 1545–1548.  
**Status**: Peer-reviewed conference note; read the complete four-page supplied conference-formatted paper, including stimulus examples, comparison graphs, and duration-adjustment plots.

## What It Is

Four experiments on **perceived duration**, not actual computation speed. They vary a progress bar's pulsating fill or moving internal texture while the completion boundary advances. They then measure how much longer an augmented bar can run before it feels equivalent to a plain bar.

## Mechanism as an Idea

The authors propose two mechanisms: rhythmic visual variation can affect timing judgments, and motion of the internal texture opposite the filling direction can induce greater apparent forward speed through relative-motion perception. These are literature-based explanations, not independently isolated causal mechanisms in these experiments. The bar's represented completion and the texture's motion are distinct channels.

Participants watched two bars **sequentially to completion**, then judged first faster, second faster, or equal duration; replay was available. Sequential presentation deliberately concealed equal actual durations. “Preference” in the results means **judged faster**, not liking, trust, comfort, or task satisfaction.

## Studies and Results

### 1. Pulsating bars

**20 participants**, **7 female**, mean age **23**, compared five constant, increasing, or decreasing pulsation behaviors. Each bar lasted **5 seconds**. All **25 ordered pairings** included identical behaviors and both presentation orders, with randomized trial order.

The preference score was the mean of **+1 / −1 / 0** for one behavior faster, the other faster, or equal; two-sided sign tests assessed differences. Increasing-frequency behaviors were judged faster than constant (**p < .05**) or decreasing ones (**p < .001**) when grouped. The fast-increasing behavior's overall mean preference score was **0.21**. For one comparison, **16 of 40 judgments** favored fast increasing, **6** slow decreasing, and **18** equal: score **0.25**. These are repeated judgments from 20 people, not 40 independent participants.

### 2. Ribbed bars

The **same 20 participants** compared seven internal-texture behaviors: still, forward, or backward motion with constant, accelerating, or decelerating movement. The same interface and **49 ordered pairings** were used; this continued the short-duration comparison paradigm of Study 1.

Backward-moving texture was judged faster than still and forward texture (**p < .001** each, grouped by direction). Grouped deceleration beat still and constant-velocity texture (**p < .05** each). Backward-decelerating texture had overall preference score **0.34**, compared with **0.29** for backward-accelerating texture. Their direct comparison slightly favored acceleration (**0.10**) but was **not significant**: “best overall” is not a demonstrated direct victory over every alternative. Figure 5 includes marginal **p < .1** edges as well as significant ones; they must not all be treated as established differences.

### 3. Augmentations versus a plain bar

A new **10-person** sample, **5 female**, mean age **19**, compared plain, fast-increasing pulsation, and backward-decelerating ribbing at **5 and 15 seconds**. Each duration used **18 trials**—nine ordered pairs repeated twice—giving **36 comparisons per person**, randomized and combined across presentation orders.

At **5 seconds**, no contrast met **p < .05**; pulsation versus plain only approached significance (**p < .1**). At **15 seconds**, both augmentations were judged faster than plain (**p < .05**). Between augmentations, pooled counts were **30 judgments favoring pulsation, 33 ribbing, and 17 equal**: little evidence that ribbing was decisively superior. These pooled judgments are not distinct participants.

### 4. Magnitude by duration matching

A new **16-person** sample, **6 female**, mean age **22**, compared backward-decelerating ribbing with a plain control fixed at **5 or 15 seconds**. The ribbed bar's duration adjusted according to each faster/slower judgment until the pair felt equal. Both presentation orders were tested, with **eight adjustment rounds**, repeated twice per condition: **64 trials per person**. Adjustment steps became smaller; the first round forced a faster/slower choice.

- A plain **5-second** bar matched a ribbed bar averaging **5.61 seconds, SE 0.14**: **0.61 seconds / 12.2% longer actual duration**.
- A plain **15-second** bar matched a ribbed bar averaging **16.75 seconds, SE 0.45**: **1.75 seconds / 11.7% longer actual duration**.
- The paper reports **p < .001** for both, without naming the test in this results section or giving standardized effects or confidence intervals.

The abstract summarizes this as an **11% perceived-duration reduction**. Longer-duration matching is not itself a direct rating of an 11% reduction at equal actual time. Approximately **10.9%** and **10.4%** reductions follow if one normalizes each matching gap by the augmented duration; that is an analyst conversion, not a separately measured outcome.

Figure 6 shows the 15-second adjustment still rising at round eight. The authors suggest further rounds might yield a larger effect; equilibrium and linear scaling to long waits remain unconfirmed. Pilots with longer waits lost participants' attention substantially.

## What the Source Recommends versus Shows

The authors advocate visually augmented bars as an inexpensive way to improve perceived performance. They show changes in **attended, short, completing-bar comparisons and duration matching**. They do not show reduced task time, improved comprehension, reduced anxiety, greater trust, beneficial cancellation decisions, or a better overall user experience. No ethics or motion-accessibility evaluation is reported.

## Analyst Takeaways

1. Separate real speed, judged duration, and preference for the experience. The paper's “preference” score measures only the second.
2. Truthful completion fraction and honest operational state remain necessary even when styling changes the felt wait. Do not substitute decorative motion for measured progress.
3. Treat the perceptual benefit as conditional, not a universal optimization: Study 3's five-second plain-bar comparison was not significant despite Study 4's matching result.
4. Attending to a finishing bar differs from glancing at background work. This evidence does not establish benefits for long-running operations or multiple concurrent tasks.
5. An ethically acceptable reduction in discomfort must not conceal delay, failure, uncertainty, or the opportunity to stop. This is an analyst boundary, not a tested conclusion of the paper.

## Questions and Limitations

- Small convenience samples, with recruitment details and disability status unstated. Studies 1 and 2 reuse participants; they are not independent replications. Later samples provide within-paper corroboration, not an established independent replication verdict.
- Repeated comparisons, replay, completion, and directed attention differ from real work. Numerous sign-test comparisons are reported without a stated multiple-comparison correction or participant-level dependence model.
- Best-behavior selection used weak head-to-head evidence. Study 4 estimates magnitude only for selected ribbing versus plain, not every visual treatment or a direct controlled comparison against the operating system's actual bar.
- **Source inconsistency**: the conclusion says the selected augmentation had equal duration to a bar “11% longer in actual time,” reversing the matching relation described in the results. It was the **augmented bar that ran longer** while feeling equal to the shorter plain control. Use the explicit **5 versus 5.61** and **15 versus 16.75** results rather than that sentence. The abstract's “11%” is a rounded interpretation, not the reported 12.2%/11.7% increases in actual matched duration.
- No evidence for long unattended work, indefinite activity cues, stalled or failing processes, motion-sensitive people, or sustained exposure. Induced motion and timing mechanisms remain interpretations.
- **Redistribution**: the first page's ACM notice permits personal/classroom copies under conditions but requires permission for republication or posting on servers. The supplied file is retained privately.

## Vault Ideas Extracted

- [Progress and Wait Feedback](/vault/progress-and-wait-feedback.md) — Supplies perceived-duration evidence, its attended short-wait boundary, and the distinction between comfort and misleading status.
- [Response-Time Thresholds](/vault/response-time-thresholds.md) — Adds visual-treatment effects at tested durations without turning them into universal timing thresholds.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Distinguishes communicating real progress from making unchanged processing appear faster.
