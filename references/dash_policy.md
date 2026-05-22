# Dash and Compound-Term Policy

This file tells the skill how to handle hyphenated, en-dash, and compound technical terms. The goal is not to remove all dashes. The goal is to keep established academic terms and remove AI-like invented compounds.

## Core Rule

Keep a dash or compound modifier when it is:

- a field-standard term;
- a unit, time range, or numeric range;
- a necessary compound adjective before a noun;
- clearer than a longer phrase;
- already defined or easily interpretable in context.

Rewrite it when it is:

- an invented label for a simple relation;
- a chain of three or more nouns that hides meaning;
- a decorative `X-Y framework`, `X-Y bridge`, or `X-Y nexus`;
- used to make the sentence sound more sophisticated rather than clearer.

## Keep: Established or Useful Technical Compounds

These forms are generally acceptable in porous media, geophysics, NMR, and reactive-transport writing:

```text
pore-scale
pore-network
pore-size distribution
pore-throat
pore-water
field-scale
time-dependent
saturation-dependent
surface-related
surface-limited
reaction-limited
transport-limited
advection-dominated
diffusion-controlled
solid-liquid interface
solid-fluid interface
fluid-air interface
fluid-rock interaction
electrical tortuosity-based permeability model
flow focusing profile
off-diagonal peak
late-time tailing
power-law tailing
non-Fickian transport
T2-distribution
T2-store-T2 map
T1-T2 map
```

Keep numeric and measurement ranges:

```text
0-4 h
1 mHz to 1 GHz
10-15 sentences
solid, fluid, and air phases
```

## Caution: Useful but Easy to Overload

These can be retained if the sentence defines them or if they are necessary for precision:

```text
electrochemical polarization-induced conductivity variations
saturation-dependent pore coupling strength
electrical tortuosity-based k prediction
transport-limited precipitation/dissolution
reaction-limited precipitation/dissolution
surface-relaxation-dominated response
diffusion-controlled transport
pore-scale physicochemical dynamics
```

When a cautious compound becomes too long, prefer a plain phrase:

| Dense compound | Safer rewrite |
|---|---|
| `electrochemical polarization-induced conductivity variations` | `conductivity variations induced by electrochemical polarization` |
| `saturation-dependent pore coupling strength` | `pore coupling strength as saturation changes` |
| `electrical tortuosity-based k prediction` | `k prediction based on electrical tortuosity` |
| `surface-relaxation-dominated response` | `a response dominated by surface relaxation` |

## Usually Rewrite: AI-Like Invented Compounds

These forms are risky unless the user has explicitly defined them as manuscript terms:

```text
structure-signal framework
connectivity-breakthrough nexus
mechanism-diagnostic bridge
pore-coupling-informed interpretation
dissolution-NMR-hydraulic framework
signal-mechanism-breakthrough relationship
matrix-vug-flow-path optimization process
process-response-signature paradigm
multi-scale insight-generating framework
physics-aware interpretation pipeline
```

Preferred rewrites:

| AI-like compound | Safer rewrite |
|---|---|
| `structure-signal framework` | `a framework that links pore structure to the measured signal` |
| `connectivity-breakthrough nexus` | `the relation between connectivity and breakthrough behavior` |
| `mechanism-diagnostic bridge` | `a diagnostic link to the mechanism` |
| `pore-coupling-informed interpretation` | `interpretation based on pore coupling` |
| `signal-mechanism-breakthrough relationship` | `the relation among signal change, mechanism, and breakthrough` |

## Dash Type Guidance

Use the project's plain-text style unless the manuscript already uses typographic dashes:

- Use hyphen `-` for compound adjectives: `pore-scale model`.
- Use en dash only if the journal style or manuscript already uses it for ranges or paired relations.
- Avoid em dash sentence interruptions in formal paper prose; use commas, parentheses, or a separate sentence.

## Polishing Instructions

1. Identify whether the dashed expression is a standard term, a necessary compound modifier, or a new label.
2. If it is standard, preserve it.
3. If it is long but meaningful, rewrite it as a plain phrase.
4. If it is a decorative invented label, remove the label and state the relation directly.
5. Do not invent new dashed terms during polishing.
6. Preserve established terms in equations, figure labels, section names, and citations.

## Examples

Good:

```text
The pore-network model represents the medium as interconnected cylindrical capillaries.
The transport-limited case mainly alters pore throats where fluid velocity is high.
The T2-store-T2 map uses off-diagonal peaks to track inter-pore exchange.
```

Prefer rewriting:

```text
Original: This structure-signal framework reveals the dissolution-NMR-hydraulic relationship.
Better: This framework links pore-structure changes to NMR and hydraulic responses.
```
