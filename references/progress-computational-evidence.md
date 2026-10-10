# Progress Computational Evidence

Read this reference for a `computational` Progress workstream and for every computational stage of a `hybrid` workstream. The reported claim must depend on code, data processing, an algorithm, or a software state.

## Process execution evidence

Use existing source and run records to connect each claim-bearing stage to the relevant evidence:

| Field | Content |
|---|---|
| Audience object | What enters this stage, in audience-readable language |
| Implemented operation | What the inspected source or contract implements |
| Execution evidence | Recorded execution and configuration, or its known absence when relevant |
| Result artifact | Observed output when execution is being reported |
| Supported claim | What the available records establish at the implementation, execution, or result stage |

Code presence, recorded execution, and result evidence are three different facts. A method found only in source is implementation-only; do not describe it as part of a completed run. If current source differs from the executed snapshot, identify which behavior the run artifacts establish and which is only current implementation.

## Parameter provenance and comparison scope

For a parameter or decision rule needed to interpret the presentation, record its role, value or formula, and source or derivation. Reuse the process execution record: a rule may be implemented without having run, or run without a direct alternative comparison. State those facts when they affect the claim.

For an actual comparison or diagnostic, record what varied, what stayed fixed, which affected stages reran, and which result was evaluated. Describe the coverage in ordinary language. For example, changing a threshold on a frozen result establishes a local comparison; a full-pipeline comparison reruns every stage the change can affect. Deleting observations from a frozen output and refitting after deletion test different properties.

Parameter origin and validation scope are separate facts: a data-derived value can also have been compared against alternatives. They need no single category label. Use “optimized,” “blind-selected,” “preregistered,” “validated,” or “generalizable” only when the source and actual comparison support that word. A local diagnostic should retain its specific scope when discussed as sensitivity or stability evidence.

When discussing transfer, distinguish the reusable rule, any quantity that must be re-estimated for new data, and the current numerical instance. Keep illustrative values separate from evidence used to choose parameters.

## Computational explanation

For a method-heavy workstream, use [progress-method-teaching.md](progress-method-teaching.md) for prerequisite order, complete examples, schematics, and notes. Keep each stage's scientific input, operation, output, and downstream use identifiable. Define how consequential groups, folds, ranges, or held-out sets are constructed. Show the general rule before its current numerical instance, and retain the implementation or execution status of the stage being explained.
