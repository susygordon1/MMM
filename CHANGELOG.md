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

---

# Round 4 — Hero bumpers + three clients in the mockup

## Mockup now shows three different clients
- **Laptop** — 4TEC Electric website
- **Tablet** — 9-Line Financial
- **Phone** — Zehaie Law / Call Yoel Now

The 4TEC campaign flyer came out. You were right: it's a flyer, not a website,
and putting it in a tablet frame implied it was one. It belongs in the portfolio
as branding work instead.

Three devices, three clients — reads as "this happens repeatedly," not "I built
one website."

## Hero bumpers
Nav, top strip, and hero now share one centred 1360px container with 5vw side
padding. Headline pulls right, devices pull left, dead space in the middle
closes up. Nothing runs edge-to-edge except the ticker, which should.

## To swap a device later
Send a new screenshot and say which device. Laptop wants ~4:3 desktop,
tablet ~4:3 narrower, phone from your actual phone.

---

# Round 5 — Form wiring confirmed

## Both forms already point to Formspree xgawvlvb
Verified: the Free Assessment modal and the Send Us A Message form both POST to
`https://formspree.io/f/xgawvlvb`.

**If the modal looked like it wasn't sending, that's because of local testing.**
Formspree rejects submissions from a `file://` page — it only accepts them from
the real domain. Test after deploy, not before.

## Added: form labelling
Every submission now carries a hidden `_subject` and `form_source` so you can
tell at a glance which form someone used:

| Form | Subject line in your inbox |
|---|---|
| Free Assessment modal | Free Assessment Request — megamissionmedia.com |
| Contact section | Contact Form — megamissionmedia.com |

This matters for the cold-call campaign — Free Assessment submissions are warm
leads who clicked a specific offer.

## Error messages now give a second route
Was: "Something went wrong."
Now: "That didn't send. Please call 817-860-8989 or email susy@megamissionmedia.com."

## Test after deploy
Submit both forms once on the live site. Confirm two emails arrive with
different subject lines. Formspree may ask you to confirm the endpoint the
first time.

---

# Round 6 — Ticker moved and rebuilt

## Ticker now sits BELOW the hero
It was above the hero, squeezed between the nav and the headline. Now it closes
the hero and opens the next block — which is what makes it feel like a divider
instead of decoration.

## Logo mark embedded in the ticker
`mmm-mark-ink.png` — a dark version of your waveform mark, since the ticker is
cyan and the cyan mark would vanish. Sits between each phrase.

## New ticker copy
Your Vision. Our Mission. · Branding · Digital Presence · Video & Podcasting ·
Back Office Support · Fort Worth, Texas

"Faith-Based Media Network" is gone. The phrases now name what you sell.
Easy to edit — they're plain `<span>` tags in the ticker div.

## Fixed: unclosed div
The `.hero-inner` wrapper added in Round 4 was never closed. Browsers
auto-corrected it so nothing looked broken, but it was invalid HTML and would
have caused trouble later. Closed properly now.

## New file
`mmm-mark-ink.png` goes alongside index.html.

---

# Round 7 — Meet The Owner rebuilt

Section went from dark to light and textured, laid out like the reference:
photo left in a white mat frame, copy right, signature at the bottom.

## What's new
- **Paper texture background** (`texture-paper.jpg`) — subtle plaster grain,
  3KB, generated not stock
- **Watermark** — your waveform mark at 2.8% opacity behind the copy. Hidden on
  mobile where it just crowded the text.
- **Photo frame** — white mat with a thin teal inner rule, drop shadow
- **Signature** — "Susy Gordon" in Great Vibes, self-hosted (`fonts/great-vibes-latin-400-normal.woff2`)
- **Heading** — "MEET **THE OWNER**", two-tone, matching the reference
- Broadcast credential tags kept: Univision · CBS 11 · Radio Intelligence ·
  25+ Years Corporate

## About that signature
It's a script typeface rendering of your name, not a scan of your handwriting.
Standard practice for a website sign-off. **Don't use it as an actual
signature on anything legal** — for that you'd sign or use a real e-signature.

## What I did NOT add
The reference has a "TOP TIER BRANDS — GUARANTEED" seal in the corner. I left
it off. Award badges you haven't been given are the kind of thing a prospect
can check, and one that doesn't hold up costs more than the badge gains.

## New files
`texture-paper.jpg`, `fonts/great-vibes-latin-400-normal.woff2`
