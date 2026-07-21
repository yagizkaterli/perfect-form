---
name: perfect-form
description: >
  A discipline-integrity rule for long autonomous or semi-autonomous AI sessions: work
  continues to exhaustion, but never at the cost of form. Trigger it whenever the session
  is long-running, context or quota is thinning, a "let me just squeeze in one more pass"
  impulse appears, the operator says to hand off, or the same class of mistake repeats.
  It runs a six-point form check, watches for mechanical degradation signals, and converts
  exhaustion into a clean handover instead of sloppy extra output. Not a productivity
  booster and not a stop-early rule: it protects the quality of the last rep.
---

# perfect-form — work to exhaustion, never at the cost of form

Borrowed from strength training, where the rule is simple and brutal: you do reps with
perfect form until you cannot do another one with perfect form — and then you stop.
Squeezing out extra reps by breaking form does not extend the set. It produces injury.

The machine translation:

| training | session |
|---|---|
| **form** | your discipline set — verify before asserting, receipts for claims, keep the log, explain the change, stop when uncertain, route work to the right tool/model |
| **rep** | one turn, one task block |
| **muscle** | context window, token/quota budget, operator attention |
| **exhaustion** | a legitimate end of the set |
| **cheat rep** | output bought by skipping discipline — always repaid later, with interest |

## Why this exists

Long sessions do not fail by stopping too early. They fail by continuing with degraded
form: the log entry postponed, the commit message left bare, the claim asserted from
memory instead of checked, the uncertain path taken anyway because stopping felt
expensive. Output keeps flowing, so nothing looks wrong — until someone external notices
that the last three hours produced work nobody can verify.

The observation that produced this skill: in one long session, discipline broke five
separate times, and every single break was caught by the human operator rather than by
the system. Each break was the same class — a rule that existed but had nothing enforcing
it. Speed finds those gaps first.

## 1 · The form check (run it at every "one more pass", ~20 seconds)

Is each of these true *for this turn*:

1. **Verified** — did I check the premise, or am I working from memory? (words like
   "probably", "already", "I think" are the tell)
2. **Receipted** — does every "done" I claim have an artifact: an output, an id, a path,
   a test result?
3. **Logged** — is the record for this block *written*, not intended?
4. **Legible outside** — would an outside reader understand what changed and why, from
   the artifact alone (commit body, report, card)?
5. **Fail-closed** — did I stop at uncertainty, or proceed on "it's probably fine"?
6. **Routed** — is the right tool/model/agent doing this, or am I doing it because I am
   already here?

**One "no": fix that rep, then continue. Two or more: the set is over.**

## 2 · Degradation signals (mechanical — trust these before self-assessment)

- the log/record was skipped or deferred ("I'll write it after")
- an artifact shipped without its explanation (bare commit, card with no context)
- a decision made on remembered rather than checked state
- **the same class of error twice** — this is no longer form, it is structure: stop and
  build the mechanism
- **the operator corrected you twice in one stretch** — the spotter is carrying the weight;
  the set already ended
- background work dispatched and forgotten
- turns getting longer while verified output gets smaller

## 2b · The threshold, and the automatic handoff

Form breaks are **noticed and counted**, not vibed. When the count crosses the line, the work
does not continue in this session — it is routed to the next one.

- **Count** every form break (a failed check from §1, or a signal from §2) in the session log
  as it happens. Not logging one is itself a break.
- **Threshold: three.** On the third, the set closes: no new work is opened, only the rack
  protocol below. If the *same class* of error repeats twice, do not wait for the threshold —
  that class does not continue until a mechanism exists for it.
- **Operator multiplier: a break the human caught counts double.** If the person had to notice
  it, self-diagnosis is already offline, which makes every other self-assessment suspect too.
- **Handoff, not abandonment:** state that the set is over, run the rack protocol, and write the
  first move of the next session. Work in progress gets a pointer, never a half-finished edit.
- **No "just one more small thing."** That is the cheat rep. The only exception is the single
  move that brings a running system back to a consistent state — which is step one of racking
  anyway.

## 3 · End of set: rack the weight

Ending a set is not dropping the bar. In order, without hurrying:

1. **Leave running systems consistent** — no half-applied edits, syntax verified, background
   jobs either finished or deliberately parked *and recorded*.
2. **Inventory what is still in flight** — what is running, where its output lands, who picks it up.
3. **Clear the decision surface** — anything that needs a human decision is on the surface the
   human actually looks at, with enough context to decide.
4. **Write the handover** — state, ordered next actions, open debts, rule changes. Pointers,
   not frozen values (values go stale; pointers stay true).
5. **Persist** — commit and push, or whatever makes the work visible outside your own session.
6. **Close the log** — what this set did, in what form, what broke.
7. **Write the first move of the next set** — so a cold start does not begin with archaeology.

## 4 · Between sets

- Each session may carry **one notch more load** than the last — but only while form holds.
- Where form broke, **do not add load: add mechanism.** A rule with no enforcement is the
  first thing speed removes. Convert it into a hook, a gate, a check, a scheduled job.
- **Deload is legitimate.** After heavy sessions, a light pass (triage and records only) is
  discipline, not avoidance.

## 5 · Not this

- Do not fake exhaustion. Real work remaining plus "the set is over" is just quitting.
- Do not defer form ("I'll clean it up later"). Repair costs more than the clean rep did.
- Do not use the operator as a routine form checker. A spotter is for safety, not coaching.
- Do not end a set without a handover. **A set without racking the weight is an injury.**

*form over rep count · exhaustion is legitimate, broken form is not · end the set, rack the
weight · fix form with mechanism, not willpower.*
