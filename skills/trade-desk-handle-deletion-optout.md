---
name: Handle a data subject deletion or opt-out request at The Trade Desk
description: Route a GDPR/CCPA deletion or opt-out request to the correct Data API endpoint for advertiser, third-party or merchant data, and confirm what came back.
api: openapi/trade-desk-deletionoptout-api-openapi.yml
operations:
  - DataSubjectRequestAdvertiserData
  - DataSubjectRequestThirdPartyData
  - DataSubjectRequestMerchantData
generated: '2026-08-13'
method: generated
source: openapi/trade-desk-deletionoptout-api-openapi.yml + https://open.thetradedesk.com/advertiser/docsApp/GuidesAdvertiser/data/doc/post-data-deletion-optout-advertiser
---

# Handle a data subject deletion or opt-out request

## Pick the right endpoint first

There is no single DSR endpoint. Which one you call depends on whose data you hold:

| You are | Operation | Path |
|---|---|---|
| An advertiser deleting your own first-party data | `DataSubjectRequestAdvertiserData` | `POST /data/deletion-optout/advertiser` |
| A third-party data provider | `DataSubjectRequestThirdPartyData` | `POST /data/deletion-optout/thirdparty` |
| A merchant / retail data provider | `DataSubjectRequestMerchantData` | `POST /data/deletion-optout/merchant` |

Calling the wrong one returns `403` with `AdvertiserMisconfigured`, `DataProviderMisconfigured` or `MerchantMisconfigured` — the platform will not silently reroute the request.

## Steps

1. Authenticate with `TTD-Auth`. Same token as every other Data API call.
2. Send the request to the data center you originally uploaded to (see the data-center table in `sandbox/` and `conventions/`), since that is where the segment membership lives.
3. Build the body: the owning ID (`AdvertiserId`, `DataProviderId` or `MerchantId`) plus the `Items` array of user IDs to act on. `PartnerDsrRequestType` distinguishes a deletion from an opt-out.
4. Send with `Content-Type: application/json`.
5. Read `FailedLines[]` in the response. Rows that fail come back with a `DsrErrorCode`; a `200` with a populated `FailedLines` array is a partial success, not a success.

## Deletion versus expiry

These endpoints are the correct mechanism for a data-subject request. Do **not** use `TTLInMinutes: 0` on `IngestAdvertiserData` to satisfy a legal deletion — that expires segment membership for targeting purposes and is a different operation with different semantics.

## Failure handling

Same error catalogue as the ingestion endpoints: see `errors/trade-desk-error-codes.yml`. Honour `Retry-After` on `429` and `503`. There is no idempotency key, but deletion is naturally idempotent in effect — re-sending the same deletion is safe in a way that re-sending an ingest is not.
