---
type: Study Note
title: Understanding WCAG 2.2
description: WCAG 2.2's informative commentary explains accessibility as preserving perception, operation, comprehension, and assistive-technology access, while admitting that testable conformance thresholds and exceptions do not guarantee usability for every disabled person.
resource: https://www.w3.org/WAI/WCAG22/Understanding/
source: /archive/understanding-wcag-2-2/index.html
tags: [accessibility-standards, accessibility, digital-interfaces, motor-accessibility, low-vision, cognitive-accessibility]
timestamp: 2026-10-11T23:52:54Z
---

# Understanding WCAG 2.2 — Study Notes

**Authors**: W3C Accessibility Guidelines Working Group (AG WG), with named participants and contributors acknowledged in the About document.  
**Published**: Continuously maintained supporting documentation for WCAG **2.2**; the saved index says “Updated 11 February 2026.” Snapshot saved **11 October 2026**.  
**Status**: Informative W3C Group Note material, not the normative WCAG Recommendation. Read the saved index and all **108 supporting HTML pages**, including introductory/conformance material and every success criterion's Intent and Benefits where present; these are not 108 success criteria. The Parsing page preserves historical explanation after its removal.  

## What It Is

An explanation of **why particular interface properties are accessibility requirements**, not a cookbook or a new empirical evaluation. [Understanding WCAG 2.2](https://www.w3.org/WAI/WCAG22/Understanding/) connects each criterion's wording to the barrier it removes, the people who benefit, examples, and possible techniques. Its strongest design contribution is the distinction between an experience's apparent usability and its ability to survive different sensory modalities, input capabilities, reading strategies, and assistive technologies.

The normative requirements live in [WCAG 2.2](https://www.w3.org/TR/WCAG22/). Understanding documents, techniques, and ACT test rules are **informative**. A sufficient technique is an accepted route to a requirement when correctly applied and accessibility-supported, not a mandatory implementation. Advisory techniques can be essential to particular users even though they do not determine the conformance level. Passing a partial automated test means no corresponding failure was detected; it does not establish the whole criterion or whole experience is accessible.

## Problem and Motivation

A design that assumes sight, precise pointing, uninterrupted attention, quick reading, and intact working memory can exclude users while remaining straightforward for its designer. The commentary treats those assumptions as separate failure modes. Blind users may receive content serially rather than spatially; magnification reduces visible context; tremor makes small crowded controls dangerous; dyslexia, memory difficulties, and executive-function limitations make repeated entry or authentication challenges prohibitive; deaf-blind users may need textual material rendered in braille.

The recurring answer is **preserve the information and achievable outcome while allowing the presentation and operation to vary**. Electronic text, meaningful relationships, understandable names, and controllable timing let user agents adapt content. Directly accessible defaults still matter: the possibility of an alternative does not excuse a control that cannot be discovered or a flashing region that prevents use of the rest of the page.

## Principles as Ideas

### POUR is a layered contract, not four checklist labels

The [introduction](https://www.w3.org/WAI/WCAG22/Understanding/intro.html) organizes **13 guidelines** beneath four principles:

- **Perceivable**: information and controls can be presented through senses the user can use.
- **Operable**: interaction cannot depend exclusively on actions the user cannot perform.
- **Understandable**: content and interface behavior must be comprehensible and predictable.
- **Robust**: content remains interpretable by different user agents, especially assistive technologies, as technology changes.

Guidelines state broad goals; **technology-neutral, testable success criteria** state pass/fail conditions. Level **A** is the minimum; **AA includes A and AA**; **AAA includes all three**. The levels are not severity scores. Their assignment also considers available workarounds, authoring feasibility, interpretation, and limits on function or aesthetics. An AAA failure can be decisive for an individual user.

[Conformance](https://www.w3.org/WAI/WCAG22/Understanding/conformance.html) applies to **full pages and complete processes**, including responsive variations, not an accessible fragment beside an inaccessible checkout. Reliance must be on accessibility-supported uses of technology, and other content must not interfere. A conforming alternate version must preserve information, functionality, language, currency, and discoverability; making the original directly accessible is preferred. Partial conformance due to uncontrolled third-party content is explicitly a statement of **non-conformance**, not a lesser badge of success.

### What WCAG 2.2 adds

The nine new criteria sharpen barriers in common interactions:

| Level | New success criteria |
|---|---|
| A | **3.2.6 Consistent Help**; **3.3.7 Redundant Entry** |
| AA | **2.4.11 Focus Not Obscured (Minimum)**; **2.5.7 Dragging Movements**; **2.5.8 Target Size (Minimum)**; **3.3.8 Accessible Authentication (Minimum)** |
| AAA | **2.4.12 Focus Not Obscured (Enhanced)**; **2.4.13 Focus Appearance**; **3.3.9 Accessible Authentication (Enhanced)** |

**4.1.1 Parsing is obsolete and removed**, not a current 2.2 requirement. Its [historical explanation](https://www.w3.org/WAI/WCAG22/Understanding/parsing.html) says browser error handling improved and assistive technologies now rely on browser parsing rather than parsing markup themselves. Accessibility consequences still matter under criteria such as Info and Relationships and Name, Role, Value. Removing an obsolete proxy does not remove the obligation to expose usable semantics.

### Contrast: make necessary information distinguishable

[1.4.3 Contrast (Minimum), AA](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) requires **4.5:1** for ordinary text and **3:1** for large text; large means **18 point**, or **14 point bold**. The rationale is luminance difference rather than a particular hue pairing: visual-acuity loss, aging, and color deficiencies can reduce effective legibility. Placeholder and interaction-revealed text are still text. Decorative/incidental text, inactive controls, and logos have exceptions, but corporate colors do not generally exempt ordinary interface copy.

[1.4.11 Non-text Contrast, AA](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html) extends **3:1 against adjacent colors** to the visual information necessary to identify controls, states, and meaningful graphical objects. It does **not** require every decorative stroke or every control boundary to contrast. A text-labelled button may be identifiable without a border; a checkbox's selected-state mark still needs to be discernible. A chart can expose its information through a conforming alternative rather than requiring every slice to do all the explanatory work. The illustrated pie charts and gradient examples make the distinction concrete: ask whether the information remains understandable when low-contrast portions are effectively invisible.

Contrast, visible differentiation, and semantics are separate. A sufficiently contrasting hidden accessible name does not supply a visible non-color cue to a sighted color-blind user. Conversely, a visible shape or label does not automatically expose its meaning to assistive technology.

### Typography and layout: support adaptation without erasing content

[1.4.4 Resize Text, AA](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html) protects enlargement to **200%** without loss of content or functionality, without requiring assistive technology. The intent includes text in controls and labels. [1.4.10 Reflow, AA](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html) protects reading without back-and-forth two-dimensional scrolling at **320 CSS pixels wide** for vertically scrolling content, or **256 CSS pixels high** for horizontally scrolling content. The familiar **400%** illustration derives from a 1280-by-1024 starting viewport; viewport dimensions, not a particular monitor or zoom percentage, are the criterion's operative measure.

Reflow is not “stack everything.” Maps, tables, certain editing interfaces, and other inherently two-dimensional content have exceptions. Those exceptions do not automatically cover surrounding headings, search, pagination, comments, or individual text cells. The figures distinguish a table legitimately scrolling from unrelated prose unnecessarily extending off-screen. Hiding navigation behind a discoverable control preserves functionality; simply dropping it does not.

[1.4.12 Text Spacing, AA](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html) protects users' ability to override spacing without clipping, overlap, or lost function. Its test values are **1.5 times font size for line height**, **2 times for paragraph spacing**, **0.12 times for letter spacing**, and **0.16 times for word spacing**. These are **adaptation tolerances, not required default typography** or universally optimal reading settings. Inapplicable properties in particular languages/scripts are excepted. The source's failure images show why a neatly fitted heading is not robust if a user's preferred spacing cuts off its last words.

### Alternatives: preserve purpose, not merely a picture's appearance

[1.1.1 Non-text Content, A](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html) uses text as a presentation-neutral intermediary: speech, braille, visual restyling, and other representations can expose the same purpose or information. Controls need an alternative expressing their **function**; charts may need fuller equivalents; decorative material should not add noise to the assistive-technology experience. A filename or generic “image” is not an informational alternative.

Media criteria add distinctions that text alternatives alone cannot resolve: captions include meaningful sounds and speaker identity, audio description supplies important visual action, and full textual media alternatives can support deaf-blind users. Text is not automatically a substitute for sign language, nor can a short title stand in for the information in a complex diagram. Semantically exposing relationships and a meaningful reading sequence preserves what layout communicates when the content is presented serially.

### Targets and dragging: reduce precision demands, not only pointer travel

[2.5.8 Target Size (Minimum), AA](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html) requires **24 × 24 CSS pixels**, with spacing, equivalent-control, inline, user-agent, and essential exceptions. This is the **active target**, not merely its visible icon. For an undersized target, a **24 CSS pixel diameter circle centred on its bounding box** must not intersect another target or another undersized target's circle. The diagrams show why a small button beside a large target needs clearance too; the exception is not just a fixed gap between equally sized icons. A rounded 24-pixel-diameter target cannot necessarily contain the required 24-pixel square and may therefore need the spacing exception.

The rationale is missed/accidental activation for tremor, spasticity, limited dexterity, less precise alternative pointers, and touch input. [2.5.5 Target Size (Enhanced), AAA](https://www.w3.org/WAI/WCAG22/Understanding/target-size-enhanced.html) sets **44 × 44 CSS pixels**, with equivalent, inline, user-agent, and essential exceptions—not the AA spacing exception. It recommends still larger targets for frequent actions, difficult reach, sequential tasks, and actions that are hard to undo. The AA document explicitly admits that **very small, difficult-to-activate targets can pass** if sufficiently isolated. A compliance floor is not a target-acquisition optimum.

[2.5.7 Dragging Movements, AA](https://www.w3.org/WAI/WCAG22/Understanding/dragging-movements.html) requires an equivalent **single-pointer operation without dragging**, unless essential or user-agent-controlled. Holding contact while repositioning and releasing imposes dexterity demands that clicking a destination does not. **Keyboard equivalence alone is insufficient** for pointer-dependent users. This is distinct from 2.5.1's multipoint/path-based gesture restriction: an unconstrained drag can fail the new criterion even if its precise path does not matter.

### Focus: existence, clearance, and discernibility are different requirements

[2.4.7 Focus Visible, AA](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html) makes the current keyboard interaction point perceivable and not time-limited. [2.4.11, AA](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-minimum.html) prevents author-created content from **entirely hiding the focused component**; [2.4.12, AAA](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-enhanced.html) protects **every part**. Sticky banners and non-modal overlays are therefore interaction constraints, not just layout decoration. The criteria assess the component, not an external focus outline; a fully hidden outline can separately fail Focus Visible. User-moved and user-opened content have specific qualifications, not a blanket exemption for any overlay a user encounters.

[2.4.13 Focus Appearance, AAA](https://www.w3.org/WAI/WCAG22/Understanding/focus-appearance.html) requires a qualifying indicator area at least equivalent to a **2 CSS pixel thick perimeter**, with **3:1 contrast between the same pixels in focused and unfocused states**. It permits shapes other than an outline and has user-agent exceptions. The figures show two independent tests: an indicator can pass change-of-state contrast yet fail adjacent-color contrast under 1.4.11, or pass adjacent contrast yet change too little to pass Focus Appearance. Sighted keyboard users, low-vision users, and users with attention or memory limitations need both a discernible state and enough context to know where action will occur.

### Predictability and memory: conserve effort for the task

[3.2.3 Consistent Navigation, AA](https://www.w3.org/WAI/WCAG22/Understanding/consistent-navigation.html) preserves repeated navigation's relative order, benefiting spatial memory, serial screen-reader navigation, and magnified views. [3.2.4 Consistent Identification, AA](https://www.w3.org/WAI/WCAG22/Understanding/consistent-identification.html) lets people reuse knowledge of repeated functionality; **consistent need not mean identical** when context appropriately changes the wording.

[3.2.6 Consistent Help, A](https://www.w3.org/WAI/WCAG22/Understanding/consistent-help.html) keeps available help mechanisms in consistent relative order across a set of pages. It **does not require help to be offered**. The document admits that visually moving help while preserving serial order can pass yet be unhelpful. Its stronger recommendation is consistency both visually and programmatically, conserving energy for people experiencing cognitive fatigue or shutdown.

[3.3.7 Redundant Entry, A](https://www.w3.org/WAI/WCAG22/Understanding/redundant-entry.html) makes already supplied information auto-populated or available to select within the same process, subject to essential, security, and no-longer-valid exceptions. This addresses working-memory demand, fatigue, repeated motor effort, and preventable mistakes. Browser autofill alone does not discharge the content's obligation; a process can cross domains. The criterion does not require storage between sessions, and careless temporary storage can still create privacy harm.

[3.3.8 Accessible Authentication (Minimum), AA](https://www.w3.org/WAI/WCAG22/Understanding/accessible-authentication-minimum.html) avoids making unaided recall, transcription, or puzzle-solving prerequisites for authenticating existing users. Cognitive-function tests need an alternative or assistance, with exceptions for object recognition and user-provided non-text content. [3.3.9, AAA](https://www.w3.org/WAI/WCAG22/Understanding/accessible-authentication-enhanced.html) removes those two exceptions. All required authentication steps, including relevant recovery and multifactor steps, need a compliant path. The figures expose superficially harmless barriers: blocked paste, a code split into fields that accept only one pasted digit, and demands for particular password characters defeat assistance. An audio CAPTCHA still requiring transcription does not solve the cognitive barrier.

### Forms, timing, and motion: prevent avoidable failure and permit recovery

[3.3.2 Labels or Instructions, A](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions.html) tells users what input is expected, including optional fields, option meanings, and unusual formats. The source warns that too much instruction can be as harmful as too little. Visible guidance, descriptive wording, programmatic association, and an accessible name are complementary obligations, not interchangeable substitutes. **2.5.3 Label in Name** also connects visible wording to speech-input commands; mismatches create hidden commands and extra memory demand.

[3.3.1 Error Identification, A](https://www.w3.org/WAI/WCAG22/Understanding/error-identification.html) makes automatically detected input errors and affected items identifiable in text; silently returning a form or silently correcting a value is insufficient. [3.3.3 Error Suggestion, AA](https://www.w3.org/WAI/WCAG22/Understanding/error-suggestion.html) adds known correction guidance unless it jeopardizes security or purpose. [3.3.4 Error Prevention, AA](https://www.w3.org/WAI/WCAG22/Understanding/error-prevention-legal-financial-data.html) protects specified legal, financial, user-data, and test submissions through reversibility, checking with correction, or review/confirmation. It is not a demand to confirm every ordinary save. **3.3.6, AAA** extends safeguards to all information submissions. These provisions target both increased mistake risk and difficulty detecting or recovering from mistakes.

[2.2.1 Timing Adjustable, A](https://www.w3.org/WAI/WCAG22/Understanding/timing-adjustable.html) prefers removing time limits, then adjustable limits, then extensions; real-time, essential, and sufficiently long limits have exceptions. Its adjustment route uses **at least ten times the default**; its extension route allows **at least 20 seconds** to respond to a warning and extension **at least ten times**. **2.2.5 Re-authenticating, AAA** preserves work across re-authentication; **2.2.6 Timeouts, AAA** warns about inactivity causing data loss unless data is retained for **more than 20 hours**. Reading, interpreting, finding controls, and operating assistive technology consume time: speed is not a neutral prerequisite.

[2.2.2 Pause, Stop, Hide, A](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide.html) addresses automatically started motion/distraction and auto-updates; the **five-second** allowance for movement does not also exempt auto-updating information. [2.3.3 Animation from Interactions, AAA](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions.html) permits disabling non-essential interaction-triggered motion, including parallax, to prevent vestibular symptoms—not merely annoyance. **2.5.4 Motion Actuation, A** separately protects users unable to shake/tilt/gesture and users who accidentally trigger motion input. Seizure-triggering flashing is another hazard: a pause control may be too late to prevent it.

## Results / Admissions

This is consensus guidance supported unevenly by standards, clinical experience, cited studies, and reasoned examples—not an experiment establishing all thresholds as optimal.

- **Contrast has an explicit derivation.** The contrast pages cite ISO 9241-3 and ANSI/HFS 100-1988 for a **3:1** normal-vision baseline, and Arditi and Faye's **2004** letter-contrast/acuity work for approximately **1.5 times** contrast-sensitivity loss associated with **20/40** acuity: **3 × 1.5 = 4.5**. The **7:1** enhanced threshold analogously addresses approximately **20/80** acuity; Gittings and Fozard **1986** is cited for aging-related acuity. This rationale is not a new controlled test of modern interface reading. Thin/anti-aliased text can nominally pass yet appear faint; the source recommends exceeding minima or using stronger strokes.
- **Target-size evidence is directional, not a displayed derivation of 24.** The AA page links [Parhi, Karlson, and Bederson's one-handed thumb target-size study](https://doi.org/10.1145/1152215.1152260). It explains accuracy, spacing, and touch hit-selection heuristics, but does not report a sample, effect estimate, or calculation establishing **24 CSS pixels** as universally sufficient. The **44-pixel** enhanced page likewise motivates larger targets without presenting a threshold-validation experiment. Inline and essential exceptions balance acquisition with readable reflow and meaningful spatial data.
- **Reflow and resize thresholds are feasibility choices.** The reflow page calls **320 CSS pixels** a “reasonable minimum” aligned with common small mobile viewports when drafted; it links Wayne Dick's **2017** work on horizontal-scrolling overhead. The resize page calls **200%** a “reasonable accommodation” compatible with varied designs and older magnifiers. These are pragmatic boundaries, not a biological discontinuity at the next pixel or percentage point.
- **Spacing cites research but compresses it.** The [text-spacing research section](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html#resources) names [McLeish 2007](https://doi.org/10.1177/0264619607075995), Wayne Dick's translation/recommendation, and studies by Chung, Rello/Baeza-Yates, Sjoblom and colleagues, and Zorzi and colleagues. It describes tests from **0.04–0.25 em**, improving speed with flattening near **0.20 em**, and a layout check across roughly **480 languages/scripts**. That check is not participant evidence that every language benefits from these settings. The paragraph also says earlier null studies began at **0.5 em**, “Right at the flat point,” without reconciling that number with the preceding **0.20–0.25** discussion; do not treat it as a coherent numerical meta-analysis.
- **Timing has an admitted security/access tradeoff.** The **tenfold** range and **20-second** warning response allowance are attributed to clinical experience and other guidelines, without a cited trial or population estimate on that page. The document acknowledges some people still cannot respond and that indefinitely long unattended financial-terminal sessions create risk. **20 hours** was chosen as longer than a full waking day; **five seconds** of movement as enough to draw attention but short enough to wait out.
- **Exceptions preserve adoption, not universal inclusion.** The non-text-content page explicitly says all CAPTCHA types exclude some disabled users, but forbidding them could discourage sites from conforming; it consequently accepts multiple modalities and recommends going further. Authentication AA admits object-recognition exceptions do not fully support cognitive accessibility. Focus Not Obscured AA permits partial obstruction in recognition of complex responsive layouts. These are openly negotiated minima.

## Analyst Takeaways

1. **Treat the criterion as a boundary and its intent as the design model.** A tiny isolated target, displaced help link, or faint nominally contrasting glyph can pass a narrow test while undermining the reason the criterion exists.
2. **Design for equivalent outcomes across channels.** Semantic relationships, text alternatives, pointer alternatives, keyboard operation, and visible cues must agree. Repairing one channel does not automatically repair another.
3. **Evaluate complete journeys under adaptation.** Enlargement, spacing, overlays, authentication, and error recovery interact. A compliant component library cannot guarantee that a composed checkout, editing view, or login process remains usable.
4. **Spend user effort on the task, not on recovering context.** Predictable navigation/help, preserved entries, visible focus, and retained work reduce avoidable memory and motor costs before they become errors.
5. **Use higher-level and advisory provisions where the barrier is material.** AAA is not recommended as a blanket whole-site policy, but that is not permission to ignore vestibular safety, robust focus, or accessible authentication for people who need them.

## Questions and Limitations

- Conformance uses functional testing; the documents explicitly recommend qualitative review and usability testing with disabled users as well. Passing all applicable criteria does not establish usability for the full range of disabilities.
- W3C does not specify how many or exactly which assistive technologies constitute sufficient accessibility support. Actual support varies by version, environment, affordability, and language; claimed semantics and usable semantics can diverge.
- The authentication explanation assumes cross-device codes can reach the clipboard and excludes evaluating seamless transfer. That content-level boundary can leave a real end-to-end accessibility barrier outside the criterion's test.
- Informative explanation evolves independently of the stable success criteria. Historical Parsing text remains deliberately obsolete; the Compatible guideline still mentions poorly formed markup as a barrier. The enhanced focus page's failure list also discusses covering part of the focus indicator, whereas its Intent explicitly scopes obstruction assessment to the component. Read such examples against the normative criterion rather than turning every sentence into an additional requirement.
- The saved index has **no `rel="canonical"`**. The source identity uses the supplied W3C collection URL rather than claiming a canonical link was observed. Footer update dates and the snapshot date identify different things; the snapshot is not a publication date for each underlying study.
- **Redistribution evidence**: the saved footer reads, “Copyright © 2026 World Wide Web Consortium. W3C® liability, trademark and permissive license rules apply unless otherwise noted. See Permission to Use WAI Material.” Its “permissive license” links to <https://www.w3.org/copyright/software-license/>, resolving to the [2023 Software and Document license](https://www.w3.org/copyright/software-license-2023/). That license states: “Permission to copy, modify, and distribute this work, with or without modification, for any purpose and without fee or royalty is hereby granted, provided that you include the following on ALL copies of the work or portions thereof, including modifications:”. Conditions include the full notice, existing intellectual-property notices/disclaimers, and notice of modifications. The public archive reference is justified by this explicit grant; redistribution must retain the applicable notices.

## Vault Ideas Extracted

- [Minimum Target Size](/vault/minimum-target-size.md) — Distinguishes active target geometry from appearance, AA spacing exceptions from AAA size, and compliance minima from easy acquisition.
- [Color Contrast Minimum](/vault/color-contrast-minimum.md) — Grounds luminance thresholds in the source's cited rationale while separating text, necessary graphics, adjacent contrast, and actual legibility.
- [Text Alternatives](/vault/text-alternatives.md) — Treats electronic text as a modality-neutral representation of purpose and information, with decorative and sensory-experience qualifications.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Connects identification, actionable correction, reversibility/review, and preserving work to unequal error and recovery costs.
- [Status Announcements](/vault/status-announcements.md) — SC 4.1.3 Status Messages commentary (read in the archived source; not summarized in the sections above) supplies the scope of programmatically determinable status, the context-equivalence rationale, and the polite-versus-urgent boundary.
- [Accessible Reordering](/vault/accessible-reordering.md) — SC 2.5.7 Dragging Movements commentary (read in the archived source; not summarized in the sections above) supplies single-pointer alternatives independent of keyboard access, essential/user-agent exceptions, and selection-revealed movement buttons and destination menus.
