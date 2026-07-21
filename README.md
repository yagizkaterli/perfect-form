# perfect-form

A tiny [Claude Code skill](https://docs.anthropic.com) for **long autonomous sessions**:
work continues to exhaustion, but never at the cost of form. When form breaks, the set
ends and the weight goes back on the rack — a clean handover — instead of cheat reps that
get repaid later as repair debt.

Borrowed from strength training: you do reps with perfect form until you cannot do another
one with perfect form, and then you stop. Extra reps bought by breaking form do not extend
the set. They produce injury.

## What you get

- **A six-point form check** the assistant runs at every "let me squeeze in one more pass"
  — verified · receipted · logged · legible outside · fail-closed · routed.
- **Mechanical degradation signals** that fire before self-assessment does — skipped log,
  bare commit, decision from memory, *same error class twice*, operator correcting you
  twice in one stretch.
- **An end-of-set protocol** (rack the weight): systems left consistent, in-flight work
  inventoried, decisions surfaced, handover written, work persisted, log closed, and the
  next session's first move already written.
- **The repair rule:** where form broke, do not add load — **add mechanism.** A rule with
  no enforcement is the first thing speed removes.

## Why it exists

Long sessions rarely fail by stopping too early. They fail by continuing with degraded
form: the log postponed, the commit body dropped, the claim asserted from memory, the
uncertain path taken because stopping felt expensive. Output keeps flowing, so nothing
looks broken — until someone outside notices that the last three hours produced work
nobody can verify.

This skill was written after a long session in which discipline broke five separate times,
and **every break was caught by the human operator rather than by the system.** Each one
was the same class: a rule that existed with nothing enforcing it. The skill is the
generalization of that measurement.

## What a run looks like

Six hours into an autonomous session, the assistant is about to start another task block:

> **form check** — logged: no (two blocks unrecorded). legible outside: no (last three
> commits went out with bare subjects). verified: yes. receipted: yes. fail-closed: yes.
> routed: yes.
> **two failures → the set is over.**
>
> **racking:** background job finished and its output filed · one agent still running,
> noted with where its report lands · two decisions needing the human moved to the surface
> they actually read · handover written (state, ordered next actions, open debts) ·
> committed and pushed · log closed · next session's first move: "accept the pending
> report, then repair the trace writer".
>
> Repair note: commit bodies dropped twice under speed — that is structure, not willpower.
> Added a commit-msg hook that rejects body-less commits.

## Install

```
npx skills add <this-repo>/perfect-form
```

Or copy `SKILL.md` into `.claude/skills/perfect-form/`.

## Not this

Not a productivity booster, and not a stop-early rule. Faking exhaustion while real work
remains is just quitting; the skill protects the quality of the **last** rep, not the count.
