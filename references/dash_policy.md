# Dash Policy

## Purpose

Control the use of hyphenated and dash-based compounds during academic sentence polishing.

The goal is not to remove all dashes. The goal is to distinguish standard technical compounds from AI-like invented labels. Standard field terms should be preserved; decorative or over-compressed compounds should usually be rewritten as plain phrases.

## General Rule

Keep dash compounds when they are:

- standard technical terms;
- measurement ranges;
- established paired concepts;
- necessary modifiers before a noun;
- already defined manuscript terms.

Revise dash compounds when they are:

- newly invented;
- rhetorically decorative;
- too dense;
- used to make the sentence sound more sophisticated;
- replaceable by a clearer plain phrase.

Do not create new dash compounds during polishing.

## Always Keep

| Expression | Reason |
|---|---|
| `pore-scale` | Standard technical modifier |
| `pore-network` | Standard porous-media term |
| `time-resolved` | Standard technical modifier |
| `non-invasive` | Standard scientific modifier |
| `first-order` | Standard reaction or model term |
| `two-dimensional` | Standard dimensional descriptor |
| `low-field NMR` | Standard NMR descriptor |
| `pore-size distribution` | Standard pore-structure descriptor |
| `pore-throat` | Standard porous-media term |
| `solid-liquid interface` | Standard paired physical interface |
| `solid-fluid interface` | Standard paired physical interface |
| `matrix-vug coupling` | Core paper-specific technical term |
| `matrix-vug connectivity` | Core paper-specific technical term |
| `advection-diffusion` | Standard transport pairing |
| `transport-reaction competition` | Standard mechanism pairing |
| `Peclet-Damkohler parameter space` | Standard paired dimensionless-number space |
| `0-4 h` | Numerical range |
| `100-1000 ms` | Numerical range |

## Usually Keep, But Avoid Overuse

| Expression | Rule |
|---|---|
| `NMR-derived metric` | Keep if the metric is derived from NMR data |
| `image-derived description` | Keep if contrasting image data with geophysical signals |
| `field-scale monitoring` | Keep only when the sentence already discusses application scale |
| `pore-structure evolution` | Keep if used as a standard modifier |
| `dissolution-driven pore coupling` | Keep if coupling is caused by dissolution |
| `surface-relaxation-dominated response` | Keep in NMR theory contexts |
| `inlet-to-outlet pathway` | Keep if describing spatial direction |
| `reaction-limited dissolution` | Keep if tied to reaction kinetics |
| `transport-limited dissolution` | Keep if tied to transport limitation |

If several dense compounds appear in one sentence, simplify at least one of them unless each is necessary for precision.

## Use With Caution

| Expression | Risk | Preferred revision |
|---|---|---|
| `structure-signal framework` | Abstract; may sound invented | `a framework linking pore structure to the measured signal` |
| `coupling-breakthrough relation` | Too compressed | `the relation between pore coupling and breakthrough` |
| `dissolution-NMR response` | Dense | `NMR response during dissolution` |
| `signal-mechanism link` | Abstract | `the link between T2 signals and dissolution mechanisms` |
| `flow-path optimization` | Implies intentional optimization | `more direct flow pathways`, if supported |
| `physics-aware interpretation` | Often rhetorical | `interpretation based on the governing physics` |
| `process-response signature` | Vague unless defined | `response associated with the process` |

Keep these only if the manuscript defines them or if the compact form is clearly needed.

## Usually Revise

| Avoid | Revise to |
|---|---|
| `dissolution-NMR-hydraulic framework` | `a framework linking dissolution, NMR response, and hydraulic change` |
| `pore-coupling-informed diagnostic` | `a diagnostic based on pore coupling` |
| `mechanism-diagnostic bridge` | `a diagnostic link to the mechanism` |
| `connectivity-breakthrough nexus` | `the relation between connectivity and breakthrough` |
| `signal-structure-transport paradigm` | `the relation among NMR signals, pore structure, and transport` |
| `matrix-vug-flow-path evolution` | `evolution of matrix-vug coupling and flow paths` |
| `signal-mechanism-breakthrough relationship` | `the relation among signal change, mechanism, and breakthrough` |
| `multi-scale insight-generating framework` | `a framework for comparing processes across scales`, only if this is stated |

## Dash Type Guidance

- Use hyphens for compound adjectives when the manuscript uses plain ASCII style: `pore-scale model`.
- Use en dashes only if the manuscript or journal style already uses them for ranges or paired relations.
- Avoid em-dash sentence interruptions in formal paper prose; use commas, parentheses, or a separate sentence.

## Character and LaTeX Compatibility

Treat these as equivalent forms when judging whether to keep a term:

| Plain ASCII | Unicode manuscript form | LaTeX-like form |
|---|---|---|
| `matrix-vug coupling` | `matrix–vug coupling` | `matrix--vug coupling` |
| `matrix-vug connectivity` | `matrix–vug connectivity` | `matrix--vug connectivity` |
| `solid-liquid interface` | `solid–liquid interface` | `solid--liquid interface` |
| `solid-fluid interface` | `solid–fluid interface` | `solid--fluid interface` |
| `advection-diffusion` | `advection–diffusion` | `advection--diffusion` |
| `transport-reaction competition` | `transport–reaction competition` | `transport--reaction competition` |
| `Peclet-Damkohler` | `Péclet–Damköhler` | `P\\'eclet--Damk\\\"ohler` |

Do not change dash type, accents, or LaTeX spelling unless the user asks for journal-style or LaTeX normalization.

## Editing Rule

If a dash compound is not listed above:

1. Ask whether it is a standard technical term.
2. Ask whether removing the dash changes the meaning.
3. Ask whether a plain phrase is clearer.
4. If the compound sounds newly invented or decorative, rewrite it as a plain phrase.
5. If deciding requires technical knowledge not present in the text, mark `author-confirm`.

## Examples

```text
Original:
This structure-signal framework reveals the dissolution-NMR-hydraulic relationship.

Better:
This framework links pore-structure changes to NMR and hydraulic responses.
```

```text
Original:
The pore-scale model captures matrix-vug connectivity during dissolution.

Better:
Keep as written if both "pore-scale" and "matrix-vug connectivity" are manuscript terms.
```
