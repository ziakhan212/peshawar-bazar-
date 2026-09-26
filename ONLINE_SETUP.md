# Online launch setup

This build is no longer a demo-only marketplace. It uses a server API for accounts, listings, reports and admin authentication.

## Server secrets
Set these environment variables on the server before production:
- `ADMIN_USERNAME` — your admin username
- `ADMIN_PASSWORD` — a long unique admin password (do not put it in app source)
- `PORT` — supplied by your hosting provider

## App API URL
Set `EXPO_PUBLIC_API_URL` to the public HTTPS URL of the server. If the Expo/Replit app and API are deployed on the same domain, the app can use `EXPO_PUBLIC_DOMAIN` automatically.

## Run
`pnpm server`

The server exposes `/api/health`, `/api/auth/register`, `/api/auth/login`, `/api/listings`, `/api/reports` and admin endpoints. User passwords are stored as salted scrypt hashes. Listings and reports persist in `server/data.json` on the server.

For serious scale, move `server/data.json` to a managed database and image storage before a large public launch.


## Email verification
Set SMTP_HOST, SMTP_PORT, SMTP_USER, SMTP_PASS and optionally SMTP_FROM on the server. New accounts receive a 6-digit code that expires after 10 minutes. Codes are stored hashed and limited to five attempts. Users must verify before they can sign in.
