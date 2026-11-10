# Designer Hub

Login with Google and LinkedIn, then a protected dashboard.

## 1. Get keys
**Google**: console.cloud.google.com > APIs & Services > Credentials > OAuth client ID (Web).
Redirect URI: `https://YOUR-SITE/api/auth/callback/google` (and `http://localhost:3000/api/auth/callback/google` for testing).

**LinkedIn**: developer.linkedin.com > Create app > Products > add "Sign In with LinkedIn using OpenID Connect".
Auth tab > Redirect URL: `https://YOUR-SITE/api/auth/callback/linkedin` (and localhost one).

## 2. Run locally
    npm install
    copy .env.example to .env.local and fill it in
    npm run dev      # http://localhost:3000

## 3. Put it online (free)
Upload this folder to GitHub, import it in vercel.com, add the same values from .env.local in
Project > Settings > Environment Variables (set NEXTAUTH_URL to your Vercel address), then Deploy.
Add that Vercel address's redirect URIs in Google and LinkedIn too.
