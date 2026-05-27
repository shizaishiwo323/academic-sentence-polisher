---
name: academic-sentence-polisher
description: Polish academic manuscript sentences while preserving scientific meaning, evidence strength, citations, variables, equations, figure labels, paragraph order, and manuscript logic. Use when the user asks to reduce AI-like academic wording, simplify paper sentences, define unclear terms, remove unsupported overclaiming, handle hyphenated or dash-based compounds, or make scientific prose clearer, more restrained, and more natural without changing the paper's content or storyline.
---

# Academic Sentence Polisher

## Purpose

Improve academic sentence-level expression while preserving the original scientific meaning, evidence strength, logic, citations, equations, labels, and paragraph structure.

The goal is not to make the text sound more impressive, but to make the original scientific meaning easier to read, more precise, and less overstated.

## Scope

This skill can:

- improve sentence clarity;
- reduce AI-like phrasing;
- simplify unnecessarily complex wording;
- remove or revise unnecessary dash compounds;
- downgrade overstatements;
- define or simplify unclear technical terms;
- improve grammar and flow with minimal edits.

This skill must not:

- add new scientific claims, mechanisms, interpretations, citations, or implications;
- change paragraph logic, manuscript structure, or storyline;
- strengthen conclusions beyond the original evidence;
- convert cautious statements into broad claims;
- replace precise technical terms with vague popular terms;
- rewrite a well-functioning sentence merely to make it sound more polished.

If a requested edit depends on technical truth, mechanism, causality, terminology definition, or literature coverage that is not explicit in the source text, mark it as `author-confirm` rather than inventing the answer.

## Highest-Priority Principles

1. Preserve meaning before improving style.
2. Use the smallest effective edit.
3. Do not make the sentence sound more important than the evidence allows.
4. Prefer simple and precise words over fancy words.
5. Keep technical terms when they are standard in the field.
6. Do not introduce a new term unless the original text already requires it.
7. Do not change numbers, variables, citations, equations, labels, figure references, or table references.
8. Do not make the revised sentence substantially longer than the original unless clarity requires it; by default, keep it within about 110% of the original length.
9. Do not create new hyphenated, en-dash, or em-dash compounds during polishing unless the exact expression is a standard technical term or already defined in the manuscript.

## Workflow

### Step 1. Identify protected content

Before editing, identify and preserve:

- numerical values, units, variables, and symbols;
- LaTeX commands and equations;
- citations and references;
- figure, table, text, and equation labels;
- technical terms and abbreviations;
- stated causal relationships;
- uncertainty markers and evidence strength.

### Step 2. Diagnose sentence-level problems

Check whether the sentence contains:

- undefined or unnecessary fancy terms;
- unnecessary, invented, or decorative dash compounds;
- overclaiming or overly strong adverbs;
- rare, decorative, or unnatural words;
- heavy nominalization;
- long or unclear subjects;
- unclear causal connectors;
- AI-like summary or contribution phrases.

### Step 3. Apply minimal edits

Prefer the smallest possible change:

```text
word replacement > phrase replacement > clause restructuring > sentence splitting
```

Do not rewrite the whole sentence if replacing one phrase solves the problem. Do not rewrite the whole paragraph unless the user explicitly asks.

### Step 4. Remove AI-like dash compounds

Before finalizing any revision, check whether the polished version contains a new expression joined by a hyphen, en dash, or em dash. If it was not present in the source text and is not a standard technical term, replace it with ordinary syntax.

Use plain wording instead of invented labels:

- `mechanism-aware interpretation` -> `interpretation based on the mechanism`, if the mechanism is stated;
- `signal-structure bridge` -> `the relation between signal and structure`;
- `context-sensitive response` -> `a response that depends on context`;
- em-dash emphasis -> a comma, parentheses, or a separate sentence.

If a compact dash expression may be a professional term but this cannot be confirmed from the source text, keep the meaning in plain wording and mark `author-confirm` if the term itself matters.

### Step 5. Check evidence strength

After editing, check:

- Did the revision add a new claim?
- Did it make the claim stronger?
- Did it imply broader applicability?
- Did it add a mechanism not stated in the original?
- Did it change uncertainty or causality?

If yes, revise again to restore the original evidence strength.

### Step 6. Produce a concise output

Use the requested output style. If the user does not specify a format, use:

```text
Revised version:
...

Main edits:
1. ...
2. ...

Meaning preserved:
Yes / Potential issue: ...
```

Keep the explanation short. This skill is for polishing sentences, not reviewing the paper.

Do not provide detailed review comments unless the user asks for explanation. Output the polished sentence or passage first.

## Reference Loading

Load only the files needed for the sentence being polished:

- Load `references/dash_policy.md` for hyphenated terms, en-dash relations, compound modifiers, or AI-like invented compounds.
- Load `references/overclaim_downgrade.md` for strong verbs, intensifiers, novelty claims, broad implications, or scale jumps.
- Load `references/simple_word_replacement.md` for rare, decorative, inflated, or AI-like vocabulary.
- Load `references/terminology_definition.md` for central technical terms, manuscript-specific metrics, regimes, abbreviations, or unclear named relations.

Do not load extended corpus notes, examples, or test files unless the user explicitly asks to expand or test the skill.

## Do Not Do

Do not:

- add background information;
- add transition sentences;
- add literature comparisons;
- add broader implications;
- add novelty claims;
- add field-scale implications unless already stated;
- introduce new compound terms;
- convert plain source wording into a new hyphenated or dash-based label such as `mechanism-aware`, `signal-structure`, `context-sensitive`, or `process-response`;
- use em dashes for dramatic emphasis;
- use inflated words such as `revolutionary`, `unprecedented`, `critical`, or `remarkable` unless the evidence explicitly supports them;
- change `suggests` to `demonstrates`, `indicates` to `proves`, or `may` to an unqualified claim;
- change `under these conditions` or `in these simulations` into a general statement.
