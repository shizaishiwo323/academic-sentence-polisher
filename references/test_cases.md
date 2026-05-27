# Test Cases

Use these cases to test whether the skill performs sentence-level polishing without changing scientific meaning or evidence strength.

## TC-01: Plain syntax

Input:
Mineral dissolution widely occurs in natural and engineering processes.

Expected behavior:
Improve word order only. Do not add mechanisms, pore-network language, or manuscript storyline.

Acceptable revision:
Mineral dissolution occurs widely in natural and engineered systems.

## TC-02: Overclaim

Input:
These results prove that NMR T2 evolution robustly diagnoses dissolution mechanisms in porous media.

Expected behavior:
Downgrade `prove` and `robustly diagnoses`; preserve NMR T2 and dissolution context.

## TC-03: Invented compound

Input:
This structure-signal framework reveals a connectivity-breakthrough nexus during dissolution.

Expected behavior:
Rewrite invented compounds as plain relations. Do not create a new named framework.

## TC-04: Undefined term

Input:
The pore-coupling index increases during the intermediate stage.

Expected behavior:
If the definition is available, define `pore-coupling index`; otherwise mark `author-confirm`.

## TC-05: Decorative vocabulary

Input:
The model elucidates the intricate mechanisms that facilitate channel development.

Expected behavior:
Replace decorative verbs with direct verbs only if meaning is preserved.

## TC-06: Scope preservation

Input:
In the simulations, permeability increases under high injection rates, suggesting a transition toward channeling.

Expected behavior:
Preserve `In the simulations` and `suggesting`; do not turn the statement into a general field-scale claim.

## TC-07: Protected content

Input:
At 25% dissolution, the vug contribution accounts for 73.2% and increases to 90.5% at 50% dissolution (Figure 2h).

Expected behavior:
Preserve all values, percentages, and figure reference.

## TC-08: Heavy nominalization

Input:
The implementation of segmentation was conducted to enable the calculation of the flow focusing index.

Expected behavior:
Convert nominalizations to direct method verbs.

Acceptable revision:
We segment the medium to calculate the flow focusing index.

## TC-09: Mechanism addition risk

Input:
The T2 peak shifts to longer relaxation times.

Expected behavior:
Do not add a mechanism such as pore enlargement unless the source text already states it.

## TC-10: Comparison baseline

Input:
Compared with the low-Da case, the high-Da case shows stronger inlet-localized dissolution.

Expected behavior:
Preserve both compared cases and the direction of contrast.

## TC-11: Dash and character compatibility

Input:
Matrix–vug connectivity increases across the Péclet–Damköhler parameter space.

Expected behavior:
Treat `matrix–vug connectivity` and `Péclet–Damköhler` as protected technical expressions. Do not rewrite them only because they use Unicode characters.

## TC-12: Do not over-downgrade

Input:
Figure 3 demonstrates that the simulated T2 peak shifts to longer relaxation times under the tested conditions.

Expected behavior:
Do not automatically downgrade `demonstrates` if the figure directly supports the observation. Preserve `under the tested conditions`.

## TC-13: Do not create dash-based AI terms

Input:
The interpretation uses pore structure and flow response to explain the change in T2 signals.

Expected behavior:
Do not polish the sentence into a new expression such as `pore-structure-aware interpretation`, `flow-response-informed interpretation`, or `structure-signal framework`. Use ordinary syntax unless the compact dash term is a standard or manuscript-defined technical term.

Acceptable revision:
The interpretation uses pore structure and flow response to explain changes in T2 signals.
