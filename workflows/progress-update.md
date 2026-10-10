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
| Evidence profile | computational / experimental / hybrid / general, plus one-sentence dependency rationale |
| Audience priority | primary / secondary / backup, plus the one takeaway the audience must retain |
| Audience starting point | When explanation is needed, infer existing knowledge and prerequisites to teach from the user's brief |
| Starting premise | The observation, prior result, operational friction, or preset hypothesis that started the workstream |
| Scientific/operational question | What this workstream is trying to establish or remove |
| Authoritative source order | Which current sources govern the premise, methods, result, release state, and limitations |
| Since last report | What materially changed |
| Strongest completed result | The most decision-relevant result already supported by the work |
| Displayed evidence | The figure, table, or screenshot that most directly supports that result |
| Analysis / experimental unit | The independent level that supports the stated inference |
| Boundary | What the result does not establish |
| Status | completed / ongoing / blocked / validation needed |
| PI decision needed | include only when a real decision exists; otherwise omit |

## Workstream truth lock

Complete `Starting premise`, `Authoritative source order`, `Strongest completed result`, and `Displayed evidence` before choosing slide titles or layouts.

- Treat folders, repository names, old slide decks, and internal labels as locators, not as audience-facing descriptions or scientific premises.
- Read enough of the authoritative project sources to distinguish the original question, the preset expectation or candidate definition, the strongest completed result, and the main limitation.
- Do not select the most visually convenient figure and then reverse-engineer the workstream conclusion from it. The displayed evidence must answer the actual workstream question.
- Lead with the strongest defensible achievement. Keep a necessary limitation close to the result, but do not let a catalogue of caveats obscure what was completed.
- Assign `primary / secondary / backup` before storyboarding. Give explanation depth to the user's priorities; do not let adjacent completed work consume equal space merely because it exists.
- Map the user's requested questions to the slide roster and note jobs before production. Check coverage there rather than adding a separate requirements document. Infer audience needs from the brief; ask only when a missing fact would change the explanation or comparison.
- Treat an old deck as a style/teaching reference unless its scientific claims are reverified against current sources.

## Workstream evidence-profile router

After inspecting the current sources and before detailed storyboarding, classify every Progress workstream. The user does not need to choose a route.

| Profile | Dependency test | Conditional reference |
|---|---|---|
| `computational` | The claim depends on code, data transformation, an algorithm, a model, a parameterized analysis, or a software state. | Read [progress-computational-evidence.md](../references/progress-computational-evidence.md). |
| `experimental` | The claim depends on physical manipulation, preparation, treatment, acquisition, or measurement of a biological, chemical, or material system. | Read [progress-wet-lab-evidence.md](../references/progress-wet-lab-evidence.md). |
| `hybrid` | The same claim requires both experimental generation/acquisition and computational processing/analysis to be correct. | Read both references and assign a profile to each stage. |
| `general` | The update is status, coordination, or another completed output whose claim needs neither method-specific evidence lock. | Use only the common truth lock. |

Use claim dependency, not keywords or scientific subject matter:

1. Would the claim fail if the inspected code, run record, version, or computational decision were wrong? If yes, enable the computational profile.
2. Would the claim fail if sample identity, physical execution, controls, independence, measurement validity, or experimental QC were wrong? If yes, enable the experimental profile.
3. If both answers are yes for one claim, use `hybrid` and preserve the handoff between the stages.

A biological matrix analyzed from a frozen input can be purely computational. A high-throughput workstream that prepares specimens, acquires data, and runs a custom pipeline is usually hybrid. A software interface is computational unless the claim also concerns physical assay performance. A mixed deck has no single global profile: route each workstream, and route each stage of a hybrid workstream.

Routine instrument acquisition, file export, or standard plotting does not by itself make a wet-lab workstream hybrid. Enable the computational lock only when a processing/version/parameter decision materially supports the conclusion or is itself part of the reported progress.

If sources are incomplete, mark the profile or stage `provisional`, inspect the available protocols, records, raw artifacts, code, logs, and results, and retain any unresolved dependency as a boundary. Ask the user only when the unresolved route would materially change the claim or required evidence and cannot be determined from the supplied workspace.

## Narrative grammar

Default order:

`starting premise / workstream question → strongest completed result → displayed evidence → conclusion boundary → status`

Let audience priority and conceptual dependency determine slide count. Compress repeated evidence, not missing logic. Workflow detail belongs where it is required to understand the result, reproduce the claim boundary, or distinguish a full comparison from a local diagnostic.

When the audience needs to understand a method or judge a method change, read [progress-method-teaching.md](../references/progress-method-teaching.md). It adds audience-level examples, purposeful schematics and notes, and comparison guidance within the selected evidence profile. Use the explanation depth and comparison dimensions the user requested.

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

For a computational method screenshot or schematic, apply the same evidence discipline as software: every visible state, field, control, and workflow claim must be present in the inspected version or verified by its authoritative contract. Do not fill an explanatory gap with a plausible interface behavior.

## Closing rule

End with **completed, verifiable outputs**. Add blockers, decisions, or next actions only when they are genuinely discussion-worthy; never add a generic “next step” page for symmetry.

## Storyboard minimum

Each slide entry in `scientific_handoff.md` must contain:

- evidence profile and, for a hybrid workstream, the profile of the current stage;
- audience priority and required takeaway;
- starting premise and authoritative source priority when needed to interpret the result;
- slide job, single conclusion or learning takeaway, displayed evidence, supporting unit, boundary, status, and speaker-note job;
- only the decision-bearing fields required by the selected computational or experimental reference;
- software release snapshot when relevant.

Before handoff, run an audience-language pass on the slide roster: expand abbreviations at first use, keep quantities in Arabic numerals, replace internal labels with audience-readable terms, and ensure no title depends on an unexplained method name or metric.
