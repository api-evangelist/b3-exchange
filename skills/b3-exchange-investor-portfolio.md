---
name: Retrieve an investor's consolidated portfolio
description: Pull D-1 positions and account movements for a consented investor (CPF/CNPJ) across equities, fixed income, treasury bonds, securities lending, and derivatives from the B3 Investor Area APIs.
api: openapi/b3-exchange-investor-position-openapi.json
operations: [EquitiesPositionGet, FixedIncomePositionGet, TreasuryBondsPositionGet, SecurityLendingPositionGet, DerivativesSwapPositionGet, EquitiesMovementGet, FixedIncomeMovementGet, TreasuryBondsMovementGet, SecuritiesLendingMovementGet, DerivativesGet]
generated: '2026-07-22'
method: generated
---

# Retrieve an investor's consolidated portfolio

For authorized fintechs and custodians only: data is served under OAuth 2.0
with investor consent (STVM request/response authorization flows), D-1
(previous business day), keyed by the investor's `documentNumber` (CPF/CNPJ).

## Steps

1. **Authenticate** with contract-issued OAuth client credentials
   (`Authorization: Bearer <token>`; Mutual TLS applies in production).
   Consent for the investor must already exist via the STVM authorization
   APIs.
2. **Positions (balance per asset class).** Call the five position operations
   with the investor's `documentNumber`
   (`GET /api/position/v3/<asset-class>/investors/{documentNumber}`):
   `EquitiesPositionGet`, `FixedIncomePositionGet`, `TreasuryBondsPositionGet`,
   `SecurityLendingPositionGet`, `DerivativesSwapPositionGet`. Positions may
   include liens (judicial blocks, guarantees, technical reserves).
3. **Movements (account history).** Call the movement operations
   (`GET /api/movement/v2/<asset-class>/investors/{documentNumber}`):
   `EquitiesMovementGet`, `FixedIncomeMovementGet`, `TreasuryBondsMovementGet`,
   `SecuritiesLendingMovementGet`, `DerivativesGet` — debits and credits
   (custody transfers, settlements, corporate events) for the queried period.
4. **Paginate** with the `links`/`meta` envelope until `next` is absent, then
   merge per asset class into the consolidated view.

## Rules

- 401 means the token or consent is invalid; 422 is a business-rule error —
  surface `errors[].code/title/detail` to the operator.
- Data is D-1: never present it as real-time.
- Respect the contract throttle: on 429 back off before retrying.
