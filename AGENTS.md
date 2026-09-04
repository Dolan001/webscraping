# Web-scraping behavior pack

This repository contains AI behavior only. Never add a runnable scraper, copied application source,
credentials, browser profiles, cookies, captured private pages, or generated selector discoveries.
Agents consume this pack with exactly one selected backend pack and write original code only inside
the target monorepo.

Web scraping activates only from an explicit PRD requirement. Prefer an authorized documented API,
embedded structured data, or HTTP parsing before browser automation. When a browser is necessary,
generate the canonical centralized UC runtime described by this pack; site adapters must never create
their own drivers. A protective block, CAPTCHA, queue, or access denial is a stop-and-report result,
not permission to bypass the control.

Discover and version the complete route to every target: URL/navigation state, window, iframe chain,
shadow-root chain, reveal actions, primary selector, fallbacks, extraction transform, validation, and
DOM fingerprint. Never accept a selector until it is repeatable across reloads and representative
records. Persist approved selector contracts for later runs; runtime rediscovery may propose a change
but must not silently rewrite production selectors or executable code.

