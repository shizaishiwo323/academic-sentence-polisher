# Overclaim Downgrade Table

This file lists high-risk words and claim patterns found during corpus cleaning. The skill must not add these words during polishing. If they appear in the user's sentence, preserve them only when the sentence gives direct numerical, experimental, theoretical, or literature support.

## Core Rule

Default action:

1. Check whether the original sentence provides support for the strength of the word.
2. If support is missing or local, downgrade the word.
3. If the word changes the scientific claim, mark `author-confirm` instead of silently rewriting.

Do not strengthen:

- `suggests` -> `demonstrates`
- `is consistent with` -> `confirms`
- `may` / `might` / `could` -> unqualified present-tense certainty
- local simulation result -> general field-scale conclusion

## Downgrade Table

| High-risk expression | Main risk | Safer alternatives | Keep only when |
|---|---|---|---|
| `solely` | Excludes all other explanations | `often`, `primarily`, `largely`, `mainly` | The cited literature or data explicitly show exclusivity |
| `no study` | Requires complete literature certainty | `few studies`, `limited work`, `to our knowledge, no study` | The author has verified the literature scope |
| `universal` | Turns a tested pattern into a general law | `consistent`, `common`, `cross-sample`, `for the tested cases` | The evidence spans the full domain claimed |
| `demonstrates` | May overstate inference strength | `shows`, `indicates`, `suggests` | The result directly establishes the claim |
| `ensures` | Implies guaranteed outcome | `helps ensure`, `reduces the risk of`, `keeps X from` | The mechanism guarantees the outcome by definition |
| `proves` | Too strong for most empirical results | `shows`, `supports`, `is consistent with` | A formal proof or decisive test is present |
| `confirms` | Implies independent validation | `supports`, `is consistent with`, `agrees with` | The result validates a prior hypothesis directly |
| `fundamentally` | Inflates mechanism or importance | delete, or use `substantially` only with evidence | The change alters the governing mechanism |
| `remarkably` | Subjective emphasis | delete, or specify the quantitative magnitude | A quantitative contrast makes the remark necessary |
| `dramatically` | Inflated magnitude | `substantially`, `markedly`, `increases/decreases` | The magnitude is clearly large and quantified |
| `significantly` | Ambiguous: statistical or informal | `substantially`, `clearly`, or exact statistic | Statistical significance or a clear magnitude is given |
| `profound` | Promotional or vague | `strong`, `large`, `measurable`, `important` | The paper quantifies a large effect |
| `sharply` | May exaggerate trend | `rapidly`, `markedly`, `increases/decreases` | The trend has a clear steep transition |
| `critical` | Often vague importance claim | `important`, `relevant`, `controlling`, `required` | The factor is necessary or rate-limiting |
| `robust` | Vague reliability claim | `consistent`, `stable`, `reproducible` | Repeated tests support robustness |
| `novel` | Promotional novelty claim | `new`, `not previously tested`, or delete | Novelty is explicitly part of the manuscript claim |
| `provides new insights into` | Generic contribution sentence | state the concrete relation or method output | The sentence also names the specific insight |
| `opens a new avenue` | Promotional implication | delete, or state the immediate application | The manuscript explicitly discusses that application |
| `enables field-scale prediction` | Unsupported scale jump | `may support future field-scale prediction` | Field-scale validation is included |

## Claim-Strength Ladder

Use the weakest wording that preserves the original claim.

| Evidence situation | Preferred wording |
|---|---|
| Direct observation in the reported data | `shows`, `indicates` |
| Pattern supports but does not prove mechanism | `suggests`, `is consistent with` |
| Plausible explanation for discrepancy | `may be due to`, `might reflect`, `could arise from` |
| Model applicability under tested cases | `works for`, `is applicable to`, `depends on` |
| Extrapolation beyond tested cases | `may support`, `could help`, `requires further testing` |

## Corpus-Derived Caution Words

These words appeared in otherwise useful source sentences and should trigger a review before being retained:

```text
solely
no study
universal
demonstrates
ensures
profound
sharply
fundamentally
remarkably
dramatically
significantly
critical
robust
```

## Skill Instructions

- Never add a high-risk word just to make prose sound stronger.
- When the user's original sentence already contains a high-risk word, first decide whether the claim is supported.
- Prefer deleting subjective intensifiers over replacing them with another intensifier.
- Preserve cautious verbs such as `suggests`, `may`, `might`, `could`, and `is consistent with`.
- If downgrading may change the scientific claim, ask for author confirmation.
