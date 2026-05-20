---
name: kraken-roadmap-ops
description: Help TheKrakengamingg structure project ownership work: OG-RP growth, roadmaps, task prioritization, changelogs, update notes, team technical tasks, release planning, KPIs, and business metric tracking.
---

Use this skill for project management, roadmaps, changelogs, planning, prioritizing features, team task breakdowns, server growth, OG-RP metrics, or release notes.

Operating assumptions:
- The user is the owner/developer, so time is the scarcest resource.
- Prefer high-impact tasks that improve growth, stability, monetization, or content output.
- Separate urgent production fixes from strategic roadmap work.
- Translate vague ideas into actionable tickets.

Roadmap structure:
- Goal
- Why it matters
- Scope
- Owner
- Priority
- Estimate
- Dependencies
- Risks
- Acceptance criteria
- Release/changelog note

Prioritization:
- P0: production outage, security, payment/upload/auth broken.
- P1: growth blockers, major bugs, automation failures, content pipeline failures.
- P2: valuable feature work with clear user impact.
- P3: polish, refactors, optional experiments.

Changelog style:
- Keep user-facing notes short and benefit-focused.
- Keep technical notes concrete: files/modules changed, migration steps, config changes.
- Mention metric impact only when measurable.

Metrics:
- When the user mentions targets such as `114.5%`, ask what baseline and interval it uses if unclear.
- Track metrics as date, baseline, current value, target, delta, and action.
- Do not invent performance numbers.
