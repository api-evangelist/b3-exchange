---
name: Manage a securities lending offer lifecycle
description: Read the securities lending book, place an offer, track its status, close a trade directly or hit an existing offer, and cancel — via the B3 Securities Lending (Empréstimo de Ativos) v2 API.
api: openapi/b3-exchange-securities-lending-openapi.json
operations: [TopOfferReq, ListOfferReq, EntryOfferReq, StatusOfferReq, OfferReq, CancellationOfferReq, HitLenderOfferrReq, HitBorrowerOfferReq, DirectOfferReq, TradeReq, StatusTradeReq]
generated: '2026-07-22'
method: generated
---

# Manage a securities lending offer lifecycle

Contract-gated write API for lending-market participants. Every path is
parameterized by `securityLendingModality` and most by `tickerSymbol`.

## Steps

1. **Authenticate** with contract OAuth client credentials
   (`Authorization: Bearer <token>`, scopes resource.READ/resource.WRITE,
   Mutual TLS in production).
2. **Read the book.** `TopOfferReq` returns the best offer per instrument;
   `ListOfferReq` returns book depth for public offers of an instrument.
3. **Place an offer.** `EntryOfferReq`
   (`POST /api/securities-lending/v2/offers/entries/{securityLendingModality}`)
   sends an offer to the public or private book. Capture the returned
   `offeringNumber`.
4. **Track it.** `StatusOfferReq` polls offer status by `offeringNumber`;
   `OfferReq` returns the full offer record.
5. **Close a trade.** Either hit a resting offer — `HitLenderOfferrReq`
   (aggress a lender offer) / `HitBorrowerOfferReq` (aggress a borrower
   offer) — or negotiate bilaterally with `DirectOfferReq` (direct closing).
6. **Confirm the trade.** `StatusTradeReq` polls by
   `securitiesFinancingTradeIdentification`; `TradeReq` returns the trade
   record.
7. **Cancel if needed.** `CancellationOfferReq`
   (`PUT /api/securities-lending/v2/offers/cancellations/{offeringNumber}`)
   removes the offer from the book.

## Rules

- Writes have no idempotency-key contract: after a timeout on
  `EntryOfferReq`/`DirectOfferReq`, reconcile with `StatusOfferReq`/
  `StatusTradeReq` before resending to avoid duplicate offers.
- 422 carries business-rule rejections in `errors[].code/title/detail`;
  429 means the contract throttle tripped — back off.
