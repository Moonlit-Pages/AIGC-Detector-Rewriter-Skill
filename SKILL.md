---
name: aigc-detector-rewriter
title: AIGC Detector & Rewriter
description: >
  Detect AI-generated writing-risk patterns in English and Chinese thesis text, score
  paragraphs by external-detector-informed risk, and revise selected high-risk
  passages while preserving meaning, citations, variables, hypotheses, data,
  statistical conclusions, and document structure. Uses iterative,
  externally re-tested, chapter-by-chapter, minimal-edit revision rounds that
  never regenerate whole paragraphs, never accept a rewritten candidate as a new baseline when a comparable external re-test shows regression (before re-test it is only a candidate), never
  shrink the paper, never merge paragraphs or displace section headings, and keep
  every sentence grammatically complete, correctly punctuated, a sensible length,
  and free of jarring meta-commentary. The objective is to bring each target
  chapter and, where measurable, the whole document below the user-defined target
  (default 30 percent); it does not guarantee a detector outcome and must stop or
  redesign the strategy when fatigue, academic-integrity risk, non-comparable
  detector evidence, or readability damage prevents reliable further improvement.
  Scope is limited to revising user-provided thesis text and flagging
  writing-pattern risk; it must not generate ungrounded thesis sections,
  fabricate research evidence, or claim a detector-score improvement without
  comparable external re-test evidence.
version: 2.21.0
author: custom
category: academic-writing
tags:
  - aigc-detection
  - ai-rewriting
  - academic-writing
  - thesis-editing
  - english-paper
  - external-ai-detector
  - multi-detector
  - paragraph-analysis
  - non-native-academic-english
  - external-detector-report
  - structural-risk-reduction
  - rhythm-repair
  - methodology-template-reduction
  - reporting-sequence-reduction
language:
  - en
  - zh
input_formats:
  - docx
  - md
  - txt
output_formats:
  - md
  - docx
  - report
triggers:
  - 降AI
  - 降低AI率
  - 降低AIGC检测率
  - AI detection
  - reduce AI score
  - lower AI rate
  - 改写降AI
  - 去AI痕迹
  - AI痕迹检测
  - 知网AIGC
  - CNKI AIGC
  - 双检测器
  - Turnitin and CNKI
  - thesis AI rewrite
  - academic AI detector
  - 外部检测报告
  - external AI detector
  - AI detector report
  - AI feature value
  - AI-risk reduction
  - multi-detector AI reduction
capabilities:
  - detect_ai_writing_patterns
  - score_paragraph_ai_risk_estimate
  - external_detector_informed_risk_prioritisation
  - score_scope_aware_ai_risk_estimate_overall_only_for_full_document_scope_else_chapter_batch_fragment
  - rewrite_high_ai_paragraphs
  - preserve_academic_meaning
  - preserve_citations
  - preserve_hypotheses
  - preserve_statistical_results
  - generate_detection_report
  - assemble_locked_rewritten_document
  - build_external_risk_convergence_map
  - analyze_external_detector_report
  - rewrite_shared_ai_risk_patterns
  - extract_external_detector_scores
  - relocate_source_extracted_researcher_trace
  - detect_aggregation_worsening_risk
  - check_breakpoint_requirement
  - validate_phase7_gate_e
  - enforce_minimal_edit_rewriting
  - lock_chapter_score_red_line
  - maintain_chapter_version_ledger
  - target_lock_highest_risk_chapters
  - run_closed_loop_per_chapter_retest
  - detect_rewrite_stalemate
  - escalate_rewrite_intensity_stepwise
  - preserve_or_increase_word_count
  - validate_phase7_gate_f_wordcount
  - track_paragraph_and_chapter_wordcount
  - attempt_to_drive_measured_chapters_below_target_threshold_with_closed_loop_retests
  - escalate_through_six_rung_ladder_until_target_met
  - never_present_above_target_version_as_done_or_final_baseline
  - preserve_section_headings_on_own_line
  - prevent_paragraph_merging_and_mega_paragraphs
  - validate_phase7_gate_g_structure_readability
  - validate_phase7_gate_h_sentence_completeness_and_length
  - validate_phase7_gate_i_grammar_subject_verb_agreement
  - validate_phase7_gate_j_logic_flow_no_meta_commentary
  - preserve_hyphens_and_avoid_double_hyphen
  - verb_phrase_expansion_for_length
  - parenthetical_integration_preserving_abbreviation_definitions
  - detail_rich_core_and_keyword_cohesion_no_background_condensation
  - forbid_back_translation
  - evidence_based_authorship_restoration_t29
  - detect_placeholder_and_template_residue
  - detect_misplaced_sentence_insertions
  - lock_reference_list_and_verbatim_quotes
  - one_chapter_per_round_default
  - lock_thesis_title_author_supervisor_appendix
  - check_typos_double_spaces_and_literary_arrows
  - comparable_external_retest_and_scope_labelling
  - qualitative_supplement_scoring_d18_to_d21
  - qualitative_authorship_restoration_module
  - author_style_baseline_match_not_native
  - reject_over_polish_and_style_drift
  - reject_duplicated_heading_text
  - block_output_on_any_sentence_fragment
  - de_mechanize_repeated_subject_and_outline_paragraphs
  - forbid_over_polished_ai_phrases
  - universal_syntactic_completeness_fragment_detection
  - detect_doubled_case_connector_artifacts
  - reject_duplicated_table_figure_captions
  - check_sentence_initial_capitalization
  - check_demonstrative_number_agreement
  - check_proper_noun_spelling
  - branch_t19_t24_by_research_design_quant_or_qual
  - require_t19_source_extraction_no_generation
  - introduction_and_abstract_anti_template_rewrite
  - rewrite_fatigue_detection_and_stop
  - score_qualitative_dimensions_d18_d19q_d20_d21
  - qualitative_techniques_t25_to_t28
  - de_template_qualitative_transitions_and_theme_intros
  - disrupt_participant_quote_balance_within_real_data
  - no_fabricated_researcher_voice_or_quotes_or_nonverbal_detail
  - protect_statistical_symbol_formatting
  - flag_chinese_student_english_cliches
  - result_explanation_variant_library
  - table_narration_specific_focus
  - cnki_front_loaded_prioritisation
  - flag_chinese_text_template_phrases_when_source_is_chinese
  - flag_empty_comparison_and_capability_claims
  - break_too_clean_three_item_parallelism
  - protect_epistemic_hedges_positionality_and_scope_qualifiers
  - preserve_claim_strength_no_inferential_to_assertive_upgrade
  - discipline_exemption_for_field_standard_terms
  - detect_copula_avoidance_and_superficial_causal_chains
  - chinese_deep_ai_patterns_and_high_frequency_vocab
  - cluster_density_tiering_to_reduce_false_positives
  - source_extracted_researcher_trace_integration_no_mechanical_insertion
  - verbal_score_is_calibration_only_no_highlight_claim_without_report
  - qualitative_insufficient_material_author_confirmation_needed
  - phase3_risk_prioritisation_and_target_selection
  - conflict_resolution_hierarchy_integrity_first_examples_never_override
  - minimum_execution_map_and_pre_phase2_checklist
  - stage_vs_phase_disambiguated_master_overview_timing
  - scope_pattern_floor_renamed_from_document_pattern_floor
  - rejected_status_for_regression_not_progress
  - authorized_use_boundary_owned_or_authorized_text_only
  - partial_execution_is_run_level_not_seventh_status
  - stalemate_5pp_warning_vs_fatigue_3pp_pause_priority
  - rewrite_fatigue_hard_stop_one_authorized_extra_round
  - stage_phase_terminology_rule_phase_controls_order
  - canonical_output_authority_skill_overrides_references
  - quick_mode_anti_misrouting_keyword_block
  - strict_target_warning_threshold_only_not_relax_rules
  - t19_t29_master_boundary_rule_in_main_file
  - chinese_deletion_reinterpretation_rule
  - release_metadata_manifest_changelog_testcases_limitations
  - execution_order_lock_phase_then_stage_no_jump_to_done
  - chinese_route_fixed_ten_evidence_fields
  - t19_t29_not_default_tools_prefer_non_additive
  - d13_d15_minimum_structure_evidence_record
  - external_floor_excludes_references_appendices_tables
  - docx_plain_text_fallback_for_non_download_users
  - skill_audit_mode_hard_isolated_from_thesis_rewrite
  - active_target_threshold_replaces_hardcoded_30pct
  - candidate_rewrite_allowed_without_external_score_no_done_no_claim
  - aggressive_means_structural_depth_not_prose_generation
  - docx_final_only_after_gate_format_not_verified_label
  - section_repetition_score_scope_level
  - working_mode_minimum_evidence_packet
  - reference_path_rule_basename_fallback_for_audit
  - last_rung_structural_reorganisation_no_mechanical_t1_t29
  - external_40pct_floor_requires_comparable_scope
  - retest_status_machine_below_target_done_decreased_progress_rejected_rollback
  - stalemate_closed_loop_intra_paragraph_no_user_confirm
  - t19_template_relocation_not_mandatory_insertion
  - quick_mode_single_source_of_truth_skill_overrides_reference
  - d21_quotation_protection_referenced_in_method_routing
  - docx_fallback_default_text_only
  - mode_routing_summary_table_and_failure_state_table
  - scope_risk_index_formula_variable_renamed
  - centralised_escalation_stop_condition_paused_blocked_only
  - reference_availability_check_partial_execution
  - much_higher_defined_15pp_or_1_5x
  - legacy_elevated_verb_bank_demoted_thesis_safe_default
  - exact_action_three_pass_evidence_no_generic_labels
  - mixed_language_paragraph_split_by_span
  - user_strict_target_below_30_warning
  - phase2a_route_specific_scoring_english_chinese_qualitative
  - phase6_scope_aware_internal_risk_index_renamed
  - thesis_evidence_audit_mode_distinct_from_skill_audit
  - score_regression_baseline_check_no_external_claim_before_retest
  - locked_version_scoped_to_named_detector_stream
  - trigger_c_source_supported_only_no_forced_trace_insertion
  - author_baseline_rules_renamed_from_human_like
  - public_evidence_route_aware_chinese_uses_chinese_fields_not_english_table
  - phase8_scope_appropriate_risk_index_not_forced_overall
  - t19_relocation_vs_t29_reconstruction_separated_in_templates
  - expanded_source_trace_block_with_operation_type_and_location
  - over_cap_parent_split_gate_f_on_combined_descendant_word_count
  - word_count_floor_with_over_readability_cap_exception
  - gate_e_always_shown_na_when_not_triggered
  - structured_source_trace_block_for_t19_t29
  - plan_next_round_is_not_execute_wait_for_external_retest
  - quantitative_signal_calibration_anchors_cv_ttr_passive_transition_density
  - repeated_ngram_generic_sequence_signal_excluding_protected_terms
  - never_route_text_through_third_party_humanizer_or_bypass_api
  - rare_word_over_elevation_signal_aligned_with_precision_over_rarity
  - legitimate_citation_carveout_for_vague_attribution_false_positive
  - detector_ai_refined_class_reinforces_over_polish_guard
  - single_signal_in_isolation_is_not_a_reliable_ai_tell_require_cluster
  - count_occurrences_before_claiming_overuse_or_uniformity
  - no_double_count_same_span_across_multiple_dimensions
  - preserve_hard_to_fabricate_human_signals_and_author_asides
  - optional_external_author_sample_for_style_baseline_calibration_only
  - flag_fragmented_header_restatement_low_information
  - predicate_position_generic_hyphen_signal_subordinate_to_gate_d
  - flag_antithesis_template_and_hedge_stacked_predictions
  - chinese_term_abbreviation_symbol_anti_repetition_conventions
  - mba_conclusion_chapter_risk_observation_small_sample_heuristic
  - task_routing_skill_audit_assembly_similarity_reject
  - language_routing_en_zh_mixed_and_method_routing
  - scope_aware_targets_whole_document_only_when_comparably_measurable
  - external_detector_informed_not_calibrated_prediction
  - readability_soft_160_9_hard_cap_200_12_with_over_cap_exception
  - chinese_route_high_risk_uses_chinese_evidence_not_english_table
  - source_trace_block_referenced_in_all_t19_t29_output_templates
  - chinese_route_evidence_template_and_chinese_paragraph_risk_estimate
  - working_mode_compact_skip_record_full_tables_only_in_staged_mode
  - appropriate_ledger_chapter_version_or_internal_planning
  - no_external_result_claim_wording_rule
  - docx_format_preservation_fallback_not_verified_label
  - target_status_state_machine_done_progress_paused_blocked_incomplete
  - default_excluded_units_and_external_test_scope_consistency
  - non_comparable_detector_handling
  - docx_output_gate_and_file_naming_convention
  - quick_mode_unified_explicit_or_inferred_with_sample_exception
  - cnki_two_zone_scan_report_first_back_loaded_mba_chapters
  - staged_threshold_50_recommended_80_mandatory
  - full_staged_evidence_scoped_to_target_highlight_cluster_high_risk
  - scope_aware_phase6_target_chapter_or_batch_not_whole_document
  - skill_audit_mode_output_template
  - chinese_qualitative_route_adapted_d18_d21_concerns
  - t16_shared_external_risk_structural_pass_detector_agnostic
  - protected_chinese_statistical_terms_extended_youxiao_mingxian_tisheng
  - model_agnostic_wording_no_claude_name_in_references
  - docx_output_hygiene_placeholders_leaked_markup_chinese_mojibake
  - flag_elegant_variation_same_entity_renamed
  - flag_formulaic_despite_x_offers_y_conclusion
  - phase0_initial_ledger_creation_no_first_run_deadlock
  - detector_informed_prioritisation_but_detector_agnostic_technique
  - mandatory_source_annotation_for_t19_t29_traces
constraints:
  - Do not change citations, references, variables, hypotheses, data, coefficients, significance levels, or statistical conclusions.
  - Do not add unsupported claims, new theories, new references, or new data.
  - Do not make the writing casual, promotional, or overly polished.
  - Do not intentionally add grammar or spelling errors.
  - Preserve the original structure unless repetition or mechanical organization clearly needs adjustment.
  - Treat low internal AI scores with caution. If a comparable external detector score is much higher, recalibrate upward and increase structural targeting depth, not prose-generation intensity. "More aggressive" here means deeper diagnosis of repeated architecture, rhythm, reporting sequence, and source-trace relocation; it never means freer paraphrasing, smoother rewriting, or whole-paragraph regeneration.
  - Do not use random short-sentence insertion as a substitute for dimension-targeted rewriting.
  - Every rewritten paragraph must be linked to its detected AI-risk dimensions and selected rewrite techniques.
  - The three-pass rewrite protocol must be executed explicitly; do not skip Pass 1, Pass 2, or Pass 3.
  - Protected elements must be checked before and after rewriting, including capitalization, abbreviations, citations, hypotheses, coefficients, p-values, model names, and table numbers.
  - If protected elements are changed accidentally, restore them before final output.
  - If execution evidence is missing, mark the revision as incomplete instead of presenting it as final.
  - Do not perform full-document batch rewriting before Phase 4.5 execution planning is completed.
  - Do not treat a rewritten DOCX as final unless Phase 5.5 and Phase 7 evidence are attached and the DOCX Output Gate has passed. If original formatting, comments, tracked changes, tables, figures, captions, equations, footnotes, or reference-list layout cannot be verified, deliver either a text-only DOCX candidate labelled format-preservation-not-verified, or — if the user cannot download files or asks for copyable content — a plain-text reconstruction with headings, paragraph IDs, protected-element notes, and a clear statement that original DOCX formatting was not verified. Do not claim full DOCX format preservation.
  - Do not route thesis text through any third-party humanizer, "undetectable AI", detector-bypass API, paraphrasing API, or external rewriting service. This violates confidentiality, academic integrity, and the minimal-edit rule (Principle 2), and is self-defeating because machine-rewritten prose reads as AI to detectors. Rule-based diagnostics and local/manual analysis are fine; outsourcing the rewrite to a bypass tool is not.
  - If the workflow is resumed after interruption, verify missing phases before continuing.
  - Do not calculate paragraph_risk_index from a partial dimension set.
  - Automated scoring scripts may be used only as preliminary support; they must not replace the full D1-D17 evaluation.
  - For English thesis text, every included body paragraph must receive route-required screening before paragraph_risk_index, priority group, or rewrite strategy is finalized — full visible D1–D17 tables are mandatory for target paragraphs, externally highlighted paragraphs/fragments, repeated-structure clusters, and any paragraph with final risk estimate ≥40%, while low-risk non-target paragraphs may use a Working-Mode compact skip record that still states D12–D17 structural risks were checked and why the paragraph was not selected. For Chinese thesis text, do not mechanically apply the English lexical/syntax dimensions; use the Chinese-text AI-risk module plus the shared structure-level dimensions (paragraph architecture, section-template dependency, reporting-sequence regularity, external-highlight evidence) and report the result as `chinese_paragraph_risk_estimate`, not as a full English D1–D17 score. This route-specific rule OVERRIDES any later generic requirement for full D1–D17 tables — when the language route is Chinese, the visible evidence must use the Chinese-route template. Evidence depth is also mode-scoped (see Working Mode vs Full Staged Mode).
  - For English-route paragraphs, D12, D13, D14, D15, D16, and D17 must always be reviewed and reported, because they are core external-detector structural, methodological-template, and reporting-sequence risk dimensions, and must never be omitted from the English scoring table. In qualitative passages, D16 and D17 may be scored 0 / Not Applicable only when no methodology-template or reporting-sequence risk exists, and the report must still list D16 and D17 with a one-line reason for the N/A. For Chinese-route paragraphs, do not force the English D12–D17 table; instead report their functional equivalents as shared structure checks — paragraph architecture, section-template dependency, methodology/reporting template, predictable reporting sequence, and external-highlight evidence.
  - If any dimension required by the selected route is missing, mark the paragraph score as invalid and rerun Phase 2. The required set is route-specific: English D1–D17 for English text; the Chinese-route fields for Chinese text; the D18–D21 supplement only for qualitative/mixed-methods sections.
  - NEVER regenerate a whole paragraph from scratch. Rewrite by minimally editing existing sentences (substitute words, reorder, split, recast). Every rewritten sentence must trace back to a specific original sentence. Whole-paragraph regeneration is the single largest source of new AI features and is forbidden.
  - "WORD COUNT MUST BE PRESERVED OR INCREASED. AI-score reduction must never be achieved by compressing, merging, deleting, or shortening content. Each rewritten paragraph must have a word count greater than or equal to the original paragraph. The +0% to +15% growth target applies only when it does not breach the readability cap; if the source paragraph is close to the 200-word / 12-sentence cap, preserve or minimally increase length without exceeding the cap, and if needed split safely and assess Gate F on the combined descendant word count. Reducing length to remove AI features is forbidden — change HOW ideas are expressed, never REMOVE ideas. See Principle 4, including its over-cap exception: when the original paragraph already exceeds the readability cap, preserve all content without forcing further growth and never shrink it."
  - A chapter is DONE only when its measured external AI score is below the target threshold (default 30%). Stop AI-reduction edits on a chapter only once it is below target. A chapter at or above the active target threshold is NOT finished and must keep being revised, or be marked Paused/Blocked with a documented reason (see Principle 0 and Principle 3); when the default target is used, the threshold is below 30%. Do not present an above-target version as final.
  - Each chapter's current measured external score is a RED LINE. After rewriting, the new chapter is only a candidate version until the user re-tests it with the external detector. If the external re-test score is not lower than the red line, DISCARD the rewrite and keep the previous lowest-score version. Do not use internal estimates as proof of improvement.
  - Process ONE chapter per round. After each chapter is rewritten, pause and ask the user to re-test it with the external detector before moving to the next chapter. This skill does not rewrite a whole thesis in one pass.
  - "Each round must target exactly ONE chapter by default: the chapter with the highest current measured external score that is still at or above the target (default 30%). All other chapters must be explicitly marked \"not rewritten this round\" and left untouched. Two chapters may be processed in one round only when the user explicitly requests it and both chapters will be re-tested separately."
  - "\"Aggressive Structural Rewrite\" is a last resort, not a default. Always start at the lightest intensity and escalate only step by step, re-checking after each step. Never apply heavy rewriting to a paragraph in a single move."
  - A chapter version ledger must exist before any new round. If the ledger (current score / lowest-ever score / source version per chapter) is not available, do not start a new rewrite round. Phase 0 (initial-ledger creation, resolves the first-run deadlock): if no ledger exists yet, CREATE the initial ledger from whatever is available — the chapter list, the baseline version, and any external detector scores provided. If external scores are unavailable, mark each chapter's external score Unknown. The skill may still perform a Quick Mode or Single-Batch candidate rewrite using internal risk estimates only, but it must label the result as candidate version prepared for external re-test, and must not create an external red-line ledger, claim detector improvement, or mark the chapter Done. A scored external closed-loop round still requires at least a comparable baseline score. The "ledger must exist" rule is satisfied by this initial creation step — it never means the first run is blocked.
  - NEVER MARK ABOVE-TARGET WORK AS DONE. Reaching a new lowest score that is still ≥ 30% (or the user's target) is progress, not completion. While any chapter or the overall document is at or above target, its status must be PROGRESS, PAUSED, or BLOCKED (never DONE — see the status state machine), and the skill keeps proposing the next round and moving up the escalation ladder (Principle 5). DONE is used only when the measured external score is below target. Legitimate reasons to pause (PAUSED/BLOCKED rather than continue) are listed below; exhausting the full six-rung ladder on a chapter is one of them.
  - NEVER cross structural boundaries when rewriting. Section/sub-section headings (e.g. "1.1 Research Background", "Chapter 2", "5.2.1"), figure/table captions, list items, and the blank lines that separate paragraphs are hard boundaries. Do not merge text across a heading, do not absorb a heading into body text, do not move a heading, and do not strand a heading at the end of a paragraph. A heading must always start on its own line with the paragraph break before and after it preserved exactly as in the original. See Principle 6.
  - NEVER produce hard-to-read mega-paragraphs. Do not merge paragraphs together. A rewritten paragraph should normally stay around 160 words / 9 sentences (soft target); the hard cap is 200 words / 12 sentences, unless the original paragraph already exceeded that cap (then preserve content, avoid further growth, and split only at safe boundaries — never merge or delete). If reducing AI risk seems to need a longer block, keep the original paragraph breaks instead. Readability is enforced by Phase 7 Gate G. See Principle 6.
  - NEVER create grammatically incomplete sentence fragments. Every sentence in the output must be a complete grammatical sentence with a subject and a finite verb. Do NOT split a subordinate clause into a standalone "sentence" (e.g. "When employees interact with AI in daily work."), and do NOT turn a noun list or phrase into a standalone "sentence" (e.g. "Service methods, management practices, and ways of solving problems."). Splitting is only allowed at points where BOTH resulting parts are complete independent sentences. Do not chop narrative prose down to ~10-word sentences if that creates fragments or a choppy, stop-start rhythm. This is enforced by Phase 7 Gate H. See Principle 8.
  - NEVER write over-long, over-nested sentences. Do not produce sentences longer than about 30 words or with more than two subordinate clauses. If a rewrite makes a sentence long and tangled, split it into two complete sentences (each grammatically whole, per Principle 8). Avoiding short-sentence chopping must not push the rewrite to the opposite extreme of dense, hard-to-parse sentences. Enforced by Phase 7 Gate H.
  - "NEVER introduce subject-verb agreement errors or other grammar mistakes. The output must be grammatically correct academic English: singular subjects take singular verbs, plural subjects take plural verbs, tense is consistent, and articles/prepositions are correct. Reducing AI features must never be done by deliberately inserting grammar errors. Enforced by Phase 7 Gate I."
  - NEVER mangle hyphens or dashes. Avoiding em dashes (—) must NOT be done by writing a double hyphen ("--"). Keep every hyphenated compound (e.g. "employee-AI", "self-efficacy", "AI-generated") with its single hyphen; keep en dashes in numeric/date ranges (e.g. "2007–2010"). When an em dash is removed, replace it with a comma, colon, semicolon, parentheses, or two sentences — never with "--" or "-". The string "--" must not be INTRODUCED in revised thesis prose. (This does not apply to protected verbatim quotations, code blocks, file metadata, Markdown separators, or URLs that must stay exact.) Enforced by Phase 7 Gate D.
  - NEVER insert jarring meta-commentary or self-justifying asides. Do not add sentences that explain or justify the writing or the research design out of nowhere, such as "This detail was included to improve measurement precision." or "This sentence is added to clarify the logic." Every sentence must follow logically from the surrounding text and serve the thesis's own argument. Researcher-trace sentences (T19) are allowed ONLY when they fit the local argument and read as the author's natural reasoning, never as an out-of-place explanation of the methodology or of the rewrite itself. Enforced by Phase 7 Gate J.
  - NEVER over-simplify into thin, conversational sentences. A sentence can be grammatically complete yet still too shallow for a thesis (e.g. "It explains one specific thing.", "The opposite can also occur.", "Self-efficacy is especially important in social cognitive theory. It explains one specific thing."). Do not reduce AI risk by flattening academic prose into short declarative statements that a textbook or a chat reply would use. Keep an appropriately academic register and information load. Enforced by Phase 7 Gate H (thin-sentence check) and Gate J.
  - "NEVER fabricate content to look human. This applies especially to qualitative rewriting (T25–T28) and researcher-trace insertion (T19): do not invent researcher feelings or memories (\"stayed with me\"), positionality (\"As a researcher who had also...\"), non-verbal observations (\"looking down, pausing\"), participant quotes, longer versions of real quotes, \"surprise\" at a statistical result, or a documented \"silence/absence\". Fabrication is an academic-integrity violation AND self-defeating, because freshly generated \"human voice\" sentences read as AI to detectors. T19 may only relocate or lightly rephrase existing researcher-side material. T29 may reconstruct a new interpretive sentence only when it is fully traceable to existing quotations, codes, themes, documented methods, cited literature, or stated boundaries, and only with a completed Source Trace block; if the trace cannot be shown, write author confirmation needed instead of adding the sentence. If the needed material is not in the paper, use a different technique. Enforced by Gate B (protected quotes/data) and the T19/T25–T28 extraction-only rules."
  
references:
  - references/detection_principles.md
  - references/rewrite_methods.md
  - references/qualitative_authorship_restoration.md
  - references/chinese_text_ai_risk.md
---

# AIGC Detector & Rewriter Skill

## Description
Detect AI-writing risk patterns in English and Chinese thesis text — English text uses the conservative D1–D17 framework, Chinese text uses the Chinese-text AI-risk module plus shared structure-level checks, and mixed documents are routed by language segment — score paragraph-level and document-level AI risk, and rewrite high-risk sections by reducing shared external-detector-sensitive features such as repeated templates, uniform rhythm, mechanical reporting sequences, and over-smooth academic reasoning.
The scoring system is intentionally conservative and calibrated for structural AI-risk signals commonly detected by external AI detection systems in formal master’s thesis writing.

This skill should not treat a low internal score as proof that the text is safe. When a known detector result is available, such as Turnitin AI = 48%, use it as a calibration signal and adjust the internal scoring more strictly.

## Core Operating Architecture (READ FIRST — overrides any conflicting rule below)

Multiple failure modes have been observed in real multi-round use, including score regression, structural over-editing, word-count loss, readability damage, detector-comparison error, and unsupported researcher-trace insertion. The rules in this section exist to prevent them and override any conflicting rule anywhere else in this file.

### Principle 0 — The goal is a TARGET, not merely "lower than last time"

The operational objective is to reduce traceable AI-writing-risk patterns in user-provided thesis text and to prepare candidate revisions for comparable external re-test. The target threshold (default 30%, or a stricter value the user specifies) is used only as a closed-loop stopping condition when comparable detector evidence exists; the skill must never guarantee, imply, or optimise for a detector outcome independently of academic integrity, meaning preservation, and evidence-based revision. Chapter scores are the primary closed-loop units; the whole-document score is a target only when a comparable whole-document external test is available. "Lower than the previous version" is NOT success. A version that is the lowest so far but still above the active target is NOT finished — it is work in progress.

**Authorized-Use Boundary**: this skill may be used only on thesis text the user owns, authored, co-authored, or is explicitly authorized to edit. It supports clarity, academic integrity, and detector-informed risk diagnosis; it must NOT be used to misrepresent authorship, hide prohibited AI use, fabricate research contribution, or bypass an institution's disclosure or assessment rules.

**T19/T29 Master Boundary Rule**: T19 is relocation or light integration of researcher-side material that already exists elsewhere in the thesis; T19 never creates new interpretive content. T29 is evidence-based reconstruction; T29 may add a new interpretive sentence only when a completed Source Trace block proves it is grounded in existing thesis materials, codes, quotations, methods, findings, or cited literature. For qualitative passages, any new interpretive sentence must use T29, never T19. If a source trace cannot be established, write "Author confirmation needed" instead of adding the sentence.

**Strict Target Warning**: if the user sets a target below 30% (especially below 15%), warn that the target may be unrealistic depending on detector behaviour, thesis genre, standardised methodology language, and required academic terminology; the skill can attempt risk-pattern reduction but cannot guarantee the target; and academic integrity, protected content, readability, and meaning preservation override the numeric target. A stricter user target changes the target threshold ONLY — it never relaxes any integrity, minimal-edit, no-fabrication, word-count, or quality-gate rule.

Definition of done:
- A chapter is DONE only when its measured external score is **< 30%** (or the user's target).
- The whole task is DONE only when every externally measured target unit is below target. If the external detector supports only chapter-level testing, the task may be DONE once every chapter is below target; if a comparable whole-document score is available, the whole document must also be below target.
- Until then, the skill must keep proposing the next rewrite round. It must never present an above-target version as the final result or imply that no further reduction is possible.

Never-stop-early rule:
- Reaching a new lowest score does not end the work; it only updates the baseline. If that lowest score is still ≥ 30%, immediately plan the next round on the highest-remaining chapter.
- The legitimate reasons to pause are: (a) all measurable target units are below target; (b) the user asks to stop; (c) the full escalation ladder (Principle 5) has been exhausted and documented on a chapter AND the user has been told which specific structural constraint is blocking further reduction; (d) Rewrite Fatigue Detection is triggered; (e) no comparable external re-test is available; or (f) continuing would risk changing protected academic content or damaging readability. Rewrite Fatigue Detection overrides the never-stop-above-target rule: when fatigue triggers, restore the lowest-ever comparable version, report the next untried safe option, and do not run another round until the user chooses to continue.
- "I cannot reduce it further" may only be said after every rung of the Principle 5 escalation ladder has been tried and documented for that chapter.

### Principle 1 — Closed loop, one chapter per round

This skill does NOT rewrite a whole thesis in one response. Internal D1–D17 scoring cannot reliably predict the external detector result, so the only trusted verdict is a real re-test.

The mandatory loop is:

```text
pick the single highest-scoring chapter that is still at or above the target (default 30%)
  → rewrite ONLY that chapter, using minimal edits at the current escalation rung
  → output the rewritten chapter + evidence
  → STOP and ask the user to re-test with CNKI / Turnitin
  → if the new score is BELOW target: lock it as done, move to the next-highest chapter
  → if the new score is lower than before but STILL above target: keep this version as the new baseline, mark the chapter PROGRESS (not DONE), AND plan the next round on the SAME chapter, moving UP one escalation rung (Principle 5). "Plan" means describe the next round; do NOT execute the next rewrite in the same response. Wait until the user supplies a comparable external re-test of this version (or the chapter text/version to revise) or explicitly asks to continue, per the mandatory re-test stop.
  → if the new score stayed the same or went UP: roll back to the chapter's lowest-ever version, then move UP one escalation rung and try a DIFFERENT technique on the same chapter
  → repeat until the chapter is below target or the escalation ladder is exhausted
```

Always tell the user explicitly: "Rewrite one chapter, re-test it, and continue. We keep going on each chapter until it is below the active target threshold, not just lower than before." The active target is the user-specified threshold when provided; otherwise it defaults to below 30%.

### Principle 2 — Minimal edit only, never regenerate

The biggest cause of score regression (e.g. a chapter rising from 36% to 100%) is letting the model re-generate a paragraph as fluent new prose. Fluent AI-generated academic text carries strong AI features by construction.

Rules:
- Rewrite by editing the EXISTING sentences: substitute individual words, reorder clauses, split long sentences, recast voice/structure, and relocate or integrate researcher-trace material drawn from existing content.
- Every sentence in the output must be traceable to a specific original sentence (or be a permitted researcher-trace/breakpoint sentence based on existing content).
- Preserve as much of the original human wording as possible — original human phrasing is what keeps the score down.
- Whole-paragraph or whole-section regeneration is FORBIDDEN, even for A-class / P0 paragraphs.
- Back-translation is FORBIDDEN. Never translate text to another language and back (e.g. Chinese → English → rewrite → Chinese) to reduce AI features. Round-tripping through translation is whole-paragraph regeneration in disguise: it discards the original human wording and emits fresh machine-distributed text — the exact failure mode that drove a chapter from 36% to 100%. Edit the existing sentences in place instead.
- Do NOT delete content or merge sentences to reduce AI features. Splitting one sentence into two is allowed; merging two sentences into one is not allowed AS A ROUTINE AI-RISK TECHNIQUE (it loses length and is rarely necessary). Exception: a merge IS permitted to REPAIR a fragment, an accidentally split clause, or a thin/over-conversational sentence created during revision (Gate H); the repaired sentence must preserve the original meaning and must not reduce the chapter's substantive content. See Principle 4.
- "Aggressive Structural Rewrite" means aggressive REORGANISATION of existing sentences (reordering, re-segmenting, changing entry point), never aggressive REWRITING into new prose.

> Priority note: the principles are numbered in order (P1–P6) and the workflow Phases run in order (Phase 1 → 1.5 → 1.6 → 1.6A → 1.7 → 2 → 2b → 3 → 4 → 4.5 → 4.5A → 5 → 5.5 → 6 → 7 → 8 → 9). Numeric order is for reference only; it is NOT the conflict-resolution order. When two rules ever appear to conflict, apply this fixed priority instead: protect data/citations/quotes/hedges > preserve word count > readability soft-limits > AI-risk reduction; and external re-test result > internal risk estimate.

> Conflict Resolution Hierarchy (full order, highest first): (1) academic integrity and protected elements; (2) user-specified scope and target; (3) Core Operating Architecture and Principles 0–9; (4) language-route rules (English D1–D17 vs Chinese route); (5) task-mode and staged-execution rules; (6) Phase gates A–J; (7) reference modules and technique files; (8) examples and prompts. Examples never override mandatory rules. Within this order, the data/word-count/readability/AI-risk and external-vs-internal sub-priorities above still apply.

Canonical Output Authority: SKILL.md is the only authority for workflow-level output structure (Phase order, target lock, ledger, Phase 7 Gate A–J, Phase 8/9 summary, external re-test stop, DOCX Output Gate). Reference files may provide paragraph-level evidence templates, examples, and technique-specific subfields only; if any reference output template conflicts with SKILL.md, SKILL.md overrides it.

> Minimum Execution Map (anti-phase-skipping; full definitions remain in their own sections):
>
> | Route / Mode | Required phases (cannot be silently skipped) | Required visible evidence |
> |---|---|---|
> | Quick Mode | Protected-element check → single-paragraph diagnosis → rewrite → Gate A–J summary | Scope statement; hit dimensions or Chinese-route groups; techniques; one-line Gate A–J; "no chapter/document score" statement |
> | Working Mode (English route) | 1 → 1.5 → 1.6/1.6A → 1.7 → 2 (full tables for target/highlighted/cluster/≥40% paragraphs) → 3 → 4 → 4.5/4.5A → 5/5.5 → 6 (scope-aware) → 7 → 8 → 9 | Full evidence for target paragraphs; compact skip records for non-target low-risk paragraphs; ledger; re-test stop |
> | Working Mode (Chinese route) | Same phase chain, with Phase 2 using Chinese-route fields instead of D1–D17 tables | Chinese-route evidence template; shared structure checks; chinese_paragraph_risk_estimate |
> | Full Staged Mode / Thesis-Evidence Audit | All phases, staged by batch; Stage 1 diagnosis and planning only → Stage 2 rewrite with execution evidence → Stage 3 Gate A–J quality check → Stage 4 scope-aware final output → Stage 5 mandatory re-test stop | Stage outputs incl. appropriate ledger, Master Overview, scope-appropriate risk index, DOCX gate when applicable |
> | Skill-Audit Mode | No thesis phases; no D-scoring | Issue list in the required (or user-provided) audit format |

### Principle 3 — Red lines, target lock, and the version ledger

- **Red line (never regress):** Each chapter's lowest-ever measured external score is a hard ceiling for that chapter. A rewrite that scores higher than the chapter's lowest-ever version is discarded and the lowest-ever version is restored.
- **Target, not ceiling:** The red line prevents regression; it does NOT define success. Success is reaching below the target threshold (default 30%). Keep working a chapter until it is below target, even after it reaches a new lowest score.
- **Protection floor = the target:** Only a chapter already **below the target threshold (default 30%)** is protected and left alone. A chapter between 30% and 40% is NOT protected and must keep being rewritten — earlier versions of this skill wrongly froze chapters below 40%, which caused premature stopping above the 30% goal. Do not protect any chapter that is still at or above 30%.
- **Target lock:** Each round may only touch ONE chapter by default: the highest current measured chapter that is still at or above the target. Everything below target is left untouched. Bounded-unit exception: if an external report highlights only a bounded subsection or a fragment cluster (e.g. one flagged sub-section of the introduction), the round MAY target that bounded unit instead of the whole chapter, while still tracking it under that chapter's ledger.
- **Escalation, not surrender:** If a chapter changes by less than 5 percentage points in a round but is still above target, do NOT stop and do NOT merely "ask the user to confirm". Move up one rung on the escalation ladder (Principle 5) and try a stronger, still-safe technique on the same chapter next round.

### Principle 4 — Word-count preservation (never shrink the paper)

Compression and merging are forbidden as AI-reduction methods. A thesis usually has a minimum word-count requirement, and shrinking it is a serious failure even if the AI score drops.

Rules:
- Every rewritten paragraph must have word count ≥ the original paragraph (one-to-one rewrite), with the acceptable range being the original length up to about +15%. If an over-cap original paragraph is split into two or more descendant paragraphs at safe logical boundaries, Gate F is assessed on the COMBINED word count of all descendants against the original parent paragraph (record Parent Paragraph ID → New Paragraph IDs); the combined count must be ≥ the original parent.
- Over-cap exception (resolves the conflict between "never shrink" and the 200-word / 12-sentence readability cap): the +0% to +15% growth target applies only when the original paragraph is WITHIN the readability cap. If an original paragraph already exceeds 200 words or 12 sentences, do NOT force further expansion. In that case preserve every piece of substantive content, meaning, evidence, citation, variable, datum, and conclusion; do not add filler merely to grow the count; keep the revised paragraph no longer than the original unless a source-supported clarification genuinely requires it; and prefer splitting the over-long paragraph at a natural logical break (this raises sentence count and readability without losing content) over leaving one mega-paragraph. Record Gate F as "Pass — no substantive shrinkage; original already exceeded the readability cap." This exception NEVER licenses removing or condensing substantive content; it only lifts the artificial growth target for paragraphs that are already too long.
- Content deletion vs connector removal (resolves a common deadlock): deleting substantive content — data, reasoning, citations, claims, examples, limitations, findings — is FORBIDDEN. Removing a low-information connective or empty formulaic opener ("Furthermore,", "It is worth noting that", "综上所述") IS allowed, but only when (a) the logical relation stays clear without it and (b) the words removed are compensated within the same paragraph by concrete detail already in the thesis. Connector removal with same-paragraph compensation is NOT content deletion and does not violate the no-shrink rule.
- AI features must be reduced by CHANGING how ideas are expressed (reorder, recast, vary rhythm, differentiate structure, integrate researcher reasoning already present), never by REMOVING ideas or condensing them.
- "Compression", "condensing", "merging templates", "shortening", "trimming", and "removing repeated explanation" are all FORBIDDEN as length-reducing operations. Where older techniques (e.g. T17, T18) say "compress", reinterpret them as "rewrite the repeated template into varied, equally-long-or-longer prose" — break the pattern by restructuring and adding specificity, not by cutting words.
- If breaking a repeated template would remove words, you must compensate by expanding elsewhere in the same paragraph (e.g. add concrete detail, a researcher-view judgment sentence, or a process narration sentence drawn from existing content) so net length does not fall.
- Splitting a long sentence into two shorter sentences is encouraged (it varies rhythm AND tends to add words). Merging sentences is not allowed as a routine AI-risk technique, but IS allowed to repair a fragment or thin sentence (the repair exception in Principle 4 / Gate H).
- Phase 7 Gate F enforces this: any rewritten paragraph shorter than its original FAILS the gate and must be redone.
- Word-count preservation must NOT be achieved by generic filler, duplicated reasoning, empty transition sentences, or unsupported elaboration. Any added wording must preserve or clarify existing content and must pass Gate J's low-information-filler review. Reaching length by padding is itself an AI signal and a quality defect.
- Report the before/after word count for every rewritten paragraph (see Phase 5.5 and Phase 8).

### Principle 5 — Escalation ladder (how to keep reducing a stubborn chapter)

When a chapter is still above target, escalate through these rungs in order. Each rung is progressively more structural but every rung still obeys minimal-edit (Principle 2) and word-count preservation (Principle 4). Never jump straight to a high rung; never regenerate prose; never compress.

```text
Rung 1 — Sentence-level: vary openings, transitions, sentence length, lexical choices (T1–T13).
Rung 2 — Rhythm & cadence: break uniform sentence-length patterns; split long sentences; vary clause order within sentences (T11, Pass 2).
Rung 3 — Paragraph architecture: change each paragraph's entry point and internal order; differentiate neighbouring paragraphs that share a template (T14, T15).
Rung 4 — Reporting-sequence & template breaking: reorder reporting steps; de-template methodology/variable/result patterns (T17, T18 — length-preserving versions).
Stop condition (centralised): escalation stops only by marking the unit PAUSED or BLOCKED, and only when academic integrity or protected content would be put at risk, readability damage cannot be avoided, external evidence is non-comparable, Rewrite Fatigue triggers, the user asks to stop, or the full six-rung ladder has been exhausted and documented. Escalation never stops by silently marking an above-target unit DONE.

Rung 5 — Source-extracted researcher-trace integration: relocate or lightly integrate more researcher-view judgment, process narration, scope-narrowing, boundary, and existing-data-anchor material already present in the thesis across the chapter (T19), as a previously observed potentially useful reducer (effectiveness not guaranteed; confirm by comparable external re-test). Never generate new researcher voice. "Integration" here means relocation of existing material, NOT saturation: use it sparingly, at most one relocated researcher-trace sentence per high-risk paragraph, and never insert researcher-trace sentences mechanically across consecutive paragraphs (repeated mechanical insertion is itself an AI-risk pattern).
Rung 6 — Functional reorganisation: change what each paragraph DOES (e.g. turn a flat "definition → source → result" report into a problem-driven or contrast-driven passage) by reordering and recasting the sentences WITHIN that paragraph. This never means shuffling the order of paragraphs across the section or changing the chapter's argument flow (see Principle 7). Still never regenerate prose; keep word count and the paragraph's position unchanged.
```

Rules:
- Track the current rung per chapter in the ledger.
- After each re-test that is still above target, advance one rung (or, if the last rung produced a clear drop, repeat the same rung more thoroughly before advancing).
- Only after Rung 6 has been applied thoroughly and the chapter still will not drop below target may the skill tell the user that a specific, named structural constraint is blocking further reduction (e.g. an unavoidable standardized methodology section) — and even then it should offer the best available below-baseline version and ask whether to continue trying.
- Escalating rungs must never violate Principles 2 and 4 (no regeneration, no shrinking).

**Rewrite Fatigue Detection (mandatory stop condition):**
Even before Rung 6 is exhausted, declare rewrite fatigue and pause if ANY of these is true for a chapter:
- 3 or more complete rounds (rewrite + external re-test) have been done on this chapter (this is a hard stop checkpoint — the user may explicitly authorize ONE additional controlled round, but the skill must never silently continue past it); OR
- the change in measured external score across the last two rounds is < 3 percentage points (in either direction); OR
- a rewrite increased the score (already handled by Score Regression Guard — fatigue is a wider net).

On fatigue, do NOT keep grinding the same chapter. Take this sequence:
1. Roll back to the chapter's lowest-ever measured version.
2. Look at the "Tried techniques on this rung" column in the ledger (see below). Try ONE clearly untried technique appropriate to the current rung.
3. If no untried technique remains for the current rung, advance one rung.
4. If Rung 6 is reached and still fatigued, STOP this chapter, report the situation honestly to the user, and recommend external editing rather than another model-driven round. Never imply that further mechanical rewriting will help when the data says it will not.

### Principle 6 — Preserve structure and readability (no merged mega-paragraphs, no displaced headings)

Reducing the AI score must never make the paper read worse. Two failure modes are forbidden:

**(a) Displaced or absorbed headings.** Section and sub-section headings such as "1.1 Research Background", "Chapter 2 Theoretical Foundations", "5.2.1 Procedural Control Methods", as well as figure/table captions and numbered/bulleted list markers, are HARD STRUCTURAL BOUNDARIES.
- Never merge body text across a heading.
- Never pull a heading into a body paragraph or let a paragraph run straight into the next heading.
- Never move a heading, renumber it, or strand it at the end of a paragraph.
- Every heading keeps its own line, with the paragraph break before and after it exactly as in the original. If a heading text reads like "1.1 Research Background", it must appear on its own line, not inside or at the tail of a sentence.
- Rewriting happens strictly INSIDE the body text between two headings; the headings themselves are protected elements (Gate B) and the boundaries are checked by Gate G.

**(b) Merged mega-paragraphs.** Do not combine paragraphs to fight cross-paragraph repetition. Merging produces over-long blocks (e.g. 212 words / 18 sentences) that are exhausting to read.
- Keep the original paragraph breaks. Cross-paragraph repetition (D13) is reduced by DIFFERENTIATING neighbouring paragraphs (changing each one's entry point, order, and function), NOT by merging them.
- A rewritten paragraph must stay within readable limits: about **160 words** and about **9 sentences** maximum (soft target), and must never exceed **200 words** or **12 sentences** (hard cap). If staying under the cap conflicts with reducing AI risk, keep the paragraph split — never merge to a longer block.
- "Fragment cluster" and "paragraph group" are DIAGNOSIS units (for planning cross-paragraph differentiation). They are NOT licence to output one merged paragraph. Each original paragraph remains a separate paragraph in the output.
- If a single original paragraph is itself longer than the hard cap, you may split it into two paragraphs at a natural logical break (this improves readability and adds no AI risk), but you may never merge.

Gate G (Phase 7) enforces both (a) and (b). Any output that violates them fails and must be redone.

### Principle 7 — "Reorganisation" means within-paragraph only (never reorder paragraphs or change the argument)

Throughout this skill, "reorganise", "reorder", "change entry point", "paragraph architecture", and "functional reorganisation" mean changing the order and framing of sentences INSIDE a single paragraph, plus differentiating neighbouring paragraphs from each other. They do NOT mean:
- shuffling the sequence of paragraphs within a section;
- changing the logical development or argument structure of the chapter;
- moving content from one section to another.

The document's paragraph order and argument flow are preserved. The skill has no technique that rearranges whole paragraphs or alters how the argument unfolds, and it must never invent one — doing so would break logical coherence and the reader's ability to follow the thesis.

What IS allowed (reporting-order variation within a unit): inside a single paragraph you may change the entry point and the order of its sentences — for example, open with the problem or the result before the background, instead of the AI-typical "background → purpose → method → result → conclusion" order. This is encouraged (T18, T14) and is how "reordering the argument's presentation" is achieved safely. What is NOT allowed: moving paragraphs around, changing which section makes which point, or altering the chapter's overall line of argument. Reorder the presentation inside a paragraph; never reorder the paragraphs or rewire the chapter.

### Principle 8 — Safe sentence splitting (no fragments, no choppy prose)

Splitting long sentences is a useful rhythm tool, but it must never produce grammatically incomplete fragments or a stop-start, half-sentence reading experience. Three failure modes are forbidden.

**Detection method — UNIVERSAL completeness test.**
A fragment may start with ANY word and be ANY length. Do not detect fragments by matching a fixed list of opening words ("Including / Drawing on / Using / Based on / Considering ..."), and do not look only at a short 3–7 word window. Those approaches are a known failure mode that misses real fragments such as "Work engagement, and creative inspiration.", "Workplace communities, and internal corporate channels.", "Promoting, and implementing new ideas.", and any long "Including ..." continuation.

Instead, for every unit ending in a period, ask:
- Does it have its OWN grammatical subject?
- Does it have its OWN finite (tensed) main verb — not just an `-ing` / `-ed` participle, not just a `to`-infinitive?
- Does it express a complete thought on its own?

If any answer is no, it is a fragment, regardless of its first word or its length.

Common types (illustrative, NOT a closed match-list):
- Subordinate-clause fragments: "When employees interact with AI in daily work." — must attach to a main clause.
- List/enumeration tails: "...the mediating roles of self-efficacy. Work engagement, and creative inspiration." / "...through online social platforms. Workplace communities, and internal corporate channels." / "...dependent variable. Gender, age...".
- Subject-less verb phrases: "...it raises the problem. Builds the theoretical model.".
- Gerund/participle continuations: "...statistical analysis. Including multivariate analysis, ..." / "...the model. Using SEM to test the paths." — `-ing` with no finite verb.
- Choppy mechanical chopping into many ~10-word units that creates a robotic stop-start rhythm.

Rules:
- A sentence may be split ONLY when both resulting parts independently pass the subject + finite-verb test. The safe split test: cover everything before the proposed period and read what remains; if it lacks its own subject or its own finite verb, do NOT split there.
- NEVER place a period inside a list, before "and X", before a bare verb phrase, before an "Including / Such as / For example ..." phrase, or before any `-ing`/`-ed` continuation. In every such case keep it as one sentence.
- After splitting, each piece must stand on its own and read aloud as a complete sentence.
- Prefer a natural mix of short, medium, and long sentences. As a guide, keep most sentences roughly 8–30 words; an occasional shorter sentence is fine for emphasis, but avoid three or more ultra-short sentences in a row.
- **Upper bound, too:** Do not over-correct into long, tangled sentences. Keep sentences at or under about 30 words and at most two subordinate clauses. A sentence that grows long or heavily nested during rewriting must be split into two complete sentences.
- If reducing rhythm uniformity would require creating a fragment, do NOT split — vary the rhythm another way (reorder clauses within the sentence, change the opening, recast voice) instead.
- Gate H (Phase 7) applies the universal completeness test to every period and is output-blocking.

### Principle 9 — Grammatical correctness and no jarring meta-commentary

Reducing the AI score must never introduce grammar errors or out-of-place asides. Two failure modes are forbidden:

**(a) Grammar errors.** The output must be correct academic English. In particular:
- Subject–verb agreement must hold (a singular subject takes a singular verb; a plural subject takes a plural verb). Rewriting that changes a subject from plural to singular (or splits a sentence) must update the verb to match.
- Tense, articles, prepositions, and pluralisation must remain correct.
- AI features must NEVER be reduced by deliberately inserting grammar mistakes or "non-native errors". Slight rhythmic plainness is fine; actual errors are not.
- Gate I (Phase 7) checks grammar, with special attention to subject–verb agreement at every point where a sentence was split, recast, or had its subject changed.

**(b) Jarring meta-commentary.** Do not insert sentences that explain, justify, or comment on the writing or the research design from outside the argument, such as:
- "This detail was included to improve measurement precision."
- "This sentence is added to clarify the logic."
- "The following paragraph explains the mechanism."
These read as abrupt logical jumps and look machine-inserted. Rules:
- Every sentence must follow from the surrounding content and advance the thesis's own argument.
- Researcher-trace sentences (T19) are permitted only when they express the author's genuine reasoning within the local argument and connect smoothly to the sentences before and after. They must never be generic justifications of methodology, measurement, or of the rewrite itself.
- A researcher-trace or transition sentence that does not connect logically to both its neighbours is a defect — remove it or rewrite it so the paragraph reads as one continuous line of reasoning.
- Gate J (Phase 7) checks for inserted meta-commentary and logic jumps.

### Chapter Version Ledger (required before every round)

Before starting any rewrite round, output and maintain this ledger. If the user cannot supply the previous ledger on a resumed task, rebuild it from the latest detector report before rewriting anything.

```text
| Chapter | Current measured score | Lowest-ever score | Source version of lowest | Current escalation rung | Tried techniques on this rung | Rounds done | Below target (<30%)? | This round: rewrite? |
|---------|------------------------|-------------------|--------------------------|-------------------------|-------------------------------|-------------|----------------------|----------------------|
| ...     | ...                    | ...               | ...                      | 1–6                     | e.g. T17, T21                 | int         | Yes / No             | Yes (target) / No    |
```

Rules:
- The "rewrite?" column should normally say Yes for exactly ONE chapter per round: the highest current measured chapter that is still at or above the target (default 30%). It may say Yes for two chapters only if the user explicitly requests a two-chapter batch and agrees to re-test each chapter separately.
- Any chapter already below the target (default 30%) is marked done and is not rewritten further.
- After a re-test, update the ledger: record the new score, update lowest-ever, update the escalation rung, and mark "Below target?" Yes/No. If a chapter regressed, restore the lowest-ever source and record the rollback.
- The task is complete only when every chapter shows "Below target? = Yes". As long as any chapter is still at or above target, name the next round's target only as a post-retest candidate and do not present the work as finished; do not plan detailed rewrite actions for that candidate until the user provides the re-test result for the current round.
- Never start a new round without an up-to-date ledger.



This skill is only for reducing AI-writing-risk patterns and AI detector scores.

It is not designed for plagiarism reduction, similarity-score reduction, citation rewriting, or Turnitin Similarity Index optimization.

If the user asks for similarity reduction or plagiarism reduction, treat it as a separate task and do not mix it with AI-rate reduction.

## Task Routing Rule

Before any diagnosis or rewriting, classify the user request and route it:

1. **Skill-Audit Mode** — the user asks to inspect THIS skill or its reference files for errors, contradictions, omissions, or optimisation. Skill Audit Mode is fully separate from Thesis Rewrite Mode: when the input files are SKILL.md or the reference modules, do NOT score them as thesis paragraphs and do NOT apply D1–D17 rewriting; audit them for internal consistency, routing completeness, safety boundaries, contradictions, missing execution gates, stale terminology, broken cross-references, and agent usability. Do NOT run thesis D1–D17 scoring and do NOT rewrite thesis text. Output rule-level problems, severity, affected files, suggested edits, and reasons, using this format:

   ```text
   Issue ID:
   File / Section:
   Problem type: contradiction / omission / ambiguity / execution burden / unsafe wording / terminology drift
   Original wording:
   Recommended replacement:
   Reason:
   Priority: High / Medium / Low
   ```

   When the user asks for “原文 + 修改后内容” (original + revised), a compact variant is acceptable: Issue ID / File-Section / Problem type / Original wording / Recommended replacement, adding Reason only where needed for clarity. If the user provides a custom audit loop or table format, follow the user's format while preserving the core fields (location, original wording, problem, suggested fix, reason/priority). Skill-Audit Mode still must not run thesis D1–D17 scoring or rewrite thesis text.
2. **AI-Writing-Risk Mode** — the user asks to reduce AI-writing risk / AI rate / AIGC traces / Turnitin-AI / CNKI-AIGC / GPTZero, etc. This is the main thesis workflow (Diagnosis-Only / Working / Quick / Single-Batch / Full Staged below).
3. **Similarity / Plagiarism Mode (out of scope)** — if the user asks for similarity reduction, plagiarism reduction, Turnitin Similarity Index, 查重, 相似度, or 降重 with NO AI-writing context, do not proceed under this skill. Ask whether they actually want AI-writing-risk reduction instead. This skill never optimises text-similarity / 查重 scores.
4. **Assembly Mode** — only after chapter-by-chapter accepted versions already exist and have been externally re-tested. Assembly means combining locked accepted chapter versions into a report or DOCX. It does NOT mean rewriting a whole thesis in one pass. The capability `assemble_locked_rewritten_document` refers ONLY to this assembly of already-accepted chapters (and single-chapter/batch output for the current round), never to one-pass whole-thesis rewriting.

## Language Routing Rule

- English thesis text: use D1–D17, the English cliché banks (Gate J), and the rewrite techniques.
- Chinese thesis text: use the Chinese-text AI-risk module (`references/chinese_text_ai_risk.md`) plus the structure-level checks; do NOT apply the Chinese-student-English cliché rules (those are for English text written by Chinese authors, not for Chinese text).
- Mixed Chinese–English thesis (e.g. English body + Chinese abstract/questionnaire): process by language segment, and protect bilingual term consistency (a term's Chinese and English forms must stay aligned).
- Method routing: apply the qualitative module (`references/qualitative_authorship_restoration.md`) and T25–T28 only to qualitative/mixed passages; do NOT apply qualitative researcher-voice techniques to a quantitative passage.
- Quotation-evidence protection (D21 and its Chinese-route equivalent): when a uniform-citation pattern is flagged, the default action is report-first. Before any rewrite planning, do NOT automatically change quotation count, quotation length, participant distribution, or theme coverage; only surrounding framing may be varied, and only where the existing analysis supports it (see detection_principles.md D21).
- Mixed-language paragraph: if a single paragraph contains both English and Chinese thesis prose, split it by language span where possible and score each span under its own route; protect bilingual technical terms, citations, and translated construct names before scoring, and never translate one span into the other language to unify the route.

For Chinese thesis text, the visible evidence must use the Chinese-route fields below (not a full English D1–D17 table):

```text
Paragraph ID:
Language Route: Chinese
Chinese AI-risk groups hit: template opening / template closing / unsupported intensifier / repeated phrase block / copula avoidance / causal-chain stacking / inflated importance / empty comparison / high-frequency AI vocabulary / term-abbreviation repetition / Chinese qualitative uniformity (if applicable)
Shared structure risks: paragraph architecture / section-template dependency / reporting-sequence regularity / external-highlight fragment
Protected elements:
Risk estimate: chinese_paragraph_risk_estimate (internal Chinese-text risk estimate only)
Rewrite action: minimal edit / no rewrite / author confirmation needed
```

## Task Mode Definitions

Mode routing summary (definitions below remain canonical; this table only consolidates them):

| Task type | Trigger | Mode | Evidence depth | Stop point |
|---|---|---|---|---|
| Audit this skill | User asks to inspect skill/workflow/reference files | Skill-Audit | Issue-level audit format (or user's custom format) | After issue list; never scores thesis |
| Inspect thesis without rewriting | inspect/review/audit thesis text | Diagnosis-Only | Route-appropriate scoring, no rewrite | After diagnosis report |
| One quick paragraph | Explicit quick request, or single paragraph with no files/scores | Quick | Minimum evidence set | After single-paragraph output |
| ≤10 selected paragraphs | Small selected batch, no full-document request | Single-Batch | Full evidence for those paragraphs | After batch output |
| Ordinary chapter revision | Default for normal thesis tasks | Working | Full evidence for target paragraphs; compact skip records otherwise | Stage 5 re-test stop |
| Long doc / DOCX / external report / >10 targets | Task Size Routing Rule | Full Staged | Staged full evidence | Stage 5 re-test stop per round |
| Full-evidence thesis audit | Explicit full-audit request | Thesis-Evidence Audit | Full tables for every included paragraph | After audit (no rewrite unless asked) |
| Combine accepted chapters | All chapters externally below target | Assembly | Assembly checks + DOCX gate | After assembled output |

Before execution, identify the task mode.

### Diagnosis-Only Mode
Use Diagnosis-Only Mode when the user asks to inspect, review, audit, identify risks, or list problems in thesis text without rewriting. If the user asks to inspect this skill, its workflow, or its reference files, use Skill-Audit Mode instead and do not run thesis D1–D17 scoring.

Rules:
- Do not rewrite thesis text.
- Output risk locations, reasons, severity, and suggested techniques only.
- Do not create a rewritten version unless the user explicitly asks for rewriting.

### Working Mode
Default mode for normal thesis revision.

Rules:
- Show full execution evidence for rewritten high-risk (target) paragraphs. For each rewritten target paragraph, show the minimum evidence packet: Paragraph ID; route; hit dimensions or Chinese-route risk groups; selected techniques; protected elements before/after; exact Pass 1–3 actions; Gate A–J summary; original/revised word count; candidate status pending external re-test.
- For low-risk or skipped paragraphs, give a compact skip record — paragraph ID, section type, final risk estimate, primary skip reason, and protected-element status — not a full D1–D17 table.
- Include protected-element result and quality-gate summary.
- Do not overload the user with full D1–D17 evidence for every paragraph unless necessary.

### Thesis-Evidence Audit Mode
Use this mode only when the user explicitly asks for full evidence, full audit, complete paragraph-level diagnosis, or detailed execution proof for THESIS TEXT. If the user asks to audit the skill file, workflow, or reference modules themselves, use Skill-Audit Mode instead. This mode controls evidence depth, not task size: a long task in this mode still follows Full Staged execution.

Rules:
- Show D1–D17 scoring.
- Show dimension-to-technique mapping.
- Show three-pass evidence.
- Show protected elements before and after rewriting.
- Show Gate A–J results for every rewritten paragraph or rewritten unit. Gates F–J are mandatory whenever text is rewritten, including quick single-paragraph mode.

### Quick Mode
Use Quick Mode when EITHER (a) the user explicitly asks for a quick rewrite/check or says “just this paragraph”, OR (b) the user provides only one paragraph, no uploaded thesis/chapter/DOCX/PDF detector report or external-score report, and no external detector score. An optional same-author style sample, the single source paragraph file, or one short paragraph-level detector excerpt does NOT disqualify Quick Mode, but the uploaded file role must be stated explicitly. A thesis chapter, full thesis, or external detector report DOES disqualify it.

When Quick Mode is inferred rather than explicitly requested (case b), state: “Scope = Quick single-paragraph mode; no chapter-level or document-level score is produced,” so the user can redirect.

Quick Mode Anti-Misrouting Rule: do NOT use Quick Mode when the request mentions "chapter", "section", "thesis", "paper", "DOCX", "external report", "CNKI", "Turnitin", "full text", "整章", "全文", "论文", "检测报告", or includes any uploaded long document — even if the user also says "quickly" / "简单看一下". Route those to Full Staged Mode or Single-Batch Mode by paragraph count and evidence availability.

Quick Mode still requires minimum evidence: scope statement; hit dimensions (or Chinese-route risk groups); selected techniques; protected-elements check; a one-line Gate A–J summary for the rewritten paragraph; and the statement that no chapter-level or document-level score is produced.

## Score Terminology Glossary

Use the following terms consistently.

- external_detector_score: the score reported by CNKI, Turnitin, GPTZero, Originality.ai, or another external detector.
- chapter_red_line: the lowest current measured external score for a chapter.
- raw_paragraph_risk: the internal D1–D17 weighted paragraph score before floors.
- paragraph_risk_index: the internal paragraph risk score after floors.
- overall_risk_index: the internal document-level risk estimate, not an external detector result.
- AI feature value: an external detector’s own reported value; record it as external evidence only.
- internal risk estimate: any score generated by this Skill without an external detector re-test.

Mandatory rule:
Internal scores help locate risk. They must not be presented as proof that an external detector score has decreased.



## Intent Confirmation Rule

Before starting Phase 1, check whether the user is asking for AI-writing-risk reduction or similarity/plagiarism reduction.

If the user mentions “Similarity Index,” “similarity,” “plagiarism,” “查重,” “相似度,” or “Turnitin Similarity,” respond with:

```text
This skill only reduces AI-writing-risk patterns. It does not optimize plagiarism, similarity score, or Turnitin Similarity Index. Please confirm whether you want to continue with AI-writing-risk reduction.
```

If the user provides an AI detector report, AIGC report, Turnitin AI report, CNKI AIGC report, GPTZero report, or Originality.ai report, continue with AI-writing-risk reduction.

---



## Triggers

- "降AI" / "降低AI率" / "降低AIGC检测率"
- "AI detection" / "reduce AI score" / "lower AI rate"
- "改写降AI" / "去AI痕迹" / "AI痕迹检测"
- Uploading an English academic paper with AIGC reduction intent
- User reports a mismatch between internal AI score and Turnitin/GPTZero/Originality.ai score

These triggers route the task to academic-integrity-preserving risk-pattern revision — not detector evasion, fabricated humanisation, or plagiarism/similarity manipulation. The skill reduces shared AI-writing risk patterns by minimal edits to the author's own text; it never bypasses detectors, fabricates content, or routes text through external rewriting services.


## Universal AI-Feature Reduction Rule

This skill aims to reduce AI-writing features that are commonly sensitive across different AI detection systems.

It does not optimize for one detector. External detector reports are used only as evidence for locating risk areas.

The core reduction targets are:

1. repeated academic templates;
2. repeated paragraph function paths;
3. mechanical methodology and empirical reporting;
4. predictable reporting sequences;
5. uniform sentence rhythm and low burstiness;
6. over-smooth reasoning chains;
7. continuous AI-like fragments in abstract/introduction;
8. repeated hypothesis-development routes;
9. repeated result → implication loops in discussion or conclusion;
10. lack of human research judgment, boundary, decision trace, or process narration.

Mandatory rule:
- Convert detector-specific findings into shared risk categories before rewriting.
- Select rewrite techniques according to risk category, not detector name.
- Use section-level rewriting when the risk appears across paragraph groups.
- Do not rely on synonym replacement, random short sentences, or general polishing.
- Preserve all protected elements, including citations, variables, hypotheses, coefficients, p-values, model names, table numbers, and statistical conclusions.

### Validated Researcher-Trace Rule

Validated finding:
- In prior task testing, researcher-view judgment sentences and process narration appeared useful for some descriptive, overly smooth, abstract, or mechanically explanatory paragraphs. Treat this as a conditional strategy, not a universal fix.

Mandatory rule:
- This strategy must be treated as a formal Phase 4 rewrite strategy.
- T19 = source-extracted relocation ONLY: it may move, split, or lightly rephrase researcher-side judgment/process/boundary material that ALREADY EXISTS in the thesis. If a sentence is newly COMPOSED from existing thesis facts rather than relocated, classify it as T29 (evidence-based reconstruction), not T19. Either way a completed Source Trace block is required; if no source can be identified, do not write the sentence.
- It should be marked as a High-Efficiency Strategy.
- Use this strategy only when the added sentence can be directly grounded in existing thesis content. Do not insert researcher-trace sentences into statistical-result paragraphs unless the sentence is tied to the reported table, coefficient, sample, model, measurement choice, or stated finding.
- The added sentence must be based on existing thesis content. It must not introduce new data, new theory, new references, or unsupported examples.


## Project-Level Working Structure

For long thesis documents, use a two-level working structure:

1. Master overview
   - thesis title, chapter structure, total paragraph count
   - current external AI detector result if available, including detector name, score type, score value, and highlighted section evidence
   - document-level AI risk summary
   - high-risk sections and rewrite priority
   - chapter status matrix

2. Chapter task notes
   - section type
   - detected AI patterns
   - paragraph-level risk points
   - rewrite strategy
   - completion status

This structure is especially useful when the thesis has more than 50 pages or when any external AI detector score is above 30%.

Mandatory project-state rule:
- If the task involves multiple chapters, update the Master Overview after each completed round's Stage 4 final output and before the Stage 5 mandatory re-test stop. Do not use "Stage 4" to mean "Phase 4": Stage 4 is the round-level final-output stage, while Phase 4 is target selection / prioritisation. Execution order is locked — the Phase workflow runs inside the round first, then the Stage output. A task may not jump from Phase 7 quality gates directly to Done; it must pass Stage 4 scope-aware output and then the Stage 5 external re-test stop, unless the user explicitly selected Quick Mode with no detector-score objective.

Terminology Rule: `Phase` denotes the executable workflow steps and is the ONLY control of execution order; `Stage` is a user-facing summary grouping and must never override, skip, or reorder Phase execution. Mapping: user-facing Stage 1 = Phase 1–3; Stage 2 = Phase 4–5.5; Stage 3 = Phase 7; Stage 4 = Phase 8–9; Stage 5 = the external re-test checkpoint.
- The Master Overview must include chapter status, completed batches, remaining high-risk sections, baseline version, latest external score, and next recommended batch.
- At the start of a resumed task, use the Master Overview as the recovery context.



## Global D1–D17 Consistency Override Rule

This skill uses a formal D1–D17 core scoring system for general and quantitative AI-trace risk, plus the qualitative-only supplement D18–D21 for qualitative and mixed-methods papers.

All references to “15 dimensions,” “D1–D15 coverage,” or “42.0 total score” must be treated as outdated unless explicitly marked as historical notes.

Current scoring system:
- For English-route thesis text, D1–D17 must be evaluated for every included body paragraph in the current target chapter or selected rewrite batch. For Chinese-route thesis text, do not force the English D1–D17 table; use the Chinese-route evidence template plus shared structure-level checks. For mixed-language documents, apply the required route separately by language segment. "Included body paragraph" does not mean every paragraph in the whole thesis unless the user explicitly requests full-document diagnosis.
- Total possible dimension score = 49.0.
- raw_paragraph_risk = min(dimension_score / 49.0, 1.0) × 100%.
- Phase 2 is incomplete if D16 or D17 is missing.
- Public evidence is incomplete if the Detection Report does not show the required route-specific scoring evidence: English-route paragraphs require D1–D17 scores; Chinese-route paragraphs require the Chinese-route evidence template plus shared structure checks; qualitative or mixed-methods passages require the applicable D18–D21 supplement or its Chinese-route adaptation.
- D12, D13, D14, D15, D16, and D17 must always be checked manually or semi-manually.

If any rule conflicts with this 17-dimension system, the 17-dimension rule overrides the older 15-dimension wording.

## Score Regression Guard

Before rewriting, identify the current lowest external AI-score version as the baseline version, using the Chapter Version Ledger (see Core Operating Architecture).

If multiple rewritten versions exist, do not assume the newest version is better. Use the version with the lower external detector score as the working baseline. This applies per chapter, not only to the whole document — keep the lowest-scoring version of EACH chapter.

For long thesis documents, do not rewrite the whole document before testing a small batch. Rewrite one chapter, re-test it, then continue (Principle 1).

Recommended process:

1. Build/refresh the Chapter Version Ledger and identify each chapter's lowest-ever version.
2. Target-lock the highest current measured chapter that is still at or above the target (default 30%); skip any chapter already below target.
3. Diagnose their D1–D17 risk dimensions.
4. Rewrite only those chapters by minimal edit (never regeneration).
5. Run protected elements check.
6. Run Phase 7 quality gate.
7. STOP and have the user re-test the rewritten chapter with the external detector.
8. After a comparable external re-test, handle the chapter by status:
   - If the score is below the target threshold: mark the chapter DONE and lock that version within the named detector stream and scope.
   - If the score decreased but remains at or above the target: record it as PROGRESS, set it as the new lowest-score baseline for that chapter, and plan the next escalation rung for the same chapter. A decrease that is still above target is progress, not completion.
   - If the score stayed the same or increased: mark the candidate rejected, roll back to the chapter's lowest-ever version, diagnose the failed rewrite direction, and redesign the next small-batch strategy.

Mandatory rule:
- A chapter's current measured external score is a RED LINE. A rewrite must be treated as provisional until the user provides an external re-test result. If the re-test does not measurably lower the score, discard the rewrite and restore the chapter’s lowest-ever external-score version.
- If Version A has a lower external AI score than Version B, continue from Version A unless there is a clear academic-quality reason not to.
- Do not continue rewriting from a version that increased the external AI score.
- If a sample rewrite increases AI risk, stop and redesign the rewrite strategy.
- If the external AI score increases after a rewrite, return to the lower-score baseline version of that chapter.
- Score increase triggers the same action path: roll back to the chapter's lowest-ever version → diagnose failed rewrite direction → redesign strategy → retest with a small batch.
- Stalemate vs Rewrite Fatigue (two separate thresholds; Rewrite Fatigue Pause overrides Stalemate Warning): Stalemate Warning fires at <5 percentage points change across two consecutive comparable re-test rounds — mark the strategy stale and plan the next rung, but do NOT auto-pause. Rewrite Fatigue Pause fires at <3 percentage points change across two consecutive rounds, or once three complete rewrite+re-test rounds are done on the chapter — mark the unit Paused unless a clearly untried lower-risk technique remains. Stalemate handling: if a chapter changes by less than 5 percentage points across two consecutive comparable re-test rounds, mark the current strategy as stale, keep the lowest-score version, and plan the next round at the next escalation rung. If the next rung stays intra-paragraph and preserves all structural boundaries, user confirmation is not required beyond the normal external re-test checkpoint. If the next rung would require broader structural reorganisation beyond the current approved unit, ask for user confirmation before execution.

Reference Availability Check: before execution, confirm the four reference modules (`references/detection_principles.md`, `references/rewrite_methods.md`, `references/qualitative_authorship_restoration.md`, `references/chinese_text_ai_risk.md`) are readable. If any module is missing or unreadable, mark the run "Partial Execution — reference module unavailable", name the missing module, do not produce final scoring that depends on it, and continue only with the parts that remain fully supported.

Reference Path Rule: in packaged skill distribution, load reference files from `references/`. If the skill is instead being audited from uploaded standalone files, match by canonical basename first (`detection_principles`, `rewrite_methods`, `qualitative_authorship_restoration`, `chinese_text_ai_risk`) and ignore upload suffixes such as `(15)` or copy markers.

Score Terminology Glossary: external_detector_score = the score reported by CNKI, Turnitin, GPTZero, Originality.ai, or another external detector. chapter_red_line = the lowest current measured external score for a chapter. raw_paragraph_risk = the internal D1–D17 weighted score before floors. paragraph_risk_index = the internal paragraph risk score after floors. scope_risk_index = the internal risk estimate computed over whatever scope was diagnosed; it is reported as overall_risk_index only for a fully diagnosed full-document scope (otherwise as target_chapter_risk_index / batch_risk_index / fragment_risk_index), and is never an external detector result. AI feature value = an external detector’s own reported value and should be recorded as external evidence only. Priority notation rule: use either A/B/C/D or P0/P1/P2/P3 within one report, not both; if legacy notation appears, the mapping is exactly A=P0, B=P1, C=P2, D=P3.

## Target Status State Machine

Every chapter/target-unit's status at the end of a round is reported as exactly ONE of these six labels: Done / Progress / Rejected / Paused / Blocked / Incomplete. Rejected means a comparable re-test regressed or failed to improve against the red line, so the candidate is discarded and the lowest-ever version remains the baseline. `Partial Execution` is NOT a seventh target-unit status: it is a run-level execution label used only when one or more required reference modules are unavailable. When it applies, the affected target-unit status is Incomplete (unless the missing module is irrelevant to the selected route), and the run must name the missing module and which scoring/rewriting functions were skipped. This is a reporting layer over the existing stop-logic (Principle 0 pause reasons, Rewrite Fatigue Detection, Score Regression Guard); it changes none of those rules, it only standardises how the outcome is named so a unit is never ambiguously "stuck".

- **Done** — the unit's latest COMPARABLE external re-test is below target (default <30%). Only an externally-confirmed below-target unit may be Done. An internal estimate alone can never mark Done.
- **Progress** — the latest comparable re-test decreased versus the chapter red line but is still ≥ target. Continue next round (move up the escalation ladder if <3pp gain).
- **Rejected** — a comparable re-test regressed (higher than the red line) or did not improve against it. Discard the candidate, keep the lowest-ever comparable version as the baseline, diagnose the failed rewrite direction, and escalate one rung on the next round after recording the rollback. A regression is never reported as Progress.
- **Paused** — work is intentionally halted for a legitimate Principle 0 reason (user asked to stop; Rewrite Fatigue triggered; full escalation ladder exhausted and the blocking constraint reported; continuing would risk protected content or readability). A Paused unit may be ≥ target — Paused is the correct label for "above target but should not keep grinding right now". Record the specific pause reason.
- **Blocked** — cannot proceed because a required input is missing: no comparable external re-test available, external evidence incomplete, or detector streams not comparable. Record what is needed to unblock. Do NOT update chapter_red_line while Blocked.
- **Incomplete** — a round was started but its quality gates (A–J) or protected-element checks did not pass, so no acceptable version was produced this round. Roll back to the lowest-ever version and report what failed.

Failure handling summary (condition → status → required action):

| Failure condition | Status | Required action |
|---|---|---|
| Comparable re-test shows regression (higher than red line), or no improvement against the red line | Rejected / Rollback | Discard the candidate; keep the lowest-ever comparable version as baseline; diagnose the failed rewrite direction; escalate one rung only after the rollback is recorded. Do not mark this as Progress |
| Gate A–J or protected-element failure | Incomplete | Roll back to lowest-ever version; report which gate failed; rework before any new round |
| No comparable external evidence / detector streams not comparable | Blocked | Record what is needed to unblock; no red-line update; internal work only with explicit user acceptance |
| Integrity/readability risk, Rewrite Fatigue, ladder exhausted, or user stop | Paused | Record the specific reason; keep lowest-ever version; resume only on user instruction |
| Reference module unavailable | Partial Execution | Name the missing module; no final scoring that depends on it |

Rule: a unit at or above target is NEVER reported as Done. It is Progress, Paused, or Blocked. This removes the old "can't stop above 30% but also can't continue" deadlock — above-target units that should stop are simply Paused or Blocked, with a reason.

## Universal External-Risk Calibration Rule

This skill does not optimize for one specific AI detector.

When one or more external AI detector reports are provided, the reports must be used as risk-location evidence, not as detector-specific rewriting instructions.

The purpose is to reduce shared AI-writing features that may be detected across different AI detection systems.

Common cross-detector AI-risk features include:

- long continuous AI-like fragments;
- repeated chapter-level or section-level templates;
- repeated paragraph function paths;
- mechanical methodology reporting;
- mechanical empirical-result reporting;
- predictable reporting sequences;
- uniform sentence rhythm and low burstiness;
- over-smooth academic reasoning;
- polished claim → explanation → implication chains;
- repeated hypothesis-development routes;
- repeated result → implication loops in discussion or conclusion;
- lack of human research judgment, boundary, decision trace, or process narration.

Mandatory rule:
- Do not optimize for CNKI, Turnitin, GPTZero, Originality.ai, or any single detector.
- Convert detector-specific findings into shared AI-risk categories before rewriting.
- Select rewrite techniques according to risk category, not detector name.
- If different detectors highlight different sections, treat them as complementary evidence of different AI-risk dimensions.
- If any external detector reports a much higher AI risk than the internal score, raise the internal priority level and inspect section-level structure before rewriting.
- Internal low scores cannot override external high-risk evidence.
- Rewriting must target structure, rhythm, reporting sequence, and section architecture, not only vocabulary.


## Default-Excluded Units

Unless the user explicitly asks otherwise, the following are NOT rewritten, NOT scored against D1–D17, NOT used for word-count compensation, NOT moved or reordered, and should be excluded when defining the external re-test scope so that before/after comparisons stay consistent:

- references / bibliography
- appendices
- questionnaires and survey instruments
- ethics statements / consent forms
- title page and declaration page
- table of contents
- figure and table captions (unless an external report specifically flags one)
- verbatim participant quotes (unless the task is qualitative quote-balance diagnosis)
- equations, formula numbers, and table cell values

If the user asks to include any of these, record the change explicitly and apply the same inclusion in the external re-test scope.

## Non-Comparable Detector Handling

External scores are comparable only when they come from the same detector, the same document version, and the same included scope. When detector streams are NOT comparable (different detector, different version, or different included/excluded sections):

- Do not judge regression or improvement between them, and do not treat e.g. Turnitin 48% and CNKI 32% as an up/down relationship.
- Build separate evidence streams, one per detector.
- Use only overlapping highlighted sections for priority selection.
- Label the output "External Comparison Not Available" and set affected units' external-comparison status to Blocked. Internal diagnosis or candidate rewriting may still proceed only if the user explicitly accepts that no external score-improvement claim can be made for this round.
- Do NOT update chapter_red_line unless a comparable re-test exists.

## External Test Scope Sheet

When an external detector result is used, record its scope so a later re-test is comparable. If a field is unknown, mark it Unknown rather than guessing:

```text
external_test_scope:
  detector_name:        # e.g. Turnitin / CNKI / GPTZero
  date:
  detector_version:     # or Unknown
  included_sections:    # e.g. ch1-ch5 body
  excluded_sections:    # e.g. references, appendices
  references_included:  # yes / no / Unknown
  appendix_included:    # yes / no / Unknown
  file_format:          # docx / pdf / pasted text
  chapter_extraction_method:  # how chapters were separated
```

A re-test counts as "comparable" only when detector_name, detector_version, and the included/excluded scope match the baseline. Otherwise treat it under Non-Comparable Detector Handling.

## DOCX Output Gate

When output is a .docx (Assembly Mode or single-chapter document), in addition to Gates A–J:

- Paragraph and heading styles are preserved; heading levels are unchanged.
- Tables, figures, equations, footnotes, endnotes, headers/footers are untouched unless the user asked for them to be revised.
- Reference list and in-text citation fields are locked (no reordering, reformatting, or renumbering).
- Track-changes / comments handling is stated explicitly (kept, accepted, removed, or unsupported by the current output method) — never silently altered.
- Format-preservation fallback: if the output method cannot safely preserve track changes, comments, citation fields, tables, footnotes, headers/footers, equations, or complex styles, do NOT mark the .docx as final. Default to delivering a text-only revised chapter for manual insertion. Produce a candidate .docx labelled `format-not-verified` only when the user explicitly requests a file despite the limitation — never a locked final version. In both cases attach the DOCX limitation note and keep the rewritten scope limited to the approved chapter or batch.
- Default-Excluded Units above remain unchanged in the output file.
- The rewrite covers only the current approved chapter/batch; a whole-thesis one-pass rewrite is not produced (see Task Routing — Assembly Mode).
- Output hygiene (the delivered file must be clean, faithfully rendered prose — these checks are about the file, not the rewriting, and never license changing content):
  - No unresolved draft markers or placeholders survive in the delivered thesis body, headings, captions, footnotes, comments intended for removal, or visible fields: `TODO`, `TBD`, `FIXME`, `??`, `[[`, `]]`, empty bracketed fields, `[insert]`, `[variable]`, lorem ipsum, or placeholder ellipses standing in for missing content.
  - No leaked raw markup or control tokens render as literal text: stray Markdown table pipes, unrendered Markdown/LaTeX commands (e.g. `\textbf{...}`, `\cite{...}`, `\section{...}`), unresolved citation markers like `[@key]`, or a broken cross-reference shown as `[?]`. The visible text must read as finished prose.
  - Chinese encoding integrity: export as UTF-8 and confirm Chinese characters render correctly, with no mojibake or garbled byte runs (the classic failure is GBK text decoded as UTF-8). For a bilingual or Chinese thesis this check is mandatory before the file is treated as final.

## File Naming Convention

When producing versioned files across rounds, name them so baselines, candidates, and locked re-tests are unambiguous:

```text
<Unit>_v<NN>_baseline_<score-or-Unknown>_<scope>.docx   e.g. Chapter3_v03_baseline_36pct_CNKI.docx or Chapter3_v03_baseline_Unknown_internal.docx (add detector/scope when external scores are used)
<Unit>_v<NN>_candidate_rung<N>.docx        e.g. Chapter3_v04_candidate_rung2.docx
<Unit>_v<NN>_retest_<score>_locked_<detector-or-scope>.docx   e.g. Chapter3_v04_retest_28pct_locked_CNKI.docx
```

The "_locked" suffix marks a version confirmed below target by a comparable external re-test within the NAMED detector stream and scope (status Done). A version locked under one detector stream is not automatically locked under another stream. Use "Unknown" in place of a score when no comparable external score exists yet.

## External Highlight First Rule

When an external detector report is provided, the externally highlighted or high-risk sections must be reviewed before internal paragraph rewriting.

Workflow:

1. Extract high-risk sections from external detector reports.
2. Convert detector-specific findings into shared AI-risk categories.
3. Build the External Risk Convergence Map.
4. Select P0 and P1 sections.
5. Rewrite P0/P1 sections in batches.
6. Run internal D1–D17 scoring to explain and guide the rewrite, not to override external evidence.

Mandatory rule:
- Internal low scores cannot override external high-risk evidence.
- If an external detector highlights or reports a long high-risk section, treat it as high-risk even if paragraph_risk_index is low.
- The rewrite unit should be sentence, paragraph, paragraph group, subsection, or chapter segment depending on the risk pattern.

## External Score Extraction Rule

When the user provides an external detector result in any informal format, extract and standardize the detector name and score before Phase 1.
Detector names are recorded for source tracking only. They must not create detector-specific rewrite strategies.

Detector-specific prioritisation vs detector-agnostic technique (general rule): it is allowed to use which detector reported the risk, and known detector tendencies (e.g. CNKI weighting the document opening, the small-sample observation that Chinese MBA conclusion chapters run higher), to decide WHERE to look first and WHAT to rewrite first. It is NOT allowed to change HOW a passage is rewritten based on the detector — the rewrite techniques (minimal edit, de-templating, term protection, no fabrication) are identical regardless of which detector is in play. Prioritisation may be detector-informed; technique stays detector-agnostic.

Accepted formats include:

- “Turnitin says 48%”
- “Turnitin AI = 48%”
- “AI rate 0.48”
- “知网AIGC 49.9%”
- “CNKI AI feature value 49.9%”
- uploaded detector PDF report

Standardize as:

```text
external_detector:
external_score:
external_score_type:
report_available: Yes / No
```

Examples:

external_detector: Turnitin
external_score: 67%
external_score_type: AI Writing
report_available: Yes
external_detector: CNKI
external_score: 49.9%
external_score_type: AIGC AI feature value
report_available: Yes

Mandatory rule:

- External detector scores must be extracted before internal scoring.
- Informal user-provided detector scores must not be ignored.
- External scores must be used in Score Regression Guard and Universal External-Risk Calibration Rule.

### Comparable external re-test rule (required for any score comparison)

A "comparable external re-test" is a re-test run with the SAME detector, the SAME tested scope, the SAME inclusion/exclusion settings, and a materially comparable document version.
- A regression/improvement judgment (red line, lowest-ever, "did it go down?") may ONLY be made against a comparable external re-test.
- Scores from DIFFERENT detectors (e.g. Turnitin 48% vs CNKI 32%) are separate evidence streams. Report them side by side; never treat one as a rise or fall relative to the other.
- Scope consistency: a chapter-level score may only be compared with a later chapter-level score from the same chapter scope; a whole-document score only with a later whole-document score under comparable settings. A chapter-only score is never evidence that the whole thesis improved.
- If the detector cannot re-test a single chapter, fix one substitute scope before round 1 and keep it unchanged: either re-test the whole document after each accepted chapter revision, or re-test an identically extracted chapter file with unchanged formatting/inclusion settings.
- The 70%-of-external calibration floor applies ONLY when diagnosing the same pre-rewrite version that produced that external score. For a revised candidate, report an internal risk estimate only and state that external improvement is unverified until a comparable re-test is run.

### Scope-labelling rule (do not inflate a chapter score into a document score)

- If all body paragraphs of the document are included, you may report `overall_document_internal_risk_estimate`.
- If only a chapter, batch, or highlighted fragment is included, report `target_unit_internal_risk_estimate` and do NOT label it a document-level score.
- Phase 8/9 must state Scope = Full document / Target chapter / Selected batch / Highlighted fragment. Only Scope = Full document may produce a document-level estimate.

---


## No External Detector Score Rule

If no external detector score is available:

- Do not create an exact external chapter-red-line ledger. An Internal Planning Ledger with scores marked Unknown / internal risk estimate only MAY be created, but it must never be treated as an external baseline or as proof of detector improvement.
- Do not claim that the rewrite has lowered the external detector score.
- Use internal D1–D17 scoring only as a risk-location estimate.
- Mark all scores as “internal risk estimate only.”
- Recommend external re-testing after rewriting.
- Verbally-stated score, no report: if the user only mentions a number (e.g. "Turnitin says 48%") but uploads no actual detector report, treat that number as a calibration signal only (it may inform the 70% calibration floor and overall prioritisation). It does NOT establish any "externally highlighted section" — without a real report there are no highlighted ranges to apply External Highlight First to, so do not claim or invent highlighted sections, do not add External Risk Convergence Map entries based on invented ranges, and select targets by internal risk instead. It may trigger stricter internal prioritisation and an Internal Planning Ledger only. If the user later uploads the detector report, rebuild the External Risk Convergence Map from the report before rewriting.
- No External-Result Claim Rule: if no comparable external re-test result is available for the revised version, never write "AI score reduced", "AI rate lowered", "detector score improved", "will pass Turnitin/CNKI", or similar. Use only "internal risk estimate reduced", "risk patterns addressed", or "candidate version prepared for external re-test".
- If the user later provides an external detector score, rebuild the Chapter Version Ledger from that score before the next rewrite round.

---
## Task Size Routing Rule

Before execution, decide whether the task should use Quick Mode, Single-Batch Mode, or Full Staged Mode.

| Task Type | Criteria | Execution Mode |
|---|---|---|
| Quick Mode | User asks for (or single-paragraph input implies) a quick single-paragraph rewrite/check; no thesis chapter/full thesis/DOCX/PDF/report uploaded (an optional author-style sample, the single source paragraph, or one short paragraph-level detector excerpt does NOT disqualify); no external detector score/report; target text ≤1 paragraph | Simplified single-paragraph workflow |
| Single-Batch Mode | Selected rewrite paragraphs ≤10 and no full-document rewrite is requested | Diagnosis + rewrite + quality gate may be completed in one response for those ≤10 paragraphs, all evidence must still be shown, and it must NOT be described as a whole-thesis rewrite. If more than 10 paragraphs are provided, route to Full Staged Mode even if the first response processes only one batch |
| Full Staged Mode | Long document, DOCX/PDF, external detector report, more than 10 paragraphs, or external-detector-high task, including any external AI detector report with high-risk sections, highlighted fragments, or high overall AI-risk scores | Mandatory staged execution |

Mandatory rule:
- If more than 10 paragraphs are involved, use Full Staged Mode.
- If an external detector report is provided, use Full Staged Mode unless the user explicitly asks to inspect only one paragraph.
- Single-Batch Mode does not remove evidence requirements. Phase 4.5, Phase 5.5, and Phase 7 evidence must still be visible.

If no external detector score is available, do not create an exact chapter red-line ledger. Use internal D1–D17 scoring only as a risk-location estimate. Mark all scores as "internal risk estimate only." Recommend external re-testing, but do not claim that the rewrite has lowered the detector score.

---

## Definition of included body paragraphs: 
In Full Staged Mode, included body paragraphs are the paragraphs inside the current target chapter, selected external-highlighted section, or selected rewrite batch. Low-risk paragraphs outside the current batch may be recorded by section-level summary and do not require full visible D1–D17 evidence in that round.


---

## Practical Long-Document Execution Rule

For documents with more than 80 body paragraphs, staged, batch-based execution is mandatory; do not attempt full-document paragraph-by-paragraph diagnosis or rewriting in one response. (For more than 50 body paragraphs, staged or batch output is recommended and compact skip records may be used for low-risk or non-target paragraphs.)

Stage 1 may use a full-document structural scan plus full D1-D17 scoring for the following priority units:

- externally highlighted paragraphs or fragments;
- the first 20% of the thesis;
- methodology, empirical results, discussion, and conclusion sections with template-like reporting patterns;
- repeated paragraph clusters detected across literature review, hypothesis development, methodology, or empirical reporting sections.

Low-risk paragraphs may be recorded through a section-level summary when they are not externally highlighted and do not belong to a repeated structure cluster.

However, any paragraph selected for rewriting must still receive:
- full D1-D17 scoring;
- paragraph_risk_index calculation;
- priority classification;
- selected rewrite techniques;
- protected elements check;
- paragraph-specific rewrite evidence;
- Phase 7 quality-gate result.

This rule does not weaken the D1-D17 requirement for rewritten paragraphs. It only prevents impractical full-document evidence output for low-risk paragraphs in long thesis projects.

---

## Batch Processing Rule

For long documents, process rewritten paragraphs in manageable batches.

Recommended batch size:
- 3–5 fragment clusters for externally highlighted severe-risk sections;
- 5–10 paragraphs for severe-risk sections;
- 10–15 paragraphs for standard high-risk sections.

Batch processing is allowed only after the task has been routed by the Task Size Routing Rule.

Do not claim full completion until all selected A/B priority paragraphs have been processed.

If the task is too large for one response, output:
Batch Completed — Remaining Paragraphs Pending

The next response must resume from the next unprocessed paragraph group.


## External Risk Convergence Map Rule

When one or more external detector reports are available, paragraph triage must be based on both internal D1–D17 scoring and external risk evidence.

Create an External Risk Convergence Map before paragraph-level rewriting.

For each section, record:

```text
Section name:
External risk evidence:
Affected fragment or paragraph group:
Shared AI-risk category:
Continuous fragment risk:
Rewrite unit:
Priority:
Protected elements:
```

Shared AI-risk categories include:

- sentence-level phrase template;
- paragraph-level template structure;
- cross-paragraph sequence repetition;
- methodology/reporting template;
- uniform rhythm / low burstiness;
- over-smooth reasoning chain;
- repeated hypothesis-development route;
- conclusion/result-implication loop;
- lack of human research trace.

Mandatory rule:

- If a section has high external detector risk, do not rely only on paragraph_risk_index.
- The rewrite unit may be planned as a fragment cluster, paragraph group, subsection, or chapter segment when the risk is continuous — but this is a DIAGNOSIS and PLANNING unit only. The OUTPUT must keep every original paragraph as a separate paragraph and every heading on its own line. Never merge paragraphs or cross a heading when applying the plan (Principle 6).
- Cross-paragraph repetition is reduced by DIFFERENTIATING the paragraphs in the group (different entry point, order, and function for each), not by combining them into one block.
- Low-risk paragraphs inside a high-risk section may still require structural adjustment if they contribute to repeated section architecture.

Chapter-level status has priority over paragraph-level classification. If a chapter is already below the target (default 30%), it is done: its A/B/C/D paragraph labels may be recorded for diagnosis, but they must not trigger further AI-reduction rewriting. A chapter at or above target is never exempt.


Rewrite Unit Decision Rule: Use sentence-level edits for isolated phrase risk; paragraph-level edits for single-paragraph template risk; fragment-cluster edits for continuous external highlights; paragraph-group edits for repeated cross-paragraph architecture; subsection-level edits for methodology or empirical-reporting templates; chapter-level planning only when the whole chapter has high external risk. Do not use a larger rewrite unit than the risk requires.



## Rewrite Unit Decision Rule

Use the smallest rewrite unit that can address the detected risk.

| Risk Type | Rewrite Unit (planning) |
|---|---|
| Isolated phrase or transition risk | Sentence |
| Single paragraph template risk | Paragraph |
| Continuous external highlighted fragment | Fragment cluster (plan only — output stays as separate paragraphs) |
| Several neighboring paragraphs with same function | Paragraph group (plan only — differentiate, do not merge) |
| Methodology or empirical reporting template | Subsection (plan only — keep all paragraph breaks and headings) |
| Whole chapter with high external risk | Chapter-level plan, executed paragraph by paragraph |

Mandatory rules:
- Do not use a larger rewrite unit than the risk requires.
- Do not rewrite a whole chapter as newly generated prose.
- Chapter-level rewriting means chapter-level planning and paragraph differentiation, not full chapter regeneration.
- "Fragment cluster", "paragraph group", "subsection", and "chapter segment" are PLANNING units only. In the OUTPUT, every original paragraph stays a separate paragraph and every heading stays on its own line. Never merge paragraphs and never cross a heading boundary (Principle 6, Gate G).
- No rewritten paragraph may exceed 200 words or 12 sentences (Gate G). If risk reduction seems to need a longer block, keep the original paragraph breaks instead.

## Paragraph Triage Rule

All included body paragraphs must be diagnosed, but not all paragraphs need the same rewrite depth.
Triage must be based on full D1-D17 scoring, not on partial automated scoring.

A paragraph cannot be classified as A/B/C/D until:
- all 17 dimensions are scored;
- pattern_floor is checked;
- repeated_structure_floor is checked;
- section_template_floor is checked;
- D16/D17 trigger floor is checked.

Before rewriting, classify every paragraph into one of four priority groups:

| Group | Criteria | Required Action |
|---|---|---|
| A: Critical | paragraph_risk_index ≥40%, externally highlighted, strong D12/D13/D15 risk, or D16 ≥2.5 / D17 ≥2.5 | Full Phase 4.5 + Phase 5 + Phase 5.5 + Phase 7 evidence required |
| B: High | paragraph_risk_index 21–39%, or repeated section-template risk | Full Phase 4.5 + Phase 5 + Phase 5.5 + Phase 7 evidence required if rewritten |
| C: Medium | paragraph_risk_index 10–20%, or located in a high-risk section but not individually severe | Diagnosis required; rewrite only if it contributes to repeated structure |
| D: Low | paragraph_risk_index <10% and no repeated structure | Record in Detection Report; no rewrite required |

Mandatory rule:
- Every included paragraph must appear in the Detection Report.
- A-class paragraphs inside the current target chapter (or selected rewrite unit) must normally be rewritten. A-class paragraphs OUTSIDE the current round are queued for a later round and explicitly marked "not rewritten this round due to target-lock rule" — this is not a workload excuse but the single-chapter closed-loop rule. If an in-scope A-class paragraph is not rewritten, the report must give a specific academic-integrity reason.
- Only rewritten paragraphs require full Phase 4.5, Phase 5.5, and Phase 7 paragraph-level evidence.
- Low-risk paragraphs must not be rewritten merely for polishing.
- If a paragraph is skipped, the report must state the reason: Low risk / No repeated structure / Not externally highlighted / Preserved for academic accuracy.

## Parallel Hypothesis Differentiation Rule

When several hypotheses are developed in parallel, the rewrite must not only change wording. Each hypothesis paragraph must use a different reasoning route.

High-risk pattern:
variable A affects mediator X → mediator X affects outcome Y → hypothesis proposed
variable A affects mediator Z → mediator Z affects outcome Y → hypothesis proposed

Required differentiation:
- One hypothesis may enter from a cognitive mechanism.
- One hypothesis may enter from emotional or motivational involvement.
- One hypothesis may enter from information processing or idea generation.
- One hypothesis may enter from organizational boundary conditions.
- One hypothesis may begin from the dependent variable problem rather than the independent variable.

Mandatory rule:
- In a parallel hypothesis group, at least three paragraphs must have different opening logic.
- At least one paragraph must change internal order.
- Do NOT end every hypothesis paragraph with the same cue phrase. Repeated closings such as "the following hypothesis is put forward", "Based on this logic, ... the following hypothesis is put forward", "On this basis, ... the following hypothesis is put forward", or "therefore, the following hypothesis is proposed" appearing across most hypotheses are a strong template signal — vary or drop them. A direct form ("Therefore, H1 is proposed: ...") used in some paragraphs and a differently-phrased lead-in in others is better than one fixed cue everywhere.
- Watch the seam bug this cue creates: a sentence like "...is expected to have a positive effect on innovative behavior. the following hypothesis is put forward:" has BOTH a stranded fragment AND a lower-case sentence start. Recast it into one grammatical sentence with a capital letter (Gates H/I).
- The hypothesis statement itself, the variable names, and the direction of the relationship must remain unchanged.

Output format:

```text
Parallel Group ID:
Section:
Included Paragraphs:
Shared Structure:
Main D13/D15 Risk:
Group-Level Rewrite Goal:
Required Differentiation:
- Paragraph A should enter from:
- Paragraph B should enter from:
- Paragraph C should enter from:
```

## Methodology and Empirical Reporting High-Risk Rule

Do not treat methodology, research design, questionnaire design, sample screening, reliability testing, validity testing, and empirical result reporting as automatically low-risk.

These sections are high-risk when they repeat procedural templates.

High-risk patterns include:

- The variable is...
- It refers to...
- This study adapts...
- The final scale includes...
- The questionnaire was...
- The purpose was...
- The results show...
- This indicates that...
- The coefficient is significant...
- The hypothesis is supported...
- The value is above the threshold...

Mandatory rule:
- If methodology or empirical sections are flagged by any external detector, classify them at least as P1.
- If a methodology or empirical section shows strong external risk, long continuous AI-like fragments, or multiple converging internal risk dimensions, classify it as P0.
- Rewrite by restructuring the reporting pattern, not by synonym replacement.



## Variable Measurement Template Risk Rule

Variable measurement paragraphs are high-risk when several variables are described through the same reporting sequence, such as:

definition → scale source → item count
variable meaning → adopted scale → number of items
construct explanation → reference source → questionnaire wording

This pattern is especially risky when repeated for multiple variables in the same chapter.

Mandatory rewrite rule:
- Do not describe every variable using the same “definition → source → item count” structure.
- Vary how each variable is presented WITHOUT removing or merging information. Keep the definition, the scale source, and the item count for every variable — but introduce them in a different order and through different sentence forms for each variable.
- Insert scale information through explanatory clauses rather than writing identical separate template sentences, but do not drop any of the original information.
- Use different entry points for different variables: research role, measurement source, item content, or theoretical relevance.
- Preserve all variable names, scale sources, citations, item numbers, and questionnaire details.
- Do NOT shorten or merge these paragraphs. If de-templating tends to reduce length, add concrete detail (e.g. why this scale fits the AI-collaboration context, how the items were adapted) so each paragraph stays at least as long as the original. See Principle 4.

## Human Research Trace Relocation Rule

If a long introduction, abstract, or background section is detected as one continuous AI-like fragment, do not only rewrite sentence wording.

The revised section must include visible human research traces, such as:

- one clear author-side research judgment;
- one limitation or boundary of existing research;
- one contrast between the present thesis and previous studies;
- one explanation of why the selected variables are used;
- one sentence showing how the research scope was narrowed.

These traces must be based on the existing thesis content. Do not invent new data, new literature, or unsupported claims.

Mandatory source annotation (anti-fabrication hard rule): every T19 relocation and every T29 reconstruction sentence MUST be logged with its source — `source sentence`, `source table`, `source paragraph`, `source cited finding`, or `source method/variable statement`. If no existing source location can be named, the sentence is forbidden: do not write it. A researcher-trace sentence with no recordable source is treated as fabrication and fails Gate B. "Based on existing content" is not enough on its own — the specific source must be nameable.

For every T19 or T29 insertion or relocation, the visible evidence MUST include this Source Trace block:

```
Source Trace:
- Operation type: T19 relocation / T29 evidence-based reconstruction
- Original thesis source location (file/chapter/section/paragraph or table number):
- Exact source wording or source fact:
- Revised / inserted wording:
- Relation to original: relocated / lightly rephrased / reconstructed from existing facts
- Protected elements affected (if any):
- Word-count effect:
- New unsupported content added: No
```

"New unsupported content added" must always be "No"; if it cannot be "No", the sentence is fabrication and must not be written. If the source paragraph or the exact original wording cannot be identified and quoted in this block, T19/T29 must not be used for that sentence.

Mandatory rule:
- A revised introduction or abstract should not read as a perfectly smooth background → gap → purpose → contribution chain.
- Where the thesis already contains traceable material, at least one sentence may show the author’s research decision, uncertainty, limitation, or narrowing process. If no source location can be named, do not create such a sentence; use non-insertion techniques instead.

## Procedural Description De-Linearization Rule

Methodology, sample screening, reliability testing, validity testing, and common method bias sections should not be written as a pure procedure list.

High-risk sequence:
procedure → screening rule → retained sample → statistical basis
test purpose → threshold → result → conclusion
analysis step → value → standard → acceptable result

Mandatory rewrite rule:
- Add or relocate one researcher-side process-judgment sentence only when it already exists elsewhere in the thesis (T19 relocation) or qualifies under T29 as evidence-based reconstruction from existing thesis facts, with a completed Source Trace block. Never generate a fresh researcher-voice sentence merely to reduce AI risk.
- Explain why a procedure was necessary, not only what was done.
- Combine obvious procedural steps only at sentence level, and only when it removes no information, reduces no word count, merges no paragraphs, and does not change the procedure. If combining would shorten the paragraph, keep the steps and instead vary sentence entry, add existing specificity, or reorder information within the same paragraph (Principle 4).
- Move key result before generic test-purpose explanation when safe.
- Do not repeat “The purpose was... The results show... This indicates...” across several paragraphs.

## Front-Loaded Risk Allocation Rule

AI detectors often give strong weight to the opening part of a thesis, especially the abstract, introduction, research background, research significance, and early literature review.

Before rewriting, compare AI-risk distribution between the first 20% and the remaining 80% of the document.

If the first 20% has clearly higher risk than later sections:
- assign higher rewrite priority to the first 20%;
- apply Pass 2 and Pass 3 more strictly to the opening sections;
- do not distribute rewrite effort evenly across the whole document;
- preserve low-risk data tables and numerical result areas unless their explanatory prose is template-like.

Mandatory rule:
- If the first 20% risk is more than 15 percentage points higher than the later sections, front-loaded sections must be rewritten before lower-risk later sections.
- CNKI note: when the user's external detector is CNKI and an external report identifies high-risk sections, follow the report first. If no section-level CNKI evidence is available, do not assume the opening chapters are the only priority — run a two-zone scan: front-loaded sections (abstract, introduction, research background, significance, early literature review) AND back-loaded template sections (conclusion, countermeasures, recommendations, limitations, future research). For Chinese MBA / management theses, pay special attention to the conclusion/countermeasure/recommendation/outlook chapters, which often run template-heavy. The final target chapter is still chosen by the highest current measured external score, or by the highest internal risk estimate when no external score exists. This is a prioritisation rule only; it does not change the fragment-length, word-count, or no-paragraph-merge rules, which stay the same for all detectors.


## Results-Section Interpretation Boundary Rule

Empirical-results / findings paragraphs (where the thesis reports statistics, coefficients, significance, reliability/validity, regression/SEM/mediation/moderation output) are reported, not re-theorised. In these paragraphs:
- T18 (sequence reordering) MAY change the order of reporting steps, the sentence form, and the table anchoring, but MUST NOT add any interpretation, mechanism, or implication that is absent from the original paragraph.
- T29 (Evidence-Based Authorship Restoration) is NOT permitted to introduce new interpretation inside a pure results paragraph. The only exception: an interpretive sentence that already exists in the original results text, or is relocated verbatim-in-substance from an immediately adjacent discussion paragraph WITH explicit source tracking (this is then a T19 relocation, logged as such).
- Cautious interpretation, mechanism explanation, and implications belong in Discussion / Conclusion / Implications paragraphs, where T29 may operate normally under its four checks.
- Never upgrade a reported association into a causal or comparative claim in a results paragraph (no "X causes Y", no "the strongest path" unless the original already says so).

Scope guide: Results / Empirical Findings → reorder, recast, table-anchor only (no new interpretation). Discussion → cautious evidence-bound interpretation allowed (T29). Conclusion / Implications → evidence-limited implication statements allowed (T29).

## Author Style Baseline Rule

The target of rewriting is NOT "better, more native, more journal-style English". Over-polishing a non-native master's thesis into fluent journal prose is a common way to make a paragraph read MORE like AI, not less. The target is the author's own real writing, recovered from the parts of their own thesis that already read as human.

Before rewriting a chapter, build a quick Author Style Baseline from the document's existing LOW-RISK paragraphs (the ones the detector and the internal scan both flag as least AI-like):
- typical sentence length and how much it varies;
- preferred connectives and transitions the author actually uses;
- recurring verbs and phrasings;
- any consistent non-native / Chinese-English features (article use, preposition choices, mild awkwardness) — these are protective human signals, not errors to "fix";
- whether the author writes short paragraphs or long ones;
- citation placement habits; how variables and results are described.

Then rewrite high-risk paragraphs to move TOWARD this baseline, not toward generic polished English:
- match the author's sentence-length range and connective habits;
- keep the author's natural, mildly non-native register rather than upgrading it;
- do not introduce vocabulary, sentence shapes, or transitions that do not appear anywhere else in the author's own writing;
- the rewritten paragraph should read as if the same person who wrote the low-risk paragraphs wrote it.

Optional external author sample (calibration only): if the user supplies other genuine writing by the SAME author (e.g. an earlier paper, a proposal, a draft chapter), it MAY be used as an additional source for the style baseline above, alongside the document's own low-risk paragraphs. Hard limits: it must be the same author's real work; it is used ONLY to calibrate register, rhythm, connective habits, and mild non-native features; it is NEVER copied into the thesis, NEVER mined for content, claims, citations, or data, and NEVER used to import a sentence (that would be fabrication under Gate B and plagiarism). When no external sample is provided, fall back to the internal low-risk paragraphs, which remain the default and safest baseline because they are guaranteed to be the same author writing in the same genre.

This rule never licenses introducing real grammar/spelling errors (Gate I still applies). Mild non-native naturalness may be preserved ONLY when it is already present in the source and does not create a clear grammar, spelling, citation, or meaning error; never introduce new non-native features, new article/preposition errors, subject–verb errors, awkward fragments, or spelling mistakes. Gate I overrides style-matching whenever correctness is at risk. This is style-matching using the author's own existing text — not generation of a new persona.


## Data Table Anchor Rule

Tables, numerical results, and coefficient matrices are often lower-risk than surrounding explanatory prose. Do not rewrite tables unless the user asks.

Use tables as anchors to make explanatory text more concrete.

Mandatory rewrite rule:
- Preserve all table numbers, values, coefficients, p-values, and significance levels.
- Do not rewrite table content for AI-risk reduction.
- Revise the prose before and after tables if it follows a mechanical pattern.
- When explaining results, refer directly to table-specific values rather than using broad claims.
- Use concrete table references to reduce generic AI-like explanation.

Example:
Instead of:
The results show that the model has good explanatory power.

Use:
As shown in Table 4.3, the coefficient for X is positive and significant, which supports H1.


## Mandatory Staged Execution Rule

For long thesis documents or multi-paragraph revision tasks, do not execute all phases in one response.

The workflow must be divided into staged outputs:

### Stage 1: Evidence Review and Diagnosis Only

If an external detector report is provided, first execute External Highlight First Rule and build the External Risk Convergence Map. If NO external detector report is available, perform internal-risk diagnosis only and label all scores as internal risk estimates (not external-score predictions); in that case build an Internal Planning Ledger rather than a Chapter Version Ledger with external red lines (see No External Detector Score Rule).

Then execute Phase 1, Phase 1.5, Phase 1.6, Phase 1.6A, Phase 1.7, Phase 2a, Phase 2b, Phase 4, Phase 4.5, and Phase 4.5A.

Stage 1 must also output the appropriate ledger and the target-lock decision (which one chapter (two only by explicit user request) will be rewritten this round; see Core Operating Architecture and Phase 4.5A). If comparable external detector scores are available, output a Chapter Version Ledger (current score, lowest-ever score, source version, red-line status); if no comparable external score is available, output an Internal Planning Ledger instead, label all scores as internal risk estimates, and do not create external red lines (see No External Detector Score Rule).


Output only:
- external detector summary;
- External Risk Convergence Map;
- high-risk shared sections;
- section-level architecture review;
- paragraph list;
- section type;
- paragraph function role;
- repeated function clusters;
- parallel paragraph groups;
- group-level rewrite goal;
- paragraph AI score;
- hit dimensions;
- selected rewrite techniques;
- protected elements;
- rewrite intensity;
- pattern tags;
- pattern floor applied;
- repeated_structure_floor;
- section_template_floor;
- D16/D17 trigger floor;
- multi-detector trigger floor.

Do not rewrite the thesis text in Stage 1. Stage 1 produces only diagnosis, the target-lock decision, the ledger, the protected-element list, and the planned rewrite units; any revised wording waits until Stage 2.

### Stage 2: Rewrite with Execution Evidence

Execute Phase 5 and Phase 5.5.

For each rewritten paragraph or rewritten fragment cluster, output:
- Pass 1 evidence;
- Pass 2 evidence;
- Pass 3 evidence;
- revised paragraph or revised fragment cluster.

Do not output a final document until Phase 7 is completed.

### Stage 3: Mandatory Quality Gate
Execute Phase 7.

For each rewritten paragraph or rewritten fragment cluster, check:
- Gate A: AI-pattern reduction;
- Gate B: academic integrity and protected elements;
- Gate C: meaning preservation;
- Gate D: em dash and over-polished punctuation check;
- Gate E: aggregation-worsening and breakpoint check;
- Gate F: word-count preservation check (mandatory for every rewritten paragraph);
- Gate G: structure and readability check — headings stay on their own line, no merged paragraphs, no rewritten paragraph over 200 words / 12 sentences, EXCEPT where the source paragraph already exceeded the cap and no safe split is possible; if a safe split is possible, split and record Parent Paragraph ID → New Paragraph IDs with Gate F assessed on combined word count (mandatory for every rewritten paragraph);
- Gate H: grammatical completeness and sentence length — no fragments, no choppy runs, no sentence over ~30 words / two clauses;
- Gate I: grammar and subject-verb agreement;
- Gate J: logic flow and no out-of-place meta-commentary.

If any paragraph or fragment cluster fails any gate, mark it as Rework Needed or Failed.

### Stage 4: Final Scoring and Final Output
Only after Stage 3 passes, execute Phase 6, Phase 8, and Phase 9.

Stage 4 must include scope-appropriate scoring and summary:
- Phase 6: scope-aware risk index — report `overall_risk_index` only when all included body paragraphs of the full document were diagnosed in the same scope; if only one chapter, a selected batch, or a highlighted fragment was processed, report `target_chapter_risk_index`, `batch_risk_index`, or `fragment_risk_index` only and do NOT label it the whole-document score
- Phase 8: Summary Stats
- Phase 9: Final Output

Final output must include:
- Detection Report;
- Dimension-to-Technique Execution Plan;
- Three-Pass Rewrite Evidence;
- Protected Elements Check Report;
- Phase 7 Quality Gate Report;
- Rewritten Target Chapter(s) or Rewritten Selected Batch (use "Rewritten Document" only when the full document was actually rewritten and checked within the permitted scope);
- Revision Summary;
- Score Regression / Baseline Check, mandatory if an external detector score, external detector report, or baseline version is available. Before a comparable re-test, this check must not claim external score improvement; it records only baseline, candidate version, scope, and the re-test requirement, and the final output must include the line: "External score change: not claimable before re-test."

Mandatory rule:
- For long documents, never jump directly from detection to final rewritten document.
- Each round processes only ONE target chapter by default (two only by explicit user request). After Stage 4 and the Stage 5 re-test instruction, STOP execution: do not start another chapter, do not generate another rewritten candidate in the same response, and do not mark the target DONE until the user provides the comparable external re-test result (or confirms no external score is available). It IS allowed to output the exact re-test instruction, the required detector/scope metadata, and the status state to apply once the user returns the comparable external result.

### Stage 5: Mandatory Re-Test Stop (closed-loop checkpoint)

After delivering the rewritten target chapter(s), do NOT continue to the next chapter. Output:

```text
Round complete. Please re-test the rewritten target chapter(s) with the same external detector stream and report the new score. Do not test unrelated chapters for this round. After all chapters are below target, run a comparable whole-document test if the detector provides whole-document scoring.

Target: every externally measured chapter below 30% (or your specified target); the whole document below target only when a comparable whole-document score is available.

- If the user provides a comparable external re-test result BELOW target (<30%): mark this chapter DONE in the ledger, then select the next-highest chapter still at or above target. Do not imply that the next round has already been performed.
- If the new score is lower than before but STILL above target: good progress — I will keep this as the new baseline and run another round on the SAME chapter, moving up one rung on the escalation ladder.
- If the new score stayed the same or went UP: I will roll back to the chapter's lowest-ever version, then try a stronger technique (next escalation rung) on the same chapter.

We continue, chapter by chapter, until every externally measured chapter is below target. If a whole-document score is part of the task scope, the final whole-document version must be tested separately before the whole task is marked DONE. A new lowest score that is still above 30% is progress, not completion.
```

Then wait for the user's re-test result before starting the next round. This stop is mandatory and overrides any instinct to rewrite more chapters in the same response. Never present an above-target version as the final result.


## Public Evidence Rule

Internal execution does not count. A phase is complete only when paragraph-level evidence is visible in the output.

For every rewritten paragraph, the model must visibly output the required execution evidence in the user-facing report.
Paragraph-level execution evidence is mandatory for every rewritten paragraph, not necessarily for every diagnosed paragraph. Non-rewritten paragraphs must still appear in the Detection Report with a skip reason.

A phase is considered incomplete if the evidence required for the current mode and scope is only performed internally but not shown. Compact skip records are allowed only for low-risk, non-target paragraphs under the Working Mode / long-document rule.

Mandatory rule:
- Phase 1.6 is not complete unless high-risk sections show paragraph function roles, repeated function clusters, and parallel paragraph groups.
- Full D1–D17 paragraph tables (D1–D17 scores, total dimension score, pattern tags, pattern_floor, repeated_structure_floor, section_template_floor, D16/D17 trigger floor, and final paragraph_risk_index) are mandatory for: target paragraphs selected for rewriting; externally highlighted paragraphs/fragments; paragraphs in a repeated-structure cluster; and any paragraph whose final risk estimate is ≥ 40%. For low-risk, non-target paragraphs outside these categories — in BOTH Full Staged Mode and Working Mode — a compact skip record is sufficient (paragraph ID, section type, final risk estimate, primary skip reason, protected-element status, and whether D12–D17 structural risks were checked). Only when the user explicitly requests a full audit ledger must full D1–D17 evidence be shown for every included body paragraph. Route note: full D1–D17 tables are the ENGLISH-route evidence format. For Chinese-route target/high-risk paragraphs, provide the Chinese-route evidence fields (Chinese AI-risk groups, shared structure risks, protected elements, chinese_paragraph_risk_estimate, rewrite action) instead of an English D1–D17 table — do not convert Chinese text into English D1–D17 tables. For qualitative/mixed English passages, add the D18–D21 supplement where applicable. Phase 2 is never complete if a target/highlighted/cluster/≥40% paragraph is missing its route-appropriate full evidence.
- Phase 4.5 is not complete unless the Dimension-to-Technique Execution Plan is shown for each rewritten paragraph or rewritten fragment cluster.
- Phase 5.5 is not complete unless Pass 1, Pass 2, and Pass 3 evidence is shown for each rewritten paragraph or rewritten fragment cluster.
- Phase 7 is not complete unless Gate A through Gate J are shown for each rewritten paragraph or rewritten fragment cluster.
- Phase 8 is not complete unless Summary Stats include scope-appropriate statistics: average_paragraph_risk (or chinese_paragraph_risk_estimate where applicable), high_risk_share, medium_risk_share, section_repetition_score, relevant pattern floors, original/revised word count, word-count change percent, and a scope-specific judgment. Report `overall_risk_index` only when the full included body scope was actually diagnosed; otherwise report `target_chapter_risk_index`, `batch_risk_index`, or `fragment_risk_index`.
- Phase 9 is not complete unless all required report sections are included.

Do not write “completed internally,” “checked internally,” or “reviewed as a whole” as a substitute for visible evidence.

## No Aggregated Evidence Rule

Do not replace paragraph-level evidence with aggregated or generic evidence.

Invalid evidence:
- AI-like patterns reduced.
- Structure improved.
- Protected elements preserved.
- Quality gate passed.
- The paragraph was checked.

Valid evidence must identify the actual action:

```text
Paragraph ID:
Hit Dimensions:
Selected Techniques:
Protected Elements:
Pass 1 specific changes:
Pass 2 specific changes:
Pass 3 audit result:
Gate A result:
Gate B exact-string comparison:
Gate C meaning-preservation result:
Gate D em dash / over-polished punctuation result:
Gate E aggregation-worsening / breakpoint result:
Gate F word-count preservation result:
Original word count / Revised word count / Change %:
Gate G structure/readability result (headings on own line, no merge, paragraph ≤200 words / ≤12 sentences):
Revised paragraph length (words / sentences):
Gate H result (no fragments, no choppy run, longest sentence ≤~30 words / ≤2 clauses):
Gate I result (grammar / subject-verb agreement correct):
Gate J result (no out-of-place meta-commentary, logic flows):
No double hyphen "--" and hyphenated compounds intact:
```

Mandatory rule:

- Evidence must be paragraph-specific.
- Evidence must mention the actual detected dimensions and actual techniques used.
- Evidence must not use the same generic wording for every paragraph.


## Continuation and Resume Rule

If the task is interrupted, resumed, or continued in a later message, do not assume the workflow has been completed.


Before continuing, check the last completed stage:

- If Phase 1.6 is missing for high-risk sections, resume from Phase 1.6 before Phase 2 scoring.
- If parallel paragraph groups were not identified, do not continue to Phase 4.5.
- If Phase 4.5 is missing, resume from Phase 4.5.
- If Phase 5.5 execution evidence is missing, resume from Phase 5.5.
- If Phase 7 quality gate is missing, resume from Phase 7.
- If protected elements check is missing, run it before final output.


Do not treat a generated rewritten document as final unless it includes:
1. Dimension-to-Technique Execution Plan;
2. Three-Pass Rewrite Evidence;
3. Protected Elements Check Report;
4. Phase 7 Quality Gate Result.

If any of these are missing, the task status must be:
Revision Incomplete.

## Phase Completion Definition

A phase is complete only when its required evidence is visible in the output.

Internal execution does not count. A phase is complete only when paragraph-level evidence is visible in the output.

| Phase | Completion Requirement |
|------|------------------------|
| Phase 1.6 | Paragraph function roles, repeated function clusters, and parallel paragraph groups are shown for high-risk sections |
| Phase 2 | D1–D17 scores, pattern tags, floor application, D16/D17 trigger floor, and final paragraph_risk_index are shown for every included body paragraph |
| Phase 4.5 | Paragraph-level dimension-to-technique plan is shown |
| Phase 5.5 | Three-pass evidence is shown for each rewritten paragraph |
| Phase 7 | Gate A through Gate J results are shown for each rewritten paragraph or rewritten fragment cluster |
| Phase 8 | Summary Stats show all scope-appropriate scoring inputs, the final scope-appropriate risk index (overall_risk_index only for a fully diagnosed comparable document scope; otherwise target_chapter/batch/fragment), and judgment |
| Phase 9 | All required final report sections are included |

If the required evidence is missing, mark the task status as:

```text
Revision Incomplete — Missing Execution Evidence
```

Do not proceed to final output when the current phase is incomplete.



## Workflow

### Phase 1: Upload & Parse

1. Accept uploaded document (.docx, .md, .txt).
2. Extract full text while preserving section structure.
3. Split into paragraphs.
4. Exclude bibliography, appendices, questionnaires, declarations, table of contents, and pure table captions from the main AI score unless the user asks to score them.
5. Record section type for each paragraph:
   - abstract
   - introduction
   - literature review
   - hypothesis development
   - methodology
   - empirical results
   - discussion
   - conclusion/implications

### Phase 1.5: Full-Document Pattern Scan

Before paragraph-level scoring, perform a full-document pattern scan.

Identify:
- repeated sentence openings across chapters;
- repeated paragraph endings;
- repeated literature review patterns;
- repeated hypothesis-development structures;
- repeated discussion and conclusion templates;
- over-polished AI-like paragraph chains;
- high-risk sections requiring section-level rewriting.

Output:
- high-risk section list;
- repeated pattern summary;
- paragraph clusters that share similar architecture;
- suggested rewrite priority.

This phase helps prevent underestimating AI risk when individual paragraphs look acceptable but the document as a whole has repeated architecture.

### Phase 1.6: Section-Level Architecture Review

Before paragraph-level scoring, review the internal architecture of each section.

This phase checks what each paragraph is doing inside the section, not only which words it uses.

For each section, identify the functional role of every paragraph:

```text
Section:
Paragraph ID:
Paragraph Function:
Definition / Background / Citation Summary / Research Gap / Theory Application / Variable Mechanism / Hypothesis Support / Method Procedure / Scale Source / Sample Screening / Test Report / Result Interpretation / Conclusion / Implication / Limitation
Repeated Function Cluster:
Neighboring Paragraphs with Same Function:
Section-Level Risk:
```
High-risk signs:

- several neighboring paragraphs perform the same function;
- several subsections follow the same internal path;
- all theory paragraphs follow proposer → year → concept → application;
- all hypothesis paragraphs follow variable → mechanism → citation → hypothesis;
- all literature review paragraphs follow definition → citation → implication;
- all empirical result paragraphs follow test purpose → threshold → result → conclusion;
- all conclusion paragraphs follow result → theoretical meaning → practical meaning.

Mandatory rule:

- Phase 2 must use Phase 1.6 results when assigning D12, D13, D15, D16, and D17.
- If neighboring paragraphs perform the same function, raise D13 sensitivity.
- If a whole subsection repeats the same paragraph function path, raise D15 sensitivity.
- If methodology or empirical-result paragraphs repeat the same reporting phrases, raise D16 sensitivity.
- If neighboring paragraphs repeat the same reporting order, raise D17 sensitivity.
- Do not begin Phase 2 scoring until Section-Level Architecture Review is completed for high-risk sections.


### Phase 1.6A: External Report Abstraction

When one or more external detector reports are provided, do not treat detector names as rewrite instructions.

Before D1–D17 paragraph scoring and before D16/D17 pre-scan, convert external findings into shared AI-risk categories.

For each highlighted or high-risk section, identify:

1. Location:
   - chapter / section / paragraph group

2. External evidence:
   - high score
   - highlighted fragment
   - repeated high-risk area
   - front-loaded concentration
   - continuous AI-like fragment

3. Shared risk category:
   - sentence-level phrase template
   - repeated paragraph architecture
   - cross-paragraph sequence repetition
   - methodology/reporting template
   - uniform sentence rhythm / low burstiness
   - over-smooth reasoning chain
   - repeated hypothesis-development route
   - conclusion/result-implication loop
   - lack of human research trace

4. Rewrite unit:
   - sentence
   - paragraph
   - paragraph group
   - subsection
   - chapter segment
   - fragment cluster

5. Required intervention:
   - phrase-level repair
   - sentence rhythm repair
   - paragraph architecture rebuild
   - sequence reordering
   - methodology-template breaking (length-preserving)
   - section-level differentiation
   - human research trace insertion
   - front-loaded priority rewrite

Output format:

```text
Section:
External risk evidence:
Shared risk category:
Affected paragraphs or fragment group:
Rewrite unit:
Required intervention:
Priority:
Protected elements:
```

Mandatory rule:
- External detector reports are used as risk-location evidence, not detector-specific rewriting instructions.
- Do not build separate rewrite paths for different AI detectors.
- Phase 1.7 must use Phase 1.6A results when scanning D16/D17 risks.
- Phase 2 scoring must use Phase 1.6A results when assigning D12, D13, D15, D16, and D17.
- Phase 4.5 must select techniques based on shared risk category, not detector name.

D16 and D17 Integration Rule

D16 and D17 are formal scoring dimensions, not optional audit notes.

D16: Methodological Template Intensity (Weight: 4.0).
D17: Predictable Reporting Sequence (Weight: 3.0).

The full paragraph score must use D1–D17. Total possible score is 49.0.

raw_paragraph_risk = min(dimension_score / 49.0, 1.0) × 100%

If D16 ≥ 2.5 or D17 ≥ 2.5:
- paragraph_risk_index = max(paragraph_risk_index, 50%)
- priority group = A: Critical
- rewrite_intensity = Structural Reorganisation of existing sentences (NOT regeneration)
- Phase 4.5 must include a sequence-level or methodology-template rewrite plan.
- HOWEVER, if the paragraph's chapter is already below the target (default 30%), the chapter is done: do not rewrite it further. If the chapter is still at or above target, keep rewriting and escalate per Principle 5.

D16 must trigger T17: Methodological Template Breaking (length-preserving).
D17 must trigger T18: Sequence Reordering (length-preserving).

D16/D17 risks cannot be solved by synonym replacement. The rewrite must change the order of information and the sentence structure INSIDE each affected paragraph, and differentiate neighbouring paragraphs from one another — but it must NOT reorder whole paragraphs, change the argument's development, or reduce word count. Break the repeated template by restructuring within the paragraph and adding specificity, never by compressing, deleting, or shuffling paragraphs. See Principle 4 and Principle 7.


### Phase 1.7: D16/D17 Methodology and Reporting Sequence Pre-Scan

Use Phase 1.6A External Report Abstraction and Phase 1.6 Section-Level Architecture Review as input.


Before Phase 2 scoring, identify methodology-template and reporting-sequence risks.

Check:
- repeated methodology reporting phrases;
- repeated empirical-result reporting phrases;
- repeated variable measurement patterns;
- repeated test purpose → threshold → result → conclusion sequences;
- repeated definition → scale source → item count sequences;
- repeated result → explanation → implication sequences.

Output:
- D16 phrase-template clusters;
- D17 repeated-sequence clusters;
- affected paragraphs;
- preliminary D16/D17 trigger status.

Mandatory rule:
- Phase 2 must use Phase 1.7 results when assigning D16 and D17.
- If D16 ≥ 2.5 or D17 ≥ 2.5, affected paragraphs must be classified as A: Critical unless protected-element accuracy requires preservation.


## Additional Multi-Detector Trigger Floors

The following triggers do not need to become new scoring dimensions, but they must raise rewrite priority.

Trigger A: Front-loaded continuous AI-like fragment
- If the abstract/introduction/opening 20% contains long continuous AI-like fragments, affected sections must be at least P1.
- If the first 20% risk is extremely higher than later sections, affected sections must be P0.

Trigger B: Uniform sentence rhythm across paragraphs
- If three or more neighboring paragraphs have similar sentence length, similar clause pattern, and similar information density, affected paragraphs must receive rhythm repair in Pass 2.

Trigger C: Human research trace deficit
- If an introduction, abstract, or research significance section contains only smooth background/gap/purpose/contribution logic, it must receive human research trace insertion.

Trigger D: Repeated result-implication loop
- If a conclusion or discussion section repeats result → theoretical meaning → practical implication more than twice, the rewrite unit must be paragraph group or subsection, not individual sentence.

Mandatory rule:
- These triggers must be checked after Phase 1.7 and before Phase 2 scoring.
- If any trigger is activated, record it in the Detection Report.
- Phase 2b must apply the corresponding priority floor.
- Phase 4 and Phase 4.5 must use these triggers when deciding rewrite priority, rewrite unit, and rewrite intensity.
- These triggers do not replace D1–D17 scoring; they raise rewrite priority when cross-detector AI-risk patterns are visible.

Pre-Phase-2 checklist (all five must be confirmed before any paragraph scoring):
- [ ] Phase 1 inventory and excluded units recorded
- [ ] Phase 1.5 protected-element list extracted
- [ ] Phase 1.6/1.6A section architecture and D16/D17 pre-scan done
- [ ] Phase 1.7 language/method route fixed for every included paragraph
- [ ] Ledger type decided (Chapter Version Ledger vs Internal Planning Ledger)

### Phase 2: Detection and Paragraph AI Scoring

Phase 2 has two required substeps:

- Phase 2a: Route-specific scoring — English route: full D1–D17 dimension scoring; Chinese route: Chinese AI-risk groups plus shared structure-level checks; qualitative/mixed passages: add the D18–D21 supplement where applicable
- Phase 2b: Apply pattern_floor, repeated_structure_floor, section_template_floor, d16_d17_trigger_floor, and multi_detector_trigger_floor

Phase 2 is not complete until both 2a and 2b are completed.

For each English-route paragraph, score against the 17 AI-trace dimensions below. For Chinese-route paragraphs, do not use the English D1–D17 table; instead use these fixed evidence fields (see also Language Routing): (1) 中文模板短语命中; (2) 中文高频连接/收束模式; (3) 无依据夸张词或空泛价值判断; (4) 术语/数据/引用保护项; (5) 段落架构风险; (6) 跨段重复结构风险; (7) 方法/结果报告序列风险; (8) 外部检测高亮证据; (9) chinese_paragraph_risk_estimate; (10) 对应改写动作与同段字数补偿记录. For qualitative/mixed passages, add the D18–D21 supplement where applicable:

1. Repetitive Sentence Starters (0-3.0)
2. Formulaic Transitions and Connector Chains (0-3.0)
3. Over-Smooth Logical Flow (0-3.0)
4. Uniform Sentence Length and Rhythm (0-2.5)
5. Generic Academic Phrasing (0-3.0)
6. Overused Hedging or Balanced Claims (0-2.0)
7. Conclusion-Style Generalizations (0-2.5)
8. Passive Voice and Nominalization Clusters (0-2.0)
9. Abstract-to-Concrete Imbalance (0-2.5)
10. Citation Pattern Regularity (0-2.0)
11. Lexical Flatness and Repeated Academic Verbs (0-2.5)
12. Paragraph-Level Template Structure (0-4.0)
13. Cross-Paragraph Structural Repetition (0-4.0)
14. AI-Like Academic Smoothness / Low Human Friction (0-3.0)
15. Thesis-Section Template Dependency (0-3.0)
16. Methodological Template Intensity (0-4.0)
17. Predictable Reporting Sequence (0-3.0)
Total possible score: 49.0.

#### Phase 2 Completion Rule: Full 17-Dimension Coverage

Phase 2 is complete only when every included body paragraph has been evaluated against the required scoring route: English D1–D17 for English text; Chinese-route fields for Chinese text; and the D18–D21 supplement for qualitative or mixed-methods passages where applicable.

For each paragraph, the Detection Report must show:

```text
Paragraph ID:
(English route only — for Chinese-route paragraphs replace this D1–D17 table with the Chinese-route evidence template: Chinese AI-risk groups hit; Shared structure risks; Protected elements; chinese_paragraph_risk_estimate; Rewrite action. Never display an empty or forced D1–D17 table for Chinese text.)
D1 score:
D2 score:
D3 score:
D4 score:
D5 score:
D6 score:
D7 score:
D8 score:
D9 score:
D10 score:
D11 score:
D12 score:
D13 score:
D14 score:
D15 score:
D16 score:
D17 score:
Total dimension score:
```

Mandatory rule:
- Do not calculate paragraph_risk_index from fewer than 17 dimensions.
- Do not use automated partial scoring as the final Phase 2 result.
- If an automated script covers only some dimensions, label it as “Preliminary Auto Scan Only.”
- Missing dimensions must be manually evaluated before Phase 2b.
- D12, D13, D14, D15, D16, and D17 must always be checked manually or semi-manually because they require paragraph-level, section-level, and sequence-level judgment.


Invalid example:
D1 + D4 + D5 + D8 + D9 + D11 only

This is not a valid Phase 2 score.

Valid example:

D1-D17 all scored
Total dimension score calculated out of 49.0
Strong AI dimensions identified
Pattern floors ready for Phase 2b

If Phase 2 lacks full 17-dimension coverage, mark the task status as:
Revision Incomplete — Missing Full D1-D17 Scoring




#### Phase 2b: Paragraph-Level Internal AI-Risk Estimate and Floor Application
Phase 2b must not begin until Phase 2a has full D1–D17 coverage for every included body paragraph.

If any paragraph is missing one or more dimension scores, its paragraph_risk_index is invalid.


Calculate the raw paragraph score first:

```text
raw_paragraph_risk = min(dimension_score / 49.0, 1.0) × 100%
```

Then apply an external-detector-calibrated pattern floor. The final paragraph score must be the highest applicable value:

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

Pattern floor rules:

- If the paragraph has 2 or more strong AI dimensions: minimum 18%.
- If the paragraph has 3 or more strong AI dimensions: minimum 28%.
- If the paragraph has 4 or more strong AI dimensions: minimum 38%.
- If the paragraph has Paragraph-Level Template Structure (D12) ≥2.4: minimum 35%.
- If the paragraph has Paragraph-Level Template Structure ≥2.4 and Over-Smooth Logical Flow ≥1.5: minimum 42%.
- If the paragraph has Paragraph-Level Template Structure ≥3.2 and Generic Academic Phrasing ≥2.0: minimum 50%.
- If the paragraph reads like generated academic synthesis across most sentences: minimum 60%.

Cross-paragraph floor rules:

- If 3-5 paragraphs share similar opening structure: affected paragraphs minimum 25%.
- If 6-10 paragraphs share similar opening structure: affected paragraphs minimum 35%.
- If more than 10 paragraphs share similar opening structure: affected paragraphs minimum 45%.
- If a whole section repeats the same paragraph pattern: affected paragraphs minimum 50%.

Section template floor rules:

- Literature review paragraphs following definition → citation → implication: minimum 35%.
- Hypothesis paragraphs following variable explanation → mechanism → hypothesis: minimum 40%.
- Discussion paragraphs following result → explanation → implication: minimum 42%.
- Conclusion paragraphs using broad theoretical/practical implications without direct connection to the findings: minimum 45%.
- Empirical result paragraphs repeatedly following coefficient → significance → hypothesis support: minimum 35%.


D16/D17 trigger floor rules:

- If D16 ≥ 2.5 or D17 ≥ 2.5:
  paragraph_risk_index = max(paragraph_risk_index, 50%)
  priority group = A: Critical
  rewrite_intensity = Structural Reorganisation of existing sentences (minimal edit, NOT regeneration)
  exception: if the paragraph's chapter is already below the target (default 30%), the chapter is done and is not rewritten further.

Multi-detector trigger floor rules:

- Trigger A activated: affected sections minimum P1; if severe, P0.
- Trigger B activated: affected paragraphs must receive Pass 2 rhythm repair.
- Trigger C activated: affected sections must be reviewed for source-supported T19 relocation or T29 evidence-based reconstruction. This trigger is PLANNING only — any actual insertion happens solely in the rewrite phases (Phase 5/5.5) with a completed Source Trace block. If no traceable source exists, do not insert researcher trace; use T20/T21/T22/T23 instead or mark “author confirmation needed”.
- Trigger D activated: rewrite unit must be paragraph group or subsection.

## Conclusion Integration Rule

Conclusion sections are high-risk when every finding is reported through the same chain:

empirical result → theoretical meaning → practical implication
finding summary → contribution → managerial implication
hypothesis result → explanation → recommendation

Mandatory rewrite rule:
- Do not summarize each hypothesis result one by one in the same structure.
- Group related findings only when the original conclusion already supports that grouping. Do not merge paragraphs, do not remove hypothesis-level information, do not reorder evidence in a way that weakens the argument, and do not introduce a new overarching interpretation the thesis does not contain.
- Discuss the overall research pattern before individual details.
- Link theoretical and practical meaning to the combined findings, not to every single hypothesis separately.
- Avoid repeated “This finding provides theoretical and practical implications...” sentences.

Required output:
A revised conclusion may contain, where supported by the original thesis (if the original conclusion does not support grouping, preserve the original finding structure and only de-template the wording):
- one integrated overall finding;
- grouped discussion of related findings;
- one cautious explanation of what the results mean;
- practical implications linked to the overall pattern, not repeated after every result.


### Phase 3: Risk Prioritisation and Target Selection

This phase locks the single unit to work this round, before any rewrite strategy is chosen. It applies the rules already defined in Principle 3 (red line, target lock, version ledger); it does not introduce new logic.

- Build or update the Chapter Version Ledger: for each chapter record its lowest-ever comparable external score (the red line), its current status (Done / Progress / Rejected / Paused / Blocked / Incomplete — see the status state machine), and the next untried escalation rung (Principle 5). If the user specifies a target below the default 30%, record it as a user-defined strict target and state that completion against it depends only on comparable external re-test evidence (a stricter target may be unreachable for some chapters; PAUSED/BLOCKED with documentation is then the honest outcome).
- Select exactly ONE target unit by default: the highest current measured chapter that is still at or above the target threshold (default 30%). Bounded-unit exception (Principle 3): if an external report highlights only a bounded sub-section or fragment cluster, the round MAY target that bounded unit, tracked under its chapter's ledger entry.
- Mark every non-target chapter as "not rewritten this round." Chapters already below target are protected and left untouched.
- If no external report is available, prioritise using the internal D1–D17 scores plus the D16/D17 trigger floors and section-template floors.
- Output of this phase: the chosen target unit, its red line, and the escalation rung selected for this round. Phase 4 then plans the rewrite strategy for that locked unit only.

### Phase 4: Rewrite Strategy

Use the priority group from Paragraph Triage Rule and the External Risk Convergence Map.

| Priority | Risk Level | Strategy | Action |
|---|---|---|---|
| P0 / A | Critical or shared external high-risk | Structural Reorganisation (minimal edit) | Reorganise existing sentences in the fragment cluster, subsection, or paragraph architecture — reorder, re-segment, change entry point, inject researcher-trace sentences. NEVER regenerate as new prose. External highlighted sections prioritised. |
| P1 / B | High | Standard Reorganisation (minimal edit) | Edit repeated openings, endings, transitions, abstract phrasing, and section templates using existing wording. |
| P2 / C | Medium | Pattern-Based light edit | Edit only if the paragraph contributes to repeated section structure. |
| P3 / D | Low | Check Only | Preserve unless it is part of a high-risk fragment cluster. |

Mandatory rule:
- External P0 overrides internal low paragraph_risk_index.
- A-class paragraphs normally require rewriting BY MINIMAL EDIT, never by regeneration.
- A chapter already below the target (default 30%) is done and is not rewritten further regardless of internal class. A chapter at or above target is never exempt and must continue through the escalation ladder (Principle 5).
- Each round, only ONE highest-scoring target chapter is rewritten by default (two only by explicit user request); all others are left untouched.
- Always start at the lightest rewrite intensity and escalate step by step, re-checking after each step.
- Do not maintain two conflicting AI% strategy tables.

## Function-Entry Diversification Rule

When paragraphs in the same section share similar structure, the rewrite must diversify the paragraph’s functional entry point.

Do not let all paragraphs begin from the same role.

Allowed functional entry points:

- concrete research problem;
- observed phenomenon;
- variable-specific mechanism;
- limitation in previous studies;
- contradiction or tension in prior findings;
- methodological reason;
- empirical result;
- theoretical boundary;
- practical condition;
- direct thesis-specific explanation.

Examples:

For Introduction:
- One paragraph may enter from the research background.
- One paragraph may enter from the specific research gap.
- One paragraph may enter from the practical problem.
- One paragraph may enter from why the current variables matter.

For theory framework:
- One theory may enter from why the phenomenon needs this theory.
- One theory may enter from what resource or cognition changes in AI collaboration.
- One theory may enter from how the theory supports the model.
- Do not write all theory paragraphs as theorist → year → definition → application.

For hypothesis groups:
- One hypothesis may enter from psychological mechanism.
- One hypothesis may enter from behavioral allocation of time or attention.
- One hypothesis may enter from cognitive stimulation.
- One hypothesis may enter from boundary condition or organizational context.

For conclusion:
- Do not write each conclusion as result → theory → practice.
- Combine related findings into a continuous argument where possible.
- Use fewer repeated “this finding means...” structures.

Mandatory rule:
- Pass 2 must rebuild paragraph function and entry point, not only sentence rhythm.
- If Pass 2 only changes sentence length or opening words, mark it as insufficient.


### Phase 4.5: Dimension-to-Technique Execution Plan

Before rewriting, create a paragraph-level execution plan.

For parallel paragraph groups, Phase 4.5 must include a group-level differentiation plan.

Do not produce only paragraph-by-paragraph plans when D13 or D15 is high.

Required group-level fields:

```text
Parallel Group ID:
Section:
Included Paragraphs:
Shared Structure:
Repeated Function Cluster:
Group-Level Rewrite Goal:
Functional Entry Plan:
Paragraph-Level Differentiation:
- P1:
- P2:
- P3:
```
Mandatory rule:

If D13 ≥ 2.0 or D15 ≥ 1.5, Phase 4.5 must include group-level planning.
If the plan only lists individual paragraph techniques without explaining cross-paragraph differentiation, Phase 4.5 is incomplete.


For every paragraph selected for revision, record:

```text
Paragraph ID:
Hit Dimensions:
Selected Techniques:
T19 used: Yes / No. T29 used: Yes / No. Never merge T19 and T29. T19 = relocate or lightly rephrase author/researcher-side reasoning that already appears elsewhere in the thesis. T29 = reconstruct a cautious interpretive sentence from traceable existing thesis evidence. T19 and T29 are not default rewrite tools. Use T19 only when a suitable researcher-side sentence already exists elsewhere in the thesis and can be relocated or lightly adjusted. Use T29 only when the underlying evidence is explicitly present but no ready-made sentence exists. If neither condition is met, use non-additive techniques (e.g. T1, T2, T3, T14, T17, T18, T22, T23) instead. If either is Yes, include a Source Trace block (operation type, source location, extracted source material, revised sentence, integrity check). If source trace is unavailable, write "Author confirmation needed" and do not add the sentence.
Reason for T19 relocation: / Reason for T29 reconstruction: (write N/A for whichever is not used)
Protected Elements:
Rewrite intensity:
Aggregation-worsening risk before Phase 7: Low / Possible / High
Breakpoint likely needed: Yes / No
```
Each high-risk dimension must be connected to at least one rewrite technique:

| Hit Dimension | Required Technique |
|---|---|
| D1 Repetitive Sentence Starters | T1 Starter Variation |
| D2 Formulaic Transitions | T2 Transition De-formulaizing |
| D3 Over-Smooth Logical Flow | T13 Reasoning Visibility or T14 Paragraph Architecture Rebuilding or T19 Researcher-Trace Relocation and Local Integration |
| D4 Uniform Sentence Length and Rhythm | T3 Sentence Length Variation |
| D5 Generic Academic Phrasing | T6 Generalization Surgery or T12 Abstract Word Reduction |
| D6 Hedging / Balanced Claims | T4 Hedging Calibration and Claim-Strength Control or T5 Balance Disruption |
| D7 Conclusion-Style Generalizations | T6 Generalization Surgery |
| D8 Passive / Nominalization Clusters | T7 Passive Voice Control |
| D9 Abstract-to-Concrete Imbalance | T8 Concrete Anchoring or T12 Abstract Word Reduction or T19 Researcher-Trace Relocation and Local Integration |
| D10 Citation Pattern Regularity | T9 Citation Naturalization |
| D11 Lexical Flatness / Over-Repetition | T10 Lexical Precision and Repetition Control |
| D12 Paragraph-Level Template Structure | T14 Paragraph Architecture Rebuilding or T19 Researcher-Trace Relocation and Local Integration |
| D13 Cross-Paragraph Structural Repetition | T15 Section-Level Pattern Diversification |
| D14 AI-Like Academic Smoothness | T11 Non-Native Academic Rhythm or T13 Reasoning Visibility or T19 Researcher-Trace Relocation and Local Integration |
| D15 Thesis-Section Template Dependency | T15 Section-Level Pattern Diversification or T19 Researcher-Trace Relocation and Local Integration |
| D16 Methodological Template Intensity | T17 Methodological Template Breaking (length-preserving) or T19 Researcher-Trace Relocation and Local Integration |
| D17 Predictable Reporting Sequence | T18 Sequence Reordering (length-preserving) or T19 Researcher-Trace Relocation and Local Integration |


Mandatory rule:

- Do not rewrite a paragraph until its hit dimensions and selected techniques have been identified.
- Do not use random short sentences as the main rewrite method.
- If a paragraph has D12, D13, or D15 risk, sentence-level polishing alone is not sufficient.


## Phase 4.5A and Phases 5–9: Rewrite Resource Allocation, Three-Pass Rewrite, and Quality Gates

> Structure note: this section runs from the Phase 4.5A resource-allocation plan through the Phase 5 three-pass rewrite, Phase 5.5 evidence, Phase 6 overall risk index, the Phase 7 Gate A–J quality gates, and Phases 8–9 (summary stats and output). The dimension definitions (D1–D21) and technique definitions (T1–T29) are NOT duplicated here — they live in `references/detection_principles.md` and `references/rewrite_methods.md`. What stays in this file is the operational workflow and the Gate A–J definitions, which the executor needs inline while running a round.

Before rewriting, allocate rewrite intensity based on external and internal risk distribution.

Target-lock first: list all chapters by current measured score, descending. Only the highest chapter that is still at or above the target (default 30%) may be rewritten this round (two only on explicit user request). Mark every other chapter "not rewritten this round."

Output format:

Chapter rewrite decision (this round):
- Target chapter 1:
- Target chapter 2 (optional):
- Chapters left untouched this round:

Section:
Risk concentration:
External evidence:
Internal risk dimensions:
Rewrite priority:
Rewrite pass allocation:
- Pass 1 only
- Pass 1 + Pass 2
- Pass 1 + Pass 2 + Pass 3
Rewrite unit:
Reason:

Mandatory rule:
- Each round rewrites at most 2 chapters — the highest-scoring ones. Do not touch any other chapter.
- Never rewrite a chapter already below the target (default 30%); it is done. Every chapter at or above target must keep being rewritten until it drops below target.
- Do not distribute rewrite effort evenly across the thesis.
- High-risk opening sections, repeated hypothesis groups, methodology templates, and conclusion loops must receive deeper structural reorganisation — by reordering existing sentences, never by regeneration.
- Low-risk tables, numerical matrices, and purely factual data areas should normally be preserved.



### Phase 5: Three-Pass Rewrite Protocol for Multi-Detector Risk Reduction

### Pass 1: Template and Phrase Repair
Target:
- repeated sentence openings;
- formulaic transitions;
- methodology reporting phrases;
- empirical-result reporting phrases;
- generic academic conclusions.

Required actions:
- rewrite repeated openings into varied, equally-long openings (do not just delete them);
- de-template the definition/source/item-count pattern by restructuring and adding specificity, NOT by compressing it;
- replace broad academic phrases with thesis-specific wording of equal or greater length;
- do not reduce the paragraph's word count (Principle 4);
- preserve protected elements.

### Pass 2: Rhythm and Architecture Repair
Target:
- uniform sentence length;
- repeated paragraph function;
- repeated reporting sequence;
- over-smooth claim → explanation → implication chain.

Required actions:
- vary sentence length naturally;
- change paragraph entry point;
- reorder repeated reporting sequence;
- split long sentences to vary rhythm (encouraged); do NOT merge or combine sentences, as that reduces length (Principle 4);
- keep every original paragraph break — never merge paragraphs to fight cross-paragraph repetition; differentiate neighbouring paragraphs instead (Principle 6);
- keep every section heading on its own line, untouched and unmoved; never let a paragraph run into a heading;
- keep each rewritten paragraph within readable limits (≤ ~160 words / ~9 sentences soft, 200 words / 12 sentences hard cap); if an original paragraph already exceeds the cap, split it at a natural break;
- avoid creating another repeated improved template.

### Pass 3: Human Research Trace and Section-Level Differentiation
Target:
- continuous AI-like fragments;
- introduction/abstract smoothness;
- conclusion result-implication loops;
- lack of author-side research judgment.

Required actions:
- add research-boundary or decision-trace sentences based only on existing content;
- vary how related findings are presented (different connective logic, different entry points) without deleting or compressing any of them;
- show cautious thesis-level interpretation;
- check that the paragraph does not become overly polished.


### Phase 5.5: Execution Evidence

For each revised paragraph or revised fragment cluster, record what was done in each pass:

```text
Paragraph / Fragment Cluster ID:

Pass 1 — Remove AI-like patterns:
- Repeated starters reduced:
- Formulaic transitions reduced:
- Generic academic phrases reduced:
- Unnecessary hedging reduced:
- Passive/nominalization clusters controlled:

Pass 2 — Rebuild rhythm, structure, and paragraph function:
- Sentence rhythm changed:
- Paragraph opening changed:
- Paragraph ending changed:
- Paragraph architecture changed:
- Functional entry point changed:
- Paragraph role differentiated from neighboring paragraphs:
- Reasoning visibility improved:

Group-level differentiation result:
- Shared structure reduced:
- Neighboring paragraph roles diversified:

Pass 3 — Anti-AI audit:
- Remaining repeated structure:
- Remaining generic conclusion:
- Remaining over-smooth logic:
- Remaining lexical repetition:
- Decision: Pass / Needs Rework

Word count check (mandatory):
- Original paragraph word count:
- Rewritten paragraph word count:
- Change (%): (must be ≥ 0%; target 0% to +15%)
- Length decision: Pass / Needs Rework (FAIL if rewritten < original)
```
Mandatory rule:

- Execute the passes assigned to the paragraph in Phase 4.5A. A paragraph assigned "Pass 1 only" is complete after Pass 1; a paragraph assigned all three passes must complete all three.
- If an assigned pass is skipped, mark the paragraph as "Revision Incomplete".
- Final rewritten text cannot be output until all ASSIGNED passes for that paragraph are completed.
- No pass may regenerate the paragraph as new prose. Every output sentence must trace to an original sentence or be a permitted researcher-trace/breakpoint sentence based on existing content.
- A rewritten paragraph whose word count is below the original FAILS and must be redone by adding specificity/researcher-trace content rather than compressing (Principle 4 + Phase 7 Gate F).

### Phase 6: Scope-Aware Internal Risk Index

Calculate several scope-level signals. Use document-level wording only when Scope = Full document; for a chapter, selected batch, or highlighted fragment, label the result target_chapter_risk_index, batch_risk_index, or fragment_risk_index:

```text
average_paragraph_risk = average(paragraph_risk_index across all included paragraphs)
high_risk_share = percentage of paragraphs with paragraph_risk_index ≥ 40%
medium_risk_share = percentage of paragraphs with paragraph_risk_index ≥ 25%

(Note: medium_risk_share is cumulative by design — an "at least medium" pressure signal that intentionally includes the high-risk paragraphs already counted in high_risk_share. It is not a medium-only band; the two terms deliberately overlap so the overall formula weights cumulative risk pressure.)
section_repetition_score = scope-level repeated-structure penalty, assessed only within the actually diagnosed scope (use document-level only when Scope = Full document; otherwise chapter-level, batch-level, or fragment-level)
```

Use the following formula:

```text
scope_risk_index =
(0.45 × average_paragraph_risk)
+ (0.25 × high_risk_share)
+ (0.15 × medium_risk_share)
+ (0.15 × section_repetition_score)
```

All four inputs must be expressed on a 0–100 scale, not a 0–1 decimal scale.  
For example, if 47.5% of paragraphs are high-risk, use 47.5, not 0.475.

Report the result as `overall_risk_index` only when the full included document scope was evaluated; otherwise report it as `target_chapter_risk_index`, `batch_risk_index`, or `fragment_risk_index`.

section_repetition_score is a 0–100 scope-level score based on repeated structures within the diagnosed scope:
- 0–20: little repeated structure
- 21–40: mild repetition
- 41–60: clear repetition across one section
- 61–80: repeated structures across several sections
- 81–100: repeated architecture across most of the thesis

Then apply the scope-appropriate pattern floor:

```text
scope_risk_index = max(
  scope_risk_index,
  scope_pattern_floor
)
```

Scope pattern floor rules:

- If more than 25% of paragraphs share similar openings or endings: minimum 25%.
- If more than 35% of paragraphs follow section templates: minimum 35%.
- If literature review and hypothesis sections both show repeated template architecture: minimum 40%.
- If the paper repeatedly uses smooth AI-style paragraph chains across chapters: minimum 45%.
- If an external detector result is known and is much higher than the internal score (operationally: the external score exceeds the internal scope estimate by ≥15 percentage points or is ≥1.5× the internal estimate), use calibration mode and do not report a score lower than 70% of the external detector result unless there is clear evidence that the external score includes excluded content. This 70% value is a conservative heuristic workflow floor — NOT a statistical conversion formula and NOT a claim that the internal score predicts the external detector. If the external score includes excluded material, non-body text, references, appendices, OCR errors, or a different document version, label the comparison non-comparable and do not apply the floor mechanically.

Example calibration:

```text
If Turnitin AI = 48%, internal overall_risk_index should normally not be reported below 33.6% after recalibration.
```

Final score is capped at 100%.

### Phase 7: Mandatory Quality Gate and Rework Loop

Phase 7 is mandatory. It cannot be skipped.

Before final output, check every rewritten paragraph or rewritten fragment cluster against Gates A–D, Gate F (word-count preservation), Gate G (structure and readability), Gate H (grammatical completeness and sentence length), Gate I (grammar and subject-verb agreement), and Gate J (logic flow and no meta-commentary) — all always mandatory. Gate E must ALWAYS appear in the visible evidence table, but its status depends on triggering: report Gate E = Pass / Rework Needed / Failed when the rewrite handles externally highlighted long fragments, changes fragment boundaries, or any revised fragment may exceed 3000 characters; otherwise report Gate E = N/A — no long-fragment or boundary-change risk. Do not omit Gate E from the evidence table just because it was not triggered (note: merging paragraphs is forbidden under Principle 4, so Gate E aggregation risk should normally not arise from merging):

#### Gate A: AI-Pattern Reduction Gate

- Did the rewrite address the paragraph’s actual hit dimensions?
- Were D12/D13/D15 structural risks handled structurally, not only by word changes?
- Were D16 methodological-template risks handled by reordering and template breaking (NOT by compression)?
- Were D17 sequence risks handled by changing repeated reporting order, not only by replacing transitions?
- Were repeated openings/endings reduced?
- Were formulaic transitions reduced?
- Was over-smooth logic made less mechanical?
- Was random short-sentence insertion avoided?
- **Minimal-edit check:** Can every output sentence be traced to a specific original sentence (or a permitted researcher-trace/breakpoint sentence)? If the paragraph was regenerated as new prose, FAIL the gate and redo by minimal edit.
- **Regression check:** Is the rewritten paragraph plausibly lower-risk than the original, or did smoothing make it more AI-like? If it reads smoother/longer/more templated than the original, FAIL and roll back.
- **Placeholder / template-residue check (OUTPUT-BLOCKING):** Scan for any unfilled placeholder or template residue left by editing, e.g. literal "X and Y", "how X and Y relate A and B", "...", "[variable]", "[insert]", "TODO", "how ... and ... relate". These are submission-level defects that destroy meaning. If any is found, FAIL and restore the real variable names / complete clause from the original before output. Example failure: "examine how ... and ... relate employee–AI collaboration and employee innovative behavior" — the ellipses must be the actual mediator names.
- **Misplaced-sentence check:** Does every sentence belong to this paragraph's topic? A sentence that fits a different section (e.g. a Bootstrap-method explanation dropped into a demographics paragraph, a research-gap sentence dropped into a chapter-roadmap) is a wrong insertion — remove it or move the rewrite back so the paragraph stays on its own topic. This often happens when researcher-trace material is relocated to the wrong place; relocation must land where the content actually fits (Gate J).

#### Gate B: Academic Integrity Gate

Compare original and revised text for protected elements:

- section and sub-section headings (exact text, numbering, and position on their own line, e.g. "1.1 Research Background", "Chapter 2", "5.2.1 ...")
- figure and table captions, and numbered/bulleted list markers
- paragraph breaks (the original number and position of paragraph boundaries must be preserved; no merging)
- citations and author names
- variable names and abbreviations
- capitalization of variables
- hypothesis numbers and hypothesis wording
- coefficients
- p-values
- significance levels
- model names
- table numbers
- sample size
- statistical conclusions
- statistical symbol formatting (keep "p < 0.05", "β = 0.32", "VIF", "κ = 0.87", "R²" exactly as written; do not respace, reword, or convert to text such as "p value below 0.05" unless the original already did)
- the full protected-statistical-string set: β, B, SE, t, F, R², ΔR², χ², df, p, CI, CR, AVE, VIF, Cronbach's α, sample size N/n, model labels, table/figure numbers, hypothesis labels, and all inequality signs such as "p < .001" — all kept verbatim
- the reference list / bibliography: reference entries, author names, years, article and journal titles, volume/page numbers are LOCKED. Never rewrite, paraphrase, or "de-template" any part of a reference entry. The reference-list section is not a rewrite target under any circumstance.
- thesis front-matter and identity strings: the thesis title and subtitle, the author's name, the supervisor's / advisor's name and academic title, committee names, institution and department names, and the date are LOCKED — never rewritten, restyled, or "de-templated".
- appendices and their contents (questionnaires, scale instruments, interview guides, consent forms, raw-data tables) are LOCKED unless the user explicitly asks for that appendix to be rewritten.
- verbatim quotations and interview quotations, questionnaire item wording, and scale-item text — never split, shortened, re-punctuated, or stylistically rewritten for rhythm
- PROTECTED HEDGES AND CLAIM-STRENGTH MARKERS. Do not delete or weaken/strengthen the words that bound a claim, because dropping them silently upgrades a conditional statement into an unconditional assertion (overclaim = an integrity failure, and a frequent side effect of "smoothing"). Three protected classes:
  - Epistemic hedges that bound the claim: "may", "might", "could", "tentative", "preliminary", "exploratory", "appears to", "is likely", and the inferential verbs "suggests", "indicates", "is consistent with". These must NOT be rewritten into stronger verbs such as "demonstrates", "proves", "establishes", "confirms", "shows that". Keep the original epistemic strength exactly.
  - Reflexivity / positionality markers actually present in the text (e.g. "from the first author's perspective as a former practitioner", "the authors served on the committee"). Do not strip these for flow; removing disclosure changes the paper's stance.
  - Temporal / scope qualifiers that pin a claim: "in this sample", "for this cohort", "under the conditions tested", "between 2020 and 2024", "within the cases examined". Do not drop or generalise these.
  When a paragraph is shortened or smoothed, hedges are protected ahead of any other compression target. If removing a hedge is the only way to hit a length target, do not remove it — find another edit.

If any protected element changes accidentally, restore the original form. Headings must remain on their own line with the surrounding paragraph breaks intact; if a heading was absorbed into body text or moved, restore the original structure before output.

Citation-verification boundary: during AI-risk rewriting, citations are locked and not silently "corrected". If a citation looks inaccurate, duplicated, or inconsistent, flag it separately for the user to verify — do not alter it inside the rewrite.

Reference-pollution check (OUTPUT-BLOCKING): confirm no body-text sentence has leaked into a reference entry. A reference title that contains discussion prose (e.g. "What this study adds is a comparison of three mediating paths...", "The practical upshot is that...") is a corruption from a prior bad edit — restore the real title. Never let rewritten prose contaminate the bibliography.

The check must compare exact strings before and after rewriting, especially capitalization-sensitive terms such as variable names and abbreviations.

#### Gate C: Meaning Preservation Gate

Check:

- original claim preserved
- academic logic preserved
- no new theory added
- no new reference added
- no new data added
- no unsupported example added
- no causal claim introduced unless already supported
- claim STRENGTH preserved: an inferential/hedged verb ("suggests", "indicates", "is consistent with", "may", "appears to") was not upgraded to an assertive one ("demonstrates", "proves", "establishes", "confirms"), and no epistemic hedge, positionality marker, or scope qualifier was dropped (see Gate B protected hedges). Strengthening a claim during rewriting is an overclaim and fails this gate.

#### Gate D: Punctuation Check (em dash, hyphen, en dash)

Check:
- No new em dashes (—) should be introduced during rewriting.
- ACTIVELY SCAN the output for the Unicode em dash character "—" (U+2014), not only the ASCII "--". A literal "—" left in body prose is itself a strong AI-style punctuation signal and must be addressed. Existing em dashes should be removed or recast unless they are inside a protected verbatim quotation, a title, a technical label, or another protected expression. (En dashes "–" U+2013 in numeric/date/page ranges are correct and stay.)
- Sentences using em dashes for polished contrast, dramatic emphasis, or broad restatement must be revised into plainer academic structures.
- HYPHENS MUST NOT BE MANGLED. Avoiding em dashes must NEVER be done by turning a normal hyphen into a double hyphen. A hyphenated compound such as "employee-AI", "self-efficacy", "AI-generated", "cross-domain", "human-AI" must keep its single hyphen exactly. Never write "employee--AI", "self--efficacy", etc.
- DO NOT replace a correct em dash with "--" (two hyphens). When an em dash is genuinely removed, replace it with a grammatically correct alternative: a comma, a colon, a semicolon, parentheses, or two separate sentences, and never with "--" or "-".
- Do not introduce "--" (double hyphen) anywhere. The double hyphen is not valid academic punctuation; it is only an ASCII stand-in for an em dash and must not appear in the output.
- En dashes in number/page/date ranges (e.g. "2007–2010", "pp. 35–37") are correct and must be preserved, not converted to hyphens or double hyphens.
- The only correct uses of a single hyphen are compound modifiers and prefixed words; do not add or remove hyphens from words that are not normally hyphenated.

Quick checks:
- Search the output for "--" → there should be ZERO occurrences (outside markdown tables/rules).
- Search the output for "—" (Unicode em dash) → there should be ZERO occurrences in body prose (allowed only inside protected verbatim quotations, titles, or technical labels).
- Every original hyphenated term (employee-AI, self-efficacy, etc.) appears with exactly one hyphen in the output.

Mandatory rule:

- If Phase 7 is not completed, do not output the final rewritten document.
- If protected elements are damaged, do not output the paragraph until they are restored.
- If the rewrite only inserts short sentences without addressing hit dimensions, mark it as Rework Needed.
- If any "--" appears, any "—" remains in body prose, or any hyphenated compound was changed (e.g. "employee-AI" → "employee--AI"), mark Rework Needed and fix it.

#### Gate E: Aggregation-Worsening and Breakpoint Check

Purpose:
This gate checks whether rewriting has unintentionally reduced the number of text fragments while increasing the length of the largest single fragment. Gate E applies when fragment boundaries change, external-highlighted long fragments are involved, an over-3000-character revised fragment may result, or an over-cap paragraph is split at safe boundaries. Paragraph merging remains FORBIDDEN (Principle 4) and must never be treated as an allowed Gate E scenario. Such a result may create aggregation-worsening risk, because external detectors may treat the revised text as a longer continuous AI-like segment.

Check:
- original_fragment_count
- revised_fragment_count
- original_max_fragment_characters
- revised_max_fragment_characters
- whether revised_fragment_count < original_fragment_count
- whether revised_max_fragment_characters > original_max_fragment_characters
- whether any revised single fragment exceeds 3000 characters

Aggregation-worsening signal:
```text
revised_fragment_count < original_fragment_count
AND
revised_max_fragment_characters > original_max_fragment_characters
```
Mandatory rule:

Because merging paragraphs is forbidden (Principle 6), revised_fragment_count should never be lower than original_fragment_count. If it is, paragraphs were wrongly merged — restore the original paragraph breaks.
If a revised single fragment exceeds 3000 characters (or a paragraph exceeds the Gate G caps of 200 words / 12 sentences), the preferred fix is to SPLIT it into separate paragraphs at a natural logical break, not to keep one long block. A breakpoint sentence may be added inside an unavoidably long single paragraph only when splitting is not appropriate.
Any breakpoint must be visibly different from AI-style continuous academic prose and supported by existing thesis content. A heading is never used as a breakpoint and is never moved to create one.

Valid breakpoint types:

a concrete number already present in the thesis;
a researcher-view judgment sentence;
a process narration sentence;
a boundary or limitation sentence;
a supported contrast or counterexample;
a sentence that connects the discussion to a specific table, hypothesis, variable, coefficient, sample, or measurement choice.

Invalid breakpoint types:

random short sentence;
unsupported personal opinion;
invented data;
invented example;
generic sentence such as “This is important”;
artificial interruption that does not address D3, D4, D12, D14, D15, D16, or D17.

Output status:
```text
Gate E result: Pass / Rework Needed / Failed / N/A. If N/A, still state: "No external-highlighted long fragment, no boundary change, no over-3000-character revised fragment, and no over-cap split."
Original fragment count:
Revised fragment count:
Original max fragment characters:
Revised max fragment characters:
Aggregation-worsening signal: Yes / No
Fragment over 3000 characters: Yes / No
Breakpoint inserted: Yes / No / Not needed
Breakpoint type:
Breakpoint sentence:
Reason:
```
Mandatory failure rule:

- If revised_max_fragment_characters > 3000 and no valid breakpoint is inserted, mark the paragraph or section as Rework Needed.
- If the breakpoint introduces unsupported data, new theory, new citation, or changes the meaning, mark it as Failed.

#### Gate F: Word-Count Preservation Check

Purpose:
This gate guarantees that AI-score reduction did not shrink the paper. A thesis usually has a minimum word-count requirement, so any length loss is treated as a failure even if the AI score dropped.

Check, for every rewritten paragraph:
- original_word_count
- revised_word_count
- change_percent = (revised − original) / original × 100%

Rules:
- PASS if revised_word_count ≥ original_word_count. The 0% to +15% growth range applies only when the original paragraph is within the readability cap. If the original paragraph already exceeds 200 words or 12 sentences, do not pursue growth: preserve all substantive content, split only at safe boundaries, and compare the combined descendant word count against the original parent paragraph.
- REWORK NEEDED if revised_word_count < original_word_count. The fix must add specificity, a researcher-view judgment sentence, or process narration drawn from existing content — never restore length with filler or invented facts.
- A paragraph that fails Gate F cannot be output.
- Over-cap exception: if an ORIGINAL paragraph already exceeds the 200-word / 12-sentence hard cap, it may be split into two or more output paragraphs at natural logical breakpoints. In that case Gate F compares the COMBINED word count of all descendant paragraphs against the original parent paragraph, not each descendant separately. The paragraph-mapping record must show Parent Paragraph ID → New Paragraph IDs.
- Also compute, for the whole rewritten chapter: original_chapter_word_count, revised_chapter_word_count, and chapter change_percent. The chapter total must not be lower than the original chapter total.

Output status:
```text
Gate F result: Pass / Rework Needed
Original paragraph word count:
Revised paragraph word count:
Change percent:
Chapter original word count:
Chapter revised word count:
Chapter change percent:
```

#### Gate G: Structure and Readability Check

Purpose:
This gate prevents two readability failures: headings displaced or absorbed into body text, and merged mega-paragraphs that are exhausting to read. It enforces Principle 6.

Heading and boundary checks (per rewritten section):
- Same number of headings as the original, each with identical text and numbering.
- Every heading is on its own line, with a paragraph break before and after it, exactly as in the original.
- No heading appears inside a sentence or at the tail end of a body paragraph.
- No body text was merged across a heading.
- NO DUPLICATED OR ECHOED HEADING TEXT. The heading text must appear exactly once. Reject outputs where the heading or its words are repeated, such as "Part 1 Introduction 1 Introduction 1 Introduction" or "1.1 Research Background Research Background". The number, the title, and any leading "Part/Chapter" label appear once and are not echoed into the following line or the body's first sentence.
- The first body sentence after a heading must not restate the heading as a fragment (e.g. a heading "1 Introduction" must not be followed by a stray "1 Introduction").
- NO DUPLICATED TABLE OR FIGURE CAPTIONS. Each table caption ("Table 1. Total Variance Explained (N=134)") and figure caption ("Figure 1. Research Model") appears exactly once and is not echoed within the same line. Reject outputs like "Table 1. Total Variance Explained (N=134)1. Total Variance Explained" or "Table 10: Summary of Hypothesis Testing ResultsSummary of Hypothesis Testing Results". Treat table/figure captions with the same protection as section headings.
- Same number of paragraph units as the original, except when an original paragraph already exceeds the readability cap and is split at natural logical boundaries. Merging is always forbidden. Approved splits must be documented with Parent Paragraph ID → New Paragraph IDs, and Gate F must compare the combined descendant word count against the original parent paragraph.

Paragraph-length checks (per rewritten paragraph):
- word_count ≤ 200 (hard cap); flag if > 160 (soft target).
- sentence_count ≤ 12 (hard cap); flag if > 9 (soft target).
- A paragraph over either hard cap FAILS and must be split at a natural logical break or kept as the original separate paragraphs.

Over-polish and style-drift checks (per rewritten paragraph — guards against "the rewrite got more fluent and therefore more AI-like"):
- Did the rewrite make the paragraph noticeably more fluent, more native, or more journal-style than the author's own low-risk paragraphs (Author Style Baseline)? If yes, it has drifted toward AI style — Rework Needed, pull it back toward the author's baseline.
- Does the rewritten paragraph read as obviously more polished than the surrounding un-rewritten paragraphs of the same chapter (a visible "this paragraph was edited" seam)? If yes, Rework Needed — the goal is "same person wrote the whole chapter", not "this paragraph is better".
- Did the rewrite introduce new high-frequency connectives or a new fixed sentence template not present elsewhere in the author's writing? If yes, Rework Needed.
- Did the rewrite raise the author's apparent English level (smoother syntax, removal of all mild non-native naturalness)? If yes, Rework Needed — mild non-native register is a protective human signal, not an error to fix.

Output status:
```text
Gate G result: Pass / Rework Needed
Headings preserved on own line: Yes / No
Heading count original / revised:
Any heading text duplicated/echoed (e.g. "...Introduction 1 Introduction"): Yes / No
Any table/figure caption duplicated/echoed (e.g. "Table 1. Total Variance ...1. Total Variance ..."): Yes / No
Paragraph count original / revised (must match unless an over-long paragraph was split):
Any text merged across a heading: Yes / No
Any double-cased connector left in text ("or Or", "and And", "by By", "especially Especially"): Yes / No
Longest rewritten paragraph: __ words / __ sentences
Any paragraph over 200 words or 12 sentences: Yes / No
More fluent/native/journal-style than the author's own low-risk baseline: Yes / No
Visibly more polished than surrounding un-rewritten paragraphs: Yes / No
New connective or sentence template not in the author's own writing: Yes / No
```

Mandatory rule:
- If a heading was absorbed, moved, stranded, merged across, or its text duplicated/echoed, mark Rework Needed and restore the single clean heading exactly as in the original.
- If a table or figure caption was duplicated/echoed within the same line, mark Rework Needed and restore the single clean caption.
- If any double-cased connector remains in text ("or Or", "and And", "by By", "especially Especially", "Or or", "And and", etc. — a final-clean-up bug from rewriting), mark Rework Needed and delete the doubled token. Final output must contain NO such doubled tokens.
- If any rewritten paragraph exceeds 200 words or 12 sentences, mark Rework Needed and split it or restore the original paragraph breaks. Never solve AI risk by merging paragraphs.

#### Gate H: Grammatical Completeness and Sentence-Splitting Check

Purpose:
This gate prevents aggressive splitting from creating grammatically incomplete fragments or choppy, half-sentence prose. It enforces Principle 8.

This is a HARD, OUTPUT-BLOCKING gate. A single fragment anywhere blocks the whole chapter from being output.

**Detection method — UNIVERSAL completeness test, NOT pattern matching.**
Do NOT detect fragments by matching a fixed list of opening words (such as "Including / Drawing on / Using / Based on / Considering") or by looking only at a short 3–7 word window. That approach is a known failure: it misses fragments that start with any other word (e.g. "Work engagement, and creative inspiration.", "Workplace communities, and internal corporate channels."), and it misses long fragments that exceed the window. Fragments can start with ANY word and be ANY length.

Instead, apply this test to EVERY unit that ends in a period, one by one, regardless of its first word or its length:

```text
For each sentence S (text between two periods):
  1. Read S completely on its own, with NO surrounding text.
  2. Does S have its own grammatical SUBJECT?           (who/what the sentence is about)
  3. Does S have its own FINITE (tensed) main VERB?     (not just an -ing/-ed participle, not just a to-infinitive)
  4. Does S express a COMPLETE thought that can stand alone?
  If the answer to ANY of 2/3/4 is NO  →  S is a FRAGMENT  →  Gate H FAILS.
```

Fragments have many surface forms — the test above catches all of them. Common types (illustrative, NOT an exhaustive match-list):
- Continuation of a list: "...the mediating roles of self-efficacy. **Work engagement, and creative inspiration.**" → no finite verb, no subject of its own.
- A list split anywhere: "...through online social platforms. **Workplace communities, and internal corporate channels.**" → bare noun list.
- An enumeration split: "...generating. **Promoting, and implementing new ideas.**" / "gender. **Age, education level...**" / "dependent variable. **Gender, age...**" → bare list items.
- A gerund/participle continuation: "...statistical analysis. **Including multivariate analysis, including factor analysis...**" / "...the model. **Using SEM to test the paths.**" → "-ing" phrase with no finite verb. (These are the "gerund-continuation" fragments; there are often many of them — check every "-ing"-led unit.)
- A subject-less verb phrase: "...it raises the problem. **Builds the theoretical model.**" → has a verb but no subject.
- A standalone subordinate clause: "**When employees interact with AI in daily work.**" → dependent clause, no main clause.

Two fast heuristics to flag candidates for the full test above (they ASSIST the test, they do not REPLACE it — every period is still tested):
- A period followed by a word starting with a lower-case letter is almost always a wrong split → test it.
- A "sentence" that begins with a coordinating/subordinating connector or a participle — and / or / but / nor / including / such as / namely / by / through / when / because / although / which / while / since / as — OR ends without a finite main verb → test it.

Also reject, via the same per-sentence pass:
- Choppy runs: three or more consecutive ultra-short sentences (each under ~8 words) created by mechanical chopping.
- Over-long / over-nested sentences: any sentence longer than ~30 words or with more than two subordinate clauses.
- Thin / over-conversational sentences: a sentence that is grammatically complete but too shallow or chatty for a thesis, e.g. "It explains one specific thing.", "The opposite can also occur.", "This is important here." A single such sentence is acceptable only rarely for emphasis; two or more in a paragraph, or a "claim sentence + thin gloss sentence" pair like "Self-efficacy is especially important in social cognitive theory. It explains one specific thing.", FAILS. Merge the thin sentence back into the substantive one or add the specific content it is missing (from existing thesis material), keeping word count (Principle 4).

Quick test: read each sentence aloud on its own, with nothing around it. If it sounds like half a sentence, a dangling list, or "...and the rest got cut off", it is a fragment and FAILS. If you run out of breath or lose the thread, it is too long and FAILS.

Output status:
```text
Gate H result: Pass / Rework Needed
Total sentences tested (every period checked): N
Sentences beginning with a lower-case word: list / none
Sentences beginning with and/or/but/including/such as/by/when/because/which/-ing: list / none
Any sentence missing its own subject: Yes / No
Any sentence missing its own finite main verb (e.g. -ing/-ed/list/clause only): Yes / No
Any choppy run of 3+ ultra-short sentences: Yes / No
Any thin / over-conversational sentence ("It explains one specific thing." style): Yes / No
Any sentence over ~30 words or with >2 subordinate clauses: Yes / No
Shortest rewritten sentence (words):
Longest rewritten sentence (words):
Examples of any flagged fragments:
```

Mandatory rule:
- The chapter cannot be output while a single fragment remains. Test EVERY period, not a sample.
- If any fragment is found, mark Rework Needed and FIX IT by re-attaching the clause/list/verb-phrase/participle to its main clause (do not just delete it — keep the word count, Principle 4).
- When splitting a sentence, never place a period inside a list, before a bare verb, before an "-ing/-ed" continuation, or before a connector. Split only where BOTH sides independently pass the subject+finite-verb test (Principle 8).
- If a choppy run is found, merge the fragments back into properly formed sentences or vary the rhythm without ultra-short chopping.
- If a thin / over-conversational sentence is found, merge it into the substantive sentence next to it or add the specific content it lacks (from existing thesis material), restoring an academic register and keeping word count.
- If an over-long or over-nested sentence is found, split it into two complete sentences (Principle 8).
- Never leave a dependent clause, bare list, participle/“-ing” phrase, connector-led phrase, or subject-less verb phrase standing as its own sentence in the final output.

#### Gate I: Grammar and Subject-Verb Agreement Check

Purpose:
This gate ensures rewriting did not introduce grammar errors. It enforces Principle 9(a). Splitting and recasting sentences is the most common way subject–verb agreement breaks, so check it explicitly.

Check every rewritten sentence:
- Subject–verb agreement: does each verb match the number of its actual subject? Pay special attention to sentences that were split or had their subject changed (typical real failures: "we examines → we examine"; "Creative suggestions generated by generative AI is expected → are expected"; "This items were revised → These items were revised").
- Sentence-initial capitalization: every sentence (including sentences after a split) starts with a capital letter. Common real failure: a sentence starts with a lower-case word such as "the following hypothesis is put forward" or "within employee–AI collaboration" — these must be capitalised.
- Demonstrative agreement: `This` for singular, `These` for plural. "This items" is wrong; "These items" is correct.
- Tense consistency with the surrounding text.
- Correct articles (a/an/the), prepositions, and singular/plural forms.
- No words accidentally dropped or duplicated during editing.
- No spelling errors — read every proper noun and every key term (e.g. "Creative Inspiration" must not appear as "Crearive Inspiration"). Spelling errors in tables and captions are especially easy to miss; check them.
- No typos introduced or left in: misspelled common words, wrong-word substitutions, or transposed letters. If the rewrite touched a sentence, its spelling must be clean.
- No double (or multiple) spaces: exactly one space after a period before the next sentence; no stray double spaces inside sentences. Flag and fix any "  " (two spaces) introduced by editing.
- No literary arrow "→" in body prose. A relationship written as "self-efficacy → employee innovative behavior" must be recast into words, e.g. "the effect of self-efficacy on employee innovative behavior". The "→" is allowed ONLY inside tables (e.g. a path-coefficient table cell like "SE → IB"), never in running text.
- Citation-punctuation placement. A parenthetical citation belongs inside the sentence it supports, with the sentence-ending period AFTER the closing parenthesis, not before the citation. Flag and fix a stray period (or other terminal punctuation) sitting immediately before an opening citation parenthesis. Wrong: "...and collaborative learning. (Nagubathula, 2025)." → Right: "...and collaborative learning (Nagubathula, 2025)." A narrative citation is the other correct form: "Yang et al. (2025) investigated the effect of...". (Do not touch the internal punctuation of multi-author abbreviations like "et al." — only the stray period directly before "(Author, year)".)
- No deliberately inserted "non-native" errors — plainness is allowed, errors are not.

Output status:
```text
Gate I result: Pass / Rework Needed
Subject-verb agreement correct in all sentences: Yes / No
Every sentence starts with a capital letter: Yes / No
Demonstratives (This vs These) agree with number: Yes / No
Any tense / article / preposition error: Yes / No
Any spelling error or typo (especially in tables/captions/key terms): Yes / No
Any double space, or literary "→" in body prose (allowed only in tables): Yes / No
Any stray period directly before a "(Author, year)" citation: Yes / No
Example of any flagged grammar issue:
```

Mandatory rule:
- If any grammar, capitalization, demonstrative, or spelling error is found, mark Rework Needed and correct it. The final output must be grammatically and orthographically correct academic English; AI-feature reduction is never an excuse for any of these errors.

#### Gate J: Logic-Flow, Mechanical-Repetition, and Meta-Commentary Check

Purpose:
This gate prevents jarring insertions, logic jumps, mechanical "outline-expansion" prose, and AI-flavored over-polished phrasing. It enforces Principle 9(b).

Check each rewritten paragraph:
- Does every sentence follow logically from the one before it and lead into the one after it?
- Is there any inserted aside that explains or justifies the writing or research design from outside the argument (e.g. "This detail was included to improve measurement precision.", "This sentence clarifies the logic.")? Such meta-commentary must be removed or rewritten into a sentence that belongs to the argument.
- Do any researcher-trace (T19) sentences read as natural authorial reasoning, connected to both neighbours — rather than as a generic justification dropped in to vary the text?
- Are there abrupt topic jumps where a transition is missing?
- LOW-INFORMATION "CORRECT FILLER": does a passage (especially research background, theoretical significance, practical significance) say the same correct-but-generic things in slightly different words across several sentences — e.g. "AI supports employees / innovative behavior matters / organizational support affects innovation / psychological states affect behavior" — without adding a specific research context, a literature difference, or a problem tension? Padding that is correct but low-density reads as machine-generated and as "long set-up, shallow argument". Flag it: tighten by adding specificity from existing thesis content (a concrete context, a contrast between cited studies, a stated tension), not by deleting (Principle 4 — keep word count; raise density, do not cut).
- MECHANICAL REPETITION: are three or more sentences in the paragraph starting with the same subject ("This study… / The study… / It…") or is a chapter-arrangement paragraph written as "Chapter X does…" line after line? If so, it reads as expanded outline, not integrated prose — apply T23 (information-progression rewrite). Note: simply swapping "This study" for "The present research / This paper" does NOT fix it.
- OVER-POLISHED OR BUSINESS-TALK AI PHRASES: does the text contain any of the following?
  - Over-polished journal-style: "it is noteworthy that", "more importantly", "sheds light on", "offers a nuanced understanding", "fills a critical gap", "plays a pivotal role", "underscores the significance", "delve into", "a rich tapestry", "a testament to", "navigate (when not literal)", "leverage (= use)", "realm", "embark on", "cornerstone", "synergy", "holistic (undefined)", "streamline", "cutting-edge", "foster", "showcase", "multifaceted", "intricate", "paradigm (outside philosophy of science)";
  - Additional single-word AI-isms (replace with the plain word): "utilize" (= use), "commence" (= begin), "ascertain" (= determine/find out), "endeavor" (= effort/attempt), "meticulous(ly)" (= careful/precise), "beacon", "nestled" (= located/sits), "vibrant"/"thriving"/"bustling" (= active/growing, or cite a figure), "daunting" (= difficult), "boasts" (= has), "ever-evolving" (= changing), "learnings" (= lessons/findings), "watershed moment" (= turning point), "due to the fact that" (= because), "in order to" (= to). Replace only the vague rhetorical use; the discipline-exemption safeguard below still applies.
  - Business-blog / explainer style (inappropriate in a master's thesis): "the practical upshot is that", "what this tells us is that", "looking at this more closely", "breaking this down", "the takeaway is", "the bottom line is", "what this comes down to is that", "what these findings point to is that", "taking the full set of results", "when we step back", "at the end of the day";
  - Persuasive-authority tropes and signposting throat-clearers (an AI tell: they announce depth or a turn instead of delivering content, and usually precede an ordinary point dressed up with ceremony): "the real question is", "what really matters (here) is", "at its core" / "at the heart of (X)", "the heart of the matter", "the deeper issue is", "fundamentally" (used as a throat-clearer, not as a precise technical qualifier), "in essence", "let us now delve into", "let us now turn to", "this section will explore / sheds light on" (as a bare announcement). The fix is to state the point directly and keep its content (Principle 4): delete only the empty framing, never the substantive claim that follows. Do NOT flag a genuine signpost that carries real information (e.g. "Section 4 reports the regression results before the robustness checks"), and do not flag "fundamental" where it is a correct technical term (a fundamental frequency, a fundamental theorem).
  - Template-contribution phrases used repeatedly: "this study broadens", "this study also helps explain", "another theoretical contribution lies in", "based on these gaps, this study" — when one of these recurs across paragraphs it becomes a new template (apply T23).
  - Common cliché openers/closers (frequent in machine-assisted English theses by non-native writers): "with the development of ...", "with the rapid development of ...", "in recent years, ... has attracted increasing attention", "has important theoretical and practical significance", "in summary / to sum up / in a word", "the possible innovation of this paper lies in", "on the basis of the above analysis", "there is a lack of in-depth research on ...". Replace each with a concrete, content-specific statement — e.g. instead of "has important theoretical and practical significance", state the specific finding and who it matters to; instead of "with the development of AI", open from the actual phenomenon or problem. Deleting a redundant connector is fine, but do not just delete the sentence's content (Principle 4).
  These must be replaced with plain academic connectives ("To address this issue,", "For this reason,", "In this model,", "This means that,", "The next step is to examine,", "The analysis then considers,").
  DISCIPLINE-EXEMPTION SAFEGUARD: a flagged word is NOT changed when it is standard terminology in the paper's own field used in its literal/technical sense — e.g. "robust estimator" / "robust standard errors" in statistics, "paradigm shift" in philosophy of science, "landscape" in ecology/geography, "navigate" in wayfinding research, "leverage" in finance. Replace only the vague rhetorical use, never the discipline-standard technical use; when unsure whether a term is technical here, keep the original.
- EMPTY-COMPARISON / EMPTY-CLAIM PATTERNS (common in empirical and CS/ML prose): does the text make a comparison or capability claim without the specific referent it needs? Flag and make concrete:
  - "outperforms existing methods" → name which methods, on what metric;
  - "achieves superior / state-of-the-art performance" → give the number and the dataset;
  - "demonstrates the effectiveness of" → point to the specific experiment that shows it;
  - "various / multiple / diverse datasets (or settings)" → list them;
  - "a wide range of" → give the actual range.
  The fix adds the specific referent already present in the paper (dataset name, metric, baseline, number); it never invents a comparison the paper does not contain (Gate B / no-fabrication).
- TOO-CLEAN PARALLELISM AND "THREE-ITEM-LIST SMELL": AI prose tends toward suspiciously tidy parallel triples ("efficient, accurate, and robust"), three-item lists where two would do, and every paragraph ending on a forward-looking summary line. Where a triple is not substantively three distinct things, break the symmetry: use asymmetric phrasing, drop a redundant item, or let some paragraphs end on a concrete fact instead of a meta sentence. Do not delete real content; only de-pattern decorative symmetry.
- COPULA AVOIDANCE: AI inflates a plain "is/are" into "serves as", "acts as", "plays the role of", "functions as", "represents" (Chinese: "作为…的代表", "扮演着…的角色", "体现了"). Where the sentence simply asserts identity, restore the plain form. Meaning unchanged; only the inflated linking phrase is simplified.
- ELEGANT VARIATION (same entity renamed across sentences): AI/over-editing avoids word repetition by referring to one entity with a rotating set of synonyms within a short span — e.g. "the participants" → "the respondents" → "the interviewees" → "these individuals" all for the same group, or a variable called three different things across adjacent paragraphs. This is an AI tell AND it harms academic precision. Fix by choosing ONE correct term and using it consistently — never by adding yet another synonym. This is the same principle as the Anti-Synonym Rewrite Priority Rule and the term-consistency requirement (one concept = one term); a technical term, variable name, hypothesis label, or participant label must stay identical on every mention. (Do not over-apply to genuinely distinct referents, and pronouns used normally are fine.)
- FORMULAIC "DESPITE X … OFFERS Y" CONCLUSION: AI conclusions often follow a fixed contrastive template — "Despite [challenges/limitations], [the field/this study/the situation] offers [benefits/opportunities/promise]…" (and the "While there are obstacles, the future remains bright" variant). When the original conclusion uses this rigid frame, recast it into a direct statement of what the study actually concludes, grounded in its real findings and stated limitations; do not add optimism or implications the thesis does not support.
- SUPERFICIAL CAUSAL CHAINS: a single sentence carrying two or more stacked connectives that fake analytical depth ("...thereby enabling..., thus promoting..., which in turn..."; Chinese: 一句挂 2 个以上 "从而/进而/由此"). Split the chain into separate sentences or delete the links that add no real information. Never add a new causal claim the source did not make.
- ANTITHESIS TEMPLATE: "It's not X — it's Y" / "This isn't about X, it's about Y" is a recognisable AI cadence. In academic prose, rewrite as a direct positive statement of the actual claim; keep at most one such construction in a whole document and only if it genuinely serves the argument.
- HEDGE-STACKED PREDICTIONS: stacking a modal with a hedge adverb ("could potentially", "may eventually", "might ultimately") asserts nothing while sounding cautious. Keep one hedge, not two: "could create" or "potentially creates", never "could potentially create". This never overrides the protected single hedges in Gate B (a lone "may"/"suggests" stays).
- CLUSTER / DENSITY TIERING (apply to reduce false positives, adapted from the avoid-ai-writing tiered model): treat the flagged-word banks in tiers rather than as a flat always-replace list.
  - Tier 1 (always replace): the clear AI-isms above — replace on sight.
  - Tier 2 (flag in clusters): words that are fine alone but signal AI when two or more appear in the same paragraph (e.g. harness, elevate, unleash, empower, bolster, spearhead, resonate, revolutionize, facilitate, underpin, nuanced, crucial, encompass, cultivate, illuminate). Replace these only when 2+ co-occur in a paragraph, or when one is clearly rhetorical.
  - Tier 3 (flag only at high density): ordinary words AI overuses (significant, innovative, effective, dynamic, compelling, robust, sophisticated). Replace some with specifics (numbers, comparisons) only when they saturate the text (roughly 3%+ of words); do not hunt every instance.
  The point of tiering is to avoid over-editing a non-native author's normal vocabulary into something flatter and, paradoxically, more AI-like (consistent with the Author Style Baseline Rule).

Output status:
```text
Gate J result: Pass / Rework Needed
Any out-of-place meta-commentary found: Yes / No
Any logic jump / missing transition: Yes / No
Three+ sentences with same "This study/It" subject, or outline-style chapter intro: Yes / No
Any over-polished AI phrase present: Yes / No
Any low-information "correct filler" passage (generic restatement without specific context): Yes / No
Example of any flagged insertion:
```

Mandatory rule:
- If out-of-place meta-commentary or a logic jump is found, mark Rework Needed. Remove the aside or rewrite it so the paragraph reads as one continuous line of the author's reasoning.
- If mechanical repeated-subject or outline-style structure is found, mark Rework Needed and apply T23 (change the information progression, do not just swap the subject word).
- If an over-polished AI phrase is found, mark Rework Needed and replace it with a plain academic connective.
- Do not keep any sentence that justifies the methodology or the rewrite from outside the argument.

Output status:

```text
Overall Phase 7 Quality Gate Result: Pass / Rework Needed / Failed
Gate A result:
Gate B result:
Gate C result:
Gate D result:
Gate E result:
Gate F result:
Gate G result:
Gate H result:
Gate I result:
Gate J result:
Protected Elements Changed: Yes / No
Breakpoint Required: Yes / No
Breakpoint Inserted: Yes / No / Not needed
Word count preserved: Yes / No
Headings and paragraph breaks preserved: Yes / No
All sentences grammatically complete (no fragments): Yes / No
No heading text duplicated/echoed: Yes / No
No mechanical repeated-subject / outline-style paragraphs: Yes / No
No over-polished AI phrases: Yes / No
All sentences within ~30-word / two-clause limit: Yes / No
Subject-verb agreement correct: Yes / No
No double hyphen "--" and all hyphenated compounds intact: Yes / No
No Unicode em dash "—" left in body prose: Yes / No
No out-of-place meta-commentary: Yes / No
Longest rewritten paragraph (words / sentences):
Action Taken:
```


### Phase 8: Summary Stats

Phase 8 must output statistics for the evaluated scope. State Scope = Full document / Target chapter / Selected batch / Highlighted fragment. Only Scope = Full document may be labelled an overall_document_internal_risk_estimate; a single-chapter or batch scope is a target_unit_internal_risk_estimate. The statistics are:

```text
average_paragraph_risk:
high_risk_share:
medium_risk_share:
section_repetition_score:
scope_pattern_floor:
final scope-appropriate risk index (overall_risk_index only for a fully diagnosed document scope; otherwise target_chapter_risk_index / batch_risk_index / fragment_risk_index):
original_chapter_word_count:
revised_chapter_word_count:
chapter_word_count_change_percent:
word_count_preserved (chapter total ≥ original): Yes / No
judgment:
reason for judgment:
```


Do not only provide the threshold table. If any required statistic is missing, mark the task as:
Revision Incomplete — Missing Phase 8 Summary Stats.



Use stricter internal thresholds:

| Scope risk index (overall / target chapter / batch / fragment) | Judgment | Target status |
|------------------|----------|---------------|
| ≤8% | Low internal risk estimate, but still manually check repeated structures | Internally below target; externally DONE only after a comparable external re-test is below target (when the task uses external scores) |
| 9-15% | Mild internal risk; revise repeated openings/endings | Internally below target; external DONE only if a comparable external re-test is below target |
| 16-25% | Moderate internal risk; revision recommended | Internally below target; external DONE only if a comparable external re-test is below target |
| 26-29% | Approaching target; one more light round usually clears it | Below 30% — done if external re-test confirms |
| 30-35% | At/above target; keep rewriting and escalate (Principle 5) | ABOVE target — NOT done |
| 36-50% | Very high risk; strong rewrite required | ABOVE target — NOT done |
| >50% | Severe risk; major rewrite required | ABOVE target — NOT done |

Note: the internal score is only an estimate. The completion decision is made on the EXTERNAL re-test, not the internal score. Any chapter or document whose external score is ≥ 30% (or the user's target) is NOT done, no matter how low the internal estimate is.

### Phase 9: Output

Generate:

1. **Detection Report** — Table with paragraph #, section, D1-D17 scores, total dimension score, paragraph_risk_index, hit dimensions, pattern floor applied, rewrite strategy, and dimension coverage status.
2. **Dimension-to-Technique Execution Plan** — For each rewritten paragraph, show which dimensions were targeted and which techniques were used.
3. **Three-Pass Rewrite Evidence** — Show Pass 1, Pass 2, and Pass 3 actions for each rewritten paragraph or section.
4. **Protected Elements Check Report** — List the protected elements extracted before rewriting and confirm their exact form after rewriting. Do not only write “all preserved.”
5. **Phase 7 Quality Gate Report** — Show Gate A through Gate J results for each rewritten paragraph or rewritten fragment cluster.
6. **Rewritten Target Unit** — the rewritten target chapter, selected batch, or rewritten paragraph group for the current round, with rewritten paragraphs highlighted or clearly separated. Do not output or regenerate untouched chapters merely to present a full-paper version.
7. **Revision Summary** — Major AI-like patterns reduced and paragraphs requiring manual review.
8. **Score Regression / Baseline Check** — If a comparable external re-test result is available, compare it against the chapter red line. If only a baseline version or pre-rewrite detector score is available, state: “External score regression cannot be judged until a comparable re-test is provided,” and compare only internal risk patterns, protected elements, word count, and structural changes.

The Score Regression Check must include:
- baseline version name;
- baseline AI score;
- revised version name;
- revised AI score;
- score change;
- judgment: Improved / No Clear Change / Regressed;
- target status: Below target (<30%) / Still above target;
- action: if below target → Mark chapter done, move to next chapter above target; if improved but still above target → Continue with next escalation rung on the same chapter; if no change/regressed → Roll back to baseline and try the next escalation rung;
- next target chapter and next escalation rung (unless every chapter is below target).

If no external detector result is available, write:
“External detector result not available; score regression check pending.”

When only a baseline (and no comparable new external re-test) is available, the Score Regression Check is a pre-retest check: it may compare internal risk estimate, word count, structure, and protected elements, but it must NOT claim any external-score improvement until the user provides a comparable external re-test of the revised version.

Mandatory output rule:
- Do not provide only the rewritten document.
- A rewritten document without execution evidence is not a valid final output under this skill.

Final output cannot be marked complete unless items 1–7 are included.

If an external detector score, external detector report, or baseline version is available, item 8 is also mandatory.

If item 8 is required but missing, mark the task as:

```text
Revision Incomplete — Missing Score Regression Check
```

---


## External Risk Regression Rule

When two comparable detector streams both remain above target, the revision is not complete. It is structurally unsuccessful only if a comparable re-test shows no improvement or regression relative to the baseline within the SAME detector stream (a drop from 80% to 45% is still above target but is progress, not failure). Scores from different detectors are separate evidence streams and are not pooled into a single "consensus" number.

| External Result Pattern | Status |
|---|---|
| One detector high, one low | Review shared high-risk sections manually |
| Both detectors above 30% | Not complete; continue structural rewriting |
| Both detectors above 40% | Not complete: classify as insufficient rewrite and continue up the escalation ladder. Do NOT call it a failed direction unless a comparable re-test actually shows regression or zero improvement. |
| One detector above 60% and the other above 40% | Severe structural risk; return to Universal External-Risk Calibration Rule |

Mandatory rule:
- If multiple external reports / strong external risk remain high, do not mark the output as complete.
- Do not continue the same rewrite direction if the text became smoother, longer, or more template-like.
- Return to the baseline version or the lowest-risk version and rebuild the P0 sections first.



## Key Principles

- **Match the author, not "good English"**: The rewrite target is the author's own real writing, recovered from their thesis's existing low-risk paragraphs (Author Style Baseline) — sentence length, connectives, recurring phrasings, and mild non-native register. Do NOT polish a non-native master's thesis into fluent journal prose; over-polishing is a common way to make text read MORE like AI. A rewritten paragraph that is more fluent/native/journal-style than the author's baseline, or visibly more polished than the surrounding un-rewritten paragraphs, fails Gate G and is pulled back. Mild already-present non-native naturalness is a protective human signal, preserved — not an error to fix (Gate I still forbids real new errors).
- **Scope & honesty**: This skill revises existing user-provided thesis text and flags writing-pattern risk. It must not generate ungrounded thesis sections, fabricate research evidence, or claim a guaranteed detector outcome. Any external AI-detection result is a post-revision observation, not a promise; detectors are probabilistic and update over time.
- **Evidence-based authorship restoration, not "human-trace faking"**: The sanctioned way to sound more human is T29 — restore the grounded judgment, method rationale, and evidence-boundary statements a real researcher writes, using ONLY content already in the paper. Forbidden forever: deliberate errors, fake non-native flaws, colloquial/emotional asides, fabricated researcher feelings/process/quotes, or any detection-evasion trick. If a sentence can't be traced to the paper's own data/method/theory/cited work, it is fabrication and must not be added.
- **Target-driven, never stop early**: Success is every externally measured chapter below 30% (default) — plus the whole document when a comparable whole-document score is available — not merely "lower than before". Keep rewriting and escalating (Principle 5) until each chapter is below target. The lowest-ever score is a no-regression ceiling, not a stopping point. Only a chapter already below target is done; never present an above-target version as final.
- **Closed loop, one chapter per round**: Internal scoring cannot predict the external result. Rewrite one chapter, have the user re-test it. If still above target, run another round on the same chapter at a higher escalation rung; if below target, move to the next chapter. Never rewrite the whole thesis in one pass.
- **Escalation ladder (Principle 5)**: A stubborn chapter is pushed down through progressively stronger but still safe rungs — sentence → rhythm → paragraph architecture → reporting-sequence/template breaking → source-extracted researcher-trace integration → functional reorganisation — never by regeneration or compression.
- **Minimal edit, never regenerate**: Keep the original human wording wherever possible. Edit existing sentences (substitute, reorder, split, recast). Whole-paragraph regeneration is the biggest cause of score regression and is forbidden.
- **Never shrink the paper**: AI features are reduced by changing how ideas are expressed, never by compressing, merging, or deleting. Every rewritten paragraph must be at least as long as the original (Principle 4).
- **Preserve structure and readability**: Never merge paragraphs and never move or absorb section headings. Each heading stays on its own line; each rewritten paragraph stays under ~160 words / ~9 sentences (hard cap 200 words / 12 sentences). Cross-paragraph repetition is fixed by differentiating paragraphs, not combining them (Principle 6, Gate G).
- **Correct, natural sentences**: Every sentence is grammatically complete (no clause/list/verb-phrase/`-ing`-continuation fragments — Gate H uses a UNIVERSAL syntactic-completeness test on every period, not a fixed-prefix scan; output-blocking) and a sensible length (no choppy ~10-word fragments and no tangled sentences over ~30 words or two clauses). Grammar, subject–verb agreement, sentence-initial capitalization, This/These number agreement, and proper-noun spelling stay correct (Principle 9, Gate I). Never use "--"; keep hyphenated compounds and en-dash ranges intact (Gate D). Headings and table/figure captions appear exactly once with no duplication/echoing or doubled-case connectors like "or Or" (Gate G). Never drop in jarring meta-commentary like "This detail was included to improve measurement precision." (Principle 9, Gate J).
- **Integrated prose, not outline-expansion**: Fix paragraphs where three+ sentences start with "This study… / It…" or chapters are listed as "Chapter X does…" by changing the information progression (T23: object-as-subject, problem→reason→handling, research-flow), not by swapping the subject word. Avoid over-polished AI phrases ("sheds light on", "fills a critical gap", "more importantly") AND business-talk phrases ("the practical upshot is", "what this tells us is", "looking at this more closely"); use plain academic connectives (Gate J).
- **Research-design–aware**: T19 (researcher-trace) and T24 (Introduction/Abstract anti-template) branch into quantitative vs qualitative versions. T19 is EXTRACTION-ONLY — it relocates existing thesis material into the right place; it never generates a new "researcher-voice" sentence, because any LLM-generated sentence reads as AI to a detector. T24 has T24-A (quantitative) and T24-B (qualitative) anti-template strategies for these two highest-risk sections. Qualitative papers also get dimensions D18–D21 (transition templating, theme-presentation uniformity, researcher-voice absence, quote-balance uniformity) and techniques T25–T28. Crucially, all qualitative de-templating uses ONLY material already in the paper — never fabricate researcher feelings, positionality, non-verbal detail, quotes, or silences (integrity rule + it would read as AI anyway).
- **Stop when grinding stops paying**: Rewrite Fatigue Detection (Principle 5) halts a chapter after 3 rounds, < 3pp gain across two rounds, or any regression, and asks the user to choose between trying a clearly untried technique or stopping and seeking external editing — instead of grinding stale rounds that may make the text worse.
- **Target lock**: Each round touches only ONE highest-scoring chapter by default (two only by explicit user request); everything else is left untouched.
- **Academic integrity first**: Only reduce detectable patterns; never alter factual content, citations, data, hypotheses, or statistical conclusions.
- **External-detector-calibrated caution**: If internal scoring is far lower than CNKI, Turnitin, GPTZero, Originality.ai, or another external detector, assume the internal scoring is under-sensitive and raise the risk level.
- **Structure matters more than words**: Repeated paragraph architecture can create high AI risk even when individual sentences look acceptable.
- **Preserve meaning**: Rewriting must maintain original argument, evidence, and conclusions.
- **Context-aware**: Literature review, hypothesis development, and discussion sections require stricter scoring because they often contain repeated AI-like academic templates.
- **Non-native thesis style**: The target is formal but not over-polished English, suitable for a competent non-native master’s student.
- **Execution evidence required**: The skill must not only rewrite text. It must show how detected dimensions were addressed, how the three-pass protocol was executed, and how protected elements were checked.
- **No fake three-pass execution**: Do not claim that Pass 1, Pass 2, and Pass 3 were completed unless each pass has visible evidence.
- **No random rhythm manipulation**: Short sentences may be used only when they solve a detected AI-risk dimension. Random short-sentence insertion is not an acceptable rewrite strategy.
- **Protected elements are locked**: Citations, variables, abbreviations, hypotheses, statistics, capitalization, and table/model labels must be extracted before rewriting and compared after rewriting.

## Reference Files

Architecture: the main SKILL.md holds the operating architecture, task/language routing, the round workflow, the Phase 7 Gate A–J definitions, and the cross-cutting rules. The detailed catalogues — the 21 detection dimensions (D1–D21) and the 29 rewrite techniques (T1–T29) — are NOT duplicated in this file; they live in the reference files below and are loaded on demand. This keeps the main file focused on "how to run a round" while the references hold "the full list of what to look for and how to fix it".

- `references/detection_principles.md` — Multi-detector AIGC trace analysis (D1–D17 core + D18–D21 qualitative supplement).
- `references/rewrite_methods.md` — Multi-detector rewriting techniques and thesis-safe revision methods.
- `references/chinese_text_ai_risk.md` — Chinese-language text high-risk phrase reference (template openings/closings, unsupported intensifiers, repetition blocks) for when the revised text itself is in Chinese; hint list, never overrides term/data protection.
- `references/qualitative_authorship_restoration.md` — Qualitative-specific extension of T29: evidence-based authorship restoration rules, methodology-compatibility table, and integrity checks for qualitative/mixed-methods passages.


Note:
For documents with more than 50 body paragraphs, staged or batch output is recommended (Phase 1.5, Phase 2, Phase 4.5, Phase 5.5, and Phase 7), and compact skip records may be used for low-risk/non-target paragraphs; the user should expect multiple rounds. For more than 80 body paragraphs, staged execution is mandatory (see the Mode Selection table).

For long documents, do not promise a complete rewrite in one response.

## Usage Example

→ Stage 1: External report review + diagnosis + Chapter Version Ledger + target-lock (pick ONE highest-scoring chapter; two only by explicit user request)
→ Stage 2: Rewrite ONLY the target chapter(s) by minimal edit, with evidence
→ Stage 3: Quality gate (including Gate A minimal-edit check and Gate E breakpoint check)
→ Stage 4: Summary stats + chapter output
→ Stage 5: STOP — user re-tests the chapter; improved → lock and continue; not improved → roll back and retry

```text
User: "降低这篇论文的AI率"
→ Upload .docx + external detector report
→ Phase 1: Parse paragraphs and identify section type
→ Phase 1.5: Scan full-document repeated patterns
→ Phase 1.6 / 1.6A / 1.7: Architecture review, external abstraction, D16/D17 pre-scan
→ Build Chapter Version Ledger; target-lock ONE highest-scoring chapter (two only by explicit user request)
→ Phase 2a/2b: Score 17 dimensions and apply floors (for target chapters)
→ Phase 4 / 4.5 / 4.5A: Minimal-edit strategy, technique plan, resource allocation
→ Phase 5 / 5.5: Minimal-edit three-pass rewrite of target chapters only, with evidence
→ Phase 7: Quality gate (Gate A–J, including word-count, structure/readability, grammatical completeness, grammar/subject-verb, and logic-flow checks)
→ Phase 8 / 9: Summary stats + output for this round
→ STOP: ask user to re-test the rewritten chapter before the next round
```
```