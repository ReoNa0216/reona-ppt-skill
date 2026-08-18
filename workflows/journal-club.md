# Workflow: Journal Club

Use for a paper deep-dive whose scientific question, evidence chain, methods, limitations, and transferable lessons must be taught clearly.

Read the primary paper, methods, figure legends, and relevant supplementary figures before planning. Verify that each selected panel is the panel described in the slide and notes.

## Audience question

> 这篇文章究竟解决了什么问题？作者用什么证据一步步支持结论？哪些地方成立、哪些地方没有证明？我们能学走什么？

## Planning artifact: `journal_map.md`

### A. Paper map

Record first:

- one-sentence central scientific question;
- author hypothesis / proposed mechanism;
- field gap before this work;
- main contribution after this work;
- 1–3 key terms that need onboarding;
- optional author/lab trajectory or prior-platform context **only if it helps explain why this study exists**.

### B. Figure map

For each main figure or selected panel:

| Field | Required content |
|---|---|
| Question | What question does this figure answer? |
| Experiment | What was actually done? |
| Analysis unit | cell / drug / mouse / patient / image etc. |
| Readout | what axes, colors, groups, scores, or panels mean |
| Result | what changed or was observed |
| Supported claim | the strongest defensible conclusion |
| Does not prove | causal/clinical/generalization boundary |
| Method worth learning | only if method matters for the user's learning goal |
| Link to next figure | why the next experiment is needed |

## Narrative grammar

Default structure:

1. **Question / concept onboarding** — usually 1–2 slides, not a textbook chapter.
2. **Field / author trajectory** — optional and brief; include only when it clarifies the novelty.
3. **Experimental design** — show the paper's overall workflow before dense figures when needed.
4. **Evidence chain** — organize by scientific question, usually one major figure per slide or per two slides.
5. **Critical synthesis** — what is genuinely new, what remains uncertain, and what is transferable to the user's work.

Do not mechanically show every panel. A figure can be summarized if its only role is robustness or a secondary control. Keep the main evidence large enough to read.

Title figure slides by the scientific question or supported conclusion, not by “Figure 3” alone. Use the source figure number only as a locator.

If one source figure supports sequential claims at different evidence levels, split those claims across slides when needed. For example, establish readout reliability or breadth before using a separate panel to argue mechanistic proximity; do not compress both into one slide merely because they share a figure number.

Preserve the source's statistical notation and denominator for every quoted metric. Record the exact statistic name, subset, threshold, analysis unit, and source locator; do not silently rewrite `Spearman ρ` as `R²` or present a subset percentage as if it described the full cohort.

## Figure-slide grammar

A good figure slide answers, in order:

`What is the question? → How did they test it? → How do I read this panel? → What is the result? → What does it prove / not prove?`

Use the slide itself for the question, key result, and 1–3 visual guides. Put detailed panel-by-panel walkthrough in speaker notes so the page stays sparse.

## Notes protocol for Journal Club

For figure-heavy slides, notes may be longer than other deck types. Prefer this sequence:

1. remind the audience of the current question;
2. describe the experiment and analysis unit;
3. explain axes/colors/panels/thresholds needed to read the figure;
4. state the result;
5. state the conclusion boundary;
6. bridge to why the next figure is necessary.

Avoid reciting every panel if it does not change the inference.

## Closing rule

Do not end with a generic paper summary. Prefer three outputs:

- **What this paper changes**;
- **What remains unresolved / where the evidence is weakest**;
- **What our lab can directly reuse, test, or extend**.
