# Idea Iteration Maintenance Scenarios

These generic scenarios were reviewed after the workflow edits to check internal consistency and intent preservation. This is a same-agent desk review, not an independent behavioral test. No slide-generation or scientific-performance score is assigned.

| Scenario | Decision reached in review | Rationale |
|---|---|---|
| A user asks to compare two research directions before making slides. | Present evidence, feasible alternatives, and a recommendation; remain in discussion. | Discussion-only intent controls production. |
| The user accepts the design and asks to make the deck; no formal approval keyword is used. | Produce within the accepted scope using the existing content source. | An ordinary production request supplies authorization. |
| A user revises one analysis page in an accepted mixed deck. | Reopen the changed analysis and update its dependent figure, notes, and references; retain other accepted content. | Revision scope follows scientific dependencies. |
| A field study adds both a new sensor and a new sampling regime, each with uncertain value. | Identify what each contributes, propose informative preliminary comparisons, and map outcomes to retained scope. | Preliminary evidence should choose the design; maximum complexity is not the default. |
| A proposed forecasting extension has equations and suitable planned data but no implementation. | Explain the extension as a proposal with assumptions and a held-out test; do not describe it as completed. | Feasibility and implementation status are separate questions. |
| A model predicts site-level mean yield from repeated within-site readings; a draft claims accurate within-site heterogeneity. | Evaluate mean predictions at the site level, define aggregation and error scale, and remove the unsupported heterogeneity claim. | Metrics and claims follow the predicted object and independent unit. |
| A temporal benchmark trains on endpoint observations, holds out interior observations, and tunes preprocessing on the entire series. | Treat the intended task as interpolation and exclude held-out targets from learned preprocessing and selection, or explicitly redefine the information available. | A task definition includes preprocessing and target access. |
| A published figure crop omits the second line of a group label, changing the apparent treatment. | Restore the full label from the original source and check the claim and notes. | Cropping must preserve the experiment's meaning. |
| A schematic's repeated icons could mean separate groups or successive stages; notes add several paragraphs saying what is not claimed. | Establish the intended relationship, repair arrows and labels, and replace defensive notes with the actual operation and readout. | Visual ambiguity is a design problem to resolve. |
| The user requests a concise derivative of an accepted deck and deletion of old generated versions. | Inherit the reference style, select content for the new meeting decision, protect the baseline, verify the final export, then remove only authorized generated duplicates. | Preserve sources and deliver the requested canonical artifact. |

The review also checked three counterexamples: a straightforward figure revision needs no pilot or prediction reference; a distribution-producing model may appropriately use distributional metrics; and removing repetitive caveats must retain a qualification that changes the interpretation of an experimental result.

The existing Progress workflow and its computational and experimental evidence references were left unchanged. Journal Club retains the paper/dialogue evidence hierarchy, panel identity, exact statistics, and analysis units; its conclusion wording now requests material qualifications rather than a mandatory negative statement on every figure.
