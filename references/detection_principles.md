# Detection Principles: Multi-Detector AIGC Trace Analysis for Quantitative and Qualitative Thesis Writing

This system uses D1–D17 as general academic-writing dimensions (applied to all papers and especially to quantitative ones), with the qualitative-only dimensions D18, D19q, D20, and D21 added for qualitative and mixed-methods papers. Do not assume a qualitative thesis only needs D1–D17; its interview reporting, theme presentation, researcher-voice, and quote-balance risks are scored by D18–D21.

## Overview

This reference is designed for conservative AI-risk estimation in English master’s thesis writing. It is stricter than ordinary phrase-based AIGC checks. The previous scoring style may produce very low values when a paragraph does not contain many obvious AI phrases, but external AI detection systems can still produce a high score when many paragraphs share similar rhythm, paragraph architecture, smooth academic logic, or generic thesis phrasing.

> Important: this internal scoring is only a diagnostic aid for LOCATING risk. It has limited power to PREDICT the external detector result, and it cannot predict what a rewrite will score. The only trusted verdict is a real external re-test of the rewritten chapter. Use these dimensions to decide *where* and *how* to edit, but always confirm the result by re-testing one chapter at a time (see SKILL.md → Core Operating Architecture). Never let a low internal score justify keeping a rewrite that a detector scored higher.

This version therefore uses three layers of detection:

1. **Sentence-level signals**: repeated starters, formulaic transitions, uniform rhythm, passive clusters, repeated academic verbs.
2. **Paragraph-level signals**: template structure, over-smooth logic, generic conclusion sentences, abstract-to-concrete imbalance.
3. **Document-level signals**: repeated paragraph architecture across a section, repeated literature-review pattern, repeated hypothesis-development pattern, and repeated discussion pattern.

A low raw score is not enough. If the paragraph belongs to a repeated structure across the paper, the scoring system must apply a floor score.

---
## Detector-Side Risk Logic

External AI detection systems should not be understood only as phrase matching. It may combine several types of signals:

1. Predictability / low perplexity
   - AI-like text often chooses safe and expected words.
   - Academic paragraphs may look risky when every sentence uses predictable phrasing.

2. Low burstiness
   - AI-like text often has similar sentence length, similar sentence rhythm, and balanced structure.
   - Human academic writing usually has more uneven rhythm.

3. Over-coherent semantic flow
   - AI-like paragraphs often move too smoothly from claim to explanation to implication.
   - This is especially common in literature review, hypothesis development, discussion, and conclusion sections.

4. Deep semantic classification
   - Modern detectors may identify paragraph-level and section-level regularity, not only repeated words.
   - Therefore, the scoring system must consider cross-paragraph structure, not only visible AI phrases.

Scoring implication:
- Do not lower a paragraph’s risk only because it has few obvious AI phrases.
- If paragraph rhythm, paragraph architecture, or section-level structure is repeated, apply the relevant floor rules.

### Statistical Risk Caution

Perplexity, burstiness, sentence-length variance, and vocabulary predictability should be treated as risk indicators, not absolute proof of AI writing.

Use them to identify:
- overly predictable wording;
- overly uniform sentence length;
- repeated sentence structures;
- smooth paragraph chains;
- lack of concrete thesis-specific information.

Do not use these indicators mechanically. A formal academic thesis may naturally contain repeated terms, stable terminology, and some standardized expressions.

Repeated structure, statistical uniformity, and unnatural fluency should be treated as combined risk signals. A paragraph may look acceptable alone, but become risky when the same rhythm appears across several sections.


### Quantitative Signal Reference (calibration anchors for manual D-scoring)

The dimensions below are scored by judgment, but the following operational thresholds — taken from explainable, rule-based detector heuristics for English prose — provide concrete numeric anchors so that D2, D4, D8, and D11 are scored consistently rather than by impression. These are CALIBRATION AIDS that supplement the D1–D21 scoring; they never replace it, and (per the Cluster-Density False-Positive Guard and the count-before-flag rule) a single metric crossing a threshold is not a verdict — combine signals. Always state the count when a score leans on one of these.

| Signal (how to compute over the span) | AI-leaning region | Human/natural region | Maps to |
|---|---|---|---|
| Sentence-length coefficient of variation = SD ÷ mean of words-per-sentence | CV < 0.35 (uniform — AI-leaning) | CV > 0.7 (varied); 0.35–0.7 natural | D4 |
| Transition-marker density = generic transition occurrences ÷ sentence count (count only generic transition markers; exclude protected methodological labels, hypothesis labels, table/figure references, and required disciplinary phrases) | > ~20% (high — AI-leaning) | < ~10% (natural) | D2 |
| Passive-voice share = passive sentences ÷ total sentences | > ~15% (high) | < ~10% (natural) | D8 |
| Type-token ratio (TTR) = unique words ÷ total words, over a comparable span | < ~0.4 (repetitive) or pushed unnaturally high | ~0.4–0.8 typical | D11 |
| Elevated/rare-word share = uncommon content words ÷ total words | > ~12% (over-elevated — machine-polished) | lower | D11 / T10 |
| Repeated n-gram share = repeated 3–4-word sequences ÷ total n-grams (excluding protected technical terms, variable names, and standard methodology phrasing) | high repetition of generic multi-word sequences across the span | low | D13 / D16 / T10 |
| Heavy-punctuation density = (em dashes + semicolons + colons + ellipses) ÷ sentences | > ~0.5 (high) | < ~0.3 (natural) | Gate D / formatting |
| Flesch–Kincaid grade level | very high uniformly | — | weak signal only — see caveat |

Academic-register caveats (mandatory — these thresholds come from general prose and will misfire on legitimate thesis writing if applied blindly):
- Passive voice above ~15% is NORMAL in Methods and Results sections; treat it as a tell only when it clusters across sections where active voice would be natural (see D8).
- A high Flesch–Kincaid grade level is EXPECTED in academic prose and is the weakest signal here; never treat it as a standalone tell, and never raise it deliberately — the whole skill aims away from over-elevation, not toward it.
- Low TTR caused by correctly REPEATING a technical term, variable name, or participant label is a protective human signal and an academic requirement (one concept = one term, Gate B / elegant-variation rule), NOT an AI tell. Do not "fix" it by introducing synonyms. TTR is also length-dependent, so compare only within spans of similar length.
- A HIGH elevated/rare-word share is the over-polish failure mode (the same problem T10's "precision over rarity" rule and Gate G guard against); it points toward pulling the wording back toward the Author Style Baseline, never toward adding more exotic vocabulary.
- Repeated n-grams made of REQUIRED technical terms, variable names, hypothesis labels, or standard methodology phrasing (e.g. "confirmatory factor analysis", a recurring construct name) are legitimate and protective — exclude them before judging n-gram repetition. Flag only repeated GENERIC multi-word sequences (e.g. "plays an important role in", "has attracted increasing attention"), which is the D16 phrase-template / T10 collocation problem and is fixed by de-templating the generic phrasing, never by renaming the technical terms.
- These numbers calibrate diagnosis only. They do not change any rewrite, never license shrinking the text, deleting content, or fabricating anything, and a rewrite that merely moves a metric across a threshold without genuine structural change has not reduced real risk.

Detector-class note: model-based detectors increasingly report a separate "human-written but AI-refined / AI-polished" class for text whose wording is genuine but has been smoothed into an over-uniform register. This is the mechanism behind the over-polish guard — editing a real thesis toward fluent uniformity can move it from the human class into the AI-refined class. It is a further reason to rewrite toward the author's own low-risk baseline rather than toward generic polish.

Commercial-detector alignment note: the signals above are the same ones third-party detectors expose under their own names — perplexity / low-predictability, burstiness (= sentence-length variation, D4), readability (≈ Flesch–Kincaid), n-gram repetition (D13/D16), average sentence length (D4), and an elevated-vocabulary or "SAT-word" percentage (= the elevated/rare-word share, D11/T10). Diagnosing against the table above therefore partially aligns the internal diagnosis with publicly discussed, explainable signal categories that some detectors may use or expose — without depending on, paying for, or routing text through any such service. It does not simulate, predict, or reverse-engineer any external detector, and must never be treated as proof of what Turnitin, CNKI, GPTZero, Originality.ai, or any other system will report. Never send thesis text to a third-party humanizer or "undetectable"/"bypass" API: that is whole-text regeneration by an outside model (violates Principle 2), an academic-integrity and confidentiality risk, and self-defeating, because the returned machine-rewritten prose reads as AI to detectors.


---

## External Detector Structural Risk Logic

When one or more external AI detector reports are available, treat externally highlighted or high-risk sections as stronger evidence than internal paragraph scores.

Shared detector-sensitive risks include:

- long continuous AI-like fragments;
- repeated chapter-level templates;
- over-smooth academic reasoning;
- repeated paragraph architecture;
- mechanical methodology reporting;
- mechanical empirical-result reporting;
- generic conclusion and implication structures;
- polished academic synthesis that does not match a normal master’s thesis style.

Mandatory rule:
- Internal low scores cannot override high external detector evidence.
- If an external report flags a section as high-risk, raise D12, D13, D14, D15, D16, and D17 sensitivity.
- If a section is externally high-risk, apply section-level floors even when individual paragraphs look acceptable.
- Treat external highlighted sections as priority evidence for Phase 1.5, Phase 1.6A, Phase 1.7, and Phase 4.


---

## Section Architecture Risk

Some AI-risk signals are not visible inside a single paragraph. They appear when several paragraphs in the same section perform the same function.

High-risk section architecture includes:

- several subsections using the same background → gap → value path;
- several theory paragraphs using theorist/year → concept → application;
- several literature review paragraphs using definition → citation → implication;
- several hypothesis paragraphs using variable → mechanism → citation → hypothesis;
- several empirical result paragraphs using test → threshold → result → conclusion;
- several conclusion paragraphs using finding → theory → practice.

Scoring implication:
- Section architecture risk should increase D13 and D15.
- If three or more neighboring paragraphs share the same functional role, D13 should normally be at least 2.0.
- If an entire subsection depends on a repeated functional path, D15 should normally be at least 1.5.
- If several subsections in a chapter use the same function path, apply section_template_floor even when individual paragraph scores are moderate.

Mandatory rule:
- Do not score D13 only by repeated words or repeated sentence openings.
- D13 must also consider repeated paragraph function.
- D15 must consider repeated subsection architecture.
- D13 and D15 floor values require a minimum structure-evidence record: paragraph IDs in the repeated cluster; each paragraph's functional path (e.g. definition → citation → implication); number of repeated units; whether repetition is local, section-level, or chapter-level; and the floor applied with its reason. Do not assign a D13/D15 floor without this cluster record.

---

## Aggregation-Worsening Risk

Aggregation-worsening risk appears when rewriting reduces the number of fragments or paragraphs but makes the largest single fragment longer than before.

This is risky because a longer continuous fragment may create:
- lower burstiness;
- smoother uninterrupted academic flow;
- longer AI-like semantic continuity;
- fewer human-style interruptions;
- stronger paragraph-level or section-level template appearance.

Detection rule:
```text
aggregation_worsening = (
  revised_fragment_count < original_fragment_count
  AND revised_max_fragment_characters > original_max_fragment_characters
)
```
High-risk threshold:
- If any revised fragment exceeds 3000 characters, treat it as a long-continuous-fragment risk: first try safe paragraph splitting at existing logical boundaries (combined word count assessed under Gate F). Insert a breakpoint sentence only when it is traceable to existing thesis content (T19 relocation or T29 reconstruction with Source Trace) and adds no unsupported interpretation.
- The risk should be reviewed together with D3, D4, D12, D14, D15, D16, and D17.
- A long fragment is not automatically wrong, but it must contain at least one valid breakpoint if it exceeds 3000 characters.

Valid breakpoint:
A breakpoint is a sentence or internal division that interrupts smooth AI-like continuity while preserving academic meaning.

Valid breakpoint types include:

- concrete number already present in the thesis;
- researcher-view judgment (valid ONLY when extracted from or directly supported by existing thesis content, with its original location recordable; a newly invented author voice is NOT a valid breakpoint);
- process narration (valid ONLY when it describes a process the thesis actually documents; never a fabricated procedure);
- scope boundary;
- supported contrast;
- reference to a specific variable, hypothesis, table, coefficient, sample, or measurement choice.

Invalid breakpoint:

- random short sentence;
- unsupported opinion;
- invented example;
- invented data;
- vague sentence that only says “this is important” or “this should be noted.”

Scoring implication:

- If aggregation-worsening is detected, increase sensitivity for D3, D4, D12, D14, D15, D16, and D17.
- If the fragment exceeds 3000 characters and has no valid breakpoint, Phase 7 must mark it as Rework Needed.

This risk does not create an additional D18 dimension. It is a post-rewrite structural risk signal that increases sensitivity for D3, D4, D12, D14, D15, D16, and D17.

---

## Core Scoring Rule

Do not score only by adding visible phrase counts. External-detector AI risk is often created by accumulated structural regularity. Therefore:

```text
paragraph_risk_index = max(
  raw_paragraph_risk,
  pattern_floor,
  repeated_structure_floor,
  section_template_floor,
  d16_d17_trigger_floor,
  multi_detector_trigger_floor
)
```
D16/D17 trigger floors and multi-detector trigger floors must be applied when methodology-template risk, reporting-sequence risk, front-loaded continuous fragments, uniform rhythm across paragraphs, human research trace deficit, or repeated result-implication loops are detected.

The final document score also uses a floor:

```text
scope_risk_index = max(
  calculated_scope_risk_index,
  scope_pattern_floor
)
```

If the user provides an external detector result, such as Turnitin AI = 48%, use it as a calibration signal. The internal score should not be reported far below the known detector result unless there is clear evidence that the external result included references, appendices, or non-body content.

---

## Full Dimension Coverage Requirement

A valid paragraph-level AI score requires all 17 dimensions to be evaluated.

Partial scoring is not valid for final paragraph_risk_index calculation.

Automated scripts may help identify surface-level signals such as repeated starters, sentence length, generic phrasing, passive clusters, abstract wording, or repeated verbs. However, these scripts often miss structural dimensions such as:

- D2 Formulaic Transitions
- D3 Over-Smooth Logical Flow
- D6 Hedging / Balanced Claims
- D7 Conclusion-Style Generalizations
- D10 Citation Pattern Regularity
- D12 Paragraph-Level Template Structure
- D13 Cross-Paragraph Structural Repetition
- D14 AI-Like Academic Smoothness
- D15 Thesis-Section Template Dependency

These missing dimensions are often the main reason for external-detector high AI scores.

Mandatory rule:
- Do not report a final paragraph_risk_index score based only on automatically detected dimensions.
- If only partial dimensions are available, label the result as “Preliminary Auto Scan Only.”
- Before final scoring, manually evaluate all missing dimensions.
- D12-D17 must always be checked because they capture structural and section-level AI risk.

---

## Dimension 1: Repetitive Sentence Starters (Weight: 3.0)

**What detectors look for**: AI-generated academic writing often starts sentences and paragraphs with a limited group of safe academic openings.

**High-risk sentence starters**:
- This study...
- This research...
- The results show...
- The findings indicate...
- Based on this...
- Therefore...
- Thus...
- Moreover...
- Furthermore...
- In addition...
- In this context...
- From this perspective...
- It is important to note that...
- It can be seen that...

**Scoring**:
- 0-1 repeated starter → 0
- 2 repeated starters → 0.8
- 3 repeated starters → 1.5
- 4 repeated starters → 2.2
- 5+ repeated starters → 3.0

**Strict rule**: If the same opening pattern appears across multiple paragraphs, also apply Dimension 13.

---

## Dimension 2: Formulaic Transitions and Connector Chains (Weight: 3.0)

**What detectors look for**: AI writing often uses transition chains to make logic look smooth.

**High-risk patterns**:
- It is worth noting that...
- It is important to emphasize that...
- In light of the above discussion...
- Taken together, these findings suggest...
- This indicates that...
- This further demonstrates that...
- Therefore, it can be concluded that...
- Based on the above analysis...
- For this reason...
- In summary...

**Scoring**:
- 0 formulaic transitions → 0
- 1 formulaic transition → 0.8
- 2 formulaic transitions → 1.5
- 3 formulaic transitions → 2.2
- 4+ formulaic transitions → 3.0

**Strict rule**: Repeated connector chains across paragraphs should be treated as structural risk, not only phrase risk.

---

## Dimension 3: Over-Smooth Logical Flow (Weight: 3.0)

**What detectors look for**: AI-generated thesis writing often sounds too coherent, too complete, and too polished. Each sentence neatly supports the next sentence, but the reasoning feels like generated synthesis.

**High-risk patterns**:
- background → explanation → implication → conclusion
- concept definition → positive effect → research value
- result → interpretation → theoretical contribution → practical implication
- every sentence has a clear transition but little human unevenness
- no visible reasoning struggle, limitation, or thesis-specific detail
- frequent use of em dashes to create smooth explanatory contrast or polished restatement.

**Scoring**:
- natural or slightly uneven academic flow → 0
- mildly smooth but acceptable → 0.8
- clearly polished and predictable logic → 1.5
- strong machine-like logical progression → 2.2
- whole paragraph reads like generated academic synthesis → 3.0

---

## Dimension 4: Uniform Sentence Length and Rhythm (Weight: 2.5)

**What detectors look for**: AI text often has sentences of similar length and structure.

**Measurement**:
```text
variance = Σ(xi - mean)² / n
```

**Scoring**:
- variance > 90 → 0
- variance 60-90 → 0.6
- variance 40-60 → 1.2
- variance 20-40 → 1.8
- variance < 20 → 2.5

**Additional warning signs**:
- most sentences fall between 18 and 28 words
- several sentences use subject + verb + object + implication
- paragraph has no short sentence and no naturally long sentence
- clauses are balanced in a similar way across sentences

---

## Dimension 5: Generic Academic Phrasing (Weight: 3.0)

**What detectors look for**: AI writing relies on safe academic phrases that sound correct but do not say much.

**High-risk phrases**:
- plays an important role
- plays a key role
- has significant implications
- provides valuable insights
- is closely related to
- has attracted increasing attention
- is of great importance
- contributes to a better understanding of
- promotes the development of
- enhances the effectiveness of
- provides theoretical support
- provides empirical evidence
- enriches the existing literature
- broad interpretive phrases added after an em dash, especially when they restate the previous clause in a more abstract way

**Scoring**:
- 0-1 generic phrase → 0
- 2 generic phrases → 0.8
- 3 generic phrases → 1.5
- 4 generic phrases → 2.2
- 5+ generic phrases → 3.0

---

## Dimension 6: Overused Academic Hedging or Balanced Claims (Weight: 2.0)

**What detectors look for**: AI-generated academic writing often uses too much cautious wording or symmetrical argument structure.

**High-risk phrases**:
- may potentially
- to some extent
- to a certain degree
- it could be argued that
- might be considered as
- appears to be somewhat
- on the one hand... on the other hand
- while some scholars argue... others suggest...

**Scoring**:
- 0-1 instance → 0
- 2 instances → 0.5
- 3 instances → 1.0
- 4 instances → 1.5
- 5+ instances → 2.0

---

## Dimension 7: Conclusion-Style Generalizations (Weight: 2.5)

**What detectors look for**: AI often ends paragraphs with broad statements that sound polished but add little.

**High-risk patterns**:
- These findings provide valuable insights for future research.
- This study contributes to the broader understanding of...
- These results have important implications for...
- Future studies should further explore...
- This provides a useful basis for both theory and practice.
- This finding enriches the existing literature.
- This result has important theoretical and practical significance.

**Scoring**:
- no vague concluding sentence → 0
- mildly generic closing sentence → 0.8
- clearly formulaic conclusion → 1.5
- strongly AI-like summary sentence → 2.0
- repeated summary-style endings across paragraphs → 2.5

---

## Dimension 8: Passive Voice and Nominalization Clusters (Weight: 2.0)

**What detectors look for**: Repeated passive voice and dense noun phrases can create machine-like academic style.

**High-risk patterns**:
- was conducted
- were analyzed
- has been demonstrated
- can be observed
- the implementation of
- the improvement of
- the enhancement of
- the influence of
- the construction of
- the formation of

**Scoring**:
- 0-2 passive or nominalized structures → 0
- 3-4 → 0.5
- 5-6 → 1.0
- 7-8 → 1.5
- 9+ → 2.0

---

## Dimension 9: Abstract-to-Concrete Imbalance (Weight: 2.5)

**What detectors look for**: AI text often contains many abstract nouns but few references to actual variables, hypotheses, tables, coefficients, sample, questionnaire, or model.

**Abstract examples**:
- innovation
- collaboration
- transformation
- mechanism
- effectiveness
- performance
- development
- relationship
- implication
- framework
- pathway
- context

**Concrete examples**:
- Employee-AI Collaboration
- Self-Efficacy
- Work Engagement
- Creative Inspiration
- POS
- Employee Innovative Behavior
- H1/H2/H3
- regression coefficient
- p-value
- sample size
- Table 4.3
- questionnaire item

**Scoring**:
- balanced or concrete-heavy → 0
- abstract-to-concrete ratio around 2:1 → 0.6
- abstract-to-concrete ratio around 3:1 → 1.2
- abstract-to-concrete ratio around 4:1 → 1.8
- abstract-to-concrete ratio above 5:1 → 2.5

---

## Dimension 10: Citation Pattern Regularity (Weight: 2.0)

**What detectors look for**: AI-generated literature reviews often place citations in a regular pattern rather than using them as part of argument development.

**High-risk pattern**:
- citation appears every 2-3 sentences
- citations are repeatedly placed at the end of general claims
- multiple paragraphs follow the same citation rhythm
- cited authors are listed without real connection to the present study

**Scoring**:
- irregular and argument-driven citation use → 0
- 2 citations at similar intervals → 0.5
- 3 citations at similar intervals → 1.0
- 4 citations at similar intervals → 1.5
- 5+ citations with mechanical rhythm → 2.0

---

## Dimension 11: Lexical Flatness and Repeated Academic Verbs (Weight: 2.5)

**What detectors look for**: AI writing often repeats a small group of academic verbs.

**High-risk verb clusters**:
- indicate
- suggest
- show
- demonstrate
- highlight
- emphasize
- reveal
- provide
- enhance
- promote
- contribute to
- play a role in
- explain
- support

**Scoring**:
- varied academic vocabulary → 0
- mild repetition → 0.6
- clear repetition of several academic verbs → 1.2
- repeated verbs across several sentences → 1.8
- same verb clusters repeated across multiple paragraphs → 2.5

---

## Dimension 12: Paragraph-Level Template Structure (Weight: 4.0)

**What detectors look for**: Strict AI detectors are sensitive to repeated paragraph architecture.

**High-risk structures**:
- topic sentence → explanation → citation → implication → conclusion
- definition → citation → general importance → research gap
- result → explanation → theoretical implication → practical implication
- variable description → mechanism explanation → hypothesis support
- broad claim → smooth transition → broad conclusion
- literature summary → limitation → present study

**Scoring**:
- natural paragraph structure → 0
- slightly formulaic structure → 0.8
- clearly template-like paragraph → 1.6
- strongly repeated academic structure → 2.4
- same structure repeated across several paragraphs → 3.2
- highly mechanical paragraph architecture across the section → 4.0

**Strict rule**: A paragraph with a score of 2.4 or above in this dimension should not receive a final paragraph_risk_index below 35%.

---

## Dimension 13: Cross-Paragraph Structural Repetition (Weight: 4.0)

**What detectors look for**: external-detector-style scoring can rise sharply when many paragraphs follow the same structure, even if each paragraph individually looks acceptable.

**High-risk patterns**:
- many paragraphs start with “This study...”, “Previous studies...”, “The results...”
- many paragraphs end with “therefore the hypothesis is proposed”
- repeated literature-review pattern across several variables
- repeated mediation-logic paragraphs with almost the same rhythm
- repeated discussion paragraphs with result → explanation → implication
- neighboring paragraphs perform the same argumentative function even when their wording is different;
- several paragraphs in the same section use different wording but follow the same functional role, such as definition → citation → implication or result → explanation → conclusion.

**Scoring**:
- no clear repetition → 0
- 3-5 paragraphs share a pattern → 1.0
- 6-10 paragraphs share a pattern → 2.0
- more than 10 paragraphs share a pattern → 3.0
- a full chapter or section depends on repeated paragraph templates → 4.0


**Floor coordination rule**:
D13 scoring directly determines cross-paragraph floor application.

- If D13 ≥ 1.0, check whether 3–5 paragraphs share a pattern.
- If D13 ≥ 2.0, cross-paragraph floor should normally be at least 35%.
- If D13 ≥ 3.0, cross-paragraph floor should normally be at least 45%.
- If D13 = 4.0, treat the section as structurally repetitive and apply the whole-section floor.

Do not re-count the paragraph cluster in a later phase. Phase 2 D13 scoring should provide the base data for floor application.

---

## Dimension 14: AI-Like Academic Smoothness / Low Human Friction (Weight: 3.0)

**What detectors look for**: AI prose often has very few awkward turns, interruptions, or slightly uneven thesis-style explanations. It sounds correct, but too clean.

**High-risk patterns**:
- every sentence sounds polished and complete
- no ordinary thesis-style explanation appears
- transitions are too elegant
- paragraph reads like a journal-style mini-summary rather than a master’s thesis
- no natural variation in certainty, emphasis, or sentence weight
- em dash structures that make the sentence sound elegant, compressed, or machine-polished.

**Scoring**:
- natural thesis style → 0
- slightly polished → 0.8
- clearly over-polished → 1.5
- very smooth and generated-sounding → 2.2
- almost no human writing friction → 3.0

---

## Dimension 15: Thesis-Section Template Dependency (Weight: 3.0)

**What detectors look for**: Some thesis sections are especially vulnerable to AI-style templates.

**High-risk section patterns**:
- literature review: definition → author citation → importance → research gap
- hypothesis development: variable explanation → mechanism → hypothesis
- empirical result: coefficient → significance → hypothesis supported → brief implication
- discussion: result → consistency with prior studies → theoretical implication
- conclusion: contribution → practical implication → limitation → future research

**Scoring**:
- section-specific structure is natural → 0
- mild template dependency → 0.8
- clear template dependency → 1.5
- strong template dependency → 2.2
- repeated section template across many paragraphs → 3.0


---

## Dimension 16: Methodological Template Intensity (Weight: 4.0)

### D16/D17 Boundary Rule
- D16 detects repeated methodological and empirical reporting phrases at the sentence level.  
- D17 detects repeated reporting sequences at the paragraph-group or section level.  
- If both dimensions are high, D16 explains the phrase-level template risk, while D17 explains the sequence-level architecture risk.

Do not merge D16 and D17 into one diagnosis. D16 should be used to identify repeated wording templates, while D17 should be used to identify repeated reporting order or repeated paragraph-group architecture.

### What detectors look for
D16 focuses on repeated sentence-level reporting templates in methodology, measurement, reliability, validity, and empirical-result sections.

- Detect the frequency of the following patterns:
  - "The variable is defined as" / "refers to"
  - "This study adapts the scale from"
  - "The final scale includes X items"
  - "The questionnaire was divided into"
  - "The purpose of this test is"
  - "The results show that"
  - "This indicates that"

### Scoring unit

D16 is first detected at the paragraph-group or subsection level, then assigned to the affected paragraphs.

Scoring:
- 0–3 occurrences in the paragraph group = 0
- 4–6 occurrences in the paragraph group = 1.5
- 7–9 occurrences in the paragraph group = 2.5
- ≥10 occurrences in the paragraph group = 4.0

If one individual paragraph contains 3 or more methodology/reporting templates, assign at least 1.5 to that paragraph even when the paragraph-group count is lower.

If D16 ≥ 2.5, Section-Level Mandatory Rewriting must be triggered. Multiple parallel paragraphs are not allowed to retain the same functional order.

---

## Dimension 17: Predictable Reporting Sequence (Weight: 3.0)
- Detect whether the following three-step or four-step sequences are repeatedly used:
  - Dependent variable: definition → scale source → number of items
  - Hypothesis: Variable A → mechanism → hypothesis
  - Empirical results: test purpose → threshold → numerical value → conclusion
  - Discussion: result → explanation → theoretical implication → practical implication
- Scoring：
  - The same sequence appears twice in the same chapter = 1.5
  - 3–4 occurrences = 2.5
  - ≥5 occurrences = 3.0
  - When D17 is triggered, assign the D17 score to all paragraphs that participate in the repeated reporting sequence, not only to the last paragraph where the repetition is observed.
  
- If D17 ≥ 2.5, sequence-disruption rewriting must be planned. At least one affected paragraph should change its entry point or the order of its reporting steps while preserving every substantive step and preserving or increasing word count. Do not merge sentences merely to shorten or compress the reporting sequence (Principle 4).


---

## Qualitative-Only Dimensions (D18–D21)

These four dimensions apply ONLY to qualitative papers (interviews, case studies, grounded theory, ethnography, phenomenology, thematic / discourse / content analysis) and to the qualitative portions of mixed-methods papers. Do NOT score them for purely quantitative papers. They capture AI patterns that are specific to qualitative writing and that the quantitative-oriented D1–D17 do not detect well.

Before scoring D18–D21, confirm the paper (or section) is qualitative. If it is quantitative, skip these and rely on D1–D17.

## Dimension 18: Transition-Sentence Templating in qualitative reporting (Weight: 3.0)
- Detect mechanical participant-to-participant transitions that make every account read the same way.
- Signals:
  - "Participant A mentioned ... Similarly, Participant B also ..."
  - repeated "Similarly, / Likewise, / In addition, / Moreover," chaining of participant accounts
  - every participant introduced with the same verb ("mentioned / stated / noted / emphasized")
- Scoring:
  - 2 such mechanical transitions in a section = 1.5
  - 3–4 = 2.5
  - ≥5 = 3.0
- If D18 ≥ 2.5, transition de-templating (T25) must be applied: differentiate how accounts connect, using contrast and relationship, not a fixed "Similarly, X also" chain. Use only what participants actually said in the paper.

## Dimension 19q: Theme-Presentation Uniformity (Weight: 3.0)
- Detect whether every theme paragraph follows an identical skeleton, e.g. "Theme N: Name. This theme captures ... Participants expressed ...".
- Signals:
  - each theme opens with "Theme N:" + the same sentence shape
  - each theme runs definition → generic participant statement → generic interpretation in the same order
- Scoring:
  - 2 identically-structured theme paragraphs = 1.5
  - 3 = 2.5
  - ≥4 = 3.0
- If D19q ≥ 2.5, theme-introduction diversification (T26) must be applied: vary each theme's entry point (from a quote, from a contradiction with the literature, from an analytic puzzle, from a counter-case), using only existing content.

(Note: this is labelled D19q to avoid confusion with any quantitative use; it is a qualitative-only dimension.)

## Dimension 20: Researcher-Voice Absence (Weight: 4.0)
- Detect whether the analysis only reports what participants said, with no researcher interpretation, decision trace, or analytic judgment anywhere — a flatness that reads as machine-summarised.
- Signals:
  - long stretches of "participant said X. This shows Y." with no analytic movement
  - no explanation of how codes/themes were derived from the data
  - no positionality or reflexivity even in methodology/analysis sections where it is expected
- Scoring:
  - some sections lack any researcher voice = 1.5
  - most analysis sections lack it = 2.5
  - the entire findings/analysis is voice-absent = 4.0
- If D20 ≥ 2.5, T27 (researcher-reflection RELOCATION, via the T19-B qualitative matrix) may be used ONLY when existing researcher judgment, positionality, coding-decision explanation, or analytic-process material can be located elsewhere in the thesis and relocated or lightly integrated here. If no such source material exists, do NOT manufacture researcher voice — use structure-preserving techniques instead. NEVER fabricate researcher feelings, non-verbal observations, or interview details not in the original (both AI-flagged and an integrity violation).

## Dimension 21: Participant-Quote Balance Uniformity (Weight: 2.0)
- Detect artificially even citation: every participant quoted the same number of times, every quote roughly the same length, every theme citing the same count of participants.
- Signals:
  - one quote per participant per theme, all of similar length
  - no participant is ever absent from a theme
  - no quote is notably longer or shorter than the others
- Scoring:
  - citation is noticeably uniform = 1.0
  - strongly uniform across the whole findings = 2.0
- If D21 ≥ 1.0, D21 is report-first by default: flag the uniform-citation pattern for manual evidence review and do NOT rewrite quotation distribution automatically. The only action allowed before manual confirmation is quote-framing variation (T28), which may vary ONLY the narrative introduction, ordering, and surrounding interpretation of existing quotations where the existing data supports it. Do NOT change quote count, quote length, participant distribution, or theme coverage, and do NOT remove, add, redistribute, or selectively suppress participant quotations, and do NOT claim an absence/silence the paper does not document. If no safe framing variation is possible, mark "D21 action = Flagged only — no rewrite applied to quotation count, length, participant distribution, or theme coverage; only surrounding framing may be varied, and only when the existing data supports it." Quotation frequency, length, and presence are research evidence, not style.


---
## Deep AI Writing Pattern Audit

In addition to the 17 scoring dimensions, check for deeper AI-writing patterns. These patterns may increase risk even when phrase-level scores are not very high.

1. Significance Inflation
   - Risk: ordinary findings are described as highly important, crucial, valuable, or broadly significant.
   - Check: if deleting “important,” “significant,” or “valuable” does not change the meaning, the phrase may be inflated.
   - Related dimensions: D5, D7, D14.

2. Synonym Cycling
   - Risk: the same concept is renamed too many times to avoid repetition.
   - Rule: core variables and theoretical terms should remain consistent.
   - Related dimensions: D11, D15.

3. Rule of Three
   - Risk: arguments are repeatedly grouped into three balanced items.
   - Examples: “X, Y, and Z”; “not only X, but also Y, and even Z.”
   - Rule: do not force every explanation into a three-part structure.
   - Related dimensions: D4, D6, D12, D13.

4. Vague Attribution
   - Risk: phrases such as “previous studies show,” “research has found,” or “scholars generally believe” appear without clear citation support.
   - Rule: either connect the claim to an existing citation or state it more cautiously.
   - Legitimate-citation carve-out (false-positive guard): before flagging an attribution phrase, check the same sentence and its immediate neighbours for a real citation. If a genuine reference is present — an author–year form like "Smith (2019)" or "Smith and Jones (2020)", an "et al." form, "according to [Name] (Year)", a parenthetical "(Author, 2019, pp. 35–37)", a named journal, a "doi:", or a URL — then the attribution is SOURCED, not vague: do NOT flag it and do NOT rewrite it. Flag only when the attribution genuinely floats free of any citation, or when the same vague phrase recurs as a template across paragraphs. This protects normal literature-review prose, where attribution phrasing legitimately accompanies citations.
   - Related dimensions: D10, D12.

5. Formulaic Limitation or Future Research Pattern
   - Risk: the limitation or future research section uses generic sentences that can fit any thesis.
   - Rule: connect limitations and future research to the actual sample, variables, method, model, or data source.
   - Related dimensions: D7, D12, D15.

6. Hanging Analysis
   - Risk: one sentence adds several abstract consequences after the main claim.
   - Examples: “thereby improving..., further promoting..., and ultimately contributing to...”
   - Rule: split the sentence, or replace low-information abstract consequences with specific scope, evidence, or reasoning already present in the thesis. Do not reduce paragraph word count; if wording is removed, compensate within the same paragraph from existing thesis content (Principle 4 / Gate F).
   - Related dimensions: D3, D5, D12, D14.

7. Generic Positive Conclusions
   - Risk: broad claims such as “this study has important theoretical and practical significance.”
   - Rule: replace with a specific contribution tied to actual findings.
   - Related dimensions: D5, D7, D15.

8. False Range
   - Risk: broad range phrases such as “from theory to practice,” “from individual to organization,” or “from micro to macro” without actual coverage.
   - Rule: name the actual scope. If the range phrase is removed, compensate in the same paragraph with existing thesis-specific scope, sample, variable, method, or finding information so that the paragraph word count does not fall (Principle 4 / Gate F).
   - Related dimensions: D5, D9, D14.

9. Fragmented-Header Restatement
   - Risk: a section/sub-section heading is immediately followed by a one-line sentence that only restates the heading before any real content begins (e.g. "3.2 Data Analysis" followed by "This section presents the data analysis."). It is a low-information warm-up sentence that adds nothing and reads as machine-padded.
   - Rule: do NOT delete the heading and do NOT shrink the paper (Principle 4). Either fold the empty restatement into the substantive first sentence so the opening carries real information (what was analysed, with which method, on which data), or expand it into a content-bearing sentence drawn from material already in the section. Never move or absorb the heading (Principle 6, Gate G).
   - Caution: a genuine orienting sentence that previews specific, real content ("Section 3.2 reports the measurement-model fit before the structural results") is NOT this pattern — leave it.
   - Related dimensions: D12, D14, D15.

10. Uniform Predicate-Position Hyphenation
   - Risk: a low-strength lexical signal. AI prose tends to hyphenate generic descriptive compounds uniformly in every position, including predicate position ("the framework is data-driven", "the team is cross-functional"), where many human writers drop the hyphen ("the framework is data driven"). Treat as a weak signal only, useful when it co-occurs with stronger tells.
   - Rule (narrow, and strictly SUBORDINATE to Gate D): this applies ONLY to generic, non-technical descriptive compounds in predicate position. It NEVER touches protected technical terms, variable names, established hyphenated constructs, or attributive-position compounds. Terms such as "self-efficacy", "employee-AI", "AI-generated", "cross-domain", "human-AI", and any compound modifier before its noun ("a data-driven framework") keep their single hyphen exactly, always (Gate D). When in doubt, do not de-hyphenate. This is an optional, low-priority micro-edit; skip it whenever it risks any conflict with Gate D's hyphen-protection.
   - Related dimensions: D11.


## Cluster-Density False-Positive Guard

A single weak signal in isolation is NOT a reliable indicator of AI authorship. Flagging isolated signals over-edits clean human prose, and over-editing a real thesis toward uniform polish is itself a leading way to RAISE AI-detector risk (see the Author Style Baseline Rule and the `cluster_density_tiering_to_reduce_false_positives` design). Require a CLUSTER (roughly three or more co-occurring signals within the same span) before treating a passage as AI-risk on these weak signals alone:

- perfect grammar and consistent style on their own (many authors are competent or have been edited; polish is not proof);
- formal or academic vocabulary on its own (the system targets *specific* AI-favored words and collocations, not all formal vocabulary — do not flatten a precise term just because it sounds advanced);
- a single common connective ("however", "moreover", "therefore") in isolation — only chains of formulaic connectors count (D2);
- one em dash, one curly quote, or one instance of title case in isolation (these are weak and often style-guide-driven; em dashes are handled by Gate D regardless, but a single one is not a paragraph-level verdict);
- a single unsourced general statement (most prose is unsourced; vague attribution is a tell only when it recurs or replaces an available citation — see Deep Audit item 4);
- one tricolon / rule-of-three where the third item carries real, distinct content (tricolons are an ancient human device; flag only padded or near-synonym triads — Deep Audit item 3).

Human signals to PRESERVE (do not "fix" them — they are what keeps the score down):

- concrete, hard-to-fabricate specifics that already exist in the paper: exact sample sizes, instrument names, coefficients, dates, site details. Keep them verbatim; never generalise them away and never invent new ones (Gate B, Principle 4);
- genuine variety in sentence length and the author's real connective habits (D4 / Author Style Baseline);
- the author's mild, consistent non-native / Chinese-English features (article and preposition choices, slight awkwardness) — protective human signals, not errors to fix (Gate G, Gate I);
- real author-side asides, caveats, decision rationales, and limitations that are already present — relocate or lightly rephrase them (T19), never delete them to "clean up";
- uneven section and paragraph lengths the author actually wrote — do not regularise them into a uniform template.

When in doubt, look for clusters, not isolated tells, and prefer leaving genuine human prose alone over polishing it.


## Pattern Tagging System

In addition to D1–D17 scores, assign 1–3 pattern tags to each paragraph.

Suggested tag groups:

| Tag Group | Meaning | Examples |
|---|---|---|
| C | Content pattern | significance inflation, vague attribution, generic positive conclusion |
| L | Language pattern | formulaic transitions, over-qualification, repeated academic verbs |
| S | Structure pattern | perfect logical closure, template paragraph, repeated three-part structure |
| T | Tone pattern | over-objective voice, broad background opening, overly polished thesis tone |
| F | Formatting pattern | unnecessary bolding, excessive lists, overuse of em dashes |
| ST | Statistical pattern | low burstiness, uniform sentence length, predictable vocabulary |
| MT | Methodology template | variable definition, scale source, item count |
| ER | Empirical-result template | test purpose, threshold, result, conclusion |
| HY | Hypothesis template | variable → mechanism → hypothesis |
| LR | Literature-review template | definition → citation → implication |
| CN | Conclusion template | finding → contribution → implication → future research |

Example:
Pattern Tags: D12+MT01, D13+CR02, D14+EL01

Mandatory rule:
- Pattern tags must not replace D1–D17 scoring.
- Pattern tags must appear in the Phase 2 Detection Report.
- Pattern tags must guide Phase 4.5 technique selection.

Scoring discipline (anti-inflation — applies to both pattern tags and D1–D21 scoring):
- Pattern stacking: when several weak signals land on the SAME phrase or sentence (e.g. boldface + a significance word + an em-dash aside on one clause), treat them as ONE strong cluster finding, not as several independent hits. Record it once under its primary dimension and note the secondary contributors in the same entry; do not list the identical span under multiple dimensions to inflate the paragraph score. Distinct spans are scored separately as normal.
- Count before claiming: before asserting that any pattern is "overused", "repeated", "uniform", or "clustered" (em dashes, a connective, copula-avoidance verbs, rule-of-three, uniform sentence length, repeated openers), actually COUNT the occurrences relative to the length of the paragraph or section. Density relative to length is the signal — not an absolute count and not an impression. A single occurrence in an otherwise varied passage is normal and is not, by itself, a tell (see the Cluster-Density False-Positive Guard). State the count in the evidence when the score depends on it.

### Tag-to-Rewrite Link

Pattern tags must be linked to rewrite action.

Examples:

| Pattern Tag | Rewrite Direction |
|------------|------------------|
| C: Significance inflation | Replace broad value claim with finding-specific statement |
| L: Formulaic transition | Replace with a more precise logical connector, integrate it into the next substantive clause, or remove it only when it carries no meaning and same-paragraph compensation preserves word count |
| S: Template paragraph | Rebuild paragraph architecture |
| T: Over-polished thesis tone | Use plainer thesis wording |
| F: Overuse of em dash/listing | Reduce punctuation-driven structure |
| ST: Uniform rhythm | Vary sentence rhythm carefully |

A tag without a rewrite action is not useful for execution.

---   

## Weighted Scoring Table

| Dimension | Weight | Max Score |
|-----------|--------|-----------|
| Repetitive Sentence Starters | 3.0 | 3.0 |
| Formulaic Transitions and Connector Chains | 3.0 | 3.0 |
| Over-Smooth Logical Flow | 3.0 | 3.0 |
| Uniform Sentence Length and Rhythm | 2.5 | 2.5 |
| Generic Academic Phrasing | 3.0 | 3.0 |
| Academic Hedging or Balanced Claims | 2.0 | 2.0 |
| Conclusion-Style Generalizations | 2.5 | 2.5 |
| Passive Voice and Nominalization Clusters | 2.0 | 2.0 |
| Abstract-to-Concrete Imbalance | 2.5 | 2.5 |
| Citation Pattern Regularity | 2.0 | 2.0 |
| Lexical Flatness and Repeated Academic Verbs | 2.5 | 2.5 |
| Paragraph-Level Template Structure | 4.0 | 4.0 |
| Cross-Paragraph Structural Repetition | 4.0 | 4.0 |
| AI-Like Academic Smoothness / Low Human Friction | 3.0 | 3.0 |
| Thesis-Section Template Dependency | 3.0 | 3.0 |
| Methodological Template Intensity | 4.0 | 4.0 |
| Predictable Reporting Sequence | 3.0 | 3.0 |
| **TOTAL** | | **49.0** |

---
### Definition of Strong AI Dimension

A dimension is considered a strong AI dimension when its score reaches at least 60% of its maximum value.

Examples:
- D1 / D2 / D3: score ≥ 1.8 out of 3.0
- D4 / D9 / D11: score ≥ 1.5 out of 2.5
- D6 / D8 / D10: score ≥ 1.2 out of 2.0
- D12 / D13: score ≥ 2.4 out of 4.0
- D14 / D15: score ≥ 1.8 out of 3.0
- D16: score ≥ 2.4 out of 4.0
- D17: score ≥ 1.8 out of 3.0
- Qualitative supplement: D18 ≥ 1.8, D19q ≥ 1.8, D20 ≥ 2.4, D21 ≥ 1.2 indicate strong qualitative-specific risk

For D12 and D13, a score at or above the strong threshold should receive special attention because paragraph architecture and cross-paragraph repetition are highly sensitive indicators.

---

## Paragraph-Level Internal AI-Risk Estimate Formula

Note on terminology: the value computed here (`paragraph_risk_index`) is an INTERNAL heuristic risk estimate on a 0–100 scale, not a statistical probability and not an external-detector probability. All internal score variables in this skill (`paragraph_risk_index`, `raw_paragraph_risk`, `overall_risk_index`, `average_paragraph_risk`, `final_qualitative_paragraph_risk`, and the `qualitative_supplement_AI` supplement) are heuristic risk estimates, not probabilities. They locate and prioritise risk; they never predict or guarantee what an external detector (Turnitin/CNKI/etc.) will report. Forbidden wording in user-facing reports (unless quoting an external detector's own label): "AI probability", "probability of AI writing", "will pass detection", and "detector score reduced" without comparable external re-test evidence. Use instead: "internal risk estimate", "risk pattern located", and "candidate version prepared for external re-test".

Calculate the raw score first:

```text
raw_paragraph_risk = min(dimension_score / 49.0, 1.0) × 100%
```

Then apply strict floors:

```text
paragraph_risk_index = max(
  raw_paragraph_risk,
  pattern_floor,
  repeated_structure_floor,
  section_template_floor,
  d16_d17_trigger_floor,
  multi_detector_trigger_floor
)
```

### Qualitative supplement score (qualitative sections only)

For qualitative sections and the qualitative portions of mixed-methods studies, compute a SEPARATE supplement from the qualitative-only dimensions (D18 = 3.0, D19q = 3.0, D20 = 4.0, D21 = 2.0; supplement total = 12.0):

```text
qualitative_supplement_AI = min((D18 + D19q + D20 + D21) / 12.0, 1.0) × 100%
final_qualitative_paragraph_risk = max(paragraph_risk_index, qualitative_supplement_AI)
```

Report the 49-point core score and the 12-point qualitative supplement SEPARATELY. Do not silently merge them into one undocumented denominator. The core D1–D17 review is always completed; for a purely qualitative passage, D16 and D17 may be scored 0 / Not Applicable with a stated reason when there is no methodology-template or reporting-sequence risk.

### Pattern Floor

- 2 or more strong AI dimensions: minimum 18%
- 3 or more strong AI dimensions: minimum 28%
- 4 or more strong AI dimensions: minimum 38%
- Paragraph-Level Template Structure ≥2.4: minimum 35%
- Paragraph-Level Template Structure ≥2.4 and Over-Smooth Logical Flow ≥1.5: minimum 42%
- Paragraph-Level Template Structure ≥3.2 and Generic Academic Phrasing ≥2.0: minimum 50%
- Entire paragraph reads like generated academic synthesis: minimum 60%

### Repeated Structure Floor

- 3-5 paragraphs with similar opening or closing structure: affected paragraphs minimum 25%
- 6-10 paragraphs with similar opening or closing structure: affected paragraphs minimum 35%
- More than 10 paragraphs with similar opening or closing structure: affected paragraphs minimum 45%
- Same paragraph architecture repeated across a full section: affected paragraphs minimum 50%

### Section Template Floor

- Literature review repeatedly follows definition → citation → implication: minimum 35%
- Hypothesis development repeatedly follows variable explanation → mechanism → hypothesis: minimum 40%
- Empirical result repeatedly follows coefficient → significance → support: minimum 35%
- Discussion repeatedly follows result → explanation → implication: minimum 42%
- Conclusion repeatedly uses broad theoretical/practical implications without concrete link to findings: minimum 45%

Final paragraph_risk_index is capped at 100%.

---
## Rewrite-Relevant Diagnosis Requirement

Detection is not complete until the diagnosis can guide rewriting.

For each paragraph, the detection report must include:

```text
Paragraph ID:
Section Type:
Raw internal risk estimate (raw_paragraph_risk):
Final paragraph_risk_index:
Hit Dimensions:
Strong AI Dimensions:
Pattern Floor Applied:
Primary Rewrite Target:
Required Techniques:
Protected Elements:
```
Do not report only a percentage.

The purpose of detection is to determine what must be rewritten. If no hit dimensions or required techniques are listed, the detection is incomplete.


---

## Scope-Aware Internal Risk Index

This index applies only to the actually diagnosed scope. Use the name `overall_risk_index` only for a fully diagnosed full-document scope; for a chapter, batch, or fragment scope, report it as the corresponding target-unit internal risk estimate (`target_chapter_risk_index`, `batch_risk_index`, or `fragment_risk_index`).

Calculate:

```text
average_paragraph_risk = average(paragraph_risk_index across included paragraphs)
high_risk_share = percentage of included paragraphs with paragraph_risk_index ≥ 40%
medium_risk_share = percentage of included paragraphs with paragraph_risk_index ≥ 25%
section_repetition_score = repeated-structure penalty within the diagnosed scope (document level only when Scope = Full document)
```

Formula:

```text
calculated_scope_risk_index =
(0.45 × average_paragraph_risk)
+ (0.25 × high_risk_share)
+ (0.15 × medium_risk_share)
+ (0.15 × section_repetition_score)
```

All four inputs must be expressed on a 0–100 scale, not a 0–1 decimal scale.
For example, if 47.5% of paragraphs are high-risk, use 47.5, not 0.475.

section_repetition_score is a 0–100 scope-level score based on repeated structures within the diagnosed scope:
- 0–20: little repeated structure
- 21–40: mild repetition
- 41–60: clear repetition across one section
- 61–80: repeated structures across several sections
- 81–100: repeated architecture across most of the thesis

Apply the document floor:

```text
scope_risk_index = max(
  calculated_scope_risk_index,
  scope_pattern_floor
)
```

### Document Pattern Floor

- More than 25% of paragraphs share similar openings or endings: minimum 25%
- More than 35% of paragraphs follow section templates: minimum 35%
- Literature review and hypothesis sections both show repeated template architecture: minimum 40%
- Smooth AI-style paragraph chains appear across several chapters: minimum 45%
- External detector score is known and much higher: minimum 70% of the external detector score unless there is a clear reason to exclude it

Example:

```text
If Turnitin AI = 48%, recalibrated internal score should normally not be below 33.6%.
```

Final overall_risk_index is capped at 100%.

---

## Detection Thresholds

| Scope risk index (overall / target unit) | Judgment |
|------------------|----------|
| ≤8% | Low risk, but still manually check repeated structures |
| 9-15% | Mild risk; revise repeated openings and endings |
| 16-25% | Moderate risk; revision recommended |
| 26–29% | Near target by internal estimate only; prepare for comparable external re-test. Do not mark DONE unless the external detector score for the same scope is below target |
| 30–35% | At or above target; continue revision and escalation |
| 36-50% | Very high risk; strong rewrite required |
| >50% | Severe risk; major rewrite required |

## Important Calibration Note

If the internal score is below 10% but an external detector reports 40% or higher, the internal method has failed to capture structural repetition or reporting-sequence risk. In that case, do not trust the raw score. Re-score the paper using Dimensions 12–17 and apply the document pattern floor.
