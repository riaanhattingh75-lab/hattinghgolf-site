# Hattingh Golf — marketing site (draft)

Static, mobile-first site for **https://www.hattinghgolf.com**. Plain HTML/CSS/minimal JS — no build step.

**Do not deploy or change DNS until Riaan approves.** The live domain currently shows a holding page.

## Pages

| Path | Purpose |
|------|---------|
| `/` | Home — hero, lessons, golf days, **shop**, about, gallery, contact |
| `/lessons/` | Lessons at Colbyn Golf Park |
| `/golf-days/` | Golf days + link to member app |
| `/shop/` | Swing Device (R1 300) & Putting Device (R2 000) — WhatsApp order |
| `/membership/` | Swing Analysis membership — join in app, send videos on WhatsApp |
| `/gallery/` | Photo/video placeholders |
| `/contact/` | WhatsApp, email, map link |

## Branding

Colours and logo match the holding page: charcoal `#0c0d0f`, surface `#141518`, red `#d21f26` / `#a8161c` / `#e03131`, gold `#f2c94c`, Archivo/system font, angled red diagonals. Logo SVG: `images/logo.svg` (also inlined in the header).

## Swap photos

1. Drop files into `images/` (prefer `.jpg` / `.webp`).
2. Keep these names **or** update the `src` in the HTML:

| File | Used on |
|------|---------|
| `images/hero-placeholder.svg` | Home hero (replace with `hero.jpg`) |
| `images/lessons-placeholder.svg` | Lessons / about |
| `images/golf-days-placeholder.svg` | Golf days |
| `images/gallery-1.svg` … `gallery-6.svg` | Gallery |
| `images/og-image.svg` | Social share preview |

Example — home hero after you have a photo:

```html
<img src="images/hero.jpg" width="1600" height="900" alt="…">
```


## Videos (placed)

Compressed web copies live in `images/videos/`; posters in `images/posters/`.

| Placement | File | Notes |
|-----------|------|--------|
| Home hero background | `hero-video01.mp4` + `posters/hero-video01.jpg` (~0:13) | muted, autoplay, loop, playsinline, no audio track |
| Putting Device | `putting-video01.mp4` | same source as hero (video01) |
| Swing Device main | `swing-video03.mp4` | |
| Swing Device alt | `swing-video04.mp4` | |
| Swing “in use” gallery | `swing-gallery-video12/09/10.mp4` | |

**Not used on purpose:** video02, video05, video06 (low quality); video07, video08 (laptop-screen recordings); video11 (duplicate of video02).

## Membership

- Page: `/membership/`
- **Join now** → `https://hattingh-golf.onrender.com/membership` (Expo app Membership tab)
- **Send your swing video** → WhatsApp prefilled message
- Price: placeholder “Price coming soon”
- Consent line on the membership page (public sharing only with member permission + Riaan’s approval)
- Footer: “YouTube channel — coming soon” (no URL yet)

## Shop / WhatsApp orders

No online checkout. Order buttons open WhatsApp with a prefilled message:

- Swing Device (R1 300): `https://wa.me/27842523817?text=Hi%20Riaan%2C%20I'd%20like%20to%20order%20the%20Swing%20Device%20(R1%2C300)`
- Putting Device (R2 000): same pattern with Putting Device / R2,000

Product descriptions are placeholders until real copy arrives.

## Local preview

```bash
cd /workspace/hattinghgolf-site
python3 -m http.server 8765
# open http://127.0.0.1:8765/
```

## Deploy (when approved)

Good fits: GitHub Pages, Netlify, Cloudflare Pages, or any static host.

1. Point the host at this folder (or a GitHub repo of it).
2. Set the custom domain to `www.hattinghgolf.com` / `hattinghgolf.com`.
3. Only then change DNS away from the holding page.
4. Replace `og-image.svg` with a real JPG/PNG for better social previews.
5. Submit `https://www.hattinghgolf.com/sitemap.xml` in Google Search Console.

Member app (golf days / memberships) stays at `https://hattingh-golf.onrender.com` until that stack moves onto the same domain.

## Still needed from Riaan

- Lesson prices & packages
- Swing Analysis membership price
- YouTube channel URL
- Coach bio / credentials (if any to publish)
- Product photos + longer Swing/Putting Device descriptions
- Exact map pin for Colbyn if different from the Google search result
- Business hours / response-time note (optional)
- Go-ahead to deploy and switch DNS

## Contact (live facts)

- WhatsApp: 084 252 3817 → https://wa.me/27842523817
- Email: riaanhattingh75@gmail.com
- Lessons: Colbyn Golf Park, Pretoria
