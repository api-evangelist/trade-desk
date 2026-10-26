# The Trade Desk (trade-desk)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
