# Tag Taxonomy

The controlled tag vocabulary for this knowledge base. Every `tags:` entry in
dossier and vault frontmatter must come from this file. Adding a tag requires
adding it here — with a one-line definition, in the same commit — so the
vocabulary grows deliberately instead of sprawling.

**This is a living document.** The tags below are a starting vocabulary chosen
before any source was ingested; some clusters will not materialize and others
will appear. Re-evaluate this taxonomy as ingests accumulate — roughly every
25–30 sources, or whenever tagging a new source feels forced. Promote a concept
to a tag when ~5 pages would genuinely carry it; demote a tag whose cluster
never materialized. Distinctive one-off concepts belong as vault pages, not
tags.

## Tagging Rules

- 3–6 tags per page, most central first.
- `digital-interfaces` goes on every page whose subject is a software or
  screen-based product, alongside its specifics. Omit it for findings about
  perception, visual design, or physical artifacts in general, even when the
  page mentions interface applications.
- `accessibility` goes on every page whose central question involves disabled
  people, alongside the specific accessibility tag.
- At most one genre tag (`survey`, `taxonomy`, `case-study`).
- Do not tag `study-note` or `synthesis` — the `type:` field already records
  this.
- Do not invent tags during ingest. If nothing fits, use the nearest broader
  tag and flag the gap in the ingest report as a candidate for this file.

## Umbrella

| Tag | Definition |
|---|---|
| `digital-interfaces` | Any page whose subject is a software or screen-based product — web, mobile, desktop, embedded, conversational. Marks where a finding was established on or applied to an interface; general perception, visual-design, and physical-design pages omit it. |

## Perception & Cognition

| Tag | Definition |
|---|---|
| `visual-perception` | How people see: contrast, acuity, grouping and Gestalt principles, figure–ground, visual search, peripheral vision. |
| `attention` | What people notice and ignore: salience, banner blindness, change blindness, interruption, eye-tracking findings. |
| `cognitive-load` | Mental effort a design demands: working-memory limits, complexity, chunking, recognition over recall. |
| `aesthetics` | Aesthetic response: what people find beautiful or appealing, first impressions, and the effect of appeal on perceived usability and trust. |
| `decision-making` | How people choose: heuristics and biases, choice architecture, defaults, choice overload. Contrast `behavior-change`, which designs toward a target behavior. |
| `human-performance` | Models and measures of human input performance: Fitts's law, Hick–Hyman law, pointing and steering, reaction time, error rates. |

## Visual Design

| Tag | Definition |
|---|---|
| `typography` | Type selection and setting: legibility and readability, measure, leading, hierarchy through type. |
| `color` | Color perception and use: palettes, contrast, color meaning and convention. Color-vision deficiency pages add `low-vision` and `accessibility`. |
| `layout` | Composition and arrangement: grids, spacing, alignment, density, responsive reflow. |
| `visual-hierarchy` | Directing the eye and ordering importance through size, weight, contrast, position, and grouping. |
| `iconography` | Icons, symbols, illustration, and imagery as communication: recognizability, labeling, cultural meaning. |
| `data-visualization` | Encoding data visually: chart choice, perceptual accuracy of encodings, dashboards, uncertainty display. |
| `brand` | Brand identity and expression: visual identity, voice, consistency across touchpoints, and its measured effects. |

## Interaction Design

| Tag | Definition |
|---|---|
| `interaction-design` | How people act on an interface and how it responds: affordances, signifiers, feedback, direct manipulation, modes, undo. |
| `information-architecture` | Organizing and labeling content: navigation, findability, categorization, site search, wayfinding. |
| `forms` | Data entry: input controls, field design, validation, error messages. |
| `motion` | Animation and transitions: timing, easing, continuity, motion as feedback. Vestibular-safety pages add `accessibility`. |
| `content-design` | Words in the interface: UX writing, microcopy, labels, plain language, voice and tone in product. |
| `mobile` | Touch and small-screen design: reach, gestures, target size, interrupted and on-the-go use. |
| `conversational-interfaces` | Voice and chat interaction: turn-taking, error repair, prompts and suggestions, persona. |
| `delegation` | Handing work to a system that acts on its own and staying responsible for it: what it may do unasked, when it should ask or wait, keeping the person informed, checking and correcting its output, calibrating trust, and taking back control when it fails. Applies whether the system is an AI agent, an assistant feature, or conventional automation. How the models or controllers work belongs in the intelligent-systems knowledge base. |

## Accessibility & Inclusion

| Tag | Definition |
|---|---|
| `accessibility` | Designing for disabled people: barriers, accommodations, and outcomes. Carried alongside the specific tag below. |
| `accessibility-standards` | WCAG and related standards and law (EN 301 549, Section 508, ADA case law): success criteria, conformance, and their rationale. Record the version. |
| `assistive-technology` | Screen readers, magnifiers, switch access, voice control, and how designs behave under them. |
| `low-vision` | Low vision and color-vision deficiency: contrast, magnification, reflow, non-color cues. |
| `motor-accessibility` | Limited dexterity, tremor, and alternative input: target size, keyboard-only use, timing, gesture alternatives. |
| `cognitive-accessibility` | Cognitive, learning, and neurological disabilities: predictability, memory demands, distraction, reading level. |
| `inclusive-design` | Designing for the range of human diversity beyond disability compliance: age, language, culture, and situational or temporary limitations. |

## Research & Evaluation

| Tag | Definition |
|---|---|
| `user-research` | Methods for understanding people and their needs: interviews, field studies, diary studies, surveys, synthesis. |
| `usability-evaluation` | Assessing whether a design works: usability testing, heuristic evaluation, cognitive walkthroughs. |
| `ux-metrics` | Measuring experience quantitatively: task success, time on task, standardized questionnaires, analytics, benchmarking. |
| `experimentation` | Controlled online experiments: A/B and multivariate tests, effect sizes, novelty effects, and their pitfalls. |

## Practice & Systems

| Tag | Definition |
|---|---|
| `design-systems` | Shared components, tokens, and patterns: their architecture, governance, adoption, and maintenance. |
| `design-process` | How design work is organized: discovery through delivery, critique, design thinking, collaboration with engineering and product. |
| `prototyping` | Representing designs before they are built: sketching, fidelity, exploring alternatives, testing prototypes. |

## Behavior & Ethics

| Tag | Definition |
|---|---|
| `behavior-change` | Designing toward a target behavior: persuasion, nudges, habit formation, gamification. Contrast `decision-making`, which covers how people choose. |
| `deceptive-patterns` | Interfaces that trick or pressure people against their interest: taxonomies, prevalence, harms, regulation. |
| `trust` | Credibility and trust: how design signals trustworthiness, and calibrated versus misplaced trust. |
| `privacy` | Privacy from the user's side: consent flows, permission prompts, data controls, and whether people understand them. |

## Genre

| Tag | Definition |
|---|---|
| `survey` | Genre tag — the source is a survey, systematic review, or meta-analysis. |
| `taxonomy` | Genre tag — the source's primary contribution is a classification scheme. |
| `case-study` | Genre tag — the source is a first-hand account of a specific product, team, or redesign and its outcome. |

## Watchlist

Candidate tags flagged during tagging because the existing vocabulary fit
poorly. Promote one when ~5 pages would genuinely carry it; prune entries that
stop accumulating evidence.

| Candidate | Evidence so far |
|---|---|
| — | No candidates yet. |

## Alias Map

Common synonyms for vocabulary tags. Do not use the left column; use the right
column.

| Alias | Use instead |
|---|---|
| `a11y` | `accessibility` |
| `wcag`, `section-508`, `compliance` | `accessibility-standards` |
| `screen-readers`, `voice-control` | `assistive-technology` |
| `color-blindness`, `contrast` | `low-vision` (add `color` when color itself is the subject) |
| `universal-design` | `inclusive-design` |
| `gestalt`, `perception` | `visual-perception` |
| `fitts-law`, `hicks-law` | `human-performance` |
| `color-theory` | `color` |
| `fonts`, `readability`, `legibility` | `typography` |
| `grids`, `composition`, `spacing` | `layout` |
| `icons`, `illustration`, `imagery` | `iconography` |
| `dataviz`, `charts` | `data-visualization` |
| `ia`, `navigation` | `information-architecture` |
| `ux-writing`, `microcopy` | `content-design` |
| `animation` | `motion` |
| `voice-ui`, `chatbots` | `conversational-interfaces` |
| `ai-interfaces`, `human-ai-interaction`, `genai-ux`, `automation`, `human-automation-interaction`, `supervisory-control` | `delegation` |
| `usability-testing`, `heuristic-evaluation` | `usability-evaluation` |
| `ab-testing` | `experimentation` |
| `component-library`, `design-tokens` | `design-systems` |
| `design-thinking` | `design-process` |
| `dark-patterns` | `deceptive-patterns` |
| `persuasion`, `nudges`, `gamification` | `behavior-change` |
| `credibility` | `trust` |
| `ux`, `ui`, `design`, `web`, `apps` | omit, or `digital-interfaces` per the umbrella rule |
| `study-note`, `synthesis` | omit — recorded by `type:` |
