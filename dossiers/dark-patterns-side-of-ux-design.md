---
type: Study Note
title: The Dark (Patterns) Side of UX Design
description: A qualitative analysis of 118 practitioner-circulated artifacts reorganizes dark patterns into five design strategies and frames them as conflicts between user and shareholder value, without measuring prevalence, designer intent, or behavioral effects.
resource: https://doi.org/10.1145/3173574.3174108
source: https://doi.org/10.1145/3173574.3174108
tags: [deceptive-patterns, design-process, digital-interfaces, interaction-design, taxonomy]
timestamp: 2026-10-11T23:50:47Z
---

# The Dark (Patterns) Side of UX Design — Study Notes

**Authors**: Colin M. Gray, Yubo Kou, Bryan Battles, Joseph Hoggatt, and Austin L. Toombs.  
**Published**: CHI 2018, April 21–26, Montréal, Canada; Paper 534, 14 pages.  
**Status**: Peer-reviewed CHI paper read in its proceedings-formatted PDF, carrying doi:10.1145/3173574.3174108. This is a practice-led qualitative taxonomy and ethical argument, not an experiment or a representative interface census.  

## What It Is

An attempt to turn practitioners' “dark patterns” discourse into a more coherent vocabulary for ethical judgment. The authors analyze **118 artifacts** and derive **five strategies**: nagging, obstruction, sneaking, interface interference, and forced action. Their central shift is from naming isolated interface tricks to describing the strategy that privileges shareholder value over the person's goals.

The work does not establish that every use of these strategies is equally harmful, malicious, or unlawful. It explicitly rejects treating the taxonomy as a mechanical ethical checklist. Its value is in making tradeoffs discussable where ordinary usability or conversion measures can obscure them.

## Problem and Motivation

Academic HCI had developed value-sensitive, reflective, critical, and persuasive design approaches, but the authors find their uptake in everyday UX practice unclear. Meanwhile practitioners were already sharing concrete examples of manipulation. A practice-led approach starts from this existing ethical vocabulary instead of assuming that a scholarly method has become a usable professional norm.

Brignull's influential categories mixed **context, strategy, and outcome**: disguised advertising names a content type, while misdirection names an influence strategy. That mixture makes comparison awkward and can leave broader ethical concerns compressed into a single accusation of “darkness.” The authors seek a strategy-level language that connects observed interactions with values, responsibility, and the organizational constraints of design work.

## Mechanism as an Idea

### Five strategies

| Strategy | What it changes for the person | Examples and included concepts |
|---|---|---|
| **Nagging** | Redirects expected activity through intrusions that persist over one or more interactions. | Prompts that offer “Not Now” without permanent refusal; repeated pressure to enable notifications or continue working. |
| **Obstruction** | Makes a process harder than it needs to be, discouraging a particular action. | Difficult cancellation, blocked copying that inhibits comparison, obscure settings, and intermediate currency that distances spending from its real-money value. |
| **Sneaking** | Hides, disguises, or delays information relevant to a decision. | Undisclosed recurring charges, late costs, unwanted basket additions, and an apparently familiar action that produces an unexpected result. |
| **Interface interference** | Privileges particular actions through presentation or interaction, limiting discoverability or confusing interpretation. | Hidden information, preselection, and aesthetic manipulation, including emotional pressure, false hierarchy, disguised ads, and trick questions. |
| **Forced action** | Requires an additional action to access or continue accessing functionality. | Unwanted updates, required disclosure, social recruitment, or repeated activity required to earn access. |

**Interface interference is broader than visual styling.** Its hidden-information subtype makes relevant options seem irrelevant or hard to discover; preselection lets an unchosen default stand in for consent; aesthetic manipulation changes perceived hierarchy, content type, emotional stakes, or urgency. A gray but clickable alternative can communicate “unavailable” despite being technically operable. The relevant distinction is between actionability and what the interface leads a person to believe about it.

The figures make these combinations visible. Figure 2 shows a notification prompt without a permanent decline. Figure 3 traces an obscure route to tracking controls. Figure 5 combines a collapsed disclosure with a preselected information-sharing option. Figure 6 presents “express” installation as recommended while the available custom route looks disabled. Figure 7 limits restart/shutdown choices to update-bearing actions. These are historical exemplars, not claims about current product versions.

### Relation to Brignull's types

The authors retain Brignull's examples but nest them under strategies:

- **Obstruction** includes Roach Motel and Price Comparison Prevention, plus the authors' Intermediate Currency.
- **Sneaking** includes Forced Continuity, Hidden Costs, Sneak into Basket, and Bait and Switch.
- **Interface interference** includes Misdirection under aesthetic manipulation, Disguised Ad, and Trick Questions, with additional concepts such as preselection, hidden information, false hierarchy, and toying with emotion.
- **Forced action** includes Privacy Zuckering; Social Pyramid expands Friend Spam to broader social recruitment, and Gamification describes repeated activity as an access condition.
- **Nagging** provides a strategy not represented by a direct type in the Brignull list reproduced in Table 1.

This organization is not a guarantee of mutually exclusive codes. The same newsletter-unsubscription example appears under both **sneaking** and **forced action**: a privacy condition can be obscured and simultaneously mandatory. Likewise, a difficult-to-cancel subscription may use hidden information to support obstruction. Overlap is part of the ethical explanation, not necessarily a coding error.

## Results / Admissions

### Corpus and method

Two researchers collected artifacts over **two months**, one with a UX background and one with a computer-science background, meeting weekly with the research team to broaden searches and discuss findings. They searched engines, social platforms, practitioner sites and blogs, and news outlets; keywords expanded from “dark patterns” and hashtags to combinations of “unethical,” “evil,” or “manipulative” with design/interface terms. A bot collected tweets carrying the dark-patterns hashtag.

The **118-artifact** corpus comprised **45 social-media items, 40 practitioner-blog items, 19 news items, 10 examples from the researchers' daily product interactions, and four items from darkpatterns.org**. Artifacts included examples, articles, and resources; this is not necessarily 118 independent products or 118 unique interface instances. Researchers recorded sources, implicated products, visual depictions, and interpretive memos.

Analysis used **document analysis and the constant comparative method**. First, Brignull's types served as a priori codes. Overlap and nonparallel categories motivated a second open-coding pass over all exemplars, attending to interaction quality, context, and intended user groups. Emergent and axial coding produced the five-strategy hierarchy.

There were **no recruited users or interviewed designers**, no randomized tasks, no measured purchase or consent effects, and no population prevalence estimate. The paper reports no interrater-reliability statistic. “Strategic motivators” are interpretations of artifacts, not direct observations of the designers' motivations.

### Ethical framing

The authors argue that design inevitably persuades, so the dividing question is not whether behavior is influenced but **whose values and goals the influence serves, under what conditions, and with what responsibility**. Techniques recognizable in persuasive design can be redirected toward coercion. The taxonomy makes that redirection inspectable rather than declaring persuasion inherently wrong.

They connect the strategies to compromised action possibilities and expectations about outcomes: a person may misread what can be done, or perform a familiar action and receive an unexpected result. A usable, smooth path toward the organization's goal can therefore remain ethically poor. This is an interpretive argument supported by exemplars, not a controlled comparison showing that dark patterns improve usability.

Responsibility is also not reduced to an isolated designer's good intentions. Organizational pressure, economic priorities, and later appropriation affect outcomes. The authors emphasize **design character**—values embedded in a practitioner's judgment—and **situated, applied ethics**, including attention to harm after a design's audience or context changes. They call for ethics education, practice-led accounts of dilemmas, and value-centered methods responsive to practitioners' actual power and constraints. These are recommendations, not evaluated interventions.

## Analyst Takeaways

1. **A strategy taxonomy is a conversation aid, not a verdict engine.** It can surface forced consent, concealed consequences, or asymmetric effort while leaving intent, proportionality, and context to be investigated.
2. **Do not let successful task completion stand in for user benefit.** If the task is defined as the organization's desired conversion, an evaluation may never encounter the person's blocked alternative. Review refusal, exit, and information-seeking paths as distinct goals; this is an analyst implication of the argument, not an experimentally validated procedure from the paper.
3. **Separate inferred motivation from observable mechanism.** The artifact can show a hidden default or constrained exit. Establishing who intended what requires different evidence. Moral responsibility can still arise after harmful consequences become known.
4. **Read [Mathur et al.](/dossiers/dark-patterns-at-scale-shopping-websites.md) as complementary, not interchangeable.** Their seven shopping categories retain Sneaking, Obstruction, and Forced Action. Their Misdirection largely corresponds to Gray's Interface Interference; confirmshaming elaborates toying with emotion, and expensive defaults elaborate preselection. Urgency and Scarcity split out pressure that Gray discusses partly through aesthetic/emotional manipulation; Social Proof becomes its own influence family. Gray's Nagging has no dedicated Mathur category. This is an analyst crosswalk, not a validated equivalence between the two coding schemes.
5. **Distinguish strategies from attributes.** Gray describes what the design does to the interaction; Mathur's asymmetric, covert, deceptive, information-hiding, and restrictive dimensions describe how influence is organized. A single strategy can carry several attributes, and the same attribute can occur across strategies.

## Questions and Limitations

- A purposive corpus of publicly criticized artifacts favors salient, discussable failures. It cannot estimate how often a strategy appears, how representative submissions are, or how much harm it causes.
- The 2018 descriptions of operating systems, games, and websites can age. Preserve the mechanism, not an accusation about today's product. Figure screenshots show available choices and framing, not every downstream behavior claimed in the surrounding narratives.
- The broad definitions can absorb ordinary defaults, reminders, gamification, or necessary prerequisites. The authors qualify darkness by intent, motivation, user goals, and context, but provide no validated threshold for resolving borderline cases.
- There is a productive tension between organizing categories around potential designer motivations and admitting that intention may be benign, unknown, or transformed by later use. The paper's ethical vocabulary should not be mistaken for evidence of individual malice.
- Overlap between sneaking, hidden information, and forced action makes the hierarchy less clean than its summary diagram suggests. Multiple mechanisms may be the correct description of one interaction.
- No efficacy evidence is supplied for ethics training, design-character development, or practitioner adoption of the proposed vocabulary. Later work such as [Luguri and Strahilevitz's experiments](https://doi.org/10.1093/jla/laaa006) concerns behavioral outcomes; it does not validate this corpus's completeness or its interpretations of intent.
- The PDF's first page has **no Creative Commons grant**. It carries the following ACM notice, so the dossier cites the canonical DOI rather than a public archive path:

> Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than the author(s) must be honored. Abstracting with credit is permitted. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from permissions@acm.org.
>
> © 2018 Copyright held by the owner/author(s). Publication rights licensed to ACM.

## Vault Ideas Extracted

- [Deceptive Pattern Attributes](/vault/deceptive-pattern-attributes.md) — Supplies five interaction strategies and an ethical framing to complement the attribute model, distinguishing observable designs from inferred intent and organization-defined success from user benefit.
