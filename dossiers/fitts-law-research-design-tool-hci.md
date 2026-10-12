---
type: Study Note
title: Fitts' Law as a Research and Design Tool in Human-Computer Interaction
description: MacKenzie strengthens pointing-time modeling with the Shannon formulation and effective target width, while showing that heterogeneous tasks and error policies prevent published device throughputs from serving as universal design constants.
resource: https://doi.org/10.1207/s15327051hci0701_3
source: https://doi.org/10.1207/s15327051hci0701_3
tags: [human-performance, interaction-design, ux-metrics, digital-interfaces, survey]
timestamp: 2026-10-11T23:52:54Z
---

# Fitts' Law as a Research and Design Tool — Study Notes

**Authors**: I. Scott MacKenzie.  
**Published**: 1992; Human–Computer Interaction 7(1), pp. 91–139; DOI 10.1207/s15327051hci0701_3.  
**Status**: Peer-reviewed theoretical review, reanalysis, and survey of six device studies, not a new participant experiment. Read the supplied 50-page scan of the published article, including its figures and EBSCO end page, with the author's [HTML transcription](https://www.yorku.ca/mack/hci1992.html) as a reading aid. The PDF carries “Copyright © 1992, Lawrence Erlbaum Associates, Inc.” and “Copyright © 2002 EBSCO Publishing”; neither is a redistribution grant.  

## What It Is

A corrective to the easy version of Fitts's law: **large, near targets are faster to acquire**, but a high correlation in one experiment does not license a universal pointing-time equation for a device. MacKenzie explains the information-theoretic analogy, improves its treatment of low-difficulty movements and endpoint variability, and then shows how published HCI studies undermine their own comparability.

Its durable contribution is methodological as much as geometric: **speed and accuracy describe one tradeoff**, not two independent device virtues. A performance index without its task, selection criterion, difficulty range, and error policy is a misleading summary.

## Problem and Motivation

Direct manipulation makes rapid, precise movement part of ordinary interface use. A model can help predict alternatives before building them, rather than merely rank finished devices. But the same mouse yields published performance indices of **10.4 and 2.6 bits/s**—a **fourfold difference**—and intercepts differing by **922 ms**. These cannot reasonably be treated as two measurements of one transferable mouse constant.

The paper asks both what the model means and what must remain stable for a fitted equation to travel. Its conclusion is deliberately less triumphal than its title: embedding an equation lifted from a research article in a design tool may be premature.

## Mechanism as an Idea

### Difficulty is a distance–precision relationship

Let $A$ be movement amplitude, $W$ target width, and $MT$ movement time. The fitted model is $MT=a+b\,ID$, with an empirically estimated intercept and slope.

- **Original Fitts formulation**: $ID=\log_2(2A/W)$. Doubling distance or halving width adds **1 bit**, and therefore adds $b$ to predicted movement time. The factor 2 shifts difficulty by one bit without changing the fitted slope or correlation.
- **Welford formulation**: $ID=\log_2(A/W+0.5)$. Common in the surveyed studies, but it still admits negative difficulty and approaches −1 bit as amplitude approaches zero.
- **Shannon formulation**: $ID=\log_2(A/W+1)$. This more directly follows Shannon's channel-capacity expression, never produces negative difficulty for nonnegative amplitude and positive width, and differs most consequentially at low difficulty, roughly **below 3 bits**.

The metaphor treats amplitude as signal and endpoint variability as noise. It is not a direct measurement of literal information packets traversing nerves. MacKenzie explicitly calls the law an **analogy waiting for a theory**: the iterative-corrections account assumes constant-duration corrections and cannot adequately explain observed submovement counts, variable initial movements, or misses. Competing linear speed–accuracy and stochastic optimized-submovement models matter particularly for temporally constrained movements; drawing or tracking is not simply pointing repeated many times.

A positive intercept may include homing, selection, or other additive activity. These explanations are plausible, not settled causal decompositions: selection can alter the slope as well, and the surveyed evidence is inconclusive. A negative fitted intercept does not mean negative observed time; it warns against extending the fit toward untested low difficulties where negative predictions may result.

### Effective width represents the performed task

Nominal width says what the experiment requested; **effective width says how participants actually used the available tolerance**. For approximately normally distributed endpoints, $W_e=4.133\,SD$. This spans about **96%** of the distribution, corresponding to a nominal **4% miss rate**. When participants are unusually accurate, $W_e<W$; when less accurate, the effective width increases. A slower but more precise performance is therefore credited with completing a harder effective task rather than simply labeled slower.

The alternative adjustment from observed error percentage assumes a centered normal distribution and becomes fragile in its tails. MacKenzie prefers endpoint dispersion because it also reveals undershooting, overshooting, and outliers. His workaround for a reported **0.00%** error condition assumes **0.0049%** errors: a pragmatic imputation, not observed accuracy. The 4% normalization is a modeling convention, **not a recommendation that interfaces should allow 4% errors**.

An effective amplitude, $A_e$, could similarly represent actual distance, especially when people undershoot. The paper cannot test it with Fitts's summary data and warns that calibration on biased endpoints could mispredict later errors.

### Performance indices are not interchangeable definitions

Fitts's direct index is $IP=ID/MT$ in bits/s, averaged over conditions. Many studies instead use **$IP=1/b$**, the reciprocal regression slope. These differ whenever the intercept is nonzero: the slope-only index excludes the intercept's cost, while the direct ratio includes it. “Throughput” is a useful modern name for this rate family, but the paper's **index of performance** should not be silently equated with a later standardized throughput procedure.

For predicting actual time, retain **both $a$ and $b$**. Ranking reciprocal slopes is not necessarily ranking total movement times. In its learning discussion, the paper favors the direct ratio as a way of incorporating changes to both speed and accuracy and avoiding separate intercept-related learning effects.

### Two dimensions expose the meaning of width

Figures 8 and 9 show why a wide, short word approached vertically is not an easy target merely because its horizontal extent is large. Width and height reverse roles as approach changes from **0° to 90°**. The paper proposes either the **smaller of width and height** or the target's span along the approach vector, $W'$. These are proposals in this article, not universally validated substitutions; a footnote points to the then-in-press MacKenzie–Buxton experiment. Its suggested two-dimensional endpoint-dispersion extension also awaits testing here.

Direction can matter independently of target geometry: Card's mouse had no reported angle effect, but its joystick was **3% slower diagonally**; Jagacinski–Monk reported **7.2%** and **9.1%** diagonal penalties for joystick and helmet sight. Geometry alone therefore does not exhaust device–body effects.

## Results / Admissions

### Reanalysis, not fresh participant evidence

Fitts's 1954 experiments comprised reciprocal tapping with **1-oz and 1-lb styli**, disc transfer, and pin transfer. The 1-oz data crossed **4 amplitudes × 4 widths**, spanning **1–7 bits**, with more than **600 observations per condition**; mean times ranged **180–731 ms**, mean errors **1.84%**, and the direct mean index was **10.10 bits/s (SD 1.33)**. This review does not provide a participant count for that original sample.

For the 1-oz tapping data, correlation rises from **r=.9831** using nominal width and original difficulty, to **.9904** with effective width, to **.9937** with effective width and Shannon difficulty; all **p<.001**. The final two correlations differ at **t=2.20, df=13, p<.05**. Reciprocal-slope IP falls **10.6→9.2→8.2 bits/s** even as fit improves; the slope's standard error falls **4.7→4.0→3.6 ms/bit**. A bigger performance index is plainly not synonymous with a better model.

The 1-lb stylus shows the same correlation trend, **.9796→.9882→.9925**, and IP **9.5→8.1→7.2 bits/s**. Disc and pin transfers show only tiny, **nonsignificant** correlation improvements with Shannon difficulty; their tested difficulties were higher and errors could not occur, so effective-width correction was unavailable. The strongest formulation evidence is therefore localized to a reanalysis where low difficulty matters, not a universal improvement of equal size.

### Six surveyed studies

The following indices are predominantly **reciprocal fitted slopes**, not a harmonized meta-analysis. The review supplies detailed tasks but not participant counts for five studies; it identifies **12 novice participants** in Epps's analysis. Missing sample detail should not be replaced with guessed counts.

| Study | Task and comparison | Reported IP and evidence boundary |
|---|---|---|
| Card, English, and Burr (1978) | Select highlighted words in CRT text with mouse, rate-controlled isometric joystick, step keys, or text keys; includes homing and selection, varied distance, word length, and approach angle. | Mouse **10.4**, joystick **4.5 bits/s**; **r=.91/.94**, standard errors **70/130 ms**. Mean times **1660/1830/2510/2260 ms** for mouse/joystick/step/text keys; mouse errors **5%**, step keys **13%**. Only continuous devices receive these Fitts fits. |
| Drury (1975) | Preferred-foot reciprocal tapping, **30 taps** per block, six distances and two pedal widths; shoe width added because any shoe contact counted. | **11.8 bits/s, r=.970, p<.01**; **187 ms** intercept. Nominal difficulty **0.53–2.47 bits**; blocks with more than one miss repeated, enforcing at most one miss per 30 taps. Not a screen-pointing task. |
| Epps (1986) | Random-position target capture with mouse, trackball, two touchpads, and two velocity-controlled joysticks; misses require correction and reselection. | Trackball **2.9**, mouse **2.6**, absolute touchpad **2.3**, relative touchpad **1.6**, force joystick **1.2**, displacement joystick **1.1 bits/s**; **r=.70–.93**. Correction-inclusive completion is not equivalent to error-free first-attempt selection. |
| Jagacinski and Monk (1985) | Circular-target capture with position-control joystick and helmet-mounted sight, eight directions, **344-ms dwell** selection. | Both **5.0 bits/s, r=.99**; intercepts **−303/−268 ms**. Dwell criterion prevents final capture errors; participants practiced up to **29 days**. |
| Kantowitz and Elvers (1988) | Isometric joystick position versus velocity control, high/low gain, four distance–size conditions; reversal terminates a trial. | Position **3.4**, velocity **2.2 bits/s**; **r=.62–.85**, errors around **25%**, intercepts **−328 to −880 ms**. No main gain effect; only **3.5–5.5 bits** tested. |
| Ware and Mikaelian (1987) | Eye-controlled selection among seven vertically arranged rectangles; hardware button, on-screen button, or **400-ms dwell**. Width constant, four distances including zero. | **13.7/10.3/9.3 bits/s** respectively, with **8.5%/22%/12%** errors. MacKenzie **infers equations from plots**; original correlations and coefficients were not supplied. Welford difficulty **−1.0 to 1.8 bits** makes the analogy especially weak. |

Across the survey, IP spans **1.1–13.7 bits/s** and intercepts **−880 to +1030 ms**. The more defensible mouse-versus-velocity-joystick comparison is within-study: the mouse's IP advantage is about **2.3×** in Card and **2.2×** in Epps. Agreement in the direction and ratio of a comparison survives where absolute constants do not.

### Why the studies disagree

- **Task definition**: serial versus discrete movement can change the index by roughly **2–3 bits/s**; search, homing, and time on target are not equally included.
- **Selection**: button press, dwell, one-handed versus two-handed operation, and correction-to-success change the measured transaction.
- **Difficulty range and formulation**: narrow or exclusively hard conditions destabilize extrapolated intercepts; zero-distance and wide-target conditions expose negative or undefined difficulty in older formulas.
- **Geometry and direction**: horizontal word width can misstate vertical precision demands; limb and controller properties can add directional effects.
- **Errors**: exclude misses, repeat blocks, stop at reversal, or allow unlimited correction—these sample different parts of the speed–accuracy function. **None of the six studies used effective width**, and missing condition-level error data prevent retrospective normalization.
- **Learning and aggregation**: some studies attempt asymptotic performance, others do not; aggregating participant means versus retaining individual variability changes correlations. A high correlation alone is not a fair cross-study quality score.

## Analyst Takeaways

1. **Use size and distance as a design lens, not a complete task model.** The source directly supports making relevant precision demands and travel visible in design reasoning. Applying that to frequently used controls—larger hit regions or shorter travel—is an analyst implication; this article does not establish a minimum pixel size or an optimal layout for every workflow.
2. **Fit the transaction you intend to predict.** The author's recommendations are broad representative difficulty ranges, appropriate geometry, explicit error normalization, adequate practice, and a clear device–task association. An analyst extension is to keep search, movement, selection, and recovery distinct when evaluating a real interface.
3. **Do not advertise slope-only throughput as total speed.** A high-IP device can carry a large additive delay or high miss rate. Preserve intercept, accuracy, selection criterion, and calibration range alongside the index.
4. **Treat rectangular geometry as unresolved unless supported by the relevant experiment.** A [later same-year study by MacKenzie and Buxton](https://doi.org/10.1145/142750.142794), read through its [author transcription](https://www.yorku.ca/mack/CHI92.html), tested **12 computer-literate adults**, **78 conditions**, and **14,040 trials**. Smaller-dimension and approach-axis definitions improved correlations to **.9501/.9333**, versus **.8097** for horizontal width (**p<.001** for both comparisons with the status quo). This is supporting extension evidence, not an independent replication of every claim in the survey or a universal rectangular-target rule.

## Questions and Limitations

- Six selected studies are a methodological survey, not a systematic review with pooled effects or comparable confidence intervals. The paper's wider literature supports robustness across limbs, ages, and settings while also documenting low-difficulty departures and disagreement about amplitude versus width effects.
- Effective-width adjustment depends on endpoint-distribution assumptions. The paper's error-percentage imputation for perfect performance and speculative two-dimensional dispersion should not become unqualified modern measurement instructions.
- Several actual inconsistencies deserve preservation rather than silent harmonization: the prose gives the Kantowitz velocity intercept average as **+863 ms**, although its table gives **−846/−880 ms**; Epps is described as four amplitudes and five widths, but later as five amplitudes and four widths, with **nine** conditions tabulated despite a described **20-cell** crossing. Card's maximum difficulty example names a **10-cm** amplitude although listed levels reach **16 cm**. These do not erase the main comparison but make secondary procedural reconstruction unsafe.
- No experiment here establishes edge/corner benefits, touchscreen target minima, or accessibility conformance. Those require other evidence; a geometric intuition about unconstrained travel is not a reported result from this source.
- Published hardware and controller settings are historical. The paper's warning against transporting constants is more durable than its device leaderboard.

## Vault Ideas Extracted

- [Fitts's Law and Pointing Time](/vault/fitts-law-pointing-time.md) — Distance–precision modeling, Shannon difficulty, two-dimensional geometry, effective-width speed–accuracy normalization, and the limits of transporting fitted equations.
- [Minimum Target Size](/vault/minimum-target-size.md) — Explains why narrow targets increase precision demand, without supplying a minimum size or an accessibility standard.
