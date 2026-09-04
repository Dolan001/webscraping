---
name: discover-target-selectors
description: Discover, score, test, and version reusable selectors and document-context routes for approved scraping targets.
---

# Discover target selectors

1. Read `references/selector-registry.md`.
2. Confirm the approved domain, URL, account, target fields, live-access permission, page/runtime
   limits, and evidence policy before navigation.
3. Search structured data and the main document, then permitted frames, nested frames, open shadow
   roots, tabs, modals, lazy content, pagination, and reveal actions.
4. Produce a primary locator and independent fallbacks. Test uniqueness/count, extracted type and
   meaning, repeatability across reloads, and representative-record coverage.
5. Write the versioned registry and sanitized discovery evidence. Do not write scraper code, mutate
   production selectors, or continue through CAPTCHA, queues, denials, or other protective controls.

