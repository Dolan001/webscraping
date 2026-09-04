# Scraping contract

For each site record its canonical name, base URL, allowed URL patterns, prohibited paths, access
owner, terms/robots review outcome, geography, authentication method and secret names, extraction
frequency, freshness target, maximum pages/records/runtime, concurrency, request rate, and change
notification policy.

For each target field record its stable name, meaning, requiredness, example shape, source page,
cardinality, type, normalization, validation, uniqueness identity, update rule, and missing/invalid
behavior. Define success with new records, success with no changes, partial result, transient failure,
authentication failure, selector drift, protective block, unavailable source, and permanent
configuration failure as different outcomes.

Require sanitized fixture ownership, live-test authorization, evidence retention/deletion, structured
metrics and correlation IDs. Never place credential values, cookies, signed links, private page bodies,
or ticket/barcode contents in the contract.

