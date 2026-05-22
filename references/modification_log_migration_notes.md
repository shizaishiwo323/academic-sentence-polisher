# Modification Log Migration Notes

`raw_modification_log.md` is a source database, not an executable skill file. It contains useful local sentence-polishing examples, teacher-level manuscript revisions, intermediate drafts, and unsafe samples that must not be learned directly.

This file defines how material can migrate from the raw log into the `academic-sentence-polisher` references.

## Current Stage

Stage: v0.1 tested and frozen.

v0.1 was frozen after a four-subagent test run produced 48/48 passes across the 12 core test cases, with no partial passes, no failures, and no repeated failure pattern.

Active executable files:

- `SKILL.md`;
- `references/dash_policy.md`;
- `references/overclaim_downgrade.md`;
- `references/simple_word_replacement.md`;
- `references/terminology_definition.md`.

Supporting test and validation files:

- `references/test_cases.md`;
- `references/test_run_log.md`;
- `references/validation_checklist.md`.

Non-executable traceability files:

- `references/modification_log_migration_notes.md`;
- `references/negative_samples_from_own_manuscript.md`;
- `references/own_manuscript_rule_cards_draft.md`;
- `references/source_sentence_corpus.md`.

The older extended reference files remain available for traceability and future expansion, but the v0.1 skill should not load them by default.

## Migration Rules

1. Entries under `可学习条目` can be converted into local negative samples and draft rule cards.
2. Entries under `可部分学习条目` can only be used for the explicitly safe local pattern.
3. Entries under `不纳入 sentence-polishing skill` must be used only as negative examples or out-of-scope guardrails.
4. The raw table is for traceability only; do not copy the full table into an executable skill prompt.
5. Any revised text containing spelling, spacing, LaTeX, grammar, or intermediate-draft errors must not be used as a positive example.
6. Sentence polishing must not learn title rewriting, abstract restructuring, paragraph reordering, new mechanism addition, new citation addition, or technical definition correction.

## Migration Targets

| Target file | Role | Current status |
|---|---|---|
| `SKILL.md` | Defines the sentence-polishing boundary, workflow, output format, and prohibitions | Active v0.1 file |
| `dash_policy.md` | Controls dash, hyphen, en-dash, and compound-term decisions | Active v0.1 rule table |
| `overclaim_downgrade.md` | Controls claim-strength downgrading and prevents overclaiming | Active v0.1 rule table |
| `simple_word_replacement.md` | Controls fancy-word replacement and nominalization reduction | Active v0.1 rule table |
| `terminology_definition.md` | Controls first-use definitions and manuscript-specific terms | Active v0.1 rule table |
| `test_run_log.md` | Records Run 01, Run 02, failure types, rule updates, and v0.1 freeze evidence | Active v0.1 testing file |
| `negative_samples_from_own_manuscript.md` | Stores negative/caution samples with `Must not learn` guardrails | Traceability and future expansion |
| `own_manuscript_rule_cards_draft.md` | Stores draft local rules from safe patterns | Traceability and future expansion |
| `modification_log_migration_notes.md` | Records how raw log entries may or may not migrate | This file |

## Files Not Loaded by Default in v0.1

The v0.1 `SKILL.md` should not load the following extended files by default:

- `ai_smell_checklist.md`
- `before_after_examples.md`
- `corpus_rule_cards.md`
- `extraction_protocol.md`
- `negative_samples_from_own_manuscript.md`
- `overclaim_downgrade_table.md`
- `own_manuscript_rule_cards_draft.md`
- `simple_word_replacements.md`
- `source_sentence_corpus.md`
- `style_principles.md`
- `terminology_definition_rules.md`
- `validation_checklist.md`
- `test_cases.md`

Load these only when the user explicitly asks to expand, test, audit, or trace the skill. This keeps the active skill narrow and prevents older draft rules from overriding the v0.1 rule tables.

## Source Group Mapping

### Learnable Local Expression Samples

Use these as caution samples and draft rule sources:

```text
A-005
A-009
I-003
I-006
I-007
M-002
M-005
M-008
R-002
R-007
R-008
R-013
```

Allowed migration:

- `negative_samples_from_own_manuscript.md`: yes;
- `own_manuscript_rule_cards_draft.md`: yes, with guardrails;
- active v0.1 rule tables: only after manual review and testing.

### Partial-Learning Samples

Use only the explicitly safe local pattern:

```text
I-011
A-006
R-015
```

Allowed migration:

- local definition pattern from I-011;
- connector pattern from A-006;
- out-of-scope guardrail from R-015.

Forbidden migration:

- newly added mechanisms;
- regime refinements not in the source;
- sentence deletion as a default polishing behavior.

### Out-of-Scope Macro and Paragraph Samples

Use only as guardrails:

```text
T-001
A-001
A-002
A-003
A-004
A-007
A-008
I-001
I-008
I-009
I-010
I-012
I-013
R-009
R-014
```

Reason:
These examples change title focus, abstract action, method framing, literature bridge, paragraph function, or evidence chain. They are useful for human manuscript revision but unsafe for sentence-polishing automation.

### Technical Definition and Method-Content Samples

Use only as `author-confirm` or protected-content guardrails:

```text
M-004
M-006
M-009
M-012
M-016
M-017
```

Reason:
These examples change parameter meanings, equations, benchmark evidence, inversion settings, or implementation details. They require scientific confirmation.

### Typo and Intermediate-Draft Samples

Use only as negative examples:

```text
I-014
I-015
I-016
R-001
R-003
R-006
M-015
M-018
```

Reason:
The teacher/intermediate versions include errors such as `a integrated`, `Usingface`, `forflow`, `To exam`, `relxation`, `seperate`, `fiinite`, malformed percentages, and spacing mistakes. These must never be positive examples.

## Promotion Criteria

A draft rule can be promoted later only if:

1. it is traceable to a safe local source ID;
2. it has a clear `Guardrail`;
3. it does not require scientific judgment beyond the source text;
4. it preserves LaTeX, variables, values, citations, and labels;
5. it passes manual review on new manuscript sentences;
6. it does not duplicate an existing rule in `dash_policy.md`, `overclaim_downgrade.md`, `simple_word_replacement.md`, or `terminology_definition.md`.

## Rejection Criteria

Reject a migration if it teaches the skill to:

- rewrite titles;
- reshape abstract storyline;
- add missing methods or frameworks;
- add citations or literature comparisons;
- comment out or delete paragraphs;
- define technical terms without author confirmation;
- correct equations or parameter definitions;
- turn local simulation evidence into broad claims;
- copy intermediate-draft text with spelling, grammar, spacing, or LaTeX errors.

## v0.1 Testing Checklist

- `negative_samples_from_own_manuscript.md` has 30-50 samples.
- Samples cover overclaim, vague subject, template phrase, heavy nominalization, undefined term, and LaTeX risk.
- Samples cover title, abstract storyline, paragraph structure, mechanism expansion, literature expansion, and technical definition correction.
- At least 5 samples are LaTeX-risk samples.
- At least 5 samples are typo/intermediate-draft samples.
- Every sample has a `Must not learn` field.
- Learnable, partial-learning, and out-of-scope samples are clearly separated.
- Raw table rows remain traceability material, not executable prompts.
- Test 10-20 real sentences against the active v0.1 files.
- Confirm no test output adds facts, mechanisms, citations, or stronger claims.
- Confirm protected values, variables, labels, and LaTeX are preserved.
- Confirm revisions use local edits rather than unnecessary paragraph rewriting.
