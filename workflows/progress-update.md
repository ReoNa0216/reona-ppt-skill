# Workflow: Progress Update

Use for lab-meeting recent-work reports, project updates, analysis status, software/tool development, and completed-output summaries.

## Audience question

> 最近做了什么？最强证据是什么？结果可信到什么程度？哪些已经完成，哪些仍然需要判断或决策？

Do **not** force independent workstreams into one causal scientific story.

## Planning artifact: `progress_map.md`

For each workstream record:

| Field | Required content |
|---|---|
| Workstream | Audience-readable name, not folder/module name |
| Scientific/operational question | What this workstream is trying to establish or remove |
| Since last report | What materially changed |
| Strongest evidence | The figure/table/screenshot worth showing |
| Analysis unit | cell / patient / event / project / software release etc. |
| Result | One direct statement |
| Boundary | What the result does not establish |
| Status | completed / ongoing / blocked / validation needed |
| PI decision needed | include only when a real decision exists; otherwise omit |

## Narrative grammar

Default order:

`workstream question → strongest result/evidence → conclusion boundary → status`

Use 1–2 slides per important workstream. Workflow/process detail belongs only where it is required to interpret the result.

Name each workstream by the audience-facing achievement or question, not by its directory, repository, package, or internal acronym. Independent workstreams may remain independent; use a brief transition instead of inventing a causal progression.

For software, use:

`user friction → one concrete review flow → evidence that the interface removes the friction → save/handoff behavior`

Do not lead with implementation facts, file formats, test counts, or internal module names.

The interface state shown must support the claimed convenience. If a capability cannot be demonstrated by the screenshot, verify it from the current release/source contract in the notes or remove the claim.

## Closing rule

End with **completed, verifiable outputs**. Add blockers, decisions, or next actions only when they are genuinely discussion-worthy; never add a generic “next step” page for symmetry.

## Storyboard minimum

Each slide entry in `scientific_handoff.md` must contain:

- slide job;
- single result/conclusion;
- displayed evidence;
- analysis unit;
- conclusion boundary;
- status if relevant;
- speaker-note job.
