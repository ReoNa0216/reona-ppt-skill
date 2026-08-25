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
- Slide job:
- Single conclusion:
- Starting premise and source priority, for Progress when needed:
- Context required:
- Evidence / asset IDs:
- Software release snapshot, if relevant:
- Formula and biological role, if any:
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

For a Progress workstream, preserve the `progress_map.md` truth lock in the handoff: starting premise, authoritative source order, strongest completed result, displayed evidence, analysis unit, and boundary. If later source review changes any of these, update the map and claim registry before changing the slide story.

## Asset Semantics

- `evidence`: original scientific figure, verified data visualization, or current software screenshot.
- `explanatory`: conceptual schematic, workflow, comparison, or mechanism diagram; redraw or image generation may be used.
- `formula`: mathematical expression used in scientific reasoning.
- `decorative`: minimal and never claim-bearing.

For evidence, identify the exact source and page/panel or software state. For software evidence, also record the official repository reference, release/version, exact interface state, and whether the data are real or demonstrative. A crop is allowed only when approved and when it cannot alter interpretation. AI-generated explanatory assets must never resemble experimental data: do not fabricate axes, sample counts, error bars, microscopy, heatmaps, embeddings, or quantitative plots.

## Evidence Status

- `established`: supported by the user's validated prior work or direct primary evidence central to the deck.
- `source-supported`: supported by an external primary source.
- `inference`: interpretation or synthesis not directly tested.
- `proposal`: future design or claim to be tested.

Use these statuses to control wording and notes. Do not place them mechanically on every slide.
