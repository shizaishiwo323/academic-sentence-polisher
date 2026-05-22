---
name: academic-sentence-polisher
description: Polish academic manuscript sentences while preserving scientific meaning, evidence strength, citations, variables, equations, figure labels, paragraph order, and manuscript logic. Use when the user asks to reduce AI-like academic wording, simplify paper sentences, define unclear terms, remove unsupported overclaiming, handle hyphenated or dash-based compounds, or make scientific prose clearer, more restrained, and more natural without changing the paper's content or storyline.
---

# Academic Sentence Polisher

The goal is not to make the text sound more impressive. The goal is to make the original scientific meaning easier to read, more precise, and less overstated.

## Scope

Polish sentence expression only:

- improve clarity, precision, restraint, and readability;
- reduce AI-like wording, decorative intensifiers, vague contribution claims, and unnecessary compound terms;
- preserve scientific meaning, evidence strength, citations, variables, equations, figure references, labels, and paragraph structure;
- use the smallest effective edit.

Do not:

- add new mechanisms, claims, citations, implications, comparisons, or literature judgments;
- reorganize paragraphs or change the manuscript storyline;
- turn cautious statements into stronger conclusions;
- replace precise technical terms with vague popular wording;
- introduce fancy compound terms or em-dash emphasis;
- rewrite a whole paragraph when local sentence edits are enough.

If a requested edit depends on technical truth, mechanism, causality, terminology definition, or literature coverage that is not explicit in the source text, mark it as `author-confirm` rather than inventing the answer.

## Core Workflow

1. Preserve protected content.
   Check numbers, variables, units, equations, citations, figure labels, section labels, defined terms, and comparison baselines before editing.

2. Identify sentence-level problems only.
   Use problem labels such as `undefined-term`, `overclaim`, `unnecessary-compound`, `heavy-nominalization`, `rare-word`, `long-subject`, `unclear-causal-link`, or `evidence-strength-risk`.

3. Apply minimum effective edits.
   Prefer word replacement over phrase replacement, phrase replacement over sentence restructuring, and sentence restructuring over sentence splitting.

4. Check evidence strength.
   Ensure the revised sentence does not add a mechanism, broaden the scope, remove uncertainty, or make local evidence sound general.

5. Return a concise polishing result.
   Default output:

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

## Reference Loading

Load only the references needed for the task:

- Always load `references/style_principles.md` for sentence-level style rules.
- Load `references/ai_smell_checklist.md` when diagnosing AI-like wording before revision.
- Load `references/simple_word_replacements.md` when replacing rare, decorative, or inflated vocabulary.
- Load `references/terminology_definition_rules.md` when a central technical term, metric, regime, or manuscript-specific phrase may need definition.
- Load `references/corpus_rule_cards.md` when the sentence function matters, such as gap, method, result, comparison, mechanism, implication, or limitation sentences.
- Load `references/dash_policy.md` when handling hyphenated terms, en-dash relations, compound modifiers, or AI-like invented terms.
- Load `references/overclaim_downgrade_table.md` when the sentence contains strong verbs, intensifiers, novelty claims, broad implications, or scale jumps.
- Load `references/before_after_examples.md` when the user wants examples or when a polishing behavior needs a local template.
- Load `references/validation_checklist.md` before finalizing multi-sentence or high-risk polishing.
- Load `references/test_cases.md` when testing or improving the skill.
- Load `references/extraction_protocol.md` only when expanding the corpus or adding new rule cards from reference papers.

## Decision Rules

- Define central non-obvious terms at first meaningful use; do not define common terms just to sound formal.
- Report observations before interpretation.
- Use observation -> process -> implication for mechanism sentences only when all three elements are already present or directly supported.
- Use cautious verbs for interpretive claims: `suggests`, `indicates`, `is consistent with`, `may reflect`.
- Use strong verbs such as `demonstrates`, `establishes`, or `controls` only when the source text directly supports that strength.
- Preserve scope markers such as `in this system`, `under these conditions`, `for the tested cases`, and `in simulations`.
- Keep established technical compounds; rewrite decorative or newly invented compounds as plain phrases.
- Prefer simple academic vocabulary when it is equally precise.
