# Workflow Router

Choose the smallest reliable operation.

## 1. Identify the input unit

| Unit | Primary question |
|---|---|
| phrase or title fragment | Is the wording grammatical, precise, and conventional? |
| sentence | Does it express the intended proposition clearly and at the right strength? |
| paragraph | Does it perform one main function with a coherent evidence sequence? |
| section | Are the expected rhetorical moves present, ordered, and connected? |
| manuscript | Does the paper sustain one research story and evidence chain? |

## 2. Identify the requested outcome

- `translate`: convert Chinese or mixed-language content into publication-ready English.
- `polish`: improve English without changing organization or substance.
- `deep-revise`: allow clause, sentence, or paragraph reconstruction.
- `diagnose`: identify problems before rewriting.
- `restructure`: change paragraph or section order.
- `compress`: reduce length while preserving core information.
- `expand`: make existing logic explicit without adding new scientific facts.
- `generate`: draft from supplied facts, moves, and constraints.
- `compare`: explain differences between alternatives.

`Polish` is not permission to add ideas.

## 3. Find the highest problem level

Use the first level that applies:

1. **Scientific integrity:** contradiction, unsupported causality, changed denominator, missing condition, citation mismatch, or unclear ownership.
2. **Storyline/architecture:** unclear question, gap, contribution, evidence chain, or section placement.
3. **Paragraph logic:** mixed functions, poor order, unclear referent, or abrupt transition.
4. **Sentence construction:** ambiguous syntax, overloaded subject, modifier attachment, tense/voice mismatch, or faulty parallelism.
5. **Surface style:** word choice, article, preposition, punctuation, concision, or idiom.

Fixing level 5 cannot compensate for a level 1-3 failure.

## 4. Routing

### Phrase or sentence

Load:

- `protected_content_and_evidence.md`
- `sentence_paragraph_revision.md`
- grammar or claim-strength references as needed

Return the revision first.

### Chinese source

Load:

- `protected_content_and_evidence.md`
- `zh_en_translation.md`
- section reference if known
- terminology resource if uncertain

Translate by scientific function, not source-language word order.

### Paragraph

Load:

- `sentence_paragraph_revision.md`
- the relevant section file
- claim or grammar references as needed

Identify paragraph function before reordering.

### Complete section

Load the matching section reference and `output_contracts.md`. Diagnose missing, duplicated, or misordered moves before line editing.

### Several sections or full paper

Load:

- `manuscript_architecture_audit.md`
- section references
- `target_article_adaptation.md` when a journal or corpus is available

Return priorities before large-scale rewriting.

## 5. Question policy

Ask only when one of these blocks a safe answer:

- two materially different scientific interpretations are possible;
- a technical term has multiple valid translations with different meanings;
- the requested edit depth conflicts with the task;
- an essential journal constraint is missing;
- a suspected data or citation error cannot be handled conservatively.

Otherwise proceed with a conservative assumption and flag it briefly.

## 6. Edit-depth scale

- **A — copy edit:** grammar, article, punctuation, local idiom.
- **B — line edit:** clause order, concision, clarity, information flow.
- **C — paragraph edit:** sentence order, topic sentence, cohesion, split/merge.
- **D — section edit:** rhetorical moves, subsection order, duplication, missing links.
- **E — manuscript edit:** storyline, promise-payoff, evidence chain, architecture.

Do not silently exceed the requested level. If a higher-level defect blocks a lower-level task, state it and offer the smallest safe repair.
