# Own Manuscript Rule Cards Draft

These draft rule cards are distilled from `raw_modification_log.md` and `negative_samples_from_own_manuscript.md`. They are not yet executable skill rules and are not registered in `SKILL.md`.

Use these cards only as candidate local expression rules. Every rule includes a guardrail because the main risk is overlearning teacher-level manuscript edits as sentence polishing.

## OWN-A-005: Clarify sequential stages with light connectors

Source: `raw_modification_log.md`, A-005  
Problem type: `stage_unclear`  
Bad pattern: `from X to Y and back to Z`  
Preferred local pattern: `from X to Y, then back to Z`  
Rule: When a sentence already contains a sequence, use `then` or `followed by` to mark temporal progression.  
Guardrail: Do not add a new stage, process endpoint, or causal mechanism.
Do not apply when:
- the sentence does not already contain a temporal sequence;
- the added connector would imply a new causal order;
- the stage order is uncertain or needs author confirmation.

## OWN-I-006: Replace vague literature subjects with concrete study types

Source: `raw_modification_log.md`, I-006  
Problem type: `vague_subject`  
Bad pattern: `Extensive efforts have identified...`  
Preferred local pattern: `Extensive experimental and numerical studies have identified...`  
Rule: Replace vague subjects with concrete study types when the original sentence already names the evidence sources.  
Guardrail: Do not broaden the literature scope or add methods/citations.
Do not apply when:
- the original sentence does not identify the study types;
- the concrete subject would require a literature judgment;
- the replacement would add methods, systems, or citations.

## OWN-I-007: Use `show how` only for supported mechanism relations

Source: `raw_modification_log.md`, I-007  
Problem type: `clarify_causal_link`  
Bad pattern: `show that X produces Y` when the point is process relation.  
Preferred local pattern: `show how X produces Y`  
Rule: Use `show how` to emphasize a process relation only when the cited or surrounding text already supports that mechanism.  
Guardrail: If the mechanism support is unclear, keep `show that` or mark `author-confirm`.
Do not apply when:
- the sentence only reports a finding rather than a process;
- the cited work has not been checked for mechanism support;
- `show how` would make the claim sound more causal than the original.

## OWN-I-003: Compress repeated regime descriptions with direct verbs

Source: `raw_modification_log.md`, I-003  
Problem type: `template_phrase`, `heavy_nominalization`  
Bad pattern: repeated `giving rise to`; redundant phrases such as `approximately throughout the entire domain`.  
Preferred local pattern: direct verbs such as `localizes`, `focuses flow`, `forms`, and `expands`.  
Rule: Replace repeated template phrases with direct physical verbs when the process is already explicit.  
Guardrail: Do not delete necessary regime distinctions, citations, or comparison conditions.
Do not apply when:
- the direct verb would add a mechanism not present in the source;
- the sentence contains protected regime definitions or citation-dependent claims;
- compression would remove necessary conditions or distinctions.

## OWN-M-002: Use restrained active voice for methods

Source: `raw_modification_log.md`, M-002  
Problem type: `heavy_nominalization`, method sentence density.  
Bad pattern: `A ... model ... was used to simulate...` with long inserted provenance.  
Preferred local pattern: `We use X based on Y to simulate Z.`  
Rule: In Methods, a restrained `We use...` construction can make model, source, and purpose clearer.  
Guardrail: Do not alter model capability, provenance, governing assumptions, or citations.
Do not apply when:
- the manuscript or journal requires passive methods style;
- the sentence reports a procedure performed by a tool rather than the authors;
- active voice would obscure model provenance or assumptions.

## OWN-M-008: Clarify module handoff with destination and attached data

Source: `raw_modification_log.md`, M-008  
Problem type: `template_phrase`, method handoff clarity.  
Bad pattern: `exported ... for NMR simulation module, together with...`  
Preferred local pattern: `were exported to the NMR simulation module alongside...`  
Rule: For workflow handoffs, state the exported object, destination module, and associated metadata clearly.  
Guardrail: Do not add, remove, or rename exported data items.
Do not apply when:
- the destination module is not stated in the source;
- the list of exported data items is incomplete or uncertain;
- the rewrite would change workflow order.

## OWN-R-007: Replace template phrases with direct result verbs

Source: `raw_modification_log.md`, R-007  
Problem type: `template_phrase`  
Bad pattern: `..., giving rise to a transient bimodal feature...`  
Preferred local pattern: `..., producing a transient bimodal feature...`  
Rule: When the causal relation is already clear, replace repeated template phrases such as `giving rise to` with direct verbs such as `producing`, `forming`, or `leading to`.  
Guardrail: Do not add a new causal mechanism. Do not strengthen the causal relation.
Do not apply when:
- the causal relation is uncertain;
- the original phrase is part of a quoted or standard expression;
- the replacement would make the process sound more direct than the evidence supports.

## OWN-R-008: Replace unclear stage labels only with known values

Source: `raw_modification_log.md`, R-008  
Problem type: `stage_unclear`, `latex_risk`  
Bad pattern: `second displayed stage`, `third stage`  
Preferred local pattern: `25\% dissolution`, `50\% dissolution`  
Rule: If a figure or source text already gives exact stage values, use them instead of relative display labels.  
Guardrail: Never invent percentages, times, values, or figure labels.
Do not apply when:
- exact stage values are not provided in the source;
- the displayed stage is intentionally tied to figure layout;
- replacing the label would require interpreting the figure or raw data.

## OWN-R-013: Put compared regimes in subject position

Source: `raw_modification_log.md`, R-013  
Problem type: `heavy_nominalization`  
Bad pattern: `The tortuosity trajectories for the channeling and wormholing regimes quantify...`  
Preferred local pattern: `Channeling and wormholing show..., but they differ...`  
Rule: When a sentence compares regimes, put the compared regimes or objects in subject position.  
Guardrail: Preserve all variables, values, comparison baselines, and interpretation strength.
Do not apply when:
- the comparison baseline would become less clear;
- the sentence is mainly defining a metric rather than comparing regimes;
- moving the subject would require deleting values, variables, or qualifiers.

## OWN-A-009: Downgrade complete diagnostic claims to bounded indicators

Source: `raw_modification_log.md`, A-009  
Problem type: `overclaim`  
Bad pattern: `establishes NMR $T_2$ evolution as a quantitative diagnostic of dissolution mechanisms`  
Preferred local pattern: `quantitative NMR signatures as diagnostic indicators for tracking dissolution dynamics`  
Rule: If evidence supports signal tracking but not full mechanism diagnosis, use bounded indicator language.  
Guardrail: Do not weaken or strengthen the scientific conclusion beyond the available evidence; mark `author-confirm` if the claim strength is uncertain.
Do not apply when:
- the original evidence actually establishes the stronger diagnostic claim;
- the author wants to preserve the stronger claim;
- downgrading would change the intended conclusion rather than expression.

## Draft Status

These cards are candidates only. Before promoting any card into an executable rule, check it against:

1. `negative_samples_from_own_manuscript.md`;
2. `style_principles.md`;
3. `validation_checklist.md`;
4. at least one real manuscript sentence not used to create the card.
