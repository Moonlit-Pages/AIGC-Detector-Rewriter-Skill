# MANIFEST — aigc-detector-rewriter

Version: 2.21.0
Type: Claude / OpenCode SKILL package
Purpose: Detect AI-writing-risk patterns in English and Chinese thesis text and revise selected high-risk passages by minimal, evidence-traced edits, preserving meaning, citations, data, structure, and word count, under a single-chapter closed-loop external re-test workflow.

## Package contents

| File | Role |
|---|---|
| `SKILL.md` | Canonical authority. Operating architecture, Principles 0–9, Phases 1–9, Stage/round workflow, language routing, task modes, Gates A–J, status state machine, conflict-resolution hierarchy, output structure, DOCX Output Gate. |
| `references/detection_principles.md` | Dimension catalog D1–D21, quantitative signal reference, scope-aware risk index, structural floors (D13/D15), false-positive guards. |
| `references/rewrite_methods.md` | Technique catalog T1–T29, strategy matrix, paragraph-level evidence templates (supplementary to SKILL.md), escalation rungs. |
| `references/qualitative_authorship_restoration.md` | Qualitative/mixed-methods restoration (D18–D21), T25–T28, evidence-grounded interpretation rules. |
| `references/chinese_text_ai_risk.md` | Chinese-route AI-risk phrase reference, fixed Chinese-route evidence fields, same-paragraph compensation rules. |
| `MANIFEST.md` | This file. |
| `CHANGELOG.md` | Version history. |
| `TEST_CASES.md` | Behavioral acceptance cases. |
| `KNOWN_LIMITATIONS.md` | Honest limitations and out-of-scope items. |

## Authority order
SKILL.md overrides all reference files for workflow-level output and rules. Reference files provide catalogs, paragraph-level templates, and examples only. See "Conflict Resolution Hierarchy" and "Canonical Output Authority" in SKILL.md.

## Three iron rules (override everything except academic integrity / protected content)
1. No whole-paragraph regeneration or back-translation.
2. No fabrication (quotes, data, emotions, citations, researcher voice).
3. No word-count reduction.
