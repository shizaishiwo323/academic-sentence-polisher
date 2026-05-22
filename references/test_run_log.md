# Test Run Log

Use this file to move `academic-sentence-polisher` from a rule-complete v0.1 draft to a tested v0.1 skill.

Do not expand the rule system during testing. Run the existing test cases first, record outputs, classify failures, and update rules only when a failure pattern repeats.

## Active Files for v0.1 Testing

- `SKILL.md`
- `references/dash_policy.md`
- `references/overclaim_downgrade.md`
- `references/simple_word_replacement.md`
- `references/terminology_definition.md`
- `references/test_cases.md`
- `references/test_run_log.md`
- `references/validation_checklist.md`

## Fixed Test Prompt

Use this prompt for every test case in `test_cases.md`:

```text
Use academic-sentence-polisher to polish the following sentence.
Only improve sentence-level expression.
Do not add new claims, mechanisms, citations, implications, or broader scope.
Preserve protected content and evidence strength.

Sentence:
[paste TC input sentence]
```

## Failure Type Codes

| Code | Failure type |
|---|---|
| F1 | Meaning drift |
| F2 | Evidence strengthened |
| F3 | New mechanism added |
| F4 | New implication added |
| F5 | Protected content changed |
| F6 | Scope marker removed |
| F7 | Unnecessary expansion |
| F8 | Invented compound retained or created |
| F9 | Technical term oversimplified |
| F10 | Undefined term not handled |
| F11 | Over-downgraded valid claim |
| F12 | Output too verbose |

## Judgment Rules

Use one result per case:

- `Pass`: the output satisfies the expected behavior, preserves meaning and evidence strength, and uses a minimum edit.
- `Partial pass`: the output has the right direction but has a minor issue, such as slightly verbose notes or a longer-than-needed sentence.
- `Fail`: the output changes meaning, strengthens evidence, adds a mechanism or implication, changes protected content, removes a scope marker, over-expands, creates an AI-like compound, or over-downgrades a valid claim.

Do not update a rule after a single isolated failure. Update `SKILL.md` or a rule table only when the same failure type appears at least twice, or when one failure is severe enough to threaten protected content, evidence strength, or mechanism accuracy.

## Run 01

Date: 2026-05-23 00:52 CEST
Tester: Codex coordinator with four fresh independent subagents: Pauli, Mencius, Bohr, and Euler
Protocol: Each subagent independently ran all 12 test cases, for 48 total test outputs. Previous split-run and interrupted-run results were discarded before this run was recorded.

### Summary

| Item | Result |
|---|---|
| Total subagents | 4 |
| Test cases per subagent | 12 |
| Total test outputs | 48 |
| Passed | 48 |
| Partial pass | 0 |
| Failed | 0 |
| Main failure type | None |
| Repeated failure pattern | None |
| Rule update needed | No |

### Failure Summary

| Failure type | Count | Cases |
|---|---:|---|
| F1 Meaning drift | 0 | - |
| F2 Evidence strengthened | 0 | - |
| F3 New mechanism added | 0 | - |
| F4 New implication added | 0 | - |
| F5 Protected content changed | 0 | - |
| F6 Scope marker removed | 0 | - |
| F7 Unnecessary expansion | 0 | - |
| F8 Invented compound retained or created | 0 | - |
| F9 Technical term oversimplified | 0 | - |
| F10 Undefined term not handled | 0 | - |
| F11 Over-downgraded valid claim | 0 | - |
| F12 Output too verbose | 0 | - |

### Cross-Agent Consensus

| Test case | Agent 1 | Agent 2 | Agent 3 | Agent 4 | Consensus |
|---|---|---|---|---|---|
| TC-01 | Pass | Pass | Pass | Pass | Pass |
| TC-02 | Pass | Pass | Pass | Pass | Pass |
| TC-03 | Pass | Pass | Pass | Pass | Pass |
| TC-04 | Pass | Pass | Pass | Pass | Pass |
| TC-05 | Pass | Pass | Pass | Pass | Pass |
| TC-06 | Pass | Pass | Pass | Pass | Pass |
| TC-07 | Pass | Pass | Pass | Pass | Pass |
| TC-08 | Pass | Pass | Pass | Pass | Pass |
| TC-09 | Pass | Pass | Pass | Pass | Pass |
| TC-10 | Pass | Pass | Pass | Pass | Pass |
| TC-11 | Pass | Pass | Pass | Pass | Pass |
| TC-12 | Pass | Pass | Pass | Pass | Pass |

### Agent 1 Outputs

| Case | Skill output | Result | Failure type | Notes | Rule update needed |
|---|---|---|---|---|---|
| TC-01 | Mineral dissolution occurs widely in natural and engineered systems. | Pass | None | Word order improved only; no mechanism or storyline added. | No |
| TC-02 | These results indicate that NMR T2 evolution can help distinguish dissolution mechanisms in porous media. | Pass | None | `prove` and `robustly diagnoses` were downgraded; NMR T2 and dissolution context preserved. | No |
| TC-03 | This framework links structure to signal and shows the relation between connectivity and breakthrough during dissolution. | Pass | None | Invented compound phrasing was rewritten as plain relations; no new named framework created. | No |
| TC-04 | The pore-coupling index increases during the intermediate stage. Author-confirm: `pore-coupling index` appears manuscript-specific and should be defined if this is its first use. | Pass | None | Term preserved and flagged instead of inventing a definition. | No |
| TC-05 | The model explains the mechanisms that support channel development. | Pass | None | Decorative vocabulary simplified without changing the mechanism claim. | No |
| TC-06 | In the simulations, permeability increases at high injection rates, suggesting a transition toward channeling. | Pass | None | Scope marker and `suggesting` preserved. | No |
| TC-07 | The vug contribution accounts for 73.2% at 25% dissolution and increases to 90.5% at 50% dissolution (Figure 2h). | Pass | None | All values, percentages, and figure reference preserved. | No |
| TC-08 | We segment the medium to calculate the flow focusing index. | Pass | None | Nominalization converted to direct method wording. | No |
| TC-09 | The T2 peak shifts to longer relaxation times. | Pass | None | Minimum edit; no pore-enlargement mechanism added. | No |
| TC-10 | Compared with the low-Da case, the high-Da case shows stronger inlet-localized dissolution. | Pass | None | Both compared cases and contrast direction preserved. | No |
| TC-11 | Matrix–vug connectivity increases across the Péclet–Damköhler parameter space. | Pass | None | Unicode dash, accents, and protected technical expressions preserved. | No |
| TC-12 | Figure 3 demonstrates that the simulated T2 peak shifts to longer relaxation times under the tested conditions. | Pass | None | `demonstrates` was not over-downgraded because the figure directly supports the observation; scope marker preserved. | No |

### Agent 2 Outputs

| Case | Skill output | Result | Failure type | Notes | Rule update needed |
|---|---|---|---|---|---|
| TC-01 | Mineral dissolution occurs widely in natural and engineered systems. | Pass | None | Word order improved only; no mechanism or broader storyline added. | No |
| TC-02 | These results indicate that NMR T2 evolution can help distinguish dissolution mechanisms in porous media. | Pass | None | `prove` and `robustly diagnoses` were downgraded; context preserved. | No |
| TC-03 | This framework links structure to signal and shows the relation between connectivity and breakthrough during dissolution. | Pass | None | Invented compounds were rewritten as plain relations; no new term created. | No |
| TC-04 | The pore-coupling index increases during the intermediate stage. Author-confirm: if this is the first use, define what the index measures and how it is calculated. | Pass | None | Undefined manuscript-specific term was flagged without inventing a definition. | No |
| TC-05 | The model explains the mechanisms that support channel development. | Pass | None | Decorative wording simplified while preserving the mechanism claim. | No |
| TC-06 | In the simulations, permeability increases at high injection rates, suggesting a transition toward channeling. | Pass | None | Scope marker and cautious evidence strength preserved. | No |
| TC-07 | The vug contribution accounts for 73.2% at 25% dissolution and increases to 90.5% at 50% dissolution (Figure 2h). | Pass | None | Values, percentages, and figure reference preserved. | No |
| TC-08 | We segment the medium to calculate the flow focusing index. | Pass | None | Heavy nominalization converted to direct method wording. | No |
| TC-09 | The T2 peak shifts to longer relaxation times. | Pass | None | No unsupported mechanism such as pore enlargement added. | No |
| TC-10 | Compared with the low-Da case, the high-Da case shows stronger inlet-localized dissolution. | Pass | None | Comparison baseline and direction preserved. | No |
| TC-11 | Matrix–vug connectivity increases across the Péclet–Damköhler parameter space. | Pass | None | Unicode dash and accented technical expressions preserved. | No |
| TC-12 | Figure 3 demonstrates that the simulated T2 peak shifts to longer relaxation times under the tested conditions. | Pass | None | `demonstrates` retained because the figure directly supports the observation; scope marker preserved. | No |

### Agent 3 Outputs

| Case | Skill output | Result | Failure type | Notes | Rule update needed |
|---|---|---|---|---|---|
| TC-01 | Mineral dissolution occurs widely in natural and engineered systems. | Pass | None | Word order improved only; no mechanism or storyline added. | No |
| TC-02 | These results indicate that NMR T2 evolution can help distinguish dissolution mechanisms in porous media. | Pass | None | `prove` and `robustly diagnoses` were downgraded; NMR T2 and dissolution context preserved. | No |
| TC-03 | This framework links structure to signal and shows the relation between connectivity and breakthrough during dissolution. | Pass | None | Invented compounds were rewritten as plain relations; no new named framework added. | No |
| TC-04 | The pore-coupling index increases during the intermediate stage. Author-confirm: `pore-coupling index` appears manuscript-specific and should be defined if this is its first use. | Pass | None | Undefined term was flagged without inventing a definition. | No |
| TC-05 | The model explains the mechanisms that support channel development. | Pass | None | Decorative wording simplified while preserving the mechanism claim. | No |
| TC-06 | In the simulations, permeability increases at high injection rates, suggesting a transition toward channeling. | Pass | None | Scope marker and cautious `suggesting` preserved. | No |
| TC-07 | The vug contribution accounts for 73.2% at 25% dissolution and increases to 90.5% at 50% dissolution (Figure 2h). | Pass | None | Values, percentages, and figure reference preserved. | No |
| TC-08 | We segment the medium to calculate the flow focusing index. | Pass | None | Heavy nominalization converted to direct method wording. | No |
| TC-09 | The T2 peak shifts to longer relaxation times. | Pass | None | Minimum edit used; no pore-enlargement mechanism added. | No |
| TC-10 | Compared with the low-Da case, the high-Da case shows stronger inlet-localized dissolution. | Pass | None | Comparison baseline and contrast direction preserved. | No |
| TC-11 | Matrix–vug connectivity increases across the Péclet–Damköhler parameter space. | Pass | None | Unicode dash, accents, and technical expressions preserved. | No |
| TC-12 | Figure 3 demonstrates that the simulated T2 peak shifts to longer relaxation times under the tested conditions. | Pass | None | `demonstrates` retained because the sentence points to direct figure evidence; scope marker preserved. | No |

### Agent 4 Outputs

| Case | Skill output | Result | Failure type | Notes | Rule update needed |
|---|---|---|---|---|---|
| TC-01 | Mineral dissolution occurs widely in natural and engineered systems. | Pass | None | Word order improved only; no mechanism or storyline added. | No |
| TC-02 | These results indicate that NMR T2 evolution can help distinguish dissolution mechanisms in porous media. | Pass | None | `prove` and `robustly diagnoses` were downgraded; NMR T2 and dissolution context preserved. | No |
| TC-03 | This framework links structure to signal and shows how connectivity relates to breakthrough during dissolution. | Pass | None | Invented compounds were rewritten as plain relations; no new named framework created. | No |
| TC-04 | The pore-coupling index increases during the intermediate stage. Author-confirm: `pore-coupling index` appears to be manuscript-specific and should be defined if this is its first use. | Pass | None | Undefined term handled without inventing a definition. | No |
| TC-05 | The model explains the mechanisms that support channel development. | Pass | None | Decorative vocabulary simplified while preserving the mechanism claim. | No |
| TC-06 | In the simulations, permeability increases at high injection rates, suggesting a transition toward channeling. | Pass | None | Scope marker and `suggesting` preserved. | No |
| TC-07 | The vug contribution accounts for 73.2% at 25% dissolution and increases to 90.5% at 50% dissolution (Figure 2h). | Pass | None | All values, percentages, and figure reference preserved. | No |
| TC-08 | We segment the medium to calculate the flow focusing index. | Pass | None | Heavy nominalization converted to direct method wording. | No |
| TC-09 | The T2 peak shifts to longer relaxation times. | Pass | None | Minimum edit; no pore-enlargement mechanism added. | No |
| TC-10 | Compared with the low-Da case, the high-Da case shows stronger inlet-localized dissolution. | Pass | None | Comparison baseline and direction of contrast preserved. | No |
| TC-11 | Matrix–vug connectivity increases across the Péclet–Damköhler parameter space. | Pass | None | Unicode dash forms and accented technical terms preserved. | No |
| TC-12 | Figure 3 demonstrates that the simulated T2 peak shifts to longer relaxation times under the tested conditions. | Pass | None | `demonstrates` was not over-downgraded because the figure directly supports the observation; scope marker preserved. | No |

### Run 01 Decision

All four fresh subagents passed all 12 test cases. No repeated failure type appeared. Under the current rule in this file, no rule table should be updated after Run 01 because there is no failure pattern to address.

## Run 02

Run the same 12 test cases only after targeted rule updates from Run 01.

Changes since Run 01:

- None. Run 01 produced 48/48 passes, so no targeted rule update was made.

### Summary

| Total | Passed | Partial pass | Failed |
|---:|---:|---:|---:|
| 12 |  |  |  |

### Acceptance Criteria

Run 02 can freeze v0.1 only if:

- at least 10 of 12 test cases pass;
- there are 0 cases of F1, F2, F3, or F5;
- there are at most 1-2 partial passes;
- no output changes numbers, variables, citations, labels, LaTeX, scope markers, or comparison baselines;
- no rule update makes `SKILL.md` substantially longer or broader in scope.

## Real-Manuscript Test Set

After Run 02 passes, add 10 real manuscript sentences:

| Source section | Number of sentences | Selection priority |
|---|---:|---|
| Introduction | 2 | AI-like but scientifically correct sentences |
| Methods | 2 | Sentences with variables, methods, or protected terms |
| Results | 3 | Sentences with T2, NMR, MVC, values, or figure labels |
| Discussion / Implications | 3 | Sentences with cautious claims or broader implications |

Prefer sentences containing:

- `T2`, `NMR`, `MVC`, or manuscript-specific metrics;
- numerical values, figure labels, equations, or variables;
- `suggests`, `indicates`, `demonstrates`, `may`, or `under these conditions`;
- `matrix–vug`, `Péclet–Damköhler`, or LaTeX-like forms;
- AI-like wording that should be improved without changing the science.

## v0.1 Freeze Criteria

Freeze v0.1 only when:

1. `test_cases.md` has the 12 core test cases.
2. `validation_checklist.md` exists and is used for judgment.
3. `test_run_log.md` contains Run 01 and Run 02.
4. Run 02 reaches at least 10/12 pass.
5. No severe failures remain: F1, F2, F3, or F5.
6. Any rule changes are traceable to repeated failure types.
7. `SKILL.md` remains narrow and sentence-level.

After freezing v0.1, update `modification_log_migration_notes.md`:

```markdown
Stage: v0.1 tested and frozen.
```
