# Doctors Portal — API server (guide for Claude & future me)

Express + MongoDB + Stripe API behind the Doctors Portal client
(github.com/FarhanaShaheed/doctors-portal-client-mui · https://doctors-portal-farhana.vercel.app).

## Run locally
```bash
npm install
cp .env.example .env      # MONGO_URI, STRIPE_SECRET, FIREBASE_SERVICE_ACCOUNT
node index.js             # http://localhost:5000
```

## Config (2026 update)
`index.js` reads **`MONGO_URI`** from the environment first (legacy `DB_USER`/`DB_PASS`
still work as a fallback). The original hard-coded Atlas cluster no longer exists —
create a free cluster at cloud.mongodb.com. Deprecated driver options were removed.
Also needs a Stripe **test** secret key and a Firebase service-account JSON for
verifying ID tokens on protected routes.

## Note
The live client currently runs in **demo mode** (seed JSON + localStorage) because this
API isn't hosted. To go fully live: deploy this server (e.g. Render.com), then set
`REACT_APP_API_BASE` on the client to its HTTPS URL — the real endpoints take over.
