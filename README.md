# Przelewy24

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
