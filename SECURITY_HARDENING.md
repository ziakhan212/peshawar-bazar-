# Peshawar Bazar security hardening

- Admin Panel is no longer shown inside the customer Profile/app navigation.
- Admin API endpoints remain protected by a server-issued admin session token and role checks.
- Admin sessions expire after 8 hours; customer/company sessions retain a 24-hour lifetime.
- Admin login is rate-limited to 5 failed attempts per IP per 15 minutes.
- Admin credentials are server-only environment variables and are never bundled in the mobile app.
- API responses use `Cache-Control: no-store` and `X-Content-Type-Options: nosniff`.
- Set `CORS_ORIGIN` to the exact trusted origin in production.

Important: use HTTPS in production and set a long random ADMIN_USERNAME/ADMIN_PASSWORD. Do not put these secrets in Expo/public environment variables.
