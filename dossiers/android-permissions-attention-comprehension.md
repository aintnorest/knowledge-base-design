---
type: Study Note
title: "Android Permissions: User Attention, Comprehension, and Behavior"
description: A 308-user survey and 25-user observational study find low attention and comprehension of install-time permissions, but neither tests redesigned prompts nor establishes that approval or rejection represents informed consent.
resource: https://doi.org/10.1145/2335356.2335360
source: https://doi.org/10.1145/2335356.2335360
tags: [privacy, attention, content-design, user-research, mobile, digital-interfaces]
timestamp: 2026-10-14T21:31:07Z
---

# Android Permissions — Study Notes

**Authors**: Adrienne Porter Felt, Elizabeth Ha, Serge Egelman, Ariel Haney, Erika Chin, and David Wagner.  
**Published**: Eighth Symposium on Usable Privacy and Security (SOUPS), July 11–13, 2012, Washington, DC; DOI **10.1145/2335356.2335360**, confirmed by the publisher's Crossref record.  
**Status**: Peer-reviewed mixed-method usability research: a September 2011 mobile survey and October 2011 observational interview study. Read the complete 14-page supplied publication-layout PDF, including all four figures, eight tables, and references. The copy does not print the DOI and retains an author-owned personal/classroom copying notice.

## What It Is

An evaluation of the then-current Android Market's **all-or-nothing install-time permission approval**. The study separates noticing the warning, understanding its scope, and changing behavior. Agreement with a permission request does not establish informed consent; rejection likewise can result from a mistaken understanding.

The source describes Android 2.2's **134 permissions** and the Market redesign released in August 2011. It is evidence about that historical interaction model, not a contemporary audit of runtime or individually selectable permissions.

## Problem and Motivation

A permission list delegates evaluation of application risk to the installer. The authors organize the evaluation around the Communication–Human Information Processing model: **attention → comprehension/memory → attitudes/beliefs → motivation → behavior**. Failure early in the chain prevents an informed downstream decision. Their studies primarily measure attention, comprehension, and past behavior; they do not fully evaluate attitudes or motivation.

The design placed permissions after the initial download decision, with large category headings, smaller specific descriptions, and optional detail dialogs. Figure 1 shows that hierarchy; Figures 2–3 show quiz stimuli and permissions on a familiar application's settings screen. Grouping can reduce list length while broad labels simultaneously distort what people think they are granting.

## Study Design

### Mobile Internet survey

An AdMob advertisement reached users inside Android applications in the **US and Canada** in September 2011, offering an Amazon MP3. Of **31,984 visitors**, **1,994** began and **350** completed the survey. Age, device, duplicate, and near-empty-response filtering left **308 valid respondents**; **302** answered all three comprehension questions and **307** answered the behavior question. Respondents reported **50% men and 49% women**; ages ranged from adult young users to over 62. Mean completion time was seven minutes.

The nine-page survey asked what people considered during their **last installation**, then presented **three randomized questions from eleven permission stimuli**, followed by privacy-attitude, past-behavior, and demographic questions. Each quiz question permitted multiple selections: exact correctness required **every correct option and no incorrect options**. Questions differed in having one, two, or four correct choices; the authors acknowledge that this affected difficulty.

The camera question has a specific interpretation problem: the authors discovered after designing it that viewing/editing the photo library required no permission. They therefore scored all four listed abilities as correct, even though the camera permission itself did not grant those library abilities. This tests what the application can do in that platform, not only the permission's marginal authorization.

### Observational interviews

Craigslist recruitment in the San Francisco Bay Area yielded **112 eligible applicants**, with age-stratified selection, **30 scheduled**, and **25 completed** sessions (**12 women, 13 men**). Compensation was **$60**. Interviews lasted **30–60 minutes** in a coffee shop, with two researchers and participants' own phones. Eligibility required the newer Market interface.

Participants installed a parking-finder application, then searched for and installed a coupon application while describing what they considered. Researchers withheld the security focus until later, recorded attention to reviews and permissions, asked privacy questions, and then elicited explanations of permissions for a familiar installed application. They also asked whether that application could send text messages without the user's knowledge and sought concrete details of past permission-based cancellation.

One person had never installed independently and was excluded from the attention analysis, making that denominator **24**, not 25. This was not a randomized intervention, and think-aloud recall is not eye tracking. Familiar applications differed in permissions, limiting comparison of participants' comprehension grades.

## Results / Admissions

### Attention: exposure does not ensure noticing

**17.5%** of survey respondents reported considering permissions at their last installation (**95% CI 13.5–22.3%**). In observation, **4/24 (17%; CI 5–37%)** noticed the current permission list; **10/24 (42%; CI 22–63%)** did not attend this time but knew such lists existed, and **10/24 (42%)** were unaware of them. Matching approximately 17% across samples and methods is convergent evidence, not an independent replication or proof of routine behavior at every installation.

Three of the ten aware-but-not-attending participants volunteered that they had stopped looking. One reported losing concern about location because so many applications requested it. Two unaware participants mistook the permission page for legal terms. These are concrete fatigue and framing accounts, not a manipulated repeated-exposure effect.

Privacy Fundamentalists in the survey were more likely to report attention (**40.5% of 42**, versus **13.9% of 266**, Fisher's exact **p < .0005**), yet most even in that group did not report it. No corresponding relationship appeared in the small observational sample.

### Comprehension: partial familiarity is not accurate scope

Only **8/302 (2.6%, rounded to 3%)** answered all three quiz questions correctly; average exact correctness was **21%**. Across **906 answers**, **53%** included at least one correct choice, including **17%** with a subset of the right options and **15%** with extra wrong options. Thus the headline does not imply that 97% understood nothing.

People reporting prior permission attention scored **30.3% versus 18.6%** (**U = 5,293, p < .007, r = .16**); Market users scored **22.3%**, compared with **4.7%** among 28 unofficial-store users (**U = 2,474, p < .001, r = .20**). Age correlated negatively with correct answers (**r = −.257, p < .0005**); phone-ownership duration, gender, and Westin classification showed no significant comprehension relationship. These associations are not causal training effects.

Exact correctness was worse when more choices were correct (**r = −.59, one-tailed p < .028**). Scores therefore cannot fairly rank permission wording across questions of different structure. For example, the one-choice calendar question had **45.5%** exact correctness, while the two-choice read-text-messages question had **0%**, despite many people recognizing at least part of its meaning.

In familiar-application explanations, mean complete correctness was **39%**, maximum **83%**, and two participants scored **0%**; omitted permissions were excluded. **Six of 25 (24%)** scored at least 70%, but only **five (20%)** also knew permissions were displayed during installation or had attended to them. On **25%** of explained permissions, participants could give no meaning at all. Descriptions were overly broad **29%** of the time, with all but three such responses attributed by the researchers to category headings.

The large headings often dominated the smaller specifics: “personal information” was interpreted as all phone data or passwords, and “phone calls” as many unrelated telephone capabilities. Understanding the ordinary words did not reliably supply their technical scope or practical risk.

### Reasoning about absence is particularly difficult

Only **9/25 (36%)** correctly judged whether their familiar application could send text messages; responses were not significantly better than guessing. Of **four** applications that could, **three** users said they could not. Of **21** that could not, **11** users said they could. These are opposite errors: false reassurance and overestimated authority.

To infer that an application cannot do something from a list of granted permissions, users need to know which absent permission would authorize that capability. Even a participant with some Android programming experience misjudged this. A positive list does not automatically communicate the boundary of allowed action.

### Behavior is not necessarily informed

**56.7% of 307** survey respondents claimed ever rejecting an application because of permissions (printed **95% CI 52.1–62.3%**). Affirmative choices came first, and respondents had already completed the permission quiz; the authors flag position bias, priming, and inaccurate recall.

Only **5/25 (20%)** interview participants supplied concrete examples; **2/25 (8%)** said probably without confirming detail, and **18/25 (72%)** said no. Two of the five affirmative participants had very poor comprehension: one explained none correctly and one explained only **two of seven** correctly. Only **2/25 (8%)** combined awareness, relatively good comprehension, and a reported past rejection. Neither study observed malware prevention or established the accuracy of those historical judgments.

### Reviews may carry information, but the proposed protection is untested

**71.1%** of survey users considered some review (**62.7%** Market, **13.6%** other Internet reviews, **8.4%** both). Researchers observed **22/25 (88%)** considering reviews; **6/25 (24%)** described learning permission information from reviews or news. The authors propose that an informed minority could protect others by sharing concerns. This study does not test that transfer, review accuracy, or downstream harm reduction.

## Recommendations versus Findings

The source recommends more accurate grouping, risk-oriented rather than resource-oriented language, fewer low-risk warnings, and reconsidering timing and contextual relevance. It suggests helping people understand permission absence and letting developers explain benefits. These are evidence-motivated proposals, **not evaluated redesigns**.

The authors explicitly discourage introducing individual permission choices before comprehension improves, reasoning that more decisions could add complexity without meaningful control. They also suggest non-dialog approaches and personalized warnings as open research directions. The source does not establish that granular permissions or runtime prompts are ineffective, nor that installation is universally the wrong moment.

## Analyst Takeaways

1. **Measure the whole chain.** Noticing, scope comprehension, motivation, and action require separate evidence; neither approval nor refusal validates understanding.
2. **Broad summaries can create false authority models.** Simplifying a list is useful only if the prominent labels preserve meaningful limits on what is being granted.
3. **Communicate boundaries as well as capabilities.** Asking users to infer denied capabilities from missing list entries imposes knowledge they often lack.
4. **Treat fatigue as a system problem, not a moral failing.** Repeated low-relevance requests can normalize acceptance, but this paper's evidence is descriptive rather than a quantified causal habituation effect.
5. **More options are not automatically more control.** The source's caution rests on poor existing comprehension; any redesigned granular choice system needs its own evaluation.

## Questions and Limitations

- Both samples are self-selected, and the observational study is small and regional. Survey selection, optional questions, phone completion burden, think-aloud tasks, and prior quiz exposure can affect estimates. No independent replication or longitudinal intervention test is established here; the two methods converge within one research project.
- Exact multi-select scoring, variable question difficulty, familiar applications with different permission sets, and omission filtering limit comparisons. Camera scoring conflates permission-controlled access with platform abilities requiring no permission.
- **Internal inconsistencies**: the method labels **1,994/31,984** starters as **1%**, though that ratio is approximately **6.2%**. Several Table 3 percentage denominators disagree with printed n: network-connectivity answers use **68** rather than **66**, text-message questions **55/78** rather than **54/77**, calendar **105** rather than **101**, and camera **73** rather than **72**. Tables 3–4 should not be silently harmonized.
- Figure 4's visible histogram bars total **27** participants, despite its caption and method specifying **25**. The prose's six participants at 70% or above agrees with the two upper populated bins; the lower-bin count discrepancy remains unresolved.
- References 40 and 41 duplicate the same *Crying Wolf* paper; reference 27 is printed as **2015** despite this 2012 publication. These bibliographic anomalies do not establish a later study version.
- **Redistribution evidence**: the PDF says copyright is held by the author/owner and grants digital/hard copying **“for personal or classroom use”**. It provides no general public redistribution grant or CC licence; keep this copy in the private archive and cite the DOI.

## Vault Ideas Extracted

- [Warning and Approval Habituation](/vault/warning-and-approval-habituation.md) — Adds convergent low-attention estimates, accounts of ceasing to inspect repeated prompts, and the distinction between consent behavior and demonstrated comprehension.
- [Recognition over Recall](/vault/recognition-over-recall.md) — Shows that a visible granted-capability list still requires recall of unshown alternatives to infer what an application cannot do.
- [Signifier Strength](/vault/signifier-strength.md) — Adds observed scope errors from prominent broad category labels overpowering narrower descriptions in a layered warning.
