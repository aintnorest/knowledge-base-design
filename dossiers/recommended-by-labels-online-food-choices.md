---
type: Study Note
title: "Online Food Choices: When Do “Recommended By” Labels Work?"
description: Two smartphone menu studies find price and preference effects but no reliable general recommendation-label benefit, with the first study's recommendation-by-price interaction failing to recur under a changed preference-based design.
resource: https://doi.org/10.3390/foods13060928
source: /archive/recommended-by-labels-online-food-choices.pdf
tags: [decision-making, behavior-change, content-design, user-research, digital-interfaces]
timestamp: 2026-10-14T21:31:01Z
---

# Recommendation Labels in Online Food Choices — Study Notes

**Authors**: Daniele Catarci, Lea Laasner Vogt, and Ester Reijnen.  
**Published**: Foods **13(6), 928**, March 19, 2024.  
**Status**: Peer-reviewed report of two randomized smartphone-based online studies. Read the complete **30-page PMC print**, captured October 14, 2026, including references and captions; its missing figure images were recovered from the publisher-supplied PMC article. This is simulated menu selection, not measured cafeteria sales, consumption, nutrition, or sustainability improvement.

## What It Is

A test of whether a general **“RECOMMENDED”** banner and vertical option position influence choice when there are only two meals, as in some university cafeterias. Despite the title, the stimulus does not name a recommender or compare named human/AI authorities. Recommendations may provide a heuristic endorsement, but the studies do not directly measure cognitive processing or visual attention.

The useful model is that a recommendation competes with **price and prior preference**, rather than overriding them. The source's broad healthy/sustainable-food motivation is not a demonstrated outcome of these experiments.

## Study 1: Binary Choice

### Participants and design

The paper reports **N = 517 ZHAW students**, ages **18–45, mean 24.0, SD 3.96**, **63.4% female**, recruited through internal mailing lists. Diet: **377 unrestricted, 113 vegetarian, 27 vegan**. It separately reports excluding **22** respondents taking over 20 minutes (**4.1%**), leaving ambiguity about whether 517 denotes recruitment or the analyzed sample; all principal tests and the three recommendation groups use **517**.

A randomized **3 × 2 × 2 between-person design** crossed recommendation (**none, curry, dal**), curry position (**top, bottom**), and curry price (**cheap, expensive**). Participants made one hypothetical binary choice between vertically arranged curry and dal meals. The expensive and cheap options were always also named **“ExQuisit” and “Daily”**, so the price factor includes a tier-label change, not an isolated monetary manipulation. Both options carried sustainability/vegan cues in the illustrated stimulus.

After choosing, participants rated meal-choice factors on five-point scales and described the recommendation banner. Responses were classified as benevolent **nudge**, revenue-oriented **marketing**, or **neutral**. These post-choice interpretations are measured, not randomized.

### Results

A probit model found **no recommendation main effect**, **χ²(2,N=517) = 1.48, p = .477**, and **no position main effect**, **χ²(1,N=517) = .52, p = .473**. Price affected choice (**χ² = 18.96, p < .001**), with cheaper curry chosen more often. Recommendation × price was significant (**χ²(2,N=517) = 11.60, p < .01**); recommendation × position, price × position, and the three-way interaction were nonsignificant.

Within recommendation groups, the price contrast was significant when curry was recommended (**n = 174, χ² = 27.24, p < .001**) but not with no recommendation (**n = 172, χ² = 2.78, p = .095**) or dal recommended (**n = 171, χ² = .58, p = .446**). Curry was chosen in **66%** of cases overall. Figure 3 visually shows cheap-curry choice increasing from approximately **73% without** to **86% with** its recommendation, and expensive-curry choice decreasing from approximately **61% to 51%**; these are approximate plot readings, not tabulated effects or separately reported recommendation-versus-control tests. A significant within-group price contrast is not itself proof of a significant label uplift within the cheap condition.

Banner interpretation was **43% nudge, 20% marketing, 37% neutral**. No significant interpretation moderation was detected (other relevant effects **p ≥ .130**). Conditional mediation was also unsupported: the reported indirect effect was **b = .032, p = .211**. The general discussion nevertheless speculates that the cheap meal's recommendation worked because it seemed benevolent; that explanation is not supported as mediation by the reported tests.

Taste, price, and satiety led self-reported importance; recommendation, popularity, and vegan status ranked relatively low. Declared importance is not causal influence.

## Study 2: Personal Preference and a Changed Measure

### Participants and design

The paper reports **N = 916 ZHAW students**, ages **18–55, mean 24.4, SD 4.73**, **71.2% female**; diets were **677 unrestricted, 191 vegetarian, 48 vegan**. It separately reports **21** exclusions for duration below 1.5 or above 20 minutes (**2.2%**), again without clearly reconciling recruitment and analysis denominators.

Participants first ranked **six menus** presented without prices in random order. Random assignment selected either their **most versus least preferred** meals (large preference gap) or their **third versus fourth ranked** meals (small gap). All menus offered vegetarian/vegan-compatible choices. The **3 × 2 × 2** design crossed recommendation (**none, preferred, nonpreferred**), preferred-menu price (**cheap, expensive**), and preference difference (**small, large**). Position was no longer manipulated.

Unlike Study 1, choice was a **0–100 slider**, originally described as Daily-to-ExQuisit and then represented as nonfavored-to-favored. Figure 7 explicitly makes the midpoint “neither.” This measures graded choice inclination, not a percentage of people making a binary purchase. Figures 8–9 use percentage-like labeling that should not erase that distinction. Banner interpretation now used a **1–9 nudge-to-marketing scale** instead of open-response coding.

### Results and replication status

Reported ANOVA results are **price F(1,916) = 112.90, p < .001**, **preference difference F(1,916) = 128.90, p < .001**, and their interaction **F(1,916) = 6.18, p = .013**. Price mattered more with a small preference gap. Other interactions were nonsignificant (**F ≤ 2.12, p ≥ .12**); the text reports no observed recommendation effect in this study. It does not provide a numerical recommendation-main-effect test or a standardized effect size/CI.

The **recommendation × price finding did not recur**. This is a within-paper conceptual follow-up, not an exact replication: meals, preference elicitation, response measure, auxiliary labels, and position manipulation changed. The roughly **61%** favored-menu summary in the small-gap condition should be interpreted cautiously because this study measured a continuous inclination score.

Banner-interpretation effects were nonsignificant (**F ≤ 1.80, p ≥ .31**). Taste again led reported importance, with price and satiety next and recommendations near the bottom. The paper proposes that stronger baseline price differences in Study 2 leave little visible room for recommendations, possibly because Study 1's auxiliary labels diverted attention; these are post-hoc hypotheses, not tested attention mechanisms.

## Analyst Takeaways

1. **A recommendation badge is not a guaranteed conversion lever.** Neither study establishes a general main-effect benefit, and the observed interaction failed to recur under the changed design.
2. **Evaluate the offer, not only the label.** Existing preference and affordability can dominate the same visual endorsement; price/tier labeling and preference strength need to be separated when interpreting outcomes.
3. **Keep a no-recommendation control.** Without it, preference for the promoted meal can be mistaken for an endorsement effect.
4. **Separate seeing, interpreting, and choosing.** Measured interpretations did not explain the choice effect; visual salience is plausible but was not measured with gaze or attention tasks.
5. **Do not generalize to named recommender authority or AI trust.** A generic banner does not test expert identity, algorithmic credibility, or calibrated reliance on an objectively correct answer.

## Questions and Limitations

- Convenience samples from one Swiss university, one short hypothetical choice per participant, no observed purchases or consumption, and no independent exact replication. Results do not establish safety against manipulative recommendations in other populations or larger menus.
- No reported standardized treatment effects or numerical uncertainty intervals for label-versus-control contrasts; graphs show standard errors. Null significance tests do not demonstrate equivalence or rule out smaller effects.
- **Internal inconsistencies**: the abstract emphasizes a negative recommendation effect when popular curry is expensive, whereas the results/discussion emphasize increased choice when it is cheap; Figure 3 suggests both directional tendencies, but the printed tests primarily compare price within recommendation groups. Avoid selecting one summary as a settled simple effect.
- **Sample/analysis ambiguity**: participant totals and exclusions are not cleanly reconciled; Study 1 recommendation groups sum to 517 despite the 22 exclusions, and Study 2 prints denominator **916** for its factorial F tests despite calling 916 its total participant count and reporting 21 exclusions. No corrected denominator is inferred here.
- Figure 5's printed path coefficients (**−.047 and −.085** from interpretation to choice) differ from the prose's **.002/.032** reported effects, while the caption identifies **.032** as the indirect effect. These may refer to different estimands, but the labeling does not clearly reconcile them.
- Several recommendation discussion claims cite reference **21**, which is a smaller-plates meta-analysis, not a recommendation-label study; the prose dates Dolnicar/Grün to **2007**, but reference 51 is **2013**. The broad “95% automatic decisions” introduction claim is not measured by these studies.
- **Redistribution evidence**: the print hides its licence in a collapsed heading. The publisher-supplied [PMC article](https://pmc.ncbi.nlm.nih.gov/articles/PMC10969444/) exposes **“© 2024 by the authors”** and **“Licensee MDPI, Basel, Switzerland”**, explicitly granting **Creative Commons Attribution (CC BY) 4.0**. MDPI's direct article/HTML URLs returned 403, but this article-specific publisher licence was recovered from the PMC HTML, not inferred from MDPI's general practice. The unchanged print is archived publicly with attribution here.

## Vault Ideas Extracted

- [Choice Architecture Effects](/vault/choice-architecture-effects.md) — Adds two controlled smartphone menu studies with no detected general recommendation or position benefit, a nonrecurring recommendation-by-price interaction, and stronger price/preference evidence under a changed response measure.
