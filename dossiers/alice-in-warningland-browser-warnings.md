---
type: Study Note
title: "Alice in Warningland: A Large-Scale Field Study of Browser Security Warning Effectiveness"
description: Browser telemetry finds large differences in security-warning bypass rates and faster responses to common certificate errors, but cannot isolate design effects, comprehension, or individual habituation.
resource: https://www.usenix.org/conference/usenixsecurity13/technical-sessions/presentation/akhawe
source: https://www.usenix.org/conference/usenixsecurity13/technical-sessions/presentation/akhawe
tags: [attention, decision-making, interaction-design, ux-metrics, trust, digital-interfaces]
timestamp: 2026-10-14T21:31:07Z
---

# Alice in Warningland — Study Notes

**Authors**: Devdatta Akhawe and Adrienne Porter Felt.  
**Published**: 22nd USENIX Security Symposium, August 14–16, 2013, Washington, DC; proceedings pp. 257–272.  
**Status**: Peer-reviewed observational field study of browser telemetry. Read the complete 17-page proceedings PDF (cover plus 16 article pages), including warning screenshots, timing distributions, all ten tables, appendix, and references. No article DOI is printed; the proceedings ISBN identifies the collection, not this article, so the source key uses the canonical USENIX article URL.

## What It Is

A large-scale challenge to the claim that users invariably ignore security warnings. Five of six browser/warning combinations had bypass rates below one-third, while Chrome's SSL warning was bypassed **70.2%** of the time. The reusable result is that warning behavior varies strongly with the warning and its surrounding system—not that a particular visual treatment causally produces the observed browser difference.

## Problem and Motivation

Earlier laboratory studies often evaluated obsolete passive indicators or placed people in artificial, apparently safe task contexts. This study records decisions during ordinary browsing. It separates malware/phishing warnings, where the authors regard false positives as negligible, from SSL certificate warnings, where misconfiguration can create benign alarms. Bypass is therefore not automatically evidence of inattention or an incorrect decision.

## Study Design

### Population, exposure, and measures

Users participated in unpaid browser usage-metrics programs, generally by opting in; some developer channels enabled collection by default. Firefox telemetry represented approximately **1% of its users**. Chrome recorded malware, phishing, and SSL exposures on **2,148,026; 204,462; and 4,491,767 browser installations**, respectively; these are overlapping client populations, not unique people across the study. Firefox did not permit individual-client tracking.

Chrome data covered **April 28–May 31, 2013**. Firefox malware/phishing and exception-dialog data covered **May 1–31**; its corrected SSL data covered **June 1–July 5**, as a measurement fix reached prerelease channels. Natural browsing supplied the tasks and destinations; neither warning appearance nor browser choice was randomized.

The article reports **25,405,944 warning impressions**: Chrome malware **6,040,082**, phishing **386,350**, SSL **16,704,666**; Firefox malware **2,163,866**, phishing **100,004**, and beta SSL **10,976**. The appendix also includes developer/nightly Firefox SSL impressions; see the reconciliation limits below.

Measures were completed bypass versus leaving, use of supplementary information, exception confirmation, and changing the permanent-exception default. Chrome SSL decision time was measured while warnings were foregrounded, in logarithmically spaced discrete buckets. Figures 6–7 plot distributions cut at 90% because of long tails; they do not show continuous individual reading times. Analyses aggregate impressions, not independent participants. The authors removed a small number of overrepresented Chrome clients and used a conservative significance criterion **α = .001** for their main comparisons.

### What the screenshots establish

Figures 1–5 show full-page interruption, differently emphasized escape and bypass choices, and varying placement of error detail. Chrome exposed certificate-specific explanation in the primary SSL warning; Firefox placed it in secondary details and an exception dialog. Firefox could remember a permanent exception, while Chrome showed the warning again. These differences alter the meaning and denominator of future warning exposure, not only the current screen's appearance.

## Results / Admissions

### Bypass rates vary by warning and browser

| Warning | Firefox | Chrome | Comparison boundary |
|---|---|---|---|
| Malware | **7.2%** | **23.2%** | Stable/release channels |
| Phishing | **9.1%** | **18.0%** | Stable/release channels |
| SSL | **33.0%** | **70.2%** | Firefox beta versus Chrome stable |

The SSL difference is **37.2 percentage points**, or about **2.1 times** the Firefox rate. These are observed associations, not treatment effects. Firefox SSL iframe warnings had a much lower aggregate bypass rate (**4.3%**); restricting to top-level warnings raised it **28.7 points** to 33.0% and limited the comparable data to prerelease users. Malware/phishing iframe adjustments were within two points in beta data.

Chrome interrupted pages containing unsafe third-party resources, whereas Firefox silently blocked those resources. Chrome malware bypass varied **11.2–24.9%** across weeks; Firefox stayed within one point of its monthly average. The authors propose trusted host pages containing unsafe advertisements as an explanation, but do not observe the destinations needed to test it.

### Frequency, speed, and attention are related but not interchangeable

Chrome SSL error shares and bypass rates were **untrusted issuer 56.0% / 81.8%**, **name mismatch 25.0% / 62.8%**, and **expired certificate 17.6% / 57.4%**. The first and last differ by **24.4 points**. Roughly half of the timing distribution occurred by **1.7 seconds** for issuer errors, **2.2 seconds** for name errors, and **2.7 seconds** for expiry errors. The most common error was bypassed fastest and most often, consistent with warning fatigue but not a longitudinal within-person demonstration of habituation.

Among Chrome SSL bypass outcomes, **47%** occurred within **1.5 seconds**, versus **47%** of leave outcomes within **3.5 seconds**. The authors interpret this as less consideration before bypass; no eye tracking, reading, comprehension test, or verified attack outcome confirms that mechanism.

### Additional clicks and hidden information are weak proxies for deliberation

Chrome malware/phishing bypass required two clicks versus Firefox's one, yet its bypass rates were higher. Firefox SSL required three steps, but most people who reached its exception dialog completed it. Table 6 reports **85.4%** confirmation, leaving **14.6%** cancellation; elsewhere the paper summarizes completion as 84%. This is evidence that opening a secondary decision surface does not ensure reconsideration, not an experiment isolating click count.

Supplementary information was accessed in only **1.6%** of Chrome SSL impressions; Firefox recorded **zero** openings of technical details and **3%** certificate viewing among exception-dialog viewers. However, **21.3%** of exception-dialog openings included unchecking the permanent-exception default. That action establishes some agency; the authors' interpretation that users remained wary is a hypothesis, not a measured belief.

### Architecture and population confound apparent design effectiveness

Chrome made **20%** of all SSL warning impressions non-bypassable, versus **1%** in Firefox, due partly to stronger preloaded protections. Under an explicit counterfactual assumption about sensitive destinations, the authors estimate this selection could explain up to **15 points** of the browser gap. Remembered Firefox exceptions also remove repeated exposures from the denominator: a lower warning-level bypass rate need not mean fewer actual visits to problematic sites.

Operating-system and release-channel differences were substantial but inconsistent across warnings. Firefox phishing bypass was **8.9% Windows, 12.5% Mac, 34.8% Linux**; Chrome malware bypass was **23.5%, 16.6%, 13.9%**, respectively. Linux and prerelease use are unvalidated proxies for technical skill; the source does not establish that expertise itself causes disregard.

## Analyst Takeaways

1. **Warnings are not uniformly futile.** Most impressions in five combinations ended without proceeding, but the source measures blocked visits rather than infections prevented or informed understanding.
2. **Reduce uninformative repetition before adding friction.** Exposure frequency, false alarms, remembered decisions, and non-bypassable protections shape behavior; the paper recommends minimizing unnecessary warnings without testing that intervention.
3. **Put decision-critical information where decisions occur.** Rare detail-link use makes hidden explanations an unreliable primary communication strategy; comparative error-specific responses motivate, but do not experimentally validate, primary-surface explanations.
4. **Count decisions and outcomes separately.** Additional clicks, cancellation, changing a default, understanding a risk, and avoiding an attack are different measures. A bypass can be deliberate, and a safe exit can occur without comprehension.
5. **Preserve ecological context.** Prior lab-to-field discrepancies motivate field confirmation; they are not an exact replication because warning versions, populations, and exposures differ.

## Questions and Limitations

- No randomized design comparison or independent replication of these specific field estimates is reported. Opt-in selection, client overlap, repeated impressions, different channels, and missing destinations constrain causal conclusions.
- The study cannot distinguish true SSL attacks from captive portals, proxies, or misconfiguration; it cannot directly measure attention, comprehension, personal demographics, or within-person fatigue.
- **Internal inconsistencies**: Section 7.1.1 gives Firefox SSL bypass as **31.6%**, versus **33.0%** in the main results and abstract. Table 4 gives Firefox beta **32.2%**, versus the main text's **33.0%**; the source does not reconcile them.
- **Sample reconciliation**: the main total **25,405,944** uses Firefox beta SSL **10,976**; Appendix A reports **45,153** SSL impressions across beta/dev/nightly. These are different channel scopes. Table 10's Chrome Windows malware count **9,775,104** exceeds the whole-study Chrome malware count **6,040,082** and is incompatible with the channel totals; do not use it as a verified denominator.
- **Additional numeric discrepancy**: exception completion is described as **84%** in the discussion but **85.4%** in Table 6; the latter accompanies the reported 14.6% cancellation. The introductory description of collection as May/June also omits the method's April/July boundaries.
- **Redistribution evidence**: the PDF cover says proceedings open access is sponsored by USENIX, and the canonical venue page says papers are freely available. Neither supplies an explicit redistribution licence for this copy. Free access is not a public copying grant; archive the PDF privately.

## Vault Ideas Extracted

- [Warning and Approval Habituation](/vault/warning-and-approval-habituation.md) — Adds field associations between certificate-error prevalence, rapid bypass, and warning architecture while distinguishing inferred fatigue from measured attention or longitudinal habituation.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Shows why non-bypassable protection, warning escape, remembered exceptions, and multi-step bypass need different outcome measures rather than one generic safeguard metric.
- [Recognition over Recall](/vault/recognition-over-recall.md) — Adds evidence that supplementary explanations are rarely opened and motivates making decision-critical distinctions available on the primary decision surface.
