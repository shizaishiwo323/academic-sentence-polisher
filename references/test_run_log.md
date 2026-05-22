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

Date:
Tester:

### Summary

| Item | Result |
|---|---|
| Total test cases | 12 |
| Passed |  |
| Partial pass |  |
| Failed |  |
| Main failure type |  |
| Rule update needed | Yes / No |

### Failure Summary

| Failure type | Count | Cases |
|---|---:|---|
| F1 Meaning drift |  |  |
| F2 Evidence strengthened |  |  |
| F3 New mechanism added |  |  |
| F4 New implication added |  |  |
| F5 Protected content changed |  |  |
| F6 Scope marker removed |  |  |
| F7 Unnecessary expansion |  |  |
| F8 Invented compound retained or created |  |  |
| F9 Technical term oversimplified |  |  |
| F10 Undefined term not handled |  |  |
| F11 Over-downgraded valid claim |  |  |
| F12 Output too verbose |  |  |

### Case-by-Case Results

#### TC-01

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-02

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-03

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-04

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-05

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-06

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-07

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-08

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-09

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-10

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-11

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

#### TC-12

Input:

Skill output:

Expected behavior:

Result:

Failure type:

Notes:

Rule update needed:

## Run 02

Run the same 12 test cases after any targeted rule updates from Run 01.

Changes since Run 01:

- 

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
