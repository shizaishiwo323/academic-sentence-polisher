# Chinese-to-English Scientific Translation

## Goal

Produce natural scientific English that preserves the Chinese proposition, evidence strength, and rhetorical role.

Translation is reconstruction, not word substitution.

## 1. Workflow

### A. Parse the proposition

Identify:

- topic and main claim;
- actor or logical subject;
- action or relation;
- object;
- conditions and scope;
- evidence source;
- comparison or causal direction;
- uncertainty and degree;
- function in the manuscript section.

### B. Choose an informative English subject

Prefer:

- `This study...`
- `The proposed method...`
- `The results...`
- `Figure 3...`
- `Increasing temperature...`
- `Previous studies...`

Do not repeatedly translate `本文`, `本研究`, `可以看出`, or `研究发现` as empty subjects when a more informative subject exists.

### C. Choose section-appropriate tense

- Introduction background: present simple.
- Specific completed prior study: past simple.
- Research activity with current relevance: present perfect.
- Study-specific procedure: usually past simple.
- Study result: usually past simple; present simple only when a general relationship is intentionally claimed.
- Interpretation: calibrated reporting verb or modal.

### D. Rebuild information order

Prefer:

```text
known/contextual information -> new information
condition -> main proposition
main clause -> bounded qualification
```

Keep subject and main verb reasonably close.

### E. Remove Chinese-to-English artifacts

Watch for:

- empty openings;
- repeated abstract subjects;
- strings of prepositional phrases;
- long noun stacks;
- excessive passives;
- unnecessary `there be` constructions;
- vague evaluations such as `important significance`;
- multiple logical relations joined only by commas.

### F. Back-check meaning

Check for omitted conditions, changed comparison, stronger causality, changed certainty, lost negation, altered time reference, and wrong claim ownership.

## 2. High-risk patterns

### `随着……的发展`

Do not automatically write `With the continuous development of...`.

Use only when historical development matters. Often prefer:

- `Recent advances in X have enabled...`
- `X is increasingly used for...`
- or omit the frame and state the scientific fact.

### `越来越多`

Avoid `more and more` in formal prose.

Possible choices:

- `an increasing number of`
- `has received increasing attention`
- `is increasingly used`

Do not imply a measured trend without evidence.

### `对……进行了研究/分析/测试`

Prefer a direct verb:

- `We investigated X.`
- `X was analyzed using Y.`
- `The study evaluated X under Y conditions.`

### `结果表明`

Choose by evidence and rhetorical function:

- `The results showed that...` for a completed observation.
- `The results indicate that...` for a current interpretation.
- `These findings suggest that...` for a cautious inference.

Do not use `prove` for ordinary empirical evidence.

### `可以看出/由图可知`

Prefer:

- `Figure 2 shows that...`
- `As shown in Figure 2, ...`
- or state the result directly.

Avoid `It can be seen that` when a direct construction is clearer.

### `具有重要意义`

Do not write `has important significance`.

State the concrete supported value:

- `This finding helps explain...`
- `The method may improve...`
- `The result provides evidence for...`

If no concrete implication is supplied, omit or mark `author-confirm`.

### `为……提供理论依据/参考`

Use a `theoretical basis` only when a theory is actually established. Depending on meaning, prefer:

- `provides evidence for`
- `provides a basis for`
- `may inform`

### `在一定程度上`

Identify what is limited:

- partial magnitude: `partly`, `to some extent`;
- limited conditions: state the conditions;
- uncertain inference: use a modal or cautious reporting verb.

### `首次`

Use `for the first time` only after novelty is verified. Otherwise mark `author-confirm`.

## 3. Terminology

Use:

1. user glossary;
2. terminology already defined in the manuscript;
3. stable target-article usage;
4. recognized field-standard terminology.

When two translations remain possible, provide the publication-ready choice and briefly state the alternative meaning.

## 4. Default output

```text
Translation:
...

Notes:
- terminology or ambiguity note, only if material;
- claim-strength note, only if material.
```

Do not include a literal translation unless requested.
