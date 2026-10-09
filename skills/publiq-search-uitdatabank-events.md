---
generated: '2026-10-09'
method: generated
name: search-uitdatabank-events
title: Search UiTdatabank events and places
description: Find cultural and leisure events, places and organizers in UiTdatabank via the Search API, filtering by query
  and facets.
api: openapi/publiq-uitdatabank-search-openapi.yml
operations:
- get-events
- get-places
- get-offers
- get-organizers
source: Grounded in openapi/publiq-uitdatabank-search-openapi.yml; every operationId verified verbatim.
---

# Search UiTdatabank events and places

Find cultural and leisure events, places and organizers in UiTdatabank via the Search API, filtering by query and facets.

## Steps

1. Call `get-events` with a query (q / advanced query parameters) to search events; send your client identification as documented.
2. Use `get-places` to find venues and `get-organizers` to find organisers.
3. Use `get-offers` to search events and places together in one result set.
4. For long or complex queries use the POST variants (`post-events`, `post-offers`).

## Rules

- Auth: see https://docs.publiq.be/docs/authentication (and ../authentication/ if present). Errors: https://docs.publiq.be/docs/errors. Develop against the Testing server in the spec before switching to Production.
- GET operations are read-only; DELETE operations are destructive — confirm before calling.
- The spec documents no idempotency keys; do not blindly retry POSTs.
