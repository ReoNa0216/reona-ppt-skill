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
| Starting premise | The observation, prior result, operational friction, or preset hypothesis that started the workstream |
| Scientific/operational question | What this workstream is trying to establish or remove |
| Authoritative source order | Which current sources govern the premise, methods, result, release state, and limitations |
| Since last report | What materially changed |
| Strongest completed result | The most decision-relevant result already supported by the work |
| Displayed evidence | The figure, table, or screenshot that most directly supports that result |
| Analysis unit | cell / patient / event / project / software release etc. |
| Boundary | What the result does not establish |
| Status | completed / ongoing / blocked / validation needed |
| PI decision needed | include only when a real decision exists; otherwise omit |

## Workstream truth lock

Complete `Starting premise`, `Authoritative source order`, `Strongest completed result`, and `Displayed evidence` before choosing slide titles or layouts.

- Treat folders, repository names, old slide decks, and internal labels as locators, not as audience-facing descriptions or scientific premises.
- Read enough of the authoritative project sources to distinguish the original question, the preset expectation or candidate definition, the strongest completed result, and the main limitation.
- Do not select the most visually convenient figure and then reverse-engineer the workstream conclusion from it. The displayed evidence must answer the actual workstream question.
- Lead with the strongest defensible achievement. Keep a necessary limitation close to the result, but do not let a catalogue of caveats obscure what was completed.

## Narrative grammar

Default order:

`starting premise / workstream question → strongest completed result → displayed evidence → conclusion boundary → status`

Use 1–2 slides per important workstream. Workflow/process detail belongs only where it is required to interpret the result.

Name each workstream by the audience-facing achievement or question, not by its directory, repository, package, or internal acronym. Independent workstreams may remain independent; use a brief transition instead of inventing a causal progression.

When a workstream begins with an internal discovery or preset candidate definition and then tests it in external data, use this optional validation grammar:

`internal discovery or preset premise → candidate-definition lock → role of each external dataset → primary-unit result → independent-unit result → boundary`

Use only the stages that exist. Do not imply that a localization dataset supports longitudinal comparison, or that a cell-level result has been independently validated at the patient, sample, or replicate level.

For software, use:

`user friction → one concrete review flow → evidence that the interface removes the friction → save/handoff behavior`

Do not lead with implementation facts, file formats, test counts, or internal module names.

The interface state shown must support the claimed convenience. If a capability cannot be demonstrated by the screenshot, verify it from the current release/source contract in the notes or remove the claim.

Before handoff, freeze one software release snapshot inside `progress_map.md` or the source manifest:

- official repository and branch/tag/commit;
- release maturity and displayed version;
- exact screenshot version and interface state;
- whether the screen uses real, demo, fixture, or synthetic data.

The slide, screenshot label, notes, and source manifest must use the same snapshot. An older interface image may be retained only when explicitly approved and must not serve as evidence for a newer interaction. Field counts, schema widths, test counts, and internal state names belong on the slide only when they materially explain the user task or output semantics.

## Closing rule

End with **completed, verifiable outputs**. Add blockers, decisions, or next actions only when they are genuinely discussion-worthy; never add a generic “next step” page for symmetry.

## Storyboard minimum

Each slide entry in `scientific_handoff.md` must contain:

- starting premise and authoritative source priority when needed to interpret the result;
- slide job;
- single result/conclusion;
- displayed evidence;
- analysis unit;
- conclusion boundary;
- status if relevant;
- software release snapshot when relevant;
- speaker-note job.
