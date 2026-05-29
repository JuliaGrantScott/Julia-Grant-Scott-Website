# BRAHMAMA Web — Meta Pixel Installation Handoff

**Date:** 27 May 2026  
**Prepared by:** Sush (via Claude / Cowork)  
**For:** Julia Grant Scott / BRAHMAMA

---

## Pixel Details

| Field | Value |
|---|---|
| Pixel name | BRAHMAMA Web |
| Pixel ID | `1319334359528637` |
| Business Portfolio | Sushmitha (business_id: 325594068209085) |
| Created | 27 May 2026 |
| Status | Code installed — pending first deployment to go live |

---

## What Was Installed

The standard Meta Pixel base code (PageView tracking) was added to the `<head>` of every HTML page on the site. It fires a `PageView` event every time any page loads.

### Pixel code installed on all pages

```html
<!-- Meta Pixel Code -->
<script>
!function(f,b,e,v,n,t,s)
{if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};
if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version="2.0";
n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];
s.parentNode.insertBefore(t,s)}(window, document,"script",
"https://connect.facebook.net/en_US/fbevents.js");
fbq("init", "1319334359528637");
fbq("track", "PageView");
</script>
<noscript><img height="1" width="1" style="display:none"
src="https://www.facebook.com/tr?id=1319334359528637&ev=PageView&noscript=1"
/></noscript>
<!-- End Meta Pixel Code -->
```

### Pages updated (13 files)

| File | Page |
|---|---|
| `index.html` | Home |
| `breath-of-life-andalusia.html` | Breath of Life — Andalusia retreat |
| `alpine-lumiere-freiburg.html` | Lumière Alpine — Freiburg retreat |
| `return-to-roots-poland.html` | Return to Roots — Poland retreat |
| `long-slow-deep-poland.html` | Long Slow Deep — Poland retreat |
| `swiss-sanctuary-retreat.html` | Swiss Sanctuary retreat |
| `joie-de-vivre-paris.html` | Joie de Vivre — Paris retreat |
| `sunkissed-sardinia-retreat.html` | Sunkissed Sardinia retreat |
| `colibri-festival-corfu.html` | Colibri Festival — Corfu retreat |
| `mother-india-yatra-2027.html` | Mother India Yatra 2027 |
| `thank-you.html` | Thank You page |
| `privacy-policy.html` | Privacy Policy |
| `terms-and-conditions.html` | Terms & Conditions |

---

## Where to Find the Pixel in Meta

1. Go to [business.facebook.com](https://business.facebook.com)
2. Switch to the **Sushmitha** Business Portfolio
3. Navigate to **Events Manager → Datasets**
4. Find **BRAHMAMA Web** — ID `1319334359528637`

Direct link:  
`https://eventsmanager.facebook.com/events_manager2/overview?business_id=325594068209085`

---

## How to Verify It's Firing (Once Live)

**Option 1 — Meta Pixel Helper (recommended)**  
Install the free [Meta Pixel Helper](https://chrome.google.com/webstore/detail/meta-pixel-helper/fdgfkebogiimcoedlicjlajpkdmockpc) Chrome extension. Visit any page on juliascott.com — the extension icon will turn green and show `PageView` if the pixel is firing correctly.

**Option 2 — Events Manager test events**  
In Events Manager, open the BRAHMAMA Web dataset → **Test Events** tab → enter the live URL and click **Open Website**. Meta will show real-time events as you browse.

**Option 3 — Browser network tab**  
Open DevTools → Network tab → filter by `facebook.net`. A successful request to `connect.facebook.net/en_US/fbevents.js` confirms the pixel loaded.

---

## Next Step Required

The pixel code is in the local files but **the site has not yet been pushed to Vercel**. The pixel will not fire until the site is deployed.

To go live:
1. Open **GitHub Desktop**
2. You will see all 13 files listed as changed
3. Commit message: `Add BRAHMAMA Web Meta Pixel to all pages`
4. Click **Push origin**
5. Vercel will redeploy in ~30 seconds
6. Verify with Meta Pixel Helper on juliascott.com

---

## Notes

- The pixel lives under Sushmitha's Business Portfolio (not Julia's personal account) because creating web pixels requires a Business Portfolio. Julia does not currently have one.
- If Julia sets up her own Business Portfolio in future, the pixel can be transferred via Meta Business Settings → Data Sources.
- No Conversions API was set up — just the browser pixel for now. CAPI can be added later for more robust tracking.
