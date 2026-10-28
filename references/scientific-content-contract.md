# Scientific Content Contract

Use this contract to keep scientific planning and visual production consistent, including revisions through an existing project pipeline.

## Planning Records

- Progress Update section: `progress_map.md`.
- Journal Club section: `journal_map.md` (plus `understanding_map.md` when a dialogue/notes file is provided, i.e. Deep-read mode).
- Idea Discussion section: current design and claim–evidence map; unresolved decisions when relevant.
- Every deck, including a mixed deck: one unified production source, conventionally `scientific_handoff.md`.

These names describe information responsibilities, not a requirement to create parallel files. Existing structured slide content, project design records, or equivalent sections can satisfy them. For a local revision, update affected entries and their dependencies rather than recreating the entire planning packet.

For a mixed deck, label each planning-artifact section clearly and merge its claims and slide roster into the single handoff. Do not invent a causal connection between independent sections.

Archetype-specific artifacts are planning worksheets; the designated production source is the canonical content contract. Synthesize by stable claim/figure/asset IDs instead of copying every paragraph. Reconcile disagreements before producing the affected content.

## Idea Review Draft

For a new or substantially restructured Idea argument, provide a readable page-by-page draft in the existing planning source: actual title and visible text, selected panels or passages with placement, full speaker notes, sources, and the page's connection to adjacent pages. Outline labels such as “explain the model” do not substitute for the explanation.

Apply the [task's review agreement](../workflows/idea-discussion.md#task-and-review-agreement). Carry accepted wording and evidence into the production source and verify the match; avoid maintaining divergent editable copies. Planning explanations and open decisions stay separate from audience-facing text. Focused revisions update only affected entries and dependencies.

## `scientific_handoff.md` Schema

```markdown
# Scientific Handoff

## Deck purpose
- Audience:
- Meeting type:
- Decision/learning goal:

## Section routing
| Section | Archetype | Section question | Required outcome |
|---|---|---|---|

## Claim registry
| ID | Claim | Status | Source | Displayed evidence | Analysis unit | Boundary |
|---|---|---|---|---|---|---|

## Slide roster
### Slide N — Audience-readable title
- Archetype:
- Progress evidence profile / current stage profile, when relevant:
- Audience priority / required takeaway, for Progress:
- Slide job:
- Core message or learning takeaway:
- Starting premise and source priority, for Progress when needed:
- Context required:
- Representation/inference lock, for a new analysis: input object / coordinate semantics / transformation or output / allowed inference / forbidden inference:
- Evidence reading contract, for claim-bearing panels: scientific question / exact panel role / visible cue / supported inference / forbidden inference:
- Evidence / asset IDs:
- Computational lock, when relevant — stage input/operation/output; implementation/execution/result; parameter scope; transferable rule/current instance:
- Experimental lock, when relevant — contrast/controls; units and exact n; performed execution; measurement/QC; evidence maturity; choice provenance:
- Reported software version/snapshot, if relevant:
- Formula and scientific/biological role, if any:
- Decision contract, for Idea slides when relevant: analysis unit / input boundary / target / strongest credible alternative / pass-fail comparison / generalization or transfer definition:
- Independent cross-check, when the main readout is indirect or plausibly confounded:
- Claim IDs:
- Material qualification to show or note, if it changes interpretation:
- Speaker-note job:
- Transition to next slide:

## Asset plan
| Asset ID | Type | Source/path | Page/panel or screen state | Direct/crop/redraw/imagegen | Claim supported | Notes |
|---|---|---|---|---|---|---|

## Internal audit concerns, when needed
- Consequential unresolved issue / required check / affected claim:
```

The handoff is authoritative for scientific content. Visual production may improve layout and hierarchy, but must not strengthen claims, change analysis units, merge evidence with proposals, or substitute a source panel without re-auditing the claim. Internal audit concerns guide revision; they are not boilerplate to paste into slides or notes.

For each substantive slide, record its job and core message, source/asset references, and speaker-note job. Inherit common workstream facts through references; add a field or override only when it changes the page's interpretation or production. Omit inapplicable fields rather than filling the whole schema on every slide. Update dependent pages when an inherited fact changes.

Use the representation/inference lock whenever terms such as distribution, state, module, alignment, or trajectory could be ambiguous. Instantiate the term for the actual data object; if it has no operational definition, remove it. A summary curve or score supports only the quantity it computes, not an unmeasured population change or mechanism.

For each evidence panel, record one panel role and the visible cue that supports the claim. Direction, causality, stage localization, or biological identity requires evidence produced for that purpose; a panel's position or visual arrangement does not supply it.

For a Progress workstream, preserve its question and starting premise, authoritative sources, current supported progress, and displayed evidence through references to the workstream record. Record the analysis or measurement object separately from the independent-repeat level when the inference needs it. Keep any material interpretation boundary with the relevant claim. If source review changes these facts, update the affected claims and pages.

Also preserve the automatically inferred evidence profile. A `hybrid` claim must retain the handoff between experimental generation/acquisition and computational processing/analysis; do not let one audited stage stand in for the other.

For a computational Progress workstream, preserve implementation, recorded execution, observed result, and consequential parameter provenance and comparison scope from the computational reference. Production may shorten wording while keeping source-only rules, local checks, and end-to-end comparisons distinguishable.

For an experimental Progress workstream, preserve the scientific contrast, controls, experimental versus nested observational units, exact `n`, actual execution, applicable validity/QC, exclusions or attrition, and evidence maturity. The visible slide may be concise, but it may not convert technical repeats into independent replication, a representative example into prevalence, or a QC-passed run into a confirmed biological result.

When an old deck is supplied as a reference, record whether each reused element is a style/layout reference, an explanatory pattern, or current scientific evidence. Only the last role can support a claim, and only after current-source verification.

## Asset Semantics

- `evidence`: original scientific figure, verified data visualization, or current software screenshot.
- `explanatory`: conceptual schematic, workflow, comparison, or mechanism diagram; redraw or image generation may be used.
- `formula`: mathematical expression used in scientific reasoning.
- `decorative`: minimal and never claim-bearing.

For evidence, identify the exact source and page/panel or software state. For software evidence, record the reported source snapshot, development or release status, exact interface state, and whether the data are real or demonstrative. Apply the shared [screenshot and figure rules](../SKILL.md#literature-screenshots). Routine cropping within an authorized edit needs no separate approval.

Explanatory assets may contain conceptual state diagrams, trajectories, or labeled teaching values when their illustrative role is clear. Generate or redraw these as schematics; preserve quantitative evidence from its original source. Do not fabricate measurements, sample counts, statistical annotations, or realistic assay images that could be mistaken for results. Record prompts and inspect generated labels and arrows against the intended scientific meaning.

For a non-intuitive chart, record the x-axis, y-axis, statistic, analysis unit, and intended reading. For a formula, record every symbol needed on the slide and one plain-language statement of what decision or transformation it performs. If those definitions cannot fit legibly, split the explanation or move the full expression to backup rather than shrinking it.

## Evidence Status

- `established`: directly supported by the user's validated work.
- `source-supported`: directly supported by reported evidence in an external primary source, including the paper under discussion.
- `inference`: interpretation or synthesis not directly tested.
- `proposal`: future design or claim to be tested.

Use these statuses to control wording and notes. Do not place them mechanically on every slide.
