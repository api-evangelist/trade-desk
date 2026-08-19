---
name: Send offline conversions to The Trade Desk
description: Post offline or in-store conversion events to the offline attribution environment so they can be attributed back to programmatic impressions.
api: openapi/trade-desk-offlineconversion-api-openapi.yml
operations:
  - IngestOfflineConversionData
generated: '2026-08-13'
method: generated
source: openapi/trade-desk-offlineconversion-api-openapi.yml + https://open.thetradedesk.com/advertiser/docsApp/GuidesAdvertiser/data/doc/post-providerapi-offlineconversion
---

# Send offline conversions

## The host is different

Offline conversions do **not** go to the regional `*-data.adsrvr.org` hosts. They go to the offline attribution environment:

```
POST https://offlineattrib.adsrvr.org/providerapi/offlineconversion
```

This is the single documented environment for this endpoint — there is no regional fan-out.

## Steps

1. Authenticate with `TTD-Auth`. If your account still uses the legacy signature scheme, the `TtdSignature` header for this endpoint is an HMAC-SHA1 base64 digest of the JSON body keyed with the **data provider** secret key — not the advertiser key. Token auth is the current path; move off signatures.
2. Call `IngestOfflineConversionData` with the conversion events in the `Items` array. Each item carries the user ID, the tracking tag it attributes to, and the conversion value.
3. Set `Content-Type: application/json`.
4. Inspect `FailedLines[]` on the response before declaring success.

## Failure handling

- `403` `DataProviderMisconfigured` — the `DataProviderId` is not enabled for offline conversions. This is provisioning, not payload.
- `413` `MaxRequestSizeExceeded` — split and resend.
- `429` / `503` — read `Retry-After`, back off exponentially, keep concurrency at four or fewer callers.

## Real-time alternative

For conversions you can send at event time rather than in batch, the Real-Time Conversion Events API takes `POST https://insight.adsrvr.org/track/realtimeconversion` with `Content-Type: application/json` and **no authentication**, up to 28.6 MB per request with no cap on event count. It has no published OpenAPI, so it is not modelled as an operation here.
