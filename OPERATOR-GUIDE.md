# Operator Guide — Julia Grant Scott Website

For Sush. Skim before each working session. Pair with `CLAUDE.md` (the AI co-pilot that auto-loads when you open Cowork in this folder).

Domain: **juliascott.com**
Brand: **BRAHMAMA / Julia Grant Scott**

---

## Files in this folder

| File | Purpose | Edited by |
|---|---|---|
| `index.html` | The website | You (build sessions) |
| `CLAUDE.md` | AI co-pilot instructions | Claude (auto-loaded) |
| `BRAND.md` | Julia's brand bible — colours, fonts, voice | Update if brand evolves |
| `BRIEF.md` | Project scope, audience, retreat goals | Update if scope changes |
| `OPERATOR-GUIDE.md` | This file — your runbook | You |
| `DEPLOY-STATE.md` | Auto-maintained deployment progress | Claude |

---

## Before each working session

- Open Cowork **in this folder**, not in a parent folder. Context isolation depends on it.
- The first thing Claude does is read `BRAND.md` + `BRIEF.md` + `DEPLOY-STATE.md`. Don't restate these to it — it already knows.
- For build / design work: open a separate Cowork session and tell it explicitly *"this is a build session, edit `index.html` directly"* — the deployment co-pilot is intentionally scoped to deploys.

---

## Before sitting down with Julia for deployment

Gather:

- **Julia's email** for GitHub + Vercel signups (must be hers, not yours — she owns the infra long-term).
- **Domain registrar login** for `juliascott.com` (Namecheap, Porkbun, GoDaddy — confirm where she bought it).
- **GitHub Desktop installed** on her Mac (`Applications/GitHub Desktop.app`).
- **~60 min time block** with her, plus 15–30 min DNS wait in the middle.

---

## Deployment phases at a glance

| # | Phase | Where | Time |
|---|---|---|---|
| 1 | `index.html` in folder | Her Mac | 2 min |
| 2 | GitHub repo (public, Julia's account) | Her Mac + github.com | 10 min |
| 3 | Vercel project import + first deploy | vercel.com | 5 min |
| 4 | Custom domain + DNS at registrar | vercel.com + registrar | 10 min + DNS wait |
| 5 | SSL padlock + verification | Browser | 5 min |

`CLAUDE.md` walks you through each phase one step at a time when you say "I'm ready to deploy".

---

## Gotchas specific to this client

- **The brand pivot is sensitive.** The site replaces (or strongly competes with) Julia's existing presence on John Scott Yoga's page. Make sure the launch plan includes either delisting JSY retreats or pointing them at `juliascott.com`. Don't go live without aligning on this with Julia first.
- **No stock photography.** Only Julia's own imagery. If she sends placeholders, mark them as placeholders in the HTML so they don't accidentally ship.
- **Devanagari font preload** must be in the `<head>` or the page will FOIT (text invisible until fonts load) and that breaks the devotional feeling.
- **Sindoor `#C9301E` is the brand red, not a generic red.** Don't substitute. Same with Cream `#F6E9D2`.
- **Voice drift is the biggest risk.** Every time you ask Claude to write or edit copy, it should check `BRAND.md` voice rules. If it slips into "lifestyle influencer" or "teacher tone", call it out and ask for a rewrite.

---

## Multi-machine setup (Sush + Julia)

After Phase 2 finishes, get added as a collaborator:

1. Julia goes to her GitHub repo → **Settings → Collaborators → Add people** → add Sush's GitHub username.
2. Sush accepts invite → in her GitHub Desktop: **File → Clone Repository** → select the repo → clone to `Documents/GitHub/juliascott-website` on her Mac.

Now both can edit. **Discipline: always Fetch/Pull origin before starting any edit.**

---

## Post-launch: the update loop

Every change after launch:

1. Edit `index.html` (or whatever file).
2. GitHub Desktop auto-detects change.
3. Short, descriptive commit message ("Add July retreat dates", "Update About copy with new opening line").
4. **Commit to main** → **Push origin**.
5. Wait ~30 sec → refresh `juliascott.com`.

---

## Things to set up post-launch (week 1)

- Smoke-test enquiry form by submitting from your phone. Confirm Julia receives the email.
- Send the live URL to a small trusted circle for sanity-check before any wider announce.
- Update Julia's Instagram bio link to `juliascott.com`.
- Decide John Scott Yoga retreat listings: delist or link-across.
- Set a 30-day post-launch check-in to review enquiries vs. expectation.

---

## Troubleshooting quick reference

| Symptom | Fix |
|---|---|
| GitHub Desktop "no changes" after edits | Wrong folder — files saved somewhere else. Verify repo path. |
| Vercel build fails | Missing `index.html` or empty repo. Check Vercel deploy log. |
| Domain "Invalid Configuration" >2 hrs | DNS conflict at registrar. Delete old `A` records first. |
| Apex works, `www` doesn't (or vice versa) | Missing the second DNS record. Add it. |
| Padlock missing 30+ min after DNS green | Click **Refresh** on the domain in Vercel settings. |
| Copy reads "off" | Run it back through `BRAND.md` voice check. Most common slip: teacher-tone. |
