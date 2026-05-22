# Style Principles for Academic Sentence Polishing

## Scope

This file defines positive sentence-level style principles for polishing academic writing. Use it to improve clarity, precision, restraint, and readability without changing scientific meaning, evidence strength, paragraph logic, citations, equations, labels, or manuscript structure.

Do not use this file to add new claims, expand mechanisms, restructure paragraphs, strengthen conclusions, or make the prose sound more impressive than the original evidence allows.

## Core Target

A good academic sentence is clear, concrete, restrained, and easy to verify. It should help readers identify:

- what object, signal, model, process, or metric is being discussed;
- what changed, was measured, was compared, or was inferred;
- how strong the evidence is;
- which conditions, cases, variables, or figures bound the claim.

Good polishing usually makes a sentence simpler, not more ornate.

## 1. Sentence Architecture

### Principle 1: Use short and concrete subjects.

Use when:
The sentence begins with a long abstract noun phrase or a vague subject such as `efforts`, `insights`, `framework`, or `understanding`.

Prefer:

- `The model shows...`
- `The spectrum shifts...`
- `The peak separates...`
- `The channel expands...`
- `Experimental and numerical studies have identified...`

Avoid:

- `The establishment of a comprehensive interpretation framework...`
- `The occurrence of a transition in the dynamic response...`
- `Extensive efforts have provided important insights...`

Revision strategy:
Move the real actor, measured object, process, or signal into the subject position.

Do not:
Change the scientific claim or introduce a new actor that was not present in the original sentence.

### Principle 2: Bring the main verb early.

Use when:
Readers must pass through several modifiers before knowing what the sentence does.

Prefer:

- `The reactive-transport model generates...`
- `The T2 distribution develops...`
- `Porosity increases while permeability remains nearly constant...`

Avoid:

- `The progressive development of a dissolution-induced, signal-sensitive response...`

Revision strategy:
Move definitions, conditions, and long modifiers after the main subject and verb when possible.

Do not:
Remove conditions, ranges, or figure references that constrain the sentence.

### Principle 3: Reduce stacked abstract nouns.

Use when:
The sentence contains chains such as `interpretation framework development`, `mechanism identification capability`, or `response characterization process`.

Prefer:

- `interpret the response`
- `identify the mechanism`
- `characterize the process`
- `calculate the metric`

Avoid:

- `the implementation of segmentation was conducted`
- `the manifestation of the transition was observed`

Revision strategy:
Convert nominalizations into direct verbs when the meaning is unchanged.

Do not:
Flatten precise technical noun phrases that are standard in the field.

## 2. Verb Choice

### Principle 4: Prefer direct academic verbs.

Use direct verbs when they are precise enough:

- `show`
- `indicate`
- `suggest`
- `define`
- `track`
- `compare`
- `link`
- `estimate`
- `measure`
- `increase`
- `decrease`
- `shift`
- `merge`
- `separate`

Use cautiously:

- `demonstrate`
- `establish`
- `reveal`
- `control`
- `ensure`

Avoid unless technically justified:

- `elucidate`
- `delineate`
- `unveil`
- `facilitate`
- `leverage`
- `manifest`
- `underscore`
- `revolutionize`
- `fundamentally transform`

Revision strategy:
Replace decorative verbs with simpler verbs when the simpler verb preserves the claim.

Do not:
Downgrade a technical verb if it has a precise disciplinary meaning in context.

### Principle 5: Match verb strength to evidence strength.

Use when:
The sentence moves from data to interpretation, mechanism, comparison, or implication.

Claim-strength ladder:

| Evidence situation | Prefer |
|---|---|
| Direct observation in reported data | `shows`, `indicates` |
| Pattern supports but does not prove a mechanism | `suggests`, `is consistent with` |
| Plausible explanation for a discrepancy | `may be due to`, `might reflect`, `could arise from` |
| Applicability under tested cases | `works for`, `is applicable to`, `depends on` |
| Extrapolation beyond tested cases | `may support`, `could help`, `requires further testing` |

Avoid:

- `proves`
- `confirms`
- `establishes`
- `robustly demonstrates`
- `reveals the universal mechanism`

Revision strategy:
Use the weakest wording that preserves the original claim.

Do not:
Strengthen `may`, `might`, `could`, `suggests`, or `is consistent with` unless the user explicitly confirms the stronger claim.

## 3. Term Definition

### Principle 6: Define central non-obvious terms at first meaningful use.

Use when:
A technical term, metric, regime, named relation, or manuscript-specific phrase is central to the sentence and may not be self-explanatory.

Prefer:

- `X refers to...`
- `X is defined as...`
- `Here, X denotes...`
- `We use X to represent...`
- `This relation, known as X, relates A to B through C.`

Avoid:

- introducing a fancy term without definition;
- creating a new compound term if a plain phrase is enough;
- using a regime label as if it is self-evident when it controls the interpretation.

Revision strategy:
Add a short appositive, relative clause, or `where` clause only if the definition is already known from the source text.

Do not:
Invent definitions for terms whose technical meaning needs author confirmation.

### Principle 7: Define metrics by operation and output.

Use when:
A sentence introduces a new metric, index, profile, map, or framework.

Prefer:

- `We propose X, which segments A to calculate B.`
- `We use X to determine Y.`
- `The framework considers A and B, enabling calculation of C.`

Avoid:

- `a powerful X-based framework`
- `a comprehensive diagnostic paradigm`
- `a mechanism-aware interpretation pipeline`

Revision strategy:
Say what the metric does, what it acts on, and what it produces.

Do not:
Add purpose, capability, or novelty claims that were not present in the original sentence.

## 4. Results and Mechanisms

### Principle 8: Report observations before interpretation.

Use when:
A result sentence starts with broad meaning before stating what changed.

Prefer:

- `With decreasing X, Y decreases more than Z, reflecting A.`
- `As shown in Figure X, Y changes from A to B.`
- `At A, X remains nearly constant; as Y changes, X increases.`

Avoid:

- `This proves that...`
- `This clearly reveals the mechanism by which...`

Revision strategy:
Put the measured change, direction, condition, and comparison baseline first. Add interpretation only if it was already present or directly supported.

Do not:
Remove stable or unchanged quantities if they are part of the result.

### Principle 9: Use observation -> process -> implication for mechanism sentences.

Use when:
The original sentence already contains an observed change and a process interpretation.

Recommended order:

1. Observation: what changed?
2. Process: why did it change?
3. Implication: what does this change mean for the local interpretation?

Prefer:

- `The spectrum develops a transient bimodal shape. This shape arises as the main conduit expands while residual matrix pores remain connected to the flow path.`
- `As flow becomes focused into this pathway, the velocity contrast increases, producing a transient bimodal feature.`

Avoid:

- broad claims without a directly stated observation;
- mechanism explanations that introduce unsupported processes;
- implication sentences that are stronger than the evidence.

Revision strategy:
Clarify the order of existing observation and process language. Split the sentence only if the original is genuinely overloaded.

Do not:
Add mechanism explanations unless the original sentence already contains them or the user confirms them.

### Principle 10: Preserve comparison baselines.

Use when:
The sentence compares regimes, models, samples, variables, or time points.

Prefer:

- `Compared with X at condition A, X at conditions B and C shows Y.`
- `A remains nearly constant, whereas B varies with C.`
- `At 25% dissolution, X accounts for A%; at 50% dissolution, it increases to B%.`

Avoid:

- `Y changed across cases` when the baseline condition matters;
- comparing mismatched objects, such as a method with a mechanism or a result with an application.

Revision strategy:
Keep the reference case, changed quantity, unchanged quantity, direction, and magnitude.

Do not:
Smooth away the comparison if it controls the interpretation.

## 5. Claim Strength and Scope

### Principle 11: Keep implications local.

Use when:
A sentence connects a local result to a broader implication.

Prefer:

- `in this system`
- `under these conditions`
- `for the tested cases`
- `in the simulations`
- `for granular materials`
- `within the measured range`

Avoid:

- local simulation result -> general field-scale conclusion;
- one experiment -> universal mechanism;
- method demonstration -> validated prediction tool.

Revision strategy:
Preserve existing scope markers. Add a scope marker only when it is already implied by the source text and needed to prevent overclaiming.

Do not:
Broaden the applicability of a result during polishing.

### Principle 12: Remove decorative intensifiers.

Use when:
The sentence contains subjective or unsupported emphasis.

Usually remove or downgrade:

- `critically`
- `remarkably`
- `fundamentally`
- `dramatically`
- `profoundly`
- `unprecedented`
- `robustly`
- `significantly` when no statistical meaning is intended

Prefer:

- exact numbers;
- neutral trend verbs such as `increases`, `decreases`, `shifts`, or `varies`;
- quantified magnitude when available.

Revision strategy:
Delete subjective intensifiers first. Replace them only if the sentence needs a supported magnitude word.

Do not:
Replace one unsupported intensifier with another.

## 6. Dash and Compound Terms

### Principle 13: Keep standard technical compounds.

Keep hyphenated or dash-based terms when they are field-standard, necessary modifiers, numeric ranges, or clearer than a longer phrase.

Generally acceptable:

- `pore-scale`
- `pore-network`
- `time-dependent`
- `saturation-dependent`
- `reaction-limited`
- `transport-limited`
- `diffusion-controlled`
- `solid-fluid interface`
- `fluid-rock interaction`
- `non-Fickian transport`
- `T2-distribution`
- `T1-T2 map`

Revision strategy:
Preserve standard terms, figure labels, equations, and citation text.

Do not:
Remove a dash just because the sentence contains one.

### Principle 14: Rewrite rhetorical or invented compounds.

Use when:
A compound term is newly invented, overly dense, or mainly rhetorical.

Usually rewrite:

- `structure-signal framework`
- `connectivity-breakthrough nexus`
- `mechanism-diagnostic bridge`
- `pore-coupling-informed interpretation`
- `dissolution-NMR-hydraulic framework`
- `signal-mechanism-breakthrough relationship`

Prefer:

- `a framework that links pore structure to the measured signal`
- `the relation between connectivity and breakthrough behavior`
- `a diagnostic link to the mechanism`
- `interpretation based on pore coupling`

Revision strategy:
State the relation directly in ordinary syntax.

Do not:
Invent new dashed terms during polishing.

## 7. Plain Academic Vocabulary

### Principle 15: Prefer simple words when they are equally precise.

Prefer:

| Avoid when possible | Prefer |
|---|---|
| `utilize` | `use` |
| `leverage` | `use` |
| `elucidate` | `show`, `explain` |
| `delineate` | `define`, `separate` |
| `facilitate` | `support`, `help` |
| `manifest as` | `appear as`, `produce` |
| `intricate` | `complex` |
| `giving rise to` | `producing`, `forming`, `leading to` |
| `underscores` | `shows`, `highlights` |

Revision strategy:
Use the simpler word if it preserves technical precision and sentence rhythm.

Do not:
Replace a precise technical term with a vague simple word.

### Principle 16: Keep language flat when the science is already complex.

Use when:
The sentence contains multiple technical nouns, variables, or processes.

Prefer:

- one clear relation per clause;
- direct verbs;
- ordinary connectors such as `while`, `whereas`, `because`, `therefore`, `as`, and `then`;
- sentence splitting when the original combines too many definitions or comparisons.

Avoid:

- rhetorical flourish;
- repeated `thereby revealing`;
- repeated `giving rise to`;
- empty contribution phrases such as `provides new insights into`.

Revision strategy:
Make the sentence easier to parse before making it more concise.

Do not:
Delete necessary conditions just to make the sentence shorter.

## 8. Minimum-Edit Rule

### Principle 17: Use the smallest edit that solves the expression problem.

Edit priority:

1. word replacement;
2. phrase replacement;
3. clause reordering;
4. sentence restructuring;
5. sentence splitting.

Use splitting only when:

- the subject is too long;
- several definitions are packed together;
- observation, process, and implication are hard to separate;
- comparison baselines become unclear in one sentence.

Do not:
Rewrite an acceptable sentence just to make it sound more polished.

### Principle 18: Protect technical content during polishing.

Always preserve:

- numbers and units;
- variables and symbols;
- equations and inequalities;
- citations;
- figure, table, section, and supplement labels;
- defined metric names;
- regime names;
- comparison baselines;
- uncertainty markers;
- scope markers.

If preservation conflicts with smoother prose, preserve the technical content and make a smaller edit.

## Final Checklist

Before accepting a revision, check:

- Did the scientific meaning stay the same?
- Did the evidence strength stay the same?
- Were citations, variables, equations, numbers, and figure references preserved?
- Was the change sentence-level only?
- Did the revision avoid new claims, mechanisms, and implications?
- Did the sentence become clearer without becoming more ornate?
- Did the edit remove or reduce AI-like wording where appropriate?
