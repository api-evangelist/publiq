---
generated: '2026-10-09'
method: generated
name: register-a-museum-visit
title: Register a museumPASSmusées visit
description: Look up a museumPASSmusées pass (or an external card) by number and register a museum visit.
api: openapi/publiq-museumpassmusees-partner-openapi.yml
operations:
- get-passes
- post-visits
- get-external-cards-type-identification
- post-external-cards-type-identification-visits
source: Grounded in openapi/publiq-museumpassmusees-partner-openapi.yml; every operationId verified verbatim.
---

# Register a museumPASSmusées visit

Look up a museumPASSmusées pass (or an external card) by number and register a museum visit.

## Steps

1. Look up the pass with `get-passes` using the card number.
2. Register the visit with `post-visits`.
3. For external cards use `get-external-cards-type-identification` then `post-external-cards-type-identification-visits`.
4. Requires a CLIENT_ACCESS_TOKEN.

## Rules

- Auth: see https://docs.publiq.be/docs/authentication (and ../authentication/ if present). Errors: https://docs.publiq.be/docs/errors. Develop against the Testing server in the spec before switching to Production.
- GET operations are read-only; DELETE operations are destructive — confirm before calling.
- The spec documents no idempotency keys; do not blindly retry POSTs.
