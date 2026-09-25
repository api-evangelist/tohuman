---
name: tohuman-submit-humanization
description: Submit a humanization request and poll for its result.
api: openapi/_ae-authored/tohuman-openapi-generated.yml
operations:
- post_api_v1_humanizations
- get_api_v1_humanizations_humanizationid
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/_ae-authored/tohuman-openapi-generated.yml ; every operationId checked against the contract
---

# tohuman-submit-humanization

Submit a humanization request and poll for its result.

## Steps

1. 1. Call `post_api_v1_humanizations` with the request body (as defined by the API) and include the `Authorization: Bearer <token>` header.
2. 2. Call `get_api_v1_humanizations_humanizationid` with the `humanizationId` returned from step 1 and include the `Authorization: Bearer <token>` header to retrieve the completed result.

## Rules

- Use a Bearer token in the `Authorization` header for all requests.
- Rate limit: 60 requests per minute; exceeding returns HTTP 429.
