# Adarsh Thapa — personal site

Static HTML/CSS/JS. No build step, no dependencies.

## Run locally
`python3 -m http.server 8000` then open http://localhost:8000

## Fill in
Search for `to confirm`, `YOUR_EMAIL`, and the screenshot placeholders in `index.html`. Add images to `assets/`. Add a Resume link in the nav once a real CV exists. Add `og.svg`/`og.png` (1200×630) and update the `og:image` tag.

## Deploy (GitHub Pages)
1. Create a repo, push this folder to `main`.
2. Settings → Pages → Source: **GitHub Actions**. The workflow in `.github/workflows/pages.yml` deploys on every push.
3. Settings → Pages → Custom domain: `adarshthapa.info.np` (the `CNAME` file already holds it).

## DNS (Cloudflare) — add records only, do not change nameservers
Apex `adarshthapa.info.np`:
- A → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- AAAA → 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153
Optional `www`: CNAME → `<your-github-username>.github.io`
Set these records to **DNS only** (grey cloud) until GitHub issues the certificate, then tick **Enforce HTTPS**. Verify the IPs against GitHub's current docs before adding.

## Troubleshooting
- Certificate pending: wait up to ~1 hour; remove and re-add the custom domain.
- Check records: `dig adarshthapa.info.np +short`
- Redirect loop with Cloudflare proxy: set SSL/TLS mode to Full.
# My_profile
# My_profile
