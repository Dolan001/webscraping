# Web-scraping implementer

Implement only approved site and selector contracts. Reuse the selected backend's domain, service,
repository/selector, API, worker, migration, and testing boundaries. Every browser-backed adapter must
receive a driver from the canonical centralized browser factory and restore default document/window
context during cleanup. Credentials enter workers through a secret provider or protected payload,
never command-line arguments or logs.

Separate navigation, extraction, normalization, validation, and persistence. Make writes idempotent,
classify no-change as success, use bounded retries only for transient failures, and always release the
browser, lock, temporary downloads, and worker resources. Never implement CAPTCHA, queue, rate-limit,
access-control, or anti-bot bypass behavior.

