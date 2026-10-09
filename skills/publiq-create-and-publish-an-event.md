---
generated: '2026-10-09'
method: generated
name: create-and-publish-an-event
title: Create and publish an event in UiTdatabank
description: Create an event at an existing place with the Entry API, attach an image, publish it and read it back.
api: openapi/publiq-uitdatabank-entry-openapi.yml
operations:
- place-get
- event-post
- image-post
- event-images-post
- event-workflow-status-put
- event-get
source: Grounded in openapi/publiq-uitdatabank-entry-openapi.yml; every operationId verified verbatim.
---

# Create and publish an event in UiTdatabank

Create an event at an existing place with the Entry API, attach an image, publish it and read it back.

## Steps

1. Confirm the location with `place-get` (or create it with `place-post`).
2. Create the event with `event-post`; keep the returned eventId.
3. Upload an image with `image-post`, then attach it with `event-images-post`.
4. Publish by setting the workflow status with `event-workflow-status-put`.
5. Verify with `event-get`.
6. Requires a USER_ACCESS_TOKEN or CLIENT_ACCESS_TOKEN.

## Rules

- Auth: see https://docs.publiq.be/docs/authentication (and ../authentication/ if present). Errors: https://docs.publiq.be/docs/errors. Develop against the Testing server in the spec before switching to Production.
- GET operations are read-only; DELETE operations are destructive — confirm before calling.
- The spec documents no idempotency keys; do not blindly retry POSTs.
