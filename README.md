# christierugh.com

Personal executive site for Christie Rugh — commercial & global growth executive.

## Structure
- `index.html` — the full site (single-page, no build step required)
- `images/christie-rugh.jpg` — headshot used in the hero section
- `CNAME` — tells GitHub Pages to serve this repo at christierugh.com
- `.nojekyll` — tells GitHub Pages to skip Jekyll processing and serve files as-is

## Editing
Open `index.html` and search for `const CONFIG = {` near the bottom (inside the `<script>` tag) to update the photo path or email address. Everything else (copy, numbers, case studies) is plain HTML/CSS in the same file — search for the section you want to change.

## Deploying (GitHub Pages)
This repo is meant to be pushed to `christierugh/christierugh.github.io` (a GitHub "user site" repo — the special name that makes GitHub Pages serve it automatically).

1. Push this repo's contents to the `main` branch of `christierugh/christierugh.github.io`.
2. In the repo, go to **Settings → Pages** and confirm the source is the `main` branch, root folder.
3. Under **Settings → Pages → Custom domain**, enter `christierugh.com` and save (this writes the CNAME file automatically if it isn't already there — it already is, in this repo).
4. At your domain registrar (wherever christierugh.com is registered), add these DNS records so the domain points to GitHub Pages:

   **A records** (for the apex domain `christierugh.com`), pointing to GitHub Pages' IPs:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153

   **CNAME record** (for `www.christierugh.com`, optional but recommended):
   - `www` → `christierugh.github.io`

5. DNS changes can take anywhere from a few minutes to 24 hours to propagate. Once they do, check the "Enforce HTTPS" box in Settings → Pages so the site serves over `https://christierugh.com`.

<!-- redeploy: republish latest main (2026-07-02) -->
