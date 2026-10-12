---
type: Synthesis
title: Fitts's Law and Pointing Time
description: Pointing time depends on distance relative to target tolerance, while effective width normalizes the performed speed–accuracy tradeoff and fitted coefficients remain task-specific.
tags: [human-performance, interaction-design, ux-metrics]
timestamp: 2026-10-12T00:00:15Z
---

# Fitts's Law and Pointing Time

Fitts's law models the time needed to acquire a target as a relationship between movement distance and precision demand. Large, near targets are generally easier to acquire than small, distant ones. Its usefulness is not a universal speed constant: it is a way to compare defined pointing tasks while keeping their geometry, timing boundaries, and accuracy visible.

## The Distance–Precision Model

Let $A$ be movement amplitude, $W$ target width, and $MT$ movement time. A fitted model is:

$$MT = a + b\,ID$$

The intercept $a$ and slope $b$ must be estimated empirically. The Shannon formulation defines difficulty as:

$$ID = \log_2(A/W + 1)$$

Unlike the original $\log_2(2A/W)$ formulation, Shannon difficulty cannot become negative for nonnegative distance and positive width. The formulations differ most consequentially at low difficulty, roughly below **3 bits**. The information-theoretic framing is an analogy, not a direct measurement of information passing through nerves.

Width must represent the tolerance relevant to the approach. A wide, short rectangle approached vertically may be difficult despite its large horizontal extent. Smaller-dimension and approach-axis definitions have supporting experimental evidence, but are not universal solutions for every target shape or movement.

## Effective Width: Normalize Speed and Accuracy Together

Nominal width describes the tolerance offered; **effective width** describes how much tolerance participants actually used. For approximately normally distributed endpoints:

$$W_e = 4.133\,SD$$

This spans about **96%** of the endpoint distribution, corresponding to a nominal **4% miss rate**. Unusually precise movements produce $W_e < W$; greater endpoint dispersion increases effective width. A slower, more precise performance is thus credited with completing a harder effective task rather than being judged on speed alone.

The 4% normalization is a measurement convention, **not an acceptable interface error budget**. Adjustment from error percentages additionally assumes a centered normal distribution and is fragile in its tails; endpoint dispersion also exposes bias and outliers. An imputed error rate for a reported zero-error condition is not observed accuracy.

Performance indices also differ. The direct ratio $ID/MT$ includes the intercept's contribution to elapsed time; reciprocal slope $1/b$ does not. They are unequal when the intercept is nonzero. For predicting actual time, retain both $a$ and $b$, rather than treating a slope-only rate as total speed or silently equating it with a later standardized throughput procedure.

## Evidence

The cited review reanalyzes historical experiments rather than recruiting a new sample. Its one-ounce stylus data cross **4 distances × 4 widths**, with more than **600 observations per condition**, movement times of **180–731 ms**, and mean errors of **1.84%**; the original participant count is not supplied. Correlation improves from **.9831** with nominal width and original difficulty, to **.9904** with effective width, to **.9937** with effective width and Shannon difficulty. The last improvement is significant (**t = 2.20, df = 13, p < .05**). Reciprocal-slope performance falls **10.6 → 9.2 → 8.2 bits/s** while fit improves: a larger index is not a better model.

The heavier stylus shows the same direction of improvement. Disc and pin transfer show only tiny, nonsignificant formulation improvements, with higher tested difficulties and no available effective-width correction. The evidence is therefore not an equal improvement across all tasks.

A later two-dimensional experiment, summarized in the dossier, tested **12 computer-literate adults**, **78 conditions**, and **14,040 trials**. Smaller-dimension and approach-axis definitions yield correlations of **.9501** and **.9333**, compared with **.8097** for horizontal width (**p < .001** for both comparisons). This supports taking approach geometry seriously, not a universally validated rectangular-target rule.

Across six surveyed device studies, reported indices range **1.1–13.7 bits/s** and intercepts **−880 to +1030 ms**. The same device has published indices of **10.4** and **2.6 bits/s** under different tasks. None of those six studies uses effective width; missing condition-level errors prevent retrospective normalization. Their absolute rates are not interchangeable device constants.

## Practical Use

- Compare distance and relevant target tolerance when arranging actions; use [minimum target size](/vault/minimum-target-size.md) guidance separately for accessibility conformance.
- Fit the transaction actually being predicted. Search, homing, movement, selection, dwell, and correction can enter different timing boundaries.
- Preserve geometry, error policy, practice, tested difficulty range, and endpoint variability alongside a fitted equation.
- Prefer matched within-study comparisons over transporting rates from unrelated tasks. Keep intercept and slope when estimating elapsed time.

## Limitations

High correlation does not establish transportability or a complete causal theory. Drawing, tracking, and temporally constrained movement are not simply repeated pointing. Directional device–body effects can remain after geometry is accounted for. Effective-width normalization depends on endpoint assumptions; proposed two-dimensional dispersion extensions are not validated in the review itself. Negative fitted intercepts warn against extrapolation toward untested easy tasks, not negative observed times.

The six-study survey is not a harmonized meta-analysis; participant counts are absent for five studies. It establishes neither touchscreen target minima nor accessibility conformance, and reports no experiment establishing edge or corner advantages.

## Sources

- [Fitts' Law as a Research and Design Tool in Human-Computer Interaction](/dossiers/fitts-law-research-design-tool-hci.md) — Provides MacKenzie's 1992 formulations, effective-width reanalysis, heterogeneous device-study comparisons, and the dossier's supporting two-dimensional experiment with its limits.
