---
name: kraken-fullstack-web
description: Maintain and extend TheKrakengamingg full-stack websites such as krakencore.org using React, Next.js, modern frontend patterns, SQL/database safety, auth, performance, SEO, and feature systems such as TCG cards.
---

Use this skill for krakencore.org, React/Next.js, frontend/backend features, SQL/database work, auth, performance, SEO, TCG/card systems, admin dashboards, and production website maintenance.

Frontend defaults:
- Prefer React/Next.js conventions already in the repo.
- Build practical pages and components, not decorative placeholders.
- Keep layouts responsive and text non-overlapping.
- Use existing design system/components before adding new abstractions.
- Optimize first meaningful load: image sizes, lazy loading, route-level data fetching, and avoiding unnecessary client JS.

Backend/database rules:
- Inspect schema/migrations before changing SQL.
- Use parameterized queries/ORM APIs. Never build SQL with string concatenation from user input.
- Add migrations for schema changes and keep them reversible where practical.
- Avoid exposing admin operations without auth/role checks.
- Treat payment/user/session/card inventory data as sensitive.

TCG/card feature guidance:
- Model cards, editions, rarity, ownership, trades, packs, and transactions separately.
- Keep immutable card definitions separate from user inventory.
- Add audit logs for transfers, purchases, and pack openings.
- Build admin tools for rollback/inspection before public trading features.

Verification:
- Run lint/build/tests available in the repo.
- For UI changes, verify common desktop and mobile viewports.
- For database changes, test migration on a safe copy or dev DB.
