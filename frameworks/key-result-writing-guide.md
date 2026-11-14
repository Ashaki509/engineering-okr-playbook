# Key Result Writing Guide

A Key Result answers one question: how will we know the objective was achieved? This guide shows how to write Key Results that measure outcomes, with a formula, a test, and worked rewrites.

---

## The Formula

Write every Key Result in this shape:

> **[Verb] [metric] from [baseline] to [target] by [date]**

Example: Reduce average cycle time from commit to production from 6 days to 2 days by end of Q3.

If you cannot fill in the baseline, your first Key Result is to measure it. Write that one as: Establish a baseline for [metric] by [date].

---

## The 4-Question Test

Run every draft Key Result through these four questions. A "no" on any of them means the draft needs another pass.

| Question | If the answer is no |
|----------|---------------------|
| Is it measurable with a number? | Find the metric behind the statement, or set a baseline first. |
| Does it measure an outcome, not a task? | Ask "so that what?" until you reach the result the task is meant to produce. |
| Would missing it signal a real problem? | It is not important enough to be a Key Result. Move it to the team backlog. |
| Can it be tracked without a meeting? | Name the dashboard, query, or report that supplies the number. |

---

## Output vs. Outcome

Most weak Key Results describe work that will be done. Strong ones describe what changes because of the work.

| Output (weak) | Outcome (strong) |
|---------------|------------------|
| Launch the new deployment pipeline | Increase deployment frequency from 2 to 10 per week |
| Migrate 40 services to the new platform | Reduce infrastructure cost per request by 20% |
| Complete security training | Reduce open critical vulnerabilities from 30 to fewer than 5 |
| Ship the onboarding redesign | Reduce new engineer time to first production commit from 3 weeks to 5 days |

The numbers above are examples. Replace them with your own baselines and targets.

A delivery milestone can still appear in your plan. Track it as an initiative under the Key Result it supports, not as the Key Result itself.

---

## Three Types of Key Results

| Type | When to use it | Shape |
|------|----------------|-------|
| Improvement | You have a baseline and want to move it | From X to Y |
| Baseline | You do not have a trustworthy number yet | Establish a baseline for X |
| Guardrail | You want to make sure a gain does not cost you elsewhere | Keep X at or above Y |

A common pairing is one improvement Key Result and one guardrail. For example, increase deployment frequency while keeping change failure rate at or below its current level.

---

## How Many

- 1 to 3 objectives per team per quarter
- 2 to 3 Key Results per objective
- One named owner per Key Result, a person and not a team

If a team has more than nine Key Results, some of them are tasks.

---

## Checklist Before You Commit

- [ ] Every Key Result follows the formula
- [ ] Every Key Result passes the 4-question test
- [ ] Baselines are real numbers, pulled in the last 30 days
- [ ] Each Key Result has one owner and one data source
- [ ] The set includes at least one guardrail where a tradeoff is likely
- [ ] Someone outside the team can read the set and understand what success means

---

## Related

- [Key Result Bank](../templates/key-result-bank.md): examples by domain
- [Anti-Patterns](anti-patterns.md): the common ways OKRs go wrong
- [Alignment Model](alignment-model.md): connecting team OKRs to strategy
