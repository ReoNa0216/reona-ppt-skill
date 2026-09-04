# Workflow: Idea Discussion

Use for proposed projects, new scientific directions, modeling ideas, experiment design, grant-style internal discussion, or any deck where the core task is to decide whether an idea is scientifically coherent and executable.

## Default behavior: interactive planning-only

A section routed to Idea Discussion is planning-only by default. Without an approved Design Freeze, do not hand off to `ppt-master`, do not generate the PPT, and do not write the final storyboard.

Planning follows this one-way flow:

```text
DISCOVERY → FREEZE_DRAFT → USER_REVIEW → APPROVED_FREEZE → handoff → ppt-master
```

`USER_REVIEW` is a **hard stop**: show the Freeze Draft summary, list frozen vs not-yet-frozen items, ask only high-leverage unresolved questions, then wait for approval. `USER_REVIEW → ppt-master` is never allowed.

### Two ways to skip the default

**Case A — an approved freeze is already provided.** Recognize keywords such as `approved / final / frozen / 已确认 / 已冻结 / 可以按此制作`.

**Case B — the user explicitly skips confirmation.** For example: *不要问我，直接按最佳判断制作。* Even then, generate the Design Freeze internally and treat it as auto-approved.

### Mixed-deck rule

In a mixed deck, deck-level production waits until **every** Idea section has an approved freeze. Other sections may finish their own planning; no final deck is produced while any Idea section is unapproved.

## DISCOVERY: evidence-first interview

Entering `DISCOVERY`, follow `references/evidence-first-interview.md`: **read first, then ask.**

- Read every user file and pre-fill what the material already supports.
- Ask only 1–4 high-leverage questions per round.
- With no decision-changing uncertainty, auto-enter `FREEZE_DRAFT`; do not keep probing.

## Audience question

> 这个问题值得做吗？我们到底要解释什么？现有证据与能力支持到哪里？方案如何被证伪？一期和长期愿景的边界在哪里？

## Planning artifact 1: `design_freeze_draft.md` → `design_freeze.md`

Produce `design_freeze_draft.md` in `FREEZE_DRAFT`; rename to `design_freeze.md` on approval. Thirteen items:

1. **Clinical/scientific problem** — one sentence.
2. **Why current approaches are insufficient** — evidence-based gap, not marketing language; name the strongest credible simpler or lower-cost alternative.
3. **Established evidence** — what is already supported experimentally (status: `established` / `source-supported`).
4. **Inferences** — reasonable synthesis from evidence, not directly tested (status: `inference`).
5. **Current platform capability** — what can actually be measured now.
6. **Hard technical boundaries** — destructive sampling, annotation uncertainty, sample access, and, when relevant, confounding in an indirect readout plus an independent cross-check.
7. **Phase I scientific question** — the smallest independently valuable question; freeze the analysis unit, input boundary, and experimental or prediction target before choosing a model.
8. **Model/experimental hypothesis** — what mechanism or state transition is being learned/tested.
9. **Explicit exclusions** — what Phase I will not claim.
10. **Success criteria** — what would count as a meaningful positive result, including comparison with the simplest and strongest credible alternative when a costly modality or complex model is proposed.
11. **Falsification / failure criteria** — what result would invalidate the proposed approach; failure to outperform the credible alternative limits the necessity claim even when the new modality is informative.
12. **Phase II gate** — what new data/evidence is required before expanding scope; if generalization or transfer is proposed, define the held-out unit, grouping rule, allowed calibration, and claim boundary.
13. **Open questions** — remaining high-leverage questions (also written to `open_questions.md`).

Do not begin slide planning until the user-provided authoritative design memo, storyboard, and asset list have been reconciled when such materials exist. Preserve their declared priority order.

## Planning artifact 2: `claim_evidence_map_draft.md` → `claim_evidence_map.md`

Produce the draft in `FREEZE_DRAFT`; rename on approval.

For every major claim:

`claim → status → source → displayed evidence → analysis unit → boundary → falsifier`

Allowed status values:

- **established** — directly supported by the user's prior work or strong primary evidence;
- **source-supported** — supported by external primary literature;
- **inference** — reasonable synthesis from evidence but not directly tested;
- **proposal** — future design/claim to be tested.

Never present an inference or proposal as established fact.

## Validity–novelty gate

When a new modality, resolution, or analysis reproduces an established result, treat that concordance as a validity anchor, not the novelty claim. Before slide planning, name the additional information unavailable to the established approach and identify the evidence or analysis that reveals it. If no such increment is supported, narrow the contribution instead of presenting replication as discovery.

## Narrative grammar

Default argument chain:

`clinical/scientific problem → biological anchor → unresolved dynamic/mechanistic gap → why current measurement is insufficient → what the platform can observe → mathematical/experimental problem definition → modeling principle → validation plan → claim boundary → phased roadmap`

The deck should feel like an argument, not a list of technologies.

Before introducing a named method, teach the audience what the data object is, what scientifically relevant information a simpler summary loses, and what representation or model must preserve. Then present candidate methods and selection criteria. Do not make the audience learn an external model before they can understand the scientific job it is meant to perform.

Planning questions are reasoning aids, not a fixed slide template. Split at scientific decision boundaries: when one page would require the audience to interpret an observation, use it to choose an intervention or design, and then read a different validation output, separate the observation/localization from the decision/intervention/readout.

## Model and formula slides

- A formula belongs in the main deck only if it clarifies the model's scientific role.
- Pair every main formula with a plain-language biological interpretation.
- Show model hierarchy and assumptions visually; move derivations and full objectives to backup slides.
- Do not claim generalization unless the evidence supports it. Define what is held out and how it is grouped, distinguish within-domain generalization from cross-scenario transfer, and state whether the new setting requires calibration.
- Do not turn a named model family, mathematical complexity, or "AI" label into the scientific contribution; the contribution must be the biological question it makes testable.
- Do not preselect a named method as the winner when method choice is unresolved; compare plausible candidates by stability, held-out performance, interpretability, and the scientific information they preserve.

## Asset rule

Classify every visual as:

- **Evidence** — original paper/user data figure or verified software screenshot; never AI-generated.
- **Explanatory schematic** — redraw or image generation allowed; must be labeled as conceptual when necessary.
- **Formula/model** — render faithfully; no decorative pseudo-math.

## Closing rule

End with a **phased evidence-gated roadmap**, not a grand universal vision. Later stages should be explicitly conditional on Phase I success.

## After approval

Once `APPROVED_FREEZE`, produce `scientific_handoff.md` (per `references/scientific-content-contract.md`) and hand off to `ppt-master`. Visual review and export belong to `ppt-master`; the ReoNa-specific final checks are in the SKILL.md "Handoff And Final Review" section.
