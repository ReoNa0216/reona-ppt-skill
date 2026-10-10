# Workflow: Progress Update

Use for lab-meeting recent-work reports, project updates, analysis status, software/tool development, and completed-output summaries.

## Audience question

> 最近做了什么？最强证据是什么？结果可信到什么程度？哪些已经完成，哪些仍然需要判断或决策？

Do **not** force independent workstreams into one causal scientific story.

## Planning artifact: `progress_map.md`

Record workstream facts once in `progress_map.md` or the existing production source. Use the relevant fields below; pages inherit them by reference.

| Field | Content |
|---|---|
| Workstream and priority | Audience-readable question or achievement; primary / secondary / backup when allocating space across workstreams |
| Evidence profile | computational / experimental / hybrid / general, plus one-sentence dependency rationale |
| Audience question and starting point | What the user wants answered; existing knowledge and prerequisites to teach when explanation is needed |
| Starting premise | The observation, prior result, operational friction, or preset hypothesis that started the workstream |
| Authoritative sources | Which sources govern the premise, method, reported version, and current findings |
| Current progress and status | What changed or was learned, including supported findings, implemented capabilities, or documented blockers |
| Displayed support | The source or artifact supporting that progress; distinguish explanatory illustrations from result evidence |
| Analysis or measurement object | What is computed, observed, or displayed; record the independent-repeat level separately when the inference needs it |
| Interpretation boundary | Include when it changes the meaning of a claim |
| Discussion or decision | Include when a real unresolved choice or blocker needs discussion |

## Workstream truth lock

Establish the question and starting premise, identify the authoritative sources, and select the most informative supported progress before choosing titles or layouts.

- Treat folders, repository names, old slide decks, and internal labels as locators, not as audience-facing descriptions or scientific premises.
- Read enough of the authoritative project sources to distinguish the original question, preset expectation or candidate definition, current findings, and material unresolved issues.
- Do not select the most visually convenient figure and then reverse-engineer the workstream conclusion from it. The displayed evidence must answer the actual workstream question.
- Lead with the most informative supported progress. Keep a necessary qualification close to the finding; an unfinished investigation or documented failure can be the central progress to discuss.
- Map the user's requested questions to the slide roster and note jobs before production. Check coverage there rather than adding a separate requirements document. Infer audience needs from the brief; ask only when a missing fact would change the explanation or comparison.

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

`starting premise / workstream question → current progress → supporting evidence → interpretation / status`

Allocate space by the user's priorities, presentation time, and conceptual dependencies. Adjacent work need not receive equal space. Compress repeated evidence, not missing logic; move secondary detail to notes or backup when needed. Workflow detail belongs where it helps the audience understand the reported progress or comparison.

When the audience needs to understand a method or judge a method change, read [progress-method-teaching.md](../references/progress-method-teaching.md). It adds audience-level examples, purposeful schematics and notes, and comparison guidance within the selected evidence profile. Use the explanation depth and comparison dimensions the user requested.

When a workstream begins with an internal discovery or preset candidate definition and then tests it in external data, use this optional validation grammar:

`internal discovery or preset premise → candidate-definition lock → role of each external dataset → primary-unit result → independent-unit result → boundary`

Use only the stages that exist. Do not imply that a localization dataset supports longitudinal comparison, or that a cell-level result has been independently validated at the patient, sample, or replicate level.

For software progress, ground the user-task narrative in one reported snapshot, recorded in the workstream or source manifest:

- source repository or local checkout and branch/tag/commit;
- development or release status and displayed version;
- exact screenshot version and interface state;
- whether the screen uses real, demo, fixture, or synthetic data.

Keep each behavior claim, screenshot, note, and source reference on the matching snapshot. A screenshot from another version can illustrate that version with its identity and role clear; it does not establish a different version's behavior.

## Closing rule

Close on the current supported progress and its significance. Include a blocker, decision, or next action when it advances the discussion; never add a generic “next step” page for symmetry.

## Storyboard minimum

Use the shared handoff schema: a substantive page needs its job and core message, source/asset references, and speaker-note job. Inherit common profile, audience, provenance, and status from its workstream. Add stage-specific evidence, units, qualifications, or version differences only where they affect interpretation. A hybrid page retains the profile of the stage it describes.

Before handoff, check requested-question coverage and whether titles and explanations are understandable from the audience's stated starting point.
