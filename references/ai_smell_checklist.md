# AI-Smell Checklist for Academic Sentence Polishing

Use this checklist to diagnose sentence-level AI-like writing before editing. Apply only to expression. Do not use it to change scientific logic, content, mechanism, or manuscript storyline.

## Core Rule

Mark a problem only when the sentence can be improved without adding new scientific information. If the fix requires knowing whether a mechanism, term, or claim is scientifically correct, mark `author-confirm`.

## High-Priority Signals

| Signal | Typical pattern | Preferred action |
|---|---|---|
| Undefined fancy term | `mechanism-diagnostic bridge`, `structure-signal framework` | Define the term if necessary, or replace it with a plain phrase |
| Decorative intensifier | `critically`, `remarkably`, `fundamentally`, `profoundly` | Delete unless quantified or directly supported |
| Overstrong claim | `proves`, `confirms`, `establishes`, `ensures` | Downgrade to `shows`, `suggests`, `supports`, or `is consistent with` |
| Empty contribution phrase | `provides new insights into`, `opens a new avenue` | State the concrete relation, metric, or use case |
| Long abstract subject | `The establishment of a comprehensive...` | Move the physical object, model, signal, or process to subject position |
| Heavy nominalization | `the occurrence of`, `the implementation of` | Convert to a direct verb |
| Rare decorative verb | `elucidate`, `delineate`, `unveil`, `facilitate` | Replace with a simple verb if equally precise |
| Invented dash compound | `connectivity-breakthrough nexus` | Rewrite as ordinary syntax |
| New dash compound in the revision | source says `based on pore structure`; revision says `pore-structure-aware` | Reject the revision unless the exact expression is a standard or defined term |
| Unclear causal jump | observation followed by broad mechanism | Keep observation first and ask for confirmation if mechanism is not explicit |
| Scope loss | removing `in simulations`, `under these conditions`, `for the tested cases` | Preserve scope markers |

## Sentence-Level Diagnosis Labels

Use these labels in `Main edits` when useful:

- `undefined-term`
- `overclaim`
- `decorative-intensifier`
- `unnecessary-compound`
- `heavy-nominalization`
- `rare-word`
- `long-subject`
- `unclear-causal-link`
- `scope-drift`
- `technical-content-risk`

## Forbidden Fixes

Do not:

- add a new mechanism to make the sentence sound deeper;
- add a new citation or literature judgment;
- create a new named framework;
- create a new hyphenated, en-dash, or em-dash compound to make the revision sound more academic;
- replace a precise technical term with a vague simple word;
- remove uncertainty markers such as `may`, `might`, `could`, `suggests`, or `is consistent with`;
- remove numerical values, units, variables, citations, or figure references for fluency;
- turn a sentence-level polish into a paragraph rewrite.

## Quick Pass

Before editing, ask:

1. Is the problem about expression rather than scientific content?
2. Can a local edit fix it?
3. Will the revised sentence preserve evidence strength?
4. Are all protected technical elements unchanged?
5. Did the revision avoid new dash-based labels unless they are standard or defined terms?
