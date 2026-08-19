---
name: Onboard a first-party audience segment to The Trade Desk
description: Upload hashed or platform IDs into a named first-party targeting segment via the Data API, with the right data center, TTL, and failure handling.
api: openapi/trade-desk-advertiser-api-openapi.yml
operations:
  - IngestAdvertiserData
generated: '2026-08-13'
method: generated
source: openapi/trade-desk-advertiser-api-openapi.yml + https://open.thetradedesk.com/advertiser/docsApp/GuidesAdvertiser/data/doc/post-data-advertiser-firstparty
---

# Onboard a first-party audience segment

## Before you start

- You need a Platform API token. Generate it in OpenTTD Access Management (one week to one year lifetime) or call `POST https://api.thetradedesk.com/v3/authentication` for a token lasting up to 24 hours. Send it as the `TTD-Auth` request header on every call.
- Pick the data center closest to the users you are targeting, and upload to exactly one of them. The platform replicates onward:
  `https://usw-data.adsrvr.org` (US West), `https://use-data.adsrvr.org` (US East), `https://euw-data.adsrvr.org` (UK/EU), `https://sin-data.adsrvr.org` (APAC), `https://tok-data.adsrvr.org` (Tokyo). China-origin data goes to `https://data-cn2.adsrvr.cn` and does not replicate out.
- Do not upload the same payload to more than one data center.
- The Partner Sandbox does **not** accept Data API traffic. Audience data must be uploaded to production and picked up by the weekly sandbox sync.

## Steps

1. **Assemble the payload.** Call `IngestAdvertiserData` — `POST /data/advertiser`. The body carries `AdvertiserId`, `DataProviderId` where applicable, and an `Items` array. Each item in `Items` carries exactly one ID plus a `Data` array of segments.
2. **Choose one ID type per item.** Supported: `TDID`, `DAID`, `UID2`, `UID2Token`, `EUID`, `EUIDToken`, `RampID`, `ID5`, `netID`, `FirstId`, `UtiqId`. `UID2`, `EUID` and their token forms are case-sensitive. `ID5`, `netID`, `FirstId` and `UtiqId` are Europe-only.
3. **Set the segment and its lifetime.** Each `Data` entry needs a `Name` (max 256 characters) and should set `TTLInMinutes`. Default is 90 days (`129600`); maximum is 180 days (`259200`); 30 days (`43200`) is the recommended floor so segments stay refreshed. Set `TTLInMinutes: 0` for a single ID to remove that user, or for every ID to delete the whole segment.
4. **Optionally attach bid economics.** `BaseBidCPM` and `BidFactor` (0.5 to 100, default 1) ride on the `Data` entry and adjust bidding for users in that segment.
5. **Send it.** `Content-Type: application/json`, `TTD-Auth: <token>`. Ask for the v2 response format — v1 is still the default and returns only `FailedLines` with per-endpoint messaging.
6. **Read the response.** A `200` does not mean every row landed. Inspect `FailedLines[]`; each entry names the line and an `ErrorCode`.

## Failure handling

- `400` — `IncorrectContent`, `MissingData`, `SerializationFailed`, `UnknownRequest`. Fix the payload; do not retry unchanged.
- `401` — `AuthenticationFailed` or `InvalidToken`. The token is wrong or expired. Tokens cannot be refreshed; generate a new one.
- `403` — `IncorrectPermissions`, `AdvertiserMisconfigured`, `TargetingDataLimitReached`. Configuration problem, not a transient one. Contact the Technical Account Manager.
- `413` — `MaxRequestSizeExceeded`. Split the file and resend.
- `429` — rate limited. Read the `Retry-After` header (seconds) and honour it, or back off exponentially: `Delay = Min(max_delay, base_delay * 2 ^ retrycount)`. Keep concurrency at or below four callers per endpoint.
- `503` — temporary overload. Same `Retry-After` handling.

> **No idempotency contract.** The Trade Desk documents no idempotency key and no replay window on this endpoint. A blind retry after a timeout may re-apply the segment membership. Retry only on `429`/`503`, and treat a timed-out request as unknown rather than failed.

## Related

- Third-party data: `IngestThirdPartyData` (`openapi/trade-desk-thirdparty-api-openapi.yml`)
- IP-address segments: `IngestFirstPartyIPAddressData` (`openapi/trade-desk-ipaddress-api-openapi.yml`)
- Deleting a user rather than expiring them: `DataSubjectRequestAdvertiserData`
