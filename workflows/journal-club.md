# Workflow: Journal Club

Use for a paper deep-dive whose scientific question, evidence chain, methods, limitations, and transferable lessons must be taught clearly.

Read the primary paper, methods, figure legends, and relevant supplementary figures before planning. Verify that each selected panel is the panel described in the slide and notes.

## Inputs and mode

| Input | Required | Role |
|---|---|---|
| Primary paper PDF | Yes | factual authority for numbers, results, and claims |
| Supplementary PDF | No | extends the evidence chain |
| ChatGPT dialogue / personal notes (markdown file path) | No | how *you* came to understand the paper |

- **Standard mode** — primary PDF only (plus supplement if provided).
- **Deep-read mode** — the user also gives a dialogue/notes file path. Whenever a dialogue or notes file is provided, plan in Deep-read mode; do not ask whether it should be used.
- Read the dialogue file from its path and extract the question chain; never paste raw dialogue into the deck.

## Source hierarchy (hard rule)

- **Factual authority**: paper / supplement > dialogue. Every number, statistic, and conclusion that first appears in the dialogue must be re-checked against the PDF before it may become a claim. Dialogue decides *how* to present and *what* to emphasize; it never decides *what the facts are*.
- **Interpretive priority**: the user's question chain and personal notes > a generic paper summary. Lead with what the reader actually asked and where they got stuck.
- Do not inherit a dialogue paraphrase as a claim; if it conflicts with the paper, stop and re-audit the claim registry.

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
| Material qualification | causal/clinical/generalization scope when it changes interpretation |
| Method worth learning | only if method matters for the user's learning goal |
| Link to next figure | why the next experiment is needed |

## Planning artifact: `understanding_map.md` (Deep-read mode only)

When a dialogue/notes file is provided, also produce `understanding_map.md`. Extract only what changed understanding; do not mechanically preserve whole ChatGPT answers.

| Section | Content |
|---|---|
| Question chain | what I first failed to understand; what question each answer raised next; which question ultimately changed my reading |
| Key conceptual hurdles | concept; why it was hard; the explanation that worked; whether it needs onboarding on a slide |
| Interpretation / insight | my understanding; the source passage; status (`source-supported` / `interpretation`) |
| Critical points | what I doubted; whether the paper actually resolves it; how to phrase the boundary in the deck |
| Methods worth learning | method; why it is worth learning; whether to expand Methods |
| Relevance to my work | directly reusable / inspiring only / must not extrapolate |

The understanding map shapes section order, figure emphasis, and speaker notes; it never overrides the paper as the factual source.

## Narrative grammar

Default structure:

1. **Question / concept onboarding** — usually 1–2 slides, not a textbook chapter.
2. **Field / author trajectory** — optional and brief; include only when it clarifies the novelty.
3. **Experimental design** — show the paper's overall workflow before dense figures when needed.
4. **Evidence chain** — organize by scientific question, usually one major figure per slide or per two slides.
5. **Critical synthesis** — what is genuinely new, what remains uncertain, and what is transferable to the user's work.

Do not mechanically show every panel. A figure can be summarized if its only role is robustness or a secondary control. Keep the main evidence large enough to read.

**Deep-read mode**: use the question chain from `understanding_map.md` as the primary section hooks. The deck should read as *「我带着什么问题读 → 哪一步让我真正相信 → 哪一步我仍不接受 → 这对我们有什么用」*, not as Introduction → Figure 1 → Figure 2 → Conclusion. Surface the reader's conceptual hurdles as onboarding moments and their doubts as explicit critique.

Title figure slides by the scientific question or supported conclusion, not by “Figure 3” alone. Use the source figure number only as a locator.

If one source figure supports sequential claims at different evidence levels, split those claims across slides when needed. For example, establish readout reliability or breadth before using a separate panel to argue mechanistic proximity; do not compress both into one slide merely because they share a figure number.

Preserve the source's statistical notation and denominator for every quoted metric. Record the exact statistic name, subset, threshold, analysis unit, and source locator; do not silently rewrite `Spearman ρ` as `R²` or present a subset percentage as if it described the full cohort.

## Figure-slide grammar

A good figure slide answers, in order:

`What is the question? → How did they test it? → How do I read this panel? → What is the result? → What conclusion follows?`

Use the slide itself for the question, key result, and 1–3 visual guides. Put detailed panel-by-panel walkthrough in speaker notes so the page stays sparse.

## Notes protocol for Journal Club

For figure-heavy slides, notes may be longer than other deck types. Prefer this sequence:

1. remind the audience of the current question;
2. describe the experiment and analysis unit;
3. explain axes/colors/panels/thresholds needed to read the figure;
4. state the result;
5. state the supported conclusion and any qualification needed to interpret it;
6. bridge to why the next figure is necessary.

Avoid reciting every panel if it does not change the inference.

**Deep-read mode**: prefer the reader's own understanding journey in notes — what was hard, which explanation finally worked, what you still doubt — over a neutral walkthrough. Keep statistics, results, and boundaries locked to the paper.

## Closing rule

Do not end with a generic paper summary. Prefer three outputs:

- **What this paper changes**;
- **What remains unresolved / where the evidence is weakest**;
- **What our lab can directly reuse, test, or extend**.
