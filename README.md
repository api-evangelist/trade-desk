# The Trade Desk (trade-desk)

The Trade Desk is an independent, omnichannel demand-side platform (DSP) for programmatic advertising, headquartered in Ventura, California. Its cloud-based platform — Kokai (the current flagship, succeeding Solimar) — lets agencies, brands, and trading desks buy and optimize digital ad inventory across connected TV (CTV), audio, mobile, video, native, display, and digital out-of-home. The Trade Desk positions itself as the buy-side counterweight to the walled gardens by championing the open internet through OpenPath (direct publisher integrations that bypass SSPs) and Unified ID 2.0 (UID2), an open-source, deterministic identity framework governed by the IAB Tech Lab. The company also stewards EUID (UID2's European equivalent), the Galileo first-party data activation framework, and Koa — its in-platform AI used for forecasting, bidding optimization, and audience modeling. Programmatic developers integrate via the TTD Workflows API (REST + GraphQL for campaign, ad group, and creative management), the Data API (advertiser/third-party data ingestion, offline conversions, deletion/opt-out), the Real-Time Conversion Events API (RTCE), and the OpenSincera data-quality APIs (acquired May 2024). Official SDKs are published in Python, Go, and Java and are Speakeasy-generated from OpenAPI specs. Most documentation lives behind the Partner Portal (partner.thetradedesk.com) but a public docs surface is exposed at open.thetradedesk.com. The Trade Desk is publicly traded (NASDAQ: TTD).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/trade-desk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/trade-desk/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Advertising
- Programmatic Advertising
- Demand-Side Platform
- DSP
- AdTech
- Connected TV
- CTV
- Identity
- Unified ID 2.0
- UID2
- OpenPath
- Kokai
- Koa AI
- Galileo
- Sincera
- Open Internet
- Real-Time Bidding
- Open Measurement

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### The Trade Desk Data API

Ingest first-party advertiser audience data, third-party provider audience data, and offline conversions (CAPI-style), and submit data-subject deletion / opt-out requests across advertiser, merchant, and provider contexts. The Data API powers audience targeting and offline-to-online measurement and supports UID2 identity mapping.

- **Human URL:** [https://open.thetradedesk.com/advertiser/docsApp/GuidesAdvertiser/data](https://open.thetradedesk.com/advertiser/docsApp/GuidesAdvertiser/data)

#### Tags

- Advertising
- Data
- Audience
- Conversions
- Privacy

#### Properties

- [Documentation](https://open.thetradedesk.com/advertiser/docsApp/GuidesAdvertiser/data/doc/post-data-advertiser-firstparty)
- [Documentation](https://open.thetradedesk.com/provider/docsApp/GuidesProvider/audience/doc/post-data-thirdparty)
- [Documentation](https://open.thetradedesk.com/advertiser/docsApp/GuidesAdvertiser/data/doc/post-providerapi-offlineconversion)
- [OpenAPI](openapi/trade-desk-data-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/trade-desk-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trade-desk-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [SDK](https://github.com/TheTradeDesk/ttd-data-python)

### The Trade Desk Workflows API

The Workflows API exposes the high-level campaign, ad group, creative, and bulk-job operations that previously required navigating the legacy Platform API. It blends REST and GraphQL surfaces (including a generic GraphQL passthrough and bulk query jobs) and is the recommended modern integration path for new partners.

- **Human URL:** [https://partner.thetradedesk.com/v3/portal/api/doc/ApiOverview](https://partner.thetradedesk.com/v3/portal/api/doc/ApiOverview)

#### Tags

- Advertising
- Campaigns
- Ad Groups
- GraphQL
- REST

#### Properties

- [Documentation](https://partner.thetradedesk.com/v3/portal/api/doc/ApiOverview)
- [Getting Started](https://partner.thetradedesk.com/v3/portal/api/doc/ApiPlatformGetStarted)
- [Documentation](https://partner.thetradedesk.com/v3/portal/api/doc/ApiReferencePlatform)
- [Documentation](https://partner.thetradedesk.com/v3/portal/api/doc/ApiUseCases)
- [Documentation](https://partner.thetradedesk.com/v3/portal/api/doc/ApiUsageGuidelines)
- [OpenAPI](https://api.thetradedesk.com/workflows/swagger/v1/swagger.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [SDK](https://github.com/TheTradeDesk/ttd-workflows-python)
- [SDK](https://github.com/TheTradeDesk/ttd-workflows-go)
- [SDK](https://github.com/TheTradeDesk/ttd-workflows-java)
- [Postman Collection](collections/trade-desk-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trade-desk-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### The Trade Desk Platform API

The original REST Platform API covering advertisers, campaigns, ad groups, creatives, targeting data, reporting, and audience operations. Documentation is gated behind the TTD Partner Portal. New integrations are generally steered to the Workflows API; Platform remains the reference for low-level objects and reporting endpoints.

- **Human URL:** [https://partner.thetradedesk.com/v3/portal/api/doc/ApiReferencePlatform](https://partner.thetradedesk.com/v3/portal/api/doc/ApiReferencePlatform)

#### Tags

- Advertising
- Campaigns
- REST
- Reporting

#### Properties

- [Documentation](https://partner.thetradedesk.com/v3/portal/api/doc/ApiReferencePlatform)
- [Documentation](https://partner.thetradedesk.com/v3/portal/api/overview)
- [Documentation](https://partner.thetradedesk.com/v3/portal/api/doc/ApiUsageGuidelines)
- [Code Examples](https://github.com/TheTradeDesk/Platform)
- [Postman Collection](collections/trade-desk-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trade-desk-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### The Trade Desk Real-Time Conversion Events API

Server-side and client-side conversion event ingestion (Apache 2.0 Google Tag Manager templates) for capturing high-fidelity attribution signals in a cookie-deprecated environment. Pairs with UID2 for identity resolution.

- **Human URL:** [https://partner.thetradedesk.com/v3/portal/api/doc/ApiOverview](https://partner.thetradedesk.com/v3/portal/api/doc/ApiOverview)

#### Tags

- Advertising
- Conversions
- Measurement
- Server-Side

#### Properties

- [SDK](https://github.com/TheTradeDesk/conversion-events-sdk-for-googletagmanager)
- [SDK](https://github.com/TheTradeDesk/conversion-events-server-side-googletagmanager)
- [Postman Collection](collections/trade-desk-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trade-desk-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unified ID 2.0 (UID2)

Unified ID 2.0 is an open-source, deterministic identity framework seeded by The Trade Desk and now governed by the IAB Tech Lab. UID2 resolves hashed email addresses and phone numbers into rotating tokens that publishers, DSPs, SSPs, and measurement vendors can use for addressable advertising without third-party cookies. The EUID variant provides a GDPR-aligned European deployment.

- **Human URL:** [https://unifiedid.com](https://unifiedid.com)

#### Tags

- Identity
- Privacy
- Open Source
- IAB Tech Lab

#### Properties

- [Portal](https://unifiedid.com)
- [Documentation](https://unifiedid.com/docs/intro)
- [Documentation](https://github.com/IABTechLab/uid2docs)
- [SDK](https://github.com/IABTechLab/uid2-operator)
- [Postman Collection](collections/trade-desk-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trade-desk-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### OpenSincera API

OpenSincera (from the May 2024 Sincera acquisition) provides programmatic supply-side transparency data — ad slot quality, page attributes, viewability metadata, supply-path metrics — to help buyers value impressions and audit inventory.

- **Human URL:** [https://partner.thetradedesk.com/v3/portal/opensincera/overview](https://partner.thetradedesk.com/v3/portal/opensincera/overview)

#### Tags

- Advertising
- Data Quality
- Supply Path
- Transparency

#### Properties

- [Documentation](https://partner.thetradedesk.com/v3/portal/opensincera/overview)
- [Postman Collection](collections/trade-desk-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trade-desk-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.thetradedesk.com)
- [Portal](https://www.thetradedesk.com/us)
- [Documentation](https://open.thetradedesk.com)
- [Documentation](https://partner.thetradedesk.com)
- [Getting Started](https://partner.thetradedesk.com/v3/portal/api/doc/ApiPlatformGetStarted)
- [Product](https://www.thetradedesk.com/us/our-platform)
- [Product](https://www.thetradedesk.com/us/our-platform/dsp-demand-side-platform)
- [Product](https://www.thetradedesk.com/us/openpath)
- [Product](https://www.thetradedesk.com/us/our-platform/koa-ai-artificial-intelligence)
- [Product](https://www.thetradedesk.com/us/news/introducing-galileo)
- [Identity](https://unifiedid.com)
- [Identity](https://euid.eu)
- [GitHub Organization](https://github.com/TheTradeDesk)
- [GitHub Organization](https://github.com/IABTechLab)
- [SDK](https://github.com/TheTradeDesk/ttd-workflows-python)
- [SDK](https://github.com/TheTradeDesk/ttd-workflows-go)
- [SDK](https://github.com/TheTradeDesk/ttd-workflows-java)
- [SDK](https://github.com/TheTradeDesk/ttd-data-python)
- [SDK](https://github.com/TheTradeDesk/ttd-databricks-python)
- [Code Examples](https://github.com/TheTradeDesk/Platform)
- [Press Room](https://www.thetradedesk.com/us/news)
- [Blog](https://www.thetradedesk.com/us/news-insights)
- [Newsroom](https://www.thetradedesk.com/us/press-room)
- [About Us](https://www.thetradedesk.com/us/about-us)
- [Careers](https://careers.thetradedesk.com)
- [Investor Relations](https://investors.thetradedesk.com)
- [Terms of Service](https://www.thetradedesk.com/us/website-privacy-policy)
- [Privacy Policy](https://www.thetradedesk.com/us/website-privacy-policy)
- [Contact](https://www.thetradedesk.com/us/contact-us)
- [LinkedIn](https://www.linkedin.com/company/the-trade-desk)
- [Twitter](https://twitter.com/thetradedesk)
- [YouTube](https://www.youtube.com/@thetradedesk)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
