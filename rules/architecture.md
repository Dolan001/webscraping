# Web-scraping architecture rules

Web scraping is backend-owned. Prefer authorized structured sources before browser automation. Keep one
adapter per site and separate orchestration, navigation, context traversal, extraction, normalization,
validation and persistence. All UC use goes through one canonical injected factory. PostgreSQL owns
durable job/result/selector-version state; Celery owns execution; Redis owns transient leases and rate
coordination only. Runtime selector discovery may propose but never silently activate changes.

