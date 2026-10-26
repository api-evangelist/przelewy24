# Przelewy24

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

Przelewy24 is Poland's leading online payment gateway with 91% brand recognition among Polish online consumers. The platform provides REST APIs enabling e-commerce merchants to accept payments via online bank transfers from 165+ Polish banks, credit and debit cards (Visa, Mastercard), BLIK mobile payments, Google Pay, digital wallets, and prepaid cards. Przelewy24 supports PLN and EUR currencies and is widely used by Polish and international merchants targeting the Polish market.

**Developer Portal:** https://developers.przelewy24.pl/

## APIs

| API | Description | Docs |
|-----|-------------|------|
| Przelewy24 REST API | Core payment gateway API for transaction registration, verification, card payments, refunds, and payment methods | https://developers.przelewy24.pl/ |
| Przelewy24 Marketplace API | Split payments and multi-vendor routing for marketplace platforms | https://developers.przelewy24.pl/marketplace/ |
| Przelewy24 Extended API | Advanced reporting, batch operations, and enterprise features | https://developers.przelewy24.pl/extended/ |
| Przelewy24 Ekspres API | One-click fast-pay for returning authenticated Przelewy24 users | https://developers.przelewy24.pl/ekspres/ |

## Key Endpoints (REST API v1)

| Method | Endpoint | Purpose |
|--------|----------|---------|
| GET | /api/v1/testAccess | Verify API connectivity |
| GET | /api/v1/payment/methods | List available payment methods |
| POST | /api/v1/transaction/register | Register a new payment transaction |
| PUT | /api/v1/transaction/verify | Verify a completed transaction |
| POST | /api/v1/transaction/refund | Process a refund |
| GET | /api/v1/transaction/by/sessionId | Retrieve transaction by session ID |
| POST | /api/v1/card/info | Get card information |
| POST | /api/v1/card/pay | Initiate card payment |
| POST | /api/v1/card/charge | Charge a card |
| POST | /api/v1/card/chargeWith3ds | Charge a card with 3D Secure |
| POST | /api/v1/transaction/registerOffline | Register offline transaction |

## Authentication

HTTP Basic Authentication using POS ID (username) and API Key (password). Transaction integrity is secured via SHA-384 signatures generated from the session ID, merchant ID, amount, currency, and CRC key.

## Environments

- **Production:** `https://secure.przelewy24.pl/api/v1`
- **Sandbox:** `https://sandbox.przelewy24.pl/api/v1`

## Pricing

- No monthly subscription fees
- No integration fees
- One-time activation fee: PLN 59 (refundable after 10 transactions in 2 months)
- Bank transfer commission: ~1.9% per transaction
- Card payment commission: 1.29% + PLN 0.30 per transaction
- BLIK commission: ~1.9% per transaction
- New merchants may qualify for 0% card commission for 12 months via Polska Bezgotówkowa program

## Resources

- [Developer Documentation](https://developers.przelewy24.pl/)
- [Commissions and Fees](https://www.przelewy24.pl/en/offer/commissions-and-fees)
- [Start Cooperation / Sign Up](https://www.przelewy24.pl/en/start-cooperation)
- [Payment Methods](https://www.przelewy24.pl/en/payment-methods)
- [API Technical Support](https://www.przelewy24.pl/en/help-center/api-technical-support)
- [Status Page](https://status.przelewy24.pl/)
- [Partner Program](https://www.przelewy24.pl/en/partner-program)
