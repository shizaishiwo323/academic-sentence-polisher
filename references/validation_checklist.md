# Validation Checklist

Use this checklist before finalizing sentence polishing, especially for multi-sentence edits or sentences containing variables, figures, mechanisms, or strong claims.

## Pass/Fail Criteria

The revision passes only if all required checks pass.

| Check | Pass condition |
|---|---|
| Meaning preserved | The scientific claim is unchanged |
| Evidence strength preserved | The revision does not strengthen or broaden the claim |
| No new mechanism | No causal process is added unless already present |
| No new implication | The revision does not add application, prediction, or field-scale meaning |
| Protected content preserved | Numbers, units, variables, equations, citations, labels, and figure references are unchanged |
| Scope preserved | Qualifiers such as `in simulations`, `under these conditions`, and `for the tested cases` remain visible |
| Sentence-level only | No paragraph order, storyline, or content structure is changed |
| AI smell reduced | At least one expression problem is improved when the original had one |
| Minimum edit used | The edit is no larger than needed |

## Protected Content

Never silently alter:

- numerical values and percentages;
- units and ranges;
- variables and symbols;
- equations and inequalities;
- citations and citation commands;
- figure, table, section, and supplement labels;
- named regimes and metrics;
- comparison baselines;
- uncertainty markers;
- scope markers.

## Evidence-Strength Check

Reject or revise if the polished sentence changes:

- `may` / `might` / `could` -> certainty;
- `suggests` -> `demonstrates`;
- `is consistent with` -> `confirms`;
- local condition -> general law;
- simulation result -> field-scale prediction;
- observation -> mechanism without support.

## Output Check

A good final response should include:

```text
Revised version:
...

Main edits:
1. ...
2. ...

Meaning preserved:
Yes / Potential issue: ...
```

Keep `Main edits` short. Do not turn the answer into a peer review unless the user asks for review.
