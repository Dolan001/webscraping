# Selector registry standard

Store machine-readable YAML under the generated backend's site adapter. A target entry must include:

- site, page, URL pattern, registry version, discovery time, and fixture fingerprint;
- window/new-tab route, ordered iframe locator chain, and ordered open-shadow-host chain;
- prerequisite actions and explicit state-based waits;
- primary locator plus fallbacks using `api_json_path`, `id`, `name`, `data_attribute`, `aria`, `role`,
  `css`, `class`, `relative_xpath`, or `text`;
- extraction source, transform pipeline, cardinality, type and business validation;
- tag, stable attributes, parent/ancestor structure and nearby-label fingerprint;
- tested pages/records/reloads, match counts, confidence and rejection reasons.

Rank documented APIs/structured data first, then stable IDs, semantic/data attributes, accessible
roles, stable CSS, relative XPath, text, and finally positional paths. Store classes and absolute
XPath only as diagnostics or low-confidence fallbacks when proven stable. A fallback must not broaden
the data scope or weaken validation. Always unwind frames, shadow contexts and windows in `finally`.

