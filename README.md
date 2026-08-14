# Mega Mission Media — v2

Single-page site. Anchor navigation. Deploy to Vercel via GitHub.

---

## BEFORE YOU DEPLOY — 3 things left

### 1. Booking link (required)
`index.html`, in the CONFIG block near the bottom:

```js
bookingUrl : "https://calendar.app.google/7EeEp5VeZZvSwdrE6",
```

Paste your Google Workspace booking page URL. Every "Book a Call" button on
the page pulls from this one line. Until it's replaced, those buttons scroll
to the contact form instead — nothing breaks.

To swap a demo build over to Cal.com later, change this one line.

### 2. Google Analytics (required)
Replace `G-XXXXXXXXXX` — appears twice in the `<head>`.

### 3. Testimonial quotes (required before launch)
Section B08. All four are placeholders in square brackets.
**Get written permission from each person before publishing their words.**

### 4. Ride & Share videos (required before launch)
Section B10. Replace `VIDEO_ID_1/2/3` with real YouTube IDs — six places
total (three links, three thumbnails). Thumbnails pull from YouTube, so
they stay current automatically.

---

## Optional but worth doing

- **Work screenshots** — B07 has three grey placeholder panels. Drop in
  `assets/work-yoel.jpg`, `work-cowtown.jpg`, `work-4tec.jpg` (16:9) and
  replace the `<div class="work-shot">` with an `<img>`.
- **Live site URLs** — Cowtown and 4Tec "Visit Website" buttons point at the
  contact form. Marked `data-href-todo`.
- **Social links** — footer icons are `href="#"`.

---

## Structure

| Block | Section |
|-------|---------|
| HDR | Sticky nav + Book a Call |
| B01 | Hero — headline, proof, photo |
| B02 | Ticker |
| B03 | Client strip |
| B04 | Services — Brand / House / Run |
| B05 | How We Work — the Roadmap |
| B06 | Ticker |
| B07 | Work carousel |
| B08 | Testimonials carousel |
| B09 | Meet the Founder |
| B10 | Ride & Share video wall |
| B11 | Ticker + CTA band + contact form |
| FTR | Four-column footer |

## Design tokens

| | |
|---|---|
| Bone | `#FAF7F2` |
| Ink | `#14100E` |
| Gold | `#F0B429` |
| Signal red | `#C8102E` |
| Teal | `#0D9488` (footer only) |
| Display | Archivo Black |
| Body | DM Sans |
| Utility | Archivo 600/700 |

Fonts are self-hosted in `/fonts` — no Google Fonts request, faster load,
nothing to break if Google changes an endpoint.

## Notes

- Contact form posts to Formspree `xgawvlvb` → susy@megamissionmedia.com
- No pricing anywhere on the page
- Tickers pause on hover; all motion respects `prefers-reduced-motion`
- Hero photo: background removed automatically. Check the hair edges at full
  size — if you want them sharper, send the original to Cheshire.
