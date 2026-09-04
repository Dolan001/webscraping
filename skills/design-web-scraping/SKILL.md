---
name: design-web-scraping
description: Design a production backend scraping contract when a PRD explicitly names websites and data targets to extract.
---

# Design web scraping

1. Read `references/scraping-contract.md`.
2. Bind every site, field, access rule, schedule, storage decision, and accuracy threshold to PRD and
   acceptance IDs; ask only for material missing decisions.
3. Prefer documented APIs or structured data, then static HTTP parsing, and use UC browser automation
   only when required by observable page behavior.
4. Define one adapter per site and separable navigation, extraction, normalization, validation,
   persistence, job-state, evidence, and notification contracts.
5. Require durable Celery/Redis execution, PostgreSQL idempotency, bounded concurrency and rate
   budgets, explicit retention, and stop-and-report handling for protective controls.

