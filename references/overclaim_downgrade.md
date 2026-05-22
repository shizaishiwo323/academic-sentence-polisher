# Overclaim Downgrade

## Purpose

Prevent sentence polishing from overstating evidence.

The skill should preserve the original evidence strength. It should downgrade exaggerated wording and avoid turning local simulation results, limited observations, or manuscript-specific findings into broad claims.

## Core Rule

Before changing a sentence, check whether the original text supports the strength of each claim. If support is missing or local, use weaker wording. If downgrading would change the intended scientific judgment, mark `author-confirm`.

Do not automatically downgrade a strong verb if the original sentence already has direct evidence and the verb is appropriate. First decide whether the problem is overclaiming or merely formal academic wording.

Do not strengthen:

- `suggests` to `demonstrates`;
- `indicates` to `proves`;
- `is consistent with` to `confirms`;
- `may`, `might`, or `could` to unqualified certainty;
- a local simulation result to a general field-scale conclusion.

## Verb Downgrade

| Avoid or use with caution | Safer alternatives | Rule |
|---|---|---|
| `prove` | `show`, `indicate`, `support` | Use `prove` only for formal proof, not simulation evidence |
| `demonstrate` | `show`, `indicate` | Use only when the evidence is direct and strong |
| `establish` | `support`, `provide`, `define` | Avoid if the result is not broadly validated |
| `reveal` | `show`, `indicate` | Use sparingly; avoid discovery tone |
| `confirm` | `support`, `is consistent with` | Use only with independent validation |
| `validate` | `support`, `benchmark`, `compare against` | Use only for strong validation against independent data |
| `enable` | `allow`, `support`, `provide a basis for` | Avoid implying direct operational capability |
| `predict` | `estimate`, `indicate`, `suggest` | Use only if a predictive model is tested |
| `govern` | `control`, `influence`, `is associated with` | Use only for clearly established mechanisms |

## Adverb Downgrade

| Avoid or use with caution | Preferred action |
|---|---|
| `remarkably` | Delete or replace with a quantitative statement |
| `critically` | Delete unless truly essential |
| `fundamentally` | Delete or replace with a specific description |
| `dramatically` | Replace with `substantially` only if data support it |
| `significantly` | Use only with statistical or clear quantitative support |
| `robustly` | Replace with `consistently` only if repeated evidence exists |
| `clearly` | Delete unless needed for contrast |
| `effectively` | Delete unless describing a method function |
| `uniquely` | Avoid unless uniqueness is proven |

## Adjective Downgrade

| Avoid or use with caution | Safer alternatives |
|---|---|
| `novel` | `proposed`, `developed`, `used here`, or delete |
| `unprecedented` | Delete |
| `transformative` | Delete |
| `critical` | `important`, `relevant`, `central`, `required` |
| `powerful` | `useful`, `sensitive`, `informative` |
| `universal` | `general` or `broader`, only if supported |
| `robust` | `consistent`, `stable`, `insensitive to tested conditions` |
| `comprehensive` | `integrated`, `combined` |

## Sentence-Level Overclaim Patterns

| Risky pattern | Safer pattern |
|---|---|
| `This framework enables field-scale monitoring.` | `This framework may support future field-scale monitoring.` |
| `These results prove that NMR can identify dissolution regimes.` | `These results indicate that T2 evolution can distinguish dissolution regimes under the simulated conditions.` |
| `MVC provides a universal diagnostic of breakthrough.` | `MVC provides an NMR-derived index for matrix-vug coupling in these simulations.` |
| `The method resolves the long-standing problem of ...` | `The method addresses part of this problem by ...` |
| `This finding fundamentally changes our understanding of ...` | `This finding links ... to ... under the conditions studied here.` |

## Evidence-Strength Rule

Use:

- `shows` for direct observations from results;
- `indicates` for supported interpretation;
- `suggests` for plausible but indirect interpretation;
- `is consistent with` for agreement with prior work or indirect support;
- `may` for implications beyond the tested conditions;
- `under these conditions` or `in these simulations` when the conclusion is simulation-specific.

Prefer deleting subjective intensifiers over replacing them with another intensifier.
