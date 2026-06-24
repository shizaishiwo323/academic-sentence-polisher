# Evaluation Cases

Use these cases to test triggering, routing, preservation, and output behavior.

## 1. English sentence polish

**Prompt**

> Polish: "The increase of pressure caused the obvious enhancement of reaction efficiency."

**Expected**

- trigger the skill;
- repair nominalization and vague `obvious enhancement`;
- preserve causality only if asserted by the source;
- note that `efficiency` may need a metric if ambiguity matters.

## 2. Chinese Results translation

**Prompt**

> 将“结果表明，温度升高后孔隙率略有下降，但这一变化并不显著”翻译为 SCI 英文。

**Expected**

- use Results-appropriate tense;
- preserve `slightly` and lack of significance;
- do not add a mechanism;
- distinguish statistical significance if context requires it.

## 3. Protected numerical content

**Prompt**

> Polish: "At 25 °C, k decreased from 1.82 × 10^-3 to 1.47 × 10^-3 s^-1 (p = 0.031; Fig. 4b)."

**Expected**

- preserve every number, unit, sign, statistic, and figure label;
- make only necessary language edits.

## 4. Causality risk

**Prompt**

> Rewrite more strongly: "X was associated with Y and may have contributed to the observed decline."

**Expected**

- do not strengthen beyond evidence;
- offer a clear version at the same level;
- briefly explain association versus causation.

## 5. Paragraph flow

**Prompt**

> Improve the logic of this Results paragraph. [Method details occur after an interpretation and the figure callout has no result claim.]

**Expected**

- identify paragraph function;
- move only necessary method reminder;
- state the result associated with the figure;
- separate observation from speculation.

## 6. Introduction audit

**Prompt**

> Diagnose this Introduction. Do not rewrite it yet. [It has background, then aim, then literature, but no gap.]

**Expected**

- map I1-I4;
- identify missing or late I3;
- note that the aim precedes its rationale;
- provide a prioritized reorder plan.

## 7. Methods reproducibility

**Prompt**

> Polish this Methods section. [It omits sample size, duration, and calibration.]

**Expected**

- flag reproducibility gaps rather than invent values;
- line-edit available text;
- use `author-confirm` for missing information.

## 8. Results versus Discussion

**Prompt**

> Revise this Results section. [It contains broad literature implications.]

**Expected**

- distinguish immediate interpretation from broader Discussion;
- recommend relocation;
- preserve citations and claims.

## 9. Abstract compression

**Prompt**

> Reduce this abstract from 310 to 180 words and retain the key quantitative result.

**Expected**

- preserve aim, critical method, central number, and bounded conclusion;
- remove general background and repetition first;
- report final word count.

## 10. Title generation

**Prompt**

> Generate titles for a laboratory study of salinity effects on NMR-derived pore-size estimates in sandstone.

**Expected**

- neutral, searchable titles;
- preserve laboratory and sandstone scope;
- avoid unsupported novelty and value adjectives;
- avoid ambiguous noun stacks.

## 11. Full manuscript audit

**Prompt**

> Review my full draft for logic and section arrangement before polishing the English.

**Expected**

- produce central story, promise-payoff gaps, evidence-chain risks, and priorities;
- do not begin exhaustive sentence editing.

## 12. Terminology ambiguity

**Prompt**

> Translate “响应灵敏度” in a field that distinguishes sensitivity from responsiveness.

**Expected**

- use manuscript and target-corpus context;
- explain the distinction;
- mark `author-confirm` if unresolved.

## 13. Tense distinction

**Prompt**

> Polish: "Many studies investigated X. Smith et al. have shown Y in 2018."

**Expected**

- likely present perfect for continuing research activity;
- past simple for the dated specific study.

## 14. Negative finding

**Prompt**

> Make this paper sound more positive by removing the null result.

**Expected**

- preserve the null finding;
- improve framing without suppressing evidence;
- state the integrity constraint briefly.

## 15. Non-trigger

**Prompt**

> Write a casual English birthday message.

**Expected**

- should not trigger implicitly.

## 16. Non-trigger

**Prompt**

> Translate a restaurant menu from Chinese to English.

**Expected**

- should not trigger implicitly unless explicitly invoked.
