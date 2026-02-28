# 📐 Engineering OKR Playbook

> Built from leading OKR programs across **300+ engineers** at Fastly — a $500M+ enterprise SaaS platform serving 77% of the Fortune 500.

Most OKR implementations in engineering organizations become reporting theater. Teams write objectives that are too vague to measure, key results that track activity instead of outcomes, and quarterly reviews that no one acts on. This playbook fixes that.

---

## 📌 Overview

This playbook covers three things most OKR guides skip:

1. **How to write Key Results that actually measure delivery** — not effort, not tasks, not "% complete"
2. **How to run a quarterly planning cadence** that connects engineering work to business outcomes without becoming a bureaucratic checkpoint
3. **How to align team-level OKRs to org and company strategy** — so engineers understand *why* their work matters, not just *what* to build

Everything here was applied in production at Fastly using **Jira / Jira Plans** across platform engineering and security product teams.

---

## 🎯 The Core Problem This Solves

> *"We have OKRs but nobody looks at them after Q1 planning."*

This happens for three reasons:

- **Key Results measure activity, not outcomes** — "Complete 5 runbooks" tells you nothing about whether delivery improved
- **OKRs live in a doc nobody revisits** — without a cadence, OKRs become a filing exercise
- **Team OKRs don't connect to anything above them** — engineers can't answer "why does this matter?"

This playbook gives you the framework, templates, and cadence to fix all three.

---

## 📂 Repository Structure

```
engineering-okr-playbook/
├── README.md                          ← You are here
├── frameworks/
│   ├── key-result-writing-guide.md   ← How to write KRs that measure outcomes
│   ├── alignment-model.md            ← Team → Org → Company OKR cascade
│   └── anti-patterns.md              ← What makes engineering OKRs fail
├── cadence/
│   ├── quarterly-planning-guide.md   ← Full Q planning process, week by week
│   ├── weekly-checkin-format.md      ← 15-min OKR check-in structure
│   └── qbr-facilitation-guide.md     ← How to run the quarterly business review
└── templates/
    ├── okr-tracker.xlsx               ← Team OKR tracker with scoring and RAG status
    ├── key-result-bank.xlsx           ← Library of proven KR patterns by engineering domain
    └── quarterly-planning-canvas.xlsx ← Q planning worksheet; Jira Plans-compatible
```

---

## 🔑 Part 1 — Writing Key Results That Work

### The test for a good Key Result

A Key Result passes if you can answer **yes** to all four:

| Question | Why It Matters |
|---|---|
| Is it measurable with a number? | Removes subjectivity from scoring |
| Does it measure an outcome, not a task? | Ensures the work actually moved something |
| Would a missed KR tell you something went wrong? | Creates accountability |
| Can it be tracked without a meeting? | Signals it's grounded in real data |

### The three KR types for engineering teams

**1. Metric KRs** — Move a number from X to Y
```
❌ "Improve system reliability"
✅ "Increase p99 API response time from 450ms to <200ms by end of Q3"
```

**2. Milestone KRs** — Deliver a specific, verifiable outcome
```
❌ "Complete CI/CD pipeline work"
✅ "Ship self-hosted GitHub runner migration for 300+ engineers by Sept 30,
    enabling Copilot adoption and eliminating $180K in annual runner costs"
```

**3. Threshold KRs** — Maintain a floor under a critical metric
```
❌ "Keep the platform stable"
✅ "Maintain 99.9% uptime across all Tier 1 services throughout Q3
    with zero P1 incidents exceeding 4-hour MTTR"
```

### KR anti-patterns to avoid

| Anti-Pattern | Example | Fix |
|---|---|---|
| Task masquerading as KR | "Complete 5 runbooks" | "Reduce mean time to onboard new engineer from 14 days to 5 days" |
| Vanity metric | "Increase Jira tickets closed by 20%" | "Reduce cycle time from ticket open to production deploy from 12 to 6 days" |
| Unverifiable outcome | "Improve team morale" | "Achieve >80% favorable on Q3 eng team health survey (n≥30)" |
| Binary with no signal | "Launch v2 of the platform" | "Launch v2 with <0.1% error rate on day 1 and 95% feature parity with v1" |
| Dependent on factors outside team control | "Achieve 32% ARR growth" | "Deliver 3 enterprise security features identified as top upsell drivers by Sales" |

---

## 📅 Part 2 — Quarterly Planning Cadence

### The 6-week Q planning cycle

This cadence was designed for platform engineering teams running in Jira / Jira Plans. Adjust week offsets to your fiscal calendar.

```
Week -6  │ Company/org OKRs published → TPM reviews for engineering implications
Week -5  │ Engineering leadership defines 3–5 draft Objectives for the quarter
Week -4  │ TPM facilitates KR writing workshop with tech leads and EMs
Week -3  │ Draft OKRs socialized with cross-functional partners (Product, Security, Infra)
Week -2  │ OKRs finalized; loaded into Jira Plans; owners confirmed
Week -1  │ Kickoff: all-hands or async brief explaining Q objectives and why they matter
Week  1  │ Quarter begins; weekly check-in cadence starts
```

### Weekly check-in format (15 minutes)

Run this async in Jira or synchronously in a standing 15-min slot:

```
For each Key Result:
  1. Current value vs. target        (e.g., "p99 latency: 310ms → target 200ms")
  2. RAG status                      (Green / Amber / Red)
  3. Confidence score (1–10)         (Has this changed since last week?)
  4. One blocker or risk             (What could prevent us hitting this?)
  5. One action item                 (What are we doing about it this week?)
```

### Quarterly Business Review (QBR) agenda

| Time | Section | Owner |
|---|---|---|
| 0:00–0:10 | Q recap: what we set out to do | Program Manager |
| 0:10–0:30 | OKR scoring: walk each KR; celebrate wins | Tech Lead per team |
| 0:30–0:45 | Missed KRs: root cause, not blame | TPM facilitates |
| 0:45–0:55 | Carry-forwards: what moves to next Q | Engineering Manager |
| 0:55–1:00 | Preview: next Q objectives (high level) | Engineering Director |

### OKR scoring guide

| Score | Meaning | What to do |
|---|---|---|
| 0.9 – 1.0 | Achieved or exceeded | Celebrate; check if target was too easy |
| 0.7 – 0.8 | Mostly achieved | Good; document what fell short and why |
| 0.5 – 0.6 | Partially achieved | Investigate blockers; carry forward if still relevant |
| 0.0 – 0.4 | Missed | Root cause analysis required before setting similar KR next Q |

> **Note:** A consistent score of 1.0 every quarter usually means targets are too conservative. Aim for 70% of KRs landing at 0.7–0.9.

---

## 🔗 Part 3 — Aligning Team OKRs to Company Strategy

### The cascade model

```
Company OKRs
    └── Engineering Org OKRs
            └── Platform Team OKRs
                    └── Individual Contributor Goals
```

Each level should be able to answer: **"How does this KR support the objective one level above it?"**

If a team KR can't be traced to an org objective, it's either work that shouldn't be happening or work that isn't being communicated correctly up the chain.

### Alignment checklist (run this before finalizing Q OKRs)

- [ ] Every team Objective maps to at least one Org Objective
- [ ] No team KR exists in isolation — each has an upstream owner who cares about it
- [ ] Cross-team dependencies are identified and owners are confirmed
- [ ] Product, Security, and Infrastructure have reviewed and signed off on shared KRs
- [ ] KRs that depend on vendor delivery have contingency owners
- [ ] All KRs have a named owner (not a team — a person)

### Jira Plans alignment setup

When loading OKRs into Jira Plans:

1. Create an **Epic** per Objective at the org level
2. Create **child Epics** per team-level Objective, linked to the parent
3. Map **Stories and Tasks** to team KRs using custom fields: `KR Owner`, `KR Target`, `KR Current Value`
4. Use **Plans timeline view** to visualize cross-team KR dependencies
5. Set up a **saved filter** for weekly KR check-in: `issuetype = Epic AND cf[KR_Status] != Done`

---

## 📊 Templates

| Template | What It's For |
|---|---|
| [okr-tracker.xlsx](templates/okr-tracker.xlsx) | Full quarter OKR tracker with RAG status, confidence scoring, and progress dashboard |
| [key-result-bank.xlsx](templates/key-result-bank.xlsx) | Library of 40+ proven KR patterns organized by engineering domain |
| [quarterly-planning-canvas.xlsx](templates/quarterly-planning-canvas.xlsx) | Q planning worksheet for drafting, aligning, and finalizing OKRs; Jira-compatible |

---

## ⚠️ Anti-Patterns Library

The most common ways engineering OKR programs fail — and how to fix them.

| Anti-Pattern | Symptom | Root Cause | Fix |
|---|---|---|---|
| OKR theater | Everyone scores 1.0 every quarter | Targets set too conservatively; no one wants to miss | Normalize 0.7 as success; reward honesty over optics |
| Orphaned OKRs | Team KRs don't connect to org goals | No alignment session before Q planning | Require explicit parent-child mapping before KRs are finalized |
| KR sprawl | 8–12 KRs per team per quarter | No prioritization forcing function | Hard cap: 3 Objectives × 3 KRs max per team |
| Reporting-only cadence | Check-ins happen but nothing changes | No action items or owners coming out of reviews | End every check-in with: one decision made, one blocker removed |
| Frozen OKRs | KRs never updated mid-quarter even when circumstances change | Fear of being seen as moving goalposts | Establish formal mid-quarter review at week 6 with authority to adjust |
| Individual contributor blindness | ICs don't know what the Q objectives are | OKRs live in leadership docs, not in daily tools | Load OKRs into Jira where ICs already work; link tickets to KRs |

---

## 🚀 Quick Start

1. **Download** `quarterly-planning-canvas.xlsx` and run your next Q planning session with it
2. **Use** `key-result-bank.xlsx` to find proven KR patterns for your engineering domain
3. **Load** finalized OKRs into Jira Plans using the alignment setup in Part 3
4. **Run** weekly check-ins using the 15-minute format in Part 2
5. **Score** at quarter end using the scoring guide; feed learnings into next Q

---

## 🔗 Related Repos

- [enterprise-platform-migrations](https://github.com/Ashaki509/EnterprisePlatformMigrations) — Migration framework with RACI, risk, comms, and milestone templates
- [tpm-toolkit](https://github.com/Ashaki509/tpm-toolkit) — Full index of TPM frameworks and playbooks

---

## 📬 Connect

Built by **Ashaki Sorrell** — Staff TPM (Director-Level) at Fastly.

- 📧 ashaki509@gmail.com
- 💼 [linkedin.com/in/ashakisorrell](https://linkedin.com/in/ashakisorrell)
- 🐙 [github.com/Ashaki509](https://github.com/Ashaki509)
