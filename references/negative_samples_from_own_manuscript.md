# Negative Samples from Own Manuscript

This file stores negative and caution examples from `raw_modification_log.md`. It is used to prevent the sentence-polishing skill from learning unsafe behaviors from the author's manuscript revision history.

It does not provide paragraph-level rewriting rules. It does not teach the skill to add mechanisms, citations, claims, or manuscript logic.

## Label System

- `overclaim`: claim strength is too high.
- `vague_subject`: subject is generic or template-like.
- `decorative_verb`: verb sounds ornate rather than precise.
- `template_phrase`: repeated phrase such as `giving rise to`.
- `invented_compound`: newly coined compound term.
- `undefined_term`: central term is introduced without a safe definition.
- `heavy_nominalization`: noun chain hides the action.
- `stage_unclear`: temporal or stage relation is unclear.
- `latex_risk`: LaTeX, variables, citations, labels, or units must be protected.
- `typo_or_intermediate_draft`: teacher/intermediate version contains spelling, spacing, or grammar errors.
- `out_of_scope_rewrite`: revision changes title, storyline, paragraph function, evidence chain, mechanism, literature bridge, or technical definition.
- `partial_learning_only`: only one local pattern can be learned.
- `author_confirm_required`: safe revision requires author confirmation.

## Usage Rule

Each sample below has a `Must not learn` field. That field is the most important part of this file.

Do not import these samples directly into `SKILL.md`. Use them first as a guardrail corpus when testing whether sentence polishing stays local and conservative.

## Expression-Level Local Samples

## NEG-001: Temporal sequence needs a light connector

Source ID: A-005  
Original or source signal: `from a single peak to separated peaks and back to one peak`  
Teacher/local version: `from a single peak to separated peaks, then back to one peak`  
Problem labels: `stage_unclear`, `template_phrase`  
Safe local correction: Add `then` or `followed by` when the temporal order is already present.  
May learn: Use a light connector to clarify sequence.  
Must not learn: Do not add a new stage, mechanism, or process endpoint.  
Scope: sentence-level.

## NEG-002: Diagnostic claim too strong

Source ID: A-009  
Original or source signal: `establishes NMR $T_2$ evolution as a quantitative diagnostic of dissolution mechanisms`  
Teacher/local version: `quantitative NMR signatures as diagnostic indicators for tracking dissolution dynamics`  
Problem labels: `overclaim`, `latex_risk`  
Safe local correction: Downgrade a full diagnostic claim to an indicator/tracking claim when evidence is local.  
May learn: Use `diagnostic indicators for tracking...` when the text supports indicators rather than complete mechanism diagnosis.  
Must not learn: Do not strengthen NMR or $T_2$ claims beyond the evidence.  
Scope: sentence-level with evidence-strength control.

## NEG-003: Repeated regime description is overloaded

Source ID: I-003  
Original or source signal: repeated `giving rise to`; `approximately throughout the entire domain`; multiple regime sentences.  
Teacher/local version: compressed regime descriptions using `localizes`, `focus flow`, `form wormholes`, and `whereas`.  
Problem labels: `template_phrase`, `decorative_verb`, `heavy_nominalization`  
Safe local correction: Remove redundant degree words and replace repeated template phrasing with direct verbs.  
May learn: Compress repeated explanatory structures while preserving regime distinctions.  
Must not learn: Do not delete necessary regime boundaries, citations, or physical contrasts.  
Scope: sentence-level to local multi-sentence compression.

## NEG-004: Vague literature subject

Source ID: I-006  
Original or source signal: `Extensive efforts have identified...`  
Teacher/local version: `Extensive experimental and numerical studies have identified...`  
Problem labels: `vague_subject`  
Safe local correction: Replace vague subjects with concrete study types when the source text already lists those types.  
May learn: Prefer concrete literature subjects over generic `efforts`.  
Must not learn: Do not broaden the literature scope or add methods not present in the sentence.  
Scope: phrase-level.

## NEG-005: Mechanism relation needs cautious connector

Source ID: I-007  
Original or source signal: `show that transport-reaction competition... produce...`  
Teacher/local version: `show how transport-reaction competition... produce...`  
Problem labels: `clarify_causal_link`  
Safe local correction: Use `show how` only when the cited studies genuinely explain a process.  
May learn: Clarify mechanism relation with a small connector change.  
Must not learn: Do not turn a result statement into a mechanism explanation without support.  
Scope: phrase-level; author-confirm if mechanism support is unclear.

## NEG-006: Method sentence too passive and inserted

Source ID: M-002  
Original or source signal: `A two-dimensional... model ... was used to simulate...`  
Teacher/local version: `We use an open source two-dimensional... model... to simulate...`  
Problem labels: `heavy_nominalization`, `latex_risk`  
Safe local correction: Use restrained active voice in methods when it preserves model capability and provenance.  
May learn: `We use X based on Y to simulate Z`.  
Must not learn: Do not alter model capability, provenance, citations, or governing assumptions.  
Scope: sentence-level methods polishing.

## NEG-007: Parameter-introduction wording

Source ID: M-005  
Original or source signal: `parameterised by the P\'{e}clet number and Damk\"{o}hler number`  
Teacher/local version: `characterized by the P\'{e}clet number and Damk\"{o}hler number`  
Problem labels: `latex_risk`, `standard_term`  
Safe local correction: Use common parameter-introduction wording when the definition is unchanged.  
May learn: `is characterized by` for introducing dimensionless numbers.  
Must not learn: Do not change Pe/Da definitions, equations, spelling commands, or technical meaning.  
Scope: phrase-level.

## NEG-008: Module handoff phrasing

Source ID: M-008  
Original or source signal: `exported ... for NMR simulation module, together with...`  
Teacher/local version: `were exported to the NMR simulation module alongside...`  
Problem labels: `template_phrase`, `latex_risk`  
Safe local correction: Use `exported to... alongside...` for module handoff sentences.  
May learn: Clarify object, destination, and attached data.  
Must not learn: Do not add, remove, or rename data products.  
Scope: sentence-level.

## NEG-009: Heading capitalization

Source ID: R-002  
Original or source signal: `\subsection{NMR $T_2$ Response from Dissolution patterns}`  
Teacher/local version: `\subsection{NMR $T_2$ Response from Dissolution Patterns}`  
Problem labels: `latex_risk`  
Safe local correction: Fix title case if the journal/manuscript style requires it.  
May learn: Treat heading capitalization as formatting, not content.  
Must not learn: Do not rewrite section titles or change labels during sentence polishing.  
Scope: format-level only.

## NEG-010: Template phrase in result mechanism

Source ID: R-007  
Original or source signal: `giving rise to a transient bimodal feature in the $T_2$ distribution`  
Teacher/local version: `producing a transient bimodal feature in the $T_2$ distribution`  
Problem labels: `template_phrase`, `latex_risk`  
Safe local correction: Replace repeated `giving rise to` with `producing`, `forming`, or `leading to` when causality is already stated.  
May learn: Prefer direct result verbs for local physical changes.  
Must not learn: Do not add a new causal mechanism or change the $T_2$ figure reference.  
Scope: sentence-level.

## NEG-011: Stage labels should use exact values only when present

Source ID: R-008  
Original or source signal: `second displayed stage`, `third stage`, `73.2\%`, `90.5\%`, `Figure~\ref{fig:fig2}h`  
Teacher/local version: `25\% dissolution`, `50\% dissolution`; values and figure reference preserved.  
Problem labels: `stage_unclear`, `latex_risk`  
Safe local correction: Replace relative stage labels with exact stage values only when the source already provides them.  
May learn: Use concrete stage values and `while` for synchronized changes.  
Must not learn: Do not invent stage percentages or alter values, units, or figure labels.  
Scope: sentence-level; protected technical content.

## NEG-012: Abstract comparison subject

Source ID: R-013  
Original or source signal: `The tortuosity trajectories ... quantify the timing contrast in channel establishment.`  
Teacher/local version: `Channeling and wormholing show lower tortuosity earlier...`  
Problem labels: `heavy_nominalization`, `latex_risk`  
Safe local correction: Move the compared regimes into subject position.  
May learn: Make comparison subjects concrete.  
Must not learn: Do not change the comparison, values, or hydraulic interpretation.  
Scope: sentence-level.

## Partial-Learning Samples

## NEG-013: Term definition pattern only

Source ID: I-011  
Original or source signal: multimodal pore systems and $T_2$ peak overlap.  
Teacher/local version: introduces `pore coupling` with `(here referred to as pore coupling)`.  
Problem labels: `undefined_term`, `partial_learning_only`, `author_confirm_required`, `latex_risk`  
Safe local correction: Learn only the local definition form.  
May learn: Use `(here referred to as...)` or `defined here as...` for a confirmed term.  
Must not learn: Do not add vugs, residual matrix pores, developing conduits, or exchange mechanisms without author confirmation.  
Scope: partial-learning-only.

## NEG-014: Regime comparison pattern only

Source ID: A-006  
Original or source signal: wormholing and channeling compared with `whereas`.  
Teacher/local version: adds `followed by rapid peak merging`.  
Problem labels: `partial_learning_only`, `author_confirm_required`, `latex_risk`  
Safe local correction: Learn careful contrast connectors only.  
May learn: Use `whereas` and `followed by` to express already-supported process order.  
Must not learn: Do not independently refine regime mechanisms or add peak-evolution details.  
Scope: partial-learning-only.

## NEG-015: Deleting misplaced content is not normal sentence polishing

Source ID: R-015  
Original or source signal: breakthrough hierarchy paragraph ends with segmented $T_2$ profiles.  
Teacher/local version: removes the segmented profile sentence.  
Problem labels: `partial_learning_only`, `out_of_scope_rewrite`, `latex_risk`  
Safe local correction: Treat as a guardrail about topic drift.  
May learn: Notice when a sentence may be out of paragraph scope.  
Must not learn: Do not delete sentences during sentence polishing unless the user asks for structural editing.  
Scope: out-of-scope guardrail.

## Out-of-Scope Macro and Paragraph Samples

## NEG-016: Title rewrite changes manuscript positioning

Source ID: T-001  
Original or source signal: title centered on `Pore Coupling During Mineral Dissolution`.  
Teacher/local version: title centered on `Quantitative Nuclear Magnetic Resonance Signatures`.  
Problem labels: `out_of_scope_rewrite`  
Safe local correction: None for sentence-polishing mode.  
May learn: Titles involve manuscript positioning.  
Must not learn: Do not rewrite title focus or research object in sentence polishing.  
Scope: out-of-scope.

## NEG-017: Abstract opening scope rewrite

Source ID: A-001  
Original or source signal: `reorganizes pore networks into... regimes`.  
Teacher/local version: `through spatially and temporally variable pathways`.  
Problem labels: `out_of_scope_rewrite`  
Safe local correction: None for sentence-polishing mode.  
May learn: Macro opening sentences can be reframed by a human.  
Must not learn: Do not change abstract scope, opening angle, or research framing automatically.  
Scope: out-of-scope.

## NEG-018: Abstract research question shift

Source ID: A-002  
Original or source signal: `interpret transient ... $T_2$ distributions as signatures...`  
Teacher/local version: `test whether quantitative ... signatures can diagnose...`  
Problem labels: `out_of_scope_rewrite`, `latex_risk`  
Safe local correction: None unless the user asks for abstract restructuring.  
May learn: Research-question wording is high-risk.  
Must not learn: Do not convert interpretation into diagnostic testing without author intent.  
Scope: out-of-scope.

## NEG-019: New method-framework sentence

Source ID: A-003  
Original or source signal: no independent method-framework sentence.  
Teacher/local version: adds coupled reactive transport simulations and NMR forward modeling.  
Problem labels: `out_of_scope_rewrite`, `author_confirm_required`  
Safe local correction: None for sentence-polishing mode.  
May learn: Missing method context may need a new sentence in manuscript editing.  
Must not learn: Do not add method-framework content during sentence polishing.  
Scope: out-of-scope.

## NEG-020: Abstract result subject changes evidence chain

Source ID: A-004  
Original or source signal: permeability breakthrough controlled by matrix-vug coupling.  
Teacher/local version: simulated $T_2$ pathways control dissolution progress wording.  
Problem labels: `out_of_scope_rewrite`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Result subjects affect evidence chain.  
Must not learn: Do not switch the result subject from permeability to $T_2$ pathways unless requested.  
Scope: out-of-scope.

## NEG-021: MVC source and validation target added

Source ID: A-007  
Original or source signal: MVC index shows earlier coupling in channeling.  
Teacher/local version: MVC index from $T_2$ spectra and comparison with tortuosity.  
Problem labels: `out_of_scope_rewrite`, `author_confirm_required`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Metric source and validation target are content decisions.  
Must not learn: Do not add metric provenance or validation target automatically.  
Scope: out-of-scope.

## NEG-022: Evidence chain expanded

Source ID: A-008  
Original or source signal: `establishes NMR $T_2$ evolution as... diagnostic`.  
Teacher/local version: adds matrix-vug exchange, tortuosity reduction, dissolution efficiency, and breakthrough.  
Problem labels: `out_of_scope_rewrite`, `overclaim`, `latex_risk`  
Safe local correction: Use NEG-002 if only claim strength needs local correction.  
May learn: Evidence-chain expansion can be useful at abstract level.  
Must not learn: Do not expand mechanism evidence during sentence polishing.  
Scope: out-of-scope.

## NEG-023: Introduction opening adds new examples and references

Source ID: I-001  
Original or source signal: natural and engineering processes with selected examples.  
Teacher/local version: adds flow/transport evolution, biological carbonate dissolution, and geological carbon storage.  
Problem labels: `out_of_scope_rewrite`, `latex_risk`  
Safe local correction: Conservative syntax only; see migration notes.  
May learn: Broad introduction openings may be strategically reframed.  
Must not learn: Do not add applications or citations during sentence polishing.  
Scope: out-of-scope.

## NEG-024: Existing-method limitation paragraph rewritten

Source ID: I-008  
Original or source signal: visual/image-derived descriptions, micro-CT limitations, flow-distribution metrics.  
Teacher/local version: rewrites limitations and field-setting accessibility.  
Problem labels: `out_of_scope_rewrite`, `typo_or_intermediate_draft`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Method limitation paragraphs need paragraph-level judgment.  
Must not learn: Do not rewrite method limitations or introduce field-application claims automatically.  
Scope: out-of-scope.

## NEG-025: Geophysical bridge added

Source ID: I-009  
Original or source signal: field-applicable framework lacking.  
Teacher/local version: adds geophysical monitoring bridge and citations.  
Problem labels: `out_of_scope_rewrite`, `author_confirm_required`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Bridge sentences can repair manuscript logic.  
Must not learn: Do not add geophysical bridge facts or citations during sentence polishing.  
Scope: out-of-scope.

## NEG-026: NMR method positioning changed

Source ID: I-010  
Original or source signal: low-field NMR characterization and $T_1$/$T_2$ uses.  
Teacher/local version: positions NMR among geophysical methods and adds literature.  
Problem labels: `out_of_scope_rewrite`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Method positioning is paragraph-level.  
Must not learn: Do not reposition the method or alter citation coverage automatically.  
Scope: out-of-scope.

## NEG-027: NMR gap rewritten

Source ID: I-012  
Original or source signal: missing dynamic NMR-interpretable metric and forward-modeling framework.  
Teacher/local version: rewrites gap and need for framework.  
Problem labels: `out_of_scope_rewrite`, `invented_compound`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Gap sharpening is manuscript-logic work.  
Must not learn: Do not rewrite the gap, research need, or framework purpose in sentence polishing.  
Scope: out-of-scope.

## NEG-028: Repeated physical explanation commented out

Source ID: I-013  
Original or source signal: paragraph explains $T_2$ evolution and matrix--vug coupling.  
Teacher/local version: whole block commented out.  
Problem labels: `out_of_scope_rewrite`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Removing repetition can be paragraph editing.  
Must not learn: Do not comment out or remove explanatory paragraphs in sentence polishing.  
Scope: out-of-scope.

## NEG-029: Results summary expanded with literature comparison

Source ID: R-009  
Original or source signal: summary of decomposed peaks across regimes.  
Teacher/local version: adds previous NMR studies, framework gap, and reviewer-style note.  
Problem labels: `out_of_scope_rewrite`, `latex_risk`, `author_confirm_required`  
Safe local correction: None for sentence-polishing mode.  
May learn: Literature comparison requires author control.  
Must not learn: Do not add or reshape literature discussion during sentence polishing.  
Scope: out-of-scope.

## NEG-030: New tortuosity/NMR literature paragraph

Source ID: R-014  
Original or source signal: no independent literature comparison paragraph.  
Teacher/local version: adds tortuosity and NMR literature comparison.  
Problem labels: `out_of_scope_rewrite`, `author_confirm_required`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: New discussion paragraphs are outside sentence polishing.  
Must not learn: Do not add literature paragraphs or claims of extension.  
Scope: out-of-scope.

## Technical Definition and Method-Content Samples

## NEG-031: Reaction parameter definition corrected

Source ID: M-004  
Original or source signal: `$k_{\mathrm{TST}}$ is the surface reaction rate constant`.  
Teacher/local version: `$k_{\mathrm{TST}}$ is an effective dissolution flux coefficient`; `\gamma c_{\mathrm{H}^+}` is dimensionless activity term.  
Problem labels: `out_of_scope_rewrite`, `author_confirm_required`, `latex_risk`  
Safe local correction: None unless the author requests technical correction.  
May learn: Parameter wording can be scientifically consequential.  
Must not learn: Do not redefine variables, coefficients, or activity terms during language polishing.  
Scope: out-of-scope technical correction.

## NEG-032: Parameter sweep explanation expanded

Source ID: M-006  
Original or source signal: Pe/Da meanings and parameter map.  
Teacher/local version: expands parameter control, fixed parameters, citations, and units.  
Problem labels: `out_of_scope_rewrite`, `author_confirm_required`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: Scope and unit details may need method editing.  
Must not learn: Do not add parameter-control logic, citations, or unit explanations.  
Scope: out-of-scope technical content.

## NEG-033: Benchmark evidence expanded

Source ID: M-009  
Original or source signal: benchmark against microfluidic calcite dissolution experiment.  
Teacher/local version: adds normalized porosity-growth comparison, 4.26 h/4.28 h, validation language.  
Problem labels: `out_of_scope_rewrite`, `overclaim`, `author_confirm_required`  
Safe local correction: None unless benchmark details are supplied by author.  
May learn: Quantitative validation requires data support.  
Must not learn: Do not add benchmark values or validation claims during sentence polishing.  
Scope: out-of-scope technical content.

## NEG-034: Equation correction

Source ID: M-012  
Original or source signal: `\frac{1}{T_{1,2}} = ...`  
Teacher/local version: `\frac{1}{T_{2}} = ...`  
Problem labels: `out_of_scope_rewrite`, `latex_risk`, `author_confirm_required`  
Safe local correction: None for sentence-polishing mode.  
May learn: Equations are protected content.  
Must not learn: Do not change equation variables or subscripts during polishing.  
Scope: out-of-scope technical correction.

## NEG-035: Inversion-consistency sentence added

Source ID: M-016  
Original or source signal: definition of $M_{xy}(t)$, $M_0$, $f_{2i}$, and $\sum_i f_{2i}=1`.  
Teacher/local version: adds consistent $T_2$ inversion settings and processing artifact control.  
Problem labels: `out_of_scope_rewrite`, `latex_risk`, `author_confirm_required`  
Safe local correction: None for sentence-polishing mode.  
May learn: Processing consistency is method content.  
Must not learn: Do not add inversion settings or artifact claims automatically.  
Scope: out-of-scope technical content.

## NEG-036: Implementation details expanded

Source ID: M-017  
Original or source signal: details of Bloch--Torrey equations and boundary conditions in Text S4.  
Teacher/local version: expands finite-element discretization, mesh regeneration, settings, and Table S2.  
Problem labels: `out_of_scope_rewrite`, `typo_or_intermediate_draft`, `latex_risk`  
Safe local correction: None for sentence-polishing mode.  
May learn: SI pointers can be expanded by author.  
Must not learn: Do not add implementation details, table pointers, or correct technical spelling automatically.  
Scope: out-of-scope technical content.

## Typo, Intermediate-Draft, and LaTeX-Risk Samples

## NEG-037: Intermediate abstract-action wording

Source ID: I-014  
Original or source signal: combines RTM with NMR module to infer pore coupling.  
Teacher/local version contains: `a integrated`, `transport - NMR`, `time varying`.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`, `out_of_scope_rewrite`  
Safe local correction: Use only as a warning that teacher/intermediate text can contain errors.  
May learn: Nothing as a positive wording model.  
Must not learn: Do not copy `a integrated` or spacing around compound modifiers.  
Scope: negative-only.

## NEG-038: Intermediate output sentence has spacing error

Source ID: I-015  
Original or source signal: RTM generates representative regimes; NMR module converts geometries into $T_2$ outputs.  
Teacher/local version contains: `Usingface-dissolution`; `time varying`.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`, `out_of_scope_rewrite`  
Safe local correction: None for this stage.  
May learn: Nothing as a positive wording model.  
Must not learn: Do not copy spacing errors or rewrite output logic from intermediate text.  
Scope: negative-only.

## NEG-039: Intermediate proxy claim has spacing error

Source ID: I-016  
Original or source signal: compare spectral evolution with permeability and tortuosity; define MVC.  
Teacher/local version contains: `proxy forflow pathway`; matrix-vug terminology changes.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`, `out_of_scope_rewrite`  
Safe local correction: None for this stage.  
May learn: Protect $T_2$, MVC, matrix--vug, and comparison targets.  
Must not learn: Do not copy `forflow` or alter proxy/metric purpose without author confirmation.  
Scope: negative-only.

## NEG-040: Results overview has grammar and punctuation errors

Source ID: R-001  
Original or source signal: Pe/Da parameter map and selected regimes.  
Teacher/local version contains: `To exam`, stray punctuation, `0.73\%` porosity wording.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`, `out_of_scope_rewrite`  
Safe local correction: None for this stage.  
May learn: Results overview edits can involve paragraph setup.  
Must not learn: Do not copy grammar errors or change parameter-map context in sentence polishing.  
Scope: negative-only.

## NEG-041: T2 result entry has spelling and LaTeX errors

Source ID: R-003  
Original or source signal: inverted $T_2$ spectra, matrix/vug thresholds, Gaussian decomposition.  
Teacher/local version contains: `relxation`, `seperate`, malformed `100\%\` spacing.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`  
Safe local correction: None for this stage.  
May learn: Protect $T_2$ ranges and decomposition references.  
Must not learn: Do not copy spelling errors or malformed LaTeX percentages.  
Scope: negative-only.

## NEG-042: Wormholing paragraph has repeated and malformed wording

Source ID: R-006  
Original or source signal: wormholing $T_2$ broad peak, $\varphi=0.894$, $k/k_0=106.0`, 92.7\%, 7.3\%.  
Teacher/local version contains: repeated `throughout`, `continous`, `resulting a`, `decreases to7.3\%`, `completedissolution`.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`, `out_of_scope_rewrite`  
Safe local correction: None for this stage.  
May learn: Protect values and variables.  
Must not learn: Do not use this teacher version as a positive example.  
Scope: negative-only.

## NEG-043: CPMG workflow intermediate text has typo

Source ID: M-015  
Original or source signal: CPMG sequence, $M_{xy}(t)$, $M_0$, $f_{2i}$, Figure~\ref{fig:fig1}c.  
Teacher/local version contains: `fiinite`, expanded finite-element and boundary-condition process.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`, `out_of_scope_rewrite`  
Safe local correction: None for this stage.  
May learn: Protect symbols and figure references.  
Must not learn: Do not add solver details or copy misspellings during sentence polishing.  
Scope: negative-only.

## NEG-044: Module integration sentence has malformed clause

Source ID: M-018  
Original or source signal: RTM-NMR snapshot export, masks, mesh conversion, CPMG, $T_2$ inversion.  
Teacher/local version contains: `which CPMG $T_2$ decay signals were simulated`.  
Problem labels: `typo_or_intermediate_draft`, `latex_risk`, `out_of_scope_rewrite`  
Safe local correction: None for this stage.  
May learn: Protect workflow ordering and technical elements.  
Must not learn: Do not copy malformed clauses or expand module integration as sentence polishing.  
Scope: negative-only.

## Coverage Summary

- Total samples: 44.
- Expression-level local samples: 12.
- Partial-learning samples: 3.
- Out-of-scope macro/paragraph samples: 15.
- Technical content samples: 6.
- Typo/intermediate/LaTeX-risk samples: 8.
