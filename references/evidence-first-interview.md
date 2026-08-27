# Evidence-first Interview

Use for the **Idea Discussion** `DISCOVERY` state. Principle: **read first, then ask.**

## Principle

Read first, then ask. Before asking anything:

1. Read every user-provided file (papers, Methods, legends, existing design memo, storyboard, asset list).
2. Pre-fill everything the material already supports (problem, evidence, capabilities, boundaries).
3. Ask only questions that genuinely change a decision.

### Never

- Open with a 10–20 item template question list.
- Re-ask what the files already state.
- Ask low-value questions to fill a table.
- Keep probing "for rigor" when there is no decision value (Rule 6).

## High-leverage question

Ask only when an uncertainty would change any of:

- Phase I scientific question
- experimental design
- model architecture
- claim boundary
- success / failure criteria
- roadmap phase gate
- audience / meeting goal

Anything else is recorded as `future option / not required for Phase I`, not a blocker.

## Examples

### Ask

> 一期只需解释已测条件，还是必须同时支持未见干预的泛化？

Because it changes: intervention panel, model representation, benchmark.

### Do not ask

> 是否还要增加一项不影响一期结论的探索性实验？

If the extra experiment is not required for Phase I to stand, record it as:

```text
future option / not required for Phase I
```

and do not block the freeze.

## Questions per round

Default **1–4** per round, highest-leverage only (Rule 5).

## Exit condition

When no decision-changing uncertainty remains, automatically enter `FREEZE_DRAFT`. Do not keep probing in `DISCOVERY`.

## Self-check before asking

A question is invalid if any of these hold:

- the answer is derivable from material already read;
- the answer changes none of the seven high-leverage items;
- it is a template roster ("who is your audience?" unless genuinely missing and it affects claim boundary / meeting goal);
- the round exceeds 4 questions (trim to the highest-leverage).

## Relation to the planning flow

```text
DISCOVERY (read → pre-fill → 1–4 high-leverage questions per round)
    ↓ no decision-changing uncertainty
FREEZE_DRAFT
```
