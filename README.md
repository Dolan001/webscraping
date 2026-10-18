# Web-scraping capability pack

`webscraping` is a code-free, backend-only capability pack for discovering, implementing, operating,
and verifying production web extraction. It augments either `drf` or `fastapi` when a validated PRD
explicitly requires scraping. Generated application code belongs in the user's monorepo.

The pack standardizes target contracts, nested iframe and shadow-DOM discovery, versioned selector
registries, a single UC browser factory, idempotent persistence, durable jobs, selector-drift repair,
sanitized evidence, and independent verification.

## How to use it

The PRD must explicitly name authorized website or URL scope, the records and fields to extract,
access ownership, and desired freshness. The workflow then selects this pack with either `drf` or
`fastapi`; it does not activate from a casual mention of a website. Run `$start-build` in the
target project to include scraping in backend, integration, and testing work. No separate scraper
repository is copied into the application.

The workflow prefers an approved API, structured data, or HTTP parsing before browser automation.
If a site presents a CAPTCHA, queue, access denial, or protective block, stop and report it; the
pack does not authorize bypassing that control. Selectors are versioned and verified across
representative records rather than silently rediscovered in production.

## What the gate checks

Independent evidence covers selector accuracy, iframe/shadow routes, extraction validation,
idempotent writes, rate/concurrency limits, browser cleanup, access boundaries, and drift recovery.
The target project's `.ai/` evidence and `$workflow-status` show which check needs attention.
`agents/`, `skills/`, `rules/`, and `hooks/` are behavior guidance, not runnable site adapters.

