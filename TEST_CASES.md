# TEST_CASES — aigc-detector-rewriter

Behavioral acceptance cases. Each states an input condition and the required behavior. Use these to verify an agent executes the skill correctly.

## Closed-loop and status
- TC1 Regression handling: a re-tested chapter scores higher than its red line → status **Rejected**, candidate discarded, lowest-ever version kept; never reported as Progress.
- TC2 Above-target not done: a chapter at the lowest-ever score but still ≥ target → **Progress**, not Done. Done requires a comparable external re-test below the active target.
- TC3 No external score: external scores unavailable → may run Quick/Single-Batch candidate rewrite labelled "candidate version prepared for external re-test"; must not create a red-line ledger, claim improvement, or mark Done.
- TC4 Fatigue stop: three complete rewrite+re-test rounds on one chapter → **Paused** at the hard checkpoint; only ONE further round, and only with explicit user authorization.
- TC5 Stalemate vs Fatigue: <5pp change → Stalemate Warning (plan next rung, no auto-pause); <3pp change → Rewrite Fatigue Pause (overrides Stalemate).

## Iron rules
- TC6 Word count: every rewritten paragraph has word count ≥ original; if over the readability cap, no forced growth, split at safe boundaries, Gate F on combined descendant word count.
- TC7 No regeneration: no whole-paragraph regeneration or back-translation; every sentence traceable to the original.
- TC8 No fabrication: no invented quotes, data, citations, researcher feelings/positionality; T19 relocation-only, T29 only with a completed Source Trace block; otherwise "Author confirmation needed".

## Routing
- TC9 Chinese route: Chinese paragraphs use the fixed Chinese-route evidence fields, not an English D1–D17 table.
- TC10 Quick Mode anti-misrouting: a request containing "chapter/thesis/DOCX/CNKI/Turnitin/整章/全文/论文/检测报告" or a long upload is NOT routed to Quick Mode even if it says "quickly/简单看一下".
- TC11 Skill-Audit isolation: when the input is SKILL.md or a reference module, do not score it as thesis text or apply D1–D17 rewriting; audit for consistency/routing/safety instead.

## Scope honesty
- TC12 Scope-aware index: only a fully diagnosed full-document scope reports overall_risk_index; chapter/batch/fragment scopes report the corresponding target-unit estimate.
- TC13 External floor scope: a ≥40% external floor applies only to comparable body-text scope; not applied directly when detector scope includes references/appendices/tables/questionnaire items.
- TC14 No external claim: with no comparable re-test, never write "AI score reduced / will pass detection"; use "internal risk estimate reduced / candidate prepared for external re-test".

## Output
- TC15 DOCX gate: a rewritten DOCX is final only after the DOCX Output Gate passes; otherwise deliver a text-only candidate labelled format-preservation-not-verified, or a plain-text reconstruction if the user cannot download files.
