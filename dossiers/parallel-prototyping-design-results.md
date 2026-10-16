---
type: Study Note
title: Parallel Prototyping Leads to Better Design Results, More Divergence, and Increased Self-Efficacy
description: A 33-person nonprofessional banner-ad experiment favors creating alternatives before critique over serial refinement, with qualified advertising metrics, more divergent concepts, and greater task-confidence gains.
resource: https://doi.org/10.1145/1879831.1879836
source: https://doi.org/10.1145/1879831.1879836
tags: [design-process, prototyping, usability-evaluation, ux-metrics, digital-interfaces]
timestamp: 2026-10-15T04:37:29Z
---

# Parallel Prototyping and Design Results — Study Notes

**Authors**: Steven P. Dow, Alana Glassco, Jonathan Kass, Melissa Schwarz, Daniel L. Schwartz, and Scott R. Klemmer.  
**Published**: ACM Transactions on Computer-Human Interaction **17(4), Article 18, December 2010, 24 pages**; received May 2010, revised and accepted August 2010.  
**Status**: Peer-reviewed between-subjects experiment, with two follow-up investigations of critique. Read the complete Stanford-hosted publication-layout PDF, including all ten figures, campaign table, four appendices, and references. The printed DOI establishes the source key.

## What It Is

A controlled comparison of **creating alternatives before receiving critique** with **receiving critique after every prototype**. The same number of designs, critique statements, and allotted minutes produced different outcomes. This is evidence for structuring exploration, not evidence that merely producing more artifacts or hiring parallel teams improves design.

## Problem and Proposed Mechanism

Immediate feedback can make refinement efficient while encouraging fixation on the current concept. Alternatives may create a comparison space for understanding design relationships, permit exploration before judgment, and separate personal investment from a single idea. These are the authors' explanations: the experiment measures outputs, similarity, confidence, and interviews, not causal mediation through comparison or ego protection.

## Study Design

### Participants and task

Of **36 recruited, 33 completed**; mean age **22**, about three-quarters students, **19 women**. Stratified random assignment balanced gender and prior experience: **16 parallel, 17 serial**. **14** had some prior graphic/ad-design experience; **none were professional designers**, and none had used the study's design tool. Thus the sample includes complete novices and somewhat experienced nonprofessionals, not an expert design population.

Participants independently made Web banner ads for a design magazine. Both conditions produced **five prototypes plus one final ad**. Parallel participants made **three**, received critique on those three, then made **two**, received critique again, and made the final. Serial participants received critique after each of five prototypes before making the final. Each prototype had **10 minutes**, each critique interval **5 minutes per prototype**, and the final **15 minutes**; the full session was **150 minutes**, compensated **$30**. All learned the same unfamiliar graphic-design tool and passed a replication practice task.

An experimenter selected **three nonrepeating descriptive statements per prototype**, one each about theme, composition/layout, and surface elements, from a professional-developed corpus. Feedback did not explicitly compare alternatives. The experimenter knew condition; time, corpus, and selection procedure were matched, but critique content was not a blinded intervention.

### Measures

- **Performance:** a **15-day** real advertising campaign, clicks/impressions, client-site visitors and engagement; **four client editors and three advertising professionals**, blind to condition, independently rated five dimensions totaling **0–50**.
- **Divergence:** **14,850 pairwise similarity judgments**, 30 assessments for each of 15 within-designer pairs across 33 designers. These are repeated judgments of designs, not 14,850 independent designers.
- **Self-efficacy:** four pre/post task-confidence questions; interviews explored reactions to feedback and intended future practice. Confidence is not independently tested design competence or long-term persistence.

## Results / Admissions

### Performance improved, but the advertising platform adapts exposure

The campaign recorded **501 clicks on 1,180,320 impressions**. Parallel/serial totals were **296/205 clicks** on **665,133/515,187 impressions**. Table I and the reported final-CTR analysis give **445.0/397.9 clicks per million impressions**, **F(1,30) = 4.227, p < .05**: a reported difference of **47.1 per million**, about **11.8% relative**, calculated from those rounded values.

MySpace preferentially served better-performing ads. The authors therefore also compared the first five days, when exposure was approximately balanced: **44 clicks/79,800 impressions parallel** versus **26/79,658 serial**, **χ² = 4.60, p < .05**. Calculated from those text counts, rates are approximately **.0551%/.0326%**, an absolute difference of **.0225 percentage points**. The whole-campaign exposure advantage is not an independently randomized benefit.

Client-site time averaged **31.3 versus 12.9 seconds**, reported **t(493) = 1.781, p < .05**. Further-page navigation did **not** differ significantly: **71/264 versus 35/158**, **χ² = 1.18, p > .05**. The broad claim of better performance on every measure should not erase that null.

Expert ratings favored parallel: **24.4 (SD 9.7) versus 21.7 (SD 8.8)**, a **2.7-point difference on 50**, **F(1,203) = 3.871, p < .05**. Only tastefulness and adherence to graphic-design principles were independently significant among the five dimensions. Click performance did not significantly predict overall expert rating (**R² = .057, p > .05**); a click is not the same outcome as a suitable design.

### More divergence and greater confidence

Serial sets were rated more similar: **3.25 (SD 1.96) versus 2.78 (SD 1.66)**, **F(1,14816) = 239.3, p < .05**, a **.47-point difference**. Similarity did not significantly predict click performance or expert quality. More variation is not itself demonstrated to cause better designs.

Reported confidence gain was **2.5 parallel versus .4 serial**, **F(1,29) = 4.210, p < .05**. The condition-by-experience interaction was significant, **F(1,29) = 6.331, p < .05**: complete novices gained about **2.9** in parallel and lost **.73** in serial. These scale-point effects retain the paper's unresolved scoring inconsistency below.

In interviews, **13/16 parallel versus 6/17 serial** called critique helpful/intuitive; **0/16 versus 8/17** described it negatively. **12/16 versus 5/17** volunteered contact details for future magazine work. These observations support different reactions to critique, not a demonstrated durable motivation effect.

### Follow-ups check critique, not replication of parallel's advantage

Two unfamiliar ad professionals evaluated selected versus random critique triads, blind to condition. Agreement with the original experimenter was moderate and comparable (**ICC .434 parallel, .496 serial**, no significant difference). This reduces one concern about differential critique suitability; it does not eliminate all experimenter bias.

A separate **30-person randomized serial-only** study compared targeted, random, and no critique. Three-week campaign totals were **203/49,414**, **157/49,543**, and **179/49,663** clicks/impressions respectively, **χ² = 6.01, p < .05**. Twenty experts rated targeted/random/none **15.9/15.1/14.4 out of 30**, **F(2,597) = 3.287, p < .05**. This supports the usefulness of targeted critique in that task; it does not repeat the parallel-versus-serial manipulation or directly measure learning of principles.

## Analyst Takeaways

1. **Preserve an exploration phase before critique narrows the search.** Parallel here means multiple concepts by the same individual, not concurrent staffing or more total production.
2. **Keep critique useful, not merely delayed.** The main result combines alternative creation and batched feedback; their separate causal contributions are unresolved.
3. **Evaluate several definitions of quality.** Engagement, expert fit, conceptual diversity, and confidence can diverge.
4. **Treat adaptive distribution as part of the measurement system.** Raw clicks and impressions confound design response with subsequent allocation; exposure-balanced comparisons are more informative.

## Questions and Limitations

- Small, short, individual banner-ad task with nonprofessional designers, scripted critique, one client, and one advertising platform. No independent or long-term replication of the central manipulation is established by this source; team and professional-design generalization remains future work.
- Several analyses use impression-, visitor-, rating-, or judgment-level observations for outcomes arising from **33 designers**. Dependence and the platform's adaptive allocation constrain precision and causal interpretation; no standardized designer-level effect sizes or confidence intervals are supplied.
- **Internal scoring inconsistency:** methods and Appendix B specify four **1–7** confidence items, but results describe a total **“out of 20.”** Similarity is described as **1–7** in methods and Figure 4, but **0–7** in results. Do not infer a missing recoding.
- **Internal count inconsistency:** first-five-day impressions are **79,800/79,658** in text but **79,844/79,684** in Figure 7. Table I gives **445.0** parallel clicks per million, while its pooled totals calculate to about **445.02**; serial pooled totals yield about **397.91**, consistent with rounding.
- **Internal ranking inconsistency:** Figure 6 labels the highest expert-rated ad **ninth** in CTR, whereas results call it **fourth**. The paper also reports **422 site visitors** but visitor-time tests use degrees of freedom **493/491**, without explaining the observation-count difference.
- **Redistribution evidence**: the ACM notice permits personal/classroom copies but states that republishing, posting on servers, or redistribution requires prior specific permission and/or a fee. No explicit public redistribution licence is given; the Stanford-hosted copy belongs in `archive/private/`.

## Vault Ideas Extracted

- [Parallel Design Exploration](/vault/parallel-design-exploration.md) — Supplies a time- and prototype-count-matched experiment on alternatives before critique, with nonprofessional banner-ad results, adaptive-exposure qualifications, divergence, and task-confidence outcomes.
