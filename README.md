# Yunick Seeds website

Static site for Yunick Agro / Yunick Seeds, Dabra, Hisar. One HTML page plus images; no build step, no server.

## Publish on GitHub Pages (one time)
1. Create a repository on github.com (e.g. `yunick-seeds`). Upload **all** files in this folder, including the hidden `.nojekyll`, keeping the `assets/` folder as is.
2. Repository → Settings → Pages → Source: "Deploy from a branch" → Branch `main`, folder `/ (root)` → Save.
3. In the same Pages settings enter your domain under "Custom domain" and tick "Enforce HTTPS" once it becomes available (can take up to an hour).
4. At your domain registrar add DNS records:
   - `A` records for `@` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - `CNAME` record for `www` → `<your-github-username>.github.io`
5. Edit the `CNAME` file in this folder so it contains your real domain (one line, no https://).

## Before going live: replace the placeholder domain
`yunickseeds.com` is used as a placeholder in: `index.html` (canonical, og:url, og:image, JSON-LD), `robots.txt`, `sitemap.xml`, `CNAME`. Find-and-replace it with the domain you buy.

## After going live
- Google Search Console: add the domain, verify by DNS, submit `sitemap.xml`.
- Google Business Profile: create/claim "Yunick Agro" with the same address and phone, link the site.
- Add YouTube video IDs to the three video cards (`data-video=""` in index.html).
- Add social links in the footer when you have them (the placeholders were removed so there are no dead links).

## Updating content
Edit `index.html` in a text editor and commit. Images live in `assets/img/`; keep new ones under ~100 KB (WebP, max 1400 px wide).
