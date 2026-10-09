---
generated: '2026-10-09'
method: generated
name: check-in-a-uitpas-passholder
title: Check in a UiTPAS passholder
description: Look up a UiTPAS pass, verify check-in eligibility for an event and register the check-in.
api: openapi/publiq-uitpas-openapi.yml
operations:
- get-passes-uitpasNumber
- get-checkin-status
- post-checkins
- get-checkins
source: Grounded in openapi/publiq-uitpas-openapi.yml; every operationId verified verbatim.
---

# Check in a UiTPAS passholder

Look up a UiTPAS pass, verify check-in eligibility for an event and register the check-in.

## Steps

1. Resolve the card with `get-passes-uitpasNumber`.
2. Check eligibility with `get-checkin-status` for the event.
3. Register with `post-checkins`.
4. Audit with `get-checkins`; undo with `delete-checkins-checkinId` if needed.

## Rules

- Auth: see https://docs.publiq.be/docs/authentication (and ../authentication/ if present). Errors: https://docs.publiq.be/docs/errors. Develop against the Testing server in the spec before switching to Production.
- GET operations are read-only; DELETE operations are destructive — confirm before calling.
- The spec documents no idempotency keys; do not blindly retry POSTs.
