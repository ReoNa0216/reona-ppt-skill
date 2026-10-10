# Progress Method Comparison

Read when a Progress workstream compares an earlier and a current algorithm or processing pipeline. Use the existing Progress map and production source; load the computational evidence reference as required by the workstream's evidence profile.

## Comparison identity and audience goal

Record which implementations, executed snapshots, inputs, and outputs the user wants compared. An original implementation, a reconstruction that preserves its rules, and a faster execution of the new rules answer different questions. Label each by its actual role. A comparison of two executions of the new rules may support an engineering diagnostic; it cannot stand in for the requested old-versus-new method comparison.

Separate changes to scientific rules from changes to execution. State the problem each change addresses and the behavior it preserves or deliberately changes. For an execution-only change, use the existing appropriate equality or tolerance checks; for a rule change, evaluate the resulting differences rather than promising identical outputs. Use run artifacts to establish either claim.

Select the narrative from the user's questions. When method understanding is a primary goal, a useful order is:

`scientific input and output → baseline operation → changed operation and reason → computational cost → output distributions and paired agreement → decision-relevant summary`

Use only the dimensions that matter for this request. Additional diagnostics and same-rule comparisons belong in notes or backup when they help; they should not displace the requested comparison.

## Teach the operation, then its acceleration

Choose a small valid teaching input and keep its identities consistent across relevant stages. Begin with the actual scientific hierarchy, such as specimen, repeated measurement, working observation, and output entry. State whether an operation acts within one specimen or pools observations across specimens. A row number, lookup list, flag, or index should be introduced through the scientific object it represents.

For every unfamiliar operation, show enough of `input → intermediate state → decision → output` that the audience can work through the example. Explain how a range is generated, what its bounds mean, how repeated observations are counted, and what changes after an observation is used when those facts govern the method.

Distinguish item labels from counts at boundaries. For example, if 3 observations lie before the left boundary and 9 before the right boundary, the range contains `9 − 3 = 6` observations. The difference works because the first count removes the observations outside the range on the left. An inclusive range of item labels uses a different convention. For interval updates, show what starts, what stops, and the running value after each position before introducing the compact implementation name. These are teaching examples, not mandatory operations for every method.

Explain acceleration against the already understood work: which repeated search, counting operation, allocation, or copy is removed; which intermediate object is reused; and which output stays the same. Avoid replacing a scientific explanation with a list of data-structure names.

## Give schematics a testable teaching job

Before generating a visual, specify the uncertainty it should resolve and the required objects, memberships, arrows, and before/after states. A generic arrow from signals to a matrix is useful only when it explains the mapping the audience needs; a method-change diagram must show the changed operation.

Actively use image generation when a conceptual schematic will clarify grouping, ownership, repeated work, or a state transition. Use native diagram elements where exact labels, arithmetic, or geometry need tighter control. Inspect the rendered result against the worked example: all identities, memberships, numbers, and arrows must agree. Regenerate or revise a visually attractive image that obscures the operation. Follow the scientific content contract for illustrative values and evidence provenance.

## Report performance at the measured scope

Record the timed input/output boundary, included and excluded stages, implementation versions, hardware and concurrency, warm-up/compilation/cache treatment, and repeat count where they affect interpretation. Peak process memory and final output size are different quantities; name the measured metric and its unit.

Choose repetitions from the required precision, run cost, and observed variation; do not prescribe one count for every benchmark. Reuse suitable recorded measurements when their versions and conditions match, documenting their origin. Show individual runs when practical and a summary suited to the question, such as mean and sample SD. A variability statistic belongs in the main deck when stability is a primary question.

For phase savings, give the seconds saved and define any percentage denominator. A phase that combines several operations and rule changes is a measured phase comparison. Independent module attribution requires a fixed-rule controlled comparison; phase timing alone does not supply it.

If a cost metric worsens, show the measured tradeoff and inspect available profiling evidence before assigning a cause. Further investigation or code changes follow the authorized scope; a slide-making task does not require new optimization experiments. When an authorized repair changes the implementation, refresh affected measurements, plots, tables, notes, and version references together and verify the relevant output invariants.

## Compare output structure and values separately

Choose plots for the quantities the user needs to assess, using consistent old/new colors, readable numeric ticks and units, and comparable scales across datasets. Use ordinary numeric formatting or scientific notation for ticks; put scale factors in axis labels. Keep plot labels and adjacent slide text far enough apart to read at presentation scale.

- **Output structure:** show the number and distribution of output objects across scientifically meaningful coordinates, plus coverage or detection when relevant. Define binning, units, and denominators. Nearly overlapping distributions may support preservation of overall structure; extra objects alone do not establish higher quality.
- **Paired values:** define how entities and observations are matched, what zeros and missing values mean, and which rows are eligible. Use all eligible pairs for a preservation claim. A scatterplot with an identity line and a direct change measure often makes agreement easier to assess than a list of selected extremes. Correlation can supplement this: specify the scale used, and include coverage or exclusions so agreement is not limited silently to survivors.
- **Annotated subsets:** report reference coverage and matching ambiguity before comparing values. Distinguish annotation candidates from confirmed identity. Compare abundance and detection separately when either can change; do not infer eligibility solely from a dataset label or use a few outliers as the whole-subset result.

Select measures for the scientific question; these are alternatives, not a mandatory panel inventory. A summary table can close the workstream by placing the requested costs, coverage, and agreement measures side by side. Keep internal recovery history, file searches, and chat wording out of the presentation. Add next steps only when a real decision remains.

## Focused acceptance check

Before export, verify that a reader with the stated background can explain the baseline, identify each major change, follow one worked example, and read the requested cost and output comparisons. Resolve missing logic in the diagram, visible text, or notes rather than adding repeated caveats. Then apply the shared final-export review and slide–notes–source consistency checks.
