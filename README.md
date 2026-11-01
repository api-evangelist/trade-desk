# The Trade Desk

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

**Areas:** Advertising · Programmatic Advertising · DSP · AdTech · Connected TV · CTV · Identity · Unified ID 2.0 · UID2 · OpenPath · Kokai · Koa AI

## The Trade Desk on APIs.io

Everything profiled for The Trade Desk is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/trade-desk/](https://apis.io/providers/trade-desk/)** — or go straight to one of the APIs or properties below.

### APIs (11)

- [The Trade Desk Platform API](https://apis.io/apis/trade-desk/trade-desk-platform-api/) — The original REST Platform API covering advertisers, campaigns, ad groups, creatives, targeting data, reporting, and audience operations. Documentation is…
- [The Trade Desk Real-Time Conversion Events API](https://apis.io/apis/trade-desk/trade-desk-realtime-conversion-events-api/) — Server-side and client-side conversion event ingestion (Apache 2.0 Google Tag Manager templates) for capturing high-fidelity attribution signals in a…
- [Unified ID 2.0 (UID2)](https://apis.io/apis/trade-desk/trade-desk-uid2-api/) — Unified ID 2.0 is an open-source, deterministic identity framework seeded by The Trade Desk and now governed by the IAB Tech Lab. UID2 resolves hashed email…
- [OpenSincera API](https://apis.io/apis/trade-desk/trade-desk-opensincera-api/) — OpenSincera (from the May 2024 Sincera acquisition) provides programmatic supply-side transparency data — ad slot quality, page attributes, viewability…
- [The Trade Desk Advertiser API](https://apis.io/apis/trade-desk/trade-desk-advertiser-api/) — The Advertiser API from The Trade Desk — 1 operation(s) for advertiser.
- [The Trade Desk DeletionOptOut API](https://apis.io/apis/trade-desk/trade-desk-deletionoptout-api/) — The DeletionOptOut API from The Trade Desk — 3 operation(s) for deletionoptout.
- [The Trade Desk OfflineConversion API](https://apis.io/apis/trade-desk/trade-desk-offlineconversion-api/) — The OfflineConversion API from The Trade Desk — 1 operation(s) for offlineconversion.
- [The Trade Desk Real-Time Conversions API](https://apis.io/apis/trade-desk/the-trade-desk-real-time-conversions-api/) — The Trade Desk Real-Time Conversions API (formerly the Real-Time Conversion Events API) allows advertisers to send conversion events server-side in real…
- [The Trade Desk Reporting API](https://apis.io/apis/trade-desk/the-trade-desk-reporting-api/) — The Trade Desk Reporting API provides programmatic access to campaign performance data including impressions, clicks, conversions, spend, win rates,…
- [The Trade Desk IP Address API](https://apis.io/apis/trade-desk/trade-desk-ip-address-api/) — The IP Address API from The Trade Desk — 2 operation(s) for ip address.
- [The Trade Desk Third Party API](https://apis.io/apis/trade-desk/trade-desk-third-party-api/) — The Third Party API from The Trade Desk — 1 operation(s) for third party.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [The Trade Desk GraphQL API](https://apis.io/graphqls/trade-desk/trade-desk-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Open Agentic Kit (OAK)](https://apis.io/servers/trade-desk/open-agentic-kit-oak/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Trade Desk Agentic Access](https://apis.io/agentic-access/trade-desk/trade-desk-agentic-access/)

#### Collections (6)

Postman and Open Collection request collections.

- [TTD Data Advertiser API](https://apis.io/collections/trade-desk/open-trade-desk-advertiser-api/)
- [TTD Data API](https://apis.io/collections/trade-desk/open-trade-desk-data-api/)
- [TTD Data Advertiser DeletionOptOut API](https://apis.io/collections/trade-desk/open-trade-desk-deletionoptout-api/)
- [TTD Data IPAddress API](https://apis.io/collections/trade-desk/open-trade-desk-ipaddress-api/)
- [TTD Data Advertiser OfflineConversion API](https://apis.io/collections/trade-desk/open-trade-desk-offlineconversion-api/)
- [TTD Data Advertiser ThirdParty API](https://apis.io/collections/trade-desk/open-trade-desk-thirdparty-api/)

#### Overlays (5)

OpenAPI overlays, including conversational phrasing for each operation.

- [Trade Desk Advertiser Api Overlay](https://apis.io/overlays/trade-desk/trade-desk-advertiser-api-overlay/)
- [Trade Desk Deletionoptout Api Overlay](https://apis.io/overlays/trade-desk/trade-desk-deletionoptout-api-overlay/)
- [Trade Desk Ipaddress Api Overlay](https://apis.io/overlays/trade-desk/trade-desk-ipaddress-api-overlay/)
- [Trade Desk Offlineconversion Api Overlay](https://apis.io/overlays/trade-desk/trade-desk-offlineconversion-api-overlay/)
- [Trade Desk Thirdparty Api Overlay](https://apis.io/overlays/trade-desk/trade-desk-thirdparty-api-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Trade Desk Authentication](https://apis.io/security/trade-desk/trade-desk-authentication/)
- [Trade Desk Domain Security](https://apis.io/security/trade-desk/trade-desk-domain-security/)
- [Trade Desk Trust Center](https://apis.io/security/trade-desk/trade-desk-trust-center/)
- [Trade Desk Vulnerability Disclosure](https://apis.io/security/trade-desk/trade-desk-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Trade Desk Scopes](https://apis.io/scopes/trade-desk/trade-desk-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Trade Desk Plans Pricing](https://apis.io/plans/trade-desk/trade-desk-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Trade Desk Rate Limits](https://apis.io/rate-limits/trade-desk/trade-desk-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.thetradedesk.com)
- [Documentation](https://open.thetradedesk.com)
- [Getting started](https://partner.thetradedesk.com/v3/portal/api/doc/ApiPlatformGetStarted)
- [API reference](https://partner.thetradedesk.com/v3/portal/api/doc/ApiReferencePlatform)
- [Sign up](https://open.sincera.io/sign_up)
- [Support](https://open.thetradedesk.com/contact-us)
- [Blog](https://www.thetradedesk.com/us/news-insights)
- [Security](https://www.thetradedesk.com/trust/report-a-vulnerability)
- [Compliance](https://www.thetradedesk.com/trust/security)
- [Trust centre](https://www.thetradedesk.com/trust)
- [Terms of service](https://www.thetradedesk.com/legal/trade-desk-advertising-terms-4-7-26)
- [Privacy policy](https://www.thetradedesk.com/legal/website-privacy-policy)
- [GitHub](https://github.com/TheTradeDesk)

## API Evangelist rating

**Kin Score 55.1** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.8 |
| Contract quality | 40.1 |
| Contract governance | 18.2 |
| Operational transparency | 42.1 |
| Developer ergonomics | 80.4 |
| Access clarity | 50.0 |

**Agent readiness 44.2** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 45.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/trade-desk/](https://apis.io/providers/trade-desk/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for The Trade Desk: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/trade-desk/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
