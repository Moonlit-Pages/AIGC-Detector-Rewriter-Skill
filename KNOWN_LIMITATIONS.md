# KNOWN_LIMITATIONS — aigc-detector-rewriter

Stated honestly so users and agents do not over-rely on the skill.

1. No detector guarantee. Internal risk estimates are heuristics; they do not predict or guarantee Turnitin, CNKI, GPTZero, Originality.ai, or any external result. Only a comparable external re-test is authoritative.
2. External re-test required for completion. Without comparable external scores, the skill can only produce candidate versions and internal diagnosis; it cannot mark a chapter Done.
3. Strict targets may be unreachable. Targets below ~15% may be unrealistic for some genres and standardized methodology language; integrity, protected content, readability, and meaning preservation override the numeric target.
4. Quantitative thresholds are calibration anchors, not classifiers. The signal table (CV, transition density, TTR, etc.) guides consistent scoring; it is not a trained detector and carries academic-register caveats.
5. Chinese-route scoring is structural and heuristic. It uses fixed evidence fields and shared-structure checks rather than the English D1–D17 model; cross-language comparability is limited.
6. DOCX format preservation is environment-dependent. Complex formatting, tracked changes, comments, equations, and reference-list layout may not be verifiable; the skill then delivers a labelled candidate or plain-text reconstruction.
7. No third-party humanizers or bypass services. The skill never routes text through external "undetectable AI"/paraphrasing APIs; this is a confidentiality and integrity boundary, not a feature gap to be worked around.
8. Authorized text only. The skill is for text the user owns, authored, co-authored, or is explicitly authorized to edit; it must not be used to misrepresent authorship or bypass institutional disclosure/assessment rules.
9. Single-chapter closed loop. By design it processes one chapter per round (two only on explicit request); whole-document handling requires multiple rounds and a comparable whole-document test.
