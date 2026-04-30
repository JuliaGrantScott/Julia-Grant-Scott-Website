# Deploy workflow — Julia Grant-Scott Website

This is a one-page static site (`index.html`) hosted on Vercel and connected to this GitHub repo. Every push to `main` triggers an automatic redeploy.

## URLs

- **Live (custom domain):** https://www.juliagrantscott.com (apex 307-redirects to www)
- **Vercel preview:** https://julia-grant-scott-website-git-main-julabye-5478s-projects.vercel.app
- **Repo:** https://github.com/JuliaGrantScott/Julia-Grant-Scott-Website
- **Vercel project ID:** `prj_xztijmaKIVD63R7hsCqeaKa6y0lt` (team `julabye-5478`)

## Editing rule

**Always edit `index.html` directly in this folder** (`/Users/juliagrantscott/Documents/GitHub/Julia Grant Scott Website/`).

Do NOT edit copies in `/Users/juliagrantscott/Documents/Claude/Projects/Website/` and then forget to copy them over — that was the old, lossy workflow. The Claude-Projects folder is for assets and reference material only.

## Push & deploy (the only manual step)

1. Open GitHub Desktop.
2. Confirm the changed files in the diff view.
3. Write a short summary, click **Commit to main**.
4. Click **Push origin**.
5. Vercel auto-redeploys within ~30 seconds. Hard-refresh the live URL to verify.

That's it — no separate Vercel step, no DNS work, no SSL renewal. Vercel handles all of that.

## DNS (already configured, do not change)

Domains attached to the Vercel project: `juliagrantscott.com` and `www.juliagrantscott.com`. `www` is the primary; apex 307-redirects.

DNS records at Squarespace Domains:
- Apex `@` → A → `216.198.79.1`
- `www` → CNAME → `4ad7efa5d786bffc.vercel-dns-017.com`

## What's in this repo

- `index.html` — the entire site (single-file HTML/CSS/JS, mobile responsive)
- `favicon/` — favicon set
- `.gitattributes`
- `DEPLOY.md` — this file

## When asking Claude to make changes

Tell Claude: *"edit index.html in the Julia Grant Scott Website repo"* — Claude will edit directly in this folder, you push via GitHub Desktop, Vercel handles the rest.
