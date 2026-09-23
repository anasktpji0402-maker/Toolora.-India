# TOOLORA
Everyday tools. One simple place.

## Run
`npm install`
`npm run dev`
`npm run build`
`npm run preview`

## Configuration
Copy `.env.example` to `.env`. `VITE_*` variables are public. Never put AI secrets in a `VITE_` variable; secure AI routes should read server environment variables such as `AI_API_KEY`.

- `VITE_SITE_URL`: canonical site origin.
- `VITE_GA4_MEASUREMENT_ID`: optional GA4 measurement ID; analytics is skipped when empty.
- `VITE_ADSENSE_PUBLISHER_ID`: optional legitimate AdSense publisher ID; ad slots remain empty otherwise.
- `AI_API_BASE_URL` / `AI_API_KEY`: server-side configuration for future AI routes. This Vite-only frontend intentionally never exposes the secret.
- `CONTACT_API_URL`: optional backend endpoint. The contact form never claims delivery unless configured.

## PWA
Vite PWA generates the service worker and manifest at build time. Install prompts are shown only when the browser exposes an install event.

## Privacy
Image, text, calculator, QR and developer operations run locally. File tools use browser processing where supported. No file is uploaded by this frontend.

## Deployment
Deploy the generated `dist/` to Vercel, Netlify, Cloudflare Pages or Firebase Hosting. If you add server AI/contact routes, deploy them on a platform that supports serverless/API routes and keep secrets server-side.

## AdSense
Set a real publisher ID only after creating the AdSense account and implementing Google's current publisher script/consent requirements. This project provides non-misleading `AdSlot` placeholders and does not fabricate ads or clicks.
