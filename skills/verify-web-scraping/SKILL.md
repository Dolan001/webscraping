---
name: verify-web-scraping
description: Independently verify production scraping accuracy, selector stability, browser lifecycle, persistence, resilience, privacy, and operations.
---

# Verify web scraping

1. Read `references/verification.md` and the accepted site/selector contracts.
2. Verify fixture provenance and sanitization before testing.
3. Independently test target accuracy and completeness, context traversal, primary/fallback selectors,
   normalization, missing/invalid values, pagination, idempotency, concurrency, retries and cleanup.
4. Run live smoke checks only when explicitly enabled for named domains/accounts and bounded pages.
5. Write phase evidence matching the workflow schema. Fail closed for missing proof, target mismatch,
   unstable selectors, leaked secrets/private evidence, unbounded execution, or bypass behavior.

