# Terminology Definition

## Purpose

Control when and how technical terms should be defined during sentence-level polishing.

The skill should not introduce fancy terms unnecessarily. If a term is central, new, manuscript-specific, or potentially unclear, define it briefly at first use or replace it with a plain phrase.

## Core Rule

Define central non-obvious terms at first meaningful use. Do not invent definitions. If the required definition is not explicit in the source text, mark `author-confirm`.

## Terms That Must Be Defined At First Use

| Term type | Definition rule | Example pattern |
|---|---|---|
| New metric | Define what it measures | `We define X as a metric that quantifies ...` |
| New index | Define input and interpretation | `X denotes ... and increases when ...` |
| Paper-specific concept | Define in plain scientific language | `Here, X refers to ...` |
| Abbreviation | Spell out first, then abbreviate | `matrix-vug connectivity (MVC)` |
| Nonstandard compound term | Define or replace | `X, defined here as ...` |
| Ambiguous process term | Specify the process only if the source text supports it | `Coupling refers to ...` |

In the current manuscript context, likely define:

- `matrix-vug connectivity (MVC)`;
- `matrix-vug coupling`;
- `pore coupling`, if used as a specific process rather than a general phrase;
- `T2 pathway`, if used as a manuscript-specific concept. If not, prefer the plainer phrase `time evolution of T2 distributions`;
- any new metric, index, regime, framework, or named relation introduced by the author.

## Terms That Usually Do Not Need Definition

| Term | Reason |
|---|---|
| `porosity` | Standard property |
| `permeability` | Standard property |
| `tortuosity` | Standard metric, unless using a custom definition |
| `Peclet number` | Standard dimensionless number, but define its equation in Methods |
| `Damkohler number` | Standard dimensionless number, but define its equation in Methods |
| `NMR` | Standard method, define once in the manuscript |
| `T2 relaxation` | Standard NMR term, define in Methods or Introduction if needed |
| `advection` | Standard transport process |
| `diffusion` | Standard transport process |
| `reaction rate` | Standard process term |
| `surface relaxation` | Standard NMR process |
| `CPMG sequence` | Standard NMR measurement sequence |

Do not add basic definitions for standard terms if doing so makes the sentence heavier.

## AI-Like Abstract Terms To Remove Or Rewrite

| Avoid | Safer action |
|---|---|
| `signal-structure paradigm` | State the relation between signal and structure directly |
| `connectivity-breakthrough nexus` | Use `the relation between connectivity and breakthrough` |
| `mechanism-diagnostic bridge` | Use `a diagnostic link to the mechanism` |
| `pore-coupling-informed interpretation` | Use `interpretation based on pore coupling` |
| `process-response signature` | Define the response or use a plain phrase |
| `multi-scale framework` | Keep only if scales, inputs, and outputs are specified |

## Definition Patterns

Use concise definitions:

1. `X refers to ...`
2. `We define X as ...`
3. `Here, X denotes ...`
4. `X is used here to describe ...`
5. `X measures ...`
6. `X increases when ...`
7. `X decreases when ...`

Avoid long definitions unless necessary. Avoid defining a term with another unclear term.

## Decision Tree

When encountering a fancy or abstract term:

1. Is this a standard technical term in the field?
   - If yes, keep it.
   - If no, continue.
2. Is it central to the sentence or manuscript argument?
   - If yes, define it briefly.
   - If no, replace it with a simpler phrase.
3. Is it newly introduced during polishing?
   - If yes, remove it unless the user explicitly requested it.
4. Can the sentence be clearer without the term?
   - If yes, use the plain phrase.
   - If no, keep the term and define it.
5. Does the definition require scientific interpretation not present in the text?
   - If yes, mark `author-confirm`.

## Examples

```text
Original:
This framework captures dynamic pore coupling.

Problem:
"Dynamic pore coupling" may be unclear if introduced without explanation.

Better:
This framework captures dynamic pore coupling, defined here as the evolving exchange between matrix pores and dissolution-induced vugs.

Meaning check:
Use this definition only if the source text supports it; otherwise mark author-confirm.
```

```text
Original:
The signal-structure relationship controls breakthrough.

Problem:
"Signal-structure relationship" is abstract and may sound AI-generated; "controls" may be too strong.

Better:
The relation between T2 evolution and pore-structure change helps explain breakthrough timing.
```
