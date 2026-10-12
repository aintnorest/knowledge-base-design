---
type: Study Note
title: "Cognitive Dimensions of Information Artefacts: a Tutorial"
description: Cognitive dimensions expose activity-dependent tradeoffs in information artefacts, but the framework is a discussion vocabulary rather than a validated overall usability score.
resource: https://www.cl.cam.ac.uk/~afb21/CognitiveDimensions/CDtutorial.pdf
source: https://www.cl.cam.ac.uk/~afb21/CognitiveDimensions/CDtutorial.pdf
tags: [usability-evaluation, cognitive-load, digital-interfaces, interaction-design, design-process, taxonomy]
timestamp: 2026-10-11T23:52:03Z
---

# Cognitive Dimensions — Study Notes

**Authors**: Thomas R. G. Green and Alan F. Blackwell.  
**Published**: October 1998; version 1.2, 75 pages; originally prepared for the BCS HCI 1998 conference.  
**Status**: Practitioner tutorial and framework exposition, not a controlled validation study. The complete version 1.2 PDF was read, including the comparative diagrams, worked applications, practice examples, and bibliography. The title page states “Copyright © T. R. G. Green and A. F. Blackwell, 1998”; no explicit redistribution grant was found.  

## What It Is

A vocabulary for discussing the cognitive consequences of an information artefact's structure. Instead of hunting isolated interface defects or producing a single difficulty score, the analyst describes a **profile of dimensions**, interprets it against the intended activity, and considers the costs of changing it. The framework applies to software and embedded controls, but also to paper timetables, programming notations, diagrams, and other non-interactive representations.

Its central contribution is not a checklist of universally desirable attributes. It is the recognition that **a design improvement is often an exchange of burdens**: less repetitive editing may require more abstraction; explicit dependencies may consume more space and create more layout work; more expressive annotation may become more work to maintain.

## Problem and Motivation

Usability is partly determined beneath the surface of a screen. An attractive editor can still make a conceptual change require dozens of operations, force decisions before necessary information exists, or conceal the consequences of editing a shared definition. The tutorial argues that fine-grained task models are expensive and that surface-oriented evaluation can overlook these structural problems. Its contrasts with other methods are advocacy, not comparative effectiveness results.

Names such as *viscosity* and *premature commitment* make half-articulated problems discussable across disciplines. The authors explicitly call the dimensions **“discussion tools, not deep analyses”**. They are intended to complement, not replace, task analysis, empirical evaluation, or other usability methods.

## Mechanism as an Idea

### Evaluate the system, not the notation alone

An artefact comprises a **notation** (perceived marks or commands), an **environment** (operations for manipulating them), and a **medium** (persistent or transient). Numbered references need not be viscous if the environment maintains them automatically. The same options may impose different demands when spoken sequentially versus presented persistently on paper.

Layers and sub-devices matter. Editing a program and executing editor commands are different layers. A style or macro manager is a sub-device with its own visibility, dependencies, and change costs. A low-barrier main experience can hide a difficult abstraction-management experience.

### Dimensions and their cognitive consequences

- **Viscosity**: resistance to a goal-level change. *Repetition viscosity* means one conceptual change requires many separate actions; *knock-on viscosity* means further changes are needed to restore consistency. Assess meaningful restructuring, not just whether individual keystrokes are easy. High viscosity interrupts exploration and makes people preserve inadequate structures; the authors also argue that it can encourage deliberation or inhibit disastrous slips in appropriate settings.
- **Hidden dependencies**: consequential relationships are not fully visible. Dependencies may be one-way, local rather than exposing a chain, or absent from the normal view. Search cost grows with trail length, branching, and effort per link. A shared style saves editing but can conceal which instances or descendants it will affect.
- **Premature commitment and enforced lookahead**: order constraints demand a decision before its relevant information is available, or require costly advance planning. The signwriter who runs out of board and the diagram editor that cannot record a relationship before both endpoints exist share the same structural problem. Low viscosity makes a bad early guess cheaper to repair; deconstraining order attacks the cause.
- **Abstraction mechanisms**: grouping entities or defining new terms changes the notation and can reduce repetition. The tutorial develops what is often discussed as the *abstraction gradient* through **abstraction barrier** (what must be understood before useful work), **abstraction hunger** (whether user-defined abstractions are required), and management costs. Abstraction-hating systems forbid definitions; tolerant systems permit them; hungry systems require them. Persistent definitions, transient selections, and exemplars with automatic, optional, or no updating have different consequences.
- **Secondary notation**: information outside the official syntax. *Redundant recoding* makes existing structure easier to read through layout, grouping, or emphasis; *escape from formalism* adds rationale, doubt, history, or intention. The paper diary's cancellations, handwriting, and scars carry information missing from an otherwise equivalent electronic record. Annotation can itself become stale when the underlying structure changes.
- **Visibility and juxtaposability**: components must be accessible, and related components must be viewable together. Sequential access is not equivalent to comparison. Without juxtaposition, users repeatedly revisit material, rely on working memory, or leave the environment for an external copy.
- **Closeness of mapping**: the representation fits the task domain rather than demanding translation into unrelated concepts.
- **Consistency**: similar meanings use similar syntactic forms. Primarily a learnability concern here, but inconsistent dialogs also invite action errors.
- **Diffuseness**: verbosity of the notation. Excess verbosity occupies space and memory; excessive terseness may increase confusability and errors.
- **Error-proneness**: the notation invites mistakes through poor discriminability, weak checking, inconsistent dialogs, or memory overload.
- **Hard mental operations**: substantial cognitive work, such as tracking branching paths through a dependency structure.
- **Progressive evaluation**: unfinished work can be checked during construction, particularly valuable to learners and interrupted or stressed users.
- **Provisionality**: tentative marks or actions can express incompletely settled ideas; this reduces premature commitment rather than requiring a fully specified end state.
- **Role-expressiveness**: a component's purpose and relationships are readily inferred. The authors admit this is difficult to clarify and insufficiently researched.

### Activities determine the useful profile

**Incrementation** adds information without restructuring; **transcription** copies known content into a representation; **modification** changes an existing structure; **exploratory design** combines adding and changing while the desired end state is still unknown. These are idealized activities, not permanent classes of user or product. A form intended for transcription may actually be completed opportunistically from scattered material.

Viscosity may be tolerable for uncomplicated transcription or incrementation, but is harmful to modification and exploration. Hidden dependencies are especially problematic when modifying someone else's structure; the authors argue that small exploratory tasks may tolerate them to preserve fluidity. Abstractions are useful when a reusable structure is known, but mandatory definitions impose setup and lookahead during exploration. Visibility, juxtaposition, and interpretation of partially completed work become particularly important when revising or discovering a solution.

The tutorial calls dimensions conceptually independent but **pairwise independent in redesign**: changing one while holding another fixed may force a third to move. Its physics analogy is a model for discussing compromise, not an experimentally established conservation law. Figure 20 explicitly does not enumerate all tradeoffs or promise that every exchange is available in every system.

## Results / Admissions

**Illustrative editing comparison, pp. 55–56**: Green and Petre's earlier analysis supplied the same rocket-flight program in Basic, LabView, and Prograph. An experienced user transcribed a precomputed air-resistance modification from a printout, separating edit execution from solving the physics problem. Reported times were **508.3 seconds in LabView, 193.6 in Prograph, and 63.3 in Basic**, approximately **8:1** between extremes. Diagram rearrangement and rewiring accounted for the visual systems' burden; Prograph reduced local rearrangement by distributing code into more windows, trading viscosity against visibility and juxtaposition.

The authors call this a **“straw-test”**. The tutorial supplies no participant sample beyond the experienced-user description, repeated-trial distribution, inferential statistics, or effect-size estimate. These exact times are evidence about those versions, that representation, and that change—not a replicated claim that textual programming is eight times faster than visual programming. The authors explicitly recommend both visual languages for appropriate purposes.

Other support is qualitative and illustrative: a diary analysis reveals easy event addition but poor bulk schedule modification; a survey respondent reports hiring someone to tidy visual-program layouts; Payne's calendar research motivates secondary notation. Toy paired examples isolate tradeoffs for discussion, not controlled outcome measurements. The bibliography describes interviews and observations with **128 academics** in a separate idea-sketch study, but does not provide its full methods or estimates.

The authors acknowledge **very little research on tradeoff relationships**, difficult metrication, and vagueness in definitions. They discuss domain-specific benchmarks and formal models as developments, not a completed universal measurement system. A later [Britton and Kutar cautionary analysis](https://ppig.org/files/2001-PPIG-13th-britton.pdf) found that restricting profiles to selected dimensions could overlook diffuseness and error-proneness changes in specification notations. That is a methodological extension/caution, not a replication of the rocket-editing times.

## Analyst Takeaways

1. **Evaluate the next change, not only the first successful creation.** Ingestion, form completion, or initial diagram construction can look excellent while recategorization, reuse, and correction remain prohibitively expensive.
2. **Name both sides of a remedy.** A reusable definition is not free simplification: it reduces repetition while introducing scope decisions, learning, dependencies, and maintenance.
3. **Diagnose early commitment together with reversal cost.** Premature guesses are especially damaging when correcting them is viscous. A reversible provisional representation can be more useful than a supposedly natural forced sequence.
4. **Preserve comparison and informal meaning.** A notation's formal content is not the whole information people need. Side-by-side views, rationale, uncertainty, and traces of previous edits support interpretation and continued work.
5. **Use the profile to generate hypotheses, not numerical authority.** The framework improves the questions an evaluation asks; actual users and consequential tasks must establish which tradeoffs matter and how much.

## Questions and Limitations

- Physical performance, aesthetics, emotion, and context-of-use are deliberately outside the framework. An adequate cognitive profile does not establish accessibility, safety, or overall experience quality.
- The tutorial repeatedly refers to **13** dimensions, but its full-set list on p. 11 contains **14 named entries**. It also states that the list is neither guaranteed complete nor fixed. Treat the terms as a vocabulary, not a settled factor model.
- There is a substantive internal inconsistency: p. 29 says secondary notation is highly relevant to exploratory work, while its local table says “harmful ?” and Figure 19 on p. 42 says “v. harmful” for exploration. The prose and examples support its interpretive value while acknowledging maintenance costs; the unexplained table cell should not become a rule against exploratory annotation.
- The diary discussion first says defaults eliminate the initial abstraction barrier (p. 50), then says users cannot completely ignore categories and sets and therefore face a real barrier (p. 51). Different sub-devices partly explain the shift, but the scope needs to be stated before assigning a profile.
- Historical product limitations are not claims about present versions. The reusable lesson is the structural tradeoff, not a permanent judgment of a named editor.

## Vault Ideas Extracted

- [Cognitive Dimensions Tradeoffs](/vault/cognitive-dimensions-tradeoffs.md) — Activity-sensitive profiles and explicit costs of redesign, including the framework's evidential and internal-consistency limits; premature commitment compounded by viscosity, provisionality as the remedy, and secondary notation's interpretive value and maintenance cost.
- [Juxtaposability for Comparison](/vault/juxtaposability-for-comparison.md) — Side-by-side access supports consistency checks and analogical problem solving without repeated memory-dependent switching.
