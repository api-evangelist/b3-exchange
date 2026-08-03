# B3 (Brasil Bolsa Balcão) (b3-exchange)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

B3 S.A. - Brasil, Bolsa, Balcão is the Brazilian exchange and financial market infrastructure operator formed by the 2017 merger of BM&FBOVESPA and Cetip, running trading, clearing, central depository, and OTC registration for equities, derivatives, fixed income, and FX. Its public B3 for Developers portal documents 114 B2B REST APIs (OAuth 2.0 client credentials and ROPC) across investor-area, OTC (Balcão), listed-markets, Tesouro Direto, Banco B3, and insurance domains. Real-time market data is distributed through the UMDF multicast feed (FIX/FAST and Binary SBE, L1/L2) via authorized distributors, and end-of-day plus reference data through the UP2DATA file service (TXT/CSV/JSON/XML via client software or cloud). All API and data access is contract-gated for institutions - B3 explicitly offers no self-serve access for individuals.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/b3-exchange/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/b3-exchange/refs/heads/main/apis.yml)

## Tags

- Financial
- Market Data
- Stocks
- Trading
- Exchange
- Derivatives
- Fixed Income
- Real-Time
- Reference Data
- Brazil

## Timestamps

- **Created:** 2026-07-21
- **Modified:** 2026-07-21

## APIs

### B3 Investor Area (Área do Investidor) APIs

D-1 investor data for authorized fintechs and custodians - investment positions, account transactions, listed-asset buy/sell activity, public offering participation, and provisioned corporate events - under OAuth 2.0 with investor consent flows (STVM request/response authorization).

- **Human URL:** [https://developers.b3.com.br/apis/api-area-do-investidor](https://developers.b3.com.br/apis/api-area-do-investidor)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- Investor Data
- Positions
- Transactions

#### Properties

- [Documentation](https://developers.b3.com.br/apis/api-area-do-investidor)
- [OpenAPI (Swagger 1.1 discovery, harvested)](openapi/b3-exchange-investor-position-openapi.json)
- [OpenAPI (Swagger 1.1 discovery, harvested)](openapi/b3-exchange-investor-transactions-openapi.json)

### B3 Tesouro Direto APIs

Treasury Direct platform APIs - the Bonds API serves reference data for Brazilian public bonds (name, maturity, Selic code, platform identifiers), Positions serves investor position balances, and Orders covers operations on the Tesouro Direto platform.

- **Human URL:** [https://developers.b3.com.br/apis/tesouro-direto](https://developers.b3.com.br/apis/tesouro-direto)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- Government Bonds
- Reference Data
- Positions

#### Properties

- [Documentation](https://developers.b3.com.br/apis/tesouro-direto)
- [OpenAPI (Swagger 1.1 discovery, harvested)](openapi/b3-exchange-tesouro-direto-bonds-openapi.json)
- [OpenAPI (Swagger 1.1 discovery, harvested)](openapi/b3-exchange-tesouro-direto-positions-openapi.json)

### B3 OTC (Balcão) APIs

Registration, custody, and consultation APIs for the OTC segment - bank funding instruments (CDB, RDB, LCA, LCI, LF, LIG), credit notes (CCB, CPR, NC), OTC derivatives (swaps, flexible options, term contracts), liens and collateral, plus the NoMe Public-Info API for OTC public information consultation.

- **Human URL:** [https://developers.b3.com.br/apis/api-balcao](https://developers.b3.com.br/apis/api-balcao)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- OTC
- Fixed Income
- Registration

#### Properties

- [Documentation](https://developers.b3.com.br/apis/api-balcao)
- [OpenAPI (Swagger 1.1 discovery, harvested)](openapi/b3-exchange-otc-public-info-openapi.json)

### B3 Listed Markets (Listados) APIs

Post-trade APIs for the listed segment - iMercado investment fund registration and equities fee details, CORE risk calculation and simulation, unified client registration, asset lending, reconciliation files, and guarantee management report data.

- **Human URL:** [https://developers.b3.com.br/apis/api-listados](https://developers.b3.com.br/apis/api-listados)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- Post-Trade
- Risk
- Funds

#### Properties

- [Documentation](https://developers.b3.com.br/apis/api-listados)

### B3 ISIN API

ISIN issuance and management for financial instruments - B3 is the Brazilian numbering agency - covering ISIN requests, updates, and consultation of instrument identifier records.

- **Human URL:** [B3 ISIN API detail page](https://developers.b3.com.br/api-details?apiId=78646d15-2690-42df-9822-93e2860fe708&managerId=1&swaggerVersion=2.0&type=rest&usage=api&Itemid=171)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- ISIN
- Reference Data
- Identifiers

#### Properties

- [Documentation](https://developers.b3.com.br/api-details?apiId=78646d15-2690-42df-9822-93e2860fe708&managerId=1&swaggerVersion=2.0&type=rest&usage=api&Itemid=171)
- [OpenAPI (Swagger 1.1 discovery, harvested)](openapi/b3-exchange-isin-openapi.json)

### Banco B3 APIs

Banco B3 Custody API for operation billing, position reports, and fund quote validation, plus the Settlement API for Pix statement consultation.

- **Human URL:** [https://developers.b3.com.br/apis/bancob3](https://developers.b3.com.br/apis/bancob3)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- Banking
- Custody
- Settlement

#### Properties

- [Documentation](https://developers.b3.com.br/apis/bancob3)

### B3 Insurance (Seguros) APIs

Insurance-segment registration APIs (V3) covering accepted co-insurance registration, claim registration, document registration, and batch processing return with data-quality feedback.

- **Human URL:** [https://developers.b3.com.br/apis/seguros](https://developers.b3.com.br/apis/seguros)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- Insurance
- Claims
- Registration

#### Properties

- [Documentation](https://developers.b3.com.br/apis/seguros)

### B3 Authentication APIs

OAuth 2.0 token issuance APIs used across the B3 API catalog - Client Credentials flows (plain, plus category_ID, key, or scope parameter variants) and Resource Owner Password Credentials flows.

- **Human URL:** [https://developers.b3.com.br/apis/autenticacao](https://developers.b3.com.br/apis/autenticacao)
- **Base URL:** `https://developers.b3.com.br:8065`

#### Tags

- Authentication
- OAuth

#### Properties

- [Documentation](https://developers.b3.com.br/apis/autenticacao)

### B3 Market Data Feed (UMDF)

B3's real-time market data distribution over the Unified Market Data Feed (UMDF) - event-based bid, ask, trade, and statistics data in L1 (top of book) or L2 (full book) depth, real-time or 15-minute delayed, delivered as FIX/FAST and lower-latency Binary SBE multicast streams to authorized distributors and direct connections under commercial contract. Not an HTTP API.

- **Human URL:** [https://www.b3.com.br/en_us/market-data-and-indices/data-services/market-data/](https://www.b3.com.br/en_us/market-data-and-indices/data-services/market-data/)

#### Tags

- Real-Time
- Market Data
- Order Book
- Multicast

#### Properties

- [Documentation](https://www.b3.com.br/en_us/market-data-and-indices/data-services/market-data/)
- [UMDF FIX/FAST Market Data Messaging Specification (PDF)](https://www.b3.com.br/data/files/A4/11/B5/27/B1C6C6106B9896C6DC0D8AA8/UMDF_MarketDataSpecification_v2.1.7.pdf)

### B3 UP2DATA

End-of-day and reference data service covering fixed income, equities, currencies, and debentures for mark-to-market, risk, and pricing workflows - standardized files in TXT, CSV, JSON, or XML delivered daily at predetermined times through client software or a cloud environment, under commercial contract. File-based delivery, not an HTTP API.

- **Human URL:** [https://www.b3.com.br/en_us/market-data-and-indices/data-services/up2data/](https://www.b3.com.br/en_us/market-data-and-indices/data-services/up2data/)

#### Tags

- End of Day
- Reference Data
- Files

#### Properties

- [Documentation](https://www.b3.com.br/en_us/market-data-and-indices/data-services/up2data/)
- [Available Data](https://www.b3.com.br/en_us/market-data-and-indices/data-services/up2data/available-data/)

## Common Properties

- [Website](https://www.b3.com.br/en_us/)
- [Portal](https://developers.b3.com.br/)
- [Documentation](https://developers.b3.com.br/apis)
- [LinkedIn](https://www.linkedin.com/company/b3)
- [Terms of Service](https://www.b3.com.br/en_us/terms-of-use-and-data-protection/)
- [Support](https://developers.b3.com.br/contato)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
