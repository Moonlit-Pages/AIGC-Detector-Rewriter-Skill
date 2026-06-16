# CHANGELOG — aigc-detector-rewriter

Semantic-versioning intent: MAJOR = new dimensions/techniques/phases or structural workflow change; MINOR = new capability dimension or release-grade additions; PATCH = consistency fixes, clarifications, naming, terminology.

## 2.21.0 — Release-readiness pass
- Clarified `Partial Execution` as a run-level label, not a 7th target-unit status.
- Resolved Stalemate (<5pp) vs Rewrite Fatigue (<3pp / 3 rounds) threshold conflict with explicit priority (Fatigue Pause overrides Stalemate Warning).
- Rewrite Fatigue made an explicit hard-stop checkpoint; user may authorize ONE controlled extra round, never silent continuation.
- Added Stage/Phase Terminology Rule (Phase controls execution order; Stage is user-facing grouping).
- Added Canonical Output Authority (SKILL.md is sole authority; reference templates are supplementary).
- Added Quick Mode Anti-Misrouting Rule (chapter/thesis/DOCX/detector keywords block Quick Mode).
- Added Strict Target Warning and T19/T29 Master Boundary Rule to the main file.
- Added Chinese Deletion Reinterpretation Rule (every 删除/删去 = remove-low-information-and-compensate, never reduce word count).
- Added release metadata: MANIFEST, CHANGELOG, TEST_CASES, KNOWN_LIMITATIONS.

## 2.20.x — Execution-consistency and scope-honesty hardening
- Authorized-Use Boundary; execution-order lock (Phase → Stage, no jump to Done).
- Rejected status for regression (regression is never Progress).
- Active-target threshold replaces hardcoded 30%; scope-aware risk index (overall only for full-document scope; else chapter/batch/fragment).
- Chinese-route fixed evidence fields; D13/D15 minimum structure-evidence record.
- External ≥40% floor restricted to comparable body-text scope, excluding references/appendices/tables.
- DOCX plain-text fallback; Skill-Audit Mode hard-isolated from Thesis Rewrite Mode.
- `scope_pattern_floor` rename; minimal-edit wording for strategy-matrix rows; T19/T29 not default tools.

## 2.18.0–2.19.1 — Routing, naming, and conflict-resolution
- English/Chinese language routing made authoritative across evidence rules.
- Conflict Resolution Hierarchy; scope-aware Phase 8; T19/T29 separated in templates; expanded Source Trace block.
- Verbal-score-is-calibration-only; No-External-Result-Claim wording rule; over-cap parent→descendant split with combined-word-count Gate F.
- Minimum Execution Map, Pre-Phase-2 checklist, Mode routing summary, Failure-handling table.

## 2.15.0–2.17.2 — Detection calibration and consistency
- Quantitative signal reference (sentence-length CV, transition density, passive share, TTR, n-gram repetition) with academic-register caveats.
- Cluster-density false-positive guard; legitimate-citation carve-out; anti-third-party-API stance.
- Phase 3 target-selection; word-count over-cap exception; Gate E always-visible; DOCX output hygiene (placeholders, leaked markup, Chinese mojibake).

## 2.12.0–2.14.2 — Core architecture
- Author Style Baseline; T19/T29 hard separation; Gate G over-polish checks; Chinese-text AI-risk module; risk_index family; execution-specification sections (Target Status State Machine, DOCX Output Gate).
