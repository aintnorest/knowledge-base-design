---
type: Study Note
title: First Principles of Interaction Design (Revised & Expanded)
description: Tognazzini argues for visible, forgiving, user-controlled interfaces and evaluates simplicity through human productivity, but most detailed rules are practitioner guidance rather than traceable experimental findings.
resource: https://asktog.com/atc/principles-of-interaction-design/
source: https://asktog.com/atc/principles-of-interaction-design/
tags: [interaction-design, usability-evaluation, human-performance, cognitive-load, digital-interfaces]
timestamp: 2026-10-11T23:50:47Z
---

# First Principles of Interaction Design — Study Notes

**Authors**: Bruce Tognazzini.  
**Published**: March 5, 2014, local publication date; metadata records March 6 UTC and a last modification on December 18, 2014. Copyright dates span 1978–2014.  
**Status**: Revised and expanded practitioner guidance on askTog, read from the saved page captured October 11, 2026, including its six substantive illustrations. The page's `rel="canonical"` identifies the resource URL above. Its examples and product judgments belong to the 2014 revision, not to current versions of the named products.  

## What It Is

A broad interaction-design framework spanning **19 principle families**, with subprinciples, argued rationales, first-hand examples, and a few references to research. The unifying model is **a visible and forgiving environment in which the user remains in control and the system does more of the work**. A clean-looking interface is not necessarily a simple activity; hidden controls, discarded work, uncertain delays, and changed learned behavior can make a visually sparse product expensive to use.

This is neither a systematic research review nor a consensus standard. Its value lies in a veteran designer's distinctions and diagnostic questions. It repeatedly calls for usability testing, but the existence of that recommendation is not evidence that each accompanying rule has been experimentally established.

## Problem and Motivation

Tognazzini targets a mismatch between showroom appeal and sustained use. Interfaces can appear easy to a buyer because complexity has been hidden, yet force actual users to hunt for controls, learn undocumented gestures, or reconstruct lost state. He is particularly critical of moving small-screen compromises to large-screen products and of prioritizing fashionable minimalism over legibility and productivity.

He explicitly acknowledges selection bias: he uses Apple products almost exclusively, worked at Apple for more than fourteen years, and holds Apple stock. Their prevalence among negative examples reflects his experience, not a comparative sample of manufacturers. The revised introduction also invites correction and better examples.

## Principles as Ideas

### Control, expectations, and comprehension

- **Aesthetics**: visual design needs specialist skill and the same testing attention as behavior. Fashion is acceptable when it preserves or improves learnability, satisfaction, and productivity; looking newer is not itself a user benefit. No comparative visual-design experiment is presented.
- **Anticipation**: bring necessary information and tools to the current task rather than making users collect them elsewhere. This requires domain understanding and evidence that people can actually find what is present. The rationale is reduced search, interruption, and abandonment, not a tested prediction that any particular arrangement works.
- **Autonomy**: let users make their own choices within an explorable, nonhazardous environment. Control requires accurate, up-to-date, easily visible status. The analogy that people need boundaries as well as freedom cites **“Yallum, 1980”** without a full reference. Personalization and adjustable input thresholds are argued from frustration and human variation, not measured treatment effects.
- **Color**: preserve color as a useful communication channel while supplying independent secondary cues. Accessibility is achieved by redundant meaning, not by eliminating the channel everyone else can use. The stated **approximately 10% of males and fewer than 1% of females** with some color blindness are uncited approximations here, not globally representative prevalence estimates.
- **Consistency**: protect learned behavior more rigidly than branding or broad visual uniformity. His increasing-strength hierarchy is platform/in-house appearance, suite appearance, single-product appearance, small visible controls, invisible structures, and finally **interpretation of habitual user actions**. Different behavior should look different; redesigns need continuity, not frozen uniformity. Buxton's quoted priority is consistency with **user expectations**. The Xerox Star printing anecdote illustrates why an elegant universal “move” rule failed when people expected printing not to destroy the original.
- **Defaults**: a default is useful only when it is a plausible choice and cheap to replace. A weak default consumes attention deciding to reject it. Reset language and visual scope must make the extent of a reversion predictable, or users either avoid benign recovery or accidentally erase valuable customization. These are cognitive and risk rationales, not a demonstrated universal benefit for preselection.
- **Human interface objects**: what users perceive and manipulate need not map to programming objects. Familiar controls carry expected manipulation and consequences; using a familiar object for different consequences corrupts the convention. The trash-can example distinguishes reversible storage from immediate destruction.
- **Metaphors**: use familiar experience to communicate the conceptual model, preferably perceptibly rather than through long prose; expand or abandon the analogy when it limits capability. The point is transferable understanding, not literal imitation of physical objects. The HyperCard exploded diagram makes shared background, individual foreground, and controls distinguishable; the dish-aiming illustrations replace abstract map interpretation with visible lines of sight.

### Discoverability, learning, and genuine simplicity

- **Discoverability**: necessary controls must be visible or reachable through visible structures. Hidden availability is effectively absent for people who never discover it. Teach gestures through perceivable diagrams, offer help that can itself be found, and introduce advanced features when they become relevant rather than repeating indiscriminate hints. Exceptions are allowed for habitually used, constrained mobile environments when users will reliably encounter the standard reveal gesture and can find help. The Popular Photography diagram and Snapseed overlay exemplify explicit gestural vocabulary, not measured proof of learning gains.
- **Learnability**: initial ease and experienced efficiency are separate objectives, not automatically opposing ones. Usage frequency and purchasing context determine their relative priority. Short first-use sessions cannot establish the mature productivity of a product intended for daily work; the framework calls for observing the learning trajectory and eventual performance, not just novice success.
- **Simplicity**: optimize the user's whole activity, including setup and repeated use. Additional setup effort can pay for lower recurring effort, but assuming a technically skilled household member is a contextual assumption, not a universal entitlement. **Progressive revelation** postpones capabilities that are not yet needed; the **illusion of simplicity** hides capabilities required now. Removing necessary functions merely displaces complexity into workarounds.
- **Visible navigation**: externalize position and available routes rather than requiring elaborate mental maps. Stable surroundings, visible current selection, and visible relation to the parent task support orientation. The recommendation for an overlay with the parent screen still visible is argued as recognition replacing memory, not evidence that overlays always outperform navigation.

### Productivity, movement, waits, and continuity

- **Efficiency of the user**: judge total human productivity rather than local machine, coding, or IT-department efficiency. A small implementation saving can impose repeated effort and costly errors across many people. Architecture and task flow can remove more work than cosmetic changes. Helpful error messages explain the problem, an actionable remedy, and the possibility of a deeper system malfunction instead of automatically blaming the user.
- **Explorable interfaces**: supply stable landmarks and a clear low-effort path without prohibiting exploration. Greater guidance suits unfamiliar, single-use tasks; experts need more latitude. Reversible actions and an obvious exit reduce the need for cautious behavior and repetitive confirmations. Recovering earlier steps should preserve later work. This is a **safety enables fluency** argument, not a recommendation to remove every confirmation regardless of consequences.
- **Fitts's law**: target acquisition depends on distance and target size; a task's cost also includes how many physical and virtual targets must be acquired. Pointer pinning at screen edges and corners can increase effective target size. The page explicitly distinguishes direct touch, where those pinning benefits normally disappear, from indirect mouse input. It calls for timed studies rather than judging a layout by appearance alone.
- **Latency reduction**: separate actual time from blocked time and uncertainty. Let useful work continue during computation, acknowledge input promptly, avoid duplicate activations caused by missing feedback, and communicate the wait honestly. Faster computation and better feedback are complementary; a busy indicator does not cure unnecessary delay.
- **Protect users' work**: preserve effort through errors, navigation, transmission trouble, and interrupted sessions. Discarding an entire form after one invalid field makes the user pay for the system's validation assumptions. This is a near-absolute normative priority, illustrated by first-hand failures, not a measured data-loss prevalence.
- **State**: maintain continuity across visits and devices so users can resume instead of reconstructing their task. The page also proposes using browsing history to anticipate interests and says stored data should be safeguarded and its purpose disclosed. Saving task progress and profiling behavior are different interventions; usefulness of the former does not automatically justify the latter.

## Results / Admissions

### What research support is actually visible

The page names **Fitts's law** and links to Tognazzini's own [Fitts quiz](https://asktog.com/columns/022DesignedToGiveFitts.html), but does not provide the original paper, test samples, coefficients, or uncertainty for its numerical applications. It claims **20–30%** slowdown from a one-pixel nonclickable screen-edge boundary and roughly **fivefold** faster Macintosh than Windows menu acquisition, saying tests confirmed the predictions. These are reported claims without inspectable study protocols here, not portable effect sizes for all menus or devices.

Two further studies are mentioned without full citations:

- An unnamed study found people in a hazardous interface made no more mistakes but worked substantially more slowly than in a supportive, visually clear environment. No participants, tasks, statistics, or magnitudes are supplied.
- An NN/g ecommerce study reportedly found that easier cart removal made users more willing to add items without increasing the deletion rate, so they bought more. No sample, site set, randomization, effect size, or link to the study is given. This supports an interesting hypothesis about reversible commitment, not a quantified causal prediction of revenue.

The HyperCard anecdote reports that users understood a layered structure immediately from Kristee Kreitman's diagram where **20 pages** of prose had failed. It is first-hand testing experience, with no participant count or controlled comparison. The dish-aiming example records a redesign Tognazzini recommended; the map and augmented view plausibly expose the conceptual advantage but provide no before/after installation outcomes. The Graphite-versus-other-CAD comparison is an invitation and assertion, not an experiment.

### The latency chart is guidance, not a study

The figure prescribes escalating feedback as waits grow: a busy indication at **0.5–2 seconds**, a possible wait duration beyond **2 seconds**, animated progress beyond **5 seconds**, continued information and occupation beyond **10 seconds**, and strong completion cues beyond **15 seconds**. The prose separately recommends acknowledging input within **50 milliseconds**. These are the author's guidelines; the page supplies no latency experiment establishing these exact boundaries.

The chart's insistence that work must end when progress reaches completion has a stronger general rationale than any exact cutoff: feedback must describe actual state, not merely display reassuring activity. The autonomy section's misleading software-update estimate illustrates the same principle.

The invisible-scrollbar calculation assumes an extra second for ten daily uses by 66 million people to claim **21 person-years per day** lost. Its arithmetic dramatizes cumulative cost, but the added second and population exposure are assumptions, not a measured aggregate productivity loss.

## Analyst Takeaways

1. **Measure simplicity in task effort, not empty pixels.** A sparse screen that adds searching, remembering, or workarounds can be operationally complex. Preserve perceivable access to what people need now.
2. **Protect procedural memory more than ornamental sameness.** Keep learned commands stable; deliberately mark changed behavior. Looking identical while behaving differently can be worse than an obvious redesign.
3. **Make recovery an efficiency mechanism.** Undo, exits, and preserved state support exploration and fluent action. Error prevention and error recovery should reduce the cost of mistakes without demanding perfect users.
4. **Do not turn practitioner numbers into universal limits.** Use the movement and latency models to generate testable expectations; specific menu ratios, feedback times, and sales effects need task-appropriate evidence.
5. **Evaluate both initial and sustained use.** Success in a brief first-use test cannot stand in for weeks of routine efficiency or the burden of relearning after an update.
6. **Separate continuity from surveillance.** Preserving a draft solves a concrete user problem. Inferring interests from movement history adds privacy and interpretation questions not resolved by the state principle's broad endorsement.

## Questions and Limitations

- The source mixes normative priorities, anecdotes, named theory, and uncited research without a bibliography or clear evidence grading. Strong rhetoric is not a substitute for sample sizes and controlled comparisons.
- “Any attempt to hide complexity” increasing it is too absolute even within the page: progressive revelation and mobile hiding are explicitly endorsed under conditions. The more defensible distinction is **postponing unneeded complexity versus concealing needed action**.
- Its opposition to controls inside desktop content areas must be read alongside its recommendation for task overlays. The useful boundary is obstruction and loss of orientation, not an unconditional ban on layering.
- Universal wording that principles do not change across platforms sits alongside platform-specific exceptions, changing latency expectations, and different learning priorities. The model is more durable than its literal implementation rules.
- The proposed eye-tracking method for avoiding accidental link activation is explicitly speculative: looking at a link is assumed to prove intent. No study or performance results are supplied; the declaration putting that invention in the public domain does not make the article public domain.
- Readability advice acknowledges that antialiasing can sharpen rather than simply blur edges. Claims about font appearance, word shapes, and age-related vision need device- and population-specific testing; this page is not a contrast or disability-conformance standard.
- Product examples, claims that every user knows search, and assumptions about a skilled household member should not be universalized. The framework advocates user testing but cannot guarantee that every error it describes would necessarily be eliminated by testing.
- The paragraph before copyright loosely describes unlimited nonpaid copying, but the actual notice requires permission for republication on a website. Personal, educational, training, and evaluation-team copy exceptions are not a blanket public-repository license.

## Vault Ideas Extracted

- [Signifier Strength](/vault/signifier-strength.md) — Argues that perceivable access and explicit gesture cues matter more than a visually empty impression of simplicity.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Prioritizes learned behavior and expected consequences over uniform appearance; changed behavior should be visibly distinguishable.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Links reversibility and preserved work to exploration, confidence, and sustained human productivity, with clear limits on the uncited evidence.
- [Response-Time Thresholds](/vault/response-time-thresholds.md) — Contributes explicitly practitioner-prescribed escalating wait feedback, distinct from experimentally validated universal time boundaries.
