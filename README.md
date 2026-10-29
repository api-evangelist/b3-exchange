# B3 (Brasil Bolsa Balcão)

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

B3 S.A. - Brasil, Bolsa, Balcão is the Brazilian exchange and financial market infrastructure operator formed by the 2017 merger of BM&FBOVESPA and Cetip, running trading, clearing, central depository, and OTC registration for equities, derivatives, fixed income, and FX. Its public B3 for Developers portal documents 114 B2B REST APIs (OAuth 2.0 client credentials and ROPC) across investor-area, OTC (Balcão), listed-markets, Tesouro Direto, Banco B3, and insurance domains. Real-time market data is distributed through the UMDF multicast feed (FIX/FAST and Binary SBE, L1/L2) via authorized distributors, and end-of-day plus reference data through the UP2DATA file service (TXT/CSV/JSON/XML via client software or cloud). All API and data access is contract-gated for institutions - B3 explicitly offers no self-serve access for individuals.

**Areas:** Finance · Market Data · Stocks · Trading · Exchange · Derivatives · Fixed Income · Real-Time · Reference Data · Brazil

## B3 (Brasil Bolsa Balcão) on APIs.io

Everything profiled for B3 (Brasil Bolsa Balcão) is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/b3-exchange/](https://apis.io/providers/b3-exchange/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [B3 Investor Area (Área do Investidor) APIs](https://apis.io/apis/b3-exchange/b3-investor-area-apis/) — D-1 investor data for authorized fintechs and custodians - investment positions, account transactions, listed-asset buy/sell activity, public offering…
- [B3 Tesouro Direto APIs](https://apis.io/apis/b3-exchange/b3-tesouro-direto-apis/) — Treasury Direct platform APIs - the Bonds API serves reference data for Brazilian public bonds (name, maturity, Selic code, platform identifiers), Positions…
- [B3 OTC (Balcão) APIs](https://apis.io/apis/b3-exchange/b3-otc-balcao-apis/) — Registration, custody, and consultation APIs for the OTC segment - bank funding instruments (CDB, RDB, LCA, LCI, LF, LIG), credit notes (CCB, CPR, NC), OTC…
- [B3 Listed Markets (Listados) APIs](https://apis.io/apis/b3-exchange/b3-listed-markets-apis/) — Post-trade APIs for the listed segment - iMercado investment fund registration and equities fee details, CORE risk calculation and simulation, unified…
- [B3 ISIN API](https://apis.io/apis/b3-exchange/b3-isin-api/) — ISIN issuance and management for financial instruments - B3 is the Brazilian numbering agency - covering ISIN requests, updates, and consultation of…
- [Banco B3 APIs](https://apis.io/apis/b3-exchange/b3-banco-b3-apis/) — Banco B3 Custody API for operation billing, position reports, and fund quote validation, plus the Settlement API for Pix statement consultation.
- [B3 Insurance (Seguros) APIs](https://apis.io/apis/b3-exchange/b3-insurance-apis/) — Insurance-segment registration APIs (V3) covering accepted co-insurance registration, claim registration, document registration, and batch processing return…
- [B3 Authentication APIs](https://apis.io/apis/b3-exchange/b3-authentication-apis/) — OAuth 2.0 token issuance APIs used across the B3 API catalog - Client Credentials flows (plain, plus category_ID, key, or scope parameter variants) and…
- [B3 Market Data Feed (UMDF)](https://apis.io/apis/b3-exchange/b3-market-data-feed-umdf/) — B3's real-time market data distribution over the Unified Market Data Feed (UMDF) - event-based bid, ask, trade, and statistics data in L1 (top of book) or…
- [B3 UP2DATA](https://apis.io/apis/b3-exchange/b3-up2data/) — End-of-day and reference data service covering fixed income, equities, currencies, and debentures for mark-to-market, risk, and pricing workflows -…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [b3-exchange](https://apis.io/servers/b3-exchange/b3-exchange/)

#### Collections (14)

Postman and Open Collection request collections.

- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-auth-client-credentials/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-auth-ropc/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-banco-b3-custody/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-banco-b3-settlement/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-core-calculation/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-insurance-claim/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-investor-position/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-investor-transactions/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-isin/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-otc-public-info/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-securities-lending/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-tesouro-direto-bonds/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-tesouro-direto-orders/)
- [API Collection](https://apis.io/collections/b3-exchange/open-b3-exchange-tesouro-direto-positions/)

#### Overlays (14)

OpenAPI overlays, including conversational phrasing for each operation.

- [B3 Exchange Auth Client Credentials Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-auth-client-credentials-overlay/)
- [B3 Exchange Auth Ropc Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-auth-ropc-overlay/)
- [B3 Exchange Banco B3 Custody Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-banco-b3-custody-overlay/)
- [B3 Exchange Banco B3 Settlement Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-banco-b3-settlement-overlay/)
- [B3 Exchange Core Calculation Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-core-calculation-overlay/)
- [B3 Exchange Insurance Claim Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-insurance-claim-overlay/)
- [B3 Exchange Investor Position Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-investor-position-overlay/)
- [B3 Exchange Investor Transactions Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-investor-transactions-overlay/)
- [B3 Exchange Isin Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-isin-overlay/)
- [B3 Exchange Otc Public Info Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-otc-public-info-overlay/)
- [B3 Exchange Securities Lending Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-securities-lending-overlay/)
- [B3 Exchange Tesouro Direto Bonds Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-tesouro-direto-bonds-overlay/)
- [B3 Exchange Tesouro Direto Orders Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-tesouro-direto-orders-overlay/)
- [B3 Exchange Tesouro Direto Positions Overlay](https://apis.io/overlays/b3-exchange/b3-exchange-tesouro-direto-positions-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [B3 Exchange Authentication](https://apis.io/security/b3-exchange/b3-exchange-authentication/)
- [B3 Exchange Domain Security](https://apis.io/security/b3-exchange/b3-exchange-domain-security/)
- [B3 Exchange Vulnerability Disclosure](https://apis.io/security/b3-exchange/b3-exchange-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [B3 Exchange Scopes](https://apis.io/scopes/b3-exchange/b3-exchange-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.b3.com.br/en_us/)
- [Documentation](https://developers.b3.com.br/apis)
- [Getting started](https://developers.b3.com.br/faq)
- [API reference](https://developers.b3.com.br/apis)
- [Support](https://developers.b3.com.br/contato)
- [Security](https://developers.b3.com.br/seguranca)
- [Terms of service](https://www.b3.com.br/en_us/terms-of-use-and-data-protection/)
- [Privacy policy](https://www.b3.com.br/en_us/terms-of-use-and-data-protection/)

## API Evangelist rating

**Kin Score 38.7** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 24.0 |
| Contract governance | 18.2 |
| Operational transparency | 26.3 |
| Developer ergonomics | 63.7 |
| Access clarity | 27.6 |

**Agent readiness 19.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 38.0** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/b3-exchange/](https://apis.io/providers/b3-exchange/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for B3 (Brasil Bolsa Balcão): the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/b3-exchange/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
