---
type: Study Note
title: Information Foraging
description: Pirolli and Card develop patch, diet, and information-scent models of information seeking, supported by two small field examples and model fits to eight adults browsing a large text collection rather than a general causal test of interface labels.
resource: https://doi.org/10.1037/0033-295x.106.4.643
source: https://doi.org/10.1037/0033-295x.106.4.643
tags: [information-architecture, decision-making, human-performance, attention, digital-interfaces]
timestamp: 2026-10-15T04:37:20Z
---

# Information Foraging — Study Notes

**Authors**: Peter Pirolli and Stuart K. Card.  
**Published**: *Psychological Review* **106(4), 643–675, October 1999**. The copy read is the **84-page January 1999 UIR Technical Report**, marked accepted for publication, **not the version of record**. Crossref confirms the journal metadata and normalizes the DOI to **10.1037/0033-295x.106.4.643**; its publisher link uses uppercase X, not a different identifier.  
**Status**: Theoretical framework, mathematical adaptation analysis, and computational cognitive model supported by descriptive field observations and reanalysis of a small browsing experiment. Read the complete report, including all 19 figures, the interface screenshot, tables, references, and mathematical appendix.

## What It Is

An account of how people seek, gather, and consume information while balancing its expected task value against access, interpretation, and handling costs. Information foraging is embedded in a larger task: the value of a document depends on what someone is trying to accomplish, not on the document alone. People can adapt their strategies and reshape their information environment to improve the rate of useful information gained.

The optimization account is a hypothesis about adaptation under constraints, **not a claim that people possess perfect knowledge or always reach a global optimum**. The authors explicitly distinguish bounded, locally improving behavior from idealized rational choice and do not establish an evolutionary lineage from animal food seeking to modern information seeking.

## Principles as Ideas

### Information scent estimates a distant source from nearby cues

A title, citation, link, icon, or text snippet is a **proximal cue** to content that has not yet been inspected. Its information scent is the person's imperfect perception of that source's value, cost, or access path relative to the current goal. Recognizing a clickable object is insufficient: the person must also predict whether following it is worthwhile.

The ACT-IF model represents this assessment through associations between goal concepts and the words in a source summary. Related meanings can matter even without literal word overlap; cues also contextualize one another rather than contributing independent fixed amounts of relevance. The report does not directly test all cue types it names: the modeled interface uses textual cluster summaries and document titles.

### Patches create a staying-versus-leaving decision

Information arrives in clusters such as document collections, search results, piles, or sites. Continuing within one patch competes with moving to another. Under the marginal-value model's assumptions, leaving becomes advantageous when expected marginal gains within the patch fall to the average return available elsewhere. Lower switching costs can make earlier departure advantageous; shorter visits need not mean a worse experience.

### Enrichment competes with immediate consumption

People can spend time filtering, organizing, or refining an information environment before consuming its contents. Enrichment can reduce travel between patches or improve the concentration of relevant material within them. Its benefit must repay the time invested; the question is when further preparation is less productive than beginning to use the selected material.

### A useful information diet is selective, not merely relevant

A source can be relevant but too costly to process compared with available alternatives. The diet model concerns expected value per processing cost and the opportunity forgone by pursuing a low-yield item. Its idealized all-or-none selection rule assumes negligible item-recognition costs and known environmental properties; it is not a universal instruction to ignore whole categories of information.

## Evidence / Results

### Field examples motivate the theory

- **One professional technology analyst** was interviewed and videotaped in his office, with an annotated materials tour and collected work products. Topic-organized piles, scanning, and selective copying appeared to reduce access and reading costs. An estimated **600 magazines/month** narrowed to **50 magazines**, then approximately **230 marked articles**, with a final writing pile of approximately **45 articles**. The stated **factor-of-12** potential-reading-cost reduction is a descriptive estimate, not measured time saved against a randomized alternative; the increase in relevant-article proportion could not be quantified.
- **Two MBA teams, of two and three people**, were observed researching a strategic-management report; detailed results concern **one team**, without identifying which team size. Observers used field notes, recorded meetings and think-aloud work, and collected source materials and reports. A query produced approximately **300 citations**, reduced to **51 printed**, **27 pursued**, and **18 retrieved articles**. Estimated reading requirements fell from **29.7 to 1.8 hours**, over a factor of **16**, using an assumed reading speed rather than an observed counterfactual. The 18 articles averaged **5.6 schema-related annotations** each. Selection of shorter sources illustrates the proposed value–cost tradeoff, not a controlled effect of length.

### Eight adults provide the browsing-model data

**Eight adults**, recruited through Xerox PARC or Stanford's graduate program, volunteered or received **$10/hour**. Each completed **six topic searches** in a **742,833-document** TIPSTER collection using Scatter/Gather: inspect cluster summaries, select and recluster promising groups, then select relevant titles. Twelve topics were divided into easy/medium/hard sets based on expert-identified relevant-document counts, averaging **865 / 303 / 46**. Blocks contained easy, medium, then hard topics; block order was counterbalanced by randomized Latin square.

Participants were randomly assigned to **speeded browsing, N = 4** (one hour per three-topic block), or **relevance-rating browsing, N = 4** (no time limit, plus cluster classification and relevance estimates). Most analyses pool these differing procedures. Time-stamped interaction logs, cluster selections, and subjective relevance ratings supply the tests; the paper does not provide a controlled strong-versus-weak-label intervention.

| Analysis | Reported result | What it supports |
|---|---|---|
| Initial clusters selected | Easy **2.25**, medium **1.63**, hard **1.38**; coarse diet-model predictions **2 / 1 / 1** | Qualitative selectivity consistent with the model, not an intervention effect size |
| Scent across successive states | **R² = .76**, predicted slope 1, **302 transitions** | Model estimates track the modeled change in relevant-information concentration |
| Subjective relevance estimates | **R² = .92**, with a fitted linear mapping to geometric-mean ratings from **four people** | Agreement with aggregate ratings, not individual prediction accuracy or a parameter-free fit |
| Ranked cluster-selection actions | **858 observations**, **χ²(10) = 400.77, p < .0001** against random selection | Higher-ranked model actions are more likely to match behavior; not all actions are top-ranked |
| Selection threshold | **2,929 cluster observations**, **χ²(1) = 50.65, p < .0001** across predicted threshold | Selection changes around profitability equaling expected alternative return |

A separate computational characterization of the clustering environment uses **29 TREC queries** and fits the distal distribution with **R² = .92**. It calibrates the scent model's scaling parameter against the information environment rather than user-choice data. These model-fit statistics are **not standardized treatment effect sizes**, and the repeated observations do not turn eight people into hundreds or thousands of independent participants.

## Analyst Takeaways

1. **Evaluate the promise as well as the target.** Good underlying information is hard to find when the visible summary does not suggest its relevance.
2. **Keep scent and effort distinct.** A promising destination may still be expensive to reach or interpret; fewer actions do not necessarily yield more useful information.
3. **Treat organization as part of the task.** Filtering and grouping can improve future returns, but continuing to organize indefinitely can displace actual use.
4. **Measure useful outcomes, not consumption alone.** Reading more, staying longer, or opening more sources can reflect costly foraging rather than progress.

## Questions and Limitations

- This is theory development supported by small, historically specific studies, not a general experimental validation of web-navigation rules. The laboratory analysis reuses **Pirolli et al. (1996)** data; it is not an independent replication. No independent replication or failure to replicate is established by this source.
- Corpus word statistics stand in for participants' memory associations. The authors explicitly acknowledge not knowing whether the corpus represents each person's experience or whether exposure suffices to learn its statistics.
- Good aggregate model fits do not independently establish the psychological mechanism, guarantee calibrated expectations, or validate every proposed extension to risk, deadlines, and overlapping tasks.
- **Internal inconsistencies:** Figure 3 labels the conference stage **70 minutes**, while the text describes approximately **30 minutes**; its stages total **252 minutes**, whereas the text uses **212 minutes**. Table 1 prints **357 seconds** for Easy (5), despite **957 seconds** for easy-task handling elsewhere and a profitability of **.93**, which is consistent with 891/957 rather than 891/357. Equation 22's prose swaps the gain/document-count change-factor names relative to its displayed formula. The appendix describes **Nₜ** as relevant-document count on page 84 although page 81 uses it for total documents. Preserve these discrepancies rather than silently repair them.
- **Redistribution evidence**: the report identifies its authors, UIR provenance, acceptance status, and funding, but contains no explicit open licence or public redistribution grant. Acceptance for an APA journal and availability of a technical-report copy do not grant redistribution rights. Keep the intact report in the private archive and cite the journal DOI; do not imply that its pagination or all its details are the version of record.

## Vault Ideas Extracted

- [Information Scent](/vault/information-scent.md) — Supplies the proximal-cue framework, goal-relative value and effort distinction, and small-sample model evidence without treating model fit as a causal label-design effect.
