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

- **Factual authority**: verify study results against the primary paper and supplement, and external background against the relevant primary literature.
- **Dialogue and notes**: trace factual claims to those sources, and record the evidence and reasoning behind interpretations or proposals. Resolve discrepancies before using the affected claim.
- **Presentation priority**: use the user's learning goals and notes to identify useful emphasis and explanations. Select the main narrative for the audience's prerequisites and the paper's evidence chain.

## Audience question

> 这篇文章究竟解决了什么问题？作者用什么证据一步步支持结论？这些证据支持到哪一步？我们能学走什么？

## Planning artifact: `journal_map.md`

### A. Paper map

Record first:

- audience background and intended learning outcome;
- one-sentence central scientific question;
- author hypothesis / proposed mechanism;
- field gap before this work;
- main contribution after this work;
- concepts and methods the audience needs to understand the central evidence;
- paper identity and key teams' research focus; expand their prior work only when it explains this study's question or novelty.

### B. Figure map

Account for each main figure's role and placement, then detail the selected panels below. Reuse this map for coverage review rather than creating a separate checklist.

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
| Placement | main deck / notes / backup / omitted; briefly explain omission of a main figure |

## Planning artifact: `understanding_map.md` (Deep-read mode only)

When a dialogue/notes file is provided, record `understanding_map.md` or equivalent entries in the existing planning source. Extract what changed understanding and unresolved questions relevant to the learning goal.

| Section | Content |
|---|---|
| Question chain | what I first failed to understand; what question each answer raised next; which question ultimately changed my reading |
| Key conceptual hurdles | concept; why it was hard; the explanation that worked; relevance to this audience's prerequisites |
| Interpretation / insight | my understanding; source passages; status using the shared [evidence-status definitions](../references/scientific-content-contract.md#evidence-status) |
| Critical points | what I doubted; whether the paper resolves it; whether it changes a central claim or its interpretation |
| Methods worth learning | method; why it is worth learning; whether to expand Methods |
| Relevance to my work | directly reusable / inspiring only / must not extrapolate |

Classify reading questions by their role: a prerequisite for understanding, a consequential issue in the evidence, or a local detail. A prerequisite needs explanation; a consequential issue needs source-checked discussion; a local detail can stay in notes or backup. The fact that the reader once asked a question does not itself make it a limitation of the paper.

## Narrative grammar

Default structure:

1. **Question / concept onboarding** — introduce the problem and prerequisites needed for the evidence that follows.
2. **Paper / team context** — briefly introduce the paper and key teams' relevant expertise near the opening; use a dedicated page only when the content warrants it.
3. **Experimental design** — show the paper's overall workflow before dense figures when needed.
4. **Evidence chain** — organize main figures, supplementary evidence, and Methods by scientific question, splitting or combining panels according to their inferential role and readability.
5. **Synthesis** — the contribution supported by the presented evidence, useful lessons, and consequential unresolved questions when present.

Use source panels for the key results and schematics to explain the design or method. A schematic should lead back to the evidence supporting the conclusion. Coverage follows the central claims, not a target number of figures, panels, or pages; summarize secondary controls when that preserves the inference. Retain negative or mixed results that affect the central conclusion.

**Deep-read mode**: use the understanding map to choose explanations and emphasis within this evidence chain. A useful explanation can be retained after the original confusion has been resolved; the audience need not retrace the dialogue's chronology.

Title figure slides by the scientific question or supported conclusion. Put each source panel locator once per slide, usually in the footer. Give literature cited in slides or notes a matching bibliographic entry with a DOI or source link.

If one source figure supports sequential claims at different evidence levels, split those claims across slides when needed. For example, establish readout reliability or breadth before using a separate panel to argue mechanistic proximity; do not compress both into one slide merely because they share a figure number.

Preserve the source's statistical notation and denominator for every quoted metric. Record the exact statistic name, subset, threshold, analysis unit, and source locator; do not silently rewrite `Spearman ρ` as `R²` or present a subset percentage as if it described the full cohort.

## Teaching methods and comparisons

Before introducing an unfamiliar method, explain which need in the preceding scientific argument it addresses. Follow the relevant input through the operation to the output used in the next step. Give the audience enough reasoning to understand the evidence; expand technical detail when it serves the learning goal.

Use a schematic or short calculation when it makes that operation easier to follow. Explain the formula's purpose before its symbols and keep the example tied to the current input and output. Apply the shared formula and illustrative-data rules.

When a comparison spans stages or repeated rounds, identify the objects being compared, what stays fixed, what changes, and the reference measurement or outcome. For model updates, state which observations enter training and which remain reserved for evaluation. Introduce an opaque identifier with its object and current role, then preserve that identity as its role changes across stages.

## Figure-slide grammar

The slide and spoken explanation together answer:

`What is the question? → How did they test it? → How do I read this panel? → What is the result? → What conclusion follows?`

Use the slide itself for the question, large evidence panels or explanatory diagrams, and brief guides needed to read them. Keep a prerequisite on the main path when later evidence depends on it. Express the user's emphasis through teaching depth; keep production labels and presenter assignments in the planning record.

## Notes and backup placement

Use the defaults and adaptations in the [Journal Club speaker-notes protocol](../references/speaker-notes-protocol.md#journal-club).

Place supporting detail according to how it will be used:

- **Notes**: explanation or supporting detail that can be understood alongside the current visual.
- **Backup**: a specific follow-up question that needs its own figure, table, comparison, or extended derivation to answer. Each backup page should have a clear question and a connection to the main deck.
- **Omit**: detail that adds neither understanding of the evidence nor a useful answer to a relevant follow-up question.

Use effective explanations from the reader's notes without copying resolved debate or drafting instructions into the spoken script. Match depth to the audience's needs; a possible question alone does not justify another page. After removing or moving a page, repair adjacent transitions and page references as part of the shared consistency check.

## Closing rule

Synthesize what the presented evidence establishes and what the lab can reuse, test, or extend. Discuss unresolved issues where they affect the central conclusion or intended application. Let those findings determine the closing structure; there is no required limitation page or three-part summary.

When proposing a follow-up experiment, use `finding → unresolved question → feasible test → outcomes that distinguish explanations`. Verify the critical intervention and controls against methods or primary literature, and identify the experiment on the slide as a proposal.
