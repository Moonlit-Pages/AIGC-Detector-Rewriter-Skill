# AIGC Detector & Rewriter Skill

**A conservative AI-writing risk detection and thesis rewriting skill for English and Chinese academic writing.**

This skill helps identify and reduce AI-generated writing-risk patterns in master’s thesis text while preserving academic meaning, citations, variables, hypotheses, statistical results, and document structure.

It is designed for users who need careful, detector-informed academic revision, especially for thesis chapters affected by **Turnitin AI**, **CNKI AIGC**, or other external AI detection reports.

> This is not a detector-bypass tool.
> It does not guarantee any AI detector score.
> It focuses on minimal, evidence-preserving revision and academic integrity.

![AIGC Detector & Rewriter overview showing closed-loop thesis AI-risk diagnosis, paragraph scoring, minimal-edit rewriting, quality gates, and external re-test workflow.展示论文 AI 风险诊断、段落评分、最小化改写、质量门检查和外部复测闭环流程](images/aigc-detector-rewriter-overview.png)

## Keywords

AI writing detection, AIGC detector, thesis AI rewrite, academic AI detection, Turnitin AI, CNKI AIGC, AI-generated writing risk, reduce AI score, master thesis rewriting, English thesis editing, Chinese thesis AI risk, detector-informed rewriting, academic integrity, minimal-edit rewriting, AI-polished text, AI-refined text, thesis revision skill.

中文关键词：降AI率，降低AIGC检测率，知网AIGC，Turnitin AI检测，论文AI痕迹，硕士论文改写，英文论文降AI，中文论文AI风险，AI润色痕迹，学术论文改写。

---

## What This Skill Does

The **AIGC Detector & Rewriter Skill** analyzes thesis text for AI-like writing patterns and revises selected high-risk passages through controlled, minimal edits.

It targets risks such as:

* Repeated sentence openings
* Over-smooth academic logic
* Mechanical paragraph structure
* Formulaic literature review patterns
* Repetitive hypothesis-development structure
* Uniform empirical-result reporting
* Generic conclusion and implication language
* AI-polished or AI-refined academic style
* Chinese template phrases and CNKI-sensitive writing patterns
* Qualitative research passages with decorative quotations or weak authorial interpretation

The skill supports:

* English thesis text
* Chinese thesis text
* Mixed English-Chinese thesis documents
* Quantitative research
* Qualitative research
* Mixed-methods research
* External AI detector report analysis
* Chapter-by-chapter revision workflow
* DOCX / Markdown / text-based workflows

![Before-and-after infographic showing AI feature value reduced from 60% to 18% after AIGC Detector & Rewriter processing, with meaning, citations, data, and academic structure preserved,降 AI 重写前后对比图，展示论文 AI 特征值经过 AIGC Detector & Rewriter 处理后从 60% 降至 18%，同时保留原意、引用、数据和论文结构 ](images/aigc-rewrite-result.png)

## Core Principle

This skill follows one central rule:

> **Reduce AI-writing risk by minimally editing the original thesis text, not by regenerating it.**

The skill does **not** rewrite a chapter from scratch. It does **not** replace the author’s work with fluent AI-generated prose. Instead, it works sentence by sentence and paragraph by paragraph to reduce detectable writing patterns while keeping the original academic content intact.

Allowed operations include:

* Substituting individual words
* Reordering clauses where safe
* Splitting overly balanced sentences
* Recasting repeated sentence openings
* Reducing formulaic transitions
* Making existing reasoning more visible
* Reorganizing paragraph architecture without changing meaning
* Relocating existing author reasoning when traceable
* Preserving or increasing word count when required

Forbidden operations include:

* Whole-paragraph regeneration
* Whole-chapter rewriting
* Back-translation
* Detector-bypass rewriting
* Third-party humanizer rewriting
* Fabricating data, citations, examples, quotes, or researcher voice
* Changing variables, hypotheses, coefficients, p-values, or conclusions
* Claiming that an external detector score has improved without a comparable external re-test

---

## Why This Skill Exists

Many AI rewriting tools make academic text more fluent, smoother, and more polished. That can make the text look **more AI-generated**, not less.

This skill is built around the opposite strategy:

* Keep as much original author wording as possible
* Avoid over-polishing
* Preserve non-native but acceptable academic style
* Break repeated structures without deleting content
* Treat detector scores as external evidence, not as something the model can predict
* Work chapter by chapter with external re-testing

The goal is not to create perfect native-speaker prose.
The goal is to preserve the author’s thesis while reducing structural AI-writing risk.

![Core capabilities of the AIGC Detector & Rewriter skill, including AI-risk detection, minimal-edit rewriting, citation and data protection, version ledger governance, and built-in academic integrity safeguards.核心能力图，展示 AI 风险检测、最小化改写、引用和数据保护、版本台账管理以及学术完整性保障](images/core-capabilities.png)

## Main Features

### 1. Multi-Layer AI-Writing Risk Analysis

The skill checks AI-risk signals at different levels:

| Level           | Risk Examples                                                          |
| --------------- | ---------------------------------------------------------------------- |
| Sentence level  | repeated openings, uniform rhythm, excessive transitions               |
| Paragraph level | mechanical claim-explanation-conclusion structure                      |
| Section level   | repeated literature review, hypothesis, or results-reporting templates |
| Chapter level   | long continuous detector-highlighted fragments                         |
| Document level  | repeated architecture across multiple chapters                         |

---

### 2. English and Chinese Route Separation

English and Chinese thesis text are handled differently.

| Text Type           | Method                                                    |
| ------------------- | --------------------------------------------------------- |
| English thesis text | Uses the D1–D17 academic AI-risk dimension framework      |
| Chinese thesis text | Uses Chinese AI-risk phrase and structure checks          |
| Mixed-language text | Routes each segment according to language                 |
| Qualitative text    | Adds qualitative-specific risk checks                     |
| Quantitative text   | Adds methodology and empirical-reporting structure checks |

This prevents Chinese thesis text from being incorrectly judged by English-only AI-writing indicators.

---

### 3. Detector-Informed but Not Detector-Dependent

The skill can use external detector reports as calibration signals, including:

* Turnitin AI reports
* CNKI AIGC reports
* GPTZero-style reports
* Originality-style reports
* Highlighted AI-risk fragments
* Chapter-level AI scores
* Whole-document AI scores

However, the skill does not claim to simulate or predict any detector.

Internal risk scores are only used for diagnosis and prioritization.
Only a real external re-test can confirm whether the detector score changed.

---

### 4. Minimal-Edit Thesis Rewriting

The rewriting process protects:

* Original academic meaning
* Research logic
* Variables and abbreviations
* Hypotheses
* Citations
* Reference names
* Statistical values
* Coefficients
* p-values
* Table and figure numbers
* Methodological claims
* Qualitative quotes
* Participant meaning
* Chapter and paragraph structure

Every rewritten paragraph must pass quality gates before being accepted.

---

### 5. Chapter-by-Chapter Closed Loop

The recommended workflow is:

1. Build a chapter version ledger
2. Record current external detector scores
3. Select the highest-risk chapter
4. Diagnose paragraph and section risks
5. Rewrite only the selected high-risk areas
6. Run quality gates
7. Ask the user to re-test the chapter externally
8. Accept the new version only if the external re-test improves
9. Continue to the next target chapter only after confirmation

A chapter is considered done only when its measured external AI score is below the target threshold.

Default target: **below 30%**, unless the user specifies another threshold.

---

## Typical Use Cases

This skill is useful for:

* Master’s thesis AI-writing risk reduction
* English thesis revision for non-native authors
* Chinese thesis CNKI AIGC risk review
* Turnitin AI report response
* Chapter-level AI detector remediation
* Literature review de-templating
* Hypothesis-development rewriting
* Methodology section revision
* Empirical results reporting improvement
* Discussion and conclusion rewriting
* Qualitative interview findings improvement
* Mixed-methods thesis editing
* Detector-informed academic editing workflows

---

## What This Skill Is Not

This skill is **not**:

* An AI detector
* A detector bypass tool
* A plagiarism reduction tool
* A similarity-score reduction tool
* A third-party humanizer
* A full thesis generator
* A citation generator
* A tool for inventing research evidence
* A tool for making fake “human-like” errors
* A guarantee of Turnitin, CNKI, or any detector result

It does not encourage academic misconduct.
It is designed for conservative academic revision of user-provided thesis text.

---

## Input Requirements

For best results, provide one of the following:

### Option 1: Single Paragraph

Use this for quick diagnosis or light rewriting.

Recommended input:

```text
Please review this paragraph for AI-writing risk and revise it minimally.
[Paste paragraph here]
```

### Option 2: Chapter Text

Use this for chapter-level diagnosis and rewriting.

Recommended input:

```text
Chapter: Chapter 4 Results
External detector score: 42%
Target score: below 30%
Detector: Turnitin AI
Please diagnose and revise only the high-risk paragraphs.
```

### Option 3: External Detector Report

Use this when you have highlighted AI-risk sections.

Recommended input:

```text
I have uploaded the Turnitin/CNKI AI report.
Please identify the highest-risk sections and create a chapter-by-chapter revision plan.
Do not rewrite the whole thesis at once.
```

### Option 4: Chinese Thesis Text

Recommended input:

```text
请按照中文论文AI痕迹风险规则检查这一段，不要套用英文D1–D17评分。
请最小改写，不要删减字数，不要改变原意。
[粘贴中文段落]
```

---

## Output Structure

Depending on task size, the skill may produce:

### Quick Single-Paragraph Mode

* Scope label
* Hit risk dimensions
* Selected techniques
* Protected elements check
* Quality gate result
* Revised paragraph
* Major changes made

### Full Staged Mode

* Task routing result
* External detector evidence map
* Protected elements list
* Paragraph risk table
* Dimension-to-technique execution plan
* Three-pass rewrite evidence
* Revised version
* Phase 7 quality gate result
* Word-count preservation check
* External re-test instruction
* Next-round status

### Skill Audit Mode

When auditing the Skill document itself, the output focuses on:

* Contradictions
* Missing rules
* Execution risks
* Ambiguous instructions
* Workflow conflicts
* Quality gate weaknesses
* Priority fix list

---

## Safety and Academic Integrity Rules

The skill follows these rules strictly:

1. Do not fabricate sources, data, findings, quotes, or researcher reflections.
2. Do not change protected academic elements.
3. Do not rewrite whole chapters as newly generated prose.
4. Do not use back-translation.
5. Do not route thesis text through third-party humanizer tools.
6. Do not claim external detector improvement without comparable external re-test evidence.
7. Do not over-polish the author’s style.
8. Do not intentionally add grammar or spelling mistakes.
9. Do not delete content to reduce AI-risk patterns.
10. Do not merge paragraphs or damage document structure.

---

## Example Prompts

### English Thesis Paragraph

```text
Please revise the following thesis paragraph to reduce AI-generated writing patterns.
Keep the meaning, citations, variables, and academic logic unchanged.
Do not over-polish the language.
Do not shorten the paragraph.
```

### Turnitin AI Chapter Revision

```text
Turnitin AI marked Chapter 5 as 48%.
Please create a chapter-level risk diagnosis first.
Then revise only the highest-risk paragraphs using minimal edits.
Do not claim the score is reduced until I re-test it.
```

### CNKI AIGC Chinese Thesis Revision

```text
请按照中文论文AIGC风险检查规则，检查下面内容是否存在模板化表达、空泛总结、机械连接和中文AI痕迹。
请只做最小改写，不要改变研究结论，不要删减字数。
```

### Skill Document QA

```text
Please review this Skill document for contradictions, missing rules, ambiguous instructions, workflow risks, and quality-gate weaknesses.
Do not rewrite the whole document.
Only identify issues and propose precise fixes.
```

---
![Workflow diagram showing how the AIGC Detector & Rewriter skill processes a thesis from upload and parsing to paragraph risk scoring, high-risk chapter selection, minimal-edit rewriting, quality gate, and external re-test.展示从上传论文、解析章节、段落风险评分、选择高风险章节、最小化改写到质量检查和外部复测的完整流程](images/how-the-skill-works.png)

## Recommended Workflow

```text
1. Upload thesis chapter or detector report
2. Identify language route: English / Chinese / mixed
3. Identify research type: quantitative / qualitative / mixed-methods
4. Record external detector score if available
5. Build chapter version ledger
6. Diagnose paragraph-level and section-level AI-risk patterns
7. Select only the highest-risk paragraphs
8. Rewrite minimally
9. Run quality gates
10. Re-test externally
11. Accept or discard candidate version based on comparable re-test result
```

---

## Quality Gates

Each revised paragraph or chapter should pass these checks:

| Gate   | Check                                       |
| ------ | ------------------------------------------- |
| Gate A | AI-pattern reduction                        |
| Gate B | Academic integrity and protected elements   |
| Gate C | Meaning preservation                        |
| Gate D | Dash and punctuation integrity              |
| Gate E | Aggregation-worsening and breakpoint risk   |
| Gate F | Word-count preservation                     |
| Gate G | Structure and readability                   |
| Gate H | Sentence completeness and sentence length   |
| Gate I | Grammar, spelling, and capitalization       |
| Gate J | Logic flow and no misplaced meta-commentary |

If any gate fails, the revision is incomplete.

---

## Project Files

Suggested repository structure:

```text
aigc-detector-rewriter/
├── README.md
├── SKILL.md
└── references/
    ├── detection_principles.md
    ├── rewrite_methods.md
    ├── qualitative_authorship_restoration.md
    └── chinese_text_ai_risk.md
```

---

## Installation / Usage

This repository is intended to be used as a custom AI writing skill or prompt-based academic revision module.

Basic usage:

1. Copy `SKILL.md` into your skill environment.
2. Keep all reference files in the `references/` folder.
3. Provide thesis text, chapter text, or detector reports as input.
4. Run the task according to the routing rules.
5. Re-test rewritten chapters externally before accepting a new baseline.

---

## Important Notes About Detector Scores

AI detector results can vary across tools, dates, settings, and document formats.

This skill treats detector results as external evidence, not as a guaranteed truth.

The skill may help reduce writing patterns that detectors often flag, but it cannot promise that:

* Turnitin AI will report a specific score
* CNKI AIGC will fall below a specific threshold
* Any detector will classify the text as human-written
* A rewritten version will always score lower

A rewritten chapter is only a candidate version until a comparable external re-test confirms improvement.

---

## Ethical Use

Use this skill only for legitimate academic revision.

Appropriate uses:

* Improving clarity while preserving meaning
* Reducing formulaic writing
* Removing excessive AI-polished patterns
* Protecting thesis originality
* Making the author’s actual reasoning more visible
* Reviewing detector-highlighted areas conservatively

Inappropriate uses:

* Submitting fabricated research
* Hiding ghostwritten work
* Manufacturing fake human style
* Bypassing academic integrity systems
* Replacing the author’s thesis with AI-generated prose

---

## FAQ

### Does this skill guarantee a lower Turnitin AI score?

No. It can reduce AI-writing risk patterns, but only an external re-test can confirm the actual detector result.

### Can it rewrite a full thesis at once?

No. The recommended workflow is chapter by chapter. Full-thesis batch rewriting increases the risk of over-editing, structure damage, and detector regression.

### Does it work for Chinese thesis text?

Yes. Chinese thesis text uses a separate Chinese AI-risk route rather than the English D1–D17 framework.

### Can it handle qualitative research?

Yes. It includes qualitative-specific checks for interviews, themes, quotations, participant meaning, researcher voice, and evidence-based interpretation.

### Can it use detector reports?

Yes. External detector reports can be used for calibration and prioritization, but the skill does not claim to reproduce detector logic.

### Is this a humanizer?

No. This skill explicitly rejects third-party humanizer logic. It focuses on academic integrity, minimal edits, and source-traceable revision.

### Does it intentionally add grammar mistakes?

No. It may preserve acceptable non-native academic style, but it never creates deliberate grammar or spelling errors.

---

## License

Choose a license that fits your intended use.

Recommended options:

* MIT License for open use
* Apache-2.0 for open use with patent language
* CC BY-NC 4.0 if you want non-commercial reuse only

---

## Disclaimer

This project is for academic writing support and document quality improvement. It does not provide legal, institutional, or academic-integrity advice. Users are responsible for following their university’s rules, disclosure requirements, and research ethics standards.

External AI detector results are not guaranteed. Always verify revisions with the relevant institution-approved process.

---
## Star History

<a href="https://www.star-history.com/?repos=Moonlit-Pages%2FAIGC-Detector-Rewriter-Skill&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=Moonlit-Pages/AIGC-Detector-Rewriter-Skill&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=Moonlit-Pages/AIGC-Detector-Rewriter-Skill&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=Moonlit-Pages/AIGC-Detector-Rewriter-Skill&type=date&legend=top-left" />
 </picture>
</a>


---
## Suggested GitHub Description

A conservative AI-writing risk detection and thesis rewriting skill for English and Chinese academic writing, supporting Turnitin AI, CNKI AIGC, detector-informed revision, minimal-edit rewriting, and academic integrity protection.

---

## Suggested GitHub Topics

```text
aigc
ai-detection
turnitin-ai
cnki-aigc
academic-writing
thesis-writing
thesis-revision
ai-writing-risk
english-thesis
chinese-thesis
academic-integrity
prompt-engineering
custom-skill
writing-skill
detector-informed-rewriting
```
