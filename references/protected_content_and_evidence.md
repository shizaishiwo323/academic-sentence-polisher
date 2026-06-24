# Protected Content and Evidence

## Purpose

Prevent fluent editing from altering scientific content.

## 1. Build a protection map

### Exact tokens

Treat these as immutable unless the user explicitly asks for correction:

- numbers, ranges, percentages, p-values, confidence intervals, and sample sizes;
- signs, inequality symbols, exponents, subscripts, superscripts, and significant figures;
- units and unit spacing;
- equations, LaTeX, variables, code identifiers, and model names;
- citations, reference order, DOI strings, figure/table/equation labels;
- chemical formulas, gene/protein names, species names, and abbreviations.

### Semantic constraints

Record:

- agent: who performed or observed the action;
- object: what was measured, changed, or compared;
- direction: increase/decrease, higher/lower, positive/negative;
- baseline or comparator;
- tested conditions, population, material, scale, and time;
- whether the claim is descriptive, associative, causal, predictive, or normative;
- degree of certainty;
- whether the claim belongs to this study or prior work.

## 2. Evidence-strength ladder

```text
direct observation or formal derivation
> robust result under stated conditions
> interpretation supported by converging evidence
> indication or association
> plausible possibility
> speculation
```

A revision must remain on the same rung unless the user supplies justification.

Unsafe strengthening includes:

- `was associated with` -> `caused`
- `suggests` -> `demonstrates`
- `may improve` -> `improves`
- `under the tested conditions` -> an unrestricted generalization
- `one possible explanation` -> `the mechanism`
- `higher` -> `significantly higher` without support
- `consistent with` -> `confirms`

## 3. Ownership of claims

Make the source visible:

- cited study: author or citation in the same sentence or unambiguous local context;
- accepted knowledge: present-tense factual statement, cited when needed;
- present study: `we`, `this study`, `our analysis`, or clear section context;
- inference: `suggests`, `is consistent with`, a modal, or another explicit signal.

Do not let an agentless passive make cited work look like the current authors' work.

## 4. Data and figure integrity

When revising Results:

- preserve absolute versus relative change;
- distinguish percent change from percentage points;
- retain uncertainty and variability;
- keep the correct comparator and denominator;
- do not call a pattern monotonic, linear, stable, negligible, or significant without support;
- do not add a trend not stated or visible.

If prose conflicts with supplied data, flag the conflict rather than silently choosing one.

## 5. Citation integrity

Do not:

- invent a reference;
- move a citation so it appears to support a different claim;
- merge sentences in a way that broadens citation scope;
- assert consensus from a single study;
- split or combine sentences without preserving citation-to-claim alignment.

## 6. `author-confirm`

Use when:

- terminology has multiple field meanings;
- a causal interpretation is plausible but unstated;
- a numerical inconsistency appears;
- claim ownership is unclear;
- a limitation or implication would require new information;
- grammatical repair requires choosing between scientific interpretations.

Format:

```text
author-confirm: Does X refer to ... or ...? The revision currently uses the more conservative interpretation.
```
