---
generated: '2026-10-09'
method: generated
name: register-a-uitpas-ticket-sale
title: Register a UiTPAS discounted ticket sale
description: Get the UiTPAS tariffs a passholder is entitled to for an event, register the ticket sale and cancel it if needed.
api: openapi/publiq-uitpas-openapi.yml
operations:
- get-tariffs
- post-ticket-sales
- get-ticket-sales
- delete-ticket-sales
source: Grounded in openapi/publiq-uitpas-openapi.yml; every operationId verified verbatim.
---

# Register a UiTPAS discounted ticket sale

Get the UiTPAS tariffs a passholder is entitled to for an event, register the ticket sale and cancel it if needed.

## Steps

1. Retrieve available discounts with `get-tariffs` for the passholder and event.
2. Register the sale with `post-ticket-sales`.
3. List registered sales with `get-ticket-sales`.
4. Cancel a registration with `delete-ticket-sales`.

## Rules

- Auth: see https://docs.publiq.be/docs/authentication (and ../authentication/ if present). Errors: https://docs.publiq.be/docs/errors. Develop against the Testing server in the spec before switching to Production.
- GET operations are read-only; DELETE operations are destructive — confirm before calling.
- The spec documents no idempotency keys; do not blindly retry POSTs.
