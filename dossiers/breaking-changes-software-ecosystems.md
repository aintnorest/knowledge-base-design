---
type: Study Note
title: "When and How to Make Breaking Changes: Policies and Practices in 18 Open Source Software Ecosystems"
description: Interviews and a mixed-method mapping of 18 software ecosystems show how compatibility practices allocate change costs differently despite shared stability values, without establishing causal effects or directly studying design systems.
resource: https://doi.org/10.1145/3447245
source: https://doi.org/10.1145/3447245
tags: [design-systems, design-process, digital-interfaces]
timestamp: 2026-10-13T18:45:20Z
---

# When and How to Make Breaking Changes — Study Notes

**Authors**: Chris Bogart, Christian Kästner, James Herbsleb, and Ferdian Thung; Carnegie Mellon University and Singapore Management University.  
**Published**: ACM Transactions on Software Engineering and Methodology, **30(4)**, **July 23, 2021**; DOI **10.1145/3447245**.  
**Status**: Peer-reviewed journal article; read the complete supplied **54-page CMU author preprint**, including all four figures, eleven tables, references, and appendices. This is not the version of record: its ACM reference block prints **Vol. 1, No. 1**, **“January 2021”**, and placeholder DOI **10.1145/nnnnnnn.nnnnnnn**. Publication metadata above identifies the verified version of record, not the copy read. The article extends the FSE 2016 paper *How to break an API*; this dossier covers the TOSEM article only.  

## What It Is

An exploratory sequential mixed-methods investigation of **how independently maintained software packages coordinate breaking changes**, whose effort those changes impose, and how ecosystem values relate to practices. Study 1 contrasts Eclipse, R/CRAN, and Node.js/npm through interviews and policy material. Study 2 combines a survey, policy analysis, and repository mining across **18 ecosystems**.

The source studies **software package ecosystems, not design systems**. Its relevance to shared component libraries is an **analyst extrapolation**: a library consumed by product teams is an upstream package with downstream consumers. The analogy is weaker for internal single-organization systems with mandated adoption, centrally allocated budgets, or limited ability to choose another dependency. Visual and interaction changes can also compile cleanly while breaking product expectations or end-user workflows; this paper does not measure those design outcomes.

## Problem and Motivation

Reuse avoids repeatedly developing common functionality, but it creates dependencies between teams with different priorities and schedules. An upstream improvement can require downstream rework; refusing that improvement can leave the upstream maintainer with technical debt, obsolete behavior, or forgone features. A developer can occupy both roles in different dependency relationships.

Section 2 defines a **breaking change** as any package change that would cause a fault in a dependent package if blindly adopted. This includes compilation failures, **incorrect behavior**, and **unacceptable performance**. Fixing a bug may therefore break consumers that relied on its actual behavior. Breaking is not limited to changing a declared interface, nor does labeling a release tell anyone whether the change was worth making.

The governing question is not simply “How can change be prevented?” It is **“Whose interests are served, who pays, and when?”** Version choice can postpone downstream work but defer access to fixes; compatibility can spare downstream teams while increasing upstream maintenance and complexity. Figure 1 locates these exchanges within community values, policies, practices, and tools.

## Mechanism and Study Design

### Study 1: contrasting cases, not prevalence estimates

The multiple case study reports **28 developers** across Eclipse, CRAN, and npm. Recruitment initially sought owners of packages with **at least two upstream and two downstream dependencies**, plus recent updates to the focal package and an upstream dependency in the year before interview (**2015**). Random batches of owners received personalized invitations; three developers were personal contacts. Later recruitment sought people involved in ecosystem tools or policies.

Semistructured telephone interviews lasted **30–60 minutes** and were recorded with consent. The evolving protocol probed concrete change decisions, alternatives, dependency selection, monitoring, and policy consequences. Researchers transcribed and iteratively coded interviews using **thematic analysis**, developing seven high-level themes; two researchers checked tagged quotations and resolved disagreements through discussion. They explicitly did **not** compute interrater reliability, claim exhaustive utterance identification, or treat interview counts as statistical prevalence. Policies, discussions, meeting minutes, and tools supplied complementary evidence.

A **member check with six respondents** found general agreement and produced corrections or qualifications, incorporated after rechecking the data. One important correction: CRAN's downstream-contact policy does not cover the majority of users outside CRAN. This checks fit with some interviewees, not independent replication or representativeness. The recruitment account contains unreconciled counts, recorded below.

### Study 2: perceived values, reported practices, and artifact proxies

The **108-question survey** ran **August–November 2016**. Recruitment used a research website, events, forums, mailing lists, Twitter, and **8,137 direct emails** to package authors in ecosystems with insufficient outreach responses. Prominent community members' tweets produced recruitment surges, especially for CRAN and npm.

Across the recruitment effort, **2,321 people started** and **932 completed**; **1,466 answered the early value questions**. Researchers solicited 31 ecosystems and retained **18 with at least 15 participants**, excluding 13 smaller-response ecosystems. Table 2's retained ecosystems all had more than 40 completed responses except Stackage (**17**) and Lua (**16**). Partial responses were retained: the mean complete-versus-incomplete difference across 65 scale questions was **0.13 scale points**, though individual differences were larger.

Respondents averaged **8.8 years developing software**, **7.2 in open source**, and **4.6 in their selected ecosystem**. **59%** had CS degrees, **59%** reported package-lead roles, and **11%** only used ecosystem packages. Of those reporting gender, **95.9% were male**, **3.2% female**, and **0.8% another gender**. These describe the responding sample, not the ecosystems' populations.

The survey distinguished **perceived community values** from **personal values for a named package**. Eleven values covered stability, innovation, replicability, compatibility, rapid access, quality, commerce, community, openness/fairness, curation, and fun/personal growth. Five ordered importance ratings ran from not important to extremely important, with separate opposition and don't-know options. Practice questions used agreement or frequency scales; 15 downstream-communication questions were skipped for people without consumers of their package. Figures 2–4 exclude skipped/don't-know answers, combine opposition with not important, and display smoothed distributions and means—not precise effect-size tables.

Policy analysis examined repository and language documentation for sanctioned practices: gatekeeping, access to old versions, release synchronization, and available dependency sources. Mining used libraries.io, repository sites, and World of Code, with unequal coverage across ecosystems:

- **Version constraints**: constraints observed during **2016**; the methods and Table 7 describe different aggregation units, so their percentages require caution.
- **Locking dependencies**: presence of recognized snapshot/lock artifacts in files committed during 2016; this detects selected mechanisms, not every way to reproduce a build.
- **Old-version maintenance**: a release number decreasing out of sequence during 2016, interpreted as a likely older-version update. This is a proxy, not inspection of patch contents or a support guarantee.
- **Cloning**: adoption during 2016 of an identical file blob **over 1 KB** previously seen in another package in the same ecosystem. It excludes modified clones and code from outside the ecosystem.

The taxonomy contains **55 practices** across platform/community choices, upstream communication/mitigation, and downstream monitoring/protection (Tables 4–6). **19 were not measured in Study 2**. The taxonomy maps a design space; it is not a ranked checklist of proven interventions.

## Results / Admissions

### Three different allocations of change cost

Section 4.2 reports **24/28 interviewees** saying they avoid downstream-breaking changes when possible. Their reasons included consumer interests and costs returning as requests for help, reversions, or abandonment. This concern coexisted with reasons to change: technical debt, efficiency, new requirements, and bug fixes. The source's printed technical-debt count does not match its listed interview codes.

| Ecosystem strategy in Study 1 | Who takes the work and what remains costly |
|---|---|
| **Eclipse: preserve existing clients** | Upstream maintainers accept compatibility work, extra complexity, and delayed modernization. Coordinated releases add planning work; some obsolete behavior persists. Stability is strongest in the core, not uniformly at its edges. |
| **CRAN: keep current repository versions mutually compatible** | Upstream maintainers notify affected repository packages; downstream maintainers must adapt promptly. Central checks protect installation coherence for end users, but short repair windows and restricted parallel maintenance burden package authors. Users outside CRAN are not equivalently protected. |
| **npm: signal change and permit independent version choice** | Upstream developers can evolve more freely; downstream developers choose when to migrate. Remaining on an old version postpones work, but eventually limits access to fixes/features. Parallel versions and older-release patches can reduce immediate coupling without eliminating maintenance. |

The source gives several **ways to divide or delay costs**, rather than a binary change/no-change choice (Section 4.2.2): retaining old interfaces increases upstream debt; parallel maintenance adds upstream effort; migration explanations and direct assistance spend upstream work to reduce downstream rework; release batching reduces disruption frequency but not necessarily severity. Separate stable and evolving interfaces or smaller packages can limit which users encounter change, at a higher design/maintenance cost.

Downstream strategies similarly exchange burdens (Section 4.3): active participation, social awareness, or reactive notifications; periodic updating; dependency vetting; copying or recreating functionality. Avoiding a dependency reduces exposure but gives up shared maintenance. Encapsulation was mentioned only rarely, and the authors acknowledge that they **did not explicitly ask about it**—absence of spontaneous mention is not evidence that wrappers are ineffective.

### Shared values do not produce identical practices

Stability, quality, and community were nearly universal stated values; compatibility, rapid access, and replicability were also broadly important (Section 5.2, Figure 2). Mean rankings still differed significantly across ecosystems for every surveyed value: **Kruskal–Wallis p < .00001**, with **χ² from 53.704 for quality to 178.69 for commerce**. Importance in all communities does not imply identical intensity or implementation.

Table 10 counts values most often tied for a respondent's highest rating, rather than forcing one winner. Selected rankings and its **C1 consensus** measure—the percentage rating no other value above the ecosystem's leading value—show distinct priorities:

| Ecosystem | Three most commonly highest-rated values | C1 |
|---|---|---|
| Stackage | Compatibility > replicability > curation | **75%** |
| Eclipse | Stability > compatibility > quality | **62%** |
| npm | Rapid access > community > innovation | **50%** |
| CRAN | Replicability > compatibility > innovation | **36%** |

Open-ended responses added a direct standardization/freedom tension: **12 responses** favored **standardization**, limiting choice to save time and effort; **17** favored **technical diversity**, protecting freedom to develop and collaborate in different ways (Section 5.2, Table 8, Appendix C). These are volunteered themes, not population preference rates. **13 responses (8%)** challenged the premise of ecosystem-wide values, either denying a coherent community or describing divergent subcommunities.

Stackage and Hackage offer a concrete contrast: curating mutually compatible package sets trades rapid release for compatibility; allowing independently submitted packages serves different priorities. The source does not establish that either model is globally superior.

### Practice frequencies and their boundaries

Figures 3–4 show median reported making and facing of breaking changes below **once a year**. The paper separately says only a quarter saw “a breaking change per year”; the questionnaire offers **several times a year**, not an exactly annual category. Do not convert this wording into a precise annual incident rate. Individual rarity can coexist with many ecosystem-wide incidents across many packages.

Every ecosystem's respondents agreed **on average** that they used semantic or comparable versioning, batched releases, documented changes, and were conservative about adding dependencies (Section 5.2). These are **self-reports**, not a measured semver-adherence percentage. Eclipse interviewees described documented breaks without major-version increments because increments themselves could trigger costly downstream updates. A nominal rule can conflict with the work it is meant to prevent.

Selected Table 7 mining results expose large differences in maintenance and dependency protection:

| Ecosystem | Out-of-sequence releases: old-version maintenance proxy | Selected dependency/locking observation |
|---|---|---|
| Maven | **25.4%** | **100.0%** exact constraints in the reported mining |
| NuGet | **17.6%** | **88.7%** minimum-only constraints |
| npm | **3.96%** | **78.6%** ranges; **0.8%** detected lock files |
| Rust/Cargo | **1.4%** | **93.6%** ranges; **14.6%** detected lock files |
| CRAN | **0.10%** | **75.6%** unconstrained; **0.8%** detected lock files |

Those are historical artifact observations, not current recommendations or percentages of releases breaking consumers. An earlier npm analysis in Section 4.2.3 found older-version maintenance in **24 of the 100 most-starred packages**. That selected popular-package result is not interchangeable with the **3.96%** ecosystem-wide 2016 proxy.

Measured file cloning stayed **below 10%** in every covered ecosystem (Table 7). Identical-file mining cannot establish how much reimplementation or modified copying occurred. CPAN illustrates another measurement mismatch: respondents reported dependency names alone (**43%**) or ranges (**36%**), while mining reported nearly **100% exact versions**. The authors suggest tooling may turn looser developer declarations into precise published metadata.

### Espoused values, perceived practice, and actual support differ

Study 2 partly corroborated Study 1 but contradicted some expectations (Section 5.1). CRAN respondents did **not** rank rapid access highly as interviews suggested, nor were they especially dependency-averse. They ranked highest in receiving personal change warnings but low in issuing them. The authors suggest interview sampling may have overweighted downstream perspectives.

In npm, **26.6%** said packages must meet strict repository acceptance standards despite the documented absence of such checks (Section 5.3). Different interpretations or subcommunity processes may explain the mismatch; it is not measured repository gatekeeping.

Across **418 value–practice comparisons** based on ecosystem means, **29** had uncorrected **p < .05**, but **none remained conclusive after Holm–Bonferroni correction** (**n = 18 ecosystems**, Section 5.4). Even the highlighted stability/exact-version association, **Spearman ρ = .506, p < .05**, belongs to this exploratory set. The paper supplies counterexamples to a simple mapping, not a validated causal model.

Its comparison of stability in Eclipse, Rust, and CPAN identifies different proposed mechanisms: compatibility obligations and design compromises; version choice and selective stability commitments; centralized volunteer testing. The authors interpret available labor, contributor incentives, and authority as important contextual factors. They do not experimentally establish the cost savings or comparative stability produced by each arrangement.

## Analyst Takeaways

1. **Treat compatibility policy as cost allocation.** Ask who maintains old behavior, who migrates, who coordinates, and who may defer. A release number does not answer those questions by itself.
2. **Distinguish preserving old clients from keeping current packages coherent.** Both can be called compatibility, yet they impose different schedules and responsibilities. Reproducibility is a third goal, not guaranteed by an easy current installation.
3. **Choose a compatible bundle of practices, not isolated rituals.** The source proposes that practices can conflict or complement each other—for example, change signaling does different work where adoption is optional than where current-version consistency is compulsory. These are discussion hypotheses, not tested prescriptions.
4. **Inspect enacted behavior as well as stated values.** Stable intentions can coexist with unstable packages, misunderstood admission rules, or infrequent warning behavior. Policy documents, self-reports, and artifact traces answer different questions.
5. **Make variation explicit without assuming unlimited flexibility.** Stable versus evolving surfaces, narrower packages, and curated sets can serve different constituencies while adding maintenance or slowing access. Standardization and technical diversity were genuinely reported competing values, but no optimal boundary was measured.

For a **design-system component library**, these takeaways are an **analyst extrapolation**, not a design-team finding: maintainers may absorb compatibility work, product teams may absorb migration, or consumers may defer upgrades. Changes in layout, focus behavior, semantics, or learned interaction can require review even when compilation succeeds. The study does not measure end-user relearning, accessibility regressions, visual consistency, or whether internal mandatory adoption alters the allocation. Compare the first-party [accessible color-system case study](/dossiers/designing-accessible-color-systems.md), which studies different evidence: palette constraints and selected contrast checks rather than dependency governance.

The general burden tradeoff also relates to [Cognitive Dimensions Tradeoffs](/vault/cognitive-dimensions-tradeoffs.md): reducing local change effort can add dependencies, learning, and management work. That is a conceptual connection, not a cognitive-performance result from this paper.

## Questions and Limitations

- **Selection and generalization**: the cases deliberately contrast policies; interview participation is voluntary. Survey outreach is nonrandom, with recruitment surges and a long instrument likely favoring interested, patient respondents. Ecosystems under the 15-response cutoff are absent; smaller communities and scientific workflow or operating-system package ecosystems were not comparably covered. The male-dominated, maintainer-heavy sample cannot represent all developer or end-user perspectives.
- **Careless-response handling**: researchers excluded blocks in which all items received exactly the same rating, across eight survey sections; exclusions ranged from **11 to 76 blocks**. Other answers from those people were retained. Uniform answers can also express genuine agreement; this rule and question-level attrition produce different denominators rather than one universal analysis sample.
- **Construct validity**: community ratings are respondents' perceptions, not directly observed values. Social desirability, ecosystem-specific standards, and differing meanings of “snapshot” or “breaking change” may alter answers. The intended behavioral definition may be broader than participants' compile-failure interpretation. Violin plots smooth variation and do not establish sharply separated ecosystem categories.
- **Association is not causation**: ecosystem-mean correlations have only **18 units**, many comparisons, and no conclusive corrected value–practice result. The personal/community value correlation pools multiple ratings per person (**ρ = .416, n = 10,878**); that is not 10,878 independent developers. No controlled intervention, direct effort-cost measurement, or evidence distinguishing cultural assimilation from value-based ecosystem selection is supplied.
- **Historical and proxy boundaries**: most observations describe **2016**, despite 2021 publication; the source expressly notes that Go dependency recommendations evolved after 2016. Repository coverage differs, old-version support is inferred from numbering, and locking is searched through selected artifacts. Current system behavior must not be inferred from these percentages.
- **Interview-account inconsistencies**: Section 3.2 prints **92 contacted**, **26 interviews**, then **8 additional developers**, while reporting **28 interviewees** overall; Table 1 contains **26 interview codes**, with two paired interviews yielding 28 individuals. The phases are not reconciled. Section 4.2.1 says **12** interviewees mentioned technical debt but lists **11 codes**; do not silently substitute a corrected count.
- **Mining-definition inconsistency**: Section 3.3.6 describes version-constraint percentages as packages flagged for any use during 2016, potentially adding to more than 100%; Table 7 describes proportions over dependency instances across package versions, and its rows approximately partition 100%. Its printed npm caret/minimum and tilde/range examples also conflict with the bounded-major caret description later in Section 4.2.2. Treat constraint columns as the source's reported classification, not a reproducible implementation specification.
- **Other printed discrepancies**: Section 5.2 describes personal quality ratings as about **0.8** scale points above community ratings, then gives **0.9**. Table 8 lists **5 CPAN testability** responses, whereas Section 5.4 says **12/30 (40%)** CPAN commenters mentioned testability; the source does not reconcile these counts. Appendix D's searched npm snapshot filename is misspelled, leaving uncertainty about the search actually used. Its lock-file notes also cite later documentation without fully resolving its relation to 2016 detection. Section 6.2 labels a practice-similarity correlation as a value correlation in its parenthetical explanation, so it should not be promoted into clean causal evidence.
- **Redistribution evidence**: the complete author preprint carries the ACM-style publication line **“2021. 1049-331X/2021/1-ART $15.00”** and placeholder DOI, but no explicit copyright-holder sentence, Creative Commons license, or redistribution grant. Author hosting and a publicly available dataset do not license redistribution of the article PDF; this copy belongs in **`archive/private/`**.

## Vault Ideas Extracted

- [Breaking-Change Cost Allocation](/vault/breaking-change-cost-allocation.md) — Contributes the upstream/downstream/end-user distinction, behavioral breaking-change definition, and contrasting Eclipse, CRAN, and npm allocations; retaining interfaces, parallel maintenance, migration assistance, and version choice shift or postpone effort rather than remove it. The historical mining proxies show variation, not measured causal savings.
- [Standardization versus Customization in Design Systems](/vault/standardization-versus-customization.md) — Contributes volunteered standardization versus technical-diversity values, curated compatibility versus rapid-access tradeoffs, and differentiated stability commitments. Its application to product-team component systems is an explicit extrapolation; the source does not test customization policies or establish an optimal centralization boundary.
