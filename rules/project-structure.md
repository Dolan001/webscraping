# Generated project structure

Place the capability inside the selected backend using its native package conventions. Require domain
contracts/errors; application discovery/extraction/orchestration services; infrastructure browser,
HTTP, persistence and observability adapters; independent per-site adapters with versioned selector
YAML, parsers, validators and sanitized fixtures; durable tasks; migrations; APIs only when required;
and unit, fixture, integration and bounded live-smoke tests.

Do not create a second backend, standalone scraper repository, shared catch-all ticket module, or
site-specific driver. DRF uses models/services/selectors/serializers/views/URLs; FastAPI uses
models/services/repositories/queries/schemas/dependencies/routes.

