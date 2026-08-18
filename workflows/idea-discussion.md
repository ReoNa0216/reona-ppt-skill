# Workflow: Idea Discussion

Use for proposed projects, new scientific directions, modeling ideas, experiment design, grant-style internal discussion, or any deck where the core task is to decide whether an idea is scientifically coherent and executable.

## Audience question

> 这个问题值得做吗？我们到底要解释什么？现有证据与能力支持到哪里？方案如何被证伪？一期和长期愿景的边界在哪里？

## Planning artifact 1: `design_freeze.md`

Freeze before slide writing:

1. **Clinical/scientific problem** — one sentence.
2. **Why current approaches are insufficient** — evidence-based gap, not marketing language.
3. **Established biological anchor(s)** — what is already supported experimentally.
4. **Current platform capability** — what can actually be measured now.
5. **Hard technical boundaries** — destructive sampling, annotation uncertainty, sample access, etc.
6. **Phase I scientific question** — the smallest independently valuable question.
7. **Model/experimental hypothesis** — what mechanism or state transition is being learned/tested.
8. **Explicit exclusions** — what Phase I will not claim.
9. **Success criteria** — what would count as a meaningful positive result.
10. **Falsification / failure criteria** — what result would invalidate the proposed approach.
11. **Phase II gate** — what new data/evidence is required before expanding scope.

Do not begin slide planning until the user-provided authoritative design memo, storyboard, and asset list have been reconciled when such materials exist. Preserve their declared priority order.

## Planning artifact 2: `claim_evidence_map.md`

For every major claim:

`claim → status → source → displayed evidence → analysis unit → boundary → falsifier`

Allowed status values:

- **established** — directly supported by the user's prior work or strong primary evidence;
- **source-supported** — supported by external primary literature;
- **inference** — reasonable synthesis from evidence but not directly tested;
- **proposal** — future design/claim to be tested.

Never present an inference or proposal as established fact.

## Narrative grammar

Default argument chain:

`clinical/scientific problem → biological anchor → unresolved dynamic/mechanistic gap → why current measurement is insufficient → what the platform can observe → mathematical/experimental problem definition → modeling principle → validation plan → claim boundary → phased roadmap`

The deck should feel like an argument, not a list of technologies.

## Model and formula slides

- A formula belongs in the main deck only if it clarifies the model's scientific role.
- Pair every main formula with a plain-language biological interpretation.
- Show model hierarchy and assumptions visually; move derivations and full objectives to backup slides.
- Do not claim unseen-perturbation generalization unless perturbation diversity and representation actually support that claim.
- Do not turn a named model family, mathematical complexity, or “AI” label into the scientific contribution; the contribution must be the biological question it makes testable.

## Asset rule

Classify every visual as:

- **Evidence** — original paper/user data figure or verified software screenshot; never AI-generated.
- **Explanatory schematic** — redraw or image generation allowed; must be labeled as conceptual when necessary.
- **Formula/model** — render faithfully; no decorative pseudo-math.

## Closing rule

End with a **phased evidence-gated roadmap**, not a grand universal vision. Later stages should be explicitly conditional on Phase I success.
