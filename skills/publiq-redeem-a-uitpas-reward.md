---
generated: '2026-10-09'
method: generated
name: redeem-a-uitpas-reward
title: Redeem a UiTPAS reward
description: Find a reward, check whether a passholder can redeem it and register the redemption.
api: openapi/publiq-uitpas-openapi.yml
operations:
- get-rewards
- get-rewards-id-redeem-status
- post-rewards-redeemed
- delete-rewards-redeemed-redeemedRewardId
source: Grounded in openapi/publiq-uitpas-openapi.yml; every operationId verified verbatim.
---

# Redeem a UiTPAS reward

Find a reward, check whether a passholder can redeem it and register the redemption.

## Steps

1. Search rewards with `get-rewards`.
2. Check eligibility with `get-rewards-id-redeem-status`.
3. Redeem with `post-rewards-redeemed`.
4. Cancel with `delete-rewards-redeemed-redeemedRewardId` if needed.

## Rules

- Auth: see https://docs.publiq.be/docs/authentication (and ../authentication/ if present). Errors: https://docs.publiq.be/docs/errors. Develop against the Testing server in the spec before switching to Production.
- GET operations are read-only; DELETE operations are destructive — confirm before calling.
- The spec documents no idempotency keys; do not blindly retry POSTs.
