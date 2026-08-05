# Changelog

## [1.1.0] — 2026-08-05
### Changed
- `MONGO_URI` is now read from the environment (the old hard-coded Atlas cluster is dead).
- Removed deprecated MongoDB driver options.
### Added
- `.env.example` documenting MONGO_URI, STRIPE_SECRET and FIREBASE_SERVICE_ACCOUNT.

## [1.0.0] — 2021-11
- Original Express + MongoDB + Stripe API with firebase-admin token verification.
