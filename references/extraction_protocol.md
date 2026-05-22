# Extraction Protocol

This file defines how to extract sentence-level examples from the seven reference papers. The corpus is used to derive polishing rules, not to copy source sentences or imitate a paper's scientific argument.

## Scope

The extraction only supports sentence-level academic polishing:

- improve clarity, concision, and evidence control;
- preserve scientific meaning, citations, variables, figure labels, equations, and paragraph order;
- avoid unsupported mechanisms, new claims, broader implications, or changes to the paper storyline.

When a sentence contains a scientific judgment that cannot be verified from the local text, mark it as `author-confirm` rather than rewriting the judgment.

## Paper IDs

| Paper ID | Source file |
|---|---|
| P01 | `Geophysical Research Letters - 2018 - Niu - Physical Explanation of Archie s Porosity Exponent in Granular Materials  A.pdf` |
| P02 | `Geophysical Research Letters - 2024 - Szawełło - Quantifying Dissolution Dynamics in Porous Media Using a Spatial Flow.pdf` |
| P03 | `Geophysical Research Letters - 2025 - Deng - Anomalous Transport in Dissolving Porous Media  Transitions Between Fickian.pdf` |
| P04 | `Geophysical Research Letters - 2026 - Zhou - How Does Fluid Exchange Between Pores in Unsaturated Porous Media.pdf` |
| P05 | `JGR Solid Earth - 2020 - Niu - A Framework for Pore‐Scale Simulation of Effective Electrical Conductivity and Permittivity (1).pdf` |
| P06 | `Water Resources Research - 2019 - Niu - Permeability Prediction in Rocks Experiencing Mineral Precipitation and Dissolution.pdf` |
| P07 | `Water Resources Research - 2025 - Zhou - How Does Pore Structure Affect the NMR Relaxation in Unsaturated Porous Media  A.pdf` |

## Extraction Target

For the first complete corpus pass:

- extract 10 sentence records per paper;
- keep all seven papers represented;
- cover Introduction, Methods, Results, and Discussion/Conclusion where possible;
- tag every record by writing function;
- convert every selected sentence into a reusable polishing rule.

The corpus can later be expanded to 12-15 records per paper after the rule cards are tested on the user's own manuscript sentences.

## Function Tags

| Tag | Meaning | What the skill should learn |
|---|---|---|
| `DEF` | Defines a term, variable, metric, or concept | Introduce specialized terms without making readers guess |
| `GAP` | States a research gap | Name a specific unresolved relation, mechanism, metric, or condition |
| `AIM` | States the study aim or contribution | Say what the paper does without promotional language |
| `MET` | Describes method, model, data, or workflow | Keep method sentences concrete and bounded |
| `ASS` | States an assumption or simplification | Explain scope without defensiveness |
| `RES` | Reports results | Put observation, direction, comparison, and numbers before interpretation |
| `CON` | Compares cases, mechanisms, or prior work | Use contrast to clarify, not to exaggerate |
| `IMP` | Interprets mechanism, implication, limitation, or future use | Keep interpretation tied to evidence and conditions |

## Scoring

Each candidate sentence is scored out of 10. Keep records scoring 7 or above.

| Criterion | Score | Question |
|---|---:|---|
| Clarity | 0-2 | Are the subject, verb, and object easy to identify? |
| Concision | 0-2 | Does the sentence avoid loose intensifiers, empty nouns, and unnecessary complexity? |
| Transferability | 0-2 | Can this sentence be converted into a reusable polishing instruction? |
| Evidence control | 0-2 | Does the sentence avoid overstating the evidence? |
| Section value | 0-2 | Is it representative of a common sentence function in that section? |

## Keep / Reject Rules

Keep sentences that:

- define a technical term at first use;
- state a concrete gap without attacking prior work;
- report a result before interpreting it;
- use a bounded claim such as `suggests`, `is consistent with`, or `under these conditions`;
- explain a method or assumption without adding results;
- show how to compare cases cleanly.

Reject sentences that:

- are good mainly because of paper logic rather than sentence expression;
- rely on long lists of citations and cannot be reused as a writing pattern;
- use fancy terms without local definition;
- contain broad claims such as `opens a new avenue` or `fundamentally changes` without strong support;
- are too context-specific to become a polishing rule.

## Record Template

Use a block record rather than a large table.

```markdown
## Pxx-Sxx

**Section:** Introduction / Methods / Results / Discussion / Conclusion  
**Function tag:** DEF / GAP / AIM / MET / ASS / RES / CON / IMP  
**Score:** 7-10/10  

**Source sentence:**  
> One selected sentence.

**Local context:**  
What this sentence does in its paragraph.

**Why it works:**  
Why it is effective at the sentence-expression level.

**Transferable rule:**  
The reusable writing rule.

**Reusable pattern:**  
`A compact pattern that can guide polishing.`

**Risk when misused:**  
How the pattern could become overstated, vague, or AI-like.

**Skill-ready instruction:**  
An instruction that can be copied into the polishing skill.
```

## Extraction Workflow

1. Build a broad candidate pool from each PDF.
   - Verify: each paper has Introduction, Methods, Results, and Discussion/Conclusion candidates when available.

2. Score and keep at least 10 records per paper.
   - Verify: every retained sentence scores 7 or above and has a function tag.

3. Convert each sentence into a rule-oriented record.
   - Verify: every record contains `Transferable rule`, `Risk when misused`, and `Skill-ready instruction`.

4. Consolidate rules by function tag into `corpus_rule_cards.md`.
   - Verify: each tag has multiple rule cards and at least one preferred pattern.

## Quality Control

After each extraction pass, check:

- all 7 papers are represented;
- total records are between 70 and 105;
- no record is just a copied sentence without analysis;
- every record supports sentence polishing rather than scientific argument revision;
- every record can help decide whether to define a term, remove a fancy phrase, reduce overclaim, simplify syntax, or preserve evidence strength;
- no rule encourages adding mechanisms, new interpretations, or broader claims.
