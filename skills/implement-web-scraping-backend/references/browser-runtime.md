# Canonical UC browser runtime

Every generated browser-backed scraper must use one versioned factory. Pin and test a compatible
Python, Selenium, `undetected-chromedriver`, Chrome and ChromeDriver matrix. Detect the installed Chrome
major version and pass it to UC. On Linux use Xvfb at 1920x1080 rather than headless mode when the
deployment supports it; fail with an actionable dependency error when the required runtime is absent.

Create `uc.ChromeOptions` centrally. Apply `--no-sandbox` and `--disable-dev-shm-usage` only in the
container profile. Apply `--disable-features=AsyncDns` only in the approved proxy/network profile.
Configure an isolated per-job download directory with prompt disabled, directory upgrade enabled and
safe browsing enabled. Read proxy configuration from a secret-safe environment setting and log only
host-level masked metadata. Never add site-specific flags in adapters.

Use a 10-second explicit element-wait default, bounded page/script/download timeouts, state-based waits,
and a startup current-window-handle health check. Fixed sleeps are allowed only for a documented browser
stabilization gap that cannot be expressed as state. On browser failure: quit the old driver, apply
bounded backoff, recreate through the same factory, and retry the whole idempotent unit at most three
times. Do not retry CAPTCHA, queues, access denials, invalid credentials or permanent contract errors.

Always restore default content, close extra windows, quit the driver, delete temporary downloads and
release the Redis lease in `finally`. Debug capture is disabled by default. When explicitly enabled,
retain only sanitized, access-controlled evidence with a documented expiry; never store full authenticated
HTML, cookies, tokens, signed URLs, personal data, barcodes or ticket payloads.

This baseline standardizes reliable browser behavior. It does not claim invisibility and must not be
extended to evade fingerprinting, bot controls, queues, CAPTCHA, rate limits or access controls.

