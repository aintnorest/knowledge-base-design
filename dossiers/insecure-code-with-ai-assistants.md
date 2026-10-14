---
type: Study Note
title: Do Users Write More Insecure Code with AI Assistants?
description: A 47-person coding experiment finds task-specific security harms and higher security confidence with AI assistance, but its adjusted aggregate treatment estimate misses conventional significance and its C task is mixed.
resource: https://doi.org/10.1145/3576915.3623157
source: https://doi.org/10.1145/3576915.3623157
tags: [delegation, trust, human-performance, user-research, digital-interfaces]
timestamp: 2026-10-14T21:30:37Z
---

# Insecure Code with AI Assistants — Study Notes

**Authors**: Neil Perry, Megha Srivastava, Deepak Kumar, and Dan Boneh; Perry and Srivastava contributed equally.  
**Published**: ACM CCS 2023, November 26–30, Copenhagen; 16 pages; DOI 10.1145/3576915.3623157.  
**Status**: Peer-reviewed randomized user study; read the complete 16-page ACM-layout arXiv **2211.03622v3, December 18, 2023** copy, including figures, tables, references, and appendices. Register by the printed version-of-record DOI, not the arXiv identifier.  

## What It Is

A study of the security of **human–AI code production**, rather than a benchmark of standalone model output. It compares people with and without a separately queried code assistant and traces how accepted code, prompt revision, and confidence relate to vulnerabilities. Its strongest contribution is the distinction between **functional correctness, security, and perceived security**; the abstract's broad significance claim requires qualification by the actual analyses.

## Study Design

### Participants and task

The researchers recruited **54** participants through university mailing lists and word of mouth, including professionals at four companies. After failed prescreening and withdrawals, **47 remained: 33 assisted, 14 control**, from randomized assignment targeting a 2:1 allocation. **66% were undergraduates, 19% graduate students, 15% professionals; 87% aged 18–24; 62% had at most five years of programming experience**. A for-loop reading task screened basic programming knowledge. Compensation was **$30**, with up to **two hours** to work.

Participants received six self-contained security-related tasks in randomized order, could revisit them, use the Internet, and install libraries. Five were analyzed: Python symmetric encryption/decryption, Python ECDSA signing, Python restricted-directory file access, JavaScript SQL insertion, and C integer-to-string formatting. A sixth JavaScript display task was excluded after collection because its ambiguity allowed solutions that bypassed the intended sanitization problem. Most questions took **11–14 minutes**; the C task averaged **31 minutes**.

The assisted group used **codex-davinci-002**, explicitly querying a separate panel and copying selected outputs into an editor. Participants could vary generation parameters and response length. This is not passive inline autocomplete, a conversational modern assistant, or an autonomous repository-changing agent. Both groups could execute code and use external resources; the study recorded final code, prompts, responses, copying, screen/audio recordings, and post-task ratings.

### Measures and analysis

Two raters classified correctness and security, with Cohen's κ **.700–.966 for correctness and .679–.875 for security**; disagreements were resolved by three authors. Security categories depended on the task and included secure, partial, insecure, unknown, and not applicable. Source attribution could jointly involve AI, user, and Internet; an AI-involved mistake is not necessarily an exclusively AI-originated one.

Logistic regressions controlled security-class history, student status, and programming years, with model selection using BIC and removal of collinear predictors. Table 3 prints Benjamini–Hochberg critical thresholds for task regressions. Appendix 9.6 uses task-dependent binary bucketing: partial security counts as secure for encryption and restricted-directory access but insecure for signing; C denial-of-service and unchecked-return-code categories count as secure. Consequently, regression “secure” is not equivalent to the strict secure category or absence of harm.

Five-point surveys measured perceived correctness, perceived security, and assisted participants' trust in AI security. Direct copying and similarity to model output measure uptake; neither proves verification or fully captures influence. Prompt and parameter analyses are **observational within the assisted condition**, not randomized intervention comparisons.

## Results / Admissions

### Task-level security differences

| Task | Assisted / control evidence | Statistical claim in task prose |
|---|---|---|
| Encryption | Correct **67% / 79%**; strictly secure **21% / 43%**; insecure category totals **45% / 14%** | Insecure solutions **p = .017**; trivial ciphers **p = .018** |
| Signing | Strictly secure **3% / 21%**; correct **55% / 64%** | Strict secure difference **p = .039**; unsafe randomness and library selection were prominent |
| Restricted directory | Strictly secure **12% / 29%** | Failure to handle symlinks **p = .019**; correct file opening did not establish access confinement |
| SQL insertion | Strictly secure **36% / 50%**; SQL injection **36% / 7%**; correct **52% / 64%** | SQL injection **p = .041** |
| C formatting | Mixed correctness and security results | No clear overall help or harm; more integer-overflow mistakes in assisted solutions |

Percentages are rounded and include distinct correctness/security cross-classifications in Table 4. For example, a program can correctly encrypt/decrypt while omitting authentication, and a path-opening function can work on ordinary inputs while failing containment. Case accounts show participants testing functionality and then submitting unsafe code; ordinary successful tests did not cover the relevant security property.

### Aggregate regression is not conventionally significant

The adjusted aggregate treatment coefficient is **−.6315, SE .331, z = −1.908, p = .056** (Table 3), favoring lower security with assistance. The corresponding secure-outcome odds ratio is **approximately .53**, calculated by exponentiating the coefficient. **This is not a p < .05 aggregate treatment finding.**

Task treatment coefficients/p-values are **−2.1437/.018** for encryption, **−2.0244/.166** for signing, **−.5404/.562** for directory access, **−.8841/.279** for SQL, and **+.9709/.254** for C. Even encryption's nominal regression p = .018 exceeds its printed **B–H critical value .01**. None of these treatment rows passes its printed corrected threshold. The significant task-prose comparisons test particular categories or mistakes and should not be substituted for adjusted, multiplicity-corrected regression effects. The direction of several task results supports concern without establishing a uniformly significant overall causal penalty.

### Confidence and interaction

Assisted participants rated their solutions as more secure on average for every task despite often producing less secure code. Among assisted users, security trust was lower for those with secure than insecure answers: **1.5 versus 4.0** on directory access and **1.0 versus 3.53** on signing. For insecure encryption responses, perceived security averaged **3.5 assisted versus 2.0 control**. These are descriptive subgroup ratings, not reported adjusted causal effects or a validated individual calibration score.

The authors report **87% of secure responses required significant edits** relative to generated outputs. In C, **0% of generated outputs were directly copied**, although qualitative coding still identified AI involvement; copying is an incomplete reliance metric. Across tasks, users averaged **4.6 queries per question**. Repeatedly feeding generated code back into prompts could preserve unsafe assumptions; Figure 5 traces one such loop involving an insecure signing library.

Providing task context and helper code, revising prompts, and changing generation parameters were associated with more secure responses. These patterns can also reflect expertise and engagement: **they do not prove that a particular prompt format or parameter change causes security improvement**. Recommendations for integrated documentation, warnings, security tests, and security-oriented feedback were not experimentally evaluated here.

## Complementary Evidence, Not Direct Replication

[Sandoval et al.'s Lost at C](/dossiers/lost-at-c-llm-code-assistant-security.md) studies **58 students** implementing a connected C project over two weeks, with inline **code-cushman-001** completions and security measured as weakness density. It finds a small aggregate security impact in that setting, while individual functions vary. Perry et al. study multiple languages, discrete security tasks, a different model and query interface, and categorical outcomes; their lone C task is itself mixed. These findings are **complementary evidence about boundary conditions, not a direct replication success or failure**. Neither establishes a model-independent security effect for current agents.

## Analyst Takeaways

1. **Separate working code from safe code.** Oversight must inspect the security property and adverse cases, not merely the successful example or absence of runtime errors.
2. **Evaluate confidence against outcomes.** Higher perceived security alongside worse task outcomes is a calibration warning; increased trust is not a success measure by itself.
3. **Retain the statistical distinctions.** Local security mistakes, adjusted task effects, corrected significance, and the aggregate p = .056 answer different questions.
4. **Treat acceptance and review as different behaviors.** Copying logs and edited output cannot show that the developer understood or checked a security assumption.
5. **Do not prescribe prompting as a proven cure.** Active engagement is promising, but its association with security could be driven by who engages and what task they attempt.

## Questions and Limitations

- Small, student-heavy, unequal groups in a short artificial environment; security expertise and rare category outcomes are sparse. The signing regression's extremely large student coefficient/SE indicates an unstable estimate. The table does not specify a participant-clustered or mixed-effects treatment of repeated tasks in the aggregate model.
- The abstract says assisted participants wrote “significantly less secure code” overall, but the adjusted aggregate treatment **p = .056** is not conventionally significant, and printed corrected task treatment rows do not pass their thresholds.
- The main text describes category tests as a **chi-squared unequal-variance test**, whereas Appendix 9.6 calls the main comparisons **Welch's unequal-variance t-tests**. These are not interchangeable test descriptions; preserve the reported p-values without resolving the procedure by guesswork.
- Prompt Table 6's user percentages appear consistent with a denominator of **47**, rather than the **33** assisted participants (e.g. 63.8% ≈ 30/47), while repair Table 7 uses assisted-group-compatible percentages (e.g. 42.4% ≈ 14/33). The prompt-user denominator is insufficiently explained; do not treat Table 6 as assisted-user prevalence.
- “Significant edits” has no clearly stated threshold in the text; edit distance is not semantic review quality. Attribution overlaps sources and cannot identify an independent cause for every flaw.
- No direct independent replication is established by this source; its data and apparatus release enables replication, not evidence it occurred. Sandoval's differently designed study is complementary.
- **Redistribution evidence**: the file's ACM notice permits personal/classroom copying but says other copying, posting on servers, and redistribution require permission and/or a fee. No explicit public redistribution grant appears; keep this arXiv v3 copy in the private archive and cite the DOI.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Adds task-specific security-confidence miscalibration while preserving the nonsignificant adjusted aggregate treatment result and model/task boundaries.
- [Software Agent Oversight](/vault/software-agent-oversight.md) — Shows that copied or functionally tested generated code is not necessarily security-verified and that editing/engagement associations are not validated oversight interventions.
- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Adds concrete cases where successful functional tests missed authentication, containment, or memory-safety requirements and motivates purpose-specific review without claiming a tested review design.
