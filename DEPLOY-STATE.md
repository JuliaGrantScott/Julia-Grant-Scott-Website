# Deployment State — juliascott.com

Auto-maintained by Claude. Hand-update only if Claude is wrong.

---

Client: Julia Grant Scott
Brand: BRAHMAMA
Domain: juliascott.com
Registrar: _________ (to fill)
GitHub repo: _________ (to fill in Phase 2)
Vercel project: _________ (to fill in Phase 3)
Live URL: https://juliascott.com (once Phase 5 completes)

---

## Progress

- [ ] Phase 1 — `index.html` in this folder
- [ ] Phase 2 — GitHub repo created, first commit pushed
- [ ] Phase 3 — Vercel project imported, `.vercel.app` URL live
- [ ] Phase 4 — Custom domain added in Vercel + DNS records at registrar
- [ ] Phase 5 — SSL padlock confirmed, mobile tested

---

## Notes

(Anything worth remembering for the next session — open questions, things Julia asked to revisit, registrar quirks, etc.)

### 2026-05-22 — Home page edits (Sush)

- **Purna crown:** added three-dot ornaments before/after the *Purna* label on the conviction strip (marigold dots, brand three-dot signature).
- **Retreat rename:** *Alpine Lumière* → *Lumière Alpine* everywhere on `index.html` (retreat card title, enquire-form `<option>`, footer nav). URL slug `alpine-lumiere-freiburg` kept as-is to preserve the existing Vercel redirect (`/Freiburg_Landing → /alpine-lumiere-freiburg`) and any inbound links. If Julia wants the slug renamed too, that's a separate task — needs a 301 added in `vercel.json`.
- **Sanskrit invocation** *सत्यं · शिवं · सुन्दरम्* (Satyam · Śivam · Sundaram — Truth · Auspiciousness · Beauty) added at the top of the closing bio-strip (the "You can be a victim or the Creator" photo). Placed there because the second screenshot wasn't actually attached to the message — closing strip was the strongest guess. Easy to move if it's the wrong section.
- **Body type size:** bumped base body from `17px / 1.85` → `19px / 1.78` on **every** HTML page in the folder (12 files updated; the stale `Breath of Life Carousel - Edited.html` was skipped — pattern didn't match). `BRAND.md` §1 updated with the new body-size guidance so the brand kit stays in sync.
- **About section image:** swapped `About Julia.png` → `About Me.jpg`.
- **About section copy:** replaced the bio prose with Julia's new long-form text. Added two centred sindoor-italic refrain lines (*"It is all my heritage."* and *"And also — just a story."*) and a Devanagari-font sign-off in marigold-red — *With all my love, Julia*. The hidden `copyBio()` clipboard function was updated to match.
- **Yantra ornament:** added a subtle marigold-outlined Sri Yantra SVG (outer square + 16-petal lotus + 8-petal lotus + 9 interlocking triangles + bindu) above the About section portrait. Breathes between 42–62% opacity on a slow 9s loop.
- **Testimonials:** Miro testimonial author is now *Miro · Montenegro*.

### Open questions / things to confirm with Julia
- The Sanskrit was placed on the closing strip — confirm that's the section she meant in the (missing) second screenshot.
- Slug for the Freiburg retreat (`alpine-lumiere-freiburg`) is unchanged. If she wants the URL renamed, add a redirect in `vercel.json`.
