# Rewrite Methods: Multi-Detector Reduction of AI-Writing Features for Master’s Thesis Text

## ⚠ Overriding rule: minimal edit, never regenerate, never shrink (read before any technique below)

Real multi-round testing showed that "raising rewrite intensity" and regenerating paragraphs as fluent new prose makes the external AI score WORSE, not better — one chapter rose from 36% to 100% after heavy rewriting. Fluent AI-generated academic prose carries strong AI features by construction.

Therefore every technique in this file must be applied as a MINIMAL EDIT to the existing sentences:
- substitute individual words, reorder clauses, split long sentences, recast sentence structure, and relocate or integrate researcher-trace material drawn from existing content;
- keep as much original human wording as possible — that wording is what keeps the score down;
- every output sentence must trace back to a specific original sentence (or be a permitted researcher-trace/breakpoint sentence based on existing content);
- NEVER regenerate a whole paragraph or section as new prose, even for the highest-risk paragraphs;
- "aggressive structural rewrite" means aggressively REORDERING and RE-SEGMENTING existing sentences, never rewriting them into new text.

⚠ WORD COUNT MUST NOT FALL. The most important constraint for thesis use: AI-score reduction must NEVER be done by compressing, merging, deleting, shortening, or condensing. A thesis has a minimum word count and shrinking it is a failure even if the AI score drops.
- Every rewritten paragraph must be ≥ the original length (target 0% to +15%). Over-cap exception (Principle 4): the +0% to +15% growth target applies only when the original paragraph is within the 200-word / 12-sentence readability cap. If the original paragraph already exceeds that cap, do not force further growth — preserve all substantive content, add no filler, keep length no greater than the original unless a source-supported clarification requires it, prefer splitting at a natural break, and record Gate F as "Pass — no substantive shrinkage; original already exceeded the readability cap." This never licenses removing or condensing content.
- Wherever a technique below says "compress", "condense", "shorten", "merge", "trim", or "remove repeated explanation", REINTERPRET it as: break the repeated pattern by RESTRUCTURING and ADDING SPECIFICITY, keeping length equal or greater. Never cut content to break a template.
- Splitting one sentence into two is encouraged. Merging two sentences into one is NOT allowed as a routine AI-risk technique; it IS allowed only to repair a fragment, an accidentally split clause, or a thin sentence created during revision (Gate H repair exception).
- If de-templating removes words, compensate within the same paragraph by adding concrete detail or a researcher-view sentence drawn from existing content.
- This rule overrides every "compress/merge/shorten" instruction anywhere in this file.

Also non-negotiable:
- The goal is to bring every externally measured target unit below the target threshold (default 30%), usually one chapter at a time. A whole-document target applies only when a comparable whole-document external score is available. "Lower than before" is progress, not completion. Keep rewriting and escalating until the current measurable target unit is below target, or until a documented PAUSED/BLOCKED condition is reached; never present an above-target version as final.
- Never merge paragraphs and never touch section headings. Section/sub-section headings (e.g. "1.1 Research Background", "5.2.1 ...") stay on their own line, with paragraph breaks before and after preserved exactly. Cross-paragraph repetition is reduced by differentiating neighbouring paragraphs, not by combining them.
- Keep every rewritten paragraph readable: about 160 words / 9 sentences as a soft target, never above 200 words / 12 sentences. If risk reduction seems to need a longer block, keep the original paragraph breaks. A 200-word, 18-sentence merged block is a defect even if its AI score is low.
- Keep every sentence grammatically complete and a sensible length. Never split a subordinate clause or a noun list into its own "sentence" (no "When employees interact with AI in daily work." or "Service methods, management practices, and ways of solving problems."). Never chop prose into choppy ~10-word fragments. Conversely, never write tangled sentences over ~30 words or with more than two subordinate clauses — split those into two complete sentences. (Principle 8 / Gate H.)
- Keep grammar correct, especially subject–verb agreement wherever a sentence is split or its subject changed. Never reduce AI features by inserting grammar errors. (Principle 9 / Gate I.)
- Never use "--" (double hyphen). Keep hyphenated compounds (employee-AI, self-efficacy) with one hyphen and keep en dashes in ranges. Replace a removed em dash with a comma, colon, semicolon, parentheses, or two sentences. (Gate D.)
- Never insert out-of-place meta-commentary such as "This detail was included to improve measurement precision." Every sentence, including researcher-trace sentences, must fit the local argument and connect to its neighbours. (Principle 9 / Gate J.)
- BACK-TRANSLATION IS FORBIDDEN. Do NOT translate the text to another language and back (e.g. Chinese → English → rewrite → Chinese), and do not paraphrase a whole paragraph by round-tripping it through translation. Back-translation is a form of whole-paragraph regeneration: it destroys the original human wording and produces fresh machine-distributed text, which is exactly the failure mode that drove a chapter from 36% to 100%. It violates the minimal-edit rule (Principle 2). Reduce AI features only by minimally editing the existing sentences in place.
- If a chapter is still above target after a round, do not stop — move up the escalation ladder: sentence-level → rhythm → paragraph architecture → reporting-sequence/template breaking → source-extracted researcher-trace relocation (T19; relocate existing author reasoning only, at most one trace per paragraph, never invent voice) → functional reorganisation. Every rung still obeys minimal-edit and word-count preservation.
- Never rewrite a chapter that is already below the target (default 30%); it is done.
- A rewrite that scores higher than the chapter's lowest-ever version is discarded; restore the lowest-ever version, then try the next escalation rung.
- Work one chapter per round and have the user re-test before continuing.

## Research design and discipline adaptation (apply before choosing techniques)

First identify the research design, because techniques and dimensions differ:
- Quantitative (survey, SEM, regression, ANOVA, experiment, hypothesis-testing): score D1–D17; use T1–T24 with the quantitative branches (T19-A, T24-A).
- Qualitative (interviews, case study, grounded theory, ethnography, phenomenology, thematic/discourse/content analysis): for ENGLISH qualitative/mixed-methods text, complete the core D1–D17 evaluation, marking D16 and D17 as 0 / Not Applicable with justification where no methodology-template or reporting-sequence risk exists, and additionally evaluate D18, D19q, D20, D21 as a separate qualitative supplement. For CHINESE qualitative/mixed-methods text, do NOT mechanically apply the English D1–D17 lexical/syntax dimensions; use the Chinese-text AI-risk route plus shared structure-level checks, and apply the qualitative concerns behind D18–D21 in adapted Chinese-route form (transition templating, theme-presentation uniformity, researcher-voice absence, quote-balance uniformity), reporting the result as `chinese_paragraph_risk_estimate`. In both languages, use the qualitative branches (T19-B, T24-B) and qualitative-only techniques T25–T28, and do not apply quantitative-template logic (variable→scale→items, coefficient→significance) to qualitative text.
- Mixed-methods: apply quantitative dimensions/techniques to the hypothesis/measurement/statistical parts and qualitative ones to the interview/coding/thematic parts.

Discipline note (secondary, lighter touch):
- Humanities: watch for over-ornate literary language; reduce stacked adjectives and flowery phrasing (this is the over-polished phrase rule, Gate J).
- Social science: methodology sections template easily; surface the researcher's real decision process from existing content (T19/T27).
- STEM / quantitative: results sections read too uniform; prefer reporting-sequence reordering (T18) and existing-data-anchored notes (T19-A), never fabricated "surprise".
In all disciplines the integrity and no-fabrication rules below are absolute.

## Purpose

This file combines the original rewriting methods for reducing AI-generated writing patterns with a thesis-specific revision prompt. It is designed for revising English master’s thesis text, especially sections involving literature review, hypothesis development, empirical results, conclusions, and implications.

This version is intentionally stricter than a normal AI-style rewrite guide. It should be used when the internal skill score is much lower than an external AI detector result, from one or more external AI detection systems.

If the same paper receives a low internal score but a high external AI detector score, assume that the problem is not only wording, but also repeated paragraph architecture, over-smooth academic logic, and section-level template dependency.

Important note on aggressive techniques: this file contains some aggressive or over-colloquial techniques inherited from a general-purpose rewrite guide. For academic thesis text these are mostly UNSAFE and must be used only as a last resort, only on a chapter that is still high after lighter edits, and never by regenerating prose. When in doubt, do not use them — prefer the lightest edit that works.

This file is for reducing AI-writing-risk patterns only. It is not intended for plagiarism reduction, similarity-score reduction, or Turnitin Similarity Index optimization.

## Universal External-Risk Calibration Protocol

Use this protocol when the internal skill score is clearly lower than one or more external AI detector results.

In this situation, do not assume the paper is low-risk. The internal score may be under-sensitive. Revisions must target hidden structural patterns, not only obvious AI phrases.

Example:
- Internal skill score: 4.5%
- External detector score: 48% / 49.9%

Revisions must target hidden structural patterns, not only obvious AI phrases.

Apply the following rules:

1. **Raise rewrite DEPTH of structural targeting, not fluency of rewriting**
   - Treat all paragraphs with repeated thesis structure as at least medium risk.
   - Treat externally flagged sections as high-sensitivity sections.
   - Pay special attention to literature review, hypothesis development, methodology, research design, questionnaire design, sample screening, empirical result reporting, discussion, and conclusion sections.
   - Do not skip paragraphs only because they have few obvious AI phrases.
   - "Higher intensity" means deeper REORGANISATION of existing sentences (reorder, re-segment, change entry point, relocate/integrate existing researcher-trace material), NOT regenerating the text. Increasing fluency makes the score worse.

2. **Rewrite by section pattern**
   - Literature review: break the repeated definition → citation → implication pattern.
   - Hypothesis development: avoid repeating variable explanation → mechanism → hypothesis.
   - Discussion: avoid repeating result → explanation → implication.
   - Conclusion: avoid repeated theoretical/practical contribution sentences.
   - Methodology: break the repeated variable definition → scale source → item count pattern.
   - Empirical results: break the repeated test purpose → threshold → result → hypothesis supported pattern.

3. **Rewrite paragraph architecture, not only vocabulary**
   - Change sentence order where safe.
   - Split long sentences to reduce uniform rhythm (do not merge, which shortens the text).
   - Rewrite repeated opening and closing structures into varied forms of equal or greater length (do not delete them).
   - Replace generic academic conclusions with findings-specific explanation.
   - Add reasoning visibility using only information already present in the thesis. Every added reasoning sentence must name its original source sentence/location (T19/T29 Source Trace) or be marked "author confirmation needed" instead of being written.

4. **Use a calibration floor**
   - If a comparable external AI detector result for the same scope, or a clearly mapped broader body-text scope, reports 40% or higher, apply the external-risk floor to structurally linked target body sections. Do NOT apply the floor directly when the detector scope includes references, appendices, questionnaire items, tables, figure captions, copied prompts, or acknowledgements, unless those units are separately mapped and intentionally included in the target scope. If the detector result is verbal-only, scope-unclear, or non-comparable, treat it as calibration evidence only and do not apply a direct paragraph-level floor.
   - When uncertain, apply deeper structural targeting while keeping wording changes minimal. Do not increase fluency, do not regenerate paragraphs, and do not add unsupported reasoning.
   - A revised paper should be checked against both phrase-level and structure-level patterns.

---
## High External-Detector Rewrite Mode

When any external AI detector report shows high AI risk, do not treat the task as normal paragraph polishing.

In this mode, the main target is not only AI-like wording, but repeated academic architecture across sections.

Apply the following rules:

1. Plan by section pattern, but execute by sentence- and paragraph-group minimal edits — never regenerate a section as a block.
   - Check whether several paragraphs in the same section follow the same structure.
   - If they do, change the paragraph architecture, not only the wording.

2. Prioritize sections based on external detector evidence:
   - sections with strong external detector evidence or repeated high-risk signals across one or more reports;
   - sections with long continuous highlighted fragments;
   - methodology, research design, questionnaire design, sample screening, reliability testing, validity testing, and empirical result reporting when flagged externally;
   - hypothesis development sections with repeated variable → mechanism → hypothesis structures;
   - conclusion and implication sections with generic contribution or future-research templates;
   - introduction, research significance, and chapter arrangement sections with repeated background → gap → value structures;
   - literature review sections with repeated definition → citation → implication patterns.

3. For each high-risk section, identify repeated templates before rewriting:
   - Literature review: definition → citation → implication
   - Hypothesis development: variable explanation → mechanism → hypothesis
   - Results discussion: result → explanation → support for hypothesis
   - Conclusion: finding summary → theoretical contribution → practical implication
   - Methodology: variable definition → scale source → item adjustment → final item count
   - Questionnaire/sample section: procedure → screening rule → retained sample → statistical basis
   - Empirical result: test purpose → threshold → numerical result → hypothesis supported

4. Do not rewrite all paragraphs in the same way.
   - Some paragraphs should begin with the research problem.
   - Some should begin with the cited finding.
   - Some should begin with the variable relationship.
   - Some should begin with a limitation or boundary condition.
   - Some should use a direct explanation instead of a polished transition.

5. When the same section contains many similar paragraphs, select a limited group of representative high-risk paragraphs for structural differentiation first. Do not mechanically rewrite 50% of the section unless external-highlight evidence or repeated architecture clearly requires it.
   - Change sentence order where safe.
   - Split long balanced sentences.
   - Rewrite repeated opening and closing formulas into varied forms of equal or greater length (do not delete them).
   - Replace generic implications with thesis-specific explanations.

---

## Master Thesis Revision Prompt

Use the following prompt when revising thesis text.

```text
Please revise the following thesis text to reduce AI-generated writing patterns while keeping it academically appropriate for a master’s thesis.

Core requirements:
1. Keep the original meaning, academic logic, variables, citations, hypotheses, data, and statistical results unchanged.
2. Do not add new references, new theories, new data, or unsupported claims.
3. Keep the tone formal and suitable for an English master’s thesis, but do not make the language too polished, too fluent, or too template-like.
4. Make the writing sound more like a naturally written thesis by a competent non-native English writer, not like AI-generated academic prose. This means preserving the author's existing acceptable style (including mild, already-present non-native naturalness); it NEVER means creating new errors or imitating "non-native" features the author does not have (Gate I).
5. Correct obvious grammar mistakes, but do not over-polish the text into perfect native-speaker style.
6. If possible, do not use "first, second... third... finally", unless it is really necessary.
7. The writing should keep a competent non-native master’s thesis style, with natural plainness and slight unevenness in rhythm, but without intentional grammar or spelling errors.

Please specifically reduce the following AI-like features:
1. Repeated sentence openings, especially “This study…”, “Based on this…”, “For this reason…”, “In this context…”, “Therefore…”, “It is important to note that…”.
2. Overly smooth transitions and mechanical paragraph structures.
3. Sentences that are too balanced, too generic, or too summary-like.
4. Excessive use of abstract expressions such as “mechanism”, “framework”, “context”, “relationship”, “significant effect”, “provide evidence”, and “further explain” when more concrete explanation is possible.
5. Paragraphs that read like textbook summaries rather than a student’s own academic reasoning.

Revision style:
1. Vary sentence length naturally. Mix short, medium, and longer sentences.
2. Use more concrete explanations where appropriate, especially when discussing the user-provided variables, mediating mechanisms, psychological states, behavioral outcomes, or empirical findings.
3. Show the reasoning process more clearly instead of only giving polished conclusions.
4. Use alternative expressions for repeated structures such as “This study examines…”, “Existing research shows…”, and “The following hypothesis is proposed…”.
5. Keep necessary academic terms consistent, including user-provided variable names, abbreviations, hypotheses, model names, and statistical labels.
Variable set:
{{variable_set_from_user_or_extracted_from_source}}  (if no variable set is provided, extract ONLY from the current thesis text or uploaded thesis; never import variables from examples, prior conversations, or unrelated documents)

If no variable set is provided, extract variable names and abbreviations from the uploaded thesis before rewriting. Do not copy example variables into unrelated thesis revisions.

If the text is a literature review:
- Keep all cited authors and cited findings unchanged.
- Avoid making every sentence sound like a textbook summary.
- Strengthen the connection between prior literature and the present research topic.
- Do not invent or modify any source.

If the text is a hypothesis-development section:
- Keep the hypothesis unchanged.
- Make the theoretical logic clearer and less mechanical.
- Explain why the independent variable may affect the mediator, and why the mediator may affect the dependent variable or outcome variable.
- Avoid excessive use of “therefore”, “based on this”, and “the following hypothesis is proposed”.

If the text is an empirical-results section:
- Keep all numbers, significance levels, coefficients, model names, and conclusions unchanged.
- Do not reinterpret the data.
- Improve readability while preserving statistical accuracy.

If the text is a conclusion or implication section:
- Avoid broad, generic statements.
- Make the implications more connected to the actual research findings.
- Keep the wording practical and academically cautious.

Important restrictions:
1. Do not intentionally add grammar errors or spelling mistakes.
2. Do not make the language casual or conversational.
3. Do not remove citations.
4. Do not change hypothesis numbers.
5. Do not change variable names.
6. Do not change the structure unless the paragraph is clearly repetitive or mechanical.
7. Do not make the text sound like promotional writing.

Output format under the full skill workflow:

1. Dimension-to-Technique Execution Plan
   - Paragraph ID
   - Hit dimensions
   - Selected techniques
   - T19 used: Yes / No. T29 used: Yes / No. (Do not merge them into one checkbox.) If either is Yes, include the Source Trace block and identify the operation type — see the T19/T29 source-annotation rule
   - Reason for T19 relocation / Reason for T29 reconstruction (N/A for whichever is unused)
   - Protected elements
   - Rewrite intensity
   - Aggregation-worsening risk before Phase 7: Low / Possible / High
   - Breakpoint likely needed: Yes / No

2. Three-Pass Rewrite Evidence (exact actions, never generic labels)
   - Pass 1: list the EXACT AI-like patterns changed (pattern → location → what was done)
   - Pass 2: list the EXACT rhythm/architecture actions taken (e.g. which openings varied, which sentences re-segmented)
   - Pass 3: list remaining risks and the pass/rework decision

3. Protected Elements Check
   - list original exact strings before rewriting;
   - list revised exact strings after rewriting;
   - mark each item as Same / Restored / Changed;
   - if no protected element exists, write “No protected elements found in this paragraph”;
   - do not only write “preserved” or “all unchanged”.

4. Phase 7 Quality Gate Result
   - Gate A: AI-pattern reduction
   - Gate B: Academic integrity and protected elements
   - Gate C: Meaning preservation
   - Gate D: Dash and punctuation integrity
   - Gate E: Aggregation-worsening / breakpoint
   - Gate F: Word-count preservation
   - Gate G: Structure and readability
   - Gate H: Sentence completeness and length
   - Gate I: Grammar, spelling, capitalization
   - Gate J: Logic flow and no out-of-place meta-commentary

5. Revised Version

6. Major changes made

For quick single-paragraph revision only, the simplified format may be used only when the user explicitly asks for a quick single-paragraph rewrite.

Even in quick mode, the output must still include:
- hit dimensions;
- selected techniques;
- protected elements check;
- quality gate result.

Quick mode must not be used for full thesis chapters, multi-paragraph revision, DOCX rewriting, or external-detector-high rewrite tasks.

I will provide you the text for revision later.
```

---
## Quick Single-Paragraph Mode

Quick Mode routing and required evidence are defined ONLY in SKILL.md (Task Size Routing Rule and Task Mode Definitions). This reference provides paragraph-level examples only. If any example here conflicts with SKILL.md, ignore the example and follow SKILL.md. Do not duplicate Quick Mode routing conditions in reference files.

Quick Mode must not be used for:
- full thesis chapters;
- multi-paragraph revision;
- DOCX rewriting;
- external detector report tasks;
- external-detector-high tasks;
- any task where protected elements, hypotheses, variables, or statistical results appear across multiple paragraphs.

Even in Quick Mode, any rewritten paragraph must pass Gates A–J. Quick Mode means concise evidence, not omitted evidence: each gate may be one short line, but all ten gates must appear. Quick Mode must not include chapter-level scores, document-level scores, external-score claims, or a Chapter Version Ledger. Output must include:
- hit dimensions;
- selected techniques;
- protected elements check;
- Gate A–J result (concise is fine, but all ten gates).


---

## Author-Baseline Thesis Rewrite Rules

When revising thesis text, the target is not polished native-speaker academic prose. The target is formal but naturally organized academic English, similar to a competent master’s student writing independently.

The rewrite should reduce AI-like regularity. It should sound less templated, less mechanically balanced, and less over-edited.

### Core Rules

1. Preserve academic rigor and readability.
2. Do not add new ideas, theories, citations, examples, data, or unsupported claims.
3. Do not delete existing citations.
4. Avoid overly polished AI-style prose.
5. Do not stack transition words.
6. Do not make all sentences follow the same structure.
7. Keep the style close to an original master’s thesis draft.
8. Reduce unnecessary hedging.
9. Avoid repeated words, repeated sentence openings, and repeated subjects.
10. Avoid “first, second, third, finally” unless the structure truly requires them.

### Specific Rewrite Requirements

1. Remove formulaic academic sentence patterns and mechanical transitions.
2. Reduce vague or weak expressions such as “may,” “might,” “possibly,” “indicate,” “show,” “seem,” and “to some extent” when they do not add necessary academic caution.
3. Use direct and natural academic English.
4. Prefer shorter or medium-length sentences when possible, but do not force every sentence to be short.
5. Avoid repeated openings such as “This study,” “The results,” “Therefore,” “Overall,” “In summary,” and “Taken together.”
6. Do not make the logic overly neat or symmetrical.
7. Reduce machine-polished wording and keep some natural unevenness in rhythm.
8. Use concrete explanation where the original text allows it.
9. Reduce broad academic clichés and abstract expressions.
10. Reduce passive voice where active or noun-based active structure is clearer.

### Advanced Author-Baseline Techniques

Use light irregularity where appropriate:

- Let one sentence become noticeably shorter.
- Start some sentences with the phenomenon or result, then explain it.
- Avoid using a standard transition word in every sentence.
- Allow the paragraph to develop in a slightly less mechanical order when the meaning remains unchanged.

Avoid an overly theoretical tone.

For example:

AI-like:
> This reflects the important role of organizational support in promoting employee innovation.

More natural:
> Employees reacted more positively when they felt the organization supported their attempts to use AI for new ideas.

Use concrete action verbs where possible.

Prefer:
- increase
- strengthen
- reduce
- change
- shape
- support
- help explain
- make it easier for

Use less often:
- facilitate
- enhance
- promote
- demonstrate
- indicate
- reveal
- underscore
- highlight

Do not apply these rules mechanically. If a cautious verb or passive structure is necessary for academic accuracy, keep it.
Do not make reasoning so complete and smooth that every paragraph becomes claim → explanation → implication. Some reasoning can remain direct, plain, and slightly less polished if the academic meaning is clear.

---
## No Academic Elegance Upgrade Rule

Do not upgrade thesis writing into elegant native-speaker academic prose.

High-risk elegant academic phrases include:

- The pages that follow...
- The argument extends one step further...
- The net effect hinges on...
- The evidence points in one direction...
- This supplies a complementary lens...
- This anchors the argument...
- This captures the core insight...
- This governs the relationship...
- This mechanism operates through...

Preferred direction:
- use plainer thesis wording;
- keep direct explanation;
- avoid journal-like metaphors;
- avoid elegant bridge sentences;
- do not make the text sound like a polished literature synthesis.

The target is not elegant academic English. The target is formal, clear, plain, and slightly uneven master’s thesis English.

---
## Em Dash Suppression Rule

AI-generated academic writing often uses em dashes to create polished explanatory contrast, dramatic emphasis, or elegant appositive structures. In thesis revision, this pattern should be actively reduced because it can make the text sound machine-polished rather than like a naturally written master’s thesis.

High-risk em dash patterns include:

- efficiency claim — broader implication
- concept explanation — polished restatement
- result statement — theoretical meaning
- tool description — strategic significance
- problem statement — elegant contrast
- sentence ending with a broad interpretive phrase after an em dash

Examples of high-risk patterns:

- Many firms still design AI deployment around efficiency metrics — faster processing, lower labor cost, and smoother workflow.
- AI becomes more than a productivity tool — it becomes part of the firm's innovation infrastructure.

Mandatory rewrite rule:

- Avoid using em dashes in revised thesis text unless the original author already used them for a necessary technical or quoted expression.
- Do not introduce new em dashes during AI-risk reduction.
- Replace em dash structures with simpler sentence forms, commas, semicolons, or separate sentences.
- NEVER replace an em dash with "--" (two hyphens) or "-" (one hyphen). The double hyphen is not valid academic punctuation and must never appear in the output. Use a comma, colon, semicolon, parentheses, or two separate sentences instead.
- NEVER turn a normal hyphen into a double hyphen. Hyphenated compounds such as "employee-AI", "self-efficacy", "AI-generated", "human-AI", "cross-domain" keep their single hyphen exactly. Writing "employee--AI" is a defect.
- Do NOT touch en dashes in numeric, page, or date ranges (e.g. "2007–2010", "pp. 35–37"); leave them as they are.
- When the em dash creates an over-polished contrast, rewrite the sentence in a plainer academic style.
- If the em dash is used to attach a broad interpretive claim, check whether that claim is too generic or unsupported.
- Do not replace every em dash mechanically with a semicolon. Choose the structure that best preserves meaning and reduces AI-like polish.

Preferred revisions:

AI-like:
Many firms still design AI deployment around efficiency metrics — faster processing, lower labor cost, and smoother workflow.

Better:
Many firms still design AI deployment around efficiency metrics, such as faster processing, lower labor cost, and smoother workflow.

AI-like:
AI becomes more than a productivity tool — it becomes part of the firm's innovation infrastructure.

Better:
AI becomes more than a productivity tool. It can also become part of the firm's innovation infrastructure.

Quality check:

Before final output, scan all revised paragraphs for newly introduced em dashes. If an em dash was added by the rewrite, remove it unless there is a clear academic necessity. Record this under the Phase 7 quality gate as “Em dash check: Passed / Rework needed.”



---


## Register Boundary Rule

Reducing AI-like writing must not push the thesis into casual or conversational language.

Allowed:
- plain academic wording
- slightly uneven rhythm
- direct explanation
- concrete reasoning
- cautious author judgment when supported by the text

Not allowed:
- slang
- internet expressions
- emotional wording
- promotional tone
- overly casual sentence patterns
- conversational questions in formal thesis sections
- unsupported personal opinions

The target is not casual English. The target is formal but less machine-polished academic English.

---

## Thesis-Specific Operating Principles

### 1. Preserve academic content before reducing AI style

The rewrite must not change the academic substance. This includes:

- original meaning
- research logic
- variable names and abbreviations
- citation placement and cited findings
- hypothesis numbers and wording
- coefficients, significance levels, model names, sample size, and statistical conclusions
- chapter or section structure unless the structure is clearly repetitive or mechanical

Reducing AI-like language is secondary. Accuracy comes first.

### 2. Keep a formal thesis tone, but avoid overly polished English

The target style is not native-speaker journal prose. The target is a competent English master’s thesis written by a non-native speaker.

This means:

- fix obvious grammar mistakes
- keep sentences readable
- avoid too many perfect transitions
- avoid making every paragraph sound like a textbook
- allow slightly plain or uneven sentence rhythm
- do not intentionally add spelling errors or grammatical mistakes

### 3. Keep variable terminology consistent

User-provided variable names, abbreviations, constructs, model labels, and hypothesis terms must remain consistent throughout the thesis.

Do not replace core academic terms with casual synonyms. If the text explains a concept informally, the formal term should still remain clear.

Example only — replace with the user’s actual thesis variables.
Example variable set for the current thesis:

| Full Term | Abbreviation |
|----------|--------------|
| Employee–AI Collaboration | EAC |
| Self-Efficacy | SE |
| Work Engagement | WE |
| Creative Inspiration | IN |
| Perceived Organizational Support for Innovation | POS |
| Employee Innovative Behavior | IB |

Do not replace these terms with casual synonyms. For example, do not change Employee–AI Collaboration into “working with machines” or “AI teamwork” unless the text is explaining the concept informally and the formal term remains clear.

When the user’s thesis uses different variables, replace this example variable set with the user-provided variables. Do not copy the example variables into unrelated thesis revisions.



### 4. Protected Elements Rule

The following elements must be protected during AI-risk reduction:

1. User-provided variable names and abbreviations.
Example only — replace with the user’s actual thesis variables.
Example variable set for the current thesis:
- Employee–AI Collaboration (EAC)
- Self-Efficacy (SE)
- Work Engagement (WE)
- Creative Inspiration (IN)
- Perceived Organizational Support for Innovation (POS)
- Employee Innovative Behavior (IB)

2. Hypothesis numbers and hypothesis statements.

3. Statistical information
   - coefficients
   - p-values
   - significance levels
   - model names
   - sample size
   - table numbers

4. Citations and cited findings.

5. Established theory names.

When these elements appear in a high-risk sentence, revise the surrounding wording, sentence order, or paragraph structure. Do not alter the protected element itself.

### 5. Protected Element Lock

Before rewriting, extract and lock protected elements.

Protected elements include:

- exact citation strings
- author names
- year markers
- variable names
- abbreviations
- capitalization of constructs
- hypothesis labels
- table numbers
- model numbers
- coefficients
- p-values
- significance markers
- sample size
- statistical conclusions
- statistical symbol formatting (keep "p < 0.05", "β = 0.32", "VIF", "κ = 0.87", "R²" exactly as written; do not respace, reword, or convert to text such as "p value below 0.05" unless the original already did)

Examples:

```text
Employee–AI Collaboration must not become employee-AI collaboration.
Self-Efficacy must not become self-efficacy if the thesis uses title case as the formal variable name.
H1a must not become H1.
p < 0.001 must not become p < .01.
Table 4.3 must not become Table 3.4.
```
After rewriting, compare the original protected elements with the revised paragraph.

If any protected element changes, restore the original form before output.

### 6. Use concrete explanation without adding new claims

Concrete explanation is encouraged, but it must come from the existing text. Do not add new examples, company names, survey results, industry cases, or theoretical arguments unless they are already present in the thesis text.

Good concrete revision:

> When employees use AI to complete information searching, idea screening, or repeated analytical tasks, they may feel more capable of handling creative work.

Risky revision:

> In companies such as Google and Microsoft, AI collaboration has already improved employee creativity.

The second version introduces unsupported external claims and should not be used.

### 7. Do not over-smooth the writing

AI-generated academic writing often sounds too balanced, too complete, and too mechanically organized. For thesis revision, avoid making every paragraph follow the same pattern:

> Prior studies say X. However, few studies say Y. Therefore, this study examines Z.

A more natural thesis style can be:

> Prior studies have discussed AI use in the workplace, but the role of employee psychological changes is still not very clear. In this thesis, the focus is placed on whether Employee–AI Collaboration can influence Employee Innovative Behavior through several psychological variables.

### 8. Minimum Necessary Intervention

Use the minimum level of intervention that can reduce AI-like patterns while preserving the author’s original academic logic.

Apply changes in this order:

1. Remove unnecessary formulaic transitions.
2. Adjust sentence openings and endings.
3. Split sentences where rhythm is too uniform. Combine sentences only to repair a fragment, an accidentally split clause, or a thin sentence created during revision — never merely to shorten, compress, or smooth the paragraph (paragraph/sentence merging as a routine AI-reduction move is forbidden; see Principle 4).
4. Move concrete reasoning earlier if the paragraph is too abstract.
5. Rebuild paragraph architecture only when the paragraph is clearly template-like or repeated across the section.

Do not rewrite a paragraph from scratch when targeted structural revision is enough.

---

## Thesis Section-Specific Guidance

### Literature Review

For literature review sections:

- keep cited authors and findings unchanged
- avoid making each sentence a separate summary of one citation
- connect prior literature with the present research problem
- avoid unnecessary phrases such as “many scholars have widely discussed”
- do not invent missing literature
- do not strengthen claims beyond the original sources

Weak AI-like version:

> Existing research has extensively explored the relationship between employee self-efficacy and innovative behavior. These studies provide valuable theoretical support for this research.

Better thesis version:

> Previous studies have linked self-efficacy with employees’ willingness to try new ideas and continue creative tasks. This is relevant to the present thesis because Employee–AI Collaboration may change how capable employees feel when facing innovation-related work.

### Hypothesis Development

For hypothesis-development sections:

- keep the hypothesis number and hypothesis statement unchanged
- make the logic more visible
- explain why one variable may influence another
- reduce repetitive “therefore” and “based on this”
- do not add new theoretical models

Weak AI-like version:

> Based on the above analysis, Employee–AI Collaboration has a positive impact on Self-Efficacy. Therefore, the following hypothesis is proposed.

Better thesis version:

> When employees can use AI to obtain information, compare alternatives, or complete some routine cognitive tasks, they may feel less uncertain about difficult work. This can make them believe more strongly in their own ability to solve problems. Thus, Employee–AI Collaboration is expected to be positively related to Self-Efficacy.


### Methodology / Variable Measurement

For methodology and variable measurement sections:

- Preserve all variable names, scale sources, citations, item numbers, and questionnaire details.
- Do not describe every variable with the same fixed structure.
- Avoid repeating the sequence: definition → scale source → item count.
- Vary the order and sentence form of variable definition, scale source, and item count for each variable, but keep all three for every variable. Do not merge or drop any of them (this would shorten the text).
- Use different entry points for different variables, such as research role, measurement source, item content, or theoretical relevance.

Weak template:
The variable is X. It refers to Y. This study adapts the scale from Z. The final scale includes N items.

Better:
X was measured with N items adapted from Z, focusing on Y.

Alternative:
To capture X, the questionnaire used N items from Z. These items describe Y.

### Empirical Results

For empirical-results sections:

- keep all numbers unchanged
- keep significance levels unchanged
- keep model names unchanged
- do not reinterpret the data
- avoid adding causal language if the original result only supports association
- improve readability without changing statistical meaning

Weak AI-like version:

> The results show that the coefficient is significant, indicating that the hypothesis is supported.

Better thesis version:

> The coefficient is positive and significant, so the result supports the hypothesis. The numerical result should be kept as reported in the original model.

### Conclusion and Implications

For conclusion and implication sections:

- avoid broad claims such as “this study provides important guidance for all organizations”
- connect implications to actual findings
- keep the tone cautious
- do not make promotional statements
- avoid overclaiming practical value

Weak AI-like version:

> This study provides valuable implications for organizations to promote innovation in the era of artificial intelligence.

Better thesis version:

> The findings suggest that organizations should not only introduce AI tools, but also pay attention to whether employees feel capable of using these tools in innovation-related tasks. This implication is limited to the variables and sample examined in this thesis.

---

## Rewrite Strategy Matrix

Use the external-detector-calibrated paragraph_risk_index score together with any available external detector result, highlighted fragment, or high-risk section evidence.

| AI% | Mode | Techniques Applied | Thesis Use |
|-----|------|-------------------|------------|
| ≥55% | Last-rung Structural Reorganisation | Select only dimension-matched techniques from T1–T29 | Rework paragraph architecture, entry point, reporting order, and repeated templates by minimal edits only. T19/T29 may be used only when source-trace evidence exists. Do not apply all techniques mechanically and do not regenerate the paragraph. |
| 40-54% | Strong Structural Rewrite | Select only dimension-matched techniques from T1–T29 when D16/D17 or long-fragment risk is triggered | Apply sentence-by-sentence minimal edits to enough sentences to break the detected structure — change entry point, reporting order, rhythm, or template dependency without regenerating the paragraph or rewriting sentences that do not carry the diagnosed risk. T19/T29 only with source-trace evidence. |
| 21-39% | Standard Structural Rewrite | T1-T13, plus T14-T19 if repeated across section | Rewrite opening, ending, transitions, abstract phrasing, methodology templates, repeated reporting logic, and (only via T19 relocation of researcher-side material that already exists in the thesis, with its source annotation — never newly composed) researcher-side judgment where needed. |
| 10-20% | Pattern-Based Rewrite | T1-T6, T11-T19 if part of repeated section pattern | Rewrite if the paragraph belongs to a repeated section pattern, even if its individual score is low. |
| <10% | Structural Check Only | T1, T11, T14-T19 if needed | Skip only when the paragraph has no repeated structure and is not part of a high-risk section. |

Strict rule:
When a comparable external detector result for the same or a broader clearly mapped scope is 40% or higher, no paragraph inside externally highlighted or structurally linked high-risk sections should be skipped only because its individual internal estimate is below 25%. If the external score scope is unclear or non-comparable, label it as calibration evidence only and do not use it as a direct paragraph-level floor.
Do not apply all listed techniques mechanically. Select only the techniques that match the paragraph’s actual detected AI-risk dimensions.


## No Global Polishing Rule

Do not reduce AI risk by globally polishing the whole thesis.

Risky rewrite direction:
- making every paragraph smoother;
- making every transition more complete;
- making each argument follow a clean academic chain;
- adding explanatory bridge sentences everywhere;
- replacing rough student wording with polished academic synthesis;
- making the introduction, literature review, and conclusion more elegant but more template-like.

This can increase external-detector AI risk, especially when an external detector identifies long smooth academic fragments.

Preferred rewrite direction:
- revise only paragraphs with clear AI-risk dimensions;
- keep acceptable roughness when it does not damage academic clarity;
- reduce repeated templates instead of making the whole paper smoother;
- remove generic bridge sentences if they make the paragraph too complete;
- preserve some natural unevenness in paragraph development.


## No Random Short-Sentence Rule

Do not reduce AI risk by randomly inserting short sentences.

Weak approach:
- Insert a short sentence only to create rhythm.
- Break one sentence into several fragments without improving logic.
- Add abrupt sentences that do not address the detected dimension.
- Use short sentences as a substitute for structural rewriting.

Acceptable use of short sentences:
- The short sentence clarifies a specific claim.
- The short sentence changes an overly uniform rhythm.
- The short sentence helps separate result, explanation, and implication.
- The short sentence supports a detected dimension such as D3, D4, D12, or D14.

Before using a short sentence, identify which AI-risk dimension it addresses.


## Aggregation-Worsening Breakpoint Rule

Do not assume that merging paragraphs or reducing fragment count always improves AI-risk performance.

If rewriting reduces the number of fragments but increases the maximum single-fragment length, check whether the revision has created a longer continuous AI-like segment.

Mandatory rule:
- If one revised fragment exceeds 3000 characters, insert at least one valid breakpoint or split the fragment.
- The breakpoint must address a real AI-risk dimension, such as D3, D4, D12, D14, D15, D16, or D17.
- The breakpoint should preferably use T19 when the fragment is descriptive, abstract, or overly smooth.

Valid breakpoint options:
1. Insert a researcher-view judgment sentence.
2. Insert a process narration sentence.
3. Insert a scope-limitation sentence.
4. Insert an existing numerical anchor.
5. Insert a supported contrast or counterpoint.
6. Refer to a specific table, hypothesis, variable, coefficient, sample, or measurement decision.

Invalid breakpoint options:
- adding a random short sentence;
- inserting unsupported personal opinion;
- inventing a number or example;
- adding a polished transition sentence;
- adding a generic sentence that could fit any thesis.

Execution evidence:
```text
Aggregation-worsening checked: Yes / No
Fragment over 3000 characters: Yes / No
Breakpoint required: Yes / No
Breakpoint inserted: Yes / No
Breakpoint type:
Targeted dimension:
```




## Dimension-Targeted Rewrite Rule

Every rewrite must target the paragraph’s actual detected dimensions.

Do not revise only by general intuition.

Before rewriting, identify:

```text
Hit dimensions:
Main source of AI risk:
Selected techniques:
Protected elements:
```
Examples:

If D1 is high, change repeated sentence openings.
If D2 is high, remove formulaic transitions.
If D3 is high, make reasoning less mechanically smooth.
If D4 is high, vary rhythm without random fragmentation.
If D5 is high, replace generic academic phrasing with specific explanation.
If D12 is high, rebuild paragraph architecture.
If D13 is high, diversify several paragraphs together.
If D15 is high, change the section-level template.
If D16 is high, BREAK the repeated methodology/empirical template by restructuring and adding specificity (not by compressing). Avoid repeated phrases such as “The variable is...”, “This study adapts...”, “The results show...” by recasting them into varied, equally-long-or-longer forms. Do not reduce word count.
If D17 is high, change the repeated reporting order across the paragraph group, such as test purpose → threshold → result → conclusion.

A paragraph with D12, D13, D15, D16, or D17 cannot be fixed by synonym replacement or random sentence splitting alone.

---


---

## Section-Level Rewrite Priority


When external detector reports are available, section priority must be based on the External Risk Convergence Map, not on a fixed chapter order.

Default high-risk sections include:

1. Sections with strong external detector evidence, long highlighted fragments, or repeated high-risk signals across one or more reports.
2. Sections with long continuous highlighted fragments.
3. Methodology, research design, questionnaire design, sample screening, and empirical result reporting if flagged externally.
4. Hypothesis development sections with repeated variable → mechanism → hypothesis structures.
5. Conclusion and implication sections with generic contribution or future-research templates.
6. Introduction, research significance, and chapter arrangement sections with repeated background → gap → value structures.
7. Literature review sections with repeated definition → citation → implication patterns.

If no external detector report is available, use internal D1–D17 scoring, D16/D17 trigger floors, and section-template floors to decide priority.

### High-Risk Thesis Section Examples

When the following section patterns appear, treat them as high priority:

1. Introduction:
   - repeated background → research gap → study value across 1.1, 1.2, 1.3, and 1.4;
   - theoretical and practical significance written in parallel sentence frames.

2. Theory framework:
   - several theories introduced by proposer/year → core concept → application to this study;
   - repeated phrase such as “provides the theoretical basis for...”.

3. Hypothesis development:
   - H2/H3/H4 or H5a/H5b/H5c share the same argument route;
   - repeated endings such as “the following hypothesis is proposed”.

4. Literature review:
   - repeated prior studies show/suggest/indicate → findings → this provides a basis pattern.

5. Conclusion:
   - repeated result → theoretical meaning → practical meaning structure across several findings.


---
## Paragraph Length Diversification

If three or more consecutive paragraphs have very similar length and structure, do not revise them in the same way.

Apply one of the following:
- vary one paragraph's repeated general explanation by making it specific (do not delete or shorten it);
- expand one paragraph with reasoning already present in the thesis;
- move a concrete explanation earlier;
- recast two repetitive sentences into two differently-structured sentences (do not merge them);
- split one overly balanced sentence;
- change the opening or closing structure of one paragraph.

Do not make all revised paragraphs similar in length. Similar paragraph length plus similar paragraph logic can still look machine-generated even after wording changes.

---

## Chapter-Level Template Rewrite Mode

When a whole chapter or subsection is detected as AI-like by more than one detector, do not revise isolated sentences only.

Rewrite the chapter-level template.

The purpose is not to make the text smoother. The purpose is to reduce repeated academic architecture while preserving thesis meaning.

### High-risk chapter templates

1. Introduction:
   - repeated background → gap → value → research question structure;
   - overly complete chapter arrangement;
   - generic theoretical/practical significance.

2. Hypothesis development:
   - repeated variable explanation → mechanism → hypothesis;
   - every hypothesis paragraph ends in the same way;
   - mediators and moderators are introduced with identical logic.

3. Research design:
   - variable definition → scale source → item adjustment → final item count;
   - questionnaire design → pilot study → formal survey;
   - sample screening → valid sample → later analysis.

4. Empirical analysis:
   - test purpose → threshold → result → acceptable conclusion;
   - repeated “this indicates that...” and “the results show...”;
   - every table is followed by a standard explanation.

5. Conclusion:
   - summary of findings → theoretical contribution → practical implication → limitation → future research;
   - broad claims that can fit many theses.

### Required rewrite actions

- recast repetitive procedural sentences into varied forms where safe (do not merge or delete them);
- move table-based details into table references instead of repeating them in prose;
- vary subsection openings;
- reduce repeated “This study...” structures;
- remove unnecessary bridge sentences;
- keep some plain thesis-style directness;
- avoid turning every paragraph into claim → explanation → implication;
- preserve all citations, variables, hypotheses, data, coefficients, p-values, and table numbers.


---
## Parallel Section Rewrite Method

Use this method when several paragraphs in the same section follow the same function path.

The goal is not to make each paragraph sound different at the word level. The goal is to make each paragraph do a different job.

### Common parallel structures

1. Introduction:
   background → gap → value → contribution repeated across subsections.

2. Theory framework:
   theorist/year → theory concept → application to this study.

3. Literature review:
   variable definition → prior findings → this study’s relevance.

4. Hypothesis development:
   variable relationship → mechanism → citation support → hypothesis.

5. Empirical analysis:
   test purpose → threshold → result → support.

6. Conclusion:
   result → theoretical meaning → practical meaning.

### Rewrite actions

- Change the paragraph’s functional entry point.
- Change the order of explanation where safe.
- Differentiate repeated background or general value statements by restructuring and adding specificity (do not merge or delete them).
- Move thesis-specific reasoning earlier.
- Reduce repeated closing formulas.
- Use different argumentative roles for neighboring paragraphs.
- Keep citations, hypotheses, coefficients, p-values, table numbers, and variable names unchanged.

### Invalid rewrite

- changing only synonyms;
- changing only sentence length;
- replacing “therefore” with another transition;
- giving every paragraph the same improved structure;
- making all paragraphs smoother and more complete.

### Valid rewrite

- one paragraph enters from a research gap;
- one paragraph enters from a variable-specific mechanism;
- one paragraph enters from a methodological reason;
- one paragraph enters from an empirical result;
- one paragraph keeps a direct thesis-style explanation without a polished bridge sentence.


---
## Hypothesis Cluster Differentiation Method

Use this method when several hypotheses share the same argument path.

Typical high-risk pattern:

```text
AI affects X → citation support → X affects innovation → therefore hypothesis is proposed
```
This pattern is especially risky when H2/H3/H4 or H5a/H5b/H5c only change the variable name.

Required strategy:

- Keep the hypothesis statement unchanged.
- Change the reasoning route before the hypothesis.
- Do not let each hypothesis start from the same general claim about AI.
- Do not let each hypothesis end with the same formulaic sentence.

Possible differentiation routes:

- Psychological mechanism route:
  use when the hypothesis concerns confidence, motivation, engagement, or perceived ability.
- Behavioral allocation route:
  use when the hypothesis concerns time, attention, task focus, or work process.
- Cognitive stimulation route:
  use when the hypothesis concerns inspiration, idea generation, or creative thinking.
- Boundary condition route:
  use when the hypothesis concerns organizational support, work context, or moderation.

Mandatory rule:

- If two or more hypotheses have the same structure, rewrite them as a hypothesis cluster.
- At least two hypotheses in the cluster must use different reasoning routes.
- Do not solve hypothesis repetition by changing only wording.
- The conclusion may remain similar, but the path leading to it must differ.

Concrete entry-point examples (all drawn from material already in the thesis — no new claims, no new citations):
- Literature-tension entry: "Although earlier work treated X as having no direct effect on Y, more recent results point to possible boundary conditions; in this study's setting, H2 is therefore proposed: ..."
- Phenomenon-observation entry: "In practice, teams with higher X are often the ones where Y appears; read through the lens of the theory already introduced, this leads to H3: ..."
- Gap-filling entry: "Prior studies mostly examined the direct X→Y link and left the transmitting mechanism open; to address that, H4 is proposed: ..."
- Result-derivation entry: "Because H1 already established that X affects the mediator M, and M is linked to Y in the literature reviewed above, H5 follows: ..."
Rotate entries so adjacent hypotheses in the cluster do not share an opening logic; keep every hypothesis statement, variable name, and citation unchanged.





---

## Caution on Aggressive Examples

Some aggressive examples in this guide are retained from the original method file. They are useful for showing how to break AI-like patterns, but they should not be copied directly into a master’s thesis.

For thesis revision, prefer the thesis-adjusted versions. Use vivid or conversational alternatives only when they remain formal, accurate, and appropriate for academic writing.

Aggressive examples are diagnostic examples, not default rewrite outputs. In a master’s thesis, do not use rhetorical questions, marketing-like expressions, or dramatic phrasing unless the original academic style already supports them.

When there is a conflict between an aggressive example and the thesis-adjusted version, always follow the thesis-adjusted version.

---

## Aggressive Technique Label Rule

Some examples in this file are intentionally aggressive and are not default thesis-writing outputs.

Any technique or example that sounds vivid, conversational, dramatic, promotional, or non-thesis-like must be treated as:

```text
[AGGRESSIVE — thesis use with caution]
```
Mandatory rule:

- Do not use AGGRESSIVE examples unless paragraph_risk_index ≥55% or the user explicitly approves stronger rewriting.
- Do not use AGGRESSIVE examples in methodology, empirical results, or statistical reporting sections.
- When revising a master’s thesis, prefer thesis-adjusted versions over aggressive examples.


---
## Technique 1: Sentence Starter Variation (Targets D1)

**Principle**: Break repeated sentence openings and the “Furthermore → Moreover → Additionally” chain.

In thesis writing, also reduce repeated openings such as:

- This study...
- Based on this...
- For this reason...
- In this context...
- Therefore...
- It is important to note that...
- Existing research shows...
- The following hypothesis is proposed...

**Before**:
> Furthermore, the results indicate... Moreover, the data shows... Additionally, the analysis reveals...

**After**:
> The results paint a different picture. What the data suggests, however, is that... A closer look at the analysis reveals...

**Thesis-appropriate alternatives**:
| AI Pattern | Thesis Alternative |
|------------|-------------------|
| This study examines... | The present thesis focuses on... / This section considers... |
| Existing research shows... | Previous studies have reported... / Prior work has linked... |
| Based on this... | This logic leads to... / From this reasoning... |
| Therefore, the following hypothesis is proposed. | The hypothesis is stated as follows. / This thesis expects that... |
| It is important to note that... | A point that needs attention is... |
| In this context... | In the case of Employee–AI Collaboration... |
| Furthermore, | In addition, / Another point is that... |
| Moreover, | Also, / A related point is... |
| Additionally, | The discussion also needs to consider... |
| Therefore, | Thus, / This suggests that... |
| However, | However, / Yet, / But this does not mean that... |
| Consequently, | As a result, / This may lead to... |

**Original aggressive alternatives retained**:
| AI Pattern | Human Alternative |
|------------|------------------|
| Furthermore, | What stands out is... / Beyond this, |
| Moreover, | A related finding is... / Equally telling, |
| Additionally, | Another dimension is... / Not to be overlooked, |
| Therefore, | This points to... / The implication is clear: |
| However, | Yet the evidence suggests... / But here the picture shifts. |
| Consequently, | The natural outcome is... / As events unfolded, |

Note: Some original alternatives may be too vivid for a master’s thesis, but they are intentionally preserved. Use them only when they do not make the thesis sound casual or promotional.

---

## Technique 2: Transition De-formulaizing (Targets D2)

**Principle**: Replace formulaic transitions with less mechanical language.

**Before**:
> It is worth noting that AI collaboration enhances innovation. It is important to emphasize that self-efficacy mediates this relationship.

**After**:
> One striking finding is how AI collaboration amplifies innovation. Equally revealing: self-efficacy acts as the bridge in this relationship.

**Thesis-adjusted version**:
> One point shown by the results is that Employee–AI Collaboration is related to Employee Innovative Behavior. Self-Efficacy also plays a mediating role in this process.

**Replacements**:
| Formulaic | Natural |
|-----------|---------|
| It is worth noting that... | One striking pattern is... |
| It is important to emphasize that... | What matters most is... |
| In light of the above... | Against this backdrop, |
| Taken together, these findings... | Viewed collectively, these patterns... |
| In conclusion, | To sum up the evidence, |

**More thesis-safe replacements**:
| Formulaic | Thesis Alternative |
|-----------|-------------------|
| It is worth noting that... | One point that needs attention is... |
| It is important to emphasize that... | This part is important because... |
| In light of the above... | Considering the above discussion... |
| Taken together, these findings... | Taken together, the results suggest... |
| In conclusion, | In summary, / Overall, |

**Prefer deletion over replacement (read this first).** Swapping one AI-frequent connective for another ("therefore" → "thus", "moreover" → "furthermore") does little: a detector treats them as equivalent. The stronger move is to DELETE a connective that the surrounding logic already makes clear, then keep the word count up by adding a concrete detail already in the paper — not by inserting another connective.

Safe-to-delete openers (when the logical relation is already obvious from the sentences themselves): "Furthermore,", "Moreover,", "In addition,", "Additionally,", "It is important to note that", "It is worth noting that", "It should be noted that", "In this context,", "From this perspective,", "Taken together,". Delete the opener, capitalise the next word, and check the sentence still reads correctly (Gates H/I).

Word-count compensation (Principle 4): the words saved by deleting a connective must be recovered by adding specificity to the same sentence, not by padding. Example: "Furthermore, the results show a positive effect." → "The regression results in Table 4.3 show a positive effect (β = 0.32, p < 0.01)." Net effect: word count holds or rises, one AI-style connective removed. Never delete a connective if doing so changes or obscures the logical relation; in that case keep or recast it instead.

---

## Technique 3: Sentence Length Variation (Targets D4)

**Principle**: Mix short, medium, and long sentences. Avoid paragraphs where every sentence has the same rhythm.

**Before**:
> The regression analysis revealed significant positive effects. Employee-AI collaboration was positively associated with innovative behavior. Self-efficacy served as a significant mediator in this relationship.

**After (varied length, every sentence complete — no fragments)**:
> The regression analysis returned significant positive effects. Employee-AI collaboration was positively associated with innovative behavior, and self-efficacy turned out to be a significant mediator that helped explain why this link held.

**Thesis-adjusted version**:
> The regression result is clear. Employee–AI collaboration is positively related to employee innovative behavior, and self-efficacy also plays a mediating role, which means employees' confidence in their own ability helps explain part of this relationship.

**Flexible rhythm rules**:
- Prefer a mix of short and medium-length sentences.
- Use a noticeably shorter sentence when it improves natural rhythm, but only if it is a complete sentence (subject + finite verb). Never use a fragment such as "significantly." or "Self-efficacy." as a standalone sentence.
- Use a longer sentence only when the logic requires it, and keep it at or under about 30 words with at most two subordinate clauses.
- Avoid three or more consecutive sentences with almost the same length and structure, and equally avoid three or more ultra-short sentences in a row.
- Do not force every paragraph to contain both a very short sentence and a very long sentence.
- Never split a subordinate clause or a noun list into its own "sentence" (see Principle 8 / Gate H).

**Thesis caution**:
These rules should not be applied mechanically. In empirical-results sections, clarity and statistical precision are more important than forcing a very short sentence into every paragraph.

---

## Technique 4: Hedging Calibration and Claim-Strength Control (Targets D6)

**Principle**: Remove unnecessary qualifiers, but keep academic caution where needed.

**Before**:
> These findings may potentially contribute to our understanding of how AI might possibly influence employee creativity to some extent.

**After**:
> These findings advance our understanding of how AI influences employee creativity.

**Thesis-adjusted version**:
> These findings help explain how AI use in work may be related to employee creativity.

**Remove or reduce these when they are unnecessary**:
- "may potentially" → use "may" or "can"
- "to some extent" → replace with a thesis-specific qualifier of equal or greater length (e.g. "within the range tested in this sample"); do not simply delete, to avoid shrinking the text
- "to a certain degree" → replace with a specific qualifier of equal or greater length rather than deleting
- "it could be argued that" → state the point more directly
- "might be considered as" → "can be seen as" or "is"
- "appears to be somewhat" → "appears to be" or "is"

**Important thesis caution**:
Do not remove hedging when the data only supports cautious interpretation. For example, if the thesis uses cross-sectional survey data, do not turn “is associated with” into “causes”.

Protected hedges — never remove or weaken hedges that mark statistical uncertainty, qualitative scope, causal-inference limits, sampling/generalisability limits, measurement limits, or author positionality. Calibration adjusts only repetitive, content-free qualifier stacking ("may potentially ... to some extent"); it never upgrades claim strength. When unsure whether a hedge is load-bearing, keep it (see also Gates B/C and the protected-epistemic-hedges rule).

For survey-based or cross-sectional studies, do not change “is related to,” “is associated with,” or “may influence” into strong causal wording such as “causes,” “leads to,” or “determines,” unless the original thesis explicitly supports causal inference.
---

## Technique 5: Balance Disruption (Targets D6)

**Principle**: Avoid overly symmetrical and mechanical structures such as “On the one hand... On the other hand...”.

**Before**:
> On the one hand, AI tools enhance efficiency. On the other hand, they may reduce human autonomy.

**After**:
> AI tools do enhance efficiency — that much is clear. But autonomy? That's where the tension lies. The data reveals a more nuanced trade-off than simple empowerment versus displacement.

**Thesis-adjusted version**:
> AI tools can improve efficiency, but this does not automatically mean that employees become more innovative. The effect may depend on whether employees feel more capable, more engaged, or more supported when using AI in their work.

**Use this technique to reduce**:
- repeated “On the one hand / On the other hand”
- perfectly balanced contrast sentences
- paragraphs that look like generated debate summaries

---
## Punctuation and Clause Density Control

Avoid overusing em dashes, semicolons, and highly balanced clause structures.

Risky patterns:
- not only X but also Y, and even Z
- on the one hand X, on the other hand Y, therefore Z
- X, Y, and Z repeated across several paragraphs
- repeated em-dash explanations
- several long clauses joined into one overly balanced sentence

Revision rule:
- keep only one major contrast per sentence;
- split overloaded sentences;
- avoid repeating the same three-part structure;
- use em dashes sparingly in formal thesis writing;
- do not turn every sentence into a neatly balanced academic structure.

---
## Technique 6: Generalization Surgery (Targets D5/D7)

**Principle**: Replace vague conclusions with specific, grounded statements.

**Before**:
> These findings provide valuable insights for future research and have important practical implications for organizations seeking to implement AI tools.

**After**:
> For HR managers evaluating AI adoption: the data points to self-efficacy training as the single highest-ROI intervention. Prioritize confidence-building before tool deployment.

**Thesis-adjusted version**:
> For organizations introducing AI tools, the result suggests that technical adoption alone may not be enough. Employees also need to feel able to use AI in tasks related to problem solving and idea generation.

**Pattern**:
- "valuable insights for future research" → specify the research gap or question
- "important practical implications" → name the practical action, but do not overclaim
- "contributes to the broader understanding" → state exactly what is clarified

**Thesis caution**:
Do not add a concrete recommendation that is not supported by the findings. If the result only tests Self-Efficacy, do not suddenly recommend a full AI governance system unless the thesis already discussed it.

---

## Technique 7: Passive Voice Control / Active-Passive Mixing (Targets D8)

**Principle**: Break passive voice clusters with active constructions, but do not remove all passive voice.

**Before**:
> The survey was distributed to 500 employees. Data was collected over six months. Responses were analyzed using SEM.

**After**:
> We surveyed 500 employees. Data collection spanned six months. SEM analysis of the responses followed.

**Thesis-adjusted version**:
> The survey was distributed to 500 employees, and data collection lasted six months. The responses were then analyzed using SEM.

**Thesis caution**:
Many master’s theses avoid excessive “we” or “I”. If the university style discourages first person, use mixed noun-based active structures:

> Data collection lasted six months. The analysis used SEM to test the proposed model.

**Coverage guidance (active/passive mixing)**:
- In a paragraph dominated by passive voice or nominalizations, convert roughly 30% of its sentences to active or noun-based active structures, so the paragraph is no longer uniformly passive. This is a guideline, not a rigid quota.
- Do not flip every sentence — a fully active paragraph reads as unnatural for a thesis as a fully passive one. Aim for a natural mix of voices.
- Conversion must keep the meaning, the real subject, and all protected elements intact, and must not introduce subject–verb agreement errors (checked by Gate I).
- Where the university style forbids first person, get the active feel from noun-based subjects ("The analysis used…", "Data collection lasted…") rather than "we" or "I".

---

## Technique 8: Concrete Anchoring (Targets D9)

**Principle**: Add specific numbers, names, or examples to ground abstract claims.

**Before**:
> AI collaboration transforms workplace dynamics by enhancing efficiency and fostering innovation across organizational contexts.

**After**:
> AI collaboration transforms workplace dynamics. At Foxconn's Shenzhen plant, AI-assisted quality control cut defect rates from 3.2% to 0.7% — while the same workers filed 40% more process improvement suggestions.

**Thesis-adjusted version**:
> Employee–AI Collaboration may change daily work because employees can use AI to search information, compare options, draft ideas, or check repeated tasks. These concrete work activities are closer to the way employees may develop innovative behavior.

**Critical thesis restriction**:
Do not add new company examples, names, numbers, or cases unless they are already present in the thesis or source material. The original aggressive example is retained, but it should not be used in thesis revision without supporting evidence.

---

## Technique 9: Citation Naturalization (Targets D10)

**Principle**: Integrate citations naturally rather than placing citations at fixed, mechanical intervals.

**Before**:
> AI adoption is increasing (Smith, 2024). Organizations report productivity gains (Jones, 2025). Employee responses vary widely (Chen, 2024). Training mediates outcomes (Wang, 2025).

**After**:
> AI adoption is accelerating across industries. Smith (2024) and Jones (2025) both document significant productivity gains, though Chen's (2024) multi-industry survey reveals striking variation in employee responses. The key differentiator, according to Wang (2025), is training quality.

**Thesis-adjusted version**:
> AI adoption has been discussed in relation to productivity and employee response. Smith (2024) and Jones (2025) reported productivity-related findings, while Chen (2024) showed that employee responses may differ across settings. Wang (2025) further connected these outcomes with training quality.

**Rules for thesis use**:
- Keep all cited authors unchanged.
- Keep cited findings unchanged.
- Do not merge citations if it changes which author supports which claim.
- Do not add page numbers unless they already exist.
- Do not invent missing references.

**Citation-rhythm variation toolkit (use when citations fall at a fixed every-1-2-sentence cadence — a pattern CNKI is sensitive to).** Vary the rhythm using only the existing citations and the claims they already support; never move a citation onto a claim it does not support:
- Multiple-citation merge: group several sources that support the same point — "Several studies (A, 2020; B, 2021; C, 2022) report ...".
- Citation-first: lead with the author — "Smith (2020) was among the first to argue that ...".
- Embedded-in-clause: fold the citation into the main sentence — "The argument advanced by Wang (2021), that ..., has since become ...".
- Contrast pairing: set two sources against each other — "Whereas Liu (2020) found A, the later work of Chen (2022) showed B.".
- End-of-passage roundup: 2–3 sentences of synthesis, then one grouped citation at the end — "... These claims have been documented across the literature (A, 2020; B, 2021).".
Guidance: across any ~8 sentences of literature review, use at least 2–3 different rhythm types; never let 4+ consecutive paragraphs share the same citation cadence. Author names, years, and which claim each source supports are protected (Gate B).

---

## Technique 10: Lexical Precision and Repetition Control (Targets D11)

**Principle**: Reduce repeated AI-favored verbs, but do not make the language unnaturally fancy.

**Word-choice subrule — precision over rarity (read before swapping any word):**
When replacing an AI-favored generic word, the test is PRECISION, not rarity. Choose the word that most exactly fits the meaning the thesis already expresses. A slightly less common word is fine ONLY when it is genuinely more precise here; never reach for an unusual, ornate, or "high-perplexity" word just because it is rare. Do NOT swap one AI-frequent word for another AI-frequent fancy word (e.g. "facilitate" → "catalyze", "enhance" → "amplify/fortify", "shows" → "illuminates") — that does not lower AI risk and often reads as machine-polished or distorts the meaning. Prefer the plain, accurate, thesis-native term over both the AI cliché and the exotic synonym. If no more precise word exists, keep the original. Never invent or coin words, and keep all technical terms exact.

**AI-favored verbs to avoid repeating too often**:
- demonstrate
- highlight
- underscore
- emphasize
- reveal
- indicate
- suggest
- show
- provide evidence
- further explain

**Legacy elevated verb bank (use only when genuinely field-appropriate AND more precise — never as default; these elevated verbs can push text toward the over-polish failure mode the rare-word guard warns against; the thesis-safe bank below is the default)**:
- illuminate
- expose
- unmask
- trace
- pinpoint
- quantify
- disentangle
- corroborate
- challenge
- complicate
- overturn
- refine
- extend
- qualify
- bridge
- surface
- foreground

**More thesis-safe verb bank**:
- examine
- discuss
- report
- find
- support
- partly explain
- help explain
- is related to
- is associated with
- plays a role in
- is connected with
- gives some support to
- helps clarify

**Before**:
> The results demonstrate that self-efficacy highlights the mechanism. This finding underscores the importance of training. The data also reveals boundary conditions.

**After**:
> The results pinpoint self-efficacy as the mechanism. This finding foregrounds training as the critical lever. The data also surfaces boundary conditions worth examining.

**Thesis-adjusted version**:
> The results support the mediating role of Self-Efficacy. This means that employees’ belief in their own ability helps explain how Employee–AI Collaboration is related to Employee Innovative Behavior.

**Low-frequency synonym selection (lexical de-templating)**:
- When replacing an AI-favored generic word, prefer a precise, lower-frequency synonym that established literature in the field actually uses — favour words that are accurate but comparatively uncommon in generic AI prose, rather than the most obvious dictionary synonym.
- Source the replacement from the discipline's own vocabulary (the terms senior scholars use for that exact concept), not from a thesaurus. The goal is a word that is correct and field-appropriate yet less statistically predictable.
- Keep technical terms and protected elements exact — only the generic connective/descriptive vocabulary is replaced.
- Do not over-reach into rare or archaic words that would read as unnatural for a non-native master's thesis. Accuracy and readability outrank rarity; a slightly less common but clearly correct word beats an exotic one.
- Vary the replacements: do not swap every instance of a repeated word for the same single alternative, or you simply create a new repeated template.

**Multi-word AI collocations (de-template the phrase, not just the word).** Detectors weight whole collocations, not only single words. These set phrases appear far more in AI prose than in real theses; replace with a plainer, content-specific phrasing (and never swap one cliché collocation for another). Use a given replacement at most twice in the whole document:
| AI-frequent collocation | Plainer replacement |
|-------------------------|---------------------|
| plays a key / crucial / important role in | is central to / matters for / shapes |
| has attracted increasing / widespread attention | has drawn growing interest / has been studied more in recent years |
| provides valuable / important insights | helps clarify / informs / adds to what is known about |
| contributes to a better understanding of | helps make sense of / adds to prior work on |
| has significant implications for | matters for / is relevant to |
| enriches the existing literature | adds to prior work / extends earlier findings |
| is closely related to | is tied to / tracks with |
| has been widely / extensively studied | has received considerable study |
| significant positive effect | positive and statistically significant effect (keep exact stats; vary the framing) |
Keep variable names, hypothesis labels, and statistics exact (Gate B); only the generic phrasing changes, and the underlying claim must stay identical (Gate C).

**Predicate-position hyphen (optional, low-priority, STRICTLY subordinate to Gate D).** A weak lexical signal: AI hyphenates generic descriptive compounds uniformly in every position, including predicate position ("the framework is data-driven", "the design is cross-sectional" used predicatively). Where a human writer would more often drop the hyphen in predicate position ("the framework is data driven"), you MAY de-hyphenate — but only for generic, non-technical descriptive compounds, and only when it does not risk any conflict with Gate D. NEVER de-hyphenate protected technical terms, variable names, or established constructs ("self-efficacy", "employee-AI", "AI-generated", "cross-domain", "human-AI"), and NEVER touch a compound modifier sitting before its noun ("a data-driven framework" keeps the hyphen). When in doubt, leave the hyphen exactly as written. This is a marginal touch-up, not a priority technique; skip it entirely if it would compete with Gate D's hyphen-protection. See Deep Audit item 10 in detection_principles.md.

---

## Technique 11: Non-Native Academic Rhythm

**Principle**: Make the writing sound like a competent non-native English master’s thesis, not like a polished AI essay.

This does not mean adding errors. It means avoiding prose that is too perfect, too balanced, or too native-like.

Use:

- slightly simpler sentence structures
- occasional direct explanation
- less elegant but clearer wording
- fewer polished transitions
- fewer abstract nouns stacked together

Avoid:

- intentional grammar errors
- spelling mistakes
- slang
- contractions
- casual questions in formal thesis sections
- promotional tone
- AI-flavored "elegant" phrases that actually raise AI suspicion: "it is noteworthy that", "more importantly", "sheds light on", "offers a nuanced understanding", "fills a critical gap", "plays a pivotal role", "underscores the significance", "a rich tapestry", "delve into". Prefer plain connectives instead ("To address this issue,", "For this reason,", "In this model,", "This means that,").
- Persuasive-authority throat-clearers that announce depth instead of delivering it: "the real question is", "what really matters is", "at its core", "at the heart of", "the deeper issue is", "fundamentally" (as a throat-clearer, not a precise technical qualifier), "in essence". State the point directly and keep its content (Principle 4); delete only the empty framing, never the substantive claim. Do not touch a correct technical use of "fundamental(ly)". Full list and false-positive cautions are in Gate J.

**Too polished**:
> This finding offers a nuanced and theoretically meaningful account of how technologically mediated work arrangements reshape the psychological foundations of employee innovation.

**Better for thesis**:
> This finding helps explain how AI-supported work may influence employees’ psychological state and then affect innovative behavior.

---

## Technique 12: Abstract Word Reduction

**Principle**: Reduce excessive abstract expressions when a concrete explanation is possible.

Common abstract words to control:

- mechanism
- framework
- context
- relationship
- significant effect
- provide evidence
- further explain
- pathway
- dynamic
- multidimensional
- theoretical contribution
- practical implication

**Before**:
> This study provides evidence for the mechanism through which Employee–AI Collaboration affects Employee Innovative Behavior in the organizational context.

**After**:
> The results show that Employee–AI Collaboration is related to Employee Innovative Behavior partly because employees may become more confident, more engaged, or more inspired when working with AI.

**Caution**:
Do not remove required academic terms entirely. For example, “mediating mechanism” may be necessary in a mediation model, but it should not appear in every sentence.

---

## Technique 13: Reasoning Visibility

**Principle**: Show the reasoning process instead of only giving polished conclusions.

**Before**:
> Employee–AI Collaboration positively affects Self-Efficacy. Therefore, H1 is proposed.

**After**:
> When employees work with AI, they may obtain information faster and receive support for some complex tasks. This can reduce uncertainty during work. If employees feel that they can handle these tasks better with AI support, their Self-Efficacy may increase. Thus, H1 is proposed.

**Use this especially in**:
- hypothesis development
- theoretical model explanation
- mediation logic
- discussion of empirical findings

**Epistemic stance (conservative)**: human reasoning is not uniformly certain. State conclusions that the thesis's own data actually support plainly and directly; for steps that are genuinely tentative in the original argument, keep the hedging the author already used ("may", "partly", "one possible reason"). Do NOT manufacture a "certain-then-hesitant" rhythm as an engineering trick, do not move hedges onto statistically supported hypothesis-test results, and do not change any statistical conclusion. The only goal is to keep the natural mix of certainty that is already present, not to fabricate doubt or confidence.

---

## Technique 14: Paragraph Architecture Rebuilding

**Principle**: external-detector-style AI detection can be sensitive to repeated paragraph architecture. If several paragraphs follow the same internal order, changing single words is not enough.

Use this technique when paragraphs follow patterns such as:

- topic sentence → explanation → citation → implication → conclusion
- definition → citation → general importance → research gap
- variable description → mechanism explanation → hypothesis
- result → explanation → implication
- contribution → practical implication → future research

**Before**:
> Previous studies have shown that Self-Efficacy is an important factor affecting employee behavior. Self-Efficacy can help employees deal with difficult tasks and improve their confidence. Therefore, Self-Efficacy may mediate the relationship between Employee–AI Collaboration and Employee Innovative Behavior. Based on the above analysis, the following hypothesis is proposed.

**Better thesis version**:
> Self-Efficacy is relevant here because employees do not respond to AI tools only at the technical level. When AI helps them search information, compare alternatives, or reduce uncertainty in work tasks, they may judge their own ability more positively. This psychological change may partly explain why Employee–AI Collaboration is related to Employee Innovative Behavior. The hypothesis is stated as follows.

**How to apply**:
- Start with the variable logic instead of a broad literature claim.
- Move the concrete reasoning earlier.
- Avoid ending every paragraph with “based on the above analysis”.
- Make the hypothesis sentence less mechanical.
- Keep all citations and hypothesis wording unchanged.

---

## Technique 15: Section-Level Pattern Diversification

**Principle**: A thesis can look AI-generated when every paragraph in a section has the same rhythm. This technique diversifies the section without changing meaning.

### Literature Review

Do not make every paragraph follow:

> definition → author citation → importance → gap

Alternative structures:

1. concept problem → prior finding → relevance to this thesis
2. cited finding → limitation in relation to the present model
3. variable explanation → why it matters for EAC/IB
4. comparison of two studies → remaining question

### Hypothesis Development

Do not make every paragraph follow:

> variable explanation → mechanism → hypothesis

Alternative structures:

1. start from employee work situation
2. explain the psychological change
3. connect the change to the dependent variable
4. state the hypothesis

### Discussion

Do not make every paragraph follow:

> result → explanation → theoretical implication → practical implication

Alternative structures:

1. result → why this result is reasonable → limitation of interpretation
2. result → connection to one variable → cautious implication
3. result → comparison with expectation → what remains unclear

### Conclusion

Do not make every paragraph follow:

> contribution → practical value → limitation → future research

Alternative structures:

1. main finding → what it clarifies → what it does not prove
2. practical implication → condition under which it applies
3. limitation → why it matters → cautious future direction

**Strict rule**: If more than one paragraph in the same section has the same opening, same middle logic, and same ending pattern, rewrite the section pattern before polishing individual sentences.

---

## Technique 16: Shared External-Risk Structural Pass

**Principle**: When CNKI AIGC, Turnitin AI, GPTZero, Originality.ai, or another external detector reports a high AI score, perform a second structural rewrite pass after normal revision. The external detector is used ONLY as risk-location evidence: this pass builds no detector-specific rewrite path and never attempts to reverse-engineer or bypass a detector — the techniques are identical regardless of which detector is in play.

Checklist for the second pass:

- [ ] Do several paragraphs start with the same type of sentence?
- [ ] Do several paragraphs end with broad summary sentences?
- [ ] Are “This study”, “Therefore”, “Based on this”, and “In this context” repeated across the paper?
- [ ] Does the literature review repeatedly use citation-after-general-claim rhythm?
- [ ] Does each hypothesis paragraph have nearly the same architecture?
- [ ] Does the discussion sound too complete and smooth?
- [ ] Are abstract words such as “mechanism”, “framework”, “relationship”, “effect”, and “implication” repeated too often?
- [ ] Are verbs such as “indicate”, “suggest”, “show”, “demonstrate”, and “provide” used repeatedly?
- [ ] Does the revised text sound too polished for a non-native master’s thesis?

If several answers are yes, the paragraph or section still needs revision.

---
## Technique 17: Methodological Template Breaking (length-preserving)  
**Targets**: D16 Methodological Template Intensity

**Principle**:  
Methodology, variable measurement, questionnaire design, reliability testing, validity testing, and empirical-result sections often become AI-risk sections when they repeat the same procedural sentence pattern. This technique reduces repeated methodology/reporting templates by RESTRUCTURING the information and changing sentence order — never by compressing or deleting it. It breaks the repeated “purpose → threshold → result → conclusion” phrasing while keeping each paragraph at least as long as the original.

**Use this technique when the text repeats patterns such as:**
- The variable is defined as...
- This study adapts the scale from...
- The final scale includes X items...
- The purpose of this test is...
- The results show that...
- This indicates that...
- The value is above the threshold...
- Therefore, the result is acceptable...

**How to apply (LENGTH-PRESERVING — every "Better" version must be as long as or longer than the original):**

1. **De-template repeated variable-measurement patterns by restructuring AND adding specificity (not by compressing)**

Weak template:
> The variable is Self-Efficacy. It refers to employees’ belief in their own ability. This study adapts the scale from Zhang et al. (2020). The final scale includes five items.

Better (different structure, equal-or-greater length, all information kept):
> Among the constructs measured in this study, Self-Efficacy captures the extent to which employees believe in their own ability to carry out work tasks under AI assistance. To operationalise it, the study drew on the established scale developed by Zhang et al. (2020) and adapted the wording to the employee–AI collaboration setting, retaining five items in the final version.

2. **Recast procedure and reason without shortening**

Weak template:
> The reliability test was conducted. The purpose was to examine internal consistency. The Cronbach’s alpha value was above 0.7. This indicates that the scale has good reliability.

Better (recast, not compressed):
> Because several constructs in the questionnaire relied on multiple items, internal consistency had to be confirmed before any further analysis. A reliability test was therefore conducted, and the resulting Cronbach’s alpha value exceeded 0.7, which indicated that the scale held together well enough to be used in the subsequent steps.

3. **Change the order of reporting while keeping every element**

Weak template:
> The purpose of the KMO test is to examine whether the data are suitable for factor analysis. The KMO value was 0.856. This indicates that the data are suitable for factor analysis.

Better (reordered, equal-or-greater length):
> The KMO value reached 0.856 in this study. Since the KMO test is used to judge whether a dataset is appropriate for factor analysis, a value at this level indicated that the present data comfortably met that requirement, and the analysis could proceed to the validity test.

4. **Avoid repeating the same reporting sentence across variables**

Do not write every variable paragraph as:
> X refers to... This study uses... The final scale includes...

Use different entry points (measurement source, research role of the variable, questionnaire content, item focus, empirical model position), and keep each variable's paragraph at least as long as the original by adding context such as why the scale fits the AI-collaboration setting or how the items were adapted.

5. **Diversify the control-variable description block (a common hidden template region)**

When 3+ control variables are listed as parallel near-identical sentences ("Age was included as a control variable. Gender was included as a control variable. Education was included as a control variable. Tenure was included as a control variable."), de-template using ONE of these — each only reorganises or contextualises information already in the thesis, adds nothing, deletes nothing:
- Grouped statement: group by type — "The model included two demographic controls (age and gender) and two work-related controls (education and organizational tenure)."
- Reason-differentiated: give each control the inclusion reason already implied by the design — "Age was held constant because creative output varies across career stages; gender entered the model given documented differences in workplace risk-taking; education was retained as a proxy for prior training; tenure captured organizational embeddedness."
- Measurement-differentiated: describe each control's coding — "Age was measured in years; gender was coded as a dummy variable (1 = male, 0 = female); education was coded into four ordinal levels; tenure was the number of years in the current organization."
Rule: never leave 3+ consecutive "X was included as a control variable" sentences with identical structure. Reasons used must be supportable from the thesis; do not invent a justification the paper does not support.

**Strict rules:**
- Do not change variable names.
- Do not change scale sources.
- Do not change item numbers.
- Do not change thresholds, coefficients, p-values, table numbers, model numbers, or conclusions.
- Do not add new methodological procedures.
- Do not make methodology sound casual.
- Do not solve D16 by synonym replacement only.
- Do NOT reduce word count. Every rewritten paragraph must be ≥ the original length.

**Execution evidence must show:**

```text
T17 used: Yes / No
Repeated methodology/reporting template:
Template-breaking method (structural change applied):
Original word count / Revised word count / Change %:
Original protected elements:
Revised protected elements:
Protected elements status:
```

---

---


## Technique 18: Sequence Reordering (length-preserving)
**Targets**: D17 Predictable Reporting Sequence

**Principle**:  
A paragraph or paragraph group becomes AI-like when several parts of the thesis follow the same reporting order. This technique reduces predictable sequence risk by changing the order of steps and varying paragraph entry points while preserving meaning, all protected elements, AND word count. It does NOT merge or delete steps — reordering is the tool, not compression.

**Use this technique when several paragraphs repeat sequences such as:**
- definition → scale source → number of items;
- variable explanation → mechanism → hypothesis;
- test purpose → threshold → numerical result → conclusion;
- coefficient → significance → hypothesis supported;
- result → explanation → theoretical implication → practical implication;
- finding summary → contribution → implication → limitation.

**How to apply (every "Better" version must be as long as or longer than the original):**

1. **Change the entry point**

Weak repeated sequence:
> The purpose of this test is to examine reliability. The Cronbach’s alpha value is above 0.7. This indicates that the scale has good reliability.

Better (reordered, equal-or-greater length):
> The Cronbach’s alpha value came out above 0.7 in this case. Because alpha is the indicator used to judge reliability, a value at this level meant that the scale's internal consistency was sound, which was a precondition before the structural relationships could be tested.

2. **Reorder the middle steps (do NOT merge them)**

Weak repeated sequence:
> The coefficient is positive. The significance level is below 0.05. This means that the hypothesis is supported.

Better (reordered and kept as separate steps, equal-or-greater length):
> The hypothesis predicted a positive relationship, and the analysis bore this out: the coefficient carried a positive sign, and its significance level fell below the 0.05 threshold. Taken together, these two results provided the support the hypothesis required.

3. **Vary hypothesis-development order**

Weak repeated sequence:
> Variable A influences Variable B. Variable B influences Variable C. Therefore, the following hypothesis is proposed.

Better:
> The logic of this hypothesis starts from Variable C. If Variable B changes how employees approach innovation-related work, then Variable A may influence Variable C through this psychological path.

4. **Break result → implication loops**

Weak repeated sequence:
> The result supports H1. This finding enriches the literature. It also provides practical implications.

Better:
> The result supports H1. In this thesis, the more important point is that the tested relationship remains positive after the control variables are included.

5. **Use section-level variation**

If several neighboring paragraphs repeat the same structure, do not fix only one paragraph. At least one paragraph in the group should change:
- opening logic;
- middle explanation order;
- result placement;
- closing sentence type;
- connection to table, hypothesis, variable, or model.

6. **Result-explanation variant library (rotate across parallel result paragraphs)**

When many result paragraphs share the "coefficient → significance → hypothesis supported → brief note" template, give each a DIFFERENT structure. All content comes from the original; only order and framing change, length stays equal or greater:
- Result-first: open with the supported result, then state the coefficient and significance — "H1 is supported by the positive, significant path from EAC to IB (β = 0.32, p < 0.01)."
- Mechanism-embedded: state what was controlled, then the result — "Even after gender and age are controlled, the EAC→IB path stays positive and significant (β = 0.32, p < 0.01)."
- Contrast entry: lead with an expected-vs-found contrast already in the data — "Unlike the control variable tenure, which was not significant (β = 0.05, p > 0.1), the core path from EAC stayed significant (β = 0.32, p < 0.01)."
- Table-anchored: enter from the table cell — "In Model 2 of Table 4.3, the EAC coefficient is 0.32 and significant at the 1% level, which supports H1."
- Meaning-first: open from what the result tells the study, then give the statistics — still without changing the statistical conclusion.
Rotate these so no two adjacent result paragraphs use the same one. Never change a coefficient, p-value, sign, or the supported/not-supported conclusion.

7. **Table/figure narration: from whole-table description to specific focus**

AI narrates tables generically ("As shown in Table 4.3, the results indicate that..."). Re-enter from a specific number that is already in the table:
> In Table 4.3, the EAC-to-Self-Efficacy path has a coefficient of 0.42 (significant at the 1% level), which supports H1.
Rules: the focused number must already exist in the table; do not omit any reported result that matters; do not change any value; one or two focal numbers per table paragraph is enough. This breaks the "Table X shows / Figure Y illustrates" template without inventing anything.
COMPARATIVE-CLAIM GUARD: do NOT describe a coefficient as the strongest, highest, lowest, weaker, more/most important, or "noticeably higher than" the others UNLESS the original thesis already makes that comparison. Reporting one value accurately is allowed; ranking or comparing values that the original did not rank is a new inferential claim and is forbidden in a results paragraph.

**Strict rules:**
- Do not change the hypothesis statement.
- Do not change statistical meaning.
- Do not change citation meaning.
- Do not add new implications.
- Do not reorder information if the new order makes the academic logic unclear.
- Do not use random short sentences as sequence disruption.
- Do not merge or delete steps. Reorder them as separate steps so word count does not fall.
- Every rewritten paragraph must be ≥ the original length (Principle 4).

**Execution evidence must show:**

```text
T18 used: Yes / No
Original word count / Revised word count / Change %:
Repeated sequence detected:
Original sequence:
Revised sequence:
Sequence change type:
Protected elements affected:
Protected elements status:
```

---

## Technique 19: Researcher-Trace Relocation and Local Integration  
**Status**: High-Efficiency Strategy / Validated, BUT carries the highest misuse risk in the entire skill  
**Targets**: D3, D9, D12, D14, D15, D16, D17

⛔ **FATAL WARNING — read first.**
Any "researcher-trace" sentence that is freshly *generated* by an LLM is statistically as AI-flavored as any other AI-generated sentence. A detector cannot tell that the sentence is "researcher-trace" — it just sees new model-generated prose. Therefore:
- Do NOT compose new researcher-trace sentences from scratch. Doing so is the single most common way T19 backfires.
- Use T19 by EXTRACTING researcher-judgment material that already exists somewhere in the thesis (a different paragraph, the discussion section, the limitations section, a footnote, a methodology aside) and re-locating or lightly rephrasing it where it serves the local argument.
- Where no suitable existing material exists, do not invent it — apply a different technique (T20/T21/T22/T23) instead. T19 is not a default; it is a placement and extraction technique, not a generation technique.
- Every T19 insertion must trace to specific original wording in the thesis. State the source location in the execution evidence.

**Three trace types (resolves the "what if the thesis has no ready-made researcher sentence?" problem).**
- Type A — Direct relocation (THIS technique, T19): move or lightly rephrase a researcher-judgment / decision / limitation sentence that ALREADY EXISTS elsewhere in the thesis to the high-risk paragraph. T19 never composes a new sentence; it only relocates, splits, or lightly adjusts existing researcher-side material. This is the entirety of what T19 does.
- Type B — Evidence-based reconstruction (NOT T19 — this is T29): when no ready-made sentence exists but the paper DOES contain the underlying facts, composing ONE new sentence that states only what is already traceable is handled exclusively by T29 (Evidence-Based Authorship Restoration), under its four mandatory checks. If an operation composes any new sentence, classify and log it as T29, never as T19.
- Type C — Forbidden fabrication: researcher feelings, surprise, memories, positionality not stated in the thesis, non-verbal observations, undocumented coding struggles, undocumented participant silence. Never.

Hard separation rule: **T19 never creates a new interpretive sentence.** If a new sentence must be composed from existing evidence, the operation is T29, not T19. Evidence must be logged accordingly (T19 → "relocated from <location>"; T29 → "reconstructed from <data/method/theory/cited work>").

**Research-design branching.**
T19 is NOT applied uniformly across thesis types. Before using T19, identify the research design:
- Quantitative empirical paper (survey, SEM, regression, ANOVA, experiment, hypothesis-testing) → use **T19-A** safety matrix below.
- Qualitative paper (interviews, case study, grounded theory, ethnography, thematic / discourse / content analysis) → use **T19-B** safety matrix below.
- Mixed-methods paper → apply T19-A to the quantitative parts (hypothesis development, measurement, statistical analysis, regression/SEM results) and T19-B to the qualitative parts (interview design, coding process, case description, thematic findings, qualitative discussion).

### T19-A — Quantitative paper section-safety matrix

| Insertion subtype                | Lit Review | Hypothesis | Methodology | Empirical Results | Discussion/Conclusion |
|----------------------------------|:---------:|:----------:|:-----------:|:-----------------:|:---------------------:|
| Researcher judgment              | ⚠ Medium  | ✅ Safe   | ⚠ Medium    | ❌ High risk      | ✅ Safe              |
| Process narration                | ✅ Safe   | ❌ High   | ✅ Safe     | ❌ High risk      | ⚠ Medium             |
| Scope limitation                 | ✅ Safe   | ✅ Safe   | ✅ Safe     | ✅ Safe           | ✅ Safe              |
| Boundary / limitation            | ⚠ Medium  | ⚠ Medium  | ⚠ Medium    | ✅ Safe           | ✅ Safe              |
| Existing-data anchor             | ❌ High   | ❌ High   | ⚠ Medium    | ✅ Safe           | ✅ Safe              |
| Supported contrast / counterpoint| ✅ Safe   | ✅ Safe   | ❌ High     | ⚠ Medium         | ✅ Safe              |
| Anticipated reader question      | ⚠ Medium  | ⚠ Medium  | ❌ High     | ❌ High risk      | ⚠ Medium             |

For empirical-result paragraphs (Chapter 5), prefer scope/boundary/data-anchor types; avoid judgment and reader-question insertions there.

### T19-B — Qualitative paper section-safety matrix

In qualitative research, researcher judgement, process narration, coding-path explanation, data anchoring, and reflexive clarification are methodologically expected. Safety depends on whether the inserted sentence is grounded in actual interview data, case materials, coding decisions, observation records, or documented analytical procedures from the original paper.

| Insertion subtype                 | Lit Review | Research Design / Methodology | Data Analysis / Coding | Findings  | Discussion/Conclusion |
|-----------------------------------|:---------:|:-----------------------------:|:----------------------:|:---------:|:---------------------:|
| Researcher judgement              | ⚠ Medium  | ✅ Safe                      | ✅ Safe                | ⚠ Medium  | ✅ Safe              |
| Process narration                 | ✅ Safe   | ✅ Safe                      | ✅ Safe                | ✅ Safe   | ⚠ Medium             |
| Scope limitation                  | ✅ Safe   | ✅ Safe                      | ✅ Safe                | ✅ Safe   | ✅ Safe              |
| Boundary / limitation             | ⚠ Medium  | ✅ Safe                      | ✅ Safe                | ✅ Safe   | ✅ Safe              |
| Data anchoring (quote/case/code)  | ⚠ Medium  | ✅ Safe                      | ✅ Safe                | ✅ Safe   | ✅ Safe              |
| Supported contrast / counterpoint | ✅ Safe   | ⚠ Medium                     | ✅ Safe                | ✅ Safe   | ✅ Safe              |
| Anticipated reader question       | ⚠ Medium  | ⚠ Medium                     | ⚠ Medium               | ⚠ Medium  | ⚠ Medium             |
| Reflexive clarification           | ❌ High   | ✅ Safe                      | ✅ Safe                | ⚠ Medium  | ✅ Safe              |
| Interpretation-path explanation   | ⚠ Medium  | ✅ Safe                      | ✅ Safe                | ✅ Safe   | ✅ Safe              |
| Case contextualisation            | ✅ Safe   | ✅ Safe                      | ✅ Safe                | ✅ Safe   | ✅ Safe              |

Rules for qualitative papers:
- Researcher-trace insertions are safer when they explain how themes, categories, codes, or interpretations were developed from actual data already reported in the paper.
- Do NOT add interview evidence, participant quotations, coding results, field notes, or case details that do not exist in the original paper.
- In Findings, researcher judgment must be tied to participant accounts, case evidence, coded themes, or repeated patterns already in the paper.
- Reflexive clarification is appropriate in Methodology, Data Analysis, and Discussion sections, but not in Literature Review unless the original paper explicitly discusses researcher positionality.
- The safest qualitative researcher-trace sentence explains analytical movement: from raw data to code, from code to theme, or from theme to theoretical interpretation — using only material the paper already contains.

**Principle**:  
When a descriptive paragraph reads too smooth, too neutral, or too mechanically explanatory, add one supported sentence that shows the author's research-side judgment, narrowing process, decision trace, or process-based explanation — sourced from existing thesis content.

This technique was previously observed as potentially useful for reducing AI-like descriptive writing patterns in a specific revision context; effectiveness is not guaranteed and must be confirmed by a comparable external re-test. It is valid ONLY when applied as extraction-and-relocation, NEVER as generation.

**Use this technique when the paragraph:**
- mainly describes a concept, variable, method, procedure, or result;
- reads like a textbook explanation;
- lacks visible author-side reasoning;
- follows a smooth claim → explanation → implication structure;
- has a high D3, D9, D12, D14, D15, D16, or D17 risk;
- is part of a long continuous AI-like fragment.

**Allowed insertion types:**
1. Researcher-view judgment  
   - Example: “For this thesis, this point is more relevant than the broader debate because the model focuses on employee-level psychological changes.”

2. Process narration  
   - Example: “The measurement choice was made mainly to keep the questionnaire consistent with the variables used in the empirical model.”

3. Scope narrowing  
   - Example: “The present analysis therefore keeps the discussion within the workplace innovation context, rather than extending it to general AI adoption.”

4. Boundary or limitation sentence  
   - Example: “This interpretation should be limited to the tested variables and should not be read as evidence for all types of AI use.”

5. Existing-data anchor  
   - Example: “This is also why the explanation should be read together with the coefficient reported in Table 4.6.”

6. Supported contrast or counterpoint  
   - Example: “However, this does not mean that AI use automatically leads to innovation; the mediating variables still need to be considered.”

7. Anticipated-reader-question (use sparingly in formal thesis prose)  
   - Express a likely objection and the thesis's response as part of the argument, NOT as a staged dialogue. Prefer an indirect form over a literal "the reader may ask".
   - Acceptable indirect form: “One concern here is whether this association merely reflects general technology use; the controls for AI-usage frequency make that explanation less likely.”
   - Avoid overt conversational forms ("Some readers might wonder… In response, this paper argues…") unless the thesis already uses that voice; in most master's theses keep it embedded in the argument.

**Restrictions:**
- Do not add new data.
- Do not add new references.
- Do not add new theoretical claims.
- Do not add personal opinion unrelated to the thesis.
- Do not insert random short sentences only to break rhythm.
- Do not use this technique as a substitute for fixing repeated paragraph architecture.
- MUST FIT THE LOCAL ARGUMENT. The inserted sentence has to connect logically to the sentence before it and the sentence after it, and read as the author's natural reasoning within that paragraph's topic. It must NOT read as an out-of-place aside that explains or justifies the writing or the research design from outside the argument.
- EXTRACTION-ONLY, NEVER GENERATION. The inserted sentence MUST be sourced from existing thesis content (a different paragraph, the discussion section, the limitations section, a footnote, a methodology aside). Lightly rephrasing existing material to fit grammatically is allowed; composing a new sentence from scratch is not. Freshly generated sentences read as AI-flavored regardless of how "researcher-like" they sound.
- IF NO EXISTING MATERIAL EXISTS, do not invent one. Apply T20 / T21 / T22 / T23 instead — those work on existing wording without inserting new sentences.
- FORBIDDEN form: bald justifications of methodology or of the rewrite, dropped in without connection, e.g. "This detail was included to improve measurement precision." or "This sentence is added to clarify the logic." These create logic jumps and look machine-inserted. If a process-narration sentence cannot be phrased so it flows from the surrounding text, do not insert it here — vary the paragraph another way.
- At most ONE researcher-trace sentence per paragraph in normal use; only at the highest escalation rung may density rise, and even then every inserted sentence must still connect smoothly to its neighbours.
- After inserting, re-read the paragraph start to finish: it must read as one continuous line of reasoning with no abrupt jump. Gate J will reject any insertion that does not.

**Execution evidence must show:**
```text
T19 used: Yes / No. T29 used: Yes / No. (Do not merge them into one checkbox.) If either is Yes, include the Source Trace block and identify the operation type — see the T19/T29 source-annotation rule
Research design (quantitative / qualitative / mixed):
T19-A or T19-B matrix applied:
Section being rewritten and the safety rating from the matrix:
Operation type: relocated sentence / split sentence / lightly integrated clause / locally repositioned researcher-trace material / no insertion (T19 is relocation, not mandatory insertion; a new sentence built from existing facts is T29, not T19)
Source location of the relocated or reconstructed material (which existing thesis location it was extracted from): MUST be filled when T19 or T29 is used
Resulting sentence or clause:
Reason for placing or integrating it here:
Protected elements affected:
Whether the result is supported by existing thesis content (must be Yes):
```


---

## Technique 20: Verb-Phrase Expansion (Targets D5/D11, supports word-count preservation)

**Status**: Length-preserving / Length-adding

**Principle**:
Generic single verbs ("analyze", "examine", "test") are statistically predictable and contribute to flat, AI-like phrasing. Expanding a bare verb into a short process-describing phrase reduces lexical flatness AND adds words, which helps satisfy the word-count-preservation rule (Principle 4). Use it especially where de-templating elsewhere removed words.

**How to apply**:
- Replace a bare generic verb with a phrase that names the actual process, using only information already in the thesis.

Examples (English):
- "analyze the data" → "work through the data step by step" / "carry out a structured examination of the data"
- "test the hypothesis" → "put the hypothesis through the regression and bootstrap procedures described above"
- "examine the relationship" → "look closely at how the two variables move together"
- "improve performance" → "lead to a measurable improvement in performance"

**Restrictions**:
- Do NOT change the meaning, the method, or any protected element (variable names, statistics, citations).
- Do NOT invent new procedures — the expansion must describe what the thesis actually did.
- Do NOT inflate every verb; over-using this turns into its own template. Apply it selectively where lexical flatness (D11) or generic phrasing (D5) is detected, or where a paragraph needs to regain words lost during de-templating.
- Keep the result grammatical and within the sentence-length limit (~30 words, Gate H).
- Do NOT make the verb phrase sound promotional or dramatic; keep a plain thesis register.

**Execution evidence must show:**
```text
T20 used: Yes / No
Original verb / expanded phrase:
Words added:
Meaning and protected elements unchanged: Yes / No
```

---

## Technique 21: Parenthetical Integration (Targets D11/D14, supports word-count preservation)

**Status**: Length-preserving / Length-adding

**Principle**:
Strings of parenthetical asides — especially abbreviation glosses and short clarifications — are a recognisable machine-edited pattern and also make prose choppy. Folding a parenthetical into the running sentence with a natural connective ("that is", "in other words", "namely", "which refers to") reduces that pattern and reads more like human academic prose. It usually adds a few words, which also helps word-count preservation.

**How to apply**:
- Turn "(...)" into an integrated clause introduced by a light connective.

Examples (English):
- "perceived organizational support (POS) influences…" → keep the abbreviation but integrate any *explanation*: "perceived organizational support, that is, employees' sense that the organization backs their work, influences…"
- "the model fit was acceptable (CFI = 0.95)" → "the model fit was acceptable, with a CFI of 0.95"
- "employees used generative AI tools (for example, chatbots and writing assistants)" → "employees used generative AI tools such as chatbots and writing assistants"

**CRITICAL protected-element rule**:
- An abbreviation's FIRST definition is a protected element. When a term is first introduced with its abbreviation — e.g. "Employee–AI Collaboration (EAC)" — you must KEEP both the full term and the "(EAC)" tag exactly. Do NOT dissolve the defining abbreviation, because later text depends on it.
- Technique 21 integrates the surrounding *explanatory* parentheses and glosses, NOT the canonical "Full Term (ABBR)" definition pair. When in doubt, leave the abbreviation definition untouched.
- Never change variable names, statistics, citations, or table references while integrating.

**Restrictions**:
- Do not integrate a parenthetical if doing so would lengthen the sentence past the ~30-word / two-clause limit (Gate H); instead make it a short separate sentence.
- Do not delete the parenthetical content — integrate it (Principle 4: no shrinking).
- Keep the result grammatically complete (Gate H) and correct (Gate I).

**Execution evidence must show:**
```text
T21 used: Yes / No
Original parenthetical / integrated form:
Abbreviation definitions preserved: Yes / No
Words added (not removed):
```

---

## Technique 22: Detail-Rich Core and Keyword Cohesion (Targets D3/D12/D14, length-preserving)

**Status**: Length-preserving / Length-adding only

**Principle**:
AI prose tends to spread effort evenly — every point gets the same shallow treatment, producing a flat "average-emphasis" texture. Human academic writing has relief: the core argument of a paragraph is developed in more depth, while routine points stay brief. This technique adds undulation by EXPANDING the core, and improves author-baseline flow by carrying a keyword forward from the previous sentence or opening a paragraph from the previous paragraph's conclusion.

**IMPORTANT — no background condensation (per Principle 4):**
- This technique creates relief ONLY by writing the core argument in MORE detail. It must NEVER shorten or condense the background/common-knowledge parts to create contrast.
- Do not delete or compress any sentence to make the paragraph "uneven". The word count of every paragraph must stay at or above the original (Principle 4, Gate F).
- The "undulation" comes from the core being expanded, not from the background being cut.

**How to apply**:

1. Detail-rich core (expansion only)
   - Identify the paragraph's central claim. Develop it further using material already in the thesis: spell out the mechanism, connect it to a reported result, or state its scope. This adds words to the core.
   - Leave routine/background sentences as they are — do not lengthen them to match, and do not shorten them either.

2. Keyword-borrowing cohesion
   - Open a sentence by picking up a key noun from the end of the previous sentence, so the reader feels a natural thread. Example: "...shaped by perceived organizational support. This support, in turn, ..."
   - Where appropriate, begin a paragraph from the conclusion of the previous paragraph (a "given X, ..." link), WITHOUT moving or reordering the paragraphs themselves (Principle 7 — paragraph order is fixed).

**Restrictions**:
- Expansion must use existing thesis content only — no new data, citations, or claims.
- Keep every sentence complete and within the ~30-word / two-clause limit (Gate H); if the expanded core gets long, split into two complete sentences (do not merge, do not exceed paragraph caps — Gate G).
- Cohesion links must read naturally and must not become a new repeated template (do not start every paragraph with the same linking device).
- Never reorder paragraphs or change the chapter's argument flow (Principle 7).

**Execution evidence must show:**
```text
T22 used: Yes / No
Core claim expanded (from existing content): Yes / No
Background condensed: must be No
Cohesion link added (keyword carried forward / prior-conclusion opener):
Paragraph word count (original / revised, must be ≥):
```

---

## Technique 23: Information-Progression Rewrite (de-mechanize "This study…" and outline-style intros) (Targets D3/D12, length-preserving)

**Status**: Length-preserving / Length-adding only

**Principle**:
A very common machine-assembled pattern is the paragraph where almost every sentence starts with the same subject and announces what the writer is doing: "This study examines… / This study focuses on… / This study provides… / This helps explain…", and the chapter-arrangement paragraph where every sentence is "Chapter 2 builds… / Chapter 3 develops… / Chapter 4 lays out…". It is grammatical and clear, but it reads like an expanded outline, not integrated academic prose. The fix is NOT to swap "This study" for synonyms — that just makes a new template. The fix is to change HOW information advances: let the research object, the problem, or the logical relationship carry the sentence.

**Use when a paragraph shows:**
- three or more sentences with the same "This study / The study / It" subject;
- a chapter-arrangement paragraph written as "Chapter X does …" line after line;
- a "definition → explanation → summary" mechanical triple.

**How to apply (three moves; all keep word count ≥ original):**

1. **Make the research object the subject, not "This study".**
   Mechanical:
   > This study examines the psychological mechanisms linking employee–AI collaboration with innovative behavior. The analysis focuses on self-efficacy, work engagement, and creative inspiration as possible mediating variables. Their different effects are also compared.
   Better:
   > The psychological mechanisms between employee–AI collaboration and innovative behavior are examined through three mediating variables: self-efficacy, work engagement, and creative inspiration. Rather than treating these mechanisms separately, the analysis compares their relative explanatory roles within the same model.

2. **Turn "definition → explanation → summary" into "problem → reason → handling".**
   Mechanical:
   > The study also analyzes the role of perceived organizational support for innovation in this relationship. More specifically, it tests whether perceived organizational support for innovation moderates the relevant paths in the proposed model.
   Better:
   > The relationship between employee–AI collaboration and innovative behavior may not be equally strong in all organizational contexts. For this reason, perceived organizational support for innovation is introduced as a boundary condition, to test whether organizational support changes the strength of the proposed paths.

3. **Write chapter arrangement as a research flow, not a table of contents.**
   Mechanical:
   > Chapter 2 builds the theoretical foundations and literature review. It reviews social cognitive theory, conservation of resources theory, and organizational support theory. It then discusses prior studies…
   Better:
   > After the introduction, the thesis first establishes the theoretical basis for the research model. Chapter 2 reviews social cognitive theory, conservation of resources theory, and organizational support theory, and then connects these theories with prior studies on employee innovative behavior, employee–AI collaboration, and the relevant psychological variables.

**Reusable transformation pattern:**
```text
Mechanical:                         Logic-driven:
This study examines A.        →     A remains insufficiently explained in prior research.
This study focuses on B.      →     To address this, B is introduced as the analytical focus.
This study provides C.        →     By linking A with B, the analysis clarifies how C occurs
This helps explain D.               and under what conditions D becomes stronger or weaker.
```

**Restrictions (keep it a master's thesis, not a journal showpiece):**
- Do NOT over-polish. Avoid AI-flavored "elegant" phrases — these read as MORE AI, not less. Forbidden phrase bank: "it is noteworthy that", "more importantly", "sheds light on", "offers a nuanced understanding", "fills a critical gap", "plays a pivotal role", "underscores the significance".
- Prefer plain human-academic connectives: "To address this issue,", "For this reason,", "In this model,", "This means that,", "The next step is to examine,", "The analysis then considers,", "This makes it possible to compare…".
- Use existing content only — no new claims, data, or citations.
- Do not reorder paragraphs or change the chapter's argument flow (Principle 7); this technique changes sentence-level information flow inside a paragraph, not the paragraph order.
- Keep every sentence complete and ≤ ~30 words / two clauses (Gate H), grammatically correct (Gate I), and the paragraph ≥ its original length (Gate F).
- Do not just replace "This study" with "The present research / This paper / The current work" as a disguise — that is still the same template and is not acceptable.

**Execution evidence must show:**
```text
T23 used: Yes / No
Repeated-subject or outline pattern detected:
Progression change applied (object-as-subject / problem-reason-handling / research-flow):
No forbidden over-polished phrases introduced: Yes / No
Paragraph word count (original / revised, must be ≥):
```

---

## Technique 24: Introduction and Abstract Anti-Template (Targets D3/D12/D15, length-preserving)

**Status**: Length-preserving / Length-adding only

**Principle**:
The Introduction and the Abstract are the highest-risk sections for AI-pattern detection because they almost always follow predictable academic structures (background → gap → value → research question; "This study examines… / The results show… / The findings suggest…"). Generic AI-style restructuring is not enough — the rewriting logic must follow the research design.

**Research-design branching.**
Before applying T24, identify the research design:
- Quantitative / hypothesis-testing / experimental / SEM-regression-ANOVA → use **T24-A**.
- Qualitative / interview / case study / grounded theory / thematic-discourse-content analysis → use **T24-B**.
- Mixed-methods → use T24-A for the quantitative parts of Intro/Abstract, T24-B for the qualitative parts.

Across both branches:
- Length-preserving (Principle 4): expand to reduce template-ness, never compress.
- Headings, abbreviations, citations, variables, hypotheses, statistics all remain protected (Gate B).
- All sentences pass Gate H (no fragments, ≤ ~30 words / two clauses) and Gate I (grammar / SVA / capitalization).

---

### T24-A — Quantitative Introduction / Abstract

**Introduction (quantitative)**:
1. Do not always follow the standard order of background → research gap → value → research question.
2. Where appropriate, start from a specific empirical phenomenon, managerial problem, statistical pattern, or practical contradiction — not from broad macro background.
3. Integrate research value into the concrete problem description, instead of placing theoretical and practical significance in a separate formulaic paragraph.
4. Reduce mechanical chapter-roadmap sentences such as "Chapter 2 reviews…, Chapter 3 introduces…" by recasting them into a less repetitive form (combined with T23). Preserve the substantive coverage of every chapter mentioned and keep the paragraph at its original length or longer — do not compress or drop chapter descriptions to reduce AI risk (Principle 4).
5. Avoid repeated openings such as "With the development of...", "In recent years...", "Therefore, this study...".

**Abstract (quantitative)**:
1. Avoid the fixed three-step pattern: "This study examines... The results show... The findings suggest...".
2. Consider opening with the main finding, relationship, or empirical problem rather than the research aim.
3. Present methodology in a less formulaic sequence while preserving all necessary methodological information and keeping the original word count or more. Do not compress methodological content for anti-template purposes (Principle 4).
4. Give more space to key results, boundary conditions, and implications.
5. Add one appropriate qualifier such as "within the sample tested", "based on the survey data", or "in the model examined".

### T24-B — Qualitative Introduction / Abstract

**Introduction (qualitative)**:
1. Do not mechanically follow the order broad background → literature gap → research value → research question.
2. Prefer opening from a concrete field phenomenon, participant experience, case tension, organizational situation, or interpretive puzzle — not from broad macro background.
3. Present the research problem as an interpretive difficulty, not only as a literature gap.
4. Integrate the value of the study into the explanation of why the phenomenon requires closer interpretation.
5. Avoid over-formulaic chapter-roadmap paragraphs. If structure must be described, recast it in a less mechanical form without removing required content or reducing the paragraph's word count (Principle 4).
6. Do NOT add field observations, interview details, case facts, or participant experiences that are not present in the original paper.

**Abstract (qualitative)** — recommended structure: Phenomenon / tension → Research focus → Data and method → Main themes → Interpretive implication → Boundary qualifier.
1. Do not force the abstract to begin with "This study aims to...". A qualitative abstract may begin with a phenomenon, tension, or context-specific problem.
2. Do not force the abstract to begin with final findings unless they are clearly supported by the original paper.
3. Keep methodology concise but transparent — usually mention data type, research context, and analysis approach.
4. Avoid the mechanical pattern "This study explores... The findings show... The study contributes...".
5. Give enough space to the main themes, interpretive insights, and contextual implications.
6. Use qualitative boundary qualifiers such as "within the cases examined", "based on the interview data", "among the participants interviewed", "in the organizational context studied", "within the scope of this study".
7. Do NOT use quantitative qualifiers ("within the sample tested") unless the paper includes statistical testing.
8. Avoid overstating generalizability. Frame qualitative findings as context-sensitive interpretations rather than universal effects.

**Restrictions (both branches)**:
- All claims must come from existing thesis content. Do not invent findings, data, participants, or contexts.
- Do not delete the gap or value content — relocate or integrate it (Principle 4: word-count preserved or increased).
- Headings, hypothesis numbers, variable names, and statistical values stay exact (Gate B).
- Keep grammar correct, no fragments, no over-polished/business-talk phrases (Gates H/I/J).

**Execution evidence must show:**
```text
T24 used: Yes / No
Research design (quantitative / qualitative / mixed):
T24-A or T24-B applied:
Section rewritten (Introduction / Abstract / both):
Anti-template moves applied (e.g. opening from phenomenon, qualifier added, roadmap recast without substantive deletion or word-count reduction):
Original word count / Revised word count / Change %:
```

---

## Qualitative-Only Techniques (T25–T28)

T25–T28 apply ONLY to qualitative papers (and the qualitative parts of mixed-methods papers). They target dimensions D18, D19q, D20, D21. Before using them, confirm the section is qualitative.

⛔ **Overriding integrity rule for ALL of T25–T28 (read first).**
These techniques de-template qualitative writing using ONLY material that already exists in the paper. You may relocate, reorder, recombine, and lightly rephrase what is already there. You may NOT:
- invent researcher feelings, reactions, or memories ("stayed with me", "I recognized", "the emotional weight was visible");
- invent non-verbal observations ("looking down, pausing for several seconds") unless the paper already records them;
- invent participant quotes, lengthen real quotes, or attribute words to a participant;
- invent a "silence" or "absence" that the paper does not document;
- invent positionality ("As a researcher who had also navigated...") unless the paper already states it.
Fabricating any of these is both an academic-integrity violation AND self-defeating: a freshly generated "researcher voice" sentence reads to a detector as AI text (same rule as T19). If the paper does not contain the material a technique needs, do not use that technique — choose another, or leave the passage.
All of T25–T28 are length-preserving (Principle 4), keep headings/quotes/citations intact (Gate B), and must pass Gates H/I/J.

## Technique 25: Transition De-Templating (qualitative) — Targets D18

**Principle**: Break the mechanical "Participant A mentioned... Similarly, Participant B also..." chain by connecting accounts through relationship and contrast rather than a fixed additive transition.

**How to apply (existing content only)**:
- Replace repeated "Similarly / Likewise / Also" links with the actual relationship between accounts that the data shows: agreement, divergence, extension, or tension.
- Vary the reporting verb and the sentence entry point, but do not add any claim the participant did not make.
- Where the paper shows participants differing, say so ("B's account pointed the other way") instead of forcing similarity.

Before:
> Participant A mentioned the importance of peer support. Similarly, Participant B also emphasized collective learning. Participant C also talked about teamwork.

After (only if the transcript content supports these relationships):
> Participant A framed peer support as the thing that kept them going. Participant B emphasised something adjacent but distinct: collective learning rather than support as such. Participant C connected the same idea of teamwork to the wider institutional setting.

**Evidence**: `T25 used; D18 before/after; relationships used are supported by the paper: Yes; word count ≥ original.`

Transition-type library (pick the type the data actually supports; never force a relationship the transcripts do not show):
- Contrast: "Unlike Participant A, who focused on efficiency, Participant B emphasised the added learning pressure."
- Echo: "Participant B's account aligns with A's earlier point that AI shifts how tasks are distributed."
- Extension: "Beyond the efficiency gains A mentioned, Participant B also noted the social isolation that came with heavier AI use."
- Escalation: "Building on A's point about task restructuring, Participant B explained how it reshaped team communication."
- Special-case: "While most participants mentioned efficiency, Participant B described the opposite — a loss of autonomy after AI was introduced."

## Technique 26: Theme-Introduction Diversification (qualitative) — Targets D19q

**Principle**: Stop opening every theme with "Theme N: Name. This theme captures...". Give each theme a different entry point, drawn from the paper's own material.

**How to apply (existing content only)**:
- Vary openings: from an actual participant quote; from a contradiction with the literature already cited; from an analytic puzzle the paper already raises; from a counter-case already in the data.
- Keep the theme name and all coded content; change only how the paragraph enters the theme.
- Do not invent complexity ("the picture was complex") that the findings do not actually show.

Theme-entry library (each must use only content already in the paper):
- Quote-first: "\"I felt like I was constantly being monitored,\" Participant 3 said. This account anchors the theme of algorithmic surveillance pressure."
- Contradiction entry: "Despite the official framing of AI as an efficiency tool, several participants described heavier workloads, which forms the theme of work intensification."
- Analytic-source entry: "The theme of professional-identity reconfiguration developed from seventeen separate references to changed job responsibilities after AI was introduced."
- Theory-link entry: "These responses line up with existing ideas about algorithmic management, forming the theme of perceived algorithmic control."

**Evidence**: `T26 used; D19q before/after; each theme entry point and its source in the paper; word count ≥ original.`

## Technique 27: Researcher-Reflection Relocation (qualitative) — Targets D20

**Principle**: Reduce researcher-voice absence by surfacing researcher judgment, coding decisions, and positionality — using the T19-B qualitative safety matrix.

**How to apply (EXTRACTION-ONLY — this is T19-B specialised for qualitative)**:
- Find researcher judgment, reflexivity, or coding-decision material that ALREADY exists somewhere in the paper (methodology, analysis notes, limitations, discussion) and relocate/rephrase it where the analysis currently reads as a flat report.
- Prefer "interpretation-path" sentences that explain how a code or theme was derived from the data the paper reports.
- Obey the T19-B section safety matrix (e.g. reflexive clarification is unsafe in Literature Review).
- One researcher-trace sentence per paragraph maximum; each must connect to its neighbours (Gate J).
- If no such material exists in the paper, DO NOT generate it. Fabricated reflection is AI-flagged and an integrity breach.

Coding decision-chain example (only if these numbers/steps are already recorded in the paper's methodology or coding table):
> Coding proceeded in three phases. Open coding of the transcripts produced 127 initial codes; axial coding then grouped these and removed 32 overlapping concepts; selective coding finally distilled the four themes reported below.
The counts (127, 32, four) and the inter-coder figure (e.g. κ = 0.87) must come from the paper. If the paper does not record them, do not state them.

**Evidence**: `T27 used; D20 before/after; source location of the relocated researcher material (must be filled); T19-B cell and its safety rating; word count ≥ original.`

## Technique 28: Quote-Framing Variation (qualitative) — Targets D21

**Principle**: Reduce the *appearance* of mechanical uniformity in how participant quotations are presented by varying only the narrative framing, ordering, and surrounding interpretation — NEVER by touching the quotations themselves or which participants appear.

**Status**: Participant quotations are research evidence. Their frequency, length, and presence/absence are findings, not style. T28 must not change them.

**How to apply (framing only)**:
- Vary how a quotation is introduced and interpreted: lead one theme with analysis then the quote, another with the quote then analysis, using only what the paper already says.
- Vary the analytical linkage and surrounding explanation between quotations, drawing only on the existing interpretation.
- First flag any genuinely uniform citation pattern for manual evidence review rather than "fixing" it by altering evidence.
- Do NOT remove, add, lengthen, shorten, reorder away, or selectively suppress participant quotations; do NOT make a participant "absent" from a theme; do NOT claim a silence the paper does not document. Any substantive change to the quotation evidence is outside the AI-risk workflow and needs explicit author approval.
- Keep every quotation verbatim and every participant label exact (Gate B).

**Evidence**: `T28 used; D21 before/after; only framing/ordering/interpretation changed (no quote added/removed/lengthened/shortened/suppressed): Yes; word count ≥ original.`

---

## Technique 29: Evidence-Based Authorship Restoration (general; Targets D3/D6/D7/D14)

**Status**: General technique. This is the ONLY sanctioned form of "adding human writing character". It is reframed deliberately: the goal is NOT to make text "look less like AI", but to let the paper more truthfully reflect the research thinking, method choices, result interpretation, and evidence boundaries the author already has. Any external detector change is a post-revision observation, never a guaranteed outcome.

**Why this is allowed when "human-trace injection" was not.**
There are two very different things people mean by "add human traces":
- Manufacturing defects — deliberate grammar/spelling errors, fake non-native mistakes, filler, random sentence-scrambling, casual/emotional asides, fabricated researcher feelings, invented non-verbal detail, invented quotes. These are FORBIDDEN (they lower quality, risk integrity, and a detector still flags generated text). See the forbidden list below.
- Restoring evidence-based authorship — turning a flat "the results show X" report into the kind of grounded judgment, method rationale, and boundary-aware statement a real researcher writes, using ONLY what the thesis already contains. This is what T29 does.

**Core rule**: If a new sentence cannot be explained by the paper's existing data, method, theoretical framework, or actually-performed research process, it is not authorship restoration — it is fabrication, and must not be added.

### Allowed operations (each must trace to existing thesis content)

1. Cautious result interpretation after a finding — consistent with the paper's own theory, not exceeding what the data supports (no correlation→causation upgrade). Example: "The results show that employee–AI collaboration has a significant positive effect on innovative behavior." → "This significant positive relationship suggests that employee–AI collaboration may act not only as technical support but also as a work resource that helps employees turn ideas into innovative actions." (only if the theory section already frames it this way)
2. Real method-choice rationale — why a method/scale was used, when that reason is true and inferable from the design. Example: "A questionnaire survey was used." → "A questionnaire survey was chosen because the variables examined here, such as work engagement and perceived organizational support, concern employees' perceptions and cannot be captured through objective records."
3. Evidence-boundary statements replacing over-smooth, over-certain conclusions. Example: "These findings fully demonstrate that EAC is essential for innovation." → "These findings support a positive association between EAC and innovative behavior within the sample examined; the cross-sectional design does not allow strong causal conclusions."
4. Variable-specific implications instead of generic ones — tie the managerial/practical implication to the actual variable relationship found.
5. Conservative scope qualifiers used to control claim strength (not as a rhythm gimmick): "in the present sample", "within the context examined", "the results suggest", "one possible interpretation is", "this should be read with caution because…".

### Placement
Appropriate: after hypothesis-test results, after mediation/moderation explanation, in discussion where findings meet prior literature, in limitations and implications.
Inappropriate: pure descriptive passages before a data table, demographics paragraphs, chapter-roadmap sentences, anywhere it would be an unsupported theoretical leap or just decoration.

### Three-tier control

ALLOWED (improves quality): evidence-based interpretation; true method rationale; design-based boundaries; variable-specific implications; literature-relationship synthesis without distortion; reducing template sentences without harming coherence.

USE WITH CAUTION (only with a real source in the paper): why specific samples were removed (needs the real criterion); questionnaire translation/back-translation (only if actually done); pilot test / expert review (only if it happened); explanation of an unusual statistic (evidence-bound, no invented data); author judgment about a literature gap (must be supportable from the cited works).

FORBIDDEN (quality or integrity risk): deliberate grammar/spelling errors; faked non-native mistakes; colloquial/emotional/off-topic personal narrative; fabricated research process, data-cleaning steps, sample-selection reasons, or sources; invented researcher feelings, surprise, or non-verbal observation; quote tampering; random replacement / word-order scrambling / meaning-blurring to dodge detection; any claim that a technique guarantees a lower AI score.

### Four mandatory verification checks (run after every T29 edit)
1. Meaning preservation — original meaning unchanged.
2. Evidence traceability — the added judgment traces to data, method, framework, or cited literature already in the paper.
3. Academic quality — language quality, clarity, and formal register did not drop; no new colloquialism or grammar error (Gates H/I/J).
4. Detector-neutral intent — the edit's purpose is clearer academic expression, not detection evasion.

**Hard guard**: T29 never generates a "researcher voice" out of nothing. If material to support the judgment is not present in the paper, do not write the sentence. This is the same extraction discipline as T19, stated positively. T29 also obeys Principle 4 (word count ≥ original) but must NOT be used to pad: any added wording must clarify existing content and pass Gate J's low-information-filler check.

**Execution evidence must show:**
```text
T29 used: Yes / No
Operation type (interpretation / method-rationale / boundary / implication / qualifier):
Existing thesis evidence it traces to — must be filled with a specific source location (file / chapter / section / paragraph or table number). Generic labels such as "data" or "method" are insufficient without that location:
Meaning preserved: Yes / No
Evidence traceable: Yes / No
Academic quality maintained (no new errors/colloquialism): Yes / No
Detector-neutral intent (not evasion): Yes / No
Word count (original / revised, must be ≥):
```

---
## Deep Pattern Rewrite Rules

When revising a paragraph, do not only remove visible AI phrases. Also check for deeper AI-writing patterns.

1. Significance Inflation
   - If the sentence inflates importance, reduce it to a specific claim.
   - Replace broad value statements with finding-specific explanation.

2. Synonym Cycling
   - If the same concept is renamed several times, standardize the term.
   - Do not change core variables just to avoid repetition.

3. Rule of Three
   - If the paragraph forces three balanced points, reduce or reorganize the list.
   - Avoid repeated “X, Y, and Z” rhythm across paragraphs.

4. Vague Attribution
   - If attribution is vague, connect it to an existing citation or remove the attribution phrase.
   - Do not write “previous studies show” without clear citation support.

5. Formulaic Limitation or Future Research Pattern
   - If the limitation sentence is generic, connect it to the actual method, sample, variables, or model.

6. Hanging Analysis
   - If one sentence contains several abstract consequences, split it into separate sentences and make each consequence concrete (do not delete content).

7. Generic Positive Conclusion
   - If the conclusion is broadly positive, make it findings-specific.

8. False Range
   - If the sentence claims a broad range, name the actual scope explicitly (do not simply delete the range, which shortens the text).


---
## Quick Reference: Dimension → Technique Mapping

| Dimension | Target | Primary Technique |
|-----------|--------|-------------------|
| D1 | Repetitive Starters | T1: Starter Variation |
| D2 | Formulaic Transitions | T2: De-formulaizing |
| D3 | Over-Smooth Logical Flow | T13: Reasoning Visibility; T14: Paragraph Architecture Rebuilding; T19: Researcher-Trace Relocation and Local Integration; T22: Detail-Rich Core and Keyword Cohesion; T23: Information-Progression Rewrite; T24: Introduction/Abstract Anti-Template; T29: Evidence-Based Authorship Restoration |
| D4 | Uniform Length and Rhythm | T3: Length Variation |
| D5 | Generic Academic Phrasing | T6: Generalization Surgery; T12: Abstract Word Reduction; T20: Verb-Phrase Expansion |
| D6 | Excessive or Weak Hedging / Balanced Claims | T4: Hedging Control; T5: Balance Disruption; T29: Evidence-Based Authorship Restoration |
| D7 | Vague Conclusions | T6: Generalization Surgery; T29: Evidence-Based Authorship Restoration |
| D8 | Passive and Nominalization Clusters | T7: Passive Voice Control / Active-Passive Mixing |
| D9 | Abstract-to-Concrete Imbalance | T8: Concrete Anchoring; T19: Researcher-Trace Relocation and Local Integration |
| D10 | Mechanical Citation Pattern | T9: Citation Naturalization |
| D11 | Lexical Flatness / Repeated Generic Verbs | T10: Lexical Precision and Repetition Control; T20: Verb-Phrase Expansion; T21: Parenthetical Integration |
| D12 | Paragraph-Level Template Structure | T14: Paragraph Architecture Rebuilding; T19: Researcher-Trace Relocation and Local Integration; T22: Detail-Rich Core and Keyword Cohesion; T23: Information-Progression Rewrite; T24: Introduction/Abstract Anti-Template |
| D13 | Cross-Paragraph Structural Repetition | T15: Section-Level Pattern Diversification |
| D14 | AI-Like Academic Smoothness / Low Human Friction | T13: Reasoning Visibility; T14: Paragraph Architecture Rebuilding; T19: Researcher-Trace Relocation and Local Integration; T21: Parenthetical Integration; T22: Detail-Rich Core and Keyword Cohesion; T29: Evidence-Based Authorship Restoration |
| D15 | Thesis-Section Template Dependency | T14: Paragraph Architecture Rebuilding; T15: Section-Level Sequence Disruption; T19: Researcher-Trace Relocation and Local Integration; T24: Introduction/Abstract Anti-Template |
| D16 | Methodological Template Intensity | T17: Methodological Template Breaking (length-preserving); T19: Researcher-Trace Relocation and Local Integration |
| D17 | Predictable Reporting Sequence | T18: Sequence Reordering (length-preserving); T19: Researcher-Trace Relocation and Local Integration |
| D18 (qualitative) | Transition-Sentence Templating | T25: Transition De-Templating |
| D19q (qualitative) | Theme-Presentation Uniformity | T26: Theme-Introduction Diversification |
| D20 (qualitative) | Researcher-Voice Absence | T27: Researcher-Reflection Relocation — extraction-only via T19-B; if reconstruction from existing evidence is needed, classify as T29 and require a Source Trace block |
| D21 (qualitative) | Participant-Quote Balance Uniformity | T28: Quote-Balance Disruption |
| Calibration | External detector high but internal score low | T16: Shared External-Risk Structural Pass (uses the external detector only as risk-location evidence — no detector-specific rewrite path, no reverse-engineering or bypass) |



---
## Non-Uniform Replacement Rule

Do not replace the same AI-like phrase with the same alternative throughout the whole thesis.

Weak approach:
- replace every “therefore” with “thus”
- replace every “indicate” with “suggest”
- replace every “important” with “significant”
- replace every “this study” with “the present study”

Better approach:
- sometimes replace the transition with a thesis-specific connective of equal or greater length (do not simply delete it)
- sometimes use a direct sentence
- sometimes change the sentence order
- sometimes move concrete reasoning earlier
- sometimes use a thesis-specific explanation
- sometimes keep the original wording if it is academically necessary

The goal is to reduce repeated patterns, not to create a new repeated replacement pattern.

---
## Anti-Synonym-Rewrite Rule

Do not reduce AI risk mainly by synonym replacement.

Weak rewrite:
- replace "indicate" with "suggest"
- replace "important" with "significant"
- replace "therefore" with "thus"

This usually does not solve external-detector-style AI detection when the problem is structural.

Preferred rewrite:
- change paragraph opening
- change sentence order
- reduce repeated conclusion sentence
- make reasoning more visible
- connect claims to the actual variables, hypotheses, tables, or findings
- vary the way different paragraphs develop their argument

A successful rewrite should change the sentence skeleton or paragraph logic where needed, not only replace verbs and adjectives.

---

## Quality Checklist for Thesis Rewrite

Before finalizing the revised text, check:

- [ ] Original meaning preserved?
- [ ] Academic logic unchanged?
- [ ] Variables and abbreviations unchanged?
- [ ] Citations intact and accurate?
- [ ] No new references added?
- [ ] No new theory added?
- [ ] No unsupported claims added?
- [ ] Hypothesis numbers unchanged?
- [ ] Statistical numbers, coefficients, significance levels, and model names unchanged?
- [ ] Section structure mostly unchanged?
- [ ] Repeated sentence openings reduced?
- [ ] Mechanical transitions reduced?
- [ ] Sentences are not too uniformly balanced?
- [ ] Abstract expressions reduced where concrete explanation is possible?
- [ ] Tone remains formal enough for a master’s thesis?
- [ ] Writing is not over-polished into native-speaker journal style?
- [ ] No intentional grammar or spelling mistakes added?
- [ ] No promotional or casual wording introduced?
- [ ] Paragraph architecture has been changed where the original was template-like?
- [ ] Repeated section patterns have been reduced?
- [ ] No section still follows the same paragraph rhythm again and again?
- [ ] If an external detector score was high, a second external-detector-high rewrite pass was completed?
- [ ] Does the revised paragraph still sound robotic, overly polished, or mechanically balanced when read aloud?
- [ ] Does the paragraph sound like a formal thesis paragraph rather than an automatic paraphrasing-tool output?
- [ ] Did the rewrite avoid making the paragraph smoother but more generic?
- [ ] Did the rewrite avoid adding unnecessary bridge sentences?
- [ ] Did the rewrite preserve acceptable student-like roughness where clarity was not harmed?
- [ ] Did the rewritten section avoid becoming more template-like than the baseline?
- [ ] Aggregation-worsening risk checked?
- [ ] Revised fragment count and maximum fragment length compared with the original?
- [ ] If any revised fragment exceeds 3000 characters, was it split or given a valid breakpoint?
- [ ] Breakpoint does not introduce new data, theory, citation, or unsupported example?

---

## Failed Rewrite Direction Signals

A rewrite direction may be wrong if the revised version:

- reads smoother but more generic;
- has more complete academic synthesis than the original;
- uses cleaner but repeated paragraph architecture;
- replaces rough student wording with AI-like polished logic;
- adds bridge sentences such as “This helps explain,” “This suggests,” “In this way,” or “For this reason” too often;
- makes introduction, significance, literature review, or hypothesis sections more formulaic;
- increases external AI detector score compared with the baseline.

If these signals appear, stop rewriting in this direction and return to the baseline version.

---
## Mandatory Failure Conditions

A rewritten paragraph fails quality review if:

- it changes any citation, variable name, hypothesis label, coefficient, p-value, model name, table number, or capitalization of a protected term;
- it only inserts short sentences without addressing the detected dimensions;
- it changes association into causation;
- it adds an example, case, theory, or interpretation not present in the original text;
- it removes a citation;
- it changes the hypothesis meaning;
- it rewrites a statistical result in a way that changes its interpretation;
- it skips the Pass 3 anti-AI audit.
- it creates a revised fragment over 3000 characters without splitting it or inserting a valid breakpoint;
- it inserts a breakpoint that introduces unsupported data, theory, citation, example, or interpretation.

If any failure condition appears, the paragraph must be revised again before final output.

---
## No Generic Evidence Rule

Do not use generic evidence statements to satisfy the execution report.

Invalid:
- AI-like patterns reduced.
- The paragraph was improved.
- Protected elements preserved.
- The meaning was checked.
- Quality gate passed.

Valid:
- Repeated starter “This study...” was replaced by a section-specific subject.
- Formulaic transition “Therefore” was removed because D2 was high.
- D12 risk was handled by moving concrete variable logic before the hypothesis sentence.
- Citation “Kong et al. (2023)” was preserved exactly.
- Variable name “Employee–AI Collaboration (EAC)” was preserved exactly.
- No coefficient, p-value, model name, or table number appeared in this paragraph.

Mandatory rule:
If the evidence cannot identify what was changed, it is not valid evidence.

---

## Recommended Output Format

**Canonical Output Rule**: SKILL.md is the only authority for workflow-level output structure (Phase order, target lock, ledger, Phase 7 Gate A–J, Phase 8 Summary Stats, Phase 9 Final Output, the Stage 5 mandatory re-test stop, skipped-paragraph records, and the DOCX Output Gate). Every output-format section in this file is a SUPPLEMENTARY paragraph-level template only and must not replace the canonical Phase 8/9 structure in SKILL.md. If any reference template conflicts with SKILL.md, SKILL.md overrides it.

When applying this guide under the full skill workflow, use this output format:

```text
[Paragraph ID]

Original Risk Diagnosis:
- Paragraph AI Score:
- Dimension Coverage: Complete D1-D17 / Partial / Invalid
- Hit Dimensions:
- Strong AI Dimensions:
- Pattern Floor Applied:
- Primary AI Problems:

Dimension-to-Technique Execution Plan:
- D1 → T1:
- D2 → T2:
- D12 → T14:
- D13 → T15:
- D16 → T17:
- D17 → T18:
- T19 used: Yes / No. T29 used: Yes / No. (Do not merge them into one checkbox.) If either is Yes, include the Source Trace block and identify the operation type — see the T19/T29 source-annotation rule
- Reason for T19 relocation: / Reason for T29 reconstruction: (write N/A for whichever is not used)
- Aggregation-worsening risk before Phase 7: Low / Possible / High
- Breakpoint likely needed: Yes / No
- Other:

Protected Elements Locked:

| Element Type | Original Exact String | Revised Exact String | Status |
|-------------|----------------------|----------------------|--------|
| Citation | | | Same / Restored / Changed |
| Variable name | | | Same / Restored / Changed |
| Hypothesis label | | | Same / Restored / Changed |
| Statistical value | | | Same / Restored / Changed |
| Table/model number | | | Same / Restored / Changed |
| Capitalization-sensitive term | | | Same / Restored / Changed |

If no protected element exists in the paragraph, write:
“No protected elements found in this paragraph.”

Do not leave the protected-elements table blank without explanation.

Three-Pass Rewrite Evidence:

Pass 1 — Remove AI-like patterns:
- Repeated starters reduced:
- Formulaic transitions reduced:
- Generic academic phrases reduced:
- Unnecessary hedging reduced:

Pass 2 — Rebuild rhythm and structure:
- Sentence rhythm changed:
- Paragraph opening changed:
- Paragraph ending changed:
- Paragraph architecture changed:
- Reasoning visibility improved:

Pass 3 — Anti-AI Audit:
- Remaining repeated structure:
- Remaining generic conclusion:
- Remaining over-smooth logic:
- Decision: Pass / Needs Rework

Quality Gate Result (all ten gates whenever text is rewritten):
- Gate A AI-pattern reduction: Pass / Rework Needed / Failed
- Gate B Academic integrity and protected elements: Pass / Rework Needed / Failed
- Gate C Meaning preservation: Pass / Rework Needed / Failed
- Gate D Dash and punctuation integrity: Pass / Rework Needed / Failed
- Gate E Aggregation-worsening / breakpoint check: Pass / Rework Needed / Failed / N/A (use `N/A — no long-fragment or boundary-change risk` when the rewrite does not handle externally highlighted long fragments, does not change fragment boundaries, and creates no revised fragment over 3000 characters)
- Gate F Word-count preservation: Pass / Rework Needed / Failed
- Gate G Structure and readability: Pass / Rework Needed / Failed
- Gate H Sentence completeness and length: Pass / Rework Needed / Failed
- Gate I Grammar, spelling, capitalization: Pass / Rework Needed / Failed
- Gate J Logic flow and no out-of-place meta-commentary: Pass / Rework Needed / Failed
- Protected elements changed: Yes / No
- Breakpoint inserted: Yes / No / Not needed
- Action taken:

[Revised Version]

Major changes made:
1.
2.
3.
```

A paragraph must not be marked complete unless the execution plan, three-pass evidence, protected elements check, and quality gate result are included.

---

## Original Method File Notes

The original method file contained aggressive rewriting strategies for lowering AI-detection patterns. Some examples are more suitable for essays, reports, marketing-style writing, or highly stylized rewriting than for a master’s thesis. They are intentionally retained ONLY as diagnostic references for recognising AI-like patterns. They are NON-EXECUTABLE as written: an aggressive legacy example may be used only after being rewritten into a thesis-safe, minimal-edit, word-count-preserving form that passes Gates A–J. No legacy instruction may override the opening restrictions of this file (no regeneration, no compression, no back-translation, no fabrication).

When using this file for thesis revision, the safest approach is:

1. Preserve meaning, citations, variables, and data first.
2. Apply thesis-safe versions of each technique.
3. Use aggressive original techniques only when they do not damage academic tone.
4. Never invent examples, evidence, references, or statistical interpretation.




---