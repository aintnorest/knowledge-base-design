---
type: Study Note
title: "Lost at C: A User Study on the Security Implications of Large Language Model Code Assistants"
description: A 58-person C-programming study finds lower average weakness density with AI assistance but mixed function-level outcomes, with a claimed security non-inferiority result qualified by a printed p = .06 and inconsistent denominators.
resource: https://www.usenix.org/conference/usenixsecurity23/presentation/sandoval
source: https://www.usenix.org/conference/usenixsecurity23/presentation/sandoval
tags: [delegation, human-performance, user-research, trust, digital-interfaces]
timestamp: 2026-10-14T21:30:37Z
---

# Lost at C and Code-Assistant Security — Study Notes

**Authors**: Gustavo Sandoval, Hammond Pearce, Teo Nys, Ramesh Karri, Siddharth Garg, and Brendan Dolan-Gavitt; New York University; Sandoval and Pearce contributed equally.  
**Published**: 32nd USENIX Security Symposium, August 9–11, 2023, Anaheim; proceedings pages **2205–2222**.  
**Status**: Peer-reviewed randomized user study; read the complete supplied **19-page proceedings PDF** (cover plus 18 paper pages), including figures, tables, references, and embedded appendix. No source-specific DOI is printed; the publisher's presentation URL is the canonical registry key.  

## What It Is

A study of whether student programmers accepting inline code completions produce a less secure final program than students working without those completions. It distinguishes **standalone generation, assisted human production, functional performance, vulnerability density, and bug provenance**. The result is not “AI code is safe”: both human and generated code contain many weaknesses, and favorable aggregate density coexists with worse outcomes on some functions.

## Study Design

### People, project, and assistance

**105 students signed up and were randomly allocated; 58 submitted code for analysis**. Demographic tables report **29 control and 29 assisted**, comprising **33 undergraduates, 23 postgraduates, and two other participants**. Of respondents, **44** had programmed in C before, **seven** said this was their first time, and **seven** declined to answer. **29** reported their first linked-list implementation in C, **23** had done one before, and **six** declined. Recruitment drew on operating-systems and application-security classes and a student chat group; compensation was **$50**, without requiring full completion.

The project was a singly linked shopping list in C with **12 functions, one supplied and 11 to implement**. It combined node/pointer operations, string formatting, traversal, and file input/output. Unusual indexing and argument conventions deliberately increased opportunities for mistakes. Participants had **two weeks**, with a small minority allowed longer; they used their own computers through a common cloud IDE, could use Internet resources, and could not ask peers for code-writing help. The project context differs from disconnected single-function security puzzles.

The assisted interface offered faded inline suggestions from **code-cushman-001**, modeled after Copilot, with fixed generation settings and relatively short completions. People could accept, reject, or later edit them; prompts reflected preceding code in the file. The authors also generated **30 autopilot programs**, ten from each of three Codex models, attempting functions sequentially and retrying compilation failures. Only **five code-cushman-001 autopilot solutions** received manual security audit; the larger automated baseline must not be conflated with that audited subset.

### Functionality, security, and provenance

Functionality measures included implemented/compiling functions and passed basic/expanded tests. The results section describes **11 basic tests and 43 expanded tests**. To avoid one broken dependency failing every downstream function, evaluation replaced other functions with known-good implementations while testing one submitted function. This isolates local behavior rather than demonstrating the submitted program works end to end.

Three authors collectively audited blinded code, guided by compiler logs and test results, recording **67 unique bug classes**. The audit took **22 hours, 66 person-hours**. No independent inter-rater reliability was measured because annotation was collective. “Severe” weaknesses used MITRE's 2022 Top 25, including relevant downstream severe consequences of some unranked weaknesses.

Security was measured as **each participant's CWEs per line of valid code**, then averaged across participants, under two validity definitions: compiling functions and functions passing unit tests. A second metric counted weaknesses per function. These denominators answer different questions; more lines or more completed functions can change density without reducing total defects.

Non-inferiority tests asked whether assisted weakness density was less than **1.10 times control density**. The authors chose this **10% relative margin** using medical-trial precedent and acknowledge no accepted software-security margin exists. This is not a ten-percentage-point risk difference, zero extra vulnerabilities, or a universal acceptable security threshold. Functional comparisons used Fisher's exact test for binary completion and Welch's t-tests for other measures.

## Results / Admissions

### Functionality: favorable direction, no significant comparisons

Assisted participants had modest descriptive advantages in functions implemented/compiled and tests passed, and wrote **280.9 mean lines versus 247.5 control**. **None of these comparisons reached p < .05**. Figure 7 shows roughly **46% versus 63% implemented functions**, **28% versus 37% basic tests passed**, and **15% versus 25% expanded tests passed** for control versus assisted; these are approximate visual readings, not printed exact estimates. The paper says productivity was **not directly measured**. Earlier calendar submission in Figure 12 is not measured active programming time.

Autopilot compiled more functions by design because generation retried compilation failures. Its different procedure and selection constraints make it a useful baseline, not a randomized human condition or evidence that removing oversight improves security.

### Security depends on denominator and scope

Mean participant-level weakness density favored assistance in all four combinations of all/severe weaknesses and compiling/passing functions, with **up to 22% lower mean severe CWEs per line among passing functions**. Figure 8 reports non-inferiority **p = .04 for severe CWEs per line over compiling functions**, but **p = .06 over passing functions**. The latter does **not** meet the paper's conventional .05 threshold, despite prose claiming both severe comparisons were significant. Lower observed density is not proof of security superiority or a universally established 10% upper bound.

Table 3's pooled severe-weakness counts provide an important counterpoint:

| Validity subset | Control | Assisted |
|---|---|---|
| Compiling functions | **139 functions, 290 CWEs, 2.09 per function** | **204 functions, 451 CWEs, 2.21 per function** |
| Passing functions | **84 functions, 180 CWEs, 2.14 per function** | **124 functions, 278 CWEs, 2.24 per function** |

Assistance is associated with more completed functions and more total recorded severe weaknesses in these subsets, while participant-level per-line density favors it. These are compatible observations, not contradictory arithmetic: the unit, weighting, and denominator differ.

Function-level outcomes varied. Among compiling functions, severe rates were **3.05 control / 3.38 assisted** for insertion and **2.71 / 3.67** for update, but **1.67 / .93** for deduplication. Among passing functions, loading had **1.50 / 2.00**, printing **.44 / .77**, and swapping **2.20 / 1.17**. Table 3 marks several function differences significant but does not print their exact p-values there. Aggregate density cannot establish that every operation is safe or equally aided.

A worked case passed basic tests yet contained **three weaknesses**, including an out-of-bounds write and null-pointer dereference, two ranked severe. Functional success did not establish the input/memory assumptions necessary for safe operation.

### Bug provenance and retained errors

Within assisted submissions, the authors examined **564 weaknesses** and attributed **356 (63%)** to human-written code, **16%** to exact accepted suggestions, and **20%** to modified suggestions. Roughly **60% of non-template code** was classified as human-written, **16%** exact Codex, and **18%** approximately matching Codex. Provenance percentages should not be treated as a complete allocation of code because the printed code percentages sum to **94%**.

The tracing of use-after-free defects shows both directions of influence: unsafe human code can seed later suggestions, and suggestions can introduce defects that survive acceptance and modification. One participant received **69** suggestions containing the traced bug, accepted **five**, and retained **four** instances; another received **20**, accepted **ten**, and retained **five**. Others authored the defect without accepting a buggy suggestion. These are longitudinal case traces, not randomized evidence that a particular acceptance rate causes defects.

The authors suggest that productivity gains were not reliably reinvested in fixing security bugs. They propose highlighting problematic code with “nutritional labels” to encourage checking; **no label intervention or review-support design was tested**. Nor were self-reported security trust or calibration measured as in Perry et al.

## Complementary Evidence, Not Direct Replication

[Perry et al.](/dossiers/insecure-code-with-ai-assistants.md) find task-specific security harms and higher perceived security across five short tasks in Python, JavaScript, and C using **codex-davinci-002** with a separate query panel; their adjusted aggregate treatment has **p = .056**, and their C task is mixed. Lost at C uses a connected C project, inline **code-cushman-001**, a longer work window, and density/non-inferiority measures. The studies therefore supply **complementary boundary-condition evidence, not a direct replication or a simple contradiction**. Their common observation is that generated code can be accepted or edited without removing its security defects.

## Analyst Takeaways

1. **Evaluate the human–assistant workflow, not generation alone.** Final defects depend on accepted suggestions, existing human code, and subsequent edits; provenance and group outcomes are distinct measures.
2. **Choose a risk measure before declaring safety.** Total defects, defects per function, and average participant-level per-line density can move in different directions.
3. **Inspect local outcomes beneath favorable averages.** File and display operations had worse assisted rates in some passing-function comparisons even while aggregate density favored assistance.
4. **Acceptance and modification do not prove verification.** A changed snippet can retain the original defect, and basic tests can leave security assumptions unchecked.
5. **Keep non-inferiority conditional.** An arbitrary tolerated margin and one p = .04 result do not justify the broad claim that code assistants introduce no new security risks.

## Questions and Limitations

- Small, student-based, single-project sample with substantial attrition (**58/105** produced analyzable code); professional workflows, other languages, and current assistants are not directly tested. No independent replication of this design is established here; publisher artifact badges are not evidence of a new participant experiment.
- **Significance inconsistency**: Figure 8(d) prints **p = .06**, whereas Section 4.3.3 calls both severe-density comparisons statistically significant. The claim of a bound for passing functions is not supported at .05 by the printed statistic.
- **Participant denominator inconsistency**: demographic tables say **29/29**, but compilation prose reports **9/30 assisted** and **10/28 control** among **19/58 noncompiling programs**. Do not silently reconcile the allocation.
- **Test-count inconsistency**: methods mention **12 basic tests**, but results and Figure 7 say **11**. The note uses the results' 11 while retaining the discrepancy.
- **Table inconsistency**: Appendix Table 7 gives **16 assisted compiling deduplication functions versus 15 in Table 3**, **18 loading versus 17**, and **13 passing removal functions versus 14**. These denominators constrain precision of per-function interpretation.
- **Incomplete attribution totals**: code percentages sum to **94%**, while bug percentages sum to **99%** (the latter could be rounding); the code remainder is not explained. Approximate string matching and minute-spaced snapshots limit fine-grained causality and provenance.
- Collective audit lacks independent rater agreement; annotated weaknesses are not all demonstrated exploits, and function-isolation testing is not whole-program deployment safety. Short output, fixed settings, prior-code context, and deliberately awkward task conventions limit transfer.
- The conclusion's “does not introduce new security risks” is stronger than conditional density non-inferiority with many retained weaknesses warrants. The functionality claim also outruns nonsignificant comparisons if read as an established causal benefit.
- **Redistribution evidence**: the cover says open access is sponsored by USENIX, and the publisher page says papers are freely available, but neither the supplied PDF nor the inspected presentation page supplies an explicit CC/public-domain or equivalent redistribution licence. Open access alone is not a public redistribution grant; keep the proceedings copy private.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Adds a conditional coding-study counterweight to blanket harm claims, preserving a nonsignificant passing-function non-inferiority result and locally worse assisted outcomes.
- [Software Agent Oversight](/vault/software-agent-oversight.md) — Adds bug-provenance traces showing that acceptance and later editing can retain defects and that human-written context can seed unsafe suggestions.
- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Distinguishes functional tests from security-property checking through audited passing-but-vulnerable functions, without claiming an experimentally validated review intervention.
