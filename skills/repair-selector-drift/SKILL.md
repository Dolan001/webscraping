---
name: repair-selector-drift
description: Diagnose and propose a controlled repair when an approved scraping selector or document-context route no longer matches.
---

# Repair selector drift

1. Read `references/drift-repair.md` and load only the failing site, target, registry version, sanitized
   evidence, fixture and recent structured errors.
2. Reproduce against fixtures first, then an explicitly authorized bounded live check if necessary.
3. Diagnose navigation, iframe/shadow context, timing, selector, extraction, schema, authentication,
   source-data, or protective-block failure separately.
4. Present the root cause, affected targets, compatibility impact, plan and verification before editing.
5. After approval, create a new selector-registry version, update focused fixtures/tests, verify old and
   new representative cases, and preserve rollback. Never silently self-modify production code.

