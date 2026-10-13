---
type: Study Note
title: "The Cognitive Walkthrough Method: A Practitioner's Guide"
description: A theory-based inspection explains how users learn through goal-directed exploration and exposes knowledge assumptions at each action, but its simplified third version had no empirical validation in this technical report.
resource: https://www.colorado.edu/ics/sites/default/files/attached-files/93-07.pdf
source: https://www.colorado.edu/ics/sites/default/files/attached-files/93-07.pdf
tags: [usability-evaluation, interaction-design, cognitive-load, design-process, digital-interfaces]
timestamp: 2026-10-12T20:35:00Z
---

# Cognitive Walkthrough — Study Notes

**Authors**: Cathleen Wharton, John Rieman, Clayton Lewis, and Peter Polson; University of Colorado at Boulder.  
**Published**: Institute of Cognitive Science Technical Report **93-07 / CU-ICS-93-07**, 1993.  
**Status**: University technical report and prospective book-chapter manuscript; no separate peer-review status is stated for this report. Read the complete supplied **49-page scan**, OCRing every page and viewing the two-page overview table. The cover and title page identify the technical report; the title page says it will appear in Nielsen and Mack's *Usability Inspection Methods* in **1994**, a related but distinct publication.  

## What It Is

A practitioner account of cognitive walkthrough (CW), a usability inspection aimed specifically at **ease of learning by exploration**. Reviewers reason about why a specified user would choose each action needed for a concrete task, and whether the response would let that person recognize progress. The result is an explicit account of required knowledge and likely breakdowns—not observation of a real user's behavior and not a comprehensive usability verdict.

The report presents the **third version** of the method. Its shift from elaborate goal structures to credible success and failure stories is central: a usable evaluation method must preserve its theory without making analysts spend their attention on burdensome formalism.

## Problem and Motivation

People often want to accomplish work before investing in broad training. They learn a feature when its immediate benefit warrants the effort. An interface must therefore help someone move from an initially rough task description to an appropriate action and interpretable result.

Designers already know the intended solution. That knowledge can conceal arbitrary prerequisite actions, unfamiliar labels, invisible interaction possibilities, and responses meaningful only after prior experience. A walkthrough makes those assumptions discussable before a full implementation exists. It is particularly suited to prompted, walk-up-and-use interaction, where visible choices and feedback guide exploratory problem solving.

## Mechanism as an Idea

### Learning by exploration

The underlying **CE+ theory** models a repeating cycle: begin with a rough task goal; explore available actions and choose one that seems relevant; observe its consequences; and decide what to do next. Means–ends analysis selects actions expected to reduce an important difference between current and desired state. Skill-acquisition theory supplies the learning link: successful actions become associated with goals and context, so easing their discovery can support later skill.

Users with little domain or interface experience depend especially on **label following**: an action appears promising because its words or graphics resemble the current task description. More sophisticated users can decompose goals and infer consequences from deeper knowledge, but the action still needs to make sense relative to their current goal. Labels are not magic; the relevant vocabulary is the user's, and plausible rival labels can attract the wrong choice.

### Four distinct questions

At each action the analyst asks:

1. **Will the user try to achieve the right effect?** A necessary system prerequisite may never occur to someone pursuing the real-world goal.
2. **Will the user notice that the correct action is available?** Knowing the goal does not reveal an unprompted gesture or hidden command.
3. **Will the user associate the correct action with the effect they are trying to achieve?** A visible control can remain semantically opaque or lose to a misleading alternative.
4. **If the correct action is performed, will the user see that progress is being made toward solution of their task?** A reaction must be interpretable in task terms, not merely perceptible.

The questions are **guidelines for a credible explanation**, not four universal interface requirements mechanically scored. Credibility rests on stated user background, task knowledge, interface experience, and information acquired earlier in the task. Assuming everyone knows a convention is not evidence that the story works.

### Task-bound reasoning and the correct-path boundary

The method combines a defined population, realistic tasks and context, a sufficiently detailed interface, and the intended action sequence. Action granularity depends on prior expertise: a familiar compound operation may be one unit for an expert and several uncertain decisions for a novice.

Even after identifying a likely failure, analysis proceeds as if the correct action occurred. This **stay-on-track assumption** enables examination of later steps but excludes the actual branching trajectory after error. It cannot by itself characterize recovery, repeated failure, or the probability of completing the journey. Analysts must distinguish genuine prior knowledge from knowledge hypothetically introduced to repair an earlier breakdown.

The call-forwarding example illustrates the model rather than measuring its accuracy. A user wanting to forward calls must first cancel forwarding and hang up—system-oriented prerequisites the user's goal gives no reason to anticipate. Similar-looking forwarding labels and unfamiliar confirmation tones expose separate action-mapping and feedback failures. The preferred conceptual remedy is to remove needless prerequisites; adding explanations is a fallback, not necessarily an equivalent repair.

## Results / Admissions

### Method evolution is evidence about the method's own usability

The original short form failed with untrained students and industrial designers: terms such as goals versus actions were misunderstood, and broad questions concealed issues. The second version made goal structures explicit but became difficult even for cognitively trained analysts and was criticized as tedious. The third version uses stories to recruit ordinary knowledge about intentions and motivation, while still requiring basic cognitive-theory understanding or an experienced facilitator.

At **CHI '92**, tutorial groups of **four to five** reportedly found intended difficulties and additional insights using the simplified method. Course use was more mixed: students did not consistently apply the criteria well. The authors explicitly state **“We do not yet have any empirical data validating the new version of the method.”** These are teaching experiences, not a participant experiment with a reported total sample, randomized conditions, or effect size. Claimed **two- to fourfold time reductions** likewise come from experience with looser and revised variants, without a controlled timing study presented here.

### Reported evaluations mostly concern earlier variants

The report discusses studies rather than presenting a new recruited-participant trial. Its quantitative summaries include:

- **Jeffries et al. (1991)** compared CW, heuristic evaluation, guidelines, and usability testing. On a **nine-point severity scale** (1 trivial, 9 critical), mean severity was **3.44 CW**, **3.59 heuristic evaluation**, **3.61 guidelines**, and **4.15 user testing**. The authors suggest problem-report phrasing may have biased severity judgments; this is an explanation, not an isolated causal result. CW tended toward specific learnability problems rather than global or recurring ones. CW and heuristic findings were described as **20% lower** in recurring problems than guidelines and testing, without a clear relative-versus-percentage-point denominator here.
- **Cuomo and Bowen (1992)** categorized findings by Norman's action stages and by data entry, data display, sequence control, and user guidance. Earlier CW concentrated on action specification, data entry, and sequence control; relatively little overlap with other methods suggests complementary scope. The suggestion that the third version repairs later-stage weaknesses is not validated by those earlier data.
- An **October 1992 personal communication from Cuomo**, reporting follow-up user testing, says **11/51 guideline problem types (22%)**, **16/35 heuristic types (46%)**, and **14/24 CW types (58%)** caused noticeable difficulty for at least one user. These are confirmation proportions among predictions, not sensitivity to all observed problems. The report does not supply the follow-up user sample, complete task/stimulus account, uncertainty, or a published replication; the apparent ranking must remain bounded to this report of that comparison.
- Mean findings per evaluator/group, quoted in the order **Jeffries / Cuomo–Bowen**, were **30.25 / 28.5** for a heuristic evaluator, **35 / 43** for CW, and **35 / 113** for guidelines; usability testing yielded **32** in the first study. Units mix individual evaluators and teams, and training, hours, task familiarity, and applications varied. Guideline sets also differed sharply: **62 versus 944**. These figures do not demonstrate equivalence or a universal number of discoverable problems.

The report does not give full participant counts or study protocols for these comparisons. Its admission that the studies conflict is more defensible than its proposed approximate “magic” problem count. [The later evaluator-effect review](/dossiers/evaluator-effect-usability-evaluation-methods.md) supplies a separate caution: specifying steps and questions does not remove evaluator judgment or guarantee agreement.

### Scope the authors explicitly concede

CW prioritizes learning, potentially at the expense of expert productivity. It is weak as a sole method for global consistency, catastrophic-error risk, general interface flaws, or whether an entire task organization matches users' needs. A paper description can expose conceptual barriers but cannot adequately represent timing, speech pacing, color distinctions, or physical interaction. Programming walkthroughs extend the hypothetical-problem-solving idea to unprompted work, but are adaptations, not proof that ordinary CW covers programming effectively.

## Analyst Takeaways

1. **Expose the missing knowledge, not just a bad label.** Failure can arise before action search because the user has no reason to form the system's required subgoal.
2. **Separate availability, mapping, and progress interpretation.** Making a control visible cannot repair an incomprehensible consequence or an unnecessary prerequisite.
3. **Make the hypothetical user falsifiable.** Tie prior knowledge and terminology to research; use unresolved story assumptions to focus actual user testing.
4. **Preserve scope boundaries.** A correct-path learnability inspection is not an error-recovery analysis, a productivity comparison, or a whole-interface certification.
5. **Use theory to guide attention, not paperwork to simulate rigor.** The method's own history shows that more formal recording can make evaluation harder without establishing better outcomes.

## Questions and Limitations

- This is a method-developer account, not an independent systematic review. Most comparative evidence concerns the second version, while favorable claims about the third are explicitly anecdotal. No independent replication of the third version is established here.
- The page-31 claim that comparison reduces the severity difference to **0.17** applies to guidelines (**3.61 − 3.44**); the heuristic difference is **0.15**, while the user-testing difference remains **0.71**. The wording should not be interpreted as a single adjusted difference for all methods.
- The proposed **28–43 / “35 ± 7”** typical problem range is internally loose: the displayed **28.5** falls slightly below 35 − 7, **43** exceeds 35 + 7, and the **113** guideline result is explicitly excluded. It is speculative rhetoric, not an empirical law.
- Unresolved **“Chapter ----”** cross-references identify the draft's prospective chapter status. The **49 scanned pages** contain cover/title/blank material and **45 numbered manuscript pages**, not 49 pages of substantive chapter text.
- The file itself identifies **CU-ICS-93-07**, but does not print the supplied hosted URL or a DOI. The canonical URL identifies this report, not the later 1994 book chapter.
- **Redistribution evidence**: no explicit redistribution grant or open license is stated in the scanned report. University hosting and the notice of future Wiley publication do not supply permission for repository republication; archive the raw copy privately.

## Vault Ideas Extracted

- [Cognitive Walkthrough](/vault/cognitive-walkthrough.md) — Explains the exploratory-learning cycle, four distinct breakdown questions, correct-path assumption, and third-version validation gap.
- [Signifier Strength](/vault/signifier-strength.md) — Separates noticing an action from understanding its goal relevance, grounded in a theory-based inspection rather than a new cue experiment.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Requires feedback that makes progress meaningful in task vocabulary, not simply a detectable reaction.
