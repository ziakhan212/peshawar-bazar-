# Peshawar Bazar — Android APK testing

This project is configured for an installable Android APK using Expo EAS.

## Build an APK
1. Install Node.js 20+.
2. From this project folder run: `npm install` (or `pnpm install` if your workspace uses pnpm).
3. Install/login to EAS CLI: `npx eas-cli@latest login`
4. Build the test APK: `npx eas-cli@latest build --platform android --profile preview`
5. When the build finishes, open the build URL on your Android phone and install the APK.

## Important for online/email verification
The APK needs the deployed API URL. Set `EXPO_PUBLIC_API_URL` to the public HTTPS URL of the Peshawar Bazar server before building. The server also needs its SMTP settings configured for email verification.
