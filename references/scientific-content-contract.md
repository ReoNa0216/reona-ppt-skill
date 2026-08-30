# Scientific Content Contract

Use this contract after archetype-specific planning and before `ppt-master` visual planning.

## Required Planning Artifacts

- Progress Update section: `progress_map.md`.
- Journal Club section: `journal_map.md` (plus `understanding_map.md` when a dialogue/notes file is provided, i.e. Deep-read mode).
- Idea Discussion section: `design_freeze_draft.md` → `design_freeze.md`, `claim_evidence_map_draft.md` → `claim_evidence_map.md`, and `open_questions.md`.
- Every deck, including a mixed deck: one unified `scientific_handoff.md`.

For a mixed deck, label each planning-artifact section clearly and merge its claims and slide roster into the single handoff. Do not invent a causal connection between independent sections.

Archetype-specific artifacts are planning worksheets; `scientific_handoff.md` is the canonical production contract. Synthesize them by stable claim/figure/asset IDs instead of copying every paragraph into both places. If they disagree, stop and reconcile the planning artifact before handoff rather than maintaining two versions of the claim.

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
- Audience priority / required takeaway, for Progress:
- Slide job:
- Single conclusion:
- Starting premise and source priority, for Progress when needed:
- Context required:
- Evidence / asset IDs:
- Method stage — input / operation / output, for computational Progress when relevant:
- Execution evidence / result artifact, for a claimed completed process when relevant:
- Parameter provenance / evidence class / wording boundary, for an exact decision value when relevant:
- Reusable rule / dataset-specific re-estimation / current instance, when transfer is discussed:
- Software release snapshot, if relevant:
- Formula and scientific/biological role, if any:
- Decision contract, for Idea slides when relevant: analysis unit / input boundary / target / strongest credible alternative / pass-fail comparison / generalization or transfer definition:
- Independent cross-check, when the main readout is indirect or plausibly confounded:
- Claim IDs:
- Boundary to show or note:
- Speaker-note job:
- Transition to next slide:

## Asset plan
| Asset ID | Type | Source/path | Page/panel or screen state | Direct/crop/redraw/imagegen | Claim supported | Notes |
|---|---|---|---|---|---|---|

## Do-not-claim list
- ...
```

The handoff is authoritative for scientific content. `ppt-master` may improve layout and visual hierarchy, but it must not strengthen claims, change analysis units, merge evidence with proposals, or substitute a different source panel without re-auditing the claim registry.

The two conditional Idea fields above are not required on every slide. Use them only where they change the scientific decision; do not create extra planning artifacts or repeat the same contract page by page.

For a Progress workstream, preserve the `progress_map.md` truth lock in the handoff: starting premise, authoritative source order, strongest completed result, displayed evidence, analysis unit, and boundary. If later source review changes any of these, update the map and claim registry before changing the slide story.

For a computational Progress workstream, also preserve the distinction between implementation, recorded execution, and observed result. Exact parameters must retain their evidence class: full rerun comparison, local endpoint comparison, fixed-axis slice, perturbation stability, data-derived, diagnostic/nonbinding, or untested frozen constant. `ppt-master` may shorten the visible wording but may not promote one class into another.

When an old deck is supplied as a reference, record whether each reused element is a style/layout reference, an explanatory pattern, or current scientific evidence. Only the last role can support a claim, and only after current-source verification.

## Asset Semantics

- `evidence`: original scientific figure, verified data visualization, or current software screenshot.
- `explanatory`: conceptual schematic, workflow, comparison, or mechanism diagram; redraw or image generation may be used.
- `formula`: mathematical expression used in scientific reasoning.
- `decorative`: minimal and never claim-bearing.

For evidence, identify the exact source and page/panel or software state. For software evidence, also record the official repository reference, release/version, exact interface state, and whether the data are real or demonstrative. A crop is allowed only when approved and when it cannot alter interpretation. AI-generated explanatory assets must never resemble experimental data: do not fabricate axes, sample counts, error bars, microscopy, heatmaps, embeddings, or quantitative plots.

For a non-intuitive chart, record the x-axis, y-axis, statistic, analysis unit, and intended reading. For a formula, record every symbol needed on the slide and one plain-language statement of what decision or transformation it performs. If those definitions cannot fit legibly, split the explanation or move the full expression to backup rather than shrinking it.

## Evidence Status

- `established`: supported by the user's validated prior work or direct primary evidence central to the deck.
- `source-supported`: supported by an external primary source.
- `inference`: interpretation or synthesis not directly tested.
- `proposal`: future design or claim to be tested.

Use these statuses to control wording and notes. Do not place them mechanically on every slide.
