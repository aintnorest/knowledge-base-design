---
type: Study Note
title: Flat UI Elements Attract Less Attention and Cause Uncertainty
description: A 71-user desktop eye-tracking experiment finds weak-signifier pages take 22% longer and require 25% more fixations in targeted findability tasks, not necessarily in complete real-world workflows.
resource: https://www.nngroup.com/articles/flat-ui-less-attention-cause-uncertainty/
source: https://www.nngroup.com/articles/flat-ui-less-attention-cause-uncertainty/
tags: [interaction-design, attention, digital-interfaces, user-research, ux-metrics]
timestamp: 2026-10-11T23:50:37Z
---

# Flat UI Elements Attract Less Attention — Study Notes

**Authors**: Kate Moran; Nielsen Norman Group (NN/g).  
**Published**: September 3, 2017; saved-page metadata reports modification February 2, 2018.  
**Status**: First-party industry research report, not a peer-reviewed paper. Read the supplied saved article and its stimulus comparisons and heatmaps; the linked October 15, 2017 response to criticism provides additional caveats.  

## What It Is

A controlled eye-tracking comparison of **strong versus weak or absent clickability signifiers** on otherwise similar webpages. Its durable result concerns the cost of recognizing actions, not a universal contest between flat aesthetics and skeuomorphism. The headline overgeneralizes the manipulation; Moran acknowledges this in her [response to criticisms](https://www.nngroup.com/articles/response-criticisms-flat-design/).

## Problem and Motivation

Removing conventional action cues can leave users able to see an element without recognizing it as the solution to a task. More looking is not necessarily engagement: when the task is to locate an action, continued visual search can represent avoidable uncertainty. NN/g sought to isolate this recognition cost rather than evaluate the overall quality of the websites supplying its stimuli.

## Mechanism as an Idea

**71 general web users** completed desktop tasks on **nine pages from nine sites across six domains**: ecommerce, nonprofit, hotel, travel, technology, and finance. Each page had two modified versions, **18 designs total**, with nominally the same content, layout, and visual style but different signifiers on links, buttons, tabs, or sliders. Treatments included depth cues, ghost buttons, contrasting link colors, underlining, and links styled like static prose. This is a bundle of cue-strength manipulations, not removal of shadows alone.

For each task, participants located a specified interactive element, said **“I found it,” and stopped**; they did not execute a complete workflow. Everyone began with a practice task. Each person saw only one version of each page; version assignment and page order were randomized. The article calls this a between-subjects design: there was no within-person comparison of both versions of the same page.

Measures were **time to identify where to click** and **number of gaze fixations**. Heatmaps aggregated fixation location and duration. Processing effort and uncertainty are interpretations of these measures; confidence, emotion, wrong-click recovery, and commercial outcomes were not directly measured.

## Results / Admissions

- Weak-signifier versions produced **22% longer average task time** and **25% more fixations**. Both comparisons were significant by a **paired t-test using sites as the random factor, p < .05**. The pairing is across page variants, not repeated exposure of an individual to both variants.
- **Six of nine page pairs** had visibly different gaze distributions. Weak variants had more dispersed attention; none of the strong variants showed the reverse distribution pattern. These are reported heatmap comparisons, not separately reported statistical spatial-effect tests.
- The Priceline departure-time task shows stronger concentration around the left-side target area in the strong variant and broader coverage in the weak variant. Hertz's reservation-cancellation task similarly shows additional weak-variant fixations on footer links, promotions, and nearby controls. Describing footer search as desperation is NN/g's interpretation, not an independently measured emotion.
- The clearest misrecognition example is Brilliant Earth's pearl-jewelry task. In the weak variant, **9 of 24** participants stopped at the heading without looking at the actual link, believing the heading was actionable. **25 of 29 (86%)** strong-variant participants looked first at the heading and then the target link, versus **12 of 24 (50%)** weak-variant participants, **p < .005**. The heatmaps show the strong link pulling attention below the heading; the weak link does not.
- **Three of nine pairs** had nearly identical gaze patterns. One preserved contrasting purple inline links while removing blue underlining; the other two combined low information density, conventional placement, and salient, separated targets. These observations qualify the broad headline: weak depth cues need not imply weak action recognition.

NN/g recommends combining low density, expected placement, and strong target distinction when using flat styling. Its claim that all three should ideally be present is guidance distilled from examples, not a factorial experiment proving necessity. Likewise, a proposed contrast continuum and the statement that contrasting inline links will always be recognized go beyond the single nearly unchanged pair.

## Analyst Takeaways

1. **Strengthen recognition, not ornament for its own sake.** Color distinction, familiar treatment, placement, contrast, and separation can communicate action without a 3D surface. The result supports discriminable signifiers, not compulsory bevels.
2. **Distinguish looking at an element from recognizing its role.** The jewelry example shows attention landing near the right content yet stopping at the wrong action hypothesis. Findability includes classification, not just visibility.
3. **Do not translate a 22% microtask penalty into a 22% business penalty.** Reading and other workflow stages may dilute the relative difference; wrong clicks could add costs, but this experiment did not measure them.
4. **Use aggregate heatmaps with behavioral detail.** Heatmaps reveal dispersed search, but the participant-level heading-to-link sequence gives a stronger account of why the search went wrong.

## Questions and Limitations

- This public report gives no raw task-time or fixation means, standard deviations, confidence intervals, exact t statistics, degrees of freedom, or complete participant demographics and recruitment criteria. The jewelry example accounts for **53 people**, not all 71; the article does not explain that smaller analysis sample or give a complete exclusion account.
- Random assignment supports a causal cue-treatment comparison within the supplied stimuli, but cue dimensions are bundled. Effects cannot be assigned uniquely to flatness, contrast, underlining, or depth. The response explicitly says contrast differences were part of the intended manipulation.
- There was no navigation, actual clicking, longitudinal learning, mobile condition, or discoverability task. Strong claims about finding previously unknown features, emotional empowerment, and brand harm remain extrapolations.
- The [October 2017 response](https://www.nngroup.com/articles/response-criticisms-flat-design/) concedes the preferred headline would specify **weak signifiers used in flat design**, says flat design is not the enemy, and admits complete-task time or success may show no difference. It cites two years of triangulated NN/g research, not an independent replication, and refers to a **70-user** study while the original says **71**.
- That response also incorrectly equates **p < .05** with precisely 95% confidence that the researchers are right. A p-value is not the probability that the conclusion is true, nor does significance establish representativeness across the internet.
- The saved page states **“Copyright © 1998–2026 Nielsen Norman Group, All Rights Reserved.”** Its [reprint policy](https://www.nngroup.com/copyright-and-reprint-info/) expressly prohibits online article copying without a paid license; limited paper reprinting is not permission for a public digital archive. The source remains the canonical URL.

## Vault Ideas Extracted

- [Signifier Strength](/vault/signifier-strength.md) — Supplies controlled findability results and a concrete heading-versus-link misrecognition example, bounded to short desktop tasks.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Shows that conventional placement can help preserve recognition when decorative cues are reduced.
