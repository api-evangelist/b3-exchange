---
name: Look up Tesouro Direto bond reference data
description: Authenticate with OAuth 2.0 client credentials and query Brazilian public bond reference data (bond details, types, indexers, business segments) from the B3 Tesouro Direto Bonds API.
api: openapi/b3-exchange-tesouro-direto-bonds-openapi.json
operations: [BondsGet, TreasuryBondsGet, BondsTypesGet, IndextypesGet, EnumsBusinesssegments1ReqGet]
generated: '2026-07-22'
method: generated
---

# Look up Tesouro Direto bond reference data

Access is B2B: you need contract-issued OAuth client credentials from B3 plus the
B3-issued client certificate (Mutual TLS with certificate pinning). Without a
contract, use the portal Sandbox (pre-registered fictitious responses).

## Steps

1. **Get a token.** POST `client_id`, `client_secret`, `grant_type=client_credentials`
   as form fields to the token endpoint (`/aapi/oauth/token` on your entitled
   gateway host — see `authentication/b3-exchange-authentication.yml`). Send the
   returned `access_token` as `Authorization: Bearer <token>` on every call.
2. **Enumerate the vocabularies first.** `BondsTypesGet` lists public bond types,
   `IndextypesGet` lists indexers (e.g. Selic, IPCA), and
   `EnumsBusinesssegments1ReqGet` lists business segments — use these enums to
   interpret and filter bond records.
3. **List bonds.** `BondsGet` (`GET /homebroker/api/bonds/v1/`) returns the bond
   catalog with name, maturity, Selic code, and platform identifiers; responses
   are paginated with `links` (self/first/prev/next) and `meta`
   (totalPages/totalRecords).
4. **Fetch one bond.** `TreasuryBondsGet`
   (`GET /homebroker/api/bonds/v1/{treasuryBondCode}`) returns detail for a
   single treasury bond code.

## Rules

- Errors arrive as `{"errors": [{"code", "title", "detail"}]}`; 422 means a
  business-rule violation, 429 means you exceeded the contract throttle —
  back off before retrying (see `errors/b3-exchange-problem-types.yml`).
- There is no idempotency-key contract; these are read-only GET operations.
