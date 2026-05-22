# Corpus Rule Cards

These cards compress the sentence records in `source_sentence_corpus.md` into executable rules for sentence-level academic polishing. They are rules for expression only; they must not change scientific logic, evidence, citations, variables, equations, figure labels, or paragraph structure.

Each rule card includes `Derived from` so the rule can be traced back to specific corpus records. Do not add future rules without this mapping.

## DEF-01: Define central terms at first meaningful use

**Derived from:** P01-S01, P05-S03, P06-S02

**Problem addressed:** AI-style writing often introduces a fancy noun or named framework without telling the reader what it means.  
**Rule:** If a term is central and not self-explanatory, define it immediately with a short appositive, relative clause, or `where` clause.  
**Preferred patterns:**
- `This relation, known as X, relates A to B through C.`
- `Here, X means Y.`
- `X, with condition C, means that A is higher than B.`
**Avoid:** New labels such as `mechanism-diagnostic bridge` unless the label is defined and necessary.  
**Skill instruction:** Add or preserve definitions for central terms; do not define common terms just to sound formal.

## DEF-02: Pair equations and symbols with plain-language meaning

**Derived from:** P01-S05, P02-S04, P04-S04, P06-S03, P07-S03

**Problem addressed:** Polishing can make formula sentences cleaner but accidentally remove the meaning of symbols.  
**Rule:** Keep equations, variables, inequalities, and ranges intact; simplify only the surrounding prose.  
**Preferred patterns:**
- `Here, X = A/B, where A is ... and B is ...`
- `The X number compares A to B and can be defined as X = ...`
- `X has values ..., where X denotes ...`
**Avoid:** Rewriting equations, deleting units, or replacing variables with vague pronouns.  
**Skill instruction:** Treat equations and variable definitions as protected content.

## DEF-03: Define regimes through observable behavior

**Derived from:** P02-S08, P03-S01, P06-S04, P07-S03

**Problem addressed:** AI often treats regime labels as self-explanatory.  
**Rule:** When a sentence introduces a regime, state the behavior, condition, or observation that defines it.  
**Preferred patterns:**
- `The X pattern is characterized by Y at Z.`
- `For small X, Y occurs in regime Z, where criterion C holds.`
- `This process is known as X and can be described by Y.`
**Avoid:** `X is a critical regime` without saying what physically identifies it.  
**Skill instruction:** Keep regime labels tied to their physical or measurable criteria.

## GAP-01: Acknowledge existing capability before naming the hard case

**Derived from:** P04-S01, P07-S01

**Problem addressed:** AI gap sentences often make prior work sound useless.  
**Rule:** Use concession when the method works in one setting but remains difficult in another.  
**Preferred patterns:**
- `Although X can provide insight into A, its application to B remains challenging.`
- `While X can provide insight into A, interpreting X in B remains challenging.`
**Avoid:** `Previous studies failed to...` unless the source explicitly says so.  
**Skill instruction:** Preserve balanced gap framing and avoid dismissive language.

## GAP-02: Make the missing piece specific

**Derived from:** P01-S02, P04-S02, P07-S02

**Problem addressed:** Vague gaps such as `little is known` do not help the reader.  
**Rule:** Name the unresolved relation, mechanism, metric, scale, condition, or variable.  
**Preferred patterns:**
- `How X changes with Y, and how this change can be observed and quantified, remains unresolved.`
- `A physical understanding of X remains limited because Y is not well constrained.`
**Avoid:** `This remains a major challenge` without a specific missing element.  
**Skill instruction:** Replace broad unknowns with concrete unresolved questions.

## GAP-03: State scope limitations, not literature failure

**Derived from:** P02-S01, P03-S03

**Problem addressed:** AI gap language often overstates by saying prior studies `ignored` or `failed`.  
**Rule:** Describe what prior studies mainly focused on and what assumption remains untested.  
**Preferred patterns:**
- `Most studies on X have focused on cases where Y remains constant.`
- `Existing classifications often rely on Y rather than Z.`
**Avoid:** `Previous studies failed to consider...` unless directly supported.  
**Skill instruction:** Use scope-based gap wording for literature review sentences.

## GAP-04: Use exclusivity words only with evidence

**Derived from:** P02-S01, P03-S03, P07-S02

**Problem addressed:** Words such as `solely`, `no study`, and `only` can overclaim.  
**Rule:** Retain exclusivity only when the original literature review supports it; otherwise downgrade.  
**Preferred patterns:**
- `often relies on`
- `has primarily focused on`
- `few studies have examined`
**Avoid:** `no study has shown` when the author cannot verify the full literature.  
**Skill instruction:** Downgrade high-risk gap claims unless the user confirms the literature basis.

## AIM-01: Say what the study does before why it matters

**Derived from:** P01-S03, P06-S01

**Problem addressed:** AI often turns study aims into promotional contribution claims.  
**Rule:** Aim sentences should name method, object, and target relation.  
**Preferred patterns:**
- `Here, we use X to obtain Y and analyze Z.`
- `This study aims to understand whether model X remains applicable under Y.`
**Avoid:** `This study provides unprecedented insight into...`  
**Skill instruction:** Keep aim sentences procedural, direct, and bounded.

## AIM-02: Define a new metric by operation and output

**Derived from:** P02-S02, P02-S05

**Problem addressed:** New metric names can sound like decorative frameworks.  
**Rule:** When introducing a metric, state what it segments, measures, calculates, or compares.  
**Preferred patterns:**
- `We propose X, which segments A to calculate B.`
- `We use X to determine Y.`
**Avoid:** `a powerful X-based framework` without operational content.  
**Skill instruction:** If a new term is necessary, immediately attach what it does.

## AIM-03: Keep framework claims concrete

**Derived from:** P05-S02, P05-S06

**Problem addressed:** `framework` can become a fancy placeholder.  
**Rule:** Use `framework` only when the sentence specifies the processes included and quantities produced.  
**Preferred patterns:**
- `We develop a framework to consider X in Y, enabling calculation of Z.`
- `The framework is outlined in Figure X, and the details are discussed below.`
**Avoid:** `a comprehensive framework for new understanding` without inputs and outputs.  
**Skill instruction:** Replace empty framework language with concrete method-output wording.

## MET-01: Use direct verbs for method steps

**Derived from:** P02-S05, P04-S05, P05-S05

**Problem addressed:** AI often turns simple method actions into nominalized prose.  
**Rule:** Prefer verbs such as `use`, `segment`, `calculate`, `scan`, `extract`, and `compare`.  
**Preferred patterns:**
- `We segment X along Y and calculate Z.`
- `Samples were scanned at X resolution, and Y segmentation was performed on Z.`
**Avoid:** `the implementation of segmentation was conducted`.  
**Skill instruction:** Convert heavy nominalizations into direct method verbs.

## MET-02: Preserve reproducibility details

**Derived from:** P01-S04, P04-S05, P07-S08

**Problem addressed:** Concision edits can remove parameters needed for reproducibility.  
**Rule:** Keep resolution, ranges, units, boundary conditions, sample states, and figure references.  
**Preferred patterns:**
- `X varies from A to B, defined by criteria C and D.`
- `Samples were scanned at X resolution.`
**Avoid:** Removing numeric values to make the sentence smoother.  
**Skill instruction:** Protect all numerical and procedural details.

## MET-03: Explain model representation, not model ambition

**Derived from:** P03-S04, P07-S05

**Problem addressed:** AI method prose often adds unnecessary claims about what the model enables.  
**Rule:** A model sentence should say what the model represents and how.  
**Preferred patterns:**
- `The X model represents Y as Z.`
- `We use A and B models to represent X.`
**Avoid:** `This model captures the full complexity of...` unless explicitly supported.  
**Skill instruction:** Keep representation language modest and literal.

## MET-04: Link simplified methods to intended scope

**Derived from:** P06-S05, P07-S04, P07-S05

**Problem addressed:** Simplified models can be polished into overconfident descriptions.  
**Rule:** State what the simplified model is intended to mimic or capture.  
**Preferred patterns:**
- `We use simplified models to mimic X, aiming to capture Y.`
- `While X is complex in natural systems, we use idealized Y in the simulation.`
**Avoid:** Claiming that a simplified model fully represents natural complexity.  
**Skill instruction:** Preserve the intended level of simplification.

## ASS-01: State the condition that justifies a simplification

**Derived from:** P03-S06, P05-S07

**Problem addressed:** AI sometimes deletes the reason an assumption is acceptable.  
**Rule:** Keep the parameter range, scale relation, or physical condition that supports an assumption.  
**Preferred patterns:**
- `For the range of X considered here, Y is small relative to Z, allowing us to neglect A.`
- `This model is only valid for X with condition C.`
**Avoid:** `We neglect A` without the condition.  
**Skill instruction:** Never remove assumption boundaries.

## ASS-02: Acknowledge excluded factors without adding new conclusions

**Derived from:** P02-S10, P04-S10

**Problem addressed:** AI may turn limitations into speculative discussion.  
**Rule:** Name what the study focuses on and which factor remains outside that focus.  
**Preferred patterns:**
- `While this study focuses on X, Y remains an important factor that can influence Z.`
- `X may be less suitable for Y where Z is not available.`
**Avoid:** Expanding a limitation into a new mechanism.  
**Skill instruction:** Keep out-of-scope factors as limitations or context.

## ASS-03: Pair limitation with scope, not reassurance

**Derived from:** P03-S10, P05-S10

**Problem addressed:** AI often softens limitations until they disappear.  
**Rule:** A limitation can be followed by relevance, but the constraint must remain visible.  
**Preferred patterns:**
- `Although this study is based on X, Y has also been observed in Z.`
- `This may be due to X, which cannot represent Y.`
**Avoid:** `This limitation does not affect the conclusions` unless explicitly shown.  
**Skill instruction:** Preserve limitations and avoid over-reassuring language.

## RES-01: Report observation before interpretation

**Derived from:** P03-S07, P04-S06

**Problem addressed:** AI result sentences often jump to mechanism before the result is clear.  
**Rule:** State the measured or observed change first; add interpretation only if already present.  
**Preferred patterns:**
- `With decreasing X, Y decreases more than Z, reflecting A.`
- `As seen in Figure X, Y changes from A to B.`
**Avoid:** Starting with `This proves that...`  
**Skill instruction:** Keep result-first ordering.

## RES-02: Preserve comparison baselines

**Derived from:** P06-S07, P07-S08

**Problem addressed:** Polishing can make comparisons smoother but less precise.  
**Rule:** Keep baseline condition, comparison condition, direction of change, and variables.  
**Preferred patterns:**
- `Compared with X at condition A, X at conditions B and C shows Y.`
- `For X cases, Y varied considerably despite minor changes in Z.`
**Avoid:** `Y changed across cases` when the baseline matters.  
**Skill instruction:** Do not drop the reference condition in comparison sentences.

## RES-03: State both changed and unchanged quantities

**Derived from:** P01-S06, P07-S06

**Problem addressed:** AI may simplify contrastive results by reporting only the change.  
**Rule:** If one variable changes and another remains stable, preserve both.  
**Preferred patterns:**
- `From A to B, X increases, while Y remains unchanged.`
- `At A, X remains nearly constant; as Y changes, X increases.`
**Avoid:** `X changes with Y` when the unchanged part is important.  
**Skill instruction:** Preserve negative or stable results because they often control interpretation.

## RES-04: Anchor figure sentences to the key visual information

**Derived from:** P03-S09, P04-S08

**Problem addressed:** Figure references can become empty signposts.  
**Rule:** State what the figure shows, including the trend, transition, or contrast.  
**Preferred patterns:**
- `Figure X shows that A leads to B, while C results in D.`
- `In Figure X, A represents ..., while B corresponds to ...`
**Avoid:** `Figure X clearly illustrates the mechanism` without saying what is shown.  
**Skill instruction:** Keep figure labels and add only the observed content already present.

## RES-05: Keep magnitude words proportional to data

**Derived from:** P01-S06, P02-S06, P06-S10

**Problem addressed:** AI overuses `dramatically`, `significantly`, and `substantially`.  
**Rule:** Use magnitude words only when supported by numeric values, figure trends, or original wording.  
**Preferred patterns:**
- `increases`
- `decreases`
- `varies considerably` only with a clear comparison
**Avoid:** `remarkably`, `fundamentally`, `profoundly` unless the paper explicitly supports them.  
**Skill instruction:** Downgrade unsupported intensifiers to neutral trend verbs.

## CON-01: Compare matched objects

**Derived from:** P02-S07, P06-S10

**Problem addressed:** AI comparison sentences can compare mismatched scales or concepts.  
**Rule:** Use contrast structures only for comparable regimes, cases, variables, or models.  
**Preferred patterns:**
- `Unlike A, where X occurs, B involves Y.`
- `Compared to A, B has a stronger influence on C.`
**Avoid:** Comparing a method with a result or a mechanism with an application.  
**Skill instruction:** Check that both sides of a comparison are parallel.

## CON-02: Use contrast to clarify mechanism, not to dramatize

**Derived from:** P03-S09, P07-S07

**Problem addressed:** AI turns contrasts into rhetorical emphasis.  
**Rule:** Let the contrast identify a physical or methodological difference.  
**Preferred patterns:**
- `A leads to B, while C results in D.`
- `A remains constant, whereas B varies with C.`
**Avoid:** `in stark contrast` unless the data justify a stark difference.  
**Skill instruction:** Prefer neutral contrast words such as `whereas`, `while`, and `compared with`.

## CON-03: Keep concessive uncertainty in classification

**Derived from:** P02-S09, P06-S04

**Problem addressed:** Gradual regime boundaries are often polished into hard categories.  
**Rule:** Preserve markers such as `subtle`, `features of`, `approximately`, and `roughly`.  
**Preferred patterns:**
- `Although the boundary is subtle, X exhibits features of Y.`
- `The pattern is roughly uniform.`
**Avoid:** Converting partial classification into definitive labels.  
**Skill instruction:** Do not remove uncertainty markers from regime-classification sentences.

## IMP-01: Use tentative verbs for inference

**Derived from:** P01-S08, P01-S09, P05-S09

**Problem addressed:** AI often upgrades `suggests` to `demonstrates` or `proves`.  
**Rule:** Use tentative verbs when moving from result to mechanism, discrepancy explanation, or broader relation.  
**Preferred patterns:**
- `This trend suggests that there might be a relation between X and Y.`
- `This discrepancy might be due to X.`
- `This behavior is consistent with Y.`
**Avoid:** `proves`, `confirms`, `establishes` unless the original evidence is decisive.  
**Skill instruction:** Preserve or restore the original evidence strength.

## IMP-02: Name the mechanism only if it is already present

**Derived from:** P03-S08, P06-S08

**Problem addressed:** AI polishers invent mechanism to make sentences sound deeper.  
**Rule:** Clarify existing mechanism language but do not add new causal processes.  
**Preferred patterns:**
- `X forms due to Y, based on feedback between A and B.`
- `This is expected because A rather than B controls C.`
**Avoid:** Adding `thereby revealing a feedback mechanism` when the original did not state one.  
**Skill instruction:** If mechanism is uncertain, mark `author-confirm`.

## IMP-03: Keep broad relations bounded by domain and evidence type

**Derived from:** P01-S10, P06-S09

**Problem addressed:** Local results can be polished into universal conclusions.  
**Rule:** Preserve phrases such as `for granular materials`, `in simulations`, `under these conditions`, and `for the tested cases`.  
**Preferred patterns:**
- `Our numerical results suggest that, for X, a relation might exist between A and B.`
- `This indicates that applicability depends on Y.`
**Avoid:** Removing scope qualifiers to make a sentence shorter.  
**Skill instruction:** Do not broaden local evidence.

## IMP-04: State practical meaning through the specific error or use case

**Derived from:** P04-S09, P07-S10

**Problem addressed:** AI implication sentences often become generic `new insights` claims.  
**Rule:** Name the interpretation error avoided, the metric tracked, or the application condition.  
**Preferred patterns:**
- `This pattern ensures that X does not exceed Y, avoiding Z.`
- `This trend reflects X and indicates that Y can track Z.`
**Avoid:** `These findings provide important insights into...`  
**Skill instruction:** Replace generic contribution language with the concrete function of the result.
