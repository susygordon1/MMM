# Mega Mission Media — Update Log

Drop `index.html` and `susy-story.jpg` into your repo, replacing the old
index.html. Everything else in the repo stays as-is.

---

## What changed

### Palette — teal is now primary
- `--teal` is now **#22E0E0** (hot cyan) instead of #5EEAD4
- Gold **retired**. `--gold` and `--gold-dim` are aliased to teal so nothing
  breaks — no markup had to change. Delete the aliases whenever you like.
- New: `--paper` #F5F8F8 (light ground), `--ink` #0B0F10 (type on light),
  `--teal-deep` #0E9EA0 (teal that stays readable on white)

### Sections now alternate dark and light
Hero (dark) → Roadmap (**light**) → Portfolio (dark) → Story (dark) →
Ride & Share (**light**) → Reviews (dark) → Booking (**light**) →
CTA (dark) → Contact (**light**) → Footer (dark)

This is what makes the teal pop. Black everywhere gave it nothing to pop against.

### Roadmap — short lists, phase names kept
Foundation / Growth / Authority stay. The long feature checklists are replaced
with Build the Brand / Build the House / Run the House. No pricing implied.

### Portfolio
- **Removed:** Cowtown Tour Company, MLK Pre Arrangements (Ride & Share only —
  MMM did not build those sites), FBI Network
- **Added:** 9-Line Financial → 9-lf.com

### NEW — "I Came Up In Broadcast"
Univision, CBS 11, Radio Intelligence brought forward. Photo + Philippians 1:6.

### NEW — Ride & Share video wall
All four episodes: Lena, Carrie, Yoel, Susy. Thumbnails pull live from YouTube,
so re-uploading a video updates the site automatically.

### NEW — Client reviews
Two real Google reviews, verbatim (Yoel Zehaie, 4TEC LLC).
Carrie, Lena and Tony are **commented out** in the HTML — uncomment each as
the real words arrive. Empty placeholder cards were advertising what's missing.

### NEW — Booking card + Free Assessment modal
- Every "Book a Call" → `calendar.app.google/7EeEp5VeZZvSwdrE6`
- Every "Free Assessment" → modal form, posts to the same Formspree endpoint
- Closes on X, click-outside, or Escape

### Footer
Social icons added (Facebook, Instagram, LinkedIn, YouTube), phone and email.

### Details
- Phone → **682-484-1335** everywhere (was 817-860-8989)
- GA4 → **G-TD5J4DJ1WB** (was a placeholder — it was never tracking)

---

## Still outstanding

1. **info@megamissionmedia.com** — using susy@ for now, as agreed
2. **Footer scripture** — the Matthew line, when it comes to you
3. **New MMM YouTube IDs** — six places, once you've re-uploaded
4. **YouTube Follow link** — currently the playlist, wants the channel URL
5. **Carrie / Lena / Tony reviews** — uncomment as they arrive
6. **Logo** — MMM_Logo.png is still the gold version against a teal palette

## Verify after deploy
- Open the live site on your phone, then check GA4 **Realtime** — you should
  appear as an active user
- Click Book a Call, make a test booking, confirm it lands on your calendar,
  then delete it
- Submit the Free Assessment modal once and confirm it reaches your inbox

---

# Round 2 — Logo, favicon, nav

## New logo files
| File | Use |
|---|---|
| `mmm-logo-tile-simple.png` | Nav bar (black tile, cyan mark) |
| `mmm-mark-simple.png` | Transparent, no tile — for dark backgrounds |
| `favicon.ico`, `favicon-16/32/48.png` | Browser tabs |
| `favicon-180.png` | Apple touch icon |
| `favicon-192/512.png` | Android |

**Two versions of the mark exist on purpose.** The ChatGPT original has ~23 thin
bars — beautiful at full size, unreadable at 48px, which is exactly the size it
runs in your own nav. The simplified 7-bar version is what's wired in. Same
idea, survives being small. Use the detailed one for large-format only.

These are still raster. For print and true scaling, have Cheshire redraw as vector.

## Nav rebuilt — three distinct actions
- **Top strip (black):** social icons + **Call Us Directly** → phone
- **Book a Call** (solid) → Google calendar
- **Get in Touch** (outline) → Free Assessment form modal

No more duplicate CTAs. Each button goes somewhere different.

## Nav is now white
Black top strip → white nav bar → cyan ticker → black hero.
Active nav item underlines in deep teal.

## Fixed
- Gold nav button (the yellow that was bugging you) — gone
- "ON AIR" dot and text were still orange — now teal
- Favicon: there wasn't one at all before

## Add to your repo
All `favicon-*.png`, `favicon.ico`, `mmm-logo-tile-simple.png`,
`mmm-mark-simple.png` go in the **same folder as index.html**.
`MMM_Logo.png` is no longer referenced — safe to delete.

---

# Round 3 — Hero, phone number, nav

## Phone number: 817-860-8989 everywhere
Nav, footer, contact note, form error messages. Matches your Google Business
Profile, which is what Google cross-references.

**Keep 682 as your cold-dialing number and never publish it.** Cold calling
burns a number — enough unanswered calls to strangers and carriers start
flagging it "Spam Likely." You do not want that happening to the number on
your Business Profile. Say the 817 out loud on calls, and forward 682 → 817.

## Hero
- Device mockup: **laptop = 4TEC website, tablet = 4TEC campaign graphic,
  phone = 9-LF mobile.** Real screenshots, no AI-generated fake interfaces.
- **Book a Call** (solid) and **Get in Touch** (outline) sit under the headline
- Caption changed: "Faith-Based Media Network" → "Branding · Websites · Video ·
  Back Office" — says what you sell

## Nav
- Socials moved to the **right** of the black top strip; phone number removed
- Single **Book a Call** button in the white bar

## Files to add
`hero-devices.png` and `hero-devices.webp` go alongside index.html.

## To swap a device screen later
The mockup is a flat image. Send new screenshots and I'll rebuild it — the
tablet is the obvious slot for Yoel's site or Tony's desktop view.
