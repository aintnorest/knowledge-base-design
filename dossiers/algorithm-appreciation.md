---
type: Study Note
title: "Algorithm Appreciation: People Prefer Algorithmic to Human Judgment"
description: Experiments find greater uptake of identical numeric advice labeled algorithmic rather than human before performance feedback, with weaker appreciation against one's own judgment and among forecasting professionals rather than evidence of universally calibrated trust.
resource: https://doi.org/10.1016/j.obhdp.2018.12.005
source: https://doi.org/10.1016/j.obhdp.2018.12.005
tags: [delegation, decision-making, trust, human-performance, digital-interfaces]
timestamp: 2026-10-14T21:30:34Z
---

# Algorithm Appreciation — Study Notes

**Authors**: Jennifer M. Logg, Julia A. Minson, and Don A. Moore.  
**Published**: Organizational Behavior and Human Decision Processes **151 (2019), 90–103**; accepted December 4, 2018.  
**Status**: Peer-reviewed experimental article. Read the complete 14-page publisher-layout version of record, including figures, tables, photograph stimulus, appendices, and references. Preregistrations, materials, and data are linked at [OSF](https://osf.io/b4mk5/); they were not independently reanalyzed here.  

## What It Is

A study of **behavioral advice uptake before performance feedback**, distinguishing preference for algorithmic versus other people's advice from preference for one's own judgment. In the central experiments, identical numbers are described as human or algorithmic advice: differences therefore concern the attributed source, not differences in actual advice quality.

Algorithm appreciation means *relatively greater reliance on algorithmic advice*, not complete deference, justified trust in every algorithm, or a demonstrated ability to distinguish correct advice from errors. The paper includes experiments 1A–1D and 2–4, plus an additional normative-benchmark experiment in the discussion; the researcher-prediction experiment does not itself measure lay advice use.

## Problem and Motivation

A general claim that people reject algorithms obscures two comparisons: **algorithm versus another person**, and **algorithm versus oneself**. Prior feedback also matters. [Algorithm aversion](/dossiers/algorithm-aversion.md) shows reduced algorithm selection after people see imperfect performance, often despite better accuracy than the human alternative; this paper primarily tests reliance **without that prior accuracy feedback**. These are complementary boundary conditions, not contradictory universal preferences.

## Study Design and Measures

The Judge Advisor System elicits an initial judgment, presents advice, then allows revision. **Weight on Advice (WOA) = (final − initial judgment) / (advice − initial judgment)**: zero means no movement and one means matching the advice. The authors Winsorize values outside 0–1. WOA measures actual revision, not self-reported trust or the correctness of accepting a particular recommendation. Separate experiments measure binary advisor selection and confidence.

Most core advice is an average of earlier participants' judgments and can truthfully be described as both human-derived and algorithmically calculated. The algorithms are minimally described; opaque operation does not prevent uptake here, but the study does not manipulate explanation quality. Experiments 1B, 1C, 1D, 2, 3, and 4 have preregistered analyses/exclusions; 1A predates that practice. Repeat-IP exclusions are described for 1B onward, with further details deferred to supplements.

| Experiment | Participants and task | Design and outcome |
|---|---|---|
| 1A | **202**, median age 28; estimate a photographed man's weight | Identical **163 lb** advice, actual weight **164 lb**; human-average versus algorithm label; WOA and confidence; accuracy rewarded through a $10 raffle |
| 1B | **215**, median age 31, screened ages 18–40 | Ten Billboard song-rank forecasts with past-rank graphs; identical advice averaged from **275** prior participants; source randomized; exact final answers earn raffle entries |
| 1C | **286**, median age 37 | Predict a described person's attraction to, amusement with, and dinner enjoyment of a photographed potential date; three 1–100 judgments, advice from **48** earlier people; human/algorithm label randomized |
| 1D | **119 retained researchers** in methods, median age 32 | Society for Judgment and Decision Making list/personal recruitment; predict 1C's WOA for both advisors, six incentivized predictions; **Table 1 instead says 199** |
| 2 | **154** university-pool participants, median age 21 | Weight-estimation task; human-only, algorithm-only, or choice between both advisors; WOA plus advisor choice |
| 3 | **403**, median age 32 | Predict one state's airline-passenger rank; randomized algorithm-versus-self or algorithm-versus-other choice, **before making an estimate or seeing case data/performance**; accuracy-based bonus |
| 4 | **301 MTurk lay participants + 70 national-security professionals**, mean ages 39/46 | Weight estimate and Tesla-delivery, cyber-sanction, and Brexit forecasts; identical human/algorithm advice; four-task WOA and forecast Brier scores |

Experiment 4's four-task WOA analysis retains **282 lay people and 61 experts**, adjusts for algorithm familiarity, and treats tasks as repeated measures. Professionals were predominantly men (**67/70**, compared with **147/301** lay participants), recruited via national-security mailing lists, and received an iPad raffle versus the lay sample's $10 raffle. Expertise is a **sample comparison**, not a randomized causal treatment.

## Results / Admissions

### Source labels change uptake

- **1A:** algorithm/human WOA **.45/.30**, SD **.37/.35**; **F(1,200) = 8.86, p = .003, d = .42**. Confidence increased more with the algorithm label: **71.30 → 79.91** versus **70.62 → 75.10**, source × time **p = .019**. Because the advice is nearly exact, moving toward it improves accuracy in this task.
- **1B:** algorithm/human mean WOA **.37/.21**; participant-clustered repeated-forecast regression **β = −.34, t(214) = 5.39, p < .001**, with source coded −1 algorithm/+1 human. The averaged participant analysis also gives **t(213) = 5.54, p < .001**. The printed dispersion label is questionable; see limitations.
- **1C:** three-judgment WOA index **α = .77**; algorithm/human **.38/.26**, SD **.28/.27**; **t(284) = 3.50, p = .001, d = .44**. No detected source × target-person interaction (**p = .818**). Forecasting another person's attraction is not the same as selecting one's own preferred partner.
- **1D:** researchers predicted *human minus algorithm* WOA **+.14, SD .20**, whereas participants showed approximately **−.11**. The source reports **t(118) = 14.03, d = 1.25** for the discrepancy and **t(118) = 7.92, d = .80** for predicted aversion versus zero, both **p < .001**. These tests and demographic counts support **119**, not Table 1's 199.
- **2:** separate-presentation WOA **.50 algorithm/.35 human**, **t(100) = 2.10, p = .038, d = .44**. In joint presentation **39/52 (75%)** chose the algorithm rather than another participant (**13/52**); direct comparison did not reverse the preference. Subsequent WOA by *chosen* advisor did not significantly differ (**.52/.41, p = .371**), a selected rather than randomized contrast.

### The self and professional experience qualify appreciation

In **3**, **88%** chose the algorithm against another participant (**N = 206**), versus **66%** against themselves (**N = 197**); the source reports **z = 6.62, p < .001**. Both proportions exceed 50%; introducing the self attenuates appreciation rather than demonstrating an overall preference for self. Confidence in the human alternative was higher when it was oneself (**2.86**) than another participant (**2.53**); algorithm confidence did not significantly differ between these conditions (**3.72/3.80, p = .286**).

In **4**, the adjusted WOA analysis showed an advisor effect (**F(1,338) = 9.46, p = .002, d = .29**), less advice-taking by experts (**F = 32.39, p < .001, d = .60**), and advisor × expertise interaction (**F = 5.05, p = .025, d = .23**). Lay people weighted algorithmic advice more; professionals discounted both sources heavily. The figures show this varies by task, not a uniform reversal to human preference.

Forecast accuracy used **two-outcome Brier error, range 0–2**, lower better. Advice was good for Tesla (20% probability; event did not occur; Brier **.08**), bad for cyber sanctions (12%; event occurred; **1.55**), and uncertain for Brexit (54%; event occurred; **.42**). The accuracy analysis found **no overall advisor effect (p = .764)**, but sample expertise **p = .002** and interaction **p = .042**; lay participants were more accurate than professionals under algorithm-labeled advice. The authors attribute this to expert discounting, but the sample contrast cannot isolate expertise from its other differences.

### Relative appreciation can coexist with underuse

An additional **N = 671** visual age-estimation experiment explicitly contrasts an algorithm aggregating **314** estimates with one randomly selected human estimate; actual advice quality is allowed to differ. The discussion reports WOA **.34 algorithm/.24 human, d = .33**, but later gives human WOA **.26** and algorithm **.66** while discussing underweighting against .50 and 1.00 benchmarks. The latter algorithm number conflicts with the earlier uptake and Figure 1; it must not be silently adopted as an independently verified mean. The conceptual distinction remains useful: *more uptake than a human comparator* need not mean *enough uptake for the advice's actual value*.

## Analyst Takeaways

1. **Name the comparator and feedback history.** Algorithm-versus-peer choice without accuracy feedback is not algorithm-versus-self choice after observing errors.
2. **Treat source attribution as behaviorally consequential, not as proof of capability.** Identical advice produces different revisions under different labels; making a recommendation look algorithmic can persuade without increasing its correctness.
3. **Measure calibration rather than maximum uptake.** WOA, confidence, advisor selection, and outcome accuracy answer different questions; this paper does not establish selective rejection of wrong advice.
4. **Do not assume experts are universally superior supervisors.** Professionals discounted useful advice here, but a nonrandom, demographically different national-security sample cannot establish a universal effect of expertise.
5. **Software-agent implications are extrapolations.** The results motivate testing how users interpret an automated recommendation's origin and compare it with their own answer, not assuming the same effects for code changes or generative agents.

## Questions and Limitations

- Short numerical estimation/forecasting tasks with specific source descriptions; no longitudinal deployment, professional coding task, high-stakes outcome, or independent replication is established by this source. Repetition across tasks within one paper is internal robustness, not independent replication.
- **Verified sample discrepancy:** Table 1 prints **N = 199 for 1D**, while methods state **120 completed, one excluded, 119 retained**; sex counts **55 + 64 = 119** and **t(118)** agree with 119. Use the methods' sample and preserve the table discrepancy.
- **Additional reporting inconsistencies:** the normative-benchmark discussion prints **.34/.24** then **.66/.26** for algorithm/human WOA; Figure 1 supports approximately .34/.24. In 1B, dispersion is printed **SD = .02** for both means, whereas footnote 3 describes standard errors for the plotted participant means; do not reinterpret it as a verified SD. Figure 1's caption says Experiment 2's “joint” conditions, although the .50/.35 result is described in text as the separate conditions.
- “High-quality advice” is not true for every realized forecast: the cyber advice is substantially wrong. There is no overall advisor-label accuracy benefit in Experiment 4.
- Normative 50%/100% weighting benchmarks depend on assumptions about relative information, judgment quality, and error relationships; they are not universal reliance rules.
- **Redistribution evidence**: page 90 states **“© 2018 Elsevier Inc. All rights reserved.”** No explicit redistribution grant appears in the supplied PDF; archive the immutable copy privately and cite the DOI.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Adds identical-advice source-label effects before performance feedback and distinguishes relative appreciation from sufficient or calibrated reliance, qualified by self-comparison and professional-sample differences.
- [Choice Architecture Effects](/vault/choice-architecture-effects.md) — Supplies the source-label evidence: identical advice gained weight when attributed to an algorithm rather than a person, a presentation effect distinct from defaults, order, or option count.
