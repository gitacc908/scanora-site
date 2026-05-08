# Scanora Landing Site

Static, isolated landing/legal site for `scanora.space`.

## Local Preview

```bash
cd landing
python3 -m http.server 4173
```

Open `http://localhost:4173`.

## Pages

- `/` - landing page
- `/download/` - download CTA redirect
- `/support.html` and `/support/` - support/help center
- `/privacy.html` and `/privacy/` - privacy policy
- `/terms.html` and `/terms/` - terms of service

Use these in RevenueCat/App Store metadata:

- Support: `https://scanora.space/support`
- Privacy: `https://scanora.space/privacy`
- Terms: `https://scanora.space/terms`

## GitHub Pages Setup

Fastest path: create a separate public GitHub repo for the landing site, copy the contents of this
folder to that repo root, then enable GitHub Pages from the `main` branch root.

Custom domain:

1. In GitHub repo settings, open Pages.
2. Set custom domain to `scanora.space`.
3. Keep the included `CNAME` file.
4. In your DNS provider, add GitHub Pages records for the apex domain:
   - `A @ 185.199.108.153`
   - `A @ 185.199.109.153`
   - `A @ 185.199.110.153`
   - `A @ 185.199.111.153`
5. Optional but recommended: add `www`:
   - `CNAME www YOUR_GITHUB_USERNAME.github.io`
6. Wait for DNS propagation, then enable Enforce HTTPS in GitHub Pages.

Also set up email forwarding for `support@scanora.space` before App Store submission.
