# Source Sentence Corpus

This file stores selected sentence-level examples from seven high-quality papers. The goal is to extract reusable writing rules for academic sentence polishing, not to copy source sentences or imitate the scientific content.

## Use Status Legend

| Status | Meaning |
|---|---|
| `positive` | Good source for a preferred expression pattern |
| `caution` | Useful local feature, but not safe to imitate directly because of strong wording, long syntax, or other risks |
| `negative` | Counterexample or test-only sentence |

If this corpus is prepared for a public repository, replace full source sentences with short paraphrases or source pointers while keeping the extracted rules.

## Corpus Overview

| Paper ID | Paper short name | Journal | Field | Why selected |
|---|---|---|---|---|
| P01 | Archie porosity exponent | GRL, 2018 | geophysics / porous media | Clear term definition, compact result reporting, cautious mechanism language |
| P02 | Spatial flow focusing profile | GRL, 2024 | reactive transport | Strong examples of metric definition, regime comparison, and method limitation |
| P03 | Anomalous transport in dissolving media | GRL, 2025 | reactive transport | Good result-to-mechanism transitions and bounded phase-diagram claims |
| P04 | Pore coupling in unsaturated media | GRL, 2026 | NMR / porous media | Good handling of technical terms, figure interpretation, and uncertainty boundaries |
| P05 | Broadband electrical properties framework | JGR Solid Earth, 2020 | petrophysics | Useful terminology discipline and framework/method sentences |
| P06 | Permeability prediction during reactions | WRR, 2019 | petrophysics / reactive transport | Strong comparison between reaction-limited and transport-limited cases |
| P07 | Pore structure and NMR relaxation | WRR, 2025 | NMR / vadose zone | Good examples of definition, assumption, result contrast, and interpretation control |

---

# P01: Archie Porosity Exponent

## Paper-Level Notes

**Strength of writing:** The paper defines central quantities before using them, reports trends with clear directions, and uses `suggest`/`might` for broader relations.  
**Useful for this skill because:** It shows how to explain mechanisms without turning local numerical results into universal claims too quickly.

## P01-S01

**Section:** Introduction  
**Function tag:** DEF  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> This relation, known as Archie's law, relates a material's resistivity at saturation to its porosity and the pore fluid resistivity with a power function.

**Local context:** Introduces the named relation before discussing its exponent.  
**Why it works:** The definition is short and immediately tied to the variables the reader needs.  
**Transferable rule:** Define a named law, metric, or framework at first use with a plain clause.  
**Reusable pattern:** `This relation, known as X, relates A to B through C.`  
**Risk when misused:** The pattern becomes heavy if every common term is over-defined.  
**Skill-ready instruction:** Define only central or potentially unfamiliar terms, and keep the definition local to the sentence.

## P01-S02

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> At present, a physical understanding of the exponent is still limited mainly due to the lack of the detailed information on the complex geometry of the pore space.

**Local context:** States why the existing empirical relation still needs explanation.  
**Why it works:** The gap is a specific missing basis, not a vague claim that little is known.  
**Transferable rule:** Connect a gap to a concrete missing mechanism, measurement, scale, or geometry.  
**Reusable pattern:** `A physical understanding of X remains limited because Y is not well constrained.`  
**Risk when misused:** `limited` can become too broad if the missing information is not named.  
**Skill-ready instruction:** When polishing gap sentences, replace broad unknowns with the specific missing relation or evidence.

## P01-S03

**Section:** Introduction  
**Function tag:** AIM  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> Here we use computational simulations to obtain the microscale geometrical characteristics of synthetic granular materials and to analyze the dominant parameter(s) impacting the exponent.

**Local context:** States what the study does after identifying the gap.  
**Why it works:** It names the method, object, and target parameter without promotional language.  
**Transferable rule:** A study-aim sentence should say `we use X to do Y` before claiming significance.  
**Reusable pattern:** `Here, we use X to obtain Y and analyze Z.`  
**Risk when misused:** Adding `novel`, `powerful`, or `unprecedented` would make it promotional.  
**Skill-ready instruction:** Keep aim sentences procedural and concrete; avoid value judgments unless the source text already supports them.

## P01-S04

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> The samples presented here consist of spherical and oblate particles, and the solid-phase concentration varies broadly, from dilute (i.e., a limited particle-particle interaction; ϕ > ~65%) to dense states (i.e., ϕ = ~30%).

**Local context:** Describes the sample design and the range of states.  
**Why it works:** The parenthetical definitions make `dilute` and `dense` operational.  
**Transferable rule:** When using qualitative state labels, attach a measurable criterion.  
**Reusable pattern:** `X varies from A (defined by criterion 1) to B (defined by criterion 2).`  
**Risk when misused:** Too many parentheticals can make a sentence hard to read.  
**Skill-ready instruction:** Keep operational definitions near state labels, but split the sentence if definitions accumulate.

## P01-S05

**Section:** Methods  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> In each sample, all the particles have the same shape (e = 1, 0.67, or 0.5 where e is the ratio of the semiminor to semimajor axes), and the particle size follows either a Dirac delta distribution centered at d or a uniform distribution in the range [0.5d, 1.5d].

**Local context:** Defines the shape parameter and size distribution in the sample setup.  
**Why it works:** The variable definition appears at the point where the variable is introduced.  
**Transferable rule:** Define symbols and ranges before using them in interpretation.  
**Reusable pattern:** `X has values ..., where X denotes ...; Y follows ...`  
**Risk when misused:** Combining too many definitions can overload one sentence.  
**Skill-ready instruction:** Preserve symbols and numeric ranges; simplify only the surrounding syntax.

## P01-S06

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> At dilute state, m roughly keeps constant; as ϕ decreases, m increases continuously.

**Local context:** Reports the primary trend before explaining it.  
**Why it works:** The sentence uses simple verbs and a clear contrast across conditions.  
**Transferable rule:** A result sentence can be short when the variables and direction of change are clear.  
**Reusable pattern:** `At A, X remains nearly constant; as Y changes, X increases/decreases.`  
**Risk when misused:** `continuously` should be kept only when the data show a continuous trend.  
**Skill-ready instruction:** Preserve the direction and condition of trends; remove unnecessary interpretation from first-result sentences.

## P01-S07

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> At dilute state, we found that m of multisized and monosized samples with same particle shape is almost identical, suggesting limited effects of particle size range on m.

**Local context:** Reports a comparison and gives a restrained implication.  
**Why it works:** `suggesting limited effects` avoids stronger verbs such as `proves`.  
**Transferable rule:** Use `suggesting` for an interpretation that follows directly from a comparison.  
**Reusable pattern:** `X is almost identical between A and B, suggesting limited effects of C.`  
**Risk when misused:** `suggesting` can still overreach if the comparison is indirect.  
**Skill-ready instruction:** Keep tentative verbs when the sentence moves from observation to interpretation.

## P01-S08

**Section:** Results  
**Function tag:** IMP  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> This observed dependence of particle size range on m of nondilute granular samples is consistent with some experimental data, for example, as reviewed by Friedman (2005).

**Local context:** Relates the numerical result to previous experimental observations.  
**Why it works:** `is consistent with` avoids claiming that the simulation validates all experiments.  
**Transferable rule:** Use consistency language when connecting a local result to prior work.  
**Reusable pattern:** `This observed dependence is consistent with previous observations of X.`  
**Risk when misused:** Consistency does not imply proof or complete agreement.  
**Skill-ready instruction:** Replace overstrong agreement claims with `is consistent with` when evidence is comparative.

## P01-S09

**Section:** Discussion  
**Function tag:** IMP  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> This unique trend suggests that there might be a universal correlation between the increase in m (relative to the dilute state of individual samples) and the relative volume of pore throats for granular materials.

**Local context:** Interprets a collapsed trend across samples.  
**Why it works:** The sentence combines a strong observed pattern with `might be`, keeping the generalization cautious.  
**Transferable rule:** When generalizing from a pattern, pair the claim with a modal verb and a domain boundary.  
**Reusable pattern:** `This trend suggests that there might be a relation between X and Y for Z.`  
**Risk when misused:** `unique` and `universal` are strong; retain them only if the source data justify them.  
**Skill-ready instruction:** Do not strengthen tentative cross-sample relations; keep modals and domain limits.

## P01-S10

**Section:** Conclusions  
**Function tag:** IMP  
**Score:** 8/10  
**Use status:** caution

**Source sentence:**  
> Our numerical results also suggest that for granular materials, a universal relation might exist, which links the volume fraction of pore throats to the increase in m (relative to the value at dilute state m0) regardless of the particle shape, particle size range, and porosities.

**Local context:** Summarizes the main inferred relation with conditions.  
**Why it works:** The claim is bounded by material class and by the simulation basis.  
**Transferable rule:** Conclusion sentences may generalize, but they should name the evidence source and scope.  
**Reusable pattern:** `Our results suggest that, for X, a relation might exist between A and B.`  
**Risk when misused:** Removing `numerical`, `for granular materials`, or `might` would overstate the conclusion.  
**Skill-ready instruction:** In conclusion polishing, preserve qualifiers that identify evidence type and applicability.

---

# P02: Spatial Flow Focusing Profile

## Paper-Level Notes

**Strength of writing:** The paper gives a clear metric, explains why it is needed, and uses temporal/spatial comparison to distinguish regimes.  
**Useful for this skill because:** It shows how to introduce a new term without making it sound like a decorative framework.

## P02-S01

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 8/10  
**Use status:** caution

**Source sentence:**  
> However, distinguishing between regimes often relies solely on qualitative, visual comparisons of emergent structures.

**Local context:** Identifies a limitation in current classification practice.  
**Why it works:** The gap is specific: classification relies on visual comparison.  
**Transferable rule:** A gap should name the current practice and the specific limitation.  
**Reusable pattern:** `However, distinguishing between X often relies on Y.`  
**Risk when misused:** `solely` is strong and should be kept only when the literature supports it.  
**Skill-ready instruction:** If a gap uses `solely`, check whether the original evidence justifies that exclusivity.

## P02-S02

**Section:** Introduction  
**Function tag:** AIM  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> Here, we propose a quantitative measure capable of identifying different regimes using the concept of the spatial flow focusing profile, which segments the medium into cross sections along the flow direction to calculate the flow focusing index for each section.

**Local context:** Introduces the proposed metric and defines its operation.  
**Why it works:** The new term is immediately followed by what it does.  
**Transferable rule:** When introducing a new named metric, define it by its operation, not by adjectives.  
**Reusable pattern:** `We propose X, which does Y to calculate Z.`  
**Risk when misused:** The sentence is long; in polishing, split it if the user sentence has additional clauses.  
**Skill-ready instruction:** Define new metrics through procedure and output, not through vague value claims.

## P02-S03

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> To demonstrate the performance of the proposed flow focusing profile and to quantitatively describe various dissolution regimes, we use the capillary pore network model of a dissolving porous medium.

**Local context:** Links the method choice to the purpose of evaluation.  
**Why it works:** It states the reason for using the model without overexplaining.  
**Transferable rule:** Method sentences can begin with purpose when the model choice needs context.  
**Reusable pattern:** `To evaluate X and describe Y, we use Z.`  
**Risk when misused:** Do not add purpose clauses that are not in the original method.  
**Skill-ready instruction:** Preserve the method-purpose relation and avoid adding new capabilities.

## P02-S04

**Section:** Methods  
**Function tag:** DEF  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> To compare the evolution for different dissolution regimes, we measure time in the simulation in terms of the total dissolved volume in the system, with T = ΔVtot/V0, where V0 is the initial total pore volume and ΔVtot is the dissolved volume.

**Local context:** Defines the normalized time variable used for regime comparison.  
**Why it works:** The purpose, metric, equation, and variable definitions are connected.  
**Transferable rule:** When a normalized variable is introduced, explain why it is used and define its components.  
**Reusable pattern:** `To compare X, we measure Y as Z, where A is ... and B is ...`  
**Risk when misused:** Removing the `where` clause can make the equation opaque.  
**Skill-ready instruction:** Preserve variable definitions and do not simplify away equation context.

## P02-S05

**Section:** Methods  
**Function tag:** MET  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> We segment the medium into cross sections along the main flow direction, x, and in each of them we calculate the flow focusing index, f50%.

**Local context:** Describes the core calculation step.  
**Why it works:** The action verbs `segment` and `calculate` make the method easy to follow.  
**Transferable rule:** Method sentences should foreground the action sequence.  
**Reusable pattern:** `We segment X along Y and calculate Z in each segment.`  
**Risk when misused:** Avoid replacing concrete verbs with abstract nouns such as `implementation of segmentation`.  
**Skill-ready instruction:** Convert heavy method nominalizations into direct verbs when meaning is unchanged.

## P02-S06

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> As the wormhole begins to develop from the inlet, the profile in that area rapidly increases, approaching values close to one.

**Local context:** Describes how the metric changes during wormhole growth.  
**Why it works:** It connects spatial location, temporal evolution, and quantitative direction.  
**Transferable rule:** A result sentence should locate where a change occurs before interpreting it.  
**Reusable pattern:** `As X develops from Y, Z increases in that area, approaching A.`  
**Risk when misused:** `rapidly` should be kept only when time evolution supports it.  
**Skill-ready instruction:** Keep spatial and temporal qualifiers attached to the trend they modify.

## P02-S07

**Section:** Results  
**Function tag:** CON  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> Unlike the wormholing regime, where the pathway grows from the inlet to the outlet, channeling involves almost uniform enlargement.

**Local context:** Contrasts two dissolution regimes.  
**Why it works:** The contrast is simple and mechanistic, not rhetorical.  
**Transferable rule:** Use `unlike` to contrast one concrete behavior with another.  
**Reusable pattern:** `Unlike A, where X occurs, B involves Y.`  
**Risk when misused:** The contrast becomes unfair if A and B are not comparable.  
**Skill-ready instruction:** Use comparison only between matched objects, regimes, or mechanisms.

## P02-S08

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> For small Damköhler numbers, the dissolution occurs in the uniform regime, where the reactant penetration length is comparable to the size of the system.

**Local context:** Connects a parameter range to a regime and a physical reason.  
**Why it works:** The `where` clause gives a criterion rather than an abstract label.  
**Transferable rule:** Explain regime labels through the condition that defines them.  
**Reusable pattern:** `For small/large X, Y occurs in regime Z, where criterion C holds.`  
**Risk when misused:** Do not add a defining criterion unless it is already supported.  
**Skill-ready instruction:** Preserve parameter-regime-condition chains in result sentences.

## P02-S09

**Section:** Results  
**Function tag:** CON  
**Score:** 8/10  
**Use status:** caution

**Source sentence:**  
> Although the boundaries between the regimes are subtle, it is evident that at low network heterogeneity, the dissolution exhibits features of wormholing, characterized by a progressing front in the flow focusing profile and asymmetric flow paths forming from the inlet.

**Local context:** Reports a classification where the boundary is not sharp.  
**Why it works:** The concession prevents overconfident regime assignment.  
**Transferable rule:** When classification is uncertain or gradual, state that boundary before naming the pattern.  
**Reusable pattern:** `Although the boundary is subtle, X exhibits features of Y, characterized by Z.`  
**Risk when misused:** `it is evident` may be too strong without clear visual or quantitative evidence.  
**Skill-ready instruction:** Keep uncertainty markers in classification sentences; consider softening `evident` to `the results indicate` if needed.

## P02-S10

**Section:** Discussion  
**Function tag:** ASS  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> However, the flow focusing profile may be less suitable for experiments and field applications where flow distribution data might not be readily available.

**Local context:** States a limitation of the proposed metric.  
**Why it works:** The limitation is practical and specific.  
**Transferable rule:** Limitation sentences should name the condition under which the method is less suitable.  
**Reusable pattern:** `X may be less suitable for Y where Z is not available.`  
**Risk when misused:** Avoid turning a limitation into a generic weakness of the whole study.  
**Skill-ready instruction:** Keep limitation language scoped to the affected application or data requirement.

---

# P03: Anomalous Transport in Dissolving Porous Media

## Paper-Level Notes

**Strength of writing:** The paper links transport behavior to dissolution regime with clear before/after contrasts.  
**Useful for this skill because:** It shows how to interpret complex mechanisms through stepwise, evidence-tied sentences.

## P03-S01

**Section:** Introduction  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> This process is known as Fickian transport and can be well described by the classical advection-dispersion equation.

**Local context:** Names a transport regime after explaining the behavior.  
**Why it works:** The definition links the term to a modeling description.  
**Transferable rule:** Introduce a technical label after the behavior it names.  
**Reusable pattern:** `This process is known as X and can be described by Y.`  
**Risk when misused:** `well described` should not be used when the fit is uncertain.  
**Skill-ready instruction:** When defining a regime, pair the label with the model or behavior that identifies it.

## P03-S02

**Section:** Introduction  
**Function tag:** CON  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> However, in heterogeneous media, variations in permeability induce velocity heterogeneity, leading to preferential flow pathways and stagnant zones.

**Local context:** Contrasts homogeneous and heterogeneous transport settings.  
**Why it works:** The cause-effect chain is short and physically grounded.  
**Transferable rule:** Keep mechanism chains to one or two linked steps unless the original sentence demands more.  
**Reusable pattern:** `In X media, variations in A induce B, leading to C.`  
**Risk when misused:** `leading to` can imply causality; keep it only when the causal relation is established.  
**Skill-ready instruction:** Preserve causal links only when they already exist in the source sentence.

## P03-S03

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> However, most studies on anomalous transport have primarily focused on cases where the structural heterogeneity of the rock remains constant.

**Local context:** Identifies the missing dynamic aspect in previous work.  
**Why it works:** The gap is restricted to a specific assumption, not all previous research.  
**Transferable rule:** State literature gaps as scope limitations rather than broad failures.  
**Reusable pattern:** `Most studies on X have focused on cases where Y remains constant.`  
**Risk when misused:** `most` requires literature support.  
**Skill-ready instruction:** Avoid `failed to`; use scope-based gap language when polishing literature gaps.

## P03-S04

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> The 2D pore network represents the porous media as a series of interconnected cylindrical capillaries with a constant length l0.

**Local context:** Defines the model representation.  
**Why it works:** It states what the model is, not what it is hoped to achieve.  
**Transferable rule:** Model-description sentences should start with representation or operation.  
**Reusable pattern:** `The X model represents Y as Z.`  
**Risk when misused:** Do not add validation or performance claims to a representation sentence.  
**Skill-ready instruction:** Keep model sentences descriptive unless the original includes evaluation.

## P03-S05

**Section:** Methods  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> The points where pores intersect are denoted as nodes, which are assumed to be volumeless and therefore non-reactive.

**Local context:** Defines a network element and a modeling assumption.  
**Why it works:** The definition and assumption are compactly connected.  
**Transferable rule:** Define model elements together with their key simplifying assumption.  
**Reusable pattern:** `The points where X occurs are denoted as Y, which are assumed to be Z.`  
**Risk when misused:** Do not hide important assumptions inside a long relative clause.  
**Skill-ready instruction:** If a definition contains a key assumption, keep it explicit.

## P03-S06

**Section:** Methods  
**Function tag:** ASS  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> However, for the range of flow and reaction rates considered in this study, the entrance length is small relative to the pore length, allowing us to neglect entrance effects.

**Local context:** Justifies a simplification with a condition.  
**Why it works:** The assumption is bounded by the parameter range of the study.  
**Transferable rule:** A good assumption sentence states the condition that makes the simplification acceptable.  
**Reusable pattern:** `For the range of X considered here, Y is small relative to Z, allowing us to neglect A.`  
**Risk when misused:** Removing `considered in this study` would overgeneralize the assumption.  
**Skill-ready instruction:** Preserve scope phrases in assumption sentences.

## P03-S07

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> As seen in Figure 2a, the BTC changes from a distribution with limited spreading to a distribution featuring early arrival and late-time tailing.

**Local context:** Reports the main before/after change in a figure.  
**Why it works:** The sentence names both the initial and final states.  
**Transferable rule:** Figure-result sentences should describe the transition, not just point to the panel.  
**Reusable pattern:** `As seen in Figure X, Y changes from A to B.`  
**Risk when misused:** Avoid adding an interpretation before the observed change is stated.  
**Skill-ready instruction:** Preserve figure labels and report the visual or quantitative contrast first.

## P03-S08

**Section:** Results  
**Function tag:** IMP  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> The wormholes form due to reactive-infiltration instability, based on a positive feedback loop between flow, transport, and dissolution.

**Local context:** Explains the mechanism behind a result.  
**Why it works:** It names the mechanism and the coupled processes without decorative wording.  
**Transferable rule:** Mechanism sentences should identify the process and the interacting components.  
**Reusable pattern:** `X forms due to Y, based on feedback between A, B, and C.`  
**Risk when misused:** Do not introduce a mechanism that is absent from the original sentence.  
**Skill-ready instruction:** Only clarify mechanisms that the source text already states.

## P03-S09

**Section:** Results  
**Function tag:** RES  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> Figure 5 shows that, regardless of the initial heterogeneity, wormholing leads to non-Fickian transport, while uniform dissolution results in Fickian transport.

**Local context:** Summarizes a phase-diagram result.  
**Why it works:** The contrast is direct and anchored to the figure.  
**Transferable rule:** Use `while` to compare matched outcomes under different regimes.  
**Reusable pattern:** `Figure X shows that A leads to B, while C results in D.`  
**Risk when misused:** `regardless of` is strong and should be retained only when all tested cases support it.  
**Skill-ready instruction:** Preserve qualifiers such as `tested`, `simulated`, or `shown` when broad contrasts are stated.

## P03-S10

**Section:** Discussion  
**Function tag:** ASS  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> Although this study is based on a 2D pore network, both wormholing and uniform dissolution have commonly observed in 3D systems.

**Local context:** Places a model limitation beside external support.  
**Why it works:** It acknowledges dimensionality without discarding relevance.  
**Transferable rule:** Limitation sentences can pair a constraint with a reason the finding remains relevant.  
**Reusable pattern:** `Although this study is based on X, Y has also been observed in Z.`  
**Risk when misused:** The second clause should not erase the limitation.  
**Skill-ready instruction:** Keep limitations visible; do not polish them into reassurance or overclaim.

---

# P04: Pore Coupling in Unsaturated Porous Media

## Paper-Level Notes

**Strength of writing:** The paper defines pore coupling and repeatedly ties NMR signatures to specific pore-network changes.  
**Useful for this skill because:** It shows how to handle technical metrics and figure interpretation without losing readability.

## P04-S01

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> Although NMR can provide detailed insights into pore coupling within saturated soils and rocks, its application in unsaturated subsurface materials remains challenging, even at the laboratory scale.

**Local context:** Contrasts established saturated applications with unsaturated difficulty.  
**Why it works:** The concession acknowledges capability before naming the hard case.  
**Transferable rule:** Gap sentences can use `although` to avoid dismissing prior methods.  
**Reusable pattern:** `Although X can provide insight into A, its application to B remains challenging.`  
**Risk when misused:** `challenging` should be followed nearby by the reason for difficulty.  
**Skill-ready instruction:** When polishing gap sentences, preserve acknowledgments of what existing methods already do.

## P04-S02

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> In particular, how the degree of pore coupling changes with decreasing saturation, and how this change can be observed and quantified, remains unresolved.

**Local context:** Narrows the gap to two unresolved questions.  
**Why it works:** It specifies the variable, trend, observation problem, and quantification problem.  
**Transferable rule:** A strong gap narrows from the broad problem to the exact unresolved relation.  
**Reusable pattern:** `How X changes with Y, and how this change can be observed and quantified, remains unresolved.`  
**Risk when misused:** The structure is too heavy if the sentence does not need two subquestions.  
**Skill-ready instruction:** Use `in particular` to narrow a gap, not to add a new unrelated topic.

## P04-S03

**Section:** Introduction  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** caution

**Source sentence:**  
> The 2D T2-store-T2 map captures this process through asymmetric off-diagonal peaks, which indicate magnetized proton exchange between pores and reflect both proton chemical shifts and inter-pore molecular exchange during mixing periods.

**Local context:** Defines how a technical map represents pore exchange.  
**Why it works:** It ties a visual feature to the physical process it indicates.  
**Transferable rule:** Define technical diagnostics by linking observed features to the underlying process.  
**Reusable pattern:** `X captures Y through feature Z, which indicates A and reflects B.`  
**Risk when misused:** The sentence can become too dense if more than two physical meanings are added.  
**Skill-ready instruction:** Keep diagnostic definitions feature-based and avoid extra mechanistic claims.

## P04-S04

**Section:** Methods  
**Function tag:** DEF  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> Here, Sw = Vw / Vpore, where Vw is water volume and Vpore is total pore volume.

**Local context:** Defines saturation in the experimental setup.  
**Why it works:** It is precise and uncluttered.  
**Transferable rule:** Formula definitions should be direct and minimal.  
**Reusable pattern:** `Here, X = A/B, where A is ... and B is ...`  
**Risk when misused:** Do not rewrite equations for style.  
**Skill-ready instruction:** Preserve equations exactly and polish only the explanatory text around them.

## P04-S05

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> Sealed samples were scanned at 3 μm voxel resolution, and three-phase segmentation (solid, fluid, and air) was performed on reconstructed 2D grayscale cross-sections along the vertical height.

**Local context:** Summarizes imaging and segmentation.  
**Why it works:** It states resolution, segmentation classes, and spatial basis.  
**Transferable rule:** Method sentences should include key parameters that make the procedure reproducible.  
**Reusable pattern:** `Samples were scanned at X resolution, and Y segmentation was performed on Z.`  
**Risk when misused:** Do not remove numeric details for concision.  
**Skill-ready instruction:** Preserve reproducibility details such as resolution, classes, and sample orientation.

## P04-S06

**Section:** Results  
**Function tag:** RES  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> With decreasing saturation, the amplitude of the longest-relaxation time peak decreases more significantly than that of the shorter-relaxation components, reflecting the preferential moisture reduction within the largest pores.

**Local context:** Connects an NMR peak change to water redistribution.  
**Why it works:** The observation comes before the interpretation.  
**Transferable rule:** Put the measured signal change first, then the physical interpretation.  
**Reusable pattern:** `With decreasing X, Y decreases more than Z, reflecting A.`  
**Risk when misused:** `reflecting` should be softened if the causal link is indirect.  
**Skill-ready instruction:** Preserve observation-then-interpretation order in result sentences.

## P04-S07

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> As saturation decreases, the peaks progressively separate, producing a clearer distinction between the long- and short-relaxation components at Sw = 85% and 70%.

**Local context:** Reports a saturation-dependent spectral change.  
**Why it works:** It gives trend, outcome, and conditions.  
**Transferable rule:** Include the condition values that define where a pattern is observed.  
**Reusable pattern:** `As X decreases, Y progressively separates, producing Z at A and B.`  
**Risk when misused:** `progressively` should match the sequence of observations.  
**Skill-ready instruction:** Do not drop condition values when they bound a result.

## P04-S08

**Section:** Results  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> Thus, in Figure 2e, diagonal peaks P11, 22 respectively represent magnetized protons remaining within large and small pore environments, while off-diagonal peaks P12, 21 correspond to protons diffusing from large to small pores and small to large pores, respectively.

**Local context:** Defines figure symbols for interpreting a 2D map.  
**Why it works:** The sentence assigns each symbol to a physical meaning.  
**Transferable rule:** Symbol-heavy figure interpretation should map symbols to meanings explicitly.  
**Reusable pattern:** `In Figure X, A represents ..., while B corresponds to ...`  
**Risk when misused:** Too many symbol definitions in one sentence may need a split.  
**Skill-ready instruction:** Preserve symbol-meaning mappings; split long definitions without changing labels.

## P04-S09

**Section:** Discussion  
**Function tag:** IMP  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> This quantitative trend reflects the reduced proportion of inter-pore magnetized proton exchange and demonstrates that T2-store-T2 maps provide insight into quantitatively tracking the weakening pore coupling in multi-pore systems as saturation decreases.

**Local context:** Interprets a trend in off-diagonal peak amplitude.  
**Why it works:** It ties the metric to the physical process and tracking purpose.  
**Transferable rule:** When interpreting a metric, state both what it reflects and what it can track.  
**Reusable pattern:** `This trend reflects X and shows that Y can track Z under condition A.`  
**Risk when misused:** `demonstrates` may be too strong if the evidence is preliminary.  
**Skill-ready instruction:** Consider downgrading `demonstrates` to `indicates` when the original evidence is limited.

## P04-S10

**Section:** Discussion  
**Function tag:** ASS  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> While our study focuses on geometric controls, ρs remains an important external factor that can influence NMR sensitivity to pore coupling.

**Local context:** States a factor outside the main focus.  
**Why it works:** The limitation is concise and does not derail the discussion.  
**Transferable rule:** Acknowledge excluded factors by naming the study focus and the remaining influence.  
**Reusable pattern:** `While this study focuses on X, Y remains an important factor that can influence Z.`  
**Risk when misused:** Do not turn an external factor into a new result.  
**Skill-ready instruction:** Keep out-of-scope factors as limitations or context, not as added conclusions.

---

# P05: Broadband Electrical Properties Framework

## Paper-Level Notes

**Strength of writing:** The paper is disciplined about terminology and distinguishes measured/effective quantities from phase-specific properties.  
**Useful for this skill because:** It offers strong examples for defining terms, scope, and model components.

## P05-S01

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> However, it is still difficult to incorporate surface-related electrochemical processes in a pore-scale simulation.

**Local context:** States the modeling difficulty motivating the work.  
**Why it works:** The gap is narrow and method-specific.  
**Transferable rule:** Technical gaps should identify the exact process that is difficult to include.  
**Reusable pattern:** `However, it remains difficult to incorporate X in Y.`  
**Risk when misused:** `difficult` can be vague if the process is not specified.  
**Skill-ready instruction:** Replace broad challenge language with the specific modeling or measurement difficulty.

## P05-S02

**Section:** Introduction  
**Function tag:** AIM  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> In this study, we develop a general framework to consider these electrochemical processes in pore-scale simulations, which enable the calculation of broadband effective electrical conductivity and permittivity of porous geological media.

**Local context:** States the framework objective and calculated properties.  
**Why it works:** It explains what the framework includes and what it calculates.  
**Transferable rule:** Framework sentences should specify input processes and output quantities.  
**Reusable pattern:** `We develop a framework to consider X in Y, enabling calculation of Z.`  
**Risk when misused:** `general framework` can sound inflated unless the scope is concrete.  
**Skill-ready instruction:** Keep `framework` only when the sentence specifies the processes and outputs it connects.

## P05-S03

**Section:** General Definition and Terminology  
**Function tag:** DEF  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> In this paper, we use the electrical conductivity and electrical permittivity to describe the electrical properties of a material at a given frequency.

**Local context:** Establishes terminology before detailed equations.  
**Why it works:** It tells readers how the paper will use the terms.  
**Transferable rule:** If a term may vary across fields, define its use in the paper.  
**Reusable pattern:** `In this paper, we use X and Y to describe Z.`  
**Risk when misused:** Do not define common terms unless local usage differs or matters.  
**Skill-ready instruction:** Add definition only for central terms whose meaning affects interpretation.

## P05-S04

**Section:** General Definition and Terminology  
**Function tag:** DEF  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> To distinguish the average properties from the property of individual phases, in this paper, we use the effective electrical conductivity and effective electrical permittivity to indicate the average (or measured) properties of geological materials.

**Local context:** Distinguishes effective properties from phase properties.  
**Why it works:** The definition is motivated by a possible ambiguity.  
**Transferable rule:** Define terms when they prevent confusion between scales or phases.  
**Reusable pattern:** `To distinguish A from B, we use X to indicate Y.`  
**Risk when misused:** Avoid adding unnecessary `effective` labels without a scale distinction.  
**Skill-ready instruction:** Preserve scale distinctions such as average, phase-specific, measured, and effective.

## P05-S05

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> In this study, we use the pore network extraction algorithms to determine these properties.

**Local context:** Describes how pore-network properties are obtained.  
**Why it works:** It is simple and procedural.  
**Transferable rule:** Use direct verbs for method steps.  
**Reusable pattern:** `We use X to determine Y.`  
**Risk when misused:** Too short a method sentence may need a preceding sentence defining `these properties`.  
**Skill-ready instruction:** Keep method verbs direct; ensure pronouns refer to nearby nouns.

## P05-S06

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> The proposed framework is outlined in Figure 2, and the details are discussed as follows.

**Local context:** Transitions from overview to detailed method steps.  
**Why it works:** It is functional and unornamented.  
**Transferable rule:** Method transition sentences should guide structure without grand claims.  
**Reusable pattern:** `The framework is outlined in Figure X, and the details are discussed below.`  
**Risk when misused:** Avoid adding `comprehensive`, `innovative`, or `powerful`.  
**Skill-ready instruction:** Keep figure roadmap sentences plain.

## P05-S07

**Section:** Methods  
**Function tag:** ASS  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> Note that this type of model is only valid for large grains with a ≫ λ, where λ is the Debye length.

**Local context:** States a validity condition for a model.  
**Why it works:** It gives the mathematical condition and defines the symbol.  
**Transferable rule:** Validity limits should be expressed as concrete parameter conditions.  
**Reusable pattern:** `This model is only valid for X with condition C, where Y is ...`  
**Risk when misused:** Removing `only` would weaken an important limitation.  
**Skill-ready instruction:** Preserve validity constraints and variable definitions.

## P05-S08

**Section:** Results  
**Function tag:** RES  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> The simulated effective permittivity due to the interfacial polarization is similar to the experiment results, and both curves exhibit a high permittivity plateau at low frequencies and a low effective permittivity at high frequencies.

**Local context:** Compares simulated and measured spectra.  
**Why it works:** It names the agreement and the features being compared.  
**Transferable rule:** Comparison sentences should state the comparable feature, not just that results agree.  
**Reusable pattern:** `The simulated X is similar to Y, and both curves exhibit A at condition 1 and B at condition 2.`  
**Risk when misused:** `similar` should not be upgraded to `match` unless quantitative agreement is shown.  
**Skill-ready instruction:** Keep comparison terms proportional to the evidence.

## P05-S09

**Section:** Results  
**Function tag:** IMP  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> This discrepancy might be due to fact that the resolution of the digital microstructural μCT images did not capture the nanometer-scale heterogeneities at the solid-liquid interface.

**Local context:** Explains a mismatch between simulation and experiment.  
**Why it works:** It uses `might be due to` for a plausible explanation.  
**Transferable rule:** Use modal explanation when interpreting discrepancies.  
**Reusable pattern:** `This discrepancy might be due to X.`  
**Risk when misused:** Do not turn plausible causes into definitive causes.  
**Skill-ready instruction:** Preserve `might`, `may`, or `could` when explaining discrepancies.

## P05-S10

**Section:** Conclusions  
**Function tag:** ASS  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> This may be due to the use of a small sample volume (~1 mm3) in the simulation that cannot consider the polarizations occurring in larger pores.

**Local context:** Identifies a limitation in the simulation volume.  
**Why it works:** It names the likely source of limitation and the omitted process.  
**Transferable rule:** Limitation sentences should link the constrained design to the process it cannot represent.  
**Reusable pattern:** `This may be due to X, which cannot represent Y.`  
**Risk when misused:** Avoid hiding a limitation by replacing it with vague `model uncertainty`.  
**Skill-ready instruction:** Keep limitation causes concrete and bounded.

---

# P06: Permeability Prediction During Mineral Reactions

## Paper-Level Notes

**Strength of writing:** The paper compares limiting cases clearly and repeatedly ties changes in permeability and formation factor to pore-scale alteration patterns.  
**Useful for this skill because:** It is a good source for contrast sentences and careful model applicability statements.

## P06-S01

**Section:** Introduction  
**Function tag:** AIM  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> This study aims to understand whether the commonly used, electrical tortuosity-based permeability model, k = reff2/8F, still works for rocks in different mineral precipitation/dissolution scenarios using a pore-scale, numerical approach.

**Local context:** States the question, model, scenarios, and approach.  
**Why it works:** The aim is framed as testing applicability, not proving superiority.  
**Transferable rule:** Aim sentences can be framed as a bounded test of whether a model works under conditions.  
**Reusable pattern:** `This study aims to understand whether model X still works for Y using Z.`  
**Risk when misused:** `still works` may be informal; polish to `remains applicable` if tone requires.  
**Skill-ready instruction:** Keep applicability questions bounded by model and scenario.

## P06-S02

**Section:** Theory  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> Here “equivalent” means the permeability of porous media with these two pore spaces is the same.

**Local context:** Defines a simplifying term in the theoretical model.  
**Why it works:** It prevents ambiguity in a plain sentence.  
**Transferable rule:** Define quoted or specialized uses of ordinary words.  
**Reusable pattern:** `Here, "X" means Y.`  
**Risk when misused:** Quotation marks should not be used for ordinary emphasis.  
**Skill-ready instruction:** Use direct definitions for terms with special local meaning.

## P06-S03

**Section:** Methods  
**Function tag:** DEF  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> The Pe number compares the rate of advection to the rate of diffusion, and it can be defined as Pe = uLc/Dm.

**Local context:** Defines a dimensionless number before using it in simulations.  
**Why it works:** It gives both physical meaning and formula.  
**Transferable rule:** Define dimensionless numbers by their physical comparison before giving the equation.  
**Reusable pattern:** `The X number compares A to B and can be defined as X = ...`  
**Risk when misused:** Do not polish away the physical comparison and leave only the formula.  
**Skill-ready instruction:** Preserve both meaning and equation for dimensionless parameters.

## P06-S04

**Section:** Methods  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> As observed in laboratory experiments, the reaction-limited precipitation/dissolution pattern is characterized by a roughly uniform growth/removal of minerals at the solid-liquid interface.

**Local context:** Defines one limiting reaction pattern.  
**Why it works:** The definition is tied to an observable pattern.  
**Transferable rule:** Define regimes through their observable behavior.  
**Reusable pattern:** `The X pattern is characterized by Y at Z.`  
**Risk when misused:** `roughly` should be retained when the pattern is approximate.  
**Skill-ready instruction:** Keep approximation markers in regime definitions.

## P06-S05

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> In this study, we use simplified models to mimic the precipitation and dissolution at the pore scale, aiming to capture the main macroscopic features of the samples as observed in laboratory experiments.

**Local context:** Explains the purpose and limitation of simplified models.  
**Why it works:** It does not claim the simplified models reproduce every detail.  
**Transferable rule:** When using simplified models, state what they are intended to capture.  
**Reusable pattern:** `We use simplified models to mimic X, aiming to capture Y.`  
**Risk when misused:** `mimic` can overpromise if not bounded by `main features`.  
**Skill-ready instruction:** Preserve the intended level of representation in simplified-model sentences.

## P06-S06

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> For reaction-limited case, both exponents (n and m) are almost constant without a large variation.

**Local context:** Reports behavior of fitted exponents under one limiting case.  
**Why it works:** It is short and avoids adding mechanism prematurely.  
**Transferable rule:** Report the stable quantity before explaining why it is stable.  
**Reusable pattern:** `For X cases, both A and B remain almost constant.`  
**Risk when misused:** `almost` should not be dropped if variation exists.  
**Skill-ready instruction:** Preserve approximate qualifiers in result summaries.

## P06-S07

**Section:** Results  
**Function tag:** CON  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> For transport-limited cases in Figure 4, both exponents varied considerably despite the minor porosity reduction.

**Local context:** Contrasts transport-limited behavior with reaction-limited behavior.  
**Why it works:** The sentence makes the surprising contrast explicit: large exponent change, small porosity change.  
**Transferable rule:** Use `despite` when the important result is a mismatch between magnitude of cause and response.  
**Reusable pattern:** `For X cases, Y varied considerably despite minor changes in Z.`  
**Risk when misused:** `considerably` requires a clear magnitude or figure reference.  
**Skill-ready instruction:** Keep figure references when they support magnitude language.

## P06-S08

**Section:** Results  
**Function tag:** IMP  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> This is understandable because it is the pore throat rather than pore body that controls the fluid flow in porous media.

**Local context:** Explains why pore body size overestimates permeability.  
**Why it works:** The contrast identifies the controlling feature plainly.  
**Transferable rule:** Mechanism explanation can be concise when it names the controlling element.  
**Reusable pattern:** `This is expected because A rather than B controls C.`  
**Risk when misused:** Avoid `understandable` if the explanation is speculative.  
**Skill-ready instruction:** Use simple causal explanations only when the controlling relation is established.

## P06-S09

**Section:** Discussion  
**Function tag:** IMP  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> This indicates that the applicability of the electrical tortuosity-based permeability model largely depends on the patterns of the mineral precipitation and dissolution.

**Local context:** Interprets when the model is applicable.  
**Why it works:** The conclusion is bounded to applicability and pattern dependence.  
**Transferable rule:** Model-evaluation sentences should say what applicability depends on.  
**Reusable pattern:** `This indicates that the applicability of X depends on Y.`  
**Risk when misused:** Do not turn dependency into universal failure or success.  
**Skill-ready instruction:** Preserve dependency language in model-performance conclusions.

## P06-S10

**Section:** Conclusions  
**Function tag:** CON  
**Score:** 8/10  
**Use status:** caution

**Source sentence:**  
> Compared to reaction-limited cases, transport-limited precipitation/dissolution has a more profound influence on fluid/electric flow and it may be characterized by a sharply changed n or m.

**Local context:** Summarizes the contrast between two limiting cases.  
**Why it works:** It combines comparison with a cautious characterization.  
**Transferable rule:** Use `may be characterized by` when the feature is diagnostic but not exclusive.  
**Reusable pattern:** `Compared to A, B has a stronger influence on C and may be characterized by D.`  
**Risk when misused:** `profound` and `sharply` are strong; keep them only if the data show large changes.  
**Skill-ready instruction:** Check strong adjectives against the original magnitude before retaining them.

---

# P07: Pore Structure and NMR Relaxation

## Paper-Level Notes

**Strength of writing:** The paper defines NMR terms and repeatedly reports signal changes before explaining pore-water distribution.  
**Useful for this skill because:** It provides examples of cautious interpretation in a technically dense field.

## P07-S01

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> While NMR can provide detailed insights into water content and distribution within saturated soils and rocks, interpreting NMR signals from unsaturated subsurface materials remains challenging, even at the laboratory scale.

**Local context:** Establishes the unsaturated interpretation problem.  
**Why it works:** It acknowledges NMR strengths before narrowing to the difficult setting.  
**Transferable rule:** Use concession to state a gap without dismissing the method.  
**Reusable pattern:** `While X can provide insight into A, interpreting X in B remains challenging.`  
**Risk when misused:** The challenge should be explained nearby, not left as a generic statement.  
**Skill-ready instruction:** Preserve what a method can do before stating its limitation.

## P07-S02

**Section:** Introduction  
**Function tag:** GAP  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> However, no study has shown the effect of different pore sizes and shapes on unsaturated NMR relaxation behaviors, contributing to interpretation challenges of unsaturated NMR responses.

**Local context:** Identifies the missing pore-structure dimension.  
**Why it works:** The gap names specific variables and the consequence for interpretation.  
**Transferable rule:** A gap is stronger when it identifies what variable has not been tested.  
**Reusable pattern:** `No study has shown the effect of X on Y, contributing to Z.`  
**Risk when misused:** `no study` is high-risk unless the literature review supports it.  
**Skill-ready instruction:** Downgrade `no study` to `few studies` when certainty is not available.

## P07-S03

**Section:** Methods  
**Function tag:** DEF  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> Fast diffusion, with κ << 1, represents that the diffusion rate is higher than the relaxation rate.

**Local context:** Defines the fast diffusion regime.  
**Why it works:** It ties a regime name to both a criterion and physical meaning.  
**Transferable rule:** Define a regime with its mathematical condition and physical interpretation.  
**Reusable pattern:** `X, with condition C, means that A is higher/lower than B.`  
**Risk when misused:** Do not remove the criterion if the term is technical.  
**Skill-ready instruction:** Preserve criteria such as inequalities when polishing technical definitions.

## P07-S04

**Section:** Methods  
**Function tag:** ASS  
**Score:** 9/10  
**Use status:** positive

**Source sentence:**  
> While the pore shape and pore size distribution are extremely complex in natural soil or rock, we use the idealized simple geometry model in our simulation.

**Local context:** States why idealized geometries are used.  
**Why it works:** It acknowledges natural complexity before the simplification.  
**Transferable rule:** Introduce idealization by naming the real-world complexity it simplifies.  
**Reusable pattern:** `While X is complex in natural systems, we use idealized Y in the simulation.`  
**Risk when misused:** Do not make the idealization sound equivalent to the full natural system.  
**Skill-ready instruction:** Keep the contrast between natural complexity and simplified model.

## P07-S05

**Section:** Methods  
**Function tag:** MET  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> In this study, we use spherical and triangle-shaped pore models to represent the unit cell of porous media, while the pore size distribution of porous media can be represented by constructing multiple pores with different sizes.

**Local context:** Describes the geometry models and size-distribution construction.  
**Why it works:** It connects model shapes to the aspect of pore structure they represent.  
**Transferable rule:** Model-choice sentences should say what feature each simplification represents.  
**Reusable pattern:** `We use A and B models to represent X, while Y is represented by Z.`  
**Risk when misused:** Avoid implying that simple geometries capture all natural pore features.  
**Skill-ready instruction:** Preserve representation language such as `represent` and avoid stronger claims.

## P07-S06

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> From unsaturated to saturated state, in the absence of surface interactions, the T2 amplitude increases, while the peak position remains unchanged.

**Local context:** Reports the baseline behavior without surface interactions.  
**Why it works:** It separates amplitude and peak-position responses.  
**Transferable rule:** Result sentences should distinguish variables that change from those that do not.  
**Reusable pattern:** `From A to B, X increases, while Y remains unchanged.`  
**Risk when misused:** `unchanged` should be retained only for the tested condition.  
**Skill-ready instruction:** Preserve both changing and unchanged quantities in contrastive result sentences.

## P07-S07

**Section:** Results  
**Function tag:** CON  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> However, for ρs = 5 and 15 μm/s, not only does the amplitude of the peak in T2-distribution increase, but the peak also shifts from short to long relaxation time components.

**Local context:** Contrasts surface-relaxivity cases with the baseline.  
**Why it works:** It reports two linked changes under specified parameter values.  
**Transferable rule:** When a condition changes multiple response variables, name each response explicitly.  
**Reusable pattern:** `For condition X, not only does A increase, but B also shifts from C to D.`  
**Risk when misused:** The `not only...but also` structure can feel heavy; use it only for genuinely paired effects.  
**Skill-ready instruction:** Preserve parameter values and avoid smoothing away paired response structure.

## P07-S08

**Section:** Results  
**Function tag:** RES  
**Score:** 8/10  
**Use status:** positive

**Source sentence:**  
> Compared with the system at Sw = 28%, the system at Sw = 44.3%, 79.7%, and 100% shows a decrease in the amplitude of shorter relaxation T2 components.

**Local context:** Reports a saturation-series comparison.  
**Why it works:** It gives the reference condition and comparison conditions.  
**Transferable rule:** Quantitative comparison should name the baseline explicitly.  
**Reusable pattern:** `Compared with X at condition A, X at conditions B, C, and D shows Y.`  
**Risk when misused:** Dropping the baseline can make the comparison ambiguous.  
**Skill-ready instruction:** Preserve baseline and comparison values in result polishing.

## P07-S09

**Section:** Discussion  
**Function tag:** IMP  
**Score:** 9/10  
**Use status:** caution

**Source sentence:**  
> Our results suggest that for two rock or soil samples with similar pore size distributions, if the pore shapes in the two samples are different, even if their T2-distributions exhibit distinct two relaxation time peaks with similar characteristics under the saturated state, the saturations of the overlap of two relaxation time peaks in their T2-distribution are distinct under the unsaturated state.

**Local context:** Interprets how pore shape affects unsaturated NMR behavior.  
**Why it works:** The sentence keeps the implication conditional, although it is long.  
**Transferable rule:** Complex conditional implications should preserve conditions but may need splitting for readability.  
**Reusable pattern:** `For samples with similar A, differences in B can produce distinct C under condition D.`  
**Risk when misused:** The sentence is too long; polishing should split it without changing conditions.  
**Skill-ready instruction:** When simplifying dense implications, keep every condition that limits the claim.

## P07-S10

**Section:** Conclusion  
**Function tag:** IMP  
**Score:** 8/10  
**Use status:** caution

**Source sentence:**  
> This pattern of pore water dynamic distribution ensures that the small pores do not exceed their maximum saturation capacity, avoiding common misinterpretations.

**Local context:** Summarizes how the interpretation method avoids a known error.  
**Why it works:** It states the avoided misinterpretation concretely.  
**Transferable rule:** Implication sentences should name the specific error or ambiguity they resolve.  
**Reusable pattern:** `This pattern ensures that X does not exceed Y, avoiding Z.`  
**Risk when misused:** `ensures` is strong and should be softened if the result is not definitive.  
**Skill-ready instruction:** Keep concrete error-avoidance language, but downgrade strong verbs when evidence is limited.
