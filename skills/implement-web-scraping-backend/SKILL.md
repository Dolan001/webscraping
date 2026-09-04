---
name: implement-web-scraping-backend
description: Implement approved production scraping adapters, jobs, selector registries, validation, and persistence in a selected DRF or FastAPI backend.
---

# Implement web scraping backend

1. Read `references/browser-runtime.md`, then the selected backend pack and approved site/selector
   contracts.
2. Generate one centralized browser factory and inject its driver into site adapters. Do not allow
   adapters to import or initialize UC directly.
3. Separate navigation, context traversal, extraction, normalization, validation and transaction-owned
   idempotent persistence; never treat zero new records as failure.
4. Run browser work in durable Celery workers with Redis locks, explicit concurrency, rate and runtime
   budgets, structured status, bounded retry/dead-letter behavior, and guaranteed cleanup.
5. Keep credentials out of argv, source, logs and evidence. Store only sanitized minimum evidence.
6. Add fixture-first tests; live smoke tests are opt-in and domain/account scoped.

