# The Trade Desk GraphQL API

generated: '2026-08-13'
method: probed
source: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/GqlApiCallsPlatform

The Trade Desk runs a single GraphQL endpoint alongside its REST Platform API. The provider frames GraphQL as
augmentative rather than a REST replacement — capability is added to it incrementally, product by product.

## Endpoints

| Environment | URL |
| --- | --- |
| Production | `https://api.thetradedesk.com/graphql` |
| Partner Sandbox | `https://ext-api.sb.thetradedesk.com/graphql` |

The Workflows API also exposes GraphQL indirectly: `submitGraphQlRequest` (`POST /graphqlrequest`) is a passthrough
for an arbitrary query or mutation, and `submitGraphQlBulkQueryJob` / `getGraphQlBulkJobStatus` run large-scale bulk
queries as asynchronous jobs. Those operationIds are verified in the provider-published Speakeasy lockfile at
`https://github.com/TheTradeDesk/ttd-workflows-python/blob/main/.speakeasy/gen.lock`.

## Schema availability — GATED

Introspection is **not** available anonymously. Probed 2026-08-13:

| Probe | Result |
| --- | --- |
| `POST https://api.thetradedesk.com/graphql` with `{__schema{queryType{name}}}` | HTTP 401 `{"message":"Unauthorized"}` (Kong gateway) |
| `POST https://ext-api.sb.thetradedesk.com/graphql` with the same query | HTTP 401 `{"message":"Unauthorized"}` |

The docs confirm introspection works once authenticated — the Postman walkthrough instructs the reader to retrieve
the schema with "Use GraphQL Introspective" after setting the `TTD-Auth` header. **No SDL is saved in this repo,
because none could be fetched without a partner credential. Nothing has been reconstructed by hand.**

## Authentication

Exactly one auth header may be sent:

- `TTD-Auth: <token>` — preferred. Desk API and Unified API tokens.
- `Authorization: Bearer <jwt>` — Desk UI JWT tokens only.

Sending both is an error. See `authentication/trade-desk-authentication.yml`.

## Limits

Rate limits are enforced identically to REST, but the REST and GraphQL call counts are independent of one another.
Nested queries are additionally subject to **complexity limits**, documented separately at
`/doc/GqlApiErrors`. Exhaustion returns HTTP 429 with a `Retry-After` header. See
`rate-limits/trade-desk-rate-limits.yml`.

## References

- GraphQL Resource Hub: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/GqlApiHub
- Making GraphQL API calls: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/GqlApiCallsPlatform
- Queries: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/GqlApiQueries
- Mutations: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/GqlApiMutations
- Errors and complexity limits: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/GqlApiErrors
- Rate limits: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/GqlApiRateLimits
